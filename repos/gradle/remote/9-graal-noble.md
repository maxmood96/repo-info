## `gradle:9-graal-noble`

```console
$ docker pull gradle@sha256:dfc558209d5600c6d25996a17d2b6e9fe34f96cfe775200ec0f962c9ace9b815
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:1f2efc87809e1298bc1244ef32667697e386e77627b18a094716cb5aa27edcfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.8 MB (661803599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bbe78625c7cad65ab2a4110956094d9ff985fb8235a09aaca125397d1c5c79f`
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
# Mon, 22 Jun 2026 18:05:46 GMT
CMD ["gradle"]
# Mon, 22 Jun 2026 18:05:46 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 22 Jun 2026 18:05:46 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 22 Jun 2026 18:05:46 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 22 Jun 2026 18:05:46 GMT
WORKDIR /home/gradle
# Mon, 22 Jun 2026 18:06:13 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 22 Jun 2026 18:06:13 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Mon, 22 Jun 2026 18:06:13 GMT
ENV JAVA_VERSION=25.0.2
# Mon, 22 Jun 2026 18:06:24 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e0be791c8fda4d03b6b0a0cb824fef3149736170057b3a515252b44419606af0     && GRAALVM_AARCH64_DOWNLOAD_SHA256=b4580d9f223d0a4b3a1757e58b18ff4c1db950e67e105fc5cb741457d2384a71     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Mon, 22 Jun 2026 18:06:24 GMT
ENV GRADLE_VERSION=9.6.0
# Mon, 22 Jun 2026 18:06:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
# Mon, 22 Jun 2026 18:06:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 22 Jun 2026 18:06:26 GMT
USER gradle
# Mon, 22 Jun 2026 18:06:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 22 Jun 2026 18:06:26 GMT
USER root
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eecfe86ed291fcf5f7ee14e6839d9a018dd4025da2842cd9df2e03cb12df9c2`  
		Last Modified: Mon, 22 Jun 2026 18:07:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700631aedc9d55e0d99046da3b011ed429dab7f12bea7a7e4fb41ad59cb728b4`  
		Last Modified: Mon, 22 Jun 2026 18:07:24 GMT  
		Size: 150.6 MB (150554815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da91195f5fe7192a47190161eb2f00061f39031869edaa85f8b93b64bdbb8be`  
		Last Modified: Mon, 22 Jun 2026 18:07:30 GMT  
		Size: 340.9 MB (340893947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e9a4a149e907786f8cb71fd48c1cd0a6d31b9b4c5c8f812c7155116ad7fb29`  
		Last Modified: Mon, 22 Jun 2026 18:07:23 GMT  
		Size: 140.6 MB (140595104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ba9924a6656e2394d53c967b6ac85ed3cc77f33c9b9e6551836e64fe416edf`  
		Last Modified: Mon, 22 Jun 2026 18:07:05 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:6d40d6d143d60d10c6ab70a3e8ee7041c3fff2e09c31ba246d60bf0a28d0664f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9074359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ac8f8a58f02ca9c0390a50f2bc0c0e62036ab2af71a7beee8b8d4ed308db39`

```dockerfile
```

-	Layers:
	-	`sha256:bb9ba53d09ead644d786ed85424e4857aed7704da00855624c350ad6ca5ed12c`  
		Last Modified: Mon, 22 Jun 2026 18:07:04 GMT  
		Size: 9.0 MB (9044123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cd538019b773e2363ef702e6738d963d6c20e26c864f548946b89922c26e5b1`  
		Last Modified: Mon, 22 Jun 2026 18:07:03 GMT  
		Size: 30.2 KB (30236 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c207825a2ba13f31d10706450acee369da091eabd3ca619d985e1d93c11f3ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.0 MB (630965608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604ee4bdea174f09b7cd5712d1d6f9bec9ea252efaf28fcf08838c9ba3ae50ad`
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
# Mon, 22 Jun 2026 18:03:53 GMT
CMD ["gradle"]
# Mon, 22 Jun 2026 18:03:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 22 Jun 2026 18:03:53 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 22 Jun 2026 18:03:53 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 22 Jun 2026 18:03:53 GMT
WORKDIR /home/gradle
# Mon, 22 Jun 2026 18:04:20 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 22 Jun 2026 18:04:20 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Mon, 22 Jun 2026 18:04:20 GMT
ENV JAVA_VERSION=25.0.2
# Mon, 22 Jun 2026 18:04:30 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e0be791c8fda4d03b6b0a0cb824fef3149736170057b3a515252b44419606af0     && GRAALVM_AARCH64_DOWNLOAD_SHA256=b4580d9f223d0a4b3a1757e58b18ff4c1db950e67e105fc5cb741457d2384a71     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Mon, 22 Jun 2026 18:04:30 GMT
ENV GRADLE_VERSION=9.6.0
# Mon, 22 Jun 2026 18:04:30 GMT
ARG GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
# Mon, 22 Jun 2026 18:04:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 22 Jun 2026 18:04:32 GMT
USER gradle
# Mon, 22 Jun 2026 18:04:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 22 Jun 2026 18:04:33 GMT
USER root
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d225bc33a9b686026b7dfa947d5271e21633990c25eaeb15d19cabaaf859a2`  
		Last Modified: Mon, 22 Jun 2026 18:05:08 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef32095f87f4db43791b4352ed01047878596673480589f2bdb65098e3ad868f`  
		Last Modified: Mon, 22 Jun 2026 18:05:16 GMT  
		Size: 145.5 MB (145476671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d23919895d21fa663a0fc22de8dfaff169637adbe18b0c2ea311ce37f2931fa`  
		Last Modified: Mon, 22 Jun 2026 18:05:19 GMT  
		Size: 316.0 MB (315986768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b1b80862aa7652b109fcb3e8e14cc4a5857ebc387d62c389b238018eca8c1a`  
		Last Modified: Mon, 22 Jun 2026 18:05:16 GMT  
		Size: 140.6 MB (140595108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e936838c3461d29353d73d62e9d743ac1ade0b4ab139e66303b2f97bcebd3d`  
		Last Modified: Mon, 22 Jun 2026 18:05:10 GMT  
		Size: 29.3 KB (29335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:0769c99c8d679c211325f2092490a3b5f78416dfc1137fc13236975014813e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9069611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1247c51e8f9f1810fa1bffdd55c24d43f777d8d003db9f04d8a3b125fdd8e59c`

```dockerfile
```

-	Layers:
	-	`sha256:7c172b80c805c79fbae15b8b21879b6941d8b582d62be825bdcd9d4fa09b60ca`  
		Last Modified: Mon, 22 Jun 2026 18:05:09 GMT  
		Size: 9.0 MB (9039115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6eb0074d67f7b199790a642c87d37b5707ac2b00f878ea12135d9b601991ef8`  
		Last Modified: Mon, 22 Jun 2026 18:05:08 GMT  
		Size: 30.5 KB (30496 bytes)  
		MIME: application/vnd.in-toto+json
