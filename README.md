# communityDB

Human curated community data for [fedidb.com](https://fedidb.com)

## Contributing to communityDB: Adding or Updating Software

Thank you for contributing to communityDB on FediDB! This document will guide you through the process of adding a new software entry or updating an existing one by submitting a Pull Request (PR). Follow the instructions below to ensure your PR can be reviewed and merged smoothly.

### ⚠️ Important: Software Author Permission Required

**Before submitting any software to communityDB, you MUST have explicit permission from the software author or maintainer.** 

- If you are the software author/maintainer, please state this clearly in your PR.
- If you are not the software author/maintainer, please include confirmation of permission in your PR (such as a link to communication or statement from the author).

PRs without verified permission will not be accepted. This requirement ensures we respect the intellectual property and preferences of all software creators.

## JSON Format for Software Entries
To add or update software in the communityDB repository, you will need to provide the details in the following JSON format:

```json
{
    "name": "Pixelfed",
    "slug": "pixelfed",
    "categories": [
        "image-sharing"
    ],
    "key_features": [
        "Photo and video sharing",
        "Discover feed",
        "Instagram-like UI",
        "Photo filters",
        "Stories feature",
        "Alt text support",
        "Accessibility features"
    ],
    "description": "Photo Sharing. For Everyone.",
    "license": "AGPL",
    "source_code": "https://github.com/pixelfed/pixelfed",
    "website": "https://pixelfed.org",
    "apps_url": "https://pixelfed.org/mobile-apps",
    "join_url": "https://pixelfed.org/servers",
    "api_docs_url": "https://beta-preview.pixelfed.io",
    "support_url": "https://github.com/pixelfed/support",
    "forum_url": "https://github.com/pixelfed/pixelfed/discussions",
    "donate_url": "https://pixelfed.org/support-our-project",
    "matrix_url": "https://matrix.to/#/#pixeldev:matrix.org",
    "logo_source_url": "https://fedidb.org/storage/software-logos/pixelfed.png",
    "logo_source_version": 2
}
```

## Steps to Add or Update Your Software Entry

### 1. Fork the Repository
Start by forking the communityDB repository to your own GitHub account. This will allow you to make changes without affecting the main repository directly.

### 2. Clone Your Fork
Clone your fork of the repository to your local machine:
```bash
git clone https://github.com/yourusername/communityDB.git
```

### 3. Create a New Branch
Create a new branch for your changes:
```bash
git checkout -b add-software-entry
```

### 4. Edit the `software.json` File
Locate the `software.json` file in the repository. Add your new software entry or update an existing one using the JSON format provided above.

#### **Field Descriptions**
- **name**: The name of the software (e.g., "Pixelfed").
- **slug**: A lowercase, URL-friendly identifier for the software (e.g., "pixelfed"). This should never change.
- **categories**: An array of categories, one or more of the following ["microblogging", "blogging", "image-sharing", "audio", "video", "events", "forum", "git", "other"]
- **key_features**: An array of key features (max 40 chars per feature, max 7 features)
- **description**: A short description of the software.
- **license**: The license of the software (e.g., "AGPL").
- **source_code**: URL to the source code repository.
- **website**: Official website URL for the software.
- **apps_url**: URL for mobile or desktop apps related to the software (optional).
- **join_url**: URL where users can join or register (optional).
- **api_docs_url**: URL for the software's API documentation (optional).
- **support_url**: URL for support resources (optional).
- **forum_url**: URL to any community discussion forums (optional).
- **donate_url**: URL for donations to support the software (optional).
- **matrix_url**: URL to a Matrix room for discussion (optional).
- **logo_source_url**: URL to the logo image of the software.
- **logo_source_version**: Version number of the logo source (used to update cached logos).

### 5. Validate Your JSON
Ensure your JSON is correctly formatted. You can use an online JSON validator such as [jsonlint.com](https://jsonlint.com/) to check for syntax errors.

### 6. Commit Your Changes
Once you have made your changes and validated the JSON, commit them:
```bash
git add software.json
git commit -m "Add Pixelfed to software list"
```

### 7. Push Your Changes
Push your changes to your fork:
```bash
git push origin add-software-entry
```

### 8. Open a Pull Request
Go to the original communityDB repository on GitHub and click the **"Compare & pull request"** button. Provide a brief description of the changes you made.

### 9. Respond to Review Feedback
The communityDB maintainers may request changes to your PR. Make any necessary updates and push them to your branch to update the PR.

## Example PR Description
When opening your Pull Request, include the following details:

- **Summary**: "Add [Software Name] to the communityDB software list"
- **Changes**: Add or update the JSON entry for the software.
- **Notes**: Provide any additional notes, such as why this software is relevant or any unique features.

## Questions?
If you have any questions or need help, feel free to open an issue or reach out to the maintainers. We appreciate your contributions!

---

## Contributing to communityDB: Adding or Updating Apps

Thank you for your interest in contributing apps to communityDB on FediDB! This document will guide you through the process of adding a new app entry or updating an existing one by submitting a Pull Request (PR).

### ⚠️ Important: App Author Permission Required

**Before submitting any app to communityDB, you MUST have explicit permission from the app's author or maintainer.** 

- If you are the app author/maintainer, please state this clearly in your PR.
- If you are not the app author/maintainer, please include confirmation of permission in your PR (such as a link to communication or statement from the author).

PRs without verified permission will not be accepted. This requirement ensures we respect the intellectual property and preferences of all app creators.

## JSON Format for App Entries
To add or update apps in the communityDB repository, you will need to provide the details in the following JSON format:

```json
{
    "name": "Tusky",
    "description": "A lightweight, open-source Mastodon client for Android supporting all Mastodon features.",
    "compatibility": ["Mastodon"],
    "categories": ["client"],
    "os": ["android"],
    "url": "https://tusky.app",
    "createdAt": "January 2017"
}
```

## Steps to Add or Update Your App Entry

### 1. Fork the Repository
Start by forking the communityDB repository to your own GitHub account.

### 2. Clone Your Fork
Clone your fork of the repository to your local machine:
```bash
git clone https://github.com/fedidb/communityDB.git
```

### 3. Create a New Branch
Create a new branch for your changes:
```bash
git checkout -b add-app-entry
```

### 4. Edit the `apps.json` File
Locate the `apps.json` file in the repository. Add your new app entry or update an existing one using the JSON format provided above.

#### **Field Descriptions**
- **name**: The name of the app (e.g., "Tusky").
- **description**: A concise description of the app and its features (recommended 200 characters max).
- **compatibility**: An array of software the app is compatible with (e.g., ["Mastodon", "Pleroma"]).
- **categories**: An array of categories, must be one of ["client", "official", "tools", "analytics", "utility", "moderation"]. Only official clients may have the "official" category.
- **os**: An array of operating systems the app supports, must be one or more of the following (e.g., ["android", "ios", "desktop", "web"]).
- **url**: Official URL for the app (app store, website, or repository).
- **createdAt**: When the app was first released (can be approximate, e.g., "January 2020" or null if unknown).

### 5. Validate Your JSON
Ensure your JSON is correctly formatted. You can use an online JSON validator such as [jsonlint.com](https://jsonlint.com/) to check for syntax errors.

### 6. Commit Your Changes
Once you have made your changes and validated the JSON, commit them:
```bash
git add apps.json
git commit -m "Add MyApp to apps list"
```

### 7. Push Your Changes
Push your changes to your fork:
```bash
git push origin add-app-entry
```

### 8. Open a Pull Request
Go to the original communityDB repository on GitHub and click the **"Compare & pull request"** button. Provide a brief description of the changes you made.

### 9. Confirm Permission
In your PR description, clearly state your relationship to the app and confirm you have permission to add it:
- "I am the developer/maintainer of this app"
- "Permission granted by [App Author] via [link to confirmation]"

### 10. Respond to Review Feedback
The communityDB maintainers may request changes to your PR. Make any necessary updates and push them to your branch to update the PR.

## Example PR Description
When opening your Pull Request, include the following details:

- **Summary**: "Add [App Name] to the communityDB apps list"
- **Permission**: "I am the developer of this app" or "Permission granted by [Developer] via [link]"
- **Changes**: Add or update the JSON entry for the app.
- **Notes**: Provide any additional notes about the app's relevance to the fediverse.

---

Thank you for helping improve FediDB's communityDB! Your contributions help showcase the diverse ecosystem of fediverse applications and software platforms.

