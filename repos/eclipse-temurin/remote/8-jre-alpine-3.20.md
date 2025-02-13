## `eclipse-temurin:8-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:94a9a05555a182031136e79d03c5727a11933802197051469729b679460b0662
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:0926922006b2b837ed794aae2964ab7dcae71e1ac94667adca0d224c90637d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61474978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298684daf1898c98b3b76104c0b17e896415c13af61b10337e0ffe7a66064712`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='4fb0636534b0cd4534a3cdcbbe7cf2e937523d6376d9cef00cc6cfd5d19537e8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2eae316463420ddff1413e58f4bd984a90544260f9fcdf1c98dd638c17bb01f`  
		Last Modified: Fri, 07 Feb 2025 10:14:29 GMT  
		Size: 16.0 MB (16022300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39f69f63d5c7e63f65064878a2382221e71cedac076cd78b9ef6644e52f1a2b`  
		Last Modified: Fri, 07 Feb 2025 10:14:30 GMT  
		Size: 41.8 MB (41824010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a9b77597bb34e935adc039dc4dd2dfa0352f8d0a959282d3b2c0cdccd55872`  
		Last Modified: Fri, 07 Feb 2025 10:14:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51be9e9216f60de3e76c431d9b1847965d4c7a107d4cc9132173fcbb4ca51c96`  
		Last Modified: Fri, 07 Feb 2025 10:14:29 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5ff18c225f52c5033182de8861d8ac8b1d5e57084f6b26058e2ac022e64fb6c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **932.9 KB (932938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058ebdc926cc58e90421ec0fa32a429a9be3571f46dac41242c3a2a58d68aed6`

```dockerfile
```

-	Layers:
	-	`sha256:6217295fc5435ec9ed5732444197cf3e60e8eda3046cbf5b608e54d1536cf197`  
		Last Modified: Fri, 31 Jan 2025 01:29:21 GMT  
		Size: 914.7 KB (914708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a77d87abac52976d2577a77f8e32f0462e5cc32fda204ad14891f28fa4ebf7f9`  
		Last Modified: Fri, 31 Jan 2025 01:29:21 GMT  
		Size: 18.2 KB (18230 bytes)  
		MIME: application/vnd.in-toto+json
