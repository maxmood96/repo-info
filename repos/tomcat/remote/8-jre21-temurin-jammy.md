## `tomcat:8-jre21-temurin-jammy`

```console
$ docker pull tomcat@sha256:bc3f750eab4534843c13ad12b61cabbf692824a1139d87495a104714c9812f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `tomcat:8-jre21-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:a6c7f0a79666119ab4efc74e18c5af33a619c1c5a81aff82fe4c406bcc8be4ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.3 MB (113311023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00d8aa85a11db2b0c992da8a29ef7ff91dc3d0d3b7f924fdad9043c9bf4d4403`
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
# Sat, 02 Dec 2023 02:01:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 02:01:53 GMT
ENV JAVA_VERSION=jdk-21.0.1+12
# Sat, 02 Dec 2023 02:02:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4582c4cc0c6d498ba7a23fdb0a5179c9d9c0d7a26f2ee8610468d5c2954fcf2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='277f4084bee875f127a978253cfbaad09c08df597feaf5ccc82d2206962279a3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jre_x64_linux_hotspot_21.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='05cc9b7bfbe246c27d307783b3d5095797be747184b168018ae3f7cc55608db2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 02 Dec 2023 02:02:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 02 Dec 2023 02:02:18 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 02 Dec 2023 02:02:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Dec 2023 08:18:12 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 02 Dec 2023 08:18:13 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 08:18:13 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 02 Dec 2023 08:18:13 GMT
WORKDIR /usr/local/tomcat
# Sat, 02 Dec 2023 08:18:13 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 02 Dec 2023 08:18:13 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 02 Dec 2023 08:27:48 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Sat, 02 Dec 2023 08:27:48 GMT
ENV TOMCAT_MAJOR=8
# Wed, 13 Dec 2023 02:11:35 GMT
ENV TOMCAT_VERSION=8.5.97
# Wed, 13 Dec 2023 02:11:35 GMT
ENV TOMCAT_SHA512=344ea91c95677fdc243bc58a1f8ab745117a80c0a458ae2e26ebc4f968e06c4bfffaf9a4aae52de3d72b945b05b6e03b7cfae98596c222cbe7d394d52363da86
# Wed, 13 Dec 2023 02:11:35 GMT
COPY dir:d34a0a222edfeba93ca26c632bf8a96e94db248ee34dddeeab9e3d1152ebf8c5 in /usr/local/tomcat 
# Wed, 13 Dec 2023 02:11:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2023 02:11:41 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Dec 2023 02:11:41 GMT
EXPOSE 8080
# Wed, 13 Dec 2023 02:11:41 GMT
ENTRYPOINT []
# Wed, 13 Dec 2023 02:11:41 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd63fc495d1a4839e5239c716fa5a6ec48209bff26db1e7d7af7b0701ac4ee7`  
		Last Modified: Sat, 02 Dec 2023 02:06:15 GMT  
		Size: 17.5 MB (17455452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4cbbc7af6726d0aead27fec4dfd36817357eef59971946f8fc3d86bd55278f8`  
		Last Modified: Sat, 02 Dec 2023 02:07:41 GMT  
		Size: 53.5 MB (53503204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d3f602482e8879611d6f84298437107d843623bb8eadea04aaa209d4c7ac06`  
		Last Modified: Sat, 02 Dec 2023 02:07:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c3cb3bde8de95b50f03e9f0b117b24f65dfad431acb713b6509aaefd29d65f`  
		Last Modified: Sat, 02 Dec 2023 02:07:34 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e387fa47428d6991f341e96bb75dd75d01a80ec67b8ceeb80f44a1712b801091`  
		Last Modified: Sat, 02 Dec 2023 08:36:10 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6df48b5fcadbf6144ed56e86c0ba668c226c303126b2eca261362d8e81a531`  
		Last Modified: Wed, 13 Dec 2023 02:34:17 GMT  
		Size: 11.4 MB (11446328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7617fbb397b4e29199e3874e0a3394a6059fe9badec2c0d2d82c738f17490e40`  
		Last Modified: Wed, 13 Dec 2023 02:34:17 GMT  
		Size: 458.5 KB (458522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2370ee23d963a1e980a875561789456b203f1106f01e210b7899bcc3043bed40`  
		Last Modified: Wed, 13 Dec 2023 02:34:16 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre21-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:2ca88f0b8df73d73e582b7c2b802e5be6bb6c3834e582ee9e6eee69aae7bebb1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111841734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69036ec0033327a25e565f6be6eb30512f4ef73ad8c92d5daa786b764522b8b`
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
# Sat, 02 Dec 2023 05:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:33:31 GMT
ENV JAVA_VERSION=jdk-21.0.1+12
# Sat, 02 Dec 2023 05:33:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4582c4cc0c6d498ba7a23fdb0a5179c9d9c0d7a26f2ee8610468d5c2954fcf2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='277f4084bee875f127a978253cfbaad09c08df597feaf5ccc82d2206962279a3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jre_x64_linux_hotspot_21.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='05cc9b7bfbe246c27d307783b3d5095797be747184b168018ae3f7cc55608db2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 02 Dec 2023 05:33:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 02 Dec 2023 05:33:55 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 02 Dec 2023 05:33:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Dec 2023 10:27:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 02 Dec 2023 10:27:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 10:27:06 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 02 Dec 2023 10:27:06 GMT
WORKDIR /usr/local/tomcat
# Sat, 02 Dec 2023 10:27:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 02 Dec 2023 10:27:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 02 Dec 2023 10:34:51 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Sat, 02 Dec 2023 10:34:51 GMT
ENV TOMCAT_MAJOR=8
# Wed, 13 Dec 2023 02:02:42 GMT
ENV TOMCAT_VERSION=8.5.97
# Wed, 13 Dec 2023 02:02:42 GMT
ENV TOMCAT_SHA512=344ea91c95677fdc243bc58a1f8ab745117a80c0a458ae2e26ebc4f968e06c4bfffaf9a4aae52de3d72b945b05b6e03b7cfae98596c222cbe7d394d52363da86
# Wed, 13 Dec 2023 02:02:43 GMT
COPY dir:cab8fab5581f32aac696b23a51b6c5a091c53d5f1c1d7ed7dec16ed843b85efc in /usr/local/tomcat 
# Wed, 13 Dec 2023 02:02:46 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2023 02:02:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Dec 2023 02:02:48 GMT
EXPOSE 8080
# Wed, 13 Dec 2023 02:02:48 GMT
ENTRYPOINT []
# Wed, 13 Dec 2023 02:02:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c3988b1198250f931d321166ff7a5f1bbd03b8fa06eae348c92ef639a62393`  
		Last Modified: Sat, 02 Dec 2023 05:37:12 GMT  
		Size: 18.9 MB (18857837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7d9da1b13d0ca36025baead8c030fb3a7dedf3e5a48cb3acc851a3e0ddc83a`  
		Last Modified: Sat, 02 Dec 2023 05:38:28 GMT  
		Size: 52.7 MB (52672873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb17612fb4a03f79db530ef0a95c75d4f7c2013f7222c752b79d9e288eec266`  
		Last Modified: Sat, 02 Dec 2023 05:38:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f464b720fa2e99e6457cd08bd6b073ca08129f82d63f1e7f8adcbb5056d3be`  
		Last Modified: Sat, 02 Dec 2023 05:38:21 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b55e1babf9d47aad23fd5f1c7c685294ccc4722b8477a9baab8350802220bb`  
		Last Modified: Sat, 02 Dec 2023 10:41:35 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20748e2a51cbe4bc7edc70bf55198c05cf9161109ce08a849ec02b10f2ddb9e5`  
		Last Modified: Wed, 13 Dec 2023 02:24:12 GMT  
		Size: 11.5 MB (11451684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f890757816b3279fc82c9a33208556dbb18cb2043743410c6c0094d81e99ed8a`  
		Last Modified: Wed, 13 Dec 2023 02:24:11 GMT  
		Size: 458.2 KB (458204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1842e9e68962b7fbaba8d6e41a8a7bc703d08365121d06b7887054e9e16ff28`  
		Last Modified: Wed, 13 Dec 2023 02:24:11 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre21-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:b6317387942d4ce00131f30693d7096e6df2684124f3612c1474137d49d9acd6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119608189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12def720eb50bd05f4441700617529f6b0d40aa99ba3fe07491bbcf2da1947c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2023 11:43:51 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:43:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:43:55 GMT
ADD file:bda128b553d54e39b55daceea1f0ad351c73f83835bbf65d10e5af879ce6fee7 in / 
# Tue, 12 Dec 2023 11:43:56 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:37:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:37:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:37:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:41:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:42:22 GMT
ENV JAVA_VERSION=jdk-21.0.1+12
# Sat, 16 Dec 2023 10:43:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4582c4cc0c6d498ba7a23fdb0a5179c9d9c0d7a26f2ee8610468d5c2954fcf2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='277f4084bee875f127a978253cfbaad09c08df597feaf5ccc82d2206962279a3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jre_x64_linux_hotspot_21.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='05cc9b7bfbe246c27d307783b3d5095797be747184b168018ae3f7cc55608db2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:43:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:43:02 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:43:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 12:47:53 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 16 Dec 2023 12:47:53 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 12:47:55 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 16 Dec 2023 12:47:55 GMT
WORKDIR /usr/local/tomcat
# Sat, 16 Dec 2023 12:47:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 16 Dec 2023 12:47:56 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 16 Dec 2023 13:07:33 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Sat, 16 Dec 2023 13:07:34 GMT
ENV TOMCAT_MAJOR=8
# Sat, 16 Dec 2023 13:07:34 GMT
ENV TOMCAT_VERSION=8.5.97
# Sat, 16 Dec 2023 13:07:35 GMT
ENV TOMCAT_SHA512=344ea91c95677fdc243bc58a1f8ab745117a80c0a458ae2e26ebc4f968e06c4bfffaf9a4aae52de3d72b945b05b6e03b7cfae98596c222cbe7d394d52363da86
# Sat, 16 Dec 2023 13:07:35 GMT
COPY dir:20747b7a36cde4b36a7274e5d441b252cd741a3763758775b6955fae0d8b7861 in /usr/local/tomcat 
# Sat, 16 Dec 2023 13:07:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 13:07:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 16 Dec 2023 13:07:44 GMT
EXPOSE 8080
# Sat, 16 Dec 2023 13:07:45 GMT
ENTRYPOINT []
# Sat, 16 Dec 2023 13:07:45 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7775720178c79208fc0d1b977c06891ef7230f39bc02e948d233c49f8a202fcf`  
		Last Modified: Sat, 16 Dec 2023 10:35:18 GMT  
		Size: 35.7 MB (35655287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5ea4a2de03097449e4184f8073a7b1f99cbf72be7cc99200a31a650ddc5512`  
		Last Modified: Sat, 16 Dec 2023 10:46:55 GMT  
		Size: 18.7 MB (18724047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc2e6fe56fd60175469e1f8709dd16b88d50a36c35bd82f4e0888290fb6972c`  
		Last Modified: Sat, 16 Dec 2023 10:48:25 GMT  
		Size: 53.3 MB (53264482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03bc7dd6d5c65b5f1d1bba46d6624ce4ea080d6e6d25774a25b2a57604141611`  
		Last Modified: Sat, 16 Dec 2023 10:48:17 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d354538b92fa2c9667e742771fd492980fd2eb519898d461046d5087f632d2`  
		Last Modified: Sat, 16 Dec 2023 10:48:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4d793cbb0ed08e74c28e3bbca4c466d6c26dc4a8d1450a95b4de41006edf49`  
		Last Modified: Sat, 16 Dec 2023 13:20:56 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3434d0816a4d44dfca1db1483a7f53dd0e94fec86b57cfd84a89b20d37544cb0`  
		Last Modified: Sat, 16 Dec 2023 13:30:26 GMT  
		Size: 11.5 MB (11473623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9413520589140bb01fb233e6a93c5330c295f40e2ee73ed484dcd97c7bf93bdb`  
		Last Modified: Sat, 16 Dec 2023 13:30:25 GMT  
		Size: 489.6 KB (489553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c7b84c0e047a2c6341eac7c248799dfd7864b15582862a3a4b4ae236b68cd2`  
		Last Modified: Sat, 16 Dec 2023 13:30:25 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
