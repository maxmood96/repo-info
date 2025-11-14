## `gradle:8-graal`

```console
$ docker pull gradle@sha256:1d5c42d2de826f01241ae81d2a411bb6de3b3b111bbc58c4d5ff725a17483bdd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-graal` - linux; amd64

```console
$ docker pull gradle@sha256:6172e7f49fc40e742ca4014eaf814c19b7b08ac7a1e137ef3ce74bfb4a83b289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.8 MB (605800311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3adcd50cda54de16e0de24f2267aa157b7372a908f02effbdb6741fffb01a653`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:23:01 GMT
CMD ["gradle"]
# Thu, 13 Nov 2025 23:23:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 13 Nov 2025 23:23:01 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 13 Nov 2025 23:23:01 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 13 Nov 2025 23:23:01 GMT
WORKDIR /home/gradle
# Thu, 13 Nov 2025 23:23:33 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 13 Nov 2025 23:23:33 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 13 Nov 2025 23:23:33 GMT
ENV JAVA_VERSION=21.0.2
# Thu, 13 Nov 2025 23:23:41 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Thu, 13 Nov 2025 23:23:41 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 13 Nov 2025 23:23:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 13 Nov 2025 23:23:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 13 Nov 2025 23:23:43 GMT
USER gradle
# Thu, 13 Nov 2025 23:23:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 13 Nov 2025 23:23:44 GMT
USER root
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1004a179a3a783d655fed04d373f630b3f835027796ec9c6e0e9f77228a0c52`  
		Last Modified: Thu, 13 Nov 2025 23:24:34 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba84c62032a3f3d4360a84520edcfd0338d9be1ee4614a0f12329005aeffacb4`  
		Last Modified: Thu, 13 Nov 2025 23:24:26 GMT  
		Size: 148.6 MB (148638146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7794d029b527fb861aed2e6fabad1e0063df1e2efb57d8a29c71fb3546a03648`  
		Last Modified: Thu, 13 Nov 2025 23:24:28 GMT  
		Size: 290.0 MB (289986079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a18842a1bb9f15e71609ced8a7daa3fa729bd82c47dae2d3453ba6d07e28a2`  
		Last Modified: Thu, 13 Nov 2025 23:24:25 GMT  
		Size: 137.4 MB (137395174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2e0c6b950278e19f44c8e36edb97263d70583b04d01216373a378fb6ae6a3e`  
		Last Modified: Thu, 13 Nov 2025 23:24:34 GMT  
		Size: 54.9 KB (54905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:17528e2f9632730857cc432c750f4eda479582f2b1c7cfaad2147526fac1b4cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9021712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2da25f133c6fc6247574df75658b5274b7e43f398a21ea8bc9d295e8100f115`

```dockerfile
```

-	Layers:
	-	`sha256:1a34bf7fa222f452b5a09758f7ee2610f32cf54f6b0c0afe3f44835f016c60da`  
		Last Modified: Fri, 14 Nov 2025 03:25:48 GMT  
		Size: 9.0 MB (8989717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aeec0321a7867cf81e6f13fa7df34c7889e3c91a0259c003a930b9014c2f02b`  
		Last Modified: Fri, 14 Nov 2025 03:25:49 GMT  
		Size: 32.0 KB (31995 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:290efa9ed673d8e453ee28d88260973bf85c6bfe8d8f9eb83c126d0753909eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.7 MB (591727197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc6213e5315028c69b8a5ae70572825b47fb95e4f08f3d4765f533e128b5f71`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:22:44 GMT
CMD ["gradle"]
# Thu, 13 Nov 2025 23:22:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 13 Nov 2025 23:22:44 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 13 Nov 2025 23:22:44 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 13 Nov 2025 23:22:44 GMT
WORKDIR /home/gradle
# Thu, 13 Nov 2025 23:23:16 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 13 Nov 2025 23:23:16 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 13 Nov 2025 23:23:16 GMT
ENV JAVA_VERSION=21.0.2
# Thu, 13 Nov 2025 23:23:25 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Thu, 13 Nov 2025 23:23:25 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 13 Nov 2025 23:23:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 13 Nov 2025 23:23:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 13 Nov 2025 23:23:27 GMT
USER gradle
# Thu, 13 Nov 2025 23:23:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 13 Nov 2025 23:23:27 GMT
USER root
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37ecb2558a223e01cc80cef6d269f724299727bd0edae45620ce7273a8244fd`  
		Last Modified: Thu, 13 Nov 2025 23:24:15 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5df72c29bf0f441a05668fb3abf09c37046924743c109ea710efdbde1e9ce9`  
		Last Modified: Thu, 13 Nov 2025 23:24:07 GMT  
		Size: 143.7 MB (143742847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586f9f5c008975ab250a89752e27b2c1697a1eb337a6edbcf7109fc8d6f42138`  
		Last Modified: Thu, 13 Nov 2025 23:24:11 GMT  
		Size: 281.7 MB (281666351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e657608ba1b0f516e36152b20667c898d37b3cb41f0ae641e435c9fcd8facaa1`  
		Last Modified: Thu, 13 Nov 2025 23:24:07 GMT  
		Size: 137.4 MB (137395197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06dc2f1775fe75e7a1f3070e4082f8b33c30c214d40e3d5dd61efb0e3b8a047`  
		Last Modified: Thu, 13 Nov 2025 23:24:15 GMT  
		Size: 59.5 KB (59525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:3f1f00e5bf150c0df856bac49f8504dc0a30579d82c4def0aaec35dd3f16f7d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9017749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932c75ec8024b2a970851e2c2836fdf467cb9c7e84842a0631f1a2d55e3cc918`

```dockerfile
```

-	Layers:
	-	`sha256:c4ab6abcc894ef84a63cddf49a6dcfb81a5311cf96c6b83bed869ad6a662996d`  
		Last Modified: Fri, 14 Nov 2025 03:25:56 GMT  
		Size: 9.0 MB (8985422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d4ed31101cbf7b1b415e6c38f75c7258e096fd9c45a8d414e80bdd5ee7340ce`  
		Last Modified: Fri, 14 Nov 2025 03:25:56 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.in-toto+json
