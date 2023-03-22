From the official nextJS guide by Vercel
https://nextjs.org/learn/foundations/from-react-to-nextjs/getting-started-with-nextjs

This project was created as follows:

- `mkdir recipes-next`
- `cd next-recipe`
- `npm init -y`
- `npm i react react-dom next`
- `git init`

(we are inside recipes-next directory)

- `mkdir pages`
- `touch pages/index.jsx (or js)`

copy this code into index.jsx

```
import { useState } from "react";

function Header({ title }) {
  return <h1>{title ? title : "Default title"}</h1>;
}

export default function HomePage() {
  const names = ["Ada Lovelace", "Grace Hopper", "Margaret Hamilton"];

  const [likes, setLikes] = useState(0);

  function handleClick() {
    setLikes(likes + 1);
  }

  return (
    <div>
      <Header title="Develop. Preview. Ship. 🚀" />
      <ul>
        {names.map((name) => (
          <li key={name}>{name}</li>
        ))}
      </ul>

      <button onClick={handleClick}>Like ({likes})</button>
    </div>
  );
}
```

> create an npm script

```
scripts: {
"dev": "next dev"
}
```
