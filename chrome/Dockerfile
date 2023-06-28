ARG VERSION=latest

FROM zenika/alpine-chrome:$VERSION

# Disables GPU hardware acceleration. If software renderer is not in place, then the GPU process won't launch.
# Disables the sandbox for all process types that are normally sandboxed. Meant to be used as a browser-level switch for testing purposes only.
# Enables remote debug over HTTP on the specified port.
# Enables remote debug over HTTP on the specified port.
CMD ["--disable-gpu", "--no-sandbox", "--remote-debugging-address=0.0.0.0", "-remote-debugging-port=9222"]
