
-- 55500001.lua (Greed Lizard)
local s,id=Get  ID()
function s.initial_effect(c)
	-- This defines the "if Normal/Special Summoned" effect
	local e1=Effect.CreateEffect(c)
	e1:SetDescription(aux.Stringid(id,0)) -- Sets the prompt text
	e1:SetCategory(CATEGORY_DRAW)
	e1:SetType(EFFECT_TYPE_SINGLE+EFFECT_TYPE_TRIGGER_O) -- Trigger effect, Optional
	e1:SetProperty(EFFECT_FLAG_DELAY)
	e1:SetCode(EVENT_SPSUMMON+EVENT_SUMMON) -- Triggers on Special and Normal Summon
	e1:SetCountLimit(1,id) -- Once per turn
	e1:SetTarget(s.target)
	e1:SetOperation(s.operation)
	c:RegisterEffect(e1)
end

-- Target function (Checks if the player has a hand to shuffle)
function s.target(e,tp,eg,ep,ev,re,r,rp,chk)
	if chk then
		return Duel.GetFieldGroupCount(tp,LOCATION_HAND,0)>0
	end
	Duel.SetOperationInfo(0,CATEGORY_TODECK,nil,1,tp,LOCATION_HAND) -- Info for the card to be returned
	Duel.SetOperationInfo(0,CATEGORY_DRAW,nil,0,tp,1) -- Info for the draw
end

-- Operation function (What happens when the effect resolves)
function s.operation(e,tp,eg,ep,ev,re,r,rp)
	Duel.Hint(HINT_SELECTMSG,tp,HINTMSG_TODECK)
	-- Selects the card to shuffle back
	local g=Duel.SelectMatchingCard(tp,s.todeckfilter,tp,LOCATION_HAND,0,1,1,nil)
	if g:GetCount()>0 then
		Duel.SendtoDeck(g,nil,SEQ_DECKSHUFFLE,REASON_EFFECT)
		-- Draws 1 card
		Duel.Draw(tp,1,REASON_EFFECT)
	end
end
-- Simple filter: any card in the hand
function s.todeckfilter(c)
	return true
end
