<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `geonetwork`

-	[`geonetwork:3`](#geonetwork3)
-	[`geonetwork:3-postgres`](#geonetwork3-postgres)
-	[`geonetwork:3.12`](#geonetwork312)
-	[`geonetwork:3.12-postgres`](#geonetwork312-postgres)
-	[`geonetwork:3.12.11`](#geonetwork31211)
-	[`geonetwork:3.12.11-postgres`](#geonetwork31211-postgres)
-	[`geonetwork:4`](#geonetwork4)
-	[`geonetwork:4.2`](#geonetwork42)
-	[`geonetwork:4.2.10`](#geonetwork4210)
-	[`geonetwork:4.4`](#geonetwork44)
-	[`geonetwork:4.4.5`](#geonetwork445)
-	[`geonetwork:latest`](#geonetworklatest)

## `geonetwork:3`

```console
$ docker pull geonetwork@sha256:bf3eee42b5b90245b7a48efb3373f591e901b8b39e349bc380ed45b7527b7713
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

### `geonetwork:3` - linux; amd64

```console
$ docker pull geonetwork@sha256:96e0421942ad0299075f09604e345f43a70082bc07af0dc2ce1d9e69dd82a511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.1 MB (394143302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ad5370e0b6b524f2ecf18a502edc6cab4ab69d30e9884da5f8e75c2fe07e71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 02 Apr 2024 10:10:05 GMT
ARG RELEASE
# Tue, 02 Apr 2024 10:10:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 02 Apr 2024 10:10:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 02 Apr 2024 10:10:05 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 02 Apr 2024 10:10:05 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["/bin/bash"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Apr 2024 10:10:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Apr 2024 10:10:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Apr 2024 10:10:05 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Apr 2024 10:10:05 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_VERSION=9.0.91
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT []
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Apr 2024 10:10:05 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_VERSION=3.12.11
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_DOWNLOAD_MD5=2ece7076f05068e7a5270af03e32d632
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Apr 2024 10:10:05 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4040a9fc8f154e4bdc7b1fada39d21321aa2fa67f5ec71b3c6ced523d6bca756`  
		Last Modified: Thu, 25 Jul 2024 17:26:10 GMT  
		Size: 103.6 MB (103615844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a876aecb20e71daf56b1b8ebbe1e3e11f26f6d9ca83e6933e9fb7b9c5a9db53e`  
		Last Modified: Thu, 25 Jul 2024 17:26:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaf0a30f7dfdef304092a7f19ad21c11e30bcf6bf04e60ff7b75b504d6cf8f4`  
		Last Modified: Thu, 25 Jul 2024 17:26:03 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba983e46ea55676251c498d1239a189987f977bb6e5fa073187abceb7e5f0cf`  
		Last Modified: Thu, 25 Jul 2024 19:07:43 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9515ec726a6d5e4c67aba5376b55ec8e44ded359a6c8fde8f8003be7dfd3dc5`  
		Last Modified: Thu, 25 Jul 2024 19:07:43 GMT  
		Size: 12.7 MB (12673367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6440b786c3d6737a9a28f7ee4373f024da452d2f8a4874164a21e56809970e0b`  
		Last Modified: Thu, 25 Jul 2024 20:10:51 GMT  
		Size: 234.5 MB (234540645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468205bc3496401939f90c6c7ba7b461679e0af5913b75d0746b3d6c754ad73a`  
		Last Modified: Thu, 25 Jul 2024 20:10:45 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:c14c673fb0a7d2e25a01e9f82dd3d234a6fa8a08c990472800ef1594fad6367f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ee72391e418cecf7f0dd3f5ba9dd69d51923f62dbecba9c44c340782e6dc4f`

```dockerfile
```

-	Layers:
	-	`sha256:d4d0a589fe0622103f9d9df49f9a493915ffa75372575ceb89ef11d837d99cf7`  
		Last Modified: Thu, 25 Jul 2024 20:10:46 GMT  
		Size: 4.3 MB (4305065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:948dda15e627d436862259ec981af9d32b043abe317f0c2958bb8d819eecea80`  
		Last Modified: Thu, 25 Jul 2024 20:10:45 GMT  
		Size: 19.2 KB (19240 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:dfa33b4015a4e19a8152b39461582b97f36c7ceb73fa73e952699f27aabea53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.4 MB (386357758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583282d5e8bed9e923c9a5af98d7536fccd8dfb18bbb2b797d62d32119e1814f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 02 Apr 2024 10:10:05 GMT
ARG RELEASE
# Tue, 02 Apr 2024 10:10:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 02 Apr 2024 10:10:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 02 Apr 2024 10:10:05 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 02 Apr 2024 10:10:05 GMT
ADD file:967120bb21c0fbaf9bf6c8fcb7b292d31ec4812e538714e8beb0a6e013eae873 in / 
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["/bin/bash"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Apr 2024 10:10:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Apr 2024 10:10:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Apr 2024 10:10:05 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Apr 2024 10:10:05 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_VERSION=9.0.91
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT []
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Apr 2024 10:10:05 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_VERSION=3.12.11
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_DOWNLOAD_MD5=2ece7076f05068e7a5270af03e32d632
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Apr 2024 10:10:05 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e180e7b68e21ed1490bb8293a3e848136812456d07f1be0783ef04f773a97867`  
		Last Modified: Fri, 28 Jun 2024 02:10:28 GMT  
		Size: 27.5 MB (27534011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3600b7820ccdab844af0b11c36a1aeadc460c5a3bc6a6fd0211a3fa9024fb1`  
		Last Modified: Tue, 02 Jul 2024 04:32:24 GMT  
		Size: 12.5 MB (12462968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2795f90fa7d600dee1f4eb73c08bb2d18123b06d13636002d46176c4b2f023f3`  
		Last Modified: Thu, 25 Jul 2024 18:01:01 GMT  
		Size: 99.2 MB (99249372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2c3b2a91fa20610bf53f9d0a722666976bbced1fddeabec3b2f1cafa30130f`  
		Last Modified: Thu, 25 Jul 2024 18:00:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4602dfe42d8b2b444328e0fb2b51ef2d074bcde8a413952b8269fe2bb2b489f6`  
		Last Modified: Thu, 25 Jul 2024 18:00:53 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc7d8efb5ef48317356561b1ec3b9b83a9949fd96d2effd6000c2a408fa0791`  
		Last Modified: Thu, 25 Jul 2024 19:39:25 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602497ca0baec3960eb142ca73787cbde70559ff89237b96f82118f2fb75a5c4`  
		Last Modified: Thu, 25 Jul 2024 19:39:26 GMT  
		Size: 12.6 MB (12580273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac5139b450dfef48663dd8c23544da8a664b35efe72d137db81ea058d954d98`  
		Last Modified: Thu, 25 Jul 2024 20:42:10 GMT  
		Size: 234.5 MB (234528624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bb4da193e005f20ee0f81ad66238a473fcfaa348f687c5513fb5743724f87c`  
		Last Modified: Thu, 25 Jul 2024 20:42:04 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:c1cafc419cefeb5e1963760100487607e34fdad3e2e76a1787b4ce4648250e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c07416149f052dac48b0c727d61ea78a21fafabc7bc53a3dc9f91e37fcc76e`

```dockerfile
```

-	Layers:
	-	`sha256:a73477235ccc024e29f5f46d1bf3d3275d01cb274168c89bff2a9efa5d9bf01c`  
		Last Modified: Thu, 25 Jul 2024 20:42:05 GMT  
		Size: 4.3 MB (4307783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63da1de726f860c2899727edc74c941c471fd1993452e6840962e7950f4e83fc`  
		Last Modified: Thu, 25 Jul 2024 20:42:04 GMT  
		Size: 19.5 KB (19453 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:13b65e11fead24599650ecf307cbcff09d7f5644911dc258886ff42711992cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.1 MB (391136969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14487c71572df86e40e6f00f0139cc42de2b5e90d547dfc3474924b10918680`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 02 Apr 2024 10:10:05 GMT
ARG RELEASE
# Tue, 02 Apr 2024 10:10:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 02 Apr 2024 10:10:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 02 Apr 2024 10:10:05 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 02 Apr 2024 10:10:05 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["/bin/bash"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Apr 2024 10:10:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Apr 2024 10:10:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Apr 2024 10:10:05 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Apr 2024 10:10:05 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_VERSION=9.0.91
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT []
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Apr 2024 10:10:05 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_VERSION=3.12.11
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_DOWNLOAD_MD5=2ece7076f05068e7a5270af03e32d632
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Apr 2024 10:10:05 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bdbc9eb1fb5990eb08fa9fe21450674d749b586acb5e75044993eaa173745d`  
		Last Modified: Tue, 02 Jul 2024 04:34:28 GMT  
		Size: 102.7 MB (102704169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2f56b637ad3ed974bf5d3f1b3963f194651c946391e4c9d1460693f56c8ea4`  
		Last Modified: Tue, 02 Jul 2024 04:34:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32dd5676062f79e6e7a076fdfd9b5dcd7f10701b1e7eb2cf21d1fece49f72190`  
		Last Modified: Tue, 02 Jul 2024 04:34:21 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af06264ab206fceff972cc63c64fadfac0dcc401e8dde9e30ede88067f01654`  
		Last Modified: Wed, 03 Jul 2024 01:00:18 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba539a524bb8cfa8b0c80f9c30f43f28d1dce4ea437dfc7fa7532ccd126336d`  
		Last Modified: Mon, 08 Jul 2024 23:14:30 GMT  
		Size: 12.7 MB (12679916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f62e239ce4eb896f669e74bc6c0dabb558fa52d23f61ff7c5d73b44e08a98a`  
		Last Modified: Tue, 09 Jul 2024 00:09:52 GMT  
		Size: 234.5 MB (234537412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42182b40f87b380bd51d17a491f660c27485c9d8375172d300419dfe824113dc`  
		Last Modified: Tue, 09 Jul 2024 00:09:47 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:77f0dee9efb464431027b94996ded1871353e61220cace8178c483a509b9b3a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4203325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4745721776422c6895ea7ed3ad26de2c0458a1bf53621b5209a87784e3099420`

```dockerfile
```

-	Layers:
	-	`sha256:49f0ee1781aa1d9573c08d54d4f6a0bf26fe793a4fd1c81e5b6091c60d6f0a80`  
		Last Modified: Tue, 09 Jul 2024 00:09:47 GMT  
		Size: 4.2 MB (4183567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1b2db8d722ed82eb4bfb595a82d293c16047c359b6f8fc016577f779a64e123`  
		Last Modified: Tue, 09 Jul 2024 00:09:46 GMT  
		Size: 19.8 KB (19758 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:033a62e86be2207bedf27147b18b9e26ee295ebdc15f5cc746d87da400543b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.7 MB (397687547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075470a2e23577cf42e19eaa98fb370bf886622fc4afe0bbcd4fdeb71c02452c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 02 Apr 2024 10:10:05 GMT
ARG RELEASE
# Tue, 02 Apr 2024 10:10:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 02 Apr 2024 10:10:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 02 Apr 2024 10:10:05 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 02 Apr 2024 10:10:05 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["/bin/bash"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Apr 2024 10:10:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Apr 2024 10:10:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Apr 2024 10:10:05 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Apr 2024 10:10:05 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_VERSION=9.0.91
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT []
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Apr 2024 10:10:05 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_VERSION=3.12.11
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_DOWNLOAD_MD5=2ece7076f05068e7a5270af03e32d632
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Apr 2024 10:10:05 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea30364eff82eb5379f35c10575a54ece802a6af1763591c0a6a999d72c84c`  
		Last Modified: Tue, 02 Jul 2024 05:04:14 GMT  
		Size: 13.7 MB (13714876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e381362c15b6f2494c8dc0d6a49beef7efc7bbf6ef1d3525b485ba3969369d6`  
		Last Modified: Tue, 02 Jul 2024 05:04:20 GMT  
		Size: 101.1 MB (101071152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4281d6414726ffc097764a21c03524fe8ed573c02d19bd3c56d0826936af97`  
		Last Modified: Tue, 02 Jul 2024 05:04:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11783fbc96e3c2e66f3c1814d9e8373cf19165f9c928ff6cbb681bb165bc69`  
		Last Modified: Tue, 02 Jul 2024 05:04:10 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31c743457c728a8c3e7ee95c76c1377e5d565ec1c89fe0bb9d0d159720e638d`  
		Last Modified: Wed, 03 Jul 2024 03:11:39 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fa0eac1b9c12ff31977df71761642bb369421b2dac22518fb3c9e9fac6592e`  
		Last Modified: Tue, 09 Jul 2024 03:16:23 GMT  
		Size: 12.7 MB (12733450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13c17d5b897e7cbafe1cd653e47ffbd7654092838fffbd142c2d5ec73ffd4f5`  
		Last Modified: Tue, 09 Jul 2024 03:53:14 GMT  
		Size: 234.6 MB (234578369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef926e15ea7df92c844cbc8e5324900cb336963bb63e4109f686c13919f6454`  
		Last Modified: Tue, 09 Jul 2024 03:53:08 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:0b172a327d1eead97c93e61fcbb68c9a92c19a55516f96219bc154a40b5addb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4206260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ef40afbdc54787ed106e3706fd22eb277beca11ce81f6f3b0c7c3ce5a5285e`

```dockerfile
```

-	Layers:
	-	`sha256:1998d068e1335482a74240c25043fb96be8a0a01a6b25f24595350d8a48b13ec`  
		Last Modified: Tue, 09 Jul 2024 03:53:08 GMT  
		Size: 4.2 MB (4186837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62775d3bb2d87c2cbc0c4cfad35d549dfd125a15c7eec754e4b7a8a17b518a7b`  
		Last Modified: Tue, 09 Jul 2024 03:53:08 GMT  
		Size: 19.4 KB (19423 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3-postgres`

```console
$ docker pull geonetwork@sha256:cfdd3798fb4d7838cea9b9c81bc5dfac61276b0812bcef7840e6ef31bcf25a60
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

### `geonetwork:3-postgres` - linux; amd64

```console
$ docker pull geonetwork@sha256:024ec9ea5fd8563122d0ef89e1ac17d64034fe3f5709317c2261914ab8732169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.6 MB (407599616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e5dcc08f4ef5d057c612fa0453df3577a42ca7aca2fecd6fa545ad1d966cea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 05 Oct 2023 16:23:50 GMT
ARG RELEASE
# Thu, 05 Oct 2023 16:23:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 16:23:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 16:23:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 16:23:50 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["/bin/bash"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Oct 2023 16:23:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 16:23:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 16:23:50 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 05 Oct 2023 16:23:50 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_MAJOR=9
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_VERSION=9.0.91
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT []
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_FILE=geonetwork.war
# Thu, 05 Oct 2023 16:23:50 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_VERSION=3.12.11
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_DOWNLOAD_MD5=2ece7076f05068e7a5270af03e32d632
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 05 Oct 2023 16:23:50 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Oct 2023 16:23:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c055a91d57277ea410b92f9111e94845a0af82fef9cd5a097d9fbc848a91ce`  
		Last Modified: Tue, 02 Jul 2024 06:00:43 GMT  
		Size: 103.6 MB (103602292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b28fbf33e422d49b0808a16bed3bec227994163e4a31055a9bafd01c79f3bb4`  
		Last Modified: Tue, 02 Jul 2024 06:00:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0181c354541a8d59c19608901cbe6e45143749529d1dff48a049e5440b1a20e`  
		Last Modified: Tue, 02 Jul 2024 06:00:35 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b492ddc7448e8d14769b96b40b1a7dedb8c6a610871a0a6a192a6d8ff456d5`  
		Last Modified: Mon, 08 Jul 2024 22:57:12 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912d3997dd70072ace062d0c85a96473dec820953c29ce3885e5dd5285b6ab6d`  
		Last Modified: Mon, 08 Jul 2024 22:57:12 GMT  
		Size: 12.7 MB (12673408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1bf3a9a7265b6eb5d03aafa2eb8fd87e52bb1c4f0627be3a2b80027e158a14`  
		Last Modified: Mon, 08 Jul 2024 23:58:33 GMT  
		Size: 234.5 MB (234540666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2a16d137ccf1ed2c6bc1e0389f34d3d8d257c14b128591ebc1ed051b930ce8`  
		Last Modified: Mon, 08 Jul 2024 23:58:28 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8971503a390816828369a65b814e8287262c48f76f8139dce08e22ea21634efb`  
		Last Modified: Tue, 09 Jul 2024 00:50:17 GMT  
		Size: 13.5 MB (13467572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910568460b30e595e6d9ee224b52205e522226f25f5962a836e6ae97852a6ca9`  
		Last Modified: Tue, 09 Jul 2024 00:50:17 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3ce9c5aa0956081b5c94d576e14c3d0be980f7db26a5e998ebe14f41c67983`  
		Last Modified: Tue, 09 Jul 2024 00:50:17 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdac29bc2d3756b2a10e9019df63f157e1d83114aa8b48d5622919be4eea2bff`  
		Last Modified: Tue, 09 Jul 2024 00:50:17 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:6f6b8f65ebc6f1cf99f763751fda210eab2ce5135fd35b5d116acd7c9bcfb4bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5744280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ccda3d98e5098581c4c045386facdd58a48a962291cedd074b5e60ba6a6484`

```dockerfile
```

-	Layers:
	-	`sha256:d78b50653269f6583de5c2e6ec4e6c39e46ff2e7feca641d9159ce31c749f35c`  
		Last Modified: Tue, 09 Jul 2024 00:50:17 GMT  
		Size: 5.7 MB (5721186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5635ec5be40490e74843464e57a40506d45678d861fd3124bc6f17ad31d8c2fa`  
		Last Modified: Tue, 09 Jul 2024 00:50:17 GMT  
		Size: 23.1 KB (23094 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:013f9f72bace9e43a931259b9e76a10257fe8e30412a8130d8c1557df79de48d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.9 MB (398879312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca8cc3c9d511716c2475a88435ff98574994eb3dbbcdc03ce51dcd0a94fc1f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 05 Oct 2023 16:23:50 GMT
ARG RELEASE
# Thu, 05 Oct 2023 16:23:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 16:23:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 16:23:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 16:23:50 GMT
ADD file:967120bb21c0fbaf9bf6c8fcb7b292d31ec4812e538714e8beb0a6e013eae873 in / 
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["/bin/bash"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Oct 2023 16:23:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 16:23:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 16:23:50 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 05 Oct 2023 16:23:50 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_MAJOR=9
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_VERSION=9.0.91
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT []
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_FILE=geonetwork.war
# Thu, 05 Oct 2023 16:23:50 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_VERSION=3.12.11
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_DOWNLOAD_MD5=2ece7076f05068e7a5270af03e32d632
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 05 Oct 2023 16:23:50 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Oct 2023 16:23:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e180e7b68e21ed1490bb8293a3e848136812456d07f1be0783ef04f773a97867`  
		Last Modified: Fri, 28 Jun 2024 02:10:28 GMT  
		Size: 27.5 MB (27534011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3600b7820ccdab844af0b11c36a1aeadc460c5a3bc6a6fd0211a3fa9024fb1`  
		Last Modified: Tue, 02 Jul 2024 04:32:24 GMT  
		Size: 12.5 MB (12462968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2795f90fa7d600dee1f4eb73c08bb2d18123b06d13636002d46176c4b2f023f3`  
		Last Modified: Thu, 25 Jul 2024 18:01:01 GMT  
		Size: 99.2 MB (99249372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2c3b2a91fa20610bf53f9d0a722666976bbced1fddeabec3b2f1cafa30130f`  
		Last Modified: Thu, 25 Jul 2024 18:00:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4602dfe42d8b2b444328e0fb2b51ef2d074bcde8a413952b8269fe2bb2b489f6`  
		Last Modified: Thu, 25 Jul 2024 18:00:53 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc7d8efb5ef48317356561b1ec3b9b83a9949fd96d2effd6000c2a408fa0791`  
		Last Modified: Thu, 25 Jul 2024 19:39:25 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602497ca0baec3960eb142ca73787cbde70559ff89237b96f82118f2fb75a5c4`  
		Last Modified: Thu, 25 Jul 2024 19:39:26 GMT  
		Size: 12.6 MB (12580273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac5139b450dfef48663dd8c23544da8a664b35efe72d137db81ea058d954d98`  
		Last Modified: Thu, 25 Jul 2024 20:42:10 GMT  
		Size: 234.5 MB (234528624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bb4da193e005f20ee0f81ad66238a473fcfaa348f687c5513fb5743724f87c`  
		Last Modified: Thu, 25 Jul 2024 20:42:04 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b541313a436da0349679abac04d5f77b68cb760b11a3b9c5d88dd355fd440ecd`  
		Last Modified: Thu, 25 Jul 2024 21:10:28 GMT  
		Size: 12.5 MB (12518186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c3c2f48a99d82931e307f1121400e8d1f5287976d73abd5f658fac7ce1a634`  
		Last Modified: Thu, 25 Jul 2024 21:10:27 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3acbbb4c8ac2d53aba6f66f95fba3ed1beced6b4a3e9f50a7aa0c6ea0e5a4b`  
		Last Modified: Thu, 25 Jul 2024 21:10:27 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db94b23e5702419e945a895972dc76c4974d7555a372dbf0cf4ab5606162111`  
		Last Modified: Thu, 25 Jul 2024 21:10:28 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:68d15619bc7b40e433defa5c897f05a376eeb0789d98f8b275506283379da83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5869865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e886f6b54463b4564188a5456bbff19f0649860e5ca2fca86560d67f730f341`

```dockerfile
```

-	Layers:
	-	`sha256:ca7d53dbcb870c65c91d980f9eeca435ef11a5dfdae42e02b48035806d9fa9cb`  
		Last Modified: Thu, 25 Jul 2024 21:10:28 GMT  
		Size: 5.8 MB (5846540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e12eb1384ad3a67e613696cd412a8f37d801d8aee7d716d259d20b49641165c7`  
		Last Modified: Thu, 25 Jul 2024 21:10:27 GMT  
		Size: 23.3 KB (23325 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:bb15b59ce073e7beb94cd3362c9b3c94907ce68897a34b2744d53e74cfe42f6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.5 MB (404510393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed02e275091a7a87ed905bf8d425f3151c6cddcc7e955642fc990521f7b6f367`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 05 Oct 2023 16:23:50 GMT
ARG RELEASE
# Thu, 05 Oct 2023 16:23:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 16:23:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 16:23:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 16:23:50 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["/bin/bash"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Oct 2023 16:23:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 16:23:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 16:23:50 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 05 Oct 2023 16:23:50 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_MAJOR=9
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_VERSION=9.0.91
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT []
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_FILE=geonetwork.war
# Thu, 05 Oct 2023 16:23:50 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_VERSION=3.12.11
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_DOWNLOAD_MD5=2ece7076f05068e7a5270af03e32d632
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 05 Oct 2023 16:23:50 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Oct 2023 16:23:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bdbc9eb1fb5990eb08fa9fe21450674d749b586acb5e75044993eaa173745d`  
		Last Modified: Tue, 02 Jul 2024 04:34:28 GMT  
		Size: 102.7 MB (102704169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2f56b637ad3ed974bf5d3f1b3963f194651c946391e4c9d1460693f56c8ea4`  
		Last Modified: Tue, 02 Jul 2024 04:34:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32dd5676062f79e6e7a076fdfd9b5dcd7f10701b1e7eb2cf21d1fece49f72190`  
		Last Modified: Tue, 02 Jul 2024 04:34:21 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af06264ab206fceff972cc63c64fadfac0dcc401e8dde9e30ede88067f01654`  
		Last Modified: Wed, 03 Jul 2024 01:00:18 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba539a524bb8cfa8b0c80f9c30f43f28d1dce4ea437dfc7fa7532ccd126336d`  
		Last Modified: Mon, 08 Jul 2024 23:14:30 GMT  
		Size: 12.7 MB (12679916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f62e239ce4eb896f669e74bc6c0dabb558fa52d23f61ff7c5d73b44e08a98a`  
		Last Modified: Tue, 09 Jul 2024 00:09:52 GMT  
		Size: 234.5 MB (234537412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42182b40f87b380bd51d17a491f660c27485c9d8375172d300419dfe824113dc`  
		Last Modified: Tue, 09 Jul 2024 00:09:47 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25ff8819b17ec944cf30355e65267d44034ba3273eb940bad5a008e7c795c9f`  
		Last Modified: Tue, 09 Jul 2024 01:57:47 GMT  
		Size: 13.4 MB (13370057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ba217245e1864d7fb653be3f13fef42969bf5b4dbf5ec3cb6bbaadee5215c3`  
		Last Modified: Tue, 09 Jul 2024 01:57:46 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a1be51ff5967fcb43262c6d971f467af67c3e2eec45927cae0e991e584b3dc`  
		Last Modified: Tue, 09 Jul 2024 01:57:46 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6727609dd100bed1f7189137b9261d29709c279fe1f95fb24a399d67d86fab23`  
		Last Modified: Tue, 09 Jul 2024 01:57:46 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:7f6b36b1015d9c6d50dcb553a322e5bb3663bff249090d35c37a4ce87d637035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5751130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ff8968139067ebdc265342755f7ddb39fd0f7da73db49d6975ed774c1ea24d`

```dockerfile
```

-	Layers:
	-	`sha256:67e5142ae0cd517a5a2fd7756f9255fe17b9d55e36819af0484c2644c1879859`  
		Last Modified: Tue, 09 Jul 2024 01:57:46 GMT  
		Size: 5.7 MB (5727513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24296a82b40f353e5c46c56331e45aabaf90560b66a2fd685f97259a7104fcf1`  
		Last Modified: Tue, 09 Jul 2024 01:57:46 GMT  
		Size: 23.6 KB (23617 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:a0dba107172c948963611fe989c87312a7364c115b35e0c2181539acb22e683e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.7 MB (411651843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700381a7f3406d736114ab55265f546c57147a684678b7d1ce8751d89fa72aa6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 05 Oct 2023 16:23:50 GMT
ARG RELEASE
# Thu, 05 Oct 2023 16:23:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 16:23:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 16:23:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 16:23:50 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["/bin/bash"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Oct 2023 16:23:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 16:23:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 16:23:50 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 05 Oct 2023 16:23:50 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_MAJOR=9
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_VERSION=9.0.91
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT []
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_FILE=geonetwork.war
# Thu, 05 Oct 2023 16:23:50 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_VERSION=3.12.11
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_DOWNLOAD_MD5=2ece7076f05068e7a5270af03e32d632
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 05 Oct 2023 16:23:50 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Oct 2023 16:23:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea30364eff82eb5379f35c10575a54ece802a6af1763591c0a6a999d72c84c`  
		Last Modified: Tue, 02 Jul 2024 05:04:14 GMT  
		Size: 13.7 MB (13714876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e381362c15b6f2494c8dc0d6a49beef7efc7bbf6ef1d3525b485ba3969369d6`  
		Last Modified: Tue, 02 Jul 2024 05:04:20 GMT  
		Size: 101.1 MB (101071152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4281d6414726ffc097764a21c03524fe8ed573c02d19bd3c56d0826936af97`  
		Last Modified: Tue, 02 Jul 2024 05:04:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11783fbc96e3c2e66f3c1814d9e8373cf19165f9c928ff6cbb681bb165bc69`  
		Last Modified: Tue, 02 Jul 2024 05:04:10 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31c743457c728a8c3e7ee95c76c1377e5d565ec1c89fe0bb9d0d159720e638d`  
		Last Modified: Wed, 03 Jul 2024 03:11:39 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fa0eac1b9c12ff31977df71761642bb369421b2dac22518fb3c9e9fac6592e`  
		Last Modified: Tue, 09 Jul 2024 03:16:23 GMT  
		Size: 12.7 MB (12733450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13c17d5b897e7cbafe1cd653e47ffbd7654092838fffbd142c2d5ec73ffd4f5`  
		Last Modified: Tue, 09 Jul 2024 03:53:14 GMT  
		Size: 234.6 MB (234578369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef926e15ea7df92c844cbc8e5324900cb336963bb63e4109f686c13919f6454`  
		Last Modified: Tue, 09 Jul 2024 03:53:08 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf3bad02a93d9e1c8bdf5974977b13d9cae8fe883e58df336468307204aeced`  
		Last Modified: Tue, 09 Jul 2024 04:49:32 GMT  
		Size: 14.0 MB (13960926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630fd7156ec9036ba7309fd4e1c9d8e27858528ca3b9353b4706818cbd1961ea`  
		Last Modified: Tue, 09 Jul 2024 04:49:32 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f42b03fa32f1fd947fb87f98a583bf1a97f119bbcf37b6b5c12e0629d14386`  
		Last Modified: Tue, 09 Jul 2024 04:49:32 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff554c409056d1c68ed9adcb987cd0c8c00a32314ba78729fad6ff3b363356b`  
		Last Modified: Tue, 09 Jul 2024 04:49:32 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:fb6b03452b517abae90bbb0a349508610fc19453276a4be4df78893a360b5d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5750724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb451ed13aa884e07a56fae9db013ef0795a87177b196787887e6d8d2cdd0307`

```dockerfile
```

-	Layers:
	-	`sha256:88031456e061ff86ae7980a0ba7a57e06524382661aafad108aaf67929d97989`  
		Last Modified: Tue, 09 Jul 2024 04:49:32 GMT  
		Size: 5.7 MB (5727440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dea8fac5f7466ef12f55a0f5e7fc323598cbc24024b2fca8c77407d63413821e`  
		Last Modified: Tue, 09 Jul 2024 04:49:32 GMT  
		Size: 23.3 KB (23284 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12`

```console
$ docker pull geonetwork@sha256:bf3eee42b5b90245b7a48efb3373f591e901b8b39e349bc380ed45b7527b7713
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

### `geonetwork:3.12` - linux; amd64

```console
$ docker pull geonetwork@sha256:96e0421942ad0299075f09604e345f43a70082bc07af0dc2ce1d9e69dd82a511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.1 MB (394143302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ad5370e0b6b524f2ecf18a502edc6cab4ab69d30e9884da5f8e75c2fe07e71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 02 Apr 2024 10:10:05 GMT
ARG RELEASE
# Tue, 02 Apr 2024 10:10:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 02 Apr 2024 10:10:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 02 Apr 2024 10:10:05 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 02 Apr 2024 10:10:05 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["/bin/bash"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Apr 2024 10:10:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Apr 2024 10:10:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Apr 2024 10:10:05 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Apr 2024 10:10:05 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_VERSION=9.0.91
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT []
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Apr 2024 10:10:05 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_VERSION=3.12.11
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_DOWNLOAD_MD5=2ece7076f05068e7a5270af03e32d632
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Apr 2024 10:10:05 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4040a9fc8f154e4bdc7b1fada39d21321aa2fa67f5ec71b3c6ced523d6bca756`  
		Last Modified: Thu, 25 Jul 2024 17:26:10 GMT  
		Size: 103.6 MB (103615844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a876aecb20e71daf56b1b8ebbe1e3e11f26f6d9ca83e6933e9fb7b9c5a9db53e`  
		Last Modified: Thu, 25 Jul 2024 17:26:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaf0a30f7dfdef304092a7f19ad21c11e30bcf6bf04e60ff7b75b504d6cf8f4`  
		Last Modified: Thu, 25 Jul 2024 17:26:03 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba983e46ea55676251c498d1239a189987f977bb6e5fa073187abceb7e5f0cf`  
		Last Modified: Thu, 25 Jul 2024 19:07:43 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9515ec726a6d5e4c67aba5376b55ec8e44ded359a6c8fde8f8003be7dfd3dc5`  
		Last Modified: Thu, 25 Jul 2024 19:07:43 GMT  
		Size: 12.7 MB (12673367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6440b786c3d6737a9a28f7ee4373f024da452d2f8a4874164a21e56809970e0b`  
		Last Modified: Thu, 25 Jul 2024 20:10:51 GMT  
		Size: 234.5 MB (234540645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468205bc3496401939f90c6c7ba7b461679e0af5913b75d0746b3d6c754ad73a`  
		Last Modified: Thu, 25 Jul 2024 20:10:45 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:c14c673fb0a7d2e25a01e9f82dd3d234a6fa8a08c990472800ef1594fad6367f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ee72391e418cecf7f0dd3f5ba9dd69d51923f62dbecba9c44c340782e6dc4f`

```dockerfile
```

-	Layers:
	-	`sha256:d4d0a589fe0622103f9d9df49f9a493915ffa75372575ceb89ef11d837d99cf7`  
		Last Modified: Thu, 25 Jul 2024 20:10:46 GMT  
		Size: 4.3 MB (4305065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:948dda15e627d436862259ec981af9d32b043abe317f0c2958bb8d819eecea80`  
		Last Modified: Thu, 25 Jul 2024 20:10:45 GMT  
		Size: 19.2 KB (19240 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:dfa33b4015a4e19a8152b39461582b97f36c7ceb73fa73e952699f27aabea53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.4 MB (386357758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583282d5e8bed9e923c9a5af98d7536fccd8dfb18bbb2b797d62d32119e1814f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 02 Apr 2024 10:10:05 GMT
ARG RELEASE
# Tue, 02 Apr 2024 10:10:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 02 Apr 2024 10:10:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 02 Apr 2024 10:10:05 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 02 Apr 2024 10:10:05 GMT
ADD file:967120bb21c0fbaf9bf6c8fcb7b292d31ec4812e538714e8beb0a6e013eae873 in / 
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["/bin/bash"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Apr 2024 10:10:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Apr 2024 10:10:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Apr 2024 10:10:05 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Apr 2024 10:10:05 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_VERSION=9.0.91
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT []
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Apr 2024 10:10:05 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_VERSION=3.12.11
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_DOWNLOAD_MD5=2ece7076f05068e7a5270af03e32d632
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Apr 2024 10:10:05 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e180e7b68e21ed1490bb8293a3e848136812456d07f1be0783ef04f773a97867`  
		Last Modified: Fri, 28 Jun 2024 02:10:28 GMT  
		Size: 27.5 MB (27534011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3600b7820ccdab844af0b11c36a1aeadc460c5a3bc6a6fd0211a3fa9024fb1`  
		Last Modified: Tue, 02 Jul 2024 04:32:24 GMT  
		Size: 12.5 MB (12462968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2795f90fa7d600dee1f4eb73c08bb2d18123b06d13636002d46176c4b2f023f3`  
		Last Modified: Thu, 25 Jul 2024 18:01:01 GMT  
		Size: 99.2 MB (99249372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2c3b2a91fa20610bf53f9d0a722666976bbced1fddeabec3b2f1cafa30130f`  
		Last Modified: Thu, 25 Jul 2024 18:00:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4602dfe42d8b2b444328e0fb2b51ef2d074bcde8a413952b8269fe2bb2b489f6`  
		Last Modified: Thu, 25 Jul 2024 18:00:53 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc7d8efb5ef48317356561b1ec3b9b83a9949fd96d2effd6000c2a408fa0791`  
		Last Modified: Thu, 25 Jul 2024 19:39:25 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602497ca0baec3960eb142ca73787cbde70559ff89237b96f82118f2fb75a5c4`  
		Last Modified: Thu, 25 Jul 2024 19:39:26 GMT  
		Size: 12.6 MB (12580273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac5139b450dfef48663dd8c23544da8a664b35efe72d137db81ea058d954d98`  
		Last Modified: Thu, 25 Jul 2024 20:42:10 GMT  
		Size: 234.5 MB (234528624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bb4da193e005f20ee0f81ad66238a473fcfaa348f687c5513fb5743724f87c`  
		Last Modified: Thu, 25 Jul 2024 20:42:04 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:c1cafc419cefeb5e1963760100487607e34fdad3e2e76a1787b4ce4648250e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c07416149f052dac48b0c727d61ea78a21fafabc7bc53a3dc9f91e37fcc76e`

```dockerfile
```

-	Layers:
	-	`sha256:a73477235ccc024e29f5f46d1bf3d3275d01cb274168c89bff2a9efa5d9bf01c`  
		Last Modified: Thu, 25 Jul 2024 20:42:05 GMT  
		Size: 4.3 MB (4307783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63da1de726f860c2899727edc74c941c471fd1993452e6840962e7950f4e83fc`  
		Last Modified: Thu, 25 Jul 2024 20:42:04 GMT  
		Size: 19.5 KB (19453 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:13b65e11fead24599650ecf307cbcff09d7f5644911dc258886ff42711992cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.1 MB (391136969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14487c71572df86e40e6f00f0139cc42de2b5e90d547dfc3474924b10918680`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 02 Apr 2024 10:10:05 GMT
ARG RELEASE
# Tue, 02 Apr 2024 10:10:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 02 Apr 2024 10:10:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 02 Apr 2024 10:10:05 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 02 Apr 2024 10:10:05 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["/bin/bash"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Apr 2024 10:10:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Apr 2024 10:10:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Apr 2024 10:10:05 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Apr 2024 10:10:05 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_VERSION=9.0.91
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT []
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Apr 2024 10:10:05 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_VERSION=3.12.11
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_DOWNLOAD_MD5=2ece7076f05068e7a5270af03e32d632
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Apr 2024 10:10:05 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bdbc9eb1fb5990eb08fa9fe21450674d749b586acb5e75044993eaa173745d`  
		Last Modified: Tue, 02 Jul 2024 04:34:28 GMT  
		Size: 102.7 MB (102704169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2f56b637ad3ed974bf5d3f1b3963f194651c946391e4c9d1460693f56c8ea4`  
		Last Modified: Tue, 02 Jul 2024 04:34:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32dd5676062f79e6e7a076fdfd9b5dcd7f10701b1e7eb2cf21d1fece49f72190`  
		Last Modified: Tue, 02 Jul 2024 04:34:21 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af06264ab206fceff972cc63c64fadfac0dcc401e8dde9e30ede88067f01654`  
		Last Modified: Wed, 03 Jul 2024 01:00:18 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba539a524bb8cfa8b0c80f9c30f43f28d1dce4ea437dfc7fa7532ccd126336d`  
		Last Modified: Mon, 08 Jul 2024 23:14:30 GMT  
		Size: 12.7 MB (12679916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f62e239ce4eb896f669e74bc6c0dabb558fa52d23f61ff7c5d73b44e08a98a`  
		Last Modified: Tue, 09 Jul 2024 00:09:52 GMT  
		Size: 234.5 MB (234537412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42182b40f87b380bd51d17a491f660c27485c9d8375172d300419dfe824113dc`  
		Last Modified: Tue, 09 Jul 2024 00:09:47 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:77f0dee9efb464431027b94996ded1871353e61220cace8178c483a509b9b3a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4203325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4745721776422c6895ea7ed3ad26de2c0458a1bf53621b5209a87784e3099420`

```dockerfile
```

-	Layers:
	-	`sha256:49f0ee1781aa1d9573c08d54d4f6a0bf26fe793a4fd1c81e5b6091c60d6f0a80`  
		Last Modified: Tue, 09 Jul 2024 00:09:47 GMT  
		Size: 4.2 MB (4183567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1b2db8d722ed82eb4bfb595a82d293c16047c359b6f8fc016577f779a64e123`  
		Last Modified: Tue, 09 Jul 2024 00:09:46 GMT  
		Size: 19.8 KB (19758 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:033a62e86be2207bedf27147b18b9e26ee295ebdc15f5cc746d87da400543b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.7 MB (397687547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075470a2e23577cf42e19eaa98fb370bf886622fc4afe0bbcd4fdeb71c02452c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 02 Apr 2024 10:10:05 GMT
ARG RELEASE
# Tue, 02 Apr 2024 10:10:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 02 Apr 2024 10:10:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 02 Apr 2024 10:10:05 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 02 Apr 2024 10:10:05 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["/bin/bash"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Apr 2024 10:10:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Apr 2024 10:10:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Apr 2024 10:10:05 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Apr 2024 10:10:05 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_VERSION=9.0.91
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT []
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Apr 2024 10:10:05 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_VERSION=3.12.11
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_DOWNLOAD_MD5=2ece7076f05068e7a5270af03e32d632
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Apr 2024 10:10:05 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea30364eff82eb5379f35c10575a54ece802a6af1763591c0a6a999d72c84c`  
		Last Modified: Tue, 02 Jul 2024 05:04:14 GMT  
		Size: 13.7 MB (13714876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e381362c15b6f2494c8dc0d6a49beef7efc7bbf6ef1d3525b485ba3969369d6`  
		Last Modified: Tue, 02 Jul 2024 05:04:20 GMT  
		Size: 101.1 MB (101071152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4281d6414726ffc097764a21c03524fe8ed573c02d19bd3c56d0826936af97`  
		Last Modified: Tue, 02 Jul 2024 05:04:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11783fbc96e3c2e66f3c1814d9e8373cf19165f9c928ff6cbb681bb165bc69`  
		Last Modified: Tue, 02 Jul 2024 05:04:10 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31c743457c728a8c3e7ee95c76c1377e5d565ec1c89fe0bb9d0d159720e638d`  
		Last Modified: Wed, 03 Jul 2024 03:11:39 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fa0eac1b9c12ff31977df71761642bb369421b2dac22518fb3c9e9fac6592e`  
		Last Modified: Tue, 09 Jul 2024 03:16:23 GMT  
		Size: 12.7 MB (12733450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13c17d5b897e7cbafe1cd653e47ffbd7654092838fffbd142c2d5ec73ffd4f5`  
		Last Modified: Tue, 09 Jul 2024 03:53:14 GMT  
		Size: 234.6 MB (234578369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef926e15ea7df92c844cbc8e5324900cb336963bb63e4109f686c13919f6454`  
		Last Modified: Tue, 09 Jul 2024 03:53:08 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:0b172a327d1eead97c93e61fcbb68c9a92c19a55516f96219bc154a40b5addb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4206260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ef40afbdc54787ed106e3706fd22eb277beca11ce81f6f3b0c7c3ce5a5285e`

```dockerfile
```

-	Layers:
	-	`sha256:1998d068e1335482a74240c25043fb96be8a0a01a6b25f24595350d8a48b13ec`  
		Last Modified: Tue, 09 Jul 2024 03:53:08 GMT  
		Size: 4.2 MB (4186837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62775d3bb2d87c2cbc0c4cfad35d549dfd125a15c7eec754e4b7a8a17b518a7b`  
		Last Modified: Tue, 09 Jul 2024 03:53:08 GMT  
		Size: 19.4 KB (19423 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12-postgres`

```console
$ docker pull geonetwork@sha256:cfdd3798fb4d7838cea9b9c81bc5dfac61276b0812bcef7840e6ef31bcf25a60
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

### `geonetwork:3.12-postgres` - linux; amd64

```console
$ docker pull geonetwork@sha256:024ec9ea5fd8563122d0ef89e1ac17d64034fe3f5709317c2261914ab8732169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.6 MB (407599616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e5dcc08f4ef5d057c612fa0453df3577a42ca7aca2fecd6fa545ad1d966cea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 05 Oct 2023 16:23:50 GMT
ARG RELEASE
# Thu, 05 Oct 2023 16:23:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 16:23:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 16:23:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 16:23:50 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["/bin/bash"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Oct 2023 16:23:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 16:23:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 16:23:50 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 05 Oct 2023 16:23:50 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_MAJOR=9
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_VERSION=9.0.91
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT []
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_FILE=geonetwork.war
# Thu, 05 Oct 2023 16:23:50 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_VERSION=3.12.11
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_DOWNLOAD_MD5=2ece7076f05068e7a5270af03e32d632
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 05 Oct 2023 16:23:50 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Oct 2023 16:23:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c055a91d57277ea410b92f9111e94845a0af82fef9cd5a097d9fbc848a91ce`  
		Last Modified: Tue, 02 Jul 2024 06:00:43 GMT  
		Size: 103.6 MB (103602292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b28fbf33e422d49b0808a16bed3bec227994163e4a31055a9bafd01c79f3bb4`  
		Last Modified: Tue, 02 Jul 2024 06:00:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0181c354541a8d59c19608901cbe6e45143749529d1dff48a049e5440b1a20e`  
		Last Modified: Tue, 02 Jul 2024 06:00:35 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b492ddc7448e8d14769b96b40b1a7dedb8c6a610871a0a6a192a6d8ff456d5`  
		Last Modified: Mon, 08 Jul 2024 22:57:12 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912d3997dd70072ace062d0c85a96473dec820953c29ce3885e5dd5285b6ab6d`  
		Last Modified: Mon, 08 Jul 2024 22:57:12 GMT  
		Size: 12.7 MB (12673408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1bf3a9a7265b6eb5d03aafa2eb8fd87e52bb1c4f0627be3a2b80027e158a14`  
		Last Modified: Mon, 08 Jul 2024 23:58:33 GMT  
		Size: 234.5 MB (234540666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2a16d137ccf1ed2c6bc1e0389f34d3d8d257c14b128591ebc1ed051b930ce8`  
		Last Modified: Mon, 08 Jul 2024 23:58:28 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8971503a390816828369a65b814e8287262c48f76f8139dce08e22ea21634efb`  
		Last Modified: Tue, 09 Jul 2024 00:50:17 GMT  
		Size: 13.5 MB (13467572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910568460b30e595e6d9ee224b52205e522226f25f5962a836e6ae97852a6ca9`  
		Last Modified: Tue, 09 Jul 2024 00:50:17 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3ce9c5aa0956081b5c94d576e14c3d0be980f7db26a5e998ebe14f41c67983`  
		Last Modified: Tue, 09 Jul 2024 00:50:17 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdac29bc2d3756b2a10e9019df63f157e1d83114aa8b48d5622919be4eea2bff`  
		Last Modified: Tue, 09 Jul 2024 00:50:17 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:6f6b8f65ebc6f1cf99f763751fda210eab2ce5135fd35b5d116acd7c9bcfb4bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5744280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ccda3d98e5098581c4c045386facdd58a48a962291cedd074b5e60ba6a6484`

```dockerfile
```

-	Layers:
	-	`sha256:d78b50653269f6583de5c2e6ec4e6c39e46ff2e7feca641d9159ce31c749f35c`  
		Last Modified: Tue, 09 Jul 2024 00:50:17 GMT  
		Size: 5.7 MB (5721186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5635ec5be40490e74843464e57a40506d45678d861fd3124bc6f17ad31d8c2fa`  
		Last Modified: Tue, 09 Jul 2024 00:50:17 GMT  
		Size: 23.1 KB (23094 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:013f9f72bace9e43a931259b9e76a10257fe8e30412a8130d8c1557df79de48d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.9 MB (398879312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca8cc3c9d511716c2475a88435ff98574994eb3dbbcdc03ce51dcd0a94fc1f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 05 Oct 2023 16:23:50 GMT
ARG RELEASE
# Thu, 05 Oct 2023 16:23:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 16:23:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 16:23:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 16:23:50 GMT
ADD file:967120bb21c0fbaf9bf6c8fcb7b292d31ec4812e538714e8beb0a6e013eae873 in / 
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["/bin/bash"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Oct 2023 16:23:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 16:23:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 16:23:50 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 05 Oct 2023 16:23:50 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_MAJOR=9
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_VERSION=9.0.91
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT []
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_FILE=geonetwork.war
# Thu, 05 Oct 2023 16:23:50 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_VERSION=3.12.11
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_DOWNLOAD_MD5=2ece7076f05068e7a5270af03e32d632
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 05 Oct 2023 16:23:50 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Oct 2023 16:23:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e180e7b68e21ed1490bb8293a3e848136812456d07f1be0783ef04f773a97867`  
		Last Modified: Fri, 28 Jun 2024 02:10:28 GMT  
		Size: 27.5 MB (27534011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3600b7820ccdab844af0b11c36a1aeadc460c5a3bc6a6fd0211a3fa9024fb1`  
		Last Modified: Tue, 02 Jul 2024 04:32:24 GMT  
		Size: 12.5 MB (12462968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2795f90fa7d600dee1f4eb73c08bb2d18123b06d13636002d46176c4b2f023f3`  
		Last Modified: Thu, 25 Jul 2024 18:01:01 GMT  
		Size: 99.2 MB (99249372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2c3b2a91fa20610bf53f9d0a722666976bbced1fddeabec3b2f1cafa30130f`  
		Last Modified: Thu, 25 Jul 2024 18:00:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4602dfe42d8b2b444328e0fb2b51ef2d074bcde8a413952b8269fe2bb2b489f6`  
		Last Modified: Thu, 25 Jul 2024 18:00:53 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc7d8efb5ef48317356561b1ec3b9b83a9949fd96d2effd6000c2a408fa0791`  
		Last Modified: Thu, 25 Jul 2024 19:39:25 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602497ca0baec3960eb142ca73787cbde70559ff89237b96f82118f2fb75a5c4`  
		Last Modified: Thu, 25 Jul 2024 19:39:26 GMT  
		Size: 12.6 MB (12580273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac5139b450dfef48663dd8c23544da8a664b35efe72d137db81ea058d954d98`  
		Last Modified: Thu, 25 Jul 2024 20:42:10 GMT  
		Size: 234.5 MB (234528624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bb4da193e005f20ee0f81ad66238a473fcfaa348f687c5513fb5743724f87c`  
		Last Modified: Thu, 25 Jul 2024 20:42:04 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b541313a436da0349679abac04d5f77b68cb760b11a3b9c5d88dd355fd440ecd`  
		Last Modified: Thu, 25 Jul 2024 21:10:28 GMT  
		Size: 12.5 MB (12518186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c3c2f48a99d82931e307f1121400e8d1f5287976d73abd5f658fac7ce1a634`  
		Last Modified: Thu, 25 Jul 2024 21:10:27 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3acbbb4c8ac2d53aba6f66f95fba3ed1beced6b4a3e9f50a7aa0c6ea0e5a4b`  
		Last Modified: Thu, 25 Jul 2024 21:10:27 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db94b23e5702419e945a895972dc76c4974d7555a372dbf0cf4ab5606162111`  
		Last Modified: Thu, 25 Jul 2024 21:10:28 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:68d15619bc7b40e433defa5c897f05a376eeb0789d98f8b275506283379da83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5869865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e886f6b54463b4564188a5456bbff19f0649860e5ca2fca86560d67f730f341`

```dockerfile
```

-	Layers:
	-	`sha256:ca7d53dbcb870c65c91d980f9eeca435ef11a5dfdae42e02b48035806d9fa9cb`  
		Last Modified: Thu, 25 Jul 2024 21:10:28 GMT  
		Size: 5.8 MB (5846540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e12eb1384ad3a67e613696cd412a8f37d801d8aee7d716d259d20b49641165c7`  
		Last Modified: Thu, 25 Jul 2024 21:10:27 GMT  
		Size: 23.3 KB (23325 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:bb15b59ce073e7beb94cd3362c9b3c94907ce68897a34b2744d53e74cfe42f6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.5 MB (404510393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed02e275091a7a87ed905bf8d425f3151c6cddcc7e955642fc990521f7b6f367`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 05 Oct 2023 16:23:50 GMT
ARG RELEASE
# Thu, 05 Oct 2023 16:23:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 16:23:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 16:23:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 16:23:50 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["/bin/bash"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Oct 2023 16:23:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 16:23:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 16:23:50 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 05 Oct 2023 16:23:50 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_MAJOR=9
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_VERSION=9.0.91
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT []
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_FILE=geonetwork.war
# Thu, 05 Oct 2023 16:23:50 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_VERSION=3.12.11
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_DOWNLOAD_MD5=2ece7076f05068e7a5270af03e32d632
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 05 Oct 2023 16:23:50 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Oct 2023 16:23:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bdbc9eb1fb5990eb08fa9fe21450674d749b586acb5e75044993eaa173745d`  
		Last Modified: Tue, 02 Jul 2024 04:34:28 GMT  
		Size: 102.7 MB (102704169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2f56b637ad3ed974bf5d3f1b3963f194651c946391e4c9d1460693f56c8ea4`  
		Last Modified: Tue, 02 Jul 2024 04:34:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32dd5676062f79e6e7a076fdfd9b5dcd7f10701b1e7eb2cf21d1fece49f72190`  
		Last Modified: Tue, 02 Jul 2024 04:34:21 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af06264ab206fceff972cc63c64fadfac0dcc401e8dde9e30ede88067f01654`  
		Last Modified: Wed, 03 Jul 2024 01:00:18 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba539a524bb8cfa8b0c80f9c30f43f28d1dce4ea437dfc7fa7532ccd126336d`  
		Last Modified: Mon, 08 Jul 2024 23:14:30 GMT  
		Size: 12.7 MB (12679916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f62e239ce4eb896f669e74bc6c0dabb558fa52d23f61ff7c5d73b44e08a98a`  
		Last Modified: Tue, 09 Jul 2024 00:09:52 GMT  
		Size: 234.5 MB (234537412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42182b40f87b380bd51d17a491f660c27485c9d8375172d300419dfe824113dc`  
		Last Modified: Tue, 09 Jul 2024 00:09:47 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25ff8819b17ec944cf30355e65267d44034ba3273eb940bad5a008e7c795c9f`  
		Last Modified: Tue, 09 Jul 2024 01:57:47 GMT  
		Size: 13.4 MB (13370057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ba217245e1864d7fb653be3f13fef42969bf5b4dbf5ec3cb6bbaadee5215c3`  
		Last Modified: Tue, 09 Jul 2024 01:57:46 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a1be51ff5967fcb43262c6d971f467af67c3e2eec45927cae0e991e584b3dc`  
		Last Modified: Tue, 09 Jul 2024 01:57:46 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6727609dd100bed1f7189137b9261d29709c279fe1f95fb24a399d67d86fab23`  
		Last Modified: Tue, 09 Jul 2024 01:57:46 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:7f6b36b1015d9c6d50dcb553a322e5bb3663bff249090d35c37a4ce87d637035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5751130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ff8968139067ebdc265342755f7ddb39fd0f7da73db49d6975ed774c1ea24d`

```dockerfile
```

-	Layers:
	-	`sha256:67e5142ae0cd517a5a2fd7756f9255fe17b9d55e36819af0484c2644c1879859`  
		Last Modified: Tue, 09 Jul 2024 01:57:46 GMT  
		Size: 5.7 MB (5727513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24296a82b40f353e5c46c56331e45aabaf90560b66a2fd685f97259a7104fcf1`  
		Last Modified: Tue, 09 Jul 2024 01:57:46 GMT  
		Size: 23.6 KB (23617 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:a0dba107172c948963611fe989c87312a7364c115b35e0c2181539acb22e683e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.7 MB (411651843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700381a7f3406d736114ab55265f546c57147a684678b7d1ce8751d89fa72aa6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 05 Oct 2023 16:23:50 GMT
ARG RELEASE
# Thu, 05 Oct 2023 16:23:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 16:23:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 16:23:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 16:23:50 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["/bin/bash"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Oct 2023 16:23:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 16:23:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 16:23:50 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 05 Oct 2023 16:23:50 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_MAJOR=9
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_VERSION=9.0.91
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT []
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_FILE=geonetwork.war
# Thu, 05 Oct 2023 16:23:50 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_VERSION=3.12.11
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_DOWNLOAD_MD5=2ece7076f05068e7a5270af03e32d632
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 05 Oct 2023 16:23:50 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Oct 2023 16:23:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea30364eff82eb5379f35c10575a54ece802a6af1763591c0a6a999d72c84c`  
		Last Modified: Tue, 02 Jul 2024 05:04:14 GMT  
		Size: 13.7 MB (13714876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e381362c15b6f2494c8dc0d6a49beef7efc7bbf6ef1d3525b485ba3969369d6`  
		Last Modified: Tue, 02 Jul 2024 05:04:20 GMT  
		Size: 101.1 MB (101071152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4281d6414726ffc097764a21c03524fe8ed573c02d19bd3c56d0826936af97`  
		Last Modified: Tue, 02 Jul 2024 05:04:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11783fbc96e3c2e66f3c1814d9e8373cf19165f9c928ff6cbb681bb165bc69`  
		Last Modified: Tue, 02 Jul 2024 05:04:10 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31c743457c728a8c3e7ee95c76c1377e5d565ec1c89fe0bb9d0d159720e638d`  
		Last Modified: Wed, 03 Jul 2024 03:11:39 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fa0eac1b9c12ff31977df71761642bb369421b2dac22518fb3c9e9fac6592e`  
		Last Modified: Tue, 09 Jul 2024 03:16:23 GMT  
		Size: 12.7 MB (12733450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13c17d5b897e7cbafe1cd653e47ffbd7654092838fffbd142c2d5ec73ffd4f5`  
		Last Modified: Tue, 09 Jul 2024 03:53:14 GMT  
		Size: 234.6 MB (234578369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef926e15ea7df92c844cbc8e5324900cb336963bb63e4109f686c13919f6454`  
		Last Modified: Tue, 09 Jul 2024 03:53:08 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf3bad02a93d9e1c8bdf5974977b13d9cae8fe883e58df336468307204aeced`  
		Last Modified: Tue, 09 Jul 2024 04:49:32 GMT  
		Size: 14.0 MB (13960926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630fd7156ec9036ba7309fd4e1c9d8e27858528ca3b9353b4706818cbd1961ea`  
		Last Modified: Tue, 09 Jul 2024 04:49:32 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f42b03fa32f1fd947fb87f98a583bf1a97f119bbcf37b6b5c12e0629d14386`  
		Last Modified: Tue, 09 Jul 2024 04:49:32 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff554c409056d1c68ed9adcb987cd0c8c00a32314ba78729fad6ff3b363356b`  
		Last Modified: Tue, 09 Jul 2024 04:49:32 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:fb6b03452b517abae90bbb0a349508610fc19453276a4be4df78893a360b5d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5750724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb451ed13aa884e07a56fae9db013ef0795a87177b196787887e6d8d2cdd0307`

```dockerfile
```

-	Layers:
	-	`sha256:88031456e061ff86ae7980a0ba7a57e06524382661aafad108aaf67929d97989`  
		Last Modified: Tue, 09 Jul 2024 04:49:32 GMT  
		Size: 5.7 MB (5727440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dea8fac5f7466ef12f55a0f5e7fc323598cbc24024b2fca8c77407d63413821e`  
		Last Modified: Tue, 09 Jul 2024 04:49:32 GMT  
		Size: 23.3 KB (23284 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12.11`

```console
$ docker pull geonetwork@sha256:bf3eee42b5b90245b7a48efb3373f591e901b8b39e349bc380ed45b7527b7713
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

### `geonetwork:3.12.11` - linux; amd64

```console
$ docker pull geonetwork@sha256:96e0421942ad0299075f09604e345f43a70082bc07af0dc2ce1d9e69dd82a511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.1 MB (394143302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ad5370e0b6b524f2ecf18a502edc6cab4ab69d30e9884da5f8e75c2fe07e71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 02 Apr 2024 10:10:05 GMT
ARG RELEASE
# Tue, 02 Apr 2024 10:10:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 02 Apr 2024 10:10:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 02 Apr 2024 10:10:05 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 02 Apr 2024 10:10:05 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["/bin/bash"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Apr 2024 10:10:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Apr 2024 10:10:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Apr 2024 10:10:05 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Apr 2024 10:10:05 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_VERSION=9.0.91
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT []
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Apr 2024 10:10:05 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_VERSION=3.12.11
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_DOWNLOAD_MD5=2ece7076f05068e7a5270af03e32d632
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Apr 2024 10:10:05 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4040a9fc8f154e4bdc7b1fada39d21321aa2fa67f5ec71b3c6ced523d6bca756`  
		Last Modified: Thu, 25 Jul 2024 17:26:10 GMT  
		Size: 103.6 MB (103615844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a876aecb20e71daf56b1b8ebbe1e3e11f26f6d9ca83e6933e9fb7b9c5a9db53e`  
		Last Modified: Thu, 25 Jul 2024 17:26:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaf0a30f7dfdef304092a7f19ad21c11e30bcf6bf04e60ff7b75b504d6cf8f4`  
		Last Modified: Thu, 25 Jul 2024 17:26:03 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba983e46ea55676251c498d1239a189987f977bb6e5fa073187abceb7e5f0cf`  
		Last Modified: Thu, 25 Jul 2024 19:07:43 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9515ec726a6d5e4c67aba5376b55ec8e44ded359a6c8fde8f8003be7dfd3dc5`  
		Last Modified: Thu, 25 Jul 2024 19:07:43 GMT  
		Size: 12.7 MB (12673367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6440b786c3d6737a9a28f7ee4373f024da452d2f8a4874164a21e56809970e0b`  
		Last Modified: Thu, 25 Jul 2024 20:10:51 GMT  
		Size: 234.5 MB (234540645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468205bc3496401939f90c6c7ba7b461679e0af5913b75d0746b3d6c754ad73a`  
		Last Modified: Thu, 25 Jul 2024 20:10:45 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.11` - unknown; unknown

```console
$ docker pull geonetwork@sha256:c14c673fb0a7d2e25a01e9f82dd3d234a6fa8a08c990472800ef1594fad6367f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ee72391e418cecf7f0dd3f5ba9dd69d51923f62dbecba9c44c340782e6dc4f`

```dockerfile
```

-	Layers:
	-	`sha256:d4d0a589fe0622103f9d9df49f9a493915ffa75372575ceb89ef11d837d99cf7`  
		Last Modified: Thu, 25 Jul 2024 20:10:46 GMT  
		Size: 4.3 MB (4305065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:948dda15e627d436862259ec981af9d32b043abe317f0c2958bb8d819eecea80`  
		Last Modified: Thu, 25 Jul 2024 20:10:45 GMT  
		Size: 19.2 KB (19240 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.11` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:dfa33b4015a4e19a8152b39461582b97f36c7ceb73fa73e952699f27aabea53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.4 MB (386357758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583282d5e8bed9e923c9a5af98d7536fccd8dfb18bbb2b797d62d32119e1814f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 02 Apr 2024 10:10:05 GMT
ARG RELEASE
# Tue, 02 Apr 2024 10:10:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 02 Apr 2024 10:10:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 02 Apr 2024 10:10:05 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 02 Apr 2024 10:10:05 GMT
ADD file:967120bb21c0fbaf9bf6c8fcb7b292d31ec4812e538714e8beb0a6e013eae873 in / 
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["/bin/bash"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Apr 2024 10:10:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Apr 2024 10:10:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Apr 2024 10:10:05 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Apr 2024 10:10:05 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_VERSION=9.0.91
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT []
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Apr 2024 10:10:05 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_VERSION=3.12.11
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_DOWNLOAD_MD5=2ece7076f05068e7a5270af03e32d632
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Apr 2024 10:10:05 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e180e7b68e21ed1490bb8293a3e848136812456d07f1be0783ef04f773a97867`  
		Last Modified: Fri, 28 Jun 2024 02:10:28 GMT  
		Size: 27.5 MB (27534011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3600b7820ccdab844af0b11c36a1aeadc460c5a3bc6a6fd0211a3fa9024fb1`  
		Last Modified: Tue, 02 Jul 2024 04:32:24 GMT  
		Size: 12.5 MB (12462968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2795f90fa7d600dee1f4eb73c08bb2d18123b06d13636002d46176c4b2f023f3`  
		Last Modified: Thu, 25 Jul 2024 18:01:01 GMT  
		Size: 99.2 MB (99249372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2c3b2a91fa20610bf53f9d0a722666976bbced1fddeabec3b2f1cafa30130f`  
		Last Modified: Thu, 25 Jul 2024 18:00:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4602dfe42d8b2b444328e0fb2b51ef2d074bcde8a413952b8269fe2bb2b489f6`  
		Last Modified: Thu, 25 Jul 2024 18:00:53 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc7d8efb5ef48317356561b1ec3b9b83a9949fd96d2effd6000c2a408fa0791`  
		Last Modified: Thu, 25 Jul 2024 19:39:25 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602497ca0baec3960eb142ca73787cbde70559ff89237b96f82118f2fb75a5c4`  
		Last Modified: Thu, 25 Jul 2024 19:39:26 GMT  
		Size: 12.6 MB (12580273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac5139b450dfef48663dd8c23544da8a664b35efe72d137db81ea058d954d98`  
		Last Modified: Thu, 25 Jul 2024 20:42:10 GMT  
		Size: 234.5 MB (234528624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bb4da193e005f20ee0f81ad66238a473fcfaa348f687c5513fb5743724f87c`  
		Last Modified: Thu, 25 Jul 2024 20:42:04 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.11` - unknown; unknown

```console
$ docker pull geonetwork@sha256:c1cafc419cefeb5e1963760100487607e34fdad3e2e76a1787b4ce4648250e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c07416149f052dac48b0c727d61ea78a21fafabc7bc53a3dc9f91e37fcc76e`

```dockerfile
```

-	Layers:
	-	`sha256:a73477235ccc024e29f5f46d1bf3d3275d01cb274168c89bff2a9efa5d9bf01c`  
		Last Modified: Thu, 25 Jul 2024 20:42:05 GMT  
		Size: 4.3 MB (4307783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63da1de726f860c2899727edc74c941c471fd1993452e6840962e7950f4e83fc`  
		Last Modified: Thu, 25 Jul 2024 20:42:04 GMT  
		Size: 19.5 KB (19453 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.11` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:13b65e11fead24599650ecf307cbcff09d7f5644911dc258886ff42711992cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.1 MB (391136969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14487c71572df86e40e6f00f0139cc42de2b5e90d547dfc3474924b10918680`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 02 Apr 2024 10:10:05 GMT
ARG RELEASE
# Tue, 02 Apr 2024 10:10:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 02 Apr 2024 10:10:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 02 Apr 2024 10:10:05 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 02 Apr 2024 10:10:05 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["/bin/bash"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Apr 2024 10:10:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Apr 2024 10:10:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Apr 2024 10:10:05 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Apr 2024 10:10:05 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_VERSION=9.0.91
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT []
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Apr 2024 10:10:05 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_VERSION=3.12.11
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_DOWNLOAD_MD5=2ece7076f05068e7a5270af03e32d632
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Apr 2024 10:10:05 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bdbc9eb1fb5990eb08fa9fe21450674d749b586acb5e75044993eaa173745d`  
		Last Modified: Tue, 02 Jul 2024 04:34:28 GMT  
		Size: 102.7 MB (102704169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2f56b637ad3ed974bf5d3f1b3963f194651c946391e4c9d1460693f56c8ea4`  
		Last Modified: Tue, 02 Jul 2024 04:34:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32dd5676062f79e6e7a076fdfd9b5dcd7f10701b1e7eb2cf21d1fece49f72190`  
		Last Modified: Tue, 02 Jul 2024 04:34:21 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af06264ab206fceff972cc63c64fadfac0dcc401e8dde9e30ede88067f01654`  
		Last Modified: Wed, 03 Jul 2024 01:00:18 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba539a524bb8cfa8b0c80f9c30f43f28d1dce4ea437dfc7fa7532ccd126336d`  
		Last Modified: Mon, 08 Jul 2024 23:14:30 GMT  
		Size: 12.7 MB (12679916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f62e239ce4eb896f669e74bc6c0dabb558fa52d23f61ff7c5d73b44e08a98a`  
		Last Modified: Tue, 09 Jul 2024 00:09:52 GMT  
		Size: 234.5 MB (234537412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42182b40f87b380bd51d17a491f660c27485c9d8375172d300419dfe824113dc`  
		Last Modified: Tue, 09 Jul 2024 00:09:47 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.11` - unknown; unknown

```console
$ docker pull geonetwork@sha256:77f0dee9efb464431027b94996ded1871353e61220cace8178c483a509b9b3a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4203325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4745721776422c6895ea7ed3ad26de2c0458a1bf53621b5209a87784e3099420`

```dockerfile
```

-	Layers:
	-	`sha256:49f0ee1781aa1d9573c08d54d4f6a0bf26fe793a4fd1c81e5b6091c60d6f0a80`  
		Last Modified: Tue, 09 Jul 2024 00:09:47 GMT  
		Size: 4.2 MB (4183567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1b2db8d722ed82eb4bfb595a82d293c16047c359b6f8fc016577f779a64e123`  
		Last Modified: Tue, 09 Jul 2024 00:09:46 GMT  
		Size: 19.8 KB (19758 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.11` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:033a62e86be2207bedf27147b18b9e26ee295ebdc15f5cc746d87da400543b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.7 MB (397687547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075470a2e23577cf42e19eaa98fb370bf886622fc4afe0bbcd4fdeb71c02452c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 02 Apr 2024 10:10:05 GMT
ARG RELEASE
# Tue, 02 Apr 2024 10:10:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 02 Apr 2024 10:10:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 02 Apr 2024 10:10:05 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 02 Apr 2024 10:10:05 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["/bin/bash"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Apr 2024 10:10:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Apr 2024 10:10:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Apr 2024 10:10:05 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Apr 2024 10:10:05 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_VERSION=9.0.91
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT []
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Apr 2024 10:10:05 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Apr 2024 10:10:05 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_VERSION=3.12.11
# Tue, 02 Apr 2024 10:10:05 GMT
ENV GN_DOWNLOAD_MD5=2ece7076f05068e7a5270af03e32d632
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Apr 2024 10:10:05 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Apr 2024 10:10:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Apr 2024 10:10:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Apr 2024 10:10:05 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea30364eff82eb5379f35c10575a54ece802a6af1763591c0a6a999d72c84c`  
		Last Modified: Tue, 02 Jul 2024 05:04:14 GMT  
		Size: 13.7 MB (13714876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e381362c15b6f2494c8dc0d6a49beef7efc7bbf6ef1d3525b485ba3969369d6`  
		Last Modified: Tue, 02 Jul 2024 05:04:20 GMT  
		Size: 101.1 MB (101071152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4281d6414726ffc097764a21c03524fe8ed573c02d19bd3c56d0826936af97`  
		Last Modified: Tue, 02 Jul 2024 05:04:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11783fbc96e3c2e66f3c1814d9e8373cf19165f9c928ff6cbb681bb165bc69`  
		Last Modified: Tue, 02 Jul 2024 05:04:10 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31c743457c728a8c3e7ee95c76c1377e5d565ec1c89fe0bb9d0d159720e638d`  
		Last Modified: Wed, 03 Jul 2024 03:11:39 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fa0eac1b9c12ff31977df71761642bb369421b2dac22518fb3c9e9fac6592e`  
		Last Modified: Tue, 09 Jul 2024 03:16:23 GMT  
		Size: 12.7 MB (12733450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13c17d5b897e7cbafe1cd653e47ffbd7654092838fffbd142c2d5ec73ffd4f5`  
		Last Modified: Tue, 09 Jul 2024 03:53:14 GMT  
		Size: 234.6 MB (234578369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef926e15ea7df92c844cbc8e5324900cb336963bb63e4109f686c13919f6454`  
		Last Modified: Tue, 09 Jul 2024 03:53:08 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.11` - unknown; unknown

```console
$ docker pull geonetwork@sha256:0b172a327d1eead97c93e61fcbb68c9a92c19a55516f96219bc154a40b5addb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4206260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ef40afbdc54787ed106e3706fd22eb277beca11ce81f6f3b0c7c3ce5a5285e`

```dockerfile
```

-	Layers:
	-	`sha256:1998d068e1335482a74240c25043fb96be8a0a01a6b25f24595350d8a48b13ec`  
		Last Modified: Tue, 09 Jul 2024 03:53:08 GMT  
		Size: 4.2 MB (4186837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62775d3bb2d87c2cbc0c4cfad35d549dfd125a15c7eec754e4b7a8a17b518a7b`  
		Last Modified: Tue, 09 Jul 2024 03:53:08 GMT  
		Size: 19.4 KB (19423 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12.11-postgres`

```console
$ docker pull geonetwork@sha256:cfdd3798fb4d7838cea9b9c81bc5dfac61276b0812bcef7840e6ef31bcf25a60
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

### `geonetwork:3.12.11-postgres` - linux; amd64

```console
$ docker pull geonetwork@sha256:024ec9ea5fd8563122d0ef89e1ac17d64034fe3f5709317c2261914ab8732169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.6 MB (407599616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e5dcc08f4ef5d057c612fa0453df3577a42ca7aca2fecd6fa545ad1d966cea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 05 Oct 2023 16:23:50 GMT
ARG RELEASE
# Thu, 05 Oct 2023 16:23:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 16:23:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 16:23:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 16:23:50 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["/bin/bash"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Oct 2023 16:23:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 16:23:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 16:23:50 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 05 Oct 2023 16:23:50 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_MAJOR=9
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_VERSION=9.0.91
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT []
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_FILE=geonetwork.war
# Thu, 05 Oct 2023 16:23:50 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_VERSION=3.12.11
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_DOWNLOAD_MD5=2ece7076f05068e7a5270af03e32d632
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 05 Oct 2023 16:23:50 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Oct 2023 16:23:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c055a91d57277ea410b92f9111e94845a0af82fef9cd5a097d9fbc848a91ce`  
		Last Modified: Tue, 02 Jul 2024 06:00:43 GMT  
		Size: 103.6 MB (103602292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b28fbf33e422d49b0808a16bed3bec227994163e4a31055a9bafd01c79f3bb4`  
		Last Modified: Tue, 02 Jul 2024 06:00:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0181c354541a8d59c19608901cbe6e45143749529d1dff48a049e5440b1a20e`  
		Last Modified: Tue, 02 Jul 2024 06:00:35 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b492ddc7448e8d14769b96b40b1a7dedb8c6a610871a0a6a192a6d8ff456d5`  
		Last Modified: Mon, 08 Jul 2024 22:57:12 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912d3997dd70072ace062d0c85a96473dec820953c29ce3885e5dd5285b6ab6d`  
		Last Modified: Mon, 08 Jul 2024 22:57:12 GMT  
		Size: 12.7 MB (12673408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1bf3a9a7265b6eb5d03aafa2eb8fd87e52bb1c4f0627be3a2b80027e158a14`  
		Last Modified: Mon, 08 Jul 2024 23:58:33 GMT  
		Size: 234.5 MB (234540666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2a16d137ccf1ed2c6bc1e0389f34d3d8d257c14b128591ebc1ed051b930ce8`  
		Last Modified: Mon, 08 Jul 2024 23:58:28 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8971503a390816828369a65b814e8287262c48f76f8139dce08e22ea21634efb`  
		Last Modified: Tue, 09 Jul 2024 00:50:17 GMT  
		Size: 13.5 MB (13467572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910568460b30e595e6d9ee224b52205e522226f25f5962a836e6ae97852a6ca9`  
		Last Modified: Tue, 09 Jul 2024 00:50:17 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3ce9c5aa0956081b5c94d576e14c3d0be980f7db26a5e998ebe14f41c67983`  
		Last Modified: Tue, 09 Jul 2024 00:50:17 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdac29bc2d3756b2a10e9019df63f157e1d83114aa8b48d5622919be4eea2bff`  
		Last Modified: Tue, 09 Jul 2024 00:50:17 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.11-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:6f6b8f65ebc6f1cf99f763751fda210eab2ce5135fd35b5d116acd7c9bcfb4bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5744280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ccda3d98e5098581c4c045386facdd58a48a962291cedd074b5e60ba6a6484`

```dockerfile
```

-	Layers:
	-	`sha256:d78b50653269f6583de5c2e6ec4e6c39e46ff2e7feca641d9159ce31c749f35c`  
		Last Modified: Tue, 09 Jul 2024 00:50:17 GMT  
		Size: 5.7 MB (5721186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5635ec5be40490e74843464e57a40506d45678d861fd3124bc6f17ad31d8c2fa`  
		Last Modified: Tue, 09 Jul 2024 00:50:17 GMT  
		Size: 23.1 KB (23094 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.11-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:013f9f72bace9e43a931259b9e76a10257fe8e30412a8130d8c1557df79de48d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.9 MB (398879312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca8cc3c9d511716c2475a88435ff98574994eb3dbbcdc03ce51dcd0a94fc1f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 05 Oct 2023 16:23:50 GMT
ARG RELEASE
# Thu, 05 Oct 2023 16:23:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 16:23:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 16:23:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 16:23:50 GMT
ADD file:967120bb21c0fbaf9bf6c8fcb7b292d31ec4812e538714e8beb0a6e013eae873 in / 
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["/bin/bash"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Oct 2023 16:23:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 16:23:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 16:23:50 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 05 Oct 2023 16:23:50 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_MAJOR=9
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_VERSION=9.0.91
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT []
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_FILE=geonetwork.war
# Thu, 05 Oct 2023 16:23:50 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_VERSION=3.12.11
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_DOWNLOAD_MD5=2ece7076f05068e7a5270af03e32d632
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 05 Oct 2023 16:23:50 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Oct 2023 16:23:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e180e7b68e21ed1490bb8293a3e848136812456d07f1be0783ef04f773a97867`  
		Last Modified: Fri, 28 Jun 2024 02:10:28 GMT  
		Size: 27.5 MB (27534011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3600b7820ccdab844af0b11c36a1aeadc460c5a3bc6a6fd0211a3fa9024fb1`  
		Last Modified: Tue, 02 Jul 2024 04:32:24 GMT  
		Size: 12.5 MB (12462968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2795f90fa7d600dee1f4eb73c08bb2d18123b06d13636002d46176c4b2f023f3`  
		Last Modified: Thu, 25 Jul 2024 18:01:01 GMT  
		Size: 99.2 MB (99249372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2c3b2a91fa20610bf53f9d0a722666976bbced1fddeabec3b2f1cafa30130f`  
		Last Modified: Thu, 25 Jul 2024 18:00:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4602dfe42d8b2b444328e0fb2b51ef2d074bcde8a413952b8269fe2bb2b489f6`  
		Last Modified: Thu, 25 Jul 2024 18:00:53 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc7d8efb5ef48317356561b1ec3b9b83a9949fd96d2effd6000c2a408fa0791`  
		Last Modified: Thu, 25 Jul 2024 19:39:25 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602497ca0baec3960eb142ca73787cbde70559ff89237b96f82118f2fb75a5c4`  
		Last Modified: Thu, 25 Jul 2024 19:39:26 GMT  
		Size: 12.6 MB (12580273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac5139b450dfef48663dd8c23544da8a664b35efe72d137db81ea058d954d98`  
		Last Modified: Thu, 25 Jul 2024 20:42:10 GMT  
		Size: 234.5 MB (234528624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bb4da193e005f20ee0f81ad66238a473fcfaa348f687c5513fb5743724f87c`  
		Last Modified: Thu, 25 Jul 2024 20:42:04 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b541313a436da0349679abac04d5f77b68cb760b11a3b9c5d88dd355fd440ecd`  
		Last Modified: Thu, 25 Jul 2024 21:10:28 GMT  
		Size: 12.5 MB (12518186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c3c2f48a99d82931e307f1121400e8d1f5287976d73abd5f658fac7ce1a634`  
		Last Modified: Thu, 25 Jul 2024 21:10:27 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3acbbb4c8ac2d53aba6f66f95fba3ed1beced6b4a3e9f50a7aa0c6ea0e5a4b`  
		Last Modified: Thu, 25 Jul 2024 21:10:27 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db94b23e5702419e945a895972dc76c4974d7555a372dbf0cf4ab5606162111`  
		Last Modified: Thu, 25 Jul 2024 21:10:28 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.11-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:68d15619bc7b40e433defa5c897f05a376eeb0789d98f8b275506283379da83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5869865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e886f6b54463b4564188a5456bbff19f0649860e5ca2fca86560d67f730f341`

```dockerfile
```

-	Layers:
	-	`sha256:ca7d53dbcb870c65c91d980f9eeca435ef11a5dfdae42e02b48035806d9fa9cb`  
		Last Modified: Thu, 25 Jul 2024 21:10:28 GMT  
		Size: 5.8 MB (5846540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e12eb1384ad3a67e613696cd412a8f37d801d8aee7d716d259d20b49641165c7`  
		Last Modified: Thu, 25 Jul 2024 21:10:27 GMT  
		Size: 23.3 KB (23325 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.11-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:bb15b59ce073e7beb94cd3362c9b3c94907ce68897a34b2744d53e74cfe42f6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.5 MB (404510393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed02e275091a7a87ed905bf8d425f3151c6cddcc7e955642fc990521f7b6f367`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 05 Oct 2023 16:23:50 GMT
ARG RELEASE
# Thu, 05 Oct 2023 16:23:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 16:23:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 16:23:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 16:23:50 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["/bin/bash"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Oct 2023 16:23:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 16:23:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 16:23:50 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 05 Oct 2023 16:23:50 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_MAJOR=9
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_VERSION=9.0.91
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT []
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_FILE=geonetwork.war
# Thu, 05 Oct 2023 16:23:50 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_VERSION=3.12.11
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_DOWNLOAD_MD5=2ece7076f05068e7a5270af03e32d632
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 05 Oct 2023 16:23:50 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Oct 2023 16:23:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bdbc9eb1fb5990eb08fa9fe21450674d749b586acb5e75044993eaa173745d`  
		Last Modified: Tue, 02 Jul 2024 04:34:28 GMT  
		Size: 102.7 MB (102704169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2f56b637ad3ed974bf5d3f1b3963f194651c946391e4c9d1460693f56c8ea4`  
		Last Modified: Tue, 02 Jul 2024 04:34:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32dd5676062f79e6e7a076fdfd9b5dcd7f10701b1e7eb2cf21d1fece49f72190`  
		Last Modified: Tue, 02 Jul 2024 04:34:21 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af06264ab206fceff972cc63c64fadfac0dcc401e8dde9e30ede88067f01654`  
		Last Modified: Wed, 03 Jul 2024 01:00:18 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba539a524bb8cfa8b0c80f9c30f43f28d1dce4ea437dfc7fa7532ccd126336d`  
		Last Modified: Mon, 08 Jul 2024 23:14:30 GMT  
		Size: 12.7 MB (12679916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f62e239ce4eb896f669e74bc6c0dabb558fa52d23f61ff7c5d73b44e08a98a`  
		Last Modified: Tue, 09 Jul 2024 00:09:52 GMT  
		Size: 234.5 MB (234537412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42182b40f87b380bd51d17a491f660c27485c9d8375172d300419dfe824113dc`  
		Last Modified: Tue, 09 Jul 2024 00:09:47 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25ff8819b17ec944cf30355e65267d44034ba3273eb940bad5a008e7c795c9f`  
		Last Modified: Tue, 09 Jul 2024 01:57:47 GMT  
		Size: 13.4 MB (13370057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ba217245e1864d7fb653be3f13fef42969bf5b4dbf5ec3cb6bbaadee5215c3`  
		Last Modified: Tue, 09 Jul 2024 01:57:46 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a1be51ff5967fcb43262c6d971f467af67c3e2eec45927cae0e991e584b3dc`  
		Last Modified: Tue, 09 Jul 2024 01:57:46 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6727609dd100bed1f7189137b9261d29709c279fe1f95fb24a399d67d86fab23`  
		Last Modified: Tue, 09 Jul 2024 01:57:46 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.11-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:7f6b36b1015d9c6d50dcb553a322e5bb3663bff249090d35c37a4ce87d637035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5751130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ff8968139067ebdc265342755f7ddb39fd0f7da73db49d6975ed774c1ea24d`

```dockerfile
```

-	Layers:
	-	`sha256:67e5142ae0cd517a5a2fd7756f9255fe17b9d55e36819af0484c2644c1879859`  
		Last Modified: Tue, 09 Jul 2024 01:57:46 GMT  
		Size: 5.7 MB (5727513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24296a82b40f353e5c46c56331e45aabaf90560b66a2fd685f97259a7104fcf1`  
		Last Modified: Tue, 09 Jul 2024 01:57:46 GMT  
		Size: 23.6 KB (23617 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.11-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:a0dba107172c948963611fe989c87312a7364c115b35e0c2181539acb22e683e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.7 MB (411651843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700381a7f3406d736114ab55265f546c57147a684678b7d1ce8751d89fa72aa6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 05 Oct 2023 16:23:50 GMT
ARG RELEASE
# Thu, 05 Oct 2023 16:23:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 16:23:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 16:23:50 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 16:23:50 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["/bin/bash"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Oct 2023 16:23:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 16:23:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 16:23:50 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 05 Oct 2023 16:23:50 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_MAJOR=9
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_VERSION=9.0.91
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT []
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_FILE=geonetwork.war
# Thu, 05 Oct 2023 16:23:50 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 05 Oct 2023 16:23:50 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_VERSION=3.12.11
# Thu, 05 Oct 2023 16:23:50 GMT
ENV GN_DOWNLOAD_MD5=2ece7076f05068e7a5270af03e32d632
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 05 Oct 2023 16:23:50 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
# Thu, 05 Oct 2023 16:23:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Oct 2023 16:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Oct 2023 16:23:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea30364eff82eb5379f35c10575a54ece802a6af1763591c0a6a999d72c84c`  
		Last Modified: Tue, 02 Jul 2024 05:04:14 GMT  
		Size: 13.7 MB (13714876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e381362c15b6f2494c8dc0d6a49beef7efc7bbf6ef1d3525b485ba3969369d6`  
		Last Modified: Tue, 02 Jul 2024 05:04:20 GMT  
		Size: 101.1 MB (101071152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4281d6414726ffc097764a21c03524fe8ed573c02d19bd3c56d0826936af97`  
		Last Modified: Tue, 02 Jul 2024 05:04:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee11783fbc96e3c2e66f3c1814d9e8373cf19165f9c928ff6cbb681bb165bc69`  
		Last Modified: Tue, 02 Jul 2024 05:04:10 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31c743457c728a8c3e7ee95c76c1377e5d565ec1c89fe0bb9d0d159720e638d`  
		Last Modified: Wed, 03 Jul 2024 03:11:39 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fa0eac1b9c12ff31977df71761642bb369421b2dac22518fb3c9e9fac6592e`  
		Last Modified: Tue, 09 Jul 2024 03:16:23 GMT  
		Size: 12.7 MB (12733450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13c17d5b897e7cbafe1cd653e47ffbd7654092838fffbd142c2d5ec73ffd4f5`  
		Last Modified: Tue, 09 Jul 2024 03:53:14 GMT  
		Size: 234.6 MB (234578369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef926e15ea7df92c844cbc8e5324900cb336963bb63e4109f686c13919f6454`  
		Last Modified: Tue, 09 Jul 2024 03:53:08 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf3bad02a93d9e1c8bdf5974977b13d9cae8fe883e58df336468307204aeced`  
		Last Modified: Tue, 09 Jul 2024 04:49:32 GMT  
		Size: 14.0 MB (13960926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630fd7156ec9036ba7309fd4e1c9d8e27858528ca3b9353b4706818cbd1961ea`  
		Last Modified: Tue, 09 Jul 2024 04:49:32 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f42b03fa32f1fd947fb87f98a583bf1a97f119bbcf37b6b5c12e0629d14386`  
		Last Modified: Tue, 09 Jul 2024 04:49:32 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff554c409056d1c68ed9adcb987cd0c8c00a32314ba78729fad6ff3b363356b`  
		Last Modified: Tue, 09 Jul 2024 04:49:32 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.11-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:fb6b03452b517abae90bbb0a349508610fc19453276a4be4df78893a360b5d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5750724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb451ed13aa884e07a56fae9db013ef0795a87177b196787887e6d8d2cdd0307`

```dockerfile
```

-	Layers:
	-	`sha256:88031456e061ff86ae7980a0ba7a57e06524382661aafad108aaf67929d97989`  
		Last Modified: Tue, 09 Jul 2024 04:49:32 GMT  
		Size: 5.7 MB (5727440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dea8fac5f7466ef12f55a0f5e7fc323598cbc24024b2fca8c77407d63413821e`  
		Last Modified: Tue, 09 Jul 2024 04:49:32 GMT  
		Size: 23.3 KB (23284 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4`

```console
$ docker pull geonetwork@sha256:93b389c9bf911b8578e1f0d8172e9d98f18ea1a77cdbde4668374d8af996eead
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:4` - linux; amd64

```console
$ docker pull geonetwork@sha256:b065add9cac399306d4b10b2ab818c059ea90fa78410e77d596b042d59b8a2c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.4 MB (488369319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7425dde07a9dee83d967d85d4db4370c49c969bbb6833b89c2d3cd80c03f8fe2`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Jun 2024 10:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:58:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='9d14a076d1440161ab4c9736644e8e9f4719eb8e9f44c03470640960c3cd5e00';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["jshell"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_VERSION=9.4.55.v20240627
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.55.v20240627/jetty-home-9.4.55.v20240627.tar.gz
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
WORKDIR /var/lib/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
USER jetty
# Tue, 18 Jun 2024 10:58:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 18 Jun 2024 10:58:54 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 18 Jun 2024 10:58:54 GMT
USER root
# Tue, 18 Jun 2024 10:58:54 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
USER jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_FILE=geonetwork.war
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_VERSION=4.4.5
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_DOWNLOAD_MD5=a7b04339041e1e8217435dc6273ac3b8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:58:54 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b454cd6d22f196b273f4ba330e473a91645ea8875a5a19fec9e095a3339aa2`  
		Last Modified: Wed, 24 Jul 2024 01:26:45 GMT  
		Size: 145.6 MB (145557968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f732ae9cdf4c8bf8cf47997726fe1f9d004cc3a94de7e1a66814cd84c15689f3`  
		Last Modified: Wed, 24 Jul 2024 01:26:34 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3259d4aad21fdb59205afd139d7cd63465836f6c003b7831821416d37f350771`  
		Last Modified: Thu, 25 Jul 2024 17:28:14 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d116df1c047e785f473acc1191d11f21ba2211020d5233171cf0d3d989e8e02f`  
		Last Modified: Thu, 25 Jul 2024 19:03:54 GMT  
		Size: 10.3 MB (10293140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858122808ab087e1e296cf0c734f7a0479220652e06c8c80ab821de887dff250`  
		Last Modified: Thu, 25 Jul 2024 19:03:34 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404938076bb48bccbc7bb4423021e94939954cbf1b17e12f7e7b8198a342301f`  
		Last Modified: Thu, 25 Jul 2024 20:10:08 GMT  
		Size: 245.2 KB (245169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d79a6ee5a0348aedaa8c10e567b40f7618ac822c01fe3413d2a51a1b172683`  
		Last Modified: Thu, 25 Jul 2024 20:10:14 GMT  
		Size: 286.8 MB (286763079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb5c1c984257d5118bae3a2ca43a15816c6d059f3ad581a74d480dcbee66a6b`  
		Last Modified: Thu, 25 Jul 2024 20:10:07 GMT  
		Size: 552.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b224130970b3f8a41ba8311b9ea67b17e37ac8ec00bc7f65cbdcb9da09ab0b`  
		Last Modified: Thu, 25 Jul 2024 20:10:07 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fd7fff663d2e9761e61bf90a707e080f3c2a425a8804a2714a37aeb85b12dc`  
		Last Modified: Thu, 25 Jul 2024 20:10:08 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:1a4c9feec825fd3197d640705400b15f4b2f18daa9c273d59a26b958f2affca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1948d4d6ca08ebb109d51cda89a09d0f5f63e6f1e147b772f76581c4e68d1893`

```dockerfile
```

-	Layers:
	-	`sha256:fc792c619a19eccee7640a03950bdaefeed8c382235a2559d10ba7cb31ca173a`  
		Last Modified: Thu, 25 Jul 2024 20:10:08 GMT  
		Size: 4.3 MB (4299246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6d955e812a11c739073e859b47052a91ce55389e46417049f801aeee59e90cd`  
		Last Modified: Thu, 25 Jul 2024 20:10:07 GMT  
		Size: 25.7 KB (25666 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:b5fff45972ac86cb708f2fae175b3b7c51205da0fbfeae267f337989ed9f4848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.6 MB (483647932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eceb7a0fea170f2114b4493287b28564426822dad4958ee91a3b6d3cdf7c3f89`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Jun 2024 10:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:58:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='9d14a076d1440161ab4c9736644e8e9f4719eb8e9f44c03470640960c3cd5e00';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["jshell"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_VERSION=9.4.55.v20240627
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.55.v20240627/jetty-home-9.4.55.v20240627.tar.gz
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
WORKDIR /var/lib/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
USER jetty
# Tue, 18 Jun 2024 10:58:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 18 Jun 2024 10:58:54 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 18 Jun 2024 10:58:54 GMT
USER root
# Tue, 18 Jun 2024 10:58:54 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
USER jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_FILE=geonetwork.war
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_VERSION=4.4.5
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_DOWNLOAD_MD5=a7b04339041e1e8217435dc6273ac3b8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:58:54 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f56fba665802b80660e75f0b84fbae178f7fa6d018e7d035229b396f302fb9`  
		Last Modified: Wed, 24 Jul 2024 00:50:30 GMT  
		Size: 142.4 MB (142361214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf0192e7fcc5bca3ccff402f57c857e0db1d000ecf4d3dc36981fe770113260`  
		Last Modified: Wed, 24 Jul 2024 00:50:21 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3beccd94eafe3dbf394edd5c06f9d458d9a4e96ab895d94308d7c602f7b6d2a8`  
		Last Modified: Wed, 24 Jul 2024 00:50:21 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b30dc2e43b3a42ccebd408a81ed512669a2387eeba908741d087e0b902f8a7f`  
		Last Modified: Wed, 24 Jul 2024 15:43:35 GMT  
		Size: 10.3 MB (10293048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13600aa53b0b178fcc3c1c1efd706cbe98ca53ee021ad3ce3ae6596cae6640f5`  
		Last Modified: Wed, 24 Jul 2024 15:43:34 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eed90cc0147451a7e0512afa409f2119c5380c38d1d3036d732e7fa7ce61b8e`  
		Last Modified: Wed, 24 Jul 2024 18:08:45 GMT  
		Size: 243.8 KB (243816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96200bc41e80059deca60d8beed6021c0bb057079bd12856dbb13552e57f7ea`  
		Last Modified: Wed, 24 Jul 2024 18:08:52 GMT  
		Size: 286.8 MB (286763094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222ea95c4ba35a2665d368505d027872dd9cc82bd1a5db0f5f92031b395528e8`  
		Last Modified: Wed, 24 Jul 2024 18:08:45 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f236d2a5b5399aa2455f285ee99f000e435aceb763a1c86883038c3bb1b9140a`  
		Last Modified: Wed, 24 Jul 2024 18:08:45 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fef65f78c950f6dabe4b7d74d1fd92055eda42218475cff541313322c6c737`  
		Last Modified: Wed, 24 Jul 2024 18:08:46 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:0a9aad022c0e71771b68cd0d369df909510a58cccfe703d45ac95d49e3c0d797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4325749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548c42540f2d5b07ee0814b463649bd1379f7f0f2e9f101aeb3a2fe232cca1b2`

```dockerfile
```

-	Layers:
	-	`sha256:89127bbc4afd4c7545670ad764ce2e24f28ec414835c56fcf53f3a7c04be637b`  
		Last Modified: Wed, 24 Jul 2024 18:08:46 GMT  
		Size: 4.3 MB (4299518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86a8fb7ca725331483ad8f03c4078271b5d8eccb1608da07cbbdf8e6d2841149`  
		Last Modified: Wed, 24 Jul 2024 18:08:45 GMT  
		Size: 26.2 KB (26231 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.2`

```console
$ docker pull geonetwork@sha256:fc138c6fef8b07291753b0f5a197941f99f3a6602ad3e51aa3cd4bf346ffd271
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:4.2` - linux; amd64

```console
$ docker pull geonetwork@sha256:4f4bcd3f9c919653f956ebad6f77d857e55ea04d751d5632cc3c63e775dadc7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.6 MB (461598224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8960ef60d311f7103669f278373c8c62449c35f2e3092f166ae6ee9ddb942cb8`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Jun 2024 10:47:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:47:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Jun 2024 10:47:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 18 Jun 2024 10:47:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JETTY_VERSION=9.4.55.v20240627
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 18 Jun 2024 10:47:09 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 18 Jun 2024 10:47:09 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.55.v20240627/jetty-home-9.4.55.v20240627.tar.gz
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 18 Jun 2024 10:47:09 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
WORKDIR /var/lib/jetty
# Tue, 18 Jun 2024 10:47:09 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
USER jetty
# Tue, 18 Jun 2024 10:47:09 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Jun 2024 10:47:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 10:47:09 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:47:09 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Tue, 18 Jun 2024 10:47:09 GMT
USER root
# Tue, 18 Jun 2024 10:47:09 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
USER jetty
# Tue, 18 Jun 2024 10:47:09 GMT
ENV GN_FILE=geonetwork.war
# Tue, 18 Jun 2024 10:47:09 GMT
ENV GN_VERSION=4.2.10
# Tue, 18 Jun 2024 10:47:09 GMT
ENV GN_DOWNLOAD_MD5=0f33998c61e7cf74de6bb5e451a571b3
# Tue, 18 Jun 2024 10:47:09 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 18 Jun 2024 10:47:09 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:47:09 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f274f6e1f69ef18d099ee66827af3d6783d2120b5d02547f94bfec5f6fa2f4`  
		Last Modified: Thu, 25 Jul 2024 17:25:53 GMT  
		Size: 103.6 MB (103616399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a56635dbb609a02dd216e84ee05912ce18e6a5a9ba41ee5bfd4fad47cddc962`  
		Last Modified: Thu, 25 Jul 2024 17:25:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a527d6107057448adfc284ec848797e1d30fa192bf0d8394679d1ed1a82dff58`  
		Last Modified: Thu, 25 Jul 2024 17:25:37 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09445e04d06a9bf479dfba57c8249b2a9802f00d07d89ab00060fb350dded4ec`  
		Last Modified: Thu, 25 Jul 2024 19:07:16 GMT  
		Size: 10.3 MB (10292270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95691ad2d31d8f25e9c90c67d48ed61c3f378f7ab237b7cd5dc38496152c96f`  
		Last Modified: Thu, 25 Jul 2024 19:07:14 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016f3552c1735b4eeea45f467c58881160473e0c89c942a3d2efab88f0826076`  
		Last Modified: Thu, 25 Jul 2024 20:10:38 GMT  
		Size: 245.2 KB (245246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e915b6fddfc15659bba67ee78dfaeb2cf292ad070be5acfa822aa246be712cd5`  
		Last Modified: Thu, 25 Jul 2024 20:10:43 GMT  
		Size: 301.9 MB (301934686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b502fed5021565466c1b3a129bbba76fb8f509c910536739b05d25d683cefee`  
		Last Modified: Thu, 25 Jul 2024 20:10:38 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2` - unknown; unknown

```console
$ docker pull geonetwork@sha256:a805b4f171c4fa46802a56003067cde197181df12a49c62eb9e02eeedb9bc363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4499943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a70219525f7fd23639abf952d533e31e91195ea44a22fad46001d5a2a8c0e2`

```dockerfile
```

-	Layers:
	-	`sha256:d26aab571981668280e98e96bf36ff7956c8fa661e688d7b68b6f6c93f201ae6`  
		Last Modified: Thu, 25 Jul 2024 20:10:38 GMT  
		Size: 4.5 MB (4481261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c1351e2ca212fd6230da57069a251a8198cffbcff770d2b2d47c4b83f56f473`  
		Last Modified: Thu, 25 Jul 2024 20:10:38 GMT  
		Size: 18.7 KB (18682 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.2` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:0d9a0ca42abb8404419325c2a51bda2803bdc535762d649ce710eb77c98e115c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.2 MB (459161514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e212a519df4be148952d32776b9a2bc50bb7d9505580f10ac200114043ec5c`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JETTY_VERSION=9.4.55.v20240627
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 18 Jun 2024 10:47:09 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 18 Jun 2024 10:47:09 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.55.v20240627/jetty-home-9.4.55.v20240627.tar.gz
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 18 Jun 2024 10:47:09 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
WORKDIR /var/lib/jetty
# Tue, 18 Jun 2024 10:47:09 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
USER jetty
# Tue, 18 Jun 2024 10:47:09 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Jun 2024 10:47:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 10:47:09 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:47:09 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Tue, 18 Jun 2024 10:47:09 GMT
USER root
# Tue, 18 Jun 2024 10:47:09 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
USER jetty
# Tue, 18 Jun 2024 10:47:09 GMT
ENV GN_FILE=geonetwork.war
# Tue, 18 Jun 2024 10:47:09 GMT
ENV GN_VERSION=4.2.10
# Tue, 18 Jun 2024 10:47:09 GMT
ENV GN_DOWNLOAD_MD5=0f33998c61e7cf74de6bb5e451a571b3
# Tue, 18 Jun 2024 10:47:09 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 18 Jun 2024 10:47:09 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:47:09 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadd77454831bce505039d08a5c372d808b3443f601c4557f162af530201df18`  
		Last Modified: Wed, 05 Jun 2024 04:54:50 GMT  
		Size: 102.7 MB (102704998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d137067f35ba71b6314ae47cc286089738597349af237e5d830e37f641fa16af`  
		Last Modified: Wed, 05 Jun 2024 04:54:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f6368d49af04d54ffec7f6dbbf4aa20deacf4710ff44c614be17af4762a154`  
		Last Modified: Wed, 05 Jun 2024 04:54:44 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ef90ebde951d2db3df62db42d4897f6280f42a56875b5b7e5cb900af388b5d`  
		Last Modified: Mon, 08 Jul 2024 18:09:34 GMT  
		Size: 10.3 MB (10292183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4484d3d29dbe8a5eab95bfea21755a4d0a6aba47f132885eef81bda672248896`  
		Last Modified: Mon, 08 Jul 2024 18:09:33 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ece742d7fa9d40c2d41bf60a886bc4a11d056faded7443035dddeb602f7c0b6`  
		Last Modified: Mon, 08 Jul 2024 19:33:01 GMT  
		Size: 243.9 KB (243933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a582a476433a5ada4649b758f73db0bdb63e9ab33c822fe85c717ef00634dd`  
		Last Modified: Mon, 08 Jul 2024 19:33:07 GMT  
		Size: 301.9 MB (301934679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0820a534f5fb8f81cde25785d3b3a8fed15d0d1b59b3456bf89910270d50f508`  
		Last Modified: Mon, 08 Jul 2024 19:33:01 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2` - unknown; unknown

```console
$ docker pull geonetwork@sha256:99f75d39e4e1d58dac90d4651c27d40fa739a15984a556db27976837adf8543e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4358196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f42d2058c28204ab00aed8054540b1198d9b0184de231e26a3b68bf03ab5e0`

```dockerfile
```

-	Layers:
	-	`sha256:fe8e1baa92cc76b19db52afcbccab0f41432705a5794fbbb6fb70aa278020ea9`  
		Last Modified: Mon, 08 Jul 2024 19:33:01 GMT  
		Size: 4.3 MB (4339037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09f83df4132807ca378e0fba236357e1b854559b52ad20cb5a0989114e2f32e8`  
		Last Modified: Mon, 08 Jul 2024 19:33:00 GMT  
		Size: 19.2 KB (19159 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.2.10`

```console
$ docker pull geonetwork@sha256:fc138c6fef8b07291753b0f5a197941f99f3a6602ad3e51aa3cd4bf346ffd271
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:4.2.10` - linux; amd64

```console
$ docker pull geonetwork@sha256:4f4bcd3f9c919653f956ebad6f77d857e55ea04d751d5632cc3c63e775dadc7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.6 MB (461598224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8960ef60d311f7103669f278373c8c62449c35f2e3092f166ae6ee9ddb942cb8`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Jun 2024 10:47:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:47:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Jun 2024 10:47:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 18 Jun 2024 10:47:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JETTY_VERSION=9.4.55.v20240627
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 18 Jun 2024 10:47:09 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 18 Jun 2024 10:47:09 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.55.v20240627/jetty-home-9.4.55.v20240627.tar.gz
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 18 Jun 2024 10:47:09 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
WORKDIR /var/lib/jetty
# Tue, 18 Jun 2024 10:47:09 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
USER jetty
# Tue, 18 Jun 2024 10:47:09 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Jun 2024 10:47:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 10:47:09 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:47:09 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Tue, 18 Jun 2024 10:47:09 GMT
USER root
# Tue, 18 Jun 2024 10:47:09 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
USER jetty
# Tue, 18 Jun 2024 10:47:09 GMT
ENV GN_FILE=geonetwork.war
# Tue, 18 Jun 2024 10:47:09 GMT
ENV GN_VERSION=4.2.10
# Tue, 18 Jun 2024 10:47:09 GMT
ENV GN_DOWNLOAD_MD5=0f33998c61e7cf74de6bb5e451a571b3
# Tue, 18 Jun 2024 10:47:09 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 18 Jun 2024 10:47:09 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:47:09 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f274f6e1f69ef18d099ee66827af3d6783d2120b5d02547f94bfec5f6fa2f4`  
		Last Modified: Thu, 25 Jul 2024 17:25:53 GMT  
		Size: 103.6 MB (103616399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a56635dbb609a02dd216e84ee05912ce18e6a5a9ba41ee5bfd4fad47cddc962`  
		Last Modified: Thu, 25 Jul 2024 17:25:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a527d6107057448adfc284ec848797e1d30fa192bf0d8394679d1ed1a82dff58`  
		Last Modified: Thu, 25 Jul 2024 17:25:37 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09445e04d06a9bf479dfba57c8249b2a9802f00d07d89ab00060fb350dded4ec`  
		Last Modified: Thu, 25 Jul 2024 19:07:16 GMT  
		Size: 10.3 MB (10292270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95691ad2d31d8f25e9c90c67d48ed61c3f378f7ab237b7cd5dc38496152c96f`  
		Last Modified: Thu, 25 Jul 2024 19:07:14 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016f3552c1735b4eeea45f467c58881160473e0c89c942a3d2efab88f0826076`  
		Last Modified: Thu, 25 Jul 2024 20:10:38 GMT  
		Size: 245.2 KB (245246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e915b6fddfc15659bba67ee78dfaeb2cf292ad070be5acfa822aa246be712cd5`  
		Last Modified: Thu, 25 Jul 2024 20:10:43 GMT  
		Size: 301.9 MB (301934686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b502fed5021565466c1b3a129bbba76fb8f509c910536739b05d25d683cefee`  
		Last Modified: Thu, 25 Jul 2024 20:10:38 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2.10` - unknown; unknown

```console
$ docker pull geonetwork@sha256:a805b4f171c4fa46802a56003067cde197181df12a49c62eb9e02eeedb9bc363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4499943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a70219525f7fd23639abf952d533e31e91195ea44a22fad46001d5a2a8c0e2`

```dockerfile
```

-	Layers:
	-	`sha256:d26aab571981668280e98e96bf36ff7956c8fa661e688d7b68b6f6c93f201ae6`  
		Last Modified: Thu, 25 Jul 2024 20:10:38 GMT  
		Size: 4.5 MB (4481261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c1351e2ca212fd6230da57069a251a8198cffbcff770d2b2d47c4b83f56f473`  
		Last Modified: Thu, 25 Jul 2024 20:10:38 GMT  
		Size: 18.7 KB (18682 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.2.10` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:0d9a0ca42abb8404419325c2a51bda2803bdc535762d649ce710eb77c98e115c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.2 MB (459161514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e212a519df4be148952d32776b9a2bc50bb7d9505580f10ac200114043ec5c`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JETTY_VERSION=9.4.55.v20240627
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 18 Jun 2024 10:47:09 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 18 Jun 2024 10:47:09 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.55.v20240627/jetty-home-9.4.55.v20240627.tar.gz
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 18 Jun 2024 10:47:09 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
WORKDIR /var/lib/jetty
# Tue, 18 Jun 2024 10:47:09 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
USER jetty
# Tue, 18 Jun 2024 10:47:09 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Jun 2024 10:47:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 10:47:09 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:47:09 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 18 Jun 2024 10:47:09 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Tue, 18 Jun 2024 10:47:09 GMT
USER root
# Tue, 18 Jun 2024 10:47:09 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
USER jetty
# Tue, 18 Jun 2024 10:47:09 GMT
ENV GN_FILE=geonetwork.war
# Tue, 18 Jun 2024 10:47:09 GMT
ENV GN_VERSION=4.2.10
# Tue, 18 Jun 2024 10:47:09 GMT
ENV GN_DOWNLOAD_MD5=0f33998c61e7cf74de6bb5e451a571b3
# Tue, 18 Jun 2024 10:47:09 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:47:09 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 18 Jun 2024 10:47:09 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:47:09 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadd77454831bce505039d08a5c372d808b3443f601c4557f162af530201df18`  
		Last Modified: Wed, 05 Jun 2024 04:54:50 GMT  
		Size: 102.7 MB (102704998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d137067f35ba71b6314ae47cc286089738597349af237e5d830e37f641fa16af`  
		Last Modified: Wed, 05 Jun 2024 04:54:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f6368d49af04d54ffec7f6dbbf4aa20deacf4710ff44c614be17af4762a154`  
		Last Modified: Wed, 05 Jun 2024 04:54:44 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ef90ebde951d2db3df62db42d4897f6280f42a56875b5b7e5cb900af388b5d`  
		Last Modified: Mon, 08 Jul 2024 18:09:34 GMT  
		Size: 10.3 MB (10292183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4484d3d29dbe8a5eab95bfea21755a4d0a6aba47f132885eef81bda672248896`  
		Last Modified: Mon, 08 Jul 2024 18:09:33 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ece742d7fa9d40c2d41bf60a886bc4a11d056faded7443035dddeb602f7c0b6`  
		Last Modified: Mon, 08 Jul 2024 19:33:01 GMT  
		Size: 243.9 KB (243933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a582a476433a5ada4649b758f73db0bdb63e9ab33c822fe85c717ef00634dd`  
		Last Modified: Mon, 08 Jul 2024 19:33:07 GMT  
		Size: 301.9 MB (301934679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0820a534f5fb8f81cde25785d3b3a8fed15d0d1b59b3456bf89910270d50f508`  
		Last Modified: Mon, 08 Jul 2024 19:33:01 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2.10` - unknown; unknown

```console
$ docker pull geonetwork@sha256:99f75d39e4e1d58dac90d4651c27d40fa739a15984a556db27976837adf8543e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4358196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f42d2058c28204ab00aed8054540b1198d9b0184de231e26a3b68bf03ab5e0`

```dockerfile
```

-	Layers:
	-	`sha256:fe8e1baa92cc76b19db52afcbccab0f41432705a5794fbbb6fb70aa278020ea9`  
		Last Modified: Mon, 08 Jul 2024 19:33:01 GMT  
		Size: 4.3 MB (4339037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09f83df4132807ca378e0fba236357e1b854559b52ad20cb5a0989114e2f32e8`  
		Last Modified: Mon, 08 Jul 2024 19:33:00 GMT  
		Size: 19.2 KB (19159 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.4`

```console
$ docker pull geonetwork@sha256:93b389c9bf911b8578e1f0d8172e9d98f18ea1a77cdbde4668374d8af996eead
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:4.4` - linux; amd64

```console
$ docker pull geonetwork@sha256:b065add9cac399306d4b10b2ab818c059ea90fa78410e77d596b042d59b8a2c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.4 MB (488369319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7425dde07a9dee83d967d85d4db4370c49c969bbb6833b89c2d3cd80c03f8fe2`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Jun 2024 10:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:58:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='9d14a076d1440161ab4c9736644e8e9f4719eb8e9f44c03470640960c3cd5e00';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["jshell"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_VERSION=9.4.55.v20240627
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.55.v20240627/jetty-home-9.4.55.v20240627.tar.gz
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
WORKDIR /var/lib/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
USER jetty
# Tue, 18 Jun 2024 10:58:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 18 Jun 2024 10:58:54 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 18 Jun 2024 10:58:54 GMT
USER root
# Tue, 18 Jun 2024 10:58:54 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
USER jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_FILE=geonetwork.war
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_VERSION=4.4.5
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_DOWNLOAD_MD5=a7b04339041e1e8217435dc6273ac3b8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:58:54 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b454cd6d22f196b273f4ba330e473a91645ea8875a5a19fec9e095a3339aa2`  
		Last Modified: Wed, 24 Jul 2024 01:26:45 GMT  
		Size: 145.6 MB (145557968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f732ae9cdf4c8bf8cf47997726fe1f9d004cc3a94de7e1a66814cd84c15689f3`  
		Last Modified: Wed, 24 Jul 2024 01:26:34 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3259d4aad21fdb59205afd139d7cd63465836f6c003b7831821416d37f350771`  
		Last Modified: Thu, 25 Jul 2024 17:28:14 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d116df1c047e785f473acc1191d11f21ba2211020d5233171cf0d3d989e8e02f`  
		Last Modified: Thu, 25 Jul 2024 19:03:54 GMT  
		Size: 10.3 MB (10293140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858122808ab087e1e296cf0c734f7a0479220652e06c8c80ab821de887dff250`  
		Last Modified: Thu, 25 Jul 2024 19:03:34 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404938076bb48bccbc7bb4423021e94939954cbf1b17e12f7e7b8198a342301f`  
		Last Modified: Thu, 25 Jul 2024 20:10:08 GMT  
		Size: 245.2 KB (245169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d79a6ee5a0348aedaa8c10e567b40f7618ac822c01fe3413d2a51a1b172683`  
		Last Modified: Thu, 25 Jul 2024 20:10:14 GMT  
		Size: 286.8 MB (286763079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb5c1c984257d5118bae3a2ca43a15816c6d059f3ad581a74d480dcbee66a6b`  
		Last Modified: Thu, 25 Jul 2024 20:10:07 GMT  
		Size: 552.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b224130970b3f8a41ba8311b9ea67b17e37ac8ec00bc7f65cbdcb9da09ab0b`  
		Last Modified: Thu, 25 Jul 2024 20:10:07 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fd7fff663d2e9761e61bf90a707e080f3c2a425a8804a2714a37aeb85b12dc`  
		Last Modified: Thu, 25 Jul 2024 20:10:08 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:1a4c9feec825fd3197d640705400b15f4b2f18daa9c273d59a26b958f2affca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1948d4d6ca08ebb109d51cda89a09d0f5f63e6f1e147b772f76581c4e68d1893`

```dockerfile
```

-	Layers:
	-	`sha256:fc792c619a19eccee7640a03950bdaefeed8c382235a2559d10ba7cb31ca173a`  
		Last Modified: Thu, 25 Jul 2024 20:10:08 GMT  
		Size: 4.3 MB (4299246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6d955e812a11c739073e859b47052a91ce55389e46417049f801aeee59e90cd`  
		Last Modified: Thu, 25 Jul 2024 20:10:07 GMT  
		Size: 25.7 KB (25666 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:b5fff45972ac86cb708f2fae175b3b7c51205da0fbfeae267f337989ed9f4848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.6 MB (483647932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eceb7a0fea170f2114b4493287b28564426822dad4958ee91a3b6d3cdf7c3f89`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Jun 2024 10:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:58:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='9d14a076d1440161ab4c9736644e8e9f4719eb8e9f44c03470640960c3cd5e00';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["jshell"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_VERSION=9.4.55.v20240627
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.55.v20240627/jetty-home-9.4.55.v20240627.tar.gz
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
WORKDIR /var/lib/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
USER jetty
# Tue, 18 Jun 2024 10:58:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 18 Jun 2024 10:58:54 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 18 Jun 2024 10:58:54 GMT
USER root
# Tue, 18 Jun 2024 10:58:54 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
USER jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_FILE=geonetwork.war
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_VERSION=4.4.5
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_DOWNLOAD_MD5=a7b04339041e1e8217435dc6273ac3b8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:58:54 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f56fba665802b80660e75f0b84fbae178f7fa6d018e7d035229b396f302fb9`  
		Last Modified: Wed, 24 Jul 2024 00:50:30 GMT  
		Size: 142.4 MB (142361214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf0192e7fcc5bca3ccff402f57c857e0db1d000ecf4d3dc36981fe770113260`  
		Last Modified: Wed, 24 Jul 2024 00:50:21 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3beccd94eafe3dbf394edd5c06f9d458d9a4e96ab895d94308d7c602f7b6d2a8`  
		Last Modified: Wed, 24 Jul 2024 00:50:21 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b30dc2e43b3a42ccebd408a81ed512669a2387eeba908741d087e0b902f8a7f`  
		Last Modified: Wed, 24 Jul 2024 15:43:35 GMT  
		Size: 10.3 MB (10293048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13600aa53b0b178fcc3c1c1efd706cbe98ca53ee021ad3ce3ae6596cae6640f5`  
		Last Modified: Wed, 24 Jul 2024 15:43:34 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eed90cc0147451a7e0512afa409f2119c5380c38d1d3036d732e7fa7ce61b8e`  
		Last Modified: Wed, 24 Jul 2024 18:08:45 GMT  
		Size: 243.8 KB (243816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96200bc41e80059deca60d8beed6021c0bb057079bd12856dbb13552e57f7ea`  
		Last Modified: Wed, 24 Jul 2024 18:08:52 GMT  
		Size: 286.8 MB (286763094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222ea95c4ba35a2665d368505d027872dd9cc82bd1a5db0f5f92031b395528e8`  
		Last Modified: Wed, 24 Jul 2024 18:08:45 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f236d2a5b5399aa2455f285ee99f000e435aceb763a1c86883038c3bb1b9140a`  
		Last Modified: Wed, 24 Jul 2024 18:08:45 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fef65f78c950f6dabe4b7d74d1fd92055eda42218475cff541313322c6c737`  
		Last Modified: Wed, 24 Jul 2024 18:08:46 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:0a9aad022c0e71771b68cd0d369df909510a58cccfe703d45ac95d49e3c0d797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4325749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548c42540f2d5b07ee0814b463649bd1379f7f0f2e9f101aeb3a2fe232cca1b2`

```dockerfile
```

-	Layers:
	-	`sha256:89127bbc4afd4c7545670ad764ce2e24f28ec414835c56fcf53f3a7c04be637b`  
		Last Modified: Wed, 24 Jul 2024 18:08:46 GMT  
		Size: 4.3 MB (4299518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86a8fb7ca725331483ad8f03c4078271b5d8eccb1608da07cbbdf8e6d2841149`  
		Last Modified: Wed, 24 Jul 2024 18:08:45 GMT  
		Size: 26.2 KB (26231 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.4.5`

```console
$ docker pull geonetwork@sha256:93b389c9bf911b8578e1f0d8172e9d98f18ea1a77cdbde4668374d8af996eead
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:4.4.5` - linux; amd64

```console
$ docker pull geonetwork@sha256:b065add9cac399306d4b10b2ab818c059ea90fa78410e77d596b042d59b8a2c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.4 MB (488369319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7425dde07a9dee83d967d85d4db4370c49c969bbb6833b89c2d3cd80c03f8fe2`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Jun 2024 10:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:58:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='9d14a076d1440161ab4c9736644e8e9f4719eb8e9f44c03470640960c3cd5e00';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["jshell"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_VERSION=9.4.55.v20240627
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.55.v20240627/jetty-home-9.4.55.v20240627.tar.gz
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
WORKDIR /var/lib/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
USER jetty
# Tue, 18 Jun 2024 10:58:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 18 Jun 2024 10:58:54 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 18 Jun 2024 10:58:54 GMT
USER root
# Tue, 18 Jun 2024 10:58:54 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
USER jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_FILE=geonetwork.war
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_VERSION=4.4.5
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_DOWNLOAD_MD5=a7b04339041e1e8217435dc6273ac3b8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:58:54 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b454cd6d22f196b273f4ba330e473a91645ea8875a5a19fec9e095a3339aa2`  
		Last Modified: Wed, 24 Jul 2024 01:26:45 GMT  
		Size: 145.6 MB (145557968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f732ae9cdf4c8bf8cf47997726fe1f9d004cc3a94de7e1a66814cd84c15689f3`  
		Last Modified: Wed, 24 Jul 2024 01:26:34 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3259d4aad21fdb59205afd139d7cd63465836f6c003b7831821416d37f350771`  
		Last Modified: Thu, 25 Jul 2024 17:28:14 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d116df1c047e785f473acc1191d11f21ba2211020d5233171cf0d3d989e8e02f`  
		Last Modified: Thu, 25 Jul 2024 19:03:54 GMT  
		Size: 10.3 MB (10293140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858122808ab087e1e296cf0c734f7a0479220652e06c8c80ab821de887dff250`  
		Last Modified: Thu, 25 Jul 2024 19:03:34 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404938076bb48bccbc7bb4423021e94939954cbf1b17e12f7e7b8198a342301f`  
		Last Modified: Thu, 25 Jul 2024 20:10:08 GMT  
		Size: 245.2 KB (245169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d79a6ee5a0348aedaa8c10e567b40f7618ac822c01fe3413d2a51a1b172683`  
		Last Modified: Thu, 25 Jul 2024 20:10:14 GMT  
		Size: 286.8 MB (286763079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb5c1c984257d5118bae3a2ca43a15816c6d059f3ad581a74d480dcbee66a6b`  
		Last Modified: Thu, 25 Jul 2024 20:10:07 GMT  
		Size: 552.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b224130970b3f8a41ba8311b9ea67b17e37ac8ec00bc7f65cbdcb9da09ab0b`  
		Last Modified: Thu, 25 Jul 2024 20:10:07 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fd7fff663d2e9761e61bf90a707e080f3c2a425a8804a2714a37aeb85b12dc`  
		Last Modified: Thu, 25 Jul 2024 20:10:08 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4.5` - unknown; unknown

```console
$ docker pull geonetwork@sha256:1a4c9feec825fd3197d640705400b15f4b2f18daa9c273d59a26b958f2affca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1948d4d6ca08ebb109d51cda89a09d0f5f63e6f1e147b772f76581c4e68d1893`

```dockerfile
```

-	Layers:
	-	`sha256:fc792c619a19eccee7640a03950bdaefeed8c382235a2559d10ba7cb31ca173a`  
		Last Modified: Thu, 25 Jul 2024 20:10:08 GMT  
		Size: 4.3 MB (4299246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6d955e812a11c739073e859b47052a91ce55389e46417049f801aeee59e90cd`  
		Last Modified: Thu, 25 Jul 2024 20:10:07 GMT  
		Size: 25.7 KB (25666 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4.5` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:b5fff45972ac86cb708f2fae175b3b7c51205da0fbfeae267f337989ed9f4848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.6 MB (483647932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eceb7a0fea170f2114b4493287b28564426822dad4958ee91a3b6d3cdf7c3f89`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Jun 2024 10:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:58:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='9d14a076d1440161ab4c9736644e8e9f4719eb8e9f44c03470640960c3cd5e00';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["jshell"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_VERSION=9.4.55.v20240627
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.55.v20240627/jetty-home-9.4.55.v20240627.tar.gz
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
WORKDIR /var/lib/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
USER jetty
# Tue, 18 Jun 2024 10:58:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 18 Jun 2024 10:58:54 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 18 Jun 2024 10:58:54 GMT
USER root
# Tue, 18 Jun 2024 10:58:54 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
USER jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_FILE=geonetwork.war
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_VERSION=4.4.5
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_DOWNLOAD_MD5=a7b04339041e1e8217435dc6273ac3b8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:58:54 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f56fba665802b80660e75f0b84fbae178f7fa6d018e7d035229b396f302fb9`  
		Last Modified: Wed, 24 Jul 2024 00:50:30 GMT  
		Size: 142.4 MB (142361214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf0192e7fcc5bca3ccff402f57c857e0db1d000ecf4d3dc36981fe770113260`  
		Last Modified: Wed, 24 Jul 2024 00:50:21 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3beccd94eafe3dbf394edd5c06f9d458d9a4e96ab895d94308d7c602f7b6d2a8`  
		Last Modified: Wed, 24 Jul 2024 00:50:21 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b30dc2e43b3a42ccebd408a81ed512669a2387eeba908741d087e0b902f8a7f`  
		Last Modified: Wed, 24 Jul 2024 15:43:35 GMT  
		Size: 10.3 MB (10293048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13600aa53b0b178fcc3c1c1efd706cbe98ca53ee021ad3ce3ae6596cae6640f5`  
		Last Modified: Wed, 24 Jul 2024 15:43:34 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eed90cc0147451a7e0512afa409f2119c5380c38d1d3036d732e7fa7ce61b8e`  
		Last Modified: Wed, 24 Jul 2024 18:08:45 GMT  
		Size: 243.8 KB (243816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96200bc41e80059deca60d8beed6021c0bb057079bd12856dbb13552e57f7ea`  
		Last Modified: Wed, 24 Jul 2024 18:08:52 GMT  
		Size: 286.8 MB (286763094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222ea95c4ba35a2665d368505d027872dd9cc82bd1a5db0f5f92031b395528e8`  
		Last Modified: Wed, 24 Jul 2024 18:08:45 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f236d2a5b5399aa2455f285ee99f000e435aceb763a1c86883038c3bb1b9140a`  
		Last Modified: Wed, 24 Jul 2024 18:08:45 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fef65f78c950f6dabe4b7d74d1fd92055eda42218475cff541313322c6c737`  
		Last Modified: Wed, 24 Jul 2024 18:08:46 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4.5` - unknown; unknown

```console
$ docker pull geonetwork@sha256:0a9aad022c0e71771b68cd0d369df909510a58cccfe703d45ac95d49e3c0d797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4325749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548c42540f2d5b07ee0814b463649bd1379f7f0f2e9f101aeb3a2fe232cca1b2`

```dockerfile
```

-	Layers:
	-	`sha256:89127bbc4afd4c7545670ad764ce2e24f28ec414835c56fcf53f3a7c04be637b`  
		Last Modified: Wed, 24 Jul 2024 18:08:46 GMT  
		Size: 4.3 MB (4299518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86a8fb7ca725331483ad8f03c4078271b5d8eccb1608da07cbbdf8e6d2841149`  
		Last Modified: Wed, 24 Jul 2024 18:08:45 GMT  
		Size: 26.2 KB (26231 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:latest`

```console
$ docker pull geonetwork@sha256:93b389c9bf911b8578e1f0d8172e9d98f18ea1a77cdbde4668374d8af996eead
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:latest` - linux; amd64

```console
$ docker pull geonetwork@sha256:b065add9cac399306d4b10b2ab818c059ea90fa78410e77d596b042d59b8a2c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.4 MB (488369319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7425dde07a9dee83d967d85d4db4370c49c969bbb6833b89c2d3cd80c03f8fe2`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Jun 2024 10:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:58:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='9d14a076d1440161ab4c9736644e8e9f4719eb8e9f44c03470640960c3cd5e00';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["jshell"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_VERSION=9.4.55.v20240627
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.55.v20240627/jetty-home-9.4.55.v20240627.tar.gz
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
WORKDIR /var/lib/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
USER jetty
# Tue, 18 Jun 2024 10:58:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 18 Jun 2024 10:58:54 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 18 Jun 2024 10:58:54 GMT
USER root
# Tue, 18 Jun 2024 10:58:54 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
USER jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_FILE=geonetwork.war
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_VERSION=4.4.5
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_DOWNLOAD_MD5=a7b04339041e1e8217435dc6273ac3b8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:58:54 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b454cd6d22f196b273f4ba330e473a91645ea8875a5a19fec9e095a3339aa2`  
		Last Modified: Wed, 24 Jul 2024 01:26:45 GMT  
		Size: 145.6 MB (145557968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f732ae9cdf4c8bf8cf47997726fe1f9d004cc3a94de7e1a66814cd84c15689f3`  
		Last Modified: Wed, 24 Jul 2024 01:26:34 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3259d4aad21fdb59205afd139d7cd63465836f6c003b7831821416d37f350771`  
		Last Modified: Thu, 25 Jul 2024 17:28:14 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d116df1c047e785f473acc1191d11f21ba2211020d5233171cf0d3d989e8e02f`  
		Last Modified: Thu, 25 Jul 2024 19:03:54 GMT  
		Size: 10.3 MB (10293140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858122808ab087e1e296cf0c734f7a0479220652e06c8c80ab821de887dff250`  
		Last Modified: Thu, 25 Jul 2024 19:03:34 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404938076bb48bccbc7bb4423021e94939954cbf1b17e12f7e7b8198a342301f`  
		Last Modified: Thu, 25 Jul 2024 20:10:08 GMT  
		Size: 245.2 KB (245169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d79a6ee5a0348aedaa8c10e567b40f7618ac822c01fe3413d2a51a1b172683`  
		Last Modified: Thu, 25 Jul 2024 20:10:14 GMT  
		Size: 286.8 MB (286763079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb5c1c984257d5118bae3a2ca43a15816c6d059f3ad581a74d480dcbee66a6b`  
		Last Modified: Thu, 25 Jul 2024 20:10:07 GMT  
		Size: 552.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b224130970b3f8a41ba8311b9ea67b17e37ac8ec00bc7f65cbdcb9da09ab0b`  
		Last Modified: Thu, 25 Jul 2024 20:10:07 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fd7fff663d2e9761e61bf90a707e080f3c2a425a8804a2714a37aeb85b12dc`  
		Last Modified: Thu, 25 Jul 2024 20:10:08 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:latest` - unknown; unknown

```console
$ docker pull geonetwork@sha256:1a4c9feec825fd3197d640705400b15f4b2f18daa9c273d59a26b958f2affca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1948d4d6ca08ebb109d51cda89a09d0f5f63e6f1e147b772f76581c4e68d1893`

```dockerfile
```

-	Layers:
	-	`sha256:fc792c619a19eccee7640a03950bdaefeed8c382235a2559d10ba7cb31ca173a`  
		Last Modified: Thu, 25 Jul 2024 20:10:08 GMT  
		Size: 4.3 MB (4299246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6d955e812a11c739073e859b47052a91ce55389e46417049f801aeee59e90cd`  
		Last Modified: Thu, 25 Jul 2024 20:10:07 GMT  
		Size: 25.7 KB (25666 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:latest` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:b5fff45972ac86cb708f2fae175b3b7c51205da0fbfeae267f337989ed9f4848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.6 MB (483647932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eceb7a0fea170f2114b4493287b28564426822dad4958ee91a3b6d3cdf7c3f89`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Jun 2024 10:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:58:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='9d14a076d1440161ab4c9736644e8e9f4719eb8e9f44c03470640960c3cd5e00';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["jshell"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_VERSION=9.4.55.v20240627
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.55.v20240627/jetty-home-9.4.55.v20240627.tar.gz
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 18 Jun 2024 10:58:54 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
WORKDIR /var/lib/jetty
# Tue, 18 Jun 2024 10:58:54 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
USER jetty
# Tue, 18 Jun 2024 10:58:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:58:54 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 18 Jun 2024 10:58:54 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 18 Jun 2024 10:58:54 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 18 Jun 2024 10:58:54 GMT
USER root
# Tue, 18 Jun 2024 10:58:54 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
USER jetty
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_FILE=geonetwork.war
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_VERSION=4.4.5
# Tue, 18 Jun 2024 10:58:54 GMT
ENV GN_DOWNLOAD_MD5=a7b04339041e1e8217435dc6273ac3b8
# Tue, 18 Jun 2024 10:58:54 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Tue, 18 Jun 2024 10:58:54 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 18 Jun 2024 10:58:54 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 18 Jun 2024 10:58:54 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f56fba665802b80660e75f0b84fbae178f7fa6d018e7d035229b396f302fb9`  
		Last Modified: Wed, 24 Jul 2024 00:50:30 GMT  
		Size: 142.4 MB (142361214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf0192e7fcc5bca3ccff402f57c857e0db1d000ecf4d3dc36981fe770113260`  
		Last Modified: Wed, 24 Jul 2024 00:50:21 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3beccd94eafe3dbf394edd5c06f9d458d9a4e96ab895d94308d7c602f7b6d2a8`  
		Last Modified: Wed, 24 Jul 2024 00:50:21 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b30dc2e43b3a42ccebd408a81ed512669a2387eeba908741d087e0b902f8a7f`  
		Last Modified: Wed, 24 Jul 2024 15:43:35 GMT  
		Size: 10.3 MB (10293048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13600aa53b0b178fcc3c1c1efd706cbe98ca53ee021ad3ce3ae6596cae6640f5`  
		Last Modified: Wed, 24 Jul 2024 15:43:34 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eed90cc0147451a7e0512afa409f2119c5380c38d1d3036d732e7fa7ce61b8e`  
		Last Modified: Wed, 24 Jul 2024 18:08:45 GMT  
		Size: 243.8 KB (243816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96200bc41e80059deca60d8beed6021c0bb057079bd12856dbb13552e57f7ea`  
		Last Modified: Wed, 24 Jul 2024 18:08:52 GMT  
		Size: 286.8 MB (286763094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222ea95c4ba35a2665d368505d027872dd9cc82bd1a5db0f5f92031b395528e8`  
		Last Modified: Wed, 24 Jul 2024 18:08:45 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f236d2a5b5399aa2455f285ee99f000e435aceb763a1c86883038c3bb1b9140a`  
		Last Modified: Wed, 24 Jul 2024 18:08:45 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fef65f78c950f6dabe4b7d74d1fd92055eda42218475cff541313322c6c737`  
		Last Modified: Wed, 24 Jul 2024 18:08:46 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:latest` - unknown; unknown

```console
$ docker pull geonetwork@sha256:0a9aad022c0e71771b68cd0d369df909510a58cccfe703d45ac95d49e3c0d797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4325749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548c42540f2d5b07ee0814b463649bd1379f7f0f2e9f101aeb3a2fe232cca1b2`

```dockerfile
```

-	Layers:
	-	`sha256:89127bbc4afd4c7545670ad764ce2e24f28ec414835c56fcf53f3a7c04be637b`  
		Last Modified: Wed, 24 Jul 2024 18:08:46 GMT  
		Size: 4.3 MB (4299518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86a8fb7ca725331483ad8f03c4078271b5d8eccb1608da07cbbdf8e6d2841149`  
		Last Modified: Wed, 24 Jul 2024 18:08:45 GMT  
		Size: 26.2 KB (26231 bytes)  
		MIME: application/vnd.in-toto+json
