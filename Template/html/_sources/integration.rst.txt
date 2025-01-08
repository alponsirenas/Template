Integration Examples
====================

This section shows how to use the microservice in real-world scenarios.

Using the Microservice in Python
--------------------------------
.. code-block:: python

   import requests

   url = "http://localhost:8080/api/v1/pipelines/start"
   data = {"name": "object_detection", "source": "sample_video.mp4"}
   response = requests.post(url, json=data)
   print(response.json())

.. Example:
.. .. code-block:: python
..    import requests
..    url = "http://localhost:8080/api/v1/pipelines/start"
..    data = {"name": "object_detection", "source": "sample_video.mp4"}
..    response = requests.post(url, json=data)
..    print(response.json())

Workflow Integration
--------------------
You can integrate this microservice into a larger workflow. For example:
1. Use a preprocessing service to prepare video input.
2. Process the video with this microservice.
3. Send the output to a visualization tool for analysis.

.. Example:
.. You can integrate this microservice into a larger workflow. For example:
.. 1. Use a preprocessing service to prepare video input.
.. 2. Process the video with this microservice.
.. 3. Send the output to a visualization tool for analysis.

Next Steps
----------
- Validate your workflow using the instructions in :doc:`testing-and-validation`.
- Learn how to troubleshoot integration issues in :doc:`troubleshooting`.

.. Example:
.. - Validate your workflow using the instructions in :doc:`testing-and-validation`.
.. - Learn how to troubleshoot integration issues in :doc:`troubleshooting`.