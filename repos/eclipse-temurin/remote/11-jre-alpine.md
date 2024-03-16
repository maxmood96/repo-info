## `eclipse-temurin:11-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:c4f9f27b887596109bb8f0270a20a891351447488c47773a64562643a546552b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:11-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:564eb67091b2cda82952299b4be52bf1b039289234b52f46057fe1286c173b71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.4 MB (55397731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badc47561d5ec94eb097350199d6b7a17888cf80321ba12b0665897fa6f05e14`
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
# Sat, 16 Mar 2024 03:22:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/*
# Sat, 16 Mar 2024 03:23:14 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Sat, 16 Mar 2024 03:23:45 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='cbadab09243a084c3dc8c7e546c0f17941758f9df9c22b227144ce4247ad94f3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Sat, 16 Mar 2024 03:23:46 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Mar 2024 03:23:46 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Sat, 16 Mar 2024 03:23:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:c097d88b73b1e287c438a09deb3bd0a9e6e57747e2f7d92f12fba571c8e4f965`  
		Last Modified: Sat, 16 Mar 2024 03:27:33 GMT  
		Size: 43.5 MB (43461376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392fe5bd8bd6589723dcbba62d0693e842a8536d83fa59b31a3e11a472e274d5`  
		Last Modified: Sat, 16 Mar 2024 03:27:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf8e1c5d9a02037b4efa8053340b0e74cdc9e8c686bc9b06b42da8a9161aa91`  
		Last Modified: Sat, 16 Mar 2024 03:27:26 GMT  
		Size: 714.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
