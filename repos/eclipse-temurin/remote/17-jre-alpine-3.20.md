## `eclipse-temurin:17-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:0fdc57e9edfd902bf9a53bf99a7995f7c2e9e8f349a44a64781bdb3063729c8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:ad261608a7f2cef47fdab88f9b1c92eae8ba831058a42145b0eb27ed6afa6f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66299145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a814b6464e34d2292093075694c3a016445e695c5f4e1a28edece0a9f4d8a0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
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
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11e8e47a558cb2cef41052ceb2e3340ba71a4039b6b0d5672d15b7fd287d830`  
		Last Modified: Mon, 04 Aug 2025 19:11:22 GMT  
		Size: 16.0 MB (16011727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18632da7630052223819e3f7f4ef1659e36adfaeb59a69c9fe4e026c3b8ae3a4`  
		Last Modified: Mon, 04 Aug 2025 19:11:22 GMT  
		Size: 46.7 MB (46664533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6284af1352cf8567a317e4f2ae16aca812efe42c9bd7324c7a77151f815545`  
		Last Modified: Mon, 04 Aug 2025 19:11:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ad722bed61bc77d1d5b5149c4909bca01ae3d92c63bdbc6d1bdce96fcad352`  
		Last Modified: Mon, 04 Aug 2025 19:11:20 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:081984f2e6d1b10ddc1cd64dd0bf30c1ab5e53a6cc56ad9cd22296e8c30cc027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **903.9 KB (903883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05080a1831cf1cb6ab21f08aba56f763870aa38fca5f65ae58ea5a3f37c6753a`

```dockerfile
```

-	Layers:
	-	`sha256:b02503aacc58ed01a7486f58608922a4b20ca41348fedfb028cfb0f3065127c2`  
		Last Modified: Mon, 04 Aug 2025 21:18:08 GMT  
		Size: 885.6 KB (885626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f2ea8c98aca08c8b842d7a99085bae5d9b1363d75876963d500e665fa5e4bb`  
		Last Modified: Mon, 04 Aug 2025 21:18:09 GMT  
		Size: 18.3 KB (18257 bytes)  
		MIME: application/vnd.in-toto+json
