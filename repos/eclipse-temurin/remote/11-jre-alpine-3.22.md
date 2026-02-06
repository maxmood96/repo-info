## `eclipse-temurin:11-jre-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:04d50472fdcfe6b09062b87906deca1d6e5b6fbb4cebf0f1eb2ea35f3b6f0c0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jre-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:2430afe65bb4466ede981d5a3b52159d128fdb26a18e5a87edbb83917709edf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63731449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044c53bc2368e0a02069223e35768477e5845f89120fece479450a0cdb58e2fc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:13:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:13:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:13:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:13:10 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:13:10 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Thu, 05 Feb 2026 22:16:26 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='b30f7db6fd41047c60978bd2c88b6b9bea108803482db4e163dd7fd2b1aec1f7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 05 Feb 2026 22:16:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:16:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:16:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1834a48a3505266cb3bc79db26f5ee911ce1e0fdccfb7f4652897577584b3f3f`  
		Last Modified: Thu, 05 Feb 2026 22:13:25 GMT  
		Size: 16.3 MB (16294159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbf5374ff29bf98fbfeccee86b45a4396939136a1c9b23faca892e2fe536710`  
		Last Modified: Thu, 05 Feb 2026 22:16:37 GMT  
		Size: 43.6 MB (43630007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5b4088e7fdffa6472067b0459b57feae49b2b19841cfc0aa4fc68d27b8c3fa`  
		Last Modified: Thu, 05 Feb 2026 22:16:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be9c3a64154ffe2219e6b5b6bef90b671481c6b31c5da9dee01069c080296a9`  
		Last Modified: Thu, 05 Feb 2026 22:16:35 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:164279979a38abaff7f8cbaa77bca0d1c5566e4e5fc37f1f29fda7ac8aa08e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **929.0 KB (929004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ea908b20b50a32e6e87b128f6534599edff0e44d6e75a6faf9068221250af2`

```dockerfile
```

-	Layers:
	-	`sha256:11301e69bbb6ef045a08b773100aa531566da48cb51042423a81f16bd0406c9d`  
		Last Modified: Thu, 05 Feb 2026 22:16:36 GMT  
		Size: 910.8 KB (910790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36e3110d1d415bf2f0ff4db6200be06d52861d2fe8d85130200d1fc763f1df44`  
		Last Modified: Thu, 05 Feb 2026 22:16:35 GMT  
		Size: 18.2 KB (18214 bytes)  
		MIME: application/vnd.in-toto+json
