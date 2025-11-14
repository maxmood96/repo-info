## `gradle:9-graal-noble`

```console
$ docker pull gradle@sha256:24df4f1a9bdc4dccc7eed589b1ae0cc4f280b13d9e356fd8989f780f97015dbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:f388ed16a2e4998d16cc62348721c94cba63c039c9c91d2ea6d92cdd06d780af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.8 MB (654792094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea5cc23caba6addfc3a4e5330fcfac70f11894c778c7400e92bc249e5afe40f`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:22:19 GMT
CMD ["gradle"]
# Thu, 13 Nov 2025 23:22:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 13 Nov 2025 23:22:19 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 13 Nov 2025 23:22:19 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 13 Nov 2025 23:22:19 GMT
WORKDIR /home/gradle
# Thu, 13 Nov 2025 23:22:52 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 13 Nov 2025 23:22:52 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 13 Nov 2025 23:22:52 GMT
ENV JAVA_VERSION=25.0.1
# Thu, 13 Nov 2025 23:23:04 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=01e39fe1a87f28b842a3e4e3b77be9b544dca3a58fa6e93b924a6106c8bac7fb     && GRAALVM_AARCH64_DOWNLOAD_SHA256=7aa0b9935a80e67f37c6025678393dbd123bb6f2226811decbc1a13093fc8ae2     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Thu, 13 Nov 2025 23:23:04 GMT
ENV GRADLE_VERSION=9.2.0
# Thu, 13 Nov 2025 23:23:04 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Thu, 13 Nov 2025 23:23:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 13 Nov 2025 23:23:05 GMT
USER gradle
# Thu, 13 Nov 2025 23:23:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 13 Nov 2025 23:23:06 GMT
USER root
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeedd1aac0190c4049f098147de287e82e799098c46f8ad2806016464d3a2c41`  
		Last Modified: Thu, 13 Nov 2025 23:24:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b555f5a3ccbc24145395dd0220dba6d499d8ac18073aaa65caed6e0252c369f2`  
		Last Modified: Thu, 13 Nov 2025 23:23:53 GMT  
		Size: 148.6 MB (148638736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ee789719d64d7c56677a42ff7c17bf7c55ec0e2945c336b1a5eebbf884b891`  
		Last Modified: Thu, 13 Nov 2025 23:23:56 GMT  
		Size: 340.9 MB (340850794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1d228cb28db57eeb36183f9085f8febed6ffeb042619558bf8125d2c0e63fc`  
		Last Modified: Thu, 13 Nov 2025 23:23:53 GMT  
		Size: 135.5 MB (135521657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23344c97a9ccde0b6d84b5b3858bc2d0704b0e857dd6192b7c7bdaaf65aa3d74`  
		Last Modified: Thu, 13 Nov 2025 23:24:00 GMT  
		Size: 54.9 KB (54900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:f95326e60f72654e9c8127b0953a9bc8ab2f9be12b1540dd24e9b0a6a423a17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9063486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f0553d2bf2f4d3afa54523a9c24e6da1219d60c88c39fce1fabc91da846838`

```dockerfile
```

-	Layers:
	-	`sha256:cfb7ccbde18ae006ea44039860956bfbe4c0e7d9f0aeda6d953d09fe471bb0ee`  
		Last Modified: Fri, 14 Nov 2025 03:33:55 GMT  
		Size: 9.0 MB (9029595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f951d2391c2a3234822be693b561ea8688688cda3f89e53134cb68cb29996d8b`  
		Last Modified: Fri, 14 Nov 2025 03:33:56 GMT  
		Size: 33.9 KB (33891 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e738067efafe69f2396fa4ba241ea1862acbc6fadd529d605173bad50c25a89a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.1 MB (624077036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73edf45d0d0d635ee345ad01b45d88396f8fb3512406634c1e32bc9ae990f34f`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:53 GMT
CMD ["gradle"]
# Thu, 13 Nov 2025 23:21:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 13 Nov 2025 23:21:53 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 13 Nov 2025 23:21:53 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 13 Nov 2025 23:21:53 GMT
WORKDIR /home/gradle
# Thu, 13 Nov 2025 23:22:23 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 13 Nov 2025 23:22:23 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 13 Nov 2025 23:22:23 GMT
ENV JAVA_VERSION=25.0.1
# Thu, 13 Nov 2025 23:22:36 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=01e39fe1a87f28b842a3e4e3b77be9b544dca3a58fa6e93b924a6106c8bac7fb     && GRAALVM_AARCH64_DOWNLOAD_SHA256=7aa0b9935a80e67f37c6025678393dbd123bb6f2226811decbc1a13093fc8ae2     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Thu, 13 Nov 2025 23:22:36 GMT
ENV GRADLE_VERSION=9.2.0
# Thu, 13 Nov 2025 23:22:36 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Thu, 13 Nov 2025 23:22:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 13 Nov 2025 23:22:39 GMT
USER gradle
# Thu, 13 Nov 2025 23:22:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 13 Nov 2025 23:22:39 GMT
USER root
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46a1e690837dbc4d3568d4f63c4a304bea74989592f560e35d6eb6072fd902d`  
		Last Modified: Thu, 13 Nov 2025 23:23:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a8fcd708a067c555584b1995135f9aaef93807843e497fc2e420235928b706`  
		Last Modified: Thu, 13 Nov 2025 23:23:22 GMT  
		Size: 143.7 MB (143743659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dc72a6d8b09c844374287bd95d094be9d4e4628eba41a14217cea6ef4f2ec6`  
		Last Modified: Thu, 13 Nov 2025 23:23:25 GMT  
		Size: 315.9 MB (315888914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7388f52f63c319a51b32462f7e8e038ff03b4f964bb5f4a1efa24e4c8a8f05`  
		Last Modified: Thu, 13 Nov 2025 23:23:23 GMT  
		Size: 135.5 MB (135521659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea1b722e94a997b77184f06d08969b2e914c8411eb3533beaf80ca03266ed6f`  
		Last Modified: Thu, 13 Nov 2025 23:23:30 GMT  
		Size: 59.5 KB (59528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:96a1c118f017c5739bd8208e3dcd51d329034aa6a5e323ab36135c2f5ff8694a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9059029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794002a99ff5c9cda657d0fb593e5ef96d1f1d29d05b84446355029c76bcb3e2`

```dockerfile
```

-	Layers:
	-	`sha256:68e9ec7d319b6989f43fe98deabb839ba918241e6b0d4d213366362086482bdd`  
		Last Modified: Fri, 14 Nov 2025 03:34:02 GMT  
		Size: 9.0 MB (9024735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84d48d6ff2d0c8b96b085d84037c0803044a695d0f6bad3e61efad6577bc7983`  
		Last Modified: Fri, 14 Nov 2025 03:34:03 GMT  
		Size: 34.3 KB (34294 bytes)  
		MIME: application/vnd.in-toto+json
