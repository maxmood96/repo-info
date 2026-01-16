## `gradle:9-jdk-graal`

```console
$ docker pull gradle@sha256:4ee772591fc5848a1e935564151edf7d53fd8673544251b0c2d2d6540bbb7c90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk-graal` - linux; amd64

```console
$ docker pull gradle@sha256:c18a461e20fac4603af693144d01e8aa060417015730cbe501ae6f7b005353e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.8 MB (654802324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c2c188135437f2eb008087803ec2b36e4f4e2a1c0bf0f473de32540949b759`
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
# Thu, 15 Jan 2026 22:20:36 GMT
CMD ["gradle"]
# Thu, 15 Jan 2026 22:20:36 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 15 Jan 2026 22:20:36 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 15 Jan 2026 22:20:36 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 15 Jan 2026 22:20:36 GMT
WORKDIR /home/gradle
# Thu, 15 Jan 2026 22:21:10 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 15 Jan 2026 22:21:10 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 15 Jan 2026 22:21:10 GMT
ENV JAVA_VERSION=25.0.1
# Thu, 15 Jan 2026 22:21:23 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=01e39fe1a87f28b842a3e4e3b77be9b544dca3a58fa6e93b924a6106c8bac7fb     && GRAALVM_AARCH64_DOWNLOAD_SHA256=7aa0b9935a80e67f37c6025678393dbd123bb6f2226811decbc1a13093fc8ae2     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Thu, 15 Jan 2026 22:21:23 GMT
ENV GRADLE_VERSION=9.2.1
# Thu, 15 Jan 2026 22:21:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Thu, 15 Jan 2026 22:21:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 15 Jan 2026 22:21:25 GMT
USER gradle
# Thu, 15 Jan 2026 22:21:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Thu, 15 Jan 2026 22:21:26 GMT
USER root
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de140388c8432451f8f606bb87e99f0e378e26ed69cbd3e056c9a371db2c6f0c`  
		Last Modified: Thu, 15 Jan 2026 22:22:18 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7011d885c1f0968c15fdfd730c0957b780adbd36f2372501f357e335ee1c18`  
		Last Modified: Fri, 16 Jan 2026 00:41:46 GMT  
		Size: 148.6 MB (148647263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f42dd6be79aba53103f936e8f8b1f27d104e538416dc3fa7eeda3b6aaa8081`  
		Last Modified: Thu, 15 Jan 2026 22:23:38 GMT  
		Size: 340.9 MB (340850853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9b1e25831bdf1c101f3c9bee51686885e33619386393780846f8b7e072bfcd`  
		Last Modified: Thu, 15 Jan 2026 23:36:07 GMT  
		Size: 135.5 MB (135521963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85310049c99ebae1bc8e66bdf2b766efaf8ae75be29772c15ba4b99b1cc352db`  
		Last Modified: Thu, 15 Jan 2026 22:22:18 GMT  
		Size: 54.9 KB (54905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:dbf1bbc45a15be1ee1ef91a62ae9e9793f3ad033256fa7036f3a2f4d9549a650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9063557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e2234b8a634c1c5dfcc8c324895699c1ee4d518ffb595fdfff7fb7db0ca049`

```dockerfile
```

-	Layers:
	-	`sha256:05bbae81e3bfec8186c2ef6c4b9bfab7d1d68d900d0c16245583efaf3a33b53f`  
		Last Modified: Fri, 16 Jan 2026 00:32:39 GMT  
		Size: 9.0 MB (9029617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4d910d4843d964cd1f398a3bd24dff4f3b3c177a3784356ec60c1a83ad5aef4`  
		Last Modified: Fri, 16 Jan 2026 00:32:40 GMT  
		Size: 33.9 KB (33940 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:4c1d959be630aabb751fcf4f38bb2c5e084fb4fdeaf10d6558c23567604d4398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.1 MB (624087576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a789a52772c4b7cb2611d828a4d50b2a206bdcafb45ad2b610963412ec8d6a`
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
# Thu, 15 Jan 2026 22:22:34 GMT
CMD ["gradle"]
# Thu, 15 Jan 2026 22:22:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 15 Jan 2026 22:22:34 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 15 Jan 2026 22:22:34 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 15 Jan 2026 22:22:34 GMT
WORKDIR /home/gradle
# Thu, 15 Jan 2026 22:23:07 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 15 Jan 2026 22:23:07 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 15 Jan 2026 22:23:07 GMT
ENV JAVA_VERSION=25.0.1
# Thu, 15 Jan 2026 22:23:19 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=01e39fe1a87f28b842a3e4e3b77be9b544dca3a58fa6e93b924a6106c8bac7fb     && GRAALVM_AARCH64_DOWNLOAD_SHA256=7aa0b9935a80e67f37c6025678393dbd123bb6f2226811decbc1a13093fc8ae2     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Thu, 15 Jan 2026 22:23:19 GMT
ENV GRADLE_VERSION=9.2.1
# Thu, 15 Jan 2026 22:23:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Thu, 15 Jan 2026 22:23:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 15 Jan 2026 22:23:21 GMT
USER gradle
# Thu, 15 Jan 2026 22:23:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Thu, 15 Jan 2026 22:23:22 GMT
USER root
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f2536b0e453ffe8976796ee26e690c93022939945f59c9fa694eb06328401c`  
		Last Modified: Thu, 15 Jan 2026 23:36:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a3085cdad0c37ac7368ac3f78ee5a0c2ee33e4677c9a8f11698c26d272e770`  
		Last Modified: Thu, 15 Jan 2026 22:26:59 GMT  
		Size: 143.8 MB (143751740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf778f97565f36b03d94525fa59412a15c2ae98b9340002fedd8b4525e399a0`  
		Last Modified: Thu, 15 Jan 2026 22:24:08 GMT  
		Size: 315.9 MB (315889204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11033bffc50941150dc83786c3e60431679b4ce2c7d2b45dc61449572e79b55b`  
		Last Modified: Fri, 16 Jan 2026 15:51:20 GMT  
		Size: 135.5 MB (135521965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee2dc39eba62138e5759a09897236d582f3d9c4fc783f23e6f95455eb0fcd62`  
		Last Modified: Thu, 15 Jan 2026 22:24:15 GMT  
		Size: 59.5 KB (59524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:4e161834b6b8a206eb4a7cd5a7ad91cffcc0b6bc41f6dd04268772d67a4f7184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9059101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf913087b2aadaea053722d021074c80a04ed60f60b551a1d485716f70d00721`

```dockerfile
```

-	Layers:
	-	`sha256:8c48357b5fb2405094b754b0e37b78155e7441d30e80f2b270458d4c986acc9d`  
		Last Modified: Fri, 16 Jan 2026 00:32:50 GMT  
		Size: 9.0 MB (9024757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29868e7dec932a744bc39e5c6bfa217adffdf2509a84924a766841c1bccb3f33`  
		Last Modified: Fri, 16 Jan 2026 00:32:51 GMT  
		Size: 34.3 KB (34344 bytes)  
		MIME: application/vnd.in-toto+json
