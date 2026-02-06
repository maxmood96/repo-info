## `eclipse-temurin:21-jre-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:cfe82487280a59c5a0887b2ec08f50d389540950e373a8f3fdcd093c33428cf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-jre-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:3a04c1de3d04de7bbd24a73a3e0100feaae935677eca47e631dcd1c8cde86c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72989620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe004c73c3a88dd47771bc84865419e7f9b60e6eded8e4df84f4f8a959b5268`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:20:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:20:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:20:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:20:40 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:20:40 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:20:43 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='d1cd7b33dcd81293b0b705f4d0e79adce092786be31736a63abe6a4b31841ae5';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='4f6200277644afe6ad49218ae1dd45ab3d0d0b2ac4109163604e36156a93a306';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 05 Feb 2026 22:20:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:20:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:20:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9aaad2b85a32d911dc8ef6a759e7d8b9f8f8b8ac2b4c7bfe12df93bb0f9c148`  
		Last Modified: Thu, 05 Feb 2026 22:20:55 GMT  
		Size: 16.2 MB (16174729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc8bcc60a9b06076cebd4f3a5291eac1545ca232e31bfd02ed05a5f7200cc08`  
		Last Modified: Thu, 05 Feb 2026 22:20:56 GMT  
		Size: 53.2 MB (53168741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f87dd2e72624130d86590fbbff1c6bb99b84d8676606fac7f279eb86d14333e`  
		Last Modified: Thu, 05 Feb 2026 22:20:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1a77072027415066a78c7bb06e185e4b6d99d5b8e2ebff090a97a8087ae4f8`  
		Last Modified: Thu, 05 Feb 2026 22:20:54 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ee12f72044b19b13d33c7e8b69dff20fb57dfe75416b3f57ee90c59cb0ab204a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **917.0 KB (917017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8254dba285fbb48fd787c87aebdda2b12dbb4a9eb5fadc1efd36f67efdd64af2`

```dockerfile
```

-	Layers:
	-	`sha256:6e1b8153b358ce856f57ad0ed7dfa180daf99caa43ae28ce7b9c8e53419550fd`  
		Last Modified: Thu, 05 Feb 2026 22:20:55 GMT  
		Size: 898.0 KB (897992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd31583507b00834203b3c92e289b096401c4be01515059731ae355b97854894`  
		Last Modified: Thu, 05 Feb 2026 22:20:55 GMT  
		Size: 19.0 KB (19025 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-alpine-3.21` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:6f54b07df82a6f1e894b3002e2001011afd155e368ddb8ae10720c6b4a610c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72374447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4245c12f40f7f39a1d3894acfaef5ac2bff9df557146d3d74f989ef41fdac37e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:19:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:19:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:19:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:19:36 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:19:36 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:19:39 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='d1cd7b33dcd81293b0b705f4d0e79adce092786be31736a63abe6a4b31841ae5';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='4f6200277644afe6ad49218ae1dd45ab3d0d0b2ac4109163604e36156a93a306';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 05 Feb 2026 22:19:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:19:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:19:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc92af5a4af214413494e76e2ef559460dbd936af8bb6f1ae2fd193ccf415ad`  
		Last Modified: Thu, 05 Feb 2026 22:19:51 GMT  
		Size: 16.1 MB (16138559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71461330617831476a476dd44f1f99bdfb5ede3f7a3431895d16a0d2acc772e8`  
		Last Modified: Thu, 05 Feb 2026 22:19:55 GMT  
		Size: 52.2 MB (52240599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2bae8de697a4524f63ffa6f41cbc334104aad6bac52302a26bae0cd76983ec`  
		Last Modified: Thu, 05 Feb 2026 22:19:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ba425da6d1b75003206beb0d69e1a811d7834254180f5e86912f5cb41ae914`  
		Last Modified: Thu, 05 Feb 2026 22:19:51 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:803bd585442e5225cf0ae0ec95eecc7a36748a1515f36ef6b5d44deb7f6de46b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **916.5 KB (916541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8877e17a4a4f105c1f97ab389db60cb5bb8f70cd077705347ec11c3075ed9f`

```dockerfile
```

-	Layers:
	-	`sha256:3d4b786a3e987231298313000ff27d258bf750dcccc78a08d0158b089b779acb`  
		Last Modified: Thu, 05 Feb 2026 22:19:51 GMT  
		Size: 897.4 KB (897406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee358e87f454b20d6502064d7d84de40338c502d001796c134bbff97eb38a6d5`  
		Last Modified: Thu, 05 Feb 2026 22:19:51 GMT  
		Size: 19.1 KB (19135 bytes)  
		MIME: application/vnd.in-toto+json
