## `gradle:7-graal-jammy`

```console
$ docker pull gradle@sha256:fb5d02c03f55a5c85ad1511a9d667f0c4c1a1580782c5915842d37419fc85ae2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:55c2d56ed14cde5dc012ef85d8629349e7bb33db3ecbfeacd95b91ab217c22be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.1 MB (576066474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e9efe51325c796e0ab24b30f8f73f3cc0243eb30f8bd52e799e2f63d7d8394`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:37:22 GMT
CMD ["gradle"]
# Wed, 15 Apr 2026 20:37:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 15 Apr 2026 20:37:22 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 15 Apr 2026 20:37:22 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 15 Apr 2026 20:37:22 GMT
WORKDIR /home/gradle
# Wed, 15 Apr 2026 20:37:52 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 15 Apr 2026 20:37:52 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 15 Apr 2026 20:37:52 GMT
ENV JAVA_VERSION=17.0.9
# Wed, 15 Apr 2026 20:38:02 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Wed, 15 Apr 2026 20:38:02 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 15 Apr 2026 20:38:02 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 15 Apr 2026 20:38:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 15 Apr 2026 20:38:04 GMT
USER gradle
# Wed, 15 Apr 2026 20:38:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 15 Apr 2026 20:38:04 GMT
USER root
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7527a225a4656062f32250fab0ae5aa3d7e7cd3130f406650872932414a977`  
		Last Modified: Wed, 15 Apr 2026 20:38:38 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c52d12b7587db3692212fd8d6ff6e0ec20fe2315172cc8039995b689c1f6049`  
		Last Modified: Wed, 15 Apr 2026 20:38:45 GMT  
		Size: 126.7 MB (126737130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6fe54d1ec432fc14908b0e979bdee6a59e3fe03d711c7557014932dfa2fb7a`  
		Last Modified: Wed, 15 Apr 2026 20:38:48 GMT  
		Size: 291.1 MB (291064193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb49e2fb639519fb1fbc0d7aa3e17ca517115ac491ba7819beaf2c8a321b06b`  
		Last Modified: Wed, 15 Apr 2026 20:38:45 GMT  
		Size: 128.5 MB (128469416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6080f7faa4c4550817ac36a5c25106e957b5e2d2d53137dbabc4fe703c593ed9`  
		Last Modified: Wed, 15 Apr 2026 20:38:39 GMT  
		Size: 54.9 KB (54899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:27a0e13cbbb3b8aa3278038e706ff0d6a2a8bb86655ec153b9388ea7fbddf2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9344656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a36b5b3b01951eaf6aafbe907306802f52a36510574964341c50e65ea966edc`

```dockerfile
```

-	Layers:
	-	`sha256:48bef3e1f5a29aaabde792089ea54cd2aa603f4ec51058dafcce1dbc5e40e8dc`  
		Last Modified: Wed, 15 Apr 2026 20:38:38 GMT  
		Size: 9.3 MB (9315622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63abd20bc6b1470f407484595994f6e63c3e90fad24571ce2a077a85571a96ae`  
		Last Modified: Wed, 15 Apr 2026 20:38:38 GMT  
		Size: 29.0 KB (29034 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:354e477cf917bf3f4a1c27b905f9f340879f603cf2912a35c88a244152b54d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.5 MB (562529766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4719272dd30e0c6cf158af40351e3dd07c65bfaf289305b69050e849416be913`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:37:41 GMT
CMD ["gradle"]
# Wed, 15 Apr 2026 20:37:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 15 Apr 2026 20:37:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 15 Apr 2026 20:37:41 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 15 Apr 2026 20:37:41 GMT
WORKDIR /home/gradle
# Wed, 15 Apr 2026 20:38:15 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 15 Apr 2026 20:38:15 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 15 Apr 2026 20:38:15 GMT
ENV JAVA_VERSION=17.0.9
# Wed, 15 Apr 2026 20:38:25 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Wed, 15 Apr 2026 20:38:25 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 15 Apr 2026 20:38:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 15 Apr 2026 20:38:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 15 Apr 2026 20:38:27 GMT
USER gradle
# Wed, 15 Apr 2026 20:38:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 15 Apr 2026 20:38:28 GMT
USER root
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb841f1a0a265bc0bdcb6fbcb631d1f215ede46c7691c44a7303ffae4448e35`  
		Last Modified: Wed, 15 Apr 2026 20:39:00 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab34ad027dab12bf7e33cc625825d1c13beebb3e1bc6289b403166905f8b4c4`  
		Last Modified: Wed, 15 Apr 2026 20:39:07 GMT  
		Size: 122.9 MB (122888039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243f3c40bc8f85618d1f34c58167fadf567af4f38a1a89d784e431cfbd84e615`  
		Last Modified: Wed, 15 Apr 2026 20:39:10 GMT  
		Size: 283.5 MB (283501890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb35d2d9c5fdc6a968150cc0f10669772858f7b9daa9c6384c83966fb2f71a27`  
		Last Modified: Wed, 15 Apr 2026 20:39:07 GMT  
		Size: 128.5 MB (128469418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924b503c3cfd09b01f3e26381c163e117c2e9fe60b5edc8414d637b132910c9a`  
		Last Modified: Wed, 15 Apr 2026 20:39:01 GMT  
		Size: 59.5 KB (59529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:00c9fe3796205733cb7995c6cccdda17c2959f3dff3a9f9093d3052479cd309c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9313696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3969608598a89622b13be4f82903ffc0f0054368238189b322744cf47a479cf5`

```dockerfile
```

-	Layers:
	-	`sha256:6af4f8327d202373c6ed026f9c209854c0289a05d8b222e0dd6e1c70226f7fd8`  
		Last Modified: Wed, 15 Apr 2026 20:39:01 GMT  
		Size: 9.3 MB (9284438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ed103ba56028e8963ca2590ef2cce87c434c6ea8d54a92358ebbd0cddd9cbb7`  
		Last Modified: Wed, 15 Apr 2026 20:39:00 GMT  
		Size: 29.3 KB (29258 bytes)  
		MIME: application/vnd.in-toto+json
