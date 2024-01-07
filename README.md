# 50 Essential Next.js Interview Questions

<div>
<p align="center">
<a href="https://devinterview.io/questions/web-and-mobile-development/">
<img src="https://firebasestorage.googleapis.com/v0/b/dev-stack-app.appspot.com/o/github-blog-img%2Fweb-and-mobile-development-github-img.jpg?alt=media&token=1b5eeecc-c9fb-49f5-9e03-50cf2e309555" alt="web-and-mobile-development" width="100%">
</a>
</p>

#### You can also find all 50 answers here 👉 [Devinterview.io - Next.js](https://devinterview.io/questions/web-and-mobile-development/next-interview-questions)

<br>

## 1. What is _Next.js_ and what are its main features?

**Next.js** stands out as a production-grade React framework, offering both speed and specialization. Its versatility, data fetching techniques, search engine optimization (SEO), and various deployment options make it a top choice for modern web development.

### Main Features

1. **Server-Side Rendering (SSR)**: Next.js dynamically generates the HTML on the server for each page request, delivering consistently rendered content to users and ensuring optimal SEO.

2. **Static Site Generation (SSG)**: By pre-computing the HTML of individual pages at the build time, Next.js achieves superior performance and security. It's especially adept at handling content-heavy websites.

3. **Hybrid Rendering**: Combining SSR and SSG, Next.js provides the flexibility to render specific pages during build time (SSG) and others on-demand (SSR). This feature is valuable when creating applications comprising both dynamic and static content.

4.  **Routing**: Opt for either filesystem-based or dynamic routing. The former obviates the need for explicit route definition while the latter enables programmatic control. Both options synergize with SSG and SSR.

5. **Code Splitting**: Out of the box, Next.js identifies separate sections of your app and optimizes the bundling, dispatching only the necessary code (and resources) to clients, benefiting both performance and load times.

6. **Formidable Image Optimization**: Image components from Next.js automate image optimization, ensuring picture quality for varying devices while still upholding rapid load times.

7.  **Instant Deployment**: Rely on services like Vercel for swift, straightforward deployments, A/B testing, and other advanced features.

8. **API Routes**: Embrace Next.js API routes for seamless incorporation of backend resources into your application.

9. **Built-in CSS Support**: With Next.js, you can utilize standard CSS files, CSS modules, or even preprocessors like Sass, all without additional setup.

10. **Vast Plugin Ecosystem**: Extend the functionality of your Next.js project by plugging into a wide array of solutions from the Next.js community.
<br>

## 2. How does _Next.js_ differ from _Create React App_?

Let's look at the key differences between Next.js and Create React App.

### Core Functionality

- **Next.js**: Built-in server-side rendering (SSR) and client-side rendering (CSR). It also supports static site generation (SSG). Offers features like pre-fetching data to enhance performance. Provides integrated API routing.
  
- **Create React App**: Primarily focuses on client-side rendering (CSR). Doesn't provide built-in server-side rendering or advanced rendering modes such as SSG or ISR. Relies on third-party solutions for server-side rendering.

### Routing

- **Next.js**: Offers file-system-based routing, which simplifies route definition. It also supports custom routes. Dynamic routing and **code splitting** are automatic, enhancing performance.
  
- **Create React App**: Utilizes client-side routing with packages like React Router. Routes need to be explicitly defined in a configuration file or as components.

### File Structure and Configuration

- **Next.js**: Employs a zero-configuration model for quick setup. It comes with sensible defaults that promote best practices. Added configuration options can further customize its behavior.
  
- **Create React App**: Similar to Next.js, it uses a zero-configuration approach. Customizations are managed via `react-scripts` and some advanced, but extensive, `eject` configurations. This step irrevocably detaches from the default configuration, making it harder to integrate future updates.

### API Handling

- **Next.js**: Integrates seamless serverless API routes. Developers can design API endpoints using standard HTTP requests. The result is a simplified backend setup without the need for server management or additional server logic.

