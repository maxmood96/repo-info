## `gradle:9-graal-noble`

```console
$ docker pull gradle@sha256:3a2af70620cfa46c4d06d780651a679da0e8a627dcf81303b27e7682a79b9fb2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:1fc5686531e228f3fb8e37c3ec27fd29304e0c90a82f0f0e2cae01cef3f1f5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.5 MB (664464621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc953467332db554991cfb9814a1d87d94aec7fc3481b27a9cf5a38125931f45`
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
# Mon, 29 Jun 2026 17:11:17 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:11:17 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:11:17 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:11:17 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:11:17 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:11:47 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:11:47 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Mon, 29 Jun 2026 17:11:47 GMT
ENV JAVA_VERSION=25.0.2
# Mon, 29 Jun 2026 17:11:58 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e0be791c8fda4d03b6b0a0cb824fef3149736170057b3a515252b44419606af0     && GRAALVM_AARCH64_DOWNLOAD_SHA256=b4580d9f223d0a4b3a1757e58b18ff4c1db950e67e105fc5cb741457d2384a71     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Mon, 29 Jun 2026 17:11:58 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:11:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:12:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:12:00 GMT
USER gradle
# Mon, 29 Jun 2026 17:12:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:12:01 GMT
USER root
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf3b7b21bd0523e4c6a7148c56582e074d13c2d5755a1105249fea6e755eb62`  
		Last Modified: Mon, 29 Jun 2026 17:12:41 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb729c8f4fcd8dc2b23024d23309de5fff8d1c4d1cded5bc37c9c45492e1a77`  
		Last Modified: Mon, 29 Jun 2026 17:12:49 GMT  
		Size: 153.2 MB (153214943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1553189e433985c9e0b1eaf32ae6631fabe9100feeb2f206d2f9ce9a5a0c5806`  
		Last Modified: Mon, 29 Jun 2026 17:12:53 GMT  
		Size: 340.9 MB (340893914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f92369c4e64e19c62dc10ef1e17f4c12d2fa3c3235cbebbdb2be7abd786328`  
		Last Modified: Mon, 29 Jun 2026 17:12:49 GMT  
		Size: 140.6 MB (140596026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fb44280f4ded6055a4252684bfd688d0fddf56d7326cdcd9c2141a3dc3d0e3`  
		Last Modified: Mon, 29 Jun 2026 17:12:43 GMT  
		Size: 25.6 KB (25613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:83c692602ebb353bcf48918ce1c3aad21cfcbc8cfc4fd645c36927d8c255bd23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9074365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12925caf400b0ee1405dedf08f000041a000e0e67c1f755ab40194a49b392a80`

```dockerfile
```

-	Layers:
	-	`sha256:58e9dbc429630cadecd4f08d90a1362a656b31c0e19ae91ef6d40fc860617116`  
		Last Modified: Mon, 29 Jun 2026 17:12:42 GMT  
		Size: 9.0 MB (9044129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6c1d9a75bde28e6e206b8139e6d2bfced2cc6f0fbbe68df266b8d1bbe757872`  
		Last Modified: Mon, 29 Jun 2026 17:12:41 GMT  
		Size: 30.2 KB (30236 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:21b778a0f67229afb8fd67c46ae00988308efb16c330d54abb8751d5dd490eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.6 MB (633565976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f295ddab29c9a8726e1845908f80e92a43064404210d7cec4b16339008210461`
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
# Mon, 29 Jun 2026 17:11:11 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:11:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:11:11 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:11:11 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:11:11 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:11:40 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:11:40 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Mon, 29 Jun 2026 17:11:40 GMT
ENV JAVA_VERSION=25.0.2
# Mon, 29 Jun 2026 17:11:50 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e0be791c8fda4d03b6b0a0cb824fef3149736170057b3a515252b44419606af0     && GRAALVM_AARCH64_DOWNLOAD_SHA256=b4580d9f223d0a4b3a1757e58b18ff4c1db950e67e105fc5cb741457d2384a71     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Mon, 29 Jun 2026 17:11:50 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:11:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:11:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:11:52 GMT
USER gradle
# Mon, 29 Jun 2026 17:11:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:11:53 GMT
USER root
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f77f2ab3784325c0bbca0f53e633090a52377e5c568794bb662969a739960d`  
		Last Modified: Mon, 29 Jun 2026 17:12:29 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacefda1e14b47c601c3f4d6b90f1c7162b42f4c505364849b0e293032f31f53`  
		Last Modified: Mon, 29 Jun 2026 17:12:36 GMT  
		Size: 148.1 MB (148076229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0828d8972d2bb18218ac52d01840edd59c8f5fd83b622305b52479b4cb5b9ba8`  
		Last Modified: Mon, 29 Jun 2026 17:12:40 GMT  
		Size: 316.0 MB (315986664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a4e590003b05e5232263f3f76b942ea12069a142fedeca2e01019c271d75b1`  
		Last Modified: Mon, 29 Jun 2026 17:12:36 GMT  
		Size: 140.6 MB (140596024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a9cb3f14f2c7a060518fdc7a2b500b943b130b100d0a564af4331c0c84074c`  
		Last Modified: Mon, 29 Jun 2026 17:12:30 GMT  
		Size: 29.3 KB (29335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:4a5cba68008f89fef0f6892c135b94900cb725b297401bf7c3d6bb7a8e475406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9069617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44a8c49f74a5a5fff5d78a2abb25e9ef57b870106ae27e28affe61a18cd915c`

```dockerfile
```

-	Layers:
	-	`sha256:4e405c42e28cc5868aabecaa55731d856b71a35a4e6a026bc5efba7942cd4809`  
		Last Modified: Mon, 29 Jun 2026 17:12:29 GMT  
		Size: 9.0 MB (9039121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66a58cf88f8ffbbf7e3305f721c4ccdf52206cd7b3139087a1ad9ea6477b500f`  
		Last Modified: Mon, 29 Jun 2026 17:12:29 GMT  
		Size: 30.5 KB (30496 bytes)  
		MIME: application/vnd.in-toto+json
