## `eclipse-temurin:17-jre-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:a8cea3518f32fcb73198d9e7343f11c38f00df0aa211d759570452a690f5940a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jre-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:c9474309ce05720ca26fa44ebbf8e973625c28a2ab02df8ba64963e1cda1dc1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66467272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d798a4426461a8a143da12b83756f75accf6b421aed4fcbc344a944039e2f2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='88424be8b71d7c801c39866cf19d3b7c49b1c499cdccfa292e103c7cba08c21b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335f9325ba32b16442fdbd2743155c15a66d7e012198d46bda9fa539e4bd653c`  
		Last Modified: Mon, 04 Aug 2025 19:11:19 GMT  
		Size: 16.2 MB (16162761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18632da7630052223819e3f7f4ef1659e36adfaeb59a69c9fe4e026c3b8ae3a4`  
		Last Modified: Mon, 04 Aug 2025 19:11:22 GMT  
		Size: 46.7 MB (46664533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6284af1352cf8567a317e4f2ae16aca812efe42c9bd7324c7a77151f815545`  
		Last Modified: Mon, 04 Aug 2025 19:11:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bb5da1a24523a0af1966f13d7bc9ffb567c894c91c19968adcfc1fe0ea1653`  
		Last Modified: Mon, 04 Aug 2025 19:11:18 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a15d11aaffe6f80dc186fc73ee6884663002a77ae1cd6b651df1a1b674ce49b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **911.1 KB (911134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0cb3e758bb4e176af516c26b3e225e463ea7a17310e70cf86c03aa9c256b1d`

```dockerfile
```

-	Layers:
	-	`sha256:a8837f35f1fd9b8d0852f0fe6d1362091d63f19e9d9dcbcd7f1addaa9876fd0d`  
		Last Modified: Mon, 04 Aug 2025 21:18:10 GMT  
		Size: 892.9 KB (892877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2797d25cfee1b01b9d823e63ec951761ee79601d617d7b7e46e642a9a2832b1c`  
		Last Modified: Mon, 04 Aug 2025 21:18:11 GMT  
		Size: 18.3 KB (18257 bytes)  
		MIME: application/vnd.in-toto+json
