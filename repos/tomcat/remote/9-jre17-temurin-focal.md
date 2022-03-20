## `tomcat:9-jre17-temurin-focal`

```console
$ docker pull tomcat@sha256:ff61109f4f49c8b165ceb328b539c9061b2dec2638630f59ebeb854def9d207a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:9-jre17-temurin-focal` - linux; amd64

```console
$ docker pull tomcat@sha256:c563c953aa6b3820203362d4f871e61371fcb3e655b98fa13beddbf71fffe425
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (108038486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f3ce82932d46462af483e8e17dedd5b1c1f2c6756a6131f438cbd0f06bd01c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 01:15:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 19 Mar 2022 01:18:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 01:19:21 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Sat, 19 Mar 2022 01:20:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6ef7a28d0d844fe347ab18f65a91db744547321fe8a101d883bd80722183ab64';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.2_8.tar.gz';          ;;        armhf|arm)          ESUM='4fd1d11f3008aba1c6c17e1d1c1cf15e2a54e68275ad0874b47a781eaf73450e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.2_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='089a940d0feb34e8095dede569492a5c4b1f082898ab02c39465fa76fe85a555';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.2_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='26a9b87d7abba7ea2d85f279b7b0109c1653fb3334871d5f3790e23b8d2b34e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.2_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='292ed702d95f5690e52e171afe9f3050b9d2fb803456b155c831735fad0f17c0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 19 Mar 2022 01:20:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 01:20:15 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Sun, 20 Mar 2022 11:06:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sun, 20 Mar 2022 11:06:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 20 Mar 2022 11:07:00 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sun, 20 Mar 2022 11:07:00 GMT
WORKDIR /usr/local/tomcat
# Sun, 20 Mar 2022 11:07:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sun, 20 Mar 2022 11:07:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sun, 20 Mar 2022 11:34:00 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sun, 20 Mar 2022 11:34:00 GMT
ENV TOMCAT_MAJOR=9
# Sun, 20 Mar 2022 11:34:01 GMT
ENV TOMCAT_VERSION=9.0.60
# Sun, 20 Mar 2022 11:34:01 GMT
ENV TOMCAT_SHA512=a4d43ac45f76e29d3dea23a2712c7570a11419aad7a1af2d1533454709c020b59666c7f9e063a77120224e0cbd4020cac06ca596dda7057cacb9a8a7e6d73eea
# Sun, 20 Mar 2022 11:34:01 GMT
COPY dir:092691d9b94cdda67b89d843fe47a63bfd575f3f897e029ba8a35272dda34560 in /usr/local/tomcat 
# Sun, 20 Mar 2022 11:34:05 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sun, 20 Mar 2022 11:34:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sun, 20 Mar 2022 11:34:07 GMT
EXPOSE 8080
# Sun, 20 Mar 2022 11:34:07 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7405b632dcc496229c61b8893b6d5aa4b72bc6af4eb9977d44655da5feea38`  
		Last Modified: Sat, 19 Mar 2022 01:23:55 GMT  
		Size: 19.8 MB (19772776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82681fa0d627df060af549399f38403e9c48355b357d16c4a9314b94831d2738`  
		Last Modified: Sat, 19 Mar 2022 03:04:50 GMT  
		Size: 47.0 MB (47038129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3425bfab69e804efa868275eb970fc581606d3d2a62df214de92e14f64f38328`  
		Last Modified: Sat, 19 Mar 2022 03:04:43 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd24b9ad3fe0d9737f78579d73fb1400f2355f0ff2c0027204a0d5213397a1a8`  
		Last Modified: Sun, 20 Mar 2022 12:06:34 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c728e8ea80ab5206c3da913e36e5379ac8013c662f94c4a0a1100e48c180a446`  
		Last Modified: Sun, 20 Mar 2022 12:20:36 GMT  
		Size: 12.2 MB (12212691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8e211e8a6ad70b3da2949ee2e582423eb70189f0b208990df067c416dd85a3`  
		Last Modified: Sun, 20 Mar 2022 12:20:34 GMT  
		Size: 448.5 KB (448521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b528fb7adf98637594046cc5d179ec90e2627957daa11b67a0ffd42635878d`  
		Last Modified: Sun, 20 Mar 2022 12:20:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre17-temurin-focal` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:37acf98e2d2fb6294d43042fdd926c89172ab98cc0f218fffe560d7d695d4401
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102013424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194fdca2680f65535fff3f235e408be4fc869bffd5e81dab0cb6a59180db2674`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 03 Mar 2022 21:21:31 GMT
ADD file:984d3d8b31abd025bb9be52f42d60245a76b1ee991f286db819ae204da45390c in / 
# Thu, 03 Mar 2022 21:21:32 GMT
CMD ["bash"]
# Fri, 04 Mar 2022 04:40:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 07 Mar 2022 20:01:28 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Mar 2022 20:02:12 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Mon, 07 Mar 2022 20:03:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6ef7a28d0d844fe347ab18f65a91db744547321fe8a101d883bd80722183ab64';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.2_8.tar.gz';          ;;        armhf|arm)          ESUM='4fd1d11f3008aba1c6c17e1d1c1cf15e2a54e68275ad0874b47a781eaf73450e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.2_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='089a940d0feb34e8095dede569492a5c4b1f082898ab02c39465fa76fe85a555';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.2_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='26a9b87d7abba7ea2d85f279b7b0109c1653fb3334871d5f3790e23b8d2b34e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.2_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='292ed702d95f5690e52e171afe9f3050b9d2fb803456b155c831735fad0f17c0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 07 Mar 2022 20:03:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Mar 2022 20:03:05 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Mon, 07 Mar 2022 20:57:55 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 07 Mar 2022 20:57:56 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Mar 2022 20:57:57 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 07 Mar 2022 20:57:58 GMT
WORKDIR /usr/local/tomcat
# Mon, 07 Mar 2022 20:57:58 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 07 Mar 2022 20:57:58 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 07 Mar 2022 21:12:29 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 07 Mar 2022 21:12:29 GMT
ENV TOMCAT_MAJOR=9
# Wed, 16 Mar 2022 00:16:01 GMT
ENV TOMCAT_VERSION=9.0.60
# Wed, 16 Mar 2022 00:16:01 GMT
ENV TOMCAT_SHA512=a4d43ac45f76e29d3dea23a2712c7570a11419aad7a1af2d1533454709c020b59666c7f9e063a77120224e0cbd4020cac06ca596dda7057cacb9a8a7e6d73eea
# Wed, 16 Mar 2022 00:16:04 GMT
COPY dir:5a6f7da7d92b5697c7d13f6ac5c3cdc44901d1e55f2aa531c0119f5f7a4ff105 in /usr/local/tomcat 
# Wed, 16 Mar 2022 00:16:15 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Mar 2022 00:16:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 16 Mar 2022 00:16:19 GMT
EXPOSE 8080
# Wed, 16 Mar 2022 00:16:20 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:12a77aaceb8aa1438ebb61cb4904d74fc225cfa20464a060980580674a0a31e9`  
		Last Modified: Thu, 03 Mar 2022 21:25:09 GMT  
		Size: 24.1 MB (24073718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72a7de35baa71c7eab0c19d4b3b81c8f5e7b807c9088977982926a9f3678ff1`  
		Last Modified: Mon, 07 Mar 2022 20:09:25 GMT  
		Size: 19.2 MB (19194475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4568ea7bcaa0a9dfa01125b71d1fc33b868323a4fea2fa8e1cd17053e325ec14`  
		Last Modified: Mon, 07 Mar 2022 20:12:39 GMT  
		Size: 44.6 MB (44611465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9150deb9b872f5d8bfefce0d406fcfe325ef05aec9b5e7fc4fab8af1997ad45`  
		Last Modified: Mon, 07 Mar 2022 20:12:10 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9078c1b52c4698e6e3d13529986ce55684818755960d41bb52049155dde2300`  
		Last Modified: Mon, 07 Mar 2022 21:39:40 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddeda1bbcb8cf3401f7ff505a72cfe469aa48ca09594f5e783ea48e1ad819ab2`  
		Last Modified: Wed, 16 Mar 2022 00:44:35 GMT  
		Size: 12.2 MB (12160435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba0c85102d55217a2cfa55fbe16ed79eb4c3e9bbf1afdfc8622805c1297c683`  
		Last Modified: Wed, 16 Mar 2022 00:44:31 GMT  
		Size: 2.0 MB (1972866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c183d8994708596bd63a2717fea60c87a76852f1f5bf6247afb0887d817bd5`  
		Last Modified: Wed, 16 Mar 2022 00:44:30 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre17-temurin-focal` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:11aad0ee76f3f455bef50d483b741dccbb8398c43f3b1f80c4a85a32d4a45f15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105595405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ae9cf16699b1fc54655b13c12aff8b9008e04363d5970dfc2309e28ee77b15`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:28:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 19 Mar 2022 15:30:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:30:40 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Sat, 19 Mar 2022 15:31:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6ef7a28d0d844fe347ab18f65a91db744547321fe8a101d883bd80722183ab64';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.2_8.tar.gz';          ;;        armhf|arm)          ESUM='4fd1d11f3008aba1c6c17e1d1c1cf15e2a54e68275ad0874b47a781eaf73450e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.2_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='089a940d0feb34e8095dede569492a5c4b1f082898ab02c39465fa76fe85a555';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.2_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='26a9b87d7abba7ea2d85f279b7b0109c1653fb3334871d5f3790e23b8d2b34e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.2_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='292ed702d95f5690e52e171afe9f3050b9d2fb803456b155c831735fad0f17c0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 19 Mar 2022 15:31:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 15:31:14 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Sat, 19 Mar 2022 22:43:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 19 Mar 2022 22:43:49 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 22:43:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 19 Mar 2022 22:43:51 GMT
WORKDIR /usr/local/tomcat
# Sat, 19 Mar 2022 22:43:52 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 19 Mar 2022 22:43:53 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 19 Mar 2022 23:07:32 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 19 Mar 2022 23:07:33 GMT
ENV TOMCAT_MAJOR=9
# Sat, 19 Mar 2022 23:07:34 GMT
ENV TOMCAT_VERSION=9.0.60
# Sat, 19 Mar 2022 23:07:35 GMT
ENV TOMCAT_SHA512=a4d43ac45f76e29d3dea23a2712c7570a11419aad7a1af2d1533454709c020b59666c7f9e063a77120224e0cbd4020cac06ca596dda7057cacb9a8a7e6d73eea
# Sat, 19 Mar 2022 23:07:37 GMT
COPY dir:38ec50d964135937be7bf6b627b55727de3df008b5646d7d39332b6f95788de2 in /usr/local/tomcat 
# Sat, 19 Mar 2022 23:07:43 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 23:07:45 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 19 Mar 2022 23:07:46 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 23:07:47 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d067b9022d6a81d16f23aca9c646f37e8ffcd5aa7fef5f2b4c1ba304068489c0`  
		Last Modified: Sat, 19 Mar 2022 15:34:43 GMT  
		Size: 20.5 MB (20499729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62a8b1891129f9fdd57b9e2d9cedba6575c6de7a1ea8d909f2fed4a68138db6`  
		Last Modified: Sat, 19 Mar 2022 15:35:58 GMT  
		Size: 45.5 MB (45484474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df17d9b1ffdfa6e33e08d7d667ebace63935e0bf75adc25efa367c3c33fcedf`  
		Last Modified: Sat, 19 Mar 2022 15:35:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f6857ec90bd9de57c9d8ab32dbaa6d549b23281b7f7b090b7a99afd3fe9a5f`  
		Last Modified: Sat, 19 Mar 2022 23:51:55 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eef243409c7175cf46a4067a634c5079b173f1086da4ada7dc119e07268d606`  
		Last Modified: Sun, 20 Mar 2022 00:01:35 GMT  
		Size: 12.2 MB (12229609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ffec4d311be9bd7c4b60d313f0812395b860521ec601d658b976d379d9d1a7`  
		Last Modified: Sun, 20 Mar 2022 00:01:38 GMT  
		Size: 211.7 KB (211711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre17-temurin-focal` - linux; ppc64le

```console
$ docker pull tomcat@sha256:88054a7fae80ad99a84e6d817de133501a01f175f77741de1349b9de243346e5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115412472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4daa14581678ab141145641773913efa9024c0bba0c120aaeb47a6ebbae3eade`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 03 Mar 2022 20:28:30 GMT
ADD file:039f04ac6c5dbbe3fb0a5eee16945cf7c5fb7565751d6bdf8ec0c1102798c1de in / 
# Thu, 03 Mar 2022 20:28:38 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 22:04:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 07 Mar 2022 19:30:41 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Mar 2022 19:32:34 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Mon, 07 Mar 2022 19:33:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6ef7a28d0d844fe347ab18f65a91db744547321fe8a101d883bd80722183ab64';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.2_8.tar.gz';          ;;        armhf|arm)          ESUM='4fd1d11f3008aba1c6c17e1d1c1cf15e2a54e68275ad0874b47a781eaf73450e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.2_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='089a940d0feb34e8095dede569492a5c4b1f082898ab02c39465fa76fe85a555';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.2_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='26a9b87d7abba7ea2d85f279b7b0109c1653fb3334871d5f3790e23b8d2b34e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.2_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='292ed702d95f5690e52e171afe9f3050b9d2fb803456b155c831735fad0f17c0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 07 Mar 2022 19:33:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Mar 2022 19:34:01 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Mon, 07 Mar 2022 20:44:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 07 Mar 2022 20:44:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Mar 2022 20:44:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 07 Mar 2022 20:44:19 GMT
WORKDIR /usr/local/tomcat
# Mon, 07 Mar 2022 20:44:23 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 07 Mar 2022 20:44:25 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 07 Mar 2022 21:18:29 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 07 Mar 2022 21:18:32 GMT
ENV TOMCAT_MAJOR=9
# Wed, 16 Mar 2022 01:55:42 GMT
ENV TOMCAT_VERSION=9.0.60
# Wed, 16 Mar 2022 01:55:46 GMT
ENV TOMCAT_SHA512=a4d43ac45f76e29d3dea23a2712c7570a11419aad7a1af2d1533454709c020b59666c7f9e063a77120224e0cbd4020cac06ca596dda7057cacb9a8a7e6d73eea
# Wed, 16 Mar 2022 01:55:48 GMT
COPY dir:12b8bfc0d42973bc4c09db5cb0a2aede6d0f1a9ddc4ecf239e34ce817e42c9c2 in /usr/local/tomcat 
# Wed, 16 Mar 2022 01:56:13 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Mar 2022 01:56:26 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 16 Mar 2022 01:56:29 GMT
EXPOSE 8080
# Wed, 16 Mar 2022 01:56:32 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a16b43de69d1e799ea2cb675e7e605db0ff3a8d692fd326fbde80a370e0676d5`  
		Last Modified: Thu, 03 Mar 2022 20:33:55 GMT  
		Size: 33.3 MB (33292195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dfe83d48d12b5f1315927dd21902bee72f1d10516a8c8d635cf7cc1d4768127`  
		Last Modified: Mon, 07 Mar 2022 19:38:25 GMT  
		Size: 21.7 MB (21691309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e46ee7aa9ebd09a8132e22537cff17cbb877993fde85cffcaf08ef4a70fb069`  
		Last Modified: Mon, 07 Mar 2022 19:39:48 GMT  
		Size: 45.6 MB (45621129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f41103b113a7f5af0786eff4ace385d6e1185e028a971784998649b8811cae1`  
		Last Modified: Mon, 07 Mar 2022 19:39:40 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1ac6a907508e47aa40dc1b89a996459f151716fdc00c2f4972d6c0411fa57b`  
		Last Modified: Mon, 07 Mar 2022 22:01:00 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83fe1d632f6f3d866b331dd34e0f407badf6ecde790b8d72a77986100f50c019`  
		Last Modified: Wed, 16 Mar 2022 02:30:51 GMT  
		Size: 12.3 MB (12256216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b664128deb7bc3a1fc13dcc3af608cb7979c9022214173411634746684477ec1`  
		Last Modified: Wed, 16 Mar 2022 02:30:50 GMT  
		Size: 2.6 MB (2551158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45d9efe78751fedc9f30f29dbcf7e151ac4e57c158504b3dc96fbfc161c9973`  
		Last Modified: Wed, 16 Mar 2022 02:30:49 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre17-temurin-focal` - linux; s390x

```console
$ docker pull tomcat@sha256:a6c31fa03b2ce07976f188d0451dbf7c936fc0348d745e1dba4fdbb362dfe400
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102612572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6927954ff2399c5f606a312880347b3b3b7ae19392d726613bab0e4006e9b14`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:14 GMT
ADD file:5827631949b30d4d05b5515208aedd6d4bc801d2243920cc4fb78e45d0b92bea in / 
# Fri, 18 Mar 2022 00:37:16 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:43:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Mar 2022 17:54:47 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:55:08 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Fri, 18 Mar 2022 17:55:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6ef7a28d0d844fe347ab18f65a91db744547321fe8a101d883bd80722183ab64';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.2_8.tar.gz';          ;;        armhf|arm)          ESUM='4fd1d11f3008aba1c6c17e1d1c1cf15e2a54e68275ad0874b47a781eaf73450e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.2_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='089a940d0feb34e8095dede569492a5c4b1f082898ab02c39465fa76fe85a555';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.2_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='26a9b87d7abba7ea2d85f279b7b0109c1653fb3334871d5f3790e23b8d2b34e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.2_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='292ed702d95f5690e52e171afe9f3050b9d2fb803456b155c831735fad0f17c0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Mar 2022 17:55:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Mar 2022 17:55:34 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Sat, 19 Mar 2022 04:45:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 19 Mar 2022 04:45:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 04:45:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 19 Mar 2022 04:45:04 GMT
WORKDIR /usr/local/tomcat
# Sat, 19 Mar 2022 04:45:04 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 19 Mar 2022 04:45:04 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 19 Mar 2022 04:53:58 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 19 Mar 2022 04:53:58 GMT
ENV TOMCAT_MAJOR=9
# Sat, 19 Mar 2022 04:53:58 GMT
ENV TOMCAT_VERSION=9.0.60
# Sat, 19 Mar 2022 04:53:58 GMT
ENV TOMCAT_SHA512=a4d43ac45f76e29d3dea23a2712c7570a11419aad7a1af2d1533454709c020b59666c7f9e063a77120224e0cbd4020cac06ca596dda7057cacb9a8a7e6d73eea
# Sat, 19 Mar 2022 04:53:58 GMT
COPY dir:4152731afc7a8b46fc8d45acbc6463c548d865dd441e3414c84f51887784133b in /usr/local/tomcat 
# Sat, 19 Mar 2022 04:54:03 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 04:54:04 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 19 Mar 2022 04:54:04 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 04:54:04 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:709bbd04f56c5b854c32271f7441419f9a84086a0425b65a4bf8e7bb6e6adead`  
		Last Modified: Fri, 18 Mar 2022 00:38:44 GMT  
		Size: 27.1 MB (27084832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1025d20d5e077c01b865d1fb9746214badd64b62f8b36506a4db3ffc0037efc9`  
		Last Modified: Fri, 18 Mar 2022 17:57:06 GMT  
		Size: 19.2 MB (19234944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b40d870a88c487f3a4b6725b2761dcea303602085f770d1d71ad82cf83ef6d`  
		Last Modified: Fri, 18 Mar 2022 17:57:51 GMT  
		Size: 43.6 MB (43616304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2515ed2c2179e9ce3b607b95a5cbac515f9414c11eb77275c71090e001e89387`  
		Last Modified: Fri, 18 Mar 2022 17:57:45 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a766aea551bd3a32189214521e8486b5d6c2b90dcc74441c9a66420f130124ea`  
		Last Modified: Sat, 19 Mar 2022 05:14:22 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e33d0a253654e35b1a995c3911a37683384536c83378b5adff564d47c6ec9e`  
		Last Modified: Sat, 19 Mar 2022 05:17:15 GMT  
		Size: 12.2 MB (12225878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ab2063893917e764bbd463f0de7fb86dd3b865968b377f5ba0ce039c9e6fc5`  
		Last Modified: Sat, 19 Mar 2022 05:17:15 GMT  
		Size: 450.2 KB (450152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2014919c9d09b317234e650137e4f3ab97ddafda17018e99051ad347e28180bf`  
		Last Modified: Sat, 19 Mar 2022 05:17:14 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
