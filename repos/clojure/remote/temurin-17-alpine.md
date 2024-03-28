## `clojure:temurin-17-alpine`

```console
$ docker pull clojure@sha256:c716c44d327acaded4c9fa254d59d83be2849d5a796d66d06ab4d75bd1abb5cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-17-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:8b10bf15df8adfd551b80a57d2ec9515a4475d8dc1b12fa54f25780418e21832
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.7 MB (185705083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5af09f2de39f72479ed0b6f31097ac2e662b2e5f291c7a7dd05bbce02f5553d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2024 16:26:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 16:26:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 16:26:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ce4085548f73ec97fa870de3f7da87634b4cbbf9753600365e2e0b255585e7e1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jan 2024 16:26:40 GMT
CMD ["jshell"]
# Thu, 28 Mar 2024 03:11:39 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 28 Mar 2024 03:11:39 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 03:11:44 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Thu, 28 Mar 2024 03:11:44 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 28 Mar 2024 03:11:44 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 28 Mar 2024 03:11:44 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Mar 2024 03:11:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fd38fd7cf5b8d60c92e1aa46a24527229fb51b451491d35a7028a8a1d0aba4`  
		Last Modified: Thu, 28 Mar 2024 02:08:23 GMT  
		Size: 13.1 MB (13142803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4198d83a78e83638cf8a7e2e64a00845d1133129605d4be2e096e047f9d34625`  
		Last Modified: Thu, 28 Mar 2024 02:08:33 GMT  
		Size: 144.1 MB (144142460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fffbae739e99f78575700699e5d6b2068dfb3b32ed589b525ee8475f3b8e576`  
		Last Modified: Thu, 28 Mar 2024 02:08:21 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0cc6b7730ff390bedbf2f91e5cadbee36904587061d17fed2c5f79baf34b4de`  
		Last Modified: Thu, 28 Mar 2024 02:08:21 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105e95721be050acec4707992aaa98192533e9a548202805c1d285775de91d02`  
		Last Modified: Thu, 28 Mar 2024 03:27:06 GMT  
		Size: 25.0 MB (25009154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e1403cfce873e10f94afb4bef1261decc1fd38d5226f5a633bd1561ffccbe2`  
		Last Modified: Thu, 28 Mar 2024 03:27:04 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1c4729a79d63268c9cc5d2d1181eec3be4a03d7d64910e81c76b7806029e15`  
		Last Modified: Thu, 28 Mar 2024 03:27:04 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
