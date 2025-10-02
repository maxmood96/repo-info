## `gradle:7-graal-noble`

```console
$ docker pull gradle@sha256:be84a17a6da280a57294dc68eae75995fc898c0ec14b8f5dbdd5114aca12717e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:3455a4a0971b891650f95b5c5e767ae3b0df407f85e01d33069991dc0fe4b902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597926152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6d1fcf705d67578a2bfe868a2ddec332df9b4ce7c7e0ee31ca1c5f368e2377`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 05 Jul 2025 02:17:41 GMT
ARG RELEASE
# Sat, 05 Jul 2025 02:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 05 Jul 2025 02:17:41 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:17:41 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_VERSION=17.0.9
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 05 Jul 2025 02:17:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER gradle
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER root
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd9e748f5ffcc7e94ddcf86284eade45d9757b890c766641a04700d26e54244`  
		Last Modified: Mon, 15 Sep 2025 22:13:36 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a37d2ef946171eb6eb757841def4cf3cf4539fdff0136e4be4dc851e8c87d`  
		Last Modified: Tue, 16 Sep 2025 06:14:44 GMT  
		Size: 148.6 MB (148612878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54bccae9420e95395c43941dcdad2db7cc076428fa9079ea864dff3ea62a259c`  
		Last Modified: Tue, 16 Sep 2025 13:52:31 GMT  
		Size: 291.1 MB (291064190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca09deeecf47d04d18516f1eed7f777eb83ed9ebd3f8e4fc0f5b04fb3e92292`  
		Last Modified: Tue, 16 Sep 2025 13:52:18 GMT  
		Size: 128.5 MB (128469418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c989156d6c5f66bf287e38176b0b9600c0e7c434882a49e15a863c15ff45a8b5`  
		Last Modified: Mon, 15 Sep 2025 22:54:39 GMT  
		Size: 54.9 KB (54900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:76a130dc38bc14da34eb7fabb5da72239421a1a9701cb0bd421d70bb3e3adbd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8955329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd87eaf898e2c8fd75eab80d5084e7f40431fab52a4caee04938e10e2e792b2`

```dockerfile
```

-	Layers:
	-	`sha256:0c99fc929be8708d2a538d271e0a5b1ade716b2c4dd9568583de9693e112dd96`  
		Last Modified: Tue, 16 Sep 2025 02:18:14 GMT  
		Size: 8.9 MB (8923217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4fc38cab56240ad6d69f9fa75308de2ebfe4fbb3aa645f12a7b3d249b777c21`  
		Last Modified: Tue, 16 Sep 2025 02:18:15 GMT  
		Size: 32.1 KB (32112 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:9b1cdd4c582cfb6d5cdfeea5405bbc9b77ab7f1234781de7192d82105e6e39d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586834244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c0f8292bb583d65d1af4cb868c5c8bedf882d43e5fcdcbfdd2a41caabe11c3`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 23 Sep 2025 15:37:00 GMT
ARG RELEASE
# Tue, 23 Sep 2025 15:37:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 15:37:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 15:37:00 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Sep 2025 15:37:00 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 23 Sep 2025 15:37:00 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 15:37:00 GMT
CMD ["gradle"]
# Tue, 23 Sep 2025 15:37:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 23 Sep 2025 15:37:00 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 23 Sep 2025 15:37:00 GMT
WORKDIR /home/gradle
# Tue, 23 Sep 2025 15:37:00 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 23 Sep 2025 15:37:00 GMT
ENV JAVA_VERSION=17.0.9
# Tue, 23 Sep 2025 15:37:00 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 23 Sep 2025 15:37:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 23 Sep 2025 15:37:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
USER gradle
# Tue, 23 Sep 2025 15:37:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
USER root
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06b95a64561736545d7d8df27a80ee037c83e490475d117319874f5f25dcc21`  
		Last Modified: Thu, 02 Oct 2025 02:10:00 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3afeec2a8c5972e8d88036360dd27979c9c33ef8276dd488ffe00ea36bba1d`  
		Last Modified: Thu, 02 Oct 2025 01:21:32 GMT  
		Size: 145.9 MB (145940584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7776438effd635b27a3f96364f28523eb43de7e930a25652fe14cc358a8dbed`  
		Last Modified: Thu, 02 Oct 2025 01:21:34 GMT  
		Size: 283.5 MB (283501819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18d22ae1c780411b799a82fbcfaac866e678864e9081dfd4aebb5ec54c96e97`  
		Last Modified: Thu, 02 Oct 2025 01:21:31 GMT  
		Size: 128.5 MB (128469416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abeffae9f4e92ae1b7934672444bd8632f55e69641f009d204030fee5c03fb55`  
		Last Modified: Thu, 02 Oct 2025 02:09:59 GMT  
		Size: 59.5 KB (59524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:ec6bf042cc886f651d6f48d8ef6c70553ea27c9257de766db75031f06cb691c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8951366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37bc03d561fd1a14304bfb65c3239603b602f0e3384d8db4ff898fff071c6f23`

```dockerfile
```

-	Layers:
	-	`sha256:299f939eb53005a0226d9ae1a139c1cbc07b4ee87d35a3ca188b06e168749ec0`  
		Last Modified: Thu, 02 Oct 2025 05:19:22 GMT  
		Size: 8.9 MB (8918922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d00ca7cedd988b87378a72371f3ca3d30412d5cc131dfa2e0b4a15e735fec8bb`  
		Last Modified: Thu, 02 Oct 2025 05:19:24 GMT  
		Size: 32.4 KB (32444 bytes)  
		MIME: application/vnd.in-toto+json
