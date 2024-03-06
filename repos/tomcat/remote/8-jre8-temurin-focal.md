## `tomcat:8-jre8-temurin-focal`

```console
$ docker pull tomcat@sha256:98689d23759e9e8d09a9957c8e0bc3de24c0b6ae1cf6d19d1486d75cc02619e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `tomcat:8-jre8-temurin-focal` - linux; amd64

```console
$ docker pull tomcat@sha256:fd27ac285244890ec24bfb4309b78d1761875b076a191a4c5bd1db31809d533e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101245626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e466b595fb693a0e6f6d234b652c016e90ddbffb04a8e9e6c03665613ea2050`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:41:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 07:41:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 07:41:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 07:42:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 07:42:14 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Fri, 02 Feb 2024 07:42:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='782f842c22fe660c5acbea8c1d7b4e812fe658a9e48cd2e8e776d088c7ab32d3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1d8c109e96bdb35ffff667dfb911ce03fb9f0f924048dcc8fdbd45198b263ecd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='d613a775573fc17ee972e62b5120dc34d8cac1810bb352e71bc01980ce3c48a8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='dd828b761805c2caecac94fcab8ea39cdf41480f07053553dc37edde104861af';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 02 Feb 2024 07:42:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete."
# Fri, 02 Feb 2024 07:42:59 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 02 Feb 2024 07:42:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 02 Feb 2024 12:33:13 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 02 Feb 2024 12:33:13 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 12:33:13 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 02 Feb 2024 12:33:13 GMT
WORKDIR /usr/local/tomcat
# Fri, 02 Feb 2024 12:33:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 02 Feb 2024 12:33:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 02 Feb 2024 12:42:31 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 02 Feb 2024 12:42:31 GMT
ENV TOMCAT_MAJOR=8
# Wed, 21 Feb 2024 01:24:51 GMT
ENV TOMCAT_VERSION=8.5.99
# Wed, 21 Feb 2024 01:24:51 GMT
ENV TOMCAT_SHA512=38f636039d00c66ff8f7347dfedcc1eef85b7ce25cf98dcc9192df07f85d4f6aec447922e0f934c1ab7d099ec484b2060aad4de496d5ca14637ac435cb55b7c0
# Wed, 21 Feb 2024 01:24:51 GMT
COPY dir:2a242279baa04d461d0b59f010d0879f2604a7a498932298a13026388021183f in /usr/local/tomcat 
# Wed, 21 Feb 2024 01:24:57 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Feb 2024 01:24:58 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 21 Feb 2024 01:24:58 GMT
EXPOSE 8080
# Wed, 21 Feb 2024 01:24:58 GMT
ENTRYPOINT []
# Wed, 21 Feb 2024 01:24:58 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3c67549075b6db92af85c8649f848d697b5bb1f448b436c4b4d6ee6834ab45f7`  
		Last Modified: Tue, 23 Jan 2024 18:44:22 GMT  
		Size: 28.6 MB (28584460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482e8906db891635177f51c396548100ceb210499ac8ae3e9f43b9b647dc8dc4`  
		Last Modified: Fri, 02 Feb 2024 07:47:19 GMT  
		Size: 16.9 MB (16923425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a26e4e4a2714b93600b2f50068ae305dd6424ae38fd77135980402bf602a399`  
		Last Modified: Fri, 02 Feb 2024 07:48:02 GMT  
		Size: 41.8 MB (41847538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6e9b2ffdd48e2e5f71cf46ab4de405564814d061558a41c2613aa07c985648`  
		Last Modified: Fri, 02 Feb 2024 07:47:57 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d710ee2636621dccb28e72016664ddb5be9e35cfb9bf53daeeb225651f89c6`  
		Last Modified: Fri, 02 Feb 2024 07:47:57 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b58e8f3ae20c8cc3107d77235cd74692ed50964911d2458ee11ac4ee36fa55`  
		Last Modified: Fri, 02 Feb 2024 12:54:54 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd72e44620a70e561ca120949d00e8bc0dc416b434e900cdaeb2f21f124a33f3`  
		Last Modified: Wed, 21 Feb 2024 01:44:18 GMT  
		Size: 11.5 MB (11531749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82668ef6c425941bb9f6b566e943df641715a6c93ddca0cef83b8e0a31db658`  
		Last Modified: Wed, 21 Feb 2024 01:44:17 GMT  
		Size: 2.4 MB (2357256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9d5baccad8de7ec5b42f080a7cecedda227265594e999d1f4fb8cff19b23ed`  
		Last Modified: Wed, 21 Feb 2024 01:44:17 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-temurin-focal` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:edb3f8d6b6965707216340935d0e2577424e592983fdf25151ca204041e3c1fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91744664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592471c5210d973384737f31de40831fc7b3beffd04da941196275fd996a66f8`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 16 Feb 2024 19:13:06 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:13:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:13:14 GMT
ADD file:66096c88a70dfe9ed5e8eb12f0baffb429f0baba39540262b8339b6de267a8bc in / 
# Fri, 16 Feb 2024 19:13:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:14:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 02:14:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 02:14:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 02:15:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:15:56 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 06 Mar 2024 02:17:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='782f842c22fe660c5acbea8c1d7b4e812fe658a9e48cd2e8e776d088c7ab32d3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1d8c109e96bdb35ffff667dfb911ce03fb9f0f924048dcc8fdbd45198b263ecd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='d613a775573fc17ee972e62b5120dc34d8cac1810bb352e71bc01980ce3c48a8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='dd828b761805c2caecac94fcab8ea39cdf41480f07053553dc37edde104861af';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 06 Mar 2024 02:17:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete."
# Wed, 06 Mar 2024 02:17:56 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 02:17:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 05:00:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Mar 2024 05:00:54 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 05:00:54 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 06 Mar 2024 05:00:54 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Mar 2024 05:00:54 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Mar 2024 05:00:54 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Mar 2024 05:06:16 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 06 Mar 2024 05:06:16 GMT
ENV TOMCAT_MAJOR=8
# Wed, 06 Mar 2024 05:06:16 GMT
ENV TOMCAT_VERSION=8.5.99
# Wed, 06 Mar 2024 05:06:16 GMT
ENV TOMCAT_SHA512=38f636039d00c66ff8f7347dfedcc1eef85b7ce25cf98dcc9192df07f85d4f6aec447922e0f934c1ab7d099ec484b2060aad4de496d5ca14637ac435cb55b7c0
# Wed, 06 Mar 2024 05:06:16 GMT
COPY dir:f5c7adf9ce0fa74c5f5143e6914802d42da7ec8ff1aa25568d28f43d8d93a19e in /usr/local/tomcat 
# Wed, 06 Mar 2024 05:06:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 05:06:22 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 06 Mar 2024 05:06:22 GMT
EXPOSE 8080
# Wed, 06 Mar 2024 05:06:22 GMT
ENTRYPOINT []
# Wed, 06 Mar 2024 05:06:22 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a57ab8f3f909fb2a530a207c0b93b306ab27641c9c91ca7906af7d1eb85594c3`  
		Last Modified: Wed, 06 Mar 2024 02:22:43 GMT  
		Size: 24.6 MB (24601340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595349879de0f9f196cebe56b48885bb6d3f4f56b496316b5c65d2657766b1d4`  
		Last Modified: Wed, 06 Mar 2024 02:22:43 GMT  
		Size: 15.7 MB (15664491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c78015ed865e17b50a552e417eec9a7a4776e742f7f30c61d118387baa2731d`  
		Last Modified: Wed, 06 Mar 2024 02:23:35 GMT  
		Size: 39.6 MB (39570280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88667e03e06f213e42d7cd421705c649e3609d51013641ec2dab3ccd38910fc`  
		Last Modified: Wed, 06 Mar 2024 02:23:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c046438ec1627840bf3f2157870c81a30ff8a0671e8c6c700ad1fd4eb3d384`  
		Last Modified: Wed, 06 Mar 2024 02:23:28 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fc0e6de27c84a60be233a133530aa9fdaf7788503173e19f7a172aadccb799`  
		Last Modified: Wed, 06 Mar 2024 05:13:37 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56bd9a39e5bc8e1ad499343f0e45eead78ea75224f061d45d0456b75295eca8`  
		Last Modified: Wed, 06 Mar 2024 05:17:45 GMT  
		Size: 11.5 MB (11481299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b89b3a648f9978efee6af7c460d2ec301168b74d5f03de7dc441d25322c9c2c`  
		Last Modified: Wed, 06 Mar 2024 05:17:43 GMT  
		Size: 426.1 KB (426062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d900fcdae65e1631baf7bef5793ea015bbae2357aabc3e304c500cb1ef2556`  
		Last Modified: Wed, 06 Mar 2024 05:17:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-temurin-focal` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:b69290c2ef61f07a1f4c9969d9da9f892b371139c48d21473d27daec0893f657
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96834036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54852ec317f701fdf9147fc98cd4a64048e7a35c6af8e7607c6e30923eca1ec0`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:01:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:01:28 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 06 Mar 2024 04:02:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='782f842c22fe660c5acbea8c1d7b4e812fe658a9e48cd2e8e776d088c7ab32d3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1d8c109e96bdb35ffff667dfb911ce03fb9f0f924048dcc8fdbd45198b263ecd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='d613a775573fc17ee972e62b5120dc34d8cac1810bb352e71bc01980ce3c48a8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='dd828b761805c2caecac94fcab8ea39cdf41480f07053553dc37edde104861af';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 06 Mar 2024 04:02:07 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete."
# Wed, 06 Mar 2024 04:02:07 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:02:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 11:31:36 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Mar 2024 11:31:36 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 11:31:37 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 06 Mar 2024 11:31:37 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Mar 2024 11:31:37 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Mar 2024 11:31:37 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Mar 2024 11:36:36 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 06 Mar 2024 11:36:36 GMT
ENV TOMCAT_MAJOR=8
# Wed, 06 Mar 2024 11:36:37 GMT
ENV TOMCAT_VERSION=8.5.99
# Wed, 06 Mar 2024 11:36:37 GMT
ENV TOMCAT_SHA512=38f636039d00c66ff8f7347dfedcc1eef85b7ce25cf98dcc9192df07f85d4f6aec447922e0f934c1ab7d099ec484b2060aad4de496d5ca14637ac435cb55b7c0
# Wed, 06 Mar 2024 11:36:37 GMT
COPY dir:084dc5808915aa5f006a47ddfd7df5932bd60ba762c557dc4de50d7802a971cb in /usr/local/tomcat 
# Wed, 06 Mar 2024 11:36:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 11:36:41 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 06 Mar 2024 11:36:41 GMT
EXPOSE 8080
# Wed, 06 Mar 2024 11:36:41 GMT
ENTRYPOINT []
# Wed, 06 Mar 2024 11:36:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0a04947909c099b173952314803a70e7ae9640298963e105b05c6aeb169e48`  
		Last Modified: Wed, 06 Mar 2024 04:05:32 GMT  
		Size: 16.8 MB (16776928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999e4a9bae01af669f3251f3413be12db5f9d24c1b86580dc33b8b752b774ff7`  
		Last Modified: Wed, 06 Mar 2024 04:06:09 GMT  
		Size: 40.9 MB (40853635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe30f732d49208745e34357341e8b85ddaf5a4c07aabe5a848e95200cebc5c1`  
		Last Modified: Wed, 06 Mar 2024 04:06:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57dce08b81f1ea3c02b14bae10986b042a9b49cb9e4c7023aed796b0baed5421`  
		Last Modified: Wed, 06 Mar 2024 04:06:06 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e305527906d71c53d406743f413fac60d1244f5c3dd889c7744684355f7fda2`  
		Last Modified: Wed, 06 Mar 2024 11:47:02 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7716bf016c47d6d308405ab773fba27cef794864f68954e2489cea861ee28cdc`  
		Last Modified: Wed, 06 Mar 2024 11:51:25 GMT  
		Size: 11.5 MB (11548766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182fdb5ef8558dc9dd863ac4f86823e36585bc59aa5e76d51a5faaccb1529c8e`  
		Last Modified: Wed, 06 Mar 2024 11:51:25 GMT  
		Size: 449.2 KB (449227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff67beefbac55bd95a6b7eb43cac0b5d1ef386a8caa54bd248e746b3e4e3a56`  
		Last Modified: Wed, 06 Mar 2024 11:51:24 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-temurin-focal` - linux; ppc64le

```console
$ docker pull tomcat@sha256:1d7b943aa3ad7b1dbbb3e165fb25b30c2f6c3a33ca068c16d6b503436a28ffd8
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104830778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54d231f59540ba7b21c0fb066462f085153cd45d89a1fa90e725640b8ddadf0`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 16 Feb 2024 19:14:37 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:14:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:14:40 GMT
ADD file:e8a9147477810033be455b6d05074e33f9e64458087ca10e58dbc087c80e00ad in / 
# Fri, 16 Feb 2024 19:14:40 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 01:35:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 01:35:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 01:35:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 01:36:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 01:36:20 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 06 Mar 2024 01:38:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='782f842c22fe660c5acbea8c1d7b4e812fe658a9e48cd2e8e776d088c7ab32d3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1d8c109e96bdb35ffff667dfb911ce03fb9f0f924048dcc8fdbd45198b263ecd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='d613a775573fc17ee972e62b5120dc34d8cac1810bb352e71bc01980ce3c48a8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='dd828b761805c2caecac94fcab8ea39cdf41480f07053553dc37edde104861af';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 06 Mar 2024 01:38:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete."
# Wed, 06 Mar 2024 01:38:08 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 01:38:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 04:45:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Mar 2024 04:45:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:45:05 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 06 Mar 2024 04:45:05 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Mar 2024 04:45:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Mar 2024 04:45:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Mar 2024 05:07:40 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 06 Mar 2024 05:07:41 GMT
ENV TOMCAT_MAJOR=8
# Wed, 06 Mar 2024 05:07:42 GMT
ENV TOMCAT_VERSION=8.5.99
# Wed, 06 Mar 2024 05:07:43 GMT
ENV TOMCAT_SHA512=38f636039d00c66ff8f7347dfedcc1eef85b7ce25cf98dcc9192df07f85d4f6aec447922e0f934c1ab7d099ec484b2060aad4de496d5ca14637ac435cb55b7c0
# Wed, 06 Mar 2024 05:07:43 GMT
COPY dir:949b0a0d46741fb9b0b9e5b99afd9f672d04404b230bb87dc25a465896a0417a in /usr/local/tomcat 
# Wed, 06 Mar 2024 05:07:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 05:07:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 06 Mar 2024 05:07:57 GMT
EXPOSE 8080
# Wed, 06 Mar 2024 05:07:58 GMT
ENTRYPOINT []
# Wed, 06 Mar 2024 05:07:59 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ecb7dea5440f763917c4b75b3f00c2617649ca914e65b3e965c37d6eb1e0dfde`  
		Last Modified: Wed, 06 Mar 2024 01:44:24 GMT  
		Size: 33.3 MB (33315609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4d55e3340199746793d8c4c58c09f654f25a0a60cb36294c7dd2576d680c64`  
		Last Modified: Wed, 06 Mar 2024 01:44:22 GMT  
		Size: 18.2 MB (18222197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a0d895b7173fdb95b95cf772681adb9906af4f9451b01402cde8931e6db9c4`  
		Last Modified: Wed, 06 Mar 2024 01:45:09 GMT  
		Size: 41.2 MB (41242094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17685ac51e1e684dff4541ff49660c209cbbdba0948c810b310c891fa31951b`  
		Last Modified: Wed, 06 Mar 2024 01:45:04 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27be1bd68861ca64d77aff9047ce963e179cea284f8c87b696917bbb1a8d5592`  
		Last Modified: Wed, 06 Mar 2024 01:45:04 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4210c467f16270b71223931a38a07d021b0ef0f835825276213c7b7204b7878`  
		Last Modified: Wed, 06 Mar 2024 05:20:18 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ed9cc24bf71f5c10afb04227b9d296e47052329edd1100f221c911a8e486fc`  
		Last Modified: Wed, 06 Mar 2024 05:25:34 GMT  
		Size: 11.6 MB (11574558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff61a86b8a125a01299be7cf286f78f9b19e14bb507574d82dea601230941300`  
		Last Modified: Wed, 06 Mar 2024 05:25:33 GMT  
		Size: 475.1 KB (475121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4679de14c854f3ea5dc09f6b83396992fb987b7631229400dcd7b007c1e875`  
		Last Modified: Wed, 06 Mar 2024 05:25:33 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
