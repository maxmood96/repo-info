## `gradle:9-jdk-lts-and-current-graal-noble`

```console
$ docker pull gradle@sha256:9f40bbcacd028795502b12b42a4b1c0a0cd868adae6c914c1846e99f9b58c028
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk-lts-and-current-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:c1667f22cfa6c75a3ab07f928d1c931172745797db2247304ab1d7e3d368b3b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.5 MB (657482058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088959fa39cd9d7d035179c20fb66571a1cd176e2ec4b0472d070373026d3118`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:21:03 GMT
CMD ["gradle"]
# Tue, 17 Feb 2026 20:21:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 17 Feb 2026 20:21:03 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 17 Feb 2026 20:21:03 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 17 Feb 2026 20:21:03 GMT
WORKDIR /home/gradle
# Tue, 17 Feb 2026 20:21:39 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 17 Feb 2026 20:21:39 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 17 Feb 2026 20:21:39 GMT
ENV JAVA_LTS_HOME=/opt/java/graalvm25
# Tue, 17 Feb 2026 20:21:39 GMT
ENV JAVA_CURRENT_HOME=/opt/java/graalvm25
# Tue, 17 Feb 2026 20:21:50 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading LTS GraalVM"     && JAVA_LTS_VERSION=25.0.1     && GRAALVM_LTS_AMD64_DOWNLOAD_SHA256=01e39fe1a87f28b842a3e4e3b77be9b544dca3a58fa6e93b924a6106c8bac7fb     && GRAALVM_LTS_AARCH64_DOWNLOAD_SHA256=7aa0b9935a80e67f37c6025678393dbd123bb6f2226811decbc1a13093fc8ae2     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_LTS_VERSION}/graalvm-community-jdk-${JAVA_LTS_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking LTS GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_LTS_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_LTS_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing LTS GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_LTS_HOME}"         && echo "Downloading current GraalVM"     && JAVA_CURRENT_VERSION=25.0.1     && GRAALVM_CURRENT_AMD64_DOWNLOAD_SHA256=01e39fe1a87f28b842a3e4e3b77be9b544dca3a58fa6e93b924a6106c8bac7fb     && GRAALVM_CURRENT_AARCH64_DOWNLOAD_SHA256=7aa0b9935a80e67f37c6025678393dbd123bb6f2226811decbc1a13093fc8ae2     && if [ "${JAVA_LTS_VERSION}" != "${JAVA_CURRENT_VERSION}" ]; then       ARCHITECTURE=$(dpkg --print-architecture)       && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi       && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi       && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_CURRENT_VERSION}/graalvm-community-jdk-${JAVA_CURRENT_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz       && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"             && echo "Checking current GraalVM download hash"       && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_CURRENT_AMD64_DOWNLOAD_SHA256}"; fi       && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_CURRENT_AARCH64_DOWNLOAD_SHA256}"; fi       && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -             && echo "Installing current GraalVM"       && tar --extract --gunzip --file graalvm.tar.gz       && rm graalvm.tar.gz       && mv graalvm-* "${JAVA_CURRENT_HOME}";     fi         && echo "Default Java to LTS GraalVM"     && ln --symbolic "${JAVA_LTS_HOME}" /opt/java/graalvm     && for bin in "$JAVA_LTS_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 17 Feb 2026 20:21:50 GMT
ENV GRADLE_VERSION=9.3.1
# Tue, 17 Feb 2026 20:21:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
# Tue, 17 Feb 2026 20:21:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 17 Feb 2026 20:21:53 GMT
USER gradle
# Tue, 17 Feb 2026 20:21:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 17 Feb 2026 20:21:53 GMT
USER root
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0e9474577e29ba8090f12e045deb539826c526173304061c06c5b226b28b1c`  
		Last Modified: Tue, 17 Feb 2026 20:22:29 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8934f274d96d389724e855baa2e7d0db0ddc14808933df9d4468ba35bddb772b`  
		Last Modified: Tue, 17 Feb 2026 20:22:37 GMT  
		Size: 149.9 MB (149858343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1e89b6ce3cb4e9edd9be07edaa223ea5811667753c0c6088b9ea9b9b136141`  
		Last Modified: Tue, 17 Feb 2026 20:22:42 GMT  
		Size: 340.8 MB (340849362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9550b94fe97a13dbc8c5aa7383b5597822fa49e2510f5a22429f9bb29c8e429`  
		Last Modified: Tue, 17 Feb 2026 20:22:37 GMT  
		Size: 137.0 MB (137019691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd8c179c279aba180837d724bbd2754c7ba2ac012d4d987b5856295a11668e8`  
		Last Modified: Tue, 17 Feb 2026 20:22:30 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-lts-and-current-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:b475212c02a1048935fbe9b9177b21fe5d7335f833d827566b6037163b04a2ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9056315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89a17f71eec4ea90fb475dc0a18570b405fbf13015d331e3fa528537d0b78ec`

```dockerfile
```

-	Layers:
	-	`sha256:26dbf28407c0c4b514e2ac600b1432d97bac0fcaf925b9040e87bd1d33021e7b`  
		Last Modified: Tue, 17 Feb 2026 20:22:29 GMT  
		Size: 9.0 MB (9017831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e50569cc9027355c3746522b09f48632a24e813145710a84baae0796ec3a9a`  
		Last Modified: Tue, 17 Feb 2026 20:22:29 GMT  
		Size: 38.5 KB (38484 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-lts-and-current-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:ab149768e53faa9acc56df5fb260b422fe2eb4d4f6c7b1e2bb28a8b8f567c011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.7 MB (626728632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80aabafc4486d6a466aa1c5c6f32dbc39f18e7f8e39b76f29e667c0a7cc0316`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:20:37 GMT
CMD ["gradle"]
# Tue, 17 Feb 2026 20:20:37 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 17 Feb 2026 20:20:37 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 17 Feb 2026 20:20:37 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 17 Feb 2026 20:20:37 GMT
WORKDIR /home/gradle
# Tue, 17 Feb 2026 20:21:12 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 17 Feb 2026 20:21:12 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 17 Feb 2026 20:21:12 GMT
ENV JAVA_LTS_HOME=/opt/java/graalvm25
# Tue, 17 Feb 2026 20:21:12 GMT
ENV JAVA_CURRENT_HOME=/opt/java/graalvm25
# Tue, 17 Feb 2026 20:21:22 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading LTS GraalVM"     && JAVA_LTS_VERSION=25.0.1     && GRAALVM_LTS_AMD64_DOWNLOAD_SHA256=01e39fe1a87f28b842a3e4e3b77be9b544dca3a58fa6e93b924a6106c8bac7fb     && GRAALVM_LTS_AARCH64_DOWNLOAD_SHA256=7aa0b9935a80e67f37c6025678393dbd123bb6f2226811decbc1a13093fc8ae2     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_LTS_VERSION}/graalvm-community-jdk-${JAVA_LTS_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking LTS GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_LTS_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_LTS_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing LTS GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_LTS_HOME}"         && echo "Downloading current GraalVM"     && JAVA_CURRENT_VERSION=25.0.1     && GRAALVM_CURRENT_AMD64_DOWNLOAD_SHA256=01e39fe1a87f28b842a3e4e3b77be9b544dca3a58fa6e93b924a6106c8bac7fb     && GRAALVM_CURRENT_AARCH64_DOWNLOAD_SHA256=7aa0b9935a80e67f37c6025678393dbd123bb6f2226811decbc1a13093fc8ae2     && if [ "${JAVA_LTS_VERSION}" != "${JAVA_CURRENT_VERSION}" ]; then       ARCHITECTURE=$(dpkg --print-architecture)       && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi       && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi       && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_CURRENT_VERSION}/graalvm-community-jdk-${JAVA_CURRENT_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz       && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"             && echo "Checking current GraalVM download hash"       && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_CURRENT_AMD64_DOWNLOAD_SHA256}"; fi       && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_CURRENT_AARCH64_DOWNLOAD_SHA256}"; fi       && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -             && echo "Installing current GraalVM"       && tar --extract --gunzip --file graalvm.tar.gz       && rm graalvm.tar.gz       && mv graalvm-* "${JAVA_CURRENT_HOME}";     fi         && echo "Default Java to LTS GraalVM"     && ln --symbolic "${JAVA_LTS_HOME}" /opt/java/graalvm     && for bin in "$JAVA_LTS_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 17 Feb 2026 20:21:22 GMT
ENV GRADLE_VERSION=9.3.1
# Tue, 17 Feb 2026 20:21:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
# Tue, 17 Feb 2026 20:21:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 17 Feb 2026 20:21:25 GMT
USER gradle
# Tue, 17 Feb 2026 20:21:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 17 Feb 2026 20:21:25 GMT
USER root
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d78463fb69aa89be720c07ecedc62b29c7b8f452551e5c5091fba3e537e3ba8`  
		Last Modified: Tue, 17 Feb 2026 20:22:01 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1cc1f5d977bff23114dd0f13e31ffbfe2eb0b8262025df21623200629eca7c`  
		Last Modified: Tue, 17 Feb 2026 20:22:09 GMT  
		Size: 144.9 MB (144921346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcb7f2dbbc696bfa2f1a5b5a77097095a98e2d4859343250b32b5cae716a638`  
		Last Modified: Tue, 17 Feb 2026 20:22:12 GMT  
		Size: 315.9 MB (315891694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf9880988cecb0841d6d66be8856942f9b3240f3e26bcaece6d4c95f1d8495b`  
		Last Modified: Tue, 17 Feb 2026 20:22:09 GMT  
		Size: 137.0 MB (137019694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e62f11cc9ac96876a210e0d805523454cdf9ce373bc0c00a5d5e10a1c519d85`  
		Last Modified: Tue, 17 Feb 2026 20:22:03 GMT  
		Size: 29.3 KB (29331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-lts-and-current-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:53e6a52012deab87e00f90bcfb953825bc8d7c70ce21c371c7cab76123ec8193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9051579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45175282dc267ecc2e87b65e9d2e196d866a7a1a0fcaa1cd41ad9bd42884bd9d`

```dockerfile
```

-	Layers:
	-	`sha256:893bfad42ffb4062887a64937ee11feda6b367d60a722f271f9d97be37f86c94`  
		Last Modified: Tue, 17 Feb 2026 20:22:02 GMT  
		Size: 9.0 MB (9012787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04f6c6e4b6f2aa6932a21f2f61fc069de005b04ea3b708632661ec84cf710ef1`  
		Last Modified: Tue, 17 Feb 2026 20:22:01 GMT  
		Size: 38.8 KB (38792 bytes)  
		MIME: application/vnd.in-toto+json
