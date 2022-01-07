## `tomcat:8-jre17-temurin`

```console
$ docker pull tomcat@sha256:eeffa404027f789e46e9bb9e7cc6f6a6ad5b8735fe993fa6eab6f1fe3c78ab75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:8-jre17-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:e36c55841834a4e63cd962d19f20055116660f9ff36358f559e205571d169941
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115846688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23942d95ed9fd4ddf37f40501eeb9f99fd9660a1ccb9b6b1ba9fda56058c3f45`
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
# Fri, 07 Jan 2022 08:06:17 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 07 Jan 2022 08:06:17 GMT
ENV TOMCAT_MAJOR=8
# Fri, 07 Jan 2022 08:06:18 GMT
ENV TOMCAT_VERSION=8.5.73
# Fri, 07 Jan 2022 08:06:18 GMT
ENV TOMCAT_SHA512=4d33760d007acc5271ba0f946d2be96f6146d4632e411c9b72d351fc49d08355e8b84b051713a2f580e0f633cbe4409b7e9bb0e62f3af8d1094c6e4b3fdb96f0
# Fri, 07 Jan 2022 08:06:18 GMT
COPY dir:be128e411be3d76e0af0dc17fba549d5eda52d1a4a9ca84d1a67f0f8ed685732 in /usr/local/tomcat 
# Fri, 07 Jan 2022 08:06:23 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 08:06:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 07 Jan 2022 08:06:25 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 08:06:25 GMT
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
	-	`sha256:3169da77d2e6938dcc8bf82d8aa33a0bf5a24da86a36bc73fb75b970c4c442a2`  
		Last Modified: Fri, 07 Jan 2022 08:28:41 GMT  
		Size: 11.3 MB (11253772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113f4a0c181d190756ed393b7e95c524da8546ab83ea16d10606ebbf74706804`  
		Last Modified: Fri, 07 Jan 2022 08:28:40 GMT  
		Size: 454.9 KB (454907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17cb7f86b2a8900ce0b63d2b60ec845d37cbbb2da7960fffe0dfb816fb968537`  
		Last Modified: Fri, 07 Jan 2022 08:28:39 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre17-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:5b462c1c75ce2f811bde783322a8e8402914f5ea5a43d801de623a5bba71e89f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107647941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2190d3e2455e0f313eed3d7971d2560c6cc79d48196f9fe6531c59ac10acbed2`
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
# Fri, 07 Jan 2022 07:09:35 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 07 Jan 2022 07:09:35 GMT
ENV TOMCAT_MAJOR=8
# Fri, 07 Jan 2022 07:09:36 GMT
ENV TOMCAT_VERSION=8.5.73
# Fri, 07 Jan 2022 07:09:36 GMT
ENV TOMCAT_SHA512=4d33760d007acc5271ba0f946d2be96f6146d4632e411c9b72d351fc49d08355e8b84b051713a2f580e0f633cbe4409b7e9bb0e62f3af8d1094c6e4b3fdb96f0
# Fri, 07 Jan 2022 07:09:39 GMT
COPY dir:7580480c0d1e4ad90c345284b47fe4ec33631742a96274e42a228c224979b10a in /usr/local/tomcat 
# Fri, 07 Jan 2022 07:09:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 07:09:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 07 Jan 2022 07:09:53 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 07:09:54 GMT
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
	-	`sha256:b31f3e0f7849056e2d676b557d467e9950c3c43170ce964c51d28afee722a885`  
		Last Modified: Fri, 07 Jan 2022 07:39:41 GMT  
		Size: 11.2 MB (11199792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d08bafc12ffe700b3f637ef20c7b961d48c51116ad6da4f4b7ef0111d778e4`  
		Last Modified: Fri, 07 Jan 2022 07:39:37 GMT  
		Size: 431.3 KB (431289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06cd0541f90c7d53311d19ec997f6e6e0afd6cbe4e135c837a29c8b31ae59c4c`  
		Last Modified: Fri, 07 Jan 2022 07:39:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre17-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:d9347c9f807730a50d665afef411c6c07f07903e6f585b7e297d743225d23396
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113473654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3366e120964c6b886c46807f35b6bb5239d7b181e8cfcc5d66927dd7b988616f`
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
# Fri, 07 Jan 2022 05:31:25 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 07 Jan 2022 05:31:26 GMT
ENV TOMCAT_MAJOR=8
# Fri, 07 Jan 2022 05:31:27 GMT
ENV TOMCAT_VERSION=8.5.73
# Fri, 07 Jan 2022 05:31:28 GMT
ENV TOMCAT_SHA512=4d33760d007acc5271ba0f946d2be96f6146d4632e411c9b72d351fc49d08355e8b84b051713a2f580e0f633cbe4409b7e9bb0e62f3af8d1094c6e4b3fdb96f0
# Fri, 07 Jan 2022 05:31:30 GMT
COPY dir:7ca211e245d8a1374a792e58db4c26e93bcb5e1aba472b6b6c1ea6a035eaf40c in /usr/local/tomcat 
# Fri, 07 Jan 2022 05:31:36 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 05:31:38 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 07 Jan 2022 05:31:39 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 05:31:40 GMT
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
	-	`sha256:6a6213add7dc9dca7d824c6314aeac19fab5edc9d3e91e133abe9fecf45be246`  
		Last Modified: Fri, 07 Jan 2022 06:07:22 GMT  
		Size: 11.3 MB (11269401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c346e7b637876f10fc0db6d5f2ae6cba5eaa5d70200f9314aedf216dcef974`  
		Last Modified: Fri, 07 Jan 2022 06:07:21 GMT  
		Size: 217.5 KB (217535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre17-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:7fc06a500fe6872c8a895ba874d0c380aeadde74ba2b01547d27b173d9de3911
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121106794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1848efa062f630e9f850325dd2823d3e38fa5c744b5191548746f0652629accf`
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
# Fri, 07 Jan 2022 06:44:03 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 07 Jan 2022 06:44:05 GMT
ENV TOMCAT_MAJOR=8
# Fri, 07 Jan 2022 06:44:07 GMT
ENV TOMCAT_VERSION=8.5.73
# Fri, 07 Jan 2022 06:44:09 GMT
ENV TOMCAT_SHA512=4d33760d007acc5271ba0f946d2be96f6146d4632e411c9b72d351fc49d08355e8b84b051713a2f580e0f633cbe4409b7e9bb0e62f3af8d1094c6e4b3fdb96f0
# Fri, 07 Jan 2022 06:44:11 GMT
COPY dir:af65d304b865b8c7369f124efe60b71dbfccb293fedd3f784cb43d662962eaa1 in /usr/local/tomcat 
# Fri, 07 Jan 2022 06:44:25 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 06:44:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 07 Jan 2022 06:44:35 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 06:44:37 GMT
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
	-	`sha256:1507e607a4298e2b3c4b65d7f4f494911af1455a4729d7ba36c785a69056f847`  
		Last Modified: Fri, 07 Jan 2022 07:10:57 GMT  
		Size: 11.3 MB (11294260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195c6373af2e14f5b6a5c2161acce6553a4b0e6bca8d72abbc0598d8784a8912`  
		Last Modified: Fri, 07 Jan 2022 07:10:56 GMT  
		Size: 479.9 KB (479906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be877eef5795658b12edf0dea33422c10a2e91e923bee4671436b4cadae2e19c`  
		Last Modified: Fri, 07 Jan 2022 07:10:56 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre17-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:36bbe0e9ae909b5f77b6fd5d9d1df8018accb6aa76318a4e2c9645c1dbf39f19
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110374243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a456521a5f47137b3c6ab469beeb33e58e7b329a00e4d4d0dae0abe34f4065ba`
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
# Fri, 07 Jan 2022 03:44:09 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 07 Jan 2022 03:44:09 GMT
ENV TOMCAT_MAJOR=8
# Fri, 07 Jan 2022 03:44:09 GMT
ENV TOMCAT_VERSION=8.5.73
# Fri, 07 Jan 2022 03:44:09 GMT
ENV TOMCAT_SHA512=4d33760d007acc5271ba0f946d2be96f6146d4632e411c9b72d351fc49d08355e8b84b051713a2f580e0f633cbe4409b7e9bb0e62f3af8d1094c6e4b3fdb96f0
# Fri, 07 Jan 2022 03:44:09 GMT
COPY dir:f13b2753e2331904556bb27c1b6f245d647754065655a28a86c678c05fa2b200 in /usr/local/tomcat 
# Fri, 07 Jan 2022 03:44:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:44:15 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 07 Jan 2022 03:44:15 GMT
EXPOSE 8080
# Fri, 07 Jan 2022 03:44:15 GMT
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
	-	`sha256:8dba4b7524fcf820ff5dae878fc4ffd7013356844c3bc271d5edd904c7771452`  
		Last Modified: Fri, 07 Jan 2022 03:54:55 GMT  
		Size: 11.3 MB (11264324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d01351fabce8771f59bfefc5945874685e0f1ce58a27ae0c9b13a75ae392d3`  
		Last Modified: Fri, 07 Jan 2022 03:54:55 GMT  
		Size: 456.5 KB (456495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dee0967fb1b5a01ccd2d041b7a9edc65f9f3d0e5aa8f60566cfcf6f41a00adc`  
		Last Modified: Fri, 07 Jan 2022 03:54:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
