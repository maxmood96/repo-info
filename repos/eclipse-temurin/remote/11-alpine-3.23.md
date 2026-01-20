## `eclipse-temurin:11-alpine-3.23`

```console
$ docker pull eclipse-temurin@sha256:ada27029c2a31b849d81b686dda36fc516a1598ef32ce62d747675571af0575a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-alpine-3.23` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:455d561bdf16ef3225e363bc9f725fccfb506f941c7a22c1b7cc1ea047d91e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160804314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b5ddd9fda963342fa3478e954c8830781a785af7c43fce151f2393b75c0fc2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 17:29:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Dec 2025 17:29:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Dec 2025 17:29:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Dec 2025 17:29:01 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 19 Dec 2025 17:29:01 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Fri, 19 Dec 2025 17:29:12 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='c7b58655ffde7b5e6fce4a32fdcd21be5745b3bb64ee2bc723fcf55eae720ebe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 19 Dec 2025 17:29:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Dec 2025 17:29:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Dec 2025 17:29:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 19 Dec 2025 17:29:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c992efb5ae401cbc39758a190afa1fa5ffbd418acdd846e9b033f4dfc8bc82b`  
		Last Modified: Fri, 19 Dec 2025 17:29:27 GMT  
		Size: 16.8 MB (16839428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71aab809bb530408657a2a7ce1552aa4f86bb4f514f05bd00c4004b4fea1f807`  
		Last Modified: Fri, 19 Dec 2025 17:31:33 GMT  
		Size: 140.1 MB (140102374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab4db384831375d637823888436f6b9ed1e24a540f294e2a0b74e699a7316bc`  
		Last Modified: Fri, 19 Dec 2025 17:29:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae86ff5f00598a66074908d7f7e3fce81328efeaa71128f9964809cbb5fc39c`  
		Last Modified: Fri, 19 Dec 2025 17:29:26 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c2f33894bccacbd3fb3363924b87976df6cef81407a98061905680e74e0fa3fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1025825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44bc12c4a9428d2a8cb9fc5d089608c1119a7a191e712206217f33c9574358bb`

```dockerfile
```

-	Layers:
	-	`sha256:95cf5c6e73dabdb2060c955e121162f187f5aa3ff4f5b3985af296d9b2175bad`  
		Last Modified: Fri, 19 Dec 2025 19:12:23 GMT  
		Size: 1.0 MB (1006655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02902eb5bbf0f86ac50f29af6bf579322461259870a0416795da425ec7891754`  
		Last Modified: Fri, 19 Dec 2025 19:12:24 GMT  
		Size: 19.2 KB (19170 bytes)  
		MIME: application/vnd.in-toto+json
