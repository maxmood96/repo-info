## `gradle:7-jdk17-graal-focal`

```console
$ docker pull gradle@sha256:61a8ffa9d8d9c6740dc60114e89353c581ede080d652d5e9de163d0b1521c155
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk17-graal-focal` - linux; amd64

```console
$ docker pull gradle@sha256:687b215e74b0014ad2c642050ef1f92f3880f8180ab471917dfd46d1992f8dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.7 MB (574729549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee9c908d34eb973b7e5784e180af06437c50dda113eeff633306741747123ca`
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
# Tue, 18 Feb 2025 21:10:40 GMT
CMD ["gradle"]
# Tue, 18 Feb 2025 21:10:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 18 Feb 2025 21:10:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 18 Feb 2025 21:10:40 GMT
WORKDIR /home/gradle
# Tue, 18 Feb 2025 21:10:40 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 18 Feb 2025 21:10:40 GMT
ENV JAVA_VERSION=17.0.9
# Tue, 18 Feb 2025 21:10:40 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
ENV GRADLE_VERSION=7.6.4
# Tue, 18 Feb 2025 21:10:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Tue, 18 Feb 2025 21:10:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
USER gradle
# Tue, 18 Feb 2025 21:10:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
USER root
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f438d3ed390b3ecac3ba6f459680306294b460edc2e1d41b748430173e57b1`  
		Last Modified: Wed, 19 Feb 2025 21:31:12 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef19d5ad95eb5781257687791892eb916271448aae0913f282378ba8b20c586`  
		Last Modified: Thu, 20 Feb 2025 01:22:59 GMT  
		Size: 133.4 MB (133364561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f418255a8598fb2746dddefc4ee6e127e2f342ef7885346482ccb5a6a19eaf0`  
		Last Modified: Thu, 20 Feb 2025 01:23:07 GMT  
		Size: 291.1 MB (291064170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52e2e3486ce649d713456268c4ae24ed830049bef8bf78dd599c3292e5c2e9a`  
		Last Modified: Thu, 20 Feb 2025 01:23:32 GMT  
		Size: 122.7 MB (122730519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a210aa11491f70dcea1f770e73b9830fe582ffbb53b2569b7b4f15cab15780`  
		Last Modified: Wed, 19 Feb 2025 21:31:13 GMT  
		Size: 54.9 KB (54900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-graal-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:718a8e270a763c11d8d579e92ae293689d366af8dd08e0a64d92b937d895e02c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9370240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f3f6ec129ab79f6852898ffffcc9eb6371fcee53c19791deec913ddbc273fce`

```dockerfile
```

-	Layers:
	-	`sha256:e404cf0aa42552c290cc4bc19c48816f6caa85b1e9b9218af6cdc43a33818f4e`  
		Last Modified: Thu, 20 Feb 2025 00:26:43 GMT  
		Size: 9.3 MB (9342869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da2faa4c24b8db9157792bd59dc5dd26f1d1bb105a07f1648fa577b4ea5f1e35`  
		Last Modified: Thu, 20 Feb 2025 00:26:44 GMT  
		Size: 27.4 KB (27371 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-graal-focal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:fe01d36b9b0291a7758c0372b2240981feb2b044bf0c1bc2cbb3292779f7d73e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.8 MB (558773084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248031d27e0bea680d3b4ab7b478f6257810c5124535eaab8e686050935ad418`
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
# Tue, 18 Feb 2025 21:10:40 GMT
CMD ["gradle"]
# Tue, 18 Feb 2025 21:10:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 18 Feb 2025 21:10:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 18 Feb 2025 21:10:40 GMT
WORKDIR /home/gradle
# Tue, 18 Feb 2025 21:10:40 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 18 Feb 2025 21:10:40 GMT
ENV JAVA_VERSION=17.0.9
# Tue, 18 Feb 2025 21:10:40 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
ENV GRADLE_VERSION=7.6.4
# Tue, 18 Feb 2025 21:10:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Tue, 18 Feb 2025 21:10:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
USER gradle
# Tue, 18 Feb 2025 21:10:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
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
	-	`sha256:5c2ef22f2491e0f23437857df3fa9f3f81c2f20c57ba0cdc6a2f63a20b7bf401`  
		Last Modified: Wed, 19 Feb 2025 22:18:25 GMT  
		Size: 122.7 MB (122730519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a8a099b325d433d6696cc4505ffe4eea4bbb5c640f59d027f9acca614e045b`  
		Last Modified: Wed, 19 Feb 2025 22:17:59 GMT  
		Size: 59.5 KB (59534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-graal-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:7c17e83aa78c1c33b3bce25b0bcc093c9f7cbb74b1baf3948df912e52c48f2d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9348071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b255b4f5d64a6244830f6a6f85685c5de5b3c3c6284de1b8b3e87f894712c3`

```dockerfile
```

-	Layers:
	-	`sha256:a0814d08225157c3224590bd9b1f1d4202745b2ffe4afc40ff9c49328b246541`  
		Last Modified: Thu, 20 Feb 2025 00:26:53 GMT  
		Size: 9.3 MB (9320476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3804975a5ba59fc8fc2a7b71d81a692e935b77e37bd0ac39fe6c9729bfb5cdc0`  
		Last Modified: Thu, 20 Feb 2025 00:26:53 GMT  
		Size: 27.6 KB (27595 bytes)  
		MIME: application/vnd.in-toto+json
