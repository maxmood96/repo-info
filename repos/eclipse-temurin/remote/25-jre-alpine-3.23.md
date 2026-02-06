## `eclipse-temurin:25-jre-alpine-3.23`

```console
$ docker pull eclipse-temurin@sha256:f10d6259d0798c1e12179b6bf3b63cea0d6843f7b09c9f9c9c422c50e44379ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:25-jre-alpine-3.23` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:0611ca158a2497b7ed6c2594a06fe88aa234401af0a43495f084ba1e986eba50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75302325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f90451d7057c02a546ab8b19b8f67fd9e541c5566667318127d0f854dc3bb1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:21:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:21:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:21:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:21:06 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:21:06 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:21:10 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='159099235c536b152f86111a694a8a03392948924736f354c79e95532dcfc1f8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='2cbb356c6923f89814b892561e6f0377ecf035ab0577e3162d2cf4e202d38ee7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Thu, 05 Feb 2026 22:21:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:21:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:21:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66e3d5010047b5ca0b8fa231570286b8249f2d4faf4358ddd71314ec67c153a`  
		Last Modified: Thu, 05 Feb 2026 22:21:22 GMT  
		Size: 9.4 MB (9448886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecbfe883bca4093948b63e6c842f4207daefa150f22c971b5d9b6bd0ec9e74a`  
		Last Modified: Thu, 05 Feb 2026 22:21:24 GMT  
		Size: 62.0 MB (61989209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5400f68ee905c01db8562ec8e7e17fc3c65a6e709687983e508fb7d5e51ece5`  
		Last Modified: Thu, 05 Feb 2026 22:21:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf082752c8dc70f8ecfae2223dfdbcc25f98f63b2c8581e87a75076168b1aea`  
		Last Modified: Thu, 05 Feb 2026 22:21:22 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d9a15b97d82ae573310bb67e7ddf8e2eddd6915a5b8a9cb16c7869b89c995dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.8 KB (822849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1440a386d2373fec40a3147d74e02939d1ad8c8b021972d664194d3a11675c03`

```dockerfile
```

-	Layers:
	-	`sha256:4b023acdb245fd9bdc4e5bbec2a34aa2590219ad2f4a12869f3fdc535cdaa297`  
		Last Modified: Thu, 05 Feb 2026 22:21:22 GMT  
		Size: 803.0 KB (803038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457e3a6b222b0468d5e7fcc4fdb4cbe83afdd721fed5046e50408fbc12a6f199`  
		Last Modified: Thu, 05 Feb 2026 22:21:21 GMT  
		Size: 19.8 KB (19811 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-alpine-3.23` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:aee45b2043d25e952af64ccdbbfdb21a37f744793ef985e0e1713032cef144c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74583868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0880c4d6acfdaea044a723398f9a176b92f54d75741c7467e05262a7527ca31`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:20:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:20:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:20:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:20:12 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:20:12 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:20:17 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='159099235c536b152f86111a694a8a03392948924736f354c79e95532dcfc1f8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='2cbb356c6923f89814b892561e6f0377ecf035ab0577e3162d2cf4e202d38ee7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Thu, 05 Feb 2026 22:20:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:20:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:20:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc0a193fb3985683a97656c409f169d3e81dc32b27bbd39a979dc99a6e836d6`  
		Last Modified: Thu, 05 Feb 2026 22:20:29 GMT  
		Size: 9.5 MB (9469498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cee1363b9f89efc0b592349f02acd07b8b0c9dbab0492c3a9a85b36f911b24`  
		Last Modified: Thu, 05 Feb 2026 22:20:31 GMT  
		Size: 60.9 MB (60914871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d7f4a95d7445d1b9f5346b199da293cb28cefe190e3caaa52694563d293229`  
		Last Modified: Thu, 05 Feb 2026 22:20:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b41a46a79df2394a39814cfe020406c8f8635ff00755e2bd9cf01c5d00dbe9`  
		Last Modified: Thu, 05 Feb 2026 22:20:29 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c27f20128d71514d0317e1a1a75d337ac8ae4e073b09e1847745c00b74fde3bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **821.8 KB (821768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeaa0de024a739de37d7599b8c14935c1a16772f07453e69124cb5e3669c57d0`

```dockerfile
```

-	Layers:
	-	`sha256:13a355e82dece2b1215c35b0356d7d902521e780cf52d6ccbd8506bf65cdf481`  
		Last Modified: Thu, 05 Feb 2026 22:20:29 GMT  
		Size: 801.8 KB (801823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f150271df7b79bb59983aceb385b826df8f90d5d4d51dda116781330a011c6c3`  
		Last Modified: Thu, 05 Feb 2026 22:20:29 GMT  
		Size: 19.9 KB (19945 bytes)  
		MIME: application/vnd.in-toto+json
