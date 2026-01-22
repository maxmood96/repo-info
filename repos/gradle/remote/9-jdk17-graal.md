## `gradle:9-jdk17-graal`

```console
$ docker pull gradle@sha256:6d246c7e30d30673522ee1d82836dca935b0d91341b1cedb4f0db3c2bea904d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk17-graal` - linux; amd64

```console
$ docker pull gradle@sha256:7bcc199e1fd6763d7e7d974e16b4522d4c788504f03baa87d72a4f55f07a910f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.5 MB (606452992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a98446525776b54ba45d75b810904e975b8b68a1840170e043be75f4e3e3ca19`
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
# Fri, 16 Jan 2026 21:44:52 GMT
CMD ["gradle"]
# Fri, 16 Jan 2026 21:44:52 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Jan 2026 21:44:52 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 16 Jan 2026 21:44:52 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Jan 2026 21:44:52 GMT
WORKDIR /home/gradle
# Fri, 16 Jan 2026 21:45:26 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 16 Jan 2026 21:45:26 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 16 Jan 2026 21:45:26 GMT
ENV JAVA_VERSION=17.0.9
# Fri, 16 Jan 2026 21:45:37 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Fri, 16 Jan 2026 21:45:37 GMT
ENV GRADLE_VERSION=9.3.0
# Fri, 16 Jan 2026 21:45:37 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Fri, 16 Jan 2026 21:45:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 16 Jan 2026 21:45:39 GMT
USER gradle
# Fri, 16 Jan 2026 21:45:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 16 Jan 2026 21:45:39 GMT
USER root
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034f4a472465f68b0a6e62e33c2662458563616278ba1861a073053679d2400e`  
		Last Modified: Fri, 16 Jan 2026 21:46:11 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3399881fc27bda820ffc34a310399a738a7a0d6d0447591975b7aeb1502d7aa5`  
		Last Modified: Fri, 16 Jan 2026 21:46:18 GMT  
		Size: 148.6 MB (148647198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07ded04472c33b69b565102b998e497c71704504653d285cda71409716aee64`  
		Last Modified: Fri, 16 Jan 2026 21:46:21 GMT  
		Size: 291.1 MB (291064014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67021afe909c06cd724c85d9cd3b5aba92ccaa86858676cdd7d3c2afc4127893`  
		Last Modified: Sat, 17 Jan 2026 00:35:15 GMT  
		Size: 137.0 MB (136988868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e0f2b0800687b1db5ea0b69ff3813d96a6e2702e6d67c310866ddb408d3ef7`  
		Last Modified: Fri, 16 Jan 2026 21:46:26 GMT  
		Size: 25.6 KB (25584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:636d694bcfabe50e42c0811b056e8ab1128274e9f8fe7069b51610e387f1fb50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9021756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b079c85ada50ab65cd41dafb1f71d9997cbd334e99ab059c23309dd9428095f8`

```dockerfile
```

-	Layers:
	-	`sha256:2b822591c60ccdc1256ca8110d281e5db863f2063e2e9594467630341f430d56`  
		Last Modified: Sat, 17 Jan 2026 00:23:52 GMT  
		Size: 9.0 MB (8992704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:797b33bef1ff22c9515b63c5b43568acb504a7c15aba91a80e0586480eebdba0`  
		Last Modified: Fri, 16 Jan 2026 21:46:11 GMT  
		Size: 29.1 KB (29052 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:aa48d34b2e25e8e1320cbad8a2f99ff9ee6d5455c224bb987085523a2b14ac0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.1 MB (593136529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b648c3662a0532ac57f71d96d8c9071add92b93e6218397eb63138c1fc811b`
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
# Fri, 16 Jan 2026 21:46:40 GMT
CMD ["gradle"]
# Fri, 16 Jan 2026 21:46:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Jan 2026 21:46:40 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 16 Jan 2026 21:46:40 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Jan 2026 21:46:40 GMT
WORKDIR /home/gradle
# Fri, 16 Jan 2026 21:47:13 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 16 Jan 2026 21:47:13 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 16 Jan 2026 21:47:13 GMT
ENV JAVA_VERSION=17.0.9
# Fri, 16 Jan 2026 21:47:25 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Fri, 16 Jan 2026 21:47:25 GMT
ENV GRADLE_VERSION=9.3.0
# Fri, 16 Jan 2026 21:47:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Fri, 16 Jan 2026 21:47:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 16 Jan 2026 21:47:27 GMT
USER gradle
# Fri, 16 Jan 2026 21:47:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 16 Jan 2026 21:47:27 GMT
USER root
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385ab6a313a4c614d992863714dd362cd3dd167b6f691cd5135803371943cd1f`  
		Last Modified: Fri, 16 Jan 2026 21:48:15 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7ac04f5f5f469e68eff15886c4e26fdfdd6c308ad5a1a5be1bc8b85cd64ee1`  
		Last Modified: Sun, 18 Jan 2026 09:09:17 GMT  
		Size: 143.8 MB (143751083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aae4fc53eae892d27a682a407b1e52c5f520ea13aebeea5395e91b6e02b2cab`  
		Last Modified: Fri, 16 Jan 2026 21:48:09 GMT  
		Size: 283.5 MB (283502126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b2492a8d2c9ec4157a7b183a0d476fa40d566a7b6091cd9391e98a451068ce`  
		Last Modified: Sun, 18 Jan 2026 09:09:20 GMT  
		Size: 137.0 MB (136988868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47798b2e950022995e998287b53471e7d2f4f7a4c697f637324aff12d5b38b0`  
		Last Modified: Fri, 16 Jan 2026 21:48:15 GMT  
		Size: 29.3 KB (29312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:a0238e1b2621a93d06698cb92e8ce5f3deace3e6079373a1ef290195ef398b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9017549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05fe23b44233f988fd0bfe817e7a089a80a884809bc9336e3de01e5c65972c9`

```dockerfile
```

-	Layers:
	-	`sha256:7025c1d4ae834a32d3c45afea7627fd3c547ecbdace7d3c239c314a78caa3a3b`  
		Last Modified: Sat, 17 Jan 2026 00:24:05 GMT  
		Size: 9.0 MB (8988285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56f83d712ffa98b6d44423b8654ed1547e741d4624cc16423d4444a9538fa918`  
		Last Modified: Sat, 17 Jan 2026 00:24:05 GMT  
		Size: 29.3 KB (29264 bytes)  
		MIME: application/vnd.in-toto+json
