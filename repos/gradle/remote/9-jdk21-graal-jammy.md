## `gradle:9-jdk21-graal-jammy`

```console
$ docker pull gradle@sha256:fe912bafa7a30e7295b410c55dd0e558689b7e656f777c46b72d5b4961f1e9ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk21-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:17f9dbff67126618f539ddb30aa40c94fc2a46758ca0920a8ce441a68142a7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.7 MB (586728215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17dc64ab871d39de343b0243c28e52e2ac05cbd10ea2934220d2500d9a48eb8`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:16:15 GMT
CMD ["gradle"]
# Fri, 15 May 2026 21:16:15 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 15 May 2026 21:16:15 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 15 May 2026 21:16:15 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 15 May 2026 21:16:15 GMT
WORKDIR /home/gradle
# Fri, 15 May 2026 21:16:39 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 15 May 2026 21:16:39 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 15 May 2026 21:16:39 GMT
ENV JAVA_VERSION=21.0.2
# Fri, 15 May 2026 21:16:49 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Fri, 15 May 2026 21:16:49 GMT
ENV GRADLE_VERSION=9.5.1
# Fri, 15 May 2026 21:16:49 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Fri, 15 May 2026 21:16:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 15 May 2026 21:16:52 GMT
USER gradle
# Fri, 15 May 2026 21:16:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 15 May 2026 21:16:53 GMT
USER root
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9612a2a096a84bf84561d968ee344e21a1664c7c0ab12d74186bc25b8f899fd`  
		Last Modified: Fri, 15 May 2026 21:17:26 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495708e1c5eada388a827888e0846a2be48b437446d6d78875c4636814ffada4`  
		Last Modified: Fri, 15 May 2026 21:17:34 GMT  
		Size: 126.7 MB (126737736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbab30c1df0ecc4b305ac247fe4304f51d2a8d9b1cbdc53b5289d1c26a9cd71`  
		Last Modified: Fri, 15 May 2026 21:17:37 GMT  
		Size: 290.0 MB (289986856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5a9594286f8c0ca33bc9200e852e82433401ac55f2437d82b284ce3b60dc34`  
		Last Modified: Fri, 15 May 2026 21:17:34 GMT  
		Size: 140.2 MB (140236984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4958676094fe87b3d6bd04e9e99b75a7b30d442213b5b7cf044c53000d08d48e`  
		Last Modified: Fri, 15 May 2026 21:17:28 GMT  
		Size: 25.6 KB (25612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:57b1177b22c522d2fafb01845d919d6e439655711b6d22b1c7dde7d75ed4cc1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:018b7d771eba8e9b1c9b2b52cd0e831ce10e76e3b708176230c657db35b1b17d`

```dockerfile
```

-	Layers:
	-	`sha256:0c25e89b0962310e5d9094e09159ad39f6b82146bbf02b56889675c7b5e605c9`  
		Last Modified: Fri, 15 May 2026 21:17:27 GMT  
		Size: 9.4 MB (9397686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7e4febcc62635c32c5e5eecf4364989e66a6326b0188bd9a4aef28860ca189a`  
		Last Modified: Fri, 15 May 2026 21:17:26 GMT  
		Size: 30.0 KB (30000 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:50f81056428d61a10f7dfed6bf4f970b14656fd17d49f8dda849359f3264a660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.4 MB (572412807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b04c5fb8f317548e16a27551eb89f455ccae95bc5b21b7915629ba8d847769`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:16:28 GMT
CMD ["gradle"]
# Fri, 15 May 2026 21:16:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 15 May 2026 21:16:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 15 May 2026 21:16:28 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 15 May 2026 21:16:28 GMT
WORKDIR /home/gradle
# Fri, 15 May 2026 21:17:02 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 15 May 2026 21:17:02 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Fri, 15 May 2026 21:17:02 GMT
ENV JAVA_VERSION=21.0.2
# Fri, 15 May 2026 21:17:17 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Fri, 15 May 2026 21:17:17 GMT
ENV GRADLE_VERSION=9.5.1
# Fri, 15 May 2026 21:17:17 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Fri, 15 May 2026 21:17:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 15 May 2026 21:17:19 GMT
USER gradle
# Fri, 15 May 2026 21:17:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 15 May 2026 21:17:20 GMT
USER root
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ea3e010afa06a5ae8614ac9cd3f6e1e99bb175cc898554b39adf6d1dc5ffbd`  
		Last Modified: Fri, 15 May 2026 21:17:51 GMT  
		Size: 4.3 KB (4318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6839b9b451692cb748a0312b5f1bbb3671418e59dcb7c981820e1068b98dca6b`  
		Last Modified: Fri, 15 May 2026 21:17:57 GMT  
		Size: 122.9 MB (122869279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcaff411ce922a9ae37766a85e86b41ee33424513f86e6842fb90b201e22a46`  
		Last Modified: Fri, 15 May 2026 21:18:01 GMT  
		Size: 281.7 MB (281666233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a2cf365e8c4a734dff457c7693d8ff9efef8e1d0f4f45b559a5e93d33f4c61`  
		Last Modified: Fri, 15 May 2026 21:17:58 GMT  
		Size: 140.2 MB (140236983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc686e67bef78e2251291ace903e68969f6122bac4e3abfe1ffcdca6a829182`  
		Last Modified: Fri, 15 May 2026 21:17:53 GMT  
		Size: 29.3 KB (29339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:90269bac14f4f5708dfb62e4ff0d2a382ac3a46cc5d4e3e8657c65463c2ddc04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9396803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faad0d08bb7c656cdb18711d8e52a78b55572c36f447f338b7219c83c1a696cb`

```dockerfile
```

-	Layers:
	-	`sha256:64fcd0c5ec49bd3d5e733a8e71a91de582081366972fb184ab01faa124249d68`  
		Last Modified: Fri, 15 May 2026 21:17:52 GMT  
		Size: 9.4 MB (9366542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c04913f4c2c4d0880d195981721217a11c71da9962e5abca3a8d9a107aa19351`  
		Last Modified: Fri, 15 May 2026 21:17:51 GMT  
		Size: 30.3 KB (30261 bytes)  
		MIME: application/vnd.in-toto+json
