```markdown
# Detailed Plan for Raja Pathan Barber Shop Website

## Overview
Create a modern, responsive, and stylistic website for Raja Pathan’s barber shop using the existing Next.js 15+ boilerplate with TypeScript, shadcn/ui components, Radix UI primitives, and Tailwind CSS. The website will be clean, professional, and accessible, focusing on typography, colors, spacing, and layout without using any icon libraries or external images.

---

## Feature Set

1. **Landing/Home Page**
   - Hero section with the barber shop name "Raja Pathan Barber Shop" and a tagline.
   - Call-to-action button (e.g., "Book an Appointment" or "Contact Us").
   - A clean, modern hero image placeholder using `<img>` with descriptive alt text.
   - Brief introduction about Raja Pathan and the barber shop.

2. **Services Section**
   - List of offered services (e.g., Haircut, Shaving, Beard Trim).
   - Pricing details for each service.
   - Use cards or panels styled with Tailwind CSS and shadcn/ui components.

3. **Gallery Section**
   - A simple carousel or grid showcasing barber shop photos.
   - Use placeholder images with descriptive alt text.
   - Responsive layout for mobile and desktop.

4. **Booking/Contact Section**
   - A contact form with fields: Name, Email, Phone, Service selection, Preferred Date & Time, and Message.
   - Form validation using React Hook Form.
   - On submission, show success or error toast notifications using Sonner.
   - No backend integration for booking; form submission can be mocked or sent to a simple API route (optional).

5. **About Section**
   - A short biography of Raja Pathan.
   - Philosophy or mission statement of the barber shop.

6. **Footer**
   - Contact information: phone number, email, address.
   - Social media links as text (no icons).
   - Copyright notice.

---

## UI/UX Considerations

- Use Tailwind CSS custom variables for consistent theming (dark/light mode support).
- Responsive design for mobile, tablet, and desktop.
- Accessibility-first approach using Radix UI primitives.
- Clean typography hierarchy with headings, subheadings, and body text.
- Use spacing and layout to create a modern, airy feel.
- Use buttons and form inputs from shadcn/ui components for consistency.
- Avoid any icon libraries or external images; use only typography and colors for visual hierarchy.
- Use placeholder images with descriptive alt text for gallery and hero sections.

---

## File and Code Changes Outline

### 1. `src/app/page.tsx`
- Create the main landing page component.
- Structure the page into sections: Hero, Services, Gallery, Booking, About, Footer.
- Import and use reusable UI components from `src/components/ui/` for buttons, cards, forms, etc.
- Use Tailwind CSS classes for styling and layout.
- Add placeholder images with descriptive alt text and graceful `onerror` fallback handlers.

### 2. `src/components/Services.tsx`
- Create a new component to list services and pricing.
- Use cards or panels styled with Tailwind CSS.
- Export and import into `page.tsx`.

### 3. `src/components/Gallery.tsx`
- Create a responsive image grid or carousel component.
- Use placeholder images with descriptive alt text.
- Export and import into `page.tsx`.

### 4. `src/components/BookingForm.tsx`
- Create a contact/booking form using React Hook Form.
- Fields: Name, Email, Phone, Service (dropdown), Date & Time (input), Message.
- Validate inputs and show error messages.
- On submit, show toast notifications using Sonner.
- Export and import into `page.tsx`.

### 5. `src/components/About.tsx`
- Create a simple about section with text content about Raja Pathan.
- Export and import into `page.tsx`.

### 6. `src/components/Footer.tsx`
- Create footer with contact info and social media text links.
- Export and import into `page.tsx`.

### 7. `src/app/globals.css`
- Add any additional global styles or Tailwind CSS customizations if needed.

---

## Error Handling and Best Practices

- Form validation with React Hook Form to prevent invalid submissions.
- Graceful fallback for images using `onerror` attribute to handle loading failures.
- Use try-catch or error boundaries if any async operations are added later.
- Accessibility: Use semantic HTML elements and ARIA attributes where appropriate.
- Responsive design tested on multiple screen sizes.
- Use TypeScript types and interfaces for props and state management.
- Use consistent naming conventions and folder structure.

---

## Integration with Existing Codebase

- Leverage existing UI components from `src/components/ui/` for buttons, inputs, cards, and toast notifications.
- Use Tailwind CSS utility classes and custom variables for styling.
- Use React Hook Form for form management as per existing dependencies.
- No external API or backend integration required initially; form submission can be mocked or extended later.
- Maintain the existing project structure and coding standards.

---

## Placeholder Images Example

```tsx
const heroImage = "https://placehold.co/1920x1080?text=Barber+Shop+Modern+Interior+with+Barber+Chair+and+Tools";
const galleryImage1 = "https://placehold.co/400x300?text=Barber+cutting+hair+in+modern+shop";
const galleryImage2 = "https://placehold.co/400x300?text=Close+up+of+beard+trim+service";
const galleryImage3 = "https://placehold.co/400x300?text=Barber+shop+waiting+area+with+chairs";

<img
  src={heroImage}
  alt="Modern barber shop interior with barber chair and tools arranged neatly"
  onError={(e) => { e.currentTarget.src = "https://placehold.co/1920x1080?text=Image+not+available"; }}
/>
```

---

## Summary

- Create a multi-section landing page in `src/app/page.tsx` using reusable components.
- Build components for Services, Gallery, BookingForm, About, and Footer in `src/components/`.
- Use React Hook Form for booking form with validation and Sonner for toast notifications.
- Use Tailwind CSS and shadcn/ui components for styling and accessibility.
- Use placeholder images with descriptive alt text and graceful fallback.
- Ensure responsive, accessible, and modern UI without external icons or images.
- No external API keys or backend integration required initially.
- Follow existing project structure and best practices for TypeScript and React.
