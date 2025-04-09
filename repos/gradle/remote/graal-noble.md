## `gradle:graal-noble`

```console
$ docker pull gradle@sha256:104615b4fde16cdd4625bf850e62c86668732b13ed3e1b9e904d3d9cd271babc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:graal-noble` - linux; amd64

```console
$ docker pull gradle@sha256:3411233ff99025dd0da807fdae8fef9bd5fb65298e4e0c083eafa3fd7f02c628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.1 MB (605108983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc478d786acaab77f943e1000f4516e29d973554c4acf0c21cb73a51c5a56c2c`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 27 Mar 2025 21:20:39 GMT
ARG RELEASE
# Thu, 27 Mar 2025 21:20:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Mar 2025 21:20:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Mar 2025 21:20:39 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 27 Mar 2025 21:20:39 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Thu, 27 Mar 2025 21:20:39 GMT
CMD ["/bin/bash"]
# Thu, 27 Mar 2025 21:20:39 GMT
CMD ["gradle"]
# Thu, 27 Mar 2025 21:20:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 27 Mar 2025 21:20:39 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 27 Mar 2025 21:20:39 GMT
WORKDIR /home/gradle
# Thu, 27 Mar 2025 21:20:39 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 27 Mar 2025 21:20:39 GMT
ENV JAVA_VERSION=21.0.2
# Thu, 27 Mar 2025 21:20:39 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
ENV GRADLE_VERSION=8.13
# Thu, 27 Mar 2025 21:20:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Thu, 27 Mar 2025 21:20:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
USER gradle
# Thu, 27 Mar 2025 21:20:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
USER root
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db1626b7da3c8ac6a4443ce40245a2195ff59253c9b8761e340d99985a25e03`  
		Last Modified: Wed, 09 Apr 2025 01:17:17 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f7a93031216b8376a6017f916a9b802dfae60fcf8817e85057568e086a2975`  
		Last Modified: Wed, 09 Apr 2025 01:17:19 GMT  
		Size: 148.4 MB (148360249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9021ce9c7b2b6e74a26286d6f2dac5020c7d0251562787ec324711187d17800c`  
		Last Modified: Wed, 09 Apr 2025 01:17:22 GMT  
		Size: 290.0 MB (289986684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c3cfc0860358e2097761e9a3f26406a77f47a7350857798e06872d8b3eeb95`  
		Last Modified: Wed, 09 Apr 2025 01:17:19 GMT  
		Size: 137.0 MB (136988188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b95dd35cb459afa5083adc1d931720c13471195a939df65e4de0494b46c84db`  
		Last Modified: Wed, 09 Apr 2025 01:17:17 GMT  
		Size: 54.9 KB (54892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:6f2ce58e3af3ab01e734b0df92f272d4ad889a876c5c4fc09b31b48fce9522fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8743340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6f560b2647978f4e68e07931e4164289b86de4b0fee40ba939007b5eef8f17`

```dockerfile
```

-	Layers:
	-	`sha256:9fa2c660522a120194f1c9b3ebd673b6730d8c2a533ec05b08aeb2ddd948f4dc`  
		Last Modified: Wed, 09 Apr 2025 01:17:17 GMT  
		Size: 8.7 MB (8711164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea0991a4e897de63271153a0938b11fbb0a36769f0b604d7ad46c2d86cc0ae81`  
		Last Modified: Wed, 09 Apr 2025 01:17:17 GMT  
		Size: 32.2 KB (32176 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:graal-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:5548af6130a4ce17f049e505c63555c3238050f2424c0b8d22c972cec55ceb73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.0 MB (591025503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d76644febc4db4a630fbb380b7b34c306713bf1fa934ee34cf2fa5227ac0e3`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 27 Mar 2025 21:20:39 GMT
ARG RELEASE
# Thu, 27 Mar 2025 21:20:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Mar 2025 21:20:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Mar 2025 21:20:39 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 27 Mar 2025 21:20:39 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Thu, 27 Mar 2025 21:20:39 GMT
CMD ["/bin/bash"]
# Thu, 27 Mar 2025 21:20:39 GMT
CMD ["gradle"]
# Thu, 27 Mar 2025 21:20:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 27 Mar 2025 21:20:39 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 27 Mar 2025 21:20:39 GMT
WORKDIR /home/gradle
# Thu, 27 Mar 2025 21:20:39 GMT
RUN set -o errexit -o nounset     && export DEBIAN_FRONTEND=noninteractive     && apt-get update     && apt-get install --yes --no-install-recommends         binutils         ca-certificates         curl         fontconfig         locales         p11-kit         tzdata         unzip         wget                 gcc         libc-dev         libz-dev         zlib1g-dev                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
ENV JAVA_HOME=/opt/java/graalvm
# Thu, 27 Mar 2025 21:20:39 GMT
ENV JAVA_VERSION=21.0.2
# Thu, 27 Mar 2025 21:20:39 GMT
RUN set -o errexit -o nounset     && mkdir /opt/java         && echo "Downloading GraalVM"     && GRAALVM_AMD64_DOWNLOAD_SHA256=b048069aaa3a99b84f5b957b162cc181a32a4330cbc35402766363c5be76ae48     && GRAALVM_AARCH64_DOWNLOAD_SHA256=a34be691ce68f0acf4655c7c6c63a9a49ed276a11859d7224fd94fc2f657cd7a     && ARCHITECTURE=$(dpkg --print-architecture)     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_ARCHITECTURE=linux-x64; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_ARCHITECTURE=linux-aarch64; fi     && GRAALVM_PKG=https://github.com/graalvm/graalvm-ce-builds/releases/download/jdk-${JAVA_VERSION}/graalvm-community-jdk-${JAVA_VERSION}_${GRAALVM_ARCHITECTURE}_bin.tar.gz     && wget --no-verbose --output-document=graalvm.tar.gz "${GRAALVM_PKG}"         && echo "Checking GraalVM download hash"     && if [ "${ARCHITECTURE}" = "amd64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AMD64_DOWNLOAD_SHA256}"; fi     && if [ "${ARCHITECTURE}" = "arm64" ]; then GRAALVM_DOWNLOAD_SHA256="${GRAALVM_AARCH64_DOWNLOAD_SHA256}"; fi     && echo "${GRAALVM_DOWNLOAD_SHA256} *graalvm.tar.gz" | sha256sum --check -         && echo "Installing GraalVM"     && tar --extract --gunzip --file graalvm.tar.gz     && rm graalvm.tar.gz     && mv graalvm-* "${JAVA_HOME}"     && for bin in "$JAVA_HOME/bin/"*; do         base="$(basename "$bin")";         [ ! -e "/usr/bin/$base" ];         update-alternatives --install "/usr/bin/${base}" "${base}" "${bin}" 1;     done         && echo "Testing GraalVM installation"     && java --version     && javac --version     && native-image --version # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
ENV GRADLE_VERSION=8.13
# Thu, 27 Mar 2025 21:20:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Thu, 27 Mar 2025 21:20:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
USER gradle
# Thu, 27 Mar 2025 21:20:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
USER root
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed6313a879343298340f8fda88aeb55e4f1abdf10f549074d5590fcd7f3714e`  
		Last Modified: Wed, 09 Apr 2025 07:19:07 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ff5b631fefb8de648c9c7c1b1ec19eab0351b7c80a4874f4920a9279f4e53e`  
		Last Modified: Wed, 09 Apr 2025 07:19:11 GMT  
		Size: 143.5 MB (143463438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe46a5bec517c3e6a5730ceb1ef9672d4cbd6ef41746e87d97102f7f22f2f2d8`  
		Last Modified: Wed, 09 Apr 2025 07:19:14 GMT  
		Size: 281.7 MB (281666095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e383a9f8c2f3253d6a36867fd68ffd0cb1e16a175a9631efc8390460e1aabbad`  
		Last Modified: Wed, 09 Apr 2025 07:19:12 GMT  
		Size: 137.0 MB (136988177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bee292c6d750408ed2d2e01d532b9c9f87e544c0657a062ec5a144cc76eba47`  
		Last Modified: Wed, 09 Apr 2025 07:19:08 GMT  
		Size: 59.5 KB (59516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:graal-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:61cfecdf7e3be7344be8d997456cd1fc02fd4cfd10979f0d1b3d0b8064db8406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8739805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a96fe04663511ab1ff590addd9751e5eb8a4635d933518de2d3769e9ff405be`

```dockerfile
```

-	Layers:
	-	`sha256:05b69393dc410034b1dca60a9c8c6bbb16943e284e34c2201bfd3f896fe0d2b0`  
		Last Modified: Wed, 09 Apr 2025 07:19:08 GMT  
		Size: 8.7 MB (8707226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0821e00ce99145268dc1aa989f583cae99f0557e86bbcc88aa7b7b5c35ac128b`  
		Last Modified: Wed, 09 Apr 2025 07:19:07 GMT  
		Size: 32.6 KB (32579 bytes)  
		MIME: application/vnd.in-toto+json
