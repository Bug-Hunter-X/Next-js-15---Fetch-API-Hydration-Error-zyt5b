# Next.js 15 - Fetch API Hydration Error

This repository demonstrates a common error encountered in Next.js 15 applications involving `fetch` calls within components.  The issue arises when attempting to make a data fetch directly within a component's render function, leading to hydration mismatches and runtime errors. 

## The Problem

In Next.js 15, fetching data directly within a component like this causes a hydration error:  The client-side rendering produces different data than the server-side rendering, resulting in a hydration mismatch.

## Solution

The solution involves moving the data fetching logic to a separate function or using a data fetching library that handles the asynchronous aspects gracefully (e.g., `useSWR`, `react-query`).   The provided solution uses `useEffect` and only renders the component once the data has successfully been fetched and parsed.