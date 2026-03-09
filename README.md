# Java to UML Generator (JS-Native Fork)

A clean, modern web application that automatically translates Java source code into high-quality UML class diagrams. 

## Features

- **Drag-and-Drop Uploads**: Easily upload multiple `.java` files simultaneously.
- **Accurate UML Parsing**: Accurately maps Java visibility modifiers (`+`, `-`, `#`), abstract methods, interfaces, inheritance (`IS-A`), and composition relationships (`HAS-A`) natively within the Node.js ecosystem.
- **Smart Filtering**: Automatically hides common Java standard libraries (like `ArrayList`, `Stack`, `HashMap`) from cluttering the diagram, ensuring the UML strictly focuses on your uploaded architecture.
- **Interactive Viewer**: Pan, zoom, and inspect generated UML diagrams using the built-in React component.
- **High-Res Export**: Download Diagrams as scalable vector shapes (SVG) or directly export them to crisp, upscaled Image files (PNG).

## Architecture

1. **Frontend**: A Next.js (React) application built with TailwindCSS for styling and `react-zoom-pan-pinch` for diagram interaction. Features native integration with Mermaid.js for drawing.
2. **Parser Pipeline**: The heavy lifting is handled entirely in JavaScript. Using an ANTLR4-generated lexer and parser, the app traverses the Java Abstract Syntax Tree (AST) using a custom `ParseTreeWalker` and outputs a Mermaid class diagram definition string. 

## Prerequisites

- **Node.js** (v18 or newer)

## Local Development Setup

1. **Install Dependencies:**
   Navigate to the project root and install the required npm packages (including `antlr4`).

   ```bash
   npm install
   ```

2. **Run the Development Server:**
   Kickstart the Next.js development server.

   ```bash
   npm run dev
   ```

3. **Open the App:**
   Open your browser and navigate to `http://localhost:3000`.

## Deployment

**Vercel / Serverless Deployment (Recommended)**
You can deploy this directly to Vercel, Netlify, or any standard Next.js hosting environment out-of-the-box. The parser runs seamlessly as part of the standard Node.js serverless functions. 

## License

MIT License