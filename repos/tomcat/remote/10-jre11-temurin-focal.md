## `tomcat:10-jre11-temurin-focal`

```console
$ docker pull tomcat@sha256:6f1c5ea2ed8e788dd28ddea92102630fa907256f99d26850782111572f8745c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; s390x

### `tomcat:10-jre11-temurin-focal` - linux; amd64

```console
$ docker pull tomcat@sha256:73d2b9d2cde12f8704c115665595e8b3dcbeb1df3b83738cc7aee9f549c49ef1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.8 MB (100803172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156b6099df73cdb8d641298192e6aa21b556887eeaad480906b3512f95d19139`
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
# Mon, 13 Sep 2021 18:21:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eebf9b6b515fd139d45410ea4a0e7c18f015acba41e677cd7a57d1fe7a553681';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='21129821a148503333dcc9868f04f3c971290c75f07ca384b1ab5d906901ea80';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x)          ESUM='17932e94e7daa84057e20f99536cc66ab5ff52637b50bd5c1dfdcc1853aad0a9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|x86_64)          ESUM='e813e270b7ea0a13f9c400ce5abd4cb811aacbd536b8909e6c7f0e346f78348c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 13 Sep 2021 18:21:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Sep 2021 18:21:22 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Mon, 13 Sep 2021 19:25:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 13 Sep 2021 19:25:58 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Sep 2021 19:25:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 13 Sep 2021 19:25:59 GMT
WORKDIR /usr/local/tomcat
# Mon, 13 Sep 2021 19:26:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 13 Sep 2021 19:26:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 13 Sep 2021 19:26:00 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Mon, 13 Sep 2021 19:26:00 GMT
ENV TOMCAT_MAJOR=10
# Mon, 13 Sep 2021 19:28:24 GMT
ENV TOMCAT_VERSION=10.0.10
# Mon, 13 Sep 2021 19:28:24 GMT
ENV TOMCAT_SHA512=3f6d5d292ab67348b3134c1013044c948caf5a4bf142b4e856b5ee63693a6e80994b0b4dbb3404d0fd3542fd6f7f52b4cbe404fc5a0f716ac98d68db879b7112
# Mon, 13 Sep 2021 19:28:25 GMT
COPY dir:8a15673607b4190c79234db303ef65d0bab8a883b284c8d661dc0a4632713849 in /usr/local/tomcat 
# Mon, 13 Sep 2021 19:28:29 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 13 Sep 2021 19:28:30 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 13 Sep 2021 19:28:31 GMT
EXPOSE 8080
# Mon, 13 Sep 2021 19:28:31 GMT
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
	-	`sha256:0cbfc14ccf6101c785c2d1ff53639357aedc16887c9c85b39529294a043a695e`  
		Last Modified: Mon, 13 Sep 2021 18:24:43 GMT  
		Size: 43.2 MB (43219906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a5d4f7a5417c56577d57524967f238c052385de0b5a61bf12826f50fedb77d`  
		Last Modified: Mon, 13 Sep 2021 18:24:36 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3361ef5865a4b8f2437560a6a94c7b32c21cad281c67446eac77081c6f8d437b`  
		Last Modified: Mon, 13 Sep 2021 19:47:11 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a321e5762a69a9a6c34d680eb2d2cf2694f2bf31c75554cf3958b1a6a6c867`  
		Last Modified: Mon, 13 Sep 2021 19:49:08 GMT  
		Size: 12.5 MB (12534315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bf1834255fe1ee6e7ab5417745436be73542712a01b7754884ef1da8317e72`  
		Last Modified: Mon, 13 Sep 2021 19:49:07 GMT  
		Size: 445.6 KB (445561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fef4ffb3800609ff023ce8e5c02ce273a2d4380ca3eaea49f9fc5a6b5422751`  
		Last Modified: Mon, 13 Sep 2021 19:49:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre11-temurin-focal` - linux; s390x

```console
$ docker pull tomcat@sha256:7286493dec3898a7a1b64c56b6c985bd75b8843701c2a96492cc8677b7c9b83e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93478244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb041c50f0dd43f7097997fb265d0aec2dc7e1972b8468e3beebcb6f99a1093`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Aug 2021 01:42:23 GMT
ADD file:979855f79ebaca36cc7878f71b2326f1cd189970fdb223b37cd64ee12d1c9a2b in / 
# Tue, 31 Aug 2021 01:42:27 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:07:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 13 Sep 2021 17:42:08 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 13 Sep 2021 17:42:11 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Mon, 13 Sep 2021 17:43:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eebf9b6b515fd139d45410ea4a0e7c18f015acba41e677cd7a57d1fe7a553681';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='21129821a148503333dcc9868f04f3c971290c75f07ca384b1ab5d906901ea80';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x)          ESUM='17932e94e7daa84057e20f99536cc66ab5ff52637b50bd5c1dfdcc1853aad0a9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|x86_64)          ESUM='e813e270b7ea0a13f9c400ce5abd4cb811aacbd536b8909e6c7f0e346f78348c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 13 Sep 2021 17:43:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Sep 2021 17:43:10 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 14 Sep 2021 17:44:53 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 14 Sep 2021 17:44:54 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Sep 2021 17:44:56 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 14 Sep 2021 17:44:56 GMT
WORKDIR /usr/local/tomcat
# Tue, 14 Sep 2021 17:44:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 14 Sep 2021 17:44:58 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 14 Sep 2021 17:44:58 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Tue, 14 Sep 2021 17:44:59 GMT
ENV TOMCAT_MAJOR=10
# Tue, 14 Sep 2021 17:48:26 GMT
ENV TOMCAT_VERSION=10.0.11
# Tue, 14 Sep 2021 17:48:27 GMT
ENV TOMCAT_SHA512=16e1879490bb0e5843059e3a475558f1990b03f897a7d5cce5788d6983598ec30cbf3749e30c18fb799f5068cab8407d04e9e6e9705700b152f90a3dc8bc0cb5
# Tue, 14 Sep 2021 17:48:29 GMT
COPY dir:f4b3dca862d4e57360f3ec3b850179eab9cd1897f85ddb53b8e2588ec7144e08 in /usr/local/tomcat 
# Tue, 14 Sep 2021 17:48:38 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 Sep 2021 17:48:41 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 14 Sep 2021 17:48:42 GMT
EXPOSE 8080
# Tue, 14 Sep 2021 17:48:43 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9fbf86d355c92d30b8de4c0360b0d79e1100e392d0885b6b5b302a1c3781dbf1`  
		Last Modified: Tue, 31 Aug 2021 01:44:13 GMT  
		Size: 27.1 MB (27127470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d20a826ef27dc1821c9889c4347bca43c74e64a47d57bbe597f7b8c77bde134`  
		Last Modified: Mon, 13 Sep 2021 17:44:19 GMT  
		Size: 15.7 MB (15741174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69890c40480bd5ace67afbce9e0f4219b07298930518dc2395ce89518d662dfd`  
		Last Modified: Mon, 13 Sep 2021 17:44:47 GMT  
		Size: 37.6 MB (37564520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc85b2408a63ded7d17a0a1cfa174d3225ffe11c36e50687dd8cab4b2ec3f22`  
		Last Modified: Mon, 13 Sep 2021 17:44:41 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0580832d6a4aef85ca2675531cc326a734a1c7ff6f08f80876af9a5d50d4fe89`  
		Last Modified: Tue, 14 Sep 2021 17:59:10 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5bc2610fb964e1330bc2f3bc5598d7c6acc6e60a01fa7872bb49eda599b1585`  
		Last Modified: Tue, 14 Sep 2021 18:00:21 GMT  
		Size: 12.6 MB (12597784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61baee8c537bc754a8b331827c8709da13c05e76bb35e7ec910ab0b21cc0d2b6`  
		Last Modified: Tue, 14 Sep 2021 18:00:20 GMT  
		Size: 446.8 KB (446836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae6684028ede37811e8a77d5d201a730f9cebfaa5eab83a553db1492c57de56`  
		Last Modified: Tue, 14 Sep 2021 18:00:21 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
