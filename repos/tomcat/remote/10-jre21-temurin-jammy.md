## `tomcat:10-jre21-temurin-jammy`

```console
$ docker pull tomcat@sha256:ba4db85f77e601be5c90d72d7516a67892fb68422759d496b0484a7c7455e459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:10-jre21-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:50d05d05b21b1f7439f1c0672d8e78616a6e3f8beb088664dd195a4431599e9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114678417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c782a7620a7000c77040e402c3b1cf44ce2e5f25dbacde85f3fe3fbc8911691`
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
# Fri, 16 Feb 2024 04:47:56 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 16 Feb 2024 04:47:56 GMT
ENV TOMCAT_MAJOR=10
# Fri, 16 Feb 2024 04:47:56 GMT
ENV TOMCAT_VERSION=10.1.18
# Fri, 16 Feb 2024 04:47:56 GMT
ENV TOMCAT_SHA512=56d1478501bd63945aae08d9f7c1fd37e14761dd9606a3bf5996870256b542b561a354fb89c4693c5695d0f13fa217028115b311d50b4ecec03acc7785006638
# Fri, 16 Feb 2024 04:47:57 GMT
COPY dir:eee50843381cfc8e87c0168fe5db70eae707d24c2687c688818a6168e4d3685e in /usr/local/tomcat 
# Fri, 16 Feb 2024 04:48:01 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:48:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 16 Feb 2024 04:48:03 GMT
EXPOSE 8080
# Fri, 16 Feb 2024 04:48:03 GMT
ENTRYPOINT []
# Fri, 16 Feb 2024 04:48:03 GMT
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
	-	`sha256:7283820b8d9d4886afa4ac8ab03b01416d6ac5f266b3d0a230a5a3dc7d9ac9fd`  
		Last Modified: Fri, 16 Feb 2024 05:01:19 GMT  
		Size: 12.3 MB (12326328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c755a26b6317b6db661abf89e72342bc69ef2e4178b817347a1548e51d9d1f8f`  
		Last Modified: Fri, 16 Feb 2024 05:01:19 GMT  
		Size: 458.6 KB (458644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d45fb19af332a887f9b0306bb4391aa200dd0f3ce2667e6f4ab6771e078832c`  
		Last Modified: Fri, 16 Feb 2024 05:01:18 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre21-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:2c70efa130dc9a0dbd89dd93892e218ddda1fd086b5072e1f2a9317fe81df4e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113192355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107d6424ebd43b40222f4754bf6fefee721dc9d61460d691ebb3696d48b86abe`
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
# Fri, 02 Feb 2024 03:49:15 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 02 Feb 2024 03:49:15 GMT
ENV TOMCAT_MAJOR=10
# Fri, 02 Feb 2024 03:49:15 GMT
ENV TOMCAT_VERSION=10.1.18
# Fri, 02 Feb 2024 03:49:15 GMT
ENV TOMCAT_SHA512=56d1478501bd63945aae08d9f7c1fd37e14761dd9606a3bf5996870256b542b561a354fb89c4693c5695d0f13fa217028115b311d50b4ecec03acc7785006638
# Fri, 02 Feb 2024 03:49:15 GMT
COPY dir:d9bbf00a68255af598f73fc7271320b1f1a7235a432c85329d1668d707ac0e6a in /usr/local/tomcat 
# Fri, 02 Feb 2024 03:49:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 03:49:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Feb 2024 03:49:20 GMT
EXPOSE 8080
# Fri, 02 Feb 2024 03:49:20 GMT
ENTRYPOINT []
# Fri, 02 Feb 2024 03:49:21 GMT
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
	-	`sha256:a29333cba14821719fcca3bd49b7ae1e20547b21584903ebec9b5ffb4f9b5c59`  
		Last Modified: Fri, 02 Feb 2024 04:10:34 GMT  
		Size: 12.3 MB (12327393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80ae2194dd678e7b7e36c38298d870bcfd8ef2354cc3703d720b61799589cca`  
		Last Modified: Fri, 02 Feb 2024 04:10:34 GMT  
		Size: 457.1 KB (457139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e713907a3947c34201615ba0985b772ff0df9e7f4b087f79304fd1457130ea4`  
		Last Modified: Fri, 02 Feb 2024 04:10:33 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre21-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:fd4f4931554df5af7d6b69f08f143fcb4b10a3308455d62c4ac8ac706ec43ae9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 MB (120985495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ef0dbbfd51ca26c8ff3fcb65126e1e65239ef71de0eec1b7fcbaf49baab864`
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
# Fri, 16 Feb 2024 04:54:35 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 16 Feb 2024 04:54:36 GMT
ENV TOMCAT_MAJOR=10
# Fri, 16 Feb 2024 04:54:36 GMT
ENV TOMCAT_VERSION=10.1.18
# Fri, 16 Feb 2024 04:54:37 GMT
ENV TOMCAT_SHA512=56d1478501bd63945aae08d9f7c1fd37e14761dd9606a3bf5996870256b542b561a354fb89c4693c5695d0f13fa217028115b311d50b4ecec03acc7785006638
# Fri, 16 Feb 2024 04:54:37 GMT
COPY dir:3af0db0830fee673b6dd078430ff425c5fe5dc3f56aee1fa5d3cc9eed7f90917 in /usr/local/tomcat 
# Fri, 16 Feb 2024 04:54:44 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:54:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 16 Feb 2024 04:54:47 GMT
EXPOSE 8080
# Fri, 16 Feb 2024 04:54:47 GMT
ENTRYPOINT []
# Fri, 16 Feb 2024 04:54:47 GMT
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
	-	`sha256:ffb658f33d1b5f39705e5e32f5135b758b4f0ad44dfd4b008cbb96b043b93a41`  
		Last Modified: Fri, 16 Feb 2024 05:19:15 GMT  
		Size: 12.3 MB (12339117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed86a00df932b57e78e5cfa168ce95aca703e9d9fc6638bef10317a1f03b53b`  
		Last Modified: Fri, 16 Feb 2024 05:19:14 GMT  
		Size: 489.8 KB (489750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f6432e4677adcc6f3b06fa61502e7caeba80e7b2e6d5458449ae4a353d6029`  
		Last Modified: Fri, 16 Feb 2024 05:19:14 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre21-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:413f5d07abcd6845aacc510888f2bfc3544e2d28351696419e5fb84b755e3da8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108550426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d794318db336041df20786064b9936b75e4705e7f46a436c1db6cd4bce24b7cd`
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
# Fri, 02 Feb 2024 08:14:01 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 02 Feb 2024 08:14:01 GMT
ENV TOMCAT_MAJOR=10
# Fri, 02 Feb 2024 08:14:02 GMT
ENV TOMCAT_VERSION=10.1.18
# Fri, 02 Feb 2024 08:14:02 GMT
ENV TOMCAT_SHA512=56d1478501bd63945aae08d9f7c1fd37e14761dd9606a3bf5996870256b542b561a354fb89c4693c5695d0f13fa217028115b311d50b4ecec03acc7785006638
# Fri, 02 Feb 2024 08:14:04 GMT
COPY dir:638eb0eb65880de081e64912b193c169737fb73366750869dd4ec50ff38bdc45 in /usr/local/tomcat 
# Fri, 02 Feb 2024 08:14:11 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 08:14:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Feb 2024 08:14:13 GMT
EXPOSE 8080
# Fri, 02 Feb 2024 08:14:13 GMT
ENTRYPOINT []
# Fri, 02 Feb 2024 08:14:14 GMT
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
	-	`sha256:e97b504f6f731136a84e12747db9ee4499388867fe69b2d85ffd5f0394bc7f87`  
		Last Modified: Fri, 02 Feb 2024 08:56:35 GMT  
		Size: 12.3 MB (12327705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ad0fa8be49ce953ee3607a87c0cb8889d8f7ac21ad641d53873ab7fa790a8a`  
		Last Modified: Fri, 02 Feb 2024 08:56:34 GMT  
		Size: 460.0 KB (459974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d79410a1cd2e79d4b71e07dd07f58145086237c6d258f9ba4d0c9b140167a175`  
		Last Modified: Fri, 02 Feb 2024 08:56:34 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
