# ![Rescuepath](https://user-images.githubusercontent.com/86598034/147409201-2f75ae4d-8c87-44f0-9b8c-72c945416347.png)
This project was developed during the [HCK-HNX Hackathon](https://www.hck-hnx.de/) hackathon.

## Description
This project was made during a 48 hour [Hackathon](https://www.hck-hnx.de/) hosted by the Hochschule Heilbronn together with the companies [Beyerdynamic](https://www.beyerdynamic.de/), [IDS](https://de.ids-imaging.com/), [Schunk](https://schunk.com/de_de/startseite/) and [42 Heilbronn](https://www.42heilbronn.de/en/).
The topic of the hackathon was "Sensors and AI" with the goal of creating a prototype of a product that uses some form of AI and the technologies offered by the companies.

After brainstorming about possibilities, we noticed a very current problem with large crowds all over the world, and decided to work on our project we later named "RescuePath".
### The initial Problem
Everyone who has been in a large crowd of people, for example during a festival, knows the feeling of being within or fighting through a massive, very dense group of people. Getting from point A to point B seems imossible and takes forever.
Imagine dancing around and seriously injuring yourself while in this situation, it would take forever for emergency services to reach you! This can potentially make small accidents exponentially more dangerous.

### Our Solution: RescuePath
We decided to create software that analyzes top-view images of large crowds and finds the most efficient way from point A to point B within this crowd. The end goal was a kind of "Navigation System" through the crowd, taking the constantly changing dynamic crowd into consideration.
Due to the time limitations, we decided to use great and ready to use open source libraries as the base of our software.
- First, we used an open-source library called [LWCC](https://github.com/tersekmatija/lwcc) (LightWeight Crowd Counting     library) to first create a density map of a given image.
  This density map gave us the (surprisingly accurate) amount of people per pixel on the image.
- Then, using the library [wylee/Dijkstar](https://github.com/wylee/Dijkstar) and utilizing its implementation of the       Dijkstra pathfinding algorithm, we were able to find the most efficient path through the density map.
- We then drew a simple line representing the path onto the original image.
- The result is a rendered image of the frame inclduing the most efficient path calculated by the algorithm.

Because of time limitations, we concentrated on creating a Minimum Viable Product to be able to pitch the general idea and plausability to the jury.

### Future Plans
- Optimize/rewrite the algorithms so a live-rendering of video feed is possible.
- "Translate" the rendered images into a human-usable form. Currently, the line is very jumpy and not very usable for a person walking through the crowd. We would like to create an app for smartphones and smartwatches that shows the general direction of where to walk to instead of a line that seems impossible to follow.
- Validate the rendered images with tests that ensure the path is truly the most efficient and practical path possible.
- Live testing in a large group of people.

### Use Cases
- Emergency services for navigating through a large crowd
- Prevention of catastrophes that happen in huge crowds by offering a navigation app to participants.
  This app can show the live density of certain regions and give suggestions on where to go and how to get there without overcrowding certain areas. Also, navigation to certain points of interest like food/drink stands, toilets, etc. can ensure safe travel through the crowd and optimize distibution of people amongst these locations, reducing waiting time and potentially maximizing profits for the stands themselves.
- Anything where large crowds of people can be a problem.



