## `gradle:jdk24-graal-noble`

```console
$ docker pull gradle@sha256:388115b95dfb4f41df5eeb2ff5a3ce6d6f07b0cfa44042360211575447f764ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk24-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:e11b559cd10b82aaf9cab7fc319a94ef761e93795bf84361bee4ff29744cb277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **649.1 MB (649093360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea2a59ff688913dd17e36e577feebf808ffe97ffecd7aa0263c5bdd28d50a50`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["gradle"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 31 Jul 2025 17:27:11 GMT
WORKDIR /home/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_VERSION=24.0.2
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=6d62846c826ddb9307deec71e7661c26fa5a5e3985d7bb9005ea42163a390720     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c54d951a858791483d58270ecbc0946f28c4742c7fac74a4ebb2764bbf66d6f5     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_VERSION=9.0.0
# Thu, 31 Jul 2025 17:27:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
USER gradle
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
USER root
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929cc2271f0803a1dd3eb519aeabb37bed35203573b52ee5618431b824728834`  
		Last Modified: Tue, 12 Aug 2025 17:25:43 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1224508f8d295c73d43bf983a7c6017c83122df9f8e83ee0ad5c5baf61e2340d`  
		Last Modified: Wed, 13 Aug 2025 01:17:06 GMT  
		Size: 148.6 MB (148610969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6c40a9f61762c40ed61f7afc060848dc09070f7a798665e4f41e836e8e1131`  
		Last Modified: Wed, 13 Aug 2025 01:17:47 GMT  
		Size: 336.2 MB (336222118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53a2dfff2e3b9d0c79a75b7734e5ed68827d9d47656e0f0360dcb4b694b00cd`  
		Last Modified: Wed, 13 Aug 2025 01:16:54 GMT  
		Size: 134.5 MB (134480833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e767a931721de8f537b19adebaedc07d5ef2c479db465a64b99919d121c68b7`  
		Last Modified: Tue, 12 Aug 2025 17:25:45 GMT  
		Size: 54.9 KB (54904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk24-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:1bc618d3d0b7c7e7a753dde6c773624218fb321c75cd5292daa5f44c8566bcce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9038502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b2aa991529ba496fa0184a617be7b8a21591f2019964f6641e2445e12ed2e6`

```dockerfile
```

-	Layers:
	-	`sha256:6c7d7436cb1283e6be3b7a44c9536bc84af25915ed174f2c6cea56beb01ec7d1`  
		Last Modified: Tue, 12 Aug 2025 20:30:06 GMT  
		Size: 9.0 MB (9009614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d38b36dd684426693db3230f9eefd91c3394ff52fe9d95d741e703f6fc223c4f`  
		Last Modified: Tue, 12 Aug 2025 20:30:07 GMT  
		Size: 28.9 KB (28888 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk24-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:8427f6a73abe227d73f5a7910dc0774b7258ebb7edeae9f25b2f3682ee7ad6f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.5 MB (617530243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b66b9e24b3305f0a0b89d8d4ce2ba8dd3d60fb6e8c30c6f93e52ea961e5d58`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["gradle"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 31 Jul 2025 17:27:11 GMT
WORKDIR /home/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_VERSION=24.0.2
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=6d62846c826ddb9307deec71e7661c26fa5a5e3985d7bb9005ea42163a390720     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c54d951a858791483d58270ecbc0946f28c4742c7fac74a4ebb2764bbf66d6f5     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_VERSION=9.0.0
# Thu, 31 Jul 2025 17:27:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
USER gradle
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
USER root
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba9bb4b6886cee8a3a9cb7af80c4cdc8365ba4e9bf63cbd53630794b923fb60`  
		Last Modified: Tue, 12 Aug 2025 18:53:40 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326e0081c09fd09ce84793887e9289be42917cc643dd0872aeeb19c1e0575c74`  
		Last Modified: Wed, 13 Aug 2025 02:26:33 GMT  
		Size: 143.7 MB (143702632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b1fa78594344c19c7f49a0e49ab83d6e3c06b5fe2660f4163d89852708f786`  
		Last Modified: Wed, 13 Aug 2025 02:46:37 GMT  
		Size: 310.4 MB (310425567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80db194a2aaa14aadf6095bca374b5eb9e40d84144dd9b7f5430c5cafa5bce5a`  
		Last Modified: Wed, 13 Aug 2025 02:57:32 GMT  
		Size: 134.5 MB (134480832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bab7964d9f47287f6a883d61f044563da29788a5ace84bbcfc487347c1e6f5`  
		Last Modified: Tue, 12 Aug 2025 18:58:54 GMT  
		Size: 59.5 KB (59517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk24-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:a4a58e223fc67e5e9a79a7c37223e85222035a94a11e1dc9d3823918843934c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9033650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2109de5560f8503c8abc21afbb5e119cf97686c51f9c28dbfab6cd53830ff795`

```dockerfile
```

-	Layers:
	-	`sha256:30c71076f51bb3274680f7bcc92e7572c95a3e79a8f50de7cfae639fecc266af`  
		Last Modified: Tue, 12 Aug 2025 20:30:16 GMT  
		Size: 9.0 MB (9004550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af3f004464bca45eaba0d5b56f4e2311a275d2d64dee8f666163d0d648a9177f`  
		Last Modified: Tue, 12 Aug 2025 20:30:17 GMT  
		Size: 29.1 KB (29100 bytes)  
		MIME: application/vnd.in-toto+json
