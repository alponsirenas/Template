Getting Started
===============

Follow these steps to set up and start using the <microservice name>.


System Requirements
-------------------
- **Operating System**: <Specify the supported operating systems>
- **Dependencies**: <List the required dependencies>
- **Hardware**: <Specify the required hardware>

.. Example:
.. - **Operating System**: Linux
.. - **Dependencies**: Docker, Python 3.8 or later
.. - **Hardware**: Intel® CPUs with Deep Learning Streamer support

Installation Guide
------------------
You can get started with the microservice using one of the following methods:

Method 1: Using a Pre-built Docker Image
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
1. Pull the pre-built Docker image:

      .. code-block:: shell

         docker pull <image_name>:<tag>

2. Start the microservice:

      .. code-block:: shell

         docker run -p <host_port>:<container_port> <image_name>:<tag>

.. Example:
.. 1. Pull the pre-built Docker image:
..    .. code-block:: shell
..       docker pull intel/evam:latest
..
.. 2. Start the microservice:
..    .. code-block:: shell
..       docker run -p 8080:8080 intel/evam:latest

Method 2: Building from Source
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
1. Clone the repository:

      .. code-block:: shell

            git clone <repository_url>
            cd <repository_directory>

2. Build the container:

      .. code-block:: shell

         docker build -t <image_name>:<tag> .

3. Start the microservice:

      .. code-block:: shell

         docker run -p <host_port>:<container_port> <image_name>:<tag>

.. Example:
.. 1. Clone the repository:
..    .. code-block:: shell
..       git clone https://github.com/intel/edge-video-analytics-microservice.git
..       cd edge-video-analytics-microservice
..
.. 2. Build the container:
..    .. code-block:: shell
..       docker build -t evam:latest .
..
.. 3. Start the microservice:
..    .. code-block:: shell
..       docker run -p 8080:8080 evam:latest

First Use
---------
In this section, you will perform a simple task to verify that the microservice is working correctly. You will start a pipeline and view the output to see the microservice in action.

1. Open the API endpoint in your browser:

      URL: `<api_endpoint_url>`

2. Start a pipeline:

      .. code-block:: shell

         curl -X POST -H "Content-Type: application/json" \
         -d '<json_payload>' \
         <api_endpoint_url>/start

3. View the output:

      Open `<output_url>` in your browser.

.. Example:
.. In this section, you will perform a simple task to verify that the microservice is working correctly. You will start a pipeline and view the output to see the microservice in action.
..
.. 1. Open the API endpoint in your browser:
..    - URL: `http://localhost:8080/api/v1/pipelines`
..
.. 2. Start a pipeline:
..    .. code-block:: shell
..       curl -X POST -H "Content-Type: application/json" \
..       -d '{"name": "object_detection", "source": "sample_video.mp4"}' \
..       http://localhost:8080/api/v1/pipelines/start
..
.. 3. View the output:
..    - Open `http://localhost:8080/streams/object_detection` in your browser.
..    - You should see a real-time video stream with detected objects highlighted. This demonstrates the microservice's capability to perform real-time video analytics and object detection using the provided video source.

Next Steps
----------
- Learn how to configure the microservice in :doc:`configuration`.
- See API endpoint details in :doc:`api-reference`.

Troubleshooting
---------------
If you encounter issues, check the following:

- Ensure <dependency> is running and you have the necessary permissions.
- Verify the <component> URL and port number.
- Check the <log_location> for error messages:

      .. code-block:: shell

       <command_to_check_logs>

.. Example:
.. If you encounter issues, check the following:
.. - Ensure Docker is running and you have the necessary permissions.
.. - Verify the API endpoint URL and port number.
.. - Check the container logs for error messages:
..   .. code-block:: shell
..      docker logs <container_id>