- **Create React App**: Leverages libraries like Axios or Fetch to interact with backend services. Unlike Next.js, it doesn't have a built-in solution for server-side API routes.

### Code Splitting

- **Next.js**: Automatically code-splits imports across pages and components. This on-demand loading optimizes initial page load times. Furthermore, module-level or even granular control over code splitting are possible.

- **Create React App**: Incorporates the `React.lazy` function and `Suspense` components to facilitate code splitting. Developers need to identify points for code splitting manually.

### Data Fetching

- **Next.js**: Offers numerous approaches for data retrieval, such as `getStaticProps`, `getStaticPaths`, `getServerSideProps`, and client-side methods. These functions are part of the **Data Fetching API** and are tailored for specific rendering strategies.

- **Create React App**: Lacks specialized data-fetching techniques inherent in Next.js. Instead, it integrates with data-fetching libraries or employs traditional strategies such as using `useEffect` in functional components.

### Deployment

- **Next.js**: Provides flexible deployment options. With serverless hosting, deploys are efficient and scalable, especially suited for small to medium projects. Traditional hosting with a Node.js server allows for more extensive customizations.

- **Create React App**: Most suitable for static or single-page applications, often deployed via content delivery networks (CDNs). For dynamic content, it needs to be paired with a backend like a REST API, and then deployed as two distinct applications.

### SEO and Meta-Tags

- **Next.js**: Offers superior support for search engine optimization (SEO). It covers foundational aspects like meta tags, but its advanced rendering modes, such as SSG and ISR, significantly benefit SEO, which is especially critical for content-heavy sites.

- **Create React App**: Lacks built-in mechanisms like SSR or specialized rendering modes for optimizing SEO. Developers have to leverage third-party tools or implement their own solutions to achieve search engine friendliness.
<br>

## 3. What command is used to create a new _Next.js_ app?

To create a new **Next.js** application, you can utilize `npx` in combination with the `create-next-app` package.

```bash
npx create-next-app folder-name
```

Replace **"folder-name"** with your desired workspace directory. Here, `npx` is a package runner that ensures you get the most recent version of `create-next-app`. If you're on Node.js 10 or earlier, you need to install `create-next-app` as a global package:

```bash
npm install -g create-next-app
create-next-app folder-name
```

This method, involving `npm` and a global package, is not recommended for more recent Node.js versions.
<br>

## 4. How does _Next.js_ handle _server-side rendering_ (SSR)?

**Next.js** handles Server-Side Rendering (SSR) through a simple and intuitive mechanism.

### Key Components

- **Page**: Represents the specific route that's being accessed.
- **Route**: A user-defined endpoint corresponding to a specific page or screen.
- **App**: The root of a Next.js application, managing the overall setup and state.

### The SSR Process

1. **Initial Request**: When a user accesses a specific route or page, Next.js intercepts this request.
2. **Data Fetching**: Any necessary page data is fetched, ensuring it's available before the page is rendered.
3. **SSR Render**: Next.js renders the requested page on the server and sends the generated content, including any fetched data, as a response to the user's initial request.

#### Benefit: Immediate Data Display

Since page content and data are rendered on the server and sent in the initial response, users see meaningful content faster, even for dynamic, data-driven pages.

#### Code Example: Basic Next.js Page

Here's the typical structure of a **Next.js** page:

```jsx
import Head from 'next/head';

const SamplePage = ({ data }) => {
  return (
    <div>
      <Head>
        <title>Sample Page</title>
      </Head>
      <h1>Sample Content</h1>
      <p>{data}</p>
    </div>
  );
};

export async function getServerSideProps() {
  // Perform necessary data fetching
  let data = 'Some server-rendered data';
  return { props: { data } };
}

export default SamplePage;
```

In this example:

