## `gradle:9-jdk-graal`

```console
$ docker pull gradle@sha256:feb5889988e8f1d10c3b349f10626f4d765907bb943d92f301fa05fe97ffa8b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk-graal` - linux; amd64

```console
$ docker pull gradle@sha256:08668af7c75afb0c07755db42f5346654e25c8cd2da728ec11d624db45b6439c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.2 MB (657244644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e96e55d7dce12f4b3b7a94bc2c0ed1d78ca216362b523c3d0560441d62e574`
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
# Tue, 17 Mar 2026 01:27:21 GMT
CMD ["gradle"]
# Tue, 17 Mar 2026 01:27:21 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 17 Mar 2026 01:27:21 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 17 Mar 2026 01:27:21 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 17 Mar 2026 01:27:21 GMT
WORKDIR /home/gradle
# Tue, 17 Mar 2026 01:27:56 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 17 Mar 2026 01:27:56 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 17 Mar 2026 01:27:56 GMT
ENV JAVA_VERSION=25.0.2
# Tue, 17 Mar 2026 01:28:08 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e0be791c8fda4d03b6b0a0cb824fef3149736170057b3a515252b44419606af0     && GRAALVM_AARCH64_DOWNLOAD_SHA256=b4580d9f223d0a4b3a1757e58b18ff4c1db950e67e105fc5cb741457d2384a71     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 17 Mar 2026 01:28:08 GMT
ENV GRADLE_VERSION=9.4.0
# Tue, 17 Mar 2026 01:28:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
# Tue, 17 Mar 2026 01:28:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 17 Mar 2026 01:28:11 GMT
USER gradle
# Tue, 17 Mar 2026 01:28:12 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 17 Mar 2026 01:28:12 GMT
USER root
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb38599bdda9566f15a3355df723607ee77f5c4e7e1199de3a7a63aa05b59b90`  
		Last Modified: Tue, 17 Mar 2026 01:28:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e3dfedf8991ab7363bc396b9c6bc0693488ddafb35da642f2fab9d778d42f8`  
		Last Modified: Tue, 17 Mar 2026 01:29:00 GMT  
		Size: 148.8 MB (148818698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bc80131f488bd70689a5879229065b7aab11567363d88af05c7580612d9dab`  
		Last Modified: Tue, 17 Mar 2026 01:29:05 GMT  
		Size: 340.9 MB (340893908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60f4e8549963e76aba7fded3b287c90f60b07a1f87ba0fa25a45aa8687b5174`  
		Last Modified: Tue, 17 Mar 2026 01:28:59 GMT  
		Size: 137.8 MB (137773116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39055d58ddcc14f430c0b7524fc70bf91356cf29693b480d1f5c7f9b43e77da`  
		Last Modified: Tue, 17 Mar 2026 01:28:53 GMT  
		Size: 25.6 KB (25611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:8541def3850249e47edf82e5c61b4d1ab5eddfdecacc98559e11fc208c4d29a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9055816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74308d42689766c916d06f2b9a62f8723b5f17b3651978ae6f2a9d5093be265`

```dockerfile
```

-	Layers:
	-	`sha256:1bde0820441b0332970749981a35c27f489b5318d3eeeb568ebcc53de4f03ae5`  
		Last Modified: Tue, 17 Mar 2026 01:28:52 GMT  
		Size: 9.0 MB (9021876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a415f5b24e4f4c40fe1697f5cc56487e9e4f83fcb4ebf6af6f7bf7328753b1f4`  
		Last Modified: Tue, 17 Mar 2026 01:28:51 GMT  
		Size: 33.9 KB (33940 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:9db571f1955f53f82a124e299bfa17baddbf2b20354c0586ffeb91bbff2c71db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.6 MB (626577575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b90ad6053d956ad6a9caab70da0b5184270c3be5fe8ba66e7d5a87b2c3f0d83`
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
# Tue, 17 Mar 2026 01:29:05 GMT
CMD ["gradle"]
# Tue, 17 Mar 2026 01:29:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 17 Mar 2026 01:29:05 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 17 Mar 2026 01:29:05 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 17 Mar 2026 01:29:05 GMT
WORKDIR /home/gradle
# Tue, 17 Mar 2026 01:29:45 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 17 Mar 2026 01:29:45 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 17 Mar 2026 01:29:45 GMT
ENV JAVA_VERSION=25.0.2
# Tue, 17 Mar 2026 01:29:56 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e0be791c8fda4d03b6b0a0cb824fef3149736170057b3a515252b44419606af0     && GRAALVM_AARCH64_DOWNLOAD_SHA256=b4580d9f223d0a4b3a1757e58b18ff4c1db950e67e105fc5cb741457d2384a71     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 17 Mar 2026 01:29:56 GMT
ENV GRADLE_VERSION=9.4.0
# Tue, 17 Mar 2026 01:29:56 GMT
ARG GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
# Tue, 17 Mar 2026 01:29:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 17 Mar 2026 01:29:59 GMT
USER gradle
# Tue, 17 Mar 2026 01:29:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 17 Mar 2026 01:29:59 GMT
USER root
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac56cce12d800db66ea441775929152fb1843bcb1c67ff44f0495d29d8081e3`  
		Last Modified: Tue, 17 Mar 2026 01:30:35 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490a717f623ccd332e39aa77c9266a40dfcdd684588ad9b93abb05ca4e055d9e`  
		Last Modified: Tue, 17 Mar 2026 01:30:45 GMT  
		Size: 143.9 MB (143917282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8633262072d37f368ca066920ca48d23989679346b97069ec92eb2b38650d4e7`  
		Last Modified: Tue, 17 Mar 2026 01:30:49 GMT  
		Size: 316.0 MB (315986773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f560a66fb15ee49d2e85dfa9cbc79f349efc7ed69125ea72cc8e4a732ca090`  
		Last Modified: Tue, 17 Mar 2026 01:30:45 GMT  
		Size: 137.8 MB (137773158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffcc28d1149b6ea9cd4857dc052a31b5bc5b837ed6fe178dd169f934a5ef938`  
		Last Modified: Tue, 17 Mar 2026 01:30:36 GMT  
		Size: 29.3 KB (29334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:27089a68681d4ad9c7fd5c8241048099c4da9c758d6fac96b7581670a98ad557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9051356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0485a06af81124c1fac7ab6d18854f141da50a3b3a3f49be2216d1a096f972e`

```dockerfile
```

-	Layers:
	-	`sha256:7cbed8dc9c9744cd17e62fc8428d9e9ee1c4b771bef27ea5bb7c726feb18cebe`  
		Last Modified: Tue, 17 Mar 2026 01:30:36 GMT  
		Size: 9.0 MB (9017012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5c56c7904b7d2178e352ab0763b683413a200a6bf2d2d696f949533060c4a12`  
		Last Modified: Tue, 17 Mar 2026 01:30:35 GMT  
		Size: 34.3 KB (34344 bytes)  
		MIME: application/vnd.in-toto+json
