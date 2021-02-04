# ITECH DEV BOILERPLATE FULLSTACK - TRAINING FOR MY NEW ITECH DEV PEEPS OwO
### CrashCourse on TechStack: Simple FullStack Course Learning (Monorepo) Application
- TechStack:
    - Backend (Strapi)
    - Frontend (Vue, Gridsome, Tailwind CSS, Consuming Backend API with REST/GraphQL using Axios)



TABLE OF CONTENTS:

- [ITECH DEV BOILERPLATE FULLSTACK - TRAINING FOR MY NEW ITECH DEV PEEPS OwO](#itech-dev-boilerplate-fullstack---training-for-my-new-itech-dev-peeps-owo)
- [I. GIT & GITHUB SETUP](#i-git--github-setup)
- [II.STRAPI](#iistrapi)
  - [Setting up our Strapi CMS Backend](#setting-up-our-strapi-cms-backend)
  - [Strapi Installation and Setup](#strapi-installation-and-setup)
  - [Create Article Content Type](#create-article-content-type)
  - [Create Categories Content Type](#create-categories-content-type)
  - [Create Authors Content Type](#create-authors-content-type)
  - [Adding the contents to have data](#adding-the-contents-to-have-data)
    - [Adding categories to categories collection](#adding-categories-to-categories-collection)
    - [Adding authors to authors collection](#adding-authors-to-authors-collection)
    - [Adding articles to articles collection type](#adding-articles-to-articles-collection-type)
  - [Set Roles and Permissions](#set-roles-and-permissions)



---


# I. GIT & GITHUB SETUP

1. Create a new folder on your desktop and name it "itech-dev-boilerplate-fullstack" You can use your command line interface (terminal) to do the steps i'll be doing.

```bash
//This command changes your directory (cd) to your desktop
cd ~/desktop

//This command makes a new directory (mkdir) called "itech-dev-boilerplate-fullstack"
mkdir itech-dev-boilerplate-fullstack

//to see what files and folders you have in your current directory, use the command ls to list them on your CLI
ls
```

2. Initialise that project directory as a git repository.

```bash
//Go inside your project directory first
cd itech-dev-boilerplate-fullstack

//Make sure first that you have git!, this command initialises your repository as a git repository
git init
```

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/41f8c261-7853-4ed4-9675-fa9955c1edd4/Screenshot_2021-02-04_at_11.40.35.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T071256Z&X-Amz-Expires=86400&X-Amz-Signature=c82d7c0427cb5ac02b772f98abca6f6c2800970af593ff0882d48455c53449e6&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_11.40.35.png%22)

3. Upload it now to github. You can do this easily with github desktop! First add this existing local repository to your github desktop app, then publish this repository to your github.

*You don't have to follow my own way naman to setup this project with git and uploading it to github, basta you get what we're trying to do here hahaha*

anyways add this folder to your code editor so you can see the action running by your commads sa terminal ;) , i personally am using vscode for this tutorial - u can use any of your prefered code editors!! :))

---

# II.STRAPI

## Setting up our Strapi CMS Backend

Now that we initialised this repository as a git repository, let us now setup our strapi cms backend in our project repo.

 

- Optional Suggestions ;) :

## Strapi Installation and Setup

make sure you are inside the directory of your project in your terminal!

on your terminal:

```bash
npx create-strapi-app backend --quickstart
```

make sure you guys have node.js and yarn, if you guys dont have node or yarn, please install them na lang:

[Node.js](https://nodejs.org/en/)

[Home](https://yarnpkg.com)

installing node.js also install npm (node package manager). Both yarn and npm are package managers that install and manage packages for you when you guys are working on these dev projects. 

to check if they are installed, check your terminals and do: 

- "node —version" and "npm —version"
- "yarn —version"

if it doesn't show any versions after you input these commands on your terminal, means prolly wala pa kayo nito, so install them na lang at your own time as you follow this tutorial at your own time as well.

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/6bbb3558-74ef-427e-b076-6021117bc1e3/Screenshot_2021-02-04_at_12.06.03.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T071629Z&X-Amz-Expires=86400&X-Amz-Signature=1ab71c437421fd54a4afcab9b6bfad6dfa0e8de704763aca61028b02d3da93b2&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_12.06.03.png%22)

going back, after you npx create-strapi-app on your terminal in your project repo, u shud see a new folder called backend (which is what we named the folder when we did the installation command), with some files in it. that over there is our strapi app. 

after the command finishes installing and setting up the app, you shud see the following prompt on your terminals: 

```bash
NB3@nellyXinwei:itech-dev-boilerplate-fullstack master ➜ npx create-strapi-app backend --quickstart
npx: installed 91 in 31.583s
Creating a new Strapi application at /Users/NB3/Desktop/itech-dev-boilerplate-fullstack/backend.

Creating a quickstart project.
Creating files.
Dependencies installed successfully.
Your application was created at /Users/NB3/Desktop/itech-dev-boilerplate-fullstack/backend.

Available commands in your project:

  yarn develop
  Start Strapi in watch mode.

  yarn start
  Start Strapi without watch mode.

  yarn build
  Build Strapi admin panel.

  yarn strapi
  Display all available commands.

You can start by doing:

  cd /Users/NB3/Desktop/itech-dev-boilerplate-fullstack/backend
  yarn develop

> backend@0.1.0 build /Users/NB3/Desktop/itech-dev-boilerplate-fullstack/backend
> strapi build "--no-optimization"

Building your admin UI with development configuration ...

✔ Webpack
  Compiled successfully in 2.29m

Running your Strapi application.

> backend@0.1.0 develop /Users/NB3/Desktop/itech-dev-boilerplate-fullstack/backend
> strapi develop

[2021-02-04T03:54:47.520Z] info File created: /Users/NB3/Desktop/itech-dev-boilerplate-fullstack/backend/extensions/users-permissions/config/jwt.js

 Project information                                                          

┌────────────────────┬──────────────────────────────────────────────────┐
│ Time               │ Thu Feb 04 2021 11:54:52 GMT+0800 (Philippine S… │
│ Launched in        │ 22617 ms                                         │
│ Environment        │ development                                      │
│ Process PID        │ 37677                                            │
│ Version            │ 3.4.6 (node v12.18.3)                            │
│ Edition            │ Community                                        │
└────────────────────┴──────────────────────────────────────────────────┘

 Actions available                                                            

One more thing...
Create your first administrator 💻 by going to the administration panel at:

┌─────────────────────────────┐
│ http://localhost:1337/admin │
└─────────────────────────────┘
```

a window on your browser shud pop out with the following link presented, if you guys accidentally closed it, just go to the same localhosted link. 

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/795a5e90-2b26-4bae-b9da-461a4836c60f/Screenshot_2021-02-04_at_12.11.04.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T071635Z&X-Amz-Expires=86400&X-Amz-Signature=1b94bc38df2061574529b9230ef9ee51d2412a198f338e61c75081eb3ac021d2&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_12.11.04.png%22)

anyways, register muna as a admin user, please do not forget your credentials or it be not gud ;). 

after registering. you shud be redirected to yall dashboard that looks like this:

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/2c0ac917-2678-4a02-8363-6e898bb28fbf/Screenshot_2021-02-04_at_13.20.00.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T071639Z&X-Amz-Expires=86400&X-Amz-Signature=f4f3892bb948b3b97626805afe354117e1190481b15b843992218e96ad48a50b&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_13.20.00.png%22)

anyways, to end the localhost server of strapi, just ctrl+c on mac, not sure for windows but if you know how to escape a running command on your windows cli, use that. 

to run again the localhost server of strapi, cd into the backend folder and yarn develop as what the comand output said earlier when we set up our app.

```bash
//Go inside your backend folder inside your project folder, then run yarn develop to run the development server of strapi.
cd backend && yarn develop
```

## Create Article Content Type

Now lets create our article collections / content type.

On the sidebar of your dashboard, go to plugins>content-types-builder

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/c2f83644-db3d-40b2-9312-47a9bf9fe6b7/Screenshot_2021-02-04_at_13.34.17.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T071852Z&X-Amz-Expires=86400&X-Amz-Signature=2d639fecd383d32e72378ab20aa2578ba774ddafbabb9a95f5a3484810ecca7f&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_13.34.17.png%22)

this is where you guys can make the different collections/content-types.

now, on that page, under collection types, create new collection type and name it "Articles".

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/c2f83644-db3d-40b2-9312-47a9bf9fe6b7/Screenshot_2021-02-04_at_13.34.17.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T071852Z&X-Amz-Expires=86400&X-Amz-Signature=2d639fecd383d32e72378ab20aa2578ba774ddafbabb9a95f5a3484810ecca7f&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_13.34.17.png%22)

now let us add the following fields:

name (text :: shorttext)

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/9d58670e-cf50-4677-8344-1573f9f407db/Screenshot_2021-02-04_at_13.37.15.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T071903Z&X-Amz-Expires=86400&X-Amz-Signature=4120dc681a7224ba1bdc5eb61894a78eba9562f1a5f2654bbc3538b60bfe4a7a&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_13.37.15.png%22)

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/5273a13a-0786-43e4-a07d-997446a0e3e3/Screenshot_2021-02-04_at_14.04.27.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T072025Z&X-Amz-Expires=86400&X-Amz-Signature=9e28acb4f202ebbd02fc4839404234718c03ca15722f7c9abb068109f7b89193&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_14.04.27.png%22)

then go to advanced settings then tick required field and unique field

content (rich text)

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/0a921192-9e29-46b4-ac69-997240860f77/Screenshot_2021-02-04_at_13.40.05.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T072030Z&X-Amz-Expires=86400&X-Amz-Signature=bed6862e8ad6f12286e710db605648a7142708d9599152da4938bbdd58221e50&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_13.40.05.png%22)

please also make this as a required field, no need unique field

thumbnail (media :: single media)

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/daa96612-8310-4fee-bc62-39bee5e7d6b7/Screenshot_2021-02-04_at_13.41.42.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T072038Z&X-Amz-Expires=86400&X-Amz-Signature=66035393a1140ca826f33aec3d9eb0cbd016cea519b83aeaaf1c9bb73fa1fe6d&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_13.41.42.png%22)

