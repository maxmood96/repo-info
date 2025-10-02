## `gradle:8-jdk24-graal-noble`

```console
$ docker pull gradle@sha256:28ce0bd463a1cc1f2cf682cb5a1579219a077067cc05ca28fa623e63c31e4c94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk24-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:759ea7afe0e52584491aab15e0ca388f93a07369d992356584016de3bbaea98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.4 MB (654425974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d626e609fb316a9ce40627d8a664dfd3d99ff47fa75ef47018fded3b0c64a6`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 29 Sep 2025 16:01:58 GMT
ARG RELEASE
# Mon, 29 Sep 2025 16:01:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Sep 2025 16:01:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Sep 2025 16:01:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Sep 2025 16:01:58 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Mon, 29 Sep 2025 16:01:58 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:01:58 GMT
CMD ["gradle"]
# Mon, 29 Sep 2025 16:01:58 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Sep 2025 16:01:58 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Sep 2025 16:01:58 GMT
WORKDIR /home/gradle
# Mon, 29 Sep 2025 16:01:58 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Mon, 29 Sep 2025 16:01:58 GMT
ENV JAVA_VERSION=24.0.2
# Mon, 29 Sep 2025 16:01:58 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=6d62846c826ddb9307deec71e7661c26fa5a5e3985d7bb9005ea42163a390720     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c54d951a858791483d58270ecbc0946f28c4742c7fac74a4ebb2764bbf66d6f5     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
ENV GRADLE_VERSION=8.14.3
# Mon, 29 Sep 2025 16:01:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Mon, 29 Sep 2025 16:01:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
USER gradle
# Mon, 29 Sep 2025 16:01:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
USER root
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53a8572043749bd457bbe2a5807b8567873a942164badfadb417cccfec88194`  
		Last Modified: Thu, 02 Oct 2025 05:05:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa753d54fc8f057dcfef161e44b9d2578c4f0b7abf64a4b6b7e4e650cc3d2c09`  
		Last Modified: Thu, 02 Oct 2025 10:36:31 GMT  
		Size: 151.0 MB (151029525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ee99d2f22c3e537d7ad647ceb00e104ab7b93fc6f0c077234c892cc236bad6`  
		Last Modified: Thu, 02 Oct 2025 07:43:38 GMT  
		Size: 336.2 MB (336222021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3c1cfd6b408b8ac6b92090dbf57f539457dc4d3e2be7c5c3aa9c6e6e999ee2`  
		Last Modified: Thu, 02 Oct 2025 10:36:30 GMT  
		Size: 137.4 MB (137395194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4847a82e6d15ede108c5b56298e6af917b715e6c2a8a59cb7935bf493d04cc`  
		Last Modified: Thu, 02 Oct 2025 05:05:58 GMT  
		Size: 54.9 KB (54906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk24-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:76a3a13996a8e582d820797b9aa0f75a594d50ffb27f342eef1ab95f7777f96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9051681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff1f88a55c1c2b1b44faf914a31fcde6e6d0dd46472483f62c5b12da806ae52`

```dockerfile
```

-	Layers:
	-	`sha256:e03f5bb37214a2d7e941cc9af561a87d9e201b58d92fce0a5f372c4dcb1d2c21`  
		Last Modified: Thu, 02 Oct 2025 05:25:23 GMT  
		Size: 9.0 MB (9023119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd939fc3dadbf564b5aa4465474c9b90d412a3a8b03518cf9a29e35b6e80caf`  
		Last Modified: Thu, 02 Oct 2025 05:25:24 GMT  
		Size: 28.6 KB (28562 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk24-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:981161ed422d90bd6c1f31e13179c3efb6dfd93887ca959946936bf0eba43099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.7 MB (622684099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73be07badf6d5fa2ef993359b09aa492e462b193af7cdf91190e2e7e301a2f6`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 29 Sep 2025 16:01:58 GMT
ARG RELEASE
# Mon, 29 Sep 2025 16:01:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Sep 2025 16:01:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Sep 2025 16:01:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Sep 2025 16:01:58 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Mon, 29 Sep 2025 16:01:58 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:01:58 GMT
CMD ["gradle"]
# Mon, 29 Sep 2025 16:01:58 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Sep 2025 16:01:58 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Sep 2025 16:01:58 GMT
WORKDIR /home/gradle
# Mon, 29 Sep 2025 16:01:58 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Mon, 29 Sep 2025 16:01:58 GMT
ENV JAVA_VERSION=24.0.2
# Mon, 29 Sep 2025 16:01:58 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=6d62846c826ddb9307deec71e7661c26fa5a5e3985d7bb9005ea42163a390720     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c54d951a858791483d58270ecbc0946f28c4742c7fac74a4ebb2764bbf66d6f5     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
ENV GRADLE_VERSION=8.14.3
# Mon, 29 Sep 2025 16:01:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Mon, 29 Sep 2025 16:01:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
USER gradle
# Mon, 29 Sep 2025 16:01:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
USER root
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1b066ab0e02d2247c92b0221ff88d82c07e3c588a31f0b113bab5a1435f62f`  
		Last Modified: Thu, 02 Oct 2025 01:20:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29d4be43343111d79b236d6e42c8d3c6ba649b9b0d5ba42147a8aeea4bd1301`  
		Last Modified: Thu, 02 Oct 2025 15:33:35 GMT  
		Size: 145.9 MB (145940993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fad44e29c459293ab266050ea1453b8706f3e9b339fbb98f85d1898b9c06a6`  
		Last Modified: Thu, 02 Oct 2025 15:29:28 GMT  
		Size: 310.4 MB (310425481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28af922dd127145aaf2183e0de2dfd855912e239cdf6edccad6b2a84e483f916`  
		Last Modified: Thu, 02 Oct 2025 15:16:40 GMT  
		Size: 137.4 MB (137395195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a00012da8fe707566bce78154612f58a25aee9c7f2f5e05e2de6e34aa35f54`  
		Last Modified: Thu, 02 Oct 2025 02:09:08 GMT  
		Size: 59.5 KB (59536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk24-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:a976cb3b129088d0a48c27c8d79ab600023c3e009847f6e7758ab4da62f26bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9046805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d16ae5620318721c7062f46dcb8bc663a793532edcbcc4f46055a490d15b54`

```dockerfile
```

-	Layers:
	-	`sha256:07961ace51bbeab24764f6348758c447325f19ac3ab8e39a638defc36068fdd8`  
		Last Modified: Thu, 02 Oct 2025 05:25:32 GMT  
		Size: 9.0 MB (9018043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c8919c7bf9344831964c056d41df9e72fc54cf303e29fc58e17c54dbcf2d3b`  
		Last Modified: Thu, 02 Oct 2025 05:25:33 GMT  
		Size: 28.8 KB (28762 bytes)  
		MIME: application/vnd.in-toto+json
