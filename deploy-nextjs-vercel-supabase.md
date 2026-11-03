# How to Deploy a Next.js App on Vercel with Supabase Environment Variables

This guide explains how to deploy a Next.js application on Vercel and connect it with a Supabase project. It is useful for developers who have built an application locally and want to make it accessible online. By the end, the application will have a live URL and the required environment variables will be configured.

## Before You Start

Before deploying, make sure you have:
- A Vercel account
- A Supabase project
- A GitHub account
- Your Next.js project uploaded to GitHub
- The Supabase project URL and API key

## Steps to Deploy the Application

### 1. Open the Vercel Dashboard

Visit [vercel.com](https://vercel.com) and sign in using your account. The dashboard displays your existing projects and provides an option to create a new project.

### 2. Import the GitHub Repository

Click on **“Add New…”** and select **“Project”**. Connect your GitHub account if it is not already connected. Find the repository containing your Next.js application and click **“Import”**.

### 3. Configure the Project

After importing the repository, Vercel displays the project configuration page. Check the project name and make sure the framework preset is set to Next.js. Vercel usually detects this automatically. Keep the default build settings unless your project requires different settings.

### 4. Add Supabase Environment Variables

Open your Supabase dashboard and select your project. Go to the project settings and find the API section. Copy the project URL and the public API key.

In Vercel, open the **“Environment Variables”** section. Add the following variables with their corresponding values:

- `NEXT_PUBLIC_SUPABASE_URL`
- `NEXT_PUBLIC_SUPABASE_ANON_KEY`

Select the environments where these variables should be available, such as Production. Make sure the variable names match the ones used in your Next.js code.

### 5. Deploy the Application

Once the configuration is complete, click **“Deploy”**. Vercel starts building the application and installs the required dependencies. Wait for the build process to finish. If the build is successful, Vercel provides a deployment URL.

### 6. Check the Deployment

Open the live URL provided by Vercel in your browser. Check whether the homepage loads correctly and whether the features connected to Supabase are working. This helps confirm that the application has been deployed properly.

## If Something Goes Wrong

**Build Failure:** If the deployment fails, open the build logs in Vercel. Check for missing dependencies, incorrect build scripts, or code errors.

**Supabase Connection Error:** If the application cannot connect to Supabase, verify the environment variable names and values. After correcting them, redeploy the application so the updated variables take effect.

## Conclusion

Deploying a Next.js application on Vercel is a straightforward process once the GitHub repository and Supabase environment variables are configured correctly. Checking the live website after deployment helps identify any issues before sharing the application with others.
