## `maven:3-eclipse-temurin-20-alpine`

```console
$ docker pull maven@sha256:0a3b5e83c310523dd554e63f5079da5acaf169256556e87276fed6d148d90eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-eclipse-temurin-20-alpine` - linux; amd64

```console
$ docker pull maven@sha256:30c851ffd9fea2b03d275413c212639b3aa34bc174ada37ae4ae22a9da2f6127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.8 MB (176760957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdd3b99a9df5c4e37a145973efa0d9dfeb8a7bb00f7630fdc6308156b0bc3dcb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 05:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jun 2023 05:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 05:11:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 03 Aug 2023 02:38:05 GMT
RUN apk add --no-cache fontconfig java-cacerts libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Thu, 03 Aug 2023 02:38:05 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Thu, 03 Aug 2023 02:38:16 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b03aced4b7a1c49bc00297e35e45480fd03818862b93e17e1551a3b721e89306';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jdk_x64_alpine-linux_hotspot_20.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 03 Aug 2023 02:38:18 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 03 Aug 2023 02:38:18 GMT
COPY file:0673fe0a4a716089bcd96321c8de60149aea8a94ae7c4ba827ecc4a74a9789a3 in / 
# Thu, 03 Aug 2023 02:38:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Aug 2023 02:38:19 GMT
CMD ["jshell"]
# Mon, 26 Jun 2023 13:48:06 GMT
RUN apk add --no-cache bash procps curl tar # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 26 Jun 2023 13:48:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
ARG MAVEN_VERSION=3.9.3
# Mon, 26 Jun 2023 13:48:06 GMT
ARG USER_HOME_DIR=/root
# Mon, 26 Jun 2023 13:48:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 26 Jun 2023 13:48:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 26 Jun 2023 13:48:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74c4e203881eb96b19b7e16e4d2070742fab18cdfaeb2f07897bd520ec0f868`  
		Last Modified: Thu, 03 Aug 2023 02:42:21 GMT  
		Size: 8.5 MB (8495234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db2f5bca0f22f2f791cbe4b3e7abe717cff049b6dfa83a26912fb609457f068`  
		Last Modified: Thu, 03 Aug 2023 02:42:32 GMT  
		Size: 152.9 MB (152930849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42cb67a7d7a0eb00c40cff496479b26a71b8eb21e657a9f6c644d7a6853e49d7`  
		Last Modified: Thu, 03 Aug 2023 02:42:20 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898b1e6cf835777501f8f1da816adc4f014445b3a3d7f57982b65a6bdc6c2f23`  
		Last Modified: Thu, 03 Aug 2023 02:42:20 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ab47d47a052a737df3c3917f0bc419ac06296b749eef16766d4a20977255ee`  
		Last Modified: Thu, 03 Aug 2023 04:56:45 GMT  
		Size: 2.6 MB (2607198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e3e5752c055f23ac99cb2c191fd757f2dc06a4d122d4d1896b8d05df62d18c`  
		Last Modified: Thu, 03 Aug 2023 04:56:45 GMT  
		Size: 9.3 MB (9327572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fd8ae820ca899e70f7bcc2929b2ec575136dbb225fb9c0c0a906260b79b501`  
		Last Modified: Thu, 03 Aug 2023 04:56:44 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca42826b66d91330a2fa551aab178443e901fc07ae9891e5792034b41c41f7a8`  
		Last Modified: Thu, 03 Aug 2023 04:56:44 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:310ce2bb119299d941f9f25be84727c6679fe4441109fcd784897f09fb139efe`  
		Last Modified: Thu, 03 Aug 2023 04:56:44 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