- The data-fetching function, `getServerSideProps`, ensures the data is available before the page is rendered. This method is specifically for Server-Side Rendering in Next.js.
- The `data` prop, obtained from the data-fetching function, is passed to the `SamplePage` component before its initial rendering. This permits immediate display of relevant data.
- The `Head` component from `next/head` encapsulates metadata specific to the page, such as the title.

### The Data-Hydration Stage

After the initial server-side rendering, the client-side JavaScript takes over. This process involves:

- **Page Navigation**: Whenever the user navigates to a new page within the application.
- **Client-Side Routing**: The browser takes control over route changes, and Next.js manages the synchronization.
- **Data Fetching**: If required, Next.js triggers additional data fetching on the client side for subsequent state updates or dynamic content changes.

#### Code Example: Next.js Link Component

Here is the code:

```jsx
import Link from 'next/link';

const Navigation = () => {
  return (
    <nav>
      <Link href="/about">
        <a>About</a>
      </Link>
      <Link href="/contact">
        <a>Contact</a>
      </Link>
    </nav>
  );
};

export default Navigation;
```

In this example:

- The `Link` component encapsulates anchor tags, ensuring user navigation within the application is efficient and considers both server-rendered content and any subsequent client-rendered updates.

### Optimal User Experience

  - Initial Server Response: Delivers server-rendered content and necessary data in the first request, improving perceived loading times.
  - Enhanced Dynamic User Experience: Seamlessly combines server-rendered content with client-side updates, optimizing page state and content.
<br>

## 5. Can you explain the purpose of the _`pages` directory_ in a _Next.js_ project?

The **`pages` directory** serves as your primary **route definition tool** in a **Next.js app**. Each file within it represents a unique URL.

### Key Features

- **Automatic Routing**: No custom routing is needed. Any file added to `pages` becomes a route.

- **File-Route Mapping**: The file structure under `pages` maps to specific routes. For instance, `pages/post/index.js` is associated with `/post`.

- **Dynamic Routes**: Files using square brackets like `[id].js` allow for dynamic parameters. For example, `pages/post/[id].js` is tied to `/post/:id`.

### Code Example: Pages and Routes

Consider the following file structure:

```plaintext
pages/
  ├── index.js
  │
  ├── post/
  │    └── [id].js
  │
  └── about.js
```

This structure corresponds to the following routes:

- **/index.js**: Serves as the landing page.
- **/post**: Serves the `post` route. Should contain code to handle non-`id` requests.
- **/about.js**: Direct route to the about page and is also treated as a route.

- **/post/abc**:
    - Maps to `pages/post/[id].js` with `id` as "abc".

### Special Roles

Some specific filenames or subdirectories have distinct routing roles.

- **`404.js`**: If present, Next.js uses this file to render a custom 404 page.
- **`_app.js`**: Sits at the top level. It is the master page that wraps other pages. Useful for including global styles or contexts.
- **`_document.js`**: Also on the top level, controls the server-rendered HTML document. Strong for continuous UI across pages.
<br>

## 6. In _Next.js_, how do you create a page that is rendered on the server for every request?

In Next.js, you can configure server-side rendering for pages that **always need fresh data**. A good example is a real-time dashboard or a data-driven landing page.

### Server-Side Rendering (SSR) vs. Static Generation (SG)

- **SSR**: This sends the request to the server on every visit to fetch fresh data and generate the HTML response. This approach is often necessary if the data changes frequently.
- **SG**: All requests serve pre-built HTML, ideal for content that doesn't change upon every visit. However, SG could become inappropriate for certain use-cases where real-time data is a requirement.

### Implementing SSR in Next.js

To enable SSR in Next.js, follow these practical steps:

1. **Configure Your Page's Component**:
   - Along with the standard static `getStaticProps` method, include `getServerSideProps` for server-side rendering.
   - This method runs on **every request**, making it suitable for dynamic data.
   - Ensure you **export** this method within your page component.

