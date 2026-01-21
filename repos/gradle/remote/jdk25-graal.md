## `gradle:jdk25-graal`

```console
$ docker pull gradle@sha256:0d04d83e7cbf0b817ab19ddf852c339e2173023b9aa6d56f3b84930a0e04f64b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk25-graal` - linux; amd64

```console
$ docker pull gradle@sha256:f4642c16a6af7571939342e3fcbe59461e43bf0848ad3cd2412acd3ac1fe9493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.2 MB (656241309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7ad26d9c59b043fb8174db2d2e97e4216c8ee44c4060767f33c99259e65d9a3`
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
# Fri, 16 Jan 2026 21:45:01 GMT
CMD ["gradle"]
# Fri, 16 Jan 2026 21:45:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Jan 2026 21:45:01 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 16 Jan 2026 21:45:01 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Jan 2026 21:45:01 GMT
WORKDIR /home/gradle
# Fri, 16 Jan 2026 21:45:37 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 16 Jan 2026 21:45:37 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 16 Jan 2026 21:45:37 GMT
ENV JAVA_VERSION=25.0.1
# Fri, 16 Jan 2026 21:45:49 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=01e39fe1a87f28b842a3e4e3b77be9b544dca3a58fa6e93b924a6106c8bac7fb     && GRAALVM_AARCH64_DOWNLOAD_SHA256=7aa0b9935a80e67f37c6025678393dbd123bb6f2226811decbc1a13093fc8ae2     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Fri, 16 Jan 2026 21:45:49 GMT
ENV GRADLE_VERSION=9.3.0
# Fri, 16 Jan 2026 21:45:49 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Fri, 16 Jan 2026 21:45:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 16 Jan 2026 21:45:51 GMT
USER gradle
# Fri, 16 Jan 2026 21:45:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 16 Jan 2026 21:45:51 GMT
USER root
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0851ebd0a412a293198bc6b3b60852d207f08626b185736b9dd14c98dff7bfc9`  
		Last Modified: Fri, 16 Jan 2026 21:46:31 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ed5704f46deb9db5cbc040e878ebbedb7e44b5853c2c0cd2bc5148a27a50ab`  
		Last Modified: Fri, 16 Jan 2026 21:46:59 GMT  
		Size: 148.6 MB (148648649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39ae5b54da23631ceda96aa88b3aa73e3c67b3a5c86aba7a211f785d9528747`  
		Last Modified: Fri, 16 Jan 2026 21:46:59 GMT  
		Size: 340.9 MB (340850864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3513254c5e5a2f8dca6b1f1e1d0e5cf2bb184538e9076089da4432685aedf5fc`  
		Last Modified: Fri, 16 Jan 2026 21:47:11 GMT  
		Size: 137.0 MB (136988872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72873e2ee300b3b731a1257511f9b4bd66846db13d5d9123e9b6bd5e544566c2`  
		Last Modified: Fri, 16 Jan 2026 21:46:49 GMT  
		Size: 25.6 KB (25593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:51b607d110cfe644f4b2cc9ef3a105114831ff058dcc74ac4e48f6b13f41a6e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9052517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829439a8d29ce86fcd34c34a7adf07804244f7dbd18aedabf74ab278d30b71b5`

```dockerfile
```

-	Layers:
	-	`sha256:bd564b87603cfb67b4762cb476b92faf63e0a54a685fa510f0b06d8b6c179221`  
		Last Modified: Fri, 16 Jan 2026 21:46:31 GMT  
		Size: 9.0 MB (9018577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f673949dd7c4a7b176df081ad739c4baef0e0b7bd61ec827c79cc433166e9209`  
		Last Modified: Sat, 17 Jan 2026 00:21:21 GMT  
		Size: 33.9 KB (33940 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk25-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:38a89d43e01739ace5f3b7adf2df99215be67ec4dd710ec288a6223ed106ed78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.5 MB (625522119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6897699b184a7388329c1b57cbeb463fb5a5c446e7839163da3da216691f0d13`
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
# Fri, 16 Jan 2026 21:43:51 GMT
CMD ["gradle"]
# Fri, 16 Jan 2026 21:43:51 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Jan 2026 21:43:51 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 16 Jan 2026 21:43:51 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Jan 2026 21:43:51 GMT
WORKDIR /home/gradle
# Fri, 16 Jan 2026 21:44:28 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 16 Jan 2026 21:44:28 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 16 Jan 2026 21:44:28 GMT
ENV JAVA_VERSION=25.0.1
# Fri, 16 Jan 2026 21:44:38 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=01e39fe1a87f28b842a3e4e3b77be9b544dca3a58fa6e93b924a6106c8bac7fb     && GRAALVM_AARCH64_DOWNLOAD_SHA256=7aa0b9935a80e67f37c6025678393dbd123bb6f2226811decbc1a13093fc8ae2     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Fri, 16 Jan 2026 21:44:38 GMT
ENV GRADLE_VERSION=9.3.0
# Fri, 16 Jan 2026 21:44:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Fri, 16 Jan 2026 21:44:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 16 Jan 2026 21:44:41 GMT
USER gradle
# Fri, 16 Jan 2026 21:44:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 16 Jan 2026 21:44:41 GMT
USER root
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e270d2818598fc8d5cc9432401ca1455f82dd7814de2ae0e280fe496e8e363e6`  
		Last Modified: Fri, 16 Jan 2026 23:37:59 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386dae7a88459680d13a09a7e7d98d9e2be8da6609ca3fe84ed0de2a5a149d6f`  
		Last Modified: Fri, 16 Jan 2026 21:45:51 GMT  
		Size: 143.7 MB (143749566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d0286361d422fe85e169c704c2e79508d6ccd8fb30d5916e43d423f03aa61f`  
		Last Modified: Fri, 16 Jan 2026 21:45:50 GMT  
		Size: 315.9 MB (315889225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ef843938eac755d9d67d21cac77ba22d9afd911ec41afa8034b5f4456c4f0a`  
		Last Modified: Fri, 16 Jan 2026 21:45:25 GMT  
		Size: 137.0 MB (136988871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d19a0e28664290af1d1b2342490192b36d15b239cb42b4c8dc0bfab36befd40`  
		Last Modified: Fri, 16 Jan 2026 21:45:38 GMT  
		Size: 29.3 KB (29315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:d8db7729720516a4115dfa71e9421a4492b44a49e444d0e1590d8aacb841de11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9048061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2c2beaa21edac384007a8b1729c4f9ea296ce4af77ea5029f43b63d2251902`

```dockerfile
```

-	Layers:
	-	`sha256:ed8ed19b4c3adee000a69768d72500c6ac425e9cc0f9d26a6127f263851cd5a9`  
		Last Modified: Sat, 17 Jan 2026 00:21:29 GMT  
		Size: 9.0 MB (9013717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3194f3066fbdc7c2aa42c8a8c32c173f5f40b3e1d9e70d93ed76873d120cbc2c`  
		Last Modified: Sat, 17 Jan 2026 00:21:29 GMT  
		Size: 34.3 KB (34344 bytes)  
		MIME: application/vnd.in-toto+json
