## `eclipse-temurin:11-alpine`

```console
$ docker pull eclipse-temurin@sha256:9ce9f39b7c86a259cf95dd43217b34ee2b16d9ed42c909b8a902f93fcd8e42df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:d7bd2c1b5fec91b749b3773f77b662db1dd9213347c49b58f87c79ed53939940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160396923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881334514873f178a40f63eca787892c7cac9d80d77ba6dece2fefb26afd7ab9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='0a431310ccccc36c85b1274b5d31e368fdc8cf62cb7c2ed98d7b59eb5a13dc82';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 21:43:40 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e43fef20d7b051aba53ee4596ecca1cb29fb1c018c2e74fc2e6a07c09d8d90f`  
		Last Modified: Tue, 07 Jan 2025 03:31:14 GMT  
		Size: 16.0 MB (16005430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e48c0d9a1bd107175bae19f8e4f432e07dfef6120eb88ead216753f4cc20dc`  
		Last Modified: Tue, 07 Jan 2025 03:31:15 GMT  
		Size: 140.8 MB (140775085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10df55c6432c9bd7d01b17806d969dd683edcec13872b46e9ea00f40da22bc3e`  
		Last Modified: Tue, 07 Jan 2025 03:31:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2433f318eeaf47ceba55c535d79c262193cb62bbf946de4b0c11cf6100a1f9f7`  
		Last Modified: Tue, 07 Jan 2025 03:31:03 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d9168ec88b642a8becbc533ccf8bfff85478edab1c2f7e47adf1021b0eecb3b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1000.6 KB (1000605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cdd0ee500da238cb35f66745b5ac94472834fa3808f6d706aa1b703131d9db`

```dockerfile
```

-	Layers:
	-	`sha256:1f60459909d54c2101ba47b13d2191e79c4691c12fd4f918fe8e128b6f093463`  
		Last Modified: Tue, 07 Jan 2025 03:31:13 GMT  
		Size: 981.4 KB (981438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68126ef68486c71f0f4442b55ec19bb0797391a9c9cc16ec615e177fddf0e691`  
		Last Modified: Tue, 07 Jan 2025 22:30:21 GMT  
		Size: 19.2 KB (19167 bytes)  
		MIME: application/vnd.in-toto+json
