## `clojure:temurin-11-alpine`

```console
$ docker pull clojure@sha256:2d6f25cacad33720116e74d41085a4e519807254ddf1e7b1a3fa56e1db4e7a80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-11-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:fdfd713e283b62d8ba505eb3473ea16c9c2d1085c8e9c30e81a27a04d6cea179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.2 MB (187218131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e484f7566937cb4b78078e12873a3fbd73846196a07cdbb48d2f351ac19ae1e5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 29 Apr 2026 22:44:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:44:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:44:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:44:05 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 29 Apr 2026 22:44:05 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:44:16 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='ed06a4b8381786a6e8091c10539856675497d2b821cd2d0200cc5b65f453b982';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 29 Apr 2026 22:44:17 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:44:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:44:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 Apr 2026 22:44:17 GMT
CMD ["jshell"]
# Wed, 29 Apr 2026 23:14:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:14:53 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:14:56 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Wed, 29 Apr 2026 23:14:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:14:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c175c39880efd27b1b0b6f4b68db4424c3664c1899709c2068bc4301855817b`  
		Last Modified: Wed, 29 Apr 2026 22:44:33 GMT  
		Size: 16.8 MB (16837661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23b06a78b6e346324b4ccae7f54064e05cc8059b37b593caf9730186b81c6cd`  
		Last Modified: Wed, 29 Apr 2026 22:44:36 GMT  
		Size: 141.1 MB (141074590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b27e99b60546186d5398cb848761881034ad4a2495edd58778348608ab13b34`  
		Last Modified: Wed, 29 Apr 2026 22:44:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5cbe1f675378862d1c920e9f972f54caa6e00e0ef8bf232fd844c01fa839ac`  
		Last Modified: Wed, 29 Apr 2026 22:44:32 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc7440d1c78e8e245abcb55f8b0ac69bf4eab410eab6825a45964f314482cc1`  
		Last Modified: Wed, 29 Apr 2026 23:15:05 GMT  
		Size: 25.4 MB (25438635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57129d9295491aae9578205d7ae9b12ca8361363e6006dfb93b3c90d4a0f8d90`  
		Last Modified: Wed, 29 Apr 2026 23:15:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:a9ca5d420daf47226d20ce686082bf75f885cc76ffb0c9b285112dcd3782e7af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1225802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1358e483ee870d28a4930498e5027d2614c7962b875285bb54ef994e6b8c4ce5`

```dockerfile
```

-	Layers:
	-	`sha256:ba2e09f7f927de82816d700af106cc0d0a020c9d59fa02103cceda257e816c49`  
		Last Modified: Wed, 29 Apr 2026 23:15:04 GMT  
		Size: 1.2 MB (1212406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a39baa4e1e8dece42b105a5c83b2c0bb0f60185a5a26725f56bddf259b53088`  
		Last Modified: Wed, 29 Apr 2026 23:15:04 GMT  
		Size: 13.4 KB (13396 bytes)  
		MIME: application/vnd.in-toto+json
