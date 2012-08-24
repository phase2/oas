The Open App Standard: Guidelines for the Creation, Use, and Distribution of Drupal Apps
----------------------------------------------------------------------------------------

### I. Goals

The goal for the Open App Standard is to define the purpose and high level components of an App infrastructure in Drupal, and to define the technical protocols required for the creation, use, and distribution of apps in the community and larger marketplace. Beyond creating a forum for best practices around apps, the high level goal of the project is to achieve interoperability of apps between sites so that the Drupal platform does not become fragmented as specific distributions become widely adopted. That is, an app which conforms to the open app standard will be capable of being installed onto any site which conforms to the same standard. Further, an open app standard should serve to facilitate greater community contribution, by eliminating any confusion about apps and their purpose, by making them easy to build, and by creating opportunities for community members to both contribute to and benefit from the Drupal distributions and platforms in the marketplace today.

### II. Components of the Open App Standard

The Open App Standard aims to provide definitions, technical specifications, and best practices around creating, using and distributing apps in Drupal. In particular, the standard aims to provide the following: 

* Definition of an “app” 
* Reasoning behind apps in Drupal 
* Definition of components and key stakeholders in the Apps ecosystem 
* Definition of the Apps API Architecture 
* Best practices around how an App is created, contributed, and shared 
* Best practices around how an App “marketplace” is constructed, owned, and operated 
* A common understanding and agreement of what elements of the Apps ecosystem belong to the open source community 
* Accepted practices for interacting with 3rd party service providers in building and selling Apps 
* Framework for enforcing best practices to ensure Drupal community needs

### III. Participants in the Open App Standard

The Open App Standard is a collaborative project initiated by the following organizations. Additional organizations interested in collaborating on this project are invited to join the discussion and participate in the development of the standard. The organizing participants are: 

* Phase2 Technology http://www.phase2technology.com
* Linnovate
* Pantheon
* LevelTen


### IV. Apps: An Introduction

The purpose of this section is to introduce the concept of “apps” in Drupal.

#### What is an app?

Before we say what an App is it’s helpful to know who it’s for: An App is for the end user, typically a non-technical user of a Drupal site such as the site administrator. These are the users we are thinking about when we discuss Apps: An App is an installable package which solves a concrete task specific use-case. The complexity of its installation should be hidden as much as possible keeping the process uniform and simple. The goal of the App concept is to make extending the functionality of a Drupal site with discrete functions in a polished, “user friendly” way its main goal. An App is a piece of packaged functionality. Upon installation, an App delivers a polished solution for a specific need. The goal of the “Apps” module is to reduce the number of steps required of users from discovery to usability for functionality for their Drupal sites. By creating a specific protocol for installing and configuring apps, we’ll streamline the end-user experience, making Drupal functionality more “pluggable” and inherently easier to use. Technically, an App is a collection of new or existing Drupal functionality, including Modules, Features, and Themes along with some simple additional code that publishes the existence of the App to the rest of the App infrastructure. What distinguishes an App from a Module or Feature is that the App includes all of the additional polish, end-user UI, configuration UI, sample content, and documentation that are needed to fully meet a specific need. Whereas Modules and Features are more developer-centric and provide building blocks for larger functionality, Apps are larger blocks of completed functionality. Unlike a Distribution or Product, one App only solves one specific problem. A collection of Apps might be seen as a full Product, just as a collection of Modules and Features might be seen as a Distribution.

#### What is the purpose of an app?

The primary purpose of an app is to simplify and make consistent the discovery, installation, setup and use of a specific piece of functionality on a Drupal site. Examples include a Mailchimp app, which synchronises site users with a MailChimp list, a Project Mapper app that provides geolocation around specific projects for an organization, and then displays them on a map, or an ImageSlideshow app, which displays your images in a slideshow.

### The App Philosophy

#### Why do apps exist?

There are a couple of things about Apps that are important to understand. First, that apps exist to solve specific problems for specific users. And second, that apps are generally built for the benefit of Drupal consumers, as opposed to modules which are generally built for the benefit of developers or site builders. To explain further:

##### Apps exist to solve specific problems for specific users.

