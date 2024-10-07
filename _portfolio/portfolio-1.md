---
title: "Trolly for automatic planting of pike seedings"
excerpt: "Group leader | Awarded Tecent Top 1% Light Camp Investment<br/><img src='/images/Trolly_model.png'>"
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
        <img src="/images/Trolly_structure.jpg" alt="Trolly" style="width: 100%;" class="hover-img" />
    </div>
    <p style="text-align: center;">
        <strong>Fig 1: Trolly_1.0</strong> <br>
    </p>
</div>

<div style="text-align: center; margin: 20px 0;">
    <video id="myVideo" controls muted width="720">
        <source src="/images/Exploded_view.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
    <script>
        var myVideo = document.getElementById("myVideo");
        myVideo.addEventListener('loadedmetadata', function() {
            this.poster = this.poster || this.captureStream().getVideoTracks()[0].getSettings().thumbnail;
        });
    </script>
</div>

<div style="text-align: center;">
    <div style="display: inline-block; text-align: center; width: 60%; vertical-align: top;">
        <img src="/images/Trolley.png" alt="Trolly" style="width: 100%;" class="hover-img" />
    </div>
    <p style="text-align: center;">
        <strong>Fig 2: Trolly_2.0</strong> <br>
    </p>
</div>

3D model:
<div style="text-align: center; margin: 20px 0;">
    <video id="myVideo" controls muted width="720">
        <source src="/images/Hollow_Drill.mp4" type="video/mp4">
        Your browser does not support the video tag.
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

<div style="text-align: center;">
    <div style="display: inline-block; text-align: center; width: 28%; vertical-align: top;">
        < img src="/images/Modeling of the seedling warehouse.png" alt="Modeling of the seedling warehouse" style="width: 80%;" class="hover-img"/>
        <p>(a)</p>
    </div>
    <div style="display: inline-block; text-align: center; width: 28%; vertical-align: top;">
        < img src="/images/Rendering of the seedling warehouse.png" alt="Rendering of the seedling warehouse" style="width: 80%;" class="hover-img"/>
        <p>(b)</p>
    </div>
    <p style="text-align: center;">
        <strong>Figure 1.1.1: Seedling Warehouse</strong> <br>
        (a) Modeling of the seedling warehouses<br>
        (b) Rendering of the seedling warehouse
    </p>
</div>

<div style="text-align: center;">
    <br>
    <div style="display: inline-block; text-align: center; width: 28%; vertical-align: top;">
        <img src="/images/Physical assembly diagram of the seedling warehouse.png" alt="Physical assembly diagram" style="width: 80%;" class="hover-img"/>
        <p>(a)</p >
    </div>
    <div style="display: inline-block; text-align: center; width: 28%; vertical-align: top;">
        <img src="/images/Physical assembly diagram the seedling warehouse.png" alt="Physical assembly diagram" style="width: 80%;" class="hover-img"/>
        <p>(b)</p >
    </div>
    <p style="text-align: center;">
        <strong>Figure 1.1.2: Seedling Warehouse</strong> <br>
        (a) left bearing<br>
        (b) Stepper Motor
    </p >
</div>

In the assembly process, we laser-cut acrylic sheets and sliced an acrylic tube into 1/4 arc segments. These were glued together using hot melt glue to create the seedling chamber. The rotating shaft was 3D printed, and using a flange coupling and a flanged bearing, the shaft was connected to both the seedling chamber and the micro stepper motor (5V/1:380).

1.2 Seedling Transport Mechanism

We initially considered two options for the seedling transport mechanism:

1.2.1 Conveyor Belt Seedling Transport

In this approach, a seedling storage tube would be used. The tube is aligned with the slanted base of the seedling chamber using a spring mechanism, and the tube’s body is suspended on a conveyor belt. A half-moon shaped baffle is positioned at the bottom, with a spring connecting the baffle and the tube. At the top of the drill, a baffle ensures that, when the seedling tube reaches the drill, the spring compresses, making the tube vertical and releasing it from the half-moon baffle, allowing the seedling to drop directly. Below is a conceptual diagram of this design:

