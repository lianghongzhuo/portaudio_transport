# portaudio_transport
ROS node based on portaudio and libsndfile to transport live sound recording via ROS topics.

## Required components:
- For audio record:  according to [this](https://ubuntuforums.org/showthread.php?t=1680154),
install packages in this order will not remove any other packages

    ```bash
    sudo apt install libsndfile1-dev
    sudo apt install libjack-jackd2-dev
    sudo apt install portaudio19-dev
    ```
## Common problems:
- ensure user is in audio group
- do not set frame rate too large, 4 is enough
- do not set parameter `save_file` to `true`, save file function is not stable at the moment