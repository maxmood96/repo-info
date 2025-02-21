## `eclipse-temurin:17-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:e738316b3b831ccedd12ec29120368116297c5950576de52196478871e92f0e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:b8827a8627b7a25fa91253a1b736013c2ae9b2c1b36d65593f79b60357b75e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.0 MB (168013517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b497486054444b3b13ba2b273ed3410c8c7e4e4c08ad99f49a65864876fe1a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='259c85e16f7bbfdfb3e0a2ec1c5d6e2063300d413422286583265a9d8a882358';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2e3832591710b1cdf22cb08628cbc16b675b1d4e3a90b8cc1fb5bc352044ca`  
		Last Modified: Fri, 14 Feb 2025 19:25:39 GMT  
		Size: 20.7 MB (20667778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d703e74ae122e03bea9fbf9c00772600fb314d9014976d348b6d8cc33a58d9`  
		Last Modified: Fri, 14 Feb 2025 19:25:41 GMT  
		Size: 143.7 MB (143716432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5cb72880b11e33c13b36b974d11617d0967f571975d77c6778a380e0960ff2`  
		Last Modified: Fri, 14 Feb 2025 19:25:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419a54e866532891566322abeaf664ae50419fb72717fa2e162c169295cab2ef`  
		Last Modified: Fri, 14 Feb 2025 19:25:38 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a40bac0810ca5367804f08a44f76444b95fe96a117ac10d166fb5399620d645e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1083778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912d09da6bafab62d81eb7c153b55d8645c8e283ba68c2fafec622bafbdcd75c`

```dockerfile
```

-	Layers:
	-	`sha256:ea239a33ed65479ee3709ff341c1c8864e9f4f61e56c0120cb98e184e97395e8`  
		Last Modified: Fri, 14 Feb 2025 19:25:38 GMT  
		Size: 1.1 MB (1064124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:181a24ac5abdfa88f4eca3b8c0a5b50660eb591e53be6f62299e4e11805a9aac`  
		Last Modified: Fri, 14 Feb 2025 19:25:38 GMT  
		Size: 19.7 KB (19654 bytes)  
		MIME: application/vnd.in-toto+json
