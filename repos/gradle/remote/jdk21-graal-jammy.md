## `gradle:jdk21-graal-jammy`

```console
$ docker pull gradle@sha256:608ea6516da1ce5abc427d87f5729d36a0683992683dee54b852067e75fd166b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk21-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:38fde117399ac762d0decb50d258fdeef2640c785f7c1066d7aeef01e38040e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.7 MB (582685027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200d0b18110fdf30a22c269da35685300803bab6a1383be77d12129bae6793f5`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 09 Sep 2024 18:59:34 GMT
ARG RELEASE
# Mon, 09 Sep 2024 18:59:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 18:59:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 18:59:34 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 18:59:34 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Mon, 09 Sep 2024 18:59:34 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 18:59:34 GMT
CMD ["gradle"]
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 09 Sep 2024 18:59:34 GMT
WORKDIR /home/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Mon, 09 Sep 2024 18:59:34 GMT
ENV JAVA_VERSION=21.0.2
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_VERSION=8.10.1
# Mon, 09 Sep 2024 18:59:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
# Mon, 09 Sep 2024 18:59:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
USER gradle
# Mon, 09 Sep 2024 18:59:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
USER root
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9187b5b4b0130297b863bfdaad37c8e5ec31dc5351b53dfb12b3f2c1612170`  
		Last Modified: Tue, 17 Sep 2024 00:59:45 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edc405ed0324f1691cca1b33192cef96d1db4bf568bf3ad6a12f6cc3926bc1e`  
		Last Modified: Tue, 17 Sep 2024 00:59:50 GMT  
		Size: 126.4 MB (126375420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5fabe54728f5284517220d3a72d1e9d168863ad6df7c83941e223a25717131`  
		Last Modified: Tue, 17 Sep 2024 00:59:51 GMT  
		Size: 290.0 MB (289986834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4924bc9d874845346732e05055dac72b901421cf3b125bcf5803276b9be579`  
		Last Modified: Tue, 17 Sep 2024 00:59:49 GMT  
		Size: 136.7 MB (136727835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fa09170a280c10e830371e31dd6f491dd400a54e16c752fea13bb74b993816`  
		Last Modified: Tue, 17 Sep 2024 00:59:46 GMT  
		Size: 54.9 KB (54908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:5ee213fe497a06cf9d3cf055635d965d387f846ae7d5c9e6d8debebd3d45cae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8725221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b73b03bf10550b195a788677995e31570e5406c70fd6d65d6571c8c38702b542`

```dockerfile
```

-	Layers:
	-	`sha256:66e41f22966ba709419e680781aab6f94c9dc66f3eb905b13915e5b121da042c`  
		Last Modified: Tue, 17 Sep 2024 00:59:46 GMT  
		Size: 8.7 MB (8698571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12e7e26867d452db34181c653a3786a6f1dff87cc1a1f49aee949a382eb00cc`  
		Last Modified: Tue, 17 Sep 2024 00:59:45 GMT  
		Size: 26.6 KB (26650 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:0f0f0af439b6d88384b604a0e5053eba53cea4bd46a1c37962acf486f25db2a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **568.3 MB (568256009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b5882472b1deefebfe9026bc33c8397b2cba4bf49371bd26ff0caf142475bf`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 09 Sep 2024 18:59:34 GMT
ARG RELEASE
# Mon, 09 Sep 2024 18:59:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 18:59:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 18:59:34 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 18:59:34 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Mon, 09 Sep 2024 18:59:34 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 18:59:34 GMT
CMD ["gradle"]
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 09 Sep 2024 18:59:34 GMT
WORKDIR /home/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Mon, 09 Sep 2024 18:59:34 GMT
ENV JAVA_VERSION=21.0.2
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_VERSION=8.10.1
# Mon, 09 Sep 2024 18:59:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
# Mon, 09 Sep 2024 18:59:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
USER gradle
# Mon, 09 Sep 2024 18:59:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
USER root
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566b7a69a4c221191d626cb115bd88772f52c62de794c7c853702f7fbc28407e`  
		Last Modified: Tue, 17 Sep 2024 02:00:10 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c34b12cf67932a2c12332d39bb39a9f5b6baa895b73c1bf0de3414e0b2f0dd`  
		Last Modified: Tue, 17 Sep 2024 02:00:13 GMT  
		Size: 122.4 MB (122439612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505f8fafc51ebe07cce3804a934311ce4f011e67697e73622a8749750e296f69`  
		Last Modified: Tue, 17 Sep 2024 02:00:22 GMT  
		Size: 281.7 MB (281666371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3fb4608ba119694e54519f9613a379a5a98b288e853fc9db2d0e716e686c1e5`  
		Last Modified: Tue, 17 Sep 2024 02:00:13 GMT  
		Size: 136.7 MB (136727831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130a08fb116f21741cd8223f1eaffd3757c5bf11840da218bcd150d8d6d3a8ef`  
		Last Modified: Tue, 17 Sep 2024 02:00:11 GMT  
		Size: 59.5 KB (59525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:13932aa8551a5708d3de45c06ba2be870a4e72958f7987600fbf74893912749e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8720613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8effa922bbc4016d5965a5d244a30a737ac84b289a72b20b6df223536f9cde0c`

```dockerfile
```

-	Layers:
	-	`sha256:eafabb77c05d6de7464a537ff926c808b56bd10ca26f624882046e2766330ef2`  
		Last Modified: Tue, 17 Sep 2024 02:00:11 GMT  
		Size: 8.7 MB (8693615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67a068b766a55f6da1e5312ff453dc123efd417ed19c5e2fcad6265c6075015e`  
		Last Modified: Tue, 17 Sep 2024 02:00:10 GMT  
		Size: 27.0 KB (26998 bytes)  
		MIME: application/vnd.in-toto+json
