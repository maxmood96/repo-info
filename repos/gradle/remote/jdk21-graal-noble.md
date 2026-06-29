## `gradle:jdk21-graal-noble`

```console
$ docker pull gradle@sha256:e6c57be9e06439a5baad31e9b410f323c6315ad10b3550898984eedcbd0e8420
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk21-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:1052834abc10ee1d10cf2202afe36f6d60eedbad1818766f3be5a7dcd93fdb65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.6 MB (613557456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b7329cbeae4294a4ad378a92586cfb439f0cec10a0877f0bd1ead0675874fa`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Mon, 29 Jun 2026 17:12:24 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:12:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:12:24 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:12:24 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:12:24 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:12:54 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:12:54 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Mon, 29 Jun 2026 17:12:54 GMT
ENV JAVA_VERSION=21.0.2
# Mon, 29 Jun 2026 17:13:03 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Mon, 29 Jun 2026 17:13:03 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:13:03 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:13:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:13:05 GMT
USER gradle
# Mon, 29 Jun 2026 17:13:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:13:05 GMT
USER root
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cd117fe9f61043bc83ca6159396506214f2ee17b19f7fd4898260d73f6ab85`  
		Last Modified: Mon, 29 Jun 2026 17:13:41 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b48eca0bcbfefc655f7598ceabd6c0697dd61a7e6e35f5a93f3865450d469e3`  
		Last Modified: Mon, 29 Jun 2026 17:13:49 GMT  
		Size: 153.2 MB (153215013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16671aec6d43ad0c302f10b8c66abc478619e3ebee93c0c589a3b91af8ebec78`  
		Last Modified: Mon, 29 Jun 2026 17:13:52 GMT  
		Size: 290.0 MB (289986695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13c7f898b29a93d642495798e79e98118b3913b7f83d6c413c8282b119030f5`  
		Last Modified: Mon, 29 Jun 2026 17:13:49 GMT  
		Size: 140.6 MB (140596025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dfe39e42424fdc75731d5713e3454f5b975a97ce06b4bbfec3f22cf82be6e2`  
		Last Modified: Mon, 29 Jun 2026 17:13:43 GMT  
		Size: 25.6 KB (25603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:626654d26e85d800061a4e21243c8e4c43c3db20de8a23d66e6993f2d16bfc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9024827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de03c9284fc585cd209b3c9ad56377704df2873aaaeaac6b68e29eb17860bc1`

```dockerfile
```

-	Layers:
	-	`sha256:9e9f63dcdd14f7d88e92a4f262087430fda7afb55993ce02471a407d97b4ea1c`  
		Last Modified: Mon, 29 Jun 2026 17:13:42 GMT  
		Size: 9.0 MB (8997135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:441e00c212a51ea8ff5bb70eb4ea669b5d3e5e01635309c72e2b7c93fb71f048`  
		Last Modified: Mon, 29 Jun 2026 17:13:41 GMT  
		Size: 27.7 KB (27692 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c7c553268e8c4fd5f12c77d440cb89e1ca6e9bb2de889b9419e8a7da0a4c6115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.2 MB (599245956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0878fd081edcfe4b777cd71ad4af171fefbef5801bae9adebff631de97c1e0ba`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Mon, 29 Jun 2026 17:12:22 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:12:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:12:22 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:12:22 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:12:22 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:12:51 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:12:51 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Mon, 29 Jun 2026 17:12:51 GMT
ENV JAVA_VERSION=21.0.2
# Mon, 29 Jun 2026 17:13:01 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Mon, 29 Jun 2026 17:13:01 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:13:01 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:13:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:13:03 GMT
USER gradle
# Mon, 29 Jun 2026 17:13:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:13:04 GMT
USER root
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044cef0f10065b264ee140f4589ba11f1bdfd971b4ed20a5156ee97d6255f69a`  
		Last Modified: Mon, 29 Jun 2026 17:13:36 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd99da28b09ee39a6b4e262ab6225cb6d9d16d8c0743b9b673818ea6e9d0cd7`  
		Last Modified: Mon, 29 Jun 2026 17:13:44 GMT  
		Size: 148.1 MB (148076563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895ababdafa819875ee1bcf2f14175745b0a754d6b8e61b0b06a59fcd8903d07`  
		Last Modified: Mon, 29 Jun 2026 17:13:47 GMT  
		Size: 281.7 MB (281666305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a42c6321778d4947f9fb8737b684c1e06cb752c1ebb6d4f73f4541c109e44a`  
		Last Modified: Mon, 29 Jun 2026 17:13:44 GMT  
		Size: 140.6 MB (140596023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809ed9540dd3bd42c5dc3750baeb7507279a4b0c087a3c21fb455cbf6bcbee1a`  
		Last Modified: Mon, 29 Jun 2026 17:13:38 GMT  
		Size: 29.3 KB (29340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:0cb6900773bc7e7cbcb07cbf2ffc69885f607ea14fe97037d8c87aae3d58591c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9020524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f406ec5d8f4d441a59a95015ae5e48ef0f795421c060943c1231d0bf1d97e9c9`

```dockerfile
```

-	Layers:
	-	`sha256:e7969b6f38e55a851f3b8d907f0f80264e6b99d9156e2584458042ca664c033a`  
		Last Modified: Mon, 29 Jun 2026 17:13:37 GMT  
		Size: 9.0 MB (8992668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb3c43f2540d85c27aed36a757866e0eedd291dfe421e3a874515bb48baafad1`  
		Last Modified: Mon, 29 Jun 2026 17:13:37 GMT  
		Size: 27.9 KB (27856 bytes)  
		MIME: application/vnd.in-toto+json
