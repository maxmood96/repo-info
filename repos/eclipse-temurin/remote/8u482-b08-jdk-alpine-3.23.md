## `eclipse-temurin:8u482-b08-jdk-alpine-3.23`

```console
$ docker pull eclipse-temurin@sha256:8c682b1926dabc805ad862e8fb5c16a40d855a95c979657cbc0edc1bc43f6779
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u482-b08-jdk-alpine-3.23` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:3d0564b740e651cc465343af05dd318f559282dd9c5df55baa4784ae9e9cc19f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73761273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06120dd360e75d60f5be28683cbb15ce9b7d8f6673404425b0ed92bbf43fa00`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:13:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:13:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:13:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:13:12 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:13:12 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Thu, 05 Feb 2026 22:13:15 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='149565c3de89ef9ceb640312ff77aadea79fb82fa946ae9aab4d024ba25eb47d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 05 Feb 2026 22:13:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:13:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:13:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba30a9b9fbd57b01a8081d96f19cccf9befdb10d3a054b012d5419c813f251a`  
		Last Modified: Thu, 05 Feb 2026 22:13:27 GMT  
		Size: 16.8 MB (16839871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b65cc608a32035ca289bff3c4fea696fb1ecf0823a86c91ed423dd94dbf4d8`  
		Last Modified: Thu, 05 Feb 2026 22:13:28 GMT  
		Size: 53.1 MB (53057148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089ec9d3b4a0ae2f48cbd3f356a2342c62ba56808906410a919e563894ca3963`  
		Last Modified: Thu, 05 Feb 2026 22:13:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4758e0f4968b23dbc7eddea73b3296e03df78caea6faffd00fde093c4fdd8f`  
		Last Modified: Thu, 05 Feb 2026 22:13:26 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u482-b08-jdk-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:59e5c15058753c3c18e2d94732ffc3f706ee600d7b6ad9dce6dc0d5501717c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1129301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7559482592788a4f9191032e0442387b51e3de9a5b8095f0d1795dc47a19d7c`

```dockerfile
```

-	Layers:
	-	`sha256:ad8f19d55830fe2270aa497c12dd14a1589684efcdf10ef0390438d7204f0d4f`  
		Last Modified: Thu, 05 Feb 2026 22:13:26 GMT  
		Size: 1.1 MB (1109598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fcc847e3bbd2cb4aa2ddabaa8d8b9d8ea1328bccd9d87415ce5e74f8ff6122f`  
		Last Modified: Thu, 05 Feb 2026 22:13:26 GMT  
		Size: 19.7 KB (19703 bytes)  
		MIME: application/vnd.in-toto+json
