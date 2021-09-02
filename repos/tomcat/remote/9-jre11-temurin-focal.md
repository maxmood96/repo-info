## `tomcat:9-jre11-temurin-focal`

```console
$ docker pull tomcat@sha256:4f2d919ca4a641a9961a7c0b5c88b0fc3e8998d7b05c9cb0dec3fa3a3e93ae0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomcat:9-jre11-temurin-focal` - linux; amd64

```console
$ docker pull tomcat@sha256:b9f961aeb1308837b9abff457efc9a92758de843b475aeea340c981abb08a429
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100458791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782ae06f2bfe138fc545a724e5b3003ae0981cf22183ea746a06a2bd057196cf`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:55 GMT
ADD file:d2abf27fe2e8b0b5f4da68c018560c73e11c53098329246e3e6fe176698ef941 in / 
# Tue, 31 Aug 2021 01:20:56 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:26:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Aug 2021 03:31:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Sep 2021 23:20:01 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Wed, 01 Sep 2021 23:20:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='e813e270b7ea0a13f9c400ce5abd4cb811aacbd536b8909e6c7f0e346f78348c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 01 Sep 2021 23:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Sep 2021 23:20:06 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 01 Sep 2021 23:20:07 GMT
CMD ["jshell"]
# Thu, 02 Sep 2021 18:34:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 02 Sep 2021 18:34:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Sep 2021 18:34:22 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 02 Sep 2021 18:34:22 GMT
WORKDIR /usr/local/tomcat
# Thu, 02 Sep 2021 18:34:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 02 Sep 2021 18:34:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 02 Sep 2021 18:37:22 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 02 Sep 2021 18:37:22 GMT
ENV TOMCAT_MAJOR=9
# Thu, 02 Sep 2021 18:37:22 GMT
ENV TOMCAT_VERSION=9.0.52
# Thu, 02 Sep 2021 18:37:22 GMT
ENV TOMCAT_SHA512=35e007e8e30e12889da27f9c71a6f4997b9cb5023b703d99add5de9271828e7d8d4956bf34dd2f48c7c71b4f8480f318c9067a4cd2a6d76eaae466286db4897b
# Thu, 02 Sep 2021 18:37:23 GMT
COPY dir:36672f32f6f02d5df2571f1c7844604856e9dd4f3b96440a54a5a5240e80f729 in /usr/local/tomcat 
# Thu, 02 Sep 2021 18:37:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Sep 2021 18:37:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 02 Sep 2021 18:37:30 GMT
EXPOSE 8080
# Thu, 02 Sep 2021 18:37:30 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:35807b77a593c1147d13dc926a91dcc3015616ff7307cc30442c5a8e07546283`  
		Last Modified: Sat, 28 Aug 2021 03:03:19 GMT  
		Size: 28.6 MB (28570074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74df1ad422e5a232e54d515fb2475eee78b57b25d905611bbceb50f364c0150c`  
		Last Modified: Tue, 31 Aug 2021 03:33:27 GMT  
		Size: 16.0 MB (16032853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5a8bd09986af1be3541f004dc3b6de2b68025805ddc5061c6e931d5753fabb`  
		Last Modified: Wed, 01 Sep 2021 23:21:13 GMT  
		Size: 43.2 MB (43219895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201c9d5aa7daa900f24e40caeb4f77e8859e1595e499dde72c86d3d174ba3d69`  
		Last Modified: Wed, 01 Sep 2021 23:21:07 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27eac6dbabcf034882a8aa063c9c1b33f4319d9039706f32daab0b68f1c8877c`  
		Last Modified: Thu, 02 Sep 2021 18:49:12 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fdce5e66320a49291dbe2e929922a667f25feae7ec6dbe564cb12dd30765a0`  
		Last Modified: Thu, 02 Sep 2021 18:51:59 GMT  
		Size: 12.2 MB (12189946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc90b572df5704688899d261fd234f31a6a195d4c93ceaae0ed770d4071cadd`  
		Last Modified: Thu, 02 Sep 2021 18:51:58 GMT  
		Size: 445.6 KB (445564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1876780ea18df51fd9f71f10d335ddc7ce3b9d9b785e40b8301932413afe467`  
		Last Modified: Thu, 02 Sep 2021 18:51:58 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
