## `eclipse-temurin:17-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:c9831f0a56e4143f8296da678cb5f3f0bce1bc0f6685ad1d498cd1f66f8ad58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:17-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:597871ad55f87f44e9e635c998538706776241e3295f24b8b4bbd121326e887a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63415942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c50f92df8cd3f8265550cfd72ad09b506545fa1214fe439e781e1cb71fa5785`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
# Sat, 16 Mar 2024 03:24:03 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/*
# Sat, 16 Mar 2024 03:24:03 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Sat, 16 Mar 2024 03:24:33 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='822f43f3de715b8eccad3fab8715cdfda02ec343f004fa56107e73433d2d6fa3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Sat, 16 Mar 2024 03:24:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Mar 2024 03:24:34 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Sat, 16 Mar 2024 03:24:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6fa00702eb0aa7934afc50cb28145402935b385451bcb6ae891ecc0d4a9b90`  
		Last Modified: Sat, 16 Mar 2024 03:27:45 GMT  
		Size: 13.1 MB (13136633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28528847f172e3604d36dd918544138fdb9d6c4a98d8f87e9cb0db07b8010f88`  
		Last Modified: Sat, 16 Mar 2024 03:28:15 GMT  
		Size: 46.9 MB (46869703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99966b7f5eb75ff89d49da006e700bf72d8e6090b0444f7d67182936676e4c96`  
		Last Modified: Sat, 16 Mar 2024 03:28:08 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6e16c0974f3b779bb90c8277cce05a08f80fbf190cd98ebfa45d8004d4a44d`  
		Last Modified: Sat, 16 Mar 2024 03:28:08 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
