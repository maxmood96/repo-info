## `gradle:8-jdk-graal`

```console
$ docker pull gradle@sha256:98b6d1c251a3ac34b9a18edf8d8f06bef5862654e5220dc64ffbf02025efb6ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk-graal` - linux; amd64

```console
$ docker pull gradle@sha256:c8118602b253d34f98a5bb0209b6ae194a309b0b5ef11aa5aa3f163e37023a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.0 MB (605982766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1eb4524b0ebb1444b2e8e3637df6ee4b7efa81a10ac29ce8dcc9e7e5cc4f1b5`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:54:37 GMT
CMD ["gradle"]
# Tue, 07 Apr 2026 01:54:37 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 07 Apr 2026 01:54:37 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 07 Apr 2026 01:54:37 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 07 Apr 2026 01:54:37 GMT
WORKDIR /home/gradle
# Tue, 07 Apr 2026 01:55:07 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 07 Apr 2026 01:55:07 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 07 Apr 2026 01:55:07 GMT
ENV JAVA_VERSION=21.0.2
# Tue, 07 Apr 2026 01:55:17 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 07 Apr 2026 01:55:17 GMT
ENV GRADLE_VERSION=8.14.4
# Tue, 07 Apr 2026 01:55:17 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Tue, 07 Apr 2026 01:55:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 07 Apr 2026 01:55:19 GMT
USER gradle
# Tue, 07 Apr 2026 01:55:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 07 Apr 2026 01:55:19 GMT
USER root
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e2774ee32fbd485200b57b5f33aeee7df336bb108a1002d66275256ae734ad`  
		Last Modified: Tue, 07 Apr 2026 01:55:52 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a99febc3977490b007088da56c851a9074cf2367ae8570d95824c30b50acafd`  
		Last Modified: Tue, 07 Apr 2026 01:56:02 GMT  
		Size: 148.8 MB (148818925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631d7728882c2064664bca61ba124ad9d4b61a10c75f423591bf81e16c3397fa`  
		Last Modified: Tue, 07 Apr 2026 01:56:05 GMT  
		Size: 290.0 MB (289985872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88fb78e14cd5d1aeef8638999d1fbec6a75fd76349c5a92d333aebfc74df220c`  
		Last Modified: Tue, 07 Apr 2026 01:56:01 GMT  
		Size: 137.4 MB (137388295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1719269e0be8b6468a63e067f5337f466d410dd660392158d8e644271aa682`  
		Last Modified: Tue, 07 Apr 2026 01:55:54 GMT  
		Size: 54.9 KB (54898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:f46c119557615f06a4ca1c42b1ec0a2c90d8d55a1623236398c72e779c6edf14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9021840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82af5c4aae35206b133b9275fbe16505f47cae22e6332ec86f53d17041f78af4`

```dockerfile
```

-	Layers:
	-	`sha256:5d2610c1eb5f71a5de03af222bbcf221c70804d2bd732b17a598c86ddd34e8c0`  
		Last Modified: Tue, 07 Apr 2026 01:55:53 GMT  
		Size: 9.0 MB (8989845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fccdbe990d7fa4b3d739fa9035aec055ea6f8282af152bfe7a667c980089de7f`  
		Last Modified: Tue, 07 Apr 2026 01:55:52 GMT  
		Size: 32.0 KB (31995 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:2081740412078a315ae51e4799b1bcc2ad8634d991e5f357f7fa13b933ef3ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.9 MB (591908042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e100344316d6acf7fb603ff385d5ce72afcbe2f054b4ff4d8f19550dcc0cf0`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:56:19 GMT
CMD ["gradle"]
# Tue, 07 Apr 2026 01:56:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 07 Apr 2026 01:56:19 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 07 Apr 2026 01:56:19 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 07 Apr 2026 01:56:19 GMT
WORKDIR /home/gradle
# Tue, 07 Apr 2026 01:58:35 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 07 Apr 2026 01:58:35 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 07 Apr 2026 01:58:35 GMT
ENV JAVA_VERSION=21.0.2
# Tue, 07 Apr 2026 01:58:44 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 07 Apr 2026 01:58:44 GMT
ENV GRADLE_VERSION=8.14.4
# Tue, 07 Apr 2026 01:58:44 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Tue, 07 Apr 2026 01:58:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 07 Apr 2026 01:58:47 GMT
USER gradle
# Tue, 07 Apr 2026 01:58:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 07 Apr 2026 01:58:47 GMT
USER root
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d78eafd1309a6577ef0b5e0d9dcf18342237d25567f52e4d78c5704c4c9bec8`  
		Last Modified: Tue, 07 Apr 2026 01:57:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05240de30d0af265e473f1fa8ce3c1f1e4146fc8aea053bcc8cc500284a56e81`  
		Last Modified: Tue, 07 Apr 2026 01:59:28 GMT  
		Size: 143.9 MB (143918637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397f95db64bfe44b71b51e56f958158d8ca999a1e4e0d676b2cefbcab7550bc9`  
		Last Modified: Tue, 07 Apr 2026 01:59:31 GMT  
		Size: 281.7 MB (281666219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e07422052433bdaa2de110f866a36669682bddc9e6eddf6ae11a4f207ff09f`  
		Last Modified: Tue, 07 Apr 2026 01:59:28 GMT  
		Size: 137.4 MB (137388269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5b38c2004727bfbee166775379ea0f7702082bebcddd3bf649bb4c518f2036`  
		Last Modified: Tue, 07 Apr 2026 01:59:20 GMT  
		Size: 59.5 KB (59525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:d61896acfd4438277ec04e85a4dadbeb0c6992d75a4d4ec1e2ab90db47fe991b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9017873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e414c731819303a1de0628f80a7527225072502465ed45b59cabf911ea849d`

```dockerfile
```

-	Layers:
	-	`sha256:cc56fef554924fc335dc49683a413fc78abf0aa4b459c3b43800ff610e93299f`  
		Last Modified: Tue, 07 Apr 2026 01:59:20 GMT  
		Size: 9.0 MB (8985546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0afb4d2f338cd15a4d4133368c10c01e7b08d0854ae6e0f7b0bad31f3967086e`  
		Last Modified: Tue, 07 Apr 2026 01:59:20 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.in-toto+json
