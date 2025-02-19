# Лабораторна робота №6

## Мета: Робота з анімацією

Дана робота є продовженням попередньої.

### Завдання:

1. **Створити у склонованій директорії** [React проект](https://vitejs.dev/guide/#scaffolding-your-first-vite-project) з назвою 'traffic-lights-6'.
2. **Перенести попередню лабораторну** та додати необхідні зміни.
3. **При кліканні на колір світлофора реалізувати ефект "моргання"** (плюсом буде реалізація зміни яскравості кольору, кількості "моргань" тощо).

```js
import { motion } from "framer-motion";
import { useEffect, useRef, useState } from "react";

export default function App() {
  const ref = useRef(1);
  const [isClick, setIsClick] = useState(true);

  useEffect(() => {}, [isClick]);

  return (
    <motion.div
      className="box"
      key={ref.current}
      initial={{ opacity: 0, scale: 0.5 }}
      animate={{ opacity: 1, scale: 1 }}
      transition={{ duration: 1 }}
      onClick={() => {
        ref.current++;
        setIsClick(!isClick);
      }}
    />
  );
}
```

```css
.box {
      width: 200px;
      height: 200px;
      border-radius: 50%;
      background: blue;
    }
```

4. **Оформити звіт на локальному комп'ютері**.
5. **Запушити лабораторну в GitHub Classroom**.
6. **В Google Classroom додати посилання на звіт**.

### Додаткове завдання:

Реалізувати анімоване з'явлення світлофорів як для горизонтального, так і для вертикального розташування, використовуючи `motion` з `framer-motion`.

