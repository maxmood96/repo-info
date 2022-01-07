## `tomcat:9-jre17-temurin`

```console
$ docker pull tomcat@sha256:4480559a793d7f187c0c6dd812da1617835414485f13ded2949f0f5153b7b658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:9-jre17-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:df8c6ea30fdb0a91eda46d3da03ee5a3e233391d9285b1187bf42c198abf7607
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116844978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0e916164f12a792ffa7dabad0422a857a29c80b7816d710c5200d29fa0651ee`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 04:41:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 07 Jan 2022 04:43:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3 binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 04:43:51 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Fri, 07 Jan 2022 04:44:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='851205c5036543cbcf1953c3f5768977b9efaf6b86c9fb5ec1b6cab01f781faf';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.1_12.tar.gz';          ;;        armhf|arm)          ESUM='e1d94e98c47f2530304eb187c74a3e3c1cf46ddb4d86c277edb1e499bb525fe1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_arm_linux_hotspot_17.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0e9eee4977e14edc14d0e2acb97cb413f4a769e2d855d02131af1ccd877779ff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.1_12.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ff88a8bcdaa8db788b463b14724460f68c4c70c80b86e556012521996281f4bf';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_s390x_linux_hotspot_17.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9d58cb741509a88e0ae33eb022334fb900b409b198eca6fe76246f0677b392ad';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_x64_linux_hotspot_17.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 07 Jan 2022 04:44:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jan 2022 04:44:16 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Fri, 07 Jan 2022 07:54:57 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 07 Jan 2022 07:54:57 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jan 2022 07:54:58 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 07 Jan 2022 07:54:58 GMT
WORKDIR /usr/local/tomcat
# Fri, 07 Jan 2022 07:54:59 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 07 Jan 2022 07:54:59 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 07 Jan 2022 08:02:00 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 07 Jan 2022 08:02:00 GMT
ENV TOMCAT_MAJOR=9
# Fri, 07 Jan 2022 08:02:00 GMT
ENV TOMCAT_VERSION=9.0.56
# Fri, 07 Jan 2022 08:02:00 GMT
ENV TOMCAT_SHA512=b4c2c85891e84f0fbd8fec889ef0890d68a2bfa53eb31d4d39fcf5758aa483694af7ac27533ea4bc3fc3fdae56f2fa9c018d4acf872574c0ec5e37bb443599ce
# Fri, 07 Jan 2022 08:02:01 GMT
COPY dir:3dc75beea9acfbba5663b299b44bd619b68145ac633a112abe10c952e279f86b in /usr/local/tomcat 
# Fri, 07 Jan 2022 08:02:05 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 08:02:07 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 07 Jan 2022 08:02:07 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 08:02:07 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524240b3a384126157616745e61cbaee5f26dca8b20949ee43cae04c6ad56470`  
		Last Modified: Fri, 07 Jan 2022 04:46:58 GMT  
		Size: 28.6 MB (28562705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:642e7b03f4098a1ce79830792565e89a8aa8b1cb93befc40cdd02602f650094d`  
		Last Modified: Fri, 07 Jan 2022 04:48:00 GMT  
		Size: 47.0 MB (47008417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba8b5fd190bce9a8de9d177074534178563d001f518bd28d7ed053277cd167c`  
		Last Modified: Fri, 07 Jan 2022 04:47:53 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b432f29209a577597ba4747e340d60dfe226b92b15238a3ca70745b8ab962e60`  
		Last Modified: Fri, 07 Jan 2022 08:18:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01559314945706e79561f756449398379dfc15f54472d3e84bd781576fb8b643`  
		Last Modified: Fri, 07 Jan 2022 08:25:07 GMT  
		Size: 12.3 MB (12252059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4118e192d13a6c25635f63b0ab61a74c88cbaf02284b908a572b762621d84d`  
		Last Modified: Fri, 07 Jan 2022 08:25:06 GMT  
		Size: 454.9 KB (454912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20c1b59d53d1131f6982909d4c57f8ba44b8ef3ac6f9bdf5426cf41894b24e4`  
		Last Modified: Fri, 07 Jan 2022 08:25:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre17-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:45f8a04908adbdd983f61ff709d3cf72935a27dc90bf63679ff30d0daaad71df
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108649247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f06eb521566385a02c82b45c1547be7d4cae1be16489b65d1fc5b14ff958e97`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 07 Jan 2022 02:26:25 GMT
ADD file:ac83e0dc7e48a0dc1805c0fd7b71b8eb119b3eeafd1fdcab93e11fbc9c0bcda0 in / 
# Fri, 07 Jan 2022 02:26:26 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:24:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 07 Jan 2022 03:28:48 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3 binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:29:37 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Fri, 07 Jan 2022 03:30:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='851205c5036543cbcf1953c3f5768977b9efaf6b86c9fb5ec1b6cab01f781faf';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.1_12.tar.gz';          ;;        armhf|arm)          ESUM='e1d94e98c47f2530304eb187c74a3e3c1cf46ddb4d86c277edb1e499bb525fe1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_arm_linux_hotspot_17.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0e9eee4977e14edc14d0e2acb97cb413f4a769e2d855d02131af1ccd877779ff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.1_12.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ff88a8bcdaa8db788b463b14724460f68c4c70c80b86e556012521996281f4bf';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_s390x_linux_hotspot_17.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9d58cb741509a88e0ae33eb022334fb900b409b198eca6fe76246f0677b392ad';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_x64_linux_hotspot_17.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 07 Jan 2022 03:30:42 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jan 2022 03:30:43 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Fri, 07 Jan 2022 06:47:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 07 Jan 2022 06:47:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jan 2022 06:47:29 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 07 Jan 2022 06:47:30 GMT
WORKDIR /usr/local/tomcat
# Fri, 07 Jan 2022 06:47:30 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 07 Jan 2022 06:47:31 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 07 Jan 2022 07:01:35 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 07 Jan 2022 07:01:36 GMT
ENV TOMCAT_MAJOR=9
# Fri, 07 Jan 2022 07:01:36 GMT
ENV TOMCAT_VERSION=9.0.56
# Fri, 07 Jan 2022 07:01:37 GMT
ENV TOMCAT_SHA512=b4c2c85891e84f0fbd8fec889ef0890d68a2bfa53eb31d4d39fcf5758aa483694af7ac27533ea4bc3fc3fdae56f2fa9c018d4acf872574c0ec5e37bb443599ce
# Fri, 07 Jan 2022 07:01:39 GMT
COPY dir:882f9cb4b2195a9e740d9a82a305c0e5ce66eb97ffae7193573e633c857337e9 in /usr/local/tomcat 
# Fri, 07 Jan 2022 07:01:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 07:01:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 07 Jan 2022 07:01:54 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 07:01:54 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9b8080fa0945580f29aa3abed4664f8ab849229eca04510b5d259a9e29616064`  
		Last Modified: Fri, 07 Jan 2022 02:30:39 GMT  
		Size: 24.1 MB (24064434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f39521c262a1f5c0297c778ca56dce4377cd3dad3269379a54e86c8e6316be`  
		Last Modified: Fri, 07 Jan 2022 03:37:15 GMT  
		Size: 27.4 MB (27368179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6214e85a71423c111a99d5b6a95a0d45da0b4a06fc32d216b4df28ee631ed502`  
		Last Modified: Fri, 07 Jan 2022 03:40:24 GMT  
		Size: 44.6 MB (44583787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e694d5a70c1dd6394cf003d100a576728ae1089165bbe266e9a08fb88eb9c7`  
		Last Modified: Fri, 07 Jan 2022 03:39:56 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd2c824c4d0d4595adb7d97b9ade5ed1d90d28123f238f99b9d732ecd9d97c5`  
		Last Modified: Fri, 07 Jan 2022 07:27:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520a6df1825630ec9a9bdb2b17b081bccc92204f673c5c2fdf0868d4d08117f7`  
		Last Modified: Fri, 07 Jan 2022 07:35:45 GMT  
		Size: 12.2 MB (12201084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd2defec3eee9527fc8f9a300c5b10b34bc9ee72d61a872e20c9d64b54fce6d`  
		Last Modified: Fri, 07 Jan 2022 07:35:41 GMT  
		Size: 431.3 KB (431304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16856b82531144e51c235492f9e4d12b99cca33a4324b06be3cfb6b0982c65bd`  
		Last Modified: Fri, 07 Jan 2022 07:35:40 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre17-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:11b0ae5690a693798bc8d63c223600f3491ba352d937a935f16bc5992ca6f23a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114471606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcabfce2b7c1b86dde656dd73b836181af25a71e02378d61d642190e96ce8092`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:45 GMT
ADD file:521a8ada4ac06e6f7720904486d481d216a8c3e08c0c7db1376c39a33e709668 in / 
# Fri, 07 Jan 2022 01:53:45 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:32:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 07 Jan 2022 02:35:11 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3 binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:35:44 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Fri, 07 Jan 2022 02:36:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='851205c5036543cbcf1953c3f5768977b9efaf6b86c9fb5ec1b6cab01f781faf';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.1_12.tar.gz';          ;;        armhf|arm)          ESUM='e1d94e98c47f2530304eb187c74a3e3c1cf46ddb4d86c277edb1e499bb525fe1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_arm_linux_hotspot_17.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0e9eee4977e14edc14d0e2acb97cb413f4a769e2d855d02131af1ccd877779ff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.1_12.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ff88a8bcdaa8db788b463b14724460f68c4c70c80b86e556012521996281f4bf';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_s390x_linux_hotspot_17.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9d58cb741509a88e0ae33eb022334fb900b409b198eca6fe76246f0677b392ad';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_x64_linux_hotspot_17.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 07 Jan 2022 02:36:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jan 2022 02:36:16 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Fri, 07 Jan 2022 05:12:16 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 07 Jan 2022 05:12:17 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jan 2022 05:12:18 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 07 Jan 2022 05:12:19 GMT
WORKDIR /usr/local/tomcat
# Fri, 07 Jan 2022 05:12:20 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 07 Jan 2022 05:12:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 07 Jan 2022 05:24:47 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 07 Jan 2022 05:24:47 GMT
ENV TOMCAT_MAJOR=9
# Fri, 07 Jan 2022 05:24:48 GMT
ENV TOMCAT_VERSION=9.0.56
# Fri, 07 Jan 2022 05:24:49 GMT
ENV TOMCAT_SHA512=b4c2c85891e84f0fbd8fec889ef0890d68a2bfa53eb31d4d39fcf5758aa483694af7ac27533ea4bc3fc3fdae56f2fa9c018d4acf872574c0ec5e37bb443599ce
# Fri, 07 Jan 2022 05:24:51 GMT
COPY dir:5a0892e6bacf3e77b9e4c3d09e9e9c90a7f4fc77b72bdb0347a53c9cb6268591 in /usr/local/tomcat 
# Fri, 07 Jan 2022 05:24:58 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 05:24:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 07 Jan 2022 05:25:00 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 05:25:01 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5f3d23ccb99f6c9462a15efcf35aef0863858073a06d56df671d0e791b26222a`  
		Last Modified: Fri, 07 Jan 2022 01:55:32 GMT  
		Size: 27.2 MB (27171074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4cc5324dc0c2bf6f5bc85f9784eb0512b2f0175a537dcb2b9dc380f681a325d`  
		Last Modified: Fri, 07 Jan 2022 02:39:34 GMT  
		Size: 29.4 MB (29377313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161ea062ff1bd87f97034e9d0adc89ff7255cb68e2fcd874750a50cb96e95cef`  
		Last Modified: Fri, 07 Jan 2022 02:40:50 GMT  
		Size: 45.4 MB (45438065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00a278478160419fd2197d9ca34d1971eca57ea08af2382c79ca69e700942f3`  
		Last Modified: Fri, 07 Jan 2022 02:40:43 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13604335b155739375f1be8d78e781ba6d593dad8b4b6fdae7525d9d2ff9556`  
		Last Modified: Fri, 07 Jan 2022 05:54:56 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3e02471c81d62d4e2582eb33f8b251a8ebbab4c3756067b41a97f3c355ae1e`  
		Last Modified: Fri, 07 Jan 2022 06:03:07 GMT  
		Size: 12.3 MB (12267355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3511115a899d1dd1bd299036c48d4ed2d2622f418ad1404e097b7e027af22043`  
		Last Modified: Fri, 07 Jan 2022 06:03:06 GMT  
		Size: 217.5 KB (217533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre17-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:f93d191eeab190678c4df93d44526bbc792f478b87930ca2430a746195148031
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122106341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3f40eec890ff19d0fb245da8dab984488a8ce42e6c54ef70770df0300b5b41`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 07 Jan 2022 02:20:15 GMT
ADD file:014236839eaee978894ae0bd6aecc246177a0a2c11af73f86d9cfafe5478ce18 in / 
# Fri, 07 Jan 2022 02:20:19 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:15:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 07 Jan 2022 03:20:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3 binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:21:22 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Fri, 07 Jan 2022 03:22:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='851205c5036543cbcf1953c3f5768977b9efaf6b86c9fb5ec1b6cab01f781faf';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.1_12.tar.gz';          ;;        armhf|arm)          ESUM='e1d94e98c47f2530304eb187c74a3e3c1cf46ddb4d86c277edb1e499bb525fe1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_arm_linux_hotspot_17.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0e9eee4977e14edc14d0e2acb97cb413f4a769e2d855d02131af1ccd877779ff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.1_12.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ff88a8bcdaa8db788b463b14724460f68c4c70c80b86e556012521996281f4bf';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_s390x_linux_hotspot_17.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9d58cb741509a88e0ae33eb022334fb900b409b198eca6fe76246f0677b392ad';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_x64_linux_hotspot_17.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 07 Jan 2022 03:22:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jan 2022 03:22:44 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Fri, 07 Jan 2022 06:07:50 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 07 Jan 2022 06:07:52 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jan 2022 06:07:56 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 07 Jan 2022 06:07:57 GMT
WORKDIR /usr/local/tomcat
# Fri, 07 Jan 2022 06:07:59 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 07 Jan 2022 06:08:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 07 Jan 2022 06:30:53 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 07 Jan 2022 06:30:55 GMT
ENV TOMCAT_MAJOR=9
# Fri, 07 Jan 2022 06:30:57 GMT
ENV TOMCAT_VERSION=9.0.56
# Fri, 07 Jan 2022 06:30:59 GMT
ENV TOMCAT_SHA512=b4c2c85891e84f0fbd8fec889ef0890d68a2bfa53eb31d4d39fcf5758aa483694af7ac27533ea4bc3fc3fdae56f2fa9c018d4acf872574c0ec5e37bb443599ce
# Fri, 07 Jan 2022 06:31:00 GMT
COPY dir:274c6942722a30234eea1579e9cda80bcdfd82bd9767ace4c5ff71101e48b772 in /usr/local/tomcat 
# Fri, 07 Jan 2022 06:31:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 06:31:22 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 07 Jan 2022 06:31:23 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 06:31:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e6e6dea5a8cc4bdc9e5e51e2bfa948159b69d5fbc2dca99bc41776fb04dab967`  
		Last Modified: Fri, 07 Jan 2022 02:22:43 GMT  
		Size: 33.3 MB (33286892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68048c5f723dff42c861f929c10dd67f192df5e872bf74f8d1bf6d2c67fb879`  
		Last Modified: Fri, 07 Jan 2022 03:26:29 GMT  
		Size: 31.1 MB (31123694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acade099d31fb09c8bd02031be342dd8f62ba9721977b5828f4ca9034ef598a0`  
		Last Modified: Fri, 07 Jan 2022 03:27:48 GMT  
		Size: 44.9 MB (44921582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cc774a15417da584a7a1ec6e6c016c4b9130722fa77d04fdf7d3b7f9b0abcc`  
		Last Modified: Fri, 07 Jan 2022 03:27:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1735bdf6d68b9a8eb3cfe4d426ee2cc342c573fefe25b517c207c66292385fd0`  
		Last Modified: Fri, 07 Jan 2022 07:01:08 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c97f1b03bacdfd6f1530d97fec681a9088bca81897876b5cee69d3f74de339a`  
		Last Modified: Fri, 07 Jan 2022 07:07:49 GMT  
		Size: 12.3 MB (12293820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61817c7b7f8a3bc52a79696625c3efd39b73995c35ad5e93181f40bfed9601f0`  
		Last Modified: Fri, 07 Jan 2022 07:07:48 GMT  
		Size: 479.9 KB (479891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8073cce24002c662ddee93b6612ffe589b832e0db021ae11ef742e8f3d1f95`  
		Last Modified: Fri, 07 Jan 2022 07:07:47 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre17-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:3928232df7388111467d2e78615fedf3e61f790350744454a551bcad3079d159
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111374671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e48ecba783ccfad704827ac6b828caf1fe9c7cae9c0ac846a8a2bdcac2e44ca8`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:20 GMT
ADD file:b6119f4fcd6a113749f515278b315ffd96aecce7006f086acb060f981e5c59db in / 
# Fri, 07 Jan 2022 01:42:22 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:15:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 07 Jan 2022 02:16:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3 binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:16:56 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Fri, 07 Jan 2022 02:17:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='851205c5036543cbcf1953c3f5768977b9efaf6b86c9fb5ec1b6cab01f781faf';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.1_12.tar.gz';          ;;        armhf|arm)          ESUM='e1d94e98c47f2530304eb187c74a3e3c1cf46ddb4d86c277edb1e499bb525fe1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_arm_linux_hotspot_17.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0e9eee4977e14edc14d0e2acb97cb413f4a769e2d855d02131af1ccd877779ff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.1_12.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ff88a8bcdaa8db788b463b14724460f68c4c70c80b86e556012521996281f4bf';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_s390x_linux_hotspot_17.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9d58cb741509a88e0ae33eb022334fb900b409b198eca6fe76246f0677b392ad';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jre_x64_linux_hotspot_17.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 07 Jan 2022 02:17:25 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jan 2022 02:17:25 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Fri, 07 Jan 2022 03:36:30 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 07 Jan 2022 03:36:30 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jan 2022 03:36:31 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 07 Jan 2022 03:36:31 GMT
WORKDIR /usr/local/tomcat
# Fri, 07 Jan 2022 03:36:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 07 Jan 2022 03:36:31 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 07 Jan 2022 03:41:31 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 07 Jan 2022 03:41:31 GMT
ENV TOMCAT_MAJOR=9
# Fri, 07 Jan 2022 03:41:31 GMT
ENV TOMCAT_VERSION=9.0.56
# Fri, 07 Jan 2022 03:41:31 GMT
ENV TOMCAT_SHA512=b4c2c85891e84f0fbd8fec889ef0890d68a2bfa53eb31d4d39fcf5758aa483694af7ac27533ea4bc3fc3fdae56f2fa9c018d4acf872574c0ec5e37bb443599ce
# Fri, 07 Jan 2022 03:41:32 GMT
COPY dir:11464a0d7f5482196b2d2343a5a3d1d1c42a453455aaa105f7c2dfbc8fcf1bdb in /usr/local/tomcat 
# Fri, 07 Jan 2022 03:41:37 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:41:38 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 07 Jan 2022 03:41:38 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 03:41:38 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6d200361446626b53394c2a1a520a74a1221795562eac9b318c58e0abe147e23`  
		Last Modified: Fri, 07 Jan 2022 01:44:09 GMT  
		Size: 27.1 MB (27120999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0b1f6cbaeb912a8e74f66e0ca6b10a5a4b7b36058d99aef3a3fa1261bc3a49`  
		Last Modified: Fri, 07 Jan 2022 02:19:03 GMT  
		Size: 27.9 MB (27942696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888aeea8565f5f74a68e902263202b02ce00eedf0fb8b4620a7193f6e37e47bb`  
		Last Modified: Fri, 07 Jan 2022 02:19:48 GMT  
		Size: 43.6 MB (43589266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54bcd02ceddb69f0a9f41d350289d4f1b69c94b2a72e23de866cc5568a98b69d`  
		Last Modified: Fri, 07 Jan 2022 02:19:42 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7ef74acfd7132ef4b02ac8014e42a7047063c26c2f1879d516ecde2d3df862`  
		Last Modified: Fri, 07 Jan 2022 03:50:22 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34d80d8f7bacfc12a751c7a7a774c6ee1c5e710f656c99e0414918d34c48053`  
		Last Modified: Fri, 07 Jan 2022 03:53:23 GMT  
		Size: 12.3 MB (12264747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c012b6f64f72a7e5cf49370683e9133ca63a6ea72c2794b497beec59db3d9f85`  
		Last Modified: Fri, 07 Jan 2022 03:53:22 GMT  
		Size: 456.5 KB (456500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170e092a5cc6aff929aec6077596f1a7461e06542998decf15688ab4a73afa3e`  
		Last Modified: Fri, 07 Jan 2022 03:53:22 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
