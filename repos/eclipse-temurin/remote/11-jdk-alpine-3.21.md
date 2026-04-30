## `eclipse-temurin:11-jdk-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:444daaf678b8459bdf4b2fd7aec4fbb30ab78bf513d4c5d304a71a8bc586a7f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jdk-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:8c2fed1fc1e55f921b0302bfb7b1679b24941bccc20af95711fd98487d7d6a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160922385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b469522ffdc91995524be10e22e055d9b5223e7f66aa0c96edd35e1b97d59d7b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Wed, 29 Apr 2026 22:44:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:44:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:44:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:44:49 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 29 Apr 2026 22:44:49 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:44:54 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='ed06a4b8381786a6e8091c10539856675497d2b821cd2d0200cc5b65f453b982';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 29 Apr 2026 22:44:56 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:44:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:44:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 Apr 2026 22:44:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c654d328dd4efcd808ec8e09ffe55032771704dd0756a8962a73e56bab870183`  
		Last Modified: Wed, 29 Apr 2026 22:45:11 GMT  
		Size: 16.2 MB (16198530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaeabedcc37bbce513aba50adc4a4352af984d364093322d68258ad945f227ff`  
		Last Modified: Wed, 29 Apr 2026 22:45:15 GMT  
		Size: 141.1 MB (141074569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e852a119f3c345deb3186e4a1a7db2bfe4fd659c8e3e6f06b0ea4e70d62e27d`  
		Last Modified: Wed, 29 Apr 2026 22:45:10 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97cca298e453435ad2ef4457d5d79f542e165c1aee55bbef6b2c9919c93bcce`  
		Last Modified: Wed, 29 Apr 2026 22:45:10 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3616e8d763c7542f3a983b39ac7f3fe80d9f7c06e76a6a8c4bc1e95f183ec991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1019248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0928491e6344436610a9a8dcd60f74ea2157af7c50809ac3550a6004f228aa44`

```dockerfile
```

-	Layers:
	-	`sha256:eff22f5eb0d121f84eeac92b5df0dfa008ab1901a06b4f6b5d4347f5f616df48`  
		Last Modified: Wed, 29 Apr 2026 22:45:10 GMT  
		Size: 1000.1 KB (1000068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f111db3b6658c476278b321fd3b44ff9cdc1f881734701ee2588abf3431eb947`  
		Last Modified: Wed, 29 Apr 2026 22:45:10 GMT  
		Size: 19.2 KB (19180 bytes)  
		MIME: application/vnd.in-toto+json
