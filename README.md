# ⚡ Terminal Cyberpunk — Menú Interactivo (README)

Bienvenido a tu **interfaz cyberpunk neon**, diseñada para lucir épica y ser totalmente interactiva desde consola.

---

## 🧬 **⚡ Neo-Terminal 3.0**

```ascii
███████╗███████╗███╗   ██╗ ██████╗ 
██╔════╝██╔════╝████╗  ██║██╔════╝ 
█████╗  █████╗  ██╔██╗ ██║██║  ███╗
██╔══╝  ██╔══╝  ██║╚██╗██║██║   ██║
██║     ███████╗██║ ╚████║╚██████╔╝
╚═╝     ╚══════╝╚═╝  ╚═══╝ ╚═════╝ 
```

> 💾 **Desarrollado por:** Joel  
> 📧 **Contacto:** joeldavidddearcos@gmail  
> 🌐 Inspirado en diseño *neon-cyberpunk*

---

## 🚀 **Menú Interactivo (Ejemplo en Node.js)**

```bash
npm install inquirer chalk gradient-string figlet
```

```js
#!/usr/bin/env node
import inquirer from "inquirer";
import chalk from "chalk";
import gradient from "gradient-string";
import figlet from "figlet";

function title() {
  console.log(
    gradient.pastel(
      figlet.textSync("NEO-TERMINAL", { horizontalLayout: "full" })
    )
  );
}

async function menu() {
  title();

  const answer = await inquirer.prompt([
    {
      type: "list",
      name: "option",
      message: chalk.cyan("⚡ Selecciona una opción:"),
      choices: [
        "📁 Ver archivos del sistema",
        "🧠 Ejecutar IA local",
        "🛠 Configuración avanzada",
        "❌ Salir",
      ],
    },
  ]);

  switch (answer.option) {
    case "📁 Ver archivos del sistema":
      console.log(chalk.green("Mostrando archivos..."));
      break;

    case "🧠 Ejecutar IA local":
      console.log(chalk.yellow("Iniciando IA..."));
      break;

    case "🛠 Configuración avanzada":
      console.log(chalk.magenta("Abriendo configuración..."));
      break;

    case "❌ Salir":
      console.log(chalk.red("Saliendo..."));
      process.exit(0);
  }

  setTimeout(menu, 1000);
}

menu();
```

---

## 🌈 Estilo Visual

- 🎨 **Neon cyan + magenta**
- 🔥 Títulos con **figlet**
- 🌌 Gradientes con **gradient-string**
- 🧩 Menú animado con **inquirer**

---

## 🛠 Como Ejecutarlo

1. Crea un archivo `terminal.js`
2. Copia el código anterior
3. Dale permisos:

```bash
chmod +x terminal.js
```

4. Ejecuta:

```bash
node terminal.js
```

---

## ⭐ ¿Quieres agregar animaciones, sonidos o HUD holográfico?  
Solo dime y puedo generar una **versión 4.0** aún más brutal 🔥👾

