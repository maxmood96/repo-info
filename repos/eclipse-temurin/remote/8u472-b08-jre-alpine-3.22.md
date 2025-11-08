## `eclipse-temurin:8u472-b08-jre-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:441beea859355c41d24bd67c4467d39cc37a8727a498eca908ae37743b74787c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u472-b08-jre-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:12a3125680460d30b69df4045359d90c81d103d5bd9c3b5432fe5220cf21bbb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61937386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cfc34e7cef018000b067e4fafdc9d52e192b9a12fc2517a2a0d3635b38e24f2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:57:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:57:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:57:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:57:12 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:57:12 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:57:14 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='0f169a177121cfd09b43ec5898770717482d02483f07b1b92a2e930dfd32fdb8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Sat, 08 Nov 2025 17:57:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:57:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:57:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251f96a19fb352d61a12a4ba29e56dfcf08b36633e186660d1b95f3501200b11`  
		Last Modified: Sat, 08 Nov 2025 17:57:31 GMT  
		Size: 16.3 MB (16289685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1d722bee532fa2855fc2685790af36e6d13d45fb6b5e2cb479705e1377b6d3`  
		Last Modified: Sat, 08 Nov 2025 17:57:33 GMT  
		Size: 41.8 MB (41842841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50c391699e56ebf080abd2548f6db59350a325bcfbed7b119301d0963130ebc`  
		Last Modified: Sat, 08 Nov 2025 17:57:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9ecec48ede3467b6c2ee632065768fb494a4fee602f819c69e2661e831ece1`  
		Last Modified: Sat, 08 Nov 2025 17:57:30 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d763825d92596fbe5c5a9900b9f5ccbc90220d7c68f4c11655db1994a01948f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **947.9 KB (947935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a2e320759b2da1f16b482b690eaee2d202997c981b092867a05c2595b6d4e7`

```dockerfile
```

-	Layers:
	-	`sha256:80a256f1595a7a5002b23de771eadadb32333e056c7e8e42e2bbd24fd01d916c`  
		Last Modified: Sat, 08 Nov 2025 19:28:08 GMT  
		Size: 929.1 KB (929076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2d38ee7a9aa0982ac85948fc5c85fd388dfac509766715a51ead1c679ecdbf1`  
		Last Modified: Sat, 08 Nov 2025 19:28:09 GMT  
		Size: 18.9 KB (18859 bytes)  
		MIME: application/vnd.in-toto+json