To be clear from the beginning: the Drupal framework for creating functionality (modules), for creating specific designs (themes), and for delivering combinations of functionality and design (distributions) is a solid framework, from which the concept of “apps” does not deviate, fork, or undermine. Rather, apps adds another piece to this framework – the ability to solve very specific problems, for very specific end-users in a highly user-friendly way, using Drupal. Apps do not seek to add blanketing functionality to every part of a site, or to provide multi-function solutions to complex problems. Apps resolve discrete, specific needs for very specific groups of users.

##### Apps are built for Drupal consumers:

First, let’s clarify the concept of “Drupal consumer.” A Drupal consumer is a site builder or site administrator or site owner (such as a Blogger) who is using a Drupal site. Drupal consumers are often not comfortable working in the code of a web site and may not have the knowledge to do so. These consumers are not visitors to sites, but rather, the owners/administrators who make decisions about what content and functionality they need for their site, and require a solution to provide it. Consumers & end users are a picky bunch. They say things like ‘it’s almost there, but I also need this …’ But in a distribution or a SaaS product, “almost” isn’t good enough. “Almost” is what drives end users ‘back’ to find something else. Borrowing from the Pareto principle, Drupal itself solves 80% of these problems, but consumers of Drupal need that last 20%. Apps can solve this problem, by simplifying the process of adding functionality to one’s Drupal web site.

#### Components of an app:

At a minimum, an app should include the following components: 

* Specific functionality or the connection of the end user to a third party service that provides specific functionality 
* The ability to install, uninstall, enable, & disable, cleanly 
* Settings or configurations for the end user to customize their use of the functionality 
* Descriptions, screenshots, and graphics that tell an end user what the app is, what it does, and how it is used

#### What’s Not an App:

The following are characteristics that preclude something from being an
“app”: 
* It is not a complete solution: if an app only provides raw materials or building blocks, of a solution, it is not a good app. 
* It is trying to solve too many problems, or too big a problem: Apps that install functionality into many different places in a site, or that try to solve a large host of problems, will not be good apps. (e.g. A CRM app would likely be too large a problem to solve)

#### Can any module or theme be an App?

Apps are specific and not broad, in nature – they are designed to solve one problem, solve it well, and solve it completely. Generally, an app will both keep track of data in some way (as a content type, etc) as well as use it or display it in a specific way (on a map, etc). So, an app like “Ideation,” created and contributed by Development Seed, is a great example of an app that solves one problem, solves it well, and solves it completely. Ideation provides feedback functionality for organizations. It solves it well, with a beautiful interface and simple-to-configure set-up, and it solves it completely, giving users the ability to not only suggest ideas, but also give feedback on that idea and rate the idea; and giving administrators the ability to accept or remove ideas from rotation. Many excellent modules would not be considered an app, but perform vital functionality as modules. For instance, modules like CTools or Panels add enormous functionality to a Drupal web site, but perform their function very broadly, and therefore do not fulfill the “specific functionality” guideline for apps.

#### What is the difference between apps and “Features?”

Apps need not be Features, but a really good start for an App is to simply create a Feature. You need a good use case and functionality that can be isolated, self-contained and individually exportable and Features support that. They can contain Content Types, Views, Permission settings, Panels pages, Context/Spaces/Strongarm/Boxes settings, etc. Here are some good resources for learning how to build a good Feature. An App may actually consist of more than one Feature to encourage Features to focus on smaller blocks of general-purpose functionality.

#### How do Apps work with the rest of Drupal?

Apps are designed to work within the Drupal framework, not outside of it. The following diagram outlines how Apps work in concert with the Drupal framework, and how they relate to Drupal Core, modules, Features, distributions, and SaaS platforms.

#### Who can create an app?

App development is open to any member of the community. Apps can be developed by organizations or individuals who want to make their functionality simple to install, configure, and use with Drupal or with a specific distribution of Drupal such as OpenPublic. Organizations who want to integrate their third-party applications should also consider creating an app. Apps that link users to other applications such as analytics, data storage, or social media aggregation can provide new customers to companies seeking integration with open sources CMSs like Drupal distributions.

### V. The Apps Ecosystem

