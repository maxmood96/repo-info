## `eclipse-temurin:21-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:848653d62f2fe03f2ef6d0527236fbdedd296ee44bfeb7a9836662dc2f0f58d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:9ea38b5e9d526756c9026d84eb905f67bc430512288bd69482d4346859e30b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66705643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6082b9c98528712354fe3341b42670bdcb40d37fa94d35a5445aec516d40b03`
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
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f9410264235861deaf30f97bec80870cf3bc38b1d8e57d897d8bb1f706ae6705';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='0dfd0ebab44d777f65bceaff7f79e8e0b9deb74a5eb166922483f1864bcf2052';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:1921b4db4f1d1f0ab83b5f1350ba7ad16a4700028edd88ee28dd988c0c983fb7`  
		Last Modified: Sat, 19 Oct 2024 00:56:09 GMT  
		Size: 9.4 MB (9389058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a2eebbcfae42393c3a98cd1463f2b001e6b880c46ee8349c4d869e040ed9c1`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 53.7 MB (53690545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab951cda57d014e0b441feeb2e7b72c4f23f3bc4762798e7f04e0b1b08a2ca8`  
		Last Modified: Sat, 19 Oct 2024 00:56:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4f02afed8c9c993f2a8efce64a1d49042f67833bb15843b6528aa56942d1f8`  
		Last Modified: Sat, 19 Oct 2024 00:56:08 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:154daae9ac0027def6afcd207a9d88c99f19829accca40f0df78f6ee70199f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **800.7 KB (800729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07cfee7af2338ca218dd9e16623f9c1c764c559accb6339585bde7b6dd192b80`

```dockerfile
```

-	Layers:
	-	`sha256:0dd2be68ca659a02a8ab53943fb4216a72dbc01706afa6c8d76ca1a60836c6e1`  
		Last Modified: Sat, 19 Oct 2024 00:56:08 GMT  
		Size: 783.2 KB (783170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bbba21068fb327b34fe602993cd9a2057eeae6803ff027d6e82b73883f61e96`  
		Last Modified: Sat, 19 Oct 2024 00:56:08 GMT  
		Size: 17.6 KB (17559 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:74450c342c521dc6300539854c3b51d8df251c13ad53ea9d641fa2bf2fe64d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66321597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de22c7104ea32b63eb6b3ba6980e567803913a46a06ed6b85e98029f33696b0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 22 Aug 2024 07:58:33 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f9410264235861deaf30f97bec80870cf3bc38b1d8e57d897d8bb1f706ae6705';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='0dfd0ebab44d777f65bceaff7f79e8e0b9deb74a5eb166922483f1864bcf2052';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fe858122ab028c64a3fffeb0f39cf14498fc825d71dd5f74cd2ea534e7a84c`  
		Last Modified: Sat, 19 Oct 2024 01:18:26 GMT  
		Size: 9.5 MB (9514761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c148abb2ce92df06ce1b8bcd2ca3fc1f06897e9980238f078046c8733722e6`  
		Last Modified: Sat, 19 Oct 2024 01:18:28 GMT  
		Size: 52.7 MB (52716955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8d6fa83fc9c210df798ec4d929cc186092dcc34f63f446725618a6c9126ea7`  
		Last Modified: Sat, 19 Oct 2024 01:18:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed9202a4559f505edd6ce56ff9f83b3432bd88fb6935346fa3494fdaad982b8`  
		Last Modified: Sat, 19 Oct 2024 01:18:26 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3812c91ae631dc1b238f016522f3df4798f20209c5b9e8c149d06701104256a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **800.2 KB (800246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6902d944c162167e78cb40de43a03698ad7feae106a73d62eaf12fd30d1afe2c`

```dockerfile
```

-	Layers:
	-	`sha256:5e3b25bd680e9faf3fe0ef06027ea393eebfc3f3479605f2d2b248fce2a8d900`  
		Last Modified: Sat, 19 Oct 2024 01:18:26 GMT  
		Size: 782.6 KB (782583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:642da21ec0fc904f2b24dcbd8a26905f8792dd4163b5acb7297dbcaa43fca5b9`  
		Last Modified: Sat, 19 Oct 2024 01:18:26 GMT  
		Size: 17.7 KB (17663 bytes)  
		MIME: application/vnd.in-toto+json
