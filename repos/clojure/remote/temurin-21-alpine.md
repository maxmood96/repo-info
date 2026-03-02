## `clojure:temurin-21-alpine`

```console
$ docker pull clojure@sha256:b052bfa61463b7242c940680e69a4a931b69a167278b4ccb87a277dbdf0a0830
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:367129cfa8b1dc3062c1e5f91a309bb993c87bf4ef4a58d52064d299deb5af4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.7 MB (208660045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4066bb0513b74ee57fdca1547468343fbd69061526983f139f78b2a49044afa1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:19:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:19:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:19:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:19:13 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:19:13 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:19:19 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='19eba6c3877612157ef1f46deb92745b4567cfcd64b79f15449c68cd2b7501e3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='8eb39f442c3c603e414af43844b419a9b5d4f3fe221181f323aa4eec1bd20cf8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:19:20 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:19:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:19:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:19:20 GMT
CMD ["jshell"]
# Mon, 02 Mar 2026 19:47:03 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:47:03 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:47:06 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Mon, 02 Mar 2026 19:47:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:47:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:47:06 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:47:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf27b2f1dcc34bb3592032d2fca01d720abfd1e6baa1293e287a9ccab686e2c`  
		Last Modified: Thu, 05 Feb 2026 22:19:36 GMT  
		Size: 21.3 MB (21315086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52562347e5095f91dcef07e31744d38da2218e3d68ed36686ee889ef31ae2406`  
		Last Modified: Thu, 05 Feb 2026 22:19:39 GMT  
		Size: 158.1 MB (158118844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0b3aa0fc9566eb09be60af94e6aa6908c7e5e316b531ec5a22f49ee8685b66`  
		Last Modified: Thu, 05 Feb 2026 22:19:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b736977b63e2d08f494efff566b76b53223018ba70ef3f070289f1f0830e61`  
		Last Modified: Thu, 05 Feb 2026 22:19:35 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f5b497e7f3cfcfc818329b9f7bf79209f59f02e253d3357087af9abb1328a4`  
		Last Modified: Mon, 02 Mar 2026 19:47:15 GMT  
		Size: 25.4 MB (25360835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed7910c5ef8aeea4800ce08f34fe4d1d67ce311cc4b65f6832079c8a3d1bee2`  
		Last Modified: Mon, 02 Mar 2026 19:47:15 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b69e0b18f8c6275126db22e7b668fe771822fe01078992c0605a012470ea50e`  
		Last Modified: Mon, 02 Mar 2026 19:47:15 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:f0d2352bd64679aa90c19847a68a0bcc7fdb57113079a9fed70ee8e68b82533b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1327336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd22bd4ade643fedc3a4763f93370b6cd49f3be6b145506b954aa890f6cd89a`

```dockerfile
```

-	Layers:
	-	`sha256:d90556d1d0c4a4c026002f5a53b017e6f926b39fe1114be1c65785d0475b600e`  
		Last Modified: Mon, 02 Mar 2026 19:47:15 GMT  
		Size: 1.3 MB (1311905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2246632b049ac6309f5634835065b20b04ed5af50443b6d1e23f76430eb9c277`  
		Last Modified: Mon, 02 Mar 2026 19:47:14 GMT  
		Size: 15.4 KB (15431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-alpine` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:151cf2f4913c1304d1ac1ed869cd66d62aa4af606765bf971f01e69de512654d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207154201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ffc33d37dabce205266724e7da649586321c54246099c2fe896c9d75709d99e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:18:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:18:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:18:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:18:10 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:18:10 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:18:17 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='19eba6c3877612157ef1f46deb92745b4567cfcd64b79f15449c68cd2b7501e3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='8eb39f442c3c603e414af43844b419a9b5d4f3fe221181f323aa4eec1bd20cf8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:18:18 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:18:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:18:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:18:18 GMT
CMD ["jshell"]
# Mon, 02 Mar 2026 19:47:12 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:47:12 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:47:16 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Mon, 02 Mar 2026 19:47:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:47:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:47:16 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:47:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5089fa766c3c57eb5cdb3a5598c7f03110834ceee51d81992317c110371aff`  
		Last Modified: Thu, 05 Feb 2026 22:18:35 GMT  
		Size: 21.3 MB (21312383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17a1043f9baa0dcfa204d652bd299bd7e2ea6bf633efb9cd52c3f9f54976b7c`  
		Last Modified: Thu, 05 Feb 2026 22:18:38 GMT  
		Size: 156.1 MB (156130023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b7508607faa8f1e571f0bf716125a563c17b8e3883efba109aff61801ae738`  
		Last Modified: Thu, 05 Feb 2026 22:18:34 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f522a964bdc39f18b044b5e8f2817027173df17e2d19e26e356d7ef7c4afa85c`  
		Last Modified: Thu, 05 Feb 2026 22:18:34 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8da6022d1c3f50a0833339678b6168e23d25b3b69c9f7d753e403535138d72`  
		Last Modified: Mon, 02 Mar 2026 19:47:26 GMT  
		Size: 25.5 MB (25511239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2b5cedfe82078cdd9b38ee09dbd03ece8ab9eabc7ec6c08180e1ca7d9e8a04`  
		Last Modified: Mon, 02 Mar 2026 19:47:25 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db92b02c3d407f7d7d21f1ab130ea4784df1f7417fd5f55d5521f1c01890a374`  
		Last Modified: Mon, 02 Mar 2026 19:47:25 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:b5aee0a240871b6c9f1fc486023785b2a94c151178c41215033db72991a54e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 MB (1476780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:497dd41124d71707332df7bc4462d7e2218c994ceca4e984f0cc50e882c0a674`

```dockerfile
```

-	Layers:
	-	`sha256:91b1e704fe0f46e382ddce23b16cbf7f2b08917574b0c0c482cf713ad9d1cc08`  
		Last Modified: Mon, 02 Mar 2026 19:47:25 GMT  
		Size: 1.5 MB (1461257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69f1d3bcfebc42c51e4f2cfd5ca18d3b87b72251480d2065141623a80a88c0c0`  
		Last Modified: Mon, 02 Mar 2026 19:47:25 GMT  
		Size: 15.5 KB (15523 bytes)  
		MIME: application/vnd.in-toto+json
