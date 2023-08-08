## `eclipse-temurin:20-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:995f07c557f4840eabcfbe7a76d01182f7dfac62cfb1110011447ae1dbf792d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:20-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:03220324c1c11df4f0683031240753fe0ecdf831b2202977a635402b5e2e7488
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61861306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701515ddb709c241781c18b7ea773eefcfd41132f0755d1924121eec4989db6e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 19:19:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Aug 2023 19:19:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 19:19:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 19:19:46 GMT
RUN apk add --no-cache fontconfig java-cacerts libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Tue, 08 Aug 2023 19:24:43 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Tue, 08 Aug 2023 19:25:10 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='53b34747a3c042a4cccb2b8b78fba3330b105bc523f0861237baa9143dc39115';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jre_x64_alpine-linux_hotspot_20.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Tue, 08 Aug 2023 19:25:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 08 Aug 2023 19:25:11 GMT
COPY file:0673fe0a4a716089bcd96321c8de60149aea8a94ae7c4ba827ecc4a74a9789a3 in / 
# Tue, 08 Aug 2023 19:25:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fb73fc61a1a25f2a3dc05916ccac6537b166b6bb8aec0290fccb908e4e46e9`  
		Last Modified: Tue, 08 Aug 2023 19:26:28 GMT  
		Size: 8.5 MB (8495235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f239cf15ca63f296cc69778b9a8d05f0ee0e46b47e19642f308c8b4962010a0`  
		Last Modified: Tue, 08 Aug 2023 19:34:19 GMT  
		Size: 50.0 MB (49963630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a93788b0fe9a5cbc40d346aa5ceec6ccd542977b63a8a108bf5d810f421c776`  
		Last Modified: Tue, 08 Aug 2023 19:34:13 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a081a51b46362505dc1d2e9c99289fdb5caf98ae5b28369bdf0af7e229443c1b`  
		Last Modified: Tue, 08 Aug 2023 19:34:12 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
