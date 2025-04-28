## `gradle:8-jdk21-graal-jammy`

```console
$ docker pull gradle@sha256:e3176c8592d54d1b5a2cf17be4c32dec92fc90a943b1a2eecad31811fc6bf1cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk21-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:44680b55221c8b99cd6cbe6adea50a7066cd8a9d63ff764b70e0b703d1675373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.7 MB (585704016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a01daea1445cbf0590e5751191237c33971fca49d12ad583836bb7e1acc5a6b`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 07 Apr 2025 07:24:14 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:24:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:24:17 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 07 Apr 2025 07:24:18 GMT
CMD ["/bin/bash"]
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["gradle"]
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 26 Apr 2025 01:26:29 GMT
WORKDIR /home/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_VERSION=21.0.2
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_VERSION=8.14
# Sat, 26 Apr 2025 01:26:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER gradle
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER root
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2269b50ad37475ba37d0a6d496fd4a2f71f752daa1d0e55b80ff17c60de9739`  
		Last Modified: Mon, 28 Apr 2025 17:52:25 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb844179e3d7dc0579954a16ede4dad73152b5b9560fa7fd7ab38e15f7512e3`  
		Last Modified: Mon, 28 Apr 2025 17:52:34 GMT  
		Size: 128.7 MB (128731111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bbdbe1c7e2a53c6e0d2e88440a52e47171b2001d1a78b699fde4d47234a223`  
		Last Modified: Mon, 28 Apr 2025 17:52:30 GMT  
		Size: 290.0 MB (289986749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8eaf0bfb214586fb775fd7fbc17b15c323dca58f25d53049ec3c4ff396b3a42`  
		Last Modified: Mon, 28 Apr 2025 17:52:28 GMT  
		Size: 137.4 MB (137394549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353532adeb2950fa505d9c5eb4618af81b606a08dfe528a54076aae43737bf5f`  
		Last Modified: Mon, 28 Apr 2025 17:52:26 GMT  
		Size: 54.9 KB (54900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:12eea7ddad1bc736e2773aa4983072b7578977b87bedc76b59ab1d0583388224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9147649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded3c08e4db2a05244e2200d5392d8b4cec581041a4c8647048a6777941fbd09`

```dockerfile
```

-	Layers:
	-	`sha256:f1da37120aa32489f80f1e9ba301a3698d2bac13021cbdb5dda1a9a9d614ca4c`  
		Last Modified: Mon, 28 Apr 2025 17:52:26 GMT  
		Size: 9.1 MB (9119449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:816e4012f6fe7b82d76ccbdfdf3b1affd5e1a0f532cb7598f86e99d805ca00e8`  
		Last Modified: Mon, 28 Apr 2025 17:52:25 GMT  
		Size: 28.2 KB (28200 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:0492d9642d24a6009d05304c2629625e4482200884839eda500c674643960de3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.0 MB (568954006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5188f474a430881156ad4e6bf5e094c9ac41a84c8ca9eb3d899a1f20eed713`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 07 Apr 2025 07:27:02 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:27:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:27:04 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Mon, 07 Apr 2025 07:27:05 GMT
CMD ["/bin/bash"]
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["gradle"]
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 26 Apr 2025 01:26:29 GMT
WORKDIR /home/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_VERSION=21.0.2
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_VERSION=8.14
# Sat, 26 Apr 2025 01:26:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER gradle
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER root
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cda66dec3f7d2d74252128aa423101dae7874ac5acfb66e43c5531a387c8a13`  
		Last Modified: Wed, 09 Apr 2025 07:21:21 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721f31c0699542f9d3ebba04f54bc3710b2cdcda5f2bab0ae0444ef0aa07b534`  
		Last Modified: Wed, 09 Apr 2025 07:21:25 GMT  
		Size: 122.5 MB (122475095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fd199b2064ca57cdd8b4d259baeb31b79c5c56b97517201a899ac5ef1189fe`  
		Last Modified: Wed, 09 Apr 2025 07:21:27 GMT  
		Size: 281.7 MB (281666245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1309fb75d6614a2b1b5c99999cc4b9bb78f436a31feb10b76ccd27bed24aeb20`  
		Last Modified: Mon, 28 Apr 2025 17:56:08 GMT  
		Size: 137.4 MB (137394556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da76b6ab2bcf729fb262dc4838cf378df0ef65e8429e2f0c8aef0ceac3f5739d`  
		Last Modified: Mon, 28 Apr 2025 17:56:04 GMT  
		Size: 59.5 KB (59538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:79aea2b22fa64239ad76bff88f6eb2a2c326849cb772c267c23413dd4f4393cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9116764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6fd2118793c508a3387677412021531a1b276af3ce892a48325753bcdec70a`

```dockerfile
```

-	Layers:
	-	`sha256:fb0309b5549142899d2ced75ed5c6019c851b9ffc899bba6cbe430ba11b6a60c`  
		Last Modified: Mon, 28 Apr 2025 17:56:04 GMT  
		Size: 9.1 MB (9088304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e6e9e54b6dec8f0a5efd364e98db9afea32fd9887b857ab371c6ae090e4c4c1`  
		Last Modified: Mon, 28 Apr 2025 17:56:03 GMT  
		Size: 28.5 KB (28460 bytes)  
		MIME: application/vnd.in-toto+json
