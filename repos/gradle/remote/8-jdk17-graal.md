## `gradle:8-jdk17-graal`

```console
$ docker pull gradle@sha256:c40eb2082d331cffbe0c1f9373f1bd08ed0cb3228491d7168f1537ac9f3de108
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk17-graal` - linux; amd64

```console
$ docker pull gradle@sha256:2c1d0380dad620364c0c91b22abc5f13df37a5b9a3228e6fa1e41a8582f0079d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.1 MB (607061122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1194b9b48bf9282ad27290818daa65cd6094956c7b15f2d77a62f3895dba605e`
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
# Tue, 07 Apr 2026 01:54:36 GMT
CMD ["gradle"]
# Tue, 07 Apr 2026 01:54:36 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 07 Apr 2026 01:54:36 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 07 Apr 2026 01:54:36 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 07 Apr 2026 01:54:36 GMT
WORKDIR /home/gradle
# Tue, 07 Apr 2026 01:55:11 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 07 Apr 2026 01:55:11 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 07 Apr 2026 01:55:11 GMT
ENV JAVA_VERSION=17.0.9
# Tue, 07 Apr 2026 01:55:20 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Tue, 07 Apr 2026 01:55:20 GMT
ENV GRADLE_VERSION=8.14.4
# Tue, 07 Apr 2026 01:55:20 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Tue, 07 Apr 2026 01:55:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 07 Apr 2026 01:55:22 GMT
USER gradle
# Tue, 07 Apr 2026 01:55:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 07 Apr 2026 01:55:23 GMT
USER root
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a47a81fe518aad7f9f492334ebeb8e36cf978bd2f2a7d170b3a01157202877`  
		Last Modified: Tue, 07 Apr 2026 01:55:57 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c05e5fc5547cec0f8b8851c12b1eda0e547f29355aa4d3783d05ed3151d344`  
		Last Modified: Tue, 07 Apr 2026 01:56:04 GMT  
		Size: 148.8 MB (148819027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8a44e52d6f5d6d015213a1009ec5cb163d9fe86ae3147e327d5a2ea901fde`  
		Last Modified: Tue, 07 Apr 2026 01:56:07 GMT  
		Size: 291.1 MB (291064148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eef8d001ef2968558df4bf3092d1d48512daf87c9b6fcebade549abcee53b77`  
		Last Modified: Tue, 07 Apr 2026 01:56:04 GMT  
		Size: 137.4 MB (137388265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd582aa78bac156d44f9e4ac34d241022a1eaf92a6d40a9b2136865c4580e81`  
		Last Modified: Tue, 07 Apr 2026 01:55:58 GMT  
		Size: 54.9 KB (54905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:bfcc4e69486faca5e6609450af5109cfd5452742e84e6a5d31db95b5c8661dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9037287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb34c9c1327e39904a3bc122643f880af470f1f8cc4b7c59047db36481d8021`

```dockerfile
```

-	Layers:
	-	`sha256:042ab175f68e9e8aabe16d4f91008fce85e55a7888eb20faf7ad05b58b7f5128`  
		Last Modified: Tue, 07 Apr 2026 01:55:58 GMT  
		Size: 9.0 MB (9008976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89c2c934d7ffb156c4d307e6fa64aa53156b593ef1b4259c0434549866935c4f`  
		Last Modified: Tue, 07 Apr 2026 01:55:57 GMT  
		Size: 28.3 KB (28311 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:79b022b9df053ecc03ada449bb593157f40bc48648e31141d0688f6809ac71d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.7 MB (593743288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405b6cfb8a036e34d464f4a4f80e111d02324926de0ae3b4e96e3867691f9894`
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
# Tue, 07 Apr 2026 01:58:08 GMT
CMD ["gradle"]
# Tue, 07 Apr 2026 01:58:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 07 Apr 2026 01:58:08 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 07 Apr 2026 01:58:08 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 07 Apr 2026 01:58:08 GMT
WORKDIR /home/gradle
# Tue, 07 Apr 2026 01:58:46 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 07 Apr 2026 01:58:46 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 07 Apr 2026 01:58:46 GMT
ENV JAVA_VERSION=17.0.9
# Tue, 07 Apr 2026 01:58:55 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Tue, 07 Apr 2026 01:58:55 GMT
ENV GRADLE_VERSION=8.14.4
# Tue, 07 Apr 2026 01:58:55 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Tue, 07 Apr 2026 01:58:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 07 Apr 2026 01:58:57 GMT
USER gradle
# Tue, 07 Apr 2026 01:58:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 07 Apr 2026 01:58:58 GMT
USER root
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768b3e9ae7bd66d53314db99d1828d312f14dae2c38b988bbd9aa397a999daae`  
		Last Modified: Tue, 07 Apr 2026 01:59:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e6c66f72596c1196b9e6c268fb53bc74db037f0b4ee586aeb991e2490e38ff`  
		Last Modified: Tue, 07 Apr 2026 01:59:40 GMT  
		Size: 143.9 MB (143918226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe3429be9953269527950cb29ad8934d23590a4a5240c74fa078829652faaa2`  
		Last Modified: Tue, 07 Apr 2026 01:59:43 GMT  
		Size: 283.5 MB (283501872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ec808e20d28e69099dfd7e926b7b00dadf21fee8f2185624cd1f0ad9af5b4d`  
		Last Modified: Tue, 07 Apr 2026 01:59:39 GMT  
		Size: 137.4 MB (137388268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8216919ff79527e00d3cafc8502ddb02aff51a49a2d64001462f0856dbfd128`  
		Last Modified: Tue, 07 Apr 2026 01:59:33 GMT  
		Size: 59.5 KB (59529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:0555f3aface704fb62cf1cd43cfe1db71ed768408f79912e056d5df4d926cde1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9033028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc51f108d7caba87baa3ee34207ca427a1ba440e7a46775290c860059014ca8`

```dockerfile
```

-	Layers:
	-	`sha256:1019a89dbba8d0dd0292fc81121ecb754bce5816e0d0c8ac21ce78ac94da7d2a`  
		Last Modified: Tue, 07 Apr 2026 01:59:33 GMT  
		Size: 9.0 MB (9004529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20b7e432c7868ba16e4580661b9c9f9fde288d20598b84fb22f8f47a0c86ae5d`  
		Last Modified: Tue, 07 Apr 2026 01:59:32 GMT  
		Size: 28.5 KB (28499 bytes)  
		MIME: application/vnd.in-toto+json
