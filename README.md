# GitHub User and Repository Data Analysis for Berlin

- **Data Collection:** Using the GitHub API, I scraped user data for individuals in Berlin with over 200 followers and their up-to-500 most recent public repositories.
- **Key Finding:** A significant number of high-follower users are affiliated with start-ups, emphasizing Berlin's vibrant tech scene with strong GitHub activity across open-source projects.
- **Recommendation:** Developers aiming to increase visibility should prioritize showcasing their open-source contributions and collaboration on GitHub to attract followers and potential job opportunities.

## Project Overview

This project uses the GitHub API to gather information on GitHub users located in Berlin with more than 200 followers. The data includes information about the users themselves and their public repositories, up to a maximum of 500 repositories per user. 

### Files Included
1. **users.csv**: Contains information about GitHub users from Berlin with the following fields:
   - `login`, `name`, `company`, `location`, `email`, `hireable`, `bio`, `public_repos`, `followers`, `following`, `created_at`

2. **repositories.csv**: Contains details about the users' public repositories, with the following fields:
   - `login`, `full_name`, `created_at`, `stargazers_count`, `watchers_count`, `language`, `has_projects`, `has_wiki`, `license_name`

### Data Collection and Cleaning Process

1. **User Collection**: The script pulls user data through the GitHub API's search endpoint, filtering for users in Berlin with over 200 followers.
2. **Data Cleaning**: Company names are cleaned by removing any leading `@` symbol, trimming whitespace, and converting the names to uppercase.
3. **Repository Collection**: For each user in `users.csv`, the script fetches up to 500 of their most recently pushed public repositories, preserving key attributes like `stargazers_count`, `language`, and `license_name`.
4. **File Output**: The data is saved in CSV format, following the format requirements specified.

### Analysis Methodology

1. **Data Aggregation**: Analyzed user data for patterns in job affiliations and compared company profiles to follower counts.
2. **Repository Metrics**: Assessed repository languages, license types, and features (projects and wikis) for patterns related to engagement (stargazers and watchers).

### Noteworthy Insights
- Berlin's GitHub ecosystem is highly concentrated around tech startups, with many repositories focused on JavaScript and Python.
- Developers with public repositories under popular open-source licenses tend to attract more followers.

## How to Use
Clone the repository and access `users.csv` and `repositories.csv` for data insights. Use these files to explore the GitHub ecosystem in Berlin and identify collaboration or employment opportunities based on GitHub activity trends.

--- 

> **Note:** This project reflects a snapshot of GitHub's Berlin community and serves as a foundation for analyzing user engagement and content trends on the platform.
