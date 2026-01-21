## `eclipse-temurin:21-jre-alpine-3.23`

```console
$ docker pull eclipse-temurin@sha256:243e711289b0f17e05a4df60454bbb1b8ed7b126db4de2d5535da994b7417111
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-jre-alpine-3.23` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:f599f6fa11f007b6dcf6e85ec2c372c1eba2b6940a7828eb6e665665ea5edd1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73870977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b02fa3f6613c997bf4f5242927cefb0b9d2a8a8ce76a1ef3a1c919e9bbb8846`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 17:28:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Dec 2025 17:28:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Dec 2025 17:28:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Dec 2025 17:28:53 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 19 Dec 2025 17:28:53 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Fri, 19 Dec 2025 17:29:20 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7f8c230ba505b418e4288e2b34758a6e4da32470944740e5ba0cfaae02271c22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='17aca4ecc1600f70ec88ea0f8bf3a06ba6806bdae8c96d03c07683c800f0d4e8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 19 Dec 2025 17:29:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Dec 2025 17:29:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Dec 2025 17:29:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd339c1f2a49a0d087a1906b976a8cb90780165f243db41c6ab009b23aaf828`  
		Last Modified: Fri, 19 Dec 2025 17:29:08 GMT  
		Size: 16.8 MB (16839444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027d154c4912f856424593d41ad3925c9aa63ca610b3eac723baabcd09912f15`  
		Last Modified: Fri, 19 Dec 2025 17:29:44 GMT  
		Size: 53.2 MB (53169022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fc38b2a5cd0b367c46325e2890d927c53cc6d6c8b90d4aef32d896b9af4336`  
		Last Modified: Fri, 19 Dec 2025 18:19:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f6bf4580711b50f555fe6ade2e888d105ed024043a729c01d58b22e4f6e5a0`  
		Last Modified: Fri, 19 Dec 2025 17:29:39 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5a3f2642f4030f0ec9e77c9585646a4183969186881dfb5f00e9af5c9d861bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **924.2 KB (924185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b0549d5c2b4bc5947c10a8428cc3bc850302dedc1f5e9e1cae3d391a2f1847`

```dockerfile
```

-	Layers:
	-	`sha256:57e804fcc5a786ab070e4cc49f94dae2b4ae6f844e7c7025c22d548cba49c4f6`  
		Last Modified: Fri, 19 Dec 2025 19:14:36 GMT  
		Size: 905.2 KB (905160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a81e0de002daea2b8bfdf9d7bc7293a0362b59a86ea69a194502a33bfff11a88`  
		Last Modified: Fri, 19 Dec 2025 17:29:31 GMT  
		Size: 19.0 KB (19025 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-alpine-3.23` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:c36c121f56949ad7511adf4bdc301b7724ee06619bed26d9b0fb74f255a36290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73216036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d13f3bf9acc039ef255d88ffa76797d0a5306948dc4c5ba9e2598438898326d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 17:29:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Dec 2025 17:29:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Dec 2025 17:29:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 19 Dec 2025 17:29:08 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 19 Dec 2025 17:29:08 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Fri, 19 Dec 2025 17:29:12 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7f8c230ba505b418e4288e2b34758a6e4da32470944740e5ba0cfaae02271c22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='17aca4ecc1600f70ec88ea0f8bf3a06ba6806bdae8c96d03c07683c800f0d4e8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 19 Dec 2025 17:29:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 19 Dec 2025 17:29:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 19 Dec 2025 17:29:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5b85993e08e6f6ca2fab32f5edd81d5536953eb539ff93bc7eef6f211c073c`  
		Last Modified: Fri, 19 Dec 2025 17:29:37 GMT  
		Size: 16.8 MB (16791429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6cd3afb1ef3e01ca3a4ebde8b2fa4c08655ef327a565fe49ae9fadb58a5b2c`  
		Last Modified: Fri, 19 Dec 2025 17:29:25 GMT  
		Size: 52.2 MB (52226461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b2fb215164af3ec6850314b6d4f391afb1638a07f20dd2df063a98fe45cb2a`  
		Last Modified: Fri, 19 Dec 2025 17:29:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089b27720a799b2899430bf1c510c7b352c4072b415b031bbde889cd5e85f371`  
		Last Modified: Fri, 19 Dec 2025 17:29:31 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5cdeb24c80ff5bc1532cba67b0f2ab55addc6899ac11c825394d4cd6d3644c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **923.1 KB (923059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb03b64116187ae24c4ce98426a288a686295400dc0bf78938549e4a0569239a`

```dockerfile
```

-	Layers:
	-	`sha256:2e5811880f4188bf67a301c7e0ea674f1eb916fb0084f674aa19ce5a09296c29`  
		Last Modified: Fri, 19 Dec 2025 19:14:40 GMT  
		Size: 903.9 KB (903924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f25a4dc7f1bb5e655703e6b3828fbe3f904ea542f089ff9c8234bb038a387411`  
		Last Modified: Fri, 19 Dec 2025 19:14:41 GMT  
		Size: 19.1 KB (19135 bytes)  
		MIME: application/vnd.in-toto+json