2. **Using the Data**:
   - `getServerSideProps` should return the necessary data, as is common for data-fetching methods in Next.js.
   - Data will be available as props to your page component.

3. **Deploy on a System that Supports SSR**:
   - Next.js delivers SSR out-of-the-box, which means you do not need to change any configurations to support this concern.
   - For efficiency, you may utilize a **caching mechanism** to shape data that stays constant between subsequent requests.

### Code Example: Page Requiring Server-Side Rendering

Here is the code:

1. **Page Component**: Pages/ServerSide.js

   ```javascript
   export default function ServerSide({ time }) {
     return <p>Current time: {time}</p>;
   }

   export async function getServerSideProps() {
     return {
       props: {
         time: new Date().toISOString(),
       },
     };
   }
   ```

   This code provides a `time` prop that updates on each request, showcasing server-side rendering.

2. **Linking in Your Application**: ParentComponent.js

   ```javascript
   import Link from 'next/link';

   export default function ParentComponent() {
     return (
       <div>
         <Link href="/ServerSide">Live Time Page</Link>
       </div>
     );
   }
   ```

   Users see the updated time each time they access the "Live Time Page."
<br>

## 7. What file extensions does _Next.js_ support for pages?

**Next.js** allows great flexibility in defining page components, supporting a variety of file extensions.

### Supported Extensions

- `.js`: Traditional JavaScript.
- `.jsx`: React with JavaScript.
- `.ts`: TypeScript.
- `.tsx`: React with TypeScript.

### Text formats

- `.mdx`: MDX for markdown with JSX extensions, enabling interactivity.

### Styling Components

- `.css`: Standard CSS.
- `.module.css`: CSS Modules for local scoping.
- `.scss`: SCSS, with its extended features and nesting.

### Data Fetching

- `.fetch.js`: Client-side data fetching.
- `.fetch.ts`: Client-side TypeScript data fetching.

### Error Handling

- `_error.*`: Special filename used to define custom error pages.

### Examples

- Page using `.jsx` and `.scss`

```jsx
// myPage.jsx
import React from 'react';
import styles from './myPage.module.scss';

const MyPage = () => {
  return <div className={styles.myPage}>Hello, SCSS!</div>;
};

export default MyPage;
```

- MDX file with React components and styling

```jsx
// myMDXPage.mdx
import MyComponent from '../components/MyComponent';
import './myMDXPageStyles.css';

# My MDX Page

<MyComponent />
```
<br>

## 8. How do _environment variables_ work in _Next.js_?

**Environment variables**  in Next.js are used to configure deployment-specific values.

#### Server, Build, and Client-side Env Vars

- **Server**: Required before app/web server starts, e.g., API keys.
- **Build**: For settings during the build process.
- **Client**: For global client-side use. Ensure no sensitive information here.

#### Configuring Environment Variables

1. Create an `.env.local` file in the project's root, listing the key-value pairs, each on a separate line:

   ```plaintext
   DB_HOST=localhost
   DB_USER=myuser
   DB_PASS=mypassword
   ```

2. Access the defined variables in code using `process.env.<VARIABLE_NAME>`:

   ```javascript
   console.log(process.env.DB_HOST);
   ```

3. Secure sensitive information on platforms like Vercel, by using their environment variable management tools.

4. Establishing Default Values: 

   By adding defaults in the code, Next.js ensures the app doesn't break if an environment variable is missing:

   ```javascript
   const dbHost = process.env.DB_HOST || 'localhost';
   ```
<br>

## 9. What is _Automatic Static Optimization_ in _Next.js_?

**Automatic Static Optimization** in **Next.js** enables pages to be automatically prerendered to static HTML as long as they do not fetch data from an external source.

This technique eliminates the need for runtime server rendering when a page only relies on client-side data.

### How It Works

1. **Page Analysis**: During build time, Next.js analyzes each page to determine if it fetches data. If not, the page is marked for static optimization. This often includes pages that only use internal state, client-side libraries, or context.

