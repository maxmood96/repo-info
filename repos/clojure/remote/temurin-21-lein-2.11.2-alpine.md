## `clojure:temurin-21-lein-2.11.2-alpine`

```console
$ docker pull clojure@sha256:3907189612997a0246779934a874ec41e82a3dc0b514a6c6b8880287bdd86b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-21-lein-2.11.2-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:88156d6515ea84429a220087b9cf7a70d88bf2bc2f8742eafc4d371b37537b52
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194373370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9e416220656f149cb4f22a140903ac8cb5623ee091394873bba810e211402e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ae933ea8eeb4a077f19277842ba95ba93d29177e44d53cec7a98afd3b9abb2c3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|x86_64)          ESUM='f1aef3652dd52778e81eb4897a88a34e38ca0159d22f160f7205e69907a0f14d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jan 2024 16:26:40 GMT
CMD ["jshell"]
# Thu, 28 Mar 2024 03:13:58 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 28 Mar 2024 03:13:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 03:13:59 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 03:14:06 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg
# Thu, 28 Mar 2024 03:14:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 03:14:06 GMT
ENV LEIN_ROOT=1
# Thu, 28 Mar 2024 03:14:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 28 Mar 2024 03:14:09 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 28 Mar 2024 03:14:09 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Mar 2024 03:14:09 GMT
CMD ["repl"]
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
	-	`sha256:13c8d44cd81ae585be60b12254377d294b8eb28ebfa809cee3de1933df329bc9`  
		Last Modified: Thu, 28 Mar 2024 02:11:35 GMT  
		Size: 158.6 MB (158613224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca06bcaef85ff89a17a87f72633d787d9e78bec3d6847e9e259d9660c0ce804c`  
		Last Modified: Thu, 28 Mar 2024 02:11:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2fb673cb6a1c61ed86e2fe70b91500f6379514b0cc3c30f293c27c441cdb44`  
		Last Modified: Thu, 28 Mar 2024 02:11:23 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857c1fb428559035bf556a667282ef5f7cda97b91ae87cabff2ee0238ac0eb6d`  
		Last Modified: Thu, 28 Mar 2024 03:29:07 GMT  
		Size: 14.8 MB (14808172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297814393f1d2e1fe0f8eea33e4e653f9092330c2bffb6fc17812ad64fb1ef93`  
		Last Modified: Thu, 28 Mar 2024 03:29:06 GMT  
		Size: 4.4 MB (4399128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e56af147e9570d0fd4954ec6bb52651deca510b9059c64fff96fd507936ab52`  
		Last Modified: Thu, 28 Mar 2024 03:29:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
