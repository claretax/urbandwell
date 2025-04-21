# UrbanDwell Real Estate Website

A modern real estate website built with Next.js, TypeScript, and Tailwind CSS.

## Image Structure

The project uses the following image structure:

```
/public
  /images
    /properties      # Property images organized by property ID
      /prop-001
        image1.jpg
        image2.jpg
      /prop-002
        image1.jpg
        image2.jpg
    /agents          # Agent profile images
    /logos           # Website logos and branding
    /banners         # Hero banners and section backgrounds
    /blog            # Blog post images
```

## Adding Images

To add images to the project:

1. Place property images in the appropriate property folder under `/public/images/properties/prop-xxx/`
2. Place agent images in `/public/images/agents/`
3. Update the image paths in the data files to reference the actual images

## Image Optimization

This project uses Next.js Image component for automatic image optimization. When adding images:

- Use the `<Image>` component from Next.js
- Specify width and height or use the `fill` property with a parent container that has position relative
- Add appropriate `alt` text for accessibility

## Example Usage

```jsx
import Image from 'next/image'

// For fixed size images
<Image 
  src="/images/properties/prop-001/image1.jpg" 
  width={800} 
  height={600} 
  alt="Modern apartment living room" 
/>

// For responsive images that fill their container
<div className="relative h-64 w-full">
  <Image 
    src="/images/banners/hero.jpg" 
    fill 
    className="object-cover" 
    alt="Beautiful homes in Jaipur" 
  />
</div>
```
