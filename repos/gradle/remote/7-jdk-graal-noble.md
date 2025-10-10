## `gradle:7-jdk-graal-noble`

```console
$ docker pull gradle@sha256:df5dee9b39936754fe786164a7cfcbe98bdd69b31a2bcba0226c2dd6391e490e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:8afa70b18f9ce9580613ef9d33e36298bf7f1ce31216661135677d25e8a5ca1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597940477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ccf33fe4788e25d5b5a8926e32d281cf7dcb6150d80c9e241d2734b3418198`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 23 Sep 2025 15:37:00 GMT
ARG RELEASE
# Tue, 23 Sep 2025 15:37:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 15:37:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 15:37:00 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Sep 2025 15:37:00 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Tue, 23 Sep 2025 15:37:00 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 15:37:00 GMT
CMD ["gradle"]
# Tue, 23 Sep 2025 15:37:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 23 Sep 2025 15:37:00 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 23 Sep 2025 15:37:00 GMT
WORKDIR /home/gradle
# Tue, 23 Sep 2025 15:37:00 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 23 Sep 2025 15:37:00 GMT
ENV JAVA_VERSION=17.0.9
# Tue, 23 Sep 2025 15:37:00 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 23 Sep 2025 15:37:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 23 Sep 2025 15:37:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
USER gradle
# Tue, 23 Sep 2025 15:37:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
USER root
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f53f21937defc1e87f1e32dfad1d254ecf443efda0ec51e07aa3f581b918bd`  
		Last Modified: Thu, 09 Oct 2025 21:15:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654b8d831bf687f148456e8c48e0437462c52b5df30414a93992570df93b3d4a`  
		Last Modified: Fri, 10 Oct 2025 04:12:03 GMT  
		Size: 148.6 MB (148627593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f851ed00b038e501b9e38e1670068c542c8502cee5d20668f3e60cfc22b5b45`  
		Last Modified: Fri, 10 Oct 2025 04:12:34 GMT  
		Size: 291.1 MB (291064116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96bf587ec3bec141f852f30bbda93c93ba9f2f330221060f6144286e040c9bd`  
		Last Modified: Fri, 10 Oct 2025 04:13:43 GMT  
		Size: 128.5 MB (128469403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bb2650fe72921c3e6be5f9d6a329147ccbb0ec384088e6c89a8b7e57ff6309`  
		Last Modified: Thu, 09 Oct 2025 21:17:14 GMT  
		Size: 54.9 KB (54900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:79542b056edae4d6533004218c7283c5b2fca87bcabaff71c95af8efe6f63b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8955333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e3bb1eb84f5a009068cd52899ceb30c1840e6df7a6326e1535eb015191103a`

```dockerfile
```

-	Layers:
	-	`sha256:a122648b1e1a45ceeb2b6d479578eb8f1b3bbfbafdea7adb503ba79d0e4ebfb8`  
		Last Modified: Thu, 09 Oct 2025 23:18:09 GMT  
		Size: 8.9 MB (8923221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29f6a9cb57bbdc3c9ab4bcc06626e5f92f7a0a807ac897d81e09d2502c5e6a4f`  
		Last Modified: Thu, 09 Oct 2025 23:18:10 GMT  
		Size: 32.1 KB (32112 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e1c6c887c53b390efb676f6163adb1041e15191e956805e3f17e07b6fb38ac73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.6 MB (584630908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d724cb892a7cac0b8797630d4166862fccbb99d5482b9e184598cb1fef4173df`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 23 Sep 2025 15:37:00 GMT
ARG RELEASE
# Tue, 23 Sep 2025 15:37:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 15:37:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 15:37:00 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Sep 2025 15:37:00 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Tue, 23 Sep 2025 15:37:00 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 15:37:00 GMT
CMD ["gradle"]
# Tue, 23 Sep 2025 15:37:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 23 Sep 2025 15:37:00 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 23 Sep 2025 15:37:00 GMT
WORKDIR /home/gradle
# Tue, 23 Sep 2025 15:37:00 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 23 Sep 2025 15:37:00 GMT
ENV JAVA_VERSION=17.0.9
# Tue, 23 Sep 2025 15:37:00 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 23 Sep 2025 15:37:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 23 Sep 2025 15:37:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
USER gradle
# Tue, 23 Sep 2025 15:37:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
USER root
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ca11254a8bcddf5cd579d5976909cc91126c6dcb1ce2ddea5054f01818c01e`  
		Last Modified: Thu, 09 Oct 2025 21:18:29 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e48e20f2879a3c84500691997a62de5ac04f2ddfad2bf4183bcef0373360e88`  
		Last Modified: Thu, 09 Oct 2025 23:18:38 GMT  
		Size: 143.7 MB (143737011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5441868273537200573b5f20cda982df576c5307b0a04bdbc153f0353d215bc0`  
		Last Modified: Thu, 09 Oct 2025 23:18:58 GMT  
		Size: 283.5 MB (283501894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385efa7ddc93885e27dc3a039f359bfbd4e72c8d1730100aba383a28f92c1faf`  
		Last Modified: Thu, 09 Oct 2025 21:18:18 GMT  
		Size: 128.5 MB (128469443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a949f5264394a5dc0e26f9ed818a43982c49bbc76d20f526e60c4beae95f0a`  
		Last Modified: Thu, 09 Oct 2025 21:18:29 GMT  
		Size: 59.5 KB (59528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:745a591e1ca5cc2de204bd57a13cf4060865fa4bf57f97c663da85cd04434d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8951362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2623f5c52ea8ed76876c95d0373f7c246f5aac539bd2548b300b87843a9ddd`

```dockerfile
```

-	Layers:
	-	`sha256:5013f9c2767ff7438ad5f7e68d71d02a9b1f40d1771eb398e8913c48e05f863d`  
		Last Modified: Thu, 09 Oct 2025 23:18:49 GMT  
		Size: 8.9 MB (8918918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:477eb7999d6e4d26cc7e09cee80ace95177a6e664289eea35478e0cdb040cc84`  
		Last Modified: Thu, 09 Oct 2025 23:18:49 GMT  
		Size: 32.4 KB (32444 bytes)  
		MIME: application/vnd.in-toto+json