The purpose of this section is to define the components of the “ecosystem” around Drupal apps, and to show the relationship between that ecosystem and the larger Drupal ecosystem.

#### General Concepts:

*App*: a discrete piece of functionality that is focused around managing the UI interactions and data to perform a particular task. e.g. adding a mailchimp signup form block to a page’s region. The process of ‘installing’ an app should be a simple click operation for the end user and the app framework would take care of any underlying dependencies required. 
*App Market*: An app market is the user interface that allows a Drupal site owner to extend the functionality of a site with apps located on a App Serve and provide payment processing and checkout functionality as needed.

#### Technical Components:

*Distributions*: a collection of Drupal code combined with an installation profile to accomplish specific functionality for a user group 
*Apps Manifest Specification*: A technical specification that describes which apps are available, what their dependencies are, and associated information such as descriptions, logos, and screenshots.
*Apps Manifest API*: the bi-directional interface between the App Server and the App Client which mostly consists of requests and deliveries of data that adheres to the Apps Manifest Specification.
*App Server*: An app server is responsible for publishing a catalogue of its apps, synchronising versions with d.o. and other appstores, allow searching over the catalogue, packaging and delivering the apps and providing a payment infrastructure. It is thought appstore servers will be focused on serving a particular domain problem, e.g. Open Public, SubHub, etc. The App Server is a provider of data that adheres to the Apps Manifest Specification. 
*App Client*: An app client would allow the user to browse/discover a remote collection of apps, prompt for any necessary technical and monetary requirements and install them on the chosen site. A process that should convey a simple, robust and secure UX. It is required that the client abstract as much technical information away as possible making the process of using and extending a Drupal installation as simple as possible. It’s likely this would be a module. It is a consumer of data that adheres to the Apps Manifest Specification. Technically, one client could browse multiple “app markets” pointing to different servers, if desired. 
*Apps module*: the open source Drupal module that allows for the installation and use of apps in a Drupal distribution. This is an implementation of an App Client as defined above.

#### Definition of Roles Involved in Apps

*App owner*: the person or organization who owns or maintains the code for the app. 
*3rd party service provider*: a company who provides a service that they would like to make available to a platform’s app consumers through an app. (e.g. if MailChimp wants to sell its services to users of the SubHub platform through an app, MailChimp is the “3rd party service provider”) 
*Platform owner*: the person or organization who owns or maintains a distribution or SaaS platform which utilizes apps or an app market. This owner defines which App Client gets used, and which stores it provides. (e.g. SubHub is the “platform owner” of the SubHub SaaS offering; Phase2 Technology is the “platform owner” of the OpenPublic distribution) 
*App market owner*: the person or organization who hosts an app server, curates a collection of apps for that app market, and makes the app market target specific platforms. Often, a platform owner will also be an app market owner. However, another organization could host an app market and implement it in an instance of an open source Drupal distribution, and in that case, this organization would be the “app market owner,” but not the “platform owner.” 
*App consumers*: app consumers are the site administrators or site builders who make decisions about which functionality to include on their sites. 
*Direct app consumers*: site administrators or builders who are making decisions for their own sites. Indirect app consumers: site builders who are making decisions for their clients’ sites. (e.g. a development shop using OpenPublic to implement sites for public sector clients chooses apps appropriate for each client. This development shop is an “indirect app consumer”)

### VI. The Apps Manifest API

The purpose of this section is to describe the RESTful API between the
server and the client

#### Apps RESTful API Requests

[DRAFT NOTE: This documentation is forthcoming]

#### Apps RESTful API Response

[DRAFT NOTE: This documentation is forthcoming]

#### Apps Manifest Specification

##### General Attributes

**Key**


**Value**


**Name**: The common name description of of your App. Examples: Project Mapper, Ideation, Section Fronts, etc.


**Description**: A more descriptive explanation of the App. This can be many paragraphs if needed. This should be plain text.


**machine_name**: The machine name of the main module. This is most often the name of the folder and the .module file


**Version**: The version number of the App to be displayed in the App Console and Detail page


**Downloadable**: The key in the downloadables array for the main module


**Author**: The name of the App author. Plain text name of person/company/organization.


