## `clojure:temurin-11-lein-noble`

```console
$ docker pull clojure@sha256:0522056351f465f94e9398ea2648cab4ba7c461e827c3ca281831511dd129069
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-lein-noble` - linux; amd64

```console
$ docker pull clojure@sha256:13510de6e9b2241f14bd624cc5f15d9a5d4275a759593b839368dfa9455a7375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211534089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a01cea75df3f84f1f17f30d100081a00d06ff41c73cf7a103776d5955f8338`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:33:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:33:03 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 15 Apr 2026 20:33:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='1ef020c2215f3169c7610df573581806c58f00a0a1d512fd945a2687cbed1173';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:33:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:33:10 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 22:02:20 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:02:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:02:20 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:02:33 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:02:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:02:33 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:02:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:02:35 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259bcdc624a912057aa754687df482d253fa52f4ecde7d816b42bfa092f530be`  
		Last Modified: Wed, 15 Apr 2026 20:33:26 GMT  
		Size: 17.0 MB (16983415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60280751ded65a2e682a2ab378c3fc9a796351e1fab267a226f3ea7878d378a5`  
		Last Modified: Wed, 15 Apr 2026 20:33:29 GMT  
		Size: 145.8 MB (145819268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e015fc8da2e3c44e2c7410290bbf43ffadf1289af0aafa394e83f0c297b46369`  
		Last Modified: Wed, 15 Apr 2026 20:33:25 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ceea77ee92dbbe89b1743c8186e9eafca85b8e102dbe624fe58ff9bef3c9bd3`  
		Last Modified: Wed, 15 Apr 2026 20:33:25 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992e0a5788e4d97b926910b1e7dbd1064dcc058c0058215aa35a8bbd48c6e5b6`  
		Last Modified: Wed, 15 Apr 2026 22:02:44 GMT  
		Size: 14.5 MB (14478239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eafa05a683737fc61b09d30652b7e6e5a37cb601ac2572ebedcc9e5f21a0a4b`  
		Last Modified: Wed, 15 Apr 2026 22:02:43 GMT  
		Size: 4.5 MB (4517716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:76849f659c2d443f768dc62cb42d30e5f307bb16b93735617e64d631f9d0affc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3380643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db303b7104d70aa60c21fe5975c4e51425dd37088d9f6d7911826a3f3b565b4c`

```dockerfile
```

-	Layers:
	-	`sha256:09cbad7fa8e9a894622f0ab01b2046a4f97c490922c9e66e14027dec20ee23f9`  
		Last Modified: Wed, 15 Apr 2026 22:02:43 GMT  
		Size: 3.4 MB (3364081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0667d8191493f95b1da2572ea4035bdfa6f57a7ca7f615b318a41047595e2dc1`  
		Last Modified: Wed, 15 Apr 2026 22:02:43 GMT  
		Size: 16.6 KB (16562 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-noble` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c1edbc8c2ccb2381ce85bb88753efbd700c2e8cdf5f2cd6a1a4fa4a2aac9baec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.4 MB (207384893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8df25be94f4a732b24aac5502ae476eb02fdc6dfe45639a1704e100571c5c31`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:33:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:33:24 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 15 Apr 2026 20:33:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='1ef020c2215f3169c7610df573581806c58f00a0a1d512fd945a2687cbed1173';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:33:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:33:31 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 22:13:43 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:13:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:13:43 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:13:59 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:13:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:13:59 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:14:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:14:00 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57e12f19a04b5ac9e1a6bd3ff16544bf8e32e25bbe05c07e9af1de9064224ea`  
		Last Modified: Wed, 15 Apr 2026 20:33:48 GMT  
		Size: 17.0 MB (16996196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8d051c925caddc27e15fb896e85e25957e80cb155fa0f58152964eef48a1dd`  
		Last Modified: Wed, 15 Apr 2026 20:33:51 GMT  
		Size: 142.5 MB (142513589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f15fe7227a0a815386947fb45f060258e49a2f1a7676f01f4949b72be68768`  
		Last Modified: Wed, 15 Apr 2026 20:33:48 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776b8c511c610219bb1baa901cb7773f0737c0d8ea7cff702d9aebb36e146807`  
		Last Modified: Wed, 15 Apr 2026 20:33:48 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6100e76dfdb5addcea85304c8674e0bb893c5157e69565ea141ea82dce852085`  
		Last Modified: Wed, 15 Apr 2026 22:14:11 GMT  
		Size: 14.5 MB (14479170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c972d32020bf44047e938d5e3f70b65f9a813ed55d61c5b128d1281e8d84734`  
		Last Modified: Wed, 15 Apr 2026 22:14:11 GMT  
		Size: 4.5 MB (4517685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:f7a07989e26a7a4c3b08119a6f9f603bdbcca540bf039630df484d2809018abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3381847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bace37e67dc2af79368cfe6750fb8c85f01fc7298639b9e18c2e028bf9797e14`

```dockerfile
```

-	Layers:
	-	`sha256:95e30ebcc1e9b98cb4f80137b44a2d9ce1e64d40fe1e812fe26ec05d898eb2f0`  
		Last Modified: Wed, 15 Apr 2026 22:14:11 GMT  
		Size: 3.4 MB (3365166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c4a94dc45870b74c60c8ee78b79d14f5311e1c4aa7dcbb86454fcd8e006e131`  
		Last Modified: Wed, 15 Apr 2026 22:14:11 GMT  
		Size: 16.7 KB (16681 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-noble` - linux; ppc64le

```console
$ docker pull clojure@sha256:98be277f36025f0641dda6575ea83d67ba7eac61f219781d98fd7c1ae999ec46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205175275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f8f6961bc699bb4f3c053200af10b7c8fc574db5720df2c92fbf2766ec5106`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 04:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 04:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 04:26:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 04:26:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:26:01 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 07 Apr 2026 04:27:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='1ef020c2215f3169c7610df573581806c58f00a0a1d512fd945a2687cbed1173';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 04:27:52 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 04:27:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 04:27:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 04:27:53 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 14:30:17 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 14:30:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 14:30:17 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:30:42 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 14:30:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 14:30:42 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 14:30:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 14:30:45 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d800c8df15b3edabc2d41fd12584d685162ec3e3407bdd29445e3916467625`  
		Last Modified: Tue, 07 Apr 2026 04:26:41 GMT  
		Size: 18.8 MB (18813117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a220c00f58cce4caec204896167dc168c2256b2b53fa887a51fa66eeccbc5b1f`  
		Last Modified: Tue, 07 Apr 2026 04:28:26 GMT  
		Size: 133.0 MB (133004967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c58ce451ad0981433298447fb3f692b8c3483469ea9d36516505fd460a9a8`  
		Last Modified: Tue, 07 Apr 2026 04:28:23 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f113810f8354a10896c0eaf92f06a48327ff4c0bf1e24f3557cb1984b01bdba9`  
		Last Modified: Tue, 07 Apr 2026 04:28:23 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b464b091eb15c85c79e1e341aea7af5ac71ce93672939489123cd345927c2ab`  
		Last Modified: Tue, 07 Apr 2026 14:31:08 GMT  
		Size: 14.5 MB (14523661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14672146ed9e0e28760b523d5722e5e0b21f2d2ed6ed31979f43b9e55c6e17e2`  
		Last Modified: Tue, 07 Apr 2026 14:31:08 GMT  
		Size: 4.5 MB (4517722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:c730ad3fa47709d24530bd379f4cdef5a0770293ead3c694f5e8e6779ff46f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3382191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bad7a2716530002b178bb27b0d38f6e5a8fabf90e9a07da7eba4655c2b6a892`

```dockerfile
```

-	Layers:
	-	`sha256:c09d593dd0824e0607c8f10fe4b8ef7afbffcc5009d39327a8aa5b2882cf1b69`  
		Last Modified: Tue, 07 Apr 2026 14:31:08 GMT  
		Size: 3.4 MB (3365583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0780d5ecd8b38230be34e4f3af32c0029af3b88c39821628c7660da7f9ca81c`  
		Last Modified: Tue, 07 Apr 2026 14:31:07 GMT  
		Size: 16.6 KB (16608 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-noble` - linux; s390x

```console
$ docker pull clojure@sha256:c02fd03ea6bafaff63e84cf7aebf6b9e8151107af7e69be60734a485fea2a6ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 MB (193075978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342ca3c22926d70569698628ec45757609c999618a6bc110ff792e121fda1031`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 03 Apr 2026 15:12:46 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:12:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:12:46 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:12:48 GMT
ADD file:31d45a66208318e1066130bac8975f44dea6e7e93cbfb2d29b0888e686bb10d5 in / 
# Fri, 03 Apr 2026 15:12:48 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 03:09:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:09:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:09:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 03:09:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:09:23 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 07 Apr 2026 03:09:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='1ef020c2215f3169c7610df573581806c58f00a0a1d512fd945a2687cbed1173';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 03:09:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 03:09:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:09:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 03:09:28 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 05:39:16 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 05:39:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 05:39:16 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:39:24 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 05:39:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 05:39:24 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 05:39:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 05:39:26 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:248eeda3355e38b5891b7f407370b5faea53785cd947438684bf34a757d0f83c`  
		Last Modified: Fri, 03 Apr 2026 15:57:06 GMT  
		Size: 29.9 MB (29911843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cafd1916c5cba31aaa22e1e52aa83c9c76d6979e0d05bbd0bccbd399520dd951`  
		Last Modified: Tue, 07 Apr 2026 03:09:52 GMT  
		Size: 17.6 MB (17579082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4b6b54faf1d0b905618d6c72981d0b30b7342ea2dde4805dc122eff6b8174b`  
		Last Modified: Tue, 07 Apr 2026 03:09:54 GMT  
		Size: 126.6 MB (126566100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b4944bffc81c057fa6031b471300cb088996165b8c0ae0219dde861cab1abb`  
		Last Modified: Tue, 07 Apr 2026 03:09:51 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d69899eb0c6daeaca16e7d61f72a2166b79ad0def7c9347df5ee9c033b2b7d5`  
		Last Modified: Tue, 07 Apr 2026 03:09:51 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23aeb7093790f6d0de3a42b0ae80efca428c1d232e32458f42826ed67c0cbd2`  
		Last Modified: Tue, 07 Apr 2026 05:39:40 GMT  
		Size: 14.5 MB (14498789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fe250fc29852ca133a086ea980f705e0bff5220c5d510ee22ae50c77960f86`  
		Last Modified: Tue, 07 Apr 2026 05:39:39 GMT  
		Size: 4.5 MB (4517692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:55b25f20507e2f3b31a763d9618c49e3055cb699b031ae0084f0140e28588ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3378451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8893b9e4b6acccdebcfc730953319921449d9c6340d35cfdb95d8244a5a0fa`

```dockerfile
```

-	Layers:
	-	`sha256:8fbf4cd4ae90fffd2f5f37e32699925424330f966f66d2bf2f0e7eb78d6ed944`  
		Last Modified: Tue, 07 Apr 2026 05:39:39 GMT  
		Size: 3.4 MB (3361889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:149960e0a07de0075282a99f71bf3651cda77dfdd473218cb589041efb4130f0`  
		Last Modified: Tue, 07 Apr 2026 05:39:39 GMT  
		Size: 16.6 KB (16562 bytes)  
		MIME: application/vnd.in-toto+json
