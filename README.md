Taboola Home Assignment
The project involves:
Loading data from a JSON file and displaying it in a RecyclerView with images.
Embedding Taboola widgets in cells 3 and 10.
Adding communication between two apps where the second app changes the background color of RecyclerView cells.
The components of the project include:

Fetching data from a JSON endpoint and displaying it in a RecyclerView.
Embedding Taboola Classic Unit widget in cell 3 and Taboola Feed widget in cell 10.
Communication between two apps to alter the RecyclerView's cell colors.
Issues and Solutions
Issue 1: Disk Space Shortage
During the development, I encountered a disk space shortage that prevented me from building the project and verifying the results.

Solution:
Cleaned up old files from my machine and Android Studio.
Moved the SDK to another drive.
Executed Clean Project in Android Studio to resolve issues.
Issue 2: Loading Data from JSON
The task required loading data from a JSON file and displaying it in a RecyclerView, with cells 3 and 10 being empty. Initially

Solution (cont.):
Implemented a JSON parser that correctly handles the required cell exclusions (cells 3 and 10 are left empty).
Used OkHttpClient to fetch the JSON data asynchronously.
Issue 3: Loading Images from URLs
One of the requirements was to display images fetched from URLs in the JSON data. Initially, images were not showing as expected.

Solution:
Used the Picasso library to load images from URLs and display them in the RecyclerView. This ensured that images were loaded correctly from external sources.
Issue 4: Taboola Widgets Not Displaying Properly
The integration of Taboola widgets (TBLClassicUnit and TBLClassicFeed) into cells 3 and 10 was problematic initially, as they didn't load correctly.

Solution:
Followed Taboola's official documentation and ensured that all necessary parameters (Publisher ID, Mode ID, Placement ID, etc.) were properly set for the widgets.
The widgets were then properly displayed in cells 3 and 10.
Issue 5: Performance and UI Issues
There were some performance issues with RecyclerView, especially when embedding Taboola widgets, which led to UI lag and rendering delays.

Solution:
Optimized the RecyclerView by using the ViewHolder pattern for each cell type (standard data cells and Taboola widgets). This improved rendering performance and ensured smooth scrolling.
Issue 6: Communication Between Two Apps
The requirement to have communication between two apps (with the second app changing the background color of RecyclerView cells) was unclear initially and required additional development time.

Solution:
Implemented a second app that communicates with the first app using an Intent. This second app sends data to the first app to change the background color of specific RecyclerView cells.
Issue 7: Compilation Error
While working on the project, I encountered the following error during the build process:

csharp
Copy
Edit
Caused by: org.codehaus.groovy.control.MultipleCompilationErrorsException: startup fail
Solution:
This error typically occurs due to issues in the Groovy scripts used by Android Studio. I resolved this by ensuring that all dependencies were correctly configured and that there were no syntax issues in the Gradle files.
Also performed a Sync Project with Gradle Files operation to make sure all dependencies were up to date.

Technology Requirements
Language: Java
Libraries:
Picasso – For loading images from URLs.
OkHttpClient – For fetching JSON data from a remote URL.
Taboola SDK – For embedding Taboola widgets.
Android Studio – IDE used for development.
How to Run the Project
Pre-requisites:

Install Android Studio.
Ensure you have the correct SDK installed.
Ensure you have the necessary Java version (if required, use a compatible version for Android development).
Steps:

Clone this repository to your local machine.
Open the project in Android Studio.
Run the app on an emulator or a connected device.
The app will fetch data from the JSON endpoint and display it in a RecyclerView with the necessary widgets embedded in cells 3 and 10.
