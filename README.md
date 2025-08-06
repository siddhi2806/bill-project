# Bill Splitter App

A Next.js 14 application for splitting bills by scanning receipts using LLaMA 3.2 Vision API.

## Tech Stack

- **Next.js 14** (App Router)
- **Tailwind CSS** for styling
- **shadcn/ui** for UI components (to be added)
- **LLaMA 3.2 Vision** integration via Together API
- **TypeScript** for type safety

## Features

- 📱 **Home Page** - Simple landing page with scan/manual entry options
- 📷 **Receipt Scanning** - Upload or take photos of receipts
- ✏️ **Edit Items** - Review and modify extracted receipt items
- 👥 **Assign People** - Add people and assign items to them
- 💰 **Split Summary** - View final bill split with sharing options

## Project Structure

```
/app
  /page.tsx                    → Home (/)
  /scan/page.tsx              → Scan Receipt (/scan)
  /edit-receipt/page.tsx      → Edit Receipt Items (/edit-receipt)
  /assign-items/page.tsx      → Assign People to Items (/assign-items)
  /split-summary/page.tsx     → Split Summary (/split-summary)
  /api/scrape/route.ts        → API route for LLaMA Vision integration
  /layout.tsx                 → Root layout
  /globals.css                → Global styles with Tailwind
/components
  /ItemCard.tsx               → Item display component
  /PersonInput.tsx            → Person input component
  /SplitSummary.tsx          → Summary display component
  /ReceiptUpload.tsx         → File upload component
```

## Getting Started

1. **Install dependencies:**

   ```bash
   npm install
   ```

2. **Set up environment variables:**
   Create a `.env.local` file and add your Together API key:

   ```
   TOGETHER_API_KEY=your_together_api_key_here
   ```

3. **Run the development server:**

   ```bash
   npm run dev
   ```

4. **Open in browser:**
   Navigate to [http://localhost:3000](http://localhost:3000)

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run lint` - Run ESLint

## API Integration

The `/api/scrape` route handles receipt image processing using the Together API with LLaMA 3.2 Vision model. Send a POST request with a base64-encoded image to extract receipt items.

## Status

✅ **Project Setup Complete**

- All TypeScript/JSX errors resolved
- Next.js 14 with App Router configured
- Tailwind CSS integrated
- Basic page structure implemented
- API route structure ready for LLaMA integration

🚧 **Next Steps**

- Add shadcn/ui components
- Implement receipt upload functionality
- Complete LLaMA Vision API integration
- Build interactive item assignment features
- Add sharing functionality
