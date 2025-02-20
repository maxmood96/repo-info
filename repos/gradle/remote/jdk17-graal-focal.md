## `gradle:jdk17-graal-focal`

```console
$ docker pull gradle@sha256:df883726e610dc059b3fc177ffa65bd05fe5d8c1ef8dc8b80f2009c1b36e700e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk17-graal-focal` - linux; amd64

```console
$ docker pull gradle@sha256:06a11a0c7a42fa5042db4b39d2c5f2cb7b21ad23d161e690756b2f33fd32bf0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.6 MB (588560841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4900428334c2ee26fa8e7c56ee50fa3c0a83428c38f508bb0dd2af6f92fb9509`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Wed, 19 Feb 2025 02:55:56 GMT
CMD ["gradle"]
# Wed, 19 Feb 2025 02:55:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 19 Feb 2025 02:55:56 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 19 Feb 2025 02:55:56 GMT
WORKDIR /home/gradle
# Wed, 19 Feb 2025 02:55:56 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 19 Feb 2025 02:55:56 GMT
ENV JAVA_VERSION=17.0.9
# Wed, 19 Feb 2025 02:55:56 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
ENV GRADLE_VERSION=8.12.1
# Wed, 19 Feb 2025 02:55:56 GMT
ARG GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
# Wed, 19 Feb 2025 02:55:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
USER gradle
# Wed, 19 Feb 2025 02:55:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
USER root
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8537b757efbc95c5955082681a973d4f27ce86a8777825a445db89222734067`  
		Last Modified: Wed, 19 Feb 2025 21:30:29 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32b4a8e3161a7e57d30653aa07a57fa92f670811f7ff142573bed0b5d3d1a3e`  
		Last Modified: Thu, 20 Feb 2025 01:32:42 GMT  
		Size: 133.4 MB (133364481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c814e3b434240f13c902c3f2cef9eb19488a19cf468da5ff8ba9733007d3a4`  
		Last Modified: Thu, 20 Feb 2025 01:32:51 GMT  
		Size: 291.1 MB (291064130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969af7b00f980275bbdfb78b974a72346612948c0ed13d27ccc59feb9549f7ee`  
		Last Modified: Thu, 20 Feb 2025 01:33:01 GMT  
		Size: 136.6 MB (136561934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70da88f255a0d2b96bcf7dd8d3469ba7bd7da761266449bd682974558565f190`  
		Last Modified: Wed, 19 Feb 2025 21:30:29 GMT  
		Size: 54.9 KB (54895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-graal-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:e08eb6ef13b036f97bafbcb09dc29129755de142db63732490a0f75b8879c12c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9459692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad5a8854ba7abc6922d0954dc74700bab3aafdb742a828d9b56d3a2020da7a2`

```dockerfile
```

-	Layers:
	-	`sha256:934c0b36cb236c0cf4d62ba68b8f2ec07ef788f1ddcef94e99fbcee6042a52b0`  
		Last Modified: Thu, 20 Feb 2025 00:34:22 GMT  
		Size: 9.4 MB (9431363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30a540ce27f0edab21bdc094dd6237b1be2dc494c61c46a49da5b5eb81a1c84b`  
		Last Modified: Thu, 20 Feb 2025 00:34:22 GMT  
		Size: 28.3 KB (28329 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-graal-focal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:8ffb00223aa1ed464eedc55e91fea90b1f09f84299feaeedc8e50e76fd857d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.6 MB (572604484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96fc6f3084150b64a82d00a7950befff2d4af306c43629f1f5036dd771762999`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Wed, 19 Feb 2025 02:55:56 GMT
CMD ["gradle"]
# Wed, 19 Feb 2025 02:55:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 19 Feb 2025 02:55:56 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 19 Feb 2025 02:55:56 GMT
WORKDIR /home/gradle
# Wed, 19 Feb 2025 02:55:56 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 19 Feb 2025 02:55:56 GMT
ENV JAVA_VERSION=17.0.9
# Wed, 19 Feb 2025 02:55:56 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
ENV GRADLE_VERSION=8.12.1
# Wed, 19 Feb 2025 02:55:56 GMT
ARG GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
# Wed, 19 Feb 2025 02:55:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
USER gradle
# Wed, 19 Feb 2025 02:55:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
USER root
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246473082eee96be802cf9b8b94bb0c5ad6a9c4bd4ebf44770fbcacd08edfe55`  
		Last Modified: Wed, 19 Feb 2025 21:35:46 GMT  
		Size: 4.3 KB (4318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aaee58be6a497204ef4fa6c92d231d5f4b642038702f30cf2e377c51cd5ac8d`  
		Last Modified: Wed, 19 Feb 2025 21:35:53 GMT  
		Size: 126.5 MB (126502989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482d9d7f554bc2c67a555ef2f1ed1b431e3fc037bd58f7cda15459a8307b9b0c`  
		Last Modified: Thu, 20 Feb 2025 01:13:26 GMT  
		Size: 283.5 MB (283501864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4764c62cc9792b142d5003da57e7fd523c0c86e2b4846a7b41001523b72b2a`  
		Last Modified: Thu, 20 Feb 2025 01:34:08 GMT  
		Size: 136.6 MB (136561935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b318880f92f02a63551fb571e0c4aa0234e2942312aced8f2f5c357af076e854`  
		Last Modified: Wed, 19 Feb 2025 21:35:47 GMT  
		Size: 59.5 KB (59518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-graal-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:1b14afa82bb7da2232183ed5524f767ac614a2e43943b2b5169088c9728060a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9437595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2c6f9926ec43e36bbed547c5306f657857aaa3a2b5031d21e053b0fbdc532c`

```dockerfile
```

-	Layers:
	-	`sha256:2512b3db98b6d6857823373e593b1478901b73eae4a32bd21b0fea631c563ebe`  
		Last Modified: Thu, 20 Feb 2025 00:34:27 GMT  
		Size: 9.4 MB (9409006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab1e8d406721680917f15555cfee20f6b28c6bf689dbd3ea108518809b6badd8`  
		Last Modified: Thu, 20 Feb 2025 00:34:28 GMT  
		Size: 28.6 KB (28589 bytes)  
		MIME: application/vnd.in-toto+json
