

# <AI Code Reviewer/> 

<p align="center">
  <a href="#overview">🔍 Overview</a> •
  <a href="#usage">💻 Usage</a> •
  <a href="#faq">📖 FAQ</a> •
  <a href="#installation">🔧 Installation</a>
</p>

## Overview

This is a Chrome extension(works on edge too) which reviews 
- Azure devops pull Requests using [ChatGPT](https://chat.openai.com/) 
- Add comments on a PR from your behalf.
- Review the selected code on your page.
- Github private and public repo reviews (coming soon)

Here's an example output:
<img width="601" alt="image" src="https://user-images.githubusercontent.com/10302110/219318708-dd508803-a467-4dc6-8122-eeadd62eb179.png">

## Usage

### Azure devops PR review: 
- Navigate to a Azure devops Pull Request that you want a review for.
- Click the extension icon
- If you have not already, the extension will ask you to log in at [chat.openai.com](https://chat.openai.com)
- You get code review comments from ChatGPT in the popup window and in the file you have selected.

### Review selected code
- Select the code and click the code review button.

**Note:** Running the review multiple times often produces different feedback, so if you are dealing with a larger PR, it might be a good idea to do that to get the most out of it.

## FAQ

###

**Q:** Are the reviews 100% trustworthy?

**A:** This tool can help you spot bugs, but sometimes it is not 100% accurate. We are working on optimizing the queries to give you the best result.

###

**Q:** What aspects of the Pull Request are considered during the review?

**A:** Every file's diff is sent seperately to ChatGPT to avoid request size issue. Comment are added on every changed file based on the response.

## Installation

- Clone or download the zip of this repo 

- Go to edge://extensions in your browser.

- Enable developer mode

  <img width="280" alt="image" src="https://user-images.githubusercontent.com/10302110/218680951-11a09d9a-95dc-4bcb-95a9-553ff7d75439.png">

- Click on `Load unpacked` on this page

  <img width="735" alt="image" src="https://user-images.githubusercontent.com/10302110/218681042-17634a8d-78c1-4666-82c1-47cbbb27de61.png">

- Select the folder where you have downloaded the repo code.

### Get PAT token
<img width="211" alt="image" src="https://user-images.githubusercontent.com/10302110/219079910-792abcd7-0c36-46b8-8b00-c0cd01ca8fb3.png">

<img width="315" alt="image" src="https://user-images.githubusercontent.com/10302110/219082142-474337fd-e128-4269-8d36-0e243b626c63.png">

## Supported browsers

Chrome and edge

## Permissions

This is a list of permissions the extension uses with the respective reason.

- `activeTab` is used to get the URL or the active tab. This is needed to fetch the get the Pull Request details
- `storage` is used to cache the responses from OpenAI
- `scripting` to read the selected text from screen
