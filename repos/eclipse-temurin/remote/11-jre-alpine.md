## `eclipse-temurin:11-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:640f77aafcb3be736a550f3b2230abbd11acf08221336eec845100d9d116fdfa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:bc6d25668130c07cf8527b335265abe8d2b288c7f51e7d6624f816fdaec7020a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65511602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7ea2fdeba756dc73bbe4b4ae28bea8c305b3e25c808ee7ff92ca1dfb7e99b9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
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
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='905e35f14228904d67a7a56f9f0b8ede58e9b15f9af3a3d54fb86f78c8e47a34';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb2831a0384f7139841ad3dbca976f0db0643b819a108b4c1dce7e255309c4b`  
		Last Modified: Thu, 24 Oct 2024 00:56:33 GMT  
		Size: 18.3 MB (18307482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf742362f936f1af99046582a78334db874b167db3583ca05315acc6ff765ce`  
		Last Modified: Thu, 24 Oct 2024 00:56:33 GMT  
		Size: 43.6 MB (43577909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6b4fa47f17ecc1d38143f39a612776415bfca4ce770911d39abb9902c3cadc`  
		Last Modified: Thu, 24 Oct 2024 00:56:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc8086457f8a9cf1c8dbd7d0182da4f95bbfdfc8f2c59ca55d1624e6cfcd806`  
		Last Modified: Thu, 24 Oct 2024 00:56:33 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2a41484a33b4ab6315a4f5b74e6b5367b2c1b2cf1ef5c8e8adacf4d82025ded6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.0 KB (914040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7770193a3ed7c86bb2a0a128cee7fd477fd5a04036f1510b5d419acae4378d1`

```dockerfile
```

-	Layers:
	-	`sha256:0d492b05c7ff5729f68450e319795c81a96019d11f8756404bf1a397a3fda9aa`  
		Last Modified: Thu, 24 Oct 2024 00:56:33 GMT  
		Size: 896.0 KB (895955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:400a69bb469be8c23856290d9ef40dbf333c2a178a504f8901a6456d6805475a`  
		Last Modified: Thu, 24 Oct 2024 00:56:33 GMT  
		Size: 18.1 KB (18085 bytes)  
		MIME: application/vnd.in-toto+json
