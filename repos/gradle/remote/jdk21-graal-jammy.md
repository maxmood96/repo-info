## `gradle:jdk21-graal-jammy`

```console
$ docker pull gradle@sha256:e9b977e24217983a19b18f503dd98879acc15570de2c9d12a02e004afb83520c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk21-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:a36711d6bd30ef24d0b4e133510e0352c51341643adfc6aa6eb97c7ad7c2b04a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.2 MB (589236763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f2e1158c05fa5065215668f145abf8d3cfc68f8b5aaeb24b0660b53dbcce7f`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
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
	-	`sha256:a8b1c5f80c2d2a757adc963e3fe2dad0b4d229f83df3349fbb70e4d12dd48822`  
		Last Modified: Sat, 27 Apr 2024 14:45:30 GMT  
		Size: 29.5 MB (29533949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b53fd95efc125f33803859012ce067371d04a189ee36ca339e1878043b8f6e`  
		Last Modified: Mon, 03 Jun 2024 19:01:25 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3f5a87d1d0b7b5637839fd8d3ae4c2618ed6bcf9866665f07b254d4c18cece`  
		Last Modified: Mon, 03 Jun 2024 19:01:30 GMT  
		Size: 131.6 MB (131594279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e817af0d995d70eb2b40d7c321bae57f37fb87a5947d75bd35975b11bf4196`  
		Last Modified: Mon, 03 Jun 2024 19:01:29 GMT  
		Size: 290.0 MB (289986750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7d59bd7c435aa098aaf1fb75706964e32316a8444f974851f45fbc6c43c98e`  
		Last Modified: Mon, 03 Jun 2024 19:01:30 GMT  
		Size: 138.1 MB (138062553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0bcfc448f51c8202508042e3bf59faa2b23b0948b2b1c4ee4e60d42b566607`  
		Last Modified: Mon, 03 Jun 2024 19:01:26 GMT  
		Size: 54.9 KB (54894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:6d9220b83b45d2bd964520eca4b2e881916f6bfc4feaa6a581bd7e2bc80276d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8602475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5f9175e021bc7609a39669283f2a1db7a8b6a9da190a51c557adb7acd202117`

```dockerfile
```

-	Layers:
	-	`sha256:63d3462d8464f07ab23121a527e8a218b4fcf3385bbf35e8032e863db5d20297`  
		Last Modified: Mon, 03 Jun 2024 19:01:25 GMT  
		Size: 8.6 MB (8575892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ade72d9b86549dfb3695a2c4215ca1af629896e174020549f3cf2e18cc3a84a`  
		Last Modified: Mon, 03 Jun 2024 19:01:25 GMT  
		Size: 26.6 KB (26583 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:dc66c576ebde1412c986a1d18abc8a322ccf7eabc0f9534fdaab6581e65d4879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.7 MB (573738609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7453557dfdc7c8bbfc40315ea836532b98601814f24112a7237029b01ed56a9e`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
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
	-	`sha256:d5a2ad729c09fbfdb259ae764f92188efc67a615ffde9bb34a46298d1edf3cd6`  
		Last Modified: Sat, 27 Apr 2024 14:45:36 GMT  
		Size: 27.4 MB (27360530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571e20d7a1c1aa2b4837f90213eb3e17f10dc96e0c6c1bb4d1de619294a51e87`  
		Last Modified: Tue, 04 Jun 2024 05:11:59 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5531e47c70ad654319b358ac532ce5f9563d542e0e8c9cddb015848411a65132`  
		Last Modified: Tue, 04 Jun 2024 05:12:03 GMT  
		Size: 126.6 MB (126585454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a095294037378f6f5b0ff868dc66a0b02f5abf47ecd3a9bbc42d5e580b3c5e40`  
		Last Modified: Tue, 04 Jun 2024 05:12:05 GMT  
		Size: 281.7 MB (281666204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42cecf4a979d00732df2d226ed9835906e4528fd6ee4dde9e4bc4bb2243a2f1d`  
		Last Modified: Tue, 04 Jun 2024 05:12:03 GMT  
		Size: 138.1 MB (138062552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905542d381fc24400fdcddaab020eebd3f3f268e27b04549027443288ffcd117`  
		Last Modified: Tue, 04 Jun 2024 05:12:00 GMT  
		Size: 59.5 KB (59523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:3eebb248d91ec698bcad292e0b6093fb7da1cdc3d460525e0b374a77f128baff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8597865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62430bb98055be21ac6d3accc31b5809d95cf0e2b7d1ebf4d9390174183d1b3`

```dockerfile
```

-	Layers:
	-	`sha256:7121bb94158289084c854fab34b554949caf4c61ff16879f449ac09b39287145`  
		Last Modified: Tue, 04 Jun 2024 05:12:00 GMT  
		Size: 8.6 MB (8570933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50858142e60e0a23c5e25b86ed052ba1bd3dcfb013b90d53eb01dc687e3be2e8`  
		Last Modified: Tue, 04 Jun 2024 05:11:59 GMT  
		Size: 26.9 KB (26932 bytes)  
		MIME: application/vnd.in-toto+json
