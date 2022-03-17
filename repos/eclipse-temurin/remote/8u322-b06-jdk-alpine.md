## `eclipse-temurin:8u322-b06-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:59a8c89b9af0d5aca8d28c02f4a7f7da9f98fdaefdc281abab4f22cc045c32a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:8u322-b06-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:6b1dd43477276b620d5c53f6689e11f2d26825b350047d97a82e187d811dabd0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104822128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1128eb3031df6deeaa526e87d1d1c40062f0b2fecca63709373405afd69687eb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 08:42:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Mar 2022 08:42:17 GMT
RUN apk add --no-cache tzdata musl-locales musl-locales-lang     && rm -rf /var/cache/apk/*
# Thu, 17 Mar 2022 08:42:18 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Thu, 17 Mar 2022 08:42:27 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c7e781064c4a63ad6cd2399b2fa34de854a7d9bfd3ad2543d34bd7ba8f818822';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 17 Mar 2022 08:42:27 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 08:42:28 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:d3241c60a520bd1858031ec2f595cd5de4f19fd2685370f8dc21e53cab2f68a2`  
		Last Modified: Thu, 17 Mar 2022 08:46:43 GMT  
		Size: 101.6 MB (101579006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaae8b1c335df2c1cd0eff5c326c4c32af88e484f7f188203c732ce33204a969`  
		Last Modified: Thu, 17 Mar 2022 08:46:33 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
