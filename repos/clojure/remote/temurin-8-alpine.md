## `clojure:temurin-8-alpine`

```console
$ docker pull clojure@sha256:e55acf2fd37c1e4d1bb15f82fe6ecea2621f942a769a32c21a5127dda736b526
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-8-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:f36b53fa0b7dcbccfd6a77f809ea723d54db579d63a865e13d7218d7abf3fa01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97621989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c050842f8719b94e14cb8276fa12f630e1b85a6bc0e24bad1b2664f6a1b480db`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='9fcb96380b25c1d1caec65b7606c387716a7ae51caf359f5f3ff0dcca40f231f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apk add --no-cache curl bash make git && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e051779621babce45fd71367a0c87a5078c4a8c05300e0aaa03c5ed16394f8`  
		Last Modified: Fri, 14 Feb 2025 19:25:02 GMT  
		Size: 16.2 MB (16175443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4119d6c392dd343a89edc4139e141ba64150668fc685c394fecd95daacc9de`  
		Last Modified: Fri, 14 Feb 2025 19:25:03 GMT  
		Size: 52.6 MB (52629492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb653b79f50152b98bc9181e457100d854227740b5903015ff279145de70b2b6`  
		Last Modified: Fri, 14 Feb 2025 19:25:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497368c2ceb6756665d99b9bad58be8b90f42929da7d304904908dae2fee40a4`  
		Last Modified: Fri, 14 Feb 2025 19:25:02 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818f5afd49e8e45369b511102dfaf2ce845960f5b618adc3b4a58e40a761cff1`  
		Last Modified: Thu, 20 Feb 2025 02:29:10 GMT  
		Size: 25.2 MB (25171724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1e880d576df284559cfebe23b90dd622095bf2009b93664bdb3707c978dcc2`  
		Last Modified: Thu, 20 Feb 2025 02:29:09 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:2fc0e74e2a9f4bfc5b02ca01dade6a0b34d36837b05f6800908e09b761bd9d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1265911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379f8140dfdcc47675991bba528f15b4a20407b94ce3e0a1e50d83b61d2837f2`

```dockerfile
```

-	Layers:
	-	`sha256:59339af76b34da50e2f8a62e380ae1981a4622a9d1beb6e550f0b872cababc4a`  
		Last Modified: Thu, 20 Feb 2025 02:29:09 GMT  
		Size: 1.3 MB (1252503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8979b408c36a135170f233dcb6f4f13483bd52ef0090570a5cf7574a130791f5`  
		Last Modified: Thu, 20 Feb 2025 02:29:09 GMT  
		Size: 13.4 KB (13408 bytes)  
		MIME: application/vnd.in-toto+json