**author_url**: A URL to the author's homepage/website.


**Screenshots**: This is an array of image URLs. Multiple screenshots will make a slideshow.


**Logo**: URL to the image logo. This is expected to be an icon/logo of 120 x 120px


**Demo Content Module**: The machine name of the module that contains the Demo Content. This module should be included within the the main App module, but it can be provided as a separate downloadable too. When possible this module should make use of the Default Content and Features modules


**Demo Content Description**: A description of what kinds of content and usability the demo content module will provide. This give the user an idea of what to expect when demo content is enabled.


**Dependencies**: These contain the module dependencies for the App. This is a normalized list of all modules keyed by module machine name with a value that represents the module & version. The value string are keys in the downlodables array. These modules will be downloaded into sites/all/modules.


Example:
> "dependencies": {
> "openlayers_views": "openlayers 7.x-2.0-alpha1",
> "openlayers_plus": "openlayers_plus 7.x-1.0-alpha2",
> "feeds": "feeds 7.x-2.0-alpha3",
> "mapbox" : "mapbox 7.x-2.0-alpha0",
> "geofield" : "geofield 7.x-1.0-alpha1",
> "job_scheduler" : "job_scheduler 7.x-2.0-alpha2"
> }


**Libraries**: These contain the 3rd party library dependencies for the App. This is a normalized list of all libraries keyed by library name with a value that represents the library & version. The value string are keys in the downlodables array. These libraries will be downloaded into sites/all/libraries.


Example:
> "libraries" : {
> "openlayers_slim" : "openlayers_slim 1.7"
> }


**Downloadables**: This contains the entire list of all things to be downloaded. The keys in this array represent the values from the dependencies and libraries. The value of these entries is the full URL to the downloadable resource.


Example:
> "downloadables": {
> "openpublic_projects 7.x-1.0-alpha3" : "http://featureserver.phase2technology.com/sites/default/files/fserver/openpublic_projects-7.x-1.0-alpha3.tgz",
> "openlayers 7.x-2.0-alpha1" : "http://ftp.drupal.org/files/projects/openlayers-7.x-2.0-alpha1.tar.gz",
> "openlayers_plus 7.x-1.0-alpha2" : "http://featureserver.phase2technology.com/sites/default/files/fserver/openlayers_plus-7.x-1.0-alpha2.tgz",
> "mapbox 7.x-2.0-alpha0" : "http://ftp.drupal.org/files/projects/mapbox-7.x-2.0-alpha0.tar.gz",
> "feeds 7.x-2.0-alpha3" : "http://ftp.drupal.org/files/projects/feeds-7.x-2.0-alpha3.tar.gz",
> "geofield 7.x-1.0-alpha1" : "http://featureserver.phase2technology.com/sites/default/files/fserver/geofield-7.x-1.0-alpha1.tgz",
> "openlayers_slim 1.7" : "http://appserver.openpublicapp.com/sites/default/files/fserver/openlayers_slim.tgz",
> "job_scheduler 7.x-2.0-alpha2" :"http://ftp.drupal.org/files/projects/job_scheduler-7.x-2.0-alpha2.tar.gz"
> }


**Complete Example**: This is an example of the Project Mapper App manifest


