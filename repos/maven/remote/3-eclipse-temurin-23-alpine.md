## `maven:3-eclipse-temurin-23-alpine`

```console
$ docker pull maven@sha256:a074c81c6501237c379c8a0ad486b628262a0f7b6826d835962345d512b4420c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-eclipse-temurin-23-alpine` - linux; amd64

```console
$ docker pull maven@sha256:2b2f8d49b1784009b7557dd76cd93742f79b3d8509f8ea4461f153400f346da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196567754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d97f63b7dd8cc9e7d1e39a15b20a232ff41f536f6023578137c3c0dc515cd3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7e842c9b8a44a5a21d83a3e38ae3b141cfbdb429dde70ff264d3da4bff44e1c7';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23_37.tar.gz';          ;;        x86_64)          ESUM='bff4c78f30d8d173e622bf2f40c36113df47337fc6d1ee5105ed2459841165aa';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["jshell"]
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c465b99ed376b808b3496edf1585f2ad0cb453ae29a1d59ee5096f69d6be8535`  
		Last Modified: Sat, 19 Oct 2024 00:56:58 GMT  
		Size: 14.0 MB (14032592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4bf0b0c1d7ee2470cc2bf871ee2b35c2857b0f7c9faced7f45d964eebc5b0c`  
		Last Modified: Sat, 19 Oct 2024 00:57:01 GMT  
		Size: 165.5 MB (165477030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e077ca61de339e804266d1ee1932d35309101b9b23394e95c804b0dc7e1de834`  
		Last Modified: Sat, 19 Oct 2024 00:56:57 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b359dd7cb5656dfcad483a65e7359531a980675f992e33c22da6803270508c46`  
		Last Modified: Sat, 19 Oct 2024 00:56:57 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7f888b9deb687eb7291f774bb817618273bd75097050febec3d70ba1196a84`  
		Last Modified: Sat, 19 Oct 2024 04:07:06 GMT  
		Size: 4.3 MB (4260620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db62b94f4f1a66ca732dbed2fca18a9cda01e314dcbffdd94c263b5dd8030d3f`  
		Last Modified: Sat, 19 Oct 2024 04:07:07 GMT  
		Size: 9.2 MB (9170422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362d0939ea8b0ff2bc9ced2d2206e446f7bfa0981510ddc67bfd51ffe369fe2b`  
		Last Modified: Sat, 19 Oct 2024 04:07:06 GMT  
		Size: 859.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5318f0e970fc83d89593d3c439a5884a47110c0e855203d6f1f537a572c24a1d`  
		Last Modified: Sat, 19 Oct 2024 04:07:06 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-23-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:11c8e3b8309cf97d6fabeed3bd1c752e2f3b17367b83ab7acce91c3ba20355de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1153396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de1d49ab5548958f166e35701a7711ed06eb6f2a8a7707dcf9d5120a21b24ee`

```dockerfile
```

-	Layers:
	-	`sha256:fc435a05efec864f662c26e25b95cb715429c4626e5fcd2addebd59dd243e7f0`  
		Last Modified: Sat, 19 Oct 2024 04:07:06 GMT  
		Size: 1.1 MB (1134021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0718f28fc212e7c98c28c0b332172f02a365de91cb3d2077c04a2685bf0dc04`  
		Last Modified: Sat, 19 Oct 2024 04:07:07 GMT  
		Size: 19.4 KB (19375 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-23-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:44bbc3d6ffb482ce05da0d9a1fd3f536d51261a9b2cf14aafb5d465c77e2bb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195284935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2862c7d750d787ae6ed84a1fe8d07c6e57f3363c27b0aebb9ca16a1ac939dc89`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7e842c9b8a44a5a21d83a3e38ae3b141cfbdb429dde70ff264d3da4bff44e1c7';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23_37.tar.gz';          ;;        x86_64)          ESUM='bff4c78f30d8d173e622bf2f40c36113df47337fc6d1ee5105ed2459841165aa';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["jshell"]
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8a2d3622211b600f84f1b27f8913afa35a6719e1ddde90ee5afb4bc8b95868`  
		Last Modified: Fri, 06 Sep 2024 23:28:36 GMT  
		Size: 14.4 MB (14361804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca71b940bc0515e2cd88c7749756cdc6809b90ef64535150471a4854be04aa96`  
		Last Modified: Wed, 18 Sep 2024 21:43:00 GMT  
		Size: 163.3 MB (163267041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5c32e826fe5026e154405a879031055c930543d9c43e64afbfdaf8408e87b2`  
		Last Modified: Wed, 18 Sep 2024 21:42:50 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b643d5e7a3f6bf6a53372aa04960330116f64f4d0d45552d997e90e1d7bd18`  
		Last Modified: Wed, 18 Sep 2024 21:42:50 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b692b35f0ff47c469468ab1c88e46d4cf2a9432c943879f63657b59d60c4e4e`  
		Last Modified: Sat, 12 Oct 2024 07:03:00 GMT  
		Size: 4.4 MB (4394694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc38c4120610f9c5efbd3f29ee635e0e72a7ce4ac64a0ec4991a081ed9ed1b19`  
		Last Modified: Sat, 12 Oct 2024 07:03:00 GMT  
		Size: 9.2 MB (9170438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f476d1de9d638726a2579e8b61668f5ca0f0d5bc9c9cba45a1888c29341e70`  
		Last Modified: Sat, 12 Oct 2024 07:03:00 GMT  
		Size: 858.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7799c0dd49eca8cd3f70e5041cd7e0c19f4d8ed364261bc55f84b14b73cbeb`  
		Last Modified: Sat, 12 Oct 2024 07:03:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-23-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:83fc58e56dde4390a294e805421b503af7498be5744c0def1647b76486018cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1252446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4a3add2b6c335235655cc3b8aab12cf6d22549d28afb801d513ec96f8e0272`

```dockerfile
```

-	Layers:
	-	`sha256:1547691b42017a3f1473060110b7c937dd12de386b72c10b706d500d70345f36`  
		Last Modified: Wed, 16 Oct 2024 07:17:47 GMT  
		Size: 1.2 MB (1232899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55b5f3584aae18390c6d7e8bbbd11a2148a1bd77db31fcd0b0cd754ab5292400`  
		Last Modified: Wed, 16 Oct 2024 07:17:47 GMT  
		Size: 19.5 KB (19547 bytes)  
		MIME: application/vnd.in-toto+json
