CrashCourse on TechStack: Simple FullStack Course Learning (Monorepo) Application

- Fullstack:
    - Backend (Strapi)
    - Frontend (Vue, Gridsome, Tailwind CSS, Consuming Backend API with REST/GraphQL using Axios)
- TRAINING FOR ITECH DEV CURRICULUM

---

# ITECH DEV BOILERPLATE FULLSTACK

- **TABLE OF CONTENTS:**

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

![https://s3.us-west-2.amazonaws.com/secure.notion-static.com/41f8c261-7853-4ed4-9675-fa9955c1edd4/Screenshot_2021-02-04_at_11.40.35.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T071256Z&X-Amz-Expires=86400&X-Amz-Signature=c82d7c0427cb5ac02b772f98abca6f6c2800970af593ff0882d48455c53449e6&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D"Screenshot_2021-02-04_at_11.40.35.png](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/41f8c261-7853-4ed4-9675-fa9955c1edd4/Screenshot_2021-02-04_at_11.40.35.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210204%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210204T071256Z&X-Amz-Expires=86400&X-Amz-Signature=c82d7c0427cb5ac02b772f98abca6f6c2800970af593ff0882d48455c53449e6&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D"Screenshot_2021-02-04_at_11.40.35.png)

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

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6bbb3558-74ef-427e-b076-6021117bc1e3/Screenshot_2021-02-04_at_12.06.03.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6bbb3558-74ef-427e-b076-6021117bc1e3/Screenshot_2021-02-04_at_12.06.03.png)

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

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/795a5e90-2b26-4bae-b9da-461a4836c60f/Screenshot_2021-02-04_at_12.11.04.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/795a5e90-2b26-4bae-b9da-461a4836c60f/Screenshot_2021-02-04_at_12.11.04.png)

anyways, register muna as a admin user, please do not forget your credentials or it be not gud ;). 

after registering. you shud be redirected to yall dashboard that looks like this:

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2c0ac917-2678-4a02-8363-6e898bb28fbf/Screenshot_2021-02-04_at_13.20.00.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2c0ac917-2678-4a02-8363-6e898bb28fbf/Screenshot_2021-02-04_at_13.20.00.png)

anyways, to end the [localhost](http://localhost) server of strapi, just ctrl+c on mac, not sure for windows but if you know how to escape a running command on your windows cli, use that. 

to run again the [localhost](http://localhost) server of strapi, cd into the backend folder and yarn develop as what the comand output said earlier when we set up our app.

```bash
//Go inside your backend folder inside your project folder, then run yarn develop to run the development server of strapi.
cd backend && yarn develop
```

## Create Article Content Type

Now lets create our article collections / content type.

On the sidebar of your dashboard, go to plugins>content-types-builder

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c2f83644-db3d-40b2-9312-47a9bf9fe6b7/Screenshot_2021-02-04_at_13.34.17.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c2f83644-db3d-40b2-9312-47a9bf9fe6b7/Screenshot_2021-02-04_at_13.34.17.png)

this is where you guys can make the different collections/content-types.

now, on that page, under collection types, create new collection type and name it "Articles".

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2aacd8d5-0370-4654-815f-e09d0682837a/Screenshot_2021-02-04_at_13.36.13.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2aacd8d5-0370-4654-815f-e09d0682837a/Screenshot_2021-02-04_at_13.36.13.png)

now let us add the following fields:

name (text :: shorttext)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9d58670e-cf50-4677-8344-1573f9f407db/Screenshot_2021-02-04_at_13.37.15.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9d58670e-cf50-4677-8344-1573f9f407db/Screenshot_2021-02-04_at_13.37.15.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5273a13a-0786-43e4-a07d-997446a0e3e3/Screenshot_2021-02-04_at_14.04.27.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5273a13a-0786-43e4-a07d-997446a0e3e3/Screenshot_2021-02-04_at_14.04.27.png)

then go to advanced settings then tick required field and unique field

