## `clojure:temurin-22-alpine`

```console
$ docker pull clojure@sha256:7a81ff661557ad54606b58429b7a607fffd20340e219e4d49df9e211d1d04d93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-22-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:2db9238b2c9f8400e0089a237ac43efd7ab960b4ac3691a607ba316ec7d4fcea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198498553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ee5f131fdab879258e03706562426328fa2b699a78facd2cd6dcb343475ca8`
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
ENV JAVA_VERSION=jdk-22.0.1+8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='86a7b47c9277f2fd063ec910616b3676d86553ab7d23aa3bd365e51a57be1dc5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_aarch64_alpine-linux_hotspot_22.0.1_8.tar.gz';          ;;        amd64|x86_64)          ESUM='d226e44b3513942db855df9a8737d848f64069848970d4cfd35ee3c38f2525c1';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_alpine-linux_hotspot_22.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:14c16e77c87132dd32f3d6a221cf59225fc030b9895a77d196cd77ff1ac25647`  
		Last Modified: Wed, 24 Apr 2024 19:18:13 GMT  
		Size: 156.9 MB (156934796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae397eb730e1b4d590698ce9937b2e515a07cc0649968abae9742be5bd6386`  
		Last Modified: Wed, 24 Apr 2024 19:18:00 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f95ebed3ed7edeb5b3c167bdfe852d99210fccc2416f5950c1210d610e4914`  
		Last Modified: Wed, 24 Apr 2024 19:18:00 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef231463975bbe24f791231af0f7263b007a83ca0385d340159157f068a52d73`  
		Last Modified: Wed, 29 May 2024 19:57:58 GMT  
		Size: 25.0 MB (25010256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbad18ea66f1549cb678dc17399553188f8361de67270e098eb6134c490152c1`  
		Last Modified: Wed, 29 May 2024 19:57:58 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077fc261c1eeadc6838856da472c1292af3b213fd3ecf044e8046d7261464bfb`  
		Last Modified: Wed, 29 May 2024 19:57:58 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:51c5624738a12829b3a502c2890afded90d6400e9c0e28fea9df373f296a3ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1349677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb2a06c5b4fd6d95a7621fe6bd8964eda68e1796f4b02b861bce71899a1420a`

```dockerfile
```

-	Layers:
	-	`sha256:cb39ecffe01a448728c3f3d2e3270a37df7bff6ae7c158456475c1987df26a5c`  
		Last Modified: Wed, 29 May 2024 19:57:57 GMT  
		Size: 1.3 MB (1334327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b29355e27473c1a5dbc3338f99490020e1e2647261e1a622d640157709509fa2`  
		Last Modified: Wed, 29 May 2024 19:57:57 GMT  
		Size: 15.3 KB (15350 bytes)  
		MIME: application/vnd.in-toto+json
