## `clojure:temurin-21-tools-deps-alpine`

```console
$ docker pull clojure@sha256:05d521edbc230c6fda570f0b3176fb5f1a585d6c0a266fdbceb34034ff6b3f91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:ab1f09555ee24938c70bf1318e47e25cf01bd7c32e2ea2a45541d39767827d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.8 MB (205755174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd05218d0ba66faf7a3db517a808b6e1de120665c4cb4c73a43a851ccd2fd780`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:57:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:57:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:57:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:57:09 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:57:09 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Mon, 22 Jun 2026 19:57:17 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='c8d63598d1dc0a656033515ed258bd6db37506a05407d9f65cd23b95c21027b5';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='38bfdcef1e4b45de2ec222047ac79c76bea75d4d7406a310e26cfa236763f05f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 22 Jun 2026 19:57:18 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:57:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:57:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 19:57:18 GMT
CMD ["jshell"]
# Mon, 22 Jun 2026 20:24:54 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Mon, 22 Jun 2026 20:24:54 GMT
WORKDIR /tmp
# Mon, 22 Jun 2026 20:24:57 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Mon, 22 Jun 2026 20:24:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Jun 2026 20:24:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Jun 2026 20:24:57 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Jun 2026 20:24:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42b27ff362c29d4c86173d5eb45dc9fc28c27d52c5791cb63a9113e6f0e3646`  
		Last Modified: Mon, 22 Jun 2026 19:57:35 GMT  
		Size: 21.3 MB (21290130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c90809b4c96d37014d44d53b2f534fcdc3a9b2baa628af103045b46795a7189`  
		Last Modified: Mon, 22 Jun 2026 19:57:38 GMT  
		Size: 158.4 MB (158396795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7ee5d98789e02e3500e8e207c5963d76ea5e48dbe5f519229aeb3847e2bc62`  
		Last Modified: Mon, 22 Jun 2026 19:57:33 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68dfaba6ad42ab866380109a6c2636053416cb8f6e06672fa092a97451fd747`  
		Last Modified: Mon, 22 Jun 2026 19:57:34 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8ffa1d9fdc408634fa73e7a80e216bab7a868f29386e63a630c986c1b0351e`  
		Last Modified: Mon, 22 Jun 2026 20:25:06 GMT  
		Size: 22.2 MB (22220368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca22de24947b3e5b542474071c83136a30313d3c12059678dcf925633b5666ec`  
		Last Modified: Mon, 22 Jun 2026 20:25:05 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e5c72800ccd8ccb64ebd8ab8d0d5d385fe335da74f222fbf903b9f880d9671`  
		Last Modified: Mon, 22 Jun 2026 20:25:06 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:617aeddfd818345a51d623265f64a8b88191227ea9da0d02353d1a51417392ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1304687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c39917dd56af28bc6a638750b2aa2fb37617c3856aa64506af7cc7902800677`

```dockerfile
```

-	Layers:
	-	`sha256:9902e64410310f074b4be10f2e3ba5e97da6ed6f4c19698d6e9626533749f437`  
		Last Modified: Mon, 22 Jun 2026 20:25:06 GMT  
		Size: 1.3 MB (1289256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de261ce4c5205f370f3afbbb2e7a797efb2de9937bc052e24b015a1aa9313789`  
		Last Modified: Mon, 22 Jun 2026 20:25:05 GMT  
		Size: 15.4 KB (15431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-alpine` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f1e314c67b1e344df29851ea0ab4fc4f4783a034559885228cf74c3e5e5e91b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204239942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2af150ddb4c1293a395d927c7ee6c37d6e5493b6e17f653a170dceece2e8e0d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:57:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:57:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:57:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:57:56 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:57:56 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Mon, 22 Jun 2026 19:58:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='c8d63598d1dc0a656033515ed258bd6db37506a05407d9f65cd23b95c21027b5';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='38bfdcef1e4b45de2ec222047ac79c76bea75d4d7406a310e26cfa236763f05f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 22 Jun 2026 19:58:07 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:58:07 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:58:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 19:58:07 GMT
CMD ["jshell"]
# Mon, 22 Jun 2026 20:58:42 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Mon, 22 Jun 2026 20:58:42 GMT
WORKDIR /tmp
# Mon, 22 Jun 2026 20:58:46 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Mon, 22 Jun 2026 20:58:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Jun 2026 20:58:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Jun 2026 20:58:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Jun 2026 20:58:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4528e8515ecbe5a4cead182002e4915088694f327a2a6d59eb4d8879cc01934`  
		Last Modified: Mon, 22 Jun 2026 19:58:24 GMT  
		Size: 21.3 MB (21281739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9ad1632bf4f15fb4547045f89810b89d4e2c12f4cc1e1cb1b38c68666c29d7`  
		Last Modified: Mon, 22 Jun 2026 19:58:27 GMT  
		Size: 156.4 MB (156402333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9d07f7518fbbb05f6c65a2c0b79b89a2e5fde15459a3d4e2f4f4ceaf1a7f70`  
		Last Modified: Mon, 22 Jun 2026 19:58:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab2a9682f8c999c8b4b42cc35b437b44dfbdf44d7726ea13daab581dd97384b`  
		Last Modified: Mon, 22 Jun 2026 19:58:23 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38cf9c9e6c5fc9a975c9e19d50fa42ebb4759487951dc87f0d5f83b0252e9f0`  
		Last Modified: Mon, 22 Jun 2026 20:58:54 GMT  
		Size: 22.4 MB (22370553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d856edc25125097cd22ad81ba3ba2b42ba215cca6fb465b3bdb304e0e17349`  
		Last Modified: Mon, 22 Jun 2026 20:58:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a665d73dde677a82c65cbb394aa3b8e2b7a4a733e10b727e983b24ad5975ee93`  
		Last Modified: Mon, 22 Jun 2026 20:58:54 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:cc238119a94f588811e3231ea80e67c3302fa9bbb2ec9336b9ea2e9a6dc0611d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 MB (1454132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d1797e3646a98ba42bbf4c0ddb9724e4b7f63ee6fa1be1c8f452f0ca0208fa`

```dockerfile
```

-	Layers:
	-	`sha256:4b13952055b9ac50c8f0068165d5fed77dd16805d53c05527155f1f5a9e50b90`  
		Last Modified: Mon, 22 Jun 2026 20:58:54 GMT  
		Size: 1.4 MB (1438608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdc933434ad359f23ed7d106b069e42f3b74fb9eb36e47ab4ea665e4d6b82c22`  
		Last Modified: Mon, 22 Jun 2026 20:58:54 GMT  
		Size: 15.5 KB (15524 bytes)  
		MIME: application/vnd.in-toto+json
