## `eclipse-temurin:17-alpine`

```console
$ docker pull eclipse-temurin@sha256:9581dc2edf2fdba4dcda43dd982c56f5b23d97cf3b64c75ef6970ba20709febe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:05163cc5cbe60844148fde0e40bd02b0d39d07ec9c6686d65eb7814442a1e9d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.0 MB (167983504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7ef543d1a76f59752c9c2ab9f55040249e71cd2ae53b4facb4e76253b5a1c6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='67632ee4563e9827b56f62ab6da95bce200d9e82092b211988c0d2113abc4071';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcb1617e759d446eb76924157e9d2a4abce94126e1aabca0005705104f883d0`  
		Last Modified: Wed, 08 Jan 2025 18:26:42 GMT  
		Size: 20.7 MB (20665909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d004dcd675c3245a83b07fc5bf7ef3c8e0d00fcbbb48fb5389af03d42fa51a56`  
		Last Modified: Wed, 08 Jan 2025 18:26:45 GMT  
		Size: 143.7 MB (143688926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee37ad4f4e20921436f927097031886033e13d06446534fa43e6052822ee74e`  
		Last Modified: Wed, 08 Jan 2025 18:26:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9eaba84656de704472f0a174bd1e39de0007ffd216ad4b5d9438717a5718152`  
		Last Modified: Tue, 14 Jan 2025 20:33:13 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e3b68adfbe262a44e82b1d19abbea62adfe1897a88bf37794895efba117eac69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1083712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:649998d79eea8a22b43cc7235b6c76af43ab74a046cdddb47f1ce7d13290ded1`

```dockerfile
```

-	Layers:
	-	`sha256:bf747f3d499314ac2df68faf019573fe4715f548a6366074c3ee759f10bd7ee3`  
		Last Modified: Wed, 08 Jan 2025 18:26:42 GMT  
		Size: 1.1 MB (1064098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5ae8efb55b6667d6d04288f87fd190196ab01b7f4cd525217223bb167307fa7`  
		Last Modified: Wed, 08 Jan 2025 18:26:41 GMT  
		Size: 19.6 KB (19614 bytes)  
		MIME: application/vnd.in-toto+json
