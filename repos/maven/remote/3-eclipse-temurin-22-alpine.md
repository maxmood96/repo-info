## `maven:3-eclipse-temurin-22-alpine`

```console
$ docker pull maven@sha256:9b8d6e3b3b069f94b8b6a895d2fde4ddc59533a3a665fbe05458932e033372dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-eclipse-temurin-22-alpine` - linux; amd64

```console
$ docker pull maven@sha256:5bfaf23a8433273b96deccf5c60f498f9d2bce7ab7676fc37c949a10436678b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185576691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050ffa5f3ae5e8bfb3ba46f9af8cd840d35613ba943a2b2c8f1bc03213719796`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Mar 2024 15:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 15:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_VERSION=jdk-22+36
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e6c97db54afe145a8f93f9ca728b4df8a0490a45f0f999999c7464c64612e936';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_aarch64_alpine-linux_hotspot_22_36.tar.gz';          ;;        amd64|x86_64)          ESUM='f88fbe6360276cc9aec406802838ff0cfb368e08c2b1cf7b6fa78a846266a7af';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_x64_alpine-linux_hotspot_22_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 27 Mar 2024 15:44:12 GMT
CMD ["jshell"]
# Thu, 28 Mar 2024 14:25:35 GMT
RUN apk add --no-cache bash procps curl tar # buildkit
# Thu, 28 Mar 2024 14:25:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 28 Mar 2024 14:25:35 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 28 Mar 2024 14:25:35 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 28 Mar 2024 14:25:35 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 28 Mar 2024 14:25:35 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 28 Mar 2024 14:25:35 GMT
ARG MAVEN_VERSION=3.9.6
# Thu, 28 Mar 2024 14:25:35 GMT
ARG USER_HOME_DIR=/root
# Thu, 28 Mar 2024 14:25:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 28 Mar 2024 14:25:35 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 28 Mar 2024 14:25:35 GMT
CMD ["mvn"]
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
	-	`sha256:7d16a09bdd2022ae839a65837d1a3d02a6a233d70f44f665de557eea30b95357`  
		Last Modified: Thu, 28 Mar 2024 02:13:29 GMT  
		Size: 156.9 MB (156908225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c642c25f34caeb8375bdecd0c42cc6b7b906402f01bd5a1cdfc0c39e220b49df`  
		Last Modified: Thu, 28 Mar 2024 02:13:16 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a202be78f0ec29cfef7091bb4d92bc81e889949058a84557ddd8c299f1b4bb`  
		Last Modified: Thu, 28 Mar 2024 02:13:16 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0784175923c8a2d126e92c6be7fbe0aec5212bc82a090cfb5dae7503fed9140a`  
		Last Modified: Wed, 03 Apr 2024 00:25:24 GMT  
		Size: 2.6 MB (2634692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07d58da67a53c2a90953acbe8d3885624c4ea440cf40bc0b8f9e32acd2bd0c7`  
		Last Modified: Wed, 03 Apr 2024 00:25:24 GMT  
		Size: 9.5 MB (9479947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614d5e813c4cdf31dc070a2c3ecce3e17b3b4bff2dc15bd122f527372967d671`  
		Last Modified: Wed, 03 Apr 2024 00:25:23 GMT  
		Size: 862.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7f3b173b607f988966a1f2660e96125de27bce1506ef68f72ee4394834ec44`  
		Last Modified: Wed, 03 Apr 2024 00:25:23 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7326a833a5d262ec40a43edaacc548e1d3a1d510b4ca3026649b35ffcc1856e6`  
		Last Modified: Wed, 03 Apr 2024 00:25:23 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-22-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:aeae201295533bdcde36fd2d0753ddaa3cc649a6a1d2be0ca747f2eda8ecabb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183728498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12884acc6abfcfb10fc7ce9954a26919a8c71764c3123ddfc55c7314ecfa95e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
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
# Thu, 28 Mar 2024 14:25:35 GMT
RUN apk add --no-cache bash procps curl tar # buildkit
# Thu, 28 Mar 2024 14:25:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 28 Mar 2024 14:25:35 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 28 Mar 2024 14:25:35 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 28 Mar 2024 14:25:35 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 28 Mar 2024 14:25:35 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 28 Mar 2024 14:25:35 GMT
ARG MAVEN_VERSION=3.9.6
# Thu, 28 Mar 2024 14:25:35 GMT
ARG USER_HOME_DIR=/root
# Thu, 28 Mar 2024 14:25:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 28 Mar 2024 14:25:35 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 28 Mar 2024 14:25:35 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38eb0c9d7c04691eff93919fd977269a8104369a10cadd69b1a9b35aba5b9085`  
		Last Modified: Thu, 28 Mar 2024 00:54:36 GMT  
		Size: 13.4 MB (13426226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc04f802e30a9b9662709264af142697ac8331f18ab84cfcc7121b36cae53ab`  
		Last Modified: Wed, 24 Apr 2024 18:02:21 GMT  
		Size: 154.7 MB (154683750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c7e802f1e104ac15c900ec5de2b80d1c2a7c8cdb00d16f69891fca20b26a65`  
		Last Modified: Wed, 24 Apr 2024 18:02:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5a08d152eccfa3cc5f6cba7c86f4db0730117a1ece02e2e570b953c9d327c4`  
		Last Modified: Wed, 24 Apr 2024 18:02:11 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2919941e9888bbb47d26fd680d47306c6a75bed5421fb025c0562648fc66cf25`  
		Last Modified: Wed, 24 Apr 2024 18:57:26 GMT  
		Size: 2.8 MB (2788567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0d89d64f2370d7df85527b3dc30dd50b4421e5fc7eca07110699f275795a04`  
		Last Modified: Wed, 24 Apr 2024 18:57:26 GMT  
		Size: 9.5 MB (9479953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d00492cf28c38b1d3e2ae826e8affe98af09b202a4f271f79eaedd44b761b1`  
		Last Modified: Wed, 24 Apr 2024 18:57:26 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4d96049f731a9293601b70cdcfd513928ae50d7b2db1dec8c1e4c175f92324`  
		Last Modified: Wed, 24 Apr 2024 18:57:25 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa38cd20234533e23adff02f7c404d0fe71aa802aa94a7d7f2b9301093428405`  
		Last Modified: Wed, 24 Apr 2024 18:57:25 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