(Here you would normally include a diagram or further visual reference of the conceptual design).

<div style="text-align: center;">
    <br>
    <div style="display: inline-block; text-align: center; width: 28%; vertical-align: top;">
        <img src="/images/Seedling storage" alt="Seedling storage" style="width: 80%;" class="hover-img"/>
        <p>(a)</p >
    </div>
    <div style="display: inline-block; text-align: center; width: 28%; vertical-align: top;">
        <img src="/images/Conveyor belt structure.png" alt="Conveyor belt structure" style="width: 80%;" class="hover-img"/>
        <p>(b)</p >
    </div>
    <p style="text-align: center;">
        <strong>Figure 1.2.1.1: Seedling storage and convey</strong> <br>
        (a) Seedling storage tube<br>
        (b) Conveyor belt structure
    </p >
</div>

1.2.2 Lever Mechanism-Based Seedling Transport

This method uses a single seedling storage tube. The vertical movement is achieved through a rack-and-pinion mechanism, while a linkage system lifts the entire structure, making it vertical for seedling delivery. The main components include: (1) an assembled cylindrical seedling storage tube, (2) a rack-and-pinion structure with a fixed mount, and (3) two linkages located at the front and middle of the storage tube.

Both methods have their advantages and disadvantages.

The conveyor belt system offers continuous structure and higher efficiency. However, its complex design raises concerns, such as whether the storage tube can properly return to its original position. It also involves considerable material consumption and complicates control, as the conveyor would need to pause and restart multiple times, potentially wasting power or wearing down components. Additionally, when we modeled the conveyor system, adding the seedling chamber made the overall structure too tall (exceeding 1 meter), which raised the center of gravity, making stable movement difficult. Given the harsh environment of desert areas, maintenance of a conveyor belt system would be challenging and expensive.

The lever-based seedling delivery system is simpler, avoiding unnecessary wear and tear. The overall structure is shorter, making it more stable, with simpler mechanics. It also has lower manufacturing and maintenance costs. However, it delivers seedlings one at a time, which reduces efficiency. But considering the drilling and planting process that follows, this lower speed is not a significant drawback.

Given the complexity of design, manufacturing difficulty, and cost considerations, we chose the lever mechanism-based seedling transport method.

<div style="text-align: center;">
    <br>
    <div style="display: inline-block; text-align: center; width: 28%; vertical-align: top;">
        < img src="/images/Modeling diagram of the first type of gear-rack seedling conveying mechanism" alt="gear-rack seedling conveying mechanism" style="width: 80%;" class="hover-img"/>
        <p>(a)</p >
    </div>
    <div style="display: inline-block; text-align: center; width: 28%; vertical-align: top;">
        < img src="/images/Modeling diagram of the second type of gear-rack seedling conveying mechanism.png" alt="gear-rack seedling conveying mechanism" style="width: 80%;" class="hover-img"/>
        <p>(b)</p >
    </div>
    <p style="text-align: center;">
        <strong>Figure 1.2.2.1: Gear-rack seedling conveying mechanism</strong> <br>
        (a) First type<br>
        (b) Second type
    </p >
</div>

After our calculations, we can get two linkage mechanisms designed as:

<div style="text-align: center;">
    <div style="display: inline-block; text-align: center; width: 60%; vertical-align: top;">
        <img src="/images/limit position diagram of the seedling transport connecting rod.png" alt="limit position diagram of the seedling transport connecting rod" style="width: 100%;" class="hover-img" />
    </div>
    <p style="text-align: center;">
        <strong>Fig 1.2.2.2: Initial/limit position diagram of the seedling transport connecting rod</strong> <br>
    </p>
</div>

2. Seedling Planting Mechanism

2.1 Overview

The seedling planting mechanism is primarily realized through a hollow drill. It consists of three main parts:

Frame: Provides support and guides movement.

