## `gradle:7-jdk-graal-jammy`

```console
$ docker pull gradle@sha256:59ed5a3e487e43fa7f25312e928d1c5383c782cc200b9ff71491c3cab5ede6bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:9e8ab165d69b8c67014366c2c4c05d11be83de7c4e3da6ca51ac5c5d4c4b4f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **575.7 MB (575669162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4207871d4a0ce2a68995bd8a5071902486105534035241cfc139171a370a08e`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:22:56 GMT
CMD ["gradle"]
# Thu, 13 Nov 2025 23:22:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 13 Nov 2025 23:22:56 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 13 Nov 2025 23:22:56 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 13 Nov 2025 23:22:56 GMT
WORKDIR /home/gradle
# Thu, 13 Nov 2025 23:25:07 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 13 Nov 2025 23:25:07 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 13 Nov 2025 23:25:07 GMT
ENV JAVA_VERSION=17.0.9
# Thu, 13 Nov 2025 23:25:16 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Thu, 13 Nov 2025 23:25:16 GMT
ENV GRADLE_VERSION=7.6.6
# Thu, 13 Nov 2025 23:25:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Thu, 13 Nov 2025 23:25:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 13 Nov 2025 23:25:18 GMT
USER gradle
# Thu, 13 Nov 2025 23:25:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 13 Nov 2025 23:25:18 GMT
USER root
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636e8e90304c91d64789089d8276a6b0db482bfee684c8888a8ccdeea3ab7261`  
		Last Modified: Thu, 13 Nov 2025 23:24:23 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cb10236e80db3c54774a1f2a8756822f024663277036725cebc9b27559702e`  
		Last Modified: Thu, 13 Nov 2025 23:26:21 GMT  
		Size: 126.5 MB (126539578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6921620fa6dda3e25d9af14a155354acab0e58df9ddeb3d60a2a077d40a5e5a9`  
		Last Modified: Fri, 14 Nov 2025 10:12:43 GMT  
		Size: 291.1 MB (291064129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcfe968c00943d4078006530773293c61751c49891c8d4f38b02017613a49ff`  
		Last Modified: Fri, 14 Nov 2025 10:12:43 GMT  
		Size: 128.5 MB (128469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eeacf7ebc49439d47a32e79ead6a1b53c32a4f3f072d9f715718f3ea549dd4f`  
		Last Modified: Thu, 13 Nov 2025 23:26:08 GMT  
		Size: 54.9 KB (54896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:9c81b251c490d21e2742ed5046bb924ca2bf487faa1a8d014735a7f6ec8e7107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9344640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5325eb561a128fdc479c9593dba7d678b61209017b4ffd99674ac7275b75f53d`

```dockerfile
```

-	Layers:
	-	`sha256:97929b0706f3551f8328daadbd2e2c3c9a4203f8251da3b28967fadf8b5b4135`  
		Last Modified: Fri, 14 Nov 2025 03:20:46 GMT  
		Size: 9.3 MB (9315606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfbbc3a155d3eef3ac320ecb02a629d98960ddb7e0fa493cf4e1f8a6ab3a62ab`  
		Last Modified: Fri, 14 Nov 2025 03:20:47 GMT  
		Size: 29.0 KB (29034 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:812c13fda550cd5513f91436f4f6c1e7d92987694fb72c0c880415f029d9ea11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.1 MB (562054581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e6caf6f95539b920889f6c23665c203ed6c04d4cdd8b9214c87f297dbb2cbe`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:24:21 GMT
CMD ["gradle"]
# Thu, 13 Nov 2025 23:24:21 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 13 Nov 2025 23:24:21 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 13 Nov 2025 23:24:21 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 13 Nov 2025 23:24:21 GMT
WORKDIR /home/gradle
# Thu, 13 Nov 2025 23:24:48 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 13 Nov 2025 23:24:48 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 13 Nov 2025 23:24:48 GMT
ENV JAVA_VERSION=17.0.9
# Thu, 13 Nov 2025 23:24:58 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Thu, 13 Nov 2025 23:24:58 GMT
ENV GRADLE_VERSION=7.6.6
# Thu, 13 Nov 2025 23:24:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Thu, 13 Nov 2025 23:25:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 13 Nov 2025 23:25:00 GMT
USER gradle
# Thu, 13 Nov 2025 23:25:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 13 Nov 2025 23:25:01 GMT
USER root
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61d2c27e65d0d107741e86d6af4d3eaf5ad2f06b5229b16f3cd811b340edde0`  
		Last Modified: Thu, 13 Nov 2025 23:25:48 GMT  
		Size: 4.3 KB (4316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15779278a88278186379fa263e583b587fc73e618d627d75c53fdc924d21d89`  
		Last Modified: Thu, 13 Nov 2025 23:25:56 GMT  
		Size: 122.6 MB (122635495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d920d8c056ca8320bdaf818bbf15fc84c287fb2c47eedac4b513ef39af16a574`  
		Last Modified: Fri, 14 Nov 2025 10:14:06 GMT  
		Size: 283.5 MB (283501921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be1b739493e85934f816d7ade62a89d46a16d7fe3b3de5c9eeeb86ba993070a`  
		Last Modified: Fri, 14 Nov 2025 10:14:12 GMT  
		Size: 128.5 MB (128469418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59900c8194097e12a363003dd83871d3be3a958f3d895ac0d66a245c8eb06629`  
		Last Modified: Thu, 13 Nov 2025 23:25:48 GMT  
		Size: 59.5 KB (59522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:6d85fd02812fbe03dc8d5f212617e8d3814b09ca55a3a615913979ceac652554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9313684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cfabb99847476f103469f71123f1f3a5ba599d811d59b50381c48ce9501454`

```dockerfile
```

-	Layers:
	-	`sha256:2855e73f04585f93d3b57969f77d1c3fa52ccb0bee3b4d201d39309066883ecb`  
		Last Modified: Fri, 14 Nov 2025 03:20:53 GMT  
		Size: 9.3 MB (9284426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fe7e77521dae4055eb80ee7c8228ed0cacd48452a9bfa49ed523a01406a433a`  
		Last Modified: Fri, 14 Nov 2025 03:20:54 GMT  
		Size: 29.3 KB (29258 bytes)  
		MIME: application/vnd.in-toto+json