> {
>  "name": "Project Mapper",
>  "description": "Open Public's Project Mapper is a great way to present your work on a beautiful map. It provides you with a landing page that shows > your projects as pins on a map and as a grid of image thumbnails giving your users a quick way to get an overview of your activities. Each project has > its own page for publishing detailed information. You can create new projects by simply logging on to your Open Public Site and filling-out a web > form.",
> "machine_name" : "openpublic_projects",
>  "version" : "1.0-beta1",
>  "downloadable" : "openpublic_projects 7.x-1.0-alpha3",
>  "author" : "Development Seed",
>  "author_url" : "http://www.developmentseed.org",
>  "screenshots" : ["http://appserver.openpublicapp.com/sites/default/files/apps/project-mapper-screenshot1.jpg"],
>  "logo" : "http://appserver.openpublicapp.com/sites/default/files/apps/project-mapper-logo.png",
>  "demo content module": "openpublic_projects_demo_content",
>  "demo content description": "Pre-loaded content to assist in easier demonstration of the app. Once switched off, the demo content is removed from all > areas of the public web site, allowing users to populate the site with their own content.",
>  "dependencies": {
>    "openlayers_views": "openlayers 7.x-2.0-alpha1",
>    "openlayers_plus": "openlayers_plus 7.x-1.0-alpha2",
>    "feeds": "feeds 7.x-2.0-alpha3",
>    "mapbox" : "mapbox 7.x-2.0-alpha0",
>    "geofield" : "geofield 7.x-1.0-alpha1",
>    "job_scheduler" : "job_scheduler 7.x-2.0-alpha2"
>  },
>  "libraries" : {
>    "openlayers_slim" : "openlayers_slim 1.7"
>  },
>  "downloadables": {
>    "openpublic_projects 7.x-1.0-alpha3" : "http://featureserver.phase2technology.com/sites/default/files/fserver/openpublic_projects-7.x-1.0-alpha3.tgz",
>    "openlayers 7.x-2.0-alpha1" : "http://ftp.drupal.org/files/projects/openlayers-7.x-2.0-alpha1.tar.gz",
>    "openlayers_plus 7.x-1.0-alpha2" : "http://featureserver.phase2technology.com/sites/default/files/fserver/openlayers_plus-7.x-1.0-alpha2.tgz",
>    "mapbox 7.x-2.0-alpha0" : "http://ftp.drupal.org/files/projects/mapbox-7.x-2.0-alpha0.tar.gz",
>    "feeds 7.x-2.0-alpha3" : "http://ftp.drupal.org/files/projects/feeds-7.x-2.0-alpha3.tar.gz",
>    "geofield 7.x-1.0-alpha1" : "http://featureserver.phase2technology.com/sites/default/files/fserver/geofield-7.x-1.0-alpha1.tgz",
>    "openlayers_slim 1.7" : "http://appserver.openpublicapp.com/sites/default/files/fserver/openlayers_slim.tgz",
>    "job_scheduler 7.x-2.0-alpha2" :"http://ftp.drupal.org/files/projects/job_scheduler-7.x-2.0-alpha2.tar.gz"
>  }
> }

### VII. Best Practices for Creating Apps

The purpose of this section is to describe how apps are created and
built. These are best practices that are enforced by the App Server
Owner.

#### How do you create an app?

Creating Apps for OpenPublic follows the same process as creating
modules for Drupal. The difference is that apps are Features-based and
KIT-compliant, and often bundle together configuration forms, demo
content, and other functionality to ensure that they’re simple to
implement with a single click. Here’s how to do it:

##### Plan for your App.

As you’re determining the app you’d like to build, a litte pre-planning
is key. Consider the following: \* What is the specific problem you’re
trying to solve with this app? Does this need apply to many people? \*
Is there an existing app that is solving this problem already? \* If
there is an existing app, why would you not use that? What is it missing
or unable to accomplish? Define your app, so that it: \* Solves a
specific problem \* Solves it completely \* Does not solve anything else
For help with planning your app, the [How to Build an App section on the
Phase2 Technology product platform site][] may be a great place to
start. Use this opportunity to refine your plan and ensure that there is
a need in the community for it.

##### Create or locate the main module for your app.

Creating the main module for your app is not unlike general module
creation for Drupal. Here are a few specifications: \* Your main app
module should be Features-based. Documentation and instructions for
packaging modules as features can be found here:
http://drupal.org/node/580026 \* Your main app module should be
KIT-Compliant. The KIT specification for Features can be found here: 1.
http://drupal.org/project/kit 2.
http://drupalcode.org/project/kit.git/blob\_plain/refs/heads/master:/kitf.txt
You’ll find the Apps API at apps.api.txt. Apps uses the standard hooks
architecture of Drupal for its API. For your app, you’ll need to
implement thehook\_apps\_app\_info in the module.

##### Create or collect enhancements for your app.

These are optional elements of an app, but will may be important to
ensuring usability, which is important for any app. Consider the
following: \* Create a config form that will live in the Apps interface
for controlling how your App functions. Using the Form API Quickstart
Guide will make this easier:http://drupal.org/node/751826 \* Create a
demo content module to bundle with your module that does the following:
1. When enabled, places content on the site that demonstrates the
feature set of your app 2. When disabled, removes all demo content

