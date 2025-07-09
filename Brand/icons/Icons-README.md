## Files created using https://realfavicongenerator.net/ with `knots-favicon-master-1024.png` as the input
`og-image-1200x630.png` added manually via Figma export
`favicon-no-background.svg` added manually via Figma export

## Avatar files for Discord, X etc.

Use this square 512x512 PNG image as the profile picture for official Knots accounts. Crop accordingly:

- `web-app-manifest-512x512.png`  

---

## How to use in HTML websites

1. Extract the package to `<website-root>/favicon/` (e.g., `https://example.com/favicon/`).

2. Add the following code inside the `<head>` section of your pages:

```html
<link rel="icon" type="image/png" href="/favicon/favicon-96x96.png" sizes="96x96" />
<link rel="icon" type="image/svg+xml" href="/favicon/favicon.svg" />
<link rel="shortcut icon" href="/favicon/favicon.ico" />
<link rel="apple-touch-icon" sizes="180x180" href="/favicon/apple-touch-icon.png" />
<meta name="apple-mobile-web-app-title" content="Knots" />
<link rel="manifest" href="/favicon/site.webmanifest" />
```

---

## How to use in a C++ application

Qt applications typically use `.ico` files on Windows and `.png` files on other platforms.

1. Add the icon files to your Qt resource file (`.qrc`) or keep them accessible in your app directory.

2. Set the window icon in your code:

```cpp
#include <QApplication>
#include <QWidget>
#include <QIcon>

int main(int argc, char *argv[]) {
    QApplication app(argc, argv);

    QWidget window;
    window.setWindowIcon(QIcon(":/icons/favicon.ico")); // or direct path
    window.show();

    return app.exec();
}
```

3. For system tray icons:

```cpp
#include <QSystemTrayIcon>

/ ...

QSystemTrayIcon trayIcon;
trayIcon.setIcon(QIcon(":/icons/favicon.ico"));
trayIcon.show();
```

---

## How to add full-size banner preview to website for social media sharing previews (X, Discord, Facebook, LinkedIn, etc.)

Social platforms use *Open Graph images* when sharing your links. 
See what OG images look like in use: https://preview.ogimage.gallery/?url=github.com
Learn more about OG images here: https://ogp.me/

1. Use the Open Graph preview image `og-image-1200x630.png`.

2. Add the following Open Graph meta tags inside your `<head>`:

```html
<meta property="og:title" content="Knots" />
<meta property="og:type" content="website" />
<meta property="og:url" content="https://example.com" />
<meta property="og:image" content="/favicon/og-image-1200x630.png" />
<meta property="og:image:width" content="1200" />
<meta property="og:image:height" content="630" />
<meta property="og:description" content="Description of your website or product." />
```

---

---

## Other uses

- For SVG use `favicon.svg` as this contains black circle background.
- `favicon-no-background.svg` can be used for just the shape but may not display well in light mode.
- For high res square PNG use `knots-favicon-master-1024.png`

