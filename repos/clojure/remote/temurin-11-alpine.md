## `clojure:temurin-11-alpine`

```console
$ docker pull clojure@sha256:4229cd1ebd3df83dd6e285f3d2a6eda6c68b724684b19a0e4a04bfe65c27d6ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-11-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:f476627d29ee1aac1cac367b51b2c3182a733e4b8b8bce1acbb87cfe7e8a1c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.7 MB (185721021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8063cf97af7d069c169caecdb1e8f7d5a9d3f3c279e32eac1524fd16f2e42c48`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["/bin/sh"]
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 06 Jan 2025 23:07:46 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Mon, 06 Jan 2025 23:07:46 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='0a431310ccccc36c85b1274b5d31e368fdc8cf62cb7c2ed98d7b59eb5a13dc82';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 06 Jan 2025 23:07:46 GMT
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173d2d9b0a8b46032d314316667cd35f83981b340801b2eee2e4b2f5a9e1551a`  
		Last Modified: Wed, 22 Jan 2025 18:27:50 GMT  
		Size: 16.1 MB (16135215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57e5d440f7c1441b7d1825ea8f76a92995b27246ce624f8a62a09b758d92aee`  
		Last Modified: Wed, 22 Jan 2025 18:27:54 GMT  
		Size: 140.8 MB (140775205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2a28f11eac8e07ee789aec0651a007ebf7347f6b67af05c483b2a842c93310`  
		Last Modified: Wed, 22 Jan 2025 18:27:48 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eec7655b90e61e589217af43d5e02f51e095291b9cedf34c5739d3c5bac5f9`  
		Last Modified: Wed, 22 Jan 2025 18:27:49 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8774de48f43d9268bbab0164db7be286ecb6cf5f32b0be8d7bb92a72db90387b`  
		Last Modified: Wed, 22 Jan 2025 19:41:50 GMT  
		Size: 25.2 MB (25165825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf78864e6b2134df712aa929c48c4d1700736fbc66f8d2e7adb3ba723f07bb1`  
		Last Modified: Wed, 22 Jan 2025 19:41:50 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:6a8ebb99538887db8eb005aebd03a5fdacef110310a0d53c8a7771939c9514a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df1d8592147d53939c9a665fcf13bdde00676ecc590fbf934384ca5a9f732eae`

```dockerfile
```

-	Layers:
	-	`sha256:ecb63e64571306fb533ab82da57625d32201a66a566539027b2b0e49f70c5f54`  
		Last Modified: Wed, 22 Jan 2025 19:41:50 GMT  
		Size: 1.2 MB (1151179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:061123d5bf290e2c6f96fcad418a52188b4bec39d7c33c868ce033b55e4d0cee`  
		Last Modified: Wed, 22 Jan 2025 19:41:50 GMT  
		Size: 13.4 KB (13423 bytes)  
		MIME: application/vnd.in-toto+json
