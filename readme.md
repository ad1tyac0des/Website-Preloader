# Dynamic Website Preloader

**Implement a professional preloader with just a copy-paste and simple configuration!** This project provides an easy-to-use, customizable preloader that dynamically tracks the loading of assets (images and videos) and updates the progress accordingly.

## Key Benefits

- **Zero coding required**: Simply copy the provided files and adjust the configuration.
- **Fully customizable**: Easily change asset paths, file naming conventions, and styling.
- **Disable scroll during Preloader**: Prevents user interaction until all assets are loaded.
- **Dynamic progress tracking**: Automatically calculates and displays loading progress.
- **Flexible asset handling**: Works with both images and videos.

## Quick Start

1. Create a new project folder with the following structure:
   ```
   YourProject/
   ├── index.html
   ├── style.css
   ├── script.js
   └── Assets/
       ├── Images/
       │   ├── img1.jpg
       │   ├── img2.jpg
       │   └── ...
       └── Videos/
           ├── vid1.mp4
           └── ...
   ```

2. Copy the contents of `index.html`, `style.css`, and `script.js` from this repository into your corresponding files.

3. Place your images and videos in the `Assets/Images/` and `Assets/Videos/` folders respectively.

4. Adjust the `PreloaderConfig` in `script.js` to match your assets (see Configuration section below).

5. Open `index.html` in a web browser to see the preloader in action.

## Configuration

The preloader is configured using the `PreloaderConfig` object in `script.js`. Here's what each property does:

```javascript
const PreloaderConfig = {
    totalVideos: 3,              // Total number of videos to preload
    totalImages: 15,             // Total number of images to preload

    imageBasePath: 'Assets/Images/', // Path to the Images folder
    videoBasePath: 'Assets/Videos/', // Path to the Videos folder

    imagePrefix: 'img',          // Prefix for image filenames
    videoPrefix: 'vid',          // Prefix for video filenames

    imageFileExtension: '.jpg',  // File extension for images
    videoFileExtension: '.mp4',  // File extension for videos

    mainPreloaderSelector: '.preloader',    // CSS selector for the preloader container
    progressBarSelector: '.progress',       // CSS selector for the progress bar
    progressBarStyle: 'width',              // CSS property to animate for progress
    progressTextSelector: '.progress-text', // CSS selector for the progress text

    // ... (other properties are used internally)
};
```

## Asset Naming Convention

Ensure all asset file names and extensions are consistent with the configuration. For example, in this code:

- Images named as: `img1.jpg`, `img2.jpg`, `img3.jpg`, etc.
- Videos named as: `vid1.mp4`, `vid2.mp4`, `vid3.mp4`, etc.

These default naming conventions are based on the following configuration:

```javascript
const PreloaderConfig = {
    // ...
    imagePrefix: 'img',
    videoPrefix: 'vid',
    imageFileExtension: '.jpg',
    videoFileExtension: '.mp4',
    // ...
};
```

If you change these configuration values, make sure to rename your asset files accordingly. For instance, if you set `imagePrefix: 'photo'` and `imageFileExtension: '.png'`, your image files should be named `photo1.png`, `photo2.png`, etc.

Make sure the number of assets matches the `totalImages` and `totalVideos` in the configuration.
## Customization

1. **Styling**: Modify `style.css` to change the appearance of the preloader.
2. **HTML Structure**: Adjust the preloader structure in `index.html` if needed.
3. **Behavior**: Fine-tune the preloader behavior by editing `script.js`.

## Important Notes

- Ensure all asset file names and extensions are consistent with the configuration.
- The preloader disables scrolling until all assets are loaded.
- Check the browser console for loading progress and any warnings.

## Troubleshooting

- If assets aren't loading, check file paths and ensure they match the configuration.
- Verify that the number of assets matches the `totalImages` and `totalVideos` settings.
- If using different file extensions, update the `imageFileExtension` and `videoFileExtension` accordingly.