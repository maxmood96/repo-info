## `gradle:9-jdk-25-and-25-graal`

```console
$ docker pull gradle@sha256:c3ab31fa71919a0a1530a35893526944c9741889c3d33ce59d529e93bbc6f218
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk-25-and-25-graal` - linux; amd64

```console
$ docker pull gradle@sha256:51988cf4a1ee3d2f7a7471fe5d784d5bcccad0d8a76a3c53466717d815aecc82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.8 MB (688842368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eaaa239972e1a93271972c95b688fc70e0fbbeb40515ae4c83087050295b955`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.9106.tar --tag 26.04
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-06-10T03:30:57.931695+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-06-10T03:30:57.931695+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.control_data.9106.tar
# Fri, 19 Jun 2026 01:11:37 GMT
CMD ["gradle"]
# Fri, 19 Jun 2026 01:11:37 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 19 Jun 2026 01:11:37 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 19 Jun 2026 01:11:37 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 19 Jun 2026 01:11:37 GMT
WORKDIR /home/gradle
# Fri, 19 Jun 2026 01:12:09 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 19 Jun 2026 01:12:09 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 19 Jun 2026 01:12:09 GMT
ENV JAVA_LTS_HOME=/opt/java/graalvm25
# Fri, 19 Jun 2026 01:12:09 GMT
ENV JAVA_CURRENT_HOME=/opt/java/graalvm25
# Fri, 19 Jun 2026 01:12:20 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading LTS GraalVM"     && JAVA_LTS_VERSION=25.0.2     && GRAALVM_LTS_AMD64_DOWNLOAD_SHA256=e0be791c8fda4d03b6b0a0cb824fef3149736170057b3a515252b44419606af0     && GRAALVM_LTS_AARCH64_DOWNLOAD_SHA256=b4580d9f223d0a4b3a1757e58b18ff4c1db950e67e105fc5cb741457d2384a71     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_LTS_VERSION}/graalvm-community-jdk-${JAVA_LTS_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking LTS GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_LTS_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_LTS_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing LTS GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_LTS_HOME}"         && echo "Downloading current GraalVM"     && JAVA_CURRENT_VERSION=25.0.2     && GRAALVM_CURRENT_AMD64_DOWNLOAD_SHA256=e0be791c8fda4d03b6b0a0cb824fef3149736170057b3a515252b44419606af0     && GRAALVM_CURRENT_AARCH64_DOWNLOAD_SHA256=b4580d9f223d0a4b3a1757e58b18ff4c1db950e67e105fc5cb741457d2384a71     && if [ "${JAVA_LTS_VERSION}" != "${JAVA_CURRENT_VERSION}" ]; then       ARCHITECTURE=$(dpkg --print-architecture)       && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi       && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi       && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_CURRENT_VERSION}/graalvm-community-jdk-${JAVA_CURRENT_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz       && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"             && echo "Checking current GraalVM download hash"       && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_CURRENT_AMD64_DOWNLOAD_SHA256}"; fi       && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_CURRENT_AARCH64_DOWNLOAD_SHA256}"; fi       && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -             && echo "Installing current GraalVM"       && tar --extract --gunzip --file graalvm.tar.gz       && rm graalvm.tar.gz       && mv graalvm-* "${JAVA_CURRENT_HOME}";     fi         && echo "Default Java to LTS GraalVM"     && ln --symbolic "${JAVA_LTS_HOME}" /opt/java/graalvm     && for bin in "$JAVA_LTS_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Fri, 19 Jun 2026 01:12:20 GMT
ENV GRADLE_VERSION=9.5.1
# Fri, 19 Jun 2026 01:12:20 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Fri, 19 Jun 2026 01:12:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 19 Jun 2026 01:12:22 GMT
USER gradle
# Fri, 19 Jun 2026 01:12:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 19 Jun 2026 01:12:23 GMT
USER root
```

-	Layers:
	-	`sha256:81e2f2053c8fa702b6863110b55c09e67f6adeb78b4672745958c4d8b3d056c5`  
		Last Modified: Wed, 10 Jun 2026 08:00:11 GMT  
		Size: 41.6 MB (41562239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f56e4c7f2f2a1415c59803638274d488a73b61a8e1f9cbd9cb280327e8d21e`  
		Last Modified: Wed, 10 Jun 2026 08:00:15 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949bf63070d14891727c289214dde01a9818156356b15b2ad7ea0b4c2e9d2f47`  
		Last Modified: Fri, 19 Jun 2026 01:13:06 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d1c1956e1ec02b35afd52a028680c53a8315d364f1323c1fd298160ca952dc`  
		Last Modified: Fri, 19 Jun 2026 01:13:15 GMT  
		Size: 166.1 MB (166121705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7928ed228822c1640ca70370c9ebf2f364cc2823f852174da8ea768a8c863a`  
		Last Modified: Fri, 19 Jun 2026 01:13:18 GMT  
		Size: 340.9 MB (340893996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db2cd6f89c36f32612a7cab868ab9250d5c627debe37f9fc445ea05274017af`  
		Last Modified: Fri, 19 Jun 2026 01:13:14 GMT  
		Size: 140.2 MB (140236982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e13f077d2e7bf5323edc11608cce4896c18d8efb309f8dc9b08e1648b41e58`  
		Last Modified: Fri, 19 Jun 2026 01:13:08 GMT  
		Size: 25.6 KB (25612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-25-and-25-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:bd8d50301a53373edd1625d5a5899dda7b3cd3156cd8f929057ce64875388788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11172754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb41505845e9daf9c2c8ecc89cce03b793470f4cdbe6e05a9e764b3f5979fce5`

```dockerfile
```

-	Layers:
	-	`sha256:c2477062d94ee1d1ffc93e64a59c9c07d8b860f9f6ece2a235e509961ec9c6ea`  
		Last Modified: Fri, 19 Jun 2026 01:13:07 GMT  
		Size: 11.1 MB (11133137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed5fa57eb287223fe165703e0f15b4f5ffd42534d7fe4c553d7f1dd365cdcde6`  
		Last Modified: Fri, 19 Jun 2026 01:13:06 GMT  
		Size: 39.6 KB (39617 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-25-and-25-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:cd10b68ec43a4a0842923a1e4b0f2e928fb6d4f36e4a46576e2aa1ca2d11a43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.2 MB (656237215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edc2aedbec985bafc5580d0bfb9c20d82c01d45edd2e7a9146be9c85702a60ce`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 10 Jun 2026 03:33:02 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.9196.tar --tag 26.04
# Wed, 10 Jun 2026 03:33:02 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-06-10T03:33:03.035505+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-06-10T03:33:03.035505+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.control_data.9196.tar
# Fri, 19 Jun 2026 01:11:29 GMT
CMD ["gradle"]
# Fri, 19 Jun 2026 01:11:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 19 Jun 2026 01:11:29 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 19 Jun 2026 01:11:29 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 19 Jun 2026 01:11:29 GMT
WORKDIR /home/gradle
# Fri, 19 Jun 2026 01:11:59 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 19 Jun 2026 01:11:59 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 19 Jun 2026 01:11:59 GMT
ENV JAVA_LTS_HOME=/opt/java/graalvm25
# Fri, 19 Jun 2026 01:11:59 GMT
ENV JAVA_CURRENT_HOME=/opt/java/graalvm25
# Fri, 19 Jun 2026 01:12:10 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading LTS GraalVM"     && JAVA_LTS_VERSION=25.0.2     && GRAALVM_LTS_AMD64_DOWNLOAD_SHA256=e0be791c8fda4d03b6b0a0cb824fef3149736170057b3a515252b44419606af0     && GRAALVM_LTS_AARCH64_DOWNLOAD_SHA256=b4580d9f223d0a4b3a1757e58b18ff4c1db950e67e105fc5cb741457d2384a71     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_LTS_VERSION}/graalvm-community-jdk-${JAVA_LTS_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking LTS GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_LTS_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_LTS_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing LTS GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_LTS_HOME}"         && echo "Downloading current GraalVM"     && JAVA_CURRENT_VERSION=25.0.2     && GRAALVM_CURRENT_AMD64_DOWNLOAD_SHA256=e0be791c8fda4d03b6b0a0cb824fef3149736170057b3a515252b44419606af0     && GRAALVM_CURRENT_AARCH64_DOWNLOAD_SHA256=b4580d9f223d0a4b3a1757e58b18ff4c1db950e67e105fc5cb741457d2384a71     && if [ "${JAVA_LTS_VERSION}" != "${JAVA_CURRENT_VERSION}" ]; then       ARCHITECTURE=$(dpkg --print-architecture)       && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi       && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi       && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_CURRENT_VERSION}/graalvm-community-jdk-${JAVA_CURRENT_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz       && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"             && echo "Checking current GraalVM download hash"       && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_CURRENT_AMD64_DOWNLOAD_SHA256}"; fi       && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_CURRENT_AARCH64_DOWNLOAD_SHA256}"; fi       && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -             && echo "Installing current GraalVM"       && tar --extract --gunzip --file graalvm.tar.gz       && rm graalvm.tar.gz       && mv graalvm-* "${JAVA_CURRENT_HOME}";     fi         && echo "Default Java to LTS GraalVM"     && ln --symbolic "${JAVA_LTS_HOME}" /opt/java/graalvm     && for bin in "$JAVA_LTS_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Fri, 19 Jun 2026 01:12:10 GMT
ENV GRADLE_VERSION=9.5.1
# Fri, 19 Jun 2026 01:12:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Fri, 19 Jun 2026 01:12:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 19 Jun 2026 01:12:13 GMT
USER gradle
# Fri, 19 Jun 2026 01:12:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 19 Jun 2026 01:12:14 GMT
USER root
```

-	Layers:
	-	`sha256:c572f291b2a0cc05a1d523f3dda4d3f1992c3e480debf2e1bc9278aeab115625`  
		Last Modified: Wed, 10 Jun 2026 08:00:25 GMT  
		Size: 40.7 MB (40709186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dda33820b52cf93fd5ff3808c770af252cf0565784b42e52e3dd74e2ebf5b2`  
		Last Modified: Wed, 10 Jun 2026 08:00:29 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29582fccdc4f8ba516beeae4a1ae42fa1a3e5e450e7f101b5d38c2960477f964`  
		Last Modified: Fri, 19 Jun 2026 01:12:53 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d660b844d23d7800a67b21a81a0a8294a09f959dffd2c3f40b49865fe852ca2c`  
		Last Modified: Fri, 19 Jun 2026 01:13:10 GMT  
		Size: 159.3 MB (159273190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777f08bd18c6f67856b00a943fbf0cae4b5129bf073653eee68050664c5dc553`  
		Last Modified: Fri, 19 Jun 2026 01:13:18 GMT  
		Size: 316.0 MB (315986730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264378d26540d369871bb1f73cd1031aafa8bf7f8966a55519ee0c5835d9905b`  
		Last Modified: Fri, 19 Jun 2026 01:13:09 GMT  
		Size: 140.2 MB (140236944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ed14efc364b4d3489f0319cc0c0dbfc367499116964312f90ce427c9ff22cd`  
		Last Modified: Fri, 19 Jun 2026 01:12:55 GMT  
		Size: 29.3 KB (29336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-25-and-25-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:39c54a00b1e9138fed94a0e35caecbbdfb07df586a1821f797cafc0ae81bffbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11210893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d522bea801746cbda230eb1424abb65640a5845cfde9244d5ff45f255a84f43`

```dockerfile
```

-	Layers:
	-	`sha256:39407413633426eab8ec0d03193476230c9086232a6b31f623369b0b34a696bb`  
		Last Modified: Fri, 19 Jun 2026 01:12:54 GMT  
		Size: 11.2 MB (11170968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638b2886f048f36ec74f09bf54a4de90057bbaa3743aa024fd0eed0f3248d260`  
		Last Modified: Fri, 19 Jun 2026 01:12:53 GMT  
		Size: 39.9 KB (39925 bytes)  
		MIME: application/vnd.in-toto+json
