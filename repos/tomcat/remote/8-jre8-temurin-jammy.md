## `tomcat:8-jre8-temurin-jammy`

```console
$ docker pull tomcat@sha256:b43efe845cd9467faa4cee351c158567d01d959e890e5e48d1e2753f6cbb3648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `tomcat:8-jre8-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:5dcfb1cdc8d1201748302de7e3b1cb43dab57546b16368cbab7f4b76a888f448
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97109603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceac099204f43b122a8749c79d10548b9b8e563a497bd7b6719f52b97ce1e43a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 01:58:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 01:58:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 01:58:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Dec 2023 01:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 01:58:34 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Sat, 02 Dec 2023 01:58:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='37b997f12cd572da979283fccafec9ba903041a209605b50fcb46cc34f1a9917';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u392b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='91d31027da0d985be3549714389593d9e0da3da5057d87e3831c7c538b9a2a0f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_x64_linux_hotspot_8u392b08.tar.gz';          ;;        armhf|arm)          ESUM='877953bfabcdbcd000c11364d806456ca579a921085de2ca942280ebe168cac2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_arm_linux_hotspot_8u392b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='0ecb0aeb54fb9d3c9e1a7ea411490127e8e298d93219fafc4dd6051a5b74671f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u392b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Sat, 02 Dec 2023 01:59:00 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete."
# Sat, 02 Dec 2023 01:59:00 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 02 Dec 2023 01:59:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Dec 2023 08:25:43 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 02 Dec 2023 08:25:43 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 08:25:44 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 02 Dec 2023 08:25:44 GMT
WORKDIR /usr/local/tomcat
# Sat, 02 Dec 2023 08:25:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 02 Dec 2023 08:25:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 02 Dec 2023 08:32:50 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Sat, 02 Dec 2023 08:32:50 GMT
ENV TOMCAT_MAJOR=8
# Wed, 13 Dec 2023 02:18:44 GMT
ENV TOMCAT_VERSION=8.5.97
# Wed, 13 Dec 2023 02:18:44 GMT
ENV TOMCAT_SHA512=344ea91c95677fdc243bc58a1f8ab745117a80c0a458ae2e26ebc4f968e06c4bfffaf9a4aae52de3d72b945b05b6e03b7cfae98596c222cbe7d394d52363da86
# Wed, 13 Dec 2023 02:18:45 GMT
COPY dir:2c7170ef09698af4d892e670e3e59afabcdb7aa617d563c95d268bc26fbfbf67 in /usr/local/tomcat 
# Wed, 13 Dec 2023 02:18:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2023 02:18:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Dec 2023 02:18:50 GMT
EXPOSE 8080
# Wed, 13 Dec 2023 02:18:50 GMT
ENTRYPOINT []
# Wed, 13 Dec 2023 02:18:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a0dd4e5224ba77a5588baadfd0a49dbe1c202ba2c6eaab5e29c7a2904e8718`  
		Last Modified: Sat, 02 Dec 2023 02:03:43 GMT  
		Size: 12.9 MB (12902809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d539d0422c7447bb3150972215c15b6dc7b02ed85c90f4e521bd35f58d0da302`  
		Last Modified: Sat, 02 Dec 2023 02:04:22 GMT  
		Size: 41.9 MB (41858214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a01af5de9bf5c28523b73294b891af72ea91cf9861dfa8a81d97338a29c99b`  
		Last Modified: Sat, 02 Dec 2023 02:04:17 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d992b85c899235264f1d1316d6d3eb5bb740cfd9b6c1f082f79e82163651447e`  
		Last Modified: Sat, 02 Dec 2023 02:04:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aecc89a0836f78849d812d9e10dd26f8f6ec90edaec4b91a1e6afca119a93c7`  
		Last Modified: Sat, 02 Dec 2023 08:43:24 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f0c238b2869d6fbd55fb19ab3b6791bfb47025138c2fbb61d53697cb5a3222`  
		Last Modified: Wed, 13 Dec 2023 02:38:42 GMT  
		Size: 11.4 MB (11445301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776fdf9b032c8f8ef2b77c23ddc1908456f7539d1d84b10ec32b2c6254e37327`  
		Last Modified: Wed, 13 Dec 2023 02:38:42 GMT  
		Size: 455.8 KB (455761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fda14dbaafcc6c97f381ce8d27ed0a27cd297c287ad393740f6182a2a8ab61`  
		Last Modified: Wed, 13 Dec 2023 02:38:41 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:20bd0b59b96cfd3be4a03ce4d90fb9409a2d282328cb9138bcdd58e7a6a06248
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91394124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e652c314c4b883b16b10fd2c2df30f6e856725e6d4fa295388851b30184d4552`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Dec 2023 07:58:40 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:58:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:58:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:58:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:58:44 GMT
ADD file:852469f16f85d8eff83511eb82d6d4409a4608b882c1634281a43c1c481f70c0 in / 
# Fri, 01 Dec 2023 07:58:44 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:52:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 06:52:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 06:52:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Dec 2023 06:53:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:53:16 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Sat, 02 Dec 2023 06:53:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='37b997f12cd572da979283fccafec9ba903041a209605b50fcb46cc34f1a9917';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u392b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='91d31027da0d985be3549714389593d9e0da3da5057d87e3831c7c538b9a2a0f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_x64_linux_hotspot_8u392b08.tar.gz';          ;;        armhf|arm)          ESUM='877953bfabcdbcd000c11364d806456ca579a921085de2ca942280ebe168cac2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_arm_linux_hotspot_8u392b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='0ecb0aeb54fb9d3c9e1a7ea411490127e8e298d93219fafc4dd6051a5b74671f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u392b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Sat, 02 Dec 2023 06:53:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete."
# Sat, 02 Dec 2023 06:53:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 02 Dec 2023 06:53:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Dec 2023 08:17:11 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 02 Dec 2023 08:17:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 08:17:11 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 02 Dec 2023 08:17:11 GMT
WORKDIR /usr/local/tomcat
# Sat, 02 Dec 2023 08:17:11 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 02 Dec 2023 08:17:11 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 02 Dec 2023 08:21:55 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Sat, 02 Dec 2023 08:21:55 GMT
ENV TOMCAT_MAJOR=8
# Wed, 13 Dec 2023 01:18:41 GMT
ENV TOMCAT_VERSION=8.5.97
# Wed, 13 Dec 2023 01:18:41 GMT
ENV TOMCAT_SHA512=344ea91c95677fdc243bc58a1f8ab745117a80c0a458ae2e26ebc4f968e06c4bfffaf9a4aae52de3d72b945b05b6e03b7cfae98596c222cbe7d394d52363da86
# Wed, 13 Dec 2023 01:18:42 GMT
COPY dir:d5f1d17194323ef6e8fc0b23a67d9a17ebfe6f9ea8664e078adaccd84835dc1d in /usr/local/tomcat 
# Wed, 13 Dec 2023 01:18:46 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2023 01:18:47 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Dec 2023 01:18:47 GMT
EXPOSE 8080
# Wed, 13 Dec 2023 01:18:47 GMT
ENTRYPOINT []
# Wed, 13 Dec 2023 01:18:47 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:24265e8b291700ac2b80b990af5be5827ef3d9ba54e498a6e36563c879970e0f`  
		Last Modified: Wed, 29 Nov 2023 22:33:38 GMT  
		Size: 27.5 MB (27523678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca56cd7c50818a0ddad15a810796d44bf99dd0578c20198db6da1751082578f`  
		Last Modified: Sat, 02 Dec 2023 06:56:43 GMT  
		Size: 12.5 MB (12492095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf846ba298b166c82e018bd103e9c45a2a531ee755206e9160a0f21be2e08e8f`  
		Last Modified: Sat, 02 Dec 2023 06:57:18 GMT  
		Size: 39.6 MB (39569909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564996ce8b58ef05d7d96fe03602415cebb0422d646c9eb52d914af49dbf83bf`  
		Last Modified: Sat, 02 Dec 2023 06:57:13 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271524ed29b7430d140f016a5d16ff39a7f07ce56e6204a10f9c824f467ef84a`  
		Last Modified: Sat, 02 Dec 2023 06:57:13 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602ff249fd34724c6f2a74357760699e978c50f5668b34be3927fdde75d5eb5f`  
		Last Modified: Sat, 02 Dec 2023 08:28:47 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65283391d38fb77c03d09b5d937213ad550bcb6f9466fdf6d37255917aaee4c3`  
		Last Modified: Wed, 13 Dec 2023 01:30:20 GMT  
		Size: 11.4 MB (11376862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5684d35816ff530c1ad806254c366a4356cea2debc6098f8d521f67082c66879`  
		Last Modified: Wed, 13 Dec 2023 01:30:19 GMT  
		Size: 430.4 KB (430382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ce4409a3e68669cbed55d9b5be926368229714820a923f3aca34cfc00bc280`  
		Last Modified: Wed, 13 Dec 2023 01:30:19 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:025ab1a2b20f5b545ce453f8bfbc7cb5de07c2a0866d5c4d5796811178faba30
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (93995606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52de08f676362c13ca9dc70da609f752b0a23313e2f3f1f0fee3ab9de62855e3`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:30:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 05:30:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 05:30:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Dec 2023 05:31:08 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:31:09 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Sat, 02 Dec 2023 05:31:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='37b997f12cd572da979283fccafec9ba903041a209605b50fcb46cc34f1a9917';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u392b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='91d31027da0d985be3549714389593d9e0da3da5057d87e3831c7c538b9a2a0f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_x64_linux_hotspot_8u392b08.tar.gz';          ;;        armhf|arm)          ESUM='877953bfabcdbcd000c11364d806456ca579a921085de2ca942280ebe168cac2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_arm_linux_hotspot_8u392b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='0ecb0aeb54fb9d3c9e1a7ea411490127e8e298d93219fafc4dd6051a5b74671f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u392b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Sat, 02 Dec 2023 05:31:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete."
# Sat, 02 Dec 2023 05:31:28 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 02 Dec 2023 05:31:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Dec 2023 10:33:23 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 02 Dec 2023 10:33:23 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 10:33:24 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 02 Dec 2023 10:33:24 GMT
WORKDIR /usr/local/tomcat
# Sat, 02 Dec 2023 10:33:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 02 Dec 2023 10:33:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 02 Dec 2023 10:38:30 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Sat, 02 Dec 2023 10:38:30 GMT
ENV TOMCAT_MAJOR=8
# Wed, 13 Dec 2023 02:08:38 GMT
ENV TOMCAT_VERSION=8.5.97
# Wed, 13 Dec 2023 02:08:38 GMT
ENV TOMCAT_SHA512=344ea91c95677fdc243bc58a1f8ab745117a80c0a458ae2e26ebc4f968e06c4bfffaf9a4aae52de3d72b945b05b6e03b7cfae98596c222cbe7d394d52363da86
# Wed, 13 Dec 2023 02:08:38 GMT
COPY dir:5264b1ee3a60051b58825e23ce856336ae71c3f5bd800e35d56bb7d7b5a06edc in /usr/local/tomcat 
# Wed, 13 Dec 2023 02:08:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2023 02:08:43 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Dec 2023 02:08:43 GMT
EXPOSE 8080
# Wed, 13 Dec 2023 02:08:43 GMT
ENTRYPOINT []
# Wed, 13 Dec 2023 02:08:43 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd693e5b74a77728d853339f783bee254c5de7b0f35f20b69c65c278bcb0753`  
		Last Modified: Sat, 02 Dec 2023 05:34:59 GMT  
		Size: 12.8 MB (12844949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581c3dc9a2b52593f1272c6590a08b8cce82bd5f879eaa43538eb298218f28b6`  
		Last Modified: Sat, 02 Dec 2023 05:35:31 GMT  
		Size: 40.8 MB (40843265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51ddb0f265287d85112b825d8f8e0e2b9cdee50d435369a916da9a4efd98e73`  
		Last Modified: Sat, 02 Dec 2023 05:35:28 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74183cc7577c64ffbb42016ff50e53f8b49e6a64d7e09a2a15095e4a94c5989e`  
		Last Modified: Sat, 02 Dec 2023 05:35:28 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ab538c092fd7c5812f235e2e2fc0cf3524cfdc25473ea876e831a1785e6f88`  
		Last Modified: Sat, 02 Dec 2023 10:48:27 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51099287528f08273e2ea5cfa16d51bd8fbc3d2638e8a93c5099f0da1d8217bb`  
		Last Modified: Wed, 13 Dec 2023 02:28:28 GMT  
		Size: 11.5 MB (11450405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a2192a953052bbefe2084489ac9084f294b313ac3c217d80b36813d90fa1f95`  
		Last Modified: Wed, 13 Dec 2023 02:28:28 GMT  
		Size: 455.9 KB (455851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8bb2b8312a8a6733ab25701490713cd3ae12f66142a5dbc4d6fe9f7de97d444`  
		Last Modified: Wed, 13 Dec 2023 02:28:27 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:f542660407868ed0a1ad40232b07c29c8b6ccfaf59e967e2c5a911ac1cc9871a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102626335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140eb854a26322d88d241799459e78727bdbb8b93253ba31dcd85be0763321b9`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Dec 2023 08:12:00 GMT
ARG RELEASE
# Fri, 01 Dec 2023 08:12:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 08:12:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 08:12:00 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 08:12:03 GMT
ADD file:80047e51fa5311c19317ab688acec0517d98f1cbf74fa4c22a7105e80ebaf610 in / 
# Fri, 01 Dec 2023 08:12:04 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:06:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 06:06:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 06:06:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Dec 2023 06:06:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:06:39 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Sat, 02 Dec 2023 06:07:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='37b997f12cd572da979283fccafec9ba903041a209605b50fcb46cc34f1a9917';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u392b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='91d31027da0d985be3549714389593d9e0da3da5057d87e3831c7c538b9a2a0f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_x64_linux_hotspot_8u392b08.tar.gz';          ;;        armhf|arm)          ESUM='877953bfabcdbcd000c11364d806456ca579a921085de2ca942280ebe168cac2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_arm_linux_hotspot_8u392b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='0ecb0aeb54fb9d3c9e1a7ea411490127e8e298d93219fafc4dd6051a5b74671f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u392b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Sat, 02 Dec 2023 06:07:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete."
# Sat, 02 Dec 2023 06:07:36 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 02 Dec 2023 06:07:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Dec 2023 10:27:43 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 02 Dec 2023 10:27:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 10:27:46 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 02 Dec 2023 10:27:47 GMT
WORKDIR /usr/local/tomcat
# Sat, 02 Dec 2023 10:27:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 02 Dec 2023 10:27:49 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 02 Dec 2023 10:42:48 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Sat, 02 Dec 2023 10:42:49 GMT
ENV TOMCAT_MAJOR=8
# Wed, 13 Dec 2023 02:51:36 GMT
ENV TOMCAT_VERSION=8.5.97
# Wed, 13 Dec 2023 02:51:37 GMT
ENV TOMCAT_SHA512=344ea91c95677fdc243bc58a1f8ab745117a80c0a458ae2e26ebc4f968e06c4bfffaf9a4aae52de3d72b945b05b6e03b7cfae98596c222cbe7d394d52363da86
# Wed, 13 Dec 2023 02:51:38 GMT
COPY dir:02bc324bbaa5d454ea5835b1a91046584fccd4ae6af10f41e167033c52f297f4 in /usr/local/tomcat 
# Wed, 13 Dec 2023 02:51:47 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2023 02:51:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Dec 2023 02:51:52 GMT
EXPOSE 8080
# Wed, 13 Dec 2023 02:51:52 GMT
ENTRYPOINT []
# Wed, 13 Dec 2023 02:51:52 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c3606768af36fe4984cee7cfc0c9d919a7adf83ac4c1849c30da06916b9ec921`  
		Last Modified: Sat, 02 Dec 2023 04:49:10 GMT  
		Size: 35.7 MB (35662741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8747a30614d194a60f1319fa2df5f984832ca89eb81acd4cb9a79921a3e29ee`  
		Last Modified: Sat, 02 Dec 2023 06:15:19 GMT  
		Size: 13.8 MB (13767253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf819111ff1a8a4b3073c9add12e23e01a278394b1fe38c41baf448b4672c29`  
		Last Modified: Sat, 02 Dec 2023 06:15:56 GMT  
		Size: 41.2 MB (41235517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759af831c1b0079167a7bab77b6881e5a73d0ee71f5caea3a987ff48aec029d7`  
		Last Modified: Sat, 02 Dec 2023 06:15:51 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5109dc2ae58b044acf4b21899e4707e77ed96c564069a4073f694532fd0b690d`  
		Last Modified: Sat, 02 Dec 2023 06:15:51 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f5b841be7a3204a9665a02b3103f2e1e3f787776395fe9b328eebef2cca0f8`  
		Last Modified: Sat, 02 Dec 2023 10:54:41 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9668bf6eabd8e16b2a43ce4b9556464721a81760d235af8218e6be16fe4738`  
		Last Modified: Wed, 13 Dec 2023 03:11:43 GMT  
		Size: 11.5 MB (11472698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173a894049955b05104f358c8d172b457a23b7df9a80eb6f24fcf2361ce406a5`  
		Last Modified: Wed, 13 Dec 2023 03:11:41 GMT  
		Size: 486.9 KB (486929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d4b740d22d7f86c719731f2bdee1db2263414837c8c11b375d19d83cf2f29e`  
		Last Modified: Wed, 13 Dec 2023 03:11:41 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