##### Ensure compliance.

Make sure that your app meets the stability, reliability, and compliance
requirements necessary for Apps.

##### Documentation for Submission.

Create and compile the necessary submission information (see below)

#### The App Specific Hook

This can be found in modules/apps/apps.api.php In order to provide a
more integrated experience to the App console your app should implement
hook\_apps\_app\_info. This module allows you to describe certain
aspects of your Apps functionality to the App Console. This hook is to
return an array with the following information:

  [How to Build an App section on the Phase2 Technology product platform
  site]: http://products.phase2technology.com/display/commondocumentation/How+to+Build+an+App


**demo content description**: This tells what the App demo content will do. It is placed on the configure form along with the mechanism for enabling/disabling the demo content.


**demo content module**: The preferred way for an app to provide demo content is to have a module that when enabled will add demo content, and when disabled will remove demo content. This module should be a submodule of the App but it is not required. If it is not a submodule of the main App module it should be part of the manifest dependent modules.


**demo content enabled**: If demo content is provided as part of an existing module, then this will be the function call that should return TRUE if demo content is currently enabled, FALSE otherwise.


**demo content enable**: If demo content is provided as part of an existing module, then this will be the function call that will enable/install the demo content and should return TRUE if it was successful.


**demo content disable**: If demo content is provided as part of an existing module, then this will be the function call that will disable/uninstall the demo content and should return TRUE if it was successful.


**configure form**: This should be a function that will return a Form API (FAPI) array that will be rendered in the Apps' App Console configure form.


**post install callback**: This will be a function that will be called after the App is enabled initially or if the app has been uninstalled.

#### Submitting an App to an App Server:

##### Where to Submit:

Submit your app according to the specific requirements of the
distribution.

##### What You Need to Provide:

Submitting should be a tarball with a manifest.app file as well as any
image referenced in the manifest <a name="manifest"></a> The
manifest.app should be an ini file with the following items

> name = Test App
> description = Test App is used to show how apps work
> machine_name = test_app
> version = 1.0
> downloadable = test_app 1.0
> author = Phase2 Techonology
> author_url = http://www.phase2technology.com
> screenshots[] = screenshot.jpg
> screenshots[] = screenshot2.jpg
> logo = logo.png
> dependencies[views] = views 3.0-beta3
> dependencies[ctools] = ctools 1.0-alpha4
> downloadables[views 3.0-beta3] = http://ftp.drupal.org/files/projects/views-7.x-3.0-beta3.tar.gz
> downloadables[ctools 1.0-alpha4] = http://ftp.drupal.org/files/projects/ctools-7.x-1.0-alpha4.tar.gz
> downloadables[test_app 1.0] = http://ftp.drupal.org/files/projects/test_app-7.x-1.0.tar.gz


**Name**: Name of the App (example: Project Mapper)


**Description**: Description that tells what it does and who its for, for the apps listing in the OpenPublic apps server.  (Example: "OpenPublic's Project Mapper is a great way to present your work on a beautiful map. It provides you with a landing page that shows your projects as pins on a map and as a grid of image thumbnails giving your users a quick way to get an overview of your activities. Each project has its own page for publishing detailed information. You can create new projects by simply logging on to your OpenPublic Site and filling-out a web form.")


**Machine name**: name of the main module


**Version**: which version of the app this is. e.g. 1.0-beta1


**Location**: where the main module is found. e.g. http://drupal.org/files/projects/openpublic_projects _7.x-1.0-alpha3.tar.gz


**Author**: who created this app; e.g. Development Seed


**Author URL**: link to the author’s site; e.g http://www.developmentseed.org


**Screenshots**: an array of screen shot relative to the path of the manifest.app  A list of screen shots that will show up in app interface. e.g. http://appserver.openpublicapp.com/sites/default/files/apps/project-mapper-screenshot1.jpg


**Logo**: a logo or icon for the app itself; this path should be relative to the manifest.app path


