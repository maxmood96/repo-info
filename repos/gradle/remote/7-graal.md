## `gradle:7-graal`

```console
$ docker pull gradle@sha256:ad6402057b7dcc9bc5f9b7394f7a73175fbb8df2d4bcc778b6bcc908fd0f0e09
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-graal` - linux; amd64

```console
$ docker pull gradle@sha256:cd793ed09995fc2b9e487880398383211c86efdd9d9f27eb9a51830686710ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597883092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39da629403f6238aae39bfade5260a4190c93089b3498408f26b6f0baaf983e`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 04 Jun 2025 15:28:43 GMT
ARG RELEASE
# Wed, 04 Jun 2025 15:28:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 04 Jun 2025 15:28:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 04 Jun 2025 15:28:43 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 04 Jun 2025 15:28:43 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Wed, 04 Jun 2025 15:28:43 GMT
CMD ["/bin/bash"]
# Wed, 04 Jun 2025 15:28:43 GMT
CMD ["gradle"]
# Wed, 04 Jun 2025 15:28:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 04 Jun 2025 15:28:43 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 04 Jun 2025 15:28:43 GMT
WORKDIR /home/gradle
# Wed, 04 Jun 2025 15:28:43 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 04 Jun 2025 15:28:43 GMT
ENV JAVA_VERSION=17.0.9
# Wed, 04 Jun 2025 15:28:43 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
ENV GRADLE_VERSION=7.6.5
# Wed, 04 Jun 2025 15:28:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=b812fec0edb7d27e0ae35955887bb2954536fa3e44edaf481150da058e154d9a
# Wed, 04 Jun 2025 15:28:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b812fec0edb7d27e0ae35955887bb2954536fa3e44edaf481150da058e154d9a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
USER gradle
# Wed, 04 Jun 2025 15:28:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b812fec0edb7d27e0ae35955887bb2954536fa3e44edaf481150da058e154d9a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
USER root
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901a4fb36017f991f8bc357cd0339536d73ce30db5bc9597fd99f191616c2da5`  
		Last Modified: Wed, 02 Jul 2025 05:35:32 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae19955cbee9a866652dadda9f483a17200f95023c89a3c7e97fb83904d3cd43`  
		Last Modified: Wed, 02 Jul 2025 03:11:20 GMT  
		Size: 148.6 MB (148574560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcde8176b480710de9dbc06249a616900284494bc8da9efec73b115b687b9022`  
		Last Modified: Wed, 02 Jul 2025 03:11:23 GMT  
		Size: 291.1 MB (291064034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9110f4fec07e8ce8f5984bc38decaf65fc991761f8a299026916f3b896bcdfcf`  
		Last Modified: Wed, 02 Jul 2025 03:11:20 GMT  
		Size: 128.5 MB (128469905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5b2ce502c3474c87900fdc1191acf2c47e211f533821b9f0c510750a25f7b5`  
		Last Modified: Wed, 02 Jul 2025 05:35:36 GMT  
		Size: 54.9 KB (54908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:c08776b8c55fd418c2494922abc782f6a89a127d1eb3587641ad5008c42839c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8955323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45be11e91d6a6a15178975cb63ad4d3b522178b918d4ffc7a745aae39b21163d`

```dockerfile
```

-	Layers:
	-	`sha256:e09f7e7589054631cb3d7e6171121d4f6dbb74565cc7058019eefd14fea345dd`  
		Last Modified: Wed, 02 Jul 2025 08:18:55 GMT  
		Size: 8.9 MB (8923195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2403400e9652e19d9d831e1a5edff44067d1109b154bbe9368085b361ed88ba6`  
		Last Modified: Wed, 02 Jul 2025 08:18:56 GMT  
		Size: 32.1 KB (32128 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:f289c6aef1e6ffe5a7b90084960e876b9abe82986d420b3b79c0d779fda2cfbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.6 MB (584570027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090a21702244cccdfc45a7736ba4bd3be44a9d74a11359b365abf61ea564b434`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 04 Jun 2025 15:28:43 GMT
ARG RELEASE
# Wed, 04 Jun 2025 15:28:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 04 Jun 2025 15:28:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 04 Jun 2025 15:28:43 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 04 Jun 2025 15:28:43 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Wed, 04 Jun 2025 15:28:43 GMT
CMD ["/bin/bash"]
# Wed, 04 Jun 2025 15:28:43 GMT
CMD ["gradle"]
# Wed, 04 Jun 2025 15:28:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 04 Jun 2025 15:28:43 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 04 Jun 2025 15:28:43 GMT
WORKDIR /home/gradle
# Wed, 04 Jun 2025 15:28:43 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 04 Jun 2025 15:28:43 GMT
ENV JAVA_VERSION=17.0.9
# Wed, 04 Jun 2025 15:28:43 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
ENV GRADLE_VERSION=7.6.5
# Wed, 04 Jun 2025 15:28:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=b812fec0edb7d27e0ae35955887bb2954536fa3e44edaf481150da058e154d9a
# Wed, 04 Jun 2025 15:28:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b812fec0edb7d27e0ae35955887bb2954536fa3e44edaf481150da058e154d9a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
USER gradle
# Wed, 04 Jun 2025 15:28:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b812fec0edb7d27e0ae35955887bb2954536fa3e44edaf481150da058e154d9a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
USER root
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cffb16294cccda03d23ad58f487e583499867a754c9e438eb0726dac7c7a8ea`  
		Last Modified: Wed, 02 Jul 2025 05:17:44 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f115e0f89eef47671e5b582c9adf395cb460da8f9e21217692a0becd4a17ae7e`  
		Last Modified: Wed, 02 Jul 2025 08:36:09 GMT  
		Size: 143.7 MB (143681423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802b2689e3a4a61fc596488ff2d512a269f3b2d2656fc990ac5b38a17c7d7ddc`  
		Last Modified: Wed, 02 Jul 2025 05:19:55 GMT  
		Size: 283.5 MB (283501827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b502f0111cd08e6e18e529ce68d4f2daca89628a284a672685ee3027f7d169ec`  
		Last Modified: Wed, 02 Jul 2025 05:25:01 GMT  
		Size: 128.5 MB (128469911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e0c270c279485aff191388fe45cc053dbb135df3b873bf1af6e9360301f237`  
		Last Modified: Wed, 02 Jul 2025 05:25:12 GMT  
		Size: 59.5 KB (59528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:268bdf69d2f9d453b363ca48f36f845478188ceef9d6934acc826fbce5ae2b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8951352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2bf3189961d80866127d0c0c06fe72f56e5148704a2599069ad84ed2b05bd1`

```dockerfile
```

-	Layers:
	-	`sha256:6a31c31054a4b54643e22e8c874593f45346ccd0d26934e00f081643bd18217c`  
		Last Modified: Wed, 02 Jul 2025 08:19:03 GMT  
		Size: 8.9 MB (8918892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:960fb3494e7af00209fc7182176197ea34a7e9cf4145f974c38fc7740aa5f2cf`  
		Last Modified: Wed, 02 Jul 2025 08:19:04 GMT  
		Size: 32.5 KB (32460 bytes)  
		MIME: application/vnd.in-toto+json
