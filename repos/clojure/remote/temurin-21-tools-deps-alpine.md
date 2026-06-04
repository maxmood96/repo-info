## `clojure:temurin-21-tools-deps-alpine`

```console
$ docker pull clojure@sha256:03867e07345101c349fe1e1311de391d73c6b49ee7381f4eb196aede6e58624e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:351673c3d4691ef7e487a14a4a3497fc66e79d74804378ca8d4895a7e70f53de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.8 MB (205821011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a615089da1f9828872db726dab105622b51251de4055b6b6fd62bd5f2ff654`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 23:58:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:58:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:58:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:58:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 07 May 2026 23:58:34 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Thu, 07 May 2026 23:59:37 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='c8d63598d1dc0a656033515ed258bd6db37506a05407d9f65cd23b95c21027b5';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='38bfdcef1e4b45de2ec222047ac79c76bea75d4d7406a310e26cfa236763f05f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 07 May 2026 23:59:39 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 07 May 2026 23:59:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 07 May 2026 23:59:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 07 May 2026 23:59:39 GMT
CMD ["jshell"]
# Thu, 04 Jun 2026 17:46:17 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:46:17 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:46:19 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Thu, 04 Jun 2026 17:46:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:46:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:46:20 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:46:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b50ae58d435408a9b026fe52e1670bc1fa8333eabfe9bf8732808b503921e21`  
		Last Modified: Thu, 07 May 2026 23:58:58 GMT  
		Size: 21.3 MB (21336223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcaabbcdfa248e8282ff1b8185b085013c4acad8c1d745f6bc6c254ca2c91cb`  
		Last Modified: Thu, 07 May 2026 23:59:56 GMT  
		Size: 158.4 MB (158396777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b89d263afc40ec784ccb9f91009ff3a1331571314d0a8213a083c9035f3155`  
		Last Modified: Thu, 07 May 2026 23:59:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4011cd827d707fc4492dbd50182b9de9e9d695532577a6760b7fa8a6b093e0`  
		Last Modified: Thu, 07 May 2026 23:59:54 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d1d9883ce76a14ee685b969a66a98dd62fc35cfcda0bef51757e28d80bfd9d`  
		Last Modified: Thu, 04 Jun 2026 17:46:29 GMT  
		Size: 22.2 MB (22220365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980cc610f9c9a69a4fa98630608d857e8a441f645f699e7ce0d5e3b0bc5f9143`  
		Last Modified: Thu, 04 Jun 2026 17:46:28 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88ad30ec7a6deab97a4d40c07cc4e1023b1bbaab617d38c2c9e3a6bb7779e58`  
		Last Modified: Thu, 04 Jun 2026 17:46:29 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:477c156022830f3074bd0980ef82b26bf0cb76729f5422b3a133f17e820f3a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1321579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9c8e9cba892f05bc6c5c250e28b8181f0b34921e5ddedd79c934cfc78d256e`

```dockerfile
```

-	Layers:
	-	`sha256:14c2ef0ab9487485e5310c733beec40432ad94f6a003d5aebe7ef585cf081631`  
		Last Modified: Thu, 04 Jun 2026 17:46:29 GMT  
		Size: 1.3 MB (1306148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5f70ddcc2b2eeea5128219aadaed0d3c5ad630d1da354ed9a32d2dbbe242ecd`  
		Last Modified: Thu, 04 Jun 2026 17:46:28 GMT  
		Size: 15.4 KB (15431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-alpine` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1a1468410265db000cc07817f7f3627e5f8637683f76d3ae9c002a86c49d5154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.3 MB (204299230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13d2651547ea3adf2a96956d029eb7c3bbe4533abe2179a185f6605ca05aeb3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 23:58:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:58:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:58:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:58:58 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 07 May 2026 23:58:58 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Thu, 07 May 2026 23:59:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='c8d63598d1dc0a656033515ed258bd6db37506a05407d9f65cd23b95c21027b5';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='38bfdcef1e4b45de2ec222047ac79c76bea75d4d7406a310e26cfa236763f05f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 07 May 2026 23:59:07 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 07 May 2026 23:59:07 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 07 May 2026 23:59:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 07 May 2026 23:59:07 GMT
CMD ["jshell"]
# Thu, 04 Jun 2026 17:46:17 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:46:17 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:46:21 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Thu, 04 Jun 2026 17:46:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:46:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:46:21 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:46:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a9f60e46e53646ef0910131cad063b4c547e8b484db8a7f43c06e8c8d8ee11`  
		Last Modified: Thu, 07 May 2026 23:59:24 GMT  
		Size: 21.3 MB (21321387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e7335552e625aa4d940009043b9ade8114a61f7445ad089dd0699e9c2cbd02`  
		Last Modified: Thu, 07 May 2026 23:59:27 GMT  
		Size: 156.4 MB (156402365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbe5c3db0c5dad3a2183ba5e385ef243c43b6847fa16af1db10346a47fb9e86`  
		Last Modified: Thu, 07 May 2026 23:59:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319e0f520245ecdfe248ad69c9025626cdb9a8a435ccd3b9a19da574bc33023`  
		Last Modified: Thu, 07 May 2026 23:59:23 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbaf73c1cc882685c72f2881b6bd403e7540e2152903ddfe082f7f28eaeb89c`  
		Last Modified: Thu, 04 Jun 2026 17:46:30 GMT  
		Size: 22.4 MB (22372149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bce6ba0a112f7a26d2093dc9cf60dcfc5638f9e0005021ff739b6cc83d8c04c`  
		Last Modified: Thu, 04 Jun 2026 17:46:30 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be206871310a91b5e840d8864896adde98a9999bb0e49b797eeb235ac015a65`  
		Last Modified: Thu, 04 Jun 2026 17:46:30 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:a83a51a304fc7466c72f659b817639301ed8ed3479500a6b27f2567881a528b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 MB (1471022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76065c14574782467a371a31f4d613a46cbc5c34d9ccfba4829673a7534102c8`

```dockerfile
```

-	Layers:
	-	`sha256:f99909359f01836002fc3981ca5c4262b5fd2c1468c275fec141d4e82b797893`  
		Last Modified: Thu, 04 Jun 2026 17:46:30 GMT  
		Size: 1.5 MB (1455500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e05084b28e4c68c4cae6b579f240deed233dfedb2b174443688f598539d4c3f`  
		Last Modified: Thu, 04 Jun 2026 17:46:30 GMT  
		Size: 15.5 KB (15522 bytes)  
		MIME: application/vnd.in-toto+json
