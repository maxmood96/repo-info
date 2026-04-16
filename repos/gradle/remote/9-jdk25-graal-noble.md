## `gradle:9-jdk25-graal-noble`

```console
$ docker pull gradle@sha256:e787849f01335edae433e236a0d66c4a60be417ce7dc9c2ae7d546e6424bc5f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk25-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:7d73e3fbc24539b0f06ae7c9751f1af3f28df6f355ac888a2590c63379314256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.8 MB (656773345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d397d2cbc4e373cd09064b00997590eedeeb74de7510b6251a8d6adf80419c`
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
# Wed, 15 Apr 2026 20:35:40 GMT
CMD ["gradle"]
# Wed, 15 Apr 2026 20:35:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 15 Apr 2026 20:35:40 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 15 Apr 2026 20:35:40 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 15 Apr 2026 20:35:40 GMT
WORKDIR /home/gradle
# Wed, 15 Apr 2026 20:36:13 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 15 Apr 2026 20:36:13 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 15 Apr 2026 20:36:13 GMT
ENV JAVA_VERSION=25.0.2
# Wed, 15 Apr 2026 20:36:26 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e0be791c8fda4d03b6b0a0cb824fef3149736170057b3a515252b44419606af0     && GRAALVM_AARCH64_DOWNLOAD_SHA256=b4580d9f223d0a4b3a1757e58b18ff4c1db950e67e105fc5cb741457d2384a71     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Wed, 15 Apr 2026 20:36:26 GMT
ENV GRADLE_VERSION=9.4.1
# Wed, 15 Apr 2026 20:36:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Wed, 15 Apr 2026 20:36:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 15 Apr 2026 20:36:29 GMT
USER gradle
# Wed, 15 Apr 2026 20:36:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 15 Apr 2026 20:36:29 GMT
USER root
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8a29c2eb8d7bf14b8c14c22f6bc79046c06c23953a63a77bedc038aad28a33`  
		Last Modified: Wed, 15 Apr 2026 20:37:05 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f4239e23ac9db8626204de924dd60c85eec23e8a65d8428af4c2ec5223fe5b`  
		Last Modified: Wed, 15 Apr 2026 20:37:12 GMT  
		Size: 148.3 MB (148311179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ec2aedcfa9e68feb9750714f8b6e4d6acd47d01b8bad407f88e6146a2276d8`  
		Last Modified: Wed, 15 Apr 2026 20:37:17 GMT  
		Size: 340.9 MB (340893931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1452254d74dbead761fcfa15de19471b55f8db8792845c140933132cca1d1614`  
		Last Modified: Wed, 15 Apr 2026 20:37:12 GMT  
		Size: 137.8 MB (137808332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4647862188a6ec419db86dd273ef9a453ab5ad1b76abea5b590bac9f288dab7d`  
		Last Modified: Wed, 15 Apr 2026 20:37:06 GMT  
		Size: 25.6 KB (25607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:235c0e9d8e4a885566e562a58bce10ba3b86c534c5fa8124109b5f324ceb7461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9055832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5265c1dd2448729845944a0dae58aeed76311f9c4865d546d65a5e807cebd243`

```dockerfile
```

-	Layers:
	-	`sha256:a996f69818af70829e557915c8acad93724f72085e0235de660ee060b29bc98a`  
		Last Modified: Wed, 15 Apr 2026 20:37:05 GMT  
		Size: 9.0 MB (9021892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f0576c605e400f8caec60537abbade21c732efea86a343326201beccd149c0e`  
		Last Modified: Wed, 15 Apr 2026 20:37:05 GMT  
		Size: 33.9 KB (33940 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk25-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:bcdf461675ed0ea1d305e2fe13400b99f3500c37f2850c86b7f5675cd8198d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.1 MB (626112477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bb067c0eabb23e93195057ee85ccb62a5ffd4bd7cfe7212a5e4c04a4fdeab8`
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
# Wed, 15 Apr 2026 20:35:39 GMT
CMD ["gradle"]
# Wed, 15 Apr 2026 20:35:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 15 Apr 2026 20:35:39 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 15 Apr 2026 20:35:39 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 15 Apr 2026 20:35:39 GMT
WORKDIR /home/gradle
# Wed, 15 Apr 2026 20:36:13 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 15 Apr 2026 20:36:13 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Wed, 15 Apr 2026 20:36:13 GMT
ENV JAVA_VERSION=25.0.2
# Wed, 15 Apr 2026 20:36:23 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e0be791c8fda4d03b6b0a0cb824fef3149736170057b3a515252b44419606af0     && GRAALVM_AARCH64_DOWNLOAD_SHA256=b4580d9f223d0a4b3a1757e58b18ff4c1db950e67e105fc5cb741457d2384a71     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Wed, 15 Apr 2026 20:36:23 GMT
ENV GRADLE_VERSION=9.4.1
# Wed, 15 Apr 2026 20:36:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Wed, 15 Apr 2026 20:36:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 15 Apr 2026 20:36:25 GMT
USER gradle
# Wed, 15 Apr 2026 20:36:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 15 Apr 2026 20:36:26 GMT
USER root
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083ead1cc319f4fd6e92e1481242c2cbe623d1b685f03fce4b7879918a3474b6`  
		Last Modified: Wed, 15 Apr 2026 20:37:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefe4d41b14194e8c27ed82f67f548bbc3f34995658f16cbb859b6f710b631b4`  
		Last Modified: Wed, 15 Apr 2026 20:37:13 GMT  
		Size: 143.4 MB (143410937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bc129ccb6e809782f4fedf26b97e1f1ef6c74e3c61d71507c678feb2e61bbe`  
		Last Modified: Wed, 15 Apr 2026 20:37:20 GMT  
		Size: 316.0 MB (315986766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9350a6bd7a9d964b2084ede92464d79fbde2f99a4920f57790cfa5aac19fff6`  
		Last Modified: Wed, 15 Apr 2026 20:37:13 GMT  
		Size: 137.8 MB (137808332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e00d6dcdc8ef3bb8ccb4f8a1eab020533a6d06cf1820c487e5e8db3219aed3`  
		Last Modified: Wed, 15 Apr 2026 20:37:04 GMT  
		Size: 29.3 KB (29338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:c7682815679076a33db171a1db0705854b92bbeecdfdfe3bb7a1c941cf1bb695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9051372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbe600eccb7913f92b1c004b68a6e1f64022b3116d2a3c822754e43a7edb9ce`

```dockerfile
```

-	Layers:
	-	`sha256:7cf16211f273bb0956763ce2eb5df14fa55fbb6288da34a9782e0730b0920679`  
		Last Modified: Wed, 15 Apr 2026 20:37:04 GMT  
		Size: 9.0 MB (9017028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93971f125a12f2ac4ee54c125419479eaf7bdb75279cf99b4d1654e9ce26e11c`  
		Last Modified: Wed, 15 Apr 2026 20:37:03 GMT  
		Size: 34.3 KB (34344 bytes)  
		MIME: application/vnd.in-toto+json
