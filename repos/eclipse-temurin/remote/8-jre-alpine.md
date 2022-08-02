## `eclipse-temurin:8-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:7160e1d3745a12451880d67e7e7e56d88fb530d2eb3d354184942c47c5731756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:8-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:54bfb94e9e88e616bb63498aed04c93cee9545d684382879bd4054cfc17ee0d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56611817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9fad8f1db205f0e991f19b79c10c947526c5cbbcaffcf6e233572c88cbb5cd4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:20:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 28 Jul 2022 16:20:06 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Tue, 02 Aug 2022 19:04:09 GMT
ENV JAVA_VERSION=jdk8u342-b07
# Tue, 02 Aug 2022 19:06:47 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='dd04e366c2e03310f9522b61a09f8ca056842a739cb33651e6eac60e3305c511';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u342b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 02 Aug 2022 19:06:48 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 19:06:48 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2b3b9d0d1a1f972083dde62c850175d26be845971e3c96ff06c8145fbe2fd0`  
		Last Modified: Thu, 28 Jul 2022 16:25:19 GMT  
		Size: 12.1 MB (12050034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7990e0776c9f4a683a01352861047565364739a7c0e31da7cc69ee2244279df9`  
		Last Modified: Tue, 02 Aug 2022 19:14:26 GMT  
		Size: 41.8 MB (41762817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8ee3ba163b4114fc083dc7b8968767db8d271baf47a29799517e6ea8a37d54`  
		Last Modified: Tue, 02 Aug 2022 19:14:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
