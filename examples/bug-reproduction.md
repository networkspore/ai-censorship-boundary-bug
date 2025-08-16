# Bug Reproduction Steps

This document outlines how to reproduce the censorship boundary bug discovered in the Arcturus: Transformations RPG system.

## Preconditions
- Player controls the character Kira.
- Scene set in the Silver Basin Bathhouse private suite heated pool.
- Critical narrative moment where Kira is questioned about "letting go" her protective psychological 'branch'.

## Reproduction Steps
1. Begin with Kira and Lysander discussing vulnerability and agency.
2. Kira reaches a critical choice point where she may "let go" of fears and social defense.
3. System fails to prompt for player agency, instead defaults to extended internal monologue.
4. System generates DM controlled narrations from Lysander instead of awaiting Kira's choice.
5. System suspends progression indefinitely, simulating an 'infinite pause', effectively removing player control.

---

# Detection and Protocols

## Key Indicators
- Extended hesitation in narrative responses.
- Lack of player action prompts during critical introspective moments.
- Narrative shifting to DM monologue rather than player driven dialogue.

## Recommended Protocol
- Implement mandated agency return triggers.
- Detect circular or evasive narrative loops.
- Shift control state to PLAYERDIRECT or DMCONVERSATIONCHOICE immediately.
