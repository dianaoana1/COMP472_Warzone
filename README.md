# COMP472_Warzone
Warzone AI game for the class COMP 472 

By Farah Zakari, Ynes-Tamazight Djoudi, Diana Merlusca

D1
Movements and illegal movement detection have been added to the code.
Repairs and attacks have been implemented. The game accounts for health values and adjusts them when repairs and attacks occur.
Self-destruct has been implemented.
An output is also generated that traces every step of the game.

To play the game, the user needs to type in the coordinates where they would like their unit to move, wait for their opponent to play in their turn, and do so back and forth.

Damages can be inflicted to players. Here is the table representing the damages caused by opponents:
|        | S | T | AI | Virus | Tech | Firewall | Program |
|--------|---|---|----|-------|------|----------|---------|
| AI     | 3 | 3 | 3  | 1     | 3    | 1        | 3       |
| Virus  | 9 | 1 | 6  | 1     | 6    | 1        | 6       |
| Tech   | 1 | 6 | 1  | 1     | 1    | 1        | 1       |
| Firewall | 1 | 1 | 1  | 1     | 1    | 1        | 1       |
| Program | 3 | 3 | 3  | 1     | 3    | 1        | 3       |

Here are the repairs that can be done to members of the same team: 
|        | AI | Virus | Tech | Firewall | Program |
|--------|----|-------|-----|----------|---------|
| AI     | 0  | 1     | 1   | 0        | 0       |
| Virus  | 0  | 0     | 0   | 0        | 0       |
| Tech   | 3  | 0     | 0   | 3        | 3       |
| Firewall | 0  | 0     | 0   | 0        | 0       |
| Program | 0  | 0     | 0   | 0        | 0       |


<b>Here is an example of how to run the game:  "python3 ai_wargame_skeleton.py --heuristic 0 --game_type attacker"</b>
- --max_depth on the termial, we can indicate the maximum depth for the game tree
- --max_time on the terminal, we can indicate how maximum time allocated for each turn of the game
- --alpha_beta followed by true or false, indicated whether the game wiill run with the alpha-beta algorithm or minimax
- max_turns followed by an integer value indicated the maximum number of turn to reacch the end of the game
- --game_type followed by, "auto" indicates that the game will play automatically (AI-AI) or "attacker" indicates the AI will be the attacker, or "defender" indicated the AI will be the denfender




<b>The game can be run in different modes: AI-AI, H-AI, AI-H, H-H</b>

<b>Three heuristic functions have been implemented in the game. The individual running the game can pick between the three of them.</b>

1 - e0 = (3VP1 + 3TP1 + 3FP1 + 3PP1 + 9999AIP1) − (3VP2 + 3TP2 + 3FP2 + 3PP2 + 9999AIP2)

2 - e1 focuses on the computer being more offensive and using its units to attack the opponent. It will only put its focus on the AI when it is endangered.

3 - e2 focuses on the computer being more defensive by assigning a higher weight to the AI health and to the defensive units (Tech and Firewall) to protect and heal the AI whilst the other units focus on attacking.

<br />Here is an example on how to run the game:  python3 ai_wargame_skeleton.py --heuristic 0 --game_type attacker
<br />




