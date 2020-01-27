FROM brainbeanapps/android-nondk-build-environment:api26-v1.1.0

LABEL maintainer="devops@brainbeanapps.com"

# Switch to root
USER root

# Install Android SDK components
ARG ANDROID_NDK_VERSION="20.1.5948944"
ENV ANDROID_NDK="${ANDROID_HOME}/ndk/${ANDROID_NDK_VERSION}"
ENV ANDROID_NDK_ROOT="${ANDROID_NDK}"
ENV ANDROID_NDK_HOME="${ANDROID_NDK}"
ENV PATH="${ANDROID_NDK}:${PATH}"
RUN (yes | sdkmanager \
    "cmake;3.6.4111459" \
    "cmake;3.10.2.4988404" \
    "ndk;${ANDROID_NDK_VERSION}" \
  )

# Switch to user
USER user
WORKDIR /home/user
