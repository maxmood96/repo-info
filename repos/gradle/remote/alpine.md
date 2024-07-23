## `gradle:alpine`

```console
$ docker pull gradle@sha256:a1874ea6a9b60162f66493ebeb7217f6c1c8e71a9aa91efcf9ff2bbae4064b60
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:alpine` - linux; amd64

```console
$ docker pull gradle@sha256:d9669f06818e873347d4946649667ab592e85bdb37d2bce78a9df01be44a800a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344594428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3079edc0cebe61fd02c92e86cfdd58ac194e83796bd667de367488cfebf9ff3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 12 Jul 2024 03:13:38 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["/bin/sh"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Jul 2024 03:13:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 03:13:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='849c6d5a62a1f3dc2a3d2d7be07ffda089d35b862f6160b2a288c0408c2d8be8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='8fa232fc9de5a861c1a6b0cbdc861d0b0a2bdbdd27da53d991802a460a7f0973';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["jshell"]
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["gradle"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 12 Jul 2024 03:13:38 GMT
WORKDIR /home/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_VERSION=8.9
# Fri, 12 Jul 2024 03:13:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER gradle
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER root
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e118bbc909a65083d314d2da5fe1f703619cf9810828b0d739ed6962de633f2`  
		Last Modified: Tue, 23 Jul 2024 01:06:33 GMT  
		Size: 13.0 MB (13019343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e3150815912943854e9da00bedbea033ff9c14aa65ecc14a40a7b3c6794540`  
		Last Modified: Tue, 23 Jul 2024 01:09:39 GMT  
		Size: 158.8 MB (158815453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0ff9fc66c32a6a3d808f1331e8c8013bcae0148202aaafd087f535ffdd0e0b`  
		Last Modified: Tue, 23 Jul 2024 01:09:26 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5bd5d0f19bc0be0ab9a6d6d8ac05c50aeaeb491ba52a88a149395b81ea936e`  
		Last Modified: Tue, 23 Jul 2024 01:09:26 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ce0a21ad83a9539fb18ee03d0ff4e45c9e6d568fe1d2f042b2aa8fcbd804d6`  
		Last Modified: Tue, 23 Jul 2024 02:01:13 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18634fa002ab55be8324ebd3654b0962235406b635bfa5eab81d40da011b05bb`  
		Last Modified: Tue, 23 Jul 2024 02:01:14 GMT  
		Size: 33.0 MB (33001982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e4ded4c9f1368cb5d5ca18270a7c4e5221a90301174a036371b5fe5ad7f259`  
		Last Modified: Tue, 23 Jul 2024 02:01:15 GMT  
		Size: 136.1 MB (136131822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ccc4a93abb92dd7d232cea23f16b002b984d9f5b4106b0fdb7a5ace2e2f76bf`  
		Last Modified: Tue, 23 Jul 2024 02:01:13 GMT  
		Size: 290.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:bdfe82af87c1ef6e218fd7a957967dab0ecb581347e478ac38146a0527256926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3067596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9bb7bffc47b3e92003dbc69dff5b9214d8800fe09c69aaab494e6873a9b649`

```dockerfile
```

-	Layers:
	-	`sha256:b731e36bae46d755e3cde7c18bc499f0737aa89ad9933fd921ae506a826f49f3`  
		Last Modified: Tue, 23 Jul 2024 02:01:13 GMT  
		Size: 3.0 MB (3044891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c62704a675540067e4fafe86d80a3c234f8b258f3c4699a836643552f0fc6c47`  
		Last Modified: Tue, 23 Jul 2024 02:01:13 GMT  
		Size: 22.7 KB (22705 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:a0d0eb48778354c7d670ee323e44a0ae075a87036b197aede4b24471e2571a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.5 MB (344474412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:431e33ff0436fb64b50485a8cfed8decbef8fc3d0ab628c22bdf71e4daa47260`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0f68a9122054149861f6ce9d1b1c176bbe30dd76b36b74c916ba897c12e9d970';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|x86_64)          ESUM='8e861638bf6b08c6d5837de6dc929930550928ec5fcc81b9fa7e8296afd0f9c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["gradle"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 12 Jul 2024 03:13:38 GMT
WORKDIR /home/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_VERSION=8.9
# Fri, 12 Jul 2024 03:13:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER gradle
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER root
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db88ea1e6a26d6517be6a6098be6964b10513b0bfdfea893bc9752c9c04b6e1`  
		Last Modified: Thu, 20 Jun 2024 19:04:39 GMT  
		Size: 13.4 MB (13425513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b0682e580b8b1aea7e2a977909ae9bbc90e100935552a7b6421a8e6dc7d1b6`  
		Last Modified: Thu, 20 Jun 2024 19:04:48 GMT  
		Size: 156.6 MB (156642191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5483442b5e5e84e7ae2ea9fae5136bd6c4f733ea6148becc7c0957531e3cd47d`  
		Last Modified: Thu, 20 Jun 2024 19:04:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133900c1550c17ba4fc70c056a0119b660f80ef8f03f73d3a2cf42e890cb8136`  
		Last Modified: Thu, 20 Jun 2024 19:04:37 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663e3da4f15e3958350d83623e516eff69af58726e268edcaffd7d802a3237a8`  
		Last Modified: Fri, 12 Jul 2024 18:11:45 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcc3efe32b04b89205c3d351c59eeed7379e853e2aa41937e6295a2f770c4d1`  
		Last Modified: Fri, 12 Jul 2024 18:11:47 GMT  
		Size: 34.9 MB (34914921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05932e3efa24fee0dd3fd0306f1acad46add843522a4bab393f4cb66f6461be1`  
		Last Modified: Fri, 12 Jul 2024 18:11:51 GMT  
		Size: 136.1 MB (136132079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b584c3905830c6b934a46f99691dafa7d6e0726e59dcbe051854bc944aeaa26e`  
		Last Modified: Fri, 12 Jul 2024 18:11:45 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:83d6a4c3db9f4860279da36a578b704f8e918da08c6ee1de78247922d400dd51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3553219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33dd78d4cb83e67e4b74ac18c2b773abce5079b25292dedb4de24f8d0bb6932f`

```dockerfile
```

-	Layers:
	-	`sha256:5f5c56346273867a1a9864282641c922209a6e0e33a4f0e3b851a81060d971a6`  
		Last Modified: Fri, 12 Jul 2024 18:11:46 GMT  
		Size: 3.5 MB (3530130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aa276eb368f48d7d2fabc99d9c8ce814fa1bd97fd4ef1e5744537a3cc4b6549`  
		Last Modified: Fri, 12 Jul 2024 18:11:45 GMT  
		Size: 23.1 KB (23089 bytes)  
		MIME: application/vnd.in-toto+json
