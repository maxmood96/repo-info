## `gradle:8-jdk21-graal-noble`

```console
$ docker pull gradle@sha256:cdaa504dd0353e605c3d2f5afcbfc0b598a169846c47aa63ac113d5556140c5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk21-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:e386d5739d9f5dc40fd018859de05f82858dab78ed8173ca3dbead97208ff881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.7 MB (605710730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c76f914da370fd2e40558170c060884dd68a2c3a4e43e2a0ca140c51db7e3c0`
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
# Thu, 29 May 2025 19:22:22 GMT
CMD ["gradle"]
# Thu, 29 May 2025 19:22:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 29 May 2025 19:22:22 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 29 May 2025 19:22:22 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 29 May 2025 19:22:22 GMT
WORKDIR /home/gradle
# Thu, 29 May 2025 19:22:22 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 29 May 2025 19:22:22 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 29 May 2025 19:22:22 GMT
ENV JAVA_VERSION=21.0.2
# Thu, 29 May 2025 19:22:22 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Thu, 29 May 2025 19:22:22 GMT
ENV GRADLE_VERSION=8.14.1
# Thu, 29 May 2025 19:22:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
# Thu, 29 May 2025 19:22:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 29 May 2025 19:22:22 GMT
USER gradle
# Thu, 29 May 2025 19:22:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 29 May 2025 19:22:22 GMT
USER root
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d732f9e9a876f699f7f7ef69a64f5d90272388d56fc2baa031d1c81ce5be79f`  
		Last Modified: Mon, 02 Jun 2025 16:48:54 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb485b52cf5f1a41e6ce53e1fd6a2488cfd2580676d15e87f5b636a269273bfb`  
		Last Modified: Mon, 02 Jun 2025 16:48:58 GMT  
		Size: 148.6 MB (148554603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4f4870a36aa027f32ec7a988ca661b84c8f22a82bad48903546167e50e19b6`  
		Last Modified: Mon, 02 Jun 2025 16:49:01 GMT  
		Size: 290.0 MB (289986801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772ecf9f9a975c10d6f8f1f6f7cb4880f8a073bb8b974d3c4c834e7a41001dd4`  
		Last Modified: Mon, 02 Jun 2025 16:48:59 GMT  
		Size: 137.4 MB (137395581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeae928fc6d285f9dd5e5ef71d4b212795e9bcc7ef1d8a057ccc2a9ef5ca08a8`  
		Last Modified: Mon, 02 Jun 2025 16:48:56 GMT  
		Size: 54.9 KB (54898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:3ea1a0496dcda5548d49a27897dad039b1be36b8e2e11197606ccb361a4f1e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8802994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18895488f0950c3e4561a70a8d1585569c87bdf812e4aaeb98ce9b807cf888c1`

```dockerfile
```

-	Layers:
	-	`sha256:38cebe29721cb28a5a9f7dfd1610a2ec078e71bea0fe0107c7bc4ff5a8972313`  
		Last Modified: Mon, 02 Jun 2025 16:48:55 GMT  
		Size: 8.8 MB (8769088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4421d0a7226f4cd6d677c2c8b8ac46714d188b42b3a197e1fbffe2912e56fb25`  
		Last Modified: Mon, 02 Jun 2025 16:48:55 GMT  
		Size: 33.9 KB (33906 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:915553d0fb4d7a7ceb758b888bcbc1777627221638ef251e4f12a7dc0849d764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.6 MB (591646675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0463c9d6d8aaa7a401cb7bd64782bfb7560063eafe39dc2ef1d8941fd9315e63`
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
# Thu, 29 May 2025 19:22:22 GMT
CMD ["gradle"]
# Thu, 29 May 2025 19:22:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 29 May 2025 19:22:22 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 29 May 2025 19:22:22 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 29 May 2025 19:22:22 GMT
WORKDIR /home/gradle
# Thu, 29 May 2025 19:22:22 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 29 May 2025 19:22:22 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 29 May 2025 19:22:22 GMT
ENV JAVA_VERSION=21.0.2
# Thu, 29 May 2025 19:22:22 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Thu, 29 May 2025 19:22:22 GMT
ENV GRADLE_VERSION=8.14.1
# Thu, 29 May 2025 19:22:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
# Thu, 29 May 2025 19:22:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 29 May 2025 19:22:22 GMT
USER gradle
# Thu, 29 May 2025 19:22:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 29 May 2025 19:22:22 GMT
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
	-	`sha256:8bf44bca955c9a70bb3f3c4467abf917d88ea660263723cc9357b39473514273`  
		Last Modified: Mon, 02 Jun 2025 16:55:20 GMT  
		Size: 143.7 MB (143677065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d070beaa8b991be7e017cee77f1c574ae28f374c351548d9bfa4df46dfad05f0`  
		Last Modified: Mon, 02 Jun 2025 16:55:23 GMT  
		Size: 281.7 MB (281666302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff2653b35f475f8a2c9bc7714b705a5877a2ca075df72f3ab3220cd47ffe572`  
		Last Modified: Mon, 02 Jun 2025 16:55:21 GMT  
		Size: 137.4 MB (137395577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a01c8bc8de2cd8f635b44f2276f5d88a985969cc2afcdff8ab6f3c36ec7f7e2`  
		Last Modified: Mon, 02 Jun 2025 16:55:17 GMT  
		Size: 59.5 KB (59534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:fb26d892a64bb01821afd215ff9586b6c27c4e073b46086a6839089cbd1a7a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8799170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:740eab46250b5f54f96a5dc2cb1db9f33709e1e73822a1ae8a9a5edd571bff1b`

```dockerfile
```

-	Layers:
	-	`sha256:70b5c9bb3da96d09f7349777e6f7e705c3ff27d77e42d5b40e14056c9811b21b`  
		Last Modified: Mon, 02 Jun 2025 16:55:17 GMT  
		Size: 8.8 MB (8764860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10139258f699576dc577bea70b583ba724ef6affe93bc769ef87a3c7f38a82cc`  
		Last Modified: Mon, 02 Jun 2025 16:55:16 GMT  
		Size: 34.3 KB (34310 bytes)  
		MIME: application/vnd.in-toto+json
