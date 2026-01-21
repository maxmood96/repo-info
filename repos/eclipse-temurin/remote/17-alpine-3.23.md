## `eclipse-temurin:17-alpine-3.23`

```console
$ docker pull eclipse-temurin@sha256:6cef5ad3453489d63c85baf51c3ee126c8e71c47c79f955a5a22ff2b111aeb7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-alpine-3.23` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:252d0c785daa393b42b5c1ec3deed20432eba234fc4274dec723eb5f66b3817c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.2 MB (169168249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf385f24a4b9239c627887e795374a57380943f60dff4f85b2be1b41c81c005`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 17:28:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Dec 2025 17:28:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Dec 2025 17:28:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Dec 2025 17:28:36 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 19 Dec 2025 17:28:36 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Fri, 19 Dec 2025 17:28:43 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='4dfea527f66034c5b6f4ca26afe692ae292fd267fd3b295c7f54f6461c65fd33';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 19 Dec 2025 17:28:44 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Dec 2025 17:28:44 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Dec 2025 17:28:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 19 Dec 2025 17:28:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2232d994f359616fc37802f318a1f2070d94a025888d07995589c780243827e2`  
		Last Modified: Fri, 19 Dec 2025 17:28:59 GMT  
		Size: 21.3 MB (21316021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88f8f83cf38bf57b5e3ee38ddb37bed299ca339295b04c6ce794e663daa3d9b`  
		Last Modified: Fri, 19 Dec 2025 17:29:22 GMT  
		Size: 144.0 MB (143989717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fa3b5115746b2f70f3087c488f46fffd0ca59810e5a08480e53c634c88ff42`  
		Last Modified: Fri, 19 Dec 2025 17:28:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af190dc3576f765d50cf24e359cf6007d26738249b423b25a3b8c433da1a58f`  
		Last Modified: Fri, 19 Dec 2025 17:28:58 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:0f86768772543ab75fbb7b66c7fb3bbaa313c91a86919eec3ceb4ad20548f9c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1124963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8e2be15640bb39edb84c9a6b288387f1996678b855ca8f9b2251b4d960005e`

```dockerfile
```

-	Layers:
	-	`sha256:c71f17f545c002c06a753c2cc3a93903eca16bb0317dd1132cd3e554b18091b1`  
		Last Modified: Fri, 19 Dec 2025 19:13:14 GMT  
		Size: 1.1 MB (1105343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f845790e50290a2d4f03fc2602e9337e51308ea95cc2fef28d8053c0712e5b6`  
		Last Modified: Fri, 19 Dec 2025 17:28:59 GMT  
		Size: 19.6 KB (19620 bytes)  
		MIME: application/vnd.in-toto+json
