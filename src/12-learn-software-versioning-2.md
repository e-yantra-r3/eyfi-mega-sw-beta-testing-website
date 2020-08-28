<style>
.back{
	position: fixed;
	width: 300px;
	height: 300px;
	top: 50%;
	left: 50%;
    margin-top: auto; 
    margin-left: auto; 
	opacity: 0.15;
	}
.center {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 50%;
}
</style>



<img src="http://mooc.e-yantra.org/img/eYantra_logo.svg" alt="Paris" class="center">

<img src="http://mooc.e-yantra.org/img/EyantraLogoMini.png" class="back">


# Understanding Semantic Versioning Specification

## **A Beginner’s Guide With an Example**

**Author:** Bharghav Bachina, [Medium.com](https://medium.com/bb-tutorials-and-thoughts/understanding-semantic-versioning-spec-635b87397eec)

In software management, we often change our code and all these changes need to be tracked. As our projects grow, all the dependencies of the projects increase as well. If you want to make changes to your project and move forward, you need to make sure all your dependencies works with your current changes as well. We can’t move forward if these dependencies are too tight or loosely defined. This is called dependency hell.





![Image for post](https://miro.medium.com/max/1124/1*WoSWxl7iwLvxZ0ahgj-04A.png)





# **What is Semantic Versioning**

Semantic Versioning is introduced to avoid the dependency hell discussed above and to keep the javascript ecosystem healthy, reliable and secure. Every time we change our package, it is recommended to change the version in package.json.

By following this semantic versioning spec, you let other developers know the extent of your changes and whoever depend on your code can change their code accordingly.



# **Rules**

When you follow this semantic versioning spec, it is recommended to follow these basic rules.

- If you are starting a new project, start your project with version ***0.1.0\*** and increment minor version for each release until its first production release.
- When you are ready for the first production release, release with ***1.0.0\***
- If you are making incompatible changes to your package after the first release, you need to increment the ***MAJOR\*** version. For instance, ***1.0.0\*** becomes ***2.0.0\***
- If you are adding any functionality without any breaking or incompatible changes to your existing package, you need to increment the ***MINOR\*** version. For instance, ***1.0.0\*** becomes ***1.1.0\***
- If you are fixing any bugs without any breaking or incompatible changes to your existing package, you need to increment the ***PATCH\*** version. For instance, ***1.0.0\*** becomes ***1.0.1\***
- If your package is unstable, you should add a ***LABEL\*** indicating that your package doesn’t meet with intended requirements. For instance, ***1.0.0\*** becomes ***1.0.0-beta\*** or ***1.0..0-beta.1\***
- You can add build metadata to this version as well with the ***+\*** appending at the end. For instance, ***1.0.0-beta+1122\***





# **Why Should We Use It**

There are so many advantages to using this spec. Some of them are follows

- It’s easy to track the changes with versions.
- With version numbers, it’s easy to understand the changes with the new release.
- Developers will have the option of going back to the older version if the newer version doesn't work with their code.

# **Example Project**

Let’s put theory into practice by working on the example project.

We have a module called NameUtils with two methods firstName and lastName which takes fullName and gives you first name and last name respectively.

## **First Release**

We have a version **1.0.0** in package.json since we are releasing it for the first time.

**NameUtils package**

Let’s publish this module with `npm publish`and check the version in `npmjs.`

**nameutils version 1.0.0**





## **Patch Release**

If we fix any errors, we need to bump up the patch number.

If you look at the `index.js` file. we are returning the first name by splitting the given name by space `name.split(' ')[0].`

You might get an error if the name is not passed to that firstName function. Let’s fix this one and republish with version ***1.0.1.\***

**index.js**

Here is the updated version in the npm

**nameutils version 1.0.1**





## **Minor Release**

If we add any functionality to our existing package with backward-compatible changes, that would be ***minor\*** release.

Let’s add another function called ***getLength()\*** function to give you the length and also add the README.md file as well.



**index.js**

After publishing above changes with version ***1.1.0.\*** Here is the updated version in the npm registry.

**npmutils version 1.1.1 with README.md**



## **Major Release**

If we change any version with breaking changes without backward-compatibility, that would be our ***major\*** release.

I want to change the function names from `firstName` and `lastName` to `getFirstName` and `getLastName` respectively.

This is a major version because whoever uses this package need to change their code. Let’s add and publish it with version ***2.0.0\***

**index.js**

Here is the updated version in the npm

**npmutils 2.0.0**





# **Version History and Precedence**

We can check the version history in npm by going to versions tab like below and you can click on any version to see the details.

**package version history**

Precedence refers to how these versions are compared based on the major, minor, patch and prerelease numbers. For instance, we have 4 versions for our package so our precedence order is ***1.0.0 < 1.0.1 < 1.1.1 < 2.0.0.\***





# **How to Install Specific Versions**

Now we have several versions of our package in npm registry and let’s understand how we can install specific versions and update those accordingly.

If you install the package without any version specified, `npm i nameutils,`npm will install the latest version from the registry. In our case, it’s ***2.0.0\***

If you want to install a specific version, we can use `@` a symbol like this `npm i nameutils@1.1.1`





# **Difference between tilde (~) and caret (^)**

package.json gets updated whenever you install any package with `--save.` Every time when you install or update dependencies, These symbols caret (^) and tilde(~) makes the difference with the versions we are installing.

# **~**

For the specified minor version, ~ will match the most recent patch version. For instance, if you have `~1.3.4` in your package.json file and `1.3.6` and `1.4.0` are available in the npm registry `1.3.6` is installed and hold off with `1.4.0.`

# **^**

For the specified major version, ^ will match the most recent minor version. For instance, if you have `^2.2.0`in your package.json file and `2.3.0`and `3.0.0` are available in the npm registry `2.3.0`is installed and hold off with `3.0.0`





# **Best Practice**

- Never change any contents of the already released version, always release the new version with changes
- If your package is still in unstable mode, better start with the version ***0.x.y.\*** This facilitates rapid development.
- Only release your first version ***1.0.0\*** when it is stable.
- Make sure you have fewer major releases. Major release means breaking changes which include cost and lot of changes to the user who is using your code.
- Always have good README.md file with your release which serves good communication for both users and API providers.
- If you have deprecating changes, always put those in documentation to let the users know the changes.
- You can release a minor version as well with those deprecating changes in place. It facilitates a smooth transition.