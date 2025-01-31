## `eclipse-temurin:17-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:0be87fee3f75738a8b9e457404cab39ec2ede8ad08d61e1345f406a029596fa7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:e14d4922b32b61531f21bd1a5ec9ece6b00dc87f1d1724ba5dfa671522e3636a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66398687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f8bebd93c51d9e008048a9846d064c60ed715b7cef5b8d2d36639429df9cc2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='9dcc53a30676692e604571a6e0bd13ac0c1b15f4bc2b78d19f88bd316075f84a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ab26856ac4f725d325530eb0ee080b037f945aa0a7d1b6ba9884132373e0e5`  
		Last Modified: Fri, 31 Jan 2025 01:30:45 GMT  
		Size: 16.1 MB (16135200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb326cca950e7e93fb8a8742863258c98582d6d2df90935e1926c352584514e`  
		Last Modified: Fri, 31 Jan 2025 01:30:47 GMT  
		Size: 46.6 MB (46619364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c7f77008c462a2554e8ba35bfa3631292409ebe3f44b52206cd181866c2695`  
		Last Modified: Fri, 31 Jan 2025 01:30:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b0c9453479824b697beefdd4f4a6e47fc09a3d0e65f2b8b1bc732ffb696fd`  
		Last Modified: Fri, 31 Jan 2025 01:30:45 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:295c57b9b79d96b2350d15570b9786eedc8a1cd7747c29ad1ad4598c69149fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **909.8 KB (909846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5bf05e69fad7b0988020c065d5a7c586748e08e8711822a0b8bd7069d33f0bc`

```dockerfile
```

-	Layers:
	-	`sha256:64375248af8045b855b0a33956871a034d63d69fd6018366e055e0be4fbdc1ca`  
		Last Modified: Fri, 31 Jan 2025 01:30:45 GMT  
		Size: 890.9 KB (890916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91dc69a93bde5e9216a24747acf1fa09724122511eee10bbaa8a8b71250444cc`  
		Last Modified: Fri, 31 Jan 2025 01:30:45 GMT  
		Size: 18.9 KB (18930 bytes)  
		MIME: application/vnd.in-toto+json
