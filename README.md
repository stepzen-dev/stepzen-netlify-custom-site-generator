# custom portfolio site generator


We all know it's a pain to have to constantly update your portfolio site -- every time you create a shiny new project, you have to go back into your code and change up your website to display it.

The solution comes in the form of an easy way to keep your site up-to-date, using dynamic, rather than static information. 

Generate your own dynamic portfolio site with this repo!

__________________________________

It presents the solution via a connection to a prebuilt StepZen endpoint with API services for three websites frequently used by devs to strut their stuff: [DEV.to](https://developers.forem.com/api), [Twitter](https://developer.twitter.com/en/docs), and [Github](https://docs.github.com/en/graphql). The website it generates and deploys to Netlify (via the deploy to Netlify button) reads your top DEV.to blog posts, your pinned Github repos, and your pinned tweets, so that the only work you have to do to update your site is change your pins.

[Click here](https://zealous-albattani-13f59a.netlify.app/) to practice using the generator! You'll need your Github and Twitter API keys, as well as a case-sensitive DEV.to username. I suggest entering the name of a user who has Github and Twitter integrated into their DEV.to profile. 

We utilize this [StepZen endpoint](https://graphql.stepzen.com/devto,github,twitter) to give the concept a dynamic twist and keep this a no-code solution. We create the endpoint using StepZen's GraphQL Studio. You can navigate to the main page, and select "Developer Publishing Pack", which makes it possible to access DEV.to, Twitter, and Github APIs from a single endpoint. 

You can then copy/paste the deployed GraphQL endpoint from the upper-right widget-- and be ready to consume the endpoint on the frontend using fetch! 

[Here's the template](https://github.com/stepzen-samples/custom-site-test) that this generator uses, and [here's an example site](https://unruffled-jepsen-48941e.netlify.app/) for you to check out.

> note: The deploy-to-Netlify button/ environment variable logic for this particular portfolio project generator is based on the code in Cassidy William's [blog post](https://css-tricks.com/hack-the-deploy-to-netlify-button-using-environment-variables-to-make-a-customizable-site-generator/), but translates the template to NextJS, and the site generator to AlpineJS. 
