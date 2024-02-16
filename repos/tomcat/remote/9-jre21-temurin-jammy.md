## `tomcat:9-jre21-temurin-jammy`

```console
$ docker pull tomcat@sha256:afb1ff074743a0ce4b40bd0e6c30cc864939a3916aba7a242874d83f79802594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:9-jre21-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:e4da50cfcedd1a333c16c66814c439f79b7652ca1ee491d5b4b90630fec20a18
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114758006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1a661f93f8cb4d303f55c88ded64f1723393b5d52d0bc069c26ff7f2fee67b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 01:38:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 01:38:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 01:38:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 01:40:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 01:41:11 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Fri, 16 Feb 2024 01:41:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='64c78854184c92a4da5cda571c8e357043bfaf03a03434eef58550cc3410d8a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='51141204fe01a9f9dd74eab621d5eca7511eac67315c9975dbde5f2625bdca55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_x64_linux_hotspot_21.0.2_13.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='caaf48e50787b80b810dc08ee91bd4ffe0d0696bd14906a92f05bf8c14aabb22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.2_13.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ff8191fa5b23a175932e7f4fab10a6e8df61fd71b6529c7d21451c81e82f8d55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_s390x_linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 01:41:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 01:41:36 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 01:41:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:47:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Feb 2024 04:47:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 04:47:03 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 16 Feb 2024 04:47:03 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Feb 2024 04:47:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2024 04:47:04 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2024 04:50:34 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 16 Feb 2024 04:50:34 GMT
ENV TOMCAT_MAJOR=9
# Fri, 16 Feb 2024 04:50:34 GMT
ENV TOMCAT_VERSION=9.0.85
# Fri, 16 Feb 2024 04:50:34 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Fri, 16 Feb 2024 04:50:35 GMT
COPY dir:e0ae0af42f3c8c23193a234480e5132b6b37ca32a891fe9de5cfe4c3725f29df in /usr/local/tomcat 
# Fri, 16 Feb 2024 04:50:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:50:41 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 16 Feb 2024 04:50:41 GMT
EXPOSE 8080
# Fri, 16 Feb 2024 04:50:41 GMT
ENTRYPOINT []
# Fri, 16 Feb 2024 04:50:41 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f947fdc0fc4be68d9f9c4c3912a92df875230cdd8267c01077167a69114f54`  
		Last Modified: Fri, 16 Feb 2024 01:44:10 GMT  
		Size: 17.5 MB (17458484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8dcaf76fb72d312c4076bf140abb4c835600feb4f9b695a3506dec3929cf11`  
		Last Modified: Fri, 16 Feb 2024 01:45:24 GMT  
		Size: 54.0 MB (53983687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18823a7d9420d2f06153c34914d95ae27f6217d9d580b57a46d0c20391756f6d`  
		Last Modified: Fri, 16 Feb 2024 01:45:17 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ed966fe6f457a54ffe5569aba574c92d4768658ac44d0c1a16f171fa7da5a`  
		Last Modified: Fri, 16 Feb 2024 01:45:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f439351604da7cb5d48ff9887304976678cd7f98e1e313eeb57d4f64375d4511`  
		Last Modified: Fri, 16 Feb 2024 05:00:15 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b2848b6a0d3b67a9b872251a522e6d7d489a76a8b3142bac087983f893274f`  
		Last Modified: Fri, 16 Feb 2024 05:04:18 GMT  
		Size: 12.4 MB (12405926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7acd4206209ae21ae0d29878fb95e9c453b4a80a85c26dd67599bea418e498`  
		Last Modified: Fri, 16 Feb 2024 05:04:17 GMT  
		Size: 458.6 KB (458635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3efb6cf55472fbd04c25409765792851149875415ad721706bb72cad1908e1`  
		Last Modified: Fri, 16 Feb 2024 05:04:17 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre21-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:2555e9bc1a1bea9ffd6559107c5ac1d45a2f8be7424bc217a3a24c74ff96d869
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.3 MB (113278918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5c0862883291be3636b62e59fc39acfdf5e66ecef817802f1a63d7c4a9ba32`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:10:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 02:10:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 02:10:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 02:12:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:12:42 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Fri, 02 Feb 2024 02:13:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='64c78854184c92a4da5cda571c8e357043bfaf03a03434eef58550cc3410d8a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='51141204fe01a9f9dd74eab621d5eca7511eac67315c9975dbde5f2625bdca55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_x64_linux_hotspot_21.0.2_13.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='caaf48e50787b80b810dc08ee91bd4ffe0d0696bd14906a92f05bf8c14aabb22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.2_13.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ff8191fa5b23a175932e7f4fab10a6e8df61fd71b6529c7d21451c81e82f8d55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_s390x_linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Feb 2024 02:13:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 02 Feb 2024 02:13:04 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 02:13:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 03:48:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 02 Feb 2024 03:48:32 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 03:48:32 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 02 Feb 2024 03:48:32 GMT
WORKDIR /usr/local/tomcat
# Fri, 02 Feb 2024 03:48:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 02 Feb 2024 03:48:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 02 Feb 2024 03:51:23 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 02 Feb 2024 03:51:23 GMT
ENV TOMCAT_MAJOR=9
# Fri, 02 Feb 2024 03:51:24 GMT
ENV TOMCAT_VERSION=9.0.85
# Fri, 02 Feb 2024 03:51:24 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Fri, 02 Feb 2024 03:51:24 GMT
COPY dir:aee949b91ae15e050e4867b6f3825a715122bd6d045bd86ea95dc75c223fbbf1 in /usr/local/tomcat 
# Fri, 02 Feb 2024 03:51:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 03:51:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Feb 2024 03:51:29 GMT
EXPOSE 8080
# Fri, 02 Feb 2024 03:51:29 GMT
ENTRYPOINT []
# Fri, 02 Feb 2024 03:51:29 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d031894e4c0411af099ca88f2f4707adffb7144d8d3dc5d40457cededf240b5`  
		Last Modified: Fri, 02 Feb 2024 02:16:39 GMT  
		Size: 18.9 MB (18860666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ec56812816eb5b800ddbed6fc77aa7c1239c3270dcda3e7561d6afca1a488a`  
		Last Modified: Fri, 02 Feb 2024 02:18:06 GMT  
		Size: 53.1 MB (53145860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2885b8e0cbb21a35184c7a98d90254938391348fb7de140e1ff3d36fb76d0a66`  
		Last Modified: Fri, 02 Feb 2024 02:17:59 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a2405cb3e32cce19619b7e2ac85ada67ee52acdfa926375210e07cb5f83e86`  
		Last Modified: Fri, 02 Feb 2024 02:17:59 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea160b41f43522bab1439d798de849262c27030b12b8ec0b998780484a58b49`  
		Last Modified: Fri, 02 Feb 2024 04:09:32 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee806c3c2f52b643433879b23b76600ec9668f4106cdb91adfa83e36843a5886`  
		Last Modified: Fri, 02 Feb 2024 04:13:37 GMT  
		Size: 12.4 MB (12413930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83c984da69bd531e096f5187a8f4cae43d819f95e1bfbe6f37705de1678c653`  
		Last Modified: Fri, 02 Feb 2024 04:13:36 GMT  
		Size: 457.2 KB (457164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c50966cbb2e9f4c746388fe02148c3198f20afe5b2d392f80c74338d715d488`  
		Last Modified: Fri, 02 Feb 2024 04:13:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre21-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:2c43a3de50dbb3e3bbd45bb6acef5fee28041b43d11683000a6832af4aea9449
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121080223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f966670ddf75178045f1f3ead9d46f46b8350c845c5a1f52466d4c171b4d43`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:12 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:17 GMT
ADD file:c082e39391784606dcfb3aa7298125fa9e8fe08e83ff006496eac650ad180c35 in / 
# Tue, 13 Feb 2024 10:06:17 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:01:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 03:01:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 03:01:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 03:03:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:04:49 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Fri, 16 Feb 2024 03:05:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='64c78854184c92a4da5cda571c8e357043bfaf03a03434eef58550cc3410d8a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='51141204fe01a9f9dd74eab621d5eca7511eac67315c9975dbde5f2625bdca55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_x64_linux_hotspot_21.0.2_13.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='caaf48e50787b80b810dc08ee91bd4ffe0d0696bd14906a92f05bf8c14aabb22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.2_13.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ff8191fa5b23a175932e7f4fab10a6e8df61fd71b6529c7d21451c81e82f8d55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_s390x_linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 03:05:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 03:05:40 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 03:05:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Feb 2024 04:52:31 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Feb 2024 04:52:32 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 04:52:33 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 16 Feb 2024 04:52:33 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Feb 2024 04:52:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2024 04:52:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2024 05:00:20 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 16 Feb 2024 05:00:21 GMT
ENV TOMCAT_MAJOR=9
# Fri, 16 Feb 2024 05:00:21 GMT
ENV TOMCAT_VERSION=9.0.85
# Fri, 16 Feb 2024 05:00:22 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Fri, 16 Feb 2024 05:00:22 GMT
COPY dir:6a051cf53fdf82b3d4f65f462d842440102dd116f1076cdf941adf3633c3cc74 in /usr/local/tomcat 
# Fri, 16 Feb 2024 05:00:29 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:00:32 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 16 Feb 2024 05:00:33 GMT
EXPOSE 8080
# Fri, 16 Feb 2024 05:00:33 GMT
ENTRYPOINT []
# Fri, 16 Feb 2024 05:00:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:fb95b1654dd508e6f2d1e7103bcd3af75a00fa6826603132794816af5418de7c`  
		Last Modified: Fri, 16 Feb 2024 03:06:52 GMT  
		Size: 35.6 MB (35628838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc402319b10feb1c6820fa2bc7cfba7869a3473e27191ab283db519e7e6da50`  
		Last Modified: Fri, 16 Feb 2024 03:08:21 GMT  
		Size: 18.7 MB (18726189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1283d08861f645030f16decddb00e040cd3c9d5483c5a525cc76f1d289d461b9`  
		Last Modified: Fri, 16 Feb 2024 03:09:41 GMT  
		Size: 53.8 MB (53800406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01d1be39758afb234453ab063da226fef5ffb3df3e16620446b0f7219ff9689`  
		Last Modified: Fri, 16 Feb 2024 03:09:33 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a9c9c1dc7209304e1b2dedb5024660a3eeda46b2668ccf6537bca8e28cdfe0`  
		Last Modified: Fri, 16 Feb 2024 03:09:33 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a862fd03d7be4030d03e715277cb4eb74dc06586c207a4c383b9e47981f47867`  
		Last Modified: Fri, 16 Feb 2024 05:18:05 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b7d29c4a2acae6362aa8b7b452c224e782028706c53b8f1b584601c5e90f11`  
		Last Modified: Fri, 16 Feb 2024 05:22:45 GMT  
		Size: 12.4 MB (12433839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c4d7e7cfd97d5523e66369fd1cfb0b13eb582a3e03ea0ff1653c19dfab2463`  
		Last Modified: Fri, 16 Feb 2024 05:22:43 GMT  
		Size: 489.8 KB (489755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a2174a5ccd189ed2f04401f3e8eaf90bfd469c14b825257a376759b20a95ac`  
		Last Modified: Fri, 16 Feb 2024 05:22:43 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre21-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:d83d482bedb70824994bbac5a2664fb8538f48701b81d7d8163a5edfa274f223
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108623460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef52814463813d69db09ec8a801a44845488a29c9cc4439b0d869b721e8f688`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 25 Jan 2024 18:07:14 GMT
ARG RELEASE
# Thu, 25 Jan 2024 18:07:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 18:07:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 18:07:14 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 18:07:16 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Thu, 25 Jan 2024 18:07:16 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:52:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 01:52:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 01:52:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 02:01:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:07:48 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Fri, 02 Feb 2024 02:10:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='64c78854184c92a4da5cda571c8e357043bfaf03a03434eef58550cc3410d8a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='51141204fe01a9f9dd74eab621d5eca7511eac67315c9975dbde5f2625bdca55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_x64_linux_hotspot_21.0.2_13.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='caaf48e50787b80b810dc08ee91bd4ffe0d0696bd14906a92f05bf8c14aabb22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.2_13.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ff8191fa5b23a175932e7f4fab10a6e8df61fd71b6529c7d21451c81e82f8d55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_s390x_linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Feb 2024 02:10:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 02 Feb 2024 02:10:52 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 02:10:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 08:10:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 02 Feb 2024 08:10:54 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 08:10:55 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 02 Feb 2024 08:10:55 GMT
WORKDIR /usr/local/tomcat
# Fri, 02 Feb 2024 08:10:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 02 Feb 2024 08:10:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 02 Feb 2024 08:23:49 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 02 Feb 2024 08:23:49 GMT
ENV TOMCAT_MAJOR=9
# Fri, 02 Feb 2024 08:23:49 GMT
ENV TOMCAT_VERSION=9.0.85
# Fri, 02 Feb 2024 08:23:50 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Fri, 02 Feb 2024 08:23:50 GMT
COPY dir:22f02b44871f951af6b6d4a4041c7baa94f65ea82421991a37c5020d617db233 in /usr/local/tomcat 
# Fri, 02 Feb 2024 08:23:54 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 08:23:55 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Feb 2024 08:23:55 GMT
EXPOSE 8080
# Fri, 02 Feb 2024 08:23:56 GMT
ENTRYPOINT []
# Fri, 02 Feb 2024 08:23:56 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4d63bfd51bdce6fd8dfe83946feba0ea66b3823f4955c098602769d1933dfb1a`  
		Last Modified: Fri, 02 Feb 2024 00:42:52 GMT  
		Size: 28.7 MB (28655632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec92f300c69dd15c23ba2afafe2c0d431cee8fcae0a0a951bc7ea9d2864f204`  
		Last Modified: Fri, 02 Feb 2024 02:15:44 GMT  
		Size: 17.3 MB (17261495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886833f70ff04666c5d5a08525349a800acddeadd53b298b42c4a11bb760bdab`  
		Last Modified: Fri, 02 Feb 2024 02:16:57 GMT  
		Size: 49.8 MB (49844428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c834eea3525ae6005d2da7bb7518f920b37b58223ea71e68d2077276dc369b53`  
		Last Modified: Fri, 02 Feb 2024 02:16:50 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27024fdbe28272a6972d0701d6459e44df945f636b112020beab91f3a0a5dfd0`  
		Last Modified: Fri, 02 Feb 2024 02:16:50 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b58ef73fa5c8abbf0cd916904a3f0e5fe3cf0f9d887990ed96ab739692c3cf7`  
		Last Modified: Fri, 02 Feb 2024 08:55:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e6759f4452ea365d94690cf6ba6f7d2022fe24cb379a051c50c5afd7989c7f`  
		Last Modified: Fri, 02 Feb 2024 08:58:20 GMT  
		Size: 12.4 MB (12400746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7326db76589a79d3a6e134a6c8f0286ce7a7081d14ef841e4150184b14aea9f3`  
		Last Modified: Fri, 02 Feb 2024 08:58:19 GMT  
		Size: 460.0 KB (459968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a109dd06f5d6c181ab34e1aa3ef023536a2bbad9dbcf44734af4245da03b8c40`  
		Last Modified: Fri, 02 Feb 2024 08:58:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