make this one too required!!

always click finish or save so that you wont lose your changes !!.

anyways: heres our articles content type supposed to look like with their fields.

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/e861f113-7468-41a8-a812-067715df9e76/Screenshot_2021-02-04_at_13.43.43.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T072139Z&X-Amz-Expires=86400&X-Amz-Signature=96bc7f3742113d016650d4b07e5744b7770c18d99e2a0c9d034d27d9371dacc0&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_13.43.43.png%22)

after that, you should see on your blue sidebar, under collection types, you know have the articles collection types, this is now where you guys upload yall articles.

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/d9aeff9e-6da1-4e35-b1e7-235c92b92ef8/Screenshot_2021-02-04_at_13.49.32.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T072144Z&X-Amz-Expires=86400&X-Amz-Signature=849efa14bc8d10e85232417e18ea7de890a8c110e1cb42a32ea48e35a665eec1&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_13.49.32.png%22)

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/59b72133-284e-472a-8329-87048637d1f4/Screenshot_2021-02-04_at_13.49.49.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T072150Z&X-Amz-Expires=86400&X-Amz-Signature=d090532513f1bdcd67d638ec85b746c0a677acd07036b8b11f13b8f0d7aabd28&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_13.49.49.png%22)

in your project directory inside backend folder, if you look into the api folder, you should also see the articles folder, this is basically what we just did on our strapi development server. as we make changes, strapi automatically do stuff to our backend folder, abstracting the need to really have a hard time to code the backend from scratch (unless you want more features).

