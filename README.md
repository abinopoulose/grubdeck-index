# 💻 GrubDeck Theme Index
Welcome to the GrubDeck Theme Index repository!

This repository serves as the central directory for all themes featured in the GrubDeck theme manager application. To get your custom GRUB theme listed in the application, you just need to add an entry to the index.json file and submit a Pull Request.

### The GrubDeck Application
This index file is consumed by the main GrubDeck application, which is used by users to browse and install themes.
Find the main application repository here:  [github.com/abinopoulose/grubdeck](https://github.com/abinopoulose/grubdeck)

## How to Contribute Your Theme
Follow these steps to successfully add your theme to the GrubDeck index:

### Step 1: Prepare Your Theme Repository
Before starting, ensure your actual GRUB theme source code and all necessary preview images are hosted in a publicly accessible GitHub repository.

Theme Installation Link (repo_link): This link should point to your theme's main repository.

Image Links (cover_image, carousel_images): All image URLs must use the Raw Content URL from your repository (e.g., https://raw.githubusercontent.com/yourname/your-theme-repo/...).

### Step 2: Fork and Clone this Repository
Fork this repository to your own GitHub account.

Clone your fork to your local machine:
``` 
git clone git@github.com:YourUsername/grubdeck-theme-index.git
```

Navigate into the new directory:
``` 
cd grubdeck-theme-index
``` 

### Step 3: Edit the Index File
Open the themes/index.json file and add a new JSON object for your theme to the end of the existing list, making sure to include a comma , after the previous theme's closing curly brace (}).

### Theme Entry Structure
Your entry must strictly adhere to the following format. Pay close attention to the required data types for each field.

| Field | Type | Description | 
| :------ | :---------: | :------ |
| id | Integer | Use the next available unique integer ID (e.g., if the last theme is 5, use 6). | 
| name | String | The display name of your theme (e.g., My Awesome Theme). |
| cover_image | String | The raw URL of the image used for the theme card thumbnail on the home page. |
| repo_link | String | The public GitHub URL of your theme repository. This is used by the app to clone/install your theme.|
| description | String | A concise description of the theme (e.g., screen size, color scheme, OS focus). |
| carousel_images | Array of Strings | A list of raw URLs for screenshots/previews to be shown on the detailed theme page. Include at least one image. |
| created_by | String | Your GitHub username or name. |

Example of a New Entry

```
[ 
    // ... previous theme entries ...
    {
        "id": integer, 
        "name": "string",
        "cover_image": "string (raw image URL)",
        "repo_link": "string (github repo URL)",
        "description": "string",
        "carousel_images": [
            "string (raw image URL)",
            "string (raw image URL)"
        ],
        "created_by": "string"
    }
]
```

Once you've made your changes to index.json, simply commit the file and open a Pull Request. Thank you for contributing!
