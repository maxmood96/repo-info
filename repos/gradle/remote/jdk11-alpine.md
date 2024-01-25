## `gradle:jdk11-alpine`

```console
$ docker pull gradle@sha256:e1995eff435a8f807dfc5357f12e591bfd9d865c5cee13df3c2d41520e99f9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gradle:jdk11-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:35f802b1717db9068c1e3de63a1c62b606a066176b4ecda121ac646195f67d5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.8 MB (320808839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74c1d9d86abf5deb711e927825f1ca6864b83bd5e14db202f1460a0013a546a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2024 20:31:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 20:31:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 20:31:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jan 2024 20:31:03 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/*
# Wed, 24 Jan 2024 20:33:06 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:33:15 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b541c99a5de71ebbe53e7815f9222e377b814fa1025f9f5274cb7bad226809f8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 24 Jan 2024 20:33:17 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:33:18 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:33:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jan 2024 20:33:18 GMT
CMD ["jshell"]
# Wed, 24 Jan 2024 23:15:49 GMT
CMD ["gradle"]
# Wed, 24 Jan 2024 23:15:49 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 24 Jan 2024 23:15:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Wed, 24 Jan 2024 23:15:50 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 24 Jan 2024 23:15:50 GMT
WORKDIR /home/gradle
# Wed, 24 Jan 2024 23:15:54 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn
# Wed, 24 Jan 2024 23:15:54 GMT
ENV GRADLE_VERSION=8.5
# Wed, 24 Jan 2024 23:15:54 GMT
ARG GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
# Wed, 24 Jan 2024 23:16:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Wed, 24 Jan 2024 23:16:00 GMT
USER gradle
# Wed, 24 Jan 2024 23:16:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Wed, 24 Jan 2024 23:16:01 GMT
USER root
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afff92a91095014c3dafc9d75558423990f4d79c102b724a94588a1ecfc35b45`  
		Last Modified: Wed, 24 Jan 2024 20:39:46 GMT  
		Size: 8.5 MB (8528176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d61c1d753d7be1a0f1881b89c64548ff1faed3aa4f4f6e5c9e78f373a2f2b8f`  
		Last Modified: Wed, 24 Jan 2024 20:42:40 GMT  
		Size: 140.5 MB (140489180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a1ca47e29e7c93f825bdc7813b7fedc3ecec85de6ef5db90ef3c719062afd4`  
		Last Modified: Wed, 24 Jan 2024 20:42:29 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164db3a4f7ec96b111a59029f7c15ce2ad20bbf16d0fdb1a35d6b9242b38d553`  
		Last Modified: Wed, 24 Jan 2024 20:42:29 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421fac39a1ea8d3428891bb1d2aef3349b0ad364de3e350ae27f8e72f7671a5b`  
		Last Modified: Wed, 24 Jan 2024 23:24:05 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd6691c800883c142f636f822e9fa24ffb4f9f173b7656eed2e0e3d15e98a009`  
		Last Modified: Wed, 24 Jan 2024 23:24:10 GMT  
		Size: 35.8 MB (35836287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c3b944b6bfdc7fcb6a38b1d8a31c6d9a4fd111204e17d2ed468f11f74b0200`  
		Last Modified: Wed, 24 Jan 2024 23:24:12 GMT  
		Size: 132.5 MB (132544322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7596be57b6d18c0aaaf3288ac59ecada1e567f3eb50d4a85a60e56810ec379b`  
		Last Modified: Wed, 24 Jan 2024 23:24:05 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
