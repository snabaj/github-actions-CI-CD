# GitHub Actions CI/CD

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Node.js Version](https://img.shields.io/badge/Node-%3E%3D14-brightgreen.svg)](https://nodejs.org/)
[![MERN Stack](https://img.shields.io/badge/MERN-Stack-blue.svg)](https://www.mongodb.com/mern-stack)

[![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)](https://www.mongodb.com/)
[![Mongoose](https://img.shields.io/badge/Mongoose-%2300cf4b.svg?style=for-the-badge&logo=mongoose&logoColor=white)](https://mongoosejs.com/)
[![Express](https://img.shields.io/badge/Express-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB)](https://expressjs.com/)
[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![React](https://img.shields.io/badge/React-20232A.svg?style=for-the-badge&logo=react&logoColor=61DAFB)](https://reactjs.org/)

## Description

This project is a full-stack application that integrates Continuous Integration (CI) and Continuous Deployment (CD) with GitHub Actions. It features an automated pipeline that:

- Runs Cypress component tests when a **Pull Request** is made to the `develop` branch.
- Deploys the application to **Render** when code is merged from `develop` to the `main` branch.

### Key Features:

- **CI Pipeline with GitHub Actions**: Automatically runs tests and ensures that code passes quality checks before merging.
- **CD Pipeline**: Automatically deploys to Render when the code is merged into the `main` branch.
- **Cypress Component Tests**: Runs tests on the component level to ensure the application’s features work correctly.
- **MERN Stack**: Built using MongoDB, Express.js, React, and Node.js.

## Table Of Contents

- [GitHub Actions CI/CD](#github-actions-cicd)
  - [Description](#description)
    - [Key Features:](#key-features)
  - [Table Of Contents](#table-of-contents)
  - [Installation](#installation)
  - [Usage](#usage)
    - [CI/CD Setup](#cicd-setup)
  - [Contributing](#contributing)
  - [License](#license)
  - [Tests](#tests)
  - [Questions](#questions)

## Installation

1. **Clone the repository:**

```
git clone https://github.com/snabaj/github-actions-CI-CD.git
cd github-actions-CI-CD
```

2. **Install dependencies:**

```
npm install
```

3. **Build the project:**

```
npm run build
```

4. **Seed the database**

```
npm run seed
```

5. **Start the development server:**

```
npm run develop
```

6. **Deploy the application on Render**
7. **Setup the database on MongoDB Atlas**
   - Add MongoDB Atlas database IP address to Render environment variables.
8. **Turn Off Auto Deploys:**

   - On the Render dashboard, navigate to your web service and go to the Settings tab.
   - Scroll down to Automatic Deploys and turn off auto deploys. This is important for controlling when the app is deployed, particularly if you want to manage deployments manually via GitHub Actions.

9. **Copy the Deploy Hook:**

   - In your Render dashboard, under the Settings of your web service, find Deploy Hooks.
   - Copy the Deploy Hook URL that Render generates for your service.
   - You will use this URL in your GitHub repository to trigger the deployment when changes are merged into the main branch.

10. **Add Deploy Hook as a GitHub Secret:**

    - Go to your GitHub repository and navigate to Settings.
    - Under the Secrets and Variables section, click on Actions.
    - Click New repository secret and add the following:
      - Name: RENDER_DEPLOY_HOOK_URL
      - Value: Paste the Deploy Hook URL you copied from Render.
    - This secret will be used in your GitHub Actions workflow to trigger deployment on Render after a successful merge to the main branch.

## Usage

### CI/CD Setup

**Continuous Integration (CI)**
When a Pull Request is made to the `develop` branch:

1. **Cypress Tests:** The GitHub Action will run Cypress component tests to ensure code quality.
2. **Test Results:** You will see the test results on GitHub Actions. If the tests pass, you can merge your PR.

**Continuous Deployment (CD)**
When the code is merged into the `main` branch:

1. **Automatic Deployment:** The GitHub Action will trigger and deploy the application to Render automatically.

## Contributing

Contributions are welcome! If you’d like to improve this project, follow these steps:

1. Fork the repository.
2. Create a new branch:

```
git checkout -b feature/your-feature
```

3. Make your changes and commit:

```
git commit -m "Add feature: description"
```

4. Push the branch:

```
git push origin feature/your-feature
```

5. Open a pull request.

Please ensure your code is well-documented and tested before submitting.

## License

This project is licensed under the [MIT](https://opensource.org/licenses/MIT) license.

## Tests

The project includes Cypress component tests to ensure code quality and functionality. You can add additional tests as needed.

## Questions

Please contact me with any questions you may have at [snabajja@gmail.com](mailto:snabajja@gmail.com) or visit my GitHub profile at [snabaj](https://github.com/snabaj).
