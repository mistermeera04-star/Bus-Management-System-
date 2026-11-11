# College Bus Route & Fare Management System

A responsive browser website based on the supplied Phase 1 and Phase 2 project presentations.

## Features
- Route nodes linked in an outer singly linked list
- Stop nodes linked in an inner singly linked list for each route
- Add route and stop, search, update fee, delete stop
- Insert a stop after another stop and reverse a route
- Undo the latest fee update using a stack (LIFO)
- Compare fees, count stops and show highest annual fee
- Saves browser changes using `localStorage`

## Run locally
Open `index.html` in a modern browser. No server or installation is required.

## Publish using GitHub Pages
1. Create a new GitHub repository, for example `college-bus-route-system`.
2. Upload `index.html`, `style.css`, `script.js`, `bus_routes.c`, and this README.
3. Open **Settings → Pages** in the repository.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the `main` branch and `/ (root)` folder, then Save.
6. Wait for GitHub Pages to publish the site. Open the URL shown in Settings → Pages.

## About the C file
`bus_routes.c` is the native C version of the data-structure logic and runs as a terminal program. GitHub Pages is static hosting and will not execute a `.c` file. The web interface uses JavaScript to implement the same linked-list and stack operations in the browser. If the project must execute C inside the browser, it can be compiled to WebAssembly with Emscripten and connected to the page.

## Compile and run C version
```bash
gcc bus_routes.c -o bus_routes
./bus_routes
```
On Windows with MinGW:
```bash
gcc bus_routes.c -o bus_routes.exe
bus_routes.exe
```

## Sample data
The starter website loads the sample routes from the Phase 2 presentation:
- Route 1 - Trichy Central: Central Bus Stand (₹18,000), Thillai Nagar (₹19,500), Woraiyur (₹21,000)
- Route 2 - Srirangam: Srirangam (₹22,000), Thiruvanaikaval (₹23,000), Kallanai Road (₹24,500)
- Route 3 - Lalgudi: Samayapuram (₹25,000), Manachanallur (₹27,000), Lalgudi (₹29,000)
