## `gradle:8-jdk24-graal-noble`

```console
$ docker pull gradle@sha256:93711a1cc97e715c3cea987fc1b1ed1b16e98b04ec0848c00743530d07aebc66
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk24-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:9469ceebc7d643f570c192f7ff2ef89a46b3e26a845ab12c893202e19fbd4533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **652.0 MB (652046812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267fcf181f8c52954f32bef03830f04808201271e7a07e78faa59f6018b78523`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:23:04 GMT
CMD ["gradle"]
# Thu, 15 Jan 2026 22:23:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 15 Jan 2026 22:23:04 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 15 Jan 2026 22:23:04 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 15 Jan 2026 22:23:04 GMT
WORKDIR /home/gradle
# Thu, 15 Jan 2026 22:23:42 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 15 Jan 2026 22:23:42 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 15 Jan 2026 22:23:42 GMT
ENV JAVA_VERSION=24.0.2
# Thu, 15 Jan 2026 22:23:58 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=6d62846c826ddb9307deec71e7661c26fa5a5e3985d7bb9005ea42163a390720     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c54d951a858791483d58270ecbc0946f28c4742c7fac74a4ebb2764bbf66d6f5     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Thu, 15 Jan 2026 22:23:58 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 15 Jan 2026 22:23:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 15 Jan 2026 22:24:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 15 Jan 2026 22:24:00 GMT
USER gradle
# Thu, 15 Jan 2026 22:24:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 15 Jan 2026 22:24:00 GMT
USER root
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dacd973ccfdcd671db8fcce6d212635ec84e4344eba49dc3c5711b25d98d5e5`  
		Last Modified: Thu, 15 Jan 2026 22:24:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661412e4b5561092d552edca43aca982e2b024253307d770fe2f721d15f3266a`  
		Last Modified: Thu, 15 Jan 2026 22:24:42 GMT  
		Size: 148.6 MB (148647400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d1b88654f0db342f56c56f70ba772a84ff563bd86aa7a906f44283f413dd75`  
		Last Modified: Thu, 15 Jan 2026 22:26:14 GMT  
		Size: 336.2 MB (336222065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20063be6eec2ed77ed9f502a5f1e312b1d7827812ee3f57e498fefbbbc4c5b4`  
		Last Modified: Fri, 16 Jan 2026 01:41:10 GMT  
		Size: 137.4 MB (137395123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53aee4f6ecf7f4fc89dc70c65feae0889632601ed9f4b15481357545171a660`  
		Last Modified: Thu, 15 Jan 2026 22:24:51 GMT  
		Size: 54.9 KB (54894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk24-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:6621a23be31c575fc0a6f46b40dcec6f558e48b4c1890884ab4008b666cdbc06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9051676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6115e45fd5ad02e0073ab85ee964087c3e020ffdaf1468a8dcfebef990ddddb`

```dockerfile
```

-	Layers:
	-	`sha256:90d4f723bcaada9215e11e3c4b9cf21bdebe473221ecb67108f3ee5245384d3b`  
		Last Modified: Fri, 16 Jan 2026 00:28:07 GMT  
		Size: 9.0 MB (9023157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6272d83052a45703e41221b71d1ae340b88d83537321538360747ed4be9dcf48`  
		Last Modified: Thu, 15 Jan 2026 22:24:35 GMT  
		Size: 28.5 KB (28519 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk24-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c873fa9ed609073bdf2605b1410bbf936ef9a6af49799beb13cf99abd0b96918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.5 MB (620494235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b7b5b0faef1e0daae30e134eda6eb6c34a8fd9a20e651bb7033344d4595c8b`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:25:43 GMT
CMD ["gradle"]
# Thu, 15 Jan 2026 22:25:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 15 Jan 2026 22:25:43 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 15 Jan 2026 22:25:43 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 15 Jan 2026 22:25:43 GMT
WORKDIR /home/gradle
# Thu, 15 Jan 2026 22:26:16 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 15 Jan 2026 22:26:16 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 15 Jan 2026 22:26:16 GMT
ENV JAVA_VERSION=24.0.2
# Thu, 15 Jan 2026 22:26:33 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=6d62846c826ddb9307deec71e7661c26fa5a5e3985d7bb9005ea42163a390720     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c54d951a858791483d58270ecbc0946f28c4742c7fac74a4ebb2764bbf66d6f5     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Thu, 15 Jan 2026 22:26:33 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 15 Jan 2026 22:26:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 15 Jan 2026 22:26:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 15 Jan 2026 22:26:35 GMT
USER gradle
# Thu, 15 Jan 2026 22:26:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 15 Jan 2026 22:26:35 GMT
USER root
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b32edb6d8c67c11a8e819b6b43e8cfd9459207ac6725597e70e14f1add8dcd4`  
		Last Modified: Thu, 15 Jan 2026 22:27:10 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52b9bbac151e21da04edab5263cf89f1224ef94401bdb03e2b634d174331d79`  
		Last Modified: Thu, 15 Jan 2026 22:27:18 GMT  
		Size: 143.7 MB (143748803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75b88dd93bece1990863a9957b163445aea37ab14e1dda53e154116e102005c`  
		Last Modified: Thu, 15 Jan 2026 22:27:40 GMT  
		Size: 310.4 MB (310425567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350ae7735922a863cfaa5d141b16d0c76073ef3cac7732c6c23abb3ea164ea56`  
		Last Modified: Thu, 15 Jan 2026 22:27:45 GMT  
		Size: 137.4 MB (137395193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd67c244c8001c28fd59dc5434f2a59679e8c86dfc87bb61cfe7472168a00ea3`  
		Last Modified: Thu, 15 Jan 2026 22:27:27 GMT  
		Size: 59.5 KB (59531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk24-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:cf0b2c73f5b5044d29909246dd1ac0108fed0aca4347a1e38140b1bbc71d377e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9046800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1c3e290f1ae372986702e10c1961606d15029d41167a33ddbc2480db5a8126`

```dockerfile
```

-	Layers:
	-	`sha256:5a1d995e79eb0d2167017f2389781591fd0cccce453add00c58783ef6fea1506`  
		Last Modified: Fri, 16 Jan 2026 00:28:17 GMT  
		Size: 9.0 MB (9018081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb2c6a7be6c85f0fccb6fa323acd3d18a90f0d2ee3d155ea43c32c313e0090fb`  
		Last Modified: Fri, 16 Jan 2026 00:28:18 GMT  
		Size: 28.7 KB (28719 bytes)  
		MIME: application/vnd.in-toto+json
