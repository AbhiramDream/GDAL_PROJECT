# GDAL_PROJECT


GeoTIFF and Vector Data Processing Projects

Overview
This repository contains two projects focused on geospatial data processing using Python libraries such as `rasterio`, `matplotlib`, `numpy`, `geopandas`, and `osgeo`. These projects demonstrate how to generate synthetic raster data, perform geospatial transformations, and work with vector data (shapefiles) for tasks such as resampling, reprojecting, and clipping.

Project 1: Synthetic GeoTIFF Raster Creation and Transformation

 Description
This project demonstrates how to:
- Create a synthetic GeoTIFF raster file.
- Apply geospatial transformations, including scaling the image resolution.
- Visualize the original and transformed raster images.

 Libraries Required
- `rasterio`
- `matplotlib`
- `numpy`

 Steps:
1. Create a Synthetic GeoTIFF Raster:
   - Generate random pixel values (100x100 grid) as synthetic image data.
   - Set georeferencing metadata with a `1x1` degree resolution.

2. Load and Visualize the Original Image:
   - Use `rasterio` to load the raster and display the original image.

3. Apply Geo-Transformation (Scaling):
   - Rescale the image by changing the pixel size to `0.5x0.5` degrees.
   - Use bilinear resampling to adjust the resolution.

4. Visualize the Transformed Image:
   - Display the transformed image using `matplotlib`.

5. Print Transform Information:
   - Print the original and new geospatial transformations to compare.

 Usage
- Ensure the required libraries are installed by running:
  ```bash
  pip install rasterio matplotlib numpy
  ```

- Run the script to create, transform, and visualize the synthetic raster.

---

 Project 2: Vector and Raster Data Processing

 Description
This project demonstrates how to:
- Create synthetic vector data (a simple polygon).
- Generate synthetic raster data (e.g., a DEM grid).
- Reproject vector data to match the raster's coordinate reference system (CRS).
- Clip the raster using the vector data (polygon).

 Libraries Required
- `geopandas`
- `rasterio`
- `numpy`
- `matplotlib`
- `osgeo`

 Steps:
1. Create Synthetic Vector Data:
   - Generate a simple polygon representing administrative boundaries using `geopandas`.

2. Create Synthetic Raster Data:
   - Generate random elevation values (360x180 grid) to mimic DEM data.
   - Save this as a GeoTIFF raster file.

3. Reproject Vector Data:
   - Reproject the vector data (polygon) to match the raster's CRS using `geopandas` and `osgeo`.

4. Clip Raster with Vector Data:
   - Clip the raster data using the polygon geometry, ensuring the raster is cropped to the boundaries of the vector data.

5. Visualize Clipped Raster:
   - Display the clipped raster using `matplotlib` with a terrain color map.

 Usage
- Install the required libraries:
  ```bash
  pip install geopandas rasterio matplotlib numpy
  ```

- Run the script to create, reproject, clip, and visualize the raster data.

---

File Structure


/content/
  ├── synthetic_geotiff.tif       # Output of Project 1 (GeoTIFF file)
  ├── synthetic_dem.tif          # Output of Project 2 (DEM raster file)
  ├── clipped_synthetic_dem.tif  # Clipped output from Project 2


 License
This project is open-source and available under the [MIT License](LICENSE).

 Acknowledgements
- `rasterio` for reading and writing geospatial raster data.
- `geopandas` for handling vector data.
- `matplotlib` for visualization.
- `numpy` for numerical operations.

