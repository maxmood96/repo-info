## `gradle:jdk17-graal`

```console
$ docker pull gradle@sha256:d6a99723076db270a546ce4e36b5cea88c178929a715d914b3e9dba0616153eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk17-graal` - linux; amd64

```console
$ docker pull gradle@sha256:126e2a9210b4441b2ac029267ee9a14ce0bf97d29dd50f52bc00c64f962e5e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.4 MB (607414613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6167bd0d54a4ebeb99c905bb19e8d3f4e6277465cab4e7a0ab1800170e1f43`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:29:26 GMT
CMD ["gradle"]
# Tue, 17 Mar 2026 01:29:26 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 17 Mar 2026 01:29:26 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 17 Mar 2026 01:29:26 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 17 Mar 2026 01:29:26 GMT
WORKDIR /home/gradle
# Tue, 17 Mar 2026 01:30:03 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 17 Mar 2026 01:30:03 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 17 Mar 2026 01:30:03 GMT
ENV JAVA_VERSION=17.0.9
# Tue, 17 Mar 2026 01:30:15 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Tue, 17 Mar 2026 01:30:15 GMT
ENV GRADLE_VERSION=9.4.0
# Tue, 17 Mar 2026 01:30:15 GMT
ARG GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
# Tue, 17 Mar 2026 01:30:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 17 Mar 2026 01:30:18 GMT
USER gradle
# Tue, 17 Mar 2026 01:30:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 17 Mar 2026 01:30:18 GMT
USER root
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13b6c32a35a961572092f34407c912f4f955eb3b0b6986876593d138be25aa0`  
		Last Modified: Tue, 17 Mar 2026 01:30:49 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc43e376cec6e5374d49ffaead014cc703f2dbf452245a6e357081b69a260e9`  
		Last Modified: Tue, 17 Mar 2026 01:30:56 GMT  
		Size: 148.8 MB (148818448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b00f5ea3abbd033122bc00d3b1ff7c137c4a8f5f007834a34a4c93d614b7b2`  
		Last Modified: Tue, 17 Mar 2026 01:30:59 GMT  
		Size: 291.1 MB (291064088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d83f1cc48cb60099f3137ff58b173215df39c279ee02be168878d473a3ce254`  
		Last Modified: Tue, 17 Mar 2026 01:30:56 GMT  
		Size: 137.8 MB (137773157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f562481194b4e58f516510d1a25e89a58e92353299e0d294818a4e96968a8b5`  
		Last Modified: Tue, 17 Mar 2026 01:30:50 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:aebe008c95f0b4f19766efc41974c7d8bafe918b1150ae0c25e939f043793741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9024401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d1197d213061bb82ab13c8c8be06f0acd4367328d50a2166ff2f2abafb8d3e5`

```dockerfile
```

-	Layers:
	-	`sha256:f428a1a356975600e464e6d035824186de8dc8e146d3d6eabd5483a13cbc6f78`  
		Last Modified: Tue, 17 Mar 2026 01:30:49 GMT  
		Size: 9.0 MB (8995349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bf48b7799b6e818f27136093ec8f050e6101dbe01e486c64742650c0cbd7c02`  
		Last Modified: Tue, 17 Mar 2026 01:30:49 GMT  
		Size: 29.1 KB (29052 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c1eabc9a61fc51dbbeec27aceaeeb4c9d012c5f9bb93a4093f01ff00632c3c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.1 MB (594093359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13591d55687f6cfa0196d094e0a24e8b9a5272c2efcaa2f75d226616a9138722`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:31:32 GMT
CMD ["gradle"]
# Tue, 17 Mar 2026 01:31:32 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 17 Mar 2026 01:31:32 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 17 Mar 2026 01:31:32 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 17 Mar 2026 01:31:32 GMT
WORKDIR /home/gradle
# Tue, 17 Mar 2026 01:32:11 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 17 Mar 2026 01:32:11 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 17 Mar 2026 01:32:11 GMT
ENV JAVA_VERSION=17.0.9
# Tue, 17 Mar 2026 01:32:24 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Tue, 17 Mar 2026 01:32:24 GMT
ENV GRADLE_VERSION=9.4.0
# Tue, 17 Mar 2026 01:32:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
# Tue, 17 Mar 2026 01:32:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 17 Mar 2026 01:32:26 GMT
USER gradle
# Tue, 17 Mar 2026 01:32:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 17 Mar 2026 01:32:27 GMT
USER root
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc010aedf189c7145d5482905d3a5dd9a0c6b7470edbb9f788ea54e6d162a22`  
		Last Modified: Tue, 17 Mar 2026 01:32:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cf76a11bfd86af4a86799b312dadecf460f140e2fb2a62059b9db5f5957e1c`  
		Last Modified: Tue, 17 Mar 2026 01:33:06 GMT  
		Size: 143.9 MB (143917916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f82038fe58771722c0ace7c5d4f7e0acc2f2f650d18e2e26aab456ea93d3f0d`  
		Last Modified: Tue, 17 Mar 2026 01:33:09 GMT  
		Size: 283.5 MB (283501919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67eaeb36f077d455a6244bbadad897f3272cd6bd5323ea50861df0f914e4de68`  
		Last Modified: Tue, 17 Mar 2026 01:33:06 GMT  
		Size: 137.8 MB (137773158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5c4e58abb6a4b6ff7afa79a81a5524e7b60a76c2d62fd85375bdeccf306330`  
		Last Modified: Tue, 17 Mar 2026 01:33:01 GMT  
		Size: 29.3 KB (29338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:3916d4a1d20b5a6bb0bb1d6efdb823bd3b11122e9e7a7605c5a59ebd55afe10e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9020190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44bf8d6b662ae9139c3ce8621adc569c15842065285b40a2bf55752583d8b234`

```dockerfile
```

-	Layers:
	-	`sha256:7571ab5d7e5fcb78aa90bced8970fc26909b349a8b10b5bd70de3d1e7b48db5c`  
		Last Modified: Tue, 17 Mar 2026 01:33:00 GMT  
		Size: 9.0 MB (8990926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dedc20ffe4abdaba2787ece0725fe8de905e2ea1efdd495f3fe96bd3bfd86a06`  
		Last Modified: Tue, 17 Mar 2026 01:32:59 GMT  
		Size: 29.3 KB (29264 bytes)  
		MIME: application/vnd.in-toto+json
