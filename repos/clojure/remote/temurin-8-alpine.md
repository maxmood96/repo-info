## `clojure:temurin-8-alpine`

```console
$ docker pull clojure@sha256:33263aedc790d9d8de1359b68f0b0acde0a4dbe3989b6bad46af656a03d85199
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-8-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:129ceb5415e1c0258537bcd92ddd3ca1577df0f90c1e90d13886b835e252714e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98193064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1a510e4b0bbb4a35e662329f28a9110439157fd546953caae62c439d5405ad`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='21e28ad4faf34a2d353252ea363d57afe8d72f9d55f66a54e4e99fd1acb7786b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f203d7f2ad91296c29189d9e5c0619b490cb71fe963cad10b53ec84f88ca971d`  
		Last Modified: Mon, 04 Aug 2025 19:10:43 GMT  
		Size: 16.3 MB (16280141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b884ab8379b7e3f3639c2a35bac4787823a7d7bbcb15fec9531a4e72f8043f69`  
		Last Modified: Mon, 04 Aug 2025 19:10:52 GMT  
		Size: 52.6 MB (52635396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d301459c24bef03fac78826eaca6eef9060db4208be33da132df14690b45d88`  
		Last Modified: Mon, 04 Aug 2025 19:10:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa4fd338b932d98deda035704b29a8991d4ce5a7b04a7e3eaac2fe5e23925f1`  
		Last Modified: Mon, 04 Aug 2025 19:10:41 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ee71fc75b470d786b70296abe341a6eaba67e20957c40e4926fb53d104c882`  
		Last Modified: Tue, 26 Aug 2025 17:27:17 GMT  
		Size: 25.5 MB (25474757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2c5c1fcfae8b314f0af5219258d45dfa0844ddf6c500d13a652ef723d0dd9e`  
		Last Modified: Tue, 26 Aug 2025 17:27:14 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:9ba2018da89d1ee69991c0822f66c5cc7b17156d3df48cfb738835c3d1217973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1311308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e428a19a276f589122fbfa272cd6568cddfbd75ff09c2b7a0d02a02a290abf1`

```dockerfile
```

-	Layers:
	-	`sha256:eed3b5a272d100b0ebb88ce0835ab784e68ba6d2d0634786e92458eb642473ac`  
		Last Modified: Tue, 26 Aug 2025 18:44:44 GMT  
		Size: 1.3 MB (1297885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80507226388ab43560b84ef55ea5a99f03dff6fcb8c5d9e444597a48aa71cc77`  
		Last Modified: Tue, 26 Aug 2025 18:44:45 GMT  
		Size: 13.4 KB (13423 bytes)  
		MIME: application/vnd.in-toto+json