anyways don't add any articles yet since were still adding other collections such as the categories collection type.

## Create Categories Content Type

since this is itech u know, we want to categorise different articles to categories (hacker, hipster, hustler). 

go back to plugins>content-types-builder

create another new collection type and name it "categories" just like you did for articles.

for the fields of categories content-type:

same rin, has a name (text::short text) field, then make it required and unique field

now, add another field "relation"  and select the icon that represents many-to-many. the text should read, categories has and belongs to many articles. 

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/ba3d5aae-2d17-4aa3-b5fd-82bd3127080c/Screenshot_2021-02-04_at_14.07.37.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T072250Z&X-Amz-Expires=86400&X-Amz-Signature=44e21f8ba7f4fc7319fdf5381bffe565a2d7317dec0fccd0d5e4054571ba9a72&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_14.07.37.png%22)

this is basically an overview on how relational databases work where you have different content types or collections that are related to each other in different ways.

if we go back to the articles content type, we can see a new relational field added that reads as "Articles has and belong to many categories"

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/7a1486a6-b03f-4fde-a065-139fbfa678f1/Screenshot_2021-02-04_at_14.11.03.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T072254Z&X-Amz-Expires=86400&X-Amz-Signature=4a2ae8a723146288e28ae24ef2a365f95061b34c35a611cae73fe9ff4d487348&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_14.11.03.png%22)

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/5c0a277e-df58-4382-a0a5-1b93a2636192/Screenshot_2021-02-04_at_14.11.42.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T072258Z&X-Amz-Expires=86400&X-Amz-Signature=d4ec061753fed0396edbe326798bae485c9d85ac71a25dde22016d89bf85df3f&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_14.11.42.png%22)

