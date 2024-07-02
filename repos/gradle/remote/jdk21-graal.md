## `gradle:jdk21-graal`

```console
$ docker pull gradle@sha256:c00d79fdaf209f768e5ead78e9cf1ca33e5373b3f4ec765e5ebd20bdef269ae9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk21-graal` - linux; amd64

```console
$ docker pull gradle@sha256:27f4fe9f4926940bd3132c382dc0748d9ec8307acf9a5de318d23a15a4c687f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.0 MB (584041157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2634eecede8e158938e0f9d100d14657b416579c5fcfded7339e1bf79104c55`
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
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 16 Jun 2024 03:23:28 GMT
WORKDIR /home/gradle
# Sun, 16 Jun 2024 03:23:28 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sun, 16 Jun 2024 03:23:28 GMT
ENV JAVA_VERSION=21.0.2
# Sun, 16 Jun 2024 03:23:28 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
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
	-	`sha256:01053f5d2fa23dfb63c1e05fe20ce874fe50e8fc392c92eaf846a60cccbe16b2`  
		Last Modified: Tue, 02 Jul 2024 03:19:00 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e73f57e897594f1442023302a81d292680b76fee9e06ffbabd9852afe7eb543`  
		Last Modified: Tue, 02 Jul 2024 03:19:04 GMT  
		Size: 126.4 MB (126398605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4859b6ad3938417638ea6ffd5720443e57a0e973f3619daba9477d361fb923e8`  
		Last Modified: Tue, 02 Jul 2024 03:19:06 GMT  
		Size: 290.0 MB (289986707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6a16d95817cd8af209e0c90a40739be7a1f3bc272cceb88af02f5a8b99363b`  
		Last Modified: Tue, 02 Jul 2024 03:19:04 GMT  
		Size: 138.1 MB (138062554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d907db13906f5a545ab1103865fd2003e9c5cb88742f1390c68440558bfc2e01`  
		Last Modified: Tue, 02 Jul 2024 03:19:01 GMT  
		Size: 54.9 KB (54897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:93534d2df1c170f7a25a5b7b76b2841d1f0b516d6dec6e37ae77abd83113246d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8601436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c92228cb0090801453fff7c78a54007d1394bc8cb5a7d91f1c2556fb1256aa`

```dockerfile
```

-	Layers:
	-	`sha256:0036cb04d533e6696107ddd1ebd4aa5c466ebf96c0023d083e39792211e6f64e`  
		Last Modified: Tue, 02 Jul 2024 03:19:00 GMT  
		Size: 8.6 MB (8574804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da6b7f47c4d6fe742e2ac136fe341a689b2898972f889d6b4583f28a448634b0`  
		Last Modified: Tue, 02 Jul 2024 03:19:00 GMT  
		Size: 26.6 KB (26632 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:a9325464d96e7ab3ea4c1b2a643f8d4666749b7ef0a0e3a9ce9a69c489d10a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.6 MB (569645327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c3cf1aa380b7ab8ecc51b843f227152c28a30adf8d8515175ddf58b82e3641`
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
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 01 Jun 2024 15:03:05 GMT
WORKDIR /home/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sat, 01 Jun 2024 15:03:05 GMT
ENV JAVA_VERSION=21.0.2
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
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
	-	`sha256:d46d43080d0d3991abc2fe94f4cf3660d1cddfb337fbccc3cc5df71c1abbf783`  
		Last Modified: Wed, 05 Jun 2024 15:14:42 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc27f7833e808a36645df06c009c68bc319c5c49bb454dce5ae344722e28e2b2`  
		Last Modified: Wed, 05 Jun 2024 15:14:45 GMT  
		Size: 122.5 MB (122490763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d546ebdebcc60c34f1d15e6ba4a0d3f9c7b1e7d703fbd17c718a7864bc8d05`  
		Last Modified: Wed, 05 Jun 2024 15:14:49 GMT  
		Size: 281.7 MB (281666325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410c7b0575f118c8c58eb6be108a7175e72cccf5235648cdabc91327193948d8`  
		Last Modified: Wed, 05 Jun 2024 15:14:47 GMT  
		Size: 138.1 MB (138062591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27737763bc672c1bc232723653f32b7a6b5d67f5042a1c76cd1fd9543c850156`  
		Last Modified: Wed, 05 Jun 2024 15:14:43 GMT  
		Size: 59.5 KB (59519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:6a26c0a15398a2ceb1b8a4160929c64b5c21b51fc75f8572baee46ec99ae38ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8596773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033411d2ecbea13b8975dd5aa95629d91b1693ff34a2b099ef6ebae8108ba2d5`

```dockerfile
```

-	Layers:
	-	`sha256:07766a3fffec0431953ee21d9bc436b3a1a7c2d145c19bfbcea4fdda7cf73a28`  
		Last Modified: Wed, 05 Jun 2024 15:14:43 GMT  
		Size: 8.6 MB (8569841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cfffda7934de04928e0f873312e019041bc1a489d5daac66358e18336bee451`  
		Last Modified: Wed, 05 Jun 2024 15:14:42 GMT  
		Size: 26.9 KB (26932 bytes)  
		MIME: application/vnd.in-toto+json
