## `gradle:9-jdk17-graal`

```console
$ docker pull gradle@sha256:a3b9c68f4be4eacf60bb7abd462e370de4fb16537220d34cba0ff1e652836693
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk17-graal` - linux; amd64

```console
$ docker pull gradle@sha256:e78d07080fc0af7758d4565207f3780b2242069a82d5e3e6e25f1d175e72b9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.5 MB (607451647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd3e59a2201ec15ce4c386657fe6a1e39526856bfe98ab685c2a85842fd2838`
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
# Tue, 07 Apr 2026 01:53:49 GMT
CMD ["gradle"]
# Tue, 07 Apr 2026 01:53:49 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 07 Apr 2026 01:53:49 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 07 Apr 2026 01:53:49 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 07 Apr 2026 01:53:49 GMT
WORKDIR /home/gradle
# Tue, 07 Apr 2026 01:54:29 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 07 Apr 2026 01:54:29 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 07 Apr 2026 01:54:29 GMT
ENV JAVA_VERSION=17.0.9
# Tue, 07 Apr 2026 01:54:39 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Tue, 07 Apr 2026 01:54:39 GMT
ENV GRADLE_VERSION=9.4.1
# Tue, 07 Apr 2026 01:54:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Tue, 07 Apr 2026 01:54:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 07 Apr 2026 01:54:41 GMT
USER gradle
# Tue, 07 Apr 2026 01:54:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 07 Apr 2026 01:54:42 GMT
USER root
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cd1c2b20a6e69f99a57bd848fc0fe4a8ad9b5ca096a6a66a13b2d42729829e`  
		Last Modified: Tue, 07 Apr 2026 01:55:17 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af84b8c6d4a374bd4f713bddf625d3e4fd8803807a42977e76efd46a0df9d1b2`  
		Last Modified: Tue, 07 Apr 2026 01:55:25 GMT  
		Size: 148.8 MB (148818864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223e739cbb27d919f4d313fe3eeb74fd5585b6086224b58286bdb0aa8206487d`  
		Last Modified: Tue, 07 Apr 2026 01:55:28 GMT  
		Size: 291.1 MB (291064053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a913b689986a5246b6c135f61e64c2bbbff5dc786ae4143cc55af5775655645c`  
		Last Modified: Tue, 07 Apr 2026 01:55:25 GMT  
		Size: 137.8 MB (137808328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936003b911f4015144ea838f03e41083baf395dd613e97a29c327ff97e6f39d1`  
		Last Modified: Tue, 07 Apr 2026 01:55:18 GMT  
		Size: 25.6 KB (25626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:4eaecbc9d481efb3b10b7d8dd8adea35bc93cd3faf40cf254f684c0a5942fdc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9024417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d345e9bf054637c3678b652ddac6065b4c3020039054fef1e7731016891d969d`

```dockerfile
```

-	Layers:
	-	`sha256:5a23c6c1d4be271fc1d14c2e5f8faa6d0a814ae82c0a80254abd6352320832c0`  
		Last Modified: Tue, 07 Apr 2026 01:55:18 GMT  
		Size: 9.0 MB (8995365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11b8b74eaa354f1c79374f262c819faeb1d26b177ee6f75bef17262799585c92`  
		Last Modified: Tue, 07 Apr 2026 01:55:17 GMT  
		Size: 29.1 KB (29052 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:44e363021c7ad1cc17a4877fb56466996a160ab48fad0b67d41812f57f296a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.1 MB (594133628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85aaed0d5e55fdf2dc60c3b1b2c479b128acec54633377c58c096ca908110d41`
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
# Tue, 07 Apr 2026 01:56:30 GMT
CMD ["gradle"]
# Tue, 07 Apr 2026 01:56:30 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 07 Apr 2026 01:56:30 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 07 Apr 2026 01:56:30 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 07 Apr 2026 01:56:30 GMT
WORKDIR /home/gradle
# Tue, 07 Apr 2026 01:57:04 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 07 Apr 2026 01:57:04 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 07 Apr 2026 01:57:04 GMT
ENV JAVA_VERSION=17.0.9
# Tue, 07 Apr 2026 01:57:14 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Tue, 07 Apr 2026 01:57:14 GMT
ENV GRADLE_VERSION=9.4.1
# Tue, 07 Apr 2026 01:57:14 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Tue, 07 Apr 2026 01:57:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 07 Apr 2026 01:57:17 GMT
USER gradle
# Tue, 07 Apr 2026 01:57:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 07 Apr 2026 01:57:17 GMT
USER root
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ccdc543e4abe6dfc6b959aa0bb745e7e456e8532e71545440bfaacae2a2143`  
		Last Modified: Tue, 07 Apr 2026 01:57:50 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcd2f342984c59549397e6ba883b274c4c75a7e1668e5ba3f1efffbda0cd77d`  
		Last Modified: Tue, 07 Apr 2026 01:57:58 GMT  
		Size: 143.9 MB (143918748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5dbf2fd5c0bc33b5cfbfd0de8ad65c58524f5a87a0af641a3ab7bcea29c612`  
		Last Modified: Tue, 07 Apr 2026 01:58:01 GMT  
		Size: 283.5 MB (283501825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d57d47297ffb54cad579b73430a1d8d8e5bc1f41f09f30fa443092052a4b736`  
		Last Modified: Tue, 07 Apr 2026 01:57:57 GMT  
		Size: 137.8 MB (137808329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ccf504c229bd5a0cdbb6e213f1b86a716cd10fdd8c9756fcac7621ef5c348d`  
		Last Modified: Tue, 07 Apr 2026 01:57:52 GMT  
		Size: 29.3 KB (29333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:5acda7531ea0da660b734b3367135d3a8d522e728c91a6f3e97630c87b18988f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9020206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7aba55ce89d93c68a0982ec5f706f17c414d599c92d3228d53d8f31b89a799`

```dockerfile
```

-	Layers:
	-	`sha256:dda5f20b5a9e7a03690b7248a6fa81acf3640b1f37b65708c2164d688eb4c838`  
		Last Modified: Tue, 07 Apr 2026 01:57:51 GMT  
		Size: 9.0 MB (8990942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ad8c39d5933bf7146722c57e93085f9debc457ab78a534821eead2d2c3dd616`  
		Last Modified: Tue, 07 Apr 2026 01:57:50 GMT  
		Size: 29.3 KB (29264 bytes)  
		MIME: application/vnd.in-toto+json
