#Image Component
---------------------------

Next.js 12 introduced new improvements to the Image Component with a temporary import: next/future/image. 
These improvements included:
1. Less client-side JavaScript 
2. Easier ways to extend and style images
3. Better accessibility
4. Native browser lazy loading.

In version 13, this new behavior is now the default for next/image, which

```
import Image from 'next/image';

export default function Page() {
  return (
    <Image
      src="/profile.png"
      width={500}
      height={500}
      alt="Picture of the author"
    />
  );
}
```



The next/image import was renamed to next/legacy/image. 
The next/future/image import was renamed to next/image. 
A codemod is available to safely and automatically rename your imports.
