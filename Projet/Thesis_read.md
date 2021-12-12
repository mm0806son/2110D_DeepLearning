## Realtime Multi-Person 2D Pose Estimation using Part Affinity Fields

**Achievement**: placed first in the inaugural COCO 2016 keypoints challenge, and significantly exceeds the previous state-of-the-art result on the MPII Multi-Person benchmark, both in performance and efficiency.

### State of art

Inferring the pose of multiple people in images, especially socially engaged individuals, presents a unique set of challenges:

- An unknown number of people that can occur at any position or scale
- Interactions between people induce complex spatial interference, due to contact, occlusion, and limb articulations, making association of parts difficult
- Runtime complexity tends to grow with the number of people in the image, making real-time performance a challenge

**Top-down approaches**: person detector + single-person pose estimation -> Inconvenience:

- If the person detector fails when people are in close proximity, there is no recourse to recovery
- Run time is proportional to the number of people

**Bottom-up approach** such as jointly labeled part detection candidates and associated them to individual people -> Inconvenience:

- Average processing time = minutes~hours

The network is split into two branches: the top branch, shown in beige, predicts the confidence maps, and the bottom branch, shown in blue, predicts the affinity fields.



**Part Affinity Fields (PAFs)**: a set of 2D vector fields that encode the location and orientation of limbs over the image domain


