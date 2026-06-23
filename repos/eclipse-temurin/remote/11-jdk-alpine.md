## `eclipse-temurin:11-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:7ab5b720f367e4bb4da17cd9cd71e761572d14138d4b846d110af49f3ea116a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:2f9be6269c50d3f6c70388a03ef6170cf43b88957dfdd910221a7d4e27fe57f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161737107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b59f4a47b84e3c9ce14860666fb3b20d5744e18f36d81823b3c238a427d7d4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:56:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:56:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:56:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:56:34 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Mon, 22 Jun 2026 19:56:41 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='ed06a4b8381786a6e8091c10539856675497d2b821cd2d0200cc5b65f453b982';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 22 Jun 2026 19:56:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:56:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:56:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 19:56:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f9b522ef6226b5e762f07b84e312e749c4ff9762d64fb0a0e6a0f08d3dadc9`  
		Last Modified: Mon, 22 Jun 2026 19:56:57 GMT  
		Size: 16.8 MB (16815695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82edf31c58962a79b82269852db50864e5e46165fd344f4918a80796db584951`  
		Last Modified: Mon, 22 Jun 2026 19:57:00 GMT  
		Size: 141.1 MB (141074581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6857b309472f9776411dbc577858d377ec37fa81f85b3d973ce4c495a1a72e`  
		Last Modified: Mon, 22 Jun 2026 19:56:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2ca25c879ff73f76024b21ff3fcdcae040cc01923ae1d2bf184bd72f35d3bf`  
		Last Modified: Mon, 22 Jun 2026 19:56:57 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6612a2ebbdd44da6c2c58947bab824c51349d9029bf1c21fbb9112401122635c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c8c814f7d0f43cfe24dd5ee16f86887e040ff92b14abf250684ca3a5b1a694`

```dockerfile
```

-	Layers:
	-	`sha256:2d0daeeb756de8297e2685a08701d987a4b4281dd6f3bf2408ee9e9eadb62ea5`  
		Last Modified: Mon, 22 Jun 2026 19:56:57 GMT  
		Size: 990.1 KB (990064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7195fe4d8997a08646e448608732cec79dbb43bd0845a852629c2b2759f2e3d`  
		Last Modified: Mon, 22 Jun 2026 19:56:57 GMT  
		Size: 20.2 KB (20178 bytes)  
		MIME: application/vnd.in-toto+json
