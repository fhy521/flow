# Related SUMO and RL Repositories for Task23

This note collects external repositories that are useful references for SUMO-based reinforcement learning work around ramp merging, lane changing, safety constraints, and highway bottleneck control. Repository URLs were checked on 2026-04-23. Star counts are intentionally omitted because they become stale quickly.

## Most Relevant First

| Repository | Main topic | Why it matters for Task23 |
| --- | --- | --- |
| [jlubars/RL-MPC-LaneMerging](https://github.com/jlubars/RL-MPC-LaneMerging) | RL + MPC for on-ramp merging | Useful for studying how learned decisions can be combined with model-based and controllable constraints instead of learning raw actions only. |
| [Bill-Bi/RL_ramp_merging](https://github.com/Bill-Bi/RL_ramp_merging) | Safety-driven deep RL for cooperative ramp merging | Relevant for cooperative merging, safety-oriented features, Ray-based training, and Flow/SUMO integration ideas. |
| [TMIS-Turbo/OARL](https://github.com/TMIS-Turbo/OARL) | Observation-adversarial RL for robust lane-change decisions | Directly relevant to robust lane-change decision making in randomized mixed highway traffic. |
| [federicovergallo/SUMO-changing-lane-agent](https://github.com/federicovergallo/SUMO-changing-lane-agent) | SUMO lane-changing agent with custom Gym environment | A practical lane-change example using DQN and A2C in dense traffic; useful for state, action, reward, and training-script structure. |
| [Ilhem23/change_lane_DQN](https://github.com/Ilhem23/change_lane_DQN) | Single-vehicle lane-change DQN with SUMO + TraCI | Clean task definition with left, right, and keep-lane actions; good for quickly comparing state/action/reward design. |
| [rram12/Lane-Change-Assistance-System](https://github.com/rram12/Lane-Change-Assistance-System) | DDQN with rule-based lane-change constraints | Useful when combining high-level RL decisions with low-level safety or feasibility filters. |

## Frameworks and Base Platforms

| Repository | Main topic | Why it matters for Task23 |
| --- | --- | --- |
| [flow-project/flow](https://github.com/flow-project/flow) | Deep RL framework for traffic microsimulation | Classic SUMO + RL base framework for mixed-autonomy traffic, custom merge scenarios, bottlenecks, and network-level experiments. |
| [seawee1/driver-dojo](https://github.com/seawee1/driver-dojo) | General SUMO-based autonomous driving RL benchmark | Useful for thinking about task, traffic, and network randomization and generalization. |
| [COeXISTENCE-PROJECT/RouteRL](https://github.com/COeXISTENCE-PROJECT/RouteRL) | MARL route-choice framework with SUMO | More relevant for future network-level collective route-choice extensions than for immediate lane-level control. |

## Roadside Control and Highway Bottleneck References

| Repository | Main topic | Why it matters for Task23 |
| --- | --- | --- |
| [Kaimaoge/SUMO-DVSL](https://github.com/Kaimaoge/SUMO-DVSL) | DDPG / actor-critic differential variable speed limit control | Useful as a non-traffic-light SUMO + RL reference for freeway recurrent bottleneck control. |
| [YuHan-Research-Group-SEU/Deep-Reinforcement-Learning-Network-for-Highway-Ramp-Metering](https://github.com/YuHan-Research-Group-SEU/Deep-Reinforcement-Learning-Network-for-Highway-Ramp-Metering) | TD3-based highway ramp metering with SUMO | Close to merging bottleneck problems from the roadside-control side; useful for training, testing, and transferability workflows. |
| [kkusic/Multi_Agent_Based_Spatio_Temporal_Variable_Speed_Limit](https://github.com/kkusic/Multi_Agent_Based_Spatio_Temporal_Variable_Speed_Limit) | Multi-agent variable speed limit control | Useful for MARL implementation patterns in upstream freeway bottleneck control. |

## Smaller But On-Topic Cooperative Lane-Change Work

| Repository | Main topic | Why it matters for Task23 |
| --- | --- | --- |
| [NetworkCommunication/LCOMCCV](https://github.com/NetworkCommunication/LCOMCCV) | Cooperative overtaking and lane changing in mixed connected traffic | On-topic for cooperative lane change and overtaking, including mixed connected and non-connected vehicle settings. |

## Suggested Reading Order

1. Start with `jlubars/RL-MPC-LaneMerging`, `Bill-Bi/RL_ramp_merging`, and `rram12/Lane-Change-Assistance-System` if the current pain point is safety constraints around RL decisions.
2. Read `federicovergallo/SUMO-changing-lane-agent` and `Ilhem23/change_lane_DQN` if the immediate pain point is state/action/reward wiring in a simpler SUMO lane-change setup.
3. Use `TMIS-Turbo/OARL` when robustness and observation noise become central.
4. Keep the roadside-control repositories as comparison material for bottleneck mitigation, TD3/DDPG training loops, and multi-agent control structure.
