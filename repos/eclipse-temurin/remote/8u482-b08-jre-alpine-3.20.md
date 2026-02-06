## `eclipse-temurin:8u482-b08-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:cecb9d686582e8d34f3bdc72c3605f654edf8792c81f57c4c9bec69ea1150031
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u482-b08-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:2689ed70bbc9e6b72535d049d24d64219f9d5113312790f204b2fd51fdc379df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61968305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb18fbb13d4ca1295eedd62b9789d162839d0f5970672d09dbc7726ba05b341`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:14:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:14:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:14:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:14:09 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:14:09 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Thu, 05 Feb 2026 22:14:12 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='c1b64ab1d2c96ac0fd89c60377396cc4457f954ee7ce931f3a0e547f701e6595';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 05 Feb 2026 22:14:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:14:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:14:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9f9ac5610fc517155e0d020f98577d6ea9a151a84839cf23bfb721c67d756d`  
		Last Modified: Thu, 05 Feb 2026 22:14:22 GMT  
		Size: 16.1 MB (16081507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247c2e0bd6007899e262a0370c683ef6ef5f351949d636033a7f4a108d8bc77c`  
		Last Modified: Thu, 05 Feb 2026 22:14:23 GMT  
		Size: 42.3 MB (42256525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65a8dd6d689e985c1b83b9c162de472d737263caf1fb92ce4d3f6d0c3a6f90c`  
		Last Modified: Thu, 05 Feb 2026 22:14:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a6c873438ab36e111d6ae84fd1ef9dd7912053836ba773c48805e5faf1c66c`  
		Last Modified: Thu, 05 Feb 2026 22:14:20 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u482-b08-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9a2bc8193c4413844ba813ac436deab5ca6c32bc09b29e8136ca15567cdef26b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **939.2 KB (939185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14cff5ffce561ce2f2c1c85011a8b56cbb3edf97d3cca6372609d9614ccc2b5d`

```dockerfile
```

-	Layers:
	-	`sha256:2180bd5864af4e539d1efe468accb273bb6084305576004a4e9f940172218983`  
		Last Modified: Thu, 05 Feb 2026 22:14:21 GMT  
		Size: 921.0 KB (920998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05054dfaebbb7eb4a57ccfa1c31ca8e7a81dd202eae0bd4e1e28475ed0d2054d`  
		Last Modified: Thu, 05 Feb 2026 22:14:21 GMT  
		Size: 18.2 KB (18187 bytes)  
		MIME: application/vnd.in-toto+json
