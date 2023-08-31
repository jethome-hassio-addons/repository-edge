# Changelog since v0.2.4
- Merge pull request #48 from jethome-hassio-addons/add_62_kernel_gpionumbers

Add GPIO numbers for kernel 6.2+ 
- Update addon to support of new gpio numbers

- Add GPIO numbers for kernel 6.2+
- Update ghcr.io/hassio-addons/base-python/aarch64 from 9.0.1 to 11.0.5
- Move build.json to build.yaml as required in latest ha addon build system
- Update mqtt-io 2.2.9d version with latest pyproject.toml from 2bb2f945ea47ed87f99ab4fc966d2dbbd47fc7c7
  - in mqtt-io added a workaround for 2 different problems:
    - keepalive was not implemented in early versions of asyncio_mqtt
    - due to the way we receive messages asynchronously in our own queue we are not able
      to capture the disconnected exception and trigger the reconnection. This publish call
      will trigger the exception if the connection was lost and reconnect. (Issue #282) 
- Update Dockerfile: to match current Alpine 3.16 packages:

* openssl=1.1.1t-r0
* git=2.36.5-r0 
- Remove `lock` workflow 
- README.md: fix repo url 
