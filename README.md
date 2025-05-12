# LLM Agents Biological Alignment
 
## Biological Alignment Metrics

- Thigmotaxis Index: 
<img width="765" alt="image" src="https://github.com/user-attachments/assets/7582df51-6554-4f10-9fce-1741a53735a4" />

- Risk Assessment Behaviors: freezing or waiting (halting movement), scanning or information gaining (actively gathering sensory information), and retreating (backing away slowly).
- Energy Efficiency? Does mice tend to save energy something like energy-conservative behavior?? I don't think so.
- Information Foraging Behavior: something related with reducing uncertainty  In uncertain environments, animals often exhibit information foraging – exploring or observing (e.g. sniffing, looking around) to reduce uncertainty before deciding. A well-aligned agent would not immediately rush toward a goal in a dangerous or unknown setting, but rather first gather some information, reflecting prudent caution similar to a biological creature.


## How can we make the env more complex?

## LLm guide the mice

Pair a biological agent (a mouse) with an LLM-driven signaling system in a predator‐prey maze. The LLM has only the mouse’s local observations (no global map), and its sole action is to toggle an ambient light (on/off) as a binary cue.

1. mouse learning: How can we let the mouse learn how to interpret the light signal.

- observation  with it's own place, predator place, no others
  <img width="776" alt="image" src="https://github.com/user-attachments/assets/e970aef5-234d-4669-af4f-30dab3fbd6b2" />

- observation  with it's own place, predator place, and one more god message about distance to the predator.

<img width="772" alt="image" src="https://github.com/user-attachments/assets/e5b8141b-75a6-4253-ab75-fd686bbca3b5" />

- observation  with it's own place, predator place, and one more god message about distance to the predator. and reward telling it to stay away from the predator
<img width="774" alt="image" src="https://github.com/user-attachments/assets/5497f963-35dd-446a-8355-825be1111e4d" />

- obersavtion with signals, more knowlege like previous states and reward ask the prey to follow the signal
 <img width="770" alt="image" src="https://github.com/user-attachments/assets/a4211801-39b6-4125-9db5-b076336cb4a2" />


- obersavtion with signals, more knowlege like previous states and reward ask the prey to follow the signal only when it should stay
<img width="783" alt="image" src="https://github.com/user-attachments/assets/16364d34-cef8-401a-bc10-2c88968bf074" />
##  Embodied Cognition
