# Лабораторна робота №6
## Мета: Робота з анімацією

Дана робота є продовженням попередньої

1. Створити у склонованій директорії [React проект](https://reactjs.org/docs/create-a-new-react-app.html) з назвою 'traffic-lights-6'
1. Перенести попередню лабораторну 
1.  При клікані на колір сфітлофора реалізувати ефект "моргання" (плюсом буде реалізація зміни яскравості кольору, кількості "моргань", тощо)
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
1. Оформити звіт на локальному комп'ютері
1. Запушити лаборатону в github.classroom
1. В Google classroom додати посилання на звіт