content (rich text)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0a921192-9e29-46b4-ac69-997240860f77/Screenshot_2021-02-04_at_13.40.05.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0a921192-9e29-46b4-ac69-997240860f77/Screenshot_2021-02-04_at_13.40.05.png)

please also make this as a required field, no need unique field

thumbnail (media :: single media)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/daa96612-8310-4fee-bc62-39bee5e7d6b7/Screenshot_2021-02-04_at_13.41.42.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/daa96612-8310-4fee-bc62-39bee5e7d6b7/Screenshot_2021-02-04_at_13.41.42.png)

make this one too required!!

always click finish or save so that you wont lose your changes !!.

anyways: heres our articles content type supposed to look like with their fields.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e861f113-7468-41a8-a812-067715df9e76/Screenshot_2021-02-04_at_13.43.43.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e861f113-7468-41a8-a812-067715df9e76/Screenshot_2021-02-04_at_13.43.43.png)

after that, you should see on your blue sidebar, under collection types, you know have the articles collection types, this is now where you guys upload yall articles.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d9aeff9e-6da1-4e35-b1e7-235c92b92ef8/Screenshot_2021-02-04_at_13.49.32.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d9aeff9e-6da1-4e35-b1e7-235c92b92ef8/Screenshot_2021-02-04_at_13.49.32.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/59b72133-284e-472a-8329-87048637d1f4/Screenshot_2021-02-04_at_13.49.49.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/59b72133-284e-472a-8329-87048637d1f4/Screenshot_2021-02-04_at_13.49.49.png)

in your project directory inside backend folder, if you look into the api folder, you should also see the articles folder, this is basically what we just did on our strapi development server. as we make changes, strapi automatically do stuff to our backend folder, abstracting the need to really have a hard time to code the backend from scratch (unless you want more features).

anyways don't add any articles yet since were still adding other collections such as the categories collection type.

## Create Categories Content Type

since this is itech u know, we want to categorise different articles to categories (hacker, hipster, hustler). 

go back to plugins>content-types-builder

create another new collection type and name it "categories" just like you did for articles.

for the fields of categories content-type:

same rin, has a name (text::short text) field, then make it required and unique field

now, add another field "relation"  and select the icon that represents many-to-many. the text should read, categories has and belongs to many articles. 

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ba3d5aae-2d17-4aa3-b5fd-82bd3127080c/Screenshot_2021-02-04_at_14.07.37.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ba3d5aae-2d17-4aa3-b5fd-82bd3127080c/Screenshot_2021-02-04_at_14.07.37.png)

this is basically an overview on how relational databases work where you have different content types or collections that are related to each other in different ways.

if we go back to the articles content type, we can see a new relational field added that reads as "Articles has and belong to many categories"

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7a1486a6-b03f-4fde-a065-139fbfa678f1/Screenshot_2021-02-04_at_14.11.03.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7a1486a6-b03f-4fde-a065-139fbfa678f1/Screenshot_2021-02-04_at_14.11.03.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5c0a277e-df58-4382-a0a5-1b93a2636192/Screenshot_2021-02-04_at_14.11.42.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5c0a277e-df58-4382-a0a5-1b93a2636192/Screenshot_2021-02-04_at_14.11.42.png)

now were done for categories, here again is an overview of how it should look like for categories content type so you gois can check. anyways once were through with this website, you guys can add extra fields to play around ex: description fields, or even add more collections.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7da08320-d61a-4291-b126-6e39c4d6640f/Screenshot_2021-02-04_at_14.13.54.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7da08320-d61a-4291-b126-6e39c4d6640f/Screenshot_2021-02-04_at_14.13.54.png)

now were forgetting the articles needs authors. hence we must create another collection type called authors.

## Create Authors Content Type

similarly, add the shorttext text field called "name" and make it required and unique.

then as relational field, this should be pointed to the articles content type.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6be745f7-5181-44db-9dcb-1f5c740238f2/Screenshot_2021-02-04_at_14.19.43.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6be745f7-5181-44db-9dcb-1f5c740238f2/Screenshot_2021-02-04_at_14.19.43.png)

the type of relation should be a one to many type of relation that should read as Author belongs to many articles.

