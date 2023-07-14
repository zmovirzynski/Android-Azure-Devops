# Android Azure DevOps

This repository contains the YAML configuration to create an Azure Pipelines pipeline for setting up and starting an Android emulator. The pipeline automates the process of creating and launching the emulator on a macOS machine.

## Prerequisites

Before using this pipeline, make sure you have the following:

- An Azure DevOps account set up with a suitable project.
- A macOS agent available in your Azure Pipelines organization.

## Configuration

Follow the steps below to configure the pipeline in Azure Pipelines:

1. Clone this repository to your local environment:

```bash
git clone https://github.com/zmovirzynski/Android-Azure-Devops.git
```

In Azure DevOps, navigate to the project where you want to set up the pipeline.

In the project dashboard, go to **Pipelines** and click **New Pipeline**.

Choose the source code repository to be the cloned repository from earlier.

Select the `azure-pipelines.yml` configuration file from this repository.

Review and customize the YAML file as needed to fit your requirements.

Save and run the pipeline.

## Pipeline

The pipeline consists of a single job:

**Job: macOS**
**Pool: macOS-latest**

This job runs on a macOS agent.

**Steps:**

1. Install Node.js
   - This step installs Node.js version 16.x.

2. List already installed Android packages
   - This step lists the Android packages that are already installed.

3. Install Android image
   - This step installs the Android image with the specified version.

4. Create AVD (Android Virtual Device)
   - This step creates an AVD named "test_android_emulator" using the installed Android image.

5. Start Android emulator
   - This step starts the Android emulator by executing commands to list available AVDs, create the AVD, and start the emulator using the specified AVD.

## Contributing

Feel free to contribute to this project by opening issues and submitting pull requests. Your participation is welcome!

## Support

If you have any questions or encounter any issues related to this repository, please reach out by opening an issue. We will do our best to assist you.

## License

This project is licensed under the MIT License.
