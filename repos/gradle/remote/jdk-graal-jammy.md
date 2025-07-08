## `gradle:jdk-graal-jammy`

```console
$ docker pull gradle@sha256:3f53ea84b18d50eb405a8213c647d3616ff7004b02f8c2e4b5ec1f128481b583
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:0ee6e5f27e9d1844dc4405eeabbda943f1a2c27a0f94cd9188d78563c51d6b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.5 MB (583510933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad847556c0f5938483c4cb90f4be32f26edfdeab2cbc32873e1eff0ba4ab5ba`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 02:23:10 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:23:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:23:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:23:10 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:23:10 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sat, 05 Jul 2025 02:23:10 GMT
ENV JAVA_VERSION=21.0.2
# Sat, 05 Jul 2025 02:23:10 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
ENV GRADLE_VERSION=8.14.3
# Sat, 05 Jul 2025 02:23:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Sat, 05 Jul 2025 02:23:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
USER gradle
# Sat, 05 Jul 2025 02:23:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
USER root
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c796927cc19f6c6dac633e031a2b6629d58ea09d17893b17949e896210c2fd`  
		Last Modified: Mon, 07 Jul 2025 20:32:46 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535a6049fcc47e021d7bc4cfd0aaf7b14c706392b013754643835aa7e26af086`  
		Last Modified: Mon, 07 Jul 2025 20:32:57 GMT  
		Size: 126.5 MB (126533970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57938e1bdbdc22b532d2c06c32e392f800f7f378b65c99066f125ff96e1f1720`  
		Last Modified: Mon, 07 Jul 2025 20:32:39 GMT  
		Size: 290.0 MB (289986844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3d8c796aba3466b983f37fbc6666567ac0aebd422a6003ef5e0b9c3dcc7119`  
		Last Modified: Mon, 07 Jul 2025 20:32:37 GMT  
		Size: 137.4 MB (137395195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e912478077a1dfc6da10e42c97bd98593492222cef2b3dd60c207eec0bfa251`  
		Last Modified: Mon, 07 Jul 2025 20:32:46 GMT  
		Size: 54.9 KB (54897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:d10bce8a7967eb77f00a5b2b3f2545c21b30309d29ec5763fcb7ad4fb3f379e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9412893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1004db462461f130dbbcf518603102e5510e6c85f931147f58e3c3e0978d355`

```dockerfile
```

-	Layers:
	-	`sha256:b90e3ff05274acd460a40e3ac83d52ed00816a94297f83e845904ddbd7eb9cd4`  
		Last Modified: Mon, 07 Jul 2025 23:23:10 GMT  
		Size: 9.4 MB (9382942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:857599f3d7caf2753ae6ee79fd0fee8a945a3f3187346f586b3e6020c8738da8`  
		Last Modified: Mon, 07 Jul 2025 23:23:11 GMT  
		Size: 30.0 KB (29951 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:f1aee79a43af7fc6557ed8193372330e54d729ba57131e96037220050400bab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.0 MB (569040480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ceed731f142b578f819de61d6cb12e9b849b64089e284aa336c76b26feb2c4`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 02:23:10 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:23:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:23:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:23:10 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:23:10 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sat, 05 Jul 2025 02:23:10 GMT
ENV JAVA_VERSION=21.0.2
# Sat, 05 Jul 2025 02:23:10 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
ENV GRADLE_VERSION=8.14.3
# Sat, 05 Jul 2025 02:23:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Sat, 05 Jul 2025 02:23:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
USER gradle
# Sat, 05 Jul 2025 02:23:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
USER root
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a27608fee8aa4f7b0ef4ee52757d9b3d969cddf05f7e97b687fade2289f7b3`  
		Last Modified: Wed, 02 Jul 2025 05:19:14 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fb301efc80bfe2ecbb2e8dc5d4156491962aa69babf548f9964b66978b6051`  
		Last Modified: Wed, 02 Jul 2025 05:19:26 GMT  
		Size: 122.6 MB (122555881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9747140f208cf43cf590774499fe7bfe19a4cd80e855dce11ba6ac937417ed8f`  
		Last Modified: Wed, 02 Jul 2025 13:30:49 GMT  
		Size: 281.7 MB (281666240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd2d4ea5c0a2ba94882bca3aec94cbe8953320ed69425d2d2fe1861ed2220e7`  
		Last Modified: Mon, 07 Jul 2025 20:36:18 GMT  
		Size: 137.4 MB (137395202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ef0a58a7854cb018ec331f657d71d9925112c5056d8591b0ac3f96323fca28`  
		Last Modified: Mon, 07 Jul 2025 20:36:24 GMT  
		Size: 59.5 KB (59539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:674d6427ee24e7c969d1ca49a93f4371e8c4d9db0593cbebb5b54db00ac57125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9382009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e673ca48f51acbbaabf2c85c9fde69744cc70fb8e780aacc386c5c36321b07`

```dockerfile
```

-	Layers:
	-	`sha256:d8dd6dc99c1c16be5211ef74e0b26c46d03ed30e3f07067c30f3869029efedb3`  
		Last Modified: Mon, 07 Jul 2025 23:23:20 GMT  
		Size: 9.4 MB (9351798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:905cfab8908d5b838288d303df799a8f6324f645485f4eab6f5738aab6e95afd`  
		Last Modified: Mon, 07 Jul 2025 23:23:21 GMT  
		Size: 30.2 KB (30211 bytes)  
		MIME: application/vnd.in-toto+json
