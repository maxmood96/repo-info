## `gradle:8-jdk17-graal`

```console
$ docker pull gradle@sha256:3b7d98c360a2262e43939b521f81bc8dacab8ec9c66648e20a73076e7f1eb3f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk17-graal` - linux; amd64

```console
$ docker pull gradle@sha256:601036f3913abe0461bb93cc17289050398d9e7cfaa73b1cd69922fcebf5710c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.1 MB (585118305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf65508678939e6b6992938ec5738b6b1410cad0271e6a6dca0d213d15d743b0`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 16 Jun 2024 03:23:28 GMT
ARG RELEASE
# Sun, 16 Jun 2024 03:23:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 16 Jun 2024 03:23:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 16 Jun 2024 03:23:28 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 16 Jun 2024 03:23:28 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Sun, 16 Jun 2024 03:23:28 GMT
CMD ["/bin/bash"]
# Sun, 16 Jun 2024 03:23:28 GMT
CMD ["gradle"]
# Sun, 16 Jun 2024 03:23:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 16 Jun 2024 03:23:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 16 Jun 2024 03:23:28 GMT
WORKDIR /home/gradle
# Sun, 16 Jun 2024 03:23:28 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sun, 16 Jun 2024 03:23:28 GMT
ENV JAVA_VERSION=17.0.9
# Sun, 16 Jun 2024 03:23:28 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
ENV GRADLE_VERSION=8.8
# Sun, 16 Jun 2024 03:23:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
# Sun, 16 Jun 2024 03:23:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
USER gradle
# Sun, 16 Jun 2024 03:23:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
USER root
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5aad3d76fcae83ced133988218ee3582afc6e8f4ac5b71a99b84bd311589381`  
		Last Modified: Tue, 02 Jul 2024 03:18:39 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b2f2b4ae5a88f7c43a457013da7fc076ef763a0c2be91cd559627c591a44e0`  
		Last Modified: Tue, 02 Jul 2024 03:18:41 GMT  
		Size: 126.4 MB (126397563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3922928a97560383eedd203e84fd70aa53ca1e634cd169ecb84835eac966dbb3`  
		Last Modified: Tue, 02 Jul 2024 03:18:43 GMT  
		Size: 291.1 MB (291064897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35033a6ca4930e625e841832c6ba5f2d31c085c8111856694f3106a01666e747`  
		Last Modified: Tue, 02 Jul 2024 03:18:41 GMT  
		Size: 138.1 MB (138062553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01fe4bb073845e8146d420c58242eb6b7bd58abf34990e43421b8f90c1d112bd`  
		Last Modified: Tue, 02 Jul 2024 03:18:40 GMT  
		Size: 54.9 KB (54898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:91f914d2fa145b822f80d26b0b9144378acde564b7e45a0a68412018ad4d7537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8613607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74890a4445f12a0dc94723e39d79e716e2e071c47d434d9156cd51e7896e2b0d`

```dockerfile
```

-	Layers:
	-	`sha256:49a4cf45d2c54e3a45151d85597a9326b9e515c572d37a0686e110b1cdb7c547`  
		Last Modified: Tue, 02 Jul 2024 03:18:39 GMT  
		Size: 8.6 MB (8581862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34a660e4c0fa99d34b97438d5dcf451f3c72023c3f530e9a76f275ffc58d7d20`  
		Last Modified: Tue, 02 Jul 2024 03:18:39 GMT  
		Size: 31.7 KB (31745 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:9082611eea5b95d9956a497b89b146f430618872ef08ba90d78c4b3d88e3bcad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.5 MB (571450550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6618926f094d27f6828f8cb650a84ab4c459b5895dfc1027dbea3785467adc8d`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 16 Jun 2024 03:23:28 GMT
ARG RELEASE
# Sun, 16 Jun 2024 03:23:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 16 Jun 2024 03:23:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 16 Jun 2024 03:23:28 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 16 Jun 2024 03:23:28 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Sun, 16 Jun 2024 03:23:28 GMT
CMD ["/bin/bash"]
# Sun, 16 Jun 2024 03:23:28 GMT
CMD ["gradle"]
# Sun, 16 Jun 2024 03:23:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 16 Jun 2024 03:23:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 16 Jun 2024 03:23:28 GMT
WORKDIR /home/gradle
# Sun, 16 Jun 2024 03:23:28 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sun, 16 Jun 2024 03:23:28 GMT
ENV JAVA_VERSION=17.0.9
# Sun, 16 Jun 2024 03:23:28 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
ENV GRADLE_VERSION=8.8
# Sun, 16 Jun 2024 03:23:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
# Sun, 16 Jun 2024 03:23:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
USER gradle
# Sun, 16 Jun 2024 03:23:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
USER root
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f14bd4e38aeec66cab4e17d57eaac893fd86aea60355401c88860cafaf0732`  
		Last Modified: Tue, 02 Jul 2024 14:40:07 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821268dff1ee4588fa2c6fe884c1d54d276c0eb9e7b1e5939a5dfb8a25501374`  
		Last Modified: Tue, 02 Jul 2024 14:40:11 GMT  
		Size: 122.5 MB (122462042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fc4267383d8778a80fe24b19195c0ea505b8bf38df7aaf3f80cb8e87876636`  
		Last Modified: Tue, 02 Jul 2024 14:40:13 GMT  
		Size: 283.5 MB (283502076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e2d5a1cb0d6dcd60b83ae8bcb649c90a0742774640ff53a683ac7261f3674c`  
		Last Modified: Tue, 02 Jul 2024 14:40:11 GMT  
		Size: 138.1 MB (138062546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31db756174a4860f91a44479ea43cb89209f502d19232d19b2be9709fd8d46a`  
		Last Modified: Tue, 02 Jul 2024 14:40:08 GMT  
		Size: 59.5 KB (59520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:c5569db9938bdf4c800eb516e9748f540c622bc2e032095490645c45546b0457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8609381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2594ce9dd6b0eecd17b43ce35d394b3e3986e49311ef532a6016535e77cb3c`

```dockerfile
```

-	Layers:
	-	`sha256:80f09dfe60959ae250678d14b24d6e1fce5b5b925c8d28b258fe5813b4bdd5a9`  
		Last Modified: Tue, 02 Jul 2024 14:40:08 GMT  
		Size: 8.6 MB (8577096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46db99607c2b903c2ccd6c518c84b1cce57127e3ad51c354be78c2e45e7907b5`  
		Last Modified: Tue, 02 Jul 2024 14:40:08 GMT  
		Size: 32.3 KB (32285 bytes)  
		MIME: application/vnd.in-toto+json
