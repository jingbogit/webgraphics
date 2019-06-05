# Main thread

Determine the planet's lod tree structure. And send it to the worker thread. Wait for the 3D content to send back.

Worker thread may request to update lod nodes' 3D content. Update the content when receiving such requests.

