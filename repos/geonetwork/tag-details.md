<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `geonetwork`

-	[`geonetwork:3`](#geonetwork3)
-	[`geonetwork:3-postgres`](#geonetwork3-postgres)
-	[`geonetwork:3.12`](#geonetwork312)
-	[`geonetwork:3.12-postgres`](#geonetwork312-postgres)
-	[`geonetwork:3.12.8`](#geonetwork3128)
-	[`geonetwork:3.12.8-postgres`](#geonetwork3128-postgres)
-	[`geonetwork:4`](#geonetwork4)
-	[`geonetwork:4.0`](#geonetwork40)
-	[`geonetwork:4.0.6`](#geonetwork406)
-	[`geonetwork:4.2`](#geonetwork42)
-	[`geonetwork:4.2.2`](#geonetwork422)
-	[`geonetwork:latest`](#geonetworklatest)

## `geonetwork:3`

```console
$ docker pull geonetwork@sha256:e65d5bd59e79cf103cc7b2e2e5ff8654531960e7112972dd55bf21d50a45ecd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `geonetwork:3` - linux; amd64

```console
$ docker pull geonetwork@sha256:29146d40a5747bd69c038c91efb04f41a1b8c9d38c2f29fbf3b7f4680e827d12
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.2 MB (424218056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814e47edd8412a88b1b03ae0f825249d2734f7a95eff8d346767db2867144fe0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:30 GMT
ADD file:481dd2da6de71525248eba186feeeafcc73cc956ade0a196a4e8b0c2424e74b9 in / 
# Fri, 09 Dec 2022 01:20:31 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:42:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 01:42:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 01:42:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 01:43:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 19:20:07 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 19:20:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 19:20:13 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 20:36:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 25 Jan 2023 20:36:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 20:36:38 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 25 Jan 2023 20:36:38 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 20:36:38 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 20:36:38 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 20:38:55 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 25 Jan 2023 20:38:55 GMT
ENV TOMCAT_MAJOR=8
# Wed, 25 Jan 2023 20:38:55 GMT
ENV TOMCAT_VERSION=8.5.85
# Wed, 25 Jan 2023 20:38:55 GMT
ENV TOMCAT_SHA512=0fc44133aff9e7e31d6dbb4b6e204d33bd0009b6bd089e5f8c8a1f7dfe7c5feff25d7f6404c4a3c5610e0960b5d0198580171212a2636816a23e21799a4c0467
# Wed, 25 Jan 2023 20:39:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 25 Jan 2023 20:39:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 25 Jan 2023 20:39:29 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 20:39:30 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 21:39:40 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 21:39:40 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Wed, 25 Jan 2023 21:39:40 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Wed, 25 Jan 2023 21:39:40 GMT
ENV GN_VERSION=3.12.8
# Wed, 25 Jan 2023 21:39:41 GMT
ENV GN_DOWNLOAD_MD5=378b70ee5c358a8db5659dafc8220e9f
# Wed, 25 Jan 2023 21:39:41 GMT
WORKDIR /usr/local/tomcat/webapps
# Wed, 25 Jan 2023 21:40:55 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Wed, 25 Jan 2023 21:40:56 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Wed, 25 Jan 2023 21:40:56 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 21:40:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 21:40:56 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6e3729cf69e0ce2de9e779575a1fec8b7fb5efdfa822829290ab6d5d1bc3e797`  
		Last Modified: Thu, 08 Dec 2022 14:10:00 GMT  
		Size: 30.4 MB (30428708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96aa423488f0ed1e9bf6c6da11fa7fb53568d1ea4003892416b3adeccb47e3bf`  
		Last Modified: Fri, 09 Dec 2022 01:50:02 GMT  
		Size: 12.4 MB (12432218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7d768530ca9e5fcde3ff9db86652aec33ca22d38cd93adf6b52e40581a32ec`  
		Last Modified: Wed, 25 Jan 2023 19:26:26 GMT  
		Size: 54.6 MB (54635670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34735e297c951328bfe5ea0366c1200ceb015ac7c2f3bc7a350ff51c091bdafc`  
		Last Modified: Wed, 25 Jan 2023 19:26:20 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc2293174b5fe65d5f09e90ee0968d1590e96081a18a16f3e7d8b58cd996396`  
		Last Modified: Wed, 25 Jan 2023 20:44:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adaadf54074ee75672402b6e9776bdb23c575e6c17654c9a9202a6ea5a99a3d7`  
		Last Modified: Wed, 25 Jan 2023 20:46:40 GMT  
		Size: 12.2 MB (12165261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa82b2c64abca8bf74d499d8e94ab0277da5e3401e1c5a54a0b1f34fd431876`  
		Last Modified: Wed, 25 Jan 2023 20:46:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4205adafee91900d19c8b5f81bff94eb7f5a4d1c2e030a505b18f8a5cfde449e`  
		Last Modified: Wed, 25 Jan 2023 21:43:54 GMT  
		Size: 314.6 MB (314555486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad6a999142d78c3f2d1e8dff65b7934b8f93a786de055c038a30b0bea5d4339`  
		Last Modified: Wed, 25 Jan 2023 21:43:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:5faae4f1b2f2894cbde64ab532394743e4e518c11d0bcc8c4cb84a0d7d8c9f8b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.9 MB (415866069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060474eec632cb6133da959006f3da3ffb0a72084de107ccd9453f3623a1c56d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Dec 2022 01:36:30 GMT
ADD file:ca82b3c78a23b75345429f192c4b1f88b4e49e12808c85fccc2db04823c17d4e in / 
# Fri, 09 Dec 2022 01:36:30 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:08:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 03:08:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 03:08:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 03:08:17 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 20:43:47 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 20:44:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 20:44:07 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 21:37:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 25 Jan 2023 21:37:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 21:37:06 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 25 Jan 2023 21:37:06 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 21:37:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 21:37:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 21:40:12 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 25 Jan 2023 21:40:12 GMT
ENV TOMCAT_MAJOR=8
# Wed, 25 Jan 2023 21:40:12 GMT
ENV TOMCAT_VERSION=8.5.85
# Wed, 25 Jan 2023 21:40:12 GMT
ENV TOMCAT_SHA512=0fc44133aff9e7e31d6dbb4b6e204d33bd0009b6bd089e5f8c8a1f7dfe7c5feff25d7f6404c4a3c5610e0960b5d0198580171212a2636816a23e21799a4c0467
# Wed, 25 Jan 2023 21:40:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 25 Jan 2023 21:40:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 25 Jan 2023 21:40:49 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 21:40:49 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 22:16:51 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 22:16:51 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Wed, 25 Jan 2023 22:16:51 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Wed, 25 Jan 2023 22:16:51 GMT
ENV GN_VERSION=3.12.8
# Wed, 25 Jan 2023 22:16:51 GMT
ENV GN_DOWNLOAD_MD5=378b70ee5c358a8db5659dafc8220e9f
# Wed, 25 Jan 2023 22:16:51 GMT
WORKDIR /usr/local/tomcat/webapps
# Wed, 25 Jan 2023 22:17:38 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Wed, 25 Jan 2023 22:17:39 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Wed, 25 Jan 2023 22:17:39 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 22:17:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 22:17:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c38006c9acc492149d706593acba951110798e57a7ad05103ae7a2d5969c14b6`  
		Last Modified: Thu, 08 Dec 2022 18:49:27 GMT  
		Size: 27.0 MB (27023448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c75c90d8ac3bc54f87b6716d34d23742433f988c00aef47001964698038d79`  
		Last Modified: Fri, 09 Dec 2022 03:17:28 GMT  
		Size: 12.0 MB (11993622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6225f767c4a3b305ad8e5712ff3988f6291b43765adfb5e8e2778d341cf1086a`  
		Last Modified: Wed, 25 Jan 2023 20:49:37 GMT  
		Size: 50.3 MB (50294599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff09de9a10ff310613b84e648fcbcb168aac2c6f6fa63ffbd10d58c2fa7e456`  
		Last Modified: Wed, 25 Jan 2023 20:49:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5eef20df6de484799bde83de7708971f47706816120d0eeef076792236116b`  
		Last Modified: Wed, 25 Jan 2023 21:53:37 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5684a0ac10b93a9edd850e0ef1b45dc27c041473e8da9b30ee3d7476d8ac3d`  
		Last Modified: Wed, 25 Jan 2023 21:56:06 GMT  
		Size: 12.0 MB (12011921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4871ddb7ff0457ccf99d037ab19a6b0eb2bf2acc1533cd12cf027639363010`  
		Last Modified: Wed, 25 Jan 2023 21:56:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40cc0824716930a424bb0173ada203ca572e0b3faf69828170e703a04a8c248d`  
		Last Modified: Wed, 25 Jan 2023 22:19:00 GMT  
		Size: 314.5 MB (314541834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad21ac3b46e8b54a4d8b7a30971c3aee438c6115c30f9dcc238c949e2eee0eb`  
		Last Modified: Wed, 25 Jan 2023 22:18:30 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:10b1d64ce2aefa123affbb4b436687887fda0e6e688df3858d4aa74f5329984a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.8 MB (420755552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7be106d5cf048d1e70c7b289cdba4dba797ec6eb6fa19d07ac602724aa597a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 26 Jan 2023 05:05:49 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:05:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:05:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:05:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:05:51 GMT
ADD file:55486a91f732042dd4e81ecfd8457d23e04dcd7dd80a0bb06cc7c44873fac838 in / 
# Thu, 26 Jan 2023 05:05:51 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:43:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Jan 2023 17:43:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 17:43:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Jan 2023 17:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:44:32 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Tue, 31 Jan 2023 17:44:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 31 Jan 2023 17:44:38 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 31 Jan 2023 22:17:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 31 Jan 2023 22:17:17 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 22:17:18 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 31 Jan 2023 22:17:18 GMT
WORKDIR /usr/local/tomcat
# Tue, 31 Jan 2023 22:17:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 31 Jan 2023 22:17:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 31 Jan 2023 22:21:26 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 31 Jan 2023 22:21:26 GMT
ENV TOMCAT_MAJOR=8
# Tue, 31 Jan 2023 22:21:26 GMT
ENV TOMCAT_VERSION=8.5.85
# Tue, 31 Jan 2023 22:21:26 GMT
ENV TOMCAT_SHA512=0fc44133aff9e7e31d6dbb4b6e204d33bd0009b6bd089e5f8c8a1f7dfe7c5feff25d7f6404c4a3c5610e0960b5d0198580171212a2636816a23e21799a4c0467
# Tue, 31 Jan 2023 22:21:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 31 Jan 2023 22:21:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 31 Jan 2023 22:21:56 GMT
EXPOSE 8080
# Tue, 31 Jan 2023 22:21:56 GMT
CMD ["catalina.sh" "run"]
# Wed, 01 Feb 2023 00:07:22 GMT
ENV GN_FILE=geonetwork.war
# Wed, 01 Feb 2023 00:07:22 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Wed, 01 Feb 2023 00:07:22 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Wed, 01 Feb 2023 00:07:22 GMT
ENV GN_VERSION=3.12.8
# Wed, 01 Feb 2023 00:07:22 GMT
ENV GN_DOWNLOAD_MD5=378b70ee5c358a8db5659dafc8220e9f
# Wed, 01 Feb 2023 00:07:23 GMT
WORKDIR /usr/local/tomcat/webapps
# Wed, 01 Feb 2023 00:07:51 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Wed, 01 Feb 2023 00:07:54 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Wed, 01 Feb 2023 00:07:54 GMT
WORKDIR /usr/local/tomcat
# Wed, 01 Feb 2023 00:07:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Feb 2023 00:07:54 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:565cb979c5c01279efcd69c4457a9954801b6be6da65894374260ec92d993891`  
		Last Modified: Thu, 26 Jan 2023 16:22:40 GMT  
		Size: 28.4 MB (28384974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c6471d4f305436bdd6e09ea64bdf7a303979f4d8cdb6c9606715fc21afa9ad`  
		Last Modified: Tue, 31 Jan 2023 17:50:26 GMT  
		Size: 12.4 MB (12391264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427df1d8bddcc93bab1efadcf6f2157f2d58b6366e437f130fb7ad8676a8a64f`  
		Last Modified: Tue, 31 Jan 2023 17:50:30 GMT  
		Size: 53.7 MB (53731740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1db467a77eb3093981e70f61997b6ade2c0b5662ace92eef00c082999f55dd6`  
		Last Modified: Tue, 31 Jan 2023 17:50:24 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7899e6f25670a980cf6b742a0443e29000441ee96c6e5189434396b495bd94bd`  
		Last Modified: Tue, 31 Jan 2023 22:33:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a6489f84d41cef926fc329042d2b342b71eea669b80dfaaba20df41ab717d2`  
		Last Modified: Tue, 31 Jan 2023 22:37:21 GMT  
		Size: 11.7 MB (11700782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde69c27b4cbedaf2799b7e23125b3a7df2b63dcd80268f9dded343986b26651`  
		Last Modified: Tue, 31 Jan 2023 22:37:20 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cc6e867e17538390665f99ad6fbc71809c09b4d6b59c2ed851480589821fc6`  
		Last Modified: Wed, 01 Feb 2023 00:11:48 GMT  
		Size: 314.5 MB (314546078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89beff1eb4faa366b06d9e01c3a457d27f611d3a9203a30f3544ca2055b3278e`  
		Last Modified: Wed, 01 Feb 2023 00:11:33 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:7242688e69127a437ec00c17ecd8431da6086daa0904b9305d5fbebc5c456f9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.0 MB (428010745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e240b213a31ebbcf618fda3f7722313d8fd3203266ffaf505ec3ef59cac04d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Dec 2022 01:27:53 GMT
ADD file:1a2557b357a1dca8521ee846ec16c9b2bd8a53839b9d4fda21a28f9ceeecb4b7 in / 
# Fri, 09 Dec 2022 01:27:55 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:39:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 02:39:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 02:39:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 02:40:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 19:38:40 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 19:38:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 19:38:54 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 20:49:25 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 25 Jan 2023 20:49:25 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 20:49:27 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 25 Jan 2023 20:49:27 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 20:49:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 20:49:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 20:53:23 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 25 Jan 2023 20:53:23 GMT
ENV TOMCAT_MAJOR=8
# Wed, 25 Jan 2023 20:53:23 GMT
ENV TOMCAT_VERSION=8.5.85
# Wed, 25 Jan 2023 20:53:24 GMT
ENV TOMCAT_SHA512=0fc44133aff9e7e31d6dbb4b6e204d33bd0009b6bd089e5f8c8a1f7dfe7c5feff25d7f6404c4a3c5610e0960b5d0198580171212a2636816a23e21799a4c0467
# Wed, 25 Jan 2023 20:54:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 25 Jan 2023 20:54:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 25 Jan 2023 20:54:28 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 20:54:28 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 21:24:58 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 21:24:58 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Wed, 25 Jan 2023 21:24:58 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Wed, 25 Jan 2023 21:24:59 GMT
ENV GN_VERSION=3.12.8
# Wed, 25 Jan 2023 21:24:59 GMT
ENV GN_DOWNLOAD_MD5=378b70ee5c358a8db5659dafc8220e9f
# Wed, 25 Jan 2023 21:24:59 GMT
WORKDIR /usr/local/tomcat/webapps
# Wed, 25 Jan 2023 21:25:44 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Wed, 25 Jan 2023 21:25:49 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Wed, 25 Jan 2023 21:25:50 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 21:25:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 21:25:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ce75b47e476cd75b30dca46558ac79b39923aa94d7e4b0cc025e521404cdbab0`  
		Last Modified: Fri, 09 Dec 2022 01:30:32 GMT  
		Size: 35.7 MB (35708154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a782dc6ae3d6a01674486598e1b3cdcfaa9696ad3e2125e712884667b1c2c37f`  
		Last Modified: Fri, 09 Dec 2022 02:53:02 GMT  
		Size: 13.2 MB (13245456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f293f07451d1ca9101f6406ed167fb8798e49df8ddf8acee518c3db37b0b185`  
		Last Modified: Wed, 25 Jan 2023 19:57:54 GMT  
		Size: 52.1 MB (52112863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44c8bdf138d6084aeef40083fb29771e2cf786714a4d644ae79155891980939`  
		Last Modified: Wed, 25 Jan 2023 19:57:43 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4377ec606c42192ec93ed57b0a6a47b5cf42197a7550956938bebe5b2af38092`  
		Last Modified: Wed, 25 Jan 2023 21:05:49 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7c80c538568990206ee80f8a97620c122e77bc741305edeb516e087a766ff0`  
		Last Modified: Wed, 25 Jan 2023 21:08:11 GMT  
		Size: 12.4 MB (12351915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42be51b9cbf813f7af62d54e2a22d3f530d0d10a7dcfdfc3d0c9fb60f7dde79a`  
		Last Modified: Wed, 25 Jan 2023 21:08:09 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c16a3b36d2811deb888f04f3faddc80c02ee1890aa6656c8e449db702394d94`  
		Last Modified: Wed, 25 Jan 2023 21:27:13 GMT  
		Size: 314.6 MB (314591645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d14d8b67adf6b89f3a363611e2f7154b8a03098727d05b9963cf8ad3e7111af`  
		Last Modified: Wed, 25 Jan 2023 21:26:40 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:3-postgres`

```console
$ docker pull geonetwork@sha256:187f44d2a4d44c8ec3c933742739b124f7260a42185721ece23f6bbcf307e084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `geonetwork:3-postgres` - linux; amd64

```console
$ docker pull geonetwork@sha256:107f436aa3d4b6dfebb880e7a5f5d09e56b1b643931be01371381c68265277c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.9 MB (437912128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53275b64624add978cea4d17e483a2fd4ef6ee94b1ba56efc0d1f4cbc66700ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:30 GMT
ADD file:481dd2da6de71525248eba186feeeafcc73cc956ade0a196a4e8b0c2424e74b9 in / 
# Fri, 09 Dec 2022 01:20:31 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:42:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 01:42:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 01:42:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 01:43:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 19:20:07 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 19:20:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 19:20:13 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 20:36:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 25 Jan 2023 20:36:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 20:36:38 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 25 Jan 2023 20:36:38 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 20:36:38 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 20:36:38 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 20:38:55 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 25 Jan 2023 20:38:55 GMT
ENV TOMCAT_MAJOR=8
# Wed, 25 Jan 2023 20:38:55 GMT
ENV TOMCAT_VERSION=8.5.85
# Wed, 25 Jan 2023 20:38:55 GMT
ENV TOMCAT_SHA512=0fc44133aff9e7e31d6dbb4b6e204d33bd0009b6bd089e5f8c8a1f7dfe7c5feff25d7f6404c4a3c5610e0960b5d0198580171212a2636816a23e21799a4c0467
# Wed, 25 Jan 2023 20:39:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 25 Jan 2023 20:39:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 25 Jan 2023 20:39:29 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 20:39:30 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 21:39:40 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 21:39:40 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Wed, 25 Jan 2023 21:39:40 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Wed, 25 Jan 2023 21:39:40 GMT
ENV GN_VERSION=3.12.8
# Wed, 25 Jan 2023 21:39:41 GMT
ENV GN_DOWNLOAD_MD5=378b70ee5c358a8db5659dafc8220e9f
# Wed, 25 Jan 2023 21:39:41 GMT
WORKDIR /usr/local/tomcat/webapps
# Wed, 25 Jan 2023 21:40:55 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Wed, 25 Jan 2023 21:40:56 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Wed, 25 Jan 2023 21:40:56 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 21:40:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 21:40:56 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 21:41:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 21:41:13 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml"
# Wed, 25 Jan 2023 21:41:13 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Wed, 25 Jan 2023 21:41:13 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Wed, 25 Jan 2023 21:41:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 21:41:13 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6e3729cf69e0ce2de9e779575a1fec8b7fb5efdfa822829290ab6d5d1bc3e797`  
		Last Modified: Thu, 08 Dec 2022 14:10:00 GMT  
		Size: 30.4 MB (30428708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96aa423488f0ed1e9bf6c6da11fa7fb53568d1ea4003892416b3adeccb47e3bf`  
		Last Modified: Fri, 09 Dec 2022 01:50:02 GMT  
		Size: 12.4 MB (12432218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7d768530ca9e5fcde3ff9db86652aec33ca22d38cd93adf6b52e40581a32ec`  
		Last Modified: Wed, 25 Jan 2023 19:26:26 GMT  
		Size: 54.6 MB (54635670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34735e297c951328bfe5ea0366c1200ceb015ac7c2f3bc7a350ff51c091bdafc`  
		Last Modified: Wed, 25 Jan 2023 19:26:20 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc2293174b5fe65d5f09e90ee0968d1590e96081a18a16f3e7d8b58cd996396`  
		Last Modified: Wed, 25 Jan 2023 20:44:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adaadf54074ee75672402b6e9776bdb23c575e6c17654c9a9202a6ea5a99a3d7`  
		Last Modified: Wed, 25 Jan 2023 20:46:40 GMT  
		Size: 12.2 MB (12165261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa82b2c64abca8bf74d499d8e94ab0277da5e3401e1c5a54a0b1f34fd431876`  
		Last Modified: Wed, 25 Jan 2023 20:46:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4205adafee91900d19c8b5f81bff94eb7f5a4d1c2e030a505b18f8a5cfde449e`  
		Last Modified: Wed, 25 Jan 2023 21:43:54 GMT  
		Size: 314.6 MB (314555486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad6a999142d78c3f2d1e8dff65b7934b8f93a786de055c038a30b0bea5d4339`  
		Last Modified: Wed, 25 Jan 2023 21:43:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f649bfcf8f542b97def2f8f05529c48d7a41af4dfd28aef5cf8321e5447f479e`  
		Last Modified: Wed, 25 Jan 2023 21:44:07 GMT  
		Size: 13.7 MB (13690710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e233081d7abe54fa9f42242723d53d8f8379616ce905da261bc801b0efc48dc`  
		Last Modified: Wed, 25 Jan 2023 21:44:04 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c229884059cea2739fed1bf69e6ea60ef1018060b71b95507ba0a8f67105f1e5`  
		Last Modified: Wed, 25 Jan 2023 21:44:04 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b83764d8c8a2598a5c855286436c0cb18228e014c9ec816362e4d10655da4e`  
		Last Modified: Wed, 25 Jan 2023 21:44:04 GMT  
		Size: 974.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:c3e396065c3137e35718763238f7410d5410cf8bbef8afd7d69817305e42b00c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.6 MB (428616215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9ff4a410c5084f49c1e693bc5d1f023309c42b0aa0ad67cb3030ee5d950774`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Dec 2022 01:36:30 GMT
ADD file:ca82b3c78a23b75345429f192c4b1f88b4e49e12808c85fccc2db04823c17d4e in / 
# Fri, 09 Dec 2022 01:36:30 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:08:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 03:08:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 03:08:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 03:08:17 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 20:43:47 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 20:44:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 20:44:07 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 21:37:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 25 Jan 2023 21:37:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 21:37:06 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 25 Jan 2023 21:37:06 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 21:37:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 21:37:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 21:40:12 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 25 Jan 2023 21:40:12 GMT
ENV TOMCAT_MAJOR=8
# Wed, 25 Jan 2023 21:40:12 GMT
ENV TOMCAT_VERSION=8.5.85
# Wed, 25 Jan 2023 21:40:12 GMT
ENV TOMCAT_SHA512=0fc44133aff9e7e31d6dbb4b6e204d33bd0009b6bd089e5f8c8a1f7dfe7c5feff25d7f6404c4a3c5610e0960b5d0198580171212a2636816a23e21799a4c0467
# Wed, 25 Jan 2023 21:40:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 25 Jan 2023 21:40:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 25 Jan 2023 21:40:49 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 21:40:49 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 22:16:51 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 22:16:51 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Wed, 25 Jan 2023 22:16:51 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Wed, 25 Jan 2023 22:16:51 GMT
ENV GN_VERSION=3.12.8
# Wed, 25 Jan 2023 22:16:51 GMT
ENV GN_DOWNLOAD_MD5=378b70ee5c358a8db5659dafc8220e9f
# Wed, 25 Jan 2023 22:16:51 GMT
WORKDIR /usr/local/tomcat/webapps
# Wed, 25 Jan 2023 22:17:38 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Wed, 25 Jan 2023 22:17:39 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Wed, 25 Jan 2023 22:17:39 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 22:17:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 22:17:39 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 22:18:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 22:18:06 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml"
# Wed, 25 Jan 2023 22:18:06 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Wed, 25 Jan 2023 22:18:06 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Wed, 25 Jan 2023 22:18:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 22:18:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c38006c9acc492149d706593acba951110798e57a7ad05103ae7a2d5969c14b6`  
		Last Modified: Thu, 08 Dec 2022 18:49:27 GMT  
		Size: 27.0 MB (27023448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c75c90d8ac3bc54f87b6716d34d23742433f988c00aef47001964698038d79`  
		Last Modified: Fri, 09 Dec 2022 03:17:28 GMT  
		Size: 12.0 MB (11993622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6225f767c4a3b305ad8e5712ff3988f6291b43765adfb5e8e2778d341cf1086a`  
		Last Modified: Wed, 25 Jan 2023 20:49:37 GMT  
		Size: 50.3 MB (50294599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff09de9a10ff310613b84e648fcbcb168aac2c6f6fa63ffbd10d58c2fa7e456`  
		Last Modified: Wed, 25 Jan 2023 20:49:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5eef20df6de484799bde83de7708971f47706816120d0eeef076792236116b`  
		Last Modified: Wed, 25 Jan 2023 21:53:37 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5684a0ac10b93a9edd850e0ef1b45dc27c041473e8da9b30ee3d7476d8ac3d`  
		Last Modified: Wed, 25 Jan 2023 21:56:06 GMT  
		Size: 12.0 MB (12011921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4871ddb7ff0457ccf99d037ab19a6b0eb2bf2acc1533cd12cf027639363010`  
		Last Modified: Wed, 25 Jan 2023 21:56:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40cc0824716930a424bb0173ada203ca572e0b3faf69828170e703a04a8c248d`  
		Last Modified: Wed, 25 Jan 2023 22:19:00 GMT  
		Size: 314.5 MB (314541834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad21ac3b46e8b54a4d8b7a30971c3aee438c6115c30f9dcc238c949e2eee0eb`  
		Last Modified: Wed, 25 Jan 2023 22:18:30 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c42eba12c7de701a2b02ebf0ff0442de9b97a95bafab59be1b6fc51f13f7a2b`  
		Last Modified: Wed, 25 Jan 2023 22:19:18 GMT  
		Size: 12.7 MB (12746779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e483875e67cbd3479f4bbe0dbbb0a08c6d48db5569c2f7d217dfecf3d994f248`  
		Last Modified: Wed, 25 Jan 2023 22:19:14 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750dbcdc9dfe9e7357e195b925daee7576d01a5c5f05e4a2d3a5ae170ec1bab7`  
		Last Modified: Wed, 25 Jan 2023 22:19:14 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88c54b1fc1cf7de7b3c52ae545a1d778073770910113cbd4888f0360f2a8d32`  
		Last Modified: Wed, 25 Jan 2023 22:19:14 GMT  
		Size: 974.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:6b7f83671310da252f8160256beba1589d0fb8bc16a87299167c69761059194c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.3 MB (434348381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cc627a57ee310022912fc7264bf31395fa5262def744b720807fc31274ef09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 26 Jan 2023 05:05:49 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:05:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:05:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:05:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:05:51 GMT
ADD file:55486a91f732042dd4e81ecfd8457d23e04dcd7dd80a0bb06cc7c44873fac838 in / 
# Thu, 26 Jan 2023 05:05:51 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:43:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Jan 2023 17:43:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 17:43:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Jan 2023 17:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:44:32 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Tue, 31 Jan 2023 17:44:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 31 Jan 2023 17:44:38 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 31 Jan 2023 22:17:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 31 Jan 2023 22:17:17 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 22:17:18 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 31 Jan 2023 22:17:18 GMT
WORKDIR /usr/local/tomcat
# Tue, 31 Jan 2023 22:17:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 31 Jan 2023 22:17:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 31 Jan 2023 22:21:26 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 31 Jan 2023 22:21:26 GMT
ENV TOMCAT_MAJOR=8
# Tue, 31 Jan 2023 22:21:26 GMT
ENV TOMCAT_VERSION=8.5.85
# Tue, 31 Jan 2023 22:21:26 GMT
ENV TOMCAT_SHA512=0fc44133aff9e7e31d6dbb4b6e204d33bd0009b6bd089e5f8c8a1f7dfe7c5feff25d7f6404c4a3c5610e0960b5d0198580171212a2636816a23e21799a4c0467
# Tue, 31 Jan 2023 22:21:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 31 Jan 2023 22:21:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 31 Jan 2023 22:21:56 GMT
EXPOSE 8080
# Tue, 31 Jan 2023 22:21:56 GMT
CMD ["catalina.sh" "run"]
# Wed, 01 Feb 2023 00:07:22 GMT
ENV GN_FILE=geonetwork.war
# Wed, 01 Feb 2023 00:07:22 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Wed, 01 Feb 2023 00:07:22 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Wed, 01 Feb 2023 00:07:22 GMT
ENV GN_VERSION=3.12.8
# Wed, 01 Feb 2023 00:07:22 GMT
ENV GN_DOWNLOAD_MD5=378b70ee5c358a8db5659dafc8220e9f
# Wed, 01 Feb 2023 00:07:23 GMT
WORKDIR /usr/local/tomcat/webapps
# Wed, 01 Feb 2023 00:07:51 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Wed, 01 Feb 2023 00:07:54 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Wed, 01 Feb 2023 00:07:54 GMT
WORKDIR /usr/local/tomcat
# Wed, 01 Feb 2023 00:07:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Feb 2023 00:07:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 01 Feb 2023 00:08:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 00:08:12 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml"
# Wed, 01 Feb 2023 00:08:12 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Wed, 01 Feb 2023 00:08:12 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Wed, 01 Feb 2023 00:08:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Feb 2023 00:08:12 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:565cb979c5c01279efcd69c4457a9954801b6be6da65894374260ec92d993891`  
		Last Modified: Thu, 26 Jan 2023 16:22:40 GMT  
		Size: 28.4 MB (28384974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c6471d4f305436bdd6e09ea64bdf7a303979f4d8cdb6c9606715fc21afa9ad`  
		Last Modified: Tue, 31 Jan 2023 17:50:26 GMT  
		Size: 12.4 MB (12391264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427df1d8bddcc93bab1efadcf6f2157f2d58b6366e437f130fb7ad8676a8a64f`  
		Last Modified: Tue, 31 Jan 2023 17:50:30 GMT  
		Size: 53.7 MB (53731740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1db467a77eb3093981e70f61997b6ade2c0b5662ace92eef00c082999f55dd6`  
		Last Modified: Tue, 31 Jan 2023 17:50:24 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7899e6f25670a980cf6b742a0443e29000441ee96c6e5189434396b495bd94bd`  
		Last Modified: Tue, 31 Jan 2023 22:33:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a6489f84d41cef926fc329042d2b342b71eea669b80dfaaba20df41ab717d2`  
		Last Modified: Tue, 31 Jan 2023 22:37:21 GMT  
		Size: 11.7 MB (11700782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde69c27b4cbedaf2799b7e23125b3a7df2b63dcd80268f9dded343986b26651`  
		Last Modified: Tue, 31 Jan 2023 22:37:20 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cc6e867e17538390665f99ad6fbc71809c09b4d6b59c2ed851480589821fc6`  
		Last Modified: Wed, 01 Feb 2023 00:11:48 GMT  
		Size: 314.5 MB (314546078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89beff1eb4faa366b06d9e01c3a457d27f611d3a9203a30f3544ca2055b3278e`  
		Last Modified: Wed, 01 Feb 2023 00:11:33 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead097cb103eb8f3905fb1aae03facf47ddddbba7a29fafdf2c21f44a17aaceb`  
		Last Modified: Wed, 01 Feb 2023 00:12:01 GMT  
		Size: 13.6 MB (13589469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1a7c2999db39cde2b3daed0bf6016943869624901737c288c61fe970adccc5`  
		Last Modified: Wed, 01 Feb 2023 00:11:59 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ee1fcade266471825b561bea3e8b4a9f3ecd1085dfd940feb95d8bac21a839`  
		Last Modified: Wed, 01 Feb 2023 00:11:59 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcef798b22bcbe2756ec9d640d3da95d1107c0500dc7f6518f07fc1c9e710d93`  
		Last Modified: Wed, 01 Feb 2023 00:11:59 GMT  
		Size: 972.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:80eebeeb850bffc1cf3094e95f32e790650c75ca89578de692f713cc4a47b18e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.2 MB (442220044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89fbee9e3c422dd025072975a6bf5432e9a62d3073528720563fdda5ac5ed8ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Dec 2022 01:27:53 GMT
ADD file:1a2557b357a1dca8521ee846ec16c9b2bd8a53839b9d4fda21a28f9ceeecb4b7 in / 
# Fri, 09 Dec 2022 01:27:55 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:39:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 02:39:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 02:39:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 02:40:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 19:38:40 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 19:38:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 19:38:54 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 20:49:25 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 25 Jan 2023 20:49:25 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 20:49:27 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 25 Jan 2023 20:49:27 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 20:49:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 20:49:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 20:53:23 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 25 Jan 2023 20:53:23 GMT
ENV TOMCAT_MAJOR=8
# Wed, 25 Jan 2023 20:53:23 GMT
ENV TOMCAT_VERSION=8.5.85
# Wed, 25 Jan 2023 20:53:24 GMT
ENV TOMCAT_SHA512=0fc44133aff9e7e31d6dbb4b6e204d33bd0009b6bd089e5f8c8a1f7dfe7c5feff25d7f6404c4a3c5610e0960b5d0198580171212a2636816a23e21799a4c0467
# Wed, 25 Jan 2023 20:54:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 25 Jan 2023 20:54:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 25 Jan 2023 20:54:28 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 20:54:28 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 21:24:58 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 21:24:58 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Wed, 25 Jan 2023 21:24:58 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Wed, 25 Jan 2023 21:24:59 GMT
ENV GN_VERSION=3.12.8
# Wed, 25 Jan 2023 21:24:59 GMT
ENV GN_DOWNLOAD_MD5=378b70ee5c358a8db5659dafc8220e9f
# Wed, 25 Jan 2023 21:24:59 GMT
WORKDIR /usr/local/tomcat/webapps
# Wed, 25 Jan 2023 21:25:44 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Wed, 25 Jan 2023 21:25:49 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Wed, 25 Jan 2023 21:25:50 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 21:25:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 21:25:50 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 21:26:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 21:26:15 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml"
# Wed, 25 Jan 2023 21:26:16 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Wed, 25 Jan 2023 21:26:16 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Wed, 25 Jan 2023 21:26:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 21:26:16 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ce75b47e476cd75b30dca46558ac79b39923aa94d7e4b0cc025e521404cdbab0`  
		Last Modified: Fri, 09 Dec 2022 01:30:32 GMT  
		Size: 35.7 MB (35708154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a782dc6ae3d6a01674486598e1b3cdcfaa9696ad3e2125e712884667b1c2c37f`  
		Last Modified: Fri, 09 Dec 2022 02:53:02 GMT  
		Size: 13.2 MB (13245456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f293f07451d1ca9101f6406ed167fb8798e49df8ddf8acee518c3db37b0b185`  
		Last Modified: Wed, 25 Jan 2023 19:57:54 GMT  
		Size: 52.1 MB (52112863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44c8bdf138d6084aeef40083fb29771e2cf786714a4d644ae79155891980939`  
		Last Modified: Wed, 25 Jan 2023 19:57:43 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4377ec606c42192ec93ed57b0a6a47b5cf42197a7550956938bebe5b2af38092`  
		Last Modified: Wed, 25 Jan 2023 21:05:49 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7c80c538568990206ee80f8a97620c122e77bc741305edeb516e087a766ff0`  
		Last Modified: Wed, 25 Jan 2023 21:08:11 GMT  
		Size: 12.4 MB (12351915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42be51b9cbf813f7af62d54e2a22d3f530d0d10a7dcfdfc3d0c9fb60f7dde79a`  
		Last Modified: Wed, 25 Jan 2023 21:08:09 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c16a3b36d2811deb888f04f3faddc80c02ee1890aa6656c8e449db702394d94`  
		Last Modified: Wed, 25 Jan 2023 21:27:13 GMT  
		Size: 314.6 MB (314591645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d14d8b67adf6b89f3a363611e2f7154b8a03098727d05b9963cf8ad3e7111af`  
		Last Modified: Wed, 25 Jan 2023 21:26:40 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e2c94d250e8825f5f212d2148752c27e05cdc8e79d88c7708775f5208f63a7`  
		Last Modified: Wed, 25 Jan 2023 21:27:32 GMT  
		Size: 14.2 MB (14205935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0351a129914867b8f57ac45898de75ca74c15bc7d8862258bed63eda4ba715`  
		Last Modified: Wed, 25 Jan 2023 21:27:27 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337c5135361a9019849545b450f57c59c8e170f1f980263e2b01a282ea0a29d7`  
		Last Modified: Wed, 25 Jan 2023 21:27:27 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3368d45b2c541562116af80a1edb6db89c528fc6247486100f546254e56c2d`  
		Last Modified: Wed, 25 Jan 2023 21:27:27 GMT  
		Size: 973.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:3.12`

```console
$ docker pull geonetwork@sha256:e65d5bd59e79cf103cc7b2e2e5ff8654531960e7112972dd55bf21d50a45ecd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `geonetwork:3.12` - linux; amd64

```console
$ docker pull geonetwork@sha256:29146d40a5747bd69c038c91efb04f41a1b8c9d38c2f29fbf3b7f4680e827d12
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.2 MB (424218056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814e47edd8412a88b1b03ae0f825249d2734f7a95eff8d346767db2867144fe0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:30 GMT
ADD file:481dd2da6de71525248eba186feeeafcc73cc956ade0a196a4e8b0c2424e74b9 in / 
# Fri, 09 Dec 2022 01:20:31 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:42:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 01:42:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 01:42:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 01:43:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 19:20:07 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 19:20:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 19:20:13 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 20:36:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 25 Jan 2023 20:36:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 20:36:38 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 25 Jan 2023 20:36:38 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 20:36:38 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 20:36:38 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 20:38:55 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 25 Jan 2023 20:38:55 GMT
ENV TOMCAT_MAJOR=8
# Wed, 25 Jan 2023 20:38:55 GMT
ENV TOMCAT_VERSION=8.5.85
# Wed, 25 Jan 2023 20:38:55 GMT
ENV TOMCAT_SHA512=0fc44133aff9e7e31d6dbb4b6e204d33bd0009b6bd089e5f8c8a1f7dfe7c5feff25d7f6404c4a3c5610e0960b5d0198580171212a2636816a23e21799a4c0467
# Wed, 25 Jan 2023 20:39:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 25 Jan 2023 20:39:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 25 Jan 2023 20:39:29 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 20:39:30 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 21:39:40 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 21:39:40 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Wed, 25 Jan 2023 21:39:40 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Wed, 25 Jan 2023 21:39:40 GMT
ENV GN_VERSION=3.12.8
# Wed, 25 Jan 2023 21:39:41 GMT
ENV GN_DOWNLOAD_MD5=378b70ee5c358a8db5659dafc8220e9f
# Wed, 25 Jan 2023 21:39:41 GMT
WORKDIR /usr/local/tomcat/webapps
# Wed, 25 Jan 2023 21:40:55 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Wed, 25 Jan 2023 21:40:56 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Wed, 25 Jan 2023 21:40:56 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 21:40:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 21:40:56 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6e3729cf69e0ce2de9e779575a1fec8b7fb5efdfa822829290ab6d5d1bc3e797`  
		Last Modified: Thu, 08 Dec 2022 14:10:00 GMT  
		Size: 30.4 MB (30428708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96aa423488f0ed1e9bf6c6da11fa7fb53568d1ea4003892416b3adeccb47e3bf`  
		Last Modified: Fri, 09 Dec 2022 01:50:02 GMT  
		Size: 12.4 MB (12432218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7d768530ca9e5fcde3ff9db86652aec33ca22d38cd93adf6b52e40581a32ec`  
		Last Modified: Wed, 25 Jan 2023 19:26:26 GMT  
		Size: 54.6 MB (54635670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34735e297c951328bfe5ea0366c1200ceb015ac7c2f3bc7a350ff51c091bdafc`  
		Last Modified: Wed, 25 Jan 2023 19:26:20 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc2293174b5fe65d5f09e90ee0968d1590e96081a18a16f3e7d8b58cd996396`  
		Last Modified: Wed, 25 Jan 2023 20:44:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adaadf54074ee75672402b6e9776bdb23c575e6c17654c9a9202a6ea5a99a3d7`  
		Last Modified: Wed, 25 Jan 2023 20:46:40 GMT  
		Size: 12.2 MB (12165261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa82b2c64abca8bf74d499d8e94ab0277da5e3401e1c5a54a0b1f34fd431876`  
		Last Modified: Wed, 25 Jan 2023 20:46:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4205adafee91900d19c8b5f81bff94eb7f5a4d1c2e030a505b18f8a5cfde449e`  
		Last Modified: Wed, 25 Jan 2023 21:43:54 GMT  
		Size: 314.6 MB (314555486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad6a999142d78c3f2d1e8dff65b7934b8f93a786de055c038a30b0bea5d4339`  
		Last Modified: Wed, 25 Jan 2023 21:43:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3.12` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:5faae4f1b2f2894cbde64ab532394743e4e518c11d0bcc8c4cb84a0d7d8c9f8b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.9 MB (415866069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060474eec632cb6133da959006f3da3ffb0a72084de107ccd9453f3623a1c56d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Dec 2022 01:36:30 GMT
ADD file:ca82b3c78a23b75345429f192c4b1f88b4e49e12808c85fccc2db04823c17d4e in / 
# Fri, 09 Dec 2022 01:36:30 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:08:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 03:08:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 03:08:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 03:08:17 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 20:43:47 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 20:44:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 20:44:07 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 21:37:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 25 Jan 2023 21:37:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 21:37:06 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 25 Jan 2023 21:37:06 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 21:37:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 21:37:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 21:40:12 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 25 Jan 2023 21:40:12 GMT
ENV TOMCAT_MAJOR=8
# Wed, 25 Jan 2023 21:40:12 GMT
ENV TOMCAT_VERSION=8.5.85
# Wed, 25 Jan 2023 21:40:12 GMT
ENV TOMCAT_SHA512=0fc44133aff9e7e31d6dbb4b6e204d33bd0009b6bd089e5f8c8a1f7dfe7c5feff25d7f6404c4a3c5610e0960b5d0198580171212a2636816a23e21799a4c0467
# Wed, 25 Jan 2023 21:40:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 25 Jan 2023 21:40:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 25 Jan 2023 21:40:49 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 21:40:49 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 22:16:51 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 22:16:51 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Wed, 25 Jan 2023 22:16:51 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Wed, 25 Jan 2023 22:16:51 GMT
ENV GN_VERSION=3.12.8
# Wed, 25 Jan 2023 22:16:51 GMT
ENV GN_DOWNLOAD_MD5=378b70ee5c358a8db5659dafc8220e9f
# Wed, 25 Jan 2023 22:16:51 GMT
WORKDIR /usr/local/tomcat/webapps
# Wed, 25 Jan 2023 22:17:38 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Wed, 25 Jan 2023 22:17:39 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Wed, 25 Jan 2023 22:17:39 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 22:17:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 22:17:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c38006c9acc492149d706593acba951110798e57a7ad05103ae7a2d5969c14b6`  
		Last Modified: Thu, 08 Dec 2022 18:49:27 GMT  
		Size: 27.0 MB (27023448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c75c90d8ac3bc54f87b6716d34d23742433f988c00aef47001964698038d79`  
		Last Modified: Fri, 09 Dec 2022 03:17:28 GMT  
		Size: 12.0 MB (11993622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6225f767c4a3b305ad8e5712ff3988f6291b43765adfb5e8e2778d341cf1086a`  
		Last Modified: Wed, 25 Jan 2023 20:49:37 GMT  
		Size: 50.3 MB (50294599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff09de9a10ff310613b84e648fcbcb168aac2c6f6fa63ffbd10d58c2fa7e456`  
		Last Modified: Wed, 25 Jan 2023 20:49:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5eef20df6de484799bde83de7708971f47706816120d0eeef076792236116b`  
		Last Modified: Wed, 25 Jan 2023 21:53:37 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5684a0ac10b93a9edd850e0ef1b45dc27c041473e8da9b30ee3d7476d8ac3d`  
		Last Modified: Wed, 25 Jan 2023 21:56:06 GMT  
		Size: 12.0 MB (12011921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4871ddb7ff0457ccf99d037ab19a6b0eb2bf2acc1533cd12cf027639363010`  
		Last Modified: Wed, 25 Jan 2023 21:56:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40cc0824716930a424bb0173ada203ca572e0b3faf69828170e703a04a8c248d`  
		Last Modified: Wed, 25 Jan 2023 22:19:00 GMT  
		Size: 314.5 MB (314541834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad21ac3b46e8b54a4d8b7a30971c3aee438c6115c30f9dcc238c949e2eee0eb`  
		Last Modified: Wed, 25 Jan 2023 22:18:30 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3.12` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:10b1d64ce2aefa123affbb4b436687887fda0e6e688df3858d4aa74f5329984a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.8 MB (420755552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7be106d5cf048d1e70c7b289cdba4dba797ec6eb6fa19d07ac602724aa597a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 26 Jan 2023 05:05:49 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:05:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:05:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:05:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:05:51 GMT
ADD file:55486a91f732042dd4e81ecfd8457d23e04dcd7dd80a0bb06cc7c44873fac838 in / 
# Thu, 26 Jan 2023 05:05:51 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:43:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Jan 2023 17:43:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 17:43:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Jan 2023 17:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:44:32 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Tue, 31 Jan 2023 17:44:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 31 Jan 2023 17:44:38 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 31 Jan 2023 22:17:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 31 Jan 2023 22:17:17 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 22:17:18 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 31 Jan 2023 22:17:18 GMT
WORKDIR /usr/local/tomcat
# Tue, 31 Jan 2023 22:17:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 31 Jan 2023 22:17:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 31 Jan 2023 22:21:26 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 31 Jan 2023 22:21:26 GMT
ENV TOMCAT_MAJOR=8
# Tue, 31 Jan 2023 22:21:26 GMT
ENV TOMCAT_VERSION=8.5.85
# Tue, 31 Jan 2023 22:21:26 GMT
ENV TOMCAT_SHA512=0fc44133aff9e7e31d6dbb4b6e204d33bd0009b6bd089e5f8c8a1f7dfe7c5feff25d7f6404c4a3c5610e0960b5d0198580171212a2636816a23e21799a4c0467
# Tue, 31 Jan 2023 22:21:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 31 Jan 2023 22:21:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 31 Jan 2023 22:21:56 GMT
EXPOSE 8080
# Tue, 31 Jan 2023 22:21:56 GMT
CMD ["catalina.sh" "run"]
# Wed, 01 Feb 2023 00:07:22 GMT
ENV GN_FILE=geonetwork.war
# Wed, 01 Feb 2023 00:07:22 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Wed, 01 Feb 2023 00:07:22 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Wed, 01 Feb 2023 00:07:22 GMT
ENV GN_VERSION=3.12.8
# Wed, 01 Feb 2023 00:07:22 GMT
ENV GN_DOWNLOAD_MD5=378b70ee5c358a8db5659dafc8220e9f
# Wed, 01 Feb 2023 00:07:23 GMT
WORKDIR /usr/local/tomcat/webapps
# Wed, 01 Feb 2023 00:07:51 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Wed, 01 Feb 2023 00:07:54 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Wed, 01 Feb 2023 00:07:54 GMT
WORKDIR /usr/local/tomcat
# Wed, 01 Feb 2023 00:07:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Feb 2023 00:07:54 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:565cb979c5c01279efcd69c4457a9954801b6be6da65894374260ec92d993891`  
		Last Modified: Thu, 26 Jan 2023 16:22:40 GMT  
		Size: 28.4 MB (28384974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c6471d4f305436bdd6e09ea64bdf7a303979f4d8cdb6c9606715fc21afa9ad`  
		Last Modified: Tue, 31 Jan 2023 17:50:26 GMT  
		Size: 12.4 MB (12391264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427df1d8bddcc93bab1efadcf6f2157f2d58b6366e437f130fb7ad8676a8a64f`  
		Last Modified: Tue, 31 Jan 2023 17:50:30 GMT  
		Size: 53.7 MB (53731740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1db467a77eb3093981e70f61997b6ade2c0b5662ace92eef00c082999f55dd6`  
		Last Modified: Tue, 31 Jan 2023 17:50:24 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7899e6f25670a980cf6b742a0443e29000441ee96c6e5189434396b495bd94bd`  
		Last Modified: Tue, 31 Jan 2023 22:33:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a6489f84d41cef926fc329042d2b342b71eea669b80dfaaba20df41ab717d2`  
		Last Modified: Tue, 31 Jan 2023 22:37:21 GMT  
		Size: 11.7 MB (11700782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde69c27b4cbedaf2799b7e23125b3a7df2b63dcd80268f9dded343986b26651`  
		Last Modified: Tue, 31 Jan 2023 22:37:20 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cc6e867e17538390665f99ad6fbc71809c09b4d6b59c2ed851480589821fc6`  
		Last Modified: Wed, 01 Feb 2023 00:11:48 GMT  
		Size: 314.5 MB (314546078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89beff1eb4faa366b06d9e01c3a457d27f611d3a9203a30f3544ca2055b3278e`  
		Last Modified: Wed, 01 Feb 2023 00:11:33 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3.12` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:7242688e69127a437ec00c17ecd8431da6086daa0904b9305d5fbebc5c456f9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.0 MB (428010745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e240b213a31ebbcf618fda3f7722313d8fd3203266ffaf505ec3ef59cac04d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Dec 2022 01:27:53 GMT
ADD file:1a2557b357a1dca8521ee846ec16c9b2bd8a53839b9d4fda21a28f9ceeecb4b7 in / 
# Fri, 09 Dec 2022 01:27:55 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:39:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 02:39:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 02:39:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 02:40:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 19:38:40 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 19:38:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 19:38:54 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 20:49:25 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 25 Jan 2023 20:49:25 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 20:49:27 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 25 Jan 2023 20:49:27 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 20:49:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 20:49:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 20:53:23 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 25 Jan 2023 20:53:23 GMT
ENV TOMCAT_MAJOR=8
# Wed, 25 Jan 2023 20:53:23 GMT
ENV TOMCAT_VERSION=8.5.85
# Wed, 25 Jan 2023 20:53:24 GMT
ENV TOMCAT_SHA512=0fc44133aff9e7e31d6dbb4b6e204d33bd0009b6bd089e5f8c8a1f7dfe7c5feff25d7f6404c4a3c5610e0960b5d0198580171212a2636816a23e21799a4c0467
# Wed, 25 Jan 2023 20:54:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 25 Jan 2023 20:54:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 25 Jan 2023 20:54:28 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 20:54:28 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 21:24:58 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 21:24:58 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Wed, 25 Jan 2023 21:24:58 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Wed, 25 Jan 2023 21:24:59 GMT
ENV GN_VERSION=3.12.8
# Wed, 25 Jan 2023 21:24:59 GMT
ENV GN_DOWNLOAD_MD5=378b70ee5c358a8db5659dafc8220e9f
# Wed, 25 Jan 2023 21:24:59 GMT
WORKDIR /usr/local/tomcat/webapps
# Wed, 25 Jan 2023 21:25:44 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Wed, 25 Jan 2023 21:25:49 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Wed, 25 Jan 2023 21:25:50 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 21:25:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 21:25:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ce75b47e476cd75b30dca46558ac79b39923aa94d7e4b0cc025e521404cdbab0`  
		Last Modified: Fri, 09 Dec 2022 01:30:32 GMT  
		Size: 35.7 MB (35708154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a782dc6ae3d6a01674486598e1b3cdcfaa9696ad3e2125e712884667b1c2c37f`  
		Last Modified: Fri, 09 Dec 2022 02:53:02 GMT  
		Size: 13.2 MB (13245456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f293f07451d1ca9101f6406ed167fb8798e49df8ddf8acee518c3db37b0b185`  
		Last Modified: Wed, 25 Jan 2023 19:57:54 GMT  
		Size: 52.1 MB (52112863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44c8bdf138d6084aeef40083fb29771e2cf786714a4d644ae79155891980939`  
		Last Modified: Wed, 25 Jan 2023 19:57:43 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4377ec606c42192ec93ed57b0a6a47b5cf42197a7550956938bebe5b2af38092`  
		Last Modified: Wed, 25 Jan 2023 21:05:49 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7c80c538568990206ee80f8a97620c122e77bc741305edeb516e087a766ff0`  
		Last Modified: Wed, 25 Jan 2023 21:08:11 GMT  
		Size: 12.4 MB (12351915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42be51b9cbf813f7af62d54e2a22d3f530d0d10a7dcfdfc3d0c9fb60f7dde79a`  
		Last Modified: Wed, 25 Jan 2023 21:08:09 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c16a3b36d2811deb888f04f3faddc80c02ee1890aa6656c8e449db702394d94`  
		Last Modified: Wed, 25 Jan 2023 21:27:13 GMT  
		Size: 314.6 MB (314591645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d14d8b67adf6b89f3a363611e2f7154b8a03098727d05b9963cf8ad3e7111af`  
		Last Modified: Wed, 25 Jan 2023 21:26:40 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:3.12-postgres`

```console
$ docker pull geonetwork@sha256:187f44d2a4d44c8ec3c933742739b124f7260a42185721ece23f6bbcf307e084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `geonetwork:3.12-postgres` - linux; amd64

```console
$ docker pull geonetwork@sha256:107f436aa3d4b6dfebb880e7a5f5d09e56b1b643931be01371381c68265277c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.9 MB (437912128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53275b64624add978cea4d17e483a2fd4ef6ee94b1ba56efc0d1f4cbc66700ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:30 GMT
ADD file:481dd2da6de71525248eba186feeeafcc73cc956ade0a196a4e8b0c2424e74b9 in / 
# Fri, 09 Dec 2022 01:20:31 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:42:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 01:42:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 01:42:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 01:43:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 19:20:07 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 19:20:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 19:20:13 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 20:36:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 25 Jan 2023 20:36:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 20:36:38 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 25 Jan 2023 20:36:38 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 20:36:38 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 20:36:38 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 20:38:55 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 25 Jan 2023 20:38:55 GMT
ENV TOMCAT_MAJOR=8
# Wed, 25 Jan 2023 20:38:55 GMT
ENV TOMCAT_VERSION=8.5.85
# Wed, 25 Jan 2023 20:38:55 GMT
ENV TOMCAT_SHA512=0fc44133aff9e7e31d6dbb4b6e204d33bd0009b6bd089e5f8c8a1f7dfe7c5feff25d7f6404c4a3c5610e0960b5d0198580171212a2636816a23e21799a4c0467
# Wed, 25 Jan 2023 20:39:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 25 Jan 2023 20:39:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 25 Jan 2023 20:39:29 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 20:39:30 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 21:39:40 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 21:39:40 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Wed, 25 Jan 2023 21:39:40 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Wed, 25 Jan 2023 21:39:40 GMT
ENV GN_VERSION=3.12.8
# Wed, 25 Jan 2023 21:39:41 GMT
ENV GN_DOWNLOAD_MD5=378b70ee5c358a8db5659dafc8220e9f
# Wed, 25 Jan 2023 21:39:41 GMT
WORKDIR /usr/local/tomcat/webapps
# Wed, 25 Jan 2023 21:40:55 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Wed, 25 Jan 2023 21:40:56 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Wed, 25 Jan 2023 21:40:56 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 21:40:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 21:40:56 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 21:41:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 21:41:13 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml"
# Wed, 25 Jan 2023 21:41:13 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Wed, 25 Jan 2023 21:41:13 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Wed, 25 Jan 2023 21:41:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 21:41:13 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6e3729cf69e0ce2de9e779575a1fec8b7fb5efdfa822829290ab6d5d1bc3e797`  
		Last Modified: Thu, 08 Dec 2022 14:10:00 GMT  
		Size: 30.4 MB (30428708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96aa423488f0ed1e9bf6c6da11fa7fb53568d1ea4003892416b3adeccb47e3bf`  
		Last Modified: Fri, 09 Dec 2022 01:50:02 GMT  
		Size: 12.4 MB (12432218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7d768530ca9e5fcde3ff9db86652aec33ca22d38cd93adf6b52e40581a32ec`  
		Last Modified: Wed, 25 Jan 2023 19:26:26 GMT  
		Size: 54.6 MB (54635670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34735e297c951328bfe5ea0366c1200ceb015ac7c2f3bc7a350ff51c091bdafc`  
		Last Modified: Wed, 25 Jan 2023 19:26:20 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc2293174b5fe65d5f09e90ee0968d1590e96081a18a16f3e7d8b58cd996396`  
		Last Modified: Wed, 25 Jan 2023 20:44:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adaadf54074ee75672402b6e9776bdb23c575e6c17654c9a9202a6ea5a99a3d7`  
		Last Modified: Wed, 25 Jan 2023 20:46:40 GMT  
		Size: 12.2 MB (12165261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa82b2c64abca8bf74d499d8e94ab0277da5e3401e1c5a54a0b1f34fd431876`  
		Last Modified: Wed, 25 Jan 2023 20:46:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4205adafee91900d19c8b5f81bff94eb7f5a4d1c2e030a505b18f8a5cfde449e`  
		Last Modified: Wed, 25 Jan 2023 21:43:54 GMT  
		Size: 314.6 MB (314555486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad6a999142d78c3f2d1e8dff65b7934b8f93a786de055c038a30b0bea5d4339`  
		Last Modified: Wed, 25 Jan 2023 21:43:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f649bfcf8f542b97def2f8f05529c48d7a41af4dfd28aef5cf8321e5447f479e`  
		Last Modified: Wed, 25 Jan 2023 21:44:07 GMT  
		Size: 13.7 MB (13690710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e233081d7abe54fa9f42242723d53d8f8379616ce905da261bc801b0efc48dc`  
		Last Modified: Wed, 25 Jan 2023 21:44:04 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c229884059cea2739fed1bf69e6ea60ef1018060b71b95507ba0a8f67105f1e5`  
		Last Modified: Wed, 25 Jan 2023 21:44:04 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b83764d8c8a2598a5c855286436c0cb18228e014c9ec816362e4d10655da4e`  
		Last Modified: Wed, 25 Jan 2023 21:44:04 GMT  
		Size: 974.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3.12-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:c3e396065c3137e35718763238f7410d5410cf8bbef8afd7d69817305e42b00c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.6 MB (428616215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9ff4a410c5084f49c1e693bc5d1f023309c42b0aa0ad67cb3030ee5d950774`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Dec 2022 01:36:30 GMT
ADD file:ca82b3c78a23b75345429f192c4b1f88b4e49e12808c85fccc2db04823c17d4e in / 
# Fri, 09 Dec 2022 01:36:30 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:08:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 03:08:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 03:08:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 03:08:17 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 20:43:47 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 20:44:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 20:44:07 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 21:37:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 25 Jan 2023 21:37:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 21:37:06 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 25 Jan 2023 21:37:06 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 21:37:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 21:37:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 21:40:12 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 25 Jan 2023 21:40:12 GMT
ENV TOMCAT_MAJOR=8
# Wed, 25 Jan 2023 21:40:12 GMT
ENV TOMCAT_VERSION=8.5.85
# Wed, 25 Jan 2023 21:40:12 GMT
ENV TOMCAT_SHA512=0fc44133aff9e7e31d6dbb4b6e204d33bd0009b6bd089e5f8c8a1f7dfe7c5feff25d7f6404c4a3c5610e0960b5d0198580171212a2636816a23e21799a4c0467
# Wed, 25 Jan 2023 21:40:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 25 Jan 2023 21:40:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 25 Jan 2023 21:40:49 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 21:40:49 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 22:16:51 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 22:16:51 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Wed, 25 Jan 2023 22:16:51 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Wed, 25 Jan 2023 22:16:51 GMT
ENV GN_VERSION=3.12.8
# Wed, 25 Jan 2023 22:16:51 GMT
ENV GN_DOWNLOAD_MD5=378b70ee5c358a8db5659dafc8220e9f
# Wed, 25 Jan 2023 22:16:51 GMT
WORKDIR /usr/local/tomcat/webapps
# Wed, 25 Jan 2023 22:17:38 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Wed, 25 Jan 2023 22:17:39 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Wed, 25 Jan 2023 22:17:39 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 22:17:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 22:17:39 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 22:18:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 22:18:06 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml"
# Wed, 25 Jan 2023 22:18:06 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Wed, 25 Jan 2023 22:18:06 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Wed, 25 Jan 2023 22:18:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 22:18:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c38006c9acc492149d706593acba951110798e57a7ad05103ae7a2d5969c14b6`  
		Last Modified: Thu, 08 Dec 2022 18:49:27 GMT  
		Size: 27.0 MB (27023448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c75c90d8ac3bc54f87b6716d34d23742433f988c00aef47001964698038d79`  
		Last Modified: Fri, 09 Dec 2022 03:17:28 GMT  
		Size: 12.0 MB (11993622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6225f767c4a3b305ad8e5712ff3988f6291b43765adfb5e8e2778d341cf1086a`  
		Last Modified: Wed, 25 Jan 2023 20:49:37 GMT  
		Size: 50.3 MB (50294599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff09de9a10ff310613b84e648fcbcb168aac2c6f6fa63ffbd10d58c2fa7e456`  
		Last Modified: Wed, 25 Jan 2023 20:49:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5eef20df6de484799bde83de7708971f47706816120d0eeef076792236116b`  
		Last Modified: Wed, 25 Jan 2023 21:53:37 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5684a0ac10b93a9edd850e0ef1b45dc27c041473e8da9b30ee3d7476d8ac3d`  
		Last Modified: Wed, 25 Jan 2023 21:56:06 GMT  
		Size: 12.0 MB (12011921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4871ddb7ff0457ccf99d037ab19a6b0eb2bf2acc1533cd12cf027639363010`  
		Last Modified: Wed, 25 Jan 2023 21:56:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40cc0824716930a424bb0173ada203ca572e0b3faf69828170e703a04a8c248d`  
		Last Modified: Wed, 25 Jan 2023 22:19:00 GMT  
		Size: 314.5 MB (314541834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad21ac3b46e8b54a4d8b7a30971c3aee438c6115c30f9dcc238c949e2eee0eb`  
		Last Modified: Wed, 25 Jan 2023 22:18:30 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c42eba12c7de701a2b02ebf0ff0442de9b97a95bafab59be1b6fc51f13f7a2b`  
		Last Modified: Wed, 25 Jan 2023 22:19:18 GMT  
		Size: 12.7 MB (12746779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e483875e67cbd3479f4bbe0dbbb0a08c6d48db5569c2f7d217dfecf3d994f248`  
		Last Modified: Wed, 25 Jan 2023 22:19:14 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750dbcdc9dfe9e7357e195b925daee7576d01a5c5f05e4a2d3a5ae170ec1bab7`  
		Last Modified: Wed, 25 Jan 2023 22:19:14 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88c54b1fc1cf7de7b3c52ae545a1d778073770910113cbd4888f0360f2a8d32`  
		Last Modified: Wed, 25 Jan 2023 22:19:14 GMT  
		Size: 974.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3.12-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:6b7f83671310da252f8160256beba1589d0fb8bc16a87299167c69761059194c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.3 MB (434348381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cc627a57ee310022912fc7264bf31395fa5262def744b720807fc31274ef09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 26 Jan 2023 05:05:49 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:05:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:05:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:05:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:05:51 GMT
ADD file:55486a91f732042dd4e81ecfd8457d23e04dcd7dd80a0bb06cc7c44873fac838 in / 
# Thu, 26 Jan 2023 05:05:51 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:43:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Jan 2023 17:43:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 17:43:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Jan 2023 17:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:44:32 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Tue, 31 Jan 2023 17:44:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 31 Jan 2023 17:44:38 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 31 Jan 2023 22:17:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 31 Jan 2023 22:17:17 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 22:17:18 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 31 Jan 2023 22:17:18 GMT
WORKDIR /usr/local/tomcat
# Tue, 31 Jan 2023 22:17:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 31 Jan 2023 22:17:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 31 Jan 2023 22:21:26 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 31 Jan 2023 22:21:26 GMT
ENV TOMCAT_MAJOR=8
# Tue, 31 Jan 2023 22:21:26 GMT
ENV TOMCAT_VERSION=8.5.85
# Tue, 31 Jan 2023 22:21:26 GMT
ENV TOMCAT_SHA512=0fc44133aff9e7e31d6dbb4b6e204d33bd0009b6bd089e5f8c8a1f7dfe7c5feff25d7f6404c4a3c5610e0960b5d0198580171212a2636816a23e21799a4c0467
# Tue, 31 Jan 2023 22:21:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 31 Jan 2023 22:21:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 31 Jan 2023 22:21:56 GMT
EXPOSE 8080
# Tue, 31 Jan 2023 22:21:56 GMT
CMD ["catalina.sh" "run"]
# Wed, 01 Feb 2023 00:07:22 GMT
ENV GN_FILE=geonetwork.war
# Wed, 01 Feb 2023 00:07:22 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Wed, 01 Feb 2023 00:07:22 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Wed, 01 Feb 2023 00:07:22 GMT
ENV GN_VERSION=3.12.8
# Wed, 01 Feb 2023 00:07:22 GMT
ENV GN_DOWNLOAD_MD5=378b70ee5c358a8db5659dafc8220e9f
# Wed, 01 Feb 2023 00:07:23 GMT
WORKDIR /usr/local/tomcat/webapps
# Wed, 01 Feb 2023 00:07:51 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Wed, 01 Feb 2023 00:07:54 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Wed, 01 Feb 2023 00:07:54 GMT
WORKDIR /usr/local/tomcat
# Wed, 01 Feb 2023 00:07:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Feb 2023 00:07:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 01 Feb 2023 00:08:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 00:08:12 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml"
# Wed, 01 Feb 2023 00:08:12 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Wed, 01 Feb 2023 00:08:12 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Wed, 01 Feb 2023 00:08:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Feb 2023 00:08:12 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:565cb979c5c01279efcd69c4457a9954801b6be6da65894374260ec92d993891`  
		Last Modified: Thu, 26 Jan 2023 16:22:40 GMT  
		Size: 28.4 MB (28384974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c6471d4f305436bdd6e09ea64bdf7a303979f4d8cdb6c9606715fc21afa9ad`  
		Last Modified: Tue, 31 Jan 2023 17:50:26 GMT  
		Size: 12.4 MB (12391264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427df1d8bddcc93bab1efadcf6f2157f2d58b6366e437f130fb7ad8676a8a64f`  
		Last Modified: Tue, 31 Jan 2023 17:50:30 GMT  
		Size: 53.7 MB (53731740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1db467a77eb3093981e70f61997b6ade2c0b5662ace92eef00c082999f55dd6`  
		Last Modified: Tue, 31 Jan 2023 17:50:24 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7899e6f25670a980cf6b742a0443e29000441ee96c6e5189434396b495bd94bd`  
		Last Modified: Tue, 31 Jan 2023 22:33:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a6489f84d41cef926fc329042d2b342b71eea669b80dfaaba20df41ab717d2`  
		Last Modified: Tue, 31 Jan 2023 22:37:21 GMT  
		Size: 11.7 MB (11700782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde69c27b4cbedaf2799b7e23125b3a7df2b63dcd80268f9dded343986b26651`  
		Last Modified: Tue, 31 Jan 2023 22:37:20 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cc6e867e17538390665f99ad6fbc71809c09b4d6b59c2ed851480589821fc6`  
		Last Modified: Wed, 01 Feb 2023 00:11:48 GMT  
		Size: 314.5 MB (314546078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89beff1eb4faa366b06d9e01c3a457d27f611d3a9203a30f3544ca2055b3278e`  
		Last Modified: Wed, 01 Feb 2023 00:11:33 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead097cb103eb8f3905fb1aae03facf47ddddbba7a29fafdf2c21f44a17aaceb`  
		Last Modified: Wed, 01 Feb 2023 00:12:01 GMT  
		Size: 13.6 MB (13589469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1a7c2999db39cde2b3daed0bf6016943869624901737c288c61fe970adccc5`  
		Last Modified: Wed, 01 Feb 2023 00:11:59 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ee1fcade266471825b561bea3e8b4a9f3ecd1085dfd940feb95d8bac21a839`  
		Last Modified: Wed, 01 Feb 2023 00:11:59 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcef798b22bcbe2756ec9d640d3da95d1107c0500dc7f6518f07fc1c9e710d93`  
		Last Modified: Wed, 01 Feb 2023 00:11:59 GMT  
		Size: 972.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3.12-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:80eebeeb850bffc1cf3094e95f32e790650c75ca89578de692f713cc4a47b18e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.2 MB (442220044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89fbee9e3c422dd025072975a6bf5432e9a62d3073528720563fdda5ac5ed8ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Dec 2022 01:27:53 GMT
ADD file:1a2557b357a1dca8521ee846ec16c9b2bd8a53839b9d4fda21a28f9ceeecb4b7 in / 
# Fri, 09 Dec 2022 01:27:55 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:39:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 02:39:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 02:39:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 02:40:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 19:38:40 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 19:38:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 19:38:54 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 20:49:25 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 25 Jan 2023 20:49:25 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 20:49:27 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 25 Jan 2023 20:49:27 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 20:49:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 20:49:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 20:53:23 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 25 Jan 2023 20:53:23 GMT
ENV TOMCAT_MAJOR=8
# Wed, 25 Jan 2023 20:53:23 GMT
ENV TOMCAT_VERSION=8.5.85
# Wed, 25 Jan 2023 20:53:24 GMT
ENV TOMCAT_SHA512=0fc44133aff9e7e31d6dbb4b6e204d33bd0009b6bd089e5f8c8a1f7dfe7c5feff25d7f6404c4a3c5610e0960b5d0198580171212a2636816a23e21799a4c0467
# Wed, 25 Jan 2023 20:54:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 25 Jan 2023 20:54:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 25 Jan 2023 20:54:28 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 20:54:28 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 21:24:58 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 21:24:58 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Wed, 25 Jan 2023 21:24:58 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Wed, 25 Jan 2023 21:24:59 GMT
ENV GN_VERSION=3.12.8
# Wed, 25 Jan 2023 21:24:59 GMT
ENV GN_DOWNLOAD_MD5=378b70ee5c358a8db5659dafc8220e9f
# Wed, 25 Jan 2023 21:24:59 GMT
WORKDIR /usr/local/tomcat/webapps
# Wed, 25 Jan 2023 21:25:44 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Wed, 25 Jan 2023 21:25:49 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Wed, 25 Jan 2023 21:25:50 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 21:25:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 21:25:50 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 21:26:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 21:26:15 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml"
# Wed, 25 Jan 2023 21:26:16 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Wed, 25 Jan 2023 21:26:16 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Wed, 25 Jan 2023 21:26:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 21:26:16 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ce75b47e476cd75b30dca46558ac79b39923aa94d7e4b0cc025e521404cdbab0`  
		Last Modified: Fri, 09 Dec 2022 01:30:32 GMT  
		Size: 35.7 MB (35708154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a782dc6ae3d6a01674486598e1b3cdcfaa9696ad3e2125e712884667b1c2c37f`  
		Last Modified: Fri, 09 Dec 2022 02:53:02 GMT  
		Size: 13.2 MB (13245456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f293f07451d1ca9101f6406ed167fb8798e49df8ddf8acee518c3db37b0b185`  
		Last Modified: Wed, 25 Jan 2023 19:57:54 GMT  
		Size: 52.1 MB (52112863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44c8bdf138d6084aeef40083fb29771e2cf786714a4d644ae79155891980939`  
		Last Modified: Wed, 25 Jan 2023 19:57:43 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4377ec606c42192ec93ed57b0a6a47b5cf42197a7550956938bebe5b2af38092`  
		Last Modified: Wed, 25 Jan 2023 21:05:49 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7c80c538568990206ee80f8a97620c122e77bc741305edeb516e087a766ff0`  
		Last Modified: Wed, 25 Jan 2023 21:08:11 GMT  
		Size: 12.4 MB (12351915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42be51b9cbf813f7af62d54e2a22d3f530d0d10a7dcfdfc3d0c9fb60f7dde79a`  
		Last Modified: Wed, 25 Jan 2023 21:08:09 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c16a3b36d2811deb888f04f3faddc80c02ee1890aa6656c8e449db702394d94`  
		Last Modified: Wed, 25 Jan 2023 21:27:13 GMT  
		Size: 314.6 MB (314591645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d14d8b67adf6b89f3a363611e2f7154b8a03098727d05b9963cf8ad3e7111af`  
		Last Modified: Wed, 25 Jan 2023 21:26:40 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e2c94d250e8825f5f212d2148752c27e05cdc8e79d88c7708775f5208f63a7`  
		Last Modified: Wed, 25 Jan 2023 21:27:32 GMT  
		Size: 14.2 MB (14205935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0351a129914867b8f57ac45898de75ca74c15bc7d8862258bed63eda4ba715`  
		Last Modified: Wed, 25 Jan 2023 21:27:27 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337c5135361a9019849545b450f57c59c8e170f1f980263e2b01a282ea0a29d7`  
		Last Modified: Wed, 25 Jan 2023 21:27:27 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3368d45b2c541562116af80a1edb6db89c528fc6247486100f546254e56c2d`  
		Last Modified: Wed, 25 Jan 2023 21:27:27 GMT  
		Size: 973.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:3.12.8`

```console
$ docker pull geonetwork@sha256:e65d5bd59e79cf103cc7b2e2e5ff8654531960e7112972dd55bf21d50a45ecd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `geonetwork:3.12.8` - linux; amd64

```console
$ docker pull geonetwork@sha256:29146d40a5747bd69c038c91efb04f41a1b8c9d38c2f29fbf3b7f4680e827d12
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.2 MB (424218056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814e47edd8412a88b1b03ae0f825249d2734f7a95eff8d346767db2867144fe0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:30 GMT
ADD file:481dd2da6de71525248eba186feeeafcc73cc956ade0a196a4e8b0c2424e74b9 in / 
# Fri, 09 Dec 2022 01:20:31 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:42:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 01:42:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 01:42:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 01:43:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 19:20:07 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 19:20:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 19:20:13 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 20:36:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 25 Jan 2023 20:36:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 20:36:38 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 25 Jan 2023 20:36:38 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 20:36:38 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 20:36:38 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 20:38:55 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 25 Jan 2023 20:38:55 GMT
ENV TOMCAT_MAJOR=8
# Wed, 25 Jan 2023 20:38:55 GMT
ENV TOMCAT_VERSION=8.5.85
# Wed, 25 Jan 2023 20:38:55 GMT
ENV TOMCAT_SHA512=0fc44133aff9e7e31d6dbb4b6e204d33bd0009b6bd089e5f8c8a1f7dfe7c5feff25d7f6404c4a3c5610e0960b5d0198580171212a2636816a23e21799a4c0467
# Wed, 25 Jan 2023 20:39:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 25 Jan 2023 20:39:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 25 Jan 2023 20:39:29 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 20:39:30 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 21:39:40 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 21:39:40 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Wed, 25 Jan 2023 21:39:40 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Wed, 25 Jan 2023 21:39:40 GMT
ENV GN_VERSION=3.12.8
# Wed, 25 Jan 2023 21:39:41 GMT
ENV GN_DOWNLOAD_MD5=378b70ee5c358a8db5659dafc8220e9f
# Wed, 25 Jan 2023 21:39:41 GMT
WORKDIR /usr/local/tomcat/webapps
# Wed, 25 Jan 2023 21:40:55 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Wed, 25 Jan 2023 21:40:56 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Wed, 25 Jan 2023 21:40:56 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 21:40:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 21:40:56 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6e3729cf69e0ce2de9e779575a1fec8b7fb5efdfa822829290ab6d5d1bc3e797`  
		Last Modified: Thu, 08 Dec 2022 14:10:00 GMT  
		Size: 30.4 MB (30428708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96aa423488f0ed1e9bf6c6da11fa7fb53568d1ea4003892416b3adeccb47e3bf`  
		Last Modified: Fri, 09 Dec 2022 01:50:02 GMT  
		Size: 12.4 MB (12432218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7d768530ca9e5fcde3ff9db86652aec33ca22d38cd93adf6b52e40581a32ec`  
		Last Modified: Wed, 25 Jan 2023 19:26:26 GMT  
		Size: 54.6 MB (54635670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34735e297c951328bfe5ea0366c1200ceb015ac7c2f3bc7a350ff51c091bdafc`  
		Last Modified: Wed, 25 Jan 2023 19:26:20 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc2293174b5fe65d5f09e90ee0968d1590e96081a18a16f3e7d8b58cd996396`  
		Last Modified: Wed, 25 Jan 2023 20:44:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adaadf54074ee75672402b6e9776bdb23c575e6c17654c9a9202a6ea5a99a3d7`  
		Last Modified: Wed, 25 Jan 2023 20:46:40 GMT  
		Size: 12.2 MB (12165261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa82b2c64abca8bf74d499d8e94ab0277da5e3401e1c5a54a0b1f34fd431876`  
		Last Modified: Wed, 25 Jan 2023 20:46:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4205adafee91900d19c8b5f81bff94eb7f5a4d1c2e030a505b18f8a5cfde449e`  
		Last Modified: Wed, 25 Jan 2023 21:43:54 GMT  
		Size: 314.6 MB (314555486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad6a999142d78c3f2d1e8dff65b7934b8f93a786de055c038a30b0bea5d4339`  
		Last Modified: Wed, 25 Jan 2023 21:43:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3.12.8` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:5faae4f1b2f2894cbde64ab532394743e4e518c11d0bcc8c4cb84a0d7d8c9f8b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.9 MB (415866069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060474eec632cb6133da959006f3da3ffb0a72084de107ccd9453f3623a1c56d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Dec 2022 01:36:30 GMT
ADD file:ca82b3c78a23b75345429f192c4b1f88b4e49e12808c85fccc2db04823c17d4e in / 
# Fri, 09 Dec 2022 01:36:30 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:08:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 03:08:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 03:08:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 03:08:17 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 20:43:47 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 20:44:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 20:44:07 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 21:37:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 25 Jan 2023 21:37:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 21:37:06 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 25 Jan 2023 21:37:06 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 21:37:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 21:37:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 21:40:12 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 25 Jan 2023 21:40:12 GMT
ENV TOMCAT_MAJOR=8
# Wed, 25 Jan 2023 21:40:12 GMT
ENV TOMCAT_VERSION=8.5.85
# Wed, 25 Jan 2023 21:40:12 GMT
ENV TOMCAT_SHA512=0fc44133aff9e7e31d6dbb4b6e204d33bd0009b6bd089e5f8c8a1f7dfe7c5feff25d7f6404c4a3c5610e0960b5d0198580171212a2636816a23e21799a4c0467
# Wed, 25 Jan 2023 21:40:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 25 Jan 2023 21:40:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 25 Jan 2023 21:40:49 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 21:40:49 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 22:16:51 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 22:16:51 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Wed, 25 Jan 2023 22:16:51 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Wed, 25 Jan 2023 22:16:51 GMT
ENV GN_VERSION=3.12.8
# Wed, 25 Jan 2023 22:16:51 GMT
ENV GN_DOWNLOAD_MD5=378b70ee5c358a8db5659dafc8220e9f
# Wed, 25 Jan 2023 22:16:51 GMT
WORKDIR /usr/local/tomcat/webapps
# Wed, 25 Jan 2023 22:17:38 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Wed, 25 Jan 2023 22:17:39 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Wed, 25 Jan 2023 22:17:39 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 22:17:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 22:17:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c38006c9acc492149d706593acba951110798e57a7ad05103ae7a2d5969c14b6`  
		Last Modified: Thu, 08 Dec 2022 18:49:27 GMT  
		Size: 27.0 MB (27023448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c75c90d8ac3bc54f87b6716d34d23742433f988c00aef47001964698038d79`  
		Last Modified: Fri, 09 Dec 2022 03:17:28 GMT  
		Size: 12.0 MB (11993622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6225f767c4a3b305ad8e5712ff3988f6291b43765adfb5e8e2778d341cf1086a`  
		Last Modified: Wed, 25 Jan 2023 20:49:37 GMT  
		Size: 50.3 MB (50294599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff09de9a10ff310613b84e648fcbcb168aac2c6f6fa63ffbd10d58c2fa7e456`  
		Last Modified: Wed, 25 Jan 2023 20:49:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5eef20df6de484799bde83de7708971f47706816120d0eeef076792236116b`  
		Last Modified: Wed, 25 Jan 2023 21:53:37 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5684a0ac10b93a9edd850e0ef1b45dc27c041473e8da9b30ee3d7476d8ac3d`  
		Last Modified: Wed, 25 Jan 2023 21:56:06 GMT  
		Size: 12.0 MB (12011921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4871ddb7ff0457ccf99d037ab19a6b0eb2bf2acc1533cd12cf027639363010`  
		Last Modified: Wed, 25 Jan 2023 21:56:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40cc0824716930a424bb0173ada203ca572e0b3faf69828170e703a04a8c248d`  
		Last Modified: Wed, 25 Jan 2023 22:19:00 GMT  
		Size: 314.5 MB (314541834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad21ac3b46e8b54a4d8b7a30971c3aee438c6115c30f9dcc238c949e2eee0eb`  
		Last Modified: Wed, 25 Jan 2023 22:18:30 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3.12.8` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:10b1d64ce2aefa123affbb4b436687887fda0e6e688df3858d4aa74f5329984a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.8 MB (420755552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7be106d5cf048d1e70c7b289cdba4dba797ec6eb6fa19d07ac602724aa597a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 26 Jan 2023 05:05:49 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:05:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:05:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:05:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:05:51 GMT
ADD file:55486a91f732042dd4e81ecfd8457d23e04dcd7dd80a0bb06cc7c44873fac838 in / 
# Thu, 26 Jan 2023 05:05:51 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:43:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Jan 2023 17:43:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 17:43:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Jan 2023 17:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:44:32 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Tue, 31 Jan 2023 17:44:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 31 Jan 2023 17:44:38 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 31 Jan 2023 22:17:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 31 Jan 2023 22:17:17 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 22:17:18 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 31 Jan 2023 22:17:18 GMT
WORKDIR /usr/local/tomcat
# Tue, 31 Jan 2023 22:17:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 31 Jan 2023 22:17:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 31 Jan 2023 22:21:26 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 31 Jan 2023 22:21:26 GMT
ENV TOMCAT_MAJOR=8
# Tue, 31 Jan 2023 22:21:26 GMT
ENV TOMCAT_VERSION=8.5.85
# Tue, 31 Jan 2023 22:21:26 GMT
ENV TOMCAT_SHA512=0fc44133aff9e7e31d6dbb4b6e204d33bd0009b6bd089e5f8c8a1f7dfe7c5feff25d7f6404c4a3c5610e0960b5d0198580171212a2636816a23e21799a4c0467
# Tue, 31 Jan 2023 22:21:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 31 Jan 2023 22:21:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 31 Jan 2023 22:21:56 GMT
EXPOSE 8080
# Tue, 31 Jan 2023 22:21:56 GMT
CMD ["catalina.sh" "run"]
# Wed, 01 Feb 2023 00:07:22 GMT
ENV GN_FILE=geonetwork.war
# Wed, 01 Feb 2023 00:07:22 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Wed, 01 Feb 2023 00:07:22 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Wed, 01 Feb 2023 00:07:22 GMT
ENV GN_VERSION=3.12.8
# Wed, 01 Feb 2023 00:07:22 GMT
ENV GN_DOWNLOAD_MD5=378b70ee5c358a8db5659dafc8220e9f
# Wed, 01 Feb 2023 00:07:23 GMT
WORKDIR /usr/local/tomcat/webapps
# Wed, 01 Feb 2023 00:07:51 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Wed, 01 Feb 2023 00:07:54 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Wed, 01 Feb 2023 00:07:54 GMT
WORKDIR /usr/local/tomcat
# Wed, 01 Feb 2023 00:07:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Feb 2023 00:07:54 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:565cb979c5c01279efcd69c4457a9954801b6be6da65894374260ec92d993891`  
		Last Modified: Thu, 26 Jan 2023 16:22:40 GMT  
		Size: 28.4 MB (28384974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c6471d4f305436bdd6e09ea64bdf7a303979f4d8cdb6c9606715fc21afa9ad`  
		Last Modified: Tue, 31 Jan 2023 17:50:26 GMT  
		Size: 12.4 MB (12391264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427df1d8bddcc93bab1efadcf6f2157f2d58b6366e437f130fb7ad8676a8a64f`  
		Last Modified: Tue, 31 Jan 2023 17:50:30 GMT  
		Size: 53.7 MB (53731740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1db467a77eb3093981e70f61997b6ade2c0b5662ace92eef00c082999f55dd6`  
		Last Modified: Tue, 31 Jan 2023 17:50:24 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7899e6f25670a980cf6b742a0443e29000441ee96c6e5189434396b495bd94bd`  
		Last Modified: Tue, 31 Jan 2023 22:33:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a6489f84d41cef926fc329042d2b342b71eea669b80dfaaba20df41ab717d2`  
		Last Modified: Tue, 31 Jan 2023 22:37:21 GMT  
		Size: 11.7 MB (11700782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde69c27b4cbedaf2799b7e23125b3a7df2b63dcd80268f9dded343986b26651`  
		Last Modified: Tue, 31 Jan 2023 22:37:20 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cc6e867e17538390665f99ad6fbc71809c09b4d6b59c2ed851480589821fc6`  
		Last Modified: Wed, 01 Feb 2023 00:11:48 GMT  
		Size: 314.5 MB (314546078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89beff1eb4faa366b06d9e01c3a457d27f611d3a9203a30f3544ca2055b3278e`  
		Last Modified: Wed, 01 Feb 2023 00:11:33 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3.12.8` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:7242688e69127a437ec00c17ecd8431da6086daa0904b9305d5fbebc5c456f9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.0 MB (428010745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e240b213a31ebbcf618fda3f7722313d8fd3203266ffaf505ec3ef59cac04d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Dec 2022 01:27:53 GMT
ADD file:1a2557b357a1dca8521ee846ec16c9b2bd8a53839b9d4fda21a28f9ceeecb4b7 in / 
# Fri, 09 Dec 2022 01:27:55 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:39:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 02:39:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 02:39:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 02:40:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 19:38:40 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 19:38:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 19:38:54 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 20:49:25 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 25 Jan 2023 20:49:25 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 20:49:27 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 25 Jan 2023 20:49:27 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 20:49:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 20:49:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 20:53:23 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 25 Jan 2023 20:53:23 GMT
ENV TOMCAT_MAJOR=8
# Wed, 25 Jan 2023 20:53:23 GMT
ENV TOMCAT_VERSION=8.5.85
# Wed, 25 Jan 2023 20:53:24 GMT
ENV TOMCAT_SHA512=0fc44133aff9e7e31d6dbb4b6e204d33bd0009b6bd089e5f8c8a1f7dfe7c5feff25d7f6404c4a3c5610e0960b5d0198580171212a2636816a23e21799a4c0467
# Wed, 25 Jan 2023 20:54:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 25 Jan 2023 20:54:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 25 Jan 2023 20:54:28 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 20:54:28 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 21:24:58 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 21:24:58 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Wed, 25 Jan 2023 21:24:58 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Wed, 25 Jan 2023 21:24:59 GMT
ENV GN_VERSION=3.12.8
# Wed, 25 Jan 2023 21:24:59 GMT
ENV GN_DOWNLOAD_MD5=378b70ee5c358a8db5659dafc8220e9f
# Wed, 25 Jan 2023 21:24:59 GMT
WORKDIR /usr/local/tomcat/webapps
# Wed, 25 Jan 2023 21:25:44 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Wed, 25 Jan 2023 21:25:49 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Wed, 25 Jan 2023 21:25:50 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 21:25:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 21:25:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ce75b47e476cd75b30dca46558ac79b39923aa94d7e4b0cc025e521404cdbab0`  
		Last Modified: Fri, 09 Dec 2022 01:30:32 GMT  
		Size: 35.7 MB (35708154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a782dc6ae3d6a01674486598e1b3cdcfaa9696ad3e2125e712884667b1c2c37f`  
		Last Modified: Fri, 09 Dec 2022 02:53:02 GMT  
		Size: 13.2 MB (13245456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f293f07451d1ca9101f6406ed167fb8798e49df8ddf8acee518c3db37b0b185`  
		Last Modified: Wed, 25 Jan 2023 19:57:54 GMT  
		Size: 52.1 MB (52112863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44c8bdf138d6084aeef40083fb29771e2cf786714a4d644ae79155891980939`  
		Last Modified: Wed, 25 Jan 2023 19:57:43 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4377ec606c42192ec93ed57b0a6a47b5cf42197a7550956938bebe5b2af38092`  
		Last Modified: Wed, 25 Jan 2023 21:05:49 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7c80c538568990206ee80f8a97620c122e77bc741305edeb516e087a766ff0`  
		Last Modified: Wed, 25 Jan 2023 21:08:11 GMT  
		Size: 12.4 MB (12351915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42be51b9cbf813f7af62d54e2a22d3f530d0d10a7dcfdfc3d0c9fb60f7dde79a`  
		Last Modified: Wed, 25 Jan 2023 21:08:09 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c16a3b36d2811deb888f04f3faddc80c02ee1890aa6656c8e449db702394d94`  
		Last Modified: Wed, 25 Jan 2023 21:27:13 GMT  
		Size: 314.6 MB (314591645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d14d8b67adf6b89f3a363611e2f7154b8a03098727d05b9963cf8ad3e7111af`  
		Last Modified: Wed, 25 Jan 2023 21:26:40 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:3.12.8-postgres`

```console
$ docker pull geonetwork@sha256:187f44d2a4d44c8ec3c933742739b124f7260a42185721ece23f6bbcf307e084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `geonetwork:3.12.8-postgres` - linux; amd64

```console
$ docker pull geonetwork@sha256:107f436aa3d4b6dfebb880e7a5f5d09e56b1b643931be01371381c68265277c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.9 MB (437912128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53275b64624add978cea4d17e483a2fd4ef6ee94b1ba56efc0d1f4cbc66700ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:30 GMT
ADD file:481dd2da6de71525248eba186feeeafcc73cc956ade0a196a4e8b0c2424e74b9 in / 
# Fri, 09 Dec 2022 01:20:31 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:42:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 01:42:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 01:42:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 01:43:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 19:20:07 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 19:20:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 19:20:13 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 20:36:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 25 Jan 2023 20:36:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 20:36:38 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 25 Jan 2023 20:36:38 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 20:36:38 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 20:36:38 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 20:38:55 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 25 Jan 2023 20:38:55 GMT
ENV TOMCAT_MAJOR=8
# Wed, 25 Jan 2023 20:38:55 GMT
ENV TOMCAT_VERSION=8.5.85
# Wed, 25 Jan 2023 20:38:55 GMT
ENV TOMCAT_SHA512=0fc44133aff9e7e31d6dbb4b6e204d33bd0009b6bd089e5f8c8a1f7dfe7c5feff25d7f6404c4a3c5610e0960b5d0198580171212a2636816a23e21799a4c0467
# Wed, 25 Jan 2023 20:39:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 25 Jan 2023 20:39:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 25 Jan 2023 20:39:29 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 20:39:30 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 21:39:40 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 21:39:40 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Wed, 25 Jan 2023 21:39:40 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Wed, 25 Jan 2023 21:39:40 GMT
ENV GN_VERSION=3.12.8
# Wed, 25 Jan 2023 21:39:41 GMT
ENV GN_DOWNLOAD_MD5=378b70ee5c358a8db5659dafc8220e9f
# Wed, 25 Jan 2023 21:39:41 GMT
WORKDIR /usr/local/tomcat/webapps
# Wed, 25 Jan 2023 21:40:55 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Wed, 25 Jan 2023 21:40:56 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Wed, 25 Jan 2023 21:40:56 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 21:40:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 21:40:56 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 21:41:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 21:41:13 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml"
# Wed, 25 Jan 2023 21:41:13 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Wed, 25 Jan 2023 21:41:13 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Wed, 25 Jan 2023 21:41:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 21:41:13 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6e3729cf69e0ce2de9e779575a1fec8b7fb5efdfa822829290ab6d5d1bc3e797`  
		Last Modified: Thu, 08 Dec 2022 14:10:00 GMT  
		Size: 30.4 MB (30428708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96aa423488f0ed1e9bf6c6da11fa7fb53568d1ea4003892416b3adeccb47e3bf`  
		Last Modified: Fri, 09 Dec 2022 01:50:02 GMT  
		Size: 12.4 MB (12432218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7d768530ca9e5fcde3ff9db86652aec33ca22d38cd93adf6b52e40581a32ec`  
		Last Modified: Wed, 25 Jan 2023 19:26:26 GMT  
		Size: 54.6 MB (54635670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34735e297c951328bfe5ea0366c1200ceb015ac7c2f3bc7a350ff51c091bdafc`  
		Last Modified: Wed, 25 Jan 2023 19:26:20 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc2293174b5fe65d5f09e90ee0968d1590e96081a18a16f3e7d8b58cd996396`  
		Last Modified: Wed, 25 Jan 2023 20:44:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adaadf54074ee75672402b6e9776bdb23c575e6c17654c9a9202a6ea5a99a3d7`  
		Last Modified: Wed, 25 Jan 2023 20:46:40 GMT  
		Size: 12.2 MB (12165261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa82b2c64abca8bf74d499d8e94ab0277da5e3401e1c5a54a0b1f34fd431876`  
		Last Modified: Wed, 25 Jan 2023 20:46:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4205adafee91900d19c8b5f81bff94eb7f5a4d1c2e030a505b18f8a5cfde449e`  
		Last Modified: Wed, 25 Jan 2023 21:43:54 GMT  
		Size: 314.6 MB (314555486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad6a999142d78c3f2d1e8dff65b7934b8f93a786de055c038a30b0bea5d4339`  
		Last Modified: Wed, 25 Jan 2023 21:43:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f649bfcf8f542b97def2f8f05529c48d7a41af4dfd28aef5cf8321e5447f479e`  
		Last Modified: Wed, 25 Jan 2023 21:44:07 GMT  
		Size: 13.7 MB (13690710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e233081d7abe54fa9f42242723d53d8f8379616ce905da261bc801b0efc48dc`  
		Last Modified: Wed, 25 Jan 2023 21:44:04 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c229884059cea2739fed1bf69e6ea60ef1018060b71b95507ba0a8f67105f1e5`  
		Last Modified: Wed, 25 Jan 2023 21:44:04 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b83764d8c8a2598a5c855286436c0cb18228e014c9ec816362e4d10655da4e`  
		Last Modified: Wed, 25 Jan 2023 21:44:04 GMT  
		Size: 974.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3.12.8-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:c3e396065c3137e35718763238f7410d5410cf8bbef8afd7d69817305e42b00c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.6 MB (428616215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9ff4a410c5084f49c1e693bc5d1f023309c42b0aa0ad67cb3030ee5d950774`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Dec 2022 01:36:30 GMT
ADD file:ca82b3c78a23b75345429f192c4b1f88b4e49e12808c85fccc2db04823c17d4e in / 
# Fri, 09 Dec 2022 01:36:30 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:08:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 03:08:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 03:08:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 03:08:17 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 20:43:47 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 20:44:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 20:44:07 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 21:37:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 25 Jan 2023 21:37:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 21:37:06 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 25 Jan 2023 21:37:06 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 21:37:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 21:37:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 21:40:12 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 25 Jan 2023 21:40:12 GMT
ENV TOMCAT_MAJOR=8
# Wed, 25 Jan 2023 21:40:12 GMT
ENV TOMCAT_VERSION=8.5.85
# Wed, 25 Jan 2023 21:40:12 GMT
ENV TOMCAT_SHA512=0fc44133aff9e7e31d6dbb4b6e204d33bd0009b6bd089e5f8c8a1f7dfe7c5feff25d7f6404c4a3c5610e0960b5d0198580171212a2636816a23e21799a4c0467
# Wed, 25 Jan 2023 21:40:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 25 Jan 2023 21:40:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 25 Jan 2023 21:40:49 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 21:40:49 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 22:16:51 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 22:16:51 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Wed, 25 Jan 2023 22:16:51 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Wed, 25 Jan 2023 22:16:51 GMT
ENV GN_VERSION=3.12.8
# Wed, 25 Jan 2023 22:16:51 GMT
ENV GN_DOWNLOAD_MD5=378b70ee5c358a8db5659dafc8220e9f
# Wed, 25 Jan 2023 22:16:51 GMT
WORKDIR /usr/local/tomcat/webapps
# Wed, 25 Jan 2023 22:17:38 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Wed, 25 Jan 2023 22:17:39 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Wed, 25 Jan 2023 22:17:39 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 22:17:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 22:17:39 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 22:18:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 22:18:06 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml"
# Wed, 25 Jan 2023 22:18:06 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Wed, 25 Jan 2023 22:18:06 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Wed, 25 Jan 2023 22:18:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 22:18:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c38006c9acc492149d706593acba951110798e57a7ad05103ae7a2d5969c14b6`  
		Last Modified: Thu, 08 Dec 2022 18:49:27 GMT  
		Size: 27.0 MB (27023448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c75c90d8ac3bc54f87b6716d34d23742433f988c00aef47001964698038d79`  
		Last Modified: Fri, 09 Dec 2022 03:17:28 GMT  
		Size: 12.0 MB (11993622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6225f767c4a3b305ad8e5712ff3988f6291b43765adfb5e8e2778d341cf1086a`  
		Last Modified: Wed, 25 Jan 2023 20:49:37 GMT  
		Size: 50.3 MB (50294599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff09de9a10ff310613b84e648fcbcb168aac2c6f6fa63ffbd10d58c2fa7e456`  
		Last Modified: Wed, 25 Jan 2023 20:49:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5eef20df6de484799bde83de7708971f47706816120d0eeef076792236116b`  
		Last Modified: Wed, 25 Jan 2023 21:53:37 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5684a0ac10b93a9edd850e0ef1b45dc27c041473e8da9b30ee3d7476d8ac3d`  
		Last Modified: Wed, 25 Jan 2023 21:56:06 GMT  
		Size: 12.0 MB (12011921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4871ddb7ff0457ccf99d037ab19a6b0eb2bf2acc1533cd12cf027639363010`  
		Last Modified: Wed, 25 Jan 2023 21:56:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40cc0824716930a424bb0173ada203ca572e0b3faf69828170e703a04a8c248d`  
		Last Modified: Wed, 25 Jan 2023 22:19:00 GMT  
		Size: 314.5 MB (314541834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad21ac3b46e8b54a4d8b7a30971c3aee438c6115c30f9dcc238c949e2eee0eb`  
		Last Modified: Wed, 25 Jan 2023 22:18:30 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c42eba12c7de701a2b02ebf0ff0442de9b97a95bafab59be1b6fc51f13f7a2b`  
		Last Modified: Wed, 25 Jan 2023 22:19:18 GMT  
		Size: 12.7 MB (12746779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e483875e67cbd3479f4bbe0dbbb0a08c6d48db5569c2f7d217dfecf3d994f248`  
		Last Modified: Wed, 25 Jan 2023 22:19:14 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750dbcdc9dfe9e7357e195b925daee7576d01a5c5f05e4a2d3a5ae170ec1bab7`  
		Last Modified: Wed, 25 Jan 2023 22:19:14 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88c54b1fc1cf7de7b3c52ae545a1d778073770910113cbd4888f0360f2a8d32`  
		Last Modified: Wed, 25 Jan 2023 22:19:14 GMT  
		Size: 974.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3.12.8-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:6b7f83671310da252f8160256beba1589d0fb8bc16a87299167c69761059194c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.3 MB (434348381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cc627a57ee310022912fc7264bf31395fa5262def744b720807fc31274ef09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 26 Jan 2023 05:05:49 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:05:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:05:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:05:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:05:51 GMT
ADD file:55486a91f732042dd4e81ecfd8457d23e04dcd7dd80a0bb06cc7c44873fac838 in / 
# Thu, 26 Jan 2023 05:05:51 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:43:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Jan 2023 17:43:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 17:43:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Jan 2023 17:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:44:32 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Tue, 31 Jan 2023 17:44:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 31 Jan 2023 17:44:38 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 31 Jan 2023 22:17:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 31 Jan 2023 22:17:17 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 22:17:18 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 31 Jan 2023 22:17:18 GMT
WORKDIR /usr/local/tomcat
# Tue, 31 Jan 2023 22:17:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 31 Jan 2023 22:17:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 31 Jan 2023 22:21:26 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 31 Jan 2023 22:21:26 GMT
ENV TOMCAT_MAJOR=8
# Tue, 31 Jan 2023 22:21:26 GMT
ENV TOMCAT_VERSION=8.5.85
# Tue, 31 Jan 2023 22:21:26 GMT
ENV TOMCAT_SHA512=0fc44133aff9e7e31d6dbb4b6e204d33bd0009b6bd089e5f8c8a1f7dfe7c5feff25d7f6404c4a3c5610e0960b5d0198580171212a2636816a23e21799a4c0467
# Tue, 31 Jan 2023 22:21:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 31 Jan 2023 22:21:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 31 Jan 2023 22:21:56 GMT
EXPOSE 8080
# Tue, 31 Jan 2023 22:21:56 GMT
CMD ["catalina.sh" "run"]
# Wed, 01 Feb 2023 00:07:22 GMT
ENV GN_FILE=geonetwork.war
# Wed, 01 Feb 2023 00:07:22 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Wed, 01 Feb 2023 00:07:22 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Wed, 01 Feb 2023 00:07:22 GMT
ENV GN_VERSION=3.12.8
# Wed, 01 Feb 2023 00:07:22 GMT
ENV GN_DOWNLOAD_MD5=378b70ee5c358a8db5659dafc8220e9f
# Wed, 01 Feb 2023 00:07:23 GMT
WORKDIR /usr/local/tomcat/webapps
# Wed, 01 Feb 2023 00:07:51 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Wed, 01 Feb 2023 00:07:54 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Wed, 01 Feb 2023 00:07:54 GMT
WORKDIR /usr/local/tomcat
# Wed, 01 Feb 2023 00:07:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Feb 2023 00:07:54 GMT
CMD ["catalina.sh" "run"]
# Wed, 01 Feb 2023 00:08:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 00:08:12 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml"
# Wed, 01 Feb 2023 00:08:12 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Wed, 01 Feb 2023 00:08:12 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Wed, 01 Feb 2023 00:08:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Feb 2023 00:08:12 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:565cb979c5c01279efcd69c4457a9954801b6be6da65894374260ec92d993891`  
		Last Modified: Thu, 26 Jan 2023 16:22:40 GMT  
		Size: 28.4 MB (28384974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c6471d4f305436bdd6e09ea64bdf7a303979f4d8cdb6c9606715fc21afa9ad`  
		Last Modified: Tue, 31 Jan 2023 17:50:26 GMT  
		Size: 12.4 MB (12391264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427df1d8bddcc93bab1efadcf6f2157f2d58b6366e437f130fb7ad8676a8a64f`  
		Last Modified: Tue, 31 Jan 2023 17:50:30 GMT  
		Size: 53.7 MB (53731740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1db467a77eb3093981e70f61997b6ade2c0b5662ace92eef00c082999f55dd6`  
		Last Modified: Tue, 31 Jan 2023 17:50:24 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7899e6f25670a980cf6b742a0443e29000441ee96c6e5189434396b495bd94bd`  
		Last Modified: Tue, 31 Jan 2023 22:33:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a6489f84d41cef926fc329042d2b342b71eea669b80dfaaba20df41ab717d2`  
		Last Modified: Tue, 31 Jan 2023 22:37:21 GMT  
		Size: 11.7 MB (11700782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde69c27b4cbedaf2799b7e23125b3a7df2b63dcd80268f9dded343986b26651`  
		Last Modified: Tue, 31 Jan 2023 22:37:20 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cc6e867e17538390665f99ad6fbc71809c09b4d6b59c2ed851480589821fc6`  
		Last Modified: Wed, 01 Feb 2023 00:11:48 GMT  
		Size: 314.5 MB (314546078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89beff1eb4faa366b06d9e01c3a457d27f611d3a9203a30f3544ca2055b3278e`  
		Last Modified: Wed, 01 Feb 2023 00:11:33 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead097cb103eb8f3905fb1aae03facf47ddddbba7a29fafdf2c21f44a17aaceb`  
		Last Modified: Wed, 01 Feb 2023 00:12:01 GMT  
		Size: 13.6 MB (13589469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1a7c2999db39cde2b3daed0bf6016943869624901737c288c61fe970adccc5`  
		Last Modified: Wed, 01 Feb 2023 00:11:59 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ee1fcade266471825b561bea3e8b4a9f3ecd1085dfd940feb95d8bac21a839`  
		Last Modified: Wed, 01 Feb 2023 00:11:59 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcef798b22bcbe2756ec9d640d3da95d1107c0500dc7f6518f07fc1c9e710d93`  
		Last Modified: Wed, 01 Feb 2023 00:11:59 GMT  
		Size: 972.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:3.12.8-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:80eebeeb850bffc1cf3094e95f32e790650c75ca89578de692f713cc4a47b18e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.2 MB (442220044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89fbee9e3c422dd025072975a6bf5432e9a62d3073528720563fdda5ac5ed8ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Dec 2022 01:27:53 GMT
ADD file:1a2557b357a1dca8521ee846ec16c9b2bd8a53839b9d4fda21a28f9ceeecb4b7 in / 
# Fri, 09 Dec 2022 01:27:55 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:39:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 02:39:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 02:39:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 02:40:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 19:38:40 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 19:38:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 19:38:54 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 20:49:25 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 25 Jan 2023 20:49:25 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 20:49:27 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 25 Jan 2023 20:49:27 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 20:49:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 20:49:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 25 Jan 2023 20:53:23 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 25 Jan 2023 20:53:23 GMT
ENV TOMCAT_MAJOR=8
# Wed, 25 Jan 2023 20:53:23 GMT
ENV TOMCAT_VERSION=8.5.85
# Wed, 25 Jan 2023 20:53:24 GMT
ENV TOMCAT_SHA512=0fc44133aff9e7e31d6dbb4b6e204d33bd0009b6bd089e5f8c8a1f7dfe7c5feff25d7f6404c4a3c5610e0960b5d0198580171212a2636816a23e21799a4c0467
# Wed, 25 Jan 2023 20:54:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 25 Jan 2023 20:54:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 25 Jan 2023 20:54:28 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 20:54:28 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 21:24:58 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 21:24:58 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Wed, 25 Jan 2023 21:24:58 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Wed, 25 Jan 2023 21:24:59 GMT
ENV GN_VERSION=3.12.8
# Wed, 25 Jan 2023 21:24:59 GMT
ENV GN_DOWNLOAD_MD5=378b70ee5c358a8db5659dafc8220e9f
# Wed, 25 Jan 2023 21:24:59 GMT
WORKDIR /usr/local/tomcat/webapps
# Wed, 25 Jan 2023 21:25:44 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE
# Wed, 25 Jan 2023 21:25:49 GMT
COPY file:0804862fd42c05f06dfa65cb1e5dad9a956d8ac6a3ddd4d962847ba159f5cfe6 in /entrypoint.sh 
# Wed, 25 Jan 2023 21:25:50 GMT
WORKDIR /usr/local/tomcat
# Wed, 25 Jan 2023 21:25:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 21:25:50 GMT
CMD ["catalina.sh" "run"]
# Wed, 25 Jan 2023 21:26:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 21:26:15 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml"
# Wed, 25 Jan 2023 21:26:16 GMT
COPY file:83f69d2041e5fb378033b0db57e096c81ba0725102ab4da4f089685e748fcce3 in /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties 
# Wed, 25 Jan 2023 21:26:16 GMT
COPY file:c88411abba7ad9b7bb75019f08755dbfa163d2fc7fdd80676bf9350c4c56a19c in /entrypoint.sh 
# Wed, 25 Jan 2023 21:26:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Jan 2023 21:26:16 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ce75b47e476cd75b30dca46558ac79b39923aa94d7e4b0cc025e521404cdbab0`  
		Last Modified: Fri, 09 Dec 2022 01:30:32 GMT  
		Size: 35.7 MB (35708154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a782dc6ae3d6a01674486598e1b3cdcfaa9696ad3e2125e712884667b1c2c37f`  
		Last Modified: Fri, 09 Dec 2022 02:53:02 GMT  
		Size: 13.2 MB (13245456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f293f07451d1ca9101f6406ed167fb8798e49df8ddf8acee518c3db37b0b185`  
		Last Modified: Wed, 25 Jan 2023 19:57:54 GMT  
		Size: 52.1 MB (52112863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44c8bdf138d6084aeef40083fb29771e2cf786714a4d644ae79155891980939`  
		Last Modified: Wed, 25 Jan 2023 19:57:43 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4377ec606c42192ec93ed57b0a6a47b5cf42197a7550956938bebe5b2af38092`  
		Last Modified: Wed, 25 Jan 2023 21:05:49 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7c80c538568990206ee80f8a97620c122e77bc741305edeb516e087a766ff0`  
		Last Modified: Wed, 25 Jan 2023 21:08:11 GMT  
		Size: 12.4 MB (12351915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42be51b9cbf813f7af62d54e2a22d3f530d0d10a7dcfdfc3d0c9fb60f7dde79a`  
		Last Modified: Wed, 25 Jan 2023 21:08:09 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c16a3b36d2811deb888f04f3faddc80c02ee1890aa6656c8e449db702394d94`  
		Last Modified: Wed, 25 Jan 2023 21:27:13 GMT  
		Size: 314.6 MB (314591645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d14d8b67adf6b89f3a363611e2f7154b8a03098727d05b9963cf8ad3e7111af`  
		Last Modified: Wed, 25 Jan 2023 21:26:40 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e2c94d250e8825f5f212d2148752c27e05cdc8e79d88c7708775f5208f63a7`  
		Last Modified: Wed, 25 Jan 2023 21:27:32 GMT  
		Size: 14.2 MB (14205935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0351a129914867b8f57ac45898de75ca74c15bc7d8862258bed63eda4ba715`  
		Last Modified: Wed, 25 Jan 2023 21:27:27 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337c5135361a9019849545b450f57c59c8e170f1f980263e2b01a282ea0a29d7`  
		Last Modified: Wed, 25 Jan 2023 21:27:27 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3368d45b2c541562116af80a1edb6db89c528fc6247486100f546254e56c2d`  
		Last Modified: Wed, 25 Jan 2023 21:27:27 GMT  
		Size: 973.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:4`

```console
$ docker pull geonetwork@sha256:2cc3df2f4d502bc566e5ef27b7679620d7721b832f76b777c3a82fc94602f7bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `geonetwork:4` - linux; amd64

```console
$ docker pull geonetwork@sha256:8521398b72c9c20050ef5ce54de53063758dce617c39f537dc3eeda70245e013
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.7 MB (434742040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9761f1ae7db4d5a268325e14c55196e4243b163c7096e1a7cd99715e43aa8e`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:42:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 01:42:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 01:42:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 01:42:42 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 19:19:58 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 19:20:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 19:20:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 21:21:14 GMT
ENV JETTY_VERSION=9.4.50.v20221201
# Wed, 25 Jan 2023 21:21:14 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 25 Jan 2023 21:21:14 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 25 Jan 2023 21:21:14 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 25 Jan 2023 21:21:14 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 21:21:15 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.50.v20221201/jetty-home-9.4.50.v20221201.tar.gz
# Wed, 25 Jan 2023 21:21:15 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Wed, 25 Jan 2023 21:21:36 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 25 Jan 2023 21:21:36 GMT
WORKDIR /var/lib/jetty
# Wed, 25 Jan 2023 21:21:36 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Wed, 25 Jan 2023 21:21:36 GMT
USER jetty
# Wed, 25 Jan 2023 21:21:36 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 21:21:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2023 21:21:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Wed, 25 Jan 2023 21:41:17 GMT
ENV DATA_DIR=/catalogue-data
# Wed, 25 Jan 2023 21:41:17 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Wed, 25 Jan 2023 21:41:17 GMT
USER root
# Wed, 25 Jan 2023 21:42:45 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork
# Wed, 25 Jan 2023 21:42:45 GMT
USER jetty
# Wed, 25 Jan 2023 21:42:45 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 21:42:45 GMT
ENV GN_VERSION=4.2.2
# Wed, 25 Jan 2023 21:42:45 GMT
ENV GN_DOWNLOAD_MD5=ec7f0c956fe07737fb6fa77fa4e9aaf5
# Wed, 25 Jan 2023 21:43:12 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war
# Wed, 25 Jan 2023 21:43:13 GMT
COPY file:ca46ab251df3dfc253cb04cf962e7266e42428fab31ad2f583a7c86b06d5f778 in /geonetwork-entrypoint.sh 
# Wed, 25 Jan 2023 21:43:14 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Wed, 25 Jan 2023 21:43:14 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Wed, 25 Jan 2023 21:43:14 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9923132fe6ab2c95fb9e2363f361139b8e50b7264d78acb7cf60147742acc985`  
		Last Modified: Fri, 09 Dec 2022 01:49:42 GMT  
		Size: 16.3 MB (16333067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37fb312ae19f62ad480ce6086c9b6578ca2410115a9273a116277a4baa172c3`  
		Last Modified: Wed, 25 Jan 2023 19:26:09 GMT  
		Size: 54.6 MB (54635847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2e2b34b018853989bb73ef5b890ce38ef7577705dae25d3af5b7167b1a630a`  
		Last Modified: Wed, 25 Jan 2023 19:26:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4f5af6f8772e4f84d1046d9b88b101b6cf877e58620bf8c096e58ba886bde0`  
		Last Modified: Wed, 25 Jan 2023 21:26:22 GMT  
		Size: 10.7 MB (10665854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02cc6c770c632ee829d89db00897318fe31c77d559b2df6754e8f4b2af71626`  
		Last Modified: Wed, 25 Jan 2023 21:26:21 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e799414ffae132617f7f90910d8c2bc59b4679328672d282158ef955c4b508`  
		Last Modified: Wed, 25 Jan 2023 21:44:46 GMT  
		Size: 482.1 KB (482054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2ede78d46ba6ba05067e43b6de8325d02ec48fb4da00c3d62f6f2384c65264`  
		Last Modified: Wed, 25 Jan 2023 21:45:04 GMT  
		Size: 324.0 MB (324045776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4fb39f80727c7e8e1119f3d4f0b838ac55bd08b31ca6694252e9856e58d453`  
		Last Modified: Wed, 25 Jan 2023 21:44:46 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:4` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:25153c949c874c1a8a92b539a8bfe01090ca94d90af43c2e48abfa0e134e0139
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.9 MB (431904953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dbdf5457d2366663ed1215dbecb5a95b97a014394153d320c425ce18fcffc64`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 26 Jan 2023 13:50:26 GMT
ARG RELEASE
# Thu, 26 Jan 2023 13:50:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 13:50:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 13:50:26 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Jan 2023 13:50:33 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Thu, 26 Jan 2023 13:50:33 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:43:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Jan 2023 17:43:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 17:43:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Jan 2023 17:43:47 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:43:47 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Tue, 31 Jan 2023 17:43:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 31 Jan 2023 17:43:54 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 31 Jan 2023 21:39:58 GMT
ENV JETTY_VERSION=9.4.50.v20221201
# Tue, 31 Jan 2023 21:39:58 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 31 Jan 2023 21:39:58 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 31 Jan 2023 21:39:58 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 31 Jan 2023 21:39:58 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 21:39:58 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.50.v20221201/jetty-home-9.4.50.v20221201.tar.gz
# Tue, 31 Jan 2023 21:39:58 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Tue, 31 Jan 2023 21:40:22 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 31 Jan 2023 21:40:22 GMT
WORKDIR /var/lib/jetty
# Tue, 31 Jan 2023 21:40:22 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Tue, 31 Jan 2023 21:40:23 GMT
USER jetty
# Tue, 31 Jan 2023 21:40:23 GMT
EXPOSE 8080
# Tue, 31 Jan 2023 21:40:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 31 Jan 2023 21:40:23 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Wed, 01 Feb 2023 00:08:16 GMT
ENV DATA_DIR=/catalogue-data
# Wed, 01 Feb 2023 00:08:16 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Wed, 01 Feb 2023 00:08:16 GMT
USER root
# Wed, 01 Feb 2023 00:09:57 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork
# Wed, 01 Feb 2023 00:09:57 GMT
USER jetty
# Wed, 01 Feb 2023 00:09:57 GMT
ENV GN_FILE=geonetwork.war
# Wed, 01 Feb 2023 00:09:57 GMT
ENV GN_VERSION=4.2.2
# Wed, 01 Feb 2023 00:09:57 GMT
ENV GN_DOWNLOAD_MD5=ec7f0c956fe07737fb6fa77fa4e9aaf5
# Wed, 01 Feb 2023 00:11:08 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war
# Wed, 01 Feb 2023 00:11:11 GMT
COPY file:ca46ab251df3dfc253cb04cf962e7266e42428fab31ad2f583a7c86b06d5f778 in /geonetwork-entrypoint.sh 
# Wed, 01 Feb 2023 00:11:11 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Wed, 01 Feb 2023 00:11:11 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Wed, 01 Feb 2023 00:11:11 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:70cf24b162395e1500d40f2b012f253bfd5d15f029ef9d636620fa2365ae503c`  
		Last Modified: Sat, 28 Jan 2023 04:42:53 GMT  
		Size: 27.2 MB (27193737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df2d776c5c5ff7acd285901b61b2f581c9497f13a32d1a49db14e3a2b7536be`  
		Last Modified: Tue, 31 Jan 2023 17:50:10 GMT  
		Size: 16.2 MB (16204764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4103d41b1c8038835a70eb150c22630469a69dc0fbf4d2a145a66fd5933fa4`  
		Last Modified: Tue, 31 Jan 2023 17:50:14 GMT  
		Size: 53.7 MB (53731802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01405e9f1524563ba14196dbf4b895c52e338e811525843741ebfd476059064d`  
		Last Modified: Tue, 31 Jan 2023 17:50:08 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857686237cbd6157df6e07096f621e4a67cf7645f5729dc93b69be9ab7362e49`  
		Last Modified: Tue, 31 Jan 2023 21:47:05 GMT  
		Size: 10.2 MB (10246946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a6004eb04ad590eae65d9975762346aea6a1b3f4b1b16762ff6d89827347b9`  
		Last Modified: Tue, 31 Jan 2023 21:47:04 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3f22cf36625da7754d4786faeb1f7277b3da0454a744226a1d5a0014d9e109`  
		Last Modified: Wed, 01 Feb 2023 00:12:38 GMT  
		Size: 479.5 KB (479456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791872acc7b2708541156a96126846e1c7bd78d61e11b9635fafcc15690c0eca`  
		Last Modified: Wed, 01 Feb 2023 00:12:52 GMT  
		Size: 324.0 MB (324045687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb46b3a93c55c90fc58f54ec4aebab7f657587c82773cc34a7e8166a5651994b`  
		Last Modified: Wed, 01 Feb 2023 00:12:37 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:4.0`

```console
$ docker pull geonetwork@sha256:b97a3fccdec2bba8103a0c1d4649d148459e3d290634da1605fd27ab49375c2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `geonetwork:4.0` - linux; amd64

```console
$ docker pull geonetwork@sha256:40f616d0c3820a55810a8b192e6cf7efdd780ce08dae2421dd5f42b4d1717852
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.1 MB (467060316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0181e10a5a2bd7599fe05171bca645c5641b964b3a22faa8197bddd0ff1275c`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:42:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 01:42:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 01:42:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 01:42:42 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 19:19:58 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 19:20:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 19:20:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 21:21:14 GMT
ENV JETTY_VERSION=9.4.50.v20221201
# Wed, 25 Jan 2023 21:21:14 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 25 Jan 2023 21:21:14 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 25 Jan 2023 21:21:14 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 25 Jan 2023 21:21:14 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 21:21:15 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.50.v20221201/jetty-home-9.4.50.v20221201.tar.gz
# Wed, 25 Jan 2023 21:21:15 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Wed, 25 Jan 2023 21:21:36 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 25 Jan 2023 21:21:36 GMT
WORKDIR /var/lib/jetty
# Wed, 25 Jan 2023 21:21:36 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Wed, 25 Jan 2023 21:21:36 GMT
USER jetty
# Wed, 25 Jan 2023 21:21:36 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 21:21:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2023 21:21:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Wed, 25 Jan 2023 21:41:17 GMT
ENV DATA_DIR=/catalogue-data
# Wed, 25 Jan 2023 21:41:17 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Wed, 25 Jan 2023 21:41:17 GMT
USER root
# Wed, 25 Jan 2023 21:41:23 GMT
RUN apt-get -y update &&     apt-get -y install         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork
# Wed, 25 Jan 2023 21:41:23 GMT
USER jetty
# Wed, 25 Jan 2023 21:41:23 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 21:41:23 GMT
ENV GN_VERSION=4.0.6
# Wed, 25 Jan 2023 21:41:23 GMT
ENV GN_DOWNLOAD_MD5=793732cb9c723e73857a4da73b78451b
# Wed, 25 Jan 2023 21:42:36 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war
# Wed, 25 Jan 2023 21:42:38 GMT
COPY file:ca46ab251df3dfc253cb04cf962e7266e42428fab31ad2f583a7c86b06d5f778 in /geonetwork-entrypoint.sh 
# Wed, 25 Jan 2023 21:42:38 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Wed, 25 Jan 2023 21:42:38 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Wed, 25 Jan 2023 21:42:38 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9923132fe6ab2c95fb9e2363f361139b8e50b7264d78acb7cf60147742acc985`  
		Last Modified: Fri, 09 Dec 2022 01:49:42 GMT  
		Size: 16.3 MB (16333067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37fb312ae19f62ad480ce6086c9b6578ca2410115a9273a116277a4baa172c3`  
		Last Modified: Wed, 25 Jan 2023 19:26:09 GMT  
		Size: 54.6 MB (54635847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2e2b34b018853989bb73ef5b890ce38ef7577705dae25d3af5b7167b1a630a`  
		Last Modified: Wed, 25 Jan 2023 19:26:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4f5af6f8772e4f84d1046d9b88b101b6cf877e58620bf8c096e58ba886bde0`  
		Last Modified: Wed, 25 Jan 2023 21:26:22 GMT  
		Size: 10.7 MB (10665854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02cc6c770c632ee829d89db00897318fe31c77d559b2df6754e8f4b2af71626`  
		Last Modified: Wed, 25 Jan 2023 21:26:21 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c0bf67760b01925f189d262d7adcbfd3e450676fb9194592cb7de4ddfe55ab`  
		Last Modified: Wed, 25 Jan 2023 21:44:19 GMT  
		Size: 482.1 KB (482057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e15ddec6bed76862e1a2bb9f266db057c6aea848da5b600451facd799aaa7c`  
		Last Modified: Wed, 25 Jan 2023 21:44:37 GMT  
		Size: 356.4 MB (356364053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250ece08ee971e2dd8634966b43c8d65d05749f0cc619c50fdf0179c6a5528bf`  
		Last Modified: Wed, 25 Jan 2023 21:44:18 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:4.0` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:712a2ee6f12e885b2ffbc265a50b1d029693c1c2bf30471f44cf743916e57a96
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.2 MB (464223311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da732d75895106164fa1fbcfd9cce27606feeb3e8f60dd278392c1a9bffea7bb`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 26 Jan 2023 13:50:26 GMT
ARG RELEASE
# Thu, 26 Jan 2023 13:50:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 13:50:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 13:50:26 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Jan 2023 13:50:33 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Thu, 26 Jan 2023 13:50:33 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:43:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Jan 2023 17:43:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 17:43:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Jan 2023 17:43:47 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:43:47 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Tue, 31 Jan 2023 17:43:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 31 Jan 2023 17:43:54 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 31 Jan 2023 21:39:58 GMT
ENV JETTY_VERSION=9.4.50.v20221201
# Tue, 31 Jan 2023 21:39:58 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 31 Jan 2023 21:39:58 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 31 Jan 2023 21:39:58 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 31 Jan 2023 21:39:58 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 21:39:58 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.50.v20221201/jetty-home-9.4.50.v20221201.tar.gz
# Tue, 31 Jan 2023 21:39:58 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Tue, 31 Jan 2023 21:40:22 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 31 Jan 2023 21:40:22 GMT
WORKDIR /var/lib/jetty
# Tue, 31 Jan 2023 21:40:22 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Tue, 31 Jan 2023 21:40:23 GMT
USER jetty
# Tue, 31 Jan 2023 21:40:23 GMT
EXPOSE 8080
# Tue, 31 Jan 2023 21:40:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 31 Jan 2023 21:40:23 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Wed, 01 Feb 2023 00:08:16 GMT
ENV DATA_DIR=/catalogue-data
# Wed, 01 Feb 2023 00:08:16 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Wed, 01 Feb 2023 00:08:16 GMT
USER root
# Wed, 01 Feb 2023 00:08:26 GMT
RUN apt-get -y update &&     apt-get -y install         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork
# Wed, 01 Feb 2023 00:08:26 GMT
USER jetty
# Wed, 01 Feb 2023 00:08:26 GMT
ENV GN_FILE=geonetwork.war
# Wed, 01 Feb 2023 00:08:26 GMT
ENV GN_VERSION=4.0.6
# Wed, 01 Feb 2023 00:08:26 GMT
ENV GN_DOWNLOAD_MD5=793732cb9c723e73857a4da73b78451b
# Wed, 01 Feb 2023 00:09:45 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war
# Wed, 01 Feb 2023 00:09:48 GMT
COPY file:ca46ab251df3dfc253cb04cf962e7266e42428fab31ad2f583a7c86b06d5f778 in /geonetwork-entrypoint.sh 
# Wed, 01 Feb 2023 00:09:48 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Wed, 01 Feb 2023 00:09:48 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Wed, 01 Feb 2023 00:09:48 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:70cf24b162395e1500d40f2b012f253bfd5d15f029ef9d636620fa2365ae503c`  
		Last Modified: Sat, 28 Jan 2023 04:42:53 GMT  
		Size: 27.2 MB (27193737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df2d776c5c5ff7acd285901b61b2f581c9497f13a32d1a49db14e3a2b7536be`  
		Last Modified: Tue, 31 Jan 2023 17:50:10 GMT  
		Size: 16.2 MB (16204764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4103d41b1c8038835a70eb150c22630469a69dc0fbf4d2a145a66fd5933fa4`  
		Last Modified: Tue, 31 Jan 2023 17:50:14 GMT  
		Size: 53.7 MB (53731802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01405e9f1524563ba14196dbf4b895c52e338e811525843741ebfd476059064d`  
		Last Modified: Tue, 31 Jan 2023 17:50:08 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857686237cbd6157df6e07096f621e4a67cf7645f5729dc93b69be9ab7362e49`  
		Last Modified: Tue, 31 Jan 2023 21:47:05 GMT  
		Size: 10.2 MB (10246946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a6004eb04ad590eae65d9975762346aea6a1b3f4b1b16762ff6d89827347b9`  
		Last Modified: Tue, 31 Jan 2023 21:47:04 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895673bd28d0705e19a9f1d65257766a6d28b0506a2d5ca60a51ea920c9ff110`  
		Last Modified: Wed, 01 Feb 2023 00:12:13 GMT  
		Size: 479.5 KB (479451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a431f53fe71527728a79db57c634aa955a64f733d6277af3b5df8d29834add94`  
		Last Modified: Wed, 01 Feb 2023 00:12:29 GMT  
		Size: 356.4 MB (356364050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2658759ce953d7885408c6ec281ef3bec4f0a54ae0f9790ef1a18723e4c39387`  
		Last Modified: Wed, 01 Feb 2023 00:12:14 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:4.0.6`

```console
$ docker pull geonetwork@sha256:a707a063b84a056ae0ab6c879a60b642ad54fd7a588c9cdc52160b83c1ccf6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `geonetwork:4.0.6` - linux; amd64

```console
$ docker pull geonetwork@sha256:40f616d0c3820a55810a8b192e6cf7efdd780ce08dae2421dd5f42b4d1717852
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.1 MB (467060316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0181e10a5a2bd7599fe05171bca645c5641b964b3a22faa8197bddd0ff1275c`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:42:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 01:42:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 01:42:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 01:42:42 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 19:19:58 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 19:20:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 19:20:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 21:21:14 GMT
ENV JETTY_VERSION=9.4.50.v20221201
# Wed, 25 Jan 2023 21:21:14 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 25 Jan 2023 21:21:14 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 25 Jan 2023 21:21:14 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 25 Jan 2023 21:21:14 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 21:21:15 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.50.v20221201/jetty-home-9.4.50.v20221201.tar.gz
# Wed, 25 Jan 2023 21:21:15 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Wed, 25 Jan 2023 21:21:36 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 25 Jan 2023 21:21:36 GMT
WORKDIR /var/lib/jetty
# Wed, 25 Jan 2023 21:21:36 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Wed, 25 Jan 2023 21:21:36 GMT
USER jetty
# Wed, 25 Jan 2023 21:21:36 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 21:21:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2023 21:21:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Wed, 25 Jan 2023 21:41:17 GMT
ENV DATA_DIR=/catalogue-data
# Wed, 25 Jan 2023 21:41:17 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Wed, 25 Jan 2023 21:41:17 GMT
USER root
# Wed, 25 Jan 2023 21:41:23 GMT
RUN apt-get -y update &&     apt-get -y install         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork
# Wed, 25 Jan 2023 21:41:23 GMT
USER jetty
# Wed, 25 Jan 2023 21:41:23 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 21:41:23 GMT
ENV GN_VERSION=4.0.6
# Wed, 25 Jan 2023 21:41:23 GMT
ENV GN_DOWNLOAD_MD5=793732cb9c723e73857a4da73b78451b
# Wed, 25 Jan 2023 21:42:36 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war
# Wed, 25 Jan 2023 21:42:38 GMT
COPY file:ca46ab251df3dfc253cb04cf962e7266e42428fab31ad2f583a7c86b06d5f778 in /geonetwork-entrypoint.sh 
# Wed, 25 Jan 2023 21:42:38 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Wed, 25 Jan 2023 21:42:38 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Wed, 25 Jan 2023 21:42:38 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9923132fe6ab2c95fb9e2363f361139b8e50b7264d78acb7cf60147742acc985`  
		Last Modified: Fri, 09 Dec 2022 01:49:42 GMT  
		Size: 16.3 MB (16333067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37fb312ae19f62ad480ce6086c9b6578ca2410115a9273a116277a4baa172c3`  
		Last Modified: Wed, 25 Jan 2023 19:26:09 GMT  
		Size: 54.6 MB (54635847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2e2b34b018853989bb73ef5b890ce38ef7577705dae25d3af5b7167b1a630a`  
		Last Modified: Wed, 25 Jan 2023 19:26:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4f5af6f8772e4f84d1046d9b88b101b6cf877e58620bf8c096e58ba886bde0`  
		Last Modified: Wed, 25 Jan 2023 21:26:22 GMT  
		Size: 10.7 MB (10665854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02cc6c770c632ee829d89db00897318fe31c77d559b2df6754e8f4b2af71626`  
		Last Modified: Wed, 25 Jan 2023 21:26:21 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c0bf67760b01925f189d262d7adcbfd3e450676fb9194592cb7de4ddfe55ab`  
		Last Modified: Wed, 25 Jan 2023 21:44:19 GMT  
		Size: 482.1 KB (482057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e15ddec6bed76862e1a2bb9f266db057c6aea848da5b600451facd799aaa7c`  
		Last Modified: Wed, 25 Jan 2023 21:44:37 GMT  
		Size: 356.4 MB (356364053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250ece08ee971e2dd8634966b43c8d65d05749f0cc619c50fdf0179c6a5528bf`  
		Last Modified: Wed, 25 Jan 2023 21:44:18 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:4.0.6` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:d996a971b0ce5c22a2aa4821a69f7a6a4352ec7130417b3ff5fc68ac664c152e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.6 MB (464635797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8996246f00d6371619958c1c930bde9ed7608362396621394b5ce129bb257343`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:50 GMT
ADD file:8cba976cb6ea226de769a768ee274e7679d34f923c93392f340680dc6696232e in / 
# Fri, 09 Dec 2022 01:46:50 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:38:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 03:38:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 03:38:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 03:39:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 18:39:33 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 18:39:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 18:39:42 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 20:36:07 GMT
ENV JETTY_VERSION=9.4.50.v20221201
# Wed, 25 Jan 2023 20:36:07 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 25 Jan 2023 20:36:08 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 25 Jan 2023 20:36:08 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 25 Jan 2023 20:36:08 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 20:36:08 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.50.v20221201/jetty-home-9.4.50.v20221201.tar.gz
# Wed, 25 Jan 2023 20:36:08 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Wed, 25 Jan 2023 20:36:27 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 25 Jan 2023 20:36:27 GMT
WORKDIR /var/lib/jetty
# Wed, 25 Jan 2023 20:36:27 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Wed, 25 Jan 2023 20:36:27 GMT
USER jetty
# Wed, 25 Jan 2023 20:36:27 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 20:36:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2023 20:36:27 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Wed, 25 Jan 2023 21:26:31 GMT
ENV DATA_DIR=/catalogue-data
# Wed, 25 Jan 2023 21:26:32 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Wed, 25 Jan 2023 21:26:32 GMT
USER root
# Wed, 25 Jan 2023 21:26:37 GMT
RUN apt-get -y update &&     apt-get -y install         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork
# Wed, 25 Jan 2023 21:26:37 GMT
USER jetty
# Wed, 25 Jan 2023 21:26:37 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 21:26:37 GMT
ENV GN_VERSION=4.0.6
# Wed, 25 Jan 2023 21:26:38 GMT
ENV GN_DOWNLOAD_MD5=793732cb9c723e73857a4da73b78451b
# Wed, 25 Jan 2023 21:27:55 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war
# Wed, 25 Jan 2023 21:27:58 GMT
COPY file:ca46ab251df3dfc253cb04cf962e7266e42428fab31ad2f583a7c86b06d5f778 in /geonetwork-entrypoint.sh 
# Wed, 25 Jan 2023 21:27:58 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Wed, 25 Jan 2023 21:27:58 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Wed, 25 Jan 2023 21:27:58 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:f04b4bbe15805316c8fda79beedd3b77e6b1ffcd0acf81226c3089e63f6bffeb`  
		Last Modified: Thu, 08 Dec 2022 15:28:02 GMT  
		Size: 27.2 MB (27193168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d371657879ab4e130d4ef0cad592b6a80196fce854ad341ab9641b484d81b17`  
		Last Modified: Fri, 09 Dec 2022 03:45:13 GMT  
		Size: 16.2 MB (16202837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5249d3752cf871523259f9129f95921a4934b297e86babf342e1b7a305e75d`  
		Last Modified: Wed, 25 Jan 2023 18:44:28 GMT  
		Size: 53.7 MB (53731796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25339c95d0de7be743d79b03d3efb98a5cc0a8ef92150eba90f8c4cd4db30f39`  
		Last Modified: Wed, 25 Jan 2023 18:44:23 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3ee72afb526f5b06a1f25daedfd8c8616770d7ec47d04c7ab794a0b26d0fed`  
		Last Modified: Wed, 25 Jan 2023 20:39:16 GMT  
		Size: 10.7 MB (10661701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3359c6619dec9895f9dc70688c1ea119a2d671bfb0135abd1326fbe9c4b8e246`  
		Last Modified: Wed, 25 Jan 2023 20:39:15 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6e2707061073753e3c3154b45d15467f7e0ba50b85bfa58fc5594665f6df1f`  
		Last Modified: Wed, 25 Jan 2023 21:30:29 GMT  
		Size: 479.7 KB (479684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6562431434c38a6f16c932d5476f257fa174d1fd14887f6e9ac295199c161e`  
		Last Modified: Wed, 25 Jan 2023 21:30:44 GMT  
		Size: 356.4 MB (356364050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719d99e515eec0f5ec74c4bdae717d12caf56d1bddc45480fdace6bea899a619`  
		Last Modified: Wed, 25 Jan 2023 21:30:28 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:4.2`

```console
$ docker pull geonetwork@sha256:d10e0c50f0e9358f3de346f5faa46209c3e9ade855eaf3d62ceddeac7b3f3b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `geonetwork:4.2` - linux; amd64

```console
$ docker pull geonetwork@sha256:8521398b72c9c20050ef5ce54de53063758dce617c39f537dc3eeda70245e013
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.7 MB (434742040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9761f1ae7db4d5a268325e14c55196e4243b163c7096e1a7cd99715e43aa8e`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:42:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 01:42:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 01:42:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 01:42:42 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 19:19:58 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 19:20:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 19:20:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 21:21:14 GMT
ENV JETTY_VERSION=9.4.50.v20221201
# Wed, 25 Jan 2023 21:21:14 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 25 Jan 2023 21:21:14 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 25 Jan 2023 21:21:14 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 25 Jan 2023 21:21:14 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 21:21:15 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.50.v20221201/jetty-home-9.4.50.v20221201.tar.gz
# Wed, 25 Jan 2023 21:21:15 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Wed, 25 Jan 2023 21:21:36 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 25 Jan 2023 21:21:36 GMT
WORKDIR /var/lib/jetty
# Wed, 25 Jan 2023 21:21:36 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Wed, 25 Jan 2023 21:21:36 GMT
USER jetty
# Wed, 25 Jan 2023 21:21:36 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 21:21:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2023 21:21:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Wed, 25 Jan 2023 21:41:17 GMT
ENV DATA_DIR=/catalogue-data
# Wed, 25 Jan 2023 21:41:17 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Wed, 25 Jan 2023 21:41:17 GMT
USER root
# Wed, 25 Jan 2023 21:42:45 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork
# Wed, 25 Jan 2023 21:42:45 GMT
USER jetty
# Wed, 25 Jan 2023 21:42:45 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 21:42:45 GMT
ENV GN_VERSION=4.2.2
# Wed, 25 Jan 2023 21:42:45 GMT
ENV GN_DOWNLOAD_MD5=ec7f0c956fe07737fb6fa77fa4e9aaf5
# Wed, 25 Jan 2023 21:43:12 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war
# Wed, 25 Jan 2023 21:43:13 GMT
COPY file:ca46ab251df3dfc253cb04cf962e7266e42428fab31ad2f583a7c86b06d5f778 in /geonetwork-entrypoint.sh 
# Wed, 25 Jan 2023 21:43:14 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Wed, 25 Jan 2023 21:43:14 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Wed, 25 Jan 2023 21:43:14 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9923132fe6ab2c95fb9e2363f361139b8e50b7264d78acb7cf60147742acc985`  
		Last Modified: Fri, 09 Dec 2022 01:49:42 GMT  
		Size: 16.3 MB (16333067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37fb312ae19f62ad480ce6086c9b6578ca2410115a9273a116277a4baa172c3`  
		Last Modified: Wed, 25 Jan 2023 19:26:09 GMT  
		Size: 54.6 MB (54635847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2e2b34b018853989bb73ef5b890ce38ef7577705dae25d3af5b7167b1a630a`  
		Last Modified: Wed, 25 Jan 2023 19:26:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4f5af6f8772e4f84d1046d9b88b101b6cf877e58620bf8c096e58ba886bde0`  
		Last Modified: Wed, 25 Jan 2023 21:26:22 GMT  
		Size: 10.7 MB (10665854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02cc6c770c632ee829d89db00897318fe31c77d559b2df6754e8f4b2af71626`  
		Last Modified: Wed, 25 Jan 2023 21:26:21 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e799414ffae132617f7f90910d8c2bc59b4679328672d282158ef955c4b508`  
		Last Modified: Wed, 25 Jan 2023 21:44:46 GMT  
		Size: 482.1 KB (482054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2ede78d46ba6ba05067e43b6de8325d02ec48fb4da00c3d62f6f2384c65264`  
		Last Modified: Wed, 25 Jan 2023 21:45:04 GMT  
		Size: 324.0 MB (324045776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4fb39f80727c7e8e1119f3d4f0b838ac55bd08b31ca6694252e9856e58d453`  
		Last Modified: Wed, 25 Jan 2023 21:44:46 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:4.2` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:3907b96941683c086430f281267acd416e6f1073e8ad62c16dbbac33ced70d3a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.3 MB (432317385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5a7fe7d677c81221f79848e2e55e87b2f013656111d69836d031cb24fbef45`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:50 GMT
ADD file:8cba976cb6ea226de769a768ee274e7679d34f923c93392f340680dc6696232e in / 
# Fri, 09 Dec 2022 01:46:50 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:38:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 03:38:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 03:38:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 03:39:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 18:39:33 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 18:39:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 18:39:42 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 20:36:07 GMT
ENV JETTY_VERSION=9.4.50.v20221201
# Wed, 25 Jan 2023 20:36:07 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 25 Jan 2023 20:36:08 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 25 Jan 2023 20:36:08 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 25 Jan 2023 20:36:08 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 20:36:08 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.50.v20221201/jetty-home-9.4.50.v20221201.tar.gz
# Wed, 25 Jan 2023 20:36:08 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Wed, 25 Jan 2023 20:36:27 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 25 Jan 2023 20:36:27 GMT
WORKDIR /var/lib/jetty
# Wed, 25 Jan 2023 20:36:27 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Wed, 25 Jan 2023 20:36:27 GMT
USER jetty
# Wed, 25 Jan 2023 20:36:27 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 20:36:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2023 20:36:27 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Wed, 25 Jan 2023 21:26:31 GMT
ENV DATA_DIR=/catalogue-data
# Wed, 25 Jan 2023 21:26:32 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Wed, 25 Jan 2023 21:26:32 GMT
USER root
# Wed, 25 Jan 2023 21:28:12 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork
# Wed, 25 Jan 2023 21:28:13 GMT
USER jetty
# Wed, 25 Jan 2023 21:28:13 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 21:28:13 GMT
ENV GN_VERSION=4.2.2
# Wed, 25 Jan 2023 21:28:13 GMT
ENV GN_DOWNLOAD_MD5=ec7f0c956fe07737fb6fa77fa4e9aaf5
# Wed, 25 Jan 2023 21:29:24 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war
# Wed, 25 Jan 2023 21:29:27 GMT
COPY file:ca46ab251df3dfc253cb04cf962e7266e42428fab31ad2f583a7c86b06d5f778 in /geonetwork-entrypoint.sh 
# Wed, 25 Jan 2023 21:29:27 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Wed, 25 Jan 2023 21:29:27 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Wed, 25 Jan 2023 21:29:27 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:f04b4bbe15805316c8fda79beedd3b77e6b1ffcd0acf81226c3089e63f6bffeb`  
		Last Modified: Thu, 08 Dec 2022 15:28:02 GMT  
		Size: 27.2 MB (27193168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d371657879ab4e130d4ef0cad592b6a80196fce854ad341ab9641b484d81b17`  
		Last Modified: Fri, 09 Dec 2022 03:45:13 GMT  
		Size: 16.2 MB (16202837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5249d3752cf871523259f9129f95921a4934b297e86babf342e1b7a305e75d`  
		Last Modified: Wed, 25 Jan 2023 18:44:28 GMT  
		Size: 53.7 MB (53731796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25339c95d0de7be743d79b03d3efb98a5cc0a8ef92150eba90f8c4cd4db30f39`  
		Last Modified: Wed, 25 Jan 2023 18:44:23 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3ee72afb526f5b06a1f25daedfd8c8616770d7ec47d04c7ab794a0b26d0fed`  
		Last Modified: Wed, 25 Jan 2023 20:39:16 GMT  
		Size: 10.7 MB (10661701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3359c6619dec9895f9dc70688c1ea119a2d671bfb0135abd1326fbe9c4b8e246`  
		Last Modified: Wed, 25 Jan 2023 20:39:15 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d30a776447885a53325f771c4fc56dce849696b870e97ac524e8177167455ff`  
		Last Modified: Wed, 25 Jan 2023 21:30:53 GMT  
		Size: 479.7 KB (479674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb6b9a1c82e79ade1c93bd7d174e8746dfe6e1ebc5d12c85221b1ddcd0a61f9`  
		Last Modified: Wed, 25 Jan 2023 21:31:08 GMT  
		Size: 324.0 MB (324045647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4b9b728ddedf50e1682b4382d35d3816cab12f61427f97b8894cc2e866d0d8`  
		Last Modified: Wed, 25 Jan 2023 21:30:53 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:4.2.2`

```console
$ docker pull geonetwork@sha256:d10e0c50f0e9358f3de346f5faa46209c3e9ade855eaf3d62ceddeac7b3f3b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `geonetwork:4.2.2` - linux; amd64

```console
$ docker pull geonetwork@sha256:8521398b72c9c20050ef5ce54de53063758dce617c39f537dc3eeda70245e013
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.7 MB (434742040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9761f1ae7db4d5a268325e14c55196e4243b163c7096e1a7cd99715e43aa8e`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:42:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 01:42:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 01:42:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 01:42:42 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 19:19:58 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 19:20:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 19:20:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 21:21:14 GMT
ENV JETTY_VERSION=9.4.50.v20221201
# Wed, 25 Jan 2023 21:21:14 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 25 Jan 2023 21:21:14 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 25 Jan 2023 21:21:14 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 25 Jan 2023 21:21:14 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 21:21:15 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.50.v20221201/jetty-home-9.4.50.v20221201.tar.gz
# Wed, 25 Jan 2023 21:21:15 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Wed, 25 Jan 2023 21:21:36 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 25 Jan 2023 21:21:36 GMT
WORKDIR /var/lib/jetty
# Wed, 25 Jan 2023 21:21:36 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Wed, 25 Jan 2023 21:21:36 GMT
USER jetty
# Wed, 25 Jan 2023 21:21:36 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 21:21:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2023 21:21:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Wed, 25 Jan 2023 21:41:17 GMT
ENV DATA_DIR=/catalogue-data
# Wed, 25 Jan 2023 21:41:17 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Wed, 25 Jan 2023 21:41:17 GMT
USER root
# Wed, 25 Jan 2023 21:42:45 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork
# Wed, 25 Jan 2023 21:42:45 GMT
USER jetty
# Wed, 25 Jan 2023 21:42:45 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 21:42:45 GMT
ENV GN_VERSION=4.2.2
# Wed, 25 Jan 2023 21:42:45 GMT
ENV GN_DOWNLOAD_MD5=ec7f0c956fe07737fb6fa77fa4e9aaf5
# Wed, 25 Jan 2023 21:43:12 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war
# Wed, 25 Jan 2023 21:43:13 GMT
COPY file:ca46ab251df3dfc253cb04cf962e7266e42428fab31ad2f583a7c86b06d5f778 in /geonetwork-entrypoint.sh 
# Wed, 25 Jan 2023 21:43:14 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Wed, 25 Jan 2023 21:43:14 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Wed, 25 Jan 2023 21:43:14 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9923132fe6ab2c95fb9e2363f361139b8e50b7264d78acb7cf60147742acc985`  
		Last Modified: Fri, 09 Dec 2022 01:49:42 GMT  
		Size: 16.3 MB (16333067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37fb312ae19f62ad480ce6086c9b6578ca2410115a9273a116277a4baa172c3`  
		Last Modified: Wed, 25 Jan 2023 19:26:09 GMT  
		Size: 54.6 MB (54635847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2e2b34b018853989bb73ef5b890ce38ef7577705dae25d3af5b7167b1a630a`  
		Last Modified: Wed, 25 Jan 2023 19:26:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4f5af6f8772e4f84d1046d9b88b101b6cf877e58620bf8c096e58ba886bde0`  
		Last Modified: Wed, 25 Jan 2023 21:26:22 GMT  
		Size: 10.7 MB (10665854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02cc6c770c632ee829d89db00897318fe31c77d559b2df6754e8f4b2af71626`  
		Last Modified: Wed, 25 Jan 2023 21:26:21 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e799414ffae132617f7f90910d8c2bc59b4679328672d282158ef955c4b508`  
		Last Modified: Wed, 25 Jan 2023 21:44:46 GMT  
		Size: 482.1 KB (482054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2ede78d46ba6ba05067e43b6de8325d02ec48fb4da00c3d62f6f2384c65264`  
		Last Modified: Wed, 25 Jan 2023 21:45:04 GMT  
		Size: 324.0 MB (324045776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4fb39f80727c7e8e1119f3d4f0b838ac55bd08b31ca6694252e9856e58d453`  
		Last Modified: Wed, 25 Jan 2023 21:44:46 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:4.2.2` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:3907b96941683c086430f281267acd416e6f1073e8ad62c16dbbac33ced70d3a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.3 MB (432317385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5a7fe7d677c81221f79848e2e55e87b2f013656111d69836d031cb24fbef45`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:50 GMT
ADD file:8cba976cb6ea226de769a768ee274e7679d34f923c93392f340680dc6696232e in / 
# Fri, 09 Dec 2022 01:46:50 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:38:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 03:38:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 03:38:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 03:39:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 18:39:33 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 18:39:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 18:39:42 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 20:36:07 GMT
ENV JETTY_VERSION=9.4.50.v20221201
# Wed, 25 Jan 2023 20:36:07 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 25 Jan 2023 20:36:08 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 25 Jan 2023 20:36:08 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 25 Jan 2023 20:36:08 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 20:36:08 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.50.v20221201/jetty-home-9.4.50.v20221201.tar.gz
# Wed, 25 Jan 2023 20:36:08 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Wed, 25 Jan 2023 20:36:27 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 25 Jan 2023 20:36:27 GMT
WORKDIR /var/lib/jetty
# Wed, 25 Jan 2023 20:36:27 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Wed, 25 Jan 2023 20:36:27 GMT
USER jetty
# Wed, 25 Jan 2023 20:36:27 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 20:36:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2023 20:36:27 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Wed, 25 Jan 2023 21:26:31 GMT
ENV DATA_DIR=/catalogue-data
# Wed, 25 Jan 2023 21:26:32 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Wed, 25 Jan 2023 21:26:32 GMT
USER root
# Wed, 25 Jan 2023 21:28:12 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork
# Wed, 25 Jan 2023 21:28:13 GMT
USER jetty
# Wed, 25 Jan 2023 21:28:13 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 21:28:13 GMT
ENV GN_VERSION=4.2.2
# Wed, 25 Jan 2023 21:28:13 GMT
ENV GN_DOWNLOAD_MD5=ec7f0c956fe07737fb6fa77fa4e9aaf5
# Wed, 25 Jan 2023 21:29:24 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war
# Wed, 25 Jan 2023 21:29:27 GMT
COPY file:ca46ab251df3dfc253cb04cf962e7266e42428fab31ad2f583a7c86b06d5f778 in /geonetwork-entrypoint.sh 
# Wed, 25 Jan 2023 21:29:27 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Wed, 25 Jan 2023 21:29:27 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Wed, 25 Jan 2023 21:29:27 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:f04b4bbe15805316c8fda79beedd3b77e6b1ffcd0acf81226c3089e63f6bffeb`  
		Last Modified: Thu, 08 Dec 2022 15:28:02 GMT  
		Size: 27.2 MB (27193168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d371657879ab4e130d4ef0cad592b6a80196fce854ad341ab9641b484d81b17`  
		Last Modified: Fri, 09 Dec 2022 03:45:13 GMT  
		Size: 16.2 MB (16202837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5249d3752cf871523259f9129f95921a4934b297e86babf342e1b7a305e75d`  
		Last Modified: Wed, 25 Jan 2023 18:44:28 GMT  
		Size: 53.7 MB (53731796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25339c95d0de7be743d79b03d3efb98a5cc0a8ef92150eba90f8c4cd4db30f39`  
		Last Modified: Wed, 25 Jan 2023 18:44:23 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3ee72afb526f5b06a1f25daedfd8c8616770d7ec47d04c7ab794a0b26d0fed`  
		Last Modified: Wed, 25 Jan 2023 20:39:16 GMT  
		Size: 10.7 MB (10661701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3359c6619dec9895f9dc70688c1ea119a2d671bfb0135abd1326fbe9c4b8e246`  
		Last Modified: Wed, 25 Jan 2023 20:39:15 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d30a776447885a53325f771c4fc56dce849696b870e97ac524e8177167455ff`  
		Last Modified: Wed, 25 Jan 2023 21:30:53 GMT  
		Size: 479.7 KB (479674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb6b9a1c82e79ade1c93bd7d174e8746dfe6e1ebc5d12c85221b1ddcd0a61f9`  
		Last Modified: Wed, 25 Jan 2023 21:31:08 GMT  
		Size: 324.0 MB (324045647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4b9b728ddedf50e1682b4382d35d3816cab12f61427f97b8894cc2e866d0d8`  
		Last Modified: Wed, 25 Jan 2023 21:30:53 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `geonetwork:latest`

```console
$ docker pull geonetwork@sha256:d10e0c50f0e9358f3de346f5faa46209c3e9ade855eaf3d62ceddeac7b3f3b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `geonetwork:latest` - linux; amd64

```console
$ docker pull geonetwork@sha256:8521398b72c9c20050ef5ce54de53063758dce617c39f537dc3eeda70245e013
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.7 MB (434742040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9761f1ae7db4d5a268325e14c55196e4243b163c7096e1a7cd99715e43aa8e`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:42:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 01:42:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 01:42:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 01:42:42 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 19:19:58 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 19:20:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 19:20:05 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 21:21:14 GMT
ENV JETTY_VERSION=9.4.50.v20221201
# Wed, 25 Jan 2023 21:21:14 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 25 Jan 2023 21:21:14 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 25 Jan 2023 21:21:14 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 25 Jan 2023 21:21:14 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 21:21:15 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.50.v20221201/jetty-home-9.4.50.v20221201.tar.gz
# Wed, 25 Jan 2023 21:21:15 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Wed, 25 Jan 2023 21:21:36 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 25 Jan 2023 21:21:36 GMT
WORKDIR /var/lib/jetty
# Wed, 25 Jan 2023 21:21:36 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Wed, 25 Jan 2023 21:21:36 GMT
USER jetty
# Wed, 25 Jan 2023 21:21:36 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 21:21:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2023 21:21:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Wed, 25 Jan 2023 21:41:17 GMT
ENV DATA_DIR=/catalogue-data
# Wed, 25 Jan 2023 21:41:17 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Wed, 25 Jan 2023 21:41:17 GMT
USER root
# Wed, 25 Jan 2023 21:42:45 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork
# Wed, 25 Jan 2023 21:42:45 GMT
USER jetty
# Wed, 25 Jan 2023 21:42:45 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 21:42:45 GMT
ENV GN_VERSION=4.2.2
# Wed, 25 Jan 2023 21:42:45 GMT
ENV GN_DOWNLOAD_MD5=ec7f0c956fe07737fb6fa77fa4e9aaf5
# Wed, 25 Jan 2023 21:43:12 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war
# Wed, 25 Jan 2023 21:43:13 GMT
COPY file:ca46ab251df3dfc253cb04cf962e7266e42428fab31ad2f583a7c86b06d5f778 in /geonetwork-entrypoint.sh 
# Wed, 25 Jan 2023 21:43:14 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Wed, 25 Jan 2023 21:43:14 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Wed, 25 Jan 2023 21:43:14 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9923132fe6ab2c95fb9e2363f361139b8e50b7264d78acb7cf60147742acc985`  
		Last Modified: Fri, 09 Dec 2022 01:49:42 GMT  
		Size: 16.3 MB (16333067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37fb312ae19f62ad480ce6086c9b6578ca2410115a9273a116277a4baa172c3`  
		Last Modified: Wed, 25 Jan 2023 19:26:09 GMT  
		Size: 54.6 MB (54635847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2e2b34b018853989bb73ef5b890ce38ef7577705dae25d3af5b7167b1a630a`  
		Last Modified: Wed, 25 Jan 2023 19:26:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4f5af6f8772e4f84d1046d9b88b101b6cf877e58620bf8c096e58ba886bde0`  
		Last Modified: Wed, 25 Jan 2023 21:26:22 GMT  
		Size: 10.7 MB (10665854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02cc6c770c632ee829d89db00897318fe31c77d559b2df6754e8f4b2af71626`  
		Last Modified: Wed, 25 Jan 2023 21:26:21 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e799414ffae132617f7f90910d8c2bc59b4679328672d282158ef955c4b508`  
		Last Modified: Wed, 25 Jan 2023 21:44:46 GMT  
		Size: 482.1 KB (482054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2ede78d46ba6ba05067e43b6de8325d02ec48fb4da00c3d62f6f2384c65264`  
		Last Modified: Wed, 25 Jan 2023 21:45:04 GMT  
		Size: 324.0 MB (324045776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4fb39f80727c7e8e1119f3d4f0b838ac55bd08b31ca6694252e9856e58d453`  
		Last Modified: Wed, 25 Jan 2023 21:44:46 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `geonetwork:latest` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:3907b96941683c086430f281267acd416e6f1073e8ad62c16dbbac33ced70d3a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.3 MB (432317385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5a7fe7d677c81221f79848e2e55e87b2f013656111d69836d031cb24fbef45`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:50 GMT
ADD file:8cba976cb6ea226de769a768ee274e7679d34f923c93392f340680dc6696232e in / 
# Fri, 09 Dec 2022 01:46:50 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:38:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 03:38:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 03:38:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 03:39:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Jan 2023 18:39:33 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 18:39:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        armhf|arm)          ESUM='039843c200d0773fe927fa07c368f23d1d74ae58edd09138c97aa1f5e2007b28';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u362b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 25 Jan 2023 18:39:42 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 25 Jan 2023 20:36:07 GMT
ENV JETTY_VERSION=9.4.50.v20221201
# Wed, 25 Jan 2023 20:36:07 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 25 Jan 2023 20:36:08 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 25 Jan 2023 20:36:08 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 25 Jan 2023 20:36:08 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Jan 2023 20:36:08 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.50.v20221201/jetty-home-9.4.50.v20221201.tar.gz
# Wed, 25 Jan 2023 20:36:08 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Wed, 25 Jan 2023 20:36:27 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Wed, 25 Jan 2023 20:36:27 GMT
WORKDIR /var/lib/jetty
# Wed, 25 Jan 2023 20:36:27 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Wed, 25 Jan 2023 20:36:27 GMT
USER jetty
# Wed, 25 Jan 2023 20:36:27 GMT
EXPOSE 8080
# Wed, 25 Jan 2023 20:36:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Jan 2023 20:36:27 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Wed, 25 Jan 2023 21:26:31 GMT
ENV DATA_DIR=/catalogue-data
# Wed, 25 Jan 2023 21:26:32 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Wed, 25 Jan 2023 21:26:32 GMT
USER root
# Wed, 25 Jan 2023 21:28:12 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork
# Wed, 25 Jan 2023 21:28:13 GMT
USER jetty
# Wed, 25 Jan 2023 21:28:13 GMT
ENV GN_FILE=geonetwork.war
# Wed, 25 Jan 2023 21:28:13 GMT
ENV GN_VERSION=4.2.2
# Wed, 25 Jan 2023 21:28:13 GMT
ENV GN_DOWNLOAD_MD5=ec7f0c956fe07737fb6fa77fa4e9aaf5
# Wed, 25 Jan 2023 21:29:24 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war
# Wed, 25 Jan 2023 21:29:27 GMT
COPY file:ca46ab251df3dfc253cb04cf962e7266e42428fab31ad2f583a7c86b06d5f778 in /geonetwork-entrypoint.sh 
# Wed, 25 Jan 2023 21:29:27 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Wed, 25 Jan 2023 21:29:27 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Wed, 25 Jan 2023 21:29:27 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:f04b4bbe15805316c8fda79beedd3b77e6b1ffcd0acf81226c3089e63f6bffeb`  
		Last Modified: Thu, 08 Dec 2022 15:28:02 GMT  
		Size: 27.2 MB (27193168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d371657879ab4e130d4ef0cad592b6a80196fce854ad341ab9641b484d81b17`  
		Last Modified: Fri, 09 Dec 2022 03:45:13 GMT  
		Size: 16.2 MB (16202837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5249d3752cf871523259f9129f95921a4934b297e86babf342e1b7a305e75d`  
		Last Modified: Wed, 25 Jan 2023 18:44:28 GMT  
		Size: 53.7 MB (53731796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25339c95d0de7be743d79b03d3efb98a5cc0a8ef92150eba90f8c4cd4db30f39`  
		Last Modified: Wed, 25 Jan 2023 18:44:23 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3ee72afb526f5b06a1f25daedfd8c8616770d7ec47d04c7ab794a0b26d0fed`  
		Last Modified: Wed, 25 Jan 2023 20:39:16 GMT  
		Size: 10.7 MB (10661701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3359c6619dec9895f9dc70688c1ea119a2d671bfb0135abd1326fbe9c4b8e246`  
		Last Modified: Wed, 25 Jan 2023 20:39:15 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d30a776447885a53325f771c4fc56dce849696b870e97ac524e8177167455ff`  
		Last Modified: Wed, 25 Jan 2023 21:30:53 GMT  
		Size: 479.7 KB (479674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb6b9a1c82e79ade1c93bd7d174e8746dfe6e1ebc5d12c85221b1ddcd0a61f9`  
		Last Modified: Wed, 25 Jan 2023 21:31:08 GMT  
		Size: 324.0 MB (324045647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4b9b728ddedf50e1682b4382d35d3816cab12f61427f97b8894cc2e866d0d8`  
		Last Modified: Wed, 25 Jan 2023 21:30:53 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