2. **Prerendering**: For pages marked as static, Next.js generates HTML files during the build process. These optimized pages are then served without requiring server-side rendering.

3. **Data Revalidate**: Static pages can contain stale data. Next.js uses a revalidate strategy to periodically refresh data. This is an ideal trade-off for many applications, balancing performance and data accuracy.

### Use Cases

- **Content Pages**: Ideal for content-rich pages, such as blogs or marketing content, where the data doesn't change frequently and a slight delay in updates is acceptable.
- **Marketing Campaigns**: For promotional campaigns or one-time events, where real-time data isn't a priority and quick initial page loads are crucial.

### Caching and Limitations

- **Client Cache**: Since individual users might be served cached static pages, client-side data can still become out-of-date. Techniques like incremental static regeneration (ISR) offer better freshness guarantees by updating pages at specified intervals.

- **Data Dependencies**: Pages dependent on fresh, external data need server-side or hybrid rendering. Otherwise, they risk serving outdated content.

### Code Example: Using `getStaticProps` & `getServerSideProps`

```javascript
// pages/product/[id].jsx

// Using getStaticProps for static optimization
export async function getStaticProps({ params }) {
  const product = await someFetchFunction(params.id);
  return {
    props: { product },
    revalidate: 10, // Regenerate every 10 seconds for a more updated page
  };
}

// If real-time data is an absolute must, use getServerSideProps instead
export async function getServerSideProps({ params }) {
  const product = await someFetchFunction(params.id);
  return { props: { product } };
}

function Product({ product }) {
  // Render product details
}
```
<br>

## 10. How does _file-based routing_ work in _Next.js_?

File-based routing in Next.js simplifies the organization of web application pages. By adhering to specific file naming conventions in tandem with dedicated folders, developers can seamlessly structure their Next.js projects.

### Mechanism

The presence of **JavaScript or Markdown files** under specific directories signals Next.js to configure pages within the application. For instance, navigational links can be established using file directory structure.

#### Key Directories

- The `pages` directory serves as the **root** where the application pages are located.
-  Secondary folders, such as `pages/blog`, represent **sections** within the application.

#### File Formats

- For a standard page, use a `.js` or `.jsx` extension, or `.ts`/`.tsx` for TypeScript.
-  For blog or documentation-like sections, `.mdx` (Markdown and React hybrid) can be employed, allowing content to render alongside components.

### Benefits and Limitations

#### Benefits:

- **Straightforward Navigation**: The project's structure in the `pages` directory mirrors the website's structure.
- **Modularity**: Sections are self-contained in separate directories, contributing to a more manageable and structured codebase.
- **Isomorphism Support**: The presence of both client- and server-side code fosters web applications that run on both the client and server, enhancing SEO and initial load times.

#### Limitations:

- **Limited to Core Directories**: Unique configurations might necessitate stepping beyond the capabilities of file-based routing, demanding additional setup.
- **Directory Depth Complexity**: Managing a large number of deeply nested directories can be challenging, potentially triggering comprehension or performance issues.

### Code Example: File-Based Routing

Consider a simple e-commerce website. 

Below is the directory structure:

```plaintext
pages/
|__ index.js
|__ cart.js
|__ products/
     |__ index.js
     |__ [product-id].js
```

In the above structure, we see:

- `pages/index.js`: Serves as the landing page.
- `pages/cart.js`: Represents the shopping cart accessible via `yoursite.com/cart`.
- `pages/products/index.js`: Defines the 'Products' landing page.
- `pages/products/[product-id].js`: Corresponds to a product details page, accessible with the product's unique identifier, for example, `yoursite.com/products/123`.
<br>

## 11. How do you create _dynamic routes_ in _Next.js_?

**Dynamic Routes** in **Next.js** allow you to render pages or components based on URL parameters. This feature is useful for scenarios involving user dashboards, blog posts, or product pages, where content is tied to specific, dynamic URLs.

