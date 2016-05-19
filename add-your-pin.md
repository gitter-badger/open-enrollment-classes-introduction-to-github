---
layout: page
title: Add Your Pin to the Map
permalink: add-your-pin/
---

### Join our class repository
We want you to get your hands dirty! In order to do so, you'll need to create an account and gain access to our shared project. These steps walk you through that process.

1. [Sign up](https://github.com/join) for an account on GitHub.com.
2. Navigate to our classroom by [clicking here](https://classroom.github.com/group-assignment-invitations/0b2dd5122538e0d7d78b157007fa333f).
3. Sign in with your GitHub account.
4. You'll be prompted to select a team, click where it says *Please click on this team*.
5. Click on the link to start the assignment.

### Use Issues to Track your Progress
Issues are an easy, lightweight way to have discussions with colleagues or track your own progress. Here, we'll use them to track the steps you've completed using GitHub flow.

1. Navigate to the **Issues** tab in the class repository.
2. Click on the green **New issue** button to start an Issue.
3. The issue will populate through the use of an *issue template*. Feel free to customize your issue, here are some ideas:
  - use emoji :smile: :octocat: :+1:
  - add items to your checklist
  - create bullets
  - emphasize text with **bold**, or *italics*
  - add labels
4. Change the title of your issue to: `<your-username>: Add <your-town> to the map`
5. Click on **Submit new issue**.
6. Assign your newly submitted issue to yourself.

### Add Your Pin to the Map with a Pull Request (Option 1)

1. Check out the [class map](../index.html)! If there's already a pin on your city, jump to the next section titled **Adding your name to an existing pin**. If there's no pin on your city, continue with these steps to add one!
2. [Find your city's coordinates](http://mynasadata.larc.nasa.gov/latitudelongitude-finder/) using longitude and latitude. These values are conventionally given in the order `[Latitude, Longitude]`. For this activity, the order will be reversed: `[Longitude, Latitude]`.
  - **Longitude**: your city's location relative to east and west. Positive numbers represent east, negative numbers represent west.
  - **Latitude**: your city's location relative to north and south. Positive numbers represent north, negative numbers represent south.
3. Create a branch from `master` in the class repository. Name the new branch `your-username-your-city`.
4. In your new branch, edit the file `class-pins.topojson`.
5. Enter the following code between lines 2 and 3.

       { "type": "Feature",
         "id": "yet-another-test-student",
         "geometry": {"type": "Point", "coordinates": [YOUR_LONGITUDE, YOUR_LATITUDE]},
         "properties": {"user1": "YOUR_USERNAME"}
         },

      Ensure you've replaced:

      - `YOUR_LONGITUDE` with your east/west coordinate.
      - `YOUR_LATITUDE` with your north/south coordinate.
      - `YOUR_USERNAME` with your GitHub username.

6. Preview your additions to ensure your marker shows up.
7. Enter a commit message that describes your addition.
8. Commit your change to your branch.

### Adding Your Name to an Existing Pin (Option 2)

1. Follow these steps only if a pin already existed for your city. If you added a pin for your city, move on to the next section titled **Introducing your Addition**
2. Create a branch from `master` in the class repository. Name the new branch `your-username-your-city`.
3. In your new branch, edit the file `class-pins.topojson`.
4. Look through the file for the entry for the pin that corresponds to your hometown. Once you find it, add a new line after the last `'properties'` line.

       { "type": "Feature",
         "id": "yet-another-test-student",
         "geometry": {"type": "Point", "coordinates": [YOUR_LONGITUDE, YOUR_LATITUDE]},
         "properties": {"user1": "OTHER_USERNAME"}
         "properties": {"user2": "YOUR_USERNAME"}
         },

      Ensure you've replaced:

      - `YOUR_USERNAME` with your GitHub username.

5. Preview your additions to ensure your marker shows up.
6. Enter a commit message that describes your addition.
7. Commit your change to your branch.

### Introducing your Addition
