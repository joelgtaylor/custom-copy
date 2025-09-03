# Selective Paste - Proof of Concept

This project is a proof-of-concept for a "selective paste" feature for rich-text editors. It demonstrates how to intercept the paste event and sanitize the incoming HTML to keep only the desired formatting, while stripping out everything else (like fonts, colors, and sizes).

## The Problem

When users paste content from sources like Google Docs, Microsoft Word, or other web pages, it often comes with a lot of unwanted styling that doesn't match the application's design. This tool provides a way to control exactly which formatting elements are preserved.

## How to Use

1.  Open the `index.html` file in a web browser.
2.  Use the checkboxes to select the formatting you want to keep (e.g., Bold, Italic, Links).
3.  Copy some rich text from another source.
4.  Paste it into the editor area.

The pasted content will be sanitized according to your selections.

## Features

-   **Selective Formatting**: Keep or discard bold, italic, underline, strikethrough, links, lists, paragraphs, and line breaks.
-   **Style Stripping**: Automatically removes inline styles like `font-family`, `font-size`, `color`, etc.
-   **Semantic Conversion**: Converts style-based formatting (e.g., `style="font-weight: bold"`) into semantic HTML tags (e.g., `<strong>`).
-   **Link Sanitization**: Preserves valid `href` attributes on links while removing potentially unsafe ones.

## Technical Details

-   **Frontend**: Plain HTML and JavaScript.
-   **Styling**: [Tailwind CSS](https://tailwindcss.com/) (included via CDN).
-   **Dependencies**: None.
-   **Build Process**: None. Simply open `index.html` in a browser.
