# Introduction to Embodied AI

## Definition
- Integration of AI in physical entities capable of interacting with the physical world.
- Emphasizes interaction with the real environment surrounding us.

## Significance
- Essential for advancing towards Artificial General Intelligence (AGI).
- AGI would have the ability to perform any cognitive task that a human can, across different domains.
- Enables complex interactions and decisions in real-world settings, beyond digital computation.

## Language and Vision Integration
- **Large Language Models (LLMs)**: Process linguistic instructions from humans.
- **Multi-modal Large Models (MLMs)**: Handle visual and linguistic outputs.

## Technological Foundations and Innovations

### Multi-modal Large Models (MLMs)
- Enhance perception and interaction abilities through visual and linguistic outputs.
- **Examples**: CLIP, which combines vision and language understanding.

### World Models (WMs)
- Build cohesive understanding by integrating sensory data from multiple sources.
- Understand, predict, then interact with the physical world.
- Facilitate sophisticated environmental interactions.

### Advanced Neural Networks
- Process multi-source sensory data to create a cohesive understanding of the environment.
- **Sensory data**: Includes tactile (touch), sound, vision, etc.
- Improve real-time decision-making and adaptability.

## Critical Areas of Research and Development

### Embodied Perception

#### Techniques
- Advanced sensing and data processing for better environmental interpretation.
- Combining state estimation, scene perception, and environment exploration.

#### Key Components

##### Visual Simultaneous Localization and Mapping (vSLAM)
- Maps environment and tracks location using visual inputs from cameras.
- **Types**: Traditional vSLAM (e.g., MonoSLAM, ORB-SLAM) and Semantic vSLAM (e.g., SLAM++, DS-SLAM).

##### 3D Scene Understanding
- Interprets complex 3D environments for navigation and interaction.
- Unlike 2D, considering Depth, perspective, and physical properties.
- **Sensors**: Lidar, RGB-d camera.
- **Techniques**:
  - Projection-based (e.g., MV3D, PointPillars)
  - Voxel-based (e.g., VoxNet, MinkowskiNet)
  - Point-based (e.g., PointNet, PointNet++).

#### Active Exploration
- Robots actively explore environments, acquiring information and making decisions dynamically.
- **Techniques**: Reinforcement learning, mapless planning frameworks (e.g., NeU-NBV).

### Tactile Perception

#### Sensor Types and Their Applications
- **Non-Vision-Based Sensors (BioTac)**: Capture tactile properties such as force and location. Applications include healthcare and delicate object manipulation.
- **Vision-Based Sensors (GelSight, DIGIT)**: Utilize visual information about deformations to provide detailed texture, shape, and force data. Applications include assembling delicate components and identifying objects based on surface properties.
- **Multi-modal Tactile Sensors**: Combine pressure, proximity, acceleration, and temperature information. Applications include enhanced human-computer interaction.

#### Datasets for Tactile Sensing
- **Diversity in Object Types**: Ranges from daily necessities to specific materials like clothing, providing tactile and associated visual/audio data tailored for distinct scenarios.
- **Real vs. Simulated Environments**: Real datasets mimic real-world conditions for practical testing, while simulated datasets allow controlled testing and scalability.
- **Continuous vs. Non-Continuous Data**: Continuous data streams are vital for dynamic interactions requiring ongoing feedback, while non-continuous data is used in static, controlled tasks.

#### Tactile Perception Tasks
- **Estimation**: Estimate object properties like shape and force based on tactile data. Generate tactile images from non-tactile data (like vision) and reconstruct tactile properties.
- **Robotic Manipulation**: Inform and improve the precision of robotic manipulations. Techniques include reinforcement learning and GANs.
- **Multi-Modal Recognition**: Leverage tactile data alongside visual and audio inputs for comprehensive object recognition.

### Embodied Interaction

#### Development of AI Systems
- AI systems that can physically interact with their environment and humans.
- **Examples**: AI-driven robotic arms and humanoid robots.

#### Agent Behavior
- Autonomous behaviors allowing agents to perform complex tasks independently.
- Exploration of decision-making algorithms and adaptability in various scenarios.

#### Sim-to-Real Applications
- Address the challenge of translating behaviors learned in simulated environments to real-world applications.
- **Techniques**: Domain adaptation, domain randomization.

### End-to-End and Modular Approaches for Embodied Interaction

