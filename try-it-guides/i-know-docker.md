# Surface-level guide

## Reminders

The workshop team has a dummy Python BMI model (regardless of input, every output value is 0) that they would like you to integrate into NGIAB. The model source code is located in a [GitHub repository](https://github.com/quinnylee/bmi_dummy). The model is also published on [PyPI](https://pypi.org/project/bmi-dummy/). An input data package for testing the dummy BMI model within NGIAB is stored in [Box](https://alabama.box.com/s/8sx72ozsg9uxh3e61how7fi0qoolpy1w).

## Instructions

1. Please make sure your computer meets the requirements in our ["Before the Workshop" guide](../before-the-workshop.md).
2. Navigate to the directory where you cloned the NGIAB source code. NGIAB is built with the Dockerfile located in `docker/Dockerfile`.
3. Optional: build the NGIAB image without any changes to speed up any future rebuilds.
4. Edit the Dockerfile to make sure that the bmi-dummy Python package is accessible in the final build stage.
5. Rebuild the NGIAB Docker image.
6. Download the data package from Box if you haven't already.
7. Test your NGIAB build with this command:

   ```bash
   docker run --rm -it -v "/absolute/path/to/test/package:/ngen/ngen/data" name-of-your-NGIAB-image /ngen/ngen/data
   ```

   Follow the interactive terminal prompts to run NGIAB.

If your NGIAB run successfully executes, you've integrated the model!

For detailed instructions, follow the [detailed guide](i-do-not-know-docker.md).
