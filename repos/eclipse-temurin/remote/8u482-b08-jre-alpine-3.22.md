## `eclipse-temurin:8u482-b08-jre-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:1268883c2df69d54738b42e9b6baa0fb17b06e81de37dfbffd64dcfd49884776
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u482-b08-jre-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:1957e3faaa6490e93ad324b0afe30e5b75eca955343c1336302d54e7f55009a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62358012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f13a665716733b8da7a8133c65ab041902337236f251d89027e9f6d903ccc5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:13:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:13:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:13:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:13:10 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:13:10 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Thu, 05 Feb 2026 22:14:15 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='c1b64ab1d2c96ac0fd89c60377396cc4457f954ee7ce931f3a0e547f701e6595';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 05 Feb 2026 22:14:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:14:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:14:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1834a48a3505266cb3bc79db26f5ee911ce1e0fdccfb7f4652897577584b3f3f`  
		Last Modified: Thu, 05 Feb 2026 22:13:25 GMT  
		Size: 16.3 MB (16294159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40975502800ba388fefc119c4e979db2cfe4cbb2921951ef9c913cb1b088a7d`  
		Last Modified: Thu, 05 Feb 2026 22:14:25 GMT  
		Size: 42.3 MB (42256571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5669df24642265922a008873595fdc57d60d25bc8cc5c5a23ff55795dada1b1`  
		Last Modified: Thu, 05 Feb 2026 22:14:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd72d329daabbd7963084469d2e69f64404f0be87c09654d877df0cdff3ccf4`  
		Last Modified: Thu, 05 Feb 2026 22:14:24 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u482-b08-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f19fc55c258339fb50ec8c2260d1e3eb48d0fb9b01081b62e488e76ad0971054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **947.2 KB (947218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c1b7fb1fe3d89418318af997c385e56d7cc1202ced9a5d929552c40c4a22840`

```dockerfile
```

-	Layers:
	-	`sha256:63e0a99d163efb883e1c49b8edb5e55947d8ef9ef794e570f0d5bded198e70ef`  
		Last Modified: Thu, 05 Feb 2026 22:14:24 GMT  
		Size: 929.0 KB (929031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6e421b313c8f88c3bb9202ab26b58890167a95ee9e174fc4249ea4de7c60cf4`  
		Last Modified: Thu, 05 Feb 2026 22:14:24 GMT  
		Size: 18.2 KB (18187 bytes)  
		MIME: application/vnd.in-toto+json
