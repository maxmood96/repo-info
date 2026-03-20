## `gradle:jdk25-graal`

```console
$ docker pull gradle@sha256:70f4ce9f8666d95d4fc1c8284a8b2f3656dd75cbed1fd9eb43e0a88fdc415d5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk25-graal` - linux; amd64

```console
$ docker pull gradle@sha256:655e1a56b6389510cbfbfadfb0dfbd0fd009e00d90b61cedda28b0328ec64d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.3 MB (657281178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4239a8148f425c866ec3b2f032653d3fe5ad1af4191a75f8375b1849a918da`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 17:09:54 GMT
CMD ["gradle"]
# Fri, 20 Mar 2026 17:09:54 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Mar 2026 17:09:54 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Mar 2026 17:09:54 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Mar 2026 17:09:54 GMT
WORKDIR /home/gradle
# Fri, 20 Mar 2026 17:10:30 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 20 Mar 2026 17:10:30 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 20 Mar 2026 17:10:30 GMT
ENV JAVA_VERSION=25.0.2
# Fri, 20 Mar 2026 17:10:44 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e0be791c8fda4d03b6b0a0cb824fef3149736170057b3a515252b44419606af0     && GRAALVM_AARCH64_DOWNLOAD_SHA256=b4580d9f223d0a4b3a1757e58b18ff4c1db950e67e105fc5cb741457d2384a71     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Fri, 20 Mar 2026 17:10:44 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 20 Mar 2026 17:10:44 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 20 Mar 2026 17:10:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Mar 2026 17:10:46 GMT
USER gradle
# Fri, 20 Mar 2026 17:10:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 20 Mar 2026 17:10:46 GMT
USER root
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d6b3bdd1cb2d79f6657e659f8cab0aaed6c4167005c1acb340e5f2f9c4ce39`  
		Last Modified: Fri, 20 Mar 2026 17:11:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9808e128fc1102ee608a674434146d62980ae246e22d658066afe92a8beb42`  
		Last Modified: Fri, 20 Mar 2026 17:11:31 GMT  
		Size: 148.8 MB (148820226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8ca652d7919923916a3daa3fe272dd3ba4ee783203cb4a29216dc7fbaeb6c4`  
		Last Modified: Fri, 20 Mar 2026 17:11:35 GMT  
		Size: 340.9 MB (340893700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9044f96ce38cb6c8ee29f2006304fe2bfb6bb0466f10b4b7241c09846fa13e0`  
		Last Modified: Fri, 20 Mar 2026 17:11:30 GMT  
		Size: 137.8 MB (137808331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fce40bb200c738d260fd3d5bfb7c4514f9dc28e0dd2cc10021603588ed533ad`  
		Last Modified: Fri, 20 Mar 2026 17:11:23 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:64a220e8df2ab4bb93c38f705c47097c5082a9f8ada3529135be5e17b5e5e3a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9055832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515fb1f5f7c4c9787139dccf129bca2b39c8f68dd143d91910f439b617a01e48`

```dockerfile
```

-	Layers:
	-	`sha256:c82533009741c9c298690f98f4526230a3b7c7b435978e672604c578ca6c0d27`  
		Last Modified: Fri, 20 Mar 2026 17:11:22 GMT  
		Size: 9.0 MB (9021892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39e5ab870968ff9e762439378ec9e9d8f2dacd85315f6ed6b25e943c3592603f`  
		Last Modified: Fri, 20 Mar 2026 17:11:22 GMT  
		Size: 33.9 KB (33940 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk25-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:6dd789b2b8804de0ec54c975ba83901ba735f0e7b39aa2652291560db58ffb6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.6 MB (626614550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50da5519fb6c78aca2d47ec7c46310498489fb244c1c15db7c8bf4397d94318`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 17:09:52 GMT
CMD ["gradle"]
# Fri, 20 Mar 2026 17:09:52 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Mar 2026 17:09:52 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Mar 2026 17:09:52 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Mar 2026 17:09:52 GMT
WORKDIR /home/gradle
# Fri, 20 Mar 2026 17:10:27 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 20 Mar 2026 17:10:27 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 20 Mar 2026 17:10:27 GMT
ENV JAVA_VERSION=25.0.2
# Fri, 20 Mar 2026 17:10:39 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e0be791c8fda4d03b6b0a0cb824fef3149736170057b3a515252b44419606af0     && GRAALVM_AARCH64_DOWNLOAD_SHA256=b4580d9f223d0a4b3a1757e58b18ff4c1db950e67e105fc5cb741457d2384a71     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Fri, 20 Mar 2026 17:10:39 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 20 Mar 2026 17:10:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 20 Mar 2026 17:10:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Mar 2026 17:10:41 GMT
USER gradle
# Fri, 20 Mar 2026 17:10:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 20 Mar 2026 17:10:42 GMT
USER root
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b7012eda4dd18be7c2cafb4bbd51a068f5f79d1181315423c45af83c9bf885`  
		Last Modified: Fri, 20 Mar 2026 17:11:18 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049312a36846f089f2296c97d1f071022193b8bc5425455839860466b05520e3`  
		Last Modified: Fri, 20 Mar 2026 17:11:25 GMT  
		Size: 143.9 MB (143919044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d50c3c9d338ad140d31f98eed8d2c7105f9f183b8c072725d96bafb50faf83`  
		Last Modified: Fri, 20 Mar 2026 17:11:28 GMT  
		Size: 316.0 MB (315986809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1102c8f1ea0d89c7b23ca10ca6ab9556591623166aa10a4ece048e4686b37398`  
		Last Modified: Fri, 20 Mar 2026 17:11:25 GMT  
		Size: 137.8 MB (137808331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844c1d05785c06ffa14e0f7db9f2d0f61e21cd68bbf23f117bbc2e83f9b815cc`  
		Last Modified: Fri, 20 Mar 2026 17:11:19 GMT  
		Size: 29.3 KB (29340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:cb1857f950fd694d39c0fb7eb2fcced3d457aa3d9c37e3d4803112210d1e5001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9051371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:434ec88c28b90147700f26579c68b8a67a6f7968b295416dfb19c88c278c471c`

```dockerfile
```

-	Layers:
	-	`sha256:ed29c58d606a8f422d6f1320f8d1a34f2c2c4ccb521071339ece8a6363b7f29d`  
		Last Modified: Fri, 20 Mar 2026 17:11:19 GMT  
		Size: 9.0 MB (9017028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02f05c2245ebd5be0e4f3066532a361e00b618afeef12555deedee75e65723bc`  
		Last Modified: Fri, 20 Mar 2026 17:11:18 GMT  
		Size: 34.3 KB (34343 bytes)  
		MIME: application/vnd.in-toto+json
