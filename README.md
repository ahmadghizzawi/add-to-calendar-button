![Add to Calendar Button](https://github.com/add2cal/add-to-calendar-button/blob/main/assets/img/readme-header.png?raw=true)

[![Code Quality](https://img.shields.io/codacy/grade/572c0a102d7b4f39b792439dcd2e8aad/main?style=for-the-badge)](https://app.codacy.com/gh/add2cal/add-to-calendar-button/dashboard)
[![npm Installations Total](https://img.shields.io/npm/dt/add-to-calendar-button?label=npm%20Installations&style=for-the-badge)](https://www.npmjs.com/package/add-to-calendar-button)
[![npm Installations per Month](https://img.shields.io/npm/dm/add-to-calendar-button?label=npm%20Installations%2FMonth&style=for-the-badge)](https://www.npmjs.com/package/add-to-calendar-button)
[![jsDelivr npm Hits](https://img.shields.io/jsdelivr/npm/hm/add-to-calendar-button?label=jsDelivr%20npm%20hits&style=for-the-badge)](https://www.jsdelivr.com/package/npm/add-to-calendar-button)
![npm bundle size](https://img.shields.io/bundlephobia/minzip/add-to-calendar-button?style=for-the-badge)

<br />

# Your next Add to Calendar Button

The convenient JavaScript Web Component, which lets you reliably create beautiful buttons, where people can add events to their calendars.

[![#1 Product of the Day on ProductHunt](https://api.producthunt.com/widgets/embed-image/v1/top-post-badge.svg?post_id=319458&theme=dark&period=daily)](https://www.producthunt.com/products/add-to-calendar-button-generator)

<br /><br />

For everybody, who wants to include a button at their website or app, which enables users to easily add a specific event to their calendars.
It's main goal is to keep this process as easy as possible at maximum compatibility. Simply define your button configuration and everything else is automatically generated by the script.
Supporting calendars at Apple, Google, Microsoft (365, Outlook, Teams), Yahoo, and generic iCal.

![Supported Calendars: Apple (via iCal), Google, Microsoft (365, Outlook, Teams), Yahoo, generic iCal](https://github.com/add2cal/add-to-calendar-button/blob/main/assets/img/badge-supported-calendars.svg)

The script, since it is a web component, integrates easily with any usual HTML webpage (**VanillaJS** way) as well as popular JavaScript frameworks and libraries like **Angular**, **React**, **Vue**, **Svelte**, and more.

![Supported Technology: Angular, React, Vue, Svelte, and every other project that can load JavaScript](https://github.com/add2cal/add-to-calendar-button/blob/main/assets/img/badge-technology.svg)

In terms of system support, **all modern browsers** (Chrome, Edge, Firefox, Safari) on **Windows, Mac, Android, and iOS** as well as rather restricted webview environments like the **Instagram** in-app browser are supported.

<br /><br />

---

<br />

## ▶️ Demo

See [add-to-calendar-button.com](https://add-to-calendar-button.com/) for a live demo and playground.

And remember to [⭐ **star** this repository](#) in order to stay up-to-date and save it for later! 🤗

[![Remember to star this repository!](https://github.com/add2cal/add-to-calendar-button/blob/main/assets/img/starring.gif?raw=true)](#)

## ✨ Features

Simple and convenient integration of 1 or many buttons, configurable directly within the HTML code.

### Supported Calendars

- **Google** Calendar.
- **Apple** Calendar.
- **Yahoo** Calender.
- **Microsoft 365, Outlook, and Teams**.
- Automatically generated **iCal/ics** files (for all other calendars and cases).

### Event Types

- Timed and all-day events.
- One-time, multi-date, recurring.
- Calendar subscription.
- Most robust time zone and daylight saving management (via our own [TimeZones iCal Library](https://github.com/add2cal/timezones-ical-library)).
- Dynamic dates (like "today + 3").

### Look

- Beautiful and adjustable UI.
- Light and dark mode.
- Multiple themes.

### Accessibility

- Optimized and adjustable UX (for desktop and mobile).
- Dynamic dropdown positioning.
- Taking care of all those edge cases, where some scenarios do not support specific setups (like WebView blocking downloads); utilizing beautiful user guidance workarounds.
- Auto-generated Schema.org rich (structured) data for better SEO.
- Full support for mouse, touch, or keyboard input (W3C WAI compliant).
- Supporting 20+ languages, incl. RTL text for Arabic; but also custom labels and text blocks (i18n).

### And much more

- Well documented code, to easily understand the processes and build on top of it.
- No external service or backend dependencies.
- Fully GDPR, CCPA, and LGPD compliant by design - without the need of signing some data processing agreement.
- FREE and easy.

![Demo Screenshot](https://github.com/add2cal/add-to-calendar-button/blob/main/assets/img/demo.gif?raw=true)

<br />

---

<br />

## 📦 Installation / Setup

### Option 1: simple (CDN)

You can use the jsDelivr CDN and load the respective script directly into your website.

Place the script tag inside the `<head>` section.

```html
<script src="https://cdn.jsdelivr.net/npm/add-to-calendar-button@2" async defer></script>
```

<br />

### Option 2: npm

Import the package using the following npm command:

```sh
npm install add-to-calendar-button
```

Import the module into your project/component

```javascript
import 'add-to-calendar-button';
```

Based on your framework/library, you might need to make minor adjustments to the respective config.
Find the details for the most common ones below.

<br />

#### Angular

At the `app.module.ts`, import `CUSTOM_ELEMENTS_SCHEMA` from `@angular/core` and add the following to the `@NgModule` block:

```javascript
@NgModule({
  //(...),
  schemas: [CUSTOM_ELEMENTS_SCHEMA],
})
```

<br />

#### React

**Option A:**

With basic React projects, the web component works out-of-the-box.

If you are working with TypeScript or other stricter setups, you would need to define a respective global JSX interface.

```typescript
declare global {
  namespace JSX {
    interface IntrinsicElements {
      ['add-to-calendar-button']: CustomElement<AddToCalendarButton>;
    }
  }
}
```

**Option B:**

If this does not work OR if you want to keep it more convenient, you should use [the official Add to Calendar Button React Wrapper (click here)](https://github.com/add2cal/add-to-calendar-button-react).

This approach also enables you to provide object and array type props as objects and arrays.
Find all further information within the wrapper repository's Readme file.

<br />

#### Vue 3

In the `vite.config.js/ts`, add the following compiler option to treat all tags with a dash as custom elements and get rid of the warning. Anything else works out-of-the-box.

```javascript
compilerOptions: {
  isCustomElement: (tag) => tag.includes('-')
}
```

If you want to be more precise, you can also write something like `tag.startsWith('add-')` to apply this rule only to tags starting with "add-".

<br />

#### Svelte

Works out-of-the-box. Nice!

<br />

#### Astro

For Astro as well as other SSR setups, you might want to include the script from the CDN rather than working with the npm package!

If you still want to go for the npm way, you would need to add something like this to your page (instead of the import statement):

```javascript
<script type="module" hoist>
  const observer = new IntersectionObserver((entries) => {
    for (const entry of entries) {
      if (!entry.isIntersecting) continue;
      observer.disconnect();
      import('../../node_modules/add-to-calendar-button/dist/module/index.js');
    }
  });
  const instances = document.querySelectorAll('add-to-calendar-button');
  for (const instance of instances) observer.observe(instance);
</script>
```

<br /><br />

## 🎛️ Configuration

A button can be easily created by using the respective custom element.

```html
<add-to-calendar-button></add-to-calendar-button>
```

You can then configure the button by simply adding the options as attributes to it. Boolean values (true/false) can be set as `optionName="true"` or simply by adding `optionName` to the tag. Not setting it at all would be automatically translate to "false".

Theoretically, you could also add all the configuration as JSON structured String by placing this string as the TextContent of the tag. This is mainly due to backwards compatibility reasons and no longer recommended, since it also does not detect changes!

<br />

### Minimal structure (required)

Mind that for auto-generating rich snippets, a location would be mandatory as well.

A time zone is not required, but recommended.

```html
<add-to-calendar-button
  name="Add the title of your event"
  startDate="2022-02-21"
  options="['Google']"
>
</add-to-calendar-button>
```

<br />

### A more powerful example

```html
<add-to-calendar-button
  name="Add the title of your event"
  description="A nice description does not hurt"
  startDate="2022-02-21"
  endDate="2022-03-24"
  startTime="10:13"
  endTime="17:57"
  location="Somewhere over the rainbow"
  options="['Apple','Google','iCal','Microsoft365','Outlook.com','Yahoo']"
  timeZone="Europe/Berlin"
  trigger="click"
  inline
  listStyle="modal"
  iCalFileName="Reminder-Event"
>
</add-to-calendar-button>
```

<br />

You can find more examples as well as an interactive playground at the demo page: [add-to-calendar-button.com](https://add-to-calendar-button.com).

<br /><br />

### All options and features

Find all information about the available attributes and how to configure specific features on the demo page at [add-to-calendar-button.com/en/configuration](https://add-to-calendar-button.com/en/configuration).

<br />

---

<br />

## ⚡ Changelog

![npm Version](https://img.shields.io/npm/v/add-to-calendar-button?label=current%20version&style=for-the-badge)
[![Build Status](https://img.shields.io/github/actions/workflow/status/add2cal/add-to-calendar-button/npm-publish.yml?label=build&style=for-the-badge)](https://github.com/add2cal/add-to-calendar-button/actions/workflows/npm-publish.yml)

Find all changes in the dedicated file at [CHANGELOG.md](CHANGELOG.md).

<br />

## 🙌 Contributing

Anyone is welcome to contribute, but mind the [guidelines](.github/CONTRIBUTING.md):

- [Bug reports](.github/CONTRIBUTING.md#bugs)
- [Feature requests](.github/CONTRIBUTING.md#features)
- [Pull requests](.github/CONTRIBUTING.md#pull-requests)

**IMPORTANT NOTE:** Run `npm install` and `npm run format` to auto-lint!

<br />

## 📃 Copyright and License

Copyright (c) [Jens Kuerschner](https://jenskuerschner.de).

Licensed under [Elastic License 2.0 (ELv2)](LICENSE.txt).

**About open-source**:
We consider ourselves open-source.
However, we are also aware of the controversy coming with licenses like the one selected.
Therefore, and contrary to many other companies and products, we no longer use the term in any marketing statements unless it is about other pieces which really are under an official OSI license.

Speaking **about the license**:
We love it, because it is so simple. Have a look!
You are basically free to do anything unless you are not offering the tool itself as a product or service; or want to remove copyright and license stuff.
In doubt, simply ask and we find a way. :)

<br />

---

<br />

## 💜 Kudos go to

[uxwing.com](https://uxwing.com) as well as all contributors:

<a href="https://github.com/jekuer"><img src="https://avatars.githubusercontent.com/u/8572883?v=4" title="jekuer" width="60" height="60"></a>
<a href="https://github.com/add-to-calendar"><img src="https://avatars.githubusercontent.com/u/110406429?s=96&v=4" title="add-to-calendar" width="60" height="60"></a>
<a href="https://github.com/chadoh"><img src="https://avatars.githubusercontent.com/u/221614?v=4" title="chadoh" width="60" height="60"></a>
<a href="https://github.com/turcuciprian"><img src="https://avatars.githubusercontent.com/u/3309840?v=4" title="turcuciprian" width="60" height="60"></a>
<a href="https://github.com/lizakorab"><img src="https://avatars.githubusercontent.com/u/72821189?v=4" title="lizakorab" width="60" height="60"></a>
<a href="https://github.com/bryan-brancotte"><img src="https://avatars.githubusercontent.com/u/11556772?v=4" title="bryan-brancotte" width="60" height="60"></a>
<a href="https://github.com/nticaric"><img src="https://avatars.githubusercontent.com/u/824840?v=4" title="nticaric" width="60" height="60"></a>
<a href="https://github.com/Ortovoxx"><img src="https://avatars.githubusercontent.com/u/56805259?v=4" title="Ortovoxx" width="60" height="60"></a>
<a href="https://github.com/emilebosch"><img src="https://avatars.githubusercontent.com/u/303135?v=4" title="emilebosch" width="60" height="60"></a>
<a href="https://github.com/killerrin"><img src="https://avatars.githubusercontent.com/u/3269687?v=4" title="killerrin" width="60" height="60"></a>
<a href="https://github.com/acm-will"><img src="https://avatars.githubusercontent.com/u/103984058?v=4" title="acm-will" width="60" height="60"></a>
<a href="https://github.com/ssaaiidd"><img src="https://avatars.githubusercontent.com/u/29234802?v=4" title="ssaaiidd" width="60" height="60"></a>
<a href="https://github.com/c0rychu"><img src="https://avatars.githubusercontent.com/u/55235141?v=4" title="Cory Chu" width="60" height="60"></a>
<a href="https://github.com/Denperidge"><img src="https://avatars.githubusercontent.com/u/27348469?v=4" title="Cat" width="60" height="60"></a>
<a href="https://github.com/apps/dependabot"><img src="https://avatars.githubusercontent.com/in/29110?v=4" title="dependabot[bot]" width="60" height="60"></a>

<br />
