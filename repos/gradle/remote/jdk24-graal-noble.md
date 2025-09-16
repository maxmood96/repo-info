## `gradle:jdk24-graal-noble`

```console
$ docker pull gradle@sha256:94e2b91275c86ea996b4d87f71921f6c5d3ae897672d2e4231dbc0f2d877f0b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk24-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:e1de7656467f3d3a4042484725a69a94df982c6bce2e16603e91619d150e0aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **649.1 MB (649095348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92faee2892b60e8b9ba1e16147b5759895176d0e16b52aec33b9f7eb2ef532a2`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Jul 2025 17:27:11 GMT
ARG RELEASE
# Thu, 31 Jul 2025 17:27:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 31 Jul 2025 17:27:11 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Thu, 31 Jul 2025 17:27:11 GMT
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
	-	`sha256:a1dcaf5baf51c1355e897be1079c767df08e1518a0bf2af6e0949cfd2b4ad4e0`  
		Last Modified: Tue, 16 Sep 2025 06:14:47 GMT  
		Size: 336.2 MB (336221973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea047925f773994f158cef006db0c91e6e261de42efcb8554f0c89010f2b818`  
		Last Modified: Mon, 15 Sep 2025 22:14:52 GMT  
		Size: 134.5 MB (134480835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6268e6d312a3808dd61161fe01f10e371eae130d98069583dfd44b8436139575`  
		Last Modified: Mon, 15 Sep 2025 22:14:57 GMT  
		Size: 54.9 KB (54896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk24-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:2e193072eb7d1a6e291a949395991f307bcc65f1eae4d5cc198c578ca2dca20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9038490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e07b6cc36c278d1f5e754d8087d23c9d830922553d24af8311db3538fad1d5`

```dockerfile
```

-	Layers:
	-	`sha256:3aaad86fa3ff29f2033f9be170850469ff5779d87f1be142a6afd1a9afe5abc2`  
		Last Modified: Mon, 15 Sep 2025 23:22:41 GMT  
		Size: 9.0 MB (9009618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66260293e881928c11d55dc5a7739ca5c0c236ea768974d2b09c218fb3b4aff1`  
		Last Modified: Mon, 15 Sep 2025 23:22:42 GMT  
		Size: 28.9 KB (28872 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk24-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d71e16306b2c4071f4f57227992b2f442cdeaf4019cedce7114981b1fd390219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.6 MB (617550730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ffbf718fea547bb2dc0e1d96b74e41a0b1b8bda014e0ae17c11b000699f929`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Jul 2025 17:27:11 GMT
ARG RELEASE
# Thu, 31 Jul 2025 17:27:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 31 Jul 2025 17:27:11 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Thu, 31 Jul 2025 17:27:11 GMT
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
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadb2aab2b246258b1b72984f2e378a7b28f8dbe04b1c4a5c05f13e04d9528fc`  
		Last Modified: Mon, 15 Sep 2025 22:15:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee0339d2c593374b4566157a9bee4f66742646b0fe0a9754801bc5dea890627`  
		Last Modified: Tue, 16 Sep 2025 06:20:34 GMT  
		Size: 143.7 MB (143722031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244e016b6c2113f86d46c43e71093bd24c7c0ecde97410e42444f796422ce8c6`  
		Last Modified: Tue, 16 Sep 2025 06:20:26 GMT  
		Size: 310.4 MB (310425705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5cbe21a29b1b1b89c3476d91d59d0a65770ebc0bda2eff330335bf8898a80d`  
		Last Modified: Mon, 15 Sep 2025 22:15:35 GMT  
		Size: 134.5 MB (134480835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6663a045084eecdfd606051c84705a2fce83146d2c07be51d56b84519d453f`  
		Last Modified: Mon, 15 Sep 2025 22:15:45 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk24-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:a7657aa806131d28cbab2dcce7e78238d0083d137b58d47be2604fc190f96556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9033638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d4ba18779c97988e2bfe3d44c628cf115db62e4eab26e20a3ce7572bfbd69e`

```dockerfile
```

-	Layers:
	-	`sha256:1363548cc1f34c69bf813dfe084d9b5075feeebf73aeba5d303060f1b5ee1e4e`  
		Last Modified: Mon, 15 Sep 2025 23:22:48 GMT  
		Size: 9.0 MB (9004554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c33a8372de2ef16229d742564867b10444277a0d562fd68cd4ac89ed96e1f39`  
		Last Modified: Mon, 15 Sep 2025 23:22:49 GMT  
		Size: 29.1 KB (29084 bytes)  
		MIME: application/vnd.in-toto+json
