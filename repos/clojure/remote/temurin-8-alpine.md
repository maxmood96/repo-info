## `clojure:temurin-8-alpine`

```console
$ docker pull clojure@sha256:5a41eeaee3199c9f72c55a6c90e2cab785df30de0127a634681c2f574794b9b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-8-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:64bf9dc797ddbdede09e6c436623713ab6b06d99e3c2b6f6e8c2399d233fe987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148486290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd76651b457e41734037dfb45d501032e9df4a55450ea59bccaca1855b2bc011`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='86071bc98901cae80c62745a64bb4486212985fe5b66b5aec36ce92e8a036a9d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apk add --no-cache curl bash make git && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01eb70355033ab6dd8da26dc89c8cc17ab414daab89c3e8db799a76d8db8191`  
		Last Modified: Thu, 24 Oct 2024 00:56:30 GMT  
		Size: 18.3 MB (18307357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67011bcdbe326e5d2228ed719b06657a451c130711dd51a2765340b845aead21`  
		Last Modified: Thu, 24 Oct 2024 00:56:32 GMT  
		Size: 101.5 MB (101542504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c003f0089d423ea3950139530879c979fe6b5566302c05bb0e275681d7374661`  
		Last Modified: Thu, 24 Oct 2024 00:56:30 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a546658f7d29ae1a954fbb289a243325032aed159592ee0bd3a2b217f5a660e`  
		Last Modified: Thu, 24 Oct 2024 00:56:30 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192039af12a034cd652c6451ae9f0abe962326943f85c87b56ae6719a884a576`  
		Last Modified: Thu, 24 Oct 2024 01:58:45 GMT  
		Size: 25.0 MB (25009535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b042f12857cd3176b710e9cf5e063fff3a2abc5f7260b920f795846ec7ea77fd`  
		Last Modified: Thu, 24 Oct 2024 01:58:44 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:17087fa5dff7db82644b4fafec96302b2fa8c09431296ec144d03dd55c0f71c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1259299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39add4a4b7bfe14a767be74b9d0ec73470c3e952d1b68645f254f8fe18221900`

```dockerfile
```

-	Layers:
	-	`sha256:1930a4310a76476f526ff57d1de80dc53a5da09ab6ce200346828a814a3eb822`  
		Last Modified: Thu, 24 Oct 2024 01:58:44 GMT  
		Size: 1.2 MB (1245887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d51116f7d114833be66a774c421ecf72ded7377cc89498402cdff3a93ccaeff8`  
		Last Modified: Thu, 24 Oct 2024 01:58:44 GMT  
		Size: 13.4 KB (13412 bytes)  
		MIME: application/vnd.in-toto+json
