# GitHub Issues Fetcher to Google Sheets

This Google Apps Script fetches issues from all repositories within a specified GitHub organization and exports the details to a Google Sheet. It retrieves both open and closed issues and fetches additional details for each issue using GitHub's GraphQL API.

## Features

- **Fetch Repositories**: Retrieve all repositories under a specified GitHub organization.
- **Fetch Issues**: Collect both open and closed issues from each repository.
- **GraphQL Query**: Fetch detailed information about each issue using GitHub's GraphQL API.
- **Google Sheets Integration**: Export the issues into a Google Sheet with detailed information.

## Setup Instructions

### Prerequisites

1. **GitHub Personal Access Token**: Generate a personal access token from GitHub with `repo` and `read:org` permissions.
2. **Google Account**: You need a Google account with access to Google Sheets.

### Steps to Use

1. **Create a New Google Apps Script Project**:
   - Go to [Google Apps Script](https://script.google.com/) and create a new project.

2. **Copy the Script**:
   - Copy the code from the `googlescriptcode.gs` file in this repository and paste it into the Google Apps Script editor.

3. **Set Up Variables**:
   - Replace the following placeholder variables in the script with your actual values:
     - `token`: Your GitHub Personal Access Token.
     - `org`: The name of your GitHub organization.
     - `spreadsheetId`: The ID of your Google Spreadsheet where the issues will be saved.
     - `sheetName`: The name of the sheet within the spreadsheet where you want to export the data.

4. **Run the Script**:
   - Save and run the `fetchGitHubIssues` function. You may need to grant permissions to the script for accessing Google Sheets and making HTTP requests.
   - The script will fetch issues from all repositories within the specified organization and export the data into your Google Sheet.

### Troubleshooting

- **Sheet Not Found**: If you encounter an error that the sheet is not found, ensure that the `sheetName` matches exactly with the sheet name in your Google Spreadsheet.
- **HTTP Errors**: If you receive an HTTP error, ensure that your GitHub token is valid and has the correct permissions.

## Customization

You can customize the script to include additional fields or modify the format of the exported data. For example, you can modify the GraphQL query to retrieve more information about each issue.

## Contributing

If you'd like to contribute to this project, please fork the repository and submit a pull request. We welcome any improvements or bug fixes.

## Contact

For any questions or issues, feel free to open an issue in this repository.

---

**Author**: Evrim Aslan
**GitHub**: https://github.com/evrimaslan85
