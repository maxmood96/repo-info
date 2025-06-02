## `gradle:7-jdk-graal-noble`

```console
$ docker pull gradle@sha256:94aaa9348e898c0256e52a465b04053b7c5f17d4a02d501e09b0e8cbf10d3d78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:5a46fc2ff365f73fe5111f97beae3f03178785e51309a4f72b250894ffbf33e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.1 MB (592122965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c132a28e4c8b720fad8df9c169ac4696e7a8d72a54961ecde1ccc8979b48d6`
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
# Thu, 29 May 2025 19:53:06 GMT
CMD ["gradle"]
# Thu, 29 May 2025 19:53:06 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 29 May 2025 19:53:06 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 29 May 2025 19:53:06 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 29 May 2025 19:53:06 GMT
WORKDIR /home/gradle
# Thu, 29 May 2025 19:53:06 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 29 May 2025 19:53:06 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 29 May 2025 19:53:06 GMT
ENV JAVA_VERSION=17.0.9
# Thu, 29 May 2025 19:53:06 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Thu, 29 May 2025 19:53:06 GMT
ENV GRADLE_VERSION=7.6.4
# Thu, 29 May 2025 19:53:06 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Thu, 29 May 2025 19:53:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 29 May 2025 19:53:06 GMT
USER gradle
# Thu, 29 May 2025 19:53:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 29 May 2025 19:53:06 GMT
USER root
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a7c781e56d9853849dbf19979edd30cd4256e2aa1917a9edc19ec76222c816`  
		Last Modified: Mon, 02 Jun 2025 16:52:34 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990b82df101216fe2b0e2dd275ba8ea45762ab616535188a871c7003b7506e39`  
		Last Modified: Mon, 02 Jun 2025 16:52:38 GMT  
		Size: 148.6 MB (148554652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aad2e26795fee9d8aee9d679c0f948c483e1638caf22384a7b600213b89948c`  
		Last Modified: Mon, 02 Jun 2025 16:52:41 GMT  
		Size: 291.1 MB (291064044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b0e35e1907086c125eb458642111b4551152b1d2abef26862aacbaab2b8f39`  
		Last Modified: Mon, 02 Jun 2025 16:52:38 GMT  
		Size: 122.7 MB (122730528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f50955e689af88f08e6a201b21b5a8273ba053caa85df79db904ed43cef295`  
		Last Modified: Mon, 02 Jun 2025 16:52:35 GMT  
		Size: 54.9 KB (54891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:d3390e57a0e8941760bc8c76b6a286402b5cea955d2060139a9da5b80c9ac83b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8726392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a1a6d9c94db7dc69aeb2fd1ccd9471f52e5d2a08229a4b2cd649369626a244`

```dockerfile
```

-	Layers:
	-	`sha256:cb13eeea0280e6633ccf5a186aa4180be3cc34f0a7c15950e1beb5b83616601f`  
		Last Modified: Mon, 02 Jun 2025 16:52:34 GMT  
		Size: 8.7 MB (8694264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45477859dc62211535d2e0aae76fbb9b807531bde16bc59441e824e7b061e639`  
		Last Modified: Mon, 02 Jun 2025 16:52:34 GMT  
		Size: 32.1 KB (32128 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:563d0c5358a7cfae4392df8ac6069f0e662c829edcc7ff9a66de2fdf1ca3c632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.8 MB (578817227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9b5eb3a5f0a8382da4456bddbc484e59a8287f15f005c4a2a2dab03d433126`
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
# Thu, 29 May 2025 19:53:06 GMT
CMD ["gradle"]
# Thu, 29 May 2025 19:53:06 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 29 May 2025 19:53:06 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 29 May 2025 19:53:06 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 29 May 2025 19:53:06 GMT
WORKDIR /home/gradle
# Thu, 29 May 2025 19:53:06 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 29 May 2025 19:53:06 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 29 May 2025 19:53:06 GMT
ENV JAVA_VERSION=17.0.9
# Thu, 29 May 2025 19:53:06 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Thu, 29 May 2025 19:53:06 GMT
ENV GRADLE_VERSION=7.6.4
# Thu, 29 May 2025 19:53:06 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Thu, 29 May 2025 19:53:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 29 May 2025 19:53:06 GMT
USER gradle
# Thu, 29 May 2025 19:53:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 29 May 2025 19:53:06 GMT
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
	-	`sha256:596d7ad51bd42779fa222dd96d5850467ff9bbd33a3ee3f8c997a21b92e4f416`  
		Last Modified: Mon, 02 Jun 2025 17:04:12 GMT  
		Size: 283.5 MB (283501906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db426fccbec14f346ba34a42c3dcdc888b80f2fb3257ffafb149f59e291045b`  
		Last Modified: Mon, 02 Jun 2025 17:31:25 GMT  
		Size: 122.7 MB (122730530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd10de5bfe36fa6ec5d6c2c8eb139318467dfd834eca7198f6338e8171fbd12`  
		Last Modified: Mon, 02 Jun 2025 17:31:21 GMT  
		Size: 59.5 KB (59529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:ad2b463d9021b2b5c7949b8796462d9cafa1a9d418d4cf91db4f070fe7850818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8722420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d47f25b5cbc0bae33b259fcbc78a6c5bb8f6d003ab6e1888294460164407812`

```dockerfile
```

-	Layers:
	-	`sha256:58b840e3d3a3dfafa0a00ca2ce5b0e5f35028af57e3171720004f7ba6962ded5`  
		Last Modified: Mon, 02 Jun 2025 17:31:21 GMT  
		Size: 8.7 MB (8689960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cad7b0b2dc18d32ebf8fb9340013e01c76be8c0eff0b26db2e1925fd0830153`  
		Last Modified: Mon, 02 Jun 2025 17:31:21 GMT  
		Size: 32.5 KB (32460 bytes)  
		MIME: application/vnd.in-toto+json
