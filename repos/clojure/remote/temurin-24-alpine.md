## `clojure:temurin-24-alpine`

```console
$ docker pull clojure@sha256:d76f70274ddd217dad38316350225a95fd7840b7cd2dc1dd46b654b5434ffda6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-24-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:142e1b41c12c096525eb18cfd89953a4f5bd6f1be83c73afbed80b2b327a2653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139455939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ffdb0f76937c1c1922f5a3ba76e153ac02ba2d16300497d4f165bf3020352c4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='4a673456aa6e726b86108a095a21868b7ebcdde050a92b3073d50105ff92f07f';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_aarch64_alpine-linux_hotspot_24_36.tar.gz';          ;;        x86_64)          ESUM='a642608f0da78344ee6812fb1490b8bc1d7ad5a18064c70994d6f330568c51cb';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_alpine-linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["jshell"]
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apk add --no-cache curl bash make git && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da9e4e6bbb3d8fe7ba4feb76b9f85cc591b594ed37c725031140c217b982045`  
		Last Modified: Tue, 25 Mar 2025 21:57:50 GMT  
		Size: 21.0 MB (20950921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09b1f076e8ade81f12374738d4768afffa7e33753b8e5edec2e7165fd328397`  
		Last Modified: Tue, 25 Mar 2025 21:57:52 GMT  
		Size: 90.1 MB (90074010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fee87929fdd34f08d09385a3965e44dcfaa3724ce5f1a2515708890b07049e`  
		Last Modified: Tue, 25 Mar 2025 21:57:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d237c308bf2aec9726a2aad84026d710a041c7de9ee1603fe9726cd1491bed2`  
		Last Modified: Tue, 25 Mar 2025 21:57:49 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d957f5d990c9413aa59bdb350b588b2ca49c736896e23dc7abfbe08dd9573195`  
		Last Modified: Thu, 27 Mar 2025 17:53:16 GMT  
		Size: 24.8 MB (24785294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0795c242ac7a6f82ba6e97bf12d90b1a44877113af93c1adc0f5affaa87e3044`  
		Last Modified: Thu, 27 Mar 2025 17:53:15 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc95c85672d4a5d5b3b6963ec9cab7e0400840491165ac2b8fc877c01a69f96d`  
		Last Modified: Thu, 27 Mar 2025 17:53:15 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:f824c58bcd99d160621a376264bc9bb2c33e5a1f0eda05b9f1dac7c565ae0956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1216215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3687aad7fc034f5d8f670d683c19245c559770ce77b0991a1d9e0c263710ff`

```dockerfile
```

-	Layers:
	-	`sha256:092c772188cdd5fc54344bde76324e961088a9f8c2e0b87e10fb462d930f6555`  
		Last Modified: Thu, 27 Mar 2025 17:53:15 GMT  
		Size: 1.2 MB (1200765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8944eff06ff414500020d68ceea1f1878607711348aacc2d281aeb337bc6bb58`  
		Last Modified: Thu, 27 Mar 2025 17:53:15 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json
