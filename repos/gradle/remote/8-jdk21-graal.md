## `gradle:8-jdk21-graal`

```console
$ docker pull gradle@sha256:e696ffb92f3e505d5dec4c78ed78f8577cff41b5222415a926f639befc163004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gradle:8-jdk21-graal` - linux; amd64

```console
$ docker pull gradle@sha256:69e3f0b3f637e812ad1477d280cf1a0a9f37100188bee99d9dd66b89046f0eb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.8 MB (578793341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774aad66aae0b2571e928eceb39aadb0d36398cbe35806af490c82dd05aed72d`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:56:04 GMT
CMD ["gradle"]
# Fri, 02 Feb 2024 06:56:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 02 Feb 2024 06:58:48 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 02 Feb 2024 06:58:48 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 02 Feb 2024 06:58:48 GMT
WORKDIR /home/gradle
# Fri, 02 Feb 2024 06:59:13 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 02 Feb 2024 06:59:14 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 02 Feb 2024 06:59:14 GMT
ENV JAVA_VERSION=21.0.1
# Fri, 02 Feb 2024 06:59:25 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_DOWNLOAD_SHA256=5283EE48A61633F59A49ECDF0EF0AB4C5A8B006C16CE95209DF740BD2AEE73BF     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version
# Fri, 02 Feb 2024 06:59:27 GMT
ENV GRADLE_VERSION=8.5
# Fri, 02 Feb 2024 06:59:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
# Fri, 02 Feb 2024 06:59:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Fri, 02 Feb 2024 06:59:32 GMT
USER gradle
# Fri, 02 Feb 2024 06:59:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Fri, 02 Feb 2024 06:59:33 GMT
USER root
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea8137d42d3e10e2ce2d0bb90413a8cb52dfa1fa83e34c4ec833e6f1d836c4a`  
		Last Modified: Fri, 02 Feb 2024 07:03:29 GMT  
		Size: 4.4 KB (4361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5daba512302495a008b430e3ca3c9e997d8a91371bebce0b279e09a54778a4`  
		Last Modified: Fri, 02 Feb 2024 07:03:48 GMT  
		Size: 126.4 MB (126411604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff19e9786162f06736a632b3fd62f3e2b3d5d5c18a2671afe214db62b5b2552`  
		Last Modified: Fri, 02 Feb 2024 07:03:53 GMT  
		Size: 289.4 MB (289384599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baeaa8d23930fe0c122487fa211d9f1efc4b73feb85caef2229430bfcd0428f6`  
		Last Modified: Fri, 02 Feb 2024 07:03:37 GMT  
		Size: 132.5 MB (132544727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee563151a9bf351127b540abd6fa10acdc4f66136d5223a6de3fb49506a8305`  
		Last Modified: Fri, 02 Feb 2024 07:03:30 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
