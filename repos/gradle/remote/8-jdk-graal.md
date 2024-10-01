## `gradle:8-jdk-graal`

```console
$ docker pull gradle@sha256:68db2d05da8c0ef56838889ff326e5b092906fc70428738656659fb934b3f275
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk-graal` - linux; amd64

```console
$ docker pull gradle@sha256:f12fdb68acec4babb676ec03c6f7536f33fc8c72f3274e4a7d199961129ee733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.8 MB (583785736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2339efcf573eb825034710fe00b1f59d42237653cc83789b9ee1b131a34faa8f`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Sat, 28 Sep 2024 00:46:05 GMT
CMD ["gradle"]
# Sat, 28 Sep 2024 00:46:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 28 Sep 2024 00:46:05 GMT
WORKDIR /home/gradle
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sat, 28 Sep 2024 00:46:05 GMT
ENV JAVA_VERSION=17.0.9
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
ENV GRADLE_VERSION=8.10.2
# Sat, 28 Sep 2024 00:46:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
# Sat, 28 Sep 2024 00:46:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
USER gradle
# Sat, 28 Sep 2024 00:46:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
USER root
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7948a323c2cd768a75d7323ccfaa45ed42c5a61e0559be097ef20f6d4711bbf5`  
		Last Modified: Mon, 30 Sep 2024 21:56:40 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de68326e298fbf822a740372fa70a69490bebb35255fbb8b1c502fbeabd2e1b8`  
		Last Modified: Mon, 30 Sep 2024 21:56:41 GMT  
		Size: 126.4 MB (126396753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82bfd94cecbc0debc052e13abf6bc158c61effacf02f19c3bb9c18fd50808fde`  
		Last Modified: Mon, 30 Sep 2024 21:56:44 GMT  
		Size: 291.1 MB (291064316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babed8beb511d0df1bf377fa7fa5a339698a0775e7cc43d3cb5db3327f6d0a2d`  
		Last Modified: Mon, 30 Sep 2024 21:56:42 GMT  
		Size: 136.7 MB (136729729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df75ff57bf0ab3dc15366b44fb6fc358c2fd54c0a7509ab7a115821ead4509cb`  
		Last Modified: Mon, 30 Sep 2024 21:56:40 GMT  
		Size: 54.9 KB (54910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:3a5f1c2b20515007161a351a299db521ec5968b4e316e3c74a03ce6632953feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9118745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3025629617fd7c0d9e6f8509776dd1e38af35c94d912e17f72d70c1755c6570`

```dockerfile
```

-	Layers:
	-	`sha256:a4113ea0c1196462d7b5ded47ef918e9bf27dd6860352bc2b2d934d00f25f5e0`  
		Last Modified: Mon, 30 Sep 2024 21:56:40 GMT  
		Size: 9.1 MB (9086967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41541d877da5e920d8545e094dfab93a2e7726f8c4eea5fe40e23755e0df9cb9`  
		Last Modified: Mon, 30 Sep 2024 21:56:40 GMT  
		Size: 31.8 KB (31778 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:5867cd8f889f69ab0a5f76454dbb31cba87b6cf8c4b246739ac30329fb463b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.1 MB (570093892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2af735647c2fab4ca4f840bd0b855306e0095036eea09d7b1929078ab96302c`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Sat, 28 Sep 2024 00:46:05 GMT
CMD ["gradle"]
# Sat, 28 Sep 2024 00:46:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 28 Sep 2024 00:46:05 GMT
WORKDIR /home/gradle
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sat, 28 Sep 2024 00:46:05 GMT
ENV JAVA_VERSION=17.0.9
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
ENV GRADLE_VERSION=8.10.2
# Sat, 28 Sep 2024 00:46:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
# Sat, 28 Sep 2024 00:46:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
USER gradle
# Sat, 28 Sep 2024 00:46:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
USER root
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dbf81a4c4aaff3b6c6448eabbb382cee87c8267d0e27f132a5b6a51910bdfa`  
		Last Modified: Tue, 17 Sep 2024 01:58:31 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382f2c1e459cedc278c5decc483de60ed3b6adbb1853e4bd16e084ecbc832f01`  
		Last Modified: Tue, 17 Sep 2024 01:58:34 GMT  
		Size: 122.4 MB (122439929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94067c6ce12f6f10237f5964ebeaa86174121abc736bb16df8fcd6770f284a5`  
		Last Modified: Tue, 17 Sep 2024 01:58:39 GMT  
		Size: 283.5 MB (283502033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0528af7658a02a06e28f7fb4aaffcb1227bdd36fb66a6edb38487db27a9e981e`  
		Last Modified: Mon, 30 Sep 2024 22:03:02 GMT  
		Size: 136.7 MB (136729737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d493f8eb4a2fc3e6f75bb940e504d6bab2347ae7ee06c3597ab41b3a33623e`  
		Last Modified: Mon, 30 Sep 2024 22:02:59 GMT  
		Size: 59.5 KB (59524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:66d1d1c9ae008f37b8516a7cb2457312ffb1260a9e8902d90b1be533e7064833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9082305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c36b101c1a16708ed8a9a9668842474a91eaac608ea4ba42bfdeb8357ac6d6`

```dockerfile
```

-	Layers:
	-	`sha256:d7c18b0dd9de5220e06f6cdcb8e795737afd041a7f75db9a9c3e24f386dd666c`  
		Last Modified: Mon, 30 Sep 2024 22:02:59 GMT  
		Size: 9.0 MB (9049985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:726b017c86c49202d2c234d427751c026ac8474dab788579b5a3f7b347ae902f`  
		Last Modified: Mon, 30 Sep 2024 22:02:59 GMT  
		Size: 32.3 KB (32320 bytes)  
		MIME: application/vnd.in-toto+json
