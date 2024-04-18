# Simple Resume Template for Astro

Simplistic text-based resume template utilizing Markdown and [Tailwind CSS](https://tailwindcss.com). Built with [Astro](https://astro.build).

Focused with ease-of-use in mind, you can easily modify all your information from one central location, with the help of Markdown for formatting.

### [Demo Site](https://nikitatran.github.io/astro-simple-resume/)

Feel free to report any issues [here](https://github.com/nikitatran/astro-simple-resume/issues)!

## Features
- Responsiveness for screens > 375px wide
- Markdown for easy text formatting
- [astro-icon](https://github.com/natemoo-re/astro-icon) for easy implementation of SVG icons
- Section navigation
- Displays the last time your page was deployed in the footer
- Auto-detects your system theme on first load
- Dark/Light mode toggle
- Add/remove content (e.g. resume sections, header links) without having to change the HTML code manually
- Everything you need to edit is located in one folder*

<sup>* except for the favicon and astro config</sup>

## UI
Images coming soon!

## Set-up
Clone this repository by using the "Use this template" button at the top of the page, by following [this link](https://github.com/new?template_name=astro-simple-resume&template_owner=nikitatran), or by running this: `npm create astro@latest -- --template nikita-tran/astro-simple-resume`

> [!IMPORTANT]
> In order for your website to deploy to the correct URL, please go to the `astro.config.mjs` file and modify the `site` and `base` field. See [Astro documentation](https://docs.astro.build/en/reference/configuration-reference/#top-level-options) for more details.

After ensuring that your config is correct, execute command `npm run dev` and your project will be serving on host `http://localhost:4321/`. Now you are ready to edit the template! See [How to Edit](#how-to-edit) for details.

## How to edit
Modify the `.md` and `user_info.json` files in the ``src/resume_sections`` folder with your information to populate the template. The contents within the `.md` files correspond to individual sections of your resume (eg. Work History, Education, Certifications, etc.)

### How to make a new resume section
Simply make a new `.md` file in the `src/resume_sections` folder and the page will render a new section.

### How to re-order resume sections
The resume sections are sorted by the filename of the `.md` files (descending order) in the ``src/resume_sections`` folder. I recommend prefixing your `.md` filenames with a number or by alphabet such as `1_sectionname` or `a_sectionname` so that it sorts correctly.

### How to change icons used in the resume header
By default, the resume header uses SVG icons from the Material Design Icons iconset. If you want to change the icons, go to the `user_info.json` file and change the `iconName` value. You can go to [Iconify](https://icon-sets.iconify.design/mdi/) to figure out what icon name to use. Note that you must prefix the name with `mdi:` when referring to an icon from that set.

If you want to use your own custom SVGs or use a different icon set from Iconify, please refer to [astro-icon](https://github.com/natemoo-re/astro-icon?tab=readme-ov-file#usage) documentation.

### How to change favicon
By default, the favicon is located under the `public` folder. You could either replace the contents of the existing `favicon.svg` file with your own svg code, or you could make a new `.svg` file in the `public` folder and change `faviconFilePath` to your new file name.

# Resources used
- [Astro documentation](https://docs.astro.build/en/getting-started/)
- [astro-icon documentation](https://github.com/natemoo-re/astro-icon#astro-icon)
- [Tailwind CSS documentation](https://tailwindcss.com/docs/installation)
- [Last updated time plugin tutorial](https://docs.astro.build/en/recipes/modified-time/)
- [Dark/light mode toggle tutorial](https://docs.astro.build/en/tutorial/6-islands/2/#add-client-side-interactivity)
- [ChatGPT 3.5](https://chat.openai.com) for generating sample text used in demo site