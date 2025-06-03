## `clojure:temurin-8-tools-deps-1.12.1.1543-alpine`

```console
$ docker pull clojure@sha256:26d4a337865c9fd98f134038f48cbbe7dcaf87d460cfb4c662040cde0d747448
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.1.1543-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:ae284089f3e8710fa1309bf706f3e929cf9aa2ace2d6a5b06be07aa651d1a3f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.7 MB (97713065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f4ff74308b7cf7d82935df62f24d19f85c0f4ea3c1660ece7d8f33abe0b303`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='be8abae7586c328ceb3252aefed9e51c29be91616968c0130b41e7e57c846f0f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7141be485741d41116a845b669643de63ccceb87c3be707c0a7eaa7f5ccf8f0`  
		Last Modified: Thu, 08 May 2025 17:18:28 GMT  
		Size: 16.2 MB (16176532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d22b184abfb23338db1ce2eec5f2b1c5299eec68ec533ba9f0c96eb50f94d86`  
		Last Modified: Thu, 08 May 2025 17:18:35 GMT  
		Size: 52.6 MB (52621858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3726fa4c4e4f7f6fac67f7e4a3b9f88a7697235d9144aea259a488250ea6a4`  
		Last Modified: Thu, 08 May 2025 17:18:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267111b8758c00ce54358fe646f25d46e043fc0ee6173035ede38ede1c1aaddb`  
		Last Modified: Thu, 08 May 2025 17:18:27 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5612ec4d9457ef03fd4539caa8b0d0105c15604211e60f0bd8c13eb0ad44a71b`  
		Last Modified: Tue, 03 Jun 2025 18:24:06 GMT  
		Size: 25.3 MB (25269350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1abfd56f66ccb3fab3c8ffecb31be3ee4c1a44d9b13a17159f8f09c8684f28b`  
		Last Modified: Tue, 03 Jun 2025 18:23:54 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1543-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:e893268333c44c2a4bb75e7bfb45b91aa66aa5c9c1f95a48d32e67bcf1948c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1314324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324a3151a7a145f9c4f6251bc81c6b32f74166422402244f9b5209d98b1ae87c`

```dockerfile
```

-	Layers:
	-	`sha256:2f222f914005678e905d91d644a36b74ae24c204070fff40265c6bcbd1bfb5a4`  
		Last Modified: Tue, 03 Jun 2025 21:44:13 GMT  
		Size: 1.3 MB (1300901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69b7facedefeb82a30bc9dd7fe22d2c19d35926e73906c0c59cfd36601f8d63c`  
		Last Modified: Tue, 03 Jun 2025 21:44:14 GMT  
		Size: 13.4 KB (13423 bytes)  
		MIME: application/vnd.in-toto+json
