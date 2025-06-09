## `clojure:temurin-24-tools-deps-1.12.1.1550-alpine`

```console
$ docker pull clojure@sha256:1a7d978872a54d2737aebb77ddcc731cbf220ba8eea01e733ba343602bfa0a7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.1.1550-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:5dc84a69a4f6a5c787e61e9d5d8ec9636a98e1ce7630c08a357740af002fa95e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139569683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1fec18a9be8946110756c3127f66fc55a023a652f06af4894883d11b433e06`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='97b14f9c2f7e7ba4d4a958bba6835a23353b5fd858725031fc42af4f40a5a4ad';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_aarch64_alpine-linux_hotspot_24.0.1_9.tar.gz';          ;;        x86_64)          ESUM='74627af4084a9eb65cc5bad3bb5723b89f1ffb5eaec9afbd696ec5bf684ed79a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_alpine-linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89fa3206805da3f39f3d33e513000c7fe732767469d033fea6cf0c47b9c3a6b`  
		Last Modified: Thu, 08 May 2025 17:07:53 GMT  
		Size: 21.0 MB (20951357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e10588850906e608ba2d19a979d66a3c3231deab14453e4c96f0f145218c2f`  
		Last Modified: Thu, 08 May 2025 17:07:58 GMT  
		Size: 90.1 MB (90081657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f971aa3d7e1c0f663d0194507c129d747c8c22bd5a54388471f73fd984c2bb`  
		Last Modified: Thu, 08 May 2025 17:07:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883498cd171d42da42c278599e117d11db9885fbea522558e72b6f1740e5567d`  
		Last Modified: Thu, 08 May 2025 17:07:52 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e5868d98b9e5a81c1bcfc81a8f0de9097d94753d04de15fcc46cf8806945b9`  
		Last Modified: Mon, 09 Jun 2025 17:18:14 GMT  
		Size: 24.9 MB (24890959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee691b24a84ed9ef26ce82f8b418a229907be740a8e75fc0b4398978e4abb32e`  
		Last Modified: Mon, 09 Jun 2025 17:17:50 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdb1188bdb1328c01640cfd45b24c375bc9cdea3a4920888a3299ccbc30edcb`  
		Last Modified: Mon, 09 Jun 2025 17:17:51 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:6889fe6444869194d331f29b9379046ac666b8e15e4f41d8ca47418b5ce0106d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1264377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c50365cdd0a3491688aa6b62b104912b5770bd1b2e95aa887177e67bb149ca3`

```dockerfile
```

-	Layers:
	-	`sha256:b3cdae6ca6a6e906e15e09ea2391f8d4a4b7468e1892cc82005e95a1eaff2d40`  
		Last Modified: Mon, 09 Jun 2025 18:40:45 GMT  
		Size: 1.2 MB (1248909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0596f31108ee0023e4a350dfaec5dfded4a7478c2b59879f117035eb2cea9ac5`  
		Last Modified: Mon, 09 Jun 2025 18:40:46 GMT  
		Size: 15.5 KB (15468 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-alpine` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6d10dab6a1e002a16c365495b38fde86004d2a2ba38cbca3d28b322544796700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139081360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89ae741dcadb3de3d50d243a6022743e6f7d75cf5ce75c9d0a5858cb39005410`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='97b14f9c2f7e7ba4d4a958bba6835a23353b5fd858725031fc42af4f40a5a4ad';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_aarch64_alpine-linux_hotspot_24.0.1_9.tar.gz';          ;;        x86_64)          ESUM='74627af4084a9eb65cc5bad3bb5723b89f1ffb5eaec9afbd696ec5bf684ed79a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_alpine-linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4dc4c8e3ac1404ce7eb282c94493325536d142e577ef37ec27bcf3edd09f4b`  
		Last Modified: Thu, 08 May 2025 17:06:52 GMT  
		Size: 21.0 MB (21006028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b587585b41566074b337300ac392de9b4d45b1d80418a53a9682dc5dc5cfa792`  
		Last Modified: Thu, 08 May 2025 17:06:58 GMT  
		Size: 89.1 MB (89067358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de1aae9586f9d6276f2cc85c43560b6c4303b29fadb32b3998b60ca44ac6f4e`  
		Last Modified: Thu, 08 May 2025 17:06:50 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eef6807030255660c0fed6484392bae8ed8ca964c95eaf49f68b4b768b6af50`  
		Last Modified: Thu, 08 May 2025 17:06:51 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e2e5b1916001dd0ed182e8093f306c418454accf5ed9ecb418266009d18e79`  
		Last Modified: Mon, 09 Jun 2025 17:57:53 GMT  
		Size: 25.0 MB (25011476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fb77f0d8e757d0ab65efdbcf0d7d34fc3127c2b11942d8ff65105bb5aac010`  
		Last Modified: Mon, 09 Jun 2025 17:57:48 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89930c3ffb0c34b34bf485f30d57717b94adfe5006f9ec846d7ac1b877fed2e0`  
		Last Modified: Mon, 09 Jun 2025 17:57:47 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:61f720ac14b08279e961190c21eabf468fa9b9f9b583fee5fd11a4c09b377ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1414468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56191263b70614bc4ebf06ced1c36b9061bd37b42c79e3589433b61361a9e754`

```dockerfile
```

-	Layers:
	-	`sha256:1d9bbef78943e05c61ab7d30cfc605f22b4c750b15eba76cc3f7884840d2dc92`  
		Last Modified: Mon, 09 Jun 2025 18:40:50 GMT  
		Size: 1.4 MB (1398908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4085be57526c70edbc546e0cfc58df78785877544d132787db4cd75468caa31`  
		Last Modified: Mon, 09 Jun 2025 18:40:51 GMT  
		Size: 15.6 KB (15560 bytes)  
		MIME: application/vnd.in-toto+json
