# Images & Videos

This directory is now using carousel images from `/public/carousel/` for all visual elements.

> **Note:** All placeholders have been removed and replaced with actual carousel images.

## Current Status

✅ **Using real carousel images** - All sections use actual images from `/public/carousel/`
✅ **No placeholders** - All temporary placeholder files have been deleted
✅ **Server running** - Development server works without errors

## Image Usage

### Carousel Images Used:

- **img1.webp** - Hero video/poster, Testimonial 1
- **img2.webp** - Feature icon (Personal), Testimonial 2
- **img3.webp** - Feature icon (Proven), Testimonial 3
- **img4.webp** - Feature icon (Transformative), CTA background
- **img5.webp** - Intro section image (Joanna)
- **img6.webp** - Private Training path card
- **img7.webp** - Speak & Rise path card
- **img8.webp** - Corporate path card

## Image Mapping

### HeroSection
- Video poster: `/carousel/img1.webp`
- Video source: `/carousel/img1.webp` (fallback)

### IntroSection
- Feature icons: `/carousel/img2.webp`, `/carousel/img3.webp`, `/carousel/img4.webp`
- Joanna's photo: `/carousel/img5.webp`

### PathCard
- Private Training: `/carousel/img6.webp`
- Speak & Rise: `/carousel/img7.webp`
- Corporate: `/carousel/img8.webp`

### TestimonialCard
- Testimonial 1: `/carousel/img1.webp`
- Testimonial 2: `/carousel/img2.webp`
- Testimonial 3: `/carousel/img3.webp`

### CTASection
- Background: `/carousel/img4.webp`

## Current Placeholders

All placeholder files have been created using ImageMagick with solid colors:

- **Hero/CTA backgrounds**: Navy (#1a1a4e) - 1920x1080px
- **Intro section images**: Navy (#1a1a4e) - 500x500px
- **Path cards**: Navy (#1a1a4e) - 400x300px
- **Feature icons**: Gold (#d4952a) - 56x56px
- **Testimonials**: Gold (#d4952a) - 48x48px
- **Hero video**: Simple 3-second loop with navy background

The website will **work perfectly** with these placeholders, but replace them with actual content for production.

## Guidelines

- **File formats**: Current images are WebP format (optimized for web)
- **Optimization**: All carousel images are already web-optimized
- **Naming**: All carousel images are in `/public/carousel/` directory
- **Consistency**: Images work with navy (#1a1a4e), gold (#d4952a), and cream (#faf8f5) color scheme
- **Professional quality**: High-resolution photography throughout

## File Structure

```
/public/
  ├── carousel/
  │   ├── img1.webp (1.5MB) - Hero + Testimonial 1
  │   ├── img2.webp (1.4MB) - Feature icon + Testimonial 2
  │   ├── img3.webp (1.1MB) - Feature icon + Testimonial 3
  │   ├── img4.webp (771KB) - Feature icon + CTA background
  │   ├── img5.webp (1.4MB) - Joanna's photo
  │   ├── img6.webp (1.5MB) - Private Training card
  │   ├── img7.webp (1.5MB) - Speak & Rise card
  │   └── img8.webp (1.4MB) - Corporate card
  └── images/
      └── README.md (this file)
```

## Current Status

✅ **All placeholders deleted** - No temporary files remain
✅ **Using real images** - All sections use carousel images
✅ **Development ready** - Server runs without errors
✅ **Production ready** - Real, high-quality images in use
