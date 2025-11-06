# Sensor-Augmented-TRNG
This single-file HTML/JavaScript web application demonstrates the principle of augmenting cryptographic random number generation (RNG) with real-world physical entropy provided by the user and their mobile device.
​The app is designed to showcase how user-generated "chaos" can be mixed with a highly secure system source to create a unique and extremely robust True Random Number Generator (TRNG) key.
​✨ Key Features
​5-Second Entropy Challenge: Users have a limited time to move and shake their device, maximizing the "Chaos Score" collected from the device's motion sensors (accelerometer and gyroscope).
​Dual-Source Mixing: The collected Physical Entropy (Chaos Score) is cryptographically mixed (XORed and rotated) with the operating system's powerful OS TRNG (window.crypto.getRandomValues).
​Quality Metrics:
​Chaos Score (Human Entropy): Quantifies the raw variability of the user's movement.
​Hamming Distance: Compares the final mixed key against a reference OS TRNG key (256 bits). A score close to 128/256 signifies a near-perfect, independent mix, validating the entropy contribution.
​Mobile-First Design: Optimized for touchscreens and immediate access to DeviceOrientationEvent sensors.
​💡 Why This Approach is More Secure
​While the OS TRNG provides strong cryptographic randomness (similar in quality to services like random.org), combining it with user-generated physical noise ensures that the final key contains an element of randomness that is unpredictable by any external or internal attacker, as it is unique to the user's physical actions at that exact moment.
​🛠️ Technology Stack
​Frontend: HTML, Tailwind CSS (via CDN)
​Logic: Pure JavaScript (ES6+), leveraging the built-in window.crypto API for strong random seeding and DeviceOrientationEvent for entropy collection.
, try demo at: https://true-random.netlify.app/
