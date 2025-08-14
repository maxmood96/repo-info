## `gradle:8-jdk-lts-and-current-graal-noble`

```console
$ docker pull gradle@sha256:0beca090189fd1b42c60a15dacc888e14b809b0caa7f190ad3bd07a61f27f4cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk-lts-and-current-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:3e53436c0c9e8d1640b1dca2544ed3277bef609f69f454403c5fcae076e6f2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **942.0 MB (941992730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861b35d1fa721540eb97da5b643a6e73f277fc8ad5cd06bdfd496aabbdda91cf`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Jul 2025 03:50:10 GMT
ARG RELEASE
# Thu, 17 Jul 2025 03:50:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 17 Jul 2025 03:50:10 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["/bin/bash"]
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["gradle"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 17 Jul 2025 03:50:10 GMT
WORKDIR /home/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_LTS_HOME=/opt/java/graalvm21
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_CURRENT_HOME=/opt/java/graalvm24
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading LTS GraalVM"     && JAVA_21_VERSION=21.0.2     && GRAALVM_21_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_21_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_21_VERSION}/graalvm-community-jdk-${JAVA_21_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking LTS GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_21_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_21_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing LTS GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm21         && echo "Downloading current GraalVM"     && JAVA_24_VERSION=24.0.2     && GRAALVM_24_AMD64_DOWNLOAD_SHA256=6d62846c826ddb9307deec71e7661c26fa5a5e3985d7bb9005ea42163a390720     && GRAALVM_24_AARCH64_DOWNLOAD_SHA256=c54d951a858791483d58270ecbc0946f28c4742c7fac74a4ebb2764bbf66d6f5     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_24_VERSION}/graalvm-community-jdk-${JAVA_24_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking current GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_24_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_24_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing current GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm24         && echo "Default Java to LTS GraalVM"     && ln --symbolic /opt/java/graalvm21 /opt/java/graalvm     && for bin in /opt/java/graalvm21/bin/*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 17 Jul 2025 03:50:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version         && chown --recursive gradle:gradle /home/gradle # buildkit
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e32affcddf0a830fbd52f9018e5d156d35da8224b03405a1283a38756cce959`  
		Last Modified: Tue, 12 Aug 2025 18:09:36 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334790cbb427dec67977eb383407435638dbddb2021415889d47fb7bdba9a05d`  
		Last Modified: Wed, 13 Aug 2025 02:40:08 GMT  
		Size: 148.6 MB (148611407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce4d78d601f8219ac03868e45ab078c6b7c5519b3bcf0ef41310ae43f8e593b`  
		Last Modified: Wed, 13 Aug 2025 02:41:49 GMT  
		Size: 626.2 MB (626205085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63d27bbb91e198a0b8490e903608fe7f04f5c949658f5ef1326468669019ea5`  
		Last Modified: Wed, 13 Aug 2025 02:41:11 GMT  
		Size: 137.5 MB (137451578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-lts-and-current-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:209872ba172cafd10979ff3ab23519b6dc99d6502d155025619c8a79dd0d0ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9421003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e345b2348612e14e18ecead5a9754d198bfbc41825c661cad8845be3d17f4a`

```dockerfile
```

-	Layers:
	-	`sha256:bbea7e7450f28781e0b4bd402593a9534a1cf2065a0ae34c75a4c49581cefe96`  
		Last Modified: Tue, 12 Aug 2025 20:22:52 GMT  
		Size: 9.4 MB (9385910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe98ebe5820065425bba5a0ce854d7410582e6f72ae7e5b477a6920a754e45d7`  
		Last Modified: Tue, 12 Aug 2025 20:22:53 GMT  
		Size: 35.1 KB (35093 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-lts-and-current-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:4205a7eaca01aeaa27538374f7da9526c0a2b5704ae1aaa35df38f9bbb19476f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **902.1 MB (902104825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f044142090e73aa92d1ea3fe1bcb00f70fb6a6d7c26d89a7030bc4101930ee9`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Jul 2025 03:50:10 GMT
ARG RELEASE
# Thu, 17 Jul 2025 03:50:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 17 Jul 2025 03:50:10 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["/bin/bash"]
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["gradle"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 17 Jul 2025 03:50:10 GMT
WORKDIR /home/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_LTS_HOME=/opt/java/graalvm21
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_CURRENT_HOME=/opt/java/graalvm24
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading LTS GraalVM"     && JAVA_21_VERSION=21.0.2     && GRAALVM_21_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_21_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_21_VERSION}/graalvm-community-jdk-${JAVA_21_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking LTS GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_21_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_21_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing LTS GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm21         && echo "Downloading current GraalVM"     && JAVA_24_VERSION=24.0.2     && GRAALVM_24_AMD64_DOWNLOAD_SHA256=6d62846c826ddb9307deec71e7661c26fa5a5e3985d7bb9005ea42163a390720     && GRAALVM_24_AARCH64_DOWNLOAD_SHA256=c54d951a858791483d58270ecbc0946f28c4742c7fac74a4ebb2764bbf66d6f5     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_24_VERSION}/graalvm-community-jdk-${JAVA_24_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking current GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_24_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_24_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing current GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* /opt/java/graalvm24         && echo "Default Java to LTS GraalVM"     && ln --symbolic /opt/java/graalvm21 /opt/java/graalvm     && for bin in /opt/java/graalvm21/bin/*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 17 Jul 2025 03:50:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version         && chown --recursive gradle:gradle /home/gradle # buildkit
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f3d2a4730f4f7f732d8fa418dd789c5089376011e38d3f7bc6c7f82163700a`  
		Last Modified: Tue, 12 Aug 2025 19:51:39 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe11a29c5b203cc13f5df004955ba8b8441605368be46e7efa1acbb2f7dae81`  
		Last Modified: Tue, 12 Aug 2025 21:26:04 GMT  
		Size: 143.7 MB (143701731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a9c389bf930b3424d54323a5f4764a9c05410c34b9c8b2ceb54296ca5c4b59`  
		Last Modified: Tue, 12 Aug 2025 21:26:50 GMT  
		Size: 592.1 MB (592084147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76832899946ff217ff4f2377d3d4e3cd3ca9cce272144c58c1b860075e670e2a`  
		Last Modified: Tue, 12 Aug 2025 21:27:03 GMT  
		Size: 137.5 MB (137457126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-lts-and-current-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:1a984eec5f56560e7541233197bf040fd727108bce94896dcedcf25f30736091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9389818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6209afd3e29ee5a99651255df215cd4e35245233844123ca1c2c74009c197ad2`

```dockerfile
```

-	Layers:
	-	`sha256:30856248d40b19305c5ba630635bc7f8a41c8f78f41fcfa9ddb79b37b6404fcb`  
		Last Modified: Tue, 12 Aug 2025 20:23:02 GMT  
		Size: 9.4 MB (9354481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b750d96869005c287d0adcf408f992ac3ed6719d38729e323d937af737d8c71b`  
		Last Modified: Tue, 12 Aug 2025 20:23:03 GMT  
		Size: 35.3 KB (35337 bytes)  
		MIME: application/vnd.in-toto+json