**Dependencies**: please list all the modules that need to be installed for the App to work; and any modules that those modules depend on. The key is the name of the module, and the value is the name of the downloadable of which it is a part


**Downloadables**: please list all downloadables and the location from which they can be downloaded. Downloadables keys are referenced from the dependencies


If you want to test the app locally then reference the manifest from the module.info:


> apps[local][manifests][] = app/manifest.app


...and place your manifest and images in a subfolder of the module


> app/
> manifest.app
> screenshot.jpg
> screenshot2.jpg
> logo.png

#### Additional Best Practices for Building Apps:

##### KIT compliance:

As we said earlier, we believe Apps to typically function best when implemented as Features. In addition to being a Feature they should be a KIT-compliant Feature to make sure it does not have incompatibilities with other Apps. At it’s basis, KIT is a strategy for naming conventions and component exportable strategies that aim for independence and interoperability. Read more about KIT here.

* KIT Feature Specification: http://pingv.com/blog/kit-best-practices-for-making-drupal-features

##### Demo Content

One of the hardest things about installing new functionality in Drupal is that often times you never know quite how to use it. The demo content functionality of Apps aims to lower the barriers to using an App by providing some default content that can be easily enabled and disabled. Demo content can be implemented in any way you see fit. Some options are: 
* Manually create nodes, taxonomy, menus, etc and track their individual ids so that they can be removed later. 
* Use Feeds to import/export content from included data files (see: Ideation app) 
* Use Default Content to give Nodes machine names and export them with Features \* Use UUID Features to export content into Features for inclusion. There are countless ways to crack this nut; the real goal here though is that you can turn this content on AND OFF. This allows a user to play with content to see how it works and when they are done, disable the module and have all of that installed content disappear so they can start building their own content.

##### Contextual App configuration

Oftentimes with Drupal modules, when you are finished installing you need to track down (if you even know to look) where the modules many configuration forms are. Sometimes they are in admin/config sometimes they are in admin/structure, other times in a more specialized location. The point is that, currently in Drupal, once a module is enabled you need to track down some forms to allow for information gathering and configuration. Drupal 7 makes it a step better by providing a configuration link in the modules page but sometimes you want/need more. Here is where Apps shine, giving you a configuration form presented immediately after enabling your module and in the context of where you read about, downloaded, and enabled your App. At any point in the future you can return to the App Console and find your app and configure it directly form the console. This config form can be use to gather API keys, set permissions or any other thing might need to do. This configuration destination also natively support the enabling/disabling of demo content.

### Roadmap for future work by the Open App Standard Working Group

The Open App Standard Working Group will continue exploring concepts around Apps in Drupal, starting with gathering community feedback and interest in the draft here, and continuing to cover more aspects of the Apps ecosystem. The following are a few areas the working group is considering:

#### Questions around Monetizing Apps

Of interest to many community members is how to effectively monetize an App, or create an "app market," or market. A few app marketplaces and app servers exist now, and inevitably, more will arise. After learning about the ways community members are building and using Apps, we'll collaborate to define the architecture and best practices around a monetized App market. Among the many questions that will arise, we anticipate the following:


*   What is the architecture of an App market?
*   How do you create an Apps market?
*   Who can create an App market?
*   How do third party service providers provide their services through an App market?
*   Where are App markets housed, hosted, and located?
*   How exactly does an App market transaction take place? Where are the points where money/ code/ services/ permission/license can change hands?
*   Who runs an App market?
*   Where/when can there be multiple App markets?
*   How does each player in the Apps Ecosystem interact with the market?
*   What are the potential costs, risks, and benefits to each player in the market?
*   What does the App consumer see in the transaction?

#### Considerations around Apps in an open source community

Apps, and how they are potentially monetized, in an open source community is of course something that creates questions and challenges. As a group, we’ll seek to address the challenges around the “Apps” concept in an open source community, and to offer best practices around community contribution and participation. Among those questions: 


*   Does Apps create a "new class" of functionality in the community?
*   Can anyone create an app market in a distribution? How?
*   What components of the Apps ecosystem are open source?
*   Who maintains the open source components of the ecosystem?
*   Is there a single "Drupal App Market?" Could there be? What are the community implications?