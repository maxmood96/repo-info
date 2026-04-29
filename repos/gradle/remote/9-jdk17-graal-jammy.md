## `gradle:9-jdk17-graal-jammy`

```console
$ docker pull gradle@sha256:b8a628f6ddf24c60e5cad45b188de78a7b975f6a7c27d8fb2b9da703a3ccdcc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk17-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:3e3a97c4b51c4d1c391f03cd47e7786c6ee2686d01e0d2263447b619f090ba5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.8 MB (587811967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a94f04a548df7b9d18831cd35214e1c516aa5d65ab60f2490b7405edf5687f`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Tue, 28 Apr 2026 23:31:00 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:31:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:31:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 28 Apr 2026 23:31:00 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:31:00 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:31:29 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 28 Apr 2026 23:31:29 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 28 Apr 2026 23:31:29 GMT
ENV JAVA_VERSION=17.0.9
# Tue, 28 Apr 2026 23:31:38 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Tue, 28 Apr 2026 23:31:38 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:31:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:31:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:31:41 GMT
USER gradle
# Tue, 28 Apr 2026 23:31:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:31:41 GMT
USER root
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6735cb565b40d31d7c192f5c279aac9d986905712cd561cebdb12fb3a7068a`  
		Last Modified: Tue, 28 Apr 2026 23:32:14 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027c9606082552228c1acf93786031f35d0de1095f54514fd4fcf72804a2ea09`  
		Last Modified: Tue, 28 Apr 2026 23:32:25 GMT  
		Size: 126.7 MB (126745337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db92d3ee1835449d4c936d8741fca3956e655530632c90b36a063e9be8148dc4`  
		Last Modified: Tue, 28 Apr 2026 23:32:31 GMT  
		Size: 291.1 MB (291064263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5412ae7e8381c8ec39aac4291b78f552b7d25252c569d923e2f6b21cc46138e`  
		Last Modified: Tue, 28 Apr 2026 23:32:26 GMT  
		Size: 140.2 MB (140235924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b6d764672d8adc2e694841b58c89f8d0d7aa848b1e545f9292b2ecb602b4cf`  
		Last Modified: Tue, 28 Apr 2026 23:32:16 GMT  
		Size: 25.6 KB (25604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:756109ac8d05ef4fb9c13497ed840379c02aae169c679399c0e48a03a52f47ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9445610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e570d54159cbe3a331605b7b1b9abe5994508e787fcfc4a99a20dc761f3ac941`

```dockerfile
```

-	Layers:
	-	`sha256:f625554257d9c6ea78278172848f2903c7922d35033c556be05d7df28e5f2d3d`  
		Last Modified: Tue, 28 Apr 2026 23:32:14 GMT  
		Size: 9.4 MB (9418053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:993e6d0f33e0843d473cb20b128f05f950bf65141da6d921a774e75fbb6d5f72`  
		Last Modified: Tue, 28 Apr 2026 23:32:14 GMT  
		Size: 27.6 KB (27557 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:74d59601ce1d627a6551e1a8f0bb46a132d9045d414c26a7e74fa611ad036eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.3 MB (574261791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229551c0ade3079a64c823619cff128c0a4d63cf7e1963149fa8632f1a4fe31d`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Tue, 28 Apr 2026 23:32:21 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:32:21 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:32:21 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 28 Apr 2026 23:32:21 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:32:21 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:32:55 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 28 Apr 2026 23:32:55 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 28 Apr 2026 23:32:55 GMT
ENV JAVA_VERSION=17.0.9
# Tue, 28 Apr 2026 23:33:05 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Tue, 28 Apr 2026 23:33:05 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:33:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:33:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:33:08 GMT
USER gradle
# Tue, 28 Apr 2026 23:33:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:33:08 GMT
USER root
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bc99378a7e1bb52de71f9ccf35948febe4e0ec2eb501632329be56755e4596`  
		Last Modified: Tue, 28 Apr 2026 23:33:40 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a04271cdf3b4fe445a905b4bed58e25eff7414254cdf6d677dc42715d6b30e`  
		Last Modified: Tue, 28 Apr 2026 23:33:47 GMT  
		Size: 122.9 MB (122883819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e9eed99aa138b4d2c21c11537d717dccdb2e162eec17425c070333ffa3bfee`  
		Last Modified: Tue, 28 Apr 2026 23:33:50 GMT  
		Size: 283.5 MB (283501814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7860a6a67177b8046475aded7bcf23a366848e62ffda2bdeb755b0588d616d`  
		Last Modified: Tue, 28 Apr 2026 23:33:47 GMT  
		Size: 140.2 MB (140235939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c450cc98e7933ca3d1aff915371fd4f3400964fd062c607fd54a545c969b0796`  
		Last Modified: Tue, 28 Apr 2026 23:33:42 GMT  
		Size: 29.3 KB (29334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:d42d64114c6628595aee54f1463f0c25a7a1550e62da7b286957f87943e2af4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9414530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a734e27ab082dd3724cc8dfbd601777a02f9bfdfcae0c7929052ff6e73af9c52`

```dockerfile
```

-	Layers:
	-	`sha256:aaaa4d1c6d41312efea9723342e06895ba6bc882bafaa4a0445d23d20de40968`  
		Last Modified: Tue, 28 Apr 2026 23:33:41 GMT  
		Size: 9.4 MB (9386809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e15898e9de38fa892cd803f8029f09de51c9ac5d626313b3edcc05835eff25dd`  
		Last Modified: Tue, 28 Apr 2026 23:33:40 GMT  
		Size: 27.7 KB (27721 bytes)  
		MIME: application/vnd.in-toto+json
