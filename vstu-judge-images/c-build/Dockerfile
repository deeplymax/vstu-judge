# Use the `vstu-judge-agent` image as a base image.

FROM deeplymax/vstu-judge-agent

# Install the GNU C Compiler.

RUN apk add --no-cache musl-dev gcc

# Create a working directory for the build agent (specified in the agent's
# configuration file).

RUN mkdir /submission

# Expose the build agent's communication port (set in the agent's
# configuration file).

EXPOSE 7742
