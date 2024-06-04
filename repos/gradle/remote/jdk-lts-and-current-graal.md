## `gradle:jdk-lts-and-current-graal`

```console
$ docker pull gradle@sha256:8f19769d3496ee05571be2c7ed17c7144a0d1a991928c3cc65a6ef266a0231c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-lts-and-current-graal` - linux; amd64

```console
$ docker pull gradle@sha256:9837a5669bffc1f4c788b70373d57e79e8d97532a8f0bd509ce8ff32c06cb392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **911.1 MB (911052392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e9549a594670efe8c92a35bceb0d9cb61b89848669d19b4fdad65b77c2e07b`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 15:03:05 GMT
CMD ["gradle"]
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 01 Jun 2024 15:03:05 GMT
WORKDIR /home/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sat, 01 Jun 2024 15:03:05 GMT
ENV JAVA_LTS_HOME=/opt/java/graalvm21
# Sat, 01 Jun 2024 15:03:05 GMT
ENV JAVA_CURRENT_HOME=/opt/java/graalvm22
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading LTS GraalVM"     && JDK_VERSION=21.0.2     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JDK_VERSION}/graalvm-community-jdk-${JDK_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking LTS GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing LTS GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm21         && echo "Downloading current GraalVM"     && JDK_VERSION=22.0.0     && GRAALVM_AMD64_DOWNLOAD_SHA256=e5eeb486a23101753f18181d002c3ede9da13c463fb61d3ea448abe774db0657     && GRAALVM_AARCH64_DOWNLOAD_SHA256=da9a0e11b110ebccff33ade502516d00f574ec3247868007e452cef4143e0904     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JDK_VERSION}/graalvm-community-jdk-${JDK_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking current GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing current GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm22         && echo "Default Java to LTS GraalVM"     && ln --symbolic /opt/java/graalvm21 /opt/java/graalvm     && for bin in /opt/java/graalvm21/bin/*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_VERSION=8.8
# Sat, 01 Jun 2024 15:03:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
# Sat, 01 Jun 2024 15:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version         && chown --recursive gradle:gradle /home/gradle # buildkit
```

-	Layers:
	-	`sha256:a8b1c5f80c2d2a757adc963e3fe2dad0b4d229f83df3349fbb70e4d12dd48822`  
		Last Modified: Sat, 27 Apr 2024 14:45:30 GMT  
		Size: 29.5 MB (29533949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f47d0fdf63ec58bef6ed13cab87afb1d5843ec58f786ebebd5143635d479a04`  
		Last Modified: Mon, 03 Jun 2024 19:02:17 GMT  
		Size: 4.4 KB (4420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d08910716d11daddf108792f31ec124c6c92ed26e2e4de63990f10b02e2613f`  
		Last Modified: Mon, 03 Jun 2024 19:02:19 GMT  
		Size: 131.6 MB (131594511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e80e99dd285f6ba0e4fe7021937b8ea4ea3b6061f2b51a567ce53726136904`  
		Last Modified: Mon, 03 Jun 2024 19:02:27 GMT  
		Size: 611.8 MB (611800811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce1ea0dca01957e75991e716663f4e2496b1ecf70215aa4341535d1a0c26106`  
		Last Modified: Mon, 03 Jun 2024 19:02:19 GMT  
		Size: 138.1 MB (138118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:99287aabe0734a512cffb9c84b24efa94ad9fdb2fa73ab5c9b3fed49717c08a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8614695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e696c270e3f27e26ed41745d87386b44d1781d50180ddf1d061b1c83f8fb2b5`

```dockerfile
```

-	Layers:
	-	`sha256:b86554725369ba8ef1f91bc59ac6585f44576b549244a0734b89064e878bf618`  
		Last Modified: Mon, 03 Jun 2024 19:02:17 GMT  
		Size: 8.6 MB (8580995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f742f480f538d4b167f6a84b7c19df8b21f2a2a9f0757bbd594164ea911349ac`  
		Last Modified: Mon, 03 Jun 2024 19:02:17 GMT  
		Size: 33.7 KB (33700 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-lts-and-current-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:a73b7ef4ed0d2a6fb298543227e35350c003b1a76ad74cf3ce8e38de4b363bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **869.9 MB (869907803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac301d4b8cd3c3ee648d6e1827dae0a55c08103531c894c81ab0f13e68055fb`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 15:03:05 GMT
CMD ["gradle"]
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 01 Jun 2024 15:03:05 GMT
WORKDIR /home/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sat, 01 Jun 2024 15:03:05 GMT
ENV JAVA_LTS_HOME=/opt/java/graalvm21
# Sat, 01 Jun 2024 15:03:05 GMT
ENV JAVA_CURRENT_HOME=/opt/java/graalvm22
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading LTS GraalVM"     && JDK_VERSION=21.0.2     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JDK_VERSION}/graalvm-community-jdk-${JDK_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking LTS GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing LTS GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm21         && echo "Downloading current GraalVM"     && JDK_VERSION=22.0.0     && GRAALVM_AMD64_DOWNLOAD_SHA256=e5eeb486a23101753f18181d002c3ede9da13c463fb61d3ea448abe774db0657     && GRAALVM_AARCH64_DOWNLOAD_SHA256=da9a0e11b110ebccff33ade502516d00f574ec3247868007e452cef4143e0904     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JDK_VERSION}/graalvm-community-jdk-${JDK_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking current GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing current GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm22         && echo "Default Java to LTS GraalVM"     && ln --symbolic /opt/java/graalvm21 /opt/java/graalvm     && for bin in /opt/java/graalvm21/bin/*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_VERSION=8.8
# Sat, 01 Jun 2024 15:03:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
# Sat, 01 Jun 2024 15:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version         && chown --recursive gradle:gradle /home/gradle # buildkit
```

-	Layers:
	-	`sha256:d5a2ad729c09fbfdb259ae764f92188efc67a615ffde9bb34a46298d1edf3cd6`  
		Last Modified: Sat, 27 Apr 2024 14:45:36 GMT  
		Size: 27.4 MB (27360530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843be7ef1ebe5009bbc01eb6c51280a686e5716e46ea3301a5c38069d314242a`  
		Last Modified: Tue, 04 Jun 2024 06:59:01 GMT  
		Size: 4.4 KB (4421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4aafe1bda57ccd0ef64dfc929a88b8f3e6e553147d4014bab83ecfca3146a24`  
		Last Modified: Tue, 04 Jun 2024 06:59:05 GMT  
		Size: 126.6 MB (126585540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a3d33a61a8fb3d43143bd2f5655adb882111475cb43daea63fd70a793edbc5`  
		Last Modified: Tue, 04 Jun 2024 06:59:13 GMT  
		Size: 577.8 MB (577836451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd53eb639a7a804df87e72e1222d6b7b6a3f2e8b53d8d0838e63ce56617f215`  
		Last Modified: Tue, 04 Jun 2024 06:59:05 GMT  
		Size: 138.1 MB (138120829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:810c6b0a1e892659a5e3dbe3f7193afab6325244adae6a86f9713d4fb12c8794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8610349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cbf4b65b5052d3418185a9ccbf033a8321cea2dd76e9e8a2154ea847493774`

```dockerfile
```

-	Layers:
	-	`sha256:18baacd1649ccde295c63bccd66ca3aa57958730818b6107fa66ccc8cc4862ea`  
		Last Modified: Tue, 04 Jun 2024 06:59:02 GMT  
		Size: 8.6 MB (8576204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f35bd60a47b0dafb582af4f477b23887ab9452b86640f11936eea5f7fbffac8`  
		Last Modified: Tue, 04 Jun 2024 06:59:01 GMT  
		Size: 34.1 KB (34145 bytes)  
		MIME: application/vnd.in-toto+json