Rotating Platform: Houses the motor and controls the vertical movement of the drill (which moves up and down with the drill).

Hollow Drill: Used for drilling into the soil and planting the seedlings. Below, each part and the materials used for construction are described.

2.2 Frame

The frame is constructed from aluminum profiles, forming a rectangular structure measuring 180mm by 150mm by 460mm. A limiter block is placed 91mm below the top, which functions to control the position of the slider, and thereby the opening and closing of the drill head. A guide rail made of a steel shaft is placed 130mm from the frame, with a distance of 37mm to guide the rotating platform's vertical movement. Diamond-shaped bearings are used to secure the steel shaft to the frame, ensuring smooth and stable operation.

<div style="text-align: center;">
    <div style="display: inline-block; text-align: center; width: 60%; vertical-align: top;">
        <img src="/images/Modeling diagram of the frame part of the seedling mechanism.png" alt="frame part of the seedling mechanism" style="width: 100%;" class="hover-img" />
    </div>
    <p style="text-align: center;">
        <strong>Fig 2.2.1: Modeling diagram of the frame part of the seedling mechanism</strong> <br>
    </p>
</div>

2.3 Rotating Platform

The rotating platform of the vehicle consists of three main components:

2.3.1	Load-bearing platform: This is the base structure.

2.3.2	Motor housing: A box-like structure that contains the motor responsible for driving the rotation of the drill. This box is secured to the load-bearing platform using screws.\

2.3.3	Drill attachment: This component fixes the drill to the platform using screws. The platform also has a hollow opening that aligns with the hollow drill, allowing for seamless operation.

Due to the complexity of this part, we outsourced its manufacturing. The rotating platform is fixed to the guide rail using four linear bearings, ensuring smooth vertical movement along the rail.

<div style="text-align: center;">
    <div style="display: inline-block; text-align: center; width: 60%; vertical-align: top;">
        <img src="/images/Rotating platform.png" alt="Rotating platform" style="width: 100%;" class="hover-img" />
    </div>
    <p style="text-align: center;">
        <strong>Fig 2.3.3.1: Rotating platform</strong> <br>
    </p>
</div>

2.4 Hollow Drill

The hollow drill is the core component of the seedling planting mechanism. It consists of two main parts:

2.4.1	Threaded drill body: This part includes the drill itself, which features a threaded design. The drill is connected to a nut, which engages with the threads to facilitate the drill's up and down movement as it rotates. For more efficient soil drilling and planting, we used a T-shaped thread with a pitch of 10mm.

2.4.2	Top connector and rod mechanism: The top part connects to the internal mechanism that controls the opening and closing of the drill head. The drill head's opening and closing mechanism is controlled by a hinge-based linkage connected to three thin rods. These rods are fixed to a slider, which is controlled by a limiter block. When the slider moves upward, the drill head closes; when it moves downward, the drill head opens, allowing the seedling to drop into the soil.

This design ensures precise control of the planting process. The figure below illustrates the components and mechanism in detail:

(Here, a diagram would typically be included to show the structure of the hollow drill and its internal mechanism).

<div style="text-align: center;">
    <br>
    <div style="display: inline-block; text-align: center; width: 28%; vertical-align: top;">
        < img src="/images/Hollow drill bit nut" alt="Hollow drill bit nut" style="width: 80%;" class="hover-img"/>
        <p>(a)</p >
    </div>
    <div style="display: inline-block; text-align: center; width: 28%; vertical-align: top;">
        < img src="/images/Engineering drawing of the overall internal structure of the drill bit.png" alt="Engineering drawing of the overall internal structure of the drill bit" style="width: 80%;" class="hover-img"/>
        <p>(b)</p >
    </div>
    <p style="text-align: center;">
        <strong>Figure 2.4.2.1: Hollow drill</strong> <br>
        (a) Hollow drill bit nut<br>
        (b) Engineering drawing of the overall internal structure of the drill bit
    </p >
</div>
