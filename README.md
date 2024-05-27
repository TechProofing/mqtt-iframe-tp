
# MQTT Control Panel

A React application built with Vite to control MQTT channels. This app features a color picker, label input, and reset button, and displays an iframe.

## Features

- **Color Picker:** Sends color data to the `colorBot` MQTT channel.
- **Label Input:** Sends text input as label data to the `labelBot` MQTT channel.
- **UUID Display:** Shows the UUID received from the `webBot` MQTT channel.
- **Reset Button:** Sends a reset command to the `clearAll` MQTT channel.
- **Iframe:** Displays content from a specified URL.

## Getting Started

Follow these instructions to set up and run the project locally.

### Prerequisites

- [Node.js](https://nodejs.org/en/download/)
- [npm](https://www.npmjs.com/get-npm)

### Installation

1. **Clone the repository:**

```
git clone https://github.com/yourusername/mqtt-control-panel.git
cd mqtt-control-panel
```

2. **Install dependencies:**

```
npm install
```

3. **Run the development server:**

```
npm run dev
```

### Building for Production

To create a production build, run:

```
npm run build
```

### Deployment

To serve the production build locally, you can use a package like `serve`:

```
npm install -g serve
serve -s dist
```

## Usage

1. **Color Picker:**
   - Select a color using the color picker.
   - The selected color is sent to the `colorBot` MQTT channel as a JSON object with the key `color` and the color value in hex format.

2. **Label Input:**
   - Enter text into the input field and click the "Set Label" button.
   - The entered text is sent to the `labelBot` MQTT channel as a JSON object with the key `label` and the text value.

3. **UUID Display:**
   - The app listens for messages on the `webBot` MQTT channel.
   - If a message with the key `uuid` is received, the UUID is displayed at the top of the control panel.

4. **Reset Button:**
   - Click the "Reset" button to send a reset command.
   - A JSON object with the key `reset` and the value `true` is sent to the `clearAll` MQTT channel.

## Project Structure

```
mqtt-control-panel/
├── public/
│   └── index.html
├── src/
│   ├── App.jsx
│   ├── main.jsx
│   └── index.css
├── .gitignore
├── index.html
├── package.json
├── README.md
└── vite.config.js
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Paho MQTT](https://www.eclipse.org/paho/index.php?page=clients/js/index.php)
- [React Color](https://casesandberg.github.io/react-color/)
- [Vite](https://vitejs.dev/)

---

Feel free to contribute to this project by opening issues or submitting pull requests. Your feedback and contributions are welcome!
