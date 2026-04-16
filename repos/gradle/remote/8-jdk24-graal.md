## `gradle:8-jdk24-graal`

```console
$ docker pull gradle@sha256:468bdb9a462bec54842bfd88beb5fc2c6497fecbc9310c3dee3a08a4d38aa343
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk24-graal` - linux; amd64

```console
$ docker pull gradle@sha256:04f6bfc1b647457cc8a6e80d2454ebb13eec853240203694d04f0b95d2baaca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.7 MB (651710600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa5712747bc41a60b2fd1d3bd806345961eb6895d9921fa31bcad4f0c6e6c2a`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:37:19 GMT
CMD ["gradle"]
# Wed, 15 Apr 2026 20:37:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 15 Apr 2026 20:37:19 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 15 Apr 2026 20:37:19 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 15 Apr 2026 20:37:19 GMT
WORKDIR /home/gradle
# Wed, 15 Apr 2026 20:37:51 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 15 Apr 2026 20:37:51 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 15 Apr 2026 20:37:51 GMT
ENV JAVA_VERSION=24.0.2
# Wed, 15 Apr 2026 20:38:05 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=6d62846c826ddb9307deec71e7661c26fa5a5e3985d7bb9005ea42163a390720     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c54d951a858791483d58270ecbc0946f28c4742c7fac74a4ebb2764bbf66d6f5     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Wed, 15 Apr 2026 20:38:05 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 15 Apr 2026 20:38:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 15 Apr 2026 20:38:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 15 Apr 2026 20:38:07 GMT
USER gradle
# Wed, 15 Apr 2026 20:38:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 15 Apr 2026 20:38:07 GMT
USER root
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562b43cbb37604ec1b2e5c544c7109a14187185726b6faf04759b0f854605a44`  
		Last Modified: Wed, 15 Apr 2026 20:38:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced1415cdd8c6d64ece2d32bf53dd41dd7c1a8498db93684ccc276ac66c5623d`  
		Last Modified: Wed, 15 Apr 2026 20:38:54 GMT  
		Size: 148.3 MB (148311082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626328b42060f73f9bcc7944ebce977bf21b7ece19b3bf94516e79c24b5bb225`  
		Last Modified: Wed, 15 Apr 2026 20:38:58 GMT  
		Size: 336.2 MB (336222061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68914c8b923d83434514ad7d3b4049dda5655027dda6baa24b33f5ecdc230ade`  
		Last Modified: Wed, 15 Apr 2026 20:38:54 GMT  
		Size: 137.4 MB (137388269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f785e90c01517dcadff99f000cb4efbf4a0d6bcfc3560605a63c54b0fa43e1e6`  
		Last Modified: Wed, 15 Apr 2026 20:38:47 GMT  
		Size: 54.9 KB (54893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk24-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:2987ccadb8ca88e9a14aad7aea9f42bbb77c842004321ae08dcdccd9e24fe1f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9051782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48746a9138ff0bcb25601b23aa255d5a8bdbf9b576f4a96b8bae0ec73628319c`

```dockerfile
```

-	Layers:
	-	`sha256:2d393cc83a2e5b0c8f0dc828b21efec7d16133f5e69e69cc9f6607b64f004cb3`  
		Last Modified: Wed, 15 Apr 2026 20:38:47 GMT  
		Size: 9.0 MB (9023263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0959399f92b543f46f56a076ee38d276cf5e54282e0365aca81c97ed2f2093b`  
		Last Modified: Wed, 15 Apr 2026 20:38:45 GMT  
		Size: 28.5 KB (28519 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk24-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:820e5cf429ade6d1dffae51298cc68d23080b3c12ca121b69dd485aac68daa6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.2 MB (620162093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2db1069bfaa39b04a4d35e52e1d9135c7ed61ac99a11c9fc91377a0de11c954`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:37:41 GMT
CMD ["gradle"]
# Wed, 15 Apr 2026 20:37:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 15 Apr 2026 20:37:41 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 15 Apr 2026 20:37:41 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 15 Apr 2026 20:37:41 GMT
WORKDIR /home/gradle
# Wed, 15 Apr 2026 20:38:20 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 15 Apr 2026 20:38:20 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 15 Apr 2026 20:38:20 GMT
ENV JAVA_VERSION=24.0.2
# Wed, 15 Apr 2026 20:38:36 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=6d62846c826ddb9307deec71e7661c26fa5a5e3985d7bb9005ea42163a390720     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c54d951a858791483d58270ecbc0946f28c4742c7fac74a4ebb2764bbf66d6f5     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Wed, 15 Apr 2026 20:38:36 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 15 Apr 2026 20:38:36 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 15 Apr 2026 20:38:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 15 Apr 2026 20:38:39 GMT
USER gradle
# Wed, 15 Apr 2026 20:38:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 15 Apr 2026 20:38:39 GMT
USER root
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6010249d83f008d2bda38b36acfc164e26fdfbd823efa137dd0dd715376e61`  
		Last Modified: Wed, 15 Apr 2026 20:39:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f3965c646b4236a2e8867bf52e47150ec7cc9ab1c9a39d64020b6bfd38bb35`  
		Last Modified: Wed, 15 Apr 2026 20:39:23 GMT  
		Size: 143.4 MB (143411683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab5c0ad02c0c624cd9175a2577ede8c01f5a39628e6c1646f070b83c52f5781`  
		Last Modified: Wed, 15 Apr 2026 20:39:26 GMT  
		Size: 310.4 MB (310425502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33447d2d545d6780b569143fc776b4dc40b0728f99027036ae85aba5ed276424`  
		Last Modified: Wed, 15 Apr 2026 20:39:23 GMT  
		Size: 137.4 MB (137388269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083ce0da89d24df764d87242f67ab5162ee86db5e3f3fcdea3b0af1629e4a26e`  
		Last Modified: Wed, 15 Apr 2026 20:39:16 GMT  
		Size: 59.5 KB (59528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk24-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:d4adac95a1a7d68f5d77fa347d1d2f6b460433e8decd1508d31fecf8aeee07b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9046901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ad693245b505a170b1c4003fb4877776f3c5248afc7cc39ea78e35a16c1cc6`

```dockerfile
```

-	Layers:
	-	`sha256:71d12de673384fe8fec60a72270de45ac40efa78e9a46b16623f9cf9a9f6f983`  
		Last Modified: Wed, 15 Apr 2026 20:39:15 GMT  
		Size: 9.0 MB (9018183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:723e7676d5bc95a9ad122bf3ff336a850440bd2ab4d323138a62e4a6cea6fb67`  
		Last Modified: Wed, 15 Apr 2026 20:39:15 GMT  
		Size: 28.7 KB (28718 bytes)  
		MIME: application/vnd.in-toto+json
