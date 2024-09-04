# AK-Pensionsreformrechner Website

This repository contains the Quarto-based website for the AK-OOe-Pensionen project. The website is live at:

[https://data-science.wifo.ac.at/AK-Pensionsreformrechner/](https://data-science.wifo.ac.at/AK-Pensionsreformrechner/)

## Prerequisites

Before you can run or deploy the website, ensure that you have the following installed on your system:

- **Git**: For cloning the repository and managing code versions.
- **Quarto**: For rendering and previewing the website. You can download and install Quarto from [here](https://quarto.org/docs/get-started/).

## Cloning the Repository

To get started, clone the repository from Gitea to your local machine using Git.

1. Open your terminal (or Git Bash on Windows).
2. Run the following command to clone the repository:

   ```bash
   git clone https://gitea.wsr.ac.at/wa-projects/AK-OOe-Pensionen-PN-23011.git
   ```

3. Navigate into the cloned repository:

   ```bash
   cd AK-OOe-Pensionen-PN-23011
   ```

## Running the Website Locally

To preview the website locally, follow these steps:

1. Ensure that you have Quarto installed on your system.
2. In the terminal, navigate to the root directory of the project if you're not already there.
3. Run the following command to start a local preview of the website:

   ```bash
   quarto preview
   ```

   This will render the website and start a local web server. You should be able to view the website in your browser at `http://localhost:7777`.

4. The `quarto preview` command will watch for any changes you make to the source files and automatically update the website preview in the browser.

## Rendering the Website for Production

To render the website for production (i.e., for deployment to the live site), use the following command:

1. Make sure you are in the root directory of the repository.
2. Run the following command:

   ```bash
   quarto render
   ```

   This will render all the necessary files for the website in a production-ready format, generating the output in the `webssite/` folder.

## Deploying the Website

Once you have rendered the website for production, you'll need to deploy it to the server.

1. After rendering, navigate to the `website/` folder that contains the built website files:

   ```bash
   cd website
   ```

2. Deploy the contents of this folder to the server where the website is hosted. Depending on your server setup, you can use `scp`, `rsync`, or a web deployment tool to move the files. Here’s an example of how to use `scp` for deployment:

   ```bash
   scp -r * lschmoigl@hades:/home/lschmoigl/datascience/htdocs/pensionen
   ```

3. Replace `lschmoigl` with your actual server credentials.

## Additional Information

- **Customizing the Website**: You can customize the content of the website by editing the markdown or R Markdown files within the repository. Changes made to these files will be reflected when you re-render or preview the website.
- **Help & Support**: For further assistance with Quarto, visit the [Quarto documentation](https://quarto.org/docs/guide/).

---

### Summary of Commands

```bash
# Clone the repository
git clone https://gitea.wsr.ac.at/wa-projects/AK-OOe-Pensionen-PN-23011.git

# Change directory into the project
cd AK-OOe-Pensionen-PN-23011

# Preview the website locally
quarto preview

# Render the website for production
quarto render

# Deploy the rendered website
scp -r website/* lschmoigl@hades:/home/lschmoigl/datascience/htdocs/AK-Pensionsreformrechner 
```

Happy coding!
