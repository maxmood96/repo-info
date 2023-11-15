## `tomcat:8-jre17-temurin-focal`

```console
$ docker pull tomcat@sha256:7f642d48739b2a698e45df5a849fb7a4d4c0bdab8ae88bd81a10f762a97c4c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:8-jre17-temurin-focal` - linux; amd64

```console
$ docker pull tomcat@sha256:d809992273592c719107b06ad333d5c789ec17deaf9172b99ea981f9142ef1ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108283228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8040f018d4b50b47da6b44095f12c55d89fe69b05eca2231d3eb19413757c2d1`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 03 Oct 2023 10:45:50 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:45:51 GMT
ADD file:4809da414c2d478b4d991cbdaa2df457f2b3d07d0ff6cf673f09a66f90833e81 in / 
# Tue, 03 Oct 2023 10:45:52 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 05:50:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 05:50:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 05:50:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Oct 2023 23:27:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 30 Oct 2023 23:27:10 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Mon, 30 Oct 2023 23:29:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 30 Oct 2023 23:29:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Mon, 30 Oct 2023 23:29:10 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 30 Oct 2023 23:29:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 31 Oct 2023 03:41:22 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 31 Oct 2023 03:41:22 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:41:22 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 31 Oct 2023 03:41:22 GMT
WORKDIR /usr/local/tomcat
# Tue, 31 Oct 2023 03:41:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 31 Oct 2023 03:41:23 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 31 Oct 2023 03:46:12 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 31 Oct 2023 03:46:12 GMT
ENV TOMCAT_MAJOR=8
# Wed, 15 Nov 2023 06:01:11 GMT
ENV TOMCAT_VERSION=8.5.96
# Wed, 15 Nov 2023 06:01:11 GMT
ENV TOMCAT_SHA512=dc80b2649f2ad7f8baa6c925ef1d0bad71e27f5557dc46e313f45b8044dba05791a60062117d5257c28955f8405eded70e451ee2e0d9671c8aecd21977e0bec9
# Wed, 15 Nov 2023 06:01:11 GMT
COPY dir:bfe88498956906300e1360a890ebdc135a30dc0c113eb66bed9be8e6d5498b0c in /usr/local/tomcat 
# Wed, 15 Nov 2023 06:01:16 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 15 Nov 2023 06:01:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 15 Nov 2023 06:01:18 GMT
EXPOSE 8080
# Wed, 15 Nov 2023 06:01:18 GMT
ENTRYPOINT []
# Wed, 15 Nov 2023 06:01:18 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7a2c559011895d255fce249c00396abff5ae7e0c0a92931d0ed493e71de78e3a`  
		Last Modified: Tue, 03 Oct 2023 17:02:08 GMT  
		Size: 28.6 MB (28580681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875b30e249cd979e411fd310dc9efb9af0136fcdaa859b1de2d891b1dbb21e72`  
		Last Modified: Mon, 30 Oct 2023 23:35:43 GMT  
		Size: 20.7 MB (20661219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cabab1ce78881f9e986bcb5c594072252c032dc2dbf1a7812ada53ca9fd7c76d`  
		Last Modified: Mon, 30 Oct 2023 23:37:35 GMT  
		Size: 47.1 MB (47148547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a993c8646506f3e6340eb5a3eedabfe2571819ec907af6d39c1b84d4f9b3ee24`  
		Last Modified: Mon, 30 Oct 2023 23:37:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c0e45100d957d89e4d230fb346330544c2c7c9de0b4d7cb48cebbf89791a7f`  
		Last Modified: Mon, 30 Oct 2023 23:37:29 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbd69eada46d914ce3f3356d274befa07083ccad6a6f7448d8d9c0184bf4795`  
		Last Modified: Tue, 31 Oct 2023 03:56:59 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebae06efb3d33957b847312bddda45a1df9cee8b6b9dbe9bb226c01fd0c6da0`  
		Last Modified: Wed, 15 Nov 2023 06:14:39 GMT  
		Size: 11.4 MB (11438801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9599a05f3d0bcd3d7124346e654cd9a674f5f130e6d137ae3068ba3832f1aa`  
		Last Modified: Wed, 15 Nov 2023 06:14:38 GMT  
		Size: 452.8 KB (452786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e69043c501b34d8930c1a9b82e0302247a4b72384654f8ea598d1dd32780e2`  
		Last Modified: Wed, 15 Nov 2023 06:14:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre17-temurin-focal` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:aca5cce5b8c984efd7e3cb174e7b07f75d968cd4da2bbf1804db41bd210576c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101161977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c084fb9a734494b40021b9898cdbfa3c3237eb85eb16374ecf09aeb1f81e30`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 03 Oct 2023 10:47:59 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:47:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:48:06 GMT
ADD file:8dffbfada6e0bebb2858525182aef87ac2cbd88c624f32696ec2cb947e71a4f3 in / 
# Tue, 03 Oct 2023 10:48:07 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 01:15:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:15:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:15:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Oct 2023 23:00:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 30 Oct 2023 23:00:33 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Mon, 30 Oct 2023 23:01:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 30 Oct 2023 23:01:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Mon, 30 Oct 2023 23:01:35 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 30 Oct 2023 23:01:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 31 Oct 2023 00:28:04 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 31 Oct 2023 00:28:04 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 00:28:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 31 Oct 2023 00:28:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 31 Oct 2023 00:28:05 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 31 Oct 2023 00:28:05 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 31 Oct 2023 00:31:17 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 31 Oct 2023 00:31:17 GMT
ENV TOMCAT_MAJOR=8
# Wed, 15 Nov 2023 05:26:12 GMT
ENV TOMCAT_VERSION=8.5.96
# Wed, 15 Nov 2023 05:26:13 GMT
ENV TOMCAT_SHA512=dc80b2649f2ad7f8baa6c925ef1d0bad71e27f5557dc46e313f45b8044dba05791a60062117d5257c28955f8405eded70e451ee2e0d9671c8aecd21977e0bec9
# Wed, 15 Nov 2023 05:26:13 GMT
COPY dir:83631c8108f4e8be7887136ce49d4f181656f55c9ada93daa31a03f01f9ac670 in /usr/local/tomcat 
# Wed, 15 Nov 2023 05:26:17 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 15 Nov 2023 05:26:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 15 Nov 2023 05:26:19 GMT
EXPOSE 8080
# Wed, 15 Nov 2023 05:26:19 GMT
ENTRYPOINT []
# Wed, 15 Nov 2023 05:26:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3b5f1ba1b648ae0824ed6a95ab17335537f8e689df99917fd374af5dd34078eb`  
		Last Modified: Fri, 13 Oct 2023 01:11:42 GMT  
		Size: 24.6 MB (24592174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552f144f9b13fee3559a44fd346855066eebb23017eb6f35baf0f236ffa76b51`  
		Last Modified: Mon, 30 Oct 2023 23:04:01 GMT  
		Size: 20.0 MB (19961913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd2be0da7840ba24c9897ebdc047c8d7332a6a539556389bc8aed9a6de7207a`  
		Last Modified: Mon, 30 Oct 2023 23:04:53 GMT  
		Size: 44.8 MB (44788158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51125d8bcbbbe76c602a6b414eba5853ba51114abca398e92b7c2ded1b27c234`  
		Last Modified: Mon, 30 Oct 2023 23:04:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af040637b5d66867413bf32bb10ee9255fd64f732f99f6725975d589dec28a9`  
		Last Modified: Mon, 30 Oct 2023 23:04:46 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33552c0ca271d89fe0a6d85e69f8ca87cf9624ef9bc9eae0c14000d45bfe8782`  
		Last Modified: Tue, 31 Oct 2023 00:37:55 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44eef891e4ef6a680fbbae3dbdc26e5510daa01c8c774e227d3c9d5e8fa0488`  
		Last Modified: Wed, 15 Nov 2023 05:33:30 GMT  
		Size: 11.4 MB (11389317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4cd0972062ddb1c4951bb475962ab7f4f281387f2f1db367942cb874bc0a6a`  
		Last Modified: Wed, 15 Nov 2023 05:33:29 GMT  
		Size: 429.2 KB (429225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1590413dfff1d8b6396f0caab98e33082d60181e1530f36dbde514ecaa888599`  
		Last Modified: Wed, 15 Nov 2023 05:33:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre17-temurin-focal` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:d231f98e665a03cbccb20fa899e52f6d904fe39cfb6541ce5c08e963c20019f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107112036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16242610ca984540e78b413542b926c3c3d464ca56b3aafc754dcb599b33ce4`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 02:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 02:46:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 02:46:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Oct 2023 23:43:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 30 Oct 2023 23:43:33 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Mon, 30 Oct 2023 23:45:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 30 Oct 2023 23:45:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Mon, 30 Oct 2023 23:45:29 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 30 Oct 2023 23:45:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 31 Oct 2023 02:59:22 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 31 Oct 2023 02:59:22 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 02:59:23 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 31 Oct 2023 02:59:23 GMT
WORKDIR /usr/local/tomcat
# Tue, 31 Oct 2023 02:59:23 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 31 Oct 2023 02:59:23 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 31 Oct 2023 03:03:03 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 31 Oct 2023 03:03:03 GMT
ENV TOMCAT_MAJOR=8
# Wed, 15 Nov 2023 06:40:37 GMT
ENV TOMCAT_VERSION=8.5.96
# Wed, 15 Nov 2023 06:40:37 GMT
ENV TOMCAT_SHA512=dc80b2649f2ad7f8baa6c925ef1d0bad71e27f5557dc46e313f45b8044dba05791a60062117d5257c28955f8405eded70e451ee2e0d9671c8aecd21977e0bec9
# Wed, 15 Nov 2023 06:40:38 GMT
COPY dir:99d60790883896f88b199715a633d4a73e8e3b785ac165ea1598592763586b5f in /usr/local/tomcat 
# Wed, 15 Nov 2023 06:40:41 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 15 Nov 2023 06:40:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 15 Nov 2023 06:40:42 GMT
EXPOSE 8080
# Wed, 15 Nov 2023 06:40:42 GMT
ENTRYPOINT []
# Wed, 15 Nov 2023 06:40:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6cba4020c0a193cd551ed8edf368670967e3546345b52c4ec66cb0931436e9b9`  
		Last Modified: Thu, 05 Oct 2023 12:12:17 GMT  
		Size: 27.2 MB (27199503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3982c3bf03cb594352f69f3f546c659470c3051ff39a2f19d27f0ef95db66ca`  
		Last Modified: Mon, 30 Oct 2023 23:50:22 GMT  
		Size: 21.4 MB (21378540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e5d1582b3c2417d8b0b8335d34f748a17ee5fa019774754c1753245b62142b`  
		Last Modified: Mon, 30 Oct 2023 23:51:49 GMT  
		Size: 46.6 MB (46624289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07764e92b7187cc5adcea1819b77c42e6382b656201e4a17ab1b60f60b766297`  
		Last Modified: Mon, 30 Oct 2023 23:51:43 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1811b512327bd2ba0d318bc88d8eee511781da72b2e98b9cac89b3a16d0a1d17`  
		Last Modified: Mon, 30 Oct 2023 23:51:44 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb74c0eb1afa2469dd802ebf972661fb5d816aef8ee10f51f9fa5c4e2a35e34e`  
		Last Modified: Tue, 31 Oct 2023 03:13:24 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61650a67a102f33f8a3786e054b4276ff1cb87c55275a8ab04d8d57ce9b8201`  
		Last Modified: Wed, 15 Nov 2023 06:51:30 GMT  
		Size: 11.5 MB (11456213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d40c90a0cad8839411efbcdb80022fe782c21f8e3c132c992c3feaa1d586e8`  
		Last Modified: Wed, 15 Nov 2023 06:51:29 GMT  
		Size: 452.3 KB (452297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3935a0635128aba902aa60884c4deb1e7c3ae910a3254e5b54c886fccf1a20ff`  
		Last Modified: Wed, 15 Nov 2023 06:51:29 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre17-temurin-focal` - linux; ppc64le

```console
$ docker pull tomcat@sha256:a5dda4e1922cbb72159b801bf33fab983ef50578c4cdbc6a71eecb08856ce468
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (114972377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed6600207ac8ef629629e9bf1142aaedeffb4c1078b44c70771d4500af4cee3`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 03 Oct 2023 11:03:52 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:03:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:03:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:03:53 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:03:56 GMT
ADD file:ba2394102af0c0584d39af9ec5dd4fa13286293b4607ac7cb9e16d7a2781eef2 in / 
# Tue, 03 Oct 2023 11:03:56 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 07:59:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 07:59:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 07:59:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Oct 2023 23:23:25 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 30 Oct 2023 23:23:26 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Mon, 30 Oct 2023 23:26:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 30 Oct 2023 23:26:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Mon, 30 Oct 2023 23:26:40 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 30 Oct 2023 23:26:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 31 Oct 2023 01:22:11 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 31 Oct 2023 01:22:12 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 01:22:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 31 Oct 2023 01:22:13 GMT
WORKDIR /usr/local/tomcat
# Tue, 31 Oct 2023 01:22:13 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 31 Oct 2023 01:22:13 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 31 Oct 2023 01:28:38 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 31 Oct 2023 01:28:39 GMT
ENV TOMCAT_MAJOR=8
# Wed, 15 Nov 2023 05:42:48 GMT
ENV TOMCAT_VERSION=8.5.96
# Wed, 15 Nov 2023 05:42:48 GMT
ENV TOMCAT_SHA512=dc80b2649f2ad7f8baa6c925ef1d0bad71e27f5557dc46e313f45b8044dba05791a60062117d5257c28955f8405eded70e451ee2e0d9671c8aecd21977e0bec9
# Wed, 15 Nov 2023 05:42:49 GMT
COPY dir:490d64a2e57462ca0a16d3503dd84417d2e6162d41262fdd740fd00f02e4c87d in /usr/local/tomcat 
# Wed, 15 Nov 2023 05:42:57 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 15 Nov 2023 05:43:01 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 15 Nov 2023 05:43:02 GMT
EXPOSE 8080
# Wed, 15 Nov 2023 05:43:02 GMT
ENTRYPOINT []
# Wed, 15 Nov 2023 05:43:03 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f3046919588b0e4a9b202dcd311befda8e46083ce41f424888dcbea91ce8e6e2`  
		Last Modified: Fri, 13 Oct 2023 06:16:08 GMT  
		Size: 33.3 MB (33306424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f221d72c9bf27c7034655ef6e56fad843ff16fdbde81de07ac6186c80efb13`  
		Last Modified: Mon, 30 Oct 2023 23:32:18 GMT  
		Size: 22.7 MB (22707653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5e7692da85512dafec964ee13952a53a886d2749f49b337acb2f1ab2b8dd29`  
		Last Modified: Mon, 30 Oct 2023 23:34:03 GMT  
		Size: 47.0 MB (47000580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f6d82ece9591f2f66a57b56a0509fab3d15eba4e6fc27649546988e497a852`  
		Last Modified: Mon, 30 Oct 2023 23:33:56 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e60ba827bf4729f15db13d4b55f696c0171e21cfbe7172b19bc517ddef31e3`  
		Last Modified: Mon, 30 Oct 2023 23:33:56 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a84f06cfc2386b39161cc1d02e5a63031ac2e20f5900fd3c47c34e4cfed214`  
		Last Modified: Tue, 31 Oct 2023 01:37:09 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81eaa287d7598a0652947019878d80091795f06fc654a927e1514f5cc0f43a4a`  
		Last Modified: Wed, 15 Nov 2023 05:56:53 GMT  
		Size: 11.5 MB (11478622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4291e7c40102ef85808bee62c61fc2c324b14d1074a66197a52c894600922707`  
		Last Modified: Wed, 15 Nov 2023 05:56:52 GMT  
		Size: 477.9 KB (477902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b393c10ffd39037c7b73f93fde65313f3e80d1d7e67173b68b843d9be78ce1e2`  
		Last Modified: Wed, 15 Nov 2023 05:56:52 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre17-temurin-focal` - linux; s390x

```console
$ docker pull tomcat@sha256:209cd2b38aa41d8cb09c30413cfa959089891a94df1ddc4f89c449fc4f5122e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102816970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59aa1b8c3d86085ade49c8557c3dafc3a4e5b972092053dba815813a0f8d3833`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 03 Oct 2023 11:03:23 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:03:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:03:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:03:23 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:03:25 GMT
ADD file:1d9be1bf43c126d53bda18c06d12757c021da97c0c9d3a9c9f56df17312095b8 in / 
# Tue, 03 Oct 2023 11:03:25 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 10:08:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 10:08:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 10:08:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Oct 2023 23:26:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 30 Oct 2023 23:26:10 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Mon, 30 Oct 2023 23:27:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 30 Oct 2023 23:27:37 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Mon, 30 Oct 2023 23:27:37 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 30 Oct 2023 23:27:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 31 Oct 2023 00:44:36 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 31 Oct 2023 00:44:36 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 00:44:37 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 31 Oct 2023 00:44:37 GMT
WORKDIR /usr/local/tomcat
# Tue, 31 Oct 2023 00:44:37 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 31 Oct 2023 00:44:37 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 31 Oct 2023 00:47:50 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 31 Oct 2023 00:47:50 GMT
ENV TOMCAT_MAJOR=8
# Wed, 15 Nov 2023 05:35:07 GMT
ENV TOMCAT_VERSION=8.5.96
# Wed, 15 Nov 2023 05:35:07 GMT
ENV TOMCAT_SHA512=dc80b2649f2ad7f8baa6c925ef1d0bad71e27f5557dc46e313f45b8044dba05791a60062117d5257c28955f8405eded70e451ee2e0d9671c8aecd21977e0bec9
# Wed, 15 Nov 2023 05:35:08 GMT
COPY dir:1bdcadee6245f88c952ed7b7684c08813e3f3e1c006ea4eb7bee2e6408047ae3 in /usr/local/tomcat 
# Wed, 15 Nov 2023 05:35:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 15 Nov 2023 05:35:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 15 Nov 2023 05:35:13 GMT
EXPOSE 8080
# Wed, 15 Nov 2023 05:35:13 GMT
ENTRYPOINT []
# Wed, 15 Nov 2023 05:35:14 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2f51ce1532d2fc433720a55b8851134d5051381dedc2ef6109fb7ebb7a0edb92`  
		Last Modified: Fri, 13 Oct 2023 10:16:26 GMT  
		Size: 27.0 MB (27014102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494e2290595369aef767062fddabdef9e6de2a0df560c06c453d94e7c5355a2a`  
		Last Modified: Mon, 30 Oct 2023 23:30:25 GMT  
		Size: 20.1 MB (20140832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d979ec21da68a9037a0ba335ac7f4c9d85f8117509d012e76b961ab1c9d6262`  
		Last Modified: Mon, 30 Oct 2023 23:31:22 GMT  
		Size: 43.8 MB (43755089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe5fc02668af1b86b40cbb185cd7922889791e0de081a14a9993efd9b1c6d91`  
		Last Modified: Mon, 30 Oct 2023 23:31:16 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2e8a5f72dd6f854ad65d5497d98ada8dbba2a4e2785e7201987838b4222da2`  
		Last Modified: Mon, 30 Oct 2023 23:31:16 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85394f73aeebff2b5f6128f33aafef43f9803a41b810720ce93a16dfaa266d06`  
		Last Modified: Tue, 31 Oct 2023 00:53:12 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab09476dd213e1760dd2e0c4d16486a61e75280d39d1e6c5d5f75ef179a9fb5`  
		Last Modified: Wed, 15 Nov 2023 05:40:16 GMT  
		Size: 11.5 MB (11451273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0e9ff7ff77fc295d8de8c4bdf473f6e05460a592d9bb7dc7434b7bfdf4251a`  
		Last Modified: Wed, 15 Nov 2023 05:40:16 GMT  
		Size: 454.5 KB (454476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135cae93eb899d00388681ead1996c470d97cb44a19b209a0c5a358b30ca6164`  
		Last Modified: Wed, 15 Nov 2023 05:40:16 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
