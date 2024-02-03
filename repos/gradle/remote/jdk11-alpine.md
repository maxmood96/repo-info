## `gradle:jdk11-alpine`

```console
$ docker pull gradle@sha256:5a9dbbede5c924b070ad22729d66a2d5ede8029af95a273fef4139245f83fe90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gradle:jdk11-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:4a47507688dff989abfffc0e0c88e47d008eed8b7a69dcae50b0e351e259ccb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.1 MB (321080519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ad4abc91f723468c5159e468873fe5297e2f7b452ef8ac5847e44012ea42bc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:52:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 27 Jan 2024 00:52:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 27 Jan 2024 00:52:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 27 Jan 2024 00:53:00 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/*
# Sat, 27 Jan 2024 00:53:37 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Sat, 27 Jan 2024 00:53:46 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b541c99a5de71ebbe53e7815f9222e377b814fa1025f9f5274cb7bad226809f8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Sat, 27 Jan 2024 00:53:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Sat, 27 Jan 2024 00:53:48 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Sat, 27 Jan 2024 00:53:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 27 Jan 2024 00:53:48 GMT
CMD ["jshell"]
# Sat, 27 Jan 2024 08:41:28 GMT
CMD ["gradle"]
# Sat, 27 Jan 2024 08:41:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 27 Jan 2024 08:41:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Sat, 27 Jan 2024 08:41:29 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 27 Jan 2024 08:41:29 GMT
WORKDIR /home/gradle
# Sat, 27 Jan 2024 08:41:33 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn
# Sat, 03 Feb 2024 09:10:41 GMT
ENV GRADLE_VERSION=8.6
# Sat, 03 Feb 2024 09:10:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
# Sat, 03 Feb 2024 09:10:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Sat, 03 Feb 2024 09:10:46 GMT
USER gradle
# Sat, 03 Feb 2024 09:10:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9631d53cf3e74bfa726893aee1f8994fee4e060c401335946dba2156f440f24c
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Sat, 03 Feb 2024 09:10:48 GMT
USER root
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d043da2becbad64efc04c3177047b954002aa6a615a5716af19ecff2d3ff3ed0`  
		Last Modified: Sat, 27 Jan 2024 00:56:34 GMT  
		Size: 8.5 MB (8528146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d770813566ace7742087c2bce62d8d9bd663f7886f3b58f416026074632f870d`  
		Last Modified: Sat, 27 Jan 2024 00:57:24 GMT  
		Size: 140.5 MB (140489170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7ed25e6ab7a24f87e7e0744e91fe7f632968e4e3576013a381f17a992fb2e5`  
		Last Modified: Sat, 27 Jan 2024 00:57:14 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3eb764dc0954e0f7f98a91f4a30e02ddc68d011d4703d21207b2f1fbf2d3964`  
		Last Modified: Sat, 27 Jan 2024 00:57:14 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92a4739b677d79e9c131f86183d82b50846c1ac7605f5736ccd639f34279bfc`  
		Last Modified: Sat, 27 Jan 2024 08:44:55 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1287e3df35ed306c2a3884d0994db03ed3b452fede1fd33220215058ebd74a71`  
		Last Modified: Sat, 27 Jan 2024 08:45:00 GMT  
		Size: 35.8 MB (35836304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203e51749d82974a1af237359faec7d9d37bb670ed14d661d5183867af435ea6`  
		Last Modified: Sat, 03 Feb 2024 09:16:26 GMT  
		Size: 132.8 MB (132815779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4be3bc48a1809482ac88cd6928606fc337a568e261e2cecd13a8049e04e061`  
		Last Modified: Sat, 03 Feb 2024 09:16:19 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
