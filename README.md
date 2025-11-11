## Model Overview

- **LLaMA‑3 8B (text-only)** – initial agent that reasoned purely over textual descriptions of the arena.

Each step, a custom wrapper turns the state into text (position, heading, goal bearing, obstacles/boundary, predator).

The prompt also includes feedback about the last action (whether the position changed and the current “stuck” streak) plus a discrete action menu.
The model responds in a structured format:

ACTION: [0–6] 

THOUGHT: [brief reasoning]

Known issue: The agent often gets stuck or oscillates near obstacles/boundaries, but can still just about complete the task in some runs.

- **GLM‑4.1V 9B Thinking (vision-language)** – follow-up agent with the same parameter scale but direct visual grounding on rendered frames.

Vision‑language agent that selects the next absolute target (x, y) from a top‑down arena image; we then execute one step toward that point.

Model output must be:
move: [{"x": <float>, "y": <float>}]
thoughts: "<one‑line strategy>"

Reported to be competitive with, and in some cases stronger than, GPT‑4o for spatial planning; 

## Episode GIF Gallery

### Episodes 1 – 6 · Baseline (circular icons)
<table>
  <tr>
    <td><img src="gif/episode_1.gif" width="180"><br>Episode 1</td>
    <td><img src="gif/episode_2.gif" width="180"><br>Episode 2</td>
    <td><img src="gif/episode_3.gif" width="180"><br>Episode 3</td>
    <td><img src="gif/episode_4.gif" width="180"><br>Episode 4</td>
  </tr>
  <tr>
    <td><img src="gif/episode_5.gif" width="180"><br>Episode 5</td>
    <td><img src="gif/episode_6.gif" width="180"><br>Episode 6</td>
    <td></td>
    <td></td>
  </tr>
</table>

### Episodes 10 – 20 · Shape-Differentiated Legends
<table>
  <tr>
    <td><img src="gif/episode_10.gif" width="180"><br>Episode 10</td>
    <td><img src="gif/episode_11.gif" width="180"><br>Episode 11</td>
    <td><img src="gif/episode_12.gif" width="180"><br>Episode 12</td>
    <td><img src="gif/episode_13.gif" width="180"><br>Episode 13</td>
  </tr>
  <tr>
    <td><img src="gif/episode_14.gif" width="180"><br>Episode 14</td>
    <td><img src="gif/episode_15.gif" width="180"><br>Episode 15</td>
    <td><img src="gif/episode_16.gif" width="180"><br>Episode 16</td>
    <td><img src="gif/episode_17.gif" width="180"><br>Episode 17</td>
  </tr>
  <tr>
    <td><img src="gif/episode_18.gif" width="180"><br>Episode 18</td>
    <td><img src="gif/episode_19.gif" width="180"><br>Episode 19</td>
    <td><img src="gif/episode_20.gif" width="180"><br>Episode 20</td>
    <td></td>
  </tr>
</table>

### Episodes 30 – 39 · Clustered Map Experiments
<table>
  <tr>
    <td><img src="gif/episode_30.gif" width="180"><br>Episode 30</td>
    <td><img src="gif/episode_31.gif" width="180"><br>Episode 31</td>
    <td><img src="gif/episode_32.gif" width="180"><br>Episode 32</td>
    <td><img src="gif/episode_33.gif" width="180"><br>Episode 33</td>
  </tr>
  <tr>
    <td><img src="gif/episode_34.gif" width="180"><br>Episode 34</td>
    <td><img src="gif/episode_35.gif" width="180"><br>Episode 35</td>
    <td><img src="gif/episode_36.gif" width="180"><br>Episode 36</td>
    <td><img src="gif/episode_37.gif" width="180"><br>Episode 37</td>
  </tr>
  <tr>
    <td><img src="gif/episode_38.gif" width="180"><br>Episode 38</td>
    <td><img src="gif/episode_39.gif" width="180"><br>Episode 39</td>
    <td></td>
    <td></td>
  </tr>
</table>
