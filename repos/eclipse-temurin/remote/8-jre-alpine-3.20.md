## `eclipse-temurin:8-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:0dfea18f211b7750ea079133ec6f68ca1ec900e1bea87d8ed3f6dc9473d77dcd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:d579ea80e3e4e024fd7a7171a05d61ba0d7e8b84367e3e18b7b01a43bd1188e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61460938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a712417b3cdafa21b56a1cf101b11e5cfa198312c7665b0ba9a171a3943a8c4b`
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
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='fb10b6185c76cb48bdcbb76e466adc319b37ffc0b1cf89708a1f13e94adcc12c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
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
	-	`sha256:ae04bb5327137742b378c381e5b541347111fe8afdff2299d3cec7799f58e29b`  
		Last Modified: Mon, 04 Aug 2025 19:11:22 GMT  
		Size: 16.0 MB (16011666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c274b14e909e1c1b96c059b15ded2172fa0590a36e14528e8fd609e8db6760b`  
		Last Modified: Mon, 04 Aug 2025 19:11:26 GMT  
		Size: 41.8 MB (41826389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bef1303ebeb429082c7ab07509a6d95a8111a579bc73d6a3c8678c6e253aee`  
		Last Modified: Mon, 04 Aug 2025 19:11:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6b716faa1bef4d2899f3a63fe5021d03cd101f69664de449fcaa95d4339260`  
		Last Modified: Mon, 04 Aug 2025 19:11:24 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f407adc124807f013297b791b03880a04565d69cc761a03d858cc2f21648ce38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **935.2 KB (935213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e69f103f708954d6ca19cee9843042b8025fa749e6fe2c39e9fc471cbc8200a4`

```dockerfile
```

-	Layers:
	-	`sha256:6db0a90c502e188af6d84f5842c9b7cc3fa6e0edcd13061e68682a4b52b47ff9`  
		Last Modified: Mon, 04 Aug 2025 21:29:09 GMT  
		Size: 917.0 KB (916983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc1e85a951b09bea5bc8cae3cc98af8f410fe1a7f22e3e7f53e5246a29a2a3c`  
		Last Modified: Mon, 04 Aug 2025 21:29:10 GMT  
		Size: 18.2 KB (18230 bytes)  
		MIME: application/vnd.in-toto+json
