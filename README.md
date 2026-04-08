radar-camera-bev-evaluation
Comparative evaluation of mmWave radar and depth camera Bird's Eye View (BEV) occupancy grids against hand-measured ground truth in a controlled indoor environment.
#What This Project Does
Both sensors observe the same static indoor scene (a narrow hallway with obstacles). Each sensor produces a binary occupancy grid — a top-down map where each cell is either "occupied" or "free". This project evaluates how accurately each sensor reconstructs the scene by comparing its occupancy grid against ground truth measurements.
Sensors
SensorModelKey SpecsRadarTI xWR68xx AOP3TX × 4RX, 12 virtual antennas, Capon/Bartlett beamforming, 0.044m range resolutionCameraIntel RealSense D455848×480 depth, 86° FOV, stereo IR + active IR projector
Scenes
3 scenes × 2 lighting conditions (light/dark). Camera additionally has 2 device conditions (with/without IR projector).
SceneDescription1Object (suitcase) only2Mirror only3Mirror + object
Room: 122cm wide hallway, sensor 55cm from left wall, front wall at 201cm.
Evaluation Metrics
Grid-level (how well does the occupancy grid match ground truth):

IoU, Precision, Recall, F1

Cluster-level (how well are individual obstacles localized):

Hungarian centroid matching
OSPA distance (Schuhmacher et al., 2008)
