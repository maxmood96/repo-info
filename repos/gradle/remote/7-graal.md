## `gradle:7-graal`

```console
$ docker pull gradle@sha256:e4303f246f1114b1c35b26d35a6ab4af24aa0431706181c695c6d8380e09c9ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-graal` - linux; amd64

```console
$ docker pull gradle@sha256:7351793ba1f9f04160f1ead0971299298ebdfd9eaa3e6d56d532fc5881903fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.1 MB (598142511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586a1389b8b2dc71556645532441ce549a8ad4bdb83014923a512e44d84e1b60`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:53:03 GMT
CMD ["gradle"]
# Tue, 07 Apr 2026 01:53:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 07 Apr 2026 01:53:03 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 07 Apr 2026 01:53:03 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 07 Apr 2026 01:53:03 GMT
WORKDIR /home/gradle
# Tue, 07 Apr 2026 01:55:29 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 07 Apr 2026 01:55:29 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 07 Apr 2026 01:55:29 GMT
ENV JAVA_VERSION=17.0.9
# Tue, 07 Apr 2026 01:55:39 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Tue, 07 Apr 2026 01:55:39 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 07 Apr 2026 01:55:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 07 Apr 2026 01:55:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 07 Apr 2026 01:55:41 GMT
USER gradle
# Tue, 07 Apr 2026 01:55:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 07 Apr 2026 01:55:42 GMT
USER root
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3421e00ed84a32bec04e2413cf4fe81311670ba7237cfbbbe151fe36c8afce75`  
		Last Modified: Tue, 07 Apr 2026 01:54:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a8dd6f142ddb68b1483deafc37c3612f0f9c965a02e9aa9cdf1c3dd2145203`  
		Last Modified: Tue, 07 Apr 2026 01:56:23 GMT  
		Size: 148.8 MB (148819368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ecc46bc7a624dbd3692a3316cdafcfd6dc63481f0524ae8d012e2a2c4dcd1a2`  
		Last Modified: Tue, 07 Apr 2026 01:56:26 GMT  
		Size: 291.1 MB (291064036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19420b7b878b6620b9252fb28fcad9de889db63666c60155c75ba7e5cbd1c3ee`  
		Last Modified: Tue, 07 Apr 2026 01:56:23 GMT  
		Size: 128.5 MB (128469420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3ca847312a48cec87f3fbc9fd6ccd53a7f56d2f7df23fb761c728fec7255f0`  
		Last Modified: Tue, 07 Apr 2026 01:56:15 GMT  
		Size: 54.9 KB (54909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:c0c667d0958c40bdab599e631e306ac7fdb0022767523b6cb40c05ce8ea1ea02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8955448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426afe1b779ef97d1d01eb8d178f8544d5b87eaa895c964face4c4e1007d9c26`

```dockerfile
```

-	Layers:
	-	`sha256:7e95c47abd16e950281088d5515b4f90ad435cf18fc7e3d22dae59a9fe1cd8b7`  
		Last Modified: Tue, 07 Apr 2026 01:56:16 GMT  
		Size: 8.9 MB (8923379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50127e2966ff18a1e95ba19deb10bd9eb05766cba508efcbdd52dbab82973ac6`  
		Last Modified: Tue, 07 Apr 2026 01:56:15 GMT  
		Size: 32.1 KB (32069 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:277e5eb344d23be8be53fb5a4155c0c73bc129fb8e98155803d368131d9cf8c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.8 MB (584825928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b11bbf78276ce7078c36d7a1a17f95828bc71570745c25fcef5455aed7fde5`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:58:05 GMT
CMD ["gradle"]
# Tue, 07 Apr 2026 01:58:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 07 Apr 2026 01:58:05 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 07 Apr 2026 01:58:05 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 07 Apr 2026 01:58:05 GMT
WORKDIR /home/gradle
# Tue, 07 Apr 2026 01:58:44 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 07 Apr 2026 01:58:44 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 07 Apr 2026 01:58:44 GMT
ENV JAVA_VERSION=17.0.9
# Tue, 07 Apr 2026 01:58:54 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Tue, 07 Apr 2026 01:58:54 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 07 Apr 2026 01:58:54 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 07 Apr 2026 01:58:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 07 Apr 2026 01:58:56 GMT
USER gradle
# Tue, 07 Apr 2026 01:58:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 07 Apr 2026 01:58:57 GMT
USER root
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31a965e42bc0f1b87f92ed73318494dd59f6880e492a17092b0ba0b403f23bf`  
		Last Modified: Tue, 07 Apr 2026 01:59:29 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4201fa8bd8d4bb066a58c2b15131fcae1f2b5b41f8088a5ea398f2830a384a`  
		Last Modified: Tue, 07 Apr 2026 01:59:36 GMT  
		Size: 143.9 MB (143919729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca839356c4208d28dbe6fee2fa5853dc5c7c4bdd08c8bbf5db3f516e9b14400d`  
		Last Modified: Tue, 07 Apr 2026 01:59:38 GMT  
		Size: 283.5 MB (283501853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b168c71f8336fa53a8522c00631406c53621ce2c9ba7f232428e572c7ec12fe`  
		Last Modified: Tue, 07 Apr 2026 01:59:36 GMT  
		Size: 128.5 MB (128469441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e41295be58897b619373ca5db15c3b7bbc73f5e4e0832745963ab74fc4ed21`  
		Last Modified: Tue, 07 Apr 2026 01:59:30 GMT  
		Size: 59.5 KB (59519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:156e6d50d5f27783b26958849947dc35b440504307b4941a3afd466dbdcfdfdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8951481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:decb8f3d822709544e647c277bb90993cda035eb53f10fe8c69a727f4bd87256`

```dockerfile
```

-	Layers:
	-	`sha256:3a6cf6bb84bf8a7fef14eea01ccdd9d0a9d9ec353d9cb455aeea876fa0156b29`  
		Last Modified: Tue, 07 Apr 2026 01:59:30 GMT  
		Size: 8.9 MB (8919080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e42a8d82600a279093746f7ea87aa1cc0649f30f58bf2380020ce79192a3c061`  
		Last Modified: Tue, 07 Apr 2026 01:59:29 GMT  
		Size: 32.4 KB (32401 bytes)  
		MIME: application/vnd.in-toto+json
