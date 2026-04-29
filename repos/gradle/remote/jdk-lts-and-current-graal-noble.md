## `gradle:jdk-lts-and-current-graal-noble`

```console
$ docker pull gradle@sha256:a24142082133af483a18fc2af5e28fc811b3b99aedf047e9bb0bfef1fe323038
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-lts-and-current-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:a14d20ff9f89e86f71ce1ac625f34cd8902216e54731bd63ae8343ee188773e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.2 MB (659218481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3197ef863617a229f646e5662058282f1c5f6b7d3204bcdb4d3dc969ea063817`
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
# Tue, 28 Apr 2026 23:31:52 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:31:52 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:31:52 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 28 Apr 2026 23:31:52 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:31:52 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:32:23 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 28 Apr 2026 23:32:23 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 28 Apr 2026 23:32:23 GMT
ENV JAVA_LTS_HOME=/opt/java/graalvm25
# Tue, 28 Apr 2026 23:32:23 GMT
ENV JAVA_CURRENT_HOME=/opt/java/graalvm25
# Tue, 28 Apr 2026 23:32:35 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading LTS GraalVM"     && JAVA_LTS_VERSION=25.0.2     && GRAALVM_LTS_AMD64_DOWNLOAD_SHA256=e0be791c8fda4d03b6b0a0cb824fef3149736170057b3a515252b44419606af0     && GRAALVM_LTS_AARCH64_DOWNLOAD_SHA256=b4580d9f223d0a4b3a1757e58b18ff4c1db950e67e105fc5cb741457d2384a71     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_LTS_VERSION}/graalvm-community-jdk-${JAVA_LTS_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking LTS GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_LTS_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_LTS_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing LTS GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_LTS_HOME}"         && echo "Downloading current GraalVM"     && JAVA_CURRENT_VERSION=25.0.2     && GRAALVM_CURRENT_AMD64_DOWNLOAD_SHA256=e0be791c8fda4d03b6b0a0cb824fef3149736170057b3a515252b44419606af0     && GRAALVM_CURRENT_AARCH64_DOWNLOAD_SHA256=b4580d9f223d0a4b3a1757e58b18ff4c1db950e67e105fc5cb741457d2384a71     && if [ "${JAVA_LTS_VERSION}" != "${JAVA_CURRENT_VERSION}" ]; then       ARCHITECTURE=$(dpkg --print-architecture)       && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi       && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi       && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_CURRENT_VERSION}/graalvm-community-jdk-${JAVA_CURRENT_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz       && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"             && echo "Checking current GraalVM download hash"       && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_CURRENT_AMD64_DOWNLOAD_SHA256}"; fi       && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_CURRENT_AARCH64_DOWNLOAD_SHA256}"; fi       && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -             && echo "Installing current GraalVM"       && tar --extract --gunzip --file graalvm.tar.gz       && rm graalvm.tar.gz       && mv graalvm-* "${JAVA_CURRENT_HOME}";     fi         && echo "Default Java to LTS GraalVM"     && ln --symbolic "${JAVA_LTS_HOME}" /opt/java/graalvm     && for bin in "$JAVA_LTS_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 28 Apr 2026 23:32:35 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:32:35 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:32:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:32:37 GMT
USER gradle
# Tue, 28 Apr 2026 23:32:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:32:38 GMT
USER root
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5893c23064edd949f2d370e8246d471a1c867ca676967b195500def3ce024e0`  
		Last Modified: Tue, 28 Apr 2026 23:33:17 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4468065d95ae01c8fb485479b150d90707ce405a8a800c6f3fa0ce88d28a8247`  
		Last Modified: Tue, 28 Apr 2026 23:33:25 GMT  
		Size: 148.3 MB (148328488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a275379686f34ef1652d33b4564f7ba2b1967c6cf71a830561d08242b2a9ad`  
		Last Modified: Tue, 28 Apr 2026 23:33:29 GMT  
		Size: 340.9 MB (340894017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62b893002263b0624e7bd71ff808b091af6bf1f85e94ec1fe24742d437e47e1`  
		Last Modified: Tue, 28 Apr 2026 23:33:25 GMT  
		Size: 140.2 MB (140235939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9365d3e0e7433313af03b0f9e03c3583a2300f7d1ad17eaab0c60a2c6fbc7c80`  
		Last Modified: Tue, 28 Apr 2026 23:33:18 GMT  
		Size: 25.6 KB (25614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:7b918363024ce10c6259050ab833b71b1d974f86fec257fd5a6bc7fd9175bf44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9089879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9713e9f76e357cf04464548f938783c8b9efad98df43b26cfee5a3c964310948`

```dockerfile
```

-	Layers:
	-	`sha256:c2f2a986d18f5e073a1bf3ee8f5e92d0a17e0aa909f7fd871f84f3072d924994`  
		Last Modified: Tue, 28 Apr 2026 23:33:18 GMT  
		Size: 9.1 MB (9051397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41be8492e132e19b0cee6f82e384b0917a58c4e853895e26a0d5e0bf157e49b7`  
		Last Modified: Tue, 28 Apr 2026 23:33:17 GMT  
		Size: 38.5 KB (38482 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-lts-and-current-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:6078c5866be134bc15cbe68113601767d9fe32ae1bd1a0f0d606961478c1cac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.6 MB (628577459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff6a29b3a71666e5a0260700d6f8aceccbe6ccb66d2fd4f8fcb24434742f935`
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
# Tue, 28 Apr 2026 23:33:15 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:33:15 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:33:15 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 28 Apr 2026 23:33:15 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:33:15 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:33:54 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 28 Apr 2026 23:33:54 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 28 Apr 2026 23:33:54 GMT
ENV JAVA_LTS_HOME=/opt/java/graalvm25
# Tue, 28 Apr 2026 23:33:54 GMT
ENV JAVA_CURRENT_HOME=/opt/java/graalvm25
# Tue, 28 Apr 2026 23:34:04 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading LTS GraalVM"     && JAVA_LTS_VERSION=25.0.2     && GRAALVM_LTS_AMD64_DOWNLOAD_SHA256=e0be791c8fda4d03b6b0a0cb824fef3149736170057b3a515252b44419606af0     && GRAALVM_LTS_AARCH64_DOWNLOAD_SHA256=b4580d9f223d0a4b3a1757e58b18ff4c1db950e67e105fc5cb741457d2384a71     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_LTS_VERSION}/graalvm-community-jdk-${JAVA_LTS_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking LTS GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_LTS_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_LTS_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing LTS GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_LTS_HOME}"         && echo "Downloading current GraalVM"     && JAVA_CURRENT_VERSION=25.0.2     && GRAALVM_CURRENT_AMD64_DOWNLOAD_SHA256=e0be791c8fda4d03b6b0a0cb824fef3149736170057b3a515252b44419606af0     && GRAALVM_CURRENT_AARCH64_DOWNLOAD_SHA256=b4580d9f223d0a4b3a1757e58b18ff4c1db950e67e105fc5cb741457d2384a71     && if [ "${JAVA_LTS_VERSION}" != "${JAVA_CURRENT_VERSION}" ]; then       ARCHITECTURE=$(dpkg --print-architecture)       && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi       && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi       && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_CURRENT_VERSION}/graalvm-community-jdk-${JAVA_CURRENT_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz       && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"             && echo "Checking current GraalVM download hash"       && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_CURRENT_AMD64_DOWNLOAD_SHA256}"; fi       && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_CURRENT_AARCH64_DOWNLOAD_SHA256}"; fi       && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -             && echo "Installing current GraalVM"       && tar --extract --gunzip --file graalvm.tar.gz       && rm graalvm.tar.gz       && mv graalvm-* "${JAVA_CURRENT_HOME}";     fi         && echo "Default Java to LTS GraalVM"     && ln --symbolic "${JAVA_LTS_HOME}" /opt/java/graalvm     && for bin in "$JAVA_LTS_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 28 Apr 2026 23:34:04 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:34:04 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:34:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:34:07 GMT
USER gradle
# Tue, 28 Apr 2026 23:34:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:34:08 GMT
USER root
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca6da34f7eda58815aa282512a0cb2198dc339526b7a13253d8dad447d599ee`  
		Last Modified: Tue, 28 Apr 2026 23:34:42 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7dcf782ae98e30350a89ba678c4c68266c0f594a39ed1a1342067d7eff297d`  
		Last Modified: Tue, 28 Apr 2026 23:34:50 GMT  
		Size: 143.4 MB (143448423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b498cc5231b187d1c68bd17a044f8f750b128b99cb6a340360aebcceb9bfb5`  
		Last Modified: Tue, 28 Apr 2026 23:34:53 GMT  
		Size: 316.0 MB (315986531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bb9f8fdf810c3ad40efc7584c2ee1a8535cfbeb8da2d02a79df4bda9e474d6`  
		Last Modified: Tue, 28 Apr 2026 23:34:50 GMT  
		Size: 140.2 MB (140235938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef62f53d9ee0264b92ba539b38429dbb8b56245911493b48561d8b9c579fbff`  
		Last Modified: Tue, 28 Apr 2026 23:34:44 GMT  
		Size: 29.3 KB (29334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:425f534799d0e5a9b47409f22b51d7affcdb3309978ec7280ff225ddb8a2d2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9085144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a91d498343cd8f660f370ba8461d0dedc842d8b6bebc777915b25ba046d8cd`

```dockerfile
```

-	Layers:
	-	`sha256:914445e210c4f43d3d5cb69fdc81c2c518e265e1a5f8c0cf8c02e114fe88b658`  
		Last Modified: Tue, 28 Apr 2026 23:34:43 GMT  
		Size: 9.0 MB (9046353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:def8126a4ebadc66f7db30103bdb48929c3b38f5b1cb31530ddbe3e44d7dc12a`  
		Last Modified: Tue, 28 Apr 2026 23:34:43 GMT  
		Size: 38.8 KB (38791 bytes)  
		MIME: application/vnd.in-toto+json