### Route Configuration

- **File Naming Structure**:
  - For top-level dynamic routes, depending on whether it's a page or a client-only route, use `[param].js` or `[param].client.js` respectively. For parameterized routes nested under a directory, the filename format is `[[...slug]].js`.

- **Route** and **Query Parameters**:
  - To capture route parameters, use `[param]` for a single parameter or `[[...slug]]` for chains of parameters.
  - Additionally, you can use the `useRouter` hook or `router` object to extract query parameters like a typical URL query.
  
### Code Example: Dynamic Route Parameter Extraction

Here is the Next.js and React code:

```jsx
// pages/post/[id].js
import { useRouter } from 'next/router';

export default function Post() {
  const router = useRouter();
  const { id } = router.query;

  return <div>Post: {id}</div>;
}
```

The URL `/post/abc` would render "Post: abc".

### URL Configuration

- **Grouped Page Paths**: To group a set of dynamic routes under a shared path segment, define a parameterized `pages/[category]/[id].js` page:
  - Inner pages like `/food/sandwich`, `/drinks/cola`, and so on would be caught within that route.

- **Shallow Routing**: Shallow routing, enabled with the `shallow` option of **`router.push`** or **`next/link`**, keeps query data when navigating:
  - For instance, when on `/view?user=48&page=1` and clicking on `<Link href='/view?user=12'>`, the URL remains `/view?user=12&page=1`.

### Code Example: Shallow Routing

Here is the Next.js and React code:

```jsx
// pages/view.js
import Link from 'next/link';

export default function View() {
  return (
    <div>
      <Link href={{ pathname: '/view', query: { user: 10 } }} shallow>
        <a>User 10</a>
      </Link>
    </div>
  );
}
```

### Tool Recommendations

- **Visual Studio Code** with the **Path Autocomplete** and **vscode-react-docgen** extensions streamlines route and query param management.
<br>

## 12. Explain how to access _URL parameters_ in a dynamic route.

**Next.js** simplifies the process of handling dynamic routes and URL parameters. Here are the steps to access URL parameters in a dynamic route.

### 1. Define a Dynamic Route

For instance, create a dynamic route as `pages/post/[id].js` where `id` denotes the unique identifier you'll extract as the parameter.

### 2. Access the Parameters

To access the parameter, use `router.query` in your component file. Here is the code snippet:

```javascript
import { useRouter } from "next/router";

const DynamicPost = () => {
  const router = useRouter();
  const { id } = router.query;

  return <p>Post ID: {id}</p>;
};

export default DynamicPost;
```

### Use-Cases for Dynamic Parameters

- **Fetching Content**: Ideal for retrieving specific content from a database.
- **Pagination**: Useful for navigating through multiple pages of data.
- **SEO Optimization**: Offers cleaner and more descriptive URLs.
- **Custom URL Structures**: Great for creating custom URL structures catering to unique requirements.
<br>

## 13. Describe the functionality of the _`Link`_ component in _Next.js_.

The **`Link`** component in **Next.js** simplifies client-side navigation within your application, enhancing performance and user experience.

### Key Features

- **Prefetching**: `Link` automatically pre-caches linked pages that the user is likely to visit next. This optimizes load times during navigation.

- **Accessibility**: Assists with navigational cues for screen readers and keyboard users.

- **Code Splitting**: Next.js employs this strategy by default, loading only the JavaScript code necessary for the specific page being visited.

- **Intelligent Routing**: Handles link clicks gracefully, enhancing the user experience by providing polished navigational effects.

### Example: Code Splitting

In the following `Example.tsx`, you can see how Next.js handles code splitting under the hood.

```tsx
import Link from 'next/link';

const Home = () => {
  return (
    <div>
      <h1>Home</h1>
      <Link href="/about">
        <a>About Us</a>
      </Link>
      {/* Other navigational links */}
    </div>
  );
};

export default Home;
```

