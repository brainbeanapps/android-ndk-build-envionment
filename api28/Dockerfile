FROM brainbeanapps/android-nondk-build-environment:api28-v1.0.0

LABEL maintainer="devops@brainbeanapps.com"

# Switch to root
USER root

# Install Android SDK components
ARG CMAKE_VERSION="3.10.2.4988404"
ARG ANDROID_NDK_VERSION="20.1.5948944"
RUN (yes | sdkmanager \
    "cmake;${CMAKE_VERSION}" \
    "ndk;${ANDROID_NDK_VERSION}" \
  )

# Switch to user
USER user
WORKDIR /home/user
