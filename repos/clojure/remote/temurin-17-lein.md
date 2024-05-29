## `clojure:temurin-17-lein`

```console
$ docker pull clojure@sha256:449a868cfa51e38b366240236bfd45764a417d38a842f3b5c7271694175a4e30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein` - linux; amd64

```console
$ docker pull clojure@sha256:1e4e96ec485445ac20a649efaeef443d131419e252d76c90cf682cbafd04f4dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.6 MB (211620969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfbc2187dd446ad0bf838cd244946ae049a6178bc53fa55b52a06d626b75bfd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a900acf3ae56b000afc35468a083b6d6fd695abec87a8abdb02743d5c72f6d6d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa7fb6bb342319d227a838af5c363bfa1b4a670c209372f9e6585bd79da6220c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='9b5c375ed7ce654083c6c1137d8daadebaf8657650576115f0deafab00d0f1d7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='44bdd662c3b832cfe0b808362866b8d7a700dd60e6e39716dee97211d35c230f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='af3f33c14ed3e2fcd85a390575029fbf92a491f60cfdc274544ac8ad6532de47';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 15:17:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5d1bccc5440d3a24f4a620704b9e687b4163c6c872fcc8e812e200c9bbac58`  
		Last Modified: Thu, 02 May 2024 01:18:08 GMT  
		Size: 17.5 MB (17456240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59fd278c1b4ffe1727be6ccba42125e8f4db57e660e795cce19889d2c776457`  
		Last Modified: Thu, 02 May 2024 01:18:17 GMT  
		Size: 145.1 MB (145100254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97285723537ab7921fca4d081c256e501adfdaa8992d04637992075f4cea392`  
		Last Modified: Thu, 02 May 2024 01:18:05 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ba11f7aaaedad962216812fe84aee9061aeabac6932f0274a1d204eb96e8e8`  
		Last Modified: Thu, 02 May 2024 01:18:05 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18e232dbfa673e777f5190e54e1cca5ab690bb3deddff9cbce89591febc25e0`  
		Last Modified: Wed, 29 May 2024 19:57:01 GMT  
		Size: 14.2 MB (14225479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fac8d0bbc25f5062ccac51a7d4645a5b4599f60ae40bc4842218debd478f12f`  
		Last Modified: Wed, 29 May 2024 19:57:01 GMT  
		Size: 4.4 MB (4398006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b326920e30995d18b4e9e10fcded32dcdab41e8564dba46fc0dabe8db27132eb`  
		Last Modified: Wed, 29 May 2024 19:57:01 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:83e6d8b655f2f5dfe9c4818a5e603f8300d3ed84a1b2b999e924eacc0f89e92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3689358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69046f35230567072e165274e91de434b3c9827a24895c856cecaaf3ed12ddcb`

```dockerfile
```

-	Layers:
	-	`sha256:a7ad84ebc27ab68492d683146fc225554049e2fe6cf233c2fba9be2839986c66`  
		Last Modified: Wed, 29 May 2024 19:57:01 GMT  
		Size: 3.7 MB (3670399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7815794d7af92867a34d2790192c929406ed46368a404d6cd559fe0c08271e00`  
		Last Modified: Wed, 29 May 2024 19:57:01 GMT  
		Size: 19.0 KB (18959 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1c61fecc801cc0d729a0f8e7766a4772e2c72251a85d684d3e9c985f64b78387
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (210018887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00a7f0a6a161d4ae098486c9a9839671561bb82d6b372e4fdeb7da05ea5e42e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a900acf3ae56b000afc35468a083b6d6fd695abec87a8abdb02743d5c72f6d6d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa7fb6bb342319d227a838af5c363bfa1b4a670c209372f9e6585bd79da6220c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='9b5c375ed7ce654083c6c1137d8daadebaf8657650576115f0deafab00d0f1d7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='44bdd662c3b832cfe0b808362866b8d7a700dd60e6e39716dee97211d35c230f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='af3f33c14ed3e2fcd85a390575029fbf92a491f60cfdc274544ac8ad6532de47';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Tue, 28 May 2024 19:56:27 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 19:56:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 19:56:27 GMT
WORKDIR /tmp
# Tue, 28 May 2024 19:56:41 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 28 May 2024 19:56:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 19:56:41 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 19:56:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Tue, 28 May 2024 19:56:43 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 19:56:43 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 19:56:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8868eeb30ae6b43fdd3ec11d565b77e83f6c78c86d892957cf1cecb5cc59c9`  
		Last Modified: Thu, 02 May 2024 04:19:45 GMT  
		Size: 18.9 MB (18858238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c5f0f638087f0231a157f7deba2d5494e0cd15dfc56fab26293430ccccd3d2`  
		Last Modified: Thu, 02 May 2024 04:19:53 GMT  
		Size: 143.9 MB (143896056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b7d030db882e91686c67d5a7c655905f45b24a3e131c15eacc276f3033475c`  
		Last Modified: Thu, 02 May 2024 04:19:43 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a00ec0bc677d0cfff04f78636ce68c4815766fc7560ceb0c5f031e84ffb38607`  
		Last Modified: Thu, 02 May 2024 04:19:43 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4211cdfa5ab9f68940a42d4c20232d31426193ad422e0de9b3e790ead7da5c6b`  
		Last Modified: Tue, 28 May 2024 20:15:58 GMT  
		Size: 14.5 MB (14464017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9019cfefd30a9aac8baf8d912cfb5c16c7e1a76bbbdab3fc2605b6b1a018bef5`  
		Last Modified: Tue, 28 May 2024 20:15:57 GMT  
		Size: 4.4 MB (4398089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d18c6ba102f0dfee06735dcffae630454347fa8aec2c00f9022458e1b51da1`  
		Last Modified: Tue, 28 May 2024 20:15:56 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
