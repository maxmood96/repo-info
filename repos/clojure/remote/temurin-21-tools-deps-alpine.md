## `clojure:temurin-21-tools-deps-alpine`

```console
$ docker pull clojure@sha256:ceced7a0ff85f292205a3087269bcfeeb41af209b773d60a979e74d2b5b2ce84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:b17dc265ba35b0baa05660b9f2b499275482ac61c85d27ec79d10fd7b00902dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.3 MB (200280267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031537f412c84d28fca42a870a7b02d6e6d56f2e3bdc73730cd6194748141a66`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0f68a9122054149861f6ce9d1b1c176bbe30dd76b36b74c916ba897c12e9d970';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|x86_64)          ESUM='8e861638bf6b08c6d5837de6dc929930550928ec5fcc81b9fa7e8296afd0f9c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apk add --no-cache curl bash make git && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fd38fd7cf5b8d60c92e1aa46a24527229fb51b451491d35a7028a8a1d0aba4`  
		Last Modified: Thu, 28 Mar 2024 02:08:23 GMT  
		Size: 13.1 MB (13142803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332bf309ecf2b86f336452cb3137f9b266c99d9a10612bd124e2f13e0dad9bb3`  
		Last Modified: Wed, 24 Apr 2024 19:16:14 GMT  
		Size: 158.7 MB (158716489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e377b89d6767f434b66aef2b55d4397fa1ca4ef205a16f2fc626005be867634`  
		Last Modified: Wed, 24 Apr 2024 19:16:01 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45705fa60e5881f3a69ceb008964dcca0e72d626655d99b6d92e4c0834c7131b`  
		Last Modified: Wed, 24 Apr 2024 19:16:01 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb1bddbae594ea3ca91d45795b39b38020758f703f43b8b57148674f4b1e404`  
		Last Modified: Wed, 29 May 2024 19:57:59 GMT  
		Size: 25.0 MB (25010276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4175328c975901a90b8ec8f943793faabbde347feae66dc21912379c05926501`  
		Last Modified: Wed, 29 May 2024 19:57:59 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4656cc40666d67aa5f2e3c253427ee29c4d09c62570e2b6b08a38d3b98d94f7f`  
		Last Modified: Wed, 29 May 2024 19:57:59 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:ffffac371e0ff67e09b3de7424aea310282f86d3d12f14fc75d21156b659eb82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1349693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0719b94f8f9b9d1a64e698278ed808c821c9ae6d0ed7b81d0c20e139391801f5`

```dockerfile
```

-	Layers:
	-	`sha256:c5ae9295ac3f0eff711b8c86445cc0165307f050b91f9a8c713c9c8d07059950`  
		Last Modified: Wed, 29 May 2024 19:57:59 GMT  
		Size: 1.3 MB (1334343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a4accf5a2877290ca4742e9a2e357ad67af4c4211fa1c2ea2ed289999d343c4`  
		Last Modified: Wed, 29 May 2024 19:57:59 GMT  
		Size: 15.3 KB (15350 bytes)  
		MIME: application/vnd.in-toto+json
