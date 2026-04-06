# GEPF-Project

[Knots & Kinks as Time Shrinks]

[Shevante Powell]

Description

"Knots & Kinks as Time Shrinks" is a fast-paced 2D time-management game where the player runs a bustling natural hair salon. The player must race against the clock to manage the salon floor, greet clients, detangle knots, and complete styling requests before the customers lose their patience and storm out. The gameplay involves movement around the shop grid, interacting with different stations (wash bowl, detangling chair, braiding station), and chatting with clients to figure out their desired look.

To support this high-energy aesthetic, the engine will be enhanced with several features. A Tile System will handle the grid-based layout of the salon floor and stations. A Text Dialog Popup system will drive the customer interactions. I will also implement Multi-animations to represent the different stages of hair care (washing, detangling, styling), alongside Wobble Animations and Music to give the game a bouncy, upbeat vibe. The engine's Hitpoints component will be made into a "Patience Meter" for customers, automatically flagging them for destruction when their timer runs out.

Game Tasks

Complexity Point Subtotal: [18]

Task 1 - [6] Complexity Points

Customer Spawning and Patience Decay:

Description: Implement the logic for a continuous stream of customers spawning, walking to the waiting area, and requesting a service. This feeds into the engine's Hitpoints system—treating "HP" as "Patience" that constantly decays and results in a "Game Over" penalty if it hits zero.

Integration: This forms the stressful core loop of the time-management gameplay, utilizing the engine's destruction when a client's patience expires.

Task 2 - [5] Complexity Points

The Styling

Description: Create the interactive logic for the styling process. The player must guide clients to specific tiles (wash sink, styling chair) and complete quick tasks or wait times to finish a hairstyle before moving to the next client.

Integration: This will utilize the engine's Multi-animation component, triggering state changes in the customer's sprite as their hair goes from natural, to washed, to fully styled.

Task 3 - [3] Complexity Points

Salon Floor Layout

Description: Design the layout of the shop, placing the various necessary stations at distances to create a challenging puzzle for the player as the salon gets crowded.

Integration: This directly utilizes the engine's 2D Tile System storage to map objects and stations to the world coordinates.

Task 4 - [4] Complexity Points

Client Requests & UI

Description: Write a variety of quick customer requests. When the player approaches a waiting client, they can press an interact key to instantly see what the client needs and where they need to go next.

Integration: This provides the data for the engine's Text Dialog Popup UI to render on screen.

Engine Tasks

Complexity Point Subtotal: [12]

Task 1 - [3] Complexity Points

Tile System

Description: Implement a flexible tiling system in engine core using a 2D array for storage. Decide how to map the grid to world coordinates to support placing salon floors, walls, and interactive furniture.

Integration: This serves as the foundation for the game's environment and the station placement mechanics.

Task 2 - [3] Complexity Points

Text Dialog Popup

Description: Implement a User Interface system capable of creating a text box overlay and displaying string data when triggered.

Integration: This enables the narrative game tasks, allowing the engine to render customer requests without cluttering the main game loop with rendering logic.

Task 3 - [2] Complexity Points

Hitpoints

Description: Implement an ECS component storing max HP and current HP, and an "HpCheck" system in that flags entities reaching 0 HP for destruction.

Integration: This will be used to manage Customer Patience, automatically clearing them from memory if they wait too long.

Task 4 - [2] Complexity Points

Multi Animation

Description: Create an ECS component that supports three separate, distinct animations for a single entity.

Integration: This will allow the game to swap customer sprites between "waiting," "getting washed," and "fully styled" states.

Task 5 - [1] Complexity Point

Wobble Animation

Description: Implement a simple wobble animation system in the engine.

Integration: This will be applied to UI elements, timers, or the player character to emphasize the frantic, rushing aesthetic.

Task 6 - [1] Complexity Point

Music

Description: Add music functionality to the AudioManager, ensuring play has a fade-in bool parameter and stop has a fade-out bool parameter.

Integration: This will provide an upbeat, fast-paced background track to keep the energy high as the timer ticks down.
