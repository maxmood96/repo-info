## `gradle:9-jdk17-graal-noble`

```console
$ docker pull gradle@sha256:2f27392e5c197fa72a304ee6b1d9ef1473703c7f25b4ea605d5418cd5a472a50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk17-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:d1b78c937dc5d60aea0781e6f8b8803cd2f009f261b23260276694eb5cc6132c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.4 MB (606387163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d6ca3b5de005a56cdd320ad9a0c1bca2b368bb47f4c197af4e50a1b9b74a20`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 30 Sep 2025 09:31:25 GMT
ARG RELEASE
# Tue, 30 Sep 2025 09:31:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 09:31:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 09:31:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 09:31:25 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_VERSION=17.0.9
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8803d1690b2a40759bc20766114ee62887c8a48db3e664379db44ebc01882a78`  
		Last Modified: Thu, 02 Oct 2025 05:04:11 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bae70953900cf0e0f035476279bcc372fd74f2b3e6dc257f0e94c89bf257642`  
		Last Modified: Thu, 02 Oct 2025 05:58:34 GMT  
		Size: 151.0 MB (151029122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6f7a93bdd124c136d03a3b63d80623d0e34a08466ea243f9aec19bfa9a26cb`  
		Last Modified: Thu, 02 Oct 2025 05:58:41 GMT  
		Size: 291.1 MB (291064077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a101720f2a8c5c6325ef9fb616fbc8dde3bf1a39e5051c07ff844dcd0469627`  
		Last Modified: Thu, 02 Oct 2025 05:58:31 GMT  
		Size: 134.5 MB (134514729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1a4d44f4c945505e6de66e490f967be696199487d8d97ce2c5955e5f7ba352`  
		Last Modified: Thu, 02 Oct 2025 05:04:11 GMT  
		Size: 54.9 KB (54907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:8da9a6f3a627fc327d85ca7a22dd8df839bf9af06be318f1e1260e8901533d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9025951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9138f5a5a428db248ad8e0f51eeadd9d896f01acfb6ee06974eb5cc7a7a5410`

```dockerfile
```

-	Layers:
	-	`sha256:113e5bd16ed3b1a425278fed049cd990d9a6dfde38f0765f1cd4b924d8ba4aa9`  
		Last Modified: Thu, 02 Oct 2025 05:30:24 GMT  
		Size: 9.0 MB (8996905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a75daeaa9c48f878aacc4ae91857fe777f01c51d5ed7634bb53f187993e43b3b`  
		Last Modified: Thu, 02 Oct 2025 05:30:25 GMT  
		Size: 29.0 KB (29046 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:323f3a180e0ebdfd35b11291ca3b6d69f873fe20adedb60e2b4e7fb0f8b20759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.9 MB (592879435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc81a59af4a23c4478c7059eda50605ac4d8a66ecf710beb26568fffe447cfd`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 30 Sep 2025 09:31:25 GMT
ARG RELEASE
# Tue, 30 Sep 2025 09:31:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 09:31:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 09:31:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 09:31:25 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_VERSION=17.0.9
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1b066ab0e02d2247c92b0221ff88d82c07e3c588a31f0b113bab5a1435f62f`  
		Last Modified: Thu, 02 Oct 2025 01:20:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed4bf0cc442f9473b771bd97e1cd7a1e74cb330aa881633aa49525fabdc01bd`  
		Last Modified: Thu, 02 Oct 2025 07:15:43 GMT  
		Size: 145.9 MB (145940442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b79c6c315ee5b629d1df8955e94ef831e97f035c32a0d554c953d202049a2`  
		Last Modified: Thu, 02 Oct 2025 07:16:13 GMT  
		Size: 283.5 MB (283501890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e091caf66954d2df0be468f99137b4751b399e72fb1d62d3e17ddaab4552516`  
		Last Modified: Thu, 02 Oct 2025 07:15:46 GMT  
		Size: 134.5 MB (134514677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4bd9f8ce3188e9d5fd48d33b6d38b9a60a8df4e8912b3f5e8313ca4c3a759a`  
		Last Modified: Thu, 02 Oct 2025 01:20:02 GMT  
		Size: 59.5 KB (59532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:270ae7e01e9b887fdc911ce7c52a28334c8972c80c96227b1769dc02be3eae2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9021744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:848d40844bb180132801a00d562f1cb4ea2afd1ac1f19658474bf93210daae58`

```dockerfile
```

-	Layers:
	-	`sha256:07e0eb1c947ddbe14ee7e1d28fb20037b140ba8dba2a5a085939d148ba405962`  
		Last Modified: Thu, 02 Oct 2025 05:30:37 GMT  
		Size: 9.0 MB (8992486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1f0bf5ac490fe317a8d9e1b36172eb86f5bd70b3657d1dda035409b8ba5fc15`  
		Last Modified: Thu, 02 Oct 2025 05:30:39 GMT  
		Size: 29.3 KB (29258 bytes)  
		MIME: application/vnd.in-toto+json
