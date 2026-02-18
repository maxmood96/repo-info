## `gradle:9-graal-noble`

```console
$ docker pull gradle@sha256:a6409fd13b97d9be3cf13dd47c608c4283ccdeeeddc042976ca97348d5125cdb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:d96dd7159bb491be239dc4c493eac7a5b433a2d025cca369aa1ea5a2a313fdac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.5 MB (657483952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549cd2a29c8378b9a38762e48c471d57cc83b9b7ab9ad843224cea3a21775c62`
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
# Tue, 17 Feb 2026 20:20:21 GMT
CMD ["gradle"]
# Tue, 17 Feb 2026 20:20:21 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 17 Feb 2026 20:20:21 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 17 Feb 2026 20:20:21 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 17 Feb 2026 20:20:21 GMT
WORKDIR /home/gradle
# Tue, 17 Feb 2026 20:20:54 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 17 Feb 2026 20:20:54 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 17 Feb 2026 20:20:54 GMT
ENV JAVA_VERSION=25.0.1
# Tue, 17 Feb 2026 20:21:08 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=01e39fe1a87f28b842a3e4e3b77be9b544dca3a58fa6e93b924a6106c8bac7fb     && GRAALVM_AARCH64_DOWNLOAD_SHA256=7aa0b9935a80e67f37c6025678393dbd123bb6f2226811decbc1a13093fc8ae2     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 17 Feb 2026 20:21:08 GMT
ENV GRADLE_VERSION=9.3.1
# Tue, 17 Feb 2026 20:21:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
# Tue, 17 Feb 2026 20:21:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 17 Feb 2026 20:21:10 GMT
USER gradle
# Tue, 17 Feb 2026 20:21:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 17 Feb 2026 20:21:11 GMT
USER root
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a06830a2e6accd82407929c348728f7fe497ee9ffb7cc7bfd5fe51b17aa358`  
		Last Modified: Tue, 17 Feb 2026 20:21:47 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68899779c7d8ea5780e489e1adce8a4deb591e9bb3bf37a5d8f6bc0d5ae33b0`  
		Last Modified: Tue, 17 Feb 2026 20:21:55 GMT  
		Size: 149.9 MB (149858929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e206e1fd0d7044322ee6c9fe15096ef0aa13189f275bfc1648ad6571f991be`  
		Last Modified: Tue, 17 Feb 2026 20:21:59 GMT  
		Size: 340.9 MB (340850804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e47f443cb02e1b298c93b036ad5311f2f31a2516c301c9e4ce63bb9187df06`  
		Last Modified: Tue, 17 Feb 2026 20:21:55 GMT  
		Size: 137.0 MB (137019692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb153e8cfc8ac375be0bffbbcc72addd842f67640475cbdd7cbde0abc744367c`  
		Last Modified: Tue, 17 Feb 2026 20:21:49 GMT  
		Size: 25.6 KB (25601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:d68bf68c548c046ba07e3486d5cf49c5b1a05d1c91f0417557a1244d5e0fb0d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9052613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c6131977a68497306d07efe8219cb4cbb2c8461d54c02e125d34d1c60e33d66`

```dockerfile
```

-	Layers:
	-	`sha256:e3a3c3e5745d14c20f9d370bc1fa88b24a9ec10a114210fe923d9a9dd4ff416b`  
		Last Modified: Tue, 17 Feb 2026 20:21:49 GMT  
		Size: 9.0 MB (9018673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd79690c701ccff04c57cd6e1994d048299ec836102c9ee6140ea20ed03a232f`  
		Last Modified: Tue, 17 Feb 2026 20:21:48 GMT  
		Size: 33.9 KB (33940 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e9a37b11941f5839839f5bd657d722d8d1f875942fe851385aeecb063398f5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.7 MB (626726504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e62dab3af47a173c72fa3d8b5fc6996b26c248d2639fbc0cf5a18130ccf4878`
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
# Tue, 17 Feb 2026 20:19:46 GMT
CMD ["gradle"]
# Tue, 17 Feb 2026 20:19:46 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 17 Feb 2026 20:19:46 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 17 Feb 2026 20:19:46 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 17 Feb 2026 20:19:46 GMT
WORKDIR /home/gradle
# Tue, 17 Feb 2026 20:20:27 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 17 Feb 2026 20:20:27 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 17 Feb 2026 20:20:27 GMT
ENV JAVA_VERSION=25.0.1
# Tue, 17 Feb 2026 20:20:44 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=01e39fe1a87f28b842a3e4e3b77be9b544dca3a58fa6e93b924a6106c8bac7fb     && GRAALVM_AARCH64_DOWNLOAD_SHA256=7aa0b9935a80e67f37c6025678393dbd123bb6f2226811decbc1a13093fc8ae2     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 17 Feb 2026 20:20:44 GMT
ENV GRADLE_VERSION=9.3.1
# Tue, 17 Feb 2026 20:20:44 GMT
ARG GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
# Tue, 17 Feb 2026 20:20:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 17 Feb 2026 20:20:46 GMT
USER gradle
# Tue, 17 Feb 2026 20:20:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 17 Feb 2026 20:20:47 GMT
USER root
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb0495d2354c9ff15dad7483db2eb32eb1ee75283d2e7b6856ba8ead836a038`  
		Last Modified: Tue, 17 Feb 2026 20:21:22 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf189ace45b65a1f692eb99f78552ef8305d6bd5ef5eafec1a68b5642cd7119`  
		Last Modified: Tue, 17 Feb 2026 20:21:29 GMT  
		Size: 144.9 MB (144922320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a17bf94d84158ddcf32efcce4722c71430d0eaef926c371ee7e66ad7d2114b`  
		Last Modified: Tue, 17 Feb 2026 20:21:32 GMT  
		Size: 315.9 MB (315888714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c5d6799a53a112cfd85ce306f38f75ef068721a9585348dcccbbfd18c8a462`  
		Last Modified: Tue, 17 Feb 2026 20:21:29 GMT  
		Size: 137.0 MB (137019692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315ca9281aade6240b529c2f7c7e63071b7dab4da2c495b44c3bc2dd74221e67`  
		Last Modified: Tue, 17 Feb 2026 20:21:24 GMT  
		Size: 29.3 KB (29341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:50f7dbbd4812a9dad60d49242f6e2bfbd893dff79625c8f36544eab27392fbf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9048153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27204f12fdf9c8b56f797f42a636d7bf2627c6f8cf51810eff977b2ab3a1801b`

```dockerfile
```

-	Layers:
	-	`sha256:e4f5387e5222b4beca37671059a63931d44395ec7a9f22e0861d1b991957498a`  
		Last Modified: Tue, 17 Feb 2026 20:21:23 GMT  
		Size: 9.0 MB (9013809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7bbce7d9858660ddc3cb4e6b1314194ce2447ae96ab559735f12c40f9e3bead`  
		Last Modified: Tue, 17 Feb 2026 20:21:22 GMT  
		Size: 34.3 KB (34344 bytes)  
		MIME: application/vnd.in-toto+json
