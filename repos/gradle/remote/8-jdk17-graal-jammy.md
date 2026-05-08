## `gradle:8-jdk17-graal-jammy`

```console
$ docker pull gradle@sha256:e8753cd063201390a0b37ff08b43823bcd708417dea95f46b41d8c7323ed5822
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk17-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:70f42692872c69fa24655adaaf2974d937695f87db912249f96cf5a539d91689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.7 MB (585664215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0adeb42b15df05eec76c94fc643083716e16b9ea951021960ee229683d1fd7d7`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Fri, 08 May 2026 17:47:27 GMT
CMD ["gradle"]
# Fri, 08 May 2026 17:47:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 May 2026 17:47:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 08 May 2026 17:47:27 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 May 2026 17:47:27 GMT
WORKDIR /home/gradle
# Fri, 08 May 2026 17:47:48 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 08 May 2026 17:47:48 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 08 May 2026 17:47:48 GMT
ENV JAVA_VERSION=17.0.9
# Fri, 08 May 2026 17:47:59 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Fri, 08 May 2026 17:47:59 GMT
ENV GRADLE_VERSION=8.14.5
# Fri, 08 May 2026 17:47:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Fri, 08 May 2026 17:48:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 08 May 2026 17:48:01 GMT
USER gradle
# Fri, 08 May 2026 17:48:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 08 May 2026 17:48:02 GMT
USER root
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380c4ce0f7b92c777f50a68ead0c7998a0c0fbb550b985d49fa2c7dfb4b874f3`  
		Last Modified: Fri, 08 May 2026 17:48:32 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55436b634c69c6fe570111cb35f93a2c7bcf19444d18cfb60275594134c35f6b`  
		Last Modified: Fri, 08 May 2026 17:48:38 GMT  
		Size: 126.7 MB (126735774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6098b8b41addef545483104a0cf65cd5f37602985e4b8a4748e04b9d4744e871`  
		Last Modified: Fri, 08 May 2026 17:48:41 GMT  
		Size: 291.1 MB (291064165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f107a6e3239126eea6e6cb152da7f62105c696e081b4a35fd3b5d0520fda5553`  
		Last Modified: Fri, 08 May 2026 17:48:39 GMT  
		Size: 138.1 MB (138068532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1516e6bea3211d78565e39180c35e4db85e7a7a1cbb27dfcd5b6bd9f91daf9d7`  
		Last Modified: Fri, 08 May 2026 17:48:33 GMT  
		Size: 54.9 KB (54906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:a08e143720ea7009fd585f57375355ecd440d81c1888edb175971108e02d6602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9430284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a6af21896dda3d7406507fcd3d1c7be84a36cc8ae3030229d9a15e07a34bd4`

```dockerfile
```

-	Layers:
	-	`sha256:09bebbbca5b2c64edf33954750eae7ffd0977fa58853a0a9b983178a75194cdb`  
		Last Modified: Fri, 08 May 2026 17:48:33 GMT  
		Size: 9.4 MB (9403041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a08cbd1f58787106650919bb1b4f7a94597114c128e546413555212c7ae9c26a`  
		Last Modified: Fri, 08 May 2026 17:48:32 GMT  
		Size: 27.2 KB (27243 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e9c40295ec5cdb461d07ed2ee45941201f7d342bb3a04d94d022dba04eb0cdae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.1 MB (572109942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137de96f0be2e442a31d314aec9ce8d3761a686169830e1ad6476a6662e70ef9`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Fri, 08 May 2026 17:48:08 GMT
CMD ["gradle"]
# Fri, 08 May 2026 17:48:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 May 2026 17:48:08 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 08 May 2026 17:48:08 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 May 2026 17:48:08 GMT
WORKDIR /home/gradle
# Fri, 08 May 2026 17:48:57 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 08 May 2026 17:48:57 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 08 May 2026 17:48:57 GMT
ENV JAVA_VERSION=17.0.9
# Fri, 08 May 2026 17:49:25 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Fri, 08 May 2026 17:49:25 GMT
ENV GRADLE_VERSION=8.14.5
# Fri, 08 May 2026 17:49:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Fri, 08 May 2026 17:49:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 08 May 2026 17:49:28 GMT
USER gradle
# Fri, 08 May 2026 17:49:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 08 May 2026 17:49:28 GMT
USER root
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b3b537e3da4a7b8c9da57b61762f2f5c15c66e07c7582470297a8922a84102`  
		Last Modified: Fri, 08 May 2026 17:50:00 GMT  
		Size: 4.3 KB (4318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491189b51f892562abe0770a58ff2977e8cfefdb1ef802587f4aca0457b3c28d`  
		Last Modified: Fri, 08 May 2026 17:50:09 GMT  
		Size: 122.9 MB (122869055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d397b40e12eb81cd332b4524af78f60473d233a10947ca59068fb23593a96a`  
		Last Modified: Fri, 08 May 2026 17:50:09 GMT  
		Size: 283.5 MB (283501941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bee526cb1dc29f8586369ebf418897e1cedd90b7e744b17f7a227480ecd6ffe`  
		Last Modified: Fri, 08 May 2026 17:50:06 GMT  
		Size: 138.1 MB (138068533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca9772de255e8b6164013afa7ee208a4b2c1c6e5f78ada0237a623b7c5bb115`  
		Last Modified: Fri, 08 May 2026 17:50:01 GMT  
		Size: 59.5 KB (59520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:764fca11b00edd4a1c2240fd274fdad133addba7a9b1bd18eadf41c03a08c835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9399180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a644b2455982e98e2a1ae7070680a7f631774b196eef4e1ce1fa9ee6dafca1`

```dockerfile
```

-	Layers:
	-	`sha256:9be2aa29ceb1d21991508188d583f140544dcef3afa8bb169fcdf5b5696073f2`  
		Last Modified: Fri, 08 May 2026 17:50:01 GMT  
		Size: 9.4 MB (9371785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bfc5ce12df7a7b2eb2e2fb1ee2c8e2a0318c6b29c6e46ce2a013efd32c49456`  
		Last Modified: Fri, 08 May 2026 17:50:00 GMT  
		Size: 27.4 KB (27395 bytes)  
		MIME: application/vnd.in-toto+json
