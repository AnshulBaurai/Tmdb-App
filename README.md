# Tmdb-App
🧱 Architecture
This project uses MVVM with Repository Pattern, ensuring a clean and testable codebase with proper separation of concerns.

Layered Overview
Model: Plain Swift structures conforming to Codable, used for mapping API and persistence data.

View: UIKit-based screens like UIViewController, UITableViewCell, UICollectionViewCell.

ViewModel: Handles presentation logic, formats data for the view, and interacts with the repository.

Repository: Abstracts data fetching/storing logic. Works with both network services and local persistence (e.g., Core Data).


📱 Features Implemented
🏠 Home Screen
The Home screen displays a UITableView, and each section contains a horizontally scrollable UICollectionView to showcase categories like trending, popular, or now-playing movies.

The app intelligently falls back to Core Data when there is no internet connection to ensure offline access to previously fetched data.

Tapping a movie navigates to the Movie Detail screen.


🔍 Search Tab
Provides real-time search functionality with live API calls.

Each keystroke updates the results by hitting the network (debouncing applied).

Selecting a search result navigates to the Movie Detail screen.


🎬 Movie Detail
Shows complete information about a selected movie.

Includes a Share button that allows the user to share a deep link (custom URL scheme like inshortImdb://movie?id=1234) to the same movie detail screen.

🔗 Deep Linking Support
The app supports custom deep links via inshortImdb://movie?id=....
If the app is launched (cold start) or resumed via a deep link, it navigates directly to the Movie Detail screen of the corresponding movie.



Steps to run the app

1. Open the .xcodeproj
2. Run on simulator 
