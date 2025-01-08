Configuration
=============

Default Settings
----------------
The following are the default settings for the microservice:

- `LOG_LEVEL`: INFO
- `AUTO_START`: False

Customizing Configurations
--------------------------
You can modify the `config.json` file to customize pipeline behavior.

Example:
    .. code-block:: json

     {
       "pipelines": [
           {
               "name": "object_detection",
               "source": "gstreamer",
               "auto_start": false
           }
       ]
        }

Apply changes by restarting the service:
    .. code-block:: shell
        docker restart <container_name>


Configuration Parameters
------------------------
Here are some common configuration parameters you can customize:

- `LOG_LEVEL`: Set the logging level (e.g., DEBUG, INFO, WARN, ERROR).
- `AUTO_START`: Automatically start the pipeline on service startup (true/false).
- `pipelines`: Define the pipelines to be used by the microservice.

Next Steps
----------
- Learn how to set up the microservice in :doc:`getting-started`.
- Explore the API endpoints in :doc:`api_reference`.