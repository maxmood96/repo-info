## `eclipse-temurin:17_35-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:e78a9657273fe6d06ab55c0ff65b53cc9f88b3b5e6a2dc791d66b0630cc4cfb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:17_35-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:1153cafb5f012d1ddf61199bc2f74a9b177990c3ccba67ff283ab33751533d33
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.1 MB (195113019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1aab206831a90b086506d69e1c00293290deac808b7b7ead76d1a4c52b4a55f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 17 Sep 2021 21:41:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 24 Sep 2021 19:20:30 GMT
RUN apk add --no-cache tzdata musl-locales musl-locales-lang     && rm -rf /var/cache/apk/*
# Fri, 24 Sep 2021 19:20:30 GMT
ENV JAVA_VERSION=jdk-17+35
# Fri, 24 Sep 2021 19:20:42 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='03321e009cc5955d7dbabc9219434d63a5b390c223c8ecc303eb1741eb9036ef';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17%2B35/OpenJDK17-jdk_x64_alpine-linux_hotspot_17_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 24 Sep 2021 19:20:42 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Sep 2021 19:20:43 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 24 Sep 2021 19:20:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5491faa5141cd7b6b8bcb2f0546bc3268ca907c1a0835e91db57c666453bde3d`  
		Last Modified: Fri, 24 Sep 2021 19:23:00 GMT  
		Size: 408.6 KB (408594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d8ba3cf6cc5919b2690d102b82a8a714e02f24905d150825a35da2f5068f0d`  
		Last Modified: Fri, 24 Sep 2021 19:23:14 GMT  
		Size: 191.9 MB (191889819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff8ea996eda8bbfee06fdcbf6fe234e9b5f703caa6662ce40bc7ef309df521e`  
		Last Modified: Fri, 24 Sep 2021 19:23:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
