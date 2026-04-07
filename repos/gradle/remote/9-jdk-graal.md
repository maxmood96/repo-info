## `gradle:9-jdk-graal`

```console
$ docker pull gradle@sha256:e846831db101ab809aa205de16b4c7ccc2b9b09cd6628c02e3235b461ac3f4cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk-graal` - linux; amd64

```console
$ docker pull gradle@sha256:4639fef80d942d8f5fb3a136c39000ffb1c907bf01bc010a39041f18c33c8c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.3 MB (657281514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8fe4a61a900f3d3856ee4cd343b22e41902388c08b8ae08f3c84a14197b866c`
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
# Tue, 07 Apr 2026 01:52:57 GMT
CMD ["gradle"]
# Tue, 07 Apr 2026 01:52:57 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 07 Apr 2026 01:52:57 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 07 Apr 2026 01:52:57 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 07 Apr 2026 01:52:57 GMT
WORKDIR /home/gradle
# Tue, 07 Apr 2026 01:53:31 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 07 Apr 2026 01:53:31 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 07 Apr 2026 01:53:31 GMT
ENV JAVA_VERSION=25.0.2
# Tue, 07 Apr 2026 01:53:42 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e0be791c8fda4d03b6b0a0cb824fef3149736170057b3a515252b44419606af0     && GRAALVM_AARCH64_DOWNLOAD_SHA256=b4580d9f223d0a4b3a1757e58b18ff4c1db950e67e105fc5cb741457d2384a71     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 07 Apr 2026 01:53:42 GMT
ENV GRADLE_VERSION=9.4.1
# Tue, 07 Apr 2026 01:53:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Tue, 07 Apr 2026 01:53:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 07 Apr 2026 01:53:44 GMT
USER gradle
# Tue, 07 Apr 2026 01:53:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 07 Apr 2026 01:53:44 GMT
USER root
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6ba57d5c268c99a26b1a1bd7836f0058f6a097015a2c2a3402c312b19bc231`  
		Last Modified: Tue, 07 Apr 2026 01:54:21 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cddd769f113b9ecab15c8d2a88f10afa4b75bbb951f12f8fd0bf88bd0222a79`  
		Last Modified: Tue, 07 Apr 2026 01:54:31 GMT  
		Size: 148.8 MB (148818896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28550b9778d87830e03b41c2b60b32f6d0d058bac6572f1f54ee2f2dff9e062`  
		Last Modified: Tue, 07 Apr 2026 01:54:36 GMT  
		Size: 340.9 MB (340893911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e7ddd8d944c8ab889c32638502e2ae5d5c096d6ab97bf2eec3cbaf4b37d40e`  
		Last Modified: Tue, 07 Apr 2026 01:54:31 GMT  
		Size: 137.8 MB (137808333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603272e59580aed60a98a4f222f0e844c04a7150a4c026becd6fd657b26107f5`  
		Last Modified: Tue, 07 Apr 2026 01:54:22 GMT  
		Size: 25.6 KB (25600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:cb3dfbeb8ec05a9be58a7d5128743ab2494af1a1ee20826f239dafbdf66d5e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9055832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce2ade9b4e54d39262b4c30c55905a265e1b8719ef57e3628e74c8576902d94`

```dockerfile
```

-	Layers:
	-	`sha256:d73e23d741d7bef80a6fdc1e4e899116238460cd71aea9c2b74e060f0555c7c2`  
		Last Modified: Tue, 07 Apr 2026 01:54:21 GMT  
		Size: 9.0 MB (9021892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:970595bc0f3bb5b5e895e67bbc45b6d80a438b869194be78112c2b512b52ba24`  
		Last Modified: Tue, 07 Apr 2026 01:54:21 GMT  
		Size: 33.9 KB (33940 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:83289c4700ceda6a802b2e6233fe6e05f3a3cd2a111331ad5016f5b7e0b3754a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.6 MB (626618354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72d467d124809b4531e5577854242a8cc400aa6ce02014d54a0aa472fb600bd`
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
# Tue, 07 Apr 2026 01:56:19 GMT
CMD ["gradle"]
# Tue, 07 Apr 2026 01:56:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 07 Apr 2026 01:56:19 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 07 Apr 2026 01:56:19 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 07 Apr 2026 01:56:19 GMT
WORKDIR /home/gradle
# Tue, 07 Apr 2026 01:56:54 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 07 Apr 2026 01:56:54 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 07 Apr 2026 01:56:54 GMT
ENV JAVA_VERSION=25.0.2
# Tue, 07 Apr 2026 01:57:05 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e0be791c8fda4d03b6b0a0cb824fef3149736170057b3a515252b44419606af0     && GRAALVM_AARCH64_DOWNLOAD_SHA256=b4580d9f223d0a4b3a1757e58b18ff4c1db950e67e105fc5cb741457d2384a71     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 07 Apr 2026 01:57:05 GMT
ENV GRADLE_VERSION=9.4.1
# Tue, 07 Apr 2026 01:57:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Tue, 07 Apr 2026 01:57:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 07 Apr 2026 01:57:07 GMT
USER gradle
# Tue, 07 Apr 2026 01:57:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 07 Apr 2026 01:57:08 GMT
USER root
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d78eafd1309a6577ef0b5e0d9dcf18342237d25567f52e4d78c5704c4c9bec8`  
		Last Modified: Tue, 07 Apr 2026 01:57:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c482dcc6012d8a14ee38ac0dd3abcfd2d604a09117217610cbd7d261effba85d`  
		Last Modified: Tue, 07 Apr 2026 01:57:50 GMT  
		Size: 143.9 MB (143918564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9465db33ae947e36d799bc51c2c71d05760b676d83bc75ab0576ed50b8590bc5`  
		Last Modified: Tue, 07 Apr 2026 01:57:53 GMT  
		Size: 316.0 MB (315986733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3144136dd553e1e7399d7d4080eea42d17d15807b1d6298803f2a89715cf4b`  
		Last Modified: Tue, 07 Apr 2026 01:57:50 GMT  
		Size: 137.8 MB (137808330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78d2d8825e24468ceead7d01d12a73b107035c527ced0b09350bca6dfc2959d`  
		Last Modified: Tue, 07 Apr 2026 01:57:45 GMT  
		Size: 29.3 KB (29335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:a8cdb6bf00dc717760131b42063a864d32c395b55760ee18457b1e8dd0af88d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9051372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0267078e3459d6a6aa0ebac50090d3e7980f9551026eb4b3b873c0b3486abc`

```dockerfile
```

-	Layers:
	-	`sha256:2e3292921721836a8e0ac596e724cab5a94584e50a2d1734c2b6bba1b7ef4080`  
		Last Modified: Tue, 07 Apr 2026 01:57:44 GMT  
		Size: 9.0 MB (9017028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30c58f537f2959daa260622b8218701b8bfb981cc1f2c4e659d4e79d23b45dec`  
		Last Modified: Tue, 07 Apr 2026 01:57:43 GMT  
		Size: 34.3 KB (34344 bytes)  
		MIME: application/vnd.in-toto+json
