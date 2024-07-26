## `tomcat:jdk11-temurin-noble`

```console
$ docker pull tomcat@sha256:1aff5f2c5b5843d9b15ee610be940cd72f15e9b4cf3ad86f535c6fd7f0a97a43
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `tomcat:jdk11-temurin-noble` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:6596025bc61b11a9cf672ed92e11087a17024c39a36e57f2cf9b7319ba852b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192000794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2bcedc871963617549b3ab3428ddef01c8b2f44dc7678d816fc9ed14794e485`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 07 Jun 2024 11:56:56 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:56:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:57:05 GMT
ADD file:b748f7f0dae18a5c9b75daf9f538536d4e2ef86d0765531567a4dfe83eb96ff0 in / 
# Fri, 07 Jun 2024 11:57:06 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='9d14a076d1440161ab4c9736644e8e9f4719eb8e9f44c03470640960c3cd5e00';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Wed, 24 Jul 2024 22:19:06 GMT
CMD ["jshell"]
# Thu, 25 Jul 2024 19:41:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 25 Jul 2024 19:41:10 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jul 2024 19:41:10 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 25 Jul 2024 19:41:10 GMT
WORKDIR /usr/local/tomcat
# Thu, 25 Jul 2024 19:41:10 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 25 Jul 2024 19:41:10 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 25 Jul 2024 19:41:10 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 25 Jul 2024 19:41:10 GMT
ENV TOMCAT_MAJOR=10
# Thu, 25 Jul 2024 19:41:10 GMT
ENV TOMCAT_VERSION=10.1.26
# Thu, 25 Jul 2024 19:41:10 GMT
ENV TOMCAT_SHA512=0a62e55c1ff9f8f04d7aff938764eac46c289eda888abf43de74a82ceb7d879e94a36ea3e5e46186bc231f07871fcc4c58f11e026f51d4487a473badb21e9355
# Thu, 25 Jul 2024 19:41:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 25 Jul 2024 19:41:10 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 25 Jul 2024 19:41:10 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 25 Jul 2024 19:41:10 GMT
ENTRYPOINT []
# Thu, 25 Jul 2024 19:41:10 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3f8d8d41dba086e9a9d743fe5b990924057d2470da76cc6ffdc8e6e7bd5aaeee`  
		Last Modified: Sun, 09 Jun 2024 02:03:28 GMT  
		Size: 27.7 MB (27688462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa73b9ee1a38f82f2ba5f1908e75daf507e03ef02b02ce5916a6a2daa1842e`  
		Last Modified: Tue, 23 Jul 2024 03:18:50 GMT  
		Size: 13.1 MB (13133434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba33cee577e6532a80d4223470068063cd1cd0f21a41c43d8cdb86f164eb091`  
		Last Modified: Wed, 24 Jul 2024 01:10:03 GMT  
		Size: 138.0 MB (138037292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7005156b8291b9dc58e594f05e500cd5db2f5d969a9ea6363b8505f2b551a2`  
		Last Modified: Wed, 24 Jul 2024 01:09:46 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0dccf2eee422246c7929716495211af1135f7fa23950f5ec9805531593f129`  
		Last Modified: Thu, 25 Jul 2024 18:02:27 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe2e97e2088905d702ecc8df9ba2af70ba473c73800b6c3f3aba855cb731a2b`  
		Last Modified: Fri, 26 Jul 2024 19:17:32 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cb3ea10baf899c2c1ce05adb4cb8b57c3302bb0ac2be0b97e780aa827818e3`  
		Last Modified: Fri, 26 Jul 2024 19:17:33 GMT  
		Size: 13.1 MB (13139362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jdk11-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:bbf99fe2d40c5ec7847318570a8e33703eb0e393f020380be4fb9aaf06cebce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3023583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69232aaf583fbb258a3c0598630316bd32d759d84ad2373ef6b9d14a3e903fda`

```dockerfile
```

-	Layers:
	-	`sha256:b407b7c95f82e4a085e556d2363cec7e7be5b2fc380812af8a9fca3b3d70cb73`  
		Last Modified: Fri, 26 Jul 2024 19:17:33 GMT  
		Size: 3.0 MB (2991690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f85c5a1e401e396ed8c7316523663617c10214167d9e15e593f15a6cabce0a7`  
		Last Modified: Fri, 26 Jul 2024 19:17:32 GMT  
		Size: 31.9 KB (31893 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jdk11-temurin-noble` - linux; ppc64le

```console
$ docker pull tomcat@sha256:d9ea96c7f232c06e720c2df75f7f59b0b76b7139a4cf0552946a3cf8897160f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196574141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a00b979308636201d37229c8f5f040d49ec67c6170f88cd89417731eb0bc12b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:24 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:28 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Fri, 07 Jun 2024 12:00:29 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='9d14a076d1440161ab4c9736644e8e9f4719eb8e9f44c03470640960c3cd5e00';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Wed, 24 Jul 2024 22:19:06 GMT
CMD ["jshell"]
# Thu, 25 Jul 2024 19:41:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 25 Jul 2024 19:41:10 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jul 2024 19:41:10 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 25 Jul 2024 19:41:10 GMT
WORKDIR /usr/local/tomcat
# Thu, 25 Jul 2024 19:41:10 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 25 Jul 2024 19:41:10 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 25 Jul 2024 19:41:10 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 25 Jul 2024 19:41:10 GMT
ENV TOMCAT_MAJOR=10
# Thu, 25 Jul 2024 19:41:10 GMT
ENV TOMCAT_VERSION=10.1.26
# Thu, 25 Jul 2024 19:41:10 GMT
ENV TOMCAT_SHA512=0a62e55c1ff9f8f04d7aff938764eac46c289eda888abf43de74a82ceb7d879e94a36ea3e5e46186bc231f07871fcc4c58f11e026f51d4487a473badb21e9355
# Thu, 25 Jul 2024 19:41:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 25 Jul 2024 19:41:10 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 25 Jul 2024 19:41:10 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 25 Jul 2024 19:41:10 GMT
ENTRYPOINT []
# Thu, 25 Jul 2024 19:41:10 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a6b87acc0a568209f5593370b5b6bcffdf1ec82a13216fce26023e6eac0aaea8`  
		Last Modified: Sun, 09 Jun 2024 02:03:40 GMT  
		Size: 35.6 MB (35626958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9074cdf27e23156680daa103ed33f6d64f3a455ee0f828ee2acc7e1e3ecbd1`  
		Last Modified: Tue, 23 Jul 2024 01:44:29 GMT  
		Size: 14.9 MB (14944088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5fa3117e161020a26fa5fdaa35c644e5ed2beca97b34667154b280f828208c`  
		Last Modified: Wed, 24 Jul 2024 04:12:30 GMT  
		Size: 132.8 MB (132755912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce2c9eb8fff78851f6c0a26d95074906caaec62678fd7fd5117f972b62910de`  
		Last Modified: Wed, 24 Jul 2024 04:12:18 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b878ec76ba68e0ad0df85321be7d8a663a9b7e9a041f46250aee4632d6c6a0`  
		Last Modified: Thu, 25 Jul 2024 17:24:03 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448422ebf86f948fe8ee2a6905093f6e23c6d9a40275449a5e8612e7b0ab78c5`  
		Last Modified: Fri, 26 Jul 2024 19:21:54 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4bee4b23497ae5fae8c4b69b85226cf725029746980700d607f72542580fca`  
		Last Modified: Fri, 26 Jul 2024 19:21:55 GMT  
		Size: 13.2 MB (13244942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jdk11-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:5c4ebbef656533ef208972900d4e180d8908890e57c584fb51dce02ef110112c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3026787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7947d295d906102dd1fc19b26be568de1d2ff8a1fd9c09dacde5f3cc083514`

```dockerfile
```

-	Layers:
	-	`sha256:bf8a7e08a50aa63bf24c0d4633bce83737d9767893455c504cc1b83442cddc4d`  
		Last Modified: Fri, 26 Jul 2024 19:21:54 GMT  
		Size: 3.0 MB (2994964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de5e65c7bc188c34c1b14bd268ae699f8a20f4d1fa125a715897005611b3e0c1`  
		Last Modified: Fri, 26 Jul 2024 19:21:54 GMT  
		Size: 31.8 KB (31823 bytes)  
		MIME: application/vnd.in-toto+json
