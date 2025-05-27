## `gradle:8-graal-noble`

```console
$ docker pull gradle@sha256:a433be6dd08323421feb51271c41bd565b01210f5ada971d5cef4b76a73299c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:4b39bd612250639732ff8f7ed5b2c0c396c8764d0e8d20de76f85bb1d880ff1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.6 MB (605584504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e31c37608384dff299dd5b10dc0070edc86a65b95f8997c9eedba8ca5f6c11`
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
ENV JAVA_VERSION=21.0.2
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
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
	-	`sha256:933813cb09c84758ac929c7ccd9a1a0e8a9bffe5b24d3081a2a8f7c30a79f6f5`  
		Last Modified: Tue, 27 May 2025 18:59:34 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81155050c3f6bda1fb87ac1acf0ac4028b11ddc4bad9e654bb90e27a3d1cb980`  
		Last Modified: Tue, 27 May 2025 18:59:36 GMT  
		Size: 148.4 MB (148428482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772dcbe946db8b4c1af604f17a3132bc7511c2dfd09109a7ee4f5e42b35cd35f`  
		Last Modified: Tue, 27 May 2025 18:59:39 GMT  
		Size: 290.0 MB (289986701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cff40112f571a5366cc2a31622eceadeccbe7ca88842d791cca09b98fef4b71`  
		Last Modified: Tue, 27 May 2025 18:59:36 GMT  
		Size: 137.4 MB (137395578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42df8c5fa454f538c779e9858287979dad3fa74166cfe5b8c22b0a3917e5d63d`  
		Last Modified: Tue, 27 May 2025 18:59:35 GMT  
		Size: 54.9 KB (54895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:f18d99f0cc01486f4a9af193aa71ff1c34b6fb87560626d9eeb043ae3b02dcce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8795896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64bb38bf7fdca18cace6bc9cea37659bd367d8d8c125d7ba7b09cfbfc0adfce`

```dockerfile
```

-	Layers:
	-	`sha256:51506bf543e38df666788e3c663ef18664090dd0e6359a40a5ce6bc845610546`  
		Last Modified: Tue, 27 May 2025 18:59:34 GMT  
		Size: 8.8 MB (8763712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:356e137972acee739c3705b4ba8cdc0f2adc2b7059d6f6475cda9720f2a03a32`  
		Last Modified: Tue, 27 May 2025 18:59:34 GMT  
		Size: 32.2 KB (32184 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:275138a86b9f0933e5215e2457e749c93c94c65e85960b049942db0c05828673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.5 MB (591501872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df3f243c6f61625980f077886099cab9b3c70d39648efbff7c4875a38b2d627`
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
ENV JAVA_VERSION=21.0.2
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
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
	-	`sha256:2154a7578218acb8f6a4b44fea23df49af36b5abb3518ee220dc9ef8070466d0`  
		Last Modified: Tue, 27 May 2025 19:37:58 GMT  
		Size: 281.7 MB (281666353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47f6e6752f5bef84b84b438953a31264dcf8c4887db98ec7f0d6b9777a17132`  
		Last Modified: Tue, 27 May 2025 19:37:55 GMT  
		Size: 137.4 MB (137395578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87476ac078d627ad447a857d500dc7c61cc1520058482bf42a6383fc1caca2a7`  
		Last Modified: Tue, 27 May 2025 19:37:52 GMT  
		Size: 59.5 KB (59528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:8bace57f903c13a0d1ac29a54e946fcc213989a973fb56ffc8b9981f12bd2c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8792072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d037d3318cca8bb96531c172bd5b963017854d7047c4bb75934d219272efe26`

```dockerfile
```

-	Layers:
	-	`sha256:70eb0d789262de73c87e18402d1527f9fd0c0eb91bb6ce4877cd6c5737204fb6`  
		Last Modified: Tue, 27 May 2025 19:37:52 GMT  
		Size: 8.8 MB (8759484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04994924d7ef6bf28ce857cf0d54968eecac7b82bd161a57b325df2fe5ee690e`  
		Last Modified: Tue, 27 May 2025 19:37:51 GMT  
		Size: 32.6 KB (32588 bytes)  
		MIME: application/vnd.in-toto+json
