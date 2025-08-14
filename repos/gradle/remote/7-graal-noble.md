## `gradle:7-graal-noble`

```console
$ docker pull gradle@sha256:83748d1b2f1e6d169e0d25a3e8995ee0f5e0c2462423468199a98c9ece8fe4fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:a2a43b18b77f3477248b2e1d149991186de51dfa67558e382ad62bd7f4d1a333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597924003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9d29251cf7f34eff34f7de49d7ba8accee6ef966844e5ba20145eca41848db`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 05 Jul 2025 02:17:41 GMT
ARG RELEASE
# Sat, 05 Jul 2025 02:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 05 Jul 2025 02:17:41 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:17:41 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_VERSION=17.0.9
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 05 Jul 2025 02:17:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER gradle
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER root
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56079b3750ac6521301ba0ccd53ad80da8da2a300f3329b178bcdbf787e07bf9`  
		Last Modified: Tue, 12 Aug 2025 18:13:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35c6e2163f6a3fea79e2dc2bc263f02ebf15292b204adc2cbb75c3f9a6456d6`  
		Last Modified: Tue, 12 Aug 2025 18:13:35 GMT  
		Size: 148.6 MB (148611061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609fc6a4e8d5029427b41dc824137aaff6d6e76aeaf0cf4b11cb096fb39039fc`  
		Last Modified: Tue, 12 Aug 2025 18:14:00 GMT  
		Size: 291.1 MB (291064098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a7ad16a4626ebb5073cc1517489b61da126c26ac0016c34b86548111dccb63`  
		Last Modified: Tue, 12 Aug 2025 18:14:24 GMT  
		Size: 128.5 MB (128469416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c01011497ff1180aea4e04707bdd3130921e8c46600877bcda501e27d0517f8`  
		Last Modified: Tue, 12 Aug 2025 18:14:25 GMT  
		Size: 54.9 KB (54896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:7541bb34f03724c4e0673bc421599baf4256b2237ac14928d56f13d623b7f8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8955345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3219fb68baba7ce45c684d680b5c6cab2bb5538758a23cc2ba791a96223b9ddc`

```dockerfile
```

-	Layers:
	-	`sha256:0d96bd72236d5365f633b43603eb2c614f2d6a5e513ca2f524d5abfee8de8144`  
		Last Modified: Tue, 12 Aug 2025 20:19:00 GMT  
		Size: 8.9 MB (8923217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7964c6280e20fb693c445a549cf528b2f1c513c8206db6e3c73aba27d80d70b2`  
		Last Modified: Tue, 12 Aug 2025 20:19:01 GMT  
		Size: 32.1 KB (32128 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:a717058fe192ff83e0199a79414fb6705f2d5747323484ad1df2193e8f93bb98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.6 MB (584595134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85806bd25d94b2e2e51ff9fe7fc9c060c1aa2964b154b9682a0d14becfd5d28a`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 05 Jul 2025 02:17:41 GMT
ARG RELEASE
# Sat, 05 Jul 2025 02:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 05 Jul 2025 02:17:41 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:17:41 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make                 binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_VERSION=17.0.9
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=e47ba7229cef02393e19d5b8f46f7f1cab4829dd17bfe84d5431fc8ff0e22a96     && GRAALVM_AARCH64_DOWNLOAD_SHA256=c3281b21f5220c2f76cf6fa0d646bc42e2d729af2c022bb06e557a613ba16102     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && gu --version     && native-image --version # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 05 Jul 2025 02:17:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER gradle
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER root
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba9bb4b6886cee8a3a9cb7af80c4cdc8365ba4e9bf63cbd53630794b923fb60`  
		Last Modified: Tue, 12 Aug 2025 18:53:40 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326e0081c09fd09ce84793887e9289be42917cc643dd0872aeeb19c1e0575c74`  
		Last Modified: Wed, 13 Aug 2025 02:26:33 GMT  
		Size: 143.7 MB (143702632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1653ecfa98337585edb6442dfa9e05efb86f318e499a0ab3ba5f7fdb3ba57`  
		Last Modified: Wed, 13 Aug 2025 02:26:40 GMT  
		Size: 283.5 MB (283501862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65908707785763b45dc6662a15972fe192aa8a2cd0670bd1079270b676c9a287`  
		Last Modified: Wed, 13 Aug 2025 02:26:55 GMT  
		Size: 128.5 MB (128469420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48eda07ce86ed9f195eba6bd91dd03499af1511e0ad80434ca349dd9040a684`  
		Last Modified: Tue, 12 Aug 2025 19:05:46 GMT  
		Size: 59.5 KB (59525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:d0e3f9a8213467cae0136f4e7a69e93781c0a24e917abd85ce3b13bff659b022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8951374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b330e77e525a8a0851127fefaa0c10b843f8d9adc44cc95ffdad12a0fa77fc`

```dockerfile
```

-	Layers:
	-	`sha256:b1852803fc41d6f845ce0e66df7d59964f91369b72d690ab07c6a63dd5b33ae0`  
		Last Modified: Tue, 12 Aug 2025 20:19:16 GMT  
		Size: 8.9 MB (8918914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29552f231b3a41354d050806e376c4047d44b9d941e0df60c6188265bc3c4870`  
		Last Modified: Tue, 12 Aug 2025 20:19:17 GMT  
		Size: 32.5 KB (32460 bytes)  
		MIME: application/vnd.in-toto+json
