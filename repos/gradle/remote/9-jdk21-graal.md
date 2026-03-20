## `gradle:9-jdk21-graal`

```console
$ docker pull gradle@sha256:fbbc5d9ee456827b6e7bbe8b174d6c064481c2c186a61d84abde28c70cca49f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk21-graal` - linux; amd64

```console
$ docker pull gradle@sha256:86913f68d8a6b9f55a46be61a60cf0cc6ae28966a0ff980c8b5387571d6d01cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.4 MB (606373244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe1d0fe5606585713bfaa9707d398c464915255d2ea5ee9026006df7084cb39`
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
# Fri, 20 Mar 2026 17:10:33 GMT
CMD ["gradle"]
# Fri, 20 Mar 2026 17:10:33 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Mar 2026 17:10:33 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Mar 2026 17:10:33 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Mar 2026 17:10:33 GMT
WORKDIR /home/gradle
# Fri, 20 Mar 2026 17:11:05 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 20 Mar 2026 17:11:05 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 20 Mar 2026 17:11:05 GMT
ENV JAVA_VERSION=21.0.2
# Fri, 20 Mar 2026 17:11:16 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Fri, 20 Mar 2026 17:11:16 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 20 Mar 2026 17:11:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 20 Mar 2026 17:11:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Mar 2026 17:11:18 GMT
USER gradle
# Fri, 20 Mar 2026 17:11:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 20 Mar 2026 17:11:18 GMT
USER root
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5296016610047d9563be861115bf28075e59bc7035570776dc0175764161099`  
		Last Modified: Fri, 20 Mar 2026 17:11:50 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c555b4adb7eb6491a995d7fd93cc2d2fbe38402ce159a03b0117d6bd9ffd4d17`  
		Last Modified: Fri, 20 Mar 2026 17:11:58 GMT  
		Size: 148.8 MB (148820076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54c8069aa793a61d3ac4f3a89704a02b64b48afba60c51f743c0fcb2a42134d`  
		Last Modified: Fri, 20 Mar 2026 17:12:01 GMT  
		Size: 290.0 MB (289985919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932f75fef0397477fa877142280b6150977f35bbd61385864d50af30e73d2a8d`  
		Last Modified: Fri, 20 Mar 2026 17:11:57 GMT  
		Size: 137.8 MB (137808331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8570c09193e986e0e770f0511d7ecddd6ac172da243a71f7afccaea418a48a`  
		Last Modified: Fri, 20 Mar 2026 17:11:52 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:0379d8fdece2c75169152938f6598a97e819413f5de4b865f17dccb7aea65c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9001398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e8a4daf0e54ca658c84890393c7e05f361fd3bf3871037c91ffb5beaf1371c`

```dockerfile
```

-	Layers:
	-	`sha256:19e57cdbce15ccf0a3d26e1eba8068539378032b18afedf4a87331508ec278e9`  
		Last Modified: Fri, 20 Mar 2026 17:11:51 GMT  
		Size: 9.0 MB (8972450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b62f566254a7fed6cacf33d4fae3554397ffbd7184b79bdf5111533206984c54`  
		Last Modified: Fri, 20 Mar 2026 17:11:50 GMT  
		Size: 28.9 KB (28948 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b76c0b5dc46b5a54fe9efd161231aab3c748572fb4a2a131f79875c346e9b2e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.3 MB (592293217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a4207ad563b7fda66b756a77a6f5edb29931603af18bb6b6e43c14a2e956ff`
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
# Fri, 20 Mar 2026 17:10:20 GMT
CMD ["gradle"]
# Fri, 20 Mar 2026 17:10:20 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Mar 2026 17:10:20 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Mar 2026 17:10:20 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Mar 2026 17:10:20 GMT
WORKDIR /home/gradle
# Fri, 20 Mar 2026 17:10:54 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 20 Mar 2026 17:10:54 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 20 Mar 2026 17:10:54 GMT
ENV JAVA_VERSION=21.0.2
# Fri, 20 Mar 2026 17:11:05 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Fri, 20 Mar 2026 17:11:05 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 20 Mar 2026 17:11:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 20 Mar 2026 17:11:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Mar 2026 17:11:07 GMT
USER gradle
# Fri, 20 Mar 2026 17:11:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 20 Mar 2026 17:11:08 GMT
USER root
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1008e94104a79103dcdbf2c9a5bdf0a7b132ba556aa7bc5e4076ff6056001d7`  
		Last Modified: Fri, 20 Mar 2026 17:11:40 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ce2b71c1896c37a9117e76c2ce8dc07dd3328e69208ad0a81f581ee6aa5c7d`  
		Last Modified: Fri, 20 Mar 2026 17:11:47 GMT  
		Size: 143.9 MB (143918285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11e4e99c4ada47d81ddfee2648b7a0e3b0ea0ad91bed326337076365798c301`  
		Last Modified: Fri, 20 Mar 2026 17:11:50 GMT  
		Size: 281.7 MB (281666230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df446e96c352017659a2e9d6e4d84d911e8a81a364cfc41375a59293def7fbf9`  
		Last Modified: Fri, 20 Mar 2026 17:11:47 GMT  
		Size: 137.8 MB (137808331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c374bfe61c65d9e85071f303e9ea7880485c45d4113880ffaed1a9c7c65e6da4`  
		Last Modified: Fri, 20 Mar 2026 17:11:41 GMT  
		Size: 29.3 KB (29341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:13e9d5d24217bb9ba2e948ea48736c0be02b7d04c0132686f8b73274e5b1320c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8997190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c691d64c8f88efde8ae84b98a4220247c4a4ff5daa1a9652073943568a77a1de`

```dockerfile
```

-	Layers:
	-	`sha256:6bddfc45b9369e3ebbc9b4d6b6d0dfc314370df4025158daeb5aabbc38aaefa0`  
		Last Modified: Fri, 20 Mar 2026 17:11:40 GMT  
		Size: 9.0 MB (8968031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5122af8404686ebbe2d96040e29ce96d16f3eea13b1c7794e3c337df6a163770`  
		Last Modified: Fri, 20 Mar 2026 17:11:40 GMT  
		Size: 29.2 KB (29159 bytes)  
		MIME: application/vnd.in-toto+json