now then, seems we got all the collection types we need for now. i guess as a challenge, you guys can too add the courses collection type, and the topics collection type which can be seen in our itech website. for this website, i just want to make this really brief so you can have the necessary understanding and skill to know how to work on these things as you move forward. 

ayt, lets now add the records/data in the different collections.

## Adding the contents to have data

### Adding categories to categories collection

now lets now go to the blue side bar and go to collection types> categories

lets add the hacker, hipster, hustler.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7c8cf5bf-4195-4758-83f3-b1b6207585f5/Screenshot_2021-02-04_at_14.25.58.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7c8cf5bf-4195-4758-83f3-b1b6207585f5/Screenshot_2021-02-04_at_14.25.58.png)

im pretty sure you guys get naman how to add records, pretty self explanatory ;)

### Adding authors to authors collection

for authors, lets just add hackerman, hipsterman, hustlerman? bb-hacker, bb-hipster, bb-hustler? just add any for this tutorial gegege. for this tutorial, imma add bb-hacker, bb-hipster, bb-hustler!

again dont forget to save and publish your record!!

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/41adfa1d-fb62-4580-8bc2-e8c85b98b413/Screenshot_2021-02-04_at_14.29.22.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/41adfa1d-fb62-4580-8bc2-e8c85b98b413/Screenshot_2021-02-04_at_14.29.22.png)

### Adding articles to articles collection type

then for articles. lets just add four articles, add random stuff gegege.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/72691ca8-4441-4bb7-8343-80752d631152/Screenshot_2021-02-04_at_14.34.51.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/72691ca8-4441-4bb7-8343-80752d631152/Screenshot_2021-02-04_at_14.34.51.png)

fill all the following fields, and also if you look to the right, we find select options for the categories and authors this article has and belongs to.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/edb50350-2af7-48ce-9701-84f714bec761/Screenshot_2021-02-04_at_14.37.50.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/edb50350-2af7-48ce-9701-84f714bec761/Screenshot_2021-02-04_at_14.37.50.png)

now thats all done!!. let us now go change roles and permissions so that we can access the data or consume the api of our backend in our frontend.

## Set Roles and Permissions

on our blue sidebar, go to general>settings to go to our settinsg page

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/628a130f-12df-4927-8e04-8085b08babd1/Screenshot_2021-02-04_at_14.39.06.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/628a130f-12df-4927-8e04-8085b08babd1/Screenshot_2021-02-04_at_14.39.06.png)

then the white sidebar, go to users & permissions plugin > roles > public

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/73578243-82f4-47de-962e-222e754c66a6/Screenshot_2021-02-04_at_14.40.14.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/73578243-82f4-47de-962e-222e754c66a6/Screenshot_2021-02-04_at_14.40.14.png)

you should see permissions, select all possible permissions for each content type so that we are able to perform necessary operations we want to do with the data we get from our strapi backend api.

dont forget to save again. and THATS IT FOR THE STRAPI BACKEND FOR NOW!!! let us now do our frontend of our app.

before we go do our frontend, to visualise how this server and apis work. try going to [http://localhost:1337/articles](http://localhost:1337/articles) for example, you should then see our api (that is if you did the permissions correctly, or even have data in your collection which you should have ahhaha.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8cc0d772-c539-4c8e-99f4-48f62df627f6/Screenshot_2021-02-04_at_14.43.19.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8cc0d772-c539-4c8e-99f4-48f62df627f6/Screenshot_2021-02-04_at_14.43.19.png)

at /categories and /authors too can u see the data of the collection. that is basically how servers work ig. 

f as u can see, wrong spelling, double check yall spellings gois gg hahahha

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/bfc32276-56c2-4956-8b07-597e7a30f3eb/Screenshot_2021-02-04_at_14.47.53.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/bfc32276-56c2-4956-8b07-597e7a30f3eb/Screenshot_2021-02-04_at_14.47.53.png)

what we are now trying to do next is to setup the frontend client side (what the users would see), and to consume the api (the data from our server from our database).

let us now proceed.
