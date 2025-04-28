## `gradle:jdk24-graal-noble`

```console
$ docker pull gradle@sha256:8cd542bf523e106616216f1a4f73fe7297812e4530fc9bd504a8d0b8eb6254a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk24-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:a04bf1925f45dddd980d765eea5e618da4d38e44db73989e83a4d5b50f5339ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.1 MB (654091909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8809fa4b6ed114ffad5d43245fcabf5bbfc9f604b23e8ebb3593a9c01566cf`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
CMD ["/bin/bash"]
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["gradle"]
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 26 Apr 2025 01:26:29 GMT
WORKDIR /home/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_VERSION=24.0.1
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=d2c544de672e400476a09c8f1da79ecc6b774a9441e234948542c3b3e6a84bde     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a3d1be8fadfb0d3df632252301f79a9b02b47e523da66539d370c62e683d762e     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_VERSION=8.14
# Sat, 26 Apr 2025 01:26:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER gradle
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER root
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef7f4b3a273257903e16292cd70c85e5a1c8f68824568dd48a5c90177023250`  
		Last Modified: Mon, 28 Apr 2025 17:52:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d3e6f78f9314b926284f2cf3ea0a64b0d2789b323a8d10f5afbe47b1f39915`  
		Last Modified: Mon, 28 Apr 2025 17:52:51 GMT  
		Size: 150.8 MB (150812502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690372354dde77ead7eef435e3611944c1112a1640cffc6b41e3e8c20c6b9a1e`  
		Last Modified: Mon, 28 Apr 2025 17:52:55 GMT  
		Size: 336.1 MB (336110931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c67bccc864a1b114b8e14c508f7f8834e3c00755b576a5f3b1722bda46a9f6`  
		Last Modified: Mon, 28 Apr 2025 17:52:53 GMT  
		Size: 137.4 MB (137394599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daafd87429dabcc3ac46aefc37eff75ea1ad7d411f2dbce8c097f00731e1367`  
		Last Modified: Mon, 28 Apr 2025 17:52:50 GMT  
		Size: 54.9 KB (54904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk24-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:99932e24e8531c269d3feec76f9767ebbe569b549c4420c2f27a0786afac85c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8779886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0001566b8eb90e9d717ad4e4de39e3b575a66c27abbceed1f770ef579d0bc8ce`

```dockerfile
```

-	Layers:
	-	`sha256:81fccb22e2560293c784a29cf6244e89aa9484f1490115b62dd23f05859e1ee8`  
		Last Modified: Mon, 28 Apr 2025 17:52:49 GMT  
		Size: 8.8 MB (8752718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b42a16c1252d78d311655f00eb30da00fc2efc2e8aac8c500efb0ef57a785914`  
		Last Modified: Mon, 28 Apr 2025 17:52:49 GMT  
		Size: 27.2 KB (27168 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk24-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b43e524ebf57ef6d9440b9ea73e6e1a6004b11828b563f41b808d938bd520fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.1 MB (620055769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd303b7b9c1c912fd6448af6cb6bd8982bb8f2adf88de56911ba02641a84b00a`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
CMD ["/bin/bash"]
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["gradle"]
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 26 Apr 2025 01:26:29 GMT
WORKDIR /home/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_VERSION=24.0.1
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=d2c544de672e400476a09c8f1da79ecc6b774a9441e234948542c3b3e6a84bde     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a3d1be8fadfb0d3df632252301f79a9b02b47e523da66539d370c62e683d762e     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_VERSION=8.14
# Sat, 26 Apr 2025 01:26:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER gradle
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER root
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed6313a879343298340f8fda88aeb55e4f1abdf10f549074d5590fcd7f3714e`  
		Last Modified: Wed, 09 Apr 2025 07:19:07 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ff5b631fefb8de648c9c7c1b1ec19eab0351b7c80a4874f4920a9279f4e53e`  
		Last Modified: Wed, 09 Apr 2025 07:19:11 GMT  
		Size: 143.5 MB (143463438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff22496c523fb84bfda178a8aab4ca8432d02749f1e96017d6272c1d2fe1ce4a`  
		Last Modified: Mon, 28 Apr 2025 18:14:58 GMT  
		Size: 310.3 MB (310289963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad4d1253117363f71ae24724b5dbf5d4c26f047d799b4ad0cdb4dc494b036e0`  
		Last Modified: Mon, 28 Apr 2025 18:14:46 GMT  
		Size: 137.4 MB (137394558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43c2f1e6fa34e7d2772a0e7a40a9bfdc3ae5cef4ad1c9ce60dab507376bf912`  
		Last Modified: Mon, 28 Apr 2025 18:14:42 GMT  
		Size: 59.5 KB (59533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk24-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:aab56dcbc8e185cf10850a7e59685a28752896608b7ae642dbd12a238b713b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8775307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f57f2a16305b42cafef29c2ea9cbf733208aefb2b0c3107500e571c9e21dba`

```dockerfile
```

-	Layers:
	-	`sha256:047491f5df72d00438bafcde8bf8d072c00b0d73a05617970c372b4d9b7fa7c3`  
		Last Modified: Mon, 28 Apr 2025 18:14:42 GMT  
		Size: 8.7 MB (8747927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:443cb25c69fe78455bc02e4c980815bb24a1abbcf9cf159dfd44e8a82c4bbaa7`  
		Last Modified: Mon, 28 Apr 2025 18:14:42 GMT  
		Size: 27.4 KB (27380 bytes)  
		MIME: application/vnd.in-toto+json
