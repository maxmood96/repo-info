## `gradle:graal`

```console
$ docker pull gradle@sha256:01e949ace2c7a55555cbd2c42f30c64ec9ed4ba050a54b2e9e77ae544bfc164d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gradle:graal` - linux; amd64

```console
$ docker pull gradle@sha256:b2f6bc0a6ea998d4c3a69d07385427ee0b32e3891d620f7b03027d5d86f257c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.4 MB (577418141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb65ea8f1ae9bd39b6cb4fa3ac02a2add3301581a076c2886f37797e2a59274`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 15 Aug 2023 23:20:55 GMT
CMD ["gradle"]
# Tue, 15 Aug 2023 23:20:55 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 15 Aug 2023 23:20:56 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 15 Aug 2023 23:20:56 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 15 Aug 2023 23:20:56 GMT
WORKDIR /home/gradle
# Tue, 15 Aug 2023 23:21:55 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Tue, 15 Aug 2023 23:21:56 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 15 Aug 2023 23:22:12 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && JDK_VERSION=17.0.8     && GRAALVM_DOWNLOAD_SHA256=1dffdf5c7cc5bf38558e9f093eef6a14072a6dff0be3a9906208b37b53ecc009     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JDK_VERSION}/graalvm-community-jdk-${JDK_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version
# Tue, 15 Aug 2023 23:22:13 GMT
ENV GRADLE_VERSION=8.2.1
# Tue, 15 Aug 2023 23:22:13 GMT
ARG GRADLE_DOWNLOAD_SHA256=03ec176d388f2aa99defcadc3ac6adf8dd2bce5145a129659537c0874dea5ad1
# Tue, 15 Aug 2023 23:22:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=03ec176d388f2aa99defcadc3ac6adf8dd2bce5145a129659537c0874dea5ad1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version         && chown --recursive gradle:gradle /home/gradle
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21baf8eb83031f83e6c61ff60cf08d178c6d4d980642cd46f17385ccfbe0cd41`  
		Last Modified: Tue, 15 Aug 2023 23:28:58 GMT  
		Size: 4.4 KB (4357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da65c63bcadd8d874f3f79bb09744f1a2b5f60e3b32955869b0ee72804930983`  
		Last Modified: Tue, 15 Aug 2023 23:29:18 GMT  
		Size: 127.4 MB (127353728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a56799d9451061fe60f281e63f457e1b253bff5ac63fc0c5f1adfd9fe16b34`  
		Last Modified: Tue, 15 Aug 2023 23:29:23 GMT  
		Size: 290.9 MB (290900306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9fb1ab385c9fa8470e673fbb035234ac1e3e8f8ced9262079de01dad403b1d`  
		Last Modified: Tue, 15 Aug 2023 23:29:08 GMT  
		Size: 128.7 MB (128728521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
