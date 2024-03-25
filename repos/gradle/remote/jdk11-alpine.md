## `gradle:jdk11-alpine`

```console
$ docker pull gradle@sha256:e9427e8e23cdf023c4afe44b7d0ad999e9110e22158b2714b2d953e111ffc937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gradle:jdk11-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:3876d2d01422b7c4388a93adcde84f265313bbf777082119e51e973e7a88a3b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.5 MB (322497990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc636941d8adafc2658d3c51729a2eafafc43a7701cfbf624443d7559f8c43e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:22:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Mar 2024 03:22:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Mar 2024 03:22:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Mar 2024 03:22:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/*
# Sat, 16 Mar 2024 03:23:14 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Sat, 16 Mar 2024 03:23:23 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b541c99a5de71ebbe53e7815f9222e377b814fa1025f9f5274cb7bad226809f8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Sat, 16 Mar 2024 03:23:26 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Mar 2024 03:23:26 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Sat, 16 Mar 2024 03:23:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Mar 2024 03:23:26 GMT
CMD ["jshell"]
# Sat, 16 Mar 2024 12:11:31 GMT
CMD ["gradle"]
# Sat, 16 Mar 2024 12:11:31 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 16 Mar 2024 12:11:31 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Sat, 16 Mar 2024 12:11:31 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 16 Mar 2024 12:11:31 GMT
WORKDIR /home/gradle
# Sat, 16 Mar 2024 12:11:34 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn
# Mon, 25 Mar 2024 20:02:16 GMT
ENV GRADLE_VERSION=8.7
# Mon, 25 Mar 2024 20:02:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=544c35d6bd849ae8a5ed0bcea39ba677dc40f49df7d1835561582da2009b961d
# Mon, 25 Mar 2024 20:02:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=544c35d6bd849ae8a5ed0bcea39ba677dc40f49df7d1835561582da2009b961d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Mon, 25 Mar 2024 20:02:22 GMT
USER gradle
# Mon, 25 Mar 2024 20:02:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=544c35d6bd849ae8a5ed0bcea39ba677dc40f49df7d1835561582da2009b961d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Mon, 25 Mar 2024 20:02:24 GMT
USER root
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976103255ec1c30e915c990ab7c4afbf0348497ea66d200421c4d2bc23d6dd76`  
		Last Modified: Sat, 16 Mar 2024 03:26:22 GMT  
		Size: 8.5 MB (8526752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf1ca864b0522e1d3876431e2b6b47117f4fb4ae79aad639374b0342a549dde`  
		Last Modified: Sat, 16 Mar 2024 03:27:12 GMT  
		Size: 140.5 MB (140489184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce08a0028c1d253de32b0e996ea40a15dcd237923215d4cfe524b1d2d46a1779`  
		Last Modified: Sat, 16 Mar 2024 03:27:00 GMT  
		Size: 181.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d237574a8123d4d5783b3d4c957327736b2e96280d838605635b985b1e6c6c`  
		Last Modified: Sat, 16 Mar 2024 03:27:01 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828c025faf3e0ee2eba99382b1a54646a4dc14c3c2af0e620940be0b6c665cce`  
		Last Modified: Sat, 16 Mar 2024 12:15:02 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f440285e5c204baef22cec041db79bf3146ef4c2289754a918d47be260ea06a`  
		Last Modified: Sat, 16 Mar 2024 12:15:07 GMT  
		Size: 35.9 MB (35860817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde9019df35df49cc663917e853098449685a549918c0040914a8f1a3c4c832a`  
		Last Modified: Mon, 25 Mar 2024 20:08:01 GMT  
		Size: 134.2 MB (134210109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87865a4e73cdc79db9678a23faf880ab981aa18143201845999809ed2456e1c`  
		Last Modified: Mon, 25 Mar 2024 20:07:55 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