now were done for categories, here again is an overview of how it should look like for categories content type so you gois can check. anyways once were through with this website, you guys can add extra fields to play around ex: description fields, or even add more collections.

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/7da08320-d61a-4291-b126-6e39c4d6640f/Screenshot_2021-02-04_at_14.13.54.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T072310Z&X-Amz-Expires=86400&X-Amz-Signature=23261bcad3fa1365bac60647e5889fcc39ec9b647cff327d2632ac12bf4f57b9&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_14.13.54.png%22)

now were forgetting the articles needs authors. hence we must create another collection type called authors.

## Create Authors Content Type

similarly, add the shorttext text field called "name" and make it required and unique.

then as relational field, this should be pointed to the articles content type.

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/6be745f7-5181-44db-9dcb-1f5c740238f2/Screenshot_2021-02-04_at_14.19.43.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T072445Z&X-Amz-Expires=86400&X-Amz-Signature=df8253e9ad87f45607b9876f7c974ca9e9dd1be74e414cffcf2e3d57864da97d&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_14.19.43.png%22)

the type of relation should be a one to many type of relation that should read as Author belongs to many articles.

now then, seems we got all the collection types we need for now. i guess as a challenge, you guys can too add the courses collection type, and the topics collection type which can be seen in our itech website. for this website, i just want to make this really brief so you can have the necessary understanding and skill to know how to work on these things as you move forward. 

ayt, lets now add the records/data in the different collections.

## Adding the contents to have data

### Adding categories to categories collection

now lets now go to the blue side bar and go to collection types> categories

lets add the hacker, hipster, hustler.

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/7c8cf5bf-4195-4758-83f3-b1b6207585f5/Screenshot_2021-02-04_at_14.25.58.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T072450Z&X-Amz-Expires=86400&X-Amz-Signature=b77694435a435b9ca3c0b39d2957a6f5f8a0a0bdef0b4889250956a4f4bb3766&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_14.25.58.png%22)

im pretty sure you guys get naman how to add records, pretty self explanatory ;)

