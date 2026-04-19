# Spatio-temporal Modeling of Antarctic Sea Ice Extent 🧊

![Sea Ice Animation](lod_z_csv.gif)
*(The animation above compares the actual sea ice extent with the model results over the years).*

## 📖 Project Overview
The main goal of this project was to analyze daily Antarctic sea ice extent data and develop a mathematical model to describe these changes over time and space. The model's predictions were compared with actual measurement data through visualizations and animations.

## 📊 Data
The data used in this analysis comes from the `daily_ice_edge.csv` file, containing daily ice extent measurements starting from October 26, 1978, covering the years 1978-2009. The extent is represented as latitude for each longitude angle (from 0 to 360 degrees).

## ⚙️ Mathematical Model
An extended Fourier model was used to describe the cyclical changes in the data over time.
* The model is based on the sum of six cosine waves with different frequencies.
* A linear trend was added to capture long-term tendencies in the ice cover changes.
* Model parameters were optimized using curve fitting algorithms (`scipy.optimize.curve_fit`) separately for each longitude.

## 🚀 Technologies
The project was implemented in Python using the following libraries:
* **Pandas** – for tabular data processing.
* **NumPy** – for matrix operations and geometric transformations.
* **Matplotlib / Pillow** – for generating Cartesian plots and GIF animations.
* **SciPy** – for fitting the mathematical model to the real measurement data.
* **tqdm** – for monitoring computational loops.

## 💡 Key Findings
* The developed mathematical model accurately reflects real changes in sea ice extent, correctly describing its cyclical nature.
* Local discrepancies between the model and reality result from external factors, such as regional weather/oceanic anomalies (e.g., El Niño, La Niña) and ocean currents, which a simple periodic model does not predict.
* The use of a 3D binary grid allowed for effective and precise spatial analysis.

## 💻 How to Run the Project
1. Clone this repository: `git clone [YOUR_REPO_LINK]`
2. Install the required packages: `pip install -r requirements.txt`
3. Run the notebook to explore the data and generate the animation.
