# Peace Deal Mechanics

Peace Deal Mechanics adds negotiated mid-war settlements to Hearts of Iron IV without waiting for total capitulation.

Peace Deal Mechanics lets countries propose limited mid-war settlements based on the current balance of the war. You can demand states, offer concessions, impose war reparations, disarm the enemy, create puppets, or return territory. If the proposal is accepted, the war ends with a truce instead of pushing every conflict all the way to annexation.

**Version:** 1.0.0 | **HOI4:** 1.17.4.1+ | **DLC Required:** None

---

## What changes in your game

- Wars can end through negotiated settlements instead of only total victory or scripted white peace.
- Winning countries can demand territory and punitive terms without going all the way to a peace conference.
- Losing countries can offer negotiated settlement packages to preserve part of their state instead of fighting to total collapse.
- AI countries now use the system on their own with conservative target selection and conservative deal-building logic.

---

## Features

- Mid-war peace deal diplomatic action
- Demand terms from the enemy or offer terms as a negotiated settlement
- State-by-state terms for taking states, giving states, creating puppet states, demilitarizing territory, and liberating or returning land
- Punitive terms through war reparations and forced disarmament
- War-score-based cost system
- AI-generated peace offers and concessions
- Conservative AI target selection with narrow puppet demands in obvious cases
- Rebuilt AI acceptance that weighs war pressure, proposal terms, and geopolitics instead of defaulting to blanket refusal
- Three small game rules for system availability, AI participation, and AI acceptance stance
- Separate peace support with follow-up truce handling
- Vanilla conditional surrender disabled so Peace Deal Mechanics is the only visible mid-war peace path
- Optional Ceasefire Mechanics integration so active ceasefires can be converted into permanent peace cleanly

---

## How it works

Peace deals are built from a custom diplomatic action available against countries you are currently fighting. The proposal uses a war-score-style budget tracked between each pair of enemies. Expensive territorial demands consume more score, while concessions refund score when you are offering peace from a weaker position.

If the proposal is accepted, the mod executes a negotiated settlement immediately:

- the relevant war relation is ended with white peace
- a truce is applied
- selected states are transferred, liberated, or puppeted
- optional reparations and disarmament effects are applied

For AI countries, peace offers are intentionally conservative. They pick the strongest valid target they can negotiate with, then prioritize obvious cores, claims, and clean liberation cases before adding harsher extras like reparations, disarmament, or narrow puppet demands in clear single-tag cases.

The vanilla conditional surrender path is disabled so it does not compete with or clutter the diplomacy view while this mod is active.

---

## Compatibility

This mod has no hard dependencies.

If used together with **Ceasefire Mechanics**, Peace Deal Mechanics auto-detects active ceasefires with the target side, builds terms from the ceasefire map state, and ends the ceasefire through the Ceasefire API before applying permanent peace. That cleanup respects the ceasefire mod's territory handling and keeps the integration optional and non-invasive when the ceasefire mod is absent.

---

## Load order

No special load order is required in vanilla use.

If you use this together with large diplomacy-overhaul mods, load Peace Deal Mechanics after them if they also replace the same diplomatic action files or GUI definitions.
