# Unity Multiple Save System

A flexible and extensible multiple save system for Unity, designed to manage local and cloud-based save files, with support for multiple slots, custom data structures, and MongoDB cloud synchronization.

Description

This project provides a complete save and load system for Unity that allows you to:

- save and load game state using multiple save slots,

- organize local save files inside a dedicated Saves folder,

- serialize and deserialize custom data structures (JSON / Binary),

- manage saves across multiple scenes and game profiles,

- optionally store and retrieve saves from the cloud using MongoDB.

It is designed as a reusable foundation that can be easily integrated and extended in any Unity project.

☁️ Cloud Save Support (MongoDB)

To enable cloud saving with MongoDB, you need to install the MongoDB C# driver packages using a NuGet manager inside Unity. Unity doesn’t support NuGet packages natively, so we recommend using NuGetForUnity, a NuGet client for Unity.

📦 Required Steps

1. Install NuGetForUnity Plugin

   NuGetForUnity lets you manage NuGet packages directly in the Unity Editor:

    - GitHub page: https://github.com/GlitchEnzo/NuGetForUnity

    - NuGetForUnity CLI (optional tool): https://www.nuget.org/packages/NuGetForUnity.Cli

   Installation via Unity Package Manager:

    - Open Unity and go to Window → Package Manager

    - Click the ‘+’ button and select Add package from git URL…

    - Enter: "https://github.com/GlitchEnzo/NuGetForUnity.git?path=/src/NuGetForUnity"

    - Click Add

   Alternatively, download and import the .unitypackage file from the GitHub releases.

2. Install MongoDB Driver Packages via NuGetForUnity

   After installing NuGetForUnity:

    - In the Unity menu, go to NuGet → Manage NuGet Packages

    - Search for:

      - MongoDB.Driver (official C# driver)

      - MongoDB.Driver.Core

      - MongoDB.Bson

    - Install each package from the NuGet window

   These packages enable your project to connect to a MongoDB database for cloud saving.

3. Use the MongoDB Driver in your Cloud Save Logic

   Once imported, you can use the MongoDB driver APIs in your C# scripts to save and retrieve data from the cloud.
