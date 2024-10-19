## `eclipse-temurin:11-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:aab438ab75dfeaa9cffa35a8ec8950120a9123e4777c4dfbd322de0523414586
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:d974c7c7776f295423beab5a1bfcd37b9ff750d64e76e35cf4744f560d6f54be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56571076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74537762adca3bd39ee34d5e56e548dca05921624bc06c4fff0e141b18a05a01`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='0ac795729cc11f47323a71713eac2a5b22d4615fd9b66c8766f964c03fb6e160';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc1ae931895265fe87f996dd1b8b0484245d69c5503e509efb376fd38a5ea8f`  
		Last Modified: Sat, 19 Oct 2024 00:54:58 GMT  
		Size: 9.4 MB (9389053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2178d1ac9886110e51e8a4aac07ff75131cee4a2e7681684df21f6a8a925fce`  
		Last Modified: Sat, 19 Oct 2024 00:54:59 GMT  
		Size: 43.6 MB (43555982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fa798630fa4592e3ced7317d8603b43a2e18adc0a93bf909f20d32d58f4aa3`  
		Last Modified: Sat, 19 Oct 2024 00:54:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125366907af1bcf09346ade181a06840343e99b49f4688e6b0ad02c83eee5245`  
		Last Modified: Sat, 19 Oct 2024 00:54:57 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9c4c6ad5756fabf2f599a9388dc16240679218984df8a8f0078579c20b9bf3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **809.9 KB (809942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae17d6bb70da64d22e6d053a87fd287b745d9a078f0ee0b7b9a3cccc1bd1175e`

```dockerfile
```

-	Layers:
	-	`sha256:63ebc3708d021f0d264f1bf7af6e45f5aceda6956b051fe5ddfe25bf91e81219`  
		Last Modified: Sat, 19 Oct 2024 00:54:58 GMT  
		Size: 793.2 KB (793179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc2599fd65b5fd5d234ec90dae337d8dd292b0c0dfa7d6bf7e4afed7e44f4db3`  
		Last Modified: Sat, 19 Oct 2024 00:54:57 GMT  
		Size: 16.8 KB (16763 bytes)  
		MIME: application/vnd.in-toto+json
