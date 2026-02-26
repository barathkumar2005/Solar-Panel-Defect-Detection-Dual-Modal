# Solar-Panel-Defect-Detection-Dual-Modal
Real-time dual-modal defect detection system using YOLOv8 for thermal anomalies and MobileViT-SE for visual surface defects on solar panels


## Real-Time Solar Panel Defect Detection (Dual-Modality)

### The "Why"
Solar energy is the future, but keeping panels efficient is a massive manual headache. During this project, we realized that single-camera systems often miss the full picture—thermal cameras miss surface cracks, and visual cameras miss internal hotspots. Our goal was to build a system that sees both, helping maintenance teams find and fix issues before they lead to permanent damage or power loss.
### How we built it
We developed a two-part brain for our system:
The Thermal Eye (YOLOv8s): We trained this to hunt for internal failures. It’s fast and accurate, perfect for spotting bypass diode failures and hotspots that are invisible to the naked eye.
The Visual Eye (MobileViT-SE): Surface defects like bird droppings or micro-cracks can be subtle. We used a Squeeze-and-Excitation (SE) attention block to help the model "focus" on these fine details, even when the panel is dusty or under uneven lighting.

### Real-World Testing
This isn't just a lab experiment. We went out to the VC Green Energy Solar Plant and used the FLIR C5 camera to gather real-world data. We then optimized these models to run on a Raspberry Pi 5, proving that you can take high-end AI out into the field on a portable device.

### Tech Stack

Deep Learning: YOLOv8, MobileViT-SE (Vision Transformers) 
Hardware: Raspberry Pi 5, FLIR C5 Thermal Camera 
Libraries: PyTorch, Ultralytics, OpenCV, NumPy 
