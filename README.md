# Vision-Acoustic-Emission-with-Mixed-Attention-model

## Mixed attention fusion model
The core of this method involves a hybrid attention model that combines self-attention and cross-attention mechanisms. These are essential for fusing multi-modal data (images and AE features).

### Inter-model self-attention
Visual branching: Capturing local-global dependencies of cracked regions through spatial self-attention, focusing on key visual features such as edges and textures.
Acoustic emission branching: Using time self-attention to model the timing of parameter changes (such as energy surges, frequency shifts, etc.) during crack propagation.

### Between-model cross attention
Visual guided AE: The AE events corresponding to the crack image region are located using the visual feature as the query (Q) and the AE feature as the key-value pair (K/V).
Acoustic emission enhanced vision: Acoustic emission timing features are used as queries, and visual features are used as key-value pairs to enhance crack regions associated with acoustic emission signals in the image.

## Dataset
The experimental data utilized in this study was sourced from collaborative research institutions and consist of two distinct types of samples, which play crucial and complementary roles in the subsequent analysis. The link to the image dataset is https://pan.baidu.com/s/1TARaEfPsAvXVOQxj_3Z-dg?pwd=g86i.

The diameter of the rivet hole is 5mm. In the experiments at the Cooperative Institute, the AE sensor spacing was set to 130mm, where the centers of sensor 1 and sensor 2 were 90mm from each end of the test piece. The waveform flow data obtained in the experiment only retained the information from 30 minutes before the crack initiation to the fracture of the test piece, and the image data of the test piece during this period were recorded. The loading conditions were in the form of sinusoidal curves with a maximum load of 17kN and a minimum load of 1.7kN, a frequency of 5Hz, a gripping force of 90bar. A crack appeared on the right side of the opening of the test piece. The test started at 9:32, and the experimental process experienced several pauses and continuations, including acoustic emission acquisition and zeroing of the test machine, etc. The crack length and the number of cycles were recorded. The test piece began to crack 11 hours and 25 minutes after the start of the experiment, and broke 1 hour and 1 minute after the crack appeared, and the number of cycles at the time of fracture was 86,510. A total of 1795 images were recorded, including 755 defect-free images and 1040 defective images. After removing the data from the zeroing process of the tester, a total of 1755 aircraft crack image datasets were formed. This dataset was meticulously categorized into 714 non-defective images and 1041 defective images. Each image has a high resolution of 5472×3648 pixels, enabling the capture of fine-grained details. Significantly, these images cover the entire spectrum of the crack development process, from the initial stage of crack initiation to the final stage of specimen fracture.
