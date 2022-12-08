Next.js 13 introduced a new file convention, error.js, which allows you to show a fallback if an error is thrown within the route subtree.

Error.js defines the error boundary for a route segment and the children below it. 
It can be used to show specific error information, and functionality to attempt to recover from the error.

Error Boundaries must be client components 


```
'use client';

// 'use client' marks this page as a Client Component
// https://beta.nextjs.org/docs/rendering/server-and-client-components

import { useEffect } from 'react';

export default function Error({ error, reset }: {
  error: Error;
  reset: () => void;
}) {
  useEffect(() => {
    // Log the error to an error reporting service
    console.error(error);
  }, [error]);

  return (
    <div>
      <p>Something went wrong!</p>
      <button onClick={() => reset()}>Reset error boundary</button>
    </div>
  );
}
```
