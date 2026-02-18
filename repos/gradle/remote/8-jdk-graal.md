## `gradle:8-jdk-graal`

```console
$ docker pull gradle@sha256:cd52df02bc8e702a4921e0872591e0d8e4d024503965a0be66730cc6f168d45f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk-graal` - linux; amd64

```console
$ docker pull gradle@sha256:a9e000bc8c837fc3a9c7e7fb0639f6e0595d30c2df6c6930c5af4e0fff7b13f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.0 MB (607017534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3deba78f5862352f70d4d535f1fe06f7d2f9ee1eead0ed17a2d6dcb15610212e`
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
# Tue, 17 Feb 2026 20:21:05 GMT
CMD ["gradle"]
# Tue, 17 Feb 2026 20:21:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 17 Feb 2026 20:21:05 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 17 Feb 2026 20:21:05 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 17 Feb 2026 20:21:05 GMT
WORKDIR /home/gradle
# Tue, 17 Feb 2026 20:21:42 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 17 Feb 2026 20:21:42 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 17 Feb 2026 20:21:42 GMT
ENV JAVA_VERSION=21.0.2
# Tue, 17 Feb 2026 20:21:50 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 17 Feb 2026 20:21:50 GMT
ENV GRADLE_VERSION=8.14.4
# Tue, 17 Feb 2026 20:21:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Tue, 17 Feb 2026 20:21:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 17 Feb 2026 20:21:53 GMT
USER gradle
# Tue, 17 Feb 2026 20:21:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 17 Feb 2026 20:21:53 GMT
USER root
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55122907e1edcc73eebbe5a6a7ed1cd89153980e071639707582f688336a3c5`  
		Last Modified: Tue, 17 Feb 2026 20:22:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b43e431ec4bfa603d5b04d2cd34b4f82dc7f2c3016491abc51944598f517a4`  
		Last Modified: Tue, 17 Feb 2026 20:22:33 GMT  
		Size: 149.9 MB (149859452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b486d3b6d32585b273ef856236959d8980f2bd773141a05d0af847f9e1fc5f`  
		Last Modified: Tue, 17 Feb 2026 20:22:35 GMT  
		Size: 290.0 MB (289985990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578fa018f03c78a6d2569303d8b4ff2356f3ee5959f5d03b1ec7887ab1965cf8`  
		Last Modified: Tue, 17 Feb 2026 20:22:32 GMT  
		Size: 137.4 MB (137388272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d0cf4b205cb96adf10a1e5bdbe55c7d91572df71016dfc23ddb7535df096e4`  
		Last Modified: Tue, 17 Feb 2026 20:22:27 GMT  
		Size: 54.9 KB (54892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:bc4442accffcddf1419c58fd2f4e86f051141e394a9bc2a876f71dab73f44ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9021812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669f5550783e63ea1448c208b0ea3fee8bf7e352e71798c0a4e1b7f9823cdf6e`

```dockerfile
```

-	Layers:
	-	`sha256:ff3040519ce31575567b071511fd6297cf9032a00f5cff3bbaf1c4d8851cbad8`  
		Last Modified: Tue, 17 Feb 2026 20:22:26 GMT  
		Size: 9.0 MB (8989817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5743ee9a8dbf520a07dcfa9fbb499b75c2b3ce52848e456fb9fddb75b63e349d`  
		Last Modified: Tue, 17 Feb 2026 20:22:25 GMT  
		Size: 32.0 KB (31995 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:98a5c6372389e5c52178142af172b40a99cccdcbfdc2cf5b9996cfa57d50cf8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.9 MB (592901420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da84b7eca012cfc1d04eb84e248c16a71b1c6473f2f75da0424ff37ca36451e`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:20:40 GMT
CMD ["gradle"]
# Tue, 17 Feb 2026 20:20:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 17 Feb 2026 20:20:40 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 17 Feb 2026 20:20:40 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 17 Feb 2026 20:20:40 GMT
WORKDIR /home/gradle
# Tue, 17 Feb 2026 20:21:12 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 17 Feb 2026 20:21:12 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 17 Feb 2026 20:21:12 GMT
ENV JAVA_VERSION=21.0.2
# Tue, 17 Feb 2026 20:21:21 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 17 Feb 2026 20:21:21 GMT
ENV GRADLE_VERSION=8.14.4
# Tue, 17 Feb 2026 20:21:21 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Tue, 17 Feb 2026 20:21:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 17 Feb 2026 20:21:23 GMT
USER gradle
# Tue, 17 Feb 2026 20:21:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 17 Feb 2026 20:21:24 GMT
USER root
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424559fe2a206cf8694b7bcfb7eeee2c4622ee6bd880a4f6cda49ad0823455c4`  
		Last Modified: Tue, 17 Feb 2026 20:21:55 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a9a1553519ba0aed32f8ff906a77e32f9562c7de859f17fa7daf87e29b0a9c`  
		Last Modified: Tue, 17 Feb 2026 20:22:03 GMT  
		Size: 144.9 MB (144921021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77439d8c339800ef54d9283171d05d49777b40aae5027a0fe9ba1cdbb8153ace`  
		Last Modified: Tue, 17 Feb 2026 20:22:05 GMT  
		Size: 281.7 MB (281666160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50743ea7ab00985d522538b4254ec5563d4ab72c235a2becede06fb044b37d4`  
		Last Modified: Tue, 17 Feb 2026 20:22:03 GMT  
		Size: 137.4 MB (137388270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568b54e97a531ca5487f8d7958545f33a20a2d1f5803513166ac07f939a6b552`  
		Last Modified: Tue, 17 Feb 2026 20:21:56 GMT  
		Size: 59.5 KB (59531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:769e7b4ed8f1730d0ee944bf3ea6c3592312eb61e53c52d376b877ab13e7d0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9017844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48b5084175d35fe57081f49319d4c857355d9f61a81b01211c3afbc3c56a266`

```dockerfile
```

-	Layers:
	-	`sha256:3596882dfbec39af878f52d12b71c12417d2900b276aa43fb64931ade799ea84`  
		Last Modified: Tue, 17 Feb 2026 20:21:56 GMT  
		Size: 9.0 MB (8985518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a80c66e0be1e9bfc7ad2cdb2e100b8443bac46f49d22ef54f0f15dcab36f5b5c`  
		Last Modified: Tue, 17 Feb 2026 20:21:55 GMT  
		Size: 32.3 KB (32326 bytes)  
		MIME: application/vnd.in-toto+json
