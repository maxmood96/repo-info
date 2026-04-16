## `gradle:jdk21-graal`

```console
$ docker pull gradle@sha256:2fed0802118322d69319b9565b48d0c7695048427436abe13dc93367d62543ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk21-graal` - linux; amd64

```console
$ docker pull gradle@sha256:6da1ebb6311b27aab54c9d284fa0bfda2b95a6beaa912f86ff9b8454c0161a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.9 MB (605865327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f929aef1adf9fa971676fdcd41737ffd4dcece3c2b5c26be4e2fc49ac85cd0`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:35:44 GMT
CMD ["gradle"]
# Wed, 15 Apr 2026 20:35:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 15 Apr 2026 20:35:44 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 15 Apr 2026 20:35:44 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 15 Apr 2026 20:35:44 GMT
WORKDIR /home/gradle
# Wed, 15 Apr 2026 20:36:16 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 15 Apr 2026 20:36:16 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 15 Apr 2026 20:36:16 GMT
ENV JAVA_VERSION=21.0.2
# Wed, 15 Apr 2026 20:36:24 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Wed, 15 Apr 2026 20:36:24 GMT
ENV GRADLE_VERSION=9.4.1
# Wed, 15 Apr 2026 20:36:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Wed, 15 Apr 2026 20:36:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 15 Apr 2026 20:36:27 GMT
USER gradle
# Wed, 15 Apr 2026 20:36:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 15 Apr 2026 20:36:27 GMT
USER root
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8db009d21d9ab73d8eb1b1f149c5b842302036b7d1eda2fd433d9dcd69db6d`  
		Last Modified: Wed, 15 Apr 2026 20:36:57 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83231abf57ae59b4b6381704b7f7c6f1005c57e964a6b43b52f5ac0ed1c5c67e`  
		Last Modified: Wed, 15 Apr 2026 20:37:10 GMT  
		Size: 148.3 MB (148311136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f52576659ac7069d8fb26533d83c75c76ccc241a7d388195ea490381cc4131`  
		Last Modified: Wed, 15 Apr 2026 20:37:13 GMT  
		Size: 290.0 MB (289985956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fc3c642861f81eaf82835846bea3ca336eae74014ad4744cdf9b004aeffe17`  
		Last Modified: Wed, 15 Apr 2026 20:37:09 GMT  
		Size: 137.8 MB (137808328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e936e0b61862032ee77264bc34805398789bb9f54475274b817b9ea28cbf1334`  
		Last Modified: Wed, 15 Apr 2026 20:36:59 GMT  
		Size: 25.6 KB (25611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:e9f72a3442808905e02de684f5a6ec57289b87700f4a9364698c009781df172b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9001398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65fcc3250e371144cdbfcaf386aece7e2d6db65e3f36f8246cdd56c86a43679`

```dockerfile
```

-	Layers:
	-	`sha256:de254a1f394e9534c6b279da3ceb82b1da486c38745e3ee71bb534cadbc42f82`  
		Last Modified: Wed, 15 Apr 2026 20:36:58 GMT  
		Size: 9.0 MB (8972450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d51a363c2eaf6dfd9766ea9877516ce7da396d0791479d4f632cf69bfc89fa18`  
		Last Modified: Wed, 15 Apr 2026 20:36:57 GMT  
		Size: 28.9 KB (28948 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:997ae9799f2e5363735200803e77e4a16493f1569af30a31284f3164132c67f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.8 MB (591792684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d361f0b37f688eef5a5d83e1c01492cd0da177fba9f1d9c7f40edf28e52f687`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:35:56 GMT
CMD ["gradle"]
# Wed, 15 Apr 2026 20:35:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 15 Apr 2026 20:35:56 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 15 Apr 2026 20:35:56 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 15 Apr 2026 20:35:56 GMT
WORKDIR /home/gradle
# Wed, 15 Apr 2026 20:36:33 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 15 Apr 2026 20:36:33 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 15 Apr 2026 20:36:33 GMT
ENV JAVA_VERSION=21.0.2
# Wed, 15 Apr 2026 20:36:46 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Wed, 15 Apr 2026 20:36:46 GMT
ENV GRADLE_VERSION=9.4.1
# Wed, 15 Apr 2026 20:36:46 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Wed, 15 Apr 2026 20:36:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 15 Apr 2026 20:36:48 GMT
USER gradle
# Wed, 15 Apr 2026 20:36:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 15 Apr 2026 20:36:48 GMT
USER root
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cdd0fea457eae77c1ccf4efd71eca27e896e83138229467eb8fd8a59a285e9`  
		Last Modified: Wed, 15 Apr 2026 20:37:20 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4730f362442f57e44b93a20c85c7bb2ef61713bd8675c1558bc92c0adf87d5`  
		Last Modified: Wed, 15 Apr 2026 20:37:28 GMT  
		Size: 143.4 MB (143411343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462bef4fb0a55fc7c6f7dab8805b5d4f27c29d2c9b75ae834cbad71efc8dfee2`  
		Last Modified: Wed, 15 Apr 2026 20:37:31 GMT  
		Size: 281.7 MB (281666576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764c34240e6c55688cab73a67d90e4aecefc8ffeaa3184dfa4c7f4452c716124`  
		Last Modified: Wed, 15 Apr 2026 20:37:28 GMT  
		Size: 137.8 MB (137808331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c681fc421790cccf0ff5d4d4ae611c0fa79fd68360893b176106adb881de3a6c`  
		Last Modified: Wed, 15 Apr 2026 20:37:22 GMT  
		Size: 29.3 KB (29330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:b5386fb564dbc31c5a314e7aa89d07ea372b363ffda682c2ca81dbb6a82823b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8997191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf29e0ce1e2a3fa84c9cee5686365b506c24af9a3a19d0f1bce00957a47e5e4`

```dockerfile
```

-	Layers:
	-	`sha256:cace913204927c757b6edc6d41b89bc04d62954f83a5dff563798cfac5eb77ad`  
		Last Modified: Wed, 15 Apr 2026 20:37:21 GMT  
		Size: 9.0 MB (8968031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:938ceb5b224d027c99ca426580d997b992ffae99cff82ca1de2b3e35e409a675`  
		Last Modified: Wed, 15 Apr 2026 20:37:20 GMT  
		Size: 29.2 KB (29160 bytes)  
		MIME: application/vnd.in-toto+json
