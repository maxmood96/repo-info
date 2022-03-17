## `eclipse-temurin:16-alpine`

```console
$ docker pull eclipse-temurin@sha256:6af50314837e1e2812c6239220c14ee8c7fd4c194c29f1bec10c0d85d362228a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:16-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:4ccaf8f8d176bd68f392fe5955d5de5dd9768d55c164561edf3825b55ee8915b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.7 MB (208716870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31dbaae9462b699284a5189ed659b0d969443b274e8f9ddf9c6e66760226ff9d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 08:42:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Mar 2022 08:42:17 GMT
RUN apk add --no-cache tzdata musl-locales musl-locales-lang     && rm -rf /var/cache/apk/*
# Thu, 17 Mar 2022 08:43:24 GMT
ENV JAVA_VERSION=jdk-16.0.2+7
# Thu, 17 Mar 2022 08:44:09 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='85788b1a1f470ca7ddc576028f29abbc3bc3b08f82dd811a3e24371689d7dc0f';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_x64_alpine-linux_hotspot_16.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 17 Mar 2022 08:44:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 08:44:11 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 17 Mar 2022 08:44:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d724c850e02b04db420d6d1310332dafdcbf4f8f4280d76ed66954a1b5d0f4d`  
		Last Modified: Thu, 17 Mar 2022 08:46:33 GMT  
		Size: 430.3 KB (430324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2dae6c6ca6defdb06349ef503be3cd081b293d44f87701f434b99a8828f3bb`  
		Last Modified: Thu, 17 Mar 2022 08:48:20 GMT  
		Size: 205.5 MB (205473750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed37c39c1008f35abdb52c98c8e57919a41a2b825cf5fa046c82a7995c7256de`  
		Last Modified: Thu, 17 Mar 2022 08:48:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
