---
layout: skeleton
title: Making this website
subtitle: 26 August 2020
thumbnail: "/assets/images/making-this-website.png"
---

![Screenshot from the website design process](/assets/images/making-this-website.png "Screenshot from the website design process")

# You must have bought a domain on impulse

Yes.

# Exploring UI theory

Well, other than shopping for domain names, I wanted to learn and practice basic UI/UX prototyping skills. Creating a personal website felt like a reasonable first project in terms of scope.

I took a super basic online course called [Visual Elements of User Interface Design](https://www.coursera.org/learn/visual-elements-user-interface-design) on Coursera, which gave me some idea of what the UI design process looks like. The course also explains how "visual elements" (aka the simplest entities in UIs) influence the user experience through tone, interactiveness, navigation cues, and the like.

For this website, I wanted to make something which looked colourful and fun. I therefore stuck to saturated colours (e.g. the navigation bar) and rounded corners. In terms of the _feel_, however, I added an illusion of mass to certain elements by having their animations imply physical inertia in response to mouse-overs and clicks. Try interacting with the entries in the `Links`, `Projects`, or `Blog` sections!

# Figma is an excellent tool for mockups

I've heard lots of good things about [Figma](https://www.figma.com/). It's basically a UI prototyping tool that runs in your browser. Truth is, I was initially _very_ skeptical about running any intense software in-browser (think Google Sheets) yet Figma completely blew my expectations out of the water. Somehow, the web app manages to be powerful yet fluid. You have to try it to believe it.

![Screencast showing Figma in action](/assets/images/figma.gif "Screencast showing Figma in action")

Anyway, I tried to nail down the exact colours and dimensions in Figma mockups before beginning to code. The idea was to focus mostly on pixel-pushing using the Figma GUI, and only later did I switch into the programming flow while wrangling flex boxes.

These were the frames in my Figma project. Of course, the information architecture mirrors the site layout pretty closely.

![Screenshot of various Figma frames](/assets/images/figma-frames.png "Screenshot of various Figma frames")

# Using Jekyll for static site generation

Once upon a time, I hand-coded website pages individually, copying and pasting `nav` blocks dozens of times. These days, you can use a static site generator like [Jekyll](https://jekyllrb.com/) to minimise grunt work like this. I found the workflow to be pretty slick. You can make compose full pages from small, manageable blocks of HTML and CSS. Jekyll compiles it all into a working site.

For instance, in this website, the code for the `Links` and `Blog` section is actually identical – I just chose different inputs for the contents. For `Links` I used a YAML file containing text information. As for `Blog`, I got Jekyll to read a folder and generate the HTML out of each blog post file within. In fact, _every_ single page on this website shares the same site skeleton – namely the header bar, footer bar, page title, and page subtitles in grey.

You also get to write your posts in Markdown instead of HTML, which is nice.

# Conclusion

This is a very simple website, but I acquired some working knowledge of Figma and Jekyll through the process of building it out. I can't wait to use Figma for bigger, more complex projects in the future. Let's see what we can build!

After all, I've already bought the domain name... we might as well deploy something.
