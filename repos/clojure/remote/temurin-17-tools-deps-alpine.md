## `clojure:temurin-17-tools-deps-alpine`

```console
$ docker pull clojure@sha256:6e5f2f29bab522ab74ddf0a4464892a34bb7b688055479d5161b44c6f37769df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-17-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:a030abc4283e3c7ba4f02a5e4ac3b9a6b9393e3f8a2d9233bf4339ed045d4f3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.7 MB (185697357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2393d68ac3fc376f0bb8cf6ccd3ee20888f75912104484e2d18279396db1f016`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:52:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 27 Jan 2024 00:52:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 27 Jan 2024 00:52:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 27 Jan 2024 00:54:20 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/*
# Sat, 27 Jan 2024 00:54:20 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Sat, 27 Jan 2024 00:54:29 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ce4085548f73ec97fa870de3f7da87634b4cbbf9753600365e2e0b255585e7e1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Sat, 27 Jan 2024 00:54:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Sat, 27 Jan 2024 00:54:32 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Sat, 27 Jan 2024 00:54:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 27 Jan 2024 00:54:32 GMT
CMD ["jshell"]
# Sat, 27 Jan 2024 09:53:15 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Sat, 27 Jan 2024 09:53:15 GMT
WORKDIR /tmp
# Sat, 27 Jan 2024 09:53:19 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Sat, 27 Jan 2024 09:53:20 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 27 Jan 2024 09:53:20 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Sat, 27 Jan 2024 09:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 27 Jan 2024 09:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59648cfc069f04a8d0eece9cae80e25155888dc9b5de722b58603efafaa0d78b`  
		Last Modified: Sat, 27 Jan 2024 00:58:00 GMT  
		Size: 13.1 MB (13138018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d0e7d6722862146a131ded4549c3456466f939a62c3b10dc6c0cde4388f142`  
		Last Modified: Sat, 27 Jan 2024 00:58:09 GMT  
		Size: 144.1 MB (144142367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745a045d72287cc9b24556bae295db743545eb7a54481f9d6bbb7096a5178dde`  
		Last Modified: Sat, 27 Jan 2024 00:57:58 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20480f891b31ebf94a42342dec8efad6db7087933f7117262a9ac7cca80f68b3`  
		Last Modified: Sat, 27 Jan 2024 00:57:58 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b3d47da4063d0a1752cc87d76c347fa2ae7f688fe0e17de67e13e8dd22411c`  
		Last Modified: Sat, 27 Jan 2024 09:57:28 GMT  
		Size: 25.0 MB (25006322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cca6a2acc87ebe00fde13b33c8d695f64b46dfd36302cede7205edf4e717ef3`  
		Last Modified: Sat, 27 Jan 2024 09:57:27 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d40ff37b5b3368cc7cb2e7325ae905c175f58175f1613534871ec55be28170`  
		Last Modified: Sat, 27 Jan 2024 09:57:27 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
