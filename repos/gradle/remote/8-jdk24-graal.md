## `gradle:8-jdk24-graal`

```console
$ docker pull gradle@sha256:f26df1b28a97b7336947b4a7dcf17b72b4b7a417696b7ff2b077367b20e92197
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk24-graal` - linux; amd64

```console
$ docker pull gradle@sha256:c958adf6ce72d795de9c9a9171620cb6c20d86faf9786f6a6c58d10b1bceecd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.3 MB (653252668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8d3438dcb43c9dfc470cf09cd186c7ecadf281fbf0d73759da786175c380f6`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:20:21 GMT
CMD ["gradle"]
# Tue, 17 Feb 2026 20:20:21 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 17 Feb 2026 20:20:21 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 17 Feb 2026 20:20:21 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 17 Feb 2026 20:20:21 GMT
WORKDIR /home/gradle
# Tue, 17 Feb 2026 20:22:40 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 17 Feb 2026 20:22:40 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 17 Feb 2026 20:22:40 GMT
ENV JAVA_VERSION=24.0.2
# Tue, 17 Feb 2026 20:22:58 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=6d62846c826ddb9307deec71e7661c26fa5a5e3985d7bb9005ea42163a390720     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c54d951a858791483d58270ecbc0946f28c4742c7fac74a4ebb2764bbf66d6f5     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 17 Feb 2026 20:22:58 GMT
ENV GRADLE_VERSION=8.14.4
# Tue, 17 Feb 2026 20:22:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Tue, 17 Feb 2026 20:23:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 17 Feb 2026 20:23:01 GMT
USER gradle
# Tue, 17 Feb 2026 20:23:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 17 Feb 2026 20:23:02 GMT
USER root
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a06830a2e6accd82407929c348728f7fe497ee9ffb7cc7bfd5fe51b17aa358`  
		Last Modified: Tue, 17 Feb 2026 20:21:47 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc9b548a3a98aadad870dadccccca3fd7fa53ffa020f08b8e28a12c2f5ef819`  
		Last Modified: Tue, 17 Feb 2026 20:23:46 GMT  
		Size: 149.9 MB (149858527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06773a3e09b92d59e995dd7e16a875c1ef0fe26f4b2ea6fdc2c0a8a7f18feaf`  
		Last Modified: Tue, 17 Feb 2026 20:23:50 GMT  
		Size: 336.2 MB (336222050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c717743b8d40f9f99dfd9d4eafcaafd6e08b2cad41c138a60beffa7013346d2e`  
		Last Modified: Tue, 17 Feb 2026 20:23:46 GMT  
		Size: 137.4 MB (137388268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e950429715913c7d4d9e5fca893c3444eef78eb039b192f22f2097edde7491`  
		Last Modified: Tue, 17 Feb 2026 20:23:39 GMT  
		Size: 54.9 KB (54897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk24-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:1b6d7a0228001e12ba35ac6c7d039e608537e7fedac82a28cf08a5e343a4400a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9051754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e421c5d22d99f48a0e2c9ccd4141bc66fb81ddd34ca7b220699741f83f082c60`

```dockerfile
```

-	Layers:
	-	`sha256:50c39b4a09c56ab12a66631361e47058e9ec97acb27354e8f196615533b1b61e`  
		Last Modified: Tue, 17 Feb 2026 20:23:39 GMT  
		Size: 9.0 MB (9023235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d23817d4736405f16de70380463f89b01cc170648dbdce6b0f26b7c87496c10`  
		Last Modified: Tue, 17 Feb 2026 20:23:39 GMT  
		Size: 28.5 KB (28519 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk24-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:3daed7a731bccdc2fcb83f3fd122d02382cf5c52c50e891699ad008e1e338b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.7 MB (620661706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e978b6ddcea2b6cb926a2566df0879ece7712bcd9d579d21379a226816c082ba`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:33:17 GMT
CMD ["gradle"]
# Tue, 17 Mar 2026 01:33:17 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 17 Mar 2026 01:33:17 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 17 Mar 2026 01:33:17 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 17 Mar 2026 01:33:17 GMT
WORKDIR /home/gradle
# Tue, 17 Mar 2026 01:33:57 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 17 Mar 2026 01:33:57 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 17 Mar 2026 01:33:57 GMT
ENV JAVA_VERSION=24.0.2
# Tue, 17 Mar 2026 01:34:16 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=6d62846c826ddb9307deec71e7661c26fa5a5e3985d7bb9005ea42163a390720     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c54d951a858791483d58270ecbc0946f28c4742c7fac74a4ebb2764bbf66d6f5     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 17 Mar 2026 01:34:16 GMT
ENV GRADLE_VERSION=8.14.4
# Tue, 17 Mar 2026 01:34:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Tue, 17 Mar 2026 01:34:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 17 Mar 2026 01:34:18 GMT
USER gradle
# Tue, 17 Mar 2026 01:34:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 17 Mar 2026 01:34:19 GMT
USER root
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d971df03df6100214c3a0c2f95bea3869dedae67bfcfc01663ba8ea58e6766`  
		Last Modified: Tue, 17 Mar 2026 01:34:54 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68583a0d62654ff65577df60772c7983deb26eeefc5a19eafefc8a7a81f849eb`  
		Last Modified: Tue, 17 Mar 2026 01:35:01 GMT  
		Size: 143.9 MB (143917340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f8fadd384d6dfa1da518c1ac1674534ee62a5057247bdab23ff0a3c4ec23ad`  
		Last Modified: Tue, 17 Mar 2026 01:35:04 GMT  
		Size: 310.4 MB (310425539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3026b3573383735b2b9c71b52c52ce443409413457a3ebef4dcf8b9da6e7df1`  
		Last Modified: Tue, 17 Mar 2026 01:35:01 GMT  
		Size: 137.4 MB (137388268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8391664e878355619785fc4c3535bcf2471f371ac7dc34b87c4bd76cd87e2de`  
		Last Modified: Tue, 17 Mar 2026 01:34:56 GMT  
		Size: 59.5 KB (59531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk24-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:5cdd0fd377c77364018fe17bd7352178696719b41dbe33cd979ad9f8e22a0409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9046886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098c16825b7c834f0aa768100ed9fedad41eb09964fdbe67b509b92fe830de6f`

```dockerfile
```

-	Layers:
	-	`sha256:719d2ba4b37655b25a3c03151fa7ce11e4aa165972015ecf261c54212f065cd5`  
		Last Modified: Tue, 17 Mar 2026 01:34:55 GMT  
		Size: 9.0 MB (9018167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7293cf49f3c8d35e3788c2ededec054ea5b8b6db91b8df57ba58b8e0d670309`  
		Last Modified: Tue, 17 Mar 2026 01:34:55 GMT  
		Size: 28.7 KB (28719 bytes)  
		MIME: application/vnd.in-toto+json
