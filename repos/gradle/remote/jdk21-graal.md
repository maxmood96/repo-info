## `gradle:jdk21-graal`

```console
$ docker pull gradle@sha256:e1a9fc10a34a6b43026998bb494e9d30fb18dd6751767b6c3aad8f004f6f1747
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk21-graal` - linux; amd64

```console
$ docker pull gradle@sha256:8e5a22c6f184d913d2605a3f2efa6ac6272f655ef233d2709296429c836d3523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.3 MB (608312811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71197925747cd840c08cd77832cee3a1877e5b085d93674bfdf0392300c8306`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 20:47:52 GMT
CMD ["gradle"]
# Tue, 12 May 2026 20:47:52 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 20:47:52 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 20:47:52 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 20:47:52 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 20:48:19 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 12 May 2026 20:48:19 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 12 May 2026 20:48:19 GMT
ENV JAVA_VERSION=21.0.2
# Tue, 12 May 2026 20:48:29 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 12 May 2026 20:48:29 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 12 May 2026 20:48:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 12 May 2026 20:48:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 20:48:32 GMT
USER gradle
# Tue, 12 May 2026 20:48:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 20:48:32 GMT
USER root
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f55f56314b61ccf109ca3c1e2af043ad679b701386dc5c6bd02efac23c8ef35`  
		Last Modified: Tue, 12 May 2026 20:49:06 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9143537f605454043a458f9af6286e21cd690ed5eb3c678ca3e462b2043f3a64`  
		Last Modified: Tue, 12 May 2026 20:49:24 GMT  
		Size: 148.3 MB (148329222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d185d1a38785ef27076e574d97ef7ee4bb9701fcdc5243474c22b2dfd9e0a99f`  
		Last Modified: Tue, 12 May 2026 20:49:30 GMT  
		Size: 290.0 MB (289986707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d23e32312155f8b4a8592963bb7fd78f1e026539a43a0fa076f04400e4bd3b`  
		Last Modified: Tue, 12 May 2026 20:49:24 GMT  
		Size: 140.2 MB (140236983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb011fa47c8f16b8308d1a21fbde7c44bcc843b9b10d3b8b65842124ab22b90`  
		Last Modified: Tue, 12 May 2026 20:49:09 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:572209e72e258b58e4d0c39abb3a9c6e5979cd21606533f1d12103fc06bd5458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9031743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ffb9fdd076a8784cbd48800a081e9b8216777bf0608903472b0ce394f9d717`

```dockerfile
```

-	Layers:
	-	`sha256:4c999b807f5b11e84aef3fb8fa12537aac2e7bd5173acd863394bf72670f811b`  
		Last Modified: Tue, 12 May 2026 20:49:07 GMT  
		Size: 9.0 MB (9002795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:089565c2c559a5bb9bad2a0b7b973366428afca57c133666cb1b40d62bfa7669`  
		Last Modified: Tue, 12 May 2026 20:49:07 GMT  
		Size: 28.9 KB (28948 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b0d02dca61121d284b9c66a351993437b4453fe4050f9ee0d0a7ec0438d94130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.3 MB (594252963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fc5bdcdf1838e52678b94cdc852cf5cb361b9cb4fc64d3a6018a34b69dc5cd`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 20:48:21 GMT
CMD ["gradle"]
# Tue, 12 May 2026 20:48:21 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 20:48:21 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 20:48:21 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 20:48:21 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 20:48:58 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 12 May 2026 20:48:58 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 12 May 2026 20:48:58 GMT
ENV JAVA_VERSION=21.0.2
# Tue, 12 May 2026 20:49:07 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 12 May 2026 20:49:07 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 12 May 2026 20:49:07 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 12 May 2026 20:49:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 20:49:10 GMT
USER gradle
# Tue, 12 May 2026 20:49:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 20:49:10 GMT
USER root
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a336dd7eec1228b6bd6b47a8906b30b17ab1ef28aea6a424cb63e4e7d5f49e76`  
		Last Modified: Tue, 12 May 2026 20:49:43 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc4e8f48e53b5e8a9e28e1a59952efbaa6e6e97795b8a60292898379010e20a`  
		Last Modified: Tue, 12 May 2026 20:49:51 GMT  
		Size: 143.4 MB (143443361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37099449cd453a23cfe0ae2d52a6028f0e38f3108992a5046f1bad8799aeb0f9`  
		Last Modified: Tue, 12 May 2026 20:49:55 GMT  
		Size: 281.7 MB (281666179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84b0c7a71a9338e08345a66e3d1b5c25348321e4285a4dffc5b6eed8941de13`  
		Last Modified: Tue, 12 May 2026 20:49:52 GMT  
		Size: 140.2 MB (140236984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c2f3dbe6a4f058d7eac1cacee6d659faeddd92922cc5a86d88f946d5603177`  
		Last Modified: Tue, 12 May 2026 20:49:45 GMT  
		Size: 29.3 KB (29335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:2141c232ed2af473c221bf4d03257a650c0ff8437e7e88cafcadd68dd723f31a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9027535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4163f15bcb1d3c17a46cfc16fd645cb66b6b1e13a0b6061966d8ec6fb3653a46`

```dockerfile
```

-	Layers:
	-	`sha256:a6d6c92a9dd1fff8a34218bc9a86c0502c09f7b6230ed6f48d5bf66c460e91d9`  
		Last Modified: Tue, 12 May 2026 20:49:44 GMT  
		Size: 9.0 MB (8998376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dd45bb53450ea933fd5f721e88e5a0bf5ff5f35af33a530eb8ab3bf2b1e0714`  
		Last Modified: Tue, 12 May 2026 20:49:43 GMT  
		Size: 29.2 KB (29159 bytes)  
		MIME: application/vnd.in-toto+json
