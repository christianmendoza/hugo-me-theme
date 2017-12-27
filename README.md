# Me

Me is a slick, personal layout for any individual wanting a minimal online presence. Features include a big background image or video, logo, bio and icons. The theme also includes functionality for YouTube video backgrounds and Self-Hosted video backgrounds. It is a port of [Me](//onepagelove.com/me) by [One Page Love](//onepagelove.com).

![Hugo Me Theme screenshot](https://raw.githubusercontent.com/christianmendoza/hugo-me-theme/master/images/screenshot.png)


## Installation

Inside the folder of your Hugo site run:

    $ cd themes
    $ git clone https://github.com/christianmendoza/hugo-me-theme

For more information read the official [setup guide](//gohugo.io/overview/installing/) of Hugo.


## Getting started

After installing the Me theme successfully it requires a just a few more steps to get your site finally running.


### The config file

Take a look inside the [`exampleSite`](//github.com/christianmendoza/hugo-me-theme/tree/master/exampleSite) folder of this theme. You'll find a file called [`config.toml`](//github.com/christianmendoza/hugo-me-theme/blob/master/exampleSite/config.toml). To use it, copy the [`config.toml`](//github.com/christianmendoza/hugo-me-theme/blob/master/exampleSite/config.toml) in the root folder of your Hugo site. Feel free to customize this theme as you like.


### Use a background image

Set `enable` to `true`. Add your image to the `static` folder and change `file` to the location of your image accordingly. By default the image position is centered, however you can specify your own by supplying `position` with a valid CSS position.

```toml
[[params.background.image]]
  enable = true
  file = "images/background.jpg"
  position = "center center"
```


### Use a background video

First, disable the image by setting `enable` to `false` in `[params.image.image]`.

Second, enable the video by setting `enable` to `true` in `[params.image.video]`.

You can either use a video that you host or one that is on YouTube.

##### Use your own video

Add your video to the `static` folder and change `file` to the location of your video accordingly. Make sure you delete `youtubeId` or comment it out. 

```toml
[[params.background.image]]
  enable = false
  ...
[params.background.video]
  enable = true
  mute = true
  file = "videos/background.mp4"
  # youtubeId = "dk9uNWPP7EA"
```

##### Use a YouTube video

Get the ID of the YouTube video and add it to `youtubeId`. Make sure you delete `file` or comment it out. 

```toml
[[params.visual.image]]
  enable = false
  ...
[params.visual.video]
  enable = true
  mute = true
  # file = "videos/background.mp4"
  youtubeId = "dk9uNWPP7EA"
```

##### Additional settings

Set `mute` to `true` if you want the video to play muted and `false` if you want the sound. The video is coded to autoplay and loop. If you want to change that the code can be found in [`layouts/partials/video.html`](//github.com/christianmendoza/hugo-me-theme/tree/master/layouts/partials/video.html).


### Add logo

Add your logo image to the `static` folder and change `logo` to the location of your logo image accordingly. Set its alt text with `logoAlt`.

```toml
logo = "images/logo.png"
logoAlt = "Logo"
```


### Add bio

Add your bio with `bio`. Use markdown to add any links.

```toml
bio = "This is me. I push pixels at [Google](//google.com), write words on [Medium](//medium.com) and spill thoughts on [Twitter](//twitter.com)."
```


### Add social icon links

Add icons to your social media properties. Change `className`, `url`, and `icon` accordingly. Follow the same icon snippet structure to add more icon links. Remove any icon snippets of those you don't want.

```toml
[[params.social.icon]]
  className = "icon-twitter"
  url = "https://www.twitter.com"
  icon = "M18.258,3.266c-0.693,0.405-1.46,0.698-2.277,0.857c-0.653-0.686-1.586-1.115-2.618-1.115c-1.98,0-3.586,1.581-3.586,3.53c0,0.276,0.031,0.545,0.092,0.805C6.888,7.195,4.245,5.79,2.476,3.654C2.167,4.176,1.99,4.781,1.99,5.429c0,1.224,0.633,2.305,1.596,2.938C2.999,8.349,2.445,8.19,1.961,7.925C1.96,7.94,1.96,7.954,1.96,7.97c0,1.71,1.237,3.138,2.877,3.462c-0.301,0.08-0.617,0.123-0.945,0.123c-0.23,0-0.456-0.021-0.674-0.062c0.456,1.402,1.781,2.422,3.35,2.451c-1.228,0.947-2.773,1.512-4.454,1.512c-0.291,0-0.575-0.016-0.855-0.049c1.588,1,3.473,1.586,5.498,1.586c6.598,0,10.205-5.379,10.205-10.045c0-0.153-0.003-0.305-0.01-0.456c0.7-0.499,1.308-1.12,1.789-1.827c-0.644,0.28-1.334,0.469-2.06,0.555C17.422,4.782,17.99,4.091,18.258,3.266"
```

For the icons refer to [SVG Social Icons](http://svgicons.sparkk.fr/). Click on the icon you want and copy/paste the icon path data `d="<icon-path-data>"` to `icon`.

![SVG Social Icons screenshot](https://image.ibb.co/cxDypm/svg_icons.png)


### Add metadata

`name` and `description` metadata helps search engines with how to display your site in search results. `shareImage` and `twitterHandle` help improves how your content is displayed when your site is shared across social media sites.

```toml
name = "Your Name"
description = "Me is a slick, personal layout for any individual wanting a minimal online presence. Features include a big background image or video, logo, bio and icons."
shareImage = "images/social.jpg"
twitterHandle = "onepagelove"
```


### Add favicon
Replace [`static/favicon.ico`](//github.com/christianmendoza/hugo-me-theme/tree/master/static/favicon.ico) with your favicon. If you don't want just delete `favicon.ico` and the line below.

```toml
favicon = "favicon.ico"
```


### Add copyright
Set `copyright` with the text you want for your copyright.

```toml
copyright = "&copy;2017 Your Name"
```


### Add Google Analytics

Enable Google Analytics by adding your tracking id to `googleAnalytics`. Leave empty or remove if you don't want.

```toml
googleAnalytics = "UA-XXXXXXXX-1"
```


### Nearly finished

In order to see your site in action, run Hugo's built-in local server.

    $ hugo server

Now enter [`localhost:1313`](http://localhost:1313) in the address bar of your browser.


## Contributing

Did you found a bug or got an idea for a new feature? Feel free to use the [issue tracker](//github.com/christianmendoza/hugo-me-theme/issues) to let me know. Or make directly a [pull request](//github.com/christianmendoza/hugo-me-theme/pulls).


## License

The original template is released under the [Creative Commons Attribution 3.0 License](//github.com/christianmendoza/hugo-me-theme/blob/master/LICENSE.md). Please keep the original attribution link when using for your own project. If you'd like to use the template without the attribution, you can check out the license option via the template [author's website](//onepagelove.com/me).


## Annotations

- Original [Me](//onepagelove.com/me) Template by [One Page Love](//onepagelove.com)
- [Dude Image](https://unsplash.com/photos/sok0YssrV5g) by Forrest Cavale
- [Asian Fan Shop Video](http://www.wedistill.io/videos/c0195-1-1) by Galen Crout
- [SVG Social Icons](http://svgicons.sparkk.fr/) by [Baptiste Briel](https://twitter.com/BaptisteBriel)

Also thanks to [Steve Francia](//github.com/spf13) for creating [Hugo](//gohugo.io) and the awesome community around the project.