### Adding authors to authors collection

for authors, lets just add hackerman, hipsterman, hustlerman? bb-hacker, bb-hipster, bb-hustler? just add any for this tutorial gegege. for this tutorial, imma add bb-hacker, bb-hipster, bb-hustler!

again dont forget to save and publish your record!!

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/41adfa1d-fb62-4580-8bc2-e8c85b98b413/Screenshot_2021-02-04_at_14.29.22.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T072456Z&X-Amz-Expires=86400&X-Amz-Signature=513c54617753784bde8dbfad2b58ff60d8a61afcfb558bbff208868afdea64f0&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_14.29.22.png%22)

### Adding articles to articles collection type

then for articles. lets just add four articles, add random stuff gegege.

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/72691ca8-4441-4bb7-8343-80752d631152/Screenshot_2021-02-04_at_14.34.51.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T072506Z&X-Amz-Expires=86400&X-Amz-Signature=1a3c459f9b5407e98a3cbd623df4eab9cc9d3065fad842e07a539ea062904c47&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_14.34.51.png%22)

fill all the following fields, and also if you look to the right, we find select options for the categories and authors this article has and belongs to.

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/edb50350-2af7-48ce-9701-84f714bec761/Screenshot_2021-02-04_at_14.37.50.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T072510Z&X-Amz-Expires=86400&X-Amz-Signature=fffe63d6c0e4f0d486954632a21e096854e31e6fc0632979f6f366f97ee98cf3&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_14.37.50.png%22)

now thats all done!!. let us now go change roles and permissions so that we can access the data or consume the api of our backend in our frontend.

## Set Roles and Permissions

on our blue sidebar, go to general>settings to go to our settinsg page

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/628a130f-12df-4927-8e04-8085b08babd1/Screenshot_2021-02-04_at_14.39.06.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T072658Z&X-Amz-Expires=86400&X-Amz-Signature=cfa0f08474b2503144626756a767820903142083ca87df5bac270dd5b0b7d14a&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_14.39.06.png%22)

then the white sidebar, go to users & permissions plugin > roles > public

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/73578243-82f4-47de-962e-222e754c66a6/Screenshot_2021-02-04_at_14.40.14.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T072702Z&X-Amz-Expires=86400&X-Amz-Signature=4b6ef3385ab05b737262db09db034e705cc4e970867f4e7ba597845f0502500b&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_14.40.14.png%22)

you should see permissions, select all possible permissions for each content type so that we are able to perform necessary operations we want to do with the data we get from our strapi backend api.

dont forget to save again. and THATS IT FOR THE STRAPI BACKEND FOR NOW!!! let us now do our frontend of our app.

before we go do our frontend, to visualise how this server and apis work. try going to [http://localhost:1337/articles](http://localhost:1337/articles) for example, you should then see our api (that is if you did the permissions correctly, or even have data in your collection which you should have ahhaha.

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/8cc0d772-c539-4c8e-99f4-48f62df627f6/Screenshot_2021-02-04_at_14.43.19.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T072708Z&X-Amz-Expires=86400&X-Amz-Signature=60a75a26206252f4776d43cfa18ba17e780e068881e852a5d3910ed6d2d66c40&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_14.43.19.png%22)

at /categories and /authors too can u see the data of the collection. that is basically how servers work ig. 

f as u can see, wrong spelling, double check yall spellings gois gg hahahha

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/bfc32276-56c2-4956-8b07-597e7a30f3eb/Screenshot_2021-02-04_at_14.47.53.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T072714Z&X-Amz-Expires=86400&X-Amz-Signature=dfb96214e452f63ba25f9d0a5b08a0d5ad495a9c2ffe03815679626c8c3151b1&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screenshot_2021-02-04_at_14.47.53.png%22)

what we are now trying to do next is to setup the frontend client side (what the users would see), and to consume the api (the data from our server from our database).

let us now proceed.
