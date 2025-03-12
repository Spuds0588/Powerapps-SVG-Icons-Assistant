
# Using Free Online SVG Icon Libraries in JavaScript

This document provides a detailed guide on how to search for and return icons from various free online SVG icon libraries using JavaScript. The libraries covered in this guide include:

1. [SVG Repo](https://www.svgrepo.com/)
2. [Free SVG Icons](https://freesvgicons.com/)
3. [Iconoir](https://iconoir.com/)

## Prerequisites

To follow along with this guide, you should have a basic understanding of JavaScript and web development concepts. Ensure you have a text editor or an integrated development environment (IDE) to write and run your JavaScript code.

## 1. Querying SVG Repo

SVG Repo offers over 500,000 open-licensed SVG vectors and icons that you can query without needing an API key.

### Code Snippet

```javascript
const searchTerm = 'search';

const querySVGRepo = async (term) => {
  const response = await fetch(`https://www.svgrepo.com/api/search/${term}`);
  const icons = await response.json();
  console.log('SVG Repo Icons:', icons);
};

querySVGRepo(searchTerm);
```

## 2. Querying Free SVG Icons

Free SVG Icons provides a vast collection of open-source SVG icons, including popular sets like Feather Icons, Font Awesome, and Material Design Icons.

### Code Snippet

```javascript
const queryFreeSVGIcons = async (term) => {
  const response = await fetch(`https://freesvgicons.com/api/v1/icons?q=${term}`);
  const icons = await response.json();
  console.log('Free SVG Icons:', icons);
};

queryFreeSVGIcons(searchTerm);
```

## 3. Querying Iconoir

Iconoir is a high-quality selection of free icons available in SVG format. Note that there might be a limit on the number of requests you can make.

### Code Snippet

```javascript
const queryIconoir = async (term) => {
  const response = await fetch(`https://iconoir.com/?search=${term}`);
  const icons = await response.json();
  console.log('Iconoir Icons:', icons);
};

queryIconoir(searchTerm);
```

## Example Code

Here's an example code snippet that queries SVG Repo, Free SVG Icons, and Iconoir, as these libraries do not require an API key:

```javascript
const searchTerm = 'search';

// Query SVG Repo
const querySVGRepo = async (term) => {
  const response = await fetch(`https://www.svgrepo.com/api/search/${term}`);
  const icons = await response.json();
  console.log('SVG Repo Icons:', icons);
};

// Query Free SVG Icons
const queryFreeSVGIcons = async (term) => {
  const response = await fetch(`https://freesvgicons.com/api/v1/icons?q=${term}`);
  const icons = await response.json();
  console.log('Free SVG Icons:', icons);
};

// Query Iconoir
const queryIconoir = async (term) => {
  const response = await fetch(`https://iconoir.com/?search=${term}`);
  const icons = await response.json();
  console.log('Iconoir Icons:', icons);
};

(async () => {
  await querySVGRepo(searchTerm);
  await queryFreeSVGIcons(searchTerm);
  await queryIconoir(searchTerm);
})();
```

This document provides a comprehensive guide to querying free online SVG icon libraries using JavaScript. By following these steps, you can easily search for and retrieve icons for use in your web project
