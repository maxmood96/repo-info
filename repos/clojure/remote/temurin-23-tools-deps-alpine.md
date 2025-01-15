## `clojure:temurin-23-tools-deps-alpine`

```console
$ docker pull clojure@sha256:2aaae55920d607aaae477eab90680d29884fbb3ff0292312d468c4408f709338
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:6a9f685e3cec342d5c80a33e27548eb2ff1fd54eddb38dc35613ea3438a898f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214458519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1c99532e52aa8f8be29efaf4b3e514bd5675ed9191161ef95790ac3b002260`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='ebdd6602d27bd7535bf06f21e8a0c3d563be7b790a90bef00cb6ac4123c66f86';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='4c37a9e885c4e099b049c3ba9baa073de1525e28cd5ffca016c5c5bd7ed385a6';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apk add --no-cache curl bash make git && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8882735e21c791a47850ff1f22712790c562600ba506e9e98739dda3287d50cc`  
		Last Modified: Wed, 08 Jan 2025 18:14:49 GMT  
		Size: 20.7 MB (20665966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce94b72b036e1d425a31307aa924ed0b24b4ad1974b1f5bc3ed24d68cdfaca06`  
		Last Modified: Wed, 08 Jan 2025 18:14:50 GMT  
		Size: 165.5 MB (165513292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e2c87a019600d2f26696ca20dd7ed14ec90d8f55f9fde0cef33d73b9d9a652`  
		Last Modified: Wed, 08 Jan 2025 18:14:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bc72d1ec48be88672f2eb506b9b0257785e4724f39526b36c3d4e94bd24571`  
		Last Modified: Tue, 14 Jan 2025 20:41:25 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91a857834db4ef70a24d272f016769202575d0b98f419f819acba20032f650c`  
		Last Modified: Wed, 08 Jan 2025 18:24:36 GMT  
		Size: 24.6 MB (24649538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b11b0bb95f93105a3b4b77767d8089ac94cd2930c4c586304b19dd8516a34ff`  
		Last Modified: Wed, 08 Jan 2025 18:24:35 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479647e76f0872ca7981eda3c60ec6ee7a526f106815622f383a5e8ffb430217`  
		Last Modified: Wed, 08 Jan 2025 18:24:35 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:af1c358336d22d3ee071f554ac5c38458c6d89af6a50625b44ea87e150a59b80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1238032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801a20853d5783f706363d7e32c62822a85b208a574982711c70b7847f9da080`

```dockerfile
```

-	Layers:
	-	`sha256:effc05c02412e689e3cab9c51b11aa22db06cf3efb53190af854ef96332cb0ee`  
		Last Modified: Wed, 08 Jan 2025 18:24:35 GMT  
		Size: 1.2 MB (1222573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:366fda64627d0e1585395f29757bc90cd333ea5f1454992ef6210e72682c4b33`  
		Last Modified: Wed, 08 Jan 2025 18:24:35 GMT  
		Size: 15.5 KB (15459 bytes)  
		MIME: application/vnd.in-toto+json
