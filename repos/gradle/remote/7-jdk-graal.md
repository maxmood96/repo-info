## `gradle:7-jdk-graal`

```console
$ docker pull gradle@sha256:6446d460abe02db2f1a1142c1053f655f932af379647a9c7d7814e256d27c936
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk-graal` - linux; amd64

```console
$ docker pull gradle@sha256:cc882f05fcd4595d61200f59696bae3f0955fb677072bc9cb3313fff4131593b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.0 MB (597952942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ab7a7461ce6fca4b322ca41e968fde147e18403e43892247f3d3623217f2a8e`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:22:19 GMT
CMD ["gradle"]
# Thu, 13 Nov 2025 23:22:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 13 Nov 2025 23:22:19 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 13 Nov 2025 23:22:19 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 13 Nov 2025 23:22:19 GMT
WORKDIR /home/gradle
# Thu, 13 Nov 2025 23:24:46 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 13 Nov 2025 23:24:46 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 13 Nov 2025 23:24:46 GMT
ENV JAVA_VERSION=17.0.9
# Thu, 13 Nov 2025 23:24:54 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Thu, 13 Nov 2025 23:24:54 GMT
ENV GRADLE_VERSION=7.6.6
# Thu, 13 Nov 2025 23:24:54 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Thu, 13 Nov 2025 23:24:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 13 Nov 2025 23:24:56 GMT
USER gradle
# Thu, 13 Nov 2025 23:24:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 13 Nov 2025 23:24:57 GMT
USER root
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeedd1aac0190c4049f098147de287e82e799098c46f8ad2806016464d3a2c41`  
		Last Modified: Thu, 13 Nov 2025 23:24:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba76e7cab408c26e94d5fcbe058ea5435399b7fea866d20e15a4396cc31e6a5`  
		Last Modified: Thu, 13 Nov 2025 23:25:39 GMT  
		Size: 148.6 MB (148638497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c4e6dd611979e34eb111725763a33053df4289343221fd75ff1e82a44de1c8`  
		Last Modified: Thu, 13 Nov 2025 23:25:41 GMT  
		Size: 291.1 MB (291064109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d17f0ca5b8746946347a1196f65ec8c5a1644821d50cd52fb6c9aed343423c9`  
		Last Modified: Thu, 13 Nov 2025 23:25:38 GMT  
		Size: 128.5 MB (128469420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb233d06b3d110d685fe0b33d47d01d1c783ad78db7f16f7089654b40b0d61a`  
		Last Modified: Thu, 13 Nov 2025 23:25:48 GMT  
		Size: 54.9 KB (54909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:6f3dd083583f0a8028834f0eb3415b497287c68aa2cd9a67cdab5740587fdf53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8955306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d16b7286459e593025cb75b08427fbbc068d4b313c9c719e22679e56cd7e019`

```dockerfile
```

-	Layers:
	-	`sha256:6f378eef65deab6f1ed3a759d469735c88602b85a0d8f4d81372e277c3b445da`  
		Last Modified: Fri, 14 Nov 2025 03:20:37 GMT  
		Size: 8.9 MB (8923237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e46b3c40e9c0a719796b406926e4a2158c9b93d86d5cdb2a56cb1c1f829d646c`  
		Last Modified: Fri, 14 Nov 2025 03:20:38 GMT  
		Size: 32.1 KB (32069 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk-graal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:fd87ba89010940561a6e117d8a1cf6b9ad4904e8ec8e743b979e9c49a21b8152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.6 MB (584637524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183bf9009c8ef8839c4a4cf1853626844396f40805ba620ae00ce6de0bce5cc8`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:22:02 GMT
CMD ["gradle"]
# Thu, 13 Nov 2025 23:22:02 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 13 Nov 2025 23:22:02 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 13 Nov 2025 23:22:02 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 13 Nov 2025 23:22:02 GMT
WORKDIR /home/gradle
# Thu, 13 Nov 2025 23:24:18 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 13 Nov 2025 23:24:18 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 13 Nov 2025 23:24:18 GMT
ENV JAVA_VERSION=17.0.9
# Thu, 13 Nov 2025 23:24:26 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Thu, 13 Nov 2025 23:24:26 GMT
ENV GRADLE_VERSION=7.6.6
# Thu, 13 Nov 2025 23:24:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Thu, 13 Nov 2025 23:24:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 13 Nov 2025 23:24:28 GMT
USER gradle
# Thu, 13 Nov 2025 23:24:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 13 Nov 2025 23:24:29 GMT
USER root
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e9a1ede8b86026b394c283b4d8d74cbc4e2c63b00059fb8ee75906c3e7dadc`  
		Last Modified: Thu, 13 Nov 2025 23:23:39 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9dd72af299d9f61af1e95327f12e9c87cffd37bac3469f238c995790ee4da0`  
		Last Modified: Thu, 13 Nov 2025 23:25:09 GMT  
		Size: 143.7 MB (143743609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a491ea79b3b66cc2f6ee809ce986206fdf6088c57979d2a400a182a5d01c67`  
		Last Modified: Thu, 13 Nov 2025 23:25:11 GMT  
		Size: 283.5 MB (283501693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8c2350ec65d229860300a46571a207fcccfdecca6a10b2dddfd8f891aff4e3`  
		Last Modified: Thu, 13 Nov 2025 23:25:09 GMT  
		Size: 128.5 MB (128469420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab570d53019a20943821d49faa497229fd4c9925484eab9d4d5647bceb15e2`  
		Last Modified: Thu, 13 Nov 2025 23:25:16 GMT  
		Size: 59.5 KB (59525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk-graal` - unknown; unknown

```console
$ docker pull gradle@sha256:e444a9f70cd4e418d7e7e90355916ca99f8579484785d3bd6f0e50ea2c0f53dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8951339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7513ece6be706b2db4c51b98e6048947b3976f420e0a81034422957918543e3a`

```dockerfile
```

-	Layers:
	-	`sha256:9e5b59902696fa1198dbe74c52a78afcf6fe25468351cb4d1336ef8023b077c9`  
		Last Modified: Fri, 14 Nov 2025 03:20:51 GMT  
		Size: 8.9 MB (8918938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2124490b4aeacd84092b4d9afd3e08c35623c7114129027394133c0dccc4e20f`  
		Last Modified: Fri, 14 Nov 2025 03:20:52 GMT  
		Size: 32.4 KB (32401 bytes)  
		MIME: application/vnd.in-toto+json
