📱 NIT3213 Final Assignment – Smart Home Control App
👩‍💻 Student Information

Student ID: A8070142

Unit: NIT3213 – Mobile Application Development

Assignment: Final Project Submission

🚀 Project Overview

This project is a Smart Home Control App built as part of the NIT3213 final assignment.
The application demonstrates the full Android development lifecycle, from UI design in Figma to implementation in Android Studio, using Material 3 principles, Clean Code practices, Navigation Components, Retrofit networking, RecyclerView, Dependency Injection with Hilt, and Unit Testing.

The app includes three key screens:

Login Screen – authenticates the user with API credentials.

Dashboard Screen – fetches and displays entities from the API in a RecyclerView list.

Details Screen – shows detailed information when a list item is selected.

🎨 UI / UX Design

Initial screen layouts were generated using Figma AI Copilot, based on the prompts provided in the assignment.

Design followed Material 3 guidelines (consistent spacing, typography, color contrast).

Screens include:

Login screen with username, password, and login button.

Dashboard showing connected devices/entities.

Details screen with full entity description.

Screenshots from Figma and the final app are provided in the report.

🧩 Clean Code & Navigation

Project structured into packages: ui, data, di, repository, and api.

Used Navigation Component to define navigation graph (nav_graph.xml).

Implemented Safe Args to securely pass the keypass argument from Login → Dashboard → Details.

Code followed Clean Code principles: meaningful class names, separation of concerns, and modular design.

🌐 Networking & Repositories

Retrofit used for API calls:

AuthRepository → handles login API (POST).

DashboardRepository → fetches dashboard entities (GET).

Networking done with Coroutines to ensure non-blocking operations.

Responses parsed using Gson converter.

Errors handled with safe fallback and Toast messages to user.

📋 Dashboard with RecyclerView

RecyclerView displays API data on the Dashboard.

Implemented custom Adapter + ViewHolder to bind each entity.

Entities show titles and summaries; tapping navigates to DetailsFragment.

Efficient scrolling and rendering achieved using RecyclerView’s adapter pattern.

🛠️ Dependency Injection (Hilt)

Hilt used for Dependency Injection (Step 7).

MyApplication.kt annotated with @HiltAndroidApp.

Fragments annotated with @AndroidEntryPoint.

@Module and @Provides used to supply Retrofit instance, repositories, and ViewModels.

Benefits:

Cleaner code with no manual object creation.

Easier testing (repositories can be mocked).

🧪 Testing

JUnit + MockK + kotlinx-coroutines-test used for Unit Testing (Step 8).

Tests located in src/test/java/....

Implemented:

LoginViewModelTest → verifies login success/failure updates LiveData correctly.

DashboardViewModelTest → verifies entities load successfully and failure returns empty list.

Used Dispatchers.setMain(testDispatcher) and advanceUntilIdle() for coroutine testing.

All tests passed successfully (screenshot evidence included in report).

📂 Project Structure
app/src/main/java/com/example/a8070142/
│
├── data/              # Retrofit API interfaces + Repositories
├── di/                # Hilt modules
├── ui/
│   ├── login/         # LoginFragment + LoginViewModel
│   ├── dashboard/     # DashboardFragment + ViewModel + Adapter
│   └── details/       # DetailsFragment
├── MainActivity.kt    # Hosts NavHostFragment
└── MyApplication.kt   # Hilt entry point

⚙️ Build & Run Instructions

Clone repository:

git clone <repo_link>
cd 8070142


Open project in Android Studio (latest stable).

Let Gradle sync automatically.

Run app on emulator or device (min SDK 24).

Enter valid login credentials → navigate to Dashboard → select item to view Details.

✅ Features Implemented

 Login screen (API POST).

 Dashboard screen (RecyclerView with API GET).

 Details screen (Safe Args navigation).

 Navigation Component integrated.

 Retrofit + Coroutines networking.

 Hilt for Dependency Injection.

 Unit Tests for ViewModels (Login & Dashboard).

 Report with screenshots + explanations.

📸 Evidence

Screenshots included in the report:

Figma design prompts & screens.

App running: Login, Dashboard, Details.

JUnit test results (green checks).