The `AboutUs` component is only loaded when the user navigates to that specific route, showcasing effective code splitting:

```tsx
const AboutUs = () => {
  return (
    <div>
      <h1>About Us</h1>
      {/* About Us content */}
    </div>
  );
}

export default AboutUs;
```

### When to Use Link Component

The **`Link`** component excels for in-app navigations, particularly when:
- Directing users from one section of an app to another.
- Positive feedback is needed on user actions, such as in form submission success screens.

However, it's not the ideal choice for:
- Opening links in new browser tabs/windows.
- Managing dynamic state or side-effects.
<br>

## 14. How do you handle _catch-all routes_ in _Next.js_?

**Catch-All Routes** in **Next.js** allow dynamic URL matching with flexible path parameters, empowering your app's routing system.

### Key Features

- **Dynamic Parameters**: Access route wildcard segments through the `...` rest parameter.
- **Matching Order**: Definition order determines the route precedence.
- **Fallback behavior**: Optionally configure fallback settings.

### Configuration

Next.js routing file (`pages/foo/[...bar].js`):

- **Root Catch-All**: Load for any unmatched path or `/foo` route without further subpaths.

  ```jsx
  export default function CatchAll() {
    // Logic for Root Catch-All
  }
  ```

- **Nested Catch-Alls**: Triggered when the root path is accessed along with subdirectories.

  ```jsx
  export default function NestedCatchAll() {
    // Logic for Nested Catch-All
  }
  ```

- **Fallback Pages**: Ideal for error handling or awaiting dynamic data.

  ```js
  export async function getServerSideProps() {
    // Data-fetching logic
    return { props: { data } };
  }

  export default function Fallback({ data }) {
    return <div>{data}</div>;
  }
  ```

### Fallback Modes

Specify fallback behavior in the `getStaticPaths` method:

- **True**: Generates paths at build time and handles missing routes as fallbacks (SSG-only).
- **False**: Precisely predefines page paths during build (no fallback).
- **'blocking'**: Handles fallbacks via server at run-time (SSR or SSG).
<br>

## 15. What is `getStaticProps` and when would you use it?

**`getStaticProps`** in Next.js allows you to **pre-render** a page at **build time** by fetching data from an API, database, or any other data source.

However, the static page isn't rebuilt until you trigger a **redeployment**. This makes `getStaticProps` beneficial when content doesn't require frequent updates and can be cached for improved performance.

By choosing **when** content is updated based on a request or a rebuild, you can optimize your build and improve on tasks such as **SEO**.

### When to Use `getStaticProps`

- **Content Persistence**: For content that doesn't change often, like a blog post, where you don't need to rebuild the page every time there's a change.
  
- **Data Fetching**: When data is fetched from a headless CMS, internal API, external services, or databases that are not linked in real-time.

- **Performance**: To benefit from caching and serve pages faster, especially for content that's accessed frequently.

### Code Example: Using `getStaticProps`

Here is the JavaScript code:

```javascript
export async function getStaticProps() {
  // Fetch data from an API
  const res = await fetch('https://example.com/data');
  const data = await res.json();

  // Pass data to the page via props
  return {
    props: { data },
    // Re-generate the page every 60 seconds (optional)
    revalidate: 60,
  };
}

export default function MyStaticPage({ data }) {
  // Render data on the page
  // ...
}
```
<br>



#### Explore all 50 answers here 👉 [Devinterview.io - Next.js](https://devinterview.io/questions/web-and-mobile-development/next-interview-questions)

<br>

<a href="https://devinterview.io/questions/web-and-mobile-development/">
<img src="https://firebasestorage.googleapis.com/v0/b/dev-stack-app.appspot.com/o/github-blog-img%2Fweb-and-mobile-development-github-img.jpg?alt=media&token=1b5eeecc-c9fb-49f5-9e03-50cf2e309555" alt="web-and-mobile-development" width="100%">
</a>
</p>

