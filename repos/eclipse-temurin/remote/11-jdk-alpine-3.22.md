## `eclipse-temurin:11-jdk-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:1f8820fcea2e96c4c6fa9851164b6d3a935600efd9e38009af832f850ffcc1f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jdk-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:e2780dcc88bad9be5a370611ad4b1f1abe5cc2ce6914342acab3dd7b25654864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161018067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433dd29c442b5c0171c48a5b4577d99fae8376ef41d9f87d150b04b604de4f29`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:15:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:15:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:15:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:15:13 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:15:13 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Thu, 05 Feb 2026 22:15:18 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='b55a38b75ba99d86f4adb47552ee5306b9589e2026861a3b8f030993c42aedc7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:15:20 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:15:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:15:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:15:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c180cd39b917ec12c520a1c9fbb2222879be7ee4a20658fe911f3eb5428ef86b`  
		Last Modified: Thu, 05 Feb 2026 22:15:33 GMT  
		Size: 16.3 MB (16294084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a53b5e6f91f1ff32bed1c668506b90afb76985ad9ca687d305de9fb60f6c5c6`  
		Last Modified: Thu, 05 Feb 2026 22:15:36 GMT  
		Size: 140.9 MB (140916696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ec050240a37b134eae130d1c8a581f8dc3f6a1812c89605de53cbc4807a7c8`  
		Last Modified: Thu, 05 Feb 2026 22:15:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96c93e36109ea2a306fb075bbc7ff50e92749a35558908c668257852f7ef819`  
		Last Modified: Thu, 05 Feb 2026 22:15:33 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:35f0a895beb4308e6a670467bb777410151114f3fe09a1e1dc4de7aa4043fefe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1021465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7c95df05e83351d0554b4cb3b35121a8d8cfb1a573664e8933149b55845f48`

```dockerfile
```

-	Layers:
	-	`sha256:fd725c5fb20abd32f2053cd52f01f6385da425cd332bb08c9d5a47748d29f9b8`  
		Last Modified: Thu, 05 Feb 2026 22:15:33 GMT  
		Size: 1.0 MB (1002296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c5d217154f47a2ad3f088b79050f8abf3397b072e4e1f1cf30bc241e0ff35a4`  
		Last Modified: Thu, 05 Feb 2026 22:15:32 GMT  
		Size: 19.2 KB (19169 bytes)  
		MIME: application/vnd.in-toto+json
