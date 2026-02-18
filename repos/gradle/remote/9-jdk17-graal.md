## `gradle:9-jdk17-graal`

```console
$ docker pull gradle@sha256:a57586908ddef9ff2693e7bc3baaddbd4df39c48c5ecdd5153f044fb53e1d2e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk17-graal` - linux; amd64

```console
$ docker pull gradle@sha256:58cfb22e8b2fcfd50e473460fa6e50952c106d70c356963de1ae4b53cf585b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.7 MB (607698389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0b39f1e848b1a3bd72d8bc2d012d18dbee7574d51c224780de101249ee4d95`
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
# Tue, 17 Feb 2026 20:20:47 GMT
CMD ["gradle"]
# Tue, 17 Feb 2026 20:20:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 17 Feb 2026 20:20:47 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 17 Feb 2026 20:20:47 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 17 Feb 2026 20:20:47 GMT
WORKDIR /home/gradle
# Tue, 17 Feb 2026 20:21:24 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 17 Feb 2026 20:21:24 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 17 Feb 2026 20:21:24 GMT
ENV JAVA_VERSION=17.0.9
# Tue, 17 Feb 2026 20:21:36 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Tue, 17 Feb 2026 20:21:36 GMT
ENV GRADLE_VERSION=9.3.1
# Tue, 17 Feb 2026 20:21:36 GMT
ARG GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
# Tue, 17 Feb 2026 20:21:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 17 Feb 2026 20:21:38 GMT
USER gradle
# Tue, 17 Feb 2026 20:21:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 17 Feb 2026 20:21:38 GMT
USER root
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05dee801d0971eb4f27d266f2a5c4b27f0b7fdc1f40a38b1c6677bfd8e50355d`  
		Last Modified: Tue, 17 Feb 2026 20:22:12 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3de18a93292e35742b7c04c3b98e35decd4563d953e1f631c2868128bdbb225`  
		Last Modified: Tue, 17 Feb 2026 20:22:20 GMT  
		Size: 149.9 MB (149859420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515e45df4f18e3bd60821b54b9407f47c3d27f0d9a087e6d23888787a1b95da9`  
		Last Modified: Tue, 17 Feb 2026 20:22:22 GMT  
		Size: 291.1 MB (291064745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e931ec6c980336651441c982d4e9e9e1d368c0a66780f6c087435d8201891f`  
		Last Modified: Tue, 17 Feb 2026 20:22:19 GMT  
		Size: 137.0 MB (137019690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd78e7a9ed947837cc42fc19c3757fe497388e3cc6c8bb7c9855b7245fca39f`  
		Last Modified: Tue, 17 Feb 2026 20:22:13 GMT  
		Size: 25.6 KB (25604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:03f1fb4ccb20664512ecfda47304900718587fbb83a151ff6aab0bc2ad8a45e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9021852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f02f09d4fade950fd051cded965b286fdd3983c8cd3856d4cefbef99de8a5d`

```dockerfile
```

-	Layers:
	-	`sha256:149eec927f1d1f333be8d5f14971e6b8b3a180b7a9ed99502ceda1145b1835bb`  
		Last Modified: Tue, 17 Feb 2026 20:22:13 GMT  
		Size: 9.0 MB (8992800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39ec154ebefe9b7a7026ee3e1be0dbd04854ecb50d2502459ed63304021b0153`  
		Last Modified: Tue, 17 Feb 2026 20:22:12 GMT  
		Size: 29.1 KB (29052 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:81114e5d5c8b0cb234363c39670d0d7d086964317d7b43743b9b81438c905e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.3 MB (594338380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43506ebdb189b6a3137f801584b13c3c05b061d55355365fafcb35815adc9e8`
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
# Tue, 17 Feb 2026 20:19:54 GMT
CMD ["gradle"]
# Tue, 17 Feb 2026 20:19:54 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 17 Feb 2026 20:19:54 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 17 Feb 2026 20:19:54 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 17 Feb 2026 20:19:54 GMT
WORKDIR /home/gradle
# Tue, 17 Feb 2026 20:20:29 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 17 Feb 2026 20:20:29 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 17 Feb 2026 20:20:29 GMT
ENV JAVA_VERSION=17.0.9
# Tue, 17 Feb 2026 20:20:38 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Tue, 17 Feb 2026 20:20:38 GMT
ENV GRADLE_VERSION=9.3.1
# Tue, 17 Feb 2026 20:20:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
# Tue, 17 Feb 2026 20:20:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 17 Feb 2026 20:20:41 GMT
USER gradle
# Tue, 17 Feb 2026 20:20:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 17 Feb 2026 20:20:41 GMT
USER root
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edce5e874caabb2c0834b6424986ad27f26223c31da0458281d390596cecbf2`  
		Last Modified: Tue, 17 Feb 2026 20:21:13 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa155336df6b494bef29b822ac14e4505afcf3a526aaa89869c7c57bcc406d1`  
		Last Modified: Tue, 17 Feb 2026 20:21:20 GMT  
		Size: 144.9 MB (144921699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2481ccd5ef9b970118fd69ed98c07115ee7d444c52ab5a6dc98d4fb05745cf`  
		Last Modified: Tue, 17 Feb 2026 20:21:23 GMT  
		Size: 283.5 MB (283501217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ade452d5bc923a085f0a1934a3e8d3ed5c072f6095ddf1a6c6859565698be6`  
		Last Modified: Tue, 17 Feb 2026 20:21:20 GMT  
		Size: 137.0 MB (137019693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050bf4be764c2571a56fccab363082a2e87a32df553d14c16472dc77c1c63458`  
		Last Modified: Tue, 17 Feb 2026 20:21:14 GMT  
		Size: 29.3 KB (29333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:75d1e8dc05d03fd27a02f87221a87ca95ef643ec7ee65cb983f7259d40210842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9017641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d575354a5a3eea85f28c85a4cafaa5c2fe6c014fc4c0860bf9200e44108cec1e`

```dockerfile
```

-	Layers:
	-	`sha256:001f25e32e85c7c59c38deb101480021f669be805dc6da04510ea75cb286c4a6`  
		Last Modified: Tue, 17 Feb 2026 20:21:14 GMT  
		Size: 9.0 MB (8988377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ed7eea58813b2f8e48f0249b5a9436008fefe772845e6b7a7568c6792d16350`  
		Last Modified: Tue, 17 Feb 2026 20:21:13 GMT  
		Size: 29.3 KB (29264 bytes)  
		MIME: application/vnd.in-toto+json