#### End-to-End Approaches
- **CLIPORT**: Combines CLIP with Transporter Net for semantic understanding and grasp generation from expert demonstrations and image-text pairs.
- **Reasoning Grasping Models**: Utilize multimodal LLMs integrated with vision-based robotic frameworks to generate grasps based on semantic and visual cues.

#### Modular Approaches
- Decomposing bigger tasks into smaller tasks → independent module design.
- **F3RM**: Elevates text-image priors into 3D space for language localization and grasp generation.
- **GaussianGrasper**: Uses a 3D Gaussian field for precise geometry and language-guided task execution.

## Embodied Agent

### Definition
- An agent is an autonomous entity capable of perceiving its environment and acting to achieve specific objectives.
- Recent advancements in Multi-modal Large Models (MLMs) have expanded the application of agents to practical scenarios.
- When embodied in physical entities, these MLM-based agents can effectively transfer capabilities from virtual space to the physical world, becoming embodied agents.

### Key Processes

#### High-Level Embodied Task Planning
- Decomposing abstract and complex tasks into specific subtasks.
- **Example**: Breaking down a task like "put an apple on a plate" into subtasks such as "find the apple," "pick the apple," and "find the plate."

#### Low-Level Embodied Action Planning
- Gradually implementing these subtasks by utilizing Embodied Perception and Interaction models or leveraging the Foundation Model’s policy function.
- Action planning involves interaction with the environment and adjusting task planning based on feedback.

### Embodied Multimodal Foundation Model
- Required to integrate multiple sensory modalities and natural language processing capabilities.
- **Google DeepMind’s Robotic Transformer (RT) Series**:
  - **RT-2**: Introduced the Vision-Language-Action (VLA) model, which allows multi-step semantic reasoning and task planning.
  - **RT-H**: Achieved an end-to-end robot transformer with action hierarchies for fine-grained task planning.
  - The Open X-Embodiment dataset integrates diverse data types for training embodied agents.
  - Despite advancements, challenges remain in model inefficiency, with efforts like SARA-RT and RoboMamba addressing these by improving speed and efficiency.

### Embodied Task Planning

#### Traditional Methods
- Often based on explicit rules and logical reasoning, such as STRIPS and PDDL.

#### Emergent Capabilities of LLMs
- LLMs now use internal world knowledge and chain-of-thought reasoning for task planning.
- **Examples**: Socratic Models and Socratic Planner improve planning accuracy through multi-turn reasoning.

#### Integration with Visual Information
- Incorporating visual input into planning allows for more accurate identification of objects and obstacles.
- **Examples**: SayPlan uses hierarchical 3D scene graphs for complex task planning.

#### Utilization of VLMs
- VLMs align visual and textual information in latent space, enhancing task planning.
- **Examples**: EmbodiedGPT and LEO effectively integrate embodied, visual, and textual information for planning.

### Embodied Action Planning

#### Action Utilizing APIs
- LLMs use pre-trained policy models for executing subtasks, with systems like Reflexion adjusting tools during execution for better generalization.

#### Action Utilizing VLA Model
- The VLA model’s integration of perception, decision-making, and execution allows for real-time feedback and strategy adjustment.
- However, limitations exist in simulating physical laws without embodied world models, affecting the transition from cyberspace to the physical world.

## Challenges in Current Research

### Technological Gaps
- Identifies the gap in technology that limits practical deployment.
- Necessitates improved adaptability and decision-making capabilities.

### Unstructured Environments
- Developing AI agents to perform reliably in varied and unpredictable settings.
- Quality data for training.
- Sim-to-real transfer.
- Integration of multiple sources of data.

## Future Directions and Potential Breakthroughs

### Advancements in AI
- Future advancements to bridge current gaps, particularly in learning efficiency and adaptability.
- Potential areas for significant impacts include healthcare, autonomous vehicles, and robotics.

### Implications for AGI
- Necessity of embodied experiences for achieving AGI.
- Importance of real-world interactions for evolving AI capabilities to handle complex tasks in dynamic environments.

## Conclusion

### Unified Evaluation Benchmark
- The need for comprehensive benchmarks encompassing diverse skills using realistic simulators.
- Integration of high-level task planning and low-level control policy evaluations.

### Continual Learning
- Importance for deploying robot learning policies in diverse environments.
- **Techniques**: Incremental learning, rapid motor adaptation, human-in-the-loop learning.

### Causal Relation Discovery
- Need for understanding causal relations between knowledge, behavior, and environment.
- **Techniques**: Active causal reasoning, constructing causal graphs.
