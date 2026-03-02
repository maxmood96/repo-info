## `clojure:temurin-17-tools-deps-1.12.4.1607-alpine`

```console
$ docker pull clojure@sha256:32b164cb49c19d9e3fe71e80d834b1e9e5249a4339fbfb8bc66d9ea58faeecbb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.4.1607-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:c55a8153e7eb9e981de9bde7bfa4fd1441fef88c788413759ac91de202a278cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195303584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d149026f1b003e315120f57b6d6c527ea498e9fc31040efdb412ac822500d774`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:17:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:17:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:17:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:17:14 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:17:14 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Thu, 05 Feb 2026 22:17:20 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='3246fb1834d21c22ed717db9f8ba3f07e0f562bbeeebdc44a7499d5eb6df47bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:17:21 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:17:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:17:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:17:21 GMT
CMD ["jshell"]
# Mon, 02 Mar 2026 19:46:27 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:46:27 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:30 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Mon, 02 Mar 2026 19:46:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:46:30 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:46:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a547da4fe1538a9de970334bfb206793ffde2bd214a847994365c731033eeff`  
		Last Modified: Thu, 05 Feb 2026 22:17:35 GMT  
		Size: 21.3 MB (21315075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c540078c28f902907cb8db0fe7898ee78430d17c840a361da6ef7827dba16f`  
		Last Modified: Thu, 05 Feb 2026 22:17:38 GMT  
		Size: 144.8 MB (144762403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd2436f004e3c25b262ab1b7a9ff98f09c80c2bb3359c7e6fc8b4c4364bb969`  
		Last Modified: Thu, 05 Feb 2026 22:17:34 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946c51efe0fd37b3c13616ceba0f5a7fcc6c82f60c8679d6cf5e8fddd8620fc9`  
		Last Modified: Thu, 05 Feb 2026 22:17:34 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9082b555620b47c27dc2588680723caa11f51f0e84c477eb7a6da30d8478288`  
		Last Modified: Mon, 02 Mar 2026 19:46:40 GMT  
		Size: 25.4 MB (25360825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bff034d50aa0250a15a705b49559a5239fc1721fc9baa74a84e8f36acb0d3d`  
		Last Modified: Mon, 02 Mar 2026 19:46:39 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfe2e2f12d39291f2139e72d21d26a23d51aff2ff3fed745012c2e4844fb5c0`  
		Last Modified: Mon, 02 Mar 2026 19:46:39 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1607-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:5402b64c056a71ca9da835f3e927525a090595966d6d4b42d2a881e35da420d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c67d902f7ebb911606a9a26eda158116d6c8852fbd3340cc3bdbfe76d73601b`

```dockerfile
```

-	Layers:
	-	`sha256:bcd9374a82fd593526f9818e8c6b405221d65c225dc3a2cab6472ae4b575a15d`  
		Last Modified: Mon, 02 Mar 2026 19:46:39 GMT  
		Size: 1.3 MB (1310053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1cffcd2d093f69c89b85c4860c8a1a4b391a18410bcac762c643213da646b67`  
		Last Modified: Mon, 02 Mar 2026 19:46:39 GMT  
		Size: 15.4 KB (15431 bytes)  
		MIME: application/vnd.in-toto+json
