## `gradle:9-graal-jammy`

```console
$ docker pull gradle@sha256:6b4f4169a75842ac6305aabeeb1a92e954acd5edbdaa306b1a6dcecf64a82886
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-graal-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:20b4be73d2a438096251f04585839c876959f2fbf403f4f9065172806e04e2b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.7 MB (586725687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e070670c6cca7ddf7a542bd1dc6686dcb0941adc6a537fe6f884cc3cbb31a`
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
# Tue, 12 May 2026 20:48:11 GMT
CMD ["gradle"]
# Tue, 12 May 2026 20:48:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 20:48:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 20:48:11 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 20:48:11 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 20:48:35 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 12 May 2026 20:48:35 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 12 May 2026 20:48:35 GMT
ENV JAVA_VERSION=21.0.2
# Tue, 12 May 2026 20:48:45 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 12 May 2026 20:48:45 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 12 May 2026 20:48:45 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 12 May 2026 20:48:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 20:48:48 GMT
USER gradle
# Tue, 12 May 2026 20:48:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 20:48:48 GMT
USER root
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b39942f5ce3235b1a6ac1d2c106419d3e3b762d671b732111dabe3c1162372`  
		Last Modified: Tue, 12 May 2026 20:49:22 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8100e01cbcbd42b59e9c859e88355f2c50e004b45291e3664b6a042548f03f4`  
		Last Modified: Tue, 12 May 2026 20:49:29 GMT  
		Size: 126.7 MB (126736174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7dff85c68e67da0698b2acc788e2b080219815547c1af2bf630fe39b3719562`  
		Last Modified: Tue, 12 May 2026 20:49:33 GMT  
		Size: 290.0 MB (289986079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0e9ad6a406fbfb299abe56241d8922e968a3858dbc0010d7c796021d53f3a9`  
		Last Modified: Tue, 12 May 2026 20:49:30 GMT  
		Size: 140.2 MB (140236983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fd9ddade7b31caa8574b265998ff2d811755f09745662137d292bf568c39ee`  
		Last Modified: Tue, 12 May 2026 20:49:23 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:89670537c7774ff70b748f0a6f4ba8d0f0e3d09f5543a455025e64ca04385887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bfc54a8ad114320dde127eeee1186c20922b77042e4e66aaa528b39823fb98`

```dockerfile
```

-	Layers:
	-	`sha256:0d79e3fe646c9747da70559aca3ec5161a122d2dad4a8565bf5461a8f529aba1`  
		Last Modified: Tue, 12 May 2026 20:49:23 GMT  
		Size: 9.4 MB (9397682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d666b6fa58a578722d597625f44f35006fc9929b81ffa9b3b94b181faa02ecd`  
		Last Modified: Tue, 12 May 2026 20:49:22 GMT  
		Size: 30.0 KB (30001 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-graal-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b4b3bf1a2de85c199c16c9cc9dc6ad6d9993eeaa730df9cbd9ce1812625e31ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.4 MB (572412033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f943de63d15c3d660a1ace3b2069acbc9f219df67947e3b37a2e7d8c2330af10`
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
# Tue, 12 May 2026 20:48:21 GMT
CMD ["gradle"]
# Tue, 12 May 2026 20:48:21 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 20:48:21 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 20:48:21 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 20:48:21 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 20:48:54 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 binutils         ca-certificates         fontconfig         locales         p11-kit         tzdata         unzip                 gcc         libc-dev         libz-dev         zlib1g-dev                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 12 May 2026 20:48:54 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Tue, 12 May 2026 20:48:54 GMT
ENV JAVA_VERSION=21.0.2
# Tue, 12 May 2026 20:49:08 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Tue, 12 May 2026 20:49:08 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 12 May 2026 20:49:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 12 May 2026 20:49:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 20:49:10 GMT
USER gradle
# Tue, 12 May 2026 20:49:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 20:49:11 GMT
USER root
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39d7d0ceffec78cb6efa8501b89c84bcf2c5ca2137a9e90e37d3d8a20c9fe05`  
		Last Modified: Tue, 12 May 2026 20:49:43 GMT  
		Size: 4.3 KB (4316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6c52166f3006af675be08ddec5826e1bc25cb1d9b655b36a00e75246aa669a`  
		Last Modified: Tue, 12 May 2026 20:49:49 GMT  
		Size: 122.9 MB (122868588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3306df65db898c22c886a1903ec835ab6270a38b9fb12b265dddb3facfd66549`  
		Last Modified: Tue, 12 May 2026 20:49:52 GMT  
		Size: 281.7 MB (281666230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f96a48a67086bf637d67d45ec2d736c5fcf67c2ee8806e4856c4979dc2bcd1d`  
		Last Modified: Tue, 12 May 2026 20:49:50 GMT  
		Size: 140.2 MB (140236984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5536036ec50bdad5b6e09f4b84e9bbf2caf9a6df16e26d9cf02b5744d5ff0e66`  
		Last Modified: Tue, 12 May 2026 20:49:44 GMT  
		Size: 29.3 KB (29340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-graal-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:46957046ef38ce189aa22055b16f17705a924546cd43079df97031d9c9b1e39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9396799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee49d75618cd83783169628405a27a9538f644fbc6ecc9424444357c2b75230`

```dockerfile
```

-	Layers:
	-	`sha256:2d7fcfbe75a8b98d4cff0d23626a7b94bb3a58ed8712ec8cf89da5896b57c597`  
		Last Modified: Tue, 12 May 2026 20:49:43 GMT  
		Size: 9.4 MB (9366538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d92a4b5246ccb2d827247b53f0d2da96b283d2c05715fd8d68b0e0c5156c44e`  
		Last Modified: Tue, 12 May 2026 20:49:42 GMT  
		Size: 30.3 KB (30261 bytes)  
		MIME: application/vnd.in-toto+json
