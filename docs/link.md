### Linking a Library to a Consumer Project

This is the documentation for the `link` script, which is used to link a library to a consumer project for real-time development and testing.

#### Overview
This Bash script is designed for developers working on a JavaScript library that needs to be tested within the context of a consumer project, such as a Laravel-based application. The script efficiently creates symbolic links (symlinks) to integrate the library with a local project without the necessity of publishing it to npm (Node Package Manager). This approach is beneficial for real-time development and testing.

#### Requirements
- Bash shell environment.
- npm (Node Package Manager) installed.
- Access to both the library and the consumer project directories.

#### Usage Instructions
1. **Initialize npm Link**:
   - Run `npm link` in the library directory to create a global symlink.

2. **Make Script Executable**:
   - Execute `sudo chmod +x link` to make this script executable.

3. **Clean npm Install**:
   - Ensure a clean environment by removing the `node_modules` directory from both the library and consumer project directories.
   - Perform `npm install` in both directories to reinstall the dependencies.

4. **Execute the Script**:
   - Run the script with the consumer project path as an argument to link the library dependencies to the consumer project.
   - Example: `./link /path/to/consumer/project`

5. **Build Processes**:
   - Execute `npm run build` in the library directory. Ensure no errors are displayed.
   - Run `npm run build` in the consumer project directory and verify the library's functionality.

6. **Development Mode Tips**:
   - For library development, use `npm run start`.
   - For the consumer project, use `npx vite --force` to reflect real-time changes from the library.

#### Dependencies Managed
The script manages a series of dependencies primarily related to React and Material UI. These dependencies are explicitly declared and iterated over for linking.

#### Breakdown of the Script
- **Dependency Loop**: Each specified dependency is unlinked from the library's `node_modules` and then linked to the same dependency in the consumer project's `node_modules`.
- **Path Variables**:
  - `consumer_project_path`: The path to the consumer project (provided as an argument).
  - `node_modules_path`: The path to the `node_modules` directory of the consumer project.

#### Conclusion
This script simplifies the process of library development by enabling real-time integration and testing with a consumer project, thereby enhancing efficiency and effectiveness in development workflows.
