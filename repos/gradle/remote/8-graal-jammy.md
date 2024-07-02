## `gradle:8-graal-jammy`

```console
$ docker pull gradle@sha256:9d75614cf384676e012e223e17af7a0c0e37596be2698f08531f8e78975f0799
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:601036f3913abe0461bb93cc17289050398d9e7cfaa73b1cd69922fcebf5710c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.1 MB (585118305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf65508678939e6b6992938ec5738b6b1410cad0271e6a6dca0d213d15d743b0`
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
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 16 Jun 2024 03:23:28 GMT
WORKDIR /home/gradle
# Sun, 16 Jun 2024 03:23:28 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sun, 16 Jun 2024 03:23:28 GMT
ENV JAVA_VERSION=17.0.9
# Sun, 16 Jun 2024 03:23:28 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
ENV GRADLE_VERSION=8.8
# Sun, 16 Jun 2024 03:23:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
# Sun, 16 Jun 2024 03:23:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
USER gradle
# Sun, 16 Jun 2024 03:23:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
USER root
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5aad3d76fcae83ced133988218ee3582afc6e8f4ac5b71a99b84bd311589381`  
		Last Modified: Tue, 02 Jul 2024 03:18:39 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b2f2b4ae5a88f7c43a457013da7fc076ef763a0c2be91cd559627c591a44e0`  
		Last Modified: Tue, 02 Jul 2024 03:18:41 GMT  
		Size: 126.4 MB (126397563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3922928a97560383eedd203e84fd70aa53ca1e634cd169ecb84835eac966dbb3`  
		Last Modified: Tue, 02 Jul 2024 03:18:43 GMT  
		Size: 291.1 MB (291064897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35033a6ca4930e625e841832c6ba5f2d31c085c8111856694f3106a01666e747`  
		Last Modified: Tue, 02 Jul 2024 03:18:41 GMT  
		Size: 138.1 MB (138062553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01fe4bb073845e8146d420c58242eb6b7bd58abf34990e43421b8f90c1d112bd`  
		Last Modified: Tue, 02 Jul 2024 03:18:40 GMT  
		Size: 54.9 KB (54898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:91f914d2fa145b822f80d26b0b9144378acde564b7e45a0a68412018ad4d7537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8613607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74890a4445f12a0dc94723e39d79e716e2e071c47d434d9156cd51e7896e2b0d`

```dockerfile
```

-	Layers:
	-	`sha256:49a4cf45d2c54e3a45151d85597a9326b9e515c572d37a0686e110b1cdb7c547`  
		Last Modified: Tue, 02 Jul 2024 03:18:39 GMT  
		Size: 8.6 MB (8581862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34a660e4c0fa99d34b97438d5dcf451f3c72023c3f530e9a76f275ffc58d7d20`  
		Last Modified: Tue, 02 Jul 2024 03:18:39 GMT  
		Size: 31.7 KB (31745 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:7da3f2aab413e60fa9d8e53056f6cae9dc2a4065ba05b42b12874eacb0032b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.5 MB (571479000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376804ef4f0a51aef8b38a38eb9e1c55febf0eff15d41633faa73aa80bdfaa95`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 01 Jun 2024 15:03:05 GMT
ARG RELEASE
# Sat, 01 Jun 2024 15:03:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Jun 2024 15:03:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Jun 2024 15:03:05 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Jun 2024 15:03:05 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Sat, 01 Jun 2024 15:03:05 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 15:03:05 GMT
CMD ["gradle"]
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 01 Jun 2024 15:03:05 GMT
WORKDIR /home/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sat, 01 Jun 2024 15:03:05 GMT
ENV JAVA_VERSION=17.0.9
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_VERSION=8.8
# Sat, 01 Jun 2024 15:03:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
# Sat, 01 Jun 2024 15:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
USER gradle
# Sat, 01 Jun 2024 15:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
USER root
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0c2d4156ffddbd844819b51109946f8544c2ac757006410f452d87bc1c1a14`  
		Last Modified: Wed, 05 Jun 2024 15:12:17 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a9c0a832f43a53b8f39efce3bf6b8ee2e242fadb49209d26609c59a606c74a`  
		Last Modified: Wed, 05 Jun 2024 15:12:20 GMT  
		Size: 122.5 MB (122488831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde89fbcc21c5e9fb59da1acbc46e408e4143a0306954f4ea35e50936be7475f`  
		Last Modified: Wed, 05 Jun 2024 15:12:23 GMT  
		Size: 283.5 MB (283501935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8061093a8104592d6b076e6faf5c717223510fb64cf5c0beb561d83f07974d4c`  
		Last Modified: Wed, 05 Jun 2024 15:12:21 GMT  
		Size: 138.1 MB (138062591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91414908165882e463e068196232dedda0964cad3cc30e2d954113c74bf59cf`  
		Last Modified: Wed, 05 Jun 2024 15:12:18 GMT  
		Size: 59.5 KB (59517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:bdc09ac755894d8a78c65ce3ec90afeba9dfc6ed15b3061f9df691d0c4c234d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8609324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90dd5f09d7c4b9b56e57ff210c1c780dbe0727f692a17e2d747f29ab368985e`

```dockerfile
```

-	Layers:
	-	`sha256:8d4d1259cd2af0e822ebc07f10b763e18e40bd1277c85fbce24d2e92ccd3831d`  
		Last Modified: Wed, 05 Jun 2024 15:12:17 GMT  
		Size: 8.6 MB (8577087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:535abb48174416e8a2a288c2011c01fa5200a5d6c619fe00d6b155bbf8287cc3`  
		Last Modified: Wed, 05 Jun 2024 15:12:17 GMT  
		Size: 32.2 KB (32237 bytes)  
		MIME: application/vnd.in-toto+json
