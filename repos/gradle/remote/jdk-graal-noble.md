## `gradle:jdk-graal-noble`

```console
$ docker pull gradle@sha256:7ece51864b5eaafdb7ba63ed3b1ba73faf09ce27c736a3b24e63a4b5947fb7d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:228bdb88f2fcd43ee186d7b6d9a55226bfd995ef31ba6d17c66b59e6ddedd41a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.1 MB (659081093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16bfef1b37e1b8d6c5187eb82e35d54e6c13a7b9ab9e75636df34b5faac0245`
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
# Tue, 02 Jun 2026 08:15:10 GMT
CMD ["gradle"]
# Tue, 02 Jun 2026 08:15:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 02 Jun 2026 08:15:10 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 02 Jun 2026 08:15:10 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 02 Jun 2026 08:15:10 GMT
WORKDIR /home/gradle
# Tue, 02 Jun 2026 08:15:36 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 02 Jun 2026 08:15:36 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 02 Jun 2026 08:15:36 GMT
ENV JAVA_VERSION=25.0.2
# Tue, 02 Jun 2026 08:15:49 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e0be791c8fda4d03b6b0a0cb824fef3149736170057b3a515252b44419606af0     && GRAALVM_AARCH64_DOWNLOAD_SHA256=b4580d9f223d0a4b3a1757e58b18ff4c1db950e67e105fc5cb741457d2384a71     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 02 Jun 2026 08:15:49 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 02 Jun 2026 08:15:49 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 02 Jun 2026 08:15:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 02 Jun 2026 08:15:51 GMT
USER gradle
# Tue, 02 Jun 2026 08:15:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 02 Jun 2026 08:15:52 GMT
USER root
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b90e3011e488951b4e30d414c6c0697b4e352d973d1fb8927900e3aaa5bd10`  
		Last Modified: Tue, 02 Jun 2026 08:16:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750b7eb32bd1fb69d7201731f8fd5c618819ea9e23cd66eb17964fa0be458a0a`  
		Last Modified: Tue, 02 Jun 2026 08:16:35 GMT  
		Size: 148.2 MB (148190445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8281abddde5c898db59fed250eadc255f2633ef1aeb42c1442df476d7dbbfb`  
		Last Modified: Tue, 02 Jun 2026 08:16:40 GMT  
		Size: 340.9 MB (340893930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecb821c063c9785a3feedd761dad1e29aa384bd99624e8ee81c22a8e46a98c1`  
		Last Modified: Tue, 02 Jun 2026 08:16:35 GMT  
		Size: 140.2 MB (140236981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ecd5dd9c0335e0e0a61810ce4f2a7b339055967341a898b2f87f68a6b8ad19`  
		Last Modified: Tue, 02 Jun 2026 08:16:29 GMT  
		Size: 25.6 KB (25613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:44559acba10faf91e3c8c6b9da48fae90238334b72273f7f12811592003037d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9078786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5289e0cb0c398c979e360f4fcccebe8143104adb4adefd997ebde3ada793c6e6`

```dockerfile
```

-	Layers:
	-	`sha256:b0044840b3f8ab2ceec6d7a0ef42aabdb2bb5da7a9a5bcb0bebe74cdfbc2bcfd`  
		Last Modified: Tue, 02 Jun 2026 08:16:28 GMT  
		Size: 9.0 MB (9048551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8070b94f06b8d8c2814c5c461bad802829cc6fcd388230a09472bb3ddc86676`  
		Last Modified: Tue, 02 Jun 2026 08:16:27 GMT  
		Size: 30.2 KB (30235 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:3e19a9f57de6bf758f62964541744e916ba5c68a13a6d77d9344b67c320a414d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.4 MB (628425568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e09453252bbe036dcdc9a24abf4c8e4df4c3b2261bfb328de3439a7629ecbe`
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
# Tue, 02 Jun 2026 08:11:08 GMT
CMD ["gradle"]
# Tue, 02 Jun 2026 08:11:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 02 Jun 2026 08:11:08 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 02 Jun 2026 08:11:08 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 02 Jun 2026 08:11:08 GMT
WORKDIR /home/gradle
# Tue, 02 Jun 2026 08:11:35 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 02 Jun 2026 08:11:35 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 02 Jun 2026 08:11:35 GMT
ENV JAVA_VERSION=25.0.2
# Tue, 02 Jun 2026 08:11:45 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e0be791c8fda4d03b6b0a0cb824fef3149736170057b3a515252b44419606af0     && GRAALVM_AARCH64_DOWNLOAD_SHA256=b4580d9f223d0a4b3a1757e58b18ff4c1db950e67e105fc5cb741457d2384a71     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 02 Jun 2026 08:11:45 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 02 Jun 2026 08:11:45 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 02 Jun 2026 08:11:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 02 Jun 2026 08:11:47 GMT
USER gradle
# Tue, 02 Jun 2026 08:11:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 02 Jun 2026 08:11:48 GMT
USER root
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5ba5ccee639915ff5cd568ae20d0c1e6cf312e2090b7dccfbaa2aa7b0af31c`  
		Last Modified: Tue, 02 Jun 2026 08:12:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a3280d2b20598c0b80d53f9a2f2da0ec9e4830d05c1bb5c84236620dfd55bf`  
		Last Modified: Tue, 02 Jun 2026 08:12:31 GMT  
		Size: 143.3 MB (143294810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28dfb8f5fd6a68f707c84f1927700c67fe8d7e9fccb8fab55159a073416ea5f1`  
		Last Modified: Tue, 02 Jun 2026 08:12:35 GMT  
		Size: 316.0 MB (315986721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd8d8f7b31e79b5d63c8fa5590e07eae2a5aecffc110630f66e3ff725739049`  
		Last Modified: Tue, 02 Jun 2026 08:12:30 GMT  
		Size: 140.2 MB (140236982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d95ed578b50e83434d8ecb510d6647a4a39e3fcd4d58f336ad82158d9631771`  
		Last Modified: Tue, 02 Jun 2026 08:12:24 GMT  
		Size: 29.3 KB (29328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:17b97462b668f91b94e5cd0fae4c1d90e47dbe16c4f1d9afe7dfcee3308a1b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9074039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86df59d8f88243eca9f2a599c9a197f56d2a9a90ac8af86b2fb97edc277f6ea`

```dockerfile
```

-	Layers:
	-	`sha256:2e8e44ae4cab35330112e53da9ac640233e2ede8908ca917efaf45103c52e5d2`  
		Last Modified: Tue, 02 Jun 2026 08:12:24 GMT  
		Size: 9.0 MB (9043543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59ddfc14e7ac6a00910d0cbbe5c3dea3505652c722be5220c2a2ce6b438ac5f3`  
		Last Modified: Tue, 02 Jun 2026 08:12:23 GMT  
		Size: 30.5 KB (30496 bytes)  
		MIME: application/vnd.in-toto+json
