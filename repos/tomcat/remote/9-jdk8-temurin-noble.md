## `tomcat:9-jdk8-temurin-noble`

```console
$ docker pull tomcat@sha256:ea41b26475d2050ca17d8f3edafcb1061d7ffe216f471b0267bdf45b467288e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `tomcat:9-jdk8-temurin-noble` - linux; amd64

```console
$ docker pull tomcat@sha256:5788cd56afc7442718378b5329be694eb6711d2dcfb84f106ff9889c54303790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163428108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ad3920bfb94e4f48fc89e599e888ddf37820dd88912c26a0fc7e5cdcee7c8f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:01 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:03 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 27 Aug 2024 15:55:03 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 08:03:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 11 Sep 2024 08:03:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Sep 2024 08:03:44 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 11 Sep 2024 08:03:44 GMT
WORKDIR /usr/local/tomcat
# Wed, 11 Sep 2024 08:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 08:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 08:03:44 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 11 Sep 2024 08:03:44 GMT
ENV TOMCAT_MAJOR=9
# Wed, 11 Sep 2024 08:03:44 GMT
ENV TOMCAT_VERSION=9.0.94
# Wed, 11 Sep 2024 08:03:44 GMT
ENV TOMCAT_SHA512=14d941808565bac5913b94d3ad24e1d783ab1dfb29b7aee32b9ce1b5c7629a3a836b944b8ee7990d1719e75cf8cc928efdf682cdd4b908eaa77c69cd37e9f436
# Wed, 11 Sep 2024 08:03:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Wed, 11 Sep 2024 08:03:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 11 Sep 2024 08:03:44 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 11 Sep 2024 08:03:44 GMT
ENTRYPOINT []
# Wed, 11 Sep 2024 08:03:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:32b824d45c6101d459f5d3c13ab8658b6f79713f3bd64e363d3f6bc98faf5d6d`  
		Last Modified: Tue, 27 Aug 2024 21:43:22 GMT  
		Size: 30.6 MB (30611547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a316f85472e42ddf39be81d37cefcaa87cad98b7ca1710864ef2b8e67e9713b`  
		Last Modified: Tue, 17 Sep 2024 01:07:39 GMT  
		Size: 16.2 MB (16177262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b552d185db1a78621cdce456d67c12f7cf4df298dc7f3a2e5505e5512a3a1f2`  
		Last Modified: Tue, 17 Sep 2024 01:07:45 GMT  
		Size: 103.6 MB (103615817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63669e1016d40404c9b50ea64ae1f03422008e4b0d40cc6fb26e032ed6d602a`  
		Last Modified: Tue, 17 Sep 2024 01:07:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd5773d9860c440228f3086964dd0164ef7786dfbae56d76b149d971b886ad3`  
		Last Modified: Tue, 17 Sep 2024 01:07:36 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a865ff737c3af42fd3d583005462de00c15bb2093aa46054eb3bc9cb1f9d7cd`  
		Last Modified: Tue, 17 Sep 2024 01:58:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b25f6b8b596441bfb25a040ff4b225d52e346441f9a5b6463add9ab28947c65`  
		Last Modified: Tue, 17 Sep 2024 01:58:56 GMT  
		Size: 13.0 MB (13021021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk8-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:6b8349e1f44e9349f70c5e9d9e2875001f5cc91d6b76c412e972f21e55708e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798d7836f436bf50c7449203422ce3480dd5b558d19c52dc5a4d78ff6328b781`

```dockerfile
```

-	Layers:
	-	`sha256:0405cc9ac07dc68910a96ad900d0d6a2ceaa14736bde44536d1b33adfa1e6f36`  
		Last Modified: Tue, 17 Sep 2024 01:58:55 GMT  
		Size: 3.0 MB (3017031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32b1583ab431d6cbf9c48d7b23b8f8809610055c18fd8f2e20409c7f2ada6776`  
		Last Modified: Tue, 17 Sep 2024 01:58:55 GMT  
		Size: 31.0 KB (30959 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jdk8-temurin-noble` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:1986fb5cb80c1be5882f49533d06383f9316f8ded2975caab1f4d2306a4c9a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154807842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76cc2a27f1363391cd1df870165b0015c0150a0c73efe4595f22938b14d7963e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:10 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:14 GMT
ADD file:0efc83f80e5e3a9125a702063e487f836d2e0ff9a88f4d0330897d15e445d415 in / 
# Tue, 27 Aug 2024 15:55:14 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 08:03:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 11 Sep 2024 08:03:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Sep 2024 08:03:44 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 11 Sep 2024 08:03:44 GMT
WORKDIR /usr/local/tomcat
# Wed, 11 Sep 2024 08:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 08:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 08:03:44 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 11 Sep 2024 08:03:44 GMT
ENV TOMCAT_MAJOR=9
# Wed, 11 Sep 2024 08:03:44 GMT
ENV TOMCAT_VERSION=9.0.94
# Wed, 11 Sep 2024 08:03:44 GMT
ENV TOMCAT_SHA512=14d941808565bac5913b94d3ad24e1d783ab1dfb29b7aee32b9ce1b5c7629a3a836b944b8ee7990d1719e75cf8cc928efdf682cdd4b908eaa77c69cd37e9f436
# Wed, 11 Sep 2024 08:03:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Wed, 11 Sep 2024 08:03:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 11 Sep 2024 08:03:44 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 11 Sep 2024 08:03:44 GMT
ENTRYPOINT []
# Wed, 11 Sep 2024 08:03:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3662f20bd36fe3ab5035e3d6d75d4a5a27e32e29abe306052959223600a1522c`  
		Last Modified: Tue, 17 Sep 2024 01:24:15 GMT  
		Size: 27.7 MB (27731977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4be6c7fa81e4d16783a207dc0e7aee5ebe57ddded3444a61cd47351170b177`  
		Last Modified: Tue, 17 Sep 2024 01:24:14 GMT  
		Size: 14.9 MB (14919849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a89125bb44a745f4da810ce2c67e63292e67d29f05c6305c2f2df8b5f640ba`  
		Last Modified: Tue, 17 Sep 2024 01:24:20 GMT  
		Size: 99.2 MB (99225159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4faf7fc2bec03b302fa84ba686ab9558bc033efd9e544eede5d5886c80d1ea9f`  
		Last Modified: Tue, 17 Sep 2024 01:24:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e17dd78be1badf845d0a0626ca63af5acd8a5b8d92a1ddfb69cf89b0587a6ad`  
		Last Modified: Tue, 17 Sep 2024 01:24:11 GMT  
		Size: 2.1 KB (2131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d41563b4f060cb9c715ff88357fe6db82f8ea0946ed1d29e7b27505c6f98af8`  
		Last Modified: Tue, 17 Sep 2024 02:39:44 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb12f69e1c2592ec8272dfcd69421aeb7218ab5068318f4ee14960324287bd3`  
		Last Modified: Tue, 17 Sep 2024 02:39:44 GMT  
		Size: 12.9 MB (12928397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk8-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:c67785167926ec026c6c33b63376641c254f97ff08384d3572d589db77c8bd9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3050881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98aaa1418e0155663772bfdc34c3cec0d59f79a2b370a43513e6cfcc20116193`

```dockerfile
```

-	Layers:
	-	`sha256:0b44a1e95dabf090e8f0b71fe1c0d77c2b7733afb0f00531acd38beb280feca8`  
		Last Modified: Tue, 17 Sep 2024 02:39:44 GMT  
		Size: 3.0 MB (3019793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89c61c0262d59b78a0c1b02b9a18339cdb33d81b431cadbd48292d54a37ead7c`  
		Last Modified: Tue, 17 Sep 2024 02:39:44 GMT  
		Size: 31.1 KB (31088 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jdk8-temurin-noble` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:aca42ab7e9c0c7c4efa37a19ad21926f41551d2ce3785ad031ca7740900677e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177185528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a2bf19907a5ab4211aae81e115a01cb742f6d30db54a863dcc1f9b680d41cc`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 01 Aug 2024 15:33:35 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:33:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:33:36 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:33:38 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 01 Aug 2024 15:33:38 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 08:03:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 11 Sep 2024 08:03:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Sep 2024 08:03:44 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 11 Sep 2024 08:03:44 GMT
WORKDIR /usr/local/tomcat
# Wed, 11 Sep 2024 08:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 08:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 08:03:44 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 11 Sep 2024 08:03:44 GMT
ENV TOMCAT_MAJOR=9
# Wed, 11 Sep 2024 08:03:44 GMT
ENV TOMCAT_VERSION=9.0.94
# Wed, 11 Sep 2024 08:03:44 GMT
ENV TOMCAT_SHA512=14d941808565bac5913b94d3ad24e1d783ab1dfb29b7aee32b9ce1b5c7629a3a836b944b8ee7990d1719e75cf8cc928efdf682cdd4b908eaa77c69cd37e9f436
# Wed, 11 Sep 2024 08:03:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Wed, 11 Sep 2024 08:03:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 11 Sep 2024 08:03:44 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 11 Sep 2024 08:03:44 GMT
ENTRYPOINT []
# Wed, 11 Sep 2024 08:03:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923b74992e2f6b4e4be4f1c2bf6930b93c7593d6c834159867d3bd8ea14005ff`  
		Last Modified: Sat, 17 Aug 2024 01:33:27 GMT  
		Size: 13.8 MB (13795899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58576ea718a0fe2438afe0bb666a3a35004198540087a002268e2962b41f7923`  
		Last Modified: Sat, 17 Aug 2024 01:33:31 GMT  
		Size: 102.7 MB (102732973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b9a6c4f3c0f832785c77b255658197e74ce313e9fb3ee8cddfc9e630d56f59`  
		Last Modified: Sat, 17 Aug 2024 01:33:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8f01f034694f1dcbd5ebdbcf8074eb868fa7fd9c7c2f9df0ed44eae52141d4`  
		Last Modified: Fri, 23 Aug 2024 19:42:46 GMT  
		Size: 2.1 KB (2131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932ed36a7dfe3e055fd4eeb7ff74ce16b2a88a95849ab7244e0f1fddd01abdbc`  
		Last Modified: Wed, 11 Sep 2024 19:43:01 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61b77330202bb5bdbe3f370aeea8214b52dbd8d96de9872000ac43ce8197498`  
		Last Modified: Wed, 11 Sep 2024 19:43:02 GMT  
		Size: 30.7 MB (30744164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk8-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:49c9f14aea8e2c3d5b58f628cdce1b5b265dadab39434402737f8ed7eb9e4492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3049408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab60f4a085c991e35ffe409ff1a5f7f22c972b64c87009398455790104e0f4d`

```dockerfile
```

-	Layers:
	-	`sha256:9be548e03be83876c9d0b81b6fbbcf0c5c0917e9942279fc293b08a43128f78f`  
		Last Modified: Wed, 11 Sep 2024 19:43:02 GMT  
		Size: 3.0 MB (3018073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e80a0a76202e1c268b0e0ab880d0c10ed5a1b28fbbf580303240e4c26e69a9d`  
		Last Modified: Wed, 11 Sep 2024 19:43:01 GMT  
		Size: 31.3 KB (31335 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jdk8-temurin-noble` - linux; ppc64le

```console
$ docker pull tomcat@sha256:6ba515e469744c376ff4acc7679899cdbde7e0ac11ac8c879bfdce1806279734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.2 MB (167227994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58928f8d505c75bea4795ba1183192b47b75f343c33b22652248e519fd34aba6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 27 Aug 2024 15:56:25 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:56:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:56:28 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Tue, 27 Aug 2024 15:56:29 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 08:03:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 11 Sep 2024 08:03:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Sep 2024 08:03:44 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 11 Sep 2024 08:03:44 GMT
WORKDIR /usr/local/tomcat
# Wed, 11 Sep 2024 08:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 08:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 08:03:44 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 11 Sep 2024 08:03:44 GMT
ENV TOMCAT_MAJOR=9
# Wed, 11 Sep 2024 08:03:44 GMT
ENV TOMCAT_VERSION=9.0.94
# Wed, 11 Sep 2024 08:03:44 GMT
ENV TOMCAT_SHA512=14d941808565bac5913b94d3ad24e1d783ab1dfb29b7aee32b9ce1b5c7629a3a836b944b8ee7990d1719e75cf8cc928efdf682cdd4b908eaa77c69cd37e9f436
# Wed, 11 Sep 2024 08:03:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Wed, 11 Sep 2024 08:03:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 11 Sep 2024 08:03:44 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 11 Sep 2024 08:03:44 GMT
ENTRYPOINT []
# Wed, 11 Sep 2024 08:03:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5d340ed979f83f097fa56590781e2ea4e2d63a50fc75b5e5bc616f845d2e2f80`  
		Last Modified: Tue, 17 Sep 2024 00:53:16 GMT  
		Size: 35.5 MB (35518179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5238c0d3f97d3a0bb99bc13e9f9d3fe8c0a98a4ff7994e3485eb4e699a551d`  
		Last Modified: Tue, 17 Sep 2024 01:06:02 GMT  
		Size: 17.5 MB (17533628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6894b9ad9b74fb85da6901c69a78bc0905b192bf1e7955e620839ccaf7495763`  
		Last Modified: Tue, 17 Sep 2024 01:06:09 GMT  
		Size: 101.1 MB (101079946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027e6ab49931182ea0d639398fea3a278582f835065dd97c3c5e018b7b72d92e`  
		Last Modified: Tue, 17 Sep 2024 01:05:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4135367fa8ff18a6591c04095f26b64cfbbfbf8d348d032dcfc375152f67df44`  
		Last Modified: Tue, 17 Sep 2024 01:05:58 GMT  
		Size: 2.1 KB (2131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33888cc24e6749466b6d42e373eea0ab5fadeda8edcb1ee80250483e56906b9e`  
		Last Modified: Tue, 17 Sep 2024 05:00:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3eff7c37960db8aaa4223fdb0f6502dab835e1c8c7d4b776fad58c0ec783f6`  
		Last Modified: Tue, 17 Sep 2024 05:00:14 GMT  
		Size: 13.1 MB (13093780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk8-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:3c4bf857e47525ff99b9877d48244c3b115cafb375a08805acde10bcbe7bc28d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3051510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6962f60629ae4d865a4ab968f6603f56cb5c28c462abb80b3dda4cd871e0551a`

```dockerfile
```

-	Layers:
	-	`sha256:86d54e9ceb244724700ffb5a45eb560ace98ee37b1a89219fa985b41ca50135b`  
		Last Modified: Tue, 17 Sep 2024 05:00:12 GMT  
		Size: 3.0 MB (3020479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a248699c29b454f9e0e6b3dfa5250895c62933920570808357125e302b468747`  
		Last Modified: Tue, 17 Sep 2024 05:00:12 GMT  
		Size: 31.0 KB (31031 bytes)  
		MIME: application/vnd.in-toto+json
