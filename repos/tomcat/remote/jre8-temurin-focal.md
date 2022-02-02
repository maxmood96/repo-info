## `tomcat:jre8-temurin-focal`

```console
$ docker pull tomcat@sha256:0e2510058a5bb626f7149810b07ac832e9776d3b6304956821dc9983cef0e49e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `tomcat:jre8-temurin-focal` - linux; amd64

```console
$ docker pull tomcat@sha256:2c21a1cecd7ec2585247158f7fe95bac5b2de8f3d9a40b7bb79369b00639ee39
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108182385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d49f64efd6bacdfd064636bf41d75b9cf9163007f87ad8a0afe8795fbfa87c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:57:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 02:58:19 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:58:20 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 02 Feb 2022 02:58:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 02:58:44 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 02:58:45 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 02 Feb 2022 14:21:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 02 Feb 2022 14:21:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 14:21:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 02 Feb 2022 14:21:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 02 Feb 2022 14:21:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 14:21:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 14:21:22 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 02 Feb 2022 14:21:22 GMT
ENV TOMCAT_MAJOR=10
# Wed, 02 Feb 2022 14:21:22 GMT
ENV TOMCAT_VERSION=10.0.16
# Wed, 02 Feb 2022 14:21:22 GMT
ENV TOMCAT_SHA512=9b70f4db2c7b2efb5453cd581322b1137df7b6443acd6a8e278eaaf97de89c9ad0c7c7996a2d545ef1e4d965aca43c40d2b2c7d5e46b021695f87093143fbba2
# Wed, 02 Feb 2022 14:21:23 GMT
COPY dir:9817515b39f748e0a3e763204664898eca4130afe0c8375377f1214c08fc0767 in /usr/local/tomcat 
# Wed, 02 Feb 2022 14:21:27 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 14:21:30 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 02 Feb 2022 14:21:30 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 14:21:30 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd22f8f9007b7341ddccd906a9f476337b871592380b8c0c2cc5f7c8e4b16928`  
		Last Modified: Wed, 02 Feb 2022 03:02:00 GMT  
		Size: 24.8 MB (24814660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b5670e09cae35e525f2497821afc5c8ab0d7c165fc828f5f68d3b0597eeb66`  
		Last Modified: Wed, 02 Feb 2022 03:02:24 GMT  
		Size: 41.8 MB (41773795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c787c85c7df15d6ae55cb0f3a97270f2aa896caff7d463152f2409c2ced7aceb`  
		Last Modified: Wed, 02 Feb 2022 03:02:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc29310517c12356f12de8815e44af8645d79f1fb468b43d2d6f3cc10e587046`  
		Last Modified: Wed, 02 Feb 2022 14:56:38 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d553b4971d58468b2e5a7404930ecc9d43eb470863bfc645d8f399f3a88f2879`  
		Last Modified: Wed, 02 Feb 2022 14:56:39 GMT  
		Size: 12.6 MB (12577438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad4b591190281e2aee6cd04ab884f331f8e24c98623669aa538a1ce20390648`  
		Last Modified: Wed, 02 Feb 2022 14:56:38 GMT  
		Size: 451.9 KB (451932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060fa50e96511a8f77fee6976ce1c6569039df3f6cc43d430a013e969051d13f`  
		Last Modified: Wed, 02 Feb 2022 14:56:38 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre8-temurin-focal` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:43984ca63480bdc9b4ca50647ad52932e69079ba8ca34d7ae04cd50ce58b3e91
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99584180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56aa7322c9730026e28d58978af9b81a2ef52ff6859fd4062c382f37d10bb19`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 07 Jan 2022 02:26:25 GMT
ADD file:ac83e0dc7e48a0dc1805c0fd7b71b8eb119b3eeafd1fdcab93e11fbc9c0bcda0 in / 
# Fri, 07 Jan 2022 02:26:26 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:24:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 07 Jan 2022 03:25:22 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:25:23 GMT
ENV JAVA_VERSION=jdk8u312-b07
# Fri, 07 Jan 2022 03:26:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='961df2d520987c2252496fbee024f84c8c8c4d0be80e9fe043d221191666899e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u312b07.tar.gz';          ;;        armhf|arm)          ESUM='5f37cbf311a5c2928aff8e83a82aebcf37b5911b193b5ab8538108381dcd6276';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_arm_linux_hotspot_8u312b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='7914a2efcb7edb28df71b2d4e5194907163da06841a16f7c8c96d60677551f93';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u312b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='18fd13e77621f712326bfcf79c3e3cc08c880e3e4b8f63a1e5da619f3054b063';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_x64_linux_hotspot_8u312b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 07 Jan 2022 03:26:26 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jan 2022 03:26:28 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 07 Jan 2022 06:59:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 07 Jan 2022 06:59:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jan 2022 06:59:20 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 07 Jan 2022 06:59:20 GMT
WORKDIR /usr/local/tomcat
# Fri, 07 Jan 2022 06:59:20 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 07 Jan 2022 06:59:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 07 Jan 2022 06:59:21 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 07 Jan 2022 06:59:22 GMT
ENV TOMCAT_MAJOR=10
# Fri, 21 Jan 2022 03:43:01 GMT
ENV TOMCAT_VERSION=10.0.16
# Fri, 21 Jan 2022 03:43:01 GMT
ENV TOMCAT_SHA512=9b70f4db2c7b2efb5453cd581322b1137df7b6443acd6a8e278eaaf97de89c9ad0c7c7996a2d545ef1e4d965aca43c40d2b2c7d5e46b021695f87093143fbba2
# Fri, 21 Jan 2022 03:43:04 GMT
COPY dir:af152fb4bc94de5c517c851b37695eb32ea29fdaf3c1d46b71d8550a4c3fbc85 in /usr/local/tomcat 
# Fri, 21 Jan 2022 03:43:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Jan 2022 03:43:17 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 21 Jan 2022 03:43:17 GMT
EXPOSE 8080
# Fri, 21 Jan 2022 03:43:18 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9b8080fa0945580f29aa3abed4664f8ab849229eca04510b5d259a9e29616064`  
		Last Modified: Fri, 07 Jan 2022 02:30:39 GMT  
		Size: 24.1 MB (24064434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6e4c0409024952682215eb90badafc7748ba973c9a2d5b93c8c3148ce34ee5`  
		Last Modified: Fri, 07 Jan 2022 03:33:32 GMT  
		Size: 23.1 MB (23071830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5e7c8b7aa637b49bae8c91c642697ee48d1fa702341213bc86c1488aa78c9b`  
		Last Modified: Fri, 07 Jan 2022 03:34:37 GMT  
		Size: 39.5 MB (39491847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535dae6cb9ab7ac13e6158271d53e65b332939edffce207fa8eb7823a73f78b1`  
		Last Modified: Fri, 07 Jan 2022 03:34:16 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352ce8a5357decdef910d6256d719751bdc31886ffc9e3516cf222754bd09108`  
		Last Modified: Fri, 07 Jan 2022 07:34:25 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa3bff97b9b0a9d9a9d4030237b37fe529de963d091670b132604ca36854ecc`  
		Last Modified: Fri, 21 Jan 2022 05:59:31 GMT  
		Size: 12.5 MB (12526049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02789e2924998cc3a646879602de26b7ef56d9b8ccc36ea5060b3a8adca0ea1f`  
		Last Modified: Fri, 21 Jan 2022 05:59:26 GMT  
		Size: 429.6 KB (429560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10c6a361d9641edadd70e0418e0a8922947ee0dea96f060780355e092d6595d`  
		Last Modified: Fri, 21 Jan 2022 05:59:26 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre8-temurin-focal` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:a0e905e35a204e86a6b78aca5b4fa3857696514f8d9a772688c28b4d7dcd01a8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105509917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c21e00664e75f3371a775cac7e1049973eaf22e28ff8c38c5af7636f9ff0bc`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:01:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:01:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:01:54 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 02 Feb 2022 05:02:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:02:23 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:02:24 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 02 Feb 2022 07:38:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 02 Feb 2022 07:38:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 07:38:28 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 02 Feb 2022 07:38:29 GMT
WORKDIR /usr/local/tomcat
# Wed, 02 Feb 2022 07:38:30 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 07:38:31 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 07:38:32 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 02 Feb 2022 07:38:33 GMT
ENV TOMCAT_MAJOR=10
# Wed, 02 Feb 2022 07:38:34 GMT
ENV TOMCAT_VERSION=10.0.16
# Wed, 02 Feb 2022 07:38:35 GMT
ENV TOMCAT_SHA512=9b70f4db2c7b2efb5453cd581322b1137df7b6443acd6a8e278eaaf97de89c9ad0c7c7996a2d545ef1e4d965aca43c40d2b2c7d5e46b021695f87093143fbba2
# Wed, 02 Feb 2022 07:38:37 GMT
COPY dir:3d71aba491b1e7c5af1c2321875d02c3d93a3ece3b0c7496e00b7bef957ae4a7 in /usr/local/tomcat 
# Wed, 02 Feb 2022 07:38:44 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 07:38:45 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 02 Feb 2022 07:38:46 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 07:38:47 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20305b79e1520f1abaac4873914620f971be40e552579ba5d7dae3be52dd4f68`  
		Last Modified: Wed, 02 Feb 2022 05:06:28 GMT  
		Size: 24.8 MB (24762728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa60d6ad6ab0b8a49dad3a3c4fb5ed7f511c7af5551f18b190fbb633183e6d9`  
		Last Modified: Wed, 02 Feb 2022 05:06:55 GMT  
		Size: 40.8 MB (40769906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b7c09b7ae03343e3c1e143ec7d68f3a617c7874c33932c0c9335f9f88a1a9f`  
		Last Modified: Wed, 02 Feb 2022 05:06:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e570abd015fe209f7a092ea3eb23d92350d08d3e332a4959d21c5978d744a34`  
		Last Modified: Wed, 02 Feb 2022 08:19:17 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1a41b2879b95ed491559333700c259974a6e68bac2d6b9c219446ff4ab44fc`  
		Last Modified: Wed, 02 Feb 2022 08:19:18 GMT  
		Size: 12.6 MB (12592565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48898d7909366188d29155ad2b77e26d5be24c6f68310eff8d28520002a38205`  
		Last Modified: Wed, 02 Feb 2022 08:19:17 GMT  
		Size: 214.8 KB (214813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre8-temurin-focal` - linux; ppc64le

```console
$ docker pull tomcat@sha256:10662d67db9ddaff6da102269c5cc312decafe45d97c5784e15987471c7e4fc7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114184261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55b4ee604cea5502fde3e9bf98018e6ee8caadba68800e06d4b145a265120fc`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:45:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 05:48:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:48:47 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 02 Feb 2022 05:49:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 02 Feb 2022 05:49:51 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 05:49:59 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 02 Feb 2022 09:03:46 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 02 Feb 2022 09:03:50 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Feb 2022 09:03:55 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 02 Feb 2022 09:03:57 GMT
WORKDIR /usr/local/tomcat
# Wed, 02 Feb 2022 09:03:59 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 09:04:01 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 02 Feb 2022 09:04:04 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 02 Feb 2022 09:04:05 GMT
ENV TOMCAT_MAJOR=10
# Wed, 02 Feb 2022 09:04:07 GMT
ENV TOMCAT_VERSION=10.0.16
# Wed, 02 Feb 2022 09:04:09 GMT
ENV TOMCAT_SHA512=9b70f4db2c7b2efb5453cd581322b1137df7b6443acd6a8e278eaaf97de89c9ad0c7c7996a2d545ef1e4d965aca43c40d2b2c7d5e46b021695f87093143fbba2
# Wed, 02 Feb 2022 09:04:10 GMT
COPY dir:6da8f2051050be85f059c024081782a6f22a9d16975d224c081aec272179a2a5 in /usr/local/tomcat 
# Wed, 02 Feb 2022 09:04:27 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 09:04:43 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 02 Feb 2022 09:04:46 GMT
EXPOSE 8080
# Wed, 02 Feb 2022 09:04:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b628b171f10e336a4f91bbf963a6d636a2d90773ed7eef1ecafde5d9939c3c11`  
		Last Modified: Wed, 02 Feb 2022 05:57:19 GMT  
		Size: 26.6 MB (26643271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b575a12a35b9ef08e2b14d4755693c4abe080a1fd9113db75d7afc8af0a2ea`  
		Last Modified: Wed, 02 Feb 2022 05:57:50 GMT  
		Size: 41.2 MB (41162367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e120f90c634c0ae856cefb05c0fff297a6e3df94751cd737baa714cd5fef8e`  
		Last Modified: Wed, 02 Feb 2022 05:57:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5015285c546e9d057aa28e405e03c9bf16c1065b28da89d9e75ed8e323082f4`  
		Last Modified: Wed, 02 Feb 2022 10:09:52 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180a0ef7c633a5388a1b0752f08a6ad536bbf17324b37f997f207e9f6e5aa9c0`  
		Last Modified: Wed, 02 Feb 2022 10:09:54 GMT  
		Size: 12.6 MB (12615720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9ac90ac08d93b90b9029dcb600df8340d7422e2079114e8292776216bb2a86`  
		Last Modified: Wed, 02 Feb 2022 10:09:52 GMT  
		Size: 477.7 KB (477726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b870d784c0105db754e9ebfdd094bdae28b2d9f29435e131b3d32601449933`  
		Last Modified: Wed, 02 Feb 2022 10:09:52 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
