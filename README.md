[Documentation avaiable here ](https://greener-games.github.io/Singleton)


Managing single-instance objects is a common requirement in Unity projects. Whether it's for game managers, audio controllers, or persistent services, implementing singletons cleanly and consistently can be a challenge. This is especially true when balancing between scene-scoped and persistent lifecycles. Unity Singleton is designed to solve that problem.

Unity Singleton is a reusable, plug-and-play component that streamlines singleton creation in Unity. It abstracts away the repetitive setup and edge-case handling that often comes with singleton patterns. The result is a simple and reliable way to define single-instance behaviors.

Why Use Singleton?
Scene or Persistent Scope: You can choose whether your singleton should reset with each scene or persist across the entire play session.
Minimal Boilerplate: Just inherit from the base class and let Singleton handle the rest. There's no need to manually write instance checks or lifecycle logic.
Editor-Friendly: It works seamlessly in both play mode and edit mode. This reduces surprises during development.
Consistent Pattern: Singleton promotes a clean, uniform approach to singleton usage across your codebase. This makes it easier for teams to collaborate and maintain.
Use Cases
Game Managers: Centralize game state logic without worrying about duplicate instances.
Audio Systems: Keep audio controllers alive across scenes without reinitializing.
Service Layers: Manage input, networking, or analytics services with confidence in their lifecycle.
Getting Started
Using Unity Singleton is as simple as inheriting from the provided base class and specifying your scope. The component handles initialization, duplicate detection, and optional persistence automatically.

```
public class AudioManager : UnitySingleton<AudioManager>
{
    // Your logic here
}

```

With this setup, AudioManager.Instance is always safe to call. You can configure whether it should persist between scenes or not.

Unity Singleton is ideal for developers who want to reduce friction, enforce consistency, and focus more on building features than managing patterns. Whether you're working solo or in a team, it’s a small tool that can make a big difference in your Unity workflow.
