## `gradle:7-graal-jammy`

```console
$ docker pull gradle@sha256:f831cd745786bb3bfbc3639ec4a29722dff59378aee2675d4e11a72c7fa905f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:6ca8cc3a2340b58c8ae3249a5417912ef0034d689f1cadff8a0ad2a61817c549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.1 MB (576067617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe12bcbc598efebfb4a4fbc3cf9b1aea8aafa59e898032d48abd50762497991`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:16:41 GMT
CMD ["gradle"]
# Fri, 15 May 2026 21:16:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 15 May 2026 21:16:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 15 May 2026 21:16:41 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 15 May 2026 21:16:41 GMT
WORKDIR /home/gradle
# Fri, 15 May 2026 21:17:04 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 15 May 2026 21:17:04 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 15 May 2026 21:17:04 GMT
ENV JAVA_VERSION=17.0.9
# Fri, 15 May 2026 21:17:14 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Fri, 15 May 2026 21:17:14 GMT
ENV GRADLE_VERSION=7.6.6
# Fri, 15 May 2026 21:17:14 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Fri, 15 May 2026 21:17:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 15 May 2026 21:17:16 GMT
USER gradle
# Fri, 15 May 2026 21:17:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 15 May 2026 21:17:17 GMT
USER root
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bf06ee3e6c82c5f11a708568e70af5d0a0dc9d1f40f8efaeaa829269200e3d`  
		Last Modified: Fri, 15 May 2026 21:17:46 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34149386e4737bfbf46f11372287248e7a309597cdb393ca21ea32a4478eb6db`  
		Last Modified: Fri, 15 May 2026 21:17:56 GMT  
		Size: 126.7 MB (126737960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae38ca5fb16ab63858f10bf3dd9f26835c817c69bad05695d4888e6d57619690`  
		Last Modified: Fri, 15 May 2026 21:18:04 GMT  
		Size: 291.1 MB (291064305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a4368473a5f75a07cc145ee42705c5dd82c66f2bc763266a6f9ef32c295db5`  
		Last Modified: Fri, 15 May 2026 21:17:57 GMT  
		Size: 128.5 MB (128469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618b8ba7941f32c79c356f2fd153f9a32d245c96990e28fb12ea046c5dc5b7c1`  
		Last Modified: Fri, 15 May 2026 21:17:48 GMT  
		Size: 54.9 KB (54909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:f9ff3ae1c107f65983b27905d6f9cca5ec1ec07456cbb72d189cef12e8480d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9344656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0228167e14adc08cb8ec32b8f1bfd8cab569bb29a5c7cb1ee370765a6284af`

```dockerfile
```

-	Layers:
	-	`sha256:3dfe07ccb73cd173af090201f999b968bffd13959d5555f6c26b8e18de835076`  
		Last Modified: Fri, 15 May 2026 21:17:47 GMT  
		Size: 9.3 MB (9315622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3937b08a62e82d31c88d4056c6e8831e20e8a658887735ccfe96fdc6a03552c4`  
		Last Modified: Fri, 15 May 2026 21:17:46 GMT  
		Size: 29.0 KB (29034 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:bb5f1a91d1a9f6dfe88f00c0dae99448d3f8cecc7ac0364619e135cdee77f4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.5 MB (562511420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29e3b313b9abcf78c5db268d542735125b950d3f0ab6c1040a020be38db849f`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:16:56 GMT
CMD ["gradle"]
# Fri, 15 May 2026 21:16:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 15 May 2026 21:16:56 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 15 May 2026 21:16:56 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 15 May 2026 21:16:56 GMT
WORKDIR /home/gradle
# Fri, 15 May 2026 21:17:30 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 15 May 2026 21:17:30 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 15 May 2026 21:17:30 GMT
ENV JAVA_VERSION=17.0.9
# Fri, 15 May 2026 21:17:39 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Fri, 15 May 2026 21:17:39 GMT
ENV GRADLE_VERSION=7.6.6
# Fri, 15 May 2026 21:17:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Fri, 15 May 2026 21:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 15 May 2026 21:17:41 GMT
USER gradle
# Fri, 15 May 2026 21:17:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 15 May 2026 21:17:42 GMT
USER root
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2920ead9703800b70a1a8f4c901be979f80b796b75eb999d500b19c6aebb9ec5`  
		Last Modified: Fri, 15 May 2026 21:18:15 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14a7c2753999c8ae6d6403f11c00ce9fdff3f08783cbbac9cc16b46cca22cbe`  
		Last Modified: Fri, 15 May 2026 21:18:22 GMT  
		Size: 122.9 MB (122869626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da14f74f1c32498dc4cce457422cec03a57d48acc7ad0740a1f8b5302f3dcfbd`  
		Last Modified: Fri, 15 May 2026 21:18:25 GMT  
		Size: 283.5 MB (283501885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6c2824d0c8e5dc12c5b45dd115c21ef4d29d2ae708fd84d36e728f984208f8`  
		Last Modified: Fri, 15 May 2026 21:18:22 GMT  
		Size: 128.5 MB (128469418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964a36c0969acb030a00fb75eda27ba3913f8c180c68912aea712357ce08c444`  
		Last Modified: Fri, 15 May 2026 21:18:16 GMT  
		Size: 59.5 KB (59521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:590a21567de0e4368f239b8b954c292a2106ee8c393ea45e3ded9b6936085258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9313700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f27f1ac1f81712ab94aea0feda3995c4ce2ce982c42d7e63f3b699a4507121f5`

```dockerfile
```

-	Layers:
	-	`sha256:95260c465d3ccb0f1b8af76c90c5fcf261f0314b7cdf181a1082b26f39ceaa3c`  
		Last Modified: Fri, 15 May 2026 21:18:15 GMT  
		Size: 9.3 MB (9284442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b4958075c9572aa5054d4b24d3e4f67b4b63417d9386a22717a802e77c98fd3`  
		Last Modified: Fri, 15 May 2026 21:18:15 GMT  
		Size: 29.3 KB (29258 bytes)  
		MIME: application/vnd.in-toto+json
