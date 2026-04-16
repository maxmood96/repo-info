## `eclipse-temurin:11-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:516dcc2cebc02778a0543738f8b07ec4a8cacaa673758b3cad7870875b51cda2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:487c92e02075a92ddd9f8fef406d686908b1312e1889dd81569ae53ba3c8f91c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64334545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b319d89df5654315a14d32539ca6515a464d5792771e1769e7ec99598aa9dbd8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:32:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:32:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:32:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:32:59 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:32:59 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 15 Apr 2026 20:33:03 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='b30f7db6fd41047c60978bd2c88b6b9bea108803482db4e163dd7fd2b1aec1f7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 15 Apr 2026 20:33:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc73401d8e41e2e6ae06d762225d12796ebcea3f0b1936943ea8fb087fc5936`  
		Last Modified: Wed, 15 Apr 2026 20:33:13 GMT  
		Size: 16.8 MB (16837807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d264d73c038af3c32de3d18de00db70f1505568cdb20b0ecbde8d22d9c0772`  
		Last Modified: Wed, 15 Apr 2026 20:33:14 GMT  
		Size: 43.6 MB (43630142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b360e8de94bc536979183ca483502976428c1e609b9823babd16bcee251fb4`  
		Last Modified: Wed, 15 Apr 2026 20:33:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20074f042dc2b34c28b69199e326c1683130144bdfa09aa38a35cdfd94beeb2`  
		Last Modified: Wed, 15 Apr 2026 20:33:12 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:22ce29463bd7cdb007f2ec0b1339b4e412d4aa4777c69a3d777affea0d1cb855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **934.0 KB (934009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6d6b89c9cc7ef70cc18695390c3e8c67c4104b300bd43bda04191d276e0e56`

```dockerfile
```

-	Layers:
	-	`sha256:e668b75bf736eb0dc68adc1e129a1fdb7f092165bff723ee1e3c3e647926df1c`  
		Last Modified: Wed, 15 Apr 2026 20:33:12 GMT  
		Size: 915.1 KB (915122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46050147a0f8ae7b1248b3a657415942f2c6fe9c62ab427c9e624213adeaa8cd`  
		Last Modified: Wed, 15 Apr 2026 20:33:12 GMT  
		Size: 18.9 KB (18887 bytes)  
		MIME: application/vnd.in-toto+json
