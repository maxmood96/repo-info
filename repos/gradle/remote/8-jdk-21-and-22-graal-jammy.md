## `gradle:8-jdk-21-and-22-graal-jammy`

```console
$ docker pull gradle@sha256:0935b842517358f9d384c193a6938bb55f7b45421d3d9fccd4a8c3b11330d870
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk-21-and-22-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:3433771eb856f4bcd62b13c1c658002adb5accb4b1c4eae82aac116de14da3aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **904.9 MB (904913129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2d03100b8b23456eb7b1bce8fd0af690bbc099133e3f763f26f818c18322669`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 16 Jun 2024 03:23:28 GMT
ARG RELEASE
# Sun, 16 Jun 2024 03:23:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 16 Jun 2024 03:23:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 16 Jun 2024 03:23:28 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 16 Jun 2024 03:23:28 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Sun, 16 Jun 2024 03:23:28 GMT
CMD ["/bin/bash"]
# Sun, 16 Jun 2024 03:23:28 GMT
CMD ["gradle"]
# Sun, 16 Jun 2024 03:23:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 16 Jun 2024 03:23:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 16 Jun 2024 03:23:28 GMT
WORKDIR /home/gradle
# Sun, 16 Jun 2024 03:23:28 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sun, 16 Jun 2024 03:23:28 GMT
ENV JAVA_LTS_HOME=/opt/java/graalvm21
# Sun, 16 Jun 2024 03:23:28 GMT
ENV JAVA_CURRENT_HOME=/opt/java/graalvm22
# Sun, 16 Jun 2024 03:23:28 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading LTS GraalVM"     && JAVA_21_VERSION=21.0.2     && GRAALVM_21_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_21_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_21_VERSION}/graalvm-community-jdk-${JAVA_21_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking LTS GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_21_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_21_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing LTS GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm21         && echo "Downloading current GraalVM"     && JAVA_22_VERSION=22.0.1     && GRAALVM_22_AMD64_DOWNLOAD_SHA256=e34ec7e8e8c6a4bb99ab4fa32c3e04d01f2f2bd88920ddda7545fd35a0511f75     && GRAALVM_22_AARCH64_DOWNLOAD_SHA256=2a510338cc6b63d2bb6aebe0ce0f8df9b76d9255207456cb1f0c9c820e6428cf     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_22_VERSION}/graalvm-community-jdk-${JAVA_22_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking current GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_22_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_22_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing current GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm22         && echo "Default Java to LTS GraalVM"     && ln --symbolic /opt/java/graalvm21 /opt/java/graalvm     && for bin in /opt/java/graalvm21/bin/*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
ENV GRADLE_VERSION=8.8
# Sun, 16 Jun 2024 03:23:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
# Sun, 16 Jun 2024 03:23:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version         && chown --recursive gradle:gradle /home/gradle # buildkit
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7001e1dc282f6a01b02e7477c6d310408c5b2459bca837771c0cd09644452735`  
		Last Modified: Tue, 02 Jul 2024 03:19:12 GMT  
		Size: 4.4 KB (4418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e048e4dcd7ecd5bcb776ada4a811ee774df43947217d741602d91959630ce23b`  
		Last Modified: Tue, 02 Jul 2024 03:19:14 GMT  
		Size: 126.4 MB (126397899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ac4794fefd565bd258975225aa609631bcca720669c279dcd7b906e85f43fc`  
		Last Modified: Tue, 02 Jul 2024 03:19:19 GMT  
		Size: 610.9 MB (610858051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cd07810274b65abb3a561b5343af4a0c19fd07bc604f39c7c7df7e1e340b64`  
		Last Modified: Tue, 02 Jul 2024 03:19:14 GMT  
		Size: 138.1 MB (138118674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-21-and-22-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:58ddc38567500105a47ff156d1e2cabfb8359c5ac21c129323ef3885e7c76cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8614750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a272fbcb6a9d2924c44f9425ae69e9f7d8666653110c020acfdc04bb2ed99ab9`

```dockerfile
```

-	Layers:
	-	`sha256:daa2e8e13da6cdc7fc0c4904c94c3e93e8f51e668a0b856c07f892d62641cd9f`  
		Last Modified: Tue, 02 Jul 2024 03:19:12 GMT  
		Size: 8.6 MB (8580889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26e473225de3d95388765fb0005cda55703a9a69412c682109b33028c5484e50`  
		Last Modified: Tue, 02 Jul 2024 03:19:12 GMT  
		Size: 33.9 KB (33861 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-21-and-22-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:79091d9db252750d251e21ce22e7e6fcc8d76c2df7520bf45098e6cdc3c5661d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **864.9 MB (864855823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea876124a99a717ecb7d5902f59094b21ab028f0d0f1facafe71b33d7b7b2b4`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 16 Jun 2024 03:23:28 GMT
ARG RELEASE
# Sun, 16 Jun 2024 03:23:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 16 Jun 2024 03:23:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 16 Jun 2024 03:23:28 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 16 Jun 2024 03:23:28 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Sun, 16 Jun 2024 03:23:28 GMT
CMD ["/bin/bash"]
# Sun, 16 Jun 2024 03:23:28 GMT
CMD ["gradle"]
# Sun, 16 Jun 2024 03:23:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 16 Jun 2024 03:23:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 16 Jun 2024 03:23:28 GMT
WORKDIR /home/gradle
# Sun, 16 Jun 2024 03:23:28 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sun, 16 Jun 2024 03:23:28 GMT
ENV JAVA_LTS_HOME=/opt/java/graalvm21
# Sun, 16 Jun 2024 03:23:28 GMT
ENV JAVA_CURRENT_HOME=/opt/java/graalvm22
# Sun, 16 Jun 2024 03:23:28 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading LTS GraalVM"     && JAVA_21_VERSION=21.0.2     && GRAALVM_21_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_21_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_21_VERSION}/graalvm-community-jdk-${JAVA_21_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking LTS GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_21_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_21_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing LTS GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm21         && echo "Downloading current GraalVM"     && JAVA_22_VERSION=22.0.1     && GRAALVM_22_AMD64_DOWNLOAD_SHA256=e34ec7e8e8c6a4bb99ab4fa32c3e04d01f2f2bd88920ddda7545fd35a0511f75     && GRAALVM_22_AARCH64_DOWNLOAD_SHA256=2a510338cc6b63d2bb6aebe0ce0f8df9b76d9255207456cb1f0c9c820e6428cf     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_22_VERSION}/graalvm-community-jdk-${JAVA_22_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking current GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_22_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_22_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing current GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm22         && echo "Default Java to LTS GraalVM"     && ln --symbolic /opt/java/graalvm21 /opt/java/graalvm     && for bin in /opt/java/graalvm21/bin/*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
ENV GRADLE_VERSION=8.8
# Sun, 16 Jun 2024 03:23:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
# Sun, 16 Jun 2024 03:23:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version         && chown --recursive gradle:gradle /home/gradle # buildkit
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa7a4fed48bd512126784af7a228b68a81312295e7900e8db2a50986a220dca`  
		Last Modified: Tue, 02 Jul 2024 14:48:19 GMT  
		Size: 4.4 KB (4418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6252a2eb650e8cb559089974259628ed6ec2872161b8e0553e51b211256fc5a4`  
		Last Modified: Tue, 02 Jul 2024 14:48:23 GMT  
		Size: 122.5 MB (122462044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bcbf96df6f3fa3664bb1dcaff7466d79bf2e7101c40174bd1991c990a37685`  
		Last Modified: Tue, 02 Jul 2024 14:48:31 GMT  
		Size: 576.9 MB (576908479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43e574a92224bf3e9664a3be3e37cb2c4daa20a077e95eb7e85f19892555778`  
		Last Modified: Tue, 02 Jul 2024 14:48:23 GMT  
		Size: 138.1 MB (138120825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-21-and-22-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:65801a968d60c410e0027d197296b94c6ebcb6284324f66725f0069caf0ad327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8610334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a6d4d2847b8335b5711ed68dc33974685af973a39d05a0002620e68986c6da`

```dockerfile
```

-	Layers:
	-	`sha256:908f137922f4c14e3cb6ad5968de0ef86569dd0ae1367d73e96abef8ca159bd1`  
		Last Modified: Tue, 02 Jul 2024 14:48:20 GMT  
		Size: 8.6 MB (8576029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42e34d0ebae9a277dd165578fa7f8cc854e59eec1b05e465a3e3bf4954e817a4`  
		Last Modified: Tue, 02 Jul 2024 14:48:19 GMT  
		Size: 34.3 KB (34305 bytes)  
		MIME: application/vnd.in-toto+json
