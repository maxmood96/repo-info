## `gradle:jdk-graal`

```console
$ docker pull gradle@sha256:4ef0cafa1f3b21bda38c9950905ec3a3d83894fc72a21a15f3578a5317b58555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gradle:jdk-graal` - linux; amd64

```console
$ docker pull gradle@sha256:6d47d8dd5ae4fa81e2de0bc347494eaaa2332222c186b655556d9f1a18264f6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.5 MB (580473141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66925c848bc2c5b913324272134db15d4139e5be5c4248446a0d364ccc17e7c`
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
# Fri, 02 Feb 2024 06:56:04 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 02 Feb 2024 06:56:05 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 02 Feb 2024 06:56:05 GMT
WORKDIR /home/gradle
# Fri, 02 Feb 2024 06:58:12 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 02 Feb 2024 06:58:13 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 02 Feb 2024 06:58:13 GMT
ENV JAVA_VERSION=17.0.9
# Fri, 02 Feb 2024 06:58:25 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_DOWNLOAD_SHA256=E47BA7229CEF02393E19D5B8F46F7F1CAB4829DD17BFE84D5431FC8FF0E22A96     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version
# Fri, 02 Feb 2024 06:58:26 GMT
ENV GRADLE_VERSION=8.5
# Fri, 02 Feb 2024 06:58:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
# Fri, 02 Feb 2024 06:58:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Fri, 02 Feb 2024 06:58:31 GMT
USER gradle
# Fri, 02 Feb 2024 06:58:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Fri, 02 Feb 2024 06:58:33 GMT
USER root
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cf8cf2f5ea3a0c89b77416f10cf06056df82fda748537c93cf92392905b135`  
		Last Modified: Fri, 02 Feb 2024 07:02:07 GMT  
		Size: 4.4 KB (4359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bd74a407e5a013c8df67ae56e344d0b7b610a9a81f848f91715512a39addcd`  
		Last Modified: Fri, 02 Feb 2024 07:02:26 GMT  
		Size: 126.4 MB (126411718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86cf9f0b213eb54fdf03d9a460b1d163b364425a3dd7eb2607c2d71c9959a440`  
		Last Modified: Fri, 02 Feb 2024 07:02:31 GMT  
		Size: 291.1 MB (291064298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679b93dae4cbf487b6a815a501a37cfa936a1f4e123b518927f733830edd496c`  
		Last Modified: Fri, 02 Feb 2024 07:02:15 GMT  
		Size: 132.5 MB (132544717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296904e83973e4dfe7ac2086b67e96941ade954bd624c42e81c34cdee7ad40f4`  
		Last Modified: Fri, 02 Feb 2024 07:02:07 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
