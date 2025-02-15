## `clojure:temurin-8-tools-deps-1.12.0.1501-alpine`

```console
$ docker pull clojure@sha256:240f00c097a4b6e2afa78f9237d7a02c6de43a16013e22a9f8d7b795ab93972d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1501-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:3ddc0e66e4d77541668e1b225454a1fe55b1b5195808a180b2ca1c223f377391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97622132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae2ca6d6ba0908c44186f2d60bd7908631403eb3fbb3516ceb5b3ef4e6c8a33`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["/bin/sh"]
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Jan 2025 19:11:46 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 29 Jan 2025 19:11:46 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='9fcb96380b25c1d1caec65b7606c387716a7ae51caf359f5f3ff0dcca40f231f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apk add --no-cache curl bash make git && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e051779621babce45fd71367a0c87a5078c4a8c05300e0aaa03c5ed16394f8`  
		Last Modified: Fri, 14 Feb 2025 20:36:22 GMT  
		Size: 16.2 MB (16175443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4119d6c392dd343a89edc4139e141ba64150668fc685c394fecd95daacc9de`  
		Last Modified: Fri, 14 Feb 2025 20:36:11 GMT  
		Size: 52.6 MB (52629492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb653b79f50152b98bc9181e457100d854227740b5903015ff279145de70b2b6`  
		Last Modified: Fri, 14 Feb 2025 20:36:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497368c2ceb6756665d99b9bad58be8b90f42929da7d304904908dae2fee40a4`  
		Last Modified: Fri, 14 Feb 2025 20:36:07 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab03cc83cfd810358367c583e4655583c383f4bbf931850603e7c9e0bd31fc5`  
		Last Modified: Fri, 14 Feb 2025 20:39:07 GMT  
		Size: 25.2 MB (25171867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c056ef9b463ac85ea0e73edcbfb66a92ef2bd620015e33353a7daec4368880`  
		Last Modified: Fri, 14 Feb 2025 20:39:07 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1501-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:ff44a7704d807b2e614e0c2140e4471bdf128df729834aed75380bff96787e7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1265910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a173ad179eb0d25e1b3723ae32e0df9d7dc6ccfa445b1d5820c75b9217299f6c`

```dockerfile
```

-	Layers:
	-	`sha256:d0e9914c179e62f89d68844d04edcf9b3b67894a6175e140bb99efff33c8f0aa`  
		Last Modified: Sat, 15 Feb 2025 01:36:05 GMT  
		Size: 1.3 MB (1252503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7199da77170f89ed4e9fdd353d1528af1ae28d3cb46195dfccb1d92f8d68f961`  
		Last Modified: Sat, 15 Feb 2025 01:36:06 GMT  
		Size: 13.4 KB (13407 bytes)  
		MIME: application/vnd.in-toto+json
