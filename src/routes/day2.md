# Day 2 - The basics of Svelte components

Svelte, like many modern Javascript frameworks, are component-based. In its simplest form this means that parts of a Svelte app can be removed from the main file and put in their own file, or "component". This component can then be included back in the main file where ever it is needed.

The best example of this is something like a button. Instead of creating a new button every time we need one, we can create a button "component" and reuse that each time. Let's do exactly this.

### Create a components folder

Back in your project in your code editor, create a new folder in the _src_ folder called _components_. You could call the new folder something else if you wanted, and it doesn't have to be in the _src_ folder but these are good options for this example.

### Create the button

In your new _components_ folder make a new filecalled _Button.svelte_. Notice the filen name starts with a capital "B" which is not essential but is a useful convention when making your own components. The file should end with _.svelte_ which is the default Svelte file extension.

Open your _Button.svelte_ file and add the following:

`<button>My Button</button>`

Save the file. Now re-open your _App.svelte_ file. This is your main file at this stage. We're going to add the new button component to this file.

In between the two _script_ tags add the following:

`import Button from './components/Button.svelte'`

This will import the new Button component from the _Button.svelte_ file.

Now, below the last _div_ tag but before the style tag add the following:

`<Button />`

It should look like this:

<img src="/images/day2/button-add.png" style="width: 450px;">

### Test the component

The new button component shouln now be added to your app. To test this, start up the dev server and view the site:

`npm run dev`

You should now see your button on the main app page below the text.

To test it further, duplicate the component line a few times. If you do this and reload you should see multiple instances of your button.

Back: [Day 1 - Setting up Svelte](/day) | Next: [Day 3](/day3)
