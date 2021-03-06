# Convert PDF to 600ppi TIFF

Just like PhotoShop, Gimp can convert back-and-forth between different file formats. In this tutorial, we'll convert a PDF file (with two pages), to be two separate TIFF images (with 600ppi).


## Installation

Gimp is a free software across all three major Operating System: Windows, Mac, and Linux. In this tutorial we'll use Windows for demo, but the same steps can be shared across Mac and Linux users (with trivial difference).

Gimp can be downloaded here: https://www.gimp.org/downloads/. Simply download the installer for your specific OS, and click to install. After installation complete, open the Gimp app. Notice that the "first time open" might take a few minutes, because it'll query the available plugins and install them. Also make sure you have internet connection.


## Step-to-step Instructions

The following are the steps for the pdf-tiff conversion:

### Import pdf file with 600ppi

We will use this [sample_pdf](../assets/sample_pdf.pdf) to illustrate the steps.
1. Open Gimp, click `File -> Open`, then navigate to the sample_pdf.pdf to open it.   
    <p float="left">
    <img src="../assets/convert_pdf_to_600ppi_tiff/import_step_1.jpg" alt="import_step1" width="800" />
    </p>
    <div style="clear: both;"></div>

2. A window will prompt with import options, like the following picture. Current *Resolution* is `100 pixel/inch`, *Width* is `850px`, *Height* is `1100px`.
    <p float="left">
    <img src="../assets/convert_pdf_to_600ppi_tiff/import_step_2.jpg" alt="import_step2" width="800" />
    </p>
    <div style="clear: both;"></div>

3. Update the resolution to be 600 pixel/inch. Notice that *Width* and *Height* will automatically change with the Resolution, to become `5100px` and `6600px`, leave these values for now. Also update the `Open page as` field from `Layers` to `Images`. Then click *Import* button.
    <p float="left">
    <img src="../assets/convert_pdf_to_600ppi_tiff/import_step_3.jpg" alt="import_step3" width="800" />
    </p>
    <div style="clear: both;"></div>

### Scale Image

After import, the Gimp project will have two images opened in two tabs (corresponding to PDF page #1 and page #2). You may have more tabs if you have more pages. The handling for each page/image is exactly the same:
1. Select an image (you can do it by click tabs on the top), navigate `Image -> Scale Image`, after click you'll see the following option
    <p float="left">
    <img src="../assets/convert_pdf_to_600ppi_tiff/scale_image_before.jpg" alt="scale_image_before" width="800" />
    </p>
    <div style="clear: both;"></div>

2. Change the *Width* and *Height* to be smaller value, you can use the original pdf's dimension when import, in this case it should be `850px x 1100px`. The resolution `600 pixel/inch` is correct, so no need to change. Interpolation option is up to you (if you have special requirement). Cubic and linear are commonly used options. Then click *Scale* button.
    <p float="left">
    <img src="../assets/convert_pdf_to_600ppi_tiff/scale_image_after.jpg" alt="scale_image_after" width="800" />
    </p>
    <div style="clear: both;"></div>

### Export as TIFF Image

After finish scaling the image, we need to export it as TIFF format.
1. Click `File -> Export As`, a "Export Image" window will open. The default name is from the original pdf file, which is `sample_pdf.pdf`, change it to any preferred name end with `.tiff`, for example `page1.tiff`
    <p float="left">
    <img src="../assets/convert_pdf_to_600ppi_tiff/export_before.jpg" alt="export_before" width="800" />
    </p>
    <div style="clear: both;"></div>

2. Then a "Export Image as TIFF" window will prompt, you might need to choose a Compression option if you want the image to be smaller (JPEG is the most popular one). Then click `export`
    <p float="left">
    <img src="../assets/convert_pdf_to_600ppi_tiff/export_after.jpg" alt="export_after" width="800" />
    </p>
    <div style="clear: both;"></div>

3. Save the result TIFF file to your desired location

### Repeat the Scale/Export steps

Repeat "Scale Image" and "Export as TIFF Image" for each of the pages in the PDF (corresponding to image tabs in the Gimp). Then you're all set.
Here's the result from the [sample_pdf](../assets/sample_pdf.pdf): [page1.tiff](../assets/convert_pdf_to_600ppi_tiff/page1.tiff) and [page2.tiff](../assets/convert_pdf_to_600ppi_tiff/page1.tiff).