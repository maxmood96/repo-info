## `gradle:8-jdk24-graal-noble`

```console
$ docker pull gradle@sha256:21e6e8d314269eacec2facbabb761ad661c4d212903a8f5f7d374fdea6d2d2af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk24-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:6938a83976967cb2c0f8ebcb0e4019e29916c429fff9daef5eb30bafe8171a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.7 MB (651709332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3133d07519d5619e33253e7fd1f19e57d513c704a4000e8197ea0edddb6a13be`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:48 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:44:50 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 28 Apr 2025 09:44:51 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 02:26:11 GMT
CMD ["gradle"]
# Tue, 27 May 2025 02:26:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 27 May 2025 02:26:11 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 27 May 2025 02:26:11 GMT
WORKDIR /home/gradle
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 27 May 2025 02:26:11 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 27 May 2025 02:26:11 GMT
ENV JAVA_VERSION=24.0.1
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=d2c544de672e400476a09c8f1da79ecc6b774a9441e234948542c3b3e6a84bde     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a3d1be8fadfb0d3df632252301f79a9b02b47e523da66539d370c62e683d762e     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 27 May 2025 02:26:11 GMT
ENV GRADLE_VERSION=8.14.1
# Tue, 27 May 2025 02:26:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
# Tue, 27 May 2025 02:26:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 27 May 2025 02:26:11 GMT
USER gradle
# Tue, 27 May 2025 02:26:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 27 May 2025 02:26:11 GMT
USER root
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03328effc034dc45888aa019e4c0edc21d7d4817a2b8d86ab1ad2fe8186f11dc`  
		Last Modified: Tue, 27 May 2025 18:59:57 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b55264bf0ba4c35c8f6d0b2ddf8b35130001582c79e18ec759aaafc3944b22d`  
		Last Modified: Tue, 27 May 2025 19:00:00 GMT  
		Size: 148.4 MB (148428852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c71f9052a5d00d50142ca8f068ca5171da637326a8cf08f847410af7b13b7c0`  
		Last Modified: Tue, 27 May 2025 19:00:03 GMT  
		Size: 336.1 MB (336111194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3092387957427294ac179ad41095fd8b342a0d537d0b0d5c79da535bff0faf4`  
		Last Modified: Tue, 27 May 2025 19:00:00 GMT  
		Size: 137.4 MB (137395537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66dd6e4026838d7480db73fdfe252cc531b78976f4b56f326dd00b360b8a72`  
		Last Modified: Tue, 27 May 2025 18:59:58 GMT  
		Size: 54.9 KB (54900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk24-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:d48a2f302fe252a9b2030b697cca565a5efcf8b9eb974773adc44e502ee74bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8827151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ab4ba10b6dc2f62f11bed22f26229a409b4324964eeacb7721f099cd3ffb6d`

```dockerfile
```

-	Layers:
	-	`sha256:cbc17622cb2b28ddd80017098560b4b7c294f697719e6cd2eb6f24ba9b7cd80f`  
		Last Modified: Tue, 27 May 2025 18:59:58 GMT  
		Size: 8.8 MB (8799975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:298b5f75d3b1f016a61a251f187168623f80c7365f875bea681663f38d5661e7`  
		Last Modified: Tue, 27 May 2025 18:59:57 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk24-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e84c6260af8104febae9d9d218064fb1dd4d56c06d40abbd531bfd0a9068b83a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.1 MB (620125468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d7d432196d20c42f142911cedc92558423963d657247e9dbad12d14a73d7f5`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:58 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:45:01 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 28 Apr 2025 09:45:01 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 02:26:11 GMT
CMD ["gradle"]
# Tue, 27 May 2025 02:26:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 27 May 2025 02:26:11 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 27 May 2025 02:26:11 GMT
WORKDIR /home/gradle
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 27 May 2025 02:26:11 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 27 May 2025 02:26:11 GMT
ENV JAVA_VERSION=24.0.1
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=d2c544de672e400476a09c8f1da79ecc6b774a9441e234948542c3b3e6a84bde     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a3d1be8fadfb0d3df632252301f79a9b02b47e523da66539d370c62e683d762e     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 27 May 2025 02:26:11 GMT
ENV GRADLE_VERSION=8.14.1
# Tue, 27 May 2025 02:26:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
# Tue, 27 May 2025 02:26:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 27 May 2025 02:26:11 GMT
USER gradle
# Tue, 27 May 2025 02:26:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 27 May 2025 02:26:11 GMT
USER root
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f4a130967abc8e527f507f6887c3f7c600bfa74a249b7a1077686270d72b6a`  
		Last Modified: Tue, 27 May 2025 19:37:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa323df40ee8608cc7b3f80b9aa63d0761f0c38580bcc2b38cefbf33e5f0d9c`  
		Last Modified: Tue, 27 May 2025 19:37:55 GMT  
		Size: 143.5 MB (143532216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada50f64b882ed3e72fa21f33cc40faf128e19d2e208d6abc3de0947a97ea28c`  
		Last Modified: Tue, 27 May 2025 20:02:53 GMT  
		Size: 310.3 MB (310289943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4ef66e779971815cab2b910c3e4d22d58f0c9e442d170c65a8df2c20233c18`  
		Last Modified: Tue, 27 May 2025 20:02:50 GMT  
		Size: 137.4 MB (137395579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f5b0010a6745ed624cc84dc39a1a05fdc98de7475259f5139a106813eca6b6`  
		Last Modified: Tue, 27 May 2025 20:02:46 GMT  
		Size: 59.5 KB (59533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk24-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:a4d357e060b8f6dd334cedd1cc6bbcf2fb1350b3bdc32e0d27f0db640e922f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8822294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9042f702e4d7d2684f96780963ea473ce91b464ebac858fd88d926d76eebcce1`

```dockerfile
```

-	Layers:
	-	`sha256:934719bd38149c7a4d07c46b5ce669f9cfa32d891381a6163be0b762b3b9d35e`  
		Last Modified: Tue, 27 May 2025 20:02:46 GMT  
		Size: 8.8 MB (8794906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4ffb0d8f8abdbcce50219452aa15619b3695f6c690bf12f53b09dbb2dcaec31`  
		Last Modified: Tue, 27 May 2025 20:02:46 GMT  
		Size: 27.4 KB (27388 bytes)  
		MIME: application/vnd.in-toto+json
