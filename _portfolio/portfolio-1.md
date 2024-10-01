---
title: "Trolly for automatic planting of pike seedings"
excerpt: "Group leader<br/><img src='/images/Trolly_model.png'>"
collection: portfolio
---
My Duties: 
Created [3D model], ensuring [Feasibility of processing and installation sites]

Created [Physical Mechanical Structures] , achieving [Hollow drill seedling]

Applied [Physical Mechanical Structures in Desert and keep optimizing]

1. Mechanical Structure
1.1 3D model overview
<div style="text-align: center;">
    <div style="display: inline-block; text-align: center; width: 60%; vertical-align: top;">
        <img src="/images/Trolly_structure.png" alt="Trolly" style="width: 100%;" class="hover-img" />
    </div>
    <p style="text-align: center;">
        <strong>Fig 1: Trolly_1.0</strong> <br>
    </p>
</div>

<div style="text-align: center; margin: 20px 0;">
    <video id="myVideo" controls muted width="720">
        <source src="/images/Exploded_view.mp4" type="video/mp4">d
    </video>
    <script>


<div style="text-align: center;">
    <div style="display: inline-block; text-align: center; width: 60%; vertical-align: top;">
        <img src="/images/Trolley.png" alt="Trolly" style="width: 100%;" class="hover-img" />
    </div>
    <p style="text-align: center;">
        <strong>Fig 1: Trolly_2.0</strong> <br>
    </p>
</div>

3D model:
<div style="text-align: center; margin: 20px 0;">
    <video id="myVideo" controls muted width="720">
        <source src="/images/Hollow_Drill.mp4" type="video/mp4">d
    </video>
    <script>
        var myVideo = document.getElementById("myVideo");
        myVideo.addEventListener('loadedmetadata', function() {
            this.poster = this.poster || this.captureStream().getVideoTracks()[0].getSettings().thumbnail;
        });
    </script>
</div>

_Abstract_
Desert regions have harsh climates and low income levels for residents. Cistanche can serve as a viable economic crop to improve local income, but it requires the support of the Haloxylon ammodendron tree for stable survival. Haloxylon also enhances the local environment and helps curb land desertification. However, the survival rate of Haloxylon is currently low; young trees may be buried by sand or die from harsh weather, while adult trees are at risk from root consumption by sand rats. Addressing these uncontrollable factors is challenging. Therefore, we plan to design an automated vehicle for planting Haloxylon, which will patrol planting bases for replanting efforts. This vehicle will be powered by solar panels and autonomously return to its base for recharging. Our project is divided into four parts: mechanism selection, design, modeling and simulation, and manufacturing. We have successfully implemented a series of actions including seedling emergence, transportation, and drilling for planting. After multiple brainstorming sessions and extensive research, our team utilized SolidWorks for modeling, created animations, calculated torque for the design, adjusted motor rotation cycles, and fabricated components, leading to continuous improvements of our vehicle and achieving the desired functionality.
_Keywords_: Seedling emergence, seedling transportation, hollow drilling head

1. Solution Selection

1.1 Seedling Chamber Mechanism
The seedling release mechanism is primarily realized using a roller. By controlling motor rotation through code, the roller rotates 180 degrees and then pauses, allowing time for seedling release and planting.
This part mainly consists of two components: the seedling chamber and the rotating shaft. The seedling chamber was laser-cut from acrylic sheets and manually assembled. Since the rotating shaft needs to be lightweight with low strength requirements, it was 3D printed.
