## `tomcat:9-jre11-temurin-focal`

```console
$ docker pull tomcat@sha256:f8e5ca5a906c4620ef9531cd9311dc92c3d1d601194522720df71902c049ddc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:9-jre11-temurin-focal` - linux; amd64

```console
$ docker pull tomcat@sha256:f37ff497ed1147b335a3d3369ae4675367b0946792cb3034fc9dc8e56772f8d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105492366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74eaf0944837d1f999c3989d5730247ed287a9cc2109202d598e5eeeebfb710c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:15:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:15:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:15:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:16:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:17:09 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:17:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:17:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:17:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 16:12:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 16 Dec 2023 16:12:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 16:12:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 16 Dec 2023 16:12:21 GMT
WORKDIR /usr/local/tomcat
# Sat, 16 Dec 2023 16:12:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 16 Dec 2023 16:12:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 16 Dec 2023 16:12:22 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 16 Dec 2023 16:12:22 GMT
ENV TOMCAT_MAJOR=9
# Tue, 09 Jan 2024 22:39:54 GMT
ENV TOMCAT_VERSION=9.0.85
# Tue, 09 Jan 2024 22:39:54 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Mon, 22 Jan 2024 23:05:14 GMT
COPY dir:27e67dc76348999de65246457d9c3486384bf223aa02f2d41f117e7c85688b11 in /usr/local/tomcat 
# Mon, 22 Jan 2024 23:05:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Jan 2024 23:05:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 22 Jan 2024 23:05:21 GMT
EXPOSE 8080
# Mon, 22 Jan 2024 23:05:21 GMT
ENTRYPOINT []
# Mon, 22 Jan 2024 23:05:21 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6a6404648d953a02729d22ecf5aa18fe7f6f8d40e669ba5c45fbe6db2cd987`  
		Last Modified: Sat, 16 Dec 2023 10:21:04 GMT  
		Size: 16.9 MB (16920196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0aabae808c7efe5c3e3de163d93b9c52793dca2bc4fc888b84c4fddbc5e469`  
		Last Modified: Sat, 16 Dec 2023 10:23:00 GMT  
		Size: 47.1 MB (47068480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1594c8e637d5a3db2275fd1a636dcf282518f638974aa99b0dcca5aac84a70d9`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5fea037d78a6688a059c0383ce69b0f3edd8ef03dca04da13d0cacc36f4915`  
		Last Modified: Sat, 16 Dec 2023 10:22:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e0762dcc00985358581ccc1d2ce79a19f3be5d30c64208cef80bb183945d82`  
		Last Modified: Sat, 16 Dec 2023 16:29:38 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74bb8c3d98368dc3a7b00611473fe7ba7ce92585df619b05373879542e59517`  
		Last Modified: Mon, 22 Jan 2024 23:27:56 GMT  
		Size: 12.5 MB (12468742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5582e937eb549d3582c1f55d8b9cb7a0f9b978d24d0f55dcf5001c438d61633`  
		Last Modified: Mon, 22 Jan 2024 23:27:53 GMT  
		Size: 449.7 KB (449729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bc9122d2d73d0139958221ccbdf1e33e9d8156d8265f5b79c7a0401ece5d29`  
		Last Modified: Mon, 22 Jan 2024 23:27:53 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre11-temurin-focal` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:768b976be9efba1b6d664d4dc54f3ecd1bd611ba9dee7d96ef0dceb08742e777
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98316254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266283169ec6bcb8cb957410f6cd0f9c22fe09bb16521c9d11f9c5159cb42f75`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 13 Dec 2023 10:37:05 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:37:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:37:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:37:06 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:37:14 GMT
ADD file:195375389d64193c828c6d3f379c7e35ea85256eb1c51d2bfeab73432ea46064 in / 
# Wed, 13 Dec 2023 10:37:15 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:29:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 09:29:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 09:29:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 09:30:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 21:11:40 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 21:12:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 21:12:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 21:12:18 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 21:12:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jan 2024 22:00:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 24 Jan 2024 22:00:32 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:00:32 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 24 Jan 2024 22:00:33 GMT
WORKDIR /usr/local/tomcat
# Wed, 24 Jan 2024 22:00:33 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 24 Jan 2024 22:00:33 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 24 Jan 2024 22:00:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 24 Jan 2024 22:00:33 GMT
ENV TOMCAT_MAJOR=9
# Wed, 24 Jan 2024 22:00:33 GMT
ENV TOMCAT_VERSION=9.0.85
# Wed, 24 Jan 2024 22:00:33 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Wed, 24 Jan 2024 22:00:34 GMT
COPY dir:073354bf6b0906b7c42dceb25117d1f7e317487cde852c90b4026624180abaa5 in /usr/local/tomcat 
# Wed, 24 Jan 2024 22:00:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 22:00:43 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 24 Jan 2024 22:00:44 GMT
EXPOSE 8080
# Wed, 24 Jan 2024 22:00:44 GMT
ENTRYPOINT []
# Wed, 24 Jan 2024 22:00:45 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ba68304511cfd178c72d64196a05b1343fbdbed6093d7b4db0c0d223510c40ab`  
		Last Modified: Sat, 16 Dec 2023 09:27:50 GMT  
		Size: 24.6 MB (24600972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45dca1c5123b34dd759063c3ea5a85792ef1b887f6337f3fc1bf67a9a3971c6e`  
		Last Modified: Sat, 16 Dec 2023 09:33:39 GMT  
		Size: 15.7 MB (15659547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c16a34ca53e2829ea95d9efa43b271ad1e644e6de5157828bb4310473357890f`  
		Last Modified: Wed, 24 Jan 2024 21:16:02 GMT  
		Size: 45.2 MB (45209441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19bea667e6e18b602449311229e874101d1d3154c34016f673514aa731e5d30`  
		Last Modified: Wed, 24 Jan 2024 21:15:55 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97b2e05ddba3ef8d107ec5cd4d245c2ef0e2108b6210f13517ea6cfc9d02d19`  
		Last Modified: Wed, 24 Jan 2024 21:15:55 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdc7948d13ba383224b310a740a20be493849a1df8583987974b764a0145c15`  
		Last Modified: Wed, 24 Jan 2024 22:13:01 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b3d4ae498d448600e9c14544e317f9ef3ccc006cfad40bbb93897d49ecc4c28`  
		Last Modified: Wed, 24 Jan 2024 22:13:02 GMT  
		Size: 12.4 MB (12419743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317dc8207d1660eb15b976d35d1af4452a006816d063a2f2e9c06fa7fc79fd5f`  
		Last Modified: Wed, 24 Jan 2024 22:13:02 GMT  
		Size: 425.4 KB (425373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f1e8c18c397012141b837a23b5f9d3d96a1d9ce49c2f2c31654bd75e367c46`  
		Last Modified: Wed, 24 Jan 2024 22:13:01 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre11-temurin-focal` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:88ff1e27b7642757bf2c7b0ef0f22e3b3b7e8d2319f4871aac315ed4a7b58ec0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102310394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ddd3329a50abddaa75777ec435d83bdd63f083fee437cd51d808360ab16a38a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:02:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:03:07 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 10:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:03:42 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:03:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:02:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 16 Dec 2023 15:02:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 15:02:28 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 16 Dec 2023 15:02:28 GMT
WORKDIR /usr/local/tomcat
# Sat, 16 Dec 2023 15:02:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 16 Dec 2023 15:02:29 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 16 Dec 2023 15:02:29 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 16 Dec 2023 15:02:29 GMT
ENV TOMCAT_MAJOR=9
# Tue, 09 Jan 2024 23:06:09 GMT
ENV TOMCAT_VERSION=9.0.85
# Tue, 09 Jan 2024 23:06:09 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Mon, 22 Jan 2024 23:52:23 GMT
COPY dir:2726859908bd887585de1d03a40bcad491d99c88959a6bb2b9078aa30d4a839b in /usr/local/tomcat 
# Mon, 22 Jan 2024 23:52:26 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Jan 2024 23:52:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 22 Jan 2024 23:52:28 GMT
EXPOSE 8080
# Mon, 22 Jan 2024 23:52:28 GMT
ENTRYPOINT []
# Mon, 22 Jan 2024 23:52:28 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69f35fd155c9c0a485e63ad002a7b98a6ce1921e230d386f1cffd2c8c16878`  
		Last Modified: Sat, 16 Dec 2023 10:06:15 GMT  
		Size: 16.8 MB (16769031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a34aa4bb6bc09a61eb02d95b805a54a0fb6377e7beaea1fb56ef084a95a97f1`  
		Last Modified: Sat, 16 Dec 2023 10:08:00 GMT  
		Size: 45.4 MB (45401004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0831ffaa0d230ce918d73646966be4527d3afe4c9854e0672f6a5634c4611697`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b2a79b9345fd52d15033dc564ff8a1fd03c42b09223b1932570dcecaa84f21`  
		Last Modified: Sat, 16 Dec 2023 10:07:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42781d4972c9b6f16545d7611fe2a1f7f7f6ba3eb349d5151ea78ca93aacd83a`  
		Last Modified: Sat, 16 Dec 2023 15:18:03 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a54d9e634d80175209f77dfd9529799630cfdbd2dd8e23201506a059381662`  
		Last Modified: Tue, 23 Jan 2024 00:12:04 GMT  
		Size: 12.5 MB (12486783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9bcf76179aaab86dff201439ec9c64ad2710c3bbddac362653692e4c0bf58b9`  
		Last Modified: Tue, 23 Jan 2024 00:12:03 GMT  
		Size: 449.2 KB (449239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887aee61ab97bd055b2b6b6f6ce049659b79d3a4d20c6ad28b197c341348cfb5`  
		Last Modified: Tue, 23 Jan 2024 00:12:03 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre11-temurin-focal` - linux; ppc64le

```console
$ docker pull tomcat@sha256:fe04596d7715d780a7b23ef5465f12e3cdab53c18212aea7ed69d416a61dc171
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 MB (107010900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbd636aa8b9e4d2efae1d1c287ebad4d7ecfab8a9536fca4e3d53f1ac964131`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 13 Dec 2023 10:36:32 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:36:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:36:35 GMT
ADD file:b7dcee8fbada51f19b857a4a8ef334aab211090abf4247194ddfeb1504df7420 in / 
# Wed, 13 Dec 2023 10:36:35 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:36:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:36:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:36:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:37:10 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:36:56 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:38:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:38:48 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:38:48 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:38:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jan 2024 22:22:53 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 24 Jan 2024 22:22:54 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:22:56 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 24 Jan 2024 22:22:56 GMT
WORKDIR /usr/local/tomcat
# Wed, 24 Jan 2024 22:22:56 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 24 Jan 2024 22:22:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 24 Jan 2024 22:22:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 24 Jan 2024 22:22:58 GMT
ENV TOMCAT_MAJOR=9
# Wed, 24 Jan 2024 22:22:58 GMT
ENV TOMCAT_VERSION=9.0.85
# Wed, 24 Jan 2024 22:22:59 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Wed, 24 Jan 2024 22:22:59 GMT
COPY dir:4124636d3ab4edd201f5937308f63f45ebff66c82f24456d8192a0b4d3b575b5 in /usr/local/tomcat 
# Wed, 24 Jan 2024 22:23:08 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 22:23:10 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 24 Jan 2024 22:23:11 GMT
EXPOSE 8080
# Wed, 24 Jan 2024 22:23:11 GMT
ENTRYPOINT []
# Wed, 24 Jan 2024 22:23:12 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3cdeaacd390f730da6f0fb692f91fa6acafd7c373cd75524447a25371b6cf3b5`  
		Last Modified: Sat, 16 Dec 2023 10:34:06 GMT  
		Size: 33.3 MB (33314320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed67c1e92d231797f6ccdb5b8dfc66523da0505bda01ed804febc7f69bbc165`  
		Last Modified: Sat, 16 Dec 2023 10:43:55 GMT  
		Size: 18.2 MB (18215112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eeac73eaef794d0fd2af66928b12804a6ba0b71293da470af27a789aa2bc9cd`  
		Last Modified: Wed, 24 Jan 2024 20:51:48 GMT  
		Size: 42.5 MB (42495535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31539ab1838f951211dc075c9756ac6712397a4179fdbd940f2f9945334b49d5`  
		Last Modified: Wed, 24 Jan 2024 20:51:42 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b887f7d4a5791377a1bd5cbc6e97573d931b6dc431bbc5f873321184c870374`  
		Last Modified: Wed, 24 Jan 2024 20:51:42 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177dbe62a598a8a866df25f3e1fb082638ebc9e5d9766cec788cd1b39dd6abe5`  
		Last Modified: Wed, 24 Jan 2024 22:52:49 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114830750ee9107f1616775216f2996c63a8a8e341b186a719f830daacc9d6ac`  
		Last Modified: Wed, 24 Jan 2024 22:52:50 GMT  
		Size: 12.5 MB (12509538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2586c2b588e5dc6dd86c76b03b2b06a5f79e9e05d637086d6fd71d951817a3`  
		Last Modified: Wed, 24 Jan 2024 22:52:49 GMT  
		Size: 475.2 KB (475215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031c94ece21f5c228b7346b9a5a7c430cc28eb0ee4ee83c5b0877a0483de473a`  
		Last Modified: Wed, 24 Jan 2024 22:52:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre11-temurin-focal` - linux; s390x

```console
$ docker pull tomcat@sha256:d4166635dc04d7c3859442d2eb76f50bfd314785ad492115afe403458cdf2120
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.4 MB (97354393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07080b635b5167a07eafdc92b813fe6066baa392e71ce7cf94583f5bcc96fb95`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 13 Dec 2023 10:31:17 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:31:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:31:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:31:17 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:31:19 GMT
ADD file:acb39119899edf16a81c2953b282eebb13d32feac981d3f40b60bdfc13ad7bb5 in / 
# Wed, 13 Dec 2023 10:31:20 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 07:43:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 07:43:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 07:43:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 07:44:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 07:44:04 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Sat, 16 Dec 2023 07:45:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8dc527e5c5da62f80ad3b6a2cd7b1789f745b1d90d5e83faba45f7a1d0b6cab8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='156861bb901ef18759e05f6f008595220c7d1318a46758531b957b0c950ef2c3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        armhf|arm)          ESUM='7c12ca8f195bf719368016a1c3e7f06f8f06e4a573dc3dce0befbe30a388ffa3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='286e37ce06316185377eea847d2aa9f1523b9f1428684e59e772f2f6055e89b9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='78f18503970715c03b8e6e70191d9001c883edab23d9f51ff434e4a03c6237bd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 07:45:21 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 07:45:21 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 07:45:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 09:10:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 16 Dec 2023 09:10:37 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 09:10:37 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 16 Dec 2023 09:10:37 GMT
WORKDIR /usr/local/tomcat
# Sat, 16 Dec 2023 09:10:37 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 16 Dec 2023 09:10:38 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 16 Dec 2023 09:10:38 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 16 Dec 2023 09:10:38 GMT
ENV TOMCAT_MAJOR=9
# Tue, 09 Jan 2024 22:58:46 GMT
ENV TOMCAT_VERSION=9.0.85
# Tue, 09 Jan 2024 22:58:46 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Tue, 23 Jan 2024 00:37:27 GMT
COPY dir:f79c0c859175e7a7c82507f365a9c0155d72109243da19939e6ee111fb13bee4 in /usr/local/tomcat 
# Tue, 23 Jan 2024 00:37:32 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jan 2024 00:37:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 23 Jan 2024 00:37:34 GMT
EXPOSE 8080
# Tue, 23 Jan 2024 00:37:34 GMT
ENTRYPOINT []
# Tue, 23 Jan 2024 00:37:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b17df547765b88177f27d934075b822d3ec46e7f985d1f46b83d63a5b1b34f48`  
		Last Modified: Sat, 16 Dec 2023 07:41:56 GMT  
		Size: 27.0 MB (27015634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bdb88c522b4fe32174d19039c96b0b7add60219bfad0039c5945cb1e3fd3cc`  
		Last Modified: Sat, 16 Dec 2023 07:48:21 GMT  
		Size: 16.6 MB (16643216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5579551d1e33073a7d3c9cca5c4c0be0e3e921c2f5f1146430af064623de00ba`  
		Last Modified: Sat, 16 Dec 2023 07:48:58 GMT  
		Size: 40.8 MB (40762462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2511da475703e2fdc8faea0ae946afe4ea5baac398fa556be43546a85f3a6ae6`  
		Last Modified: Sat, 16 Dec 2023 07:48:53 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110efd1482f212716f2a1085a13f6fac8f71e2497dfc7b01a574251631d8d996`  
		Last Modified: Sat, 16 Dec 2023 07:48:53 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f680fcf08f75c9d040eb9d2fc863758bf82da9ee8ad92678772c8c7e4f6c5d`  
		Last Modified: Sat, 16 Dec 2023 09:18:12 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8595168db0aea1f6868827a3992c69aa5a54ac54be846e7d1ca84b33434aa30f`  
		Last Modified: Tue, 23 Jan 2024 00:55:15 GMT  
		Size: 12.5 MB (12480308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edfc812c8924ed6ac83bb0932d9ecf033b38aeb010c2674bd6816596b67b085b`  
		Last Modified: Tue, 23 Jan 2024 00:55:14 GMT  
		Size: 451.6 KB (451577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e620d3f6d8bf7b7b650a0000dc2e7fe829ae93cea70a7f3b08467d89dab0bc3e`  
		Last Modified: Tue, 23 Jan 2024 00:55:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
