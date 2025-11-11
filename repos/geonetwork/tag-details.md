<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `geonetwork`

-	[`geonetwork:3`](#geonetwork3)
-	[`geonetwork:3-postgres`](#geonetwork3-postgres)
-	[`geonetwork:3.12`](#geonetwork312)
-	[`geonetwork:3.12-postgres`](#geonetwork312-postgres)
-	[`geonetwork:3.12.12`](#geonetwork31212)
-	[`geonetwork:3.12.12-postgres`](#geonetwork31212-postgres)
-	[`geonetwork:4`](#geonetwork4)
-	[`geonetwork:4.2`](#geonetwork42)
-	[`geonetwork:4.2.14`](#geonetwork4214)
-	[`geonetwork:4.4`](#geonetwork44)
-	[`geonetwork:4.4.9`](#geonetwork449)
-	[`geonetwork:latest`](#geonetworklatest)

## `geonetwork:3`

```console
$ docker pull geonetwork@sha256:38616135e18e6395da47c0e7ec589739f3ce31fd3409ba5124f94dd2709ca981
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
$ docker pull geonetwork@sha256:c3ef9214f45df6fdf640d2244752b487f524b83ca9f736a0efae6bc077d98d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.0 MB (349958641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a638485d70996926f3f72e39e1c820d4d4a81c2d761222731d207c49259b7e63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:54:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:54:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:54:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:54:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 18:53:02 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 18:53:02 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 18:53:02 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 18:53:02 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 18:53:02 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:53:02 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:53:02 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 18:53:02 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 18:53:02 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 18:53:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 10 Nov 2025 18:53:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 18:53:29 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 18:53:29 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 18:53:29 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:11:38 GMT
ENV GN_FILE=geonetwork.war
# Mon, 10 Nov 2025 19:11:38 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Mon, 10 Nov 2025 19:11:38 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Mon, 10 Nov 2025 19:11:38 GMT
ENV GN_VERSION=3.12.12
# Mon, 10 Nov 2025 19:11:38 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Mon, 10 Nov 2025 19:11:38 GMT
WORKDIR /usr/local/tomcat/webapps
# Mon, 10 Nov 2025 19:13:14 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Mon, 10 Nov 2025 19:13:15 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:13:15 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:13:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:13:15 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840f58d04572d35b286c0f073abe58d11f4b666b253d07917fbcbc903bae9b53`  
		Last Modified: Sat, 08 Nov 2025 17:54:45 GMT  
		Size: 17.0 MB (16972346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08215e4eec130757e9e612ca35a5edcc4ea744b37a1d914b3901d27a65af489`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 54.7 MB (54742672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f595cc236b227d02b5bcabb2789bb7d54eefb7749592c14c0e0e19037eace1b6`  
		Last Modified: Sat, 08 Nov 2025 17:54:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c98abe2769d872e4c8aa92f676884972014b966f3c12df813eee7498cc41704`  
		Last Modified: Sat, 08 Nov 2025 17:54:43 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc468184dcb964feea939a5c9360ddb4410a9e74263f39cbe72f4019da640cec`  
		Last Modified: Mon, 10 Nov 2025 18:53:42 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e7e84eaad9e80df2d818dac4c7bfab469dbb3f5045bede936eb747b583dc8b`  
		Last Modified: Mon, 10 Nov 2025 18:53:44 GMT  
		Size: 14.0 MB (13967169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a655b890764593dddf683841dad61e623ae3b50be83fa6d715347fab93f845`  
		Last Modified: Mon, 10 Nov 2025 19:35:42 GMT  
		Size: 234.6 MB (234550359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b2205023bacb4e87dd659de07e5b13e18ee9b0dde61795134bbf2992237d3e`  
		Last Modified: Mon, 10 Nov 2025 19:13:46 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:0e6f9eab16914dd6d347477eb52ed6b69d74fbc070c3195f7640a609e7ef181b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c16a55262a838b53cf3fabff470411d26d55f4c423ef0320b0f3eb3ec68059a`

```dockerfile
```

-	Layers:
	-	`sha256:93126211573a44c937f1e390b801524f868dd0bd5f464299ece1456515fdbd28`  
		Last Modified: Mon, 10 Nov 2025 22:12:26 GMT  
		Size: 4.4 MB (4359721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f831622e8e7a8f82728e5a6a1f0524362de89f028959991f11f53b204046dd13`  
		Last Modified: Mon, 10 Nov 2025 22:12:27 GMT  
		Size: 19.1 KB (19093 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:4acedd65003cfa3852393699006efecbce7ae3dd06d7709d4f8e5594928abe2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.7 MB (341716958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc50c3726462a2b2765ffe8ae87905fb9c12e231770a9a7168d829180cefe42`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:27 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:31 GMT
ADD file:1ccdd7fca45ec88ba0ddda07e5e5acb6b40ddcb3023e0cbc04ffffdf4e30fb0a in / 
# Wed, 01 Oct 2025 13:02:31 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:52:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:52:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:52:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:52:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 18:51:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 18:51:17 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 18:51:17 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 18:51:17 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 18:51:17 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:51:17 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:51:17 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 18:51:17 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 18:51:17 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 18:51:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 10 Nov 2025 18:51:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 18:51:56 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 18:51:56 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 18:51:56 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:16:52 GMT
ENV GN_FILE=geonetwork.war
# Mon, 10 Nov 2025 19:16:52 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Mon, 10 Nov 2025 19:16:52 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Mon, 10 Nov 2025 19:16:52 GMT
ENV GN_VERSION=3.12.12
# Mon, 10 Nov 2025 19:16:52 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Mon, 10 Nov 2025 19:16:52 GMT
WORKDIR /usr/local/tomcat/webapps
# Mon, 10 Nov 2025 19:19:44 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Mon, 10 Nov 2025 19:19:44 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:19:44 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:19:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:19:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4afa85c5883c0db62b02025c149edaaa237af5ba25ea48039e875a802d465ac7`  
		Last Modified: Wed, 01 Oct 2025 18:03:16 GMT  
		Size: 26.9 MB (26851732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877d48b3edf53ed48debe07364b6988a7d485b8dc62b8695068f22bc14f16bd2`  
		Last Modified: Sat, 08 Nov 2025 17:53:17 GMT  
		Size: 16.3 MB (16306496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56962cfd33f391ca8f58fabb02890dc45b6f35aa3971d8a94c297e434a02af68`  
		Last Modified: Sat, 08 Nov 2025 17:53:33 GMT  
		Size: 50.1 MB (50145205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2d5ab79681429e656b55821f87a596bea3d26555ad21415247af253083c464`  
		Last Modified: Sat, 08 Nov 2025 17:53:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59807762691b1491fdf00347737e0e65361bafb9e0b2182ec0f250288b60f51e`  
		Last Modified: Sat, 08 Nov 2025 17:53:22 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe759f6e72937540ea0583957c10cb8c37816d1e78548efc6810cd2013e5374`  
		Last Modified: Mon, 10 Nov 2025 18:52:11 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be97b9e28aac7f0b895a8ce07ad96fdcd9d418334816e32d663bb75f74a5d8c8`  
		Last Modified: Mon, 10 Nov 2025 18:52:16 GMT  
		Size: 13.9 MB (13871638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f1187b918fef8441ef777d7cd39be469627563bf4638f7938977a5af7b2ec4`  
		Last Modified: Mon, 10 Nov 2025 19:36:07 GMT  
		Size: 234.5 MB (234538937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6191d06d9afdce2d96dea36f8eed00db34790d161d731d22770e5acaa941ff81`  
		Last Modified: Mon, 10 Nov 2025 19:20:26 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:5a9b7dd990aca22c4cb4e4a85c14ca0ea08b69caa02b66b9e9e08aa311306ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4382863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e86d99ce648b65d1b7146fcff9df437294960acd7d02ffcb06ec7b74ab13d3`

```dockerfile
```

-	Layers:
	-	`sha256:a922db36527e541e1ed81ebdc4cae11ce32632e09c845442d8fac9b6de101821`  
		Last Modified: Mon, 10 Nov 2025 22:12:32 GMT  
		Size: 4.4 MB (4363698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83cbbba028fdfc10ad7a112c355563751119afcff97d116f4642aef94a574f53`  
		Last Modified: Mon, 10 Nov 2025 22:12:33 GMT  
		Size: 19.2 KB (19165 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:6ab2cbbd68f2d18c1d7997512713073701d420505e0665fcfca9be018bbcfaf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.2 MB (348201650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3e12fbbc2ada61abe2882b8e10ac9a58a3488576e47485a1172d308d2b1821`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:53:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:53:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:53:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:53:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 18:48:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 18:48:32 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 18:48:32 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 18:48:32 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 18:48:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:48:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:48:32 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 18:48:32 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 18:48:32 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 18:49:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 10 Nov 2025 18:49:02 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 18:49:02 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 18:49:02 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 18:49:02 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:12:37 GMT
ENV GN_FILE=geonetwork.war
# Mon, 10 Nov 2025 19:12:37 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Mon, 10 Nov 2025 19:12:37 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Mon, 10 Nov 2025 19:12:37 GMT
ENV GN_VERSION=3.12.12
# Mon, 10 Nov 2025 19:12:37 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Mon, 10 Nov 2025 19:12:37 GMT
WORKDIR /usr/local/tomcat/webapps
# Mon, 10 Nov 2025 19:14:10 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Mon, 10 Nov 2025 19:14:10 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:14:10 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:14:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:14:10 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7705e10346edc5a4be243017fe5fc1b710ad4d93c6ca9ff4c006dfddbf7c730b`  
		Last Modified: Sat, 08 Nov 2025 17:53:40 GMT  
		Size: 17.0 MB (16989327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300c877d2da85ff91dfb5e728dcd643bbb53349d3a0cb32bfa183ede8a5da9e1`  
		Last Modified: Sat, 08 Nov 2025 17:53:43 GMT  
		Size: 53.8 MB (53819233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b075a0ea537a07303b1e7acf161b539998afb0ec51bbd70e28b4a5f132793026`  
		Last Modified: Sat, 08 Nov 2025 17:53:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e08d1eca77f725e234d2ee64762f6111cc25cb1045823cb05772b8d810edf3f`  
		Last Modified: Sat, 08 Nov 2025 17:53:39 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b010cd4714bd962e1de972c56137d400018846d475956941314dfa714d9c9b`  
		Last Modified: Mon, 10 Nov 2025 18:49:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f80972ce5475e44e69d42ced3357db1a0bab0060801a9bc671971fcb11d903`  
		Last Modified: Mon, 10 Nov 2025 18:49:16 GMT  
		Size: 14.0 MB (13974011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68ff0263f11155c4fd00e7197eb2a5bcfaf6b415b666f3f59696020abea07c0`  
		Last Modified: Mon, 10 Nov 2025 19:36:38 GMT  
		Size: 234.6 MB (234554416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b82d2a06a49c482fb88db6f5cdc91921dbc403ab1b5191d9b0aa4cd0379ce0`  
		Last Modified: Mon, 10 Nov 2025 19:14:45 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:7aa307e4d3b7d9908808aec4f880300926c6f0f2af717710d8c6c7858388124d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d74623175b25307d64233de174b63a53555b0adcf3fa68e8a72eb565fab3972`

```dockerfile
```

-	Layers:
	-	`sha256:17fe963c1a2a553e50f691499dc154d26c8f970fd995081ca410585d0f66237f`  
		Last Modified: Mon, 10 Nov 2025 22:12:37 GMT  
		Size: 4.4 MB (4360875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9391ddf554661f5285fafbe43fae630be90eec34bcf8837e22bbf36130b763`  
		Last Modified: Mon, 10 Nov 2025 22:12:38 GMT  
		Size: 19.2 KB (19185 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:2cb8557b2ed9e8f03de4edcd5e8c58cbe59d93f789668fa05aa67c9d2acaafa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.9 MB (353908212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873cfd0368df110da9238b9f03fdc30d1afbaaef577f6acd46976a31ba332570`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:54:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:54:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:54:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:54:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:54:06 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:54:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:54:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:54:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:54:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 19:00:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 19:00:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:00:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 19:00:00 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 19:00:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:00:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:00:00 GMT
ENV TOMCAT_MAJOR=9
# Sat, 08 Nov 2025 19:00:00 GMT
ENV TOMCAT_VERSION=9.0.112
# Sat, 08 Nov 2025 19:00:00 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 19:47:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 10 Nov 2025 19:47:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 19:47:13 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 19:47:13 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 19:47:13 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 23:15:49 GMT
ENV GN_FILE=geonetwork.war
# Mon, 10 Nov 2025 23:15:49 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Mon, 10 Nov 2025 23:15:49 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Mon, 10 Nov 2025 23:15:49 GMT
ENV GN_VERSION=3.12.12
# Mon, 10 Nov 2025 23:15:49 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Mon, 10 Nov 2025 23:15:49 GMT
WORKDIR /usr/local/tomcat/webapps
# Mon, 10 Nov 2025 23:16:50 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Mon, 10 Nov 2025 23:16:51 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 23:16:51 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 23:16:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 23:16:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c3c84c9145d6e39b87361420c42775001b0a5d2bff0b29876f0b582e69bdbf`  
		Last Modified: Sat, 08 Nov 2025 17:54:48 GMT  
		Size: 18.8 MB (18814703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5833a946e93b9fd592425a2c130d2de3d0c47593502ca8696c622ae4d8a7a466`  
		Last Modified: Sat, 08 Nov 2025 17:54:53 GMT  
		Size: 52.2 MB (52180251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e96f2543d1efb4f969021c1fa90b3c36fe7d87795d9d65bb5b40fd63941bd62`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecae247d1136bdf5a3d1676b8e621b72e8b646217244cbcacec857c4095be5e8`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55c44ff40e732795c22184283a33627cae1d4475a0ba1545977662e9b12053c`  
		Last Modified: Sat, 08 Nov 2025 19:01:20 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb71e9ee01c5de6dcc1e68621bd3649db78416b092acfe6acd5bf768a8016e2a`  
		Last Modified: Mon, 10 Nov 2025 19:47:52 GMT  
		Size: 14.0 MB (14032068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7b4dbb58f4018ad3e2ad4a31cff19d9d3af990cdb6ce705ee65893bb56b7d0`  
		Last Modified: Tue, 11 Nov 2025 01:18:31 GMT  
		Size: 234.6 MB (234574715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eae6068bfbfc6a3312ccfecf204b6867076155896b466581266c6a72f1b3daa`  
		Last Modified: Mon, 10 Nov 2025 23:17:53 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:1b4b42aaac39a9942b3b507013b64a975da3691996e7513c8b7068b1688f5900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56eb4b8ddb00004f5b3348c1e2896f0e787858891c161cdfdc6b88992ece4897`

```dockerfile
```

-	Layers:
	-	`sha256:7eaa0a8fbc0327320929428b80d559a774c64eb81e322b0ed3a75375f1058063`  
		Last Modified: Tue, 11 Nov 2025 01:12:29 GMT  
		Size: 4.4 MB (4362462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d018945adbcadb21e00c3bbd2d94aa5ac0447d617012b677bfa0482c19adab4`  
		Last Modified: Tue, 11 Nov 2025 01:12:29 GMT  
		Size: 19.1 KB (19131 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3-postgres`

```console
$ docker pull geonetwork@sha256:3342195b843ae23a8902fc5f36d595ce92df219e5170c1fba9fb0f4aaa26aa49
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
$ docker pull geonetwork@sha256:49907372a8fbc44b53d9b94bd3266dd266d470406c239b630222398d1deb70bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.9 MB (363905985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8e9ace942a6d85d3ef95e976001414e0267d3ba84cb7837a5726e96a1fd3a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:54:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:54:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:54:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:54:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 18:53:02 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 18:53:02 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 18:53:02 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 18:53:02 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 18:53:02 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:53:02 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:53:02 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 18:53:02 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 18:53:02 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 18:53:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 10 Nov 2025 18:53:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 18:53:29 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 18:53:29 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 18:53:29 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:11:38 GMT
ENV GN_FILE=geonetwork.war
# Mon, 10 Nov 2025 19:11:38 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Mon, 10 Nov 2025 19:11:38 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Mon, 10 Nov 2025 19:11:38 GMT
ENV GN_VERSION=3.12.12
# Mon, 10 Nov 2025 19:11:38 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Mon, 10 Nov 2025 19:11:38 GMT
WORKDIR /usr/local/tomcat/webapps
# Mon, 10 Nov 2025 19:13:14 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Mon, 10 Nov 2025 19:13:15 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:13:15 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:13:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:13:15 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:35:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:35:53 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Mon, 10 Nov 2025 19:35:53 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Mon, 10 Nov 2025 19:35:53 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:35:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:35:53 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840f58d04572d35b286c0f073abe58d11f4b666b253d07917fbcbc903bae9b53`  
		Last Modified: Sat, 08 Nov 2025 17:54:45 GMT  
		Size: 17.0 MB (16972346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08215e4eec130757e9e612ca35a5edcc4ea744b37a1d914b3901d27a65af489`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 54.7 MB (54742672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f595cc236b227d02b5bcabb2789bb7d54eefb7749592c14c0e0e19037eace1b6`  
		Last Modified: Sat, 08 Nov 2025 17:54:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c98abe2769d872e4c8aa92f676884972014b966f3c12df813eee7498cc41704`  
		Last Modified: Sat, 08 Nov 2025 17:54:43 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc468184dcb964feea939a5c9360ddb4410a9e74263f39cbe72f4019da640cec`  
		Last Modified: Mon, 10 Nov 2025 18:53:42 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e7e84eaad9e80df2d818dac4c7bfab469dbb3f5045bede936eb747b583dc8b`  
		Last Modified: Mon, 10 Nov 2025 18:53:44 GMT  
		Size: 14.0 MB (13967169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a655b890764593dddf683841dad61e623ae3b50be83fa6d715347fab93f845`  
		Last Modified: Mon, 10 Nov 2025 19:35:42 GMT  
		Size: 234.6 MB (234550359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b2205023bacb4e87dd659de07e5b13e18ee9b0dde61795134bbf2992237d3e`  
		Last Modified: Mon, 10 Nov 2025 19:13:46 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5393972cd2e7c3820055f41bc19ccd1527851da43509482e8381403f1845fa`  
		Last Modified: Mon, 10 Nov 2025 19:36:16 GMT  
		Size: 13.9 MB (13943935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d189f2b93a9133f7ce397b470c81a15dfd3aba6222e76201c7145726efb652c`  
		Last Modified: Mon, 10 Nov 2025 19:36:14 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4448e1494c5335d39dd01a6fcdcf0cc8c004c792f3a6373b4dac507eb0c65751`  
		Last Modified: Mon, 10 Nov 2025 19:36:14 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83816d12895b1572bd8743ed420d1687faebded06319d96b022ea2adcb75ab40`  
		Last Modified: Mon, 10 Nov 2025 19:36:14 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:c7f88b69c4b82cb3fb034fdeab3c6638f74480e72c16feadb5efb5fb22c42445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5937191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f908b786011f7f9371b451d23bc585a376a4ccde0b43f11d1635222cd883fe3`

```dockerfile
```

-	Layers:
	-	`sha256:01a65c753d15ee10ea3ed83ab32e0a90fd72bbb29d584d925c56bdf84ce610ee`  
		Last Modified: Mon, 10 Nov 2025 22:12:39 GMT  
		Size: 5.9 MB (5914372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190b0351acc0525fb06b0e94a94aef45f11c1c2b833201ff51bf02c1d55efd3d`  
		Last Modified: Mon, 10 Nov 2025 22:12:40 GMT  
		Size: 22.8 KB (22819 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:124122aed2723b2482cf26fecde1234c3a7a9f8e78736f967b771bdf917ed3e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.7 MB (354725276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59d78e19fb3a65ac3455cd0020611e669890e54369d55174b24c981f20f1626`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:27 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:31 GMT
ADD file:1ccdd7fca45ec88ba0ddda07e5e5acb6b40ddcb3023e0cbc04ffffdf4e30fb0a in / 
# Wed, 01 Oct 2025 13:02:31 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:52:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:52:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:52:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:52:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 18:51:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 18:51:17 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 18:51:17 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 18:51:17 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 18:51:17 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:51:17 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:51:17 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 18:51:17 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 18:51:17 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 18:51:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 10 Nov 2025 18:51:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 18:51:56 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 18:51:56 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 18:51:56 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:16:52 GMT
ENV GN_FILE=geonetwork.war
# Mon, 10 Nov 2025 19:16:52 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Mon, 10 Nov 2025 19:16:52 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Mon, 10 Nov 2025 19:16:52 GMT
ENV GN_VERSION=3.12.12
# Mon, 10 Nov 2025 19:16:52 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Mon, 10 Nov 2025 19:16:52 GMT
WORKDIR /usr/local/tomcat/webapps
# Mon, 10 Nov 2025 19:19:44 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Mon, 10 Nov 2025 19:19:44 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:19:44 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:19:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:19:44 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:36:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:36:28 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Mon, 10 Nov 2025 19:36:28 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Mon, 10 Nov 2025 19:36:28 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:36:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:36:28 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4afa85c5883c0db62b02025c149edaaa237af5ba25ea48039e875a802d465ac7`  
		Last Modified: Wed, 01 Oct 2025 18:03:16 GMT  
		Size: 26.9 MB (26851732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877d48b3edf53ed48debe07364b6988a7d485b8dc62b8695068f22bc14f16bd2`  
		Last Modified: Sat, 08 Nov 2025 17:53:17 GMT  
		Size: 16.3 MB (16306496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56962cfd33f391ca8f58fabb02890dc45b6f35aa3971d8a94c297e434a02af68`  
		Last Modified: Sat, 08 Nov 2025 17:53:33 GMT  
		Size: 50.1 MB (50145205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2d5ab79681429e656b55821f87a596bea3d26555ad21415247af253083c464`  
		Last Modified: Sat, 08 Nov 2025 17:53:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59807762691b1491fdf00347737e0e65361bafb9e0b2182ec0f250288b60f51e`  
		Last Modified: Sat, 08 Nov 2025 17:53:22 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe759f6e72937540ea0583957c10cb8c37816d1e78548efc6810cd2013e5374`  
		Last Modified: Mon, 10 Nov 2025 18:52:11 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be97b9e28aac7f0b895a8ce07ad96fdcd9d418334816e32d663bb75f74a5d8c8`  
		Last Modified: Mon, 10 Nov 2025 18:52:16 GMT  
		Size: 13.9 MB (13871638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f1187b918fef8441ef777d7cd39be469627563bf4638f7938977a5af7b2ec4`  
		Last Modified: Mon, 10 Nov 2025 19:36:07 GMT  
		Size: 234.5 MB (234538937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6191d06d9afdce2d96dea36f8eed00db34790d161d731d22770e5acaa941ff81`  
		Last Modified: Mon, 10 Nov 2025 19:20:26 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f12992cef2f5527f33e0d017e8016cdf730c597c803b05f233645800821d71`  
		Last Modified: Mon, 10 Nov 2025 19:36:53 GMT  
		Size: 13.0 MB (13004910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5dbec9e9cb3466835f50a6af574a7eb54833377006e4b51e4c569c08c0c5b65`  
		Last Modified: Mon, 10 Nov 2025 19:36:49 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2675d0ef251c232a8f150867ef2aae7560ec43580ac88b887ec7f3783b83466`  
		Last Modified: Mon, 10 Nov 2025 19:36:50 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f7b7f28ce6cfd42ba671edeed2cfc6d2ea1db29a284516daa8de7958afa736`  
		Last Modified: Mon, 10 Nov 2025 19:36:49 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:0f9237f5730c53f95a1cbc66cee9ddaeb3ff9630db69171b32e574378f209d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5939984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0f9a1a4041a7ddabea8f9c7c34e80f38f0617f0608a7501135b2dba36d191b`

```dockerfile
```

-	Layers:
	-	`sha256:173f5fafd605f6616457c1c6933df79a1ca8065b7a6f0a84c632e41f0de8168e`  
		Last Modified: Mon, 10 Nov 2025 22:12:45 GMT  
		Size: 5.9 MB (5917081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1176a2fba01239d3b277b0f797b1921ae88ab05df6bf55ccb0b76afff2226f29`  
		Last Modified: Mon, 10 Nov 2025 22:12:46 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:db8cff24871b1bde54dc2d1af24e632ac6990c3f5f773e51a9ecaa583ee909e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.1 MB (362114181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0feae438d37e432393cfdc30930626723af259e462126315f7f2af639bb58d1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:53:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:53:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:53:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:53:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 18:48:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 18:48:32 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 18:48:32 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 18:48:32 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 18:48:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:48:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:48:32 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 18:48:32 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 18:48:32 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 18:49:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 10 Nov 2025 18:49:02 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 18:49:02 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 18:49:02 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 18:49:02 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:12:37 GMT
ENV GN_FILE=geonetwork.war
# Mon, 10 Nov 2025 19:12:37 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Mon, 10 Nov 2025 19:12:37 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Mon, 10 Nov 2025 19:12:37 GMT
ENV GN_VERSION=3.12.12
# Mon, 10 Nov 2025 19:12:37 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Mon, 10 Nov 2025 19:12:37 GMT
WORKDIR /usr/local/tomcat/webapps
# Mon, 10 Nov 2025 19:14:10 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Mon, 10 Nov 2025 19:14:10 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:14:10 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:14:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:14:10 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:36:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:36:55 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Mon, 10 Nov 2025 19:36:55 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Mon, 10 Nov 2025 19:36:55 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:36:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:36:55 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7705e10346edc5a4be243017fe5fc1b710ad4d93c6ca9ff4c006dfddbf7c730b`  
		Last Modified: Sat, 08 Nov 2025 17:53:40 GMT  
		Size: 17.0 MB (16989327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300c877d2da85ff91dfb5e728dcd643bbb53349d3a0cb32bfa183ede8a5da9e1`  
		Last Modified: Sat, 08 Nov 2025 17:53:43 GMT  
		Size: 53.8 MB (53819233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b075a0ea537a07303b1e7acf161b539998afb0ec51bbd70e28b4a5f132793026`  
		Last Modified: Sat, 08 Nov 2025 17:53:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e08d1eca77f725e234d2ee64762f6111cc25cb1045823cb05772b8d810edf3f`  
		Last Modified: Sat, 08 Nov 2025 17:53:39 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b010cd4714bd962e1de972c56137d400018846d475956941314dfa714d9c9b`  
		Last Modified: Mon, 10 Nov 2025 18:49:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f80972ce5475e44e69d42ced3357db1a0bab0060801a9bc671971fcb11d903`  
		Last Modified: Mon, 10 Nov 2025 18:49:16 GMT  
		Size: 14.0 MB (13974011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68ff0263f11155c4fd00e7197eb2a5bcfaf6b415b666f3f59696020abea07c0`  
		Last Modified: Mon, 10 Nov 2025 19:36:38 GMT  
		Size: 234.6 MB (234554416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b82d2a06a49c482fb88db6f5cdc91921dbc403ab1b5191d9b0aa4cd0379ce0`  
		Last Modified: Mon, 10 Nov 2025 19:14:45 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab84e2a2ae1aee44bd58f903627c88e12c432ef05ffce964ed472152d16d1cc`  
		Last Modified: Mon, 10 Nov 2025 19:37:19 GMT  
		Size: 13.9 MB (13909111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bef0f8ea32ed89348873ef56018f0b353fec9ad1797a1f815c213effeca26e`  
		Last Modified: Mon, 10 Nov 2025 19:37:18 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2018b49f408f8abdf72bd36f6dbccdb37621b29455c644616a5d281b3d6f8b63`  
		Last Modified: Mon, 10 Nov 2025 19:37:18 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa436aacb9348a140a010e571a4d962124faf1f91f03363adf6d41aea55d8875`  
		Last Modified: Mon, 10 Nov 2025 19:37:19 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:b25e09aa6cbdf34ed4b92c0a2a898380bdb66df9b5eff87efa49201ea6d13783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5944500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d98ff0dfd66a991f6c6293d94d84999e1c0ea3ed7de9e2734fab22ee197b848`

```dockerfile
```

-	Layers:
	-	`sha256:f315f51b9f6d69075b7b9657c4f0743c7b1e574913e5afc19249cd5528870896`  
		Last Modified: Mon, 10 Nov 2025 22:12:51 GMT  
		Size: 5.9 MB (5921574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a597e03d7627c894b6728b3583fe3f7844cb81943f185cb3022f28099cbf9c8`  
		Last Modified: Mon, 10 Nov 2025 22:12:52 GMT  
		Size: 22.9 KB (22926 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:11ba94b34ba69f4d3cfa3455027329d22efc8079a0d990ed491a9ef1efa6f8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.3 MB (368343861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347fe03f5a28550d1aaae200ea5d4a684dc5a1b104dbae027a702bc52c9f7db4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:54:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:54:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:54:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:54:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:54:06 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:54:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:54:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:54:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:54:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 19:00:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 19:00:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:00:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 19:00:00 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 19:00:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:00:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:00:00 GMT
ENV TOMCAT_MAJOR=9
# Sat, 08 Nov 2025 19:00:00 GMT
ENV TOMCAT_VERSION=9.0.112
# Sat, 08 Nov 2025 19:00:00 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 19:47:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 10 Nov 2025 19:47:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 19:47:13 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 19:47:13 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 19:47:13 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 23:15:49 GMT
ENV GN_FILE=geonetwork.war
# Mon, 10 Nov 2025 23:15:49 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Mon, 10 Nov 2025 23:15:49 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Mon, 10 Nov 2025 23:15:49 GMT
ENV GN_VERSION=3.12.12
# Mon, 10 Nov 2025 23:15:49 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Mon, 10 Nov 2025 23:15:49 GMT
WORKDIR /usr/local/tomcat/webapps
# Mon, 10 Nov 2025 23:16:50 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Mon, 10 Nov 2025 23:16:51 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 23:16:51 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 23:16:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 23:16:51 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Nov 2025 00:10:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 00:10:39 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 11 Nov 2025 00:10:40 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 11 Nov 2025 00:10:40 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 11 Nov 2025 00:10:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Nov 2025 00:10:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c3c84c9145d6e39b87361420c42775001b0a5d2bff0b29876f0b582e69bdbf`  
		Last Modified: Sat, 08 Nov 2025 17:54:48 GMT  
		Size: 18.8 MB (18814703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5833a946e93b9fd592425a2c130d2de3d0c47593502ca8696c622ae4d8a7a466`  
		Last Modified: Sat, 08 Nov 2025 17:54:53 GMT  
		Size: 52.2 MB (52180251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e96f2543d1efb4f969021c1fa90b3c36fe7d87795d9d65bb5b40fd63941bd62`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecae247d1136bdf5a3d1676b8e621b72e8b646217244cbcacec857c4095be5e8`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55c44ff40e732795c22184283a33627cae1d4475a0ba1545977662e9b12053c`  
		Last Modified: Sat, 08 Nov 2025 19:01:20 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb71e9ee01c5de6dcc1e68621bd3649db78416b092acfe6acd5bf768a8016e2a`  
		Last Modified: Mon, 10 Nov 2025 19:47:52 GMT  
		Size: 14.0 MB (14032068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7b4dbb58f4018ad3e2ad4a31cff19d9d3af990cdb6ce705ee65893bb56b7d0`  
		Last Modified: Tue, 11 Nov 2025 01:18:31 GMT  
		Size: 234.6 MB (234574715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eae6068bfbfc6a3312ccfecf204b6867076155896b466581266c6a72f1b3daa`  
		Last Modified: Mon, 10 Nov 2025 23:17:53 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c466a80722ecbdc59bd564466ade99d5e77be3e32ed912cfa9dbf18da9bd86b7`  
		Last Modified: Tue, 11 Nov 2025 00:11:17 GMT  
		Size: 14.4 MB (14432223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1cd8126c4d88a6fb87cf54154d9874ebd79198f7e3cf74195c72105589f0b7`  
		Last Modified: Tue, 11 Nov 2025 00:11:16 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a287d7754504dc2f0b8c7ed4ac4e10ec33cd34d25f9546e159fec00846e17637`  
		Last Modified: Tue, 11 Nov 2025 00:11:16 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa028cb003c3b3f570914d7b29812c2eb2614e3c84520b131e3bf6c4623c5c16`  
		Last Modified: Tue, 11 Nov 2025 00:11:16 GMT  
		Size: 975.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:2e62fddc29b3de849fd3f494fc610ec93c0aabac54e3bad0f36be003e59b919f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcee9f27a84b7b4fa2fc3108c305f6018da73316f22318018ed56a126859bfb8`

```dockerfile
```

-	Layers:
	-	`sha256:63f947b10b73d3712472c3f99d23847ea2f2ecef66d6935655764c11c2b09b9f`  
		Last Modified: Tue, 11 Nov 2025 01:12:35 GMT  
		Size: 5.9 MB (5919870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4520def069181df2ef90ea92e652a7cbcb712f32a8c6087ad1f0fec72768a63`  
		Last Modified: Tue, 11 Nov 2025 01:12:36 GMT  
		Size: 22.9 KB (22859 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12`

```console
$ docker pull geonetwork@sha256:38616135e18e6395da47c0e7ec589739f3ce31fd3409ba5124f94dd2709ca981
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
$ docker pull geonetwork@sha256:c3ef9214f45df6fdf640d2244752b487f524b83ca9f736a0efae6bc077d98d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.0 MB (349958641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a638485d70996926f3f72e39e1c820d4d4a81c2d761222731d207c49259b7e63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:54:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:54:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:54:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:54:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 18:53:02 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 18:53:02 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 18:53:02 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 18:53:02 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 18:53:02 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:53:02 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:53:02 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 18:53:02 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 18:53:02 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 18:53:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 10 Nov 2025 18:53:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 18:53:29 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 18:53:29 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 18:53:29 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:11:38 GMT
ENV GN_FILE=geonetwork.war
# Mon, 10 Nov 2025 19:11:38 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Mon, 10 Nov 2025 19:11:38 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Mon, 10 Nov 2025 19:11:38 GMT
ENV GN_VERSION=3.12.12
# Mon, 10 Nov 2025 19:11:38 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Mon, 10 Nov 2025 19:11:38 GMT
WORKDIR /usr/local/tomcat/webapps
# Mon, 10 Nov 2025 19:13:14 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Mon, 10 Nov 2025 19:13:15 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:13:15 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:13:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:13:15 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840f58d04572d35b286c0f073abe58d11f4b666b253d07917fbcbc903bae9b53`  
		Last Modified: Sat, 08 Nov 2025 17:54:45 GMT  
		Size: 17.0 MB (16972346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08215e4eec130757e9e612ca35a5edcc4ea744b37a1d914b3901d27a65af489`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 54.7 MB (54742672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f595cc236b227d02b5bcabb2789bb7d54eefb7749592c14c0e0e19037eace1b6`  
		Last Modified: Sat, 08 Nov 2025 17:54:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c98abe2769d872e4c8aa92f676884972014b966f3c12df813eee7498cc41704`  
		Last Modified: Sat, 08 Nov 2025 17:54:43 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc468184dcb964feea939a5c9360ddb4410a9e74263f39cbe72f4019da640cec`  
		Last Modified: Mon, 10 Nov 2025 18:53:42 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e7e84eaad9e80df2d818dac4c7bfab469dbb3f5045bede936eb747b583dc8b`  
		Last Modified: Mon, 10 Nov 2025 18:53:44 GMT  
		Size: 14.0 MB (13967169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a655b890764593dddf683841dad61e623ae3b50be83fa6d715347fab93f845`  
		Last Modified: Mon, 10 Nov 2025 19:35:42 GMT  
		Size: 234.6 MB (234550359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b2205023bacb4e87dd659de07e5b13e18ee9b0dde61795134bbf2992237d3e`  
		Last Modified: Mon, 10 Nov 2025 19:13:46 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:0e6f9eab16914dd6d347477eb52ed6b69d74fbc070c3195f7640a609e7ef181b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c16a55262a838b53cf3fabff470411d26d55f4c423ef0320b0f3eb3ec68059a`

```dockerfile
```

-	Layers:
	-	`sha256:93126211573a44c937f1e390b801524f868dd0bd5f464299ece1456515fdbd28`  
		Last Modified: Mon, 10 Nov 2025 22:12:26 GMT  
		Size: 4.4 MB (4359721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f831622e8e7a8f82728e5a6a1f0524362de89f028959991f11f53b204046dd13`  
		Last Modified: Mon, 10 Nov 2025 22:12:27 GMT  
		Size: 19.1 KB (19093 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:4acedd65003cfa3852393699006efecbce7ae3dd06d7709d4f8e5594928abe2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.7 MB (341716958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc50c3726462a2b2765ffe8ae87905fb9c12e231770a9a7168d829180cefe42`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:27 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:31 GMT
ADD file:1ccdd7fca45ec88ba0ddda07e5e5acb6b40ddcb3023e0cbc04ffffdf4e30fb0a in / 
# Wed, 01 Oct 2025 13:02:31 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:52:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:52:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:52:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:52:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 18:51:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 18:51:17 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 18:51:17 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 18:51:17 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 18:51:17 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:51:17 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:51:17 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 18:51:17 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 18:51:17 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 18:51:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 10 Nov 2025 18:51:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 18:51:56 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 18:51:56 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 18:51:56 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:16:52 GMT
ENV GN_FILE=geonetwork.war
# Mon, 10 Nov 2025 19:16:52 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Mon, 10 Nov 2025 19:16:52 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Mon, 10 Nov 2025 19:16:52 GMT
ENV GN_VERSION=3.12.12
# Mon, 10 Nov 2025 19:16:52 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Mon, 10 Nov 2025 19:16:52 GMT
WORKDIR /usr/local/tomcat/webapps
# Mon, 10 Nov 2025 19:19:44 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Mon, 10 Nov 2025 19:19:44 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:19:44 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:19:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:19:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4afa85c5883c0db62b02025c149edaaa237af5ba25ea48039e875a802d465ac7`  
		Last Modified: Wed, 01 Oct 2025 18:03:16 GMT  
		Size: 26.9 MB (26851732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877d48b3edf53ed48debe07364b6988a7d485b8dc62b8695068f22bc14f16bd2`  
		Last Modified: Sat, 08 Nov 2025 17:53:17 GMT  
		Size: 16.3 MB (16306496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56962cfd33f391ca8f58fabb02890dc45b6f35aa3971d8a94c297e434a02af68`  
		Last Modified: Sat, 08 Nov 2025 17:53:33 GMT  
		Size: 50.1 MB (50145205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2d5ab79681429e656b55821f87a596bea3d26555ad21415247af253083c464`  
		Last Modified: Sat, 08 Nov 2025 17:53:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59807762691b1491fdf00347737e0e65361bafb9e0b2182ec0f250288b60f51e`  
		Last Modified: Sat, 08 Nov 2025 17:53:22 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe759f6e72937540ea0583957c10cb8c37816d1e78548efc6810cd2013e5374`  
		Last Modified: Mon, 10 Nov 2025 18:52:11 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be97b9e28aac7f0b895a8ce07ad96fdcd9d418334816e32d663bb75f74a5d8c8`  
		Last Modified: Mon, 10 Nov 2025 18:52:16 GMT  
		Size: 13.9 MB (13871638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f1187b918fef8441ef777d7cd39be469627563bf4638f7938977a5af7b2ec4`  
		Last Modified: Mon, 10 Nov 2025 19:36:07 GMT  
		Size: 234.5 MB (234538937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6191d06d9afdce2d96dea36f8eed00db34790d161d731d22770e5acaa941ff81`  
		Last Modified: Mon, 10 Nov 2025 19:20:26 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:5a9b7dd990aca22c4cb4e4a85c14ca0ea08b69caa02b66b9e9e08aa311306ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4382863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e86d99ce648b65d1b7146fcff9df437294960acd7d02ffcb06ec7b74ab13d3`

```dockerfile
```

-	Layers:
	-	`sha256:a922db36527e541e1ed81ebdc4cae11ce32632e09c845442d8fac9b6de101821`  
		Last Modified: Mon, 10 Nov 2025 22:12:32 GMT  
		Size: 4.4 MB (4363698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83cbbba028fdfc10ad7a112c355563751119afcff97d116f4642aef94a574f53`  
		Last Modified: Mon, 10 Nov 2025 22:12:33 GMT  
		Size: 19.2 KB (19165 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:6ab2cbbd68f2d18c1d7997512713073701d420505e0665fcfca9be018bbcfaf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.2 MB (348201650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3e12fbbc2ada61abe2882b8e10ac9a58a3488576e47485a1172d308d2b1821`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:53:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:53:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:53:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:53:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 18:48:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 18:48:32 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 18:48:32 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 18:48:32 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 18:48:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:48:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:48:32 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 18:48:32 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 18:48:32 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 18:49:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 10 Nov 2025 18:49:02 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 18:49:02 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 18:49:02 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 18:49:02 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:12:37 GMT
ENV GN_FILE=geonetwork.war
# Mon, 10 Nov 2025 19:12:37 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Mon, 10 Nov 2025 19:12:37 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Mon, 10 Nov 2025 19:12:37 GMT
ENV GN_VERSION=3.12.12
# Mon, 10 Nov 2025 19:12:37 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Mon, 10 Nov 2025 19:12:37 GMT
WORKDIR /usr/local/tomcat/webapps
# Mon, 10 Nov 2025 19:14:10 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Mon, 10 Nov 2025 19:14:10 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:14:10 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:14:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:14:10 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7705e10346edc5a4be243017fe5fc1b710ad4d93c6ca9ff4c006dfddbf7c730b`  
		Last Modified: Sat, 08 Nov 2025 17:53:40 GMT  
		Size: 17.0 MB (16989327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300c877d2da85ff91dfb5e728dcd643bbb53349d3a0cb32bfa183ede8a5da9e1`  
		Last Modified: Sat, 08 Nov 2025 17:53:43 GMT  
		Size: 53.8 MB (53819233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b075a0ea537a07303b1e7acf161b539998afb0ec51bbd70e28b4a5f132793026`  
		Last Modified: Sat, 08 Nov 2025 17:53:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e08d1eca77f725e234d2ee64762f6111cc25cb1045823cb05772b8d810edf3f`  
		Last Modified: Sat, 08 Nov 2025 17:53:39 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b010cd4714bd962e1de972c56137d400018846d475956941314dfa714d9c9b`  
		Last Modified: Mon, 10 Nov 2025 18:49:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f80972ce5475e44e69d42ced3357db1a0bab0060801a9bc671971fcb11d903`  
		Last Modified: Mon, 10 Nov 2025 18:49:16 GMT  
		Size: 14.0 MB (13974011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68ff0263f11155c4fd00e7197eb2a5bcfaf6b415b666f3f59696020abea07c0`  
		Last Modified: Mon, 10 Nov 2025 19:36:38 GMT  
		Size: 234.6 MB (234554416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b82d2a06a49c482fb88db6f5cdc91921dbc403ab1b5191d9b0aa4cd0379ce0`  
		Last Modified: Mon, 10 Nov 2025 19:14:45 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:7aa307e4d3b7d9908808aec4f880300926c6f0f2af717710d8c6c7858388124d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d74623175b25307d64233de174b63a53555b0adcf3fa68e8a72eb565fab3972`

```dockerfile
```

-	Layers:
	-	`sha256:17fe963c1a2a553e50f691499dc154d26c8f970fd995081ca410585d0f66237f`  
		Last Modified: Mon, 10 Nov 2025 22:12:37 GMT  
		Size: 4.4 MB (4360875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9391ddf554661f5285fafbe43fae630be90eec34bcf8837e22bbf36130b763`  
		Last Modified: Mon, 10 Nov 2025 22:12:38 GMT  
		Size: 19.2 KB (19185 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:2cb8557b2ed9e8f03de4edcd5e8c58cbe59d93f789668fa05aa67c9d2acaafa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.9 MB (353908212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873cfd0368df110da9238b9f03fdc30d1afbaaef577f6acd46976a31ba332570`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:54:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:54:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:54:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:54:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:54:06 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:54:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:54:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:54:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:54:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 19:00:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 19:00:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:00:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 19:00:00 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 19:00:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:00:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:00:00 GMT
ENV TOMCAT_MAJOR=9
# Sat, 08 Nov 2025 19:00:00 GMT
ENV TOMCAT_VERSION=9.0.112
# Sat, 08 Nov 2025 19:00:00 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 19:47:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 10 Nov 2025 19:47:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 19:47:13 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 19:47:13 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 19:47:13 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 23:15:49 GMT
ENV GN_FILE=geonetwork.war
# Mon, 10 Nov 2025 23:15:49 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Mon, 10 Nov 2025 23:15:49 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Mon, 10 Nov 2025 23:15:49 GMT
ENV GN_VERSION=3.12.12
# Mon, 10 Nov 2025 23:15:49 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Mon, 10 Nov 2025 23:15:49 GMT
WORKDIR /usr/local/tomcat/webapps
# Mon, 10 Nov 2025 23:16:50 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Mon, 10 Nov 2025 23:16:51 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 23:16:51 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 23:16:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 23:16:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c3c84c9145d6e39b87361420c42775001b0a5d2bff0b29876f0b582e69bdbf`  
		Last Modified: Sat, 08 Nov 2025 17:54:48 GMT  
		Size: 18.8 MB (18814703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5833a946e93b9fd592425a2c130d2de3d0c47593502ca8696c622ae4d8a7a466`  
		Last Modified: Sat, 08 Nov 2025 17:54:53 GMT  
		Size: 52.2 MB (52180251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e96f2543d1efb4f969021c1fa90b3c36fe7d87795d9d65bb5b40fd63941bd62`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecae247d1136bdf5a3d1676b8e621b72e8b646217244cbcacec857c4095be5e8`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55c44ff40e732795c22184283a33627cae1d4475a0ba1545977662e9b12053c`  
		Last Modified: Sat, 08 Nov 2025 19:01:20 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb71e9ee01c5de6dcc1e68621bd3649db78416b092acfe6acd5bf768a8016e2a`  
		Last Modified: Mon, 10 Nov 2025 19:47:52 GMT  
		Size: 14.0 MB (14032068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7b4dbb58f4018ad3e2ad4a31cff19d9d3af990cdb6ce705ee65893bb56b7d0`  
		Last Modified: Tue, 11 Nov 2025 01:18:31 GMT  
		Size: 234.6 MB (234574715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eae6068bfbfc6a3312ccfecf204b6867076155896b466581266c6a72f1b3daa`  
		Last Modified: Mon, 10 Nov 2025 23:17:53 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:1b4b42aaac39a9942b3b507013b64a975da3691996e7513c8b7068b1688f5900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56eb4b8ddb00004f5b3348c1e2896f0e787858891c161cdfdc6b88992ece4897`

```dockerfile
```

-	Layers:
	-	`sha256:7eaa0a8fbc0327320929428b80d559a774c64eb81e322b0ed3a75375f1058063`  
		Last Modified: Tue, 11 Nov 2025 01:12:29 GMT  
		Size: 4.4 MB (4362462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d018945adbcadb21e00c3bbd2d94aa5ac0447d617012b677bfa0482c19adab4`  
		Last Modified: Tue, 11 Nov 2025 01:12:29 GMT  
		Size: 19.1 KB (19131 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12-postgres`

```console
$ docker pull geonetwork@sha256:3342195b843ae23a8902fc5f36d595ce92df219e5170c1fba9fb0f4aaa26aa49
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
$ docker pull geonetwork@sha256:49907372a8fbc44b53d9b94bd3266dd266d470406c239b630222398d1deb70bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.9 MB (363905985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8e9ace942a6d85d3ef95e976001414e0267d3ba84cb7837a5726e96a1fd3a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:54:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:54:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:54:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:54:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 18:53:02 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 18:53:02 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 18:53:02 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 18:53:02 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 18:53:02 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:53:02 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:53:02 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 18:53:02 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 18:53:02 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 18:53:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 10 Nov 2025 18:53:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 18:53:29 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 18:53:29 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 18:53:29 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:11:38 GMT
ENV GN_FILE=geonetwork.war
# Mon, 10 Nov 2025 19:11:38 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Mon, 10 Nov 2025 19:11:38 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Mon, 10 Nov 2025 19:11:38 GMT
ENV GN_VERSION=3.12.12
# Mon, 10 Nov 2025 19:11:38 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Mon, 10 Nov 2025 19:11:38 GMT
WORKDIR /usr/local/tomcat/webapps
# Mon, 10 Nov 2025 19:13:14 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Mon, 10 Nov 2025 19:13:15 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:13:15 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:13:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:13:15 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:35:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:35:53 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Mon, 10 Nov 2025 19:35:53 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Mon, 10 Nov 2025 19:35:53 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:35:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:35:53 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840f58d04572d35b286c0f073abe58d11f4b666b253d07917fbcbc903bae9b53`  
		Last Modified: Sat, 08 Nov 2025 17:54:45 GMT  
		Size: 17.0 MB (16972346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08215e4eec130757e9e612ca35a5edcc4ea744b37a1d914b3901d27a65af489`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 54.7 MB (54742672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f595cc236b227d02b5bcabb2789bb7d54eefb7749592c14c0e0e19037eace1b6`  
		Last Modified: Sat, 08 Nov 2025 17:54:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c98abe2769d872e4c8aa92f676884972014b966f3c12df813eee7498cc41704`  
		Last Modified: Sat, 08 Nov 2025 17:54:43 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc468184dcb964feea939a5c9360ddb4410a9e74263f39cbe72f4019da640cec`  
		Last Modified: Mon, 10 Nov 2025 18:53:42 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e7e84eaad9e80df2d818dac4c7bfab469dbb3f5045bede936eb747b583dc8b`  
		Last Modified: Mon, 10 Nov 2025 18:53:44 GMT  
		Size: 14.0 MB (13967169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a655b890764593dddf683841dad61e623ae3b50be83fa6d715347fab93f845`  
		Last Modified: Mon, 10 Nov 2025 19:35:42 GMT  
		Size: 234.6 MB (234550359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b2205023bacb4e87dd659de07e5b13e18ee9b0dde61795134bbf2992237d3e`  
		Last Modified: Mon, 10 Nov 2025 19:13:46 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5393972cd2e7c3820055f41bc19ccd1527851da43509482e8381403f1845fa`  
		Last Modified: Mon, 10 Nov 2025 19:36:16 GMT  
		Size: 13.9 MB (13943935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d189f2b93a9133f7ce397b470c81a15dfd3aba6222e76201c7145726efb652c`  
		Last Modified: Mon, 10 Nov 2025 19:36:14 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4448e1494c5335d39dd01a6fcdcf0cc8c004c792f3a6373b4dac507eb0c65751`  
		Last Modified: Mon, 10 Nov 2025 19:36:14 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83816d12895b1572bd8743ed420d1687faebded06319d96b022ea2adcb75ab40`  
		Last Modified: Mon, 10 Nov 2025 19:36:14 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:c7f88b69c4b82cb3fb034fdeab3c6638f74480e72c16feadb5efb5fb22c42445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5937191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f908b786011f7f9371b451d23bc585a376a4ccde0b43f11d1635222cd883fe3`

```dockerfile
```

-	Layers:
	-	`sha256:01a65c753d15ee10ea3ed83ab32e0a90fd72bbb29d584d925c56bdf84ce610ee`  
		Last Modified: Mon, 10 Nov 2025 22:12:39 GMT  
		Size: 5.9 MB (5914372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190b0351acc0525fb06b0e94a94aef45f11c1c2b833201ff51bf02c1d55efd3d`  
		Last Modified: Mon, 10 Nov 2025 22:12:40 GMT  
		Size: 22.8 KB (22819 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:124122aed2723b2482cf26fecde1234c3a7a9f8e78736f967b771bdf917ed3e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.7 MB (354725276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59d78e19fb3a65ac3455cd0020611e669890e54369d55174b24c981f20f1626`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:27 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:31 GMT
ADD file:1ccdd7fca45ec88ba0ddda07e5e5acb6b40ddcb3023e0cbc04ffffdf4e30fb0a in / 
# Wed, 01 Oct 2025 13:02:31 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:52:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:52:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:52:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:52:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 18:51:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 18:51:17 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 18:51:17 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 18:51:17 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 18:51:17 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:51:17 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:51:17 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 18:51:17 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 18:51:17 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 18:51:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 10 Nov 2025 18:51:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 18:51:56 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 18:51:56 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 18:51:56 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:16:52 GMT
ENV GN_FILE=geonetwork.war
# Mon, 10 Nov 2025 19:16:52 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Mon, 10 Nov 2025 19:16:52 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Mon, 10 Nov 2025 19:16:52 GMT
ENV GN_VERSION=3.12.12
# Mon, 10 Nov 2025 19:16:52 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Mon, 10 Nov 2025 19:16:52 GMT
WORKDIR /usr/local/tomcat/webapps
# Mon, 10 Nov 2025 19:19:44 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Mon, 10 Nov 2025 19:19:44 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:19:44 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:19:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:19:44 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:36:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:36:28 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Mon, 10 Nov 2025 19:36:28 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Mon, 10 Nov 2025 19:36:28 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:36:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:36:28 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4afa85c5883c0db62b02025c149edaaa237af5ba25ea48039e875a802d465ac7`  
		Last Modified: Wed, 01 Oct 2025 18:03:16 GMT  
		Size: 26.9 MB (26851732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877d48b3edf53ed48debe07364b6988a7d485b8dc62b8695068f22bc14f16bd2`  
		Last Modified: Sat, 08 Nov 2025 17:53:17 GMT  
		Size: 16.3 MB (16306496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56962cfd33f391ca8f58fabb02890dc45b6f35aa3971d8a94c297e434a02af68`  
		Last Modified: Sat, 08 Nov 2025 17:53:33 GMT  
		Size: 50.1 MB (50145205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2d5ab79681429e656b55821f87a596bea3d26555ad21415247af253083c464`  
		Last Modified: Sat, 08 Nov 2025 17:53:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59807762691b1491fdf00347737e0e65361bafb9e0b2182ec0f250288b60f51e`  
		Last Modified: Sat, 08 Nov 2025 17:53:22 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe759f6e72937540ea0583957c10cb8c37816d1e78548efc6810cd2013e5374`  
		Last Modified: Mon, 10 Nov 2025 18:52:11 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be97b9e28aac7f0b895a8ce07ad96fdcd9d418334816e32d663bb75f74a5d8c8`  
		Last Modified: Mon, 10 Nov 2025 18:52:16 GMT  
		Size: 13.9 MB (13871638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f1187b918fef8441ef777d7cd39be469627563bf4638f7938977a5af7b2ec4`  
		Last Modified: Mon, 10 Nov 2025 19:36:07 GMT  
		Size: 234.5 MB (234538937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6191d06d9afdce2d96dea36f8eed00db34790d161d731d22770e5acaa941ff81`  
		Last Modified: Mon, 10 Nov 2025 19:20:26 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f12992cef2f5527f33e0d017e8016cdf730c597c803b05f233645800821d71`  
		Last Modified: Mon, 10 Nov 2025 19:36:53 GMT  
		Size: 13.0 MB (13004910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5dbec9e9cb3466835f50a6af574a7eb54833377006e4b51e4c569c08c0c5b65`  
		Last Modified: Mon, 10 Nov 2025 19:36:49 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2675d0ef251c232a8f150867ef2aae7560ec43580ac88b887ec7f3783b83466`  
		Last Modified: Mon, 10 Nov 2025 19:36:50 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f7b7f28ce6cfd42ba671edeed2cfc6d2ea1db29a284516daa8de7958afa736`  
		Last Modified: Mon, 10 Nov 2025 19:36:49 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:0f9237f5730c53f95a1cbc66cee9ddaeb3ff9630db69171b32e574378f209d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5939984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0f9a1a4041a7ddabea8f9c7c34e80f38f0617f0608a7501135b2dba36d191b`

```dockerfile
```

-	Layers:
	-	`sha256:173f5fafd605f6616457c1c6933df79a1ca8065b7a6f0a84c632e41f0de8168e`  
		Last Modified: Mon, 10 Nov 2025 22:12:45 GMT  
		Size: 5.9 MB (5917081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1176a2fba01239d3b277b0f797b1921ae88ab05df6bf55ccb0b76afff2226f29`  
		Last Modified: Mon, 10 Nov 2025 22:12:46 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:db8cff24871b1bde54dc2d1af24e632ac6990c3f5f773e51a9ecaa583ee909e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.1 MB (362114181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0feae438d37e432393cfdc30930626723af259e462126315f7f2af639bb58d1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:53:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:53:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:53:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:53:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 18:48:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 18:48:32 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 18:48:32 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 18:48:32 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 18:48:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:48:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:48:32 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 18:48:32 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 18:48:32 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 18:49:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 10 Nov 2025 18:49:02 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 18:49:02 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 18:49:02 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 18:49:02 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:12:37 GMT
ENV GN_FILE=geonetwork.war
# Mon, 10 Nov 2025 19:12:37 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Mon, 10 Nov 2025 19:12:37 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Mon, 10 Nov 2025 19:12:37 GMT
ENV GN_VERSION=3.12.12
# Mon, 10 Nov 2025 19:12:37 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Mon, 10 Nov 2025 19:12:37 GMT
WORKDIR /usr/local/tomcat/webapps
# Mon, 10 Nov 2025 19:14:10 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Mon, 10 Nov 2025 19:14:10 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:14:10 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:14:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:14:10 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:36:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:36:55 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Mon, 10 Nov 2025 19:36:55 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Mon, 10 Nov 2025 19:36:55 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:36:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:36:55 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7705e10346edc5a4be243017fe5fc1b710ad4d93c6ca9ff4c006dfddbf7c730b`  
		Last Modified: Sat, 08 Nov 2025 17:53:40 GMT  
		Size: 17.0 MB (16989327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300c877d2da85ff91dfb5e728dcd643bbb53349d3a0cb32bfa183ede8a5da9e1`  
		Last Modified: Sat, 08 Nov 2025 17:53:43 GMT  
		Size: 53.8 MB (53819233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b075a0ea537a07303b1e7acf161b539998afb0ec51bbd70e28b4a5f132793026`  
		Last Modified: Sat, 08 Nov 2025 17:53:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e08d1eca77f725e234d2ee64762f6111cc25cb1045823cb05772b8d810edf3f`  
		Last Modified: Sat, 08 Nov 2025 17:53:39 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b010cd4714bd962e1de972c56137d400018846d475956941314dfa714d9c9b`  
		Last Modified: Mon, 10 Nov 2025 18:49:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f80972ce5475e44e69d42ced3357db1a0bab0060801a9bc671971fcb11d903`  
		Last Modified: Mon, 10 Nov 2025 18:49:16 GMT  
		Size: 14.0 MB (13974011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68ff0263f11155c4fd00e7197eb2a5bcfaf6b415b666f3f59696020abea07c0`  
		Last Modified: Mon, 10 Nov 2025 19:36:38 GMT  
		Size: 234.6 MB (234554416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b82d2a06a49c482fb88db6f5cdc91921dbc403ab1b5191d9b0aa4cd0379ce0`  
		Last Modified: Mon, 10 Nov 2025 19:14:45 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab84e2a2ae1aee44bd58f903627c88e12c432ef05ffce964ed472152d16d1cc`  
		Last Modified: Mon, 10 Nov 2025 19:37:19 GMT  
		Size: 13.9 MB (13909111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bef0f8ea32ed89348873ef56018f0b353fec9ad1797a1f815c213effeca26e`  
		Last Modified: Mon, 10 Nov 2025 19:37:18 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2018b49f408f8abdf72bd36f6dbccdb37621b29455c644616a5d281b3d6f8b63`  
		Last Modified: Mon, 10 Nov 2025 19:37:18 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa436aacb9348a140a010e571a4d962124faf1f91f03363adf6d41aea55d8875`  
		Last Modified: Mon, 10 Nov 2025 19:37:19 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:b25e09aa6cbdf34ed4b92c0a2a898380bdb66df9b5eff87efa49201ea6d13783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5944500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d98ff0dfd66a991f6c6293d94d84999e1c0ea3ed7de9e2734fab22ee197b848`

```dockerfile
```

-	Layers:
	-	`sha256:f315f51b9f6d69075b7b9657c4f0743c7b1e574913e5afc19249cd5528870896`  
		Last Modified: Mon, 10 Nov 2025 22:12:51 GMT  
		Size: 5.9 MB (5921574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a597e03d7627c894b6728b3583fe3f7844cb81943f185cb3022f28099cbf9c8`  
		Last Modified: Mon, 10 Nov 2025 22:12:52 GMT  
		Size: 22.9 KB (22926 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:11ba94b34ba69f4d3cfa3455027329d22efc8079a0d990ed491a9ef1efa6f8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.3 MB (368343861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347fe03f5a28550d1aaae200ea5d4a684dc5a1b104dbae027a702bc52c9f7db4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:54:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:54:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:54:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:54:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:54:06 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:54:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:54:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:54:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:54:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 19:00:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 19:00:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:00:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 19:00:00 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 19:00:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:00:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:00:00 GMT
ENV TOMCAT_MAJOR=9
# Sat, 08 Nov 2025 19:00:00 GMT
ENV TOMCAT_VERSION=9.0.112
# Sat, 08 Nov 2025 19:00:00 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 19:47:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 10 Nov 2025 19:47:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 19:47:13 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 19:47:13 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 19:47:13 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 23:15:49 GMT
ENV GN_FILE=geonetwork.war
# Mon, 10 Nov 2025 23:15:49 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Mon, 10 Nov 2025 23:15:49 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Mon, 10 Nov 2025 23:15:49 GMT
ENV GN_VERSION=3.12.12
# Mon, 10 Nov 2025 23:15:49 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Mon, 10 Nov 2025 23:15:49 GMT
WORKDIR /usr/local/tomcat/webapps
# Mon, 10 Nov 2025 23:16:50 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Mon, 10 Nov 2025 23:16:51 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 23:16:51 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 23:16:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 23:16:51 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Nov 2025 00:10:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 00:10:39 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 11 Nov 2025 00:10:40 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 11 Nov 2025 00:10:40 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 11 Nov 2025 00:10:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Nov 2025 00:10:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c3c84c9145d6e39b87361420c42775001b0a5d2bff0b29876f0b582e69bdbf`  
		Last Modified: Sat, 08 Nov 2025 17:54:48 GMT  
		Size: 18.8 MB (18814703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5833a946e93b9fd592425a2c130d2de3d0c47593502ca8696c622ae4d8a7a466`  
		Last Modified: Sat, 08 Nov 2025 17:54:53 GMT  
		Size: 52.2 MB (52180251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e96f2543d1efb4f969021c1fa90b3c36fe7d87795d9d65bb5b40fd63941bd62`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecae247d1136bdf5a3d1676b8e621b72e8b646217244cbcacec857c4095be5e8`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55c44ff40e732795c22184283a33627cae1d4475a0ba1545977662e9b12053c`  
		Last Modified: Sat, 08 Nov 2025 19:01:20 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb71e9ee01c5de6dcc1e68621bd3649db78416b092acfe6acd5bf768a8016e2a`  
		Last Modified: Mon, 10 Nov 2025 19:47:52 GMT  
		Size: 14.0 MB (14032068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7b4dbb58f4018ad3e2ad4a31cff19d9d3af990cdb6ce705ee65893bb56b7d0`  
		Last Modified: Tue, 11 Nov 2025 01:18:31 GMT  
		Size: 234.6 MB (234574715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eae6068bfbfc6a3312ccfecf204b6867076155896b466581266c6a72f1b3daa`  
		Last Modified: Mon, 10 Nov 2025 23:17:53 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c466a80722ecbdc59bd564466ade99d5e77be3e32ed912cfa9dbf18da9bd86b7`  
		Last Modified: Tue, 11 Nov 2025 00:11:17 GMT  
		Size: 14.4 MB (14432223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1cd8126c4d88a6fb87cf54154d9874ebd79198f7e3cf74195c72105589f0b7`  
		Last Modified: Tue, 11 Nov 2025 00:11:16 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a287d7754504dc2f0b8c7ed4ac4e10ec33cd34d25f9546e159fec00846e17637`  
		Last Modified: Tue, 11 Nov 2025 00:11:16 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa028cb003c3b3f570914d7b29812c2eb2614e3c84520b131e3bf6c4623c5c16`  
		Last Modified: Tue, 11 Nov 2025 00:11:16 GMT  
		Size: 975.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:2e62fddc29b3de849fd3f494fc610ec93c0aabac54e3bad0f36be003e59b919f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcee9f27a84b7b4fa2fc3108c305f6018da73316f22318018ed56a126859bfb8`

```dockerfile
```

-	Layers:
	-	`sha256:63f947b10b73d3712472c3f99d23847ea2f2ecef66d6935655764c11c2b09b9f`  
		Last Modified: Tue, 11 Nov 2025 01:12:35 GMT  
		Size: 5.9 MB (5919870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4520def069181df2ef90ea92e652a7cbcb712f32a8c6087ad1f0fec72768a63`  
		Last Modified: Tue, 11 Nov 2025 01:12:36 GMT  
		Size: 22.9 KB (22859 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12.12`

```console
$ docker pull geonetwork@sha256:38616135e18e6395da47c0e7ec589739f3ce31fd3409ba5124f94dd2709ca981
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

### `geonetwork:3.12.12` - linux; amd64

```console
$ docker pull geonetwork@sha256:c3ef9214f45df6fdf640d2244752b487f524b83ca9f736a0efae6bc077d98d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.0 MB (349958641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a638485d70996926f3f72e39e1c820d4d4a81c2d761222731d207c49259b7e63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:54:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:54:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:54:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:54:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 18:53:02 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 18:53:02 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 18:53:02 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 18:53:02 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 18:53:02 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:53:02 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:53:02 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 18:53:02 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 18:53:02 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 18:53:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 10 Nov 2025 18:53:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 18:53:29 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 18:53:29 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 18:53:29 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:11:38 GMT
ENV GN_FILE=geonetwork.war
# Mon, 10 Nov 2025 19:11:38 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Mon, 10 Nov 2025 19:11:38 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Mon, 10 Nov 2025 19:11:38 GMT
ENV GN_VERSION=3.12.12
# Mon, 10 Nov 2025 19:11:38 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Mon, 10 Nov 2025 19:11:38 GMT
WORKDIR /usr/local/tomcat/webapps
# Mon, 10 Nov 2025 19:13:14 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Mon, 10 Nov 2025 19:13:15 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:13:15 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:13:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:13:15 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840f58d04572d35b286c0f073abe58d11f4b666b253d07917fbcbc903bae9b53`  
		Last Modified: Sat, 08 Nov 2025 17:54:45 GMT  
		Size: 17.0 MB (16972346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08215e4eec130757e9e612ca35a5edcc4ea744b37a1d914b3901d27a65af489`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 54.7 MB (54742672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f595cc236b227d02b5bcabb2789bb7d54eefb7749592c14c0e0e19037eace1b6`  
		Last Modified: Sat, 08 Nov 2025 17:54:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c98abe2769d872e4c8aa92f676884972014b966f3c12df813eee7498cc41704`  
		Last Modified: Sat, 08 Nov 2025 17:54:43 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc468184dcb964feea939a5c9360ddb4410a9e74263f39cbe72f4019da640cec`  
		Last Modified: Mon, 10 Nov 2025 18:53:42 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e7e84eaad9e80df2d818dac4c7bfab469dbb3f5045bede936eb747b583dc8b`  
		Last Modified: Mon, 10 Nov 2025 18:53:44 GMT  
		Size: 14.0 MB (13967169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a655b890764593dddf683841dad61e623ae3b50be83fa6d715347fab93f845`  
		Last Modified: Mon, 10 Nov 2025 19:35:42 GMT  
		Size: 234.6 MB (234550359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b2205023bacb4e87dd659de07e5b13e18ee9b0dde61795134bbf2992237d3e`  
		Last Modified: Mon, 10 Nov 2025 19:13:46 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:0e6f9eab16914dd6d347477eb52ed6b69d74fbc070c3195f7640a609e7ef181b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c16a55262a838b53cf3fabff470411d26d55f4c423ef0320b0f3eb3ec68059a`

```dockerfile
```

-	Layers:
	-	`sha256:93126211573a44c937f1e390b801524f868dd0bd5f464299ece1456515fdbd28`  
		Last Modified: Mon, 10 Nov 2025 22:12:26 GMT  
		Size: 4.4 MB (4359721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f831622e8e7a8f82728e5a6a1f0524362de89f028959991f11f53b204046dd13`  
		Last Modified: Mon, 10 Nov 2025 22:12:27 GMT  
		Size: 19.1 KB (19093 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:4acedd65003cfa3852393699006efecbce7ae3dd06d7709d4f8e5594928abe2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.7 MB (341716958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc50c3726462a2b2765ffe8ae87905fb9c12e231770a9a7168d829180cefe42`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:27 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:31 GMT
ADD file:1ccdd7fca45ec88ba0ddda07e5e5acb6b40ddcb3023e0cbc04ffffdf4e30fb0a in / 
# Wed, 01 Oct 2025 13:02:31 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:52:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:52:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:52:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:52:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 18:51:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 18:51:17 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 18:51:17 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 18:51:17 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 18:51:17 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:51:17 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:51:17 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 18:51:17 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 18:51:17 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 18:51:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 10 Nov 2025 18:51:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 18:51:56 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 18:51:56 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 18:51:56 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:16:52 GMT
ENV GN_FILE=geonetwork.war
# Mon, 10 Nov 2025 19:16:52 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Mon, 10 Nov 2025 19:16:52 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Mon, 10 Nov 2025 19:16:52 GMT
ENV GN_VERSION=3.12.12
# Mon, 10 Nov 2025 19:16:52 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Mon, 10 Nov 2025 19:16:52 GMT
WORKDIR /usr/local/tomcat/webapps
# Mon, 10 Nov 2025 19:19:44 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Mon, 10 Nov 2025 19:19:44 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:19:44 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:19:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:19:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4afa85c5883c0db62b02025c149edaaa237af5ba25ea48039e875a802d465ac7`  
		Last Modified: Wed, 01 Oct 2025 18:03:16 GMT  
		Size: 26.9 MB (26851732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877d48b3edf53ed48debe07364b6988a7d485b8dc62b8695068f22bc14f16bd2`  
		Last Modified: Sat, 08 Nov 2025 17:53:17 GMT  
		Size: 16.3 MB (16306496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56962cfd33f391ca8f58fabb02890dc45b6f35aa3971d8a94c297e434a02af68`  
		Last Modified: Sat, 08 Nov 2025 17:53:33 GMT  
		Size: 50.1 MB (50145205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2d5ab79681429e656b55821f87a596bea3d26555ad21415247af253083c464`  
		Last Modified: Sat, 08 Nov 2025 17:53:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59807762691b1491fdf00347737e0e65361bafb9e0b2182ec0f250288b60f51e`  
		Last Modified: Sat, 08 Nov 2025 17:53:22 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe759f6e72937540ea0583957c10cb8c37816d1e78548efc6810cd2013e5374`  
		Last Modified: Mon, 10 Nov 2025 18:52:11 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be97b9e28aac7f0b895a8ce07ad96fdcd9d418334816e32d663bb75f74a5d8c8`  
		Last Modified: Mon, 10 Nov 2025 18:52:16 GMT  
		Size: 13.9 MB (13871638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f1187b918fef8441ef777d7cd39be469627563bf4638f7938977a5af7b2ec4`  
		Last Modified: Mon, 10 Nov 2025 19:36:07 GMT  
		Size: 234.5 MB (234538937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6191d06d9afdce2d96dea36f8eed00db34790d161d731d22770e5acaa941ff81`  
		Last Modified: Mon, 10 Nov 2025 19:20:26 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:5a9b7dd990aca22c4cb4e4a85c14ca0ea08b69caa02b66b9e9e08aa311306ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4382863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e86d99ce648b65d1b7146fcff9df437294960acd7d02ffcb06ec7b74ab13d3`

```dockerfile
```

-	Layers:
	-	`sha256:a922db36527e541e1ed81ebdc4cae11ce32632e09c845442d8fac9b6de101821`  
		Last Modified: Mon, 10 Nov 2025 22:12:32 GMT  
		Size: 4.4 MB (4363698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83cbbba028fdfc10ad7a112c355563751119afcff97d116f4642aef94a574f53`  
		Last Modified: Mon, 10 Nov 2025 22:12:33 GMT  
		Size: 19.2 KB (19165 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:6ab2cbbd68f2d18c1d7997512713073701d420505e0665fcfca9be018bbcfaf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.2 MB (348201650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3e12fbbc2ada61abe2882b8e10ac9a58a3488576e47485a1172d308d2b1821`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:53:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:53:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:53:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:53:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 18:48:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 18:48:32 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 18:48:32 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 18:48:32 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 18:48:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:48:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:48:32 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 18:48:32 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 18:48:32 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 18:49:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 10 Nov 2025 18:49:02 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 18:49:02 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 18:49:02 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 18:49:02 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:12:37 GMT
ENV GN_FILE=geonetwork.war
# Mon, 10 Nov 2025 19:12:37 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Mon, 10 Nov 2025 19:12:37 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Mon, 10 Nov 2025 19:12:37 GMT
ENV GN_VERSION=3.12.12
# Mon, 10 Nov 2025 19:12:37 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Mon, 10 Nov 2025 19:12:37 GMT
WORKDIR /usr/local/tomcat/webapps
# Mon, 10 Nov 2025 19:14:10 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Mon, 10 Nov 2025 19:14:10 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:14:10 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:14:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:14:10 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7705e10346edc5a4be243017fe5fc1b710ad4d93c6ca9ff4c006dfddbf7c730b`  
		Last Modified: Sat, 08 Nov 2025 17:53:40 GMT  
		Size: 17.0 MB (16989327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300c877d2da85ff91dfb5e728dcd643bbb53349d3a0cb32bfa183ede8a5da9e1`  
		Last Modified: Sat, 08 Nov 2025 17:53:43 GMT  
		Size: 53.8 MB (53819233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b075a0ea537a07303b1e7acf161b539998afb0ec51bbd70e28b4a5f132793026`  
		Last Modified: Sat, 08 Nov 2025 17:53:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e08d1eca77f725e234d2ee64762f6111cc25cb1045823cb05772b8d810edf3f`  
		Last Modified: Sat, 08 Nov 2025 17:53:39 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b010cd4714bd962e1de972c56137d400018846d475956941314dfa714d9c9b`  
		Last Modified: Mon, 10 Nov 2025 18:49:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f80972ce5475e44e69d42ced3357db1a0bab0060801a9bc671971fcb11d903`  
		Last Modified: Mon, 10 Nov 2025 18:49:16 GMT  
		Size: 14.0 MB (13974011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68ff0263f11155c4fd00e7197eb2a5bcfaf6b415b666f3f59696020abea07c0`  
		Last Modified: Mon, 10 Nov 2025 19:36:38 GMT  
		Size: 234.6 MB (234554416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b82d2a06a49c482fb88db6f5cdc91921dbc403ab1b5191d9b0aa4cd0379ce0`  
		Last Modified: Mon, 10 Nov 2025 19:14:45 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:7aa307e4d3b7d9908808aec4f880300926c6f0f2af717710d8c6c7858388124d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d74623175b25307d64233de174b63a53555b0adcf3fa68e8a72eb565fab3972`

```dockerfile
```

-	Layers:
	-	`sha256:17fe963c1a2a553e50f691499dc154d26c8f970fd995081ca410585d0f66237f`  
		Last Modified: Mon, 10 Nov 2025 22:12:37 GMT  
		Size: 4.4 MB (4360875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9391ddf554661f5285fafbe43fae630be90eec34bcf8837e22bbf36130b763`  
		Last Modified: Mon, 10 Nov 2025 22:12:38 GMT  
		Size: 19.2 KB (19185 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:2cb8557b2ed9e8f03de4edcd5e8c58cbe59d93f789668fa05aa67c9d2acaafa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.9 MB (353908212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873cfd0368df110da9238b9f03fdc30d1afbaaef577f6acd46976a31ba332570`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:54:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:54:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:54:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:54:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:54:06 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:54:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:54:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:54:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:54:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 19:00:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 19:00:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:00:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 19:00:00 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 19:00:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:00:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:00:00 GMT
ENV TOMCAT_MAJOR=9
# Sat, 08 Nov 2025 19:00:00 GMT
ENV TOMCAT_VERSION=9.0.112
# Sat, 08 Nov 2025 19:00:00 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 19:47:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 10 Nov 2025 19:47:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 19:47:13 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 19:47:13 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 19:47:13 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 23:15:49 GMT
ENV GN_FILE=geonetwork.war
# Mon, 10 Nov 2025 23:15:49 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Mon, 10 Nov 2025 23:15:49 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Mon, 10 Nov 2025 23:15:49 GMT
ENV GN_VERSION=3.12.12
# Mon, 10 Nov 2025 23:15:49 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Mon, 10 Nov 2025 23:15:49 GMT
WORKDIR /usr/local/tomcat/webapps
# Mon, 10 Nov 2025 23:16:50 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Mon, 10 Nov 2025 23:16:51 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 23:16:51 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 23:16:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 23:16:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c3c84c9145d6e39b87361420c42775001b0a5d2bff0b29876f0b582e69bdbf`  
		Last Modified: Sat, 08 Nov 2025 17:54:48 GMT  
		Size: 18.8 MB (18814703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5833a946e93b9fd592425a2c130d2de3d0c47593502ca8696c622ae4d8a7a466`  
		Last Modified: Sat, 08 Nov 2025 17:54:53 GMT  
		Size: 52.2 MB (52180251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e96f2543d1efb4f969021c1fa90b3c36fe7d87795d9d65bb5b40fd63941bd62`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecae247d1136bdf5a3d1676b8e621b72e8b646217244cbcacec857c4095be5e8`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55c44ff40e732795c22184283a33627cae1d4475a0ba1545977662e9b12053c`  
		Last Modified: Sat, 08 Nov 2025 19:01:20 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb71e9ee01c5de6dcc1e68621bd3649db78416b092acfe6acd5bf768a8016e2a`  
		Last Modified: Mon, 10 Nov 2025 19:47:52 GMT  
		Size: 14.0 MB (14032068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7b4dbb58f4018ad3e2ad4a31cff19d9d3af990cdb6ce705ee65893bb56b7d0`  
		Last Modified: Tue, 11 Nov 2025 01:18:31 GMT  
		Size: 234.6 MB (234574715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eae6068bfbfc6a3312ccfecf204b6867076155896b466581266c6a72f1b3daa`  
		Last Modified: Mon, 10 Nov 2025 23:17:53 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:1b4b42aaac39a9942b3b507013b64a975da3691996e7513c8b7068b1688f5900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56eb4b8ddb00004f5b3348c1e2896f0e787858891c161cdfdc6b88992ece4897`

```dockerfile
```

-	Layers:
	-	`sha256:7eaa0a8fbc0327320929428b80d559a774c64eb81e322b0ed3a75375f1058063`  
		Last Modified: Tue, 11 Nov 2025 01:12:29 GMT  
		Size: 4.4 MB (4362462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d018945adbcadb21e00c3bbd2d94aa5ac0447d617012b677bfa0482c19adab4`  
		Last Modified: Tue, 11 Nov 2025 01:12:29 GMT  
		Size: 19.1 KB (19131 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12.12-postgres`

```console
$ docker pull geonetwork@sha256:3342195b843ae23a8902fc5f36d595ce92df219e5170c1fba9fb0f4aaa26aa49
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

### `geonetwork:3.12.12-postgres` - linux; amd64

```console
$ docker pull geonetwork@sha256:49907372a8fbc44b53d9b94bd3266dd266d470406c239b630222398d1deb70bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.9 MB (363905985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8e9ace942a6d85d3ef95e976001414e0267d3ba84cb7837a5726e96a1fd3a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:54:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:54:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:54:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:54:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:54:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 18:53:02 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 18:53:02 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 18:53:02 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 18:53:02 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 18:53:02 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:53:02 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:53:02 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 18:53:02 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 18:53:02 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 18:53:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 10 Nov 2025 18:53:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 18:53:29 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 18:53:29 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 18:53:29 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:11:38 GMT
ENV GN_FILE=geonetwork.war
# Mon, 10 Nov 2025 19:11:38 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Mon, 10 Nov 2025 19:11:38 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Mon, 10 Nov 2025 19:11:38 GMT
ENV GN_VERSION=3.12.12
# Mon, 10 Nov 2025 19:11:38 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Mon, 10 Nov 2025 19:11:38 GMT
WORKDIR /usr/local/tomcat/webapps
# Mon, 10 Nov 2025 19:13:14 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Mon, 10 Nov 2025 19:13:15 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:13:15 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:13:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:13:15 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:35:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:35:53 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Mon, 10 Nov 2025 19:35:53 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Mon, 10 Nov 2025 19:35:53 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:35:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:35:53 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840f58d04572d35b286c0f073abe58d11f4b666b253d07917fbcbc903bae9b53`  
		Last Modified: Sat, 08 Nov 2025 17:54:45 GMT  
		Size: 17.0 MB (16972346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08215e4eec130757e9e612ca35a5edcc4ea744b37a1d914b3901d27a65af489`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 54.7 MB (54742672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f595cc236b227d02b5bcabb2789bb7d54eefb7749592c14c0e0e19037eace1b6`  
		Last Modified: Sat, 08 Nov 2025 17:54:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c98abe2769d872e4c8aa92f676884972014b966f3c12df813eee7498cc41704`  
		Last Modified: Sat, 08 Nov 2025 17:54:43 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc468184dcb964feea939a5c9360ddb4410a9e74263f39cbe72f4019da640cec`  
		Last Modified: Mon, 10 Nov 2025 18:53:42 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e7e84eaad9e80df2d818dac4c7bfab469dbb3f5045bede936eb747b583dc8b`  
		Last Modified: Mon, 10 Nov 2025 18:53:44 GMT  
		Size: 14.0 MB (13967169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a655b890764593dddf683841dad61e623ae3b50be83fa6d715347fab93f845`  
		Last Modified: Mon, 10 Nov 2025 19:35:42 GMT  
		Size: 234.6 MB (234550359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b2205023bacb4e87dd659de07e5b13e18ee9b0dde61795134bbf2992237d3e`  
		Last Modified: Mon, 10 Nov 2025 19:13:46 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5393972cd2e7c3820055f41bc19ccd1527851da43509482e8381403f1845fa`  
		Last Modified: Mon, 10 Nov 2025 19:36:16 GMT  
		Size: 13.9 MB (13943935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d189f2b93a9133f7ce397b470c81a15dfd3aba6222e76201c7145726efb652c`  
		Last Modified: Mon, 10 Nov 2025 19:36:14 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4448e1494c5335d39dd01a6fcdcf0cc8c004c792f3a6373b4dac507eb0c65751`  
		Last Modified: Mon, 10 Nov 2025 19:36:14 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83816d12895b1572bd8743ed420d1687faebded06319d96b022ea2adcb75ab40`  
		Last Modified: Mon, 10 Nov 2025 19:36:14 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:c7f88b69c4b82cb3fb034fdeab3c6638f74480e72c16feadb5efb5fb22c42445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5937191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f908b786011f7f9371b451d23bc585a376a4ccde0b43f11d1635222cd883fe3`

```dockerfile
```

-	Layers:
	-	`sha256:01a65c753d15ee10ea3ed83ab32e0a90fd72bbb29d584d925c56bdf84ce610ee`  
		Last Modified: Mon, 10 Nov 2025 22:12:39 GMT  
		Size: 5.9 MB (5914372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190b0351acc0525fb06b0e94a94aef45f11c1c2b833201ff51bf02c1d55efd3d`  
		Last Modified: Mon, 10 Nov 2025 22:12:40 GMT  
		Size: 22.8 KB (22819 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:124122aed2723b2482cf26fecde1234c3a7a9f8e78736f967b771bdf917ed3e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.7 MB (354725276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59d78e19fb3a65ac3455cd0020611e669890e54369d55174b24c981f20f1626`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:27 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:31 GMT
ADD file:1ccdd7fca45ec88ba0ddda07e5e5acb6b40ddcb3023e0cbc04ffffdf4e30fb0a in / 
# Wed, 01 Oct 2025 13:02:31 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:52:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:52:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:52:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:52:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:52:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 18:51:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 18:51:17 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 18:51:17 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 18:51:17 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 18:51:17 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:51:17 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:51:17 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 18:51:17 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 18:51:17 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 18:51:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 10 Nov 2025 18:51:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 18:51:56 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 18:51:56 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 18:51:56 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:16:52 GMT
ENV GN_FILE=geonetwork.war
# Mon, 10 Nov 2025 19:16:52 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Mon, 10 Nov 2025 19:16:52 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Mon, 10 Nov 2025 19:16:52 GMT
ENV GN_VERSION=3.12.12
# Mon, 10 Nov 2025 19:16:52 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Mon, 10 Nov 2025 19:16:52 GMT
WORKDIR /usr/local/tomcat/webapps
# Mon, 10 Nov 2025 19:19:44 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Mon, 10 Nov 2025 19:19:44 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:19:44 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:19:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:19:44 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:36:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:36:28 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Mon, 10 Nov 2025 19:36:28 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Mon, 10 Nov 2025 19:36:28 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:36:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:36:28 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4afa85c5883c0db62b02025c149edaaa237af5ba25ea48039e875a802d465ac7`  
		Last Modified: Wed, 01 Oct 2025 18:03:16 GMT  
		Size: 26.9 MB (26851732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877d48b3edf53ed48debe07364b6988a7d485b8dc62b8695068f22bc14f16bd2`  
		Last Modified: Sat, 08 Nov 2025 17:53:17 GMT  
		Size: 16.3 MB (16306496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56962cfd33f391ca8f58fabb02890dc45b6f35aa3971d8a94c297e434a02af68`  
		Last Modified: Sat, 08 Nov 2025 17:53:33 GMT  
		Size: 50.1 MB (50145205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2d5ab79681429e656b55821f87a596bea3d26555ad21415247af253083c464`  
		Last Modified: Sat, 08 Nov 2025 17:53:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59807762691b1491fdf00347737e0e65361bafb9e0b2182ec0f250288b60f51e`  
		Last Modified: Sat, 08 Nov 2025 17:53:22 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe759f6e72937540ea0583957c10cb8c37816d1e78548efc6810cd2013e5374`  
		Last Modified: Mon, 10 Nov 2025 18:52:11 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be97b9e28aac7f0b895a8ce07ad96fdcd9d418334816e32d663bb75f74a5d8c8`  
		Last Modified: Mon, 10 Nov 2025 18:52:16 GMT  
		Size: 13.9 MB (13871638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f1187b918fef8441ef777d7cd39be469627563bf4638f7938977a5af7b2ec4`  
		Last Modified: Mon, 10 Nov 2025 19:36:07 GMT  
		Size: 234.5 MB (234538937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6191d06d9afdce2d96dea36f8eed00db34790d161d731d22770e5acaa941ff81`  
		Last Modified: Mon, 10 Nov 2025 19:20:26 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f12992cef2f5527f33e0d017e8016cdf730c597c803b05f233645800821d71`  
		Last Modified: Mon, 10 Nov 2025 19:36:53 GMT  
		Size: 13.0 MB (13004910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5dbec9e9cb3466835f50a6af574a7eb54833377006e4b51e4c569c08c0c5b65`  
		Last Modified: Mon, 10 Nov 2025 19:36:49 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2675d0ef251c232a8f150867ef2aae7560ec43580ac88b887ec7f3783b83466`  
		Last Modified: Mon, 10 Nov 2025 19:36:50 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f7b7f28ce6cfd42ba671edeed2cfc6d2ea1db29a284516daa8de7958afa736`  
		Last Modified: Mon, 10 Nov 2025 19:36:49 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:0f9237f5730c53f95a1cbc66cee9ddaeb3ff9630db69171b32e574378f209d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5939984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0f9a1a4041a7ddabea8f9c7c34e80f38f0617f0608a7501135b2dba36d191b`

```dockerfile
```

-	Layers:
	-	`sha256:173f5fafd605f6616457c1c6933df79a1ca8065b7a6f0a84c632e41f0de8168e`  
		Last Modified: Mon, 10 Nov 2025 22:12:45 GMT  
		Size: 5.9 MB (5917081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1176a2fba01239d3b277b0f797b1921ae88ab05df6bf55ccb0b76afff2226f29`  
		Last Modified: Mon, 10 Nov 2025 22:12:46 GMT  
		Size: 22.9 KB (22903 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:db8cff24871b1bde54dc2d1af24e632ac6990c3f5f773e51a9ecaa583ee909e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.1 MB (362114181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0feae438d37e432393cfdc30930626723af259e462126315f7f2af639bb58d1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:53:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:53:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:53:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:53:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:53:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 18:48:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 18:48:32 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 18:48:32 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 18:48:32 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 18:48:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:48:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 18:48:32 GMT
ENV TOMCAT_MAJOR=9
# Mon, 10 Nov 2025 18:48:32 GMT
ENV TOMCAT_VERSION=9.0.112
# Mon, 10 Nov 2025 18:48:32 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 18:49:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 10 Nov 2025 18:49:02 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 18:49:02 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 18:49:02 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 18:49:02 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:12:37 GMT
ENV GN_FILE=geonetwork.war
# Mon, 10 Nov 2025 19:12:37 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Mon, 10 Nov 2025 19:12:37 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Mon, 10 Nov 2025 19:12:37 GMT
ENV GN_VERSION=3.12.12
# Mon, 10 Nov 2025 19:12:37 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Mon, 10 Nov 2025 19:12:37 GMT
WORKDIR /usr/local/tomcat/webapps
# Mon, 10 Nov 2025 19:14:10 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Mon, 10 Nov 2025 19:14:10 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:14:10 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:14:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:14:10 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:36:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:36:55 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Mon, 10 Nov 2025 19:36:55 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Mon, 10 Nov 2025 19:36:55 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:36:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 19:36:55 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7705e10346edc5a4be243017fe5fc1b710ad4d93c6ca9ff4c006dfddbf7c730b`  
		Last Modified: Sat, 08 Nov 2025 17:53:40 GMT  
		Size: 17.0 MB (16989327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300c877d2da85ff91dfb5e728dcd643bbb53349d3a0cb32bfa183ede8a5da9e1`  
		Last Modified: Sat, 08 Nov 2025 17:53:43 GMT  
		Size: 53.8 MB (53819233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b075a0ea537a07303b1e7acf161b539998afb0ec51bbd70e28b4a5f132793026`  
		Last Modified: Sat, 08 Nov 2025 17:53:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e08d1eca77f725e234d2ee64762f6111cc25cb1045823cb05772b8d810edf3f`  
		Last Modified: Sat, 08 Nov 2025 17:53:39 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b010cd4714bd962e1de972c56137d400018846d475956941314dfa714d9c9b`  
		Last Modified: Mon, 10 Nov 2025 18:49:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f80972ce5475e44e69d42ced3357db1a0bab0060801a9bc671971fcb11d903`  
		Last Modified: Mon, 10 Nov 2025 18:49:16 GMT  
		Size: 14.0 MB (13974011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68ff0263f11155c4fd00e7197eb2a5bcfaf6b415b666f3f59696020abea07c0`  
		Last Modified: Mon, 10 Nov 2025 19:36:38 GMT  
		Size: 234.6 MB (234554416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b82d2a06a49c482fb88db6f5cdc91921dbc403ab1b5191d9b0aa4cd0379ce0`  
		Last Modified: Mon, 10 Nov 2025 19:14:45 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab84e2a2ae1aee44bd58f903627c88e12c432ef05ffce964ed472152d16d1cc`  
		Last Modified: Mon, 10 Nov 2025 19:37:19 GMT  
		Size: 13.9 MB (13909111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bef0f8ea32ed89348873ef56018f0b353fec9ad1797a1f815c213effeca26e`  
		Last Modified: Mon, 10 Nov 2025 19:37:18 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2018b49f408f8abdf72bd36f6dbccdb37621b29455c644616a5d281b3d6f8b63`  
		Last Modified: Mon, 10 Nov 2025 19:37:18 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa436aacb9348a140a010e571a4d962124faf1f91f03363adf6d41aea55d8875`  
		Last Modified: Mon, 10 Nov 2025 19:37:19 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:b25e09aa6cbdf34ed4b92c0a2a898380bdb66df9b5eff87efa49201ea6d13783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5944500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d98ff0dfd66a991f6c6293d94d84999e1c0ea3ed7de9e2734fab22ee197b848`

```dockerfile
```

-	Layers:
	-	`sha256:f315f51b9f6d69075b7b9657c4f0743c7b1e574913e5afc19249cd5528870896`  
		Last Modified: Mon, 10 Nov 2025 22:12:51 GMT  
		Size: 5.9 MB (5921574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a597e03d7627c894b6728b3583fe3f7844cb81943f185cb3022f28099cbf9c8`  
		Last Modified: Mon, 10 Nov 2025 22:12:52 GMT  
		Size: 22.9 KB (22926 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:11ba94b34ba69f4d3cfa3455027329d22efc8079a0d990ed491a9ef1efa6f8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.3 MB (368343861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347fe03f5a28550d1aaae200ea5d4a684dc5a1b104dbae027a702bc52c9f7db4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:54:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:54:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:54:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:54:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:54:06 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:54:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:54:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:54:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:54:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 19:00:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 19:00:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:00:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 19:00:00 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 19:00:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:00:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:00:00 GMT
ENV TOMCAT_MAJOR=9
# Sat, 08 Nov 2025 19:00:00 GMT
ENV TOMCAT_VERSION=9.0.112
# Sat, 08 Nov 2025 19:00:00 GMT
ENV TOMCAT_SHA512=fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d
# Mon, 10 Nov 2025 19:47:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Mon, 10 Nov 2025 19:47:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 19:47:13 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 19:47:13 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 19:47:13 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 23:15:49 GMT
ENV GN_FILE=geonetwork.war
# Mon, 10 Nov 2025 23:15:49 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Mon, 10 Nov 2025 23:15:49 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Mon, 10 Nov 2025 23:15:49 GMT
ENV GN_VERSION=3.12.12
# Mon, 10 Nov 2025 23:15:49 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Mon, 10 Nov 2025 23:15:49 GMT
WORKDIR /usr/local/tomcat/webapps
# Mon, 10 Nov 2025 23:16:50 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Mon, 10 Nov 2025 23:16:51 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Nov 2025 23:16:51 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 23:16:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Nov 2025 23:16:51 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Nov 2025 00:10:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 00:10:39 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 11 Nov 2025 00:10:40 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 11 Nov 2025 00:10:40 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 11 Nov 2025 00:10:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Nov 2025 00:10:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c3c84c9145d6e39b87361420c42775001b0a5d2bff0b29876f0b582e69bdbf`  
		Last Modified: Sat, 08 Nov 2025 17:54:48 GMT  
		Size: 18.8 MB (18814703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5833a946e93b9fd592425a2c130d2de3d0c47593502ca8696c622ae4d8a7a466`  
		Last Modified: Sat, 08 Nov 2025 17:54:53 GMT  
		Size: 52.2 MB (52180251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e96f2543d1efb4f969021c1fa90b3c36fe7d87795d9d65bb5b40fd63941bd62`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecae247d1136bdf5a3d1676b8e621b72e8b646217244cbcacec857c4095be5e8`  
		Last Modified: Sat, 08 Nov 2025 17:54:47 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55c44ff40e732795c22184283a33627cae1d4475a0ba1545977662e9b12053c`  
		Last Modified: Sat, 08 Nov 2025 19:01:20 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb71e9ee01c5de6dcc1e68621bd3649db78416b092acfe6acd5bf768a8016e2a`  
		Last Modified: Mon, 10 Nov 2025 19:47:52 GMT  
		Size: 14.0 MB (14032068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7b4dbb58f4018ad3e2ad4a31cff19d9d3af990cdb6ce705ee65893bb56b7d0`  
		Last Modified: Tue, 11 Nov 2025 01:18:31 GMT  
		Size: 234.6 MB (234574715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eae6068bfbfc6a3312ccfecf204b6867076155896b466581266c6a72f1b3daa`  
		Last Modified: Mon, 10 Nov 2025 23:17:53 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c466a80722ecbdc59bd564466ade99d5e77be3e32ed912cfa9dbf18da9bd86b7`  
		Last Modified: Tue, 11 Nov 2025 00:11:17 GMT  
		Size: 14.4 MB (14432223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1cd8126c4d88a6fb87cf54154d9874ebd79198f7e3cf74195c72105589f0b7`  
		Last Modified: Tue, 11 Nov 2025 00:11:16 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a287d7754504dc2f0b8c7ed4ac4e10ec33cd34d25f9546e159fec00846e17637`  
		Last Modified: Tue, 11 Nov 2025 00:11:16 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa028cb003c3b3f570914d7b29812c2eb2614e3c84520b131e3bf6c4623c5c16`  
		Last Modified: Tue, 11 Nov 2025 00:11:16 GMT  
		Size: 975.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:2e62fddc29b3de849fd3f494fc610ec93c0aabac54e3bad0f36be003e59b919f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcee9f27a84b7b4fa2fc3108c305f6018da73316f22318018ed56a126859bfb8`

```dockerfile
```

-	Layers:
	-	`sha256:63f947b10b73d3712472c3f99d23847ea2f2ecef66d6935655764c11c2b09b9f`  
		Last Modified: Tue, 11 Nov 2025 01:12:35 GMT  
		Size: 5.9 MB (5919870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4520def069181df2ef90ea92e652a7cbcb712f32a8c6087ad1f0fec72768a63`  
		Last Modified: Tue, 11 Nov 2025 01:12:36 GMT  
		Size: 22.9 KB (22859 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4`

```console
$ docker pull geonetwork@sha256:30033b7ef02432cd6813e1e9fa075ce07675851421d4490a3404884635dab9de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:4` - linux; amd64

```console
$ docker pull geonetwork@sha256:699e2cfc09ba7e0ef0d221b03527b651fdce80b4e927c537606e059f80de1b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.2 MB (396169507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c47d7abb026459f91a0a61675443713d93f73a81380b176ae7a373fdbe68c9`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:57:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:57:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:57:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:57:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:57:23 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Sat, 08 Nov 2025 17:57:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93454a64c922111e57a86659e5fd6d44406173226cf051aa6228af06a7a44a56';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:57:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:57:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:57:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:26:05 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Sat, 08 Nov 2025 18:26:05 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 08 Nov 2025 18:26:05 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 08 Nov 2025 18:26:05 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 08 Nov 2025 18:26:05 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:26:05 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Sat, 08 Nov 2025 18:26:05 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 08 Nov 2025 18:26:05 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Sat, 08 Nov 2025 18:26:05 GMT
WORKDIR /var/lib/jetty
# Sat, 08 Nov 2025 18:26:05 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Sat, 08 Nov 2025 18:26:05 GMT
USER jetty
# Sat, 08 Nov 2025 18:26:05 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 18:26:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:26:05 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Sat, 08 Nov 2025 19:21:21 GMT
ENV DATA_DIR=/catalogue-data
# Sat, 08 Nov 2025 19:21:21 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Sat, 08 Nov 2025 19:21:21 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Sat, 08 Nov 2025 19:21:21 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Sat, 08 Nov 2025 19:21:21 GMT
USER root
# Sat, 08 Nov 2025 19:21:21 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Sat, 08 Nov 2025 19:21:21 GMT
USER jetty
# Sat, 08 Nov 2025 19:21:21 GMT
ENV GN_FILE=geonetwork.war
# Sat, 08 Nov 2025 19:21:21 GMT
ENV GN_VERSION=4.4.9
# Sat, 08 Nov 2025 19:21:21 GMT
ENV GN_DOWNLOAD_MD5=03104df014c7a96dccf96e421267fd9f
# Sat, 08 Nov 2025 19:21:43 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Sat, 08 Nov 2025 19:21:43 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Sat, 08 Nov 2025 19:21:43 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:21:43 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Sat, 08 Nov 2025 19:21:43 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Sat, 08 Nov 2025 19:21:43 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Sat, 08 Nov 2025 19:21:43 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f89bfb3dd44266ed9543fe4604ff43b977ac927f5a38fc36e717be3eb1a36d`  
		Last Modified: Sat, 08 Nov 2025 17:57:47 GMT  
		Size: 17.0 MB (16972157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d8a69d2f75841282cb462236d1b5ce986bb6e141bd754efc97151cb24f1e27`  
		Last Modified: Sat, 08 Nov 2025 17:57:49 GMT  
		Size: 46.9 MB (46883770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa491fab65db66954d3ec2de490cefdbcfbb6d1539d4c15049f7ed4d8bbeea38`  
		Last Modified: Sat, 08 Nov 2025 17:57:43 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6abb69c3f3572d87d1ea62fa296ee988fda9b9d1c9d8f7d00a8b9902d34151`  
		Last Modified: Sat, 08 Nov 2025 17:57:43 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bf707f49abf0cf1342307382eeda957d815dda191e89abbf13bbad565421b8`  
		Last Modified: Sat, 08 Nov 2025 18:26:19 GMT  
		Size: 10.4 MB (10364488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57f29cc22f1af68be6c7c0ef3f6aa060910f54cb3392b9cda95b508055a0b47`  
		Last Modified: Sat, 08 Nov 2025 18:26:07 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ba39aaf3937f1b67cfb3c0d1ef4a020de1785827c9566f9d3000b0ed768e5f`  
		Last Modified: Sat, 08 Nov 2025 19:22:19 GMT  
		Size: 238.9 KB (238892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ce94c5e1b520f18a44835d4cebe74e8a927c991e9b3e434234abb0d10271ae`  
		Last Modified: Sat, 08 Nov 2025 23:05:19 GMT  
		Size: 292.0 MB (291981483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9982e2fae4417c8a89c6c62c8ff744d09ef33f300eb7fd8b7f994921631d27`  
		Last Modified: Sat, 08 Nov 2025 19:22:19 GMT  
		Size: 550.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab195e7da4a2251707291b71f4273a85303f2fec505af9f32a15bf3ec1c76c3`  
		Last Modified: Sat, 08 Nov 2025 19:22:19 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9ac4c42ec89ca62bf7afc579dcada7be447a20a6b865a977da970a7c95616a`  
		Last Modified: Sat, 08 Nov 2025 19:22:19 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:9c71731d0bf0847b72e315a4d18f0cead3458a2bb560e362ca47d650fb130691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41339941ec8ab8dc4b5a7f49dfc4d6a45ecb5d505fa329c1209870ff59505e1b`

```dockerfile
```

-	Layers:
	-	`sha256:1d157b650e63ed76dba73c752c8aff1987125550c82310ddd34de3bb2e9cee87`  
		Last Modified: Sat, 08 Nov 2025 22:13:05 GMT  
		Size: 4.2 MB (4219655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e19f5670a702c72d3c89b991842170f24ae8d01d94d68fbc3831f315064a00ac`  
		Last Modified: Sat, 08 Nov 2025 22:13:06 GMT  
		Size: 25.7 KB (25654 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:21f294eb7bcb019debff8c48c0bbb4cb09aaaf7eb36c201b9780117958393046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.7 MB (393664156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025a875c8a00116435a7f95242a8731ac351017b65c0a31b4bedaa6f471f2b99`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:57:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:57:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:57:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:57:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:57:32 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Sat, 08 Nov 2025 17:57:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93454a64c922111e57a86659e5fd6d44406173226cf051aa6228af06a7a44a56';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:57:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:57:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:57:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:26:17 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Sat, 08 Nov 2025 18:26:17 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 08 Nov 2025 18:26:17 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 08 Nov 2025 18:26:17 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 08 Nov 2025 18:26:17 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:26:17 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Sat, 08 Nov 2025 18:26:17 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 08 Nov 2025 18:26:17 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Sat, 08 Nov 2025 18:26:17 GMT
WORKDIR /var/lib/jetty
# Sat, 08 Nov 2025 18:26:17 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Sat, 08 Nov 2025 18:26:17 GMT
USER jetty
# Sat, 08 Nov 2025 18:26:17 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 18:26:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:26:17 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Sat, 08 Nov 2025 19:20:57 GMT
ENV DATA_DIR=/catalogue-data
# Sat, 08 Nov 2025 19:20:57 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Sat, 08 Nov 2025 19:20:57 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Sat, 08 Nov 2025 19:20:57 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Sat, 08 Nov 2025 19:20:57 GMT
USER root
# Sat, 08 Nov 2025 19:20:57 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Sat, 08 Nov 2025 19:20:57 GMT
USER jetty
# Sat, 08 Nov 2025 19:20:57 GMT
ENV GN_FILE=geonetwork.war
# Sat, 08 Nov 2025 19:20:57 GMT
ENV GN_VERSION=4.4.9
# Sat, 08 Nov 2025 19:20:57 GMT
ENV GN_DOWNLOAD_MD5=03104df014c7a96dccf96e421267fd9f
# Sat, 08 Nov 2025 19:21:18 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Sat, 08 Nov 2025 19:21:18 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Sat, 08 Nov 2025 19:21:18 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:21:19 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Sat, 08 Nov 2025 19:21:19 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Sat, 08 Nov 2025 19:21:19 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Sat, 08 Nov 2025 19:21:19 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f7654790c24728ffca0008db3fdf1df7faeb35641e71a0dbdd99dfb65ed007`  
		Last Modified: Sat, 08 Nov 2025 17:58:00 GMT  
		Size: 17.0 MB (16989385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9563970e8499be18387be96ca2b854d6c9ceec66e01fb7b4ec308468b5173701`  
		Last Modified: Sat, 08 Nov 2025 17:58:04 GMT  
		Size: 45.2 MB (45223033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a2ad96e4ba9ad2d9e7546a1385f36f4d4aefd9ac27762729c5c8b31f031ed5`  
		Last Modified: Sat, 08 Nov 2025 17:57:59 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb2bb049339afc486316d635a5e6027854bc90e756db1a4ebc2c0aed2190e14`  
		Last Modified: Sat, 08 Nov 2025 17:58:00 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bc309a635f2ee33d4caccce4f58593a67daa287b38e24728f5eb2a39b2ec48`  
		Last Modified: Sat, 08 Nov 2025 18:26:33 GMT  
		Size: 10.4 MB (10364809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe900a1b703153ab53dff2140bf884a1055f13b8de02489310fcbdbe4a9c8c70`  
		Last Modified: Sat, 08 Nov 2025 18:26:32 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0426a0f560b06fdd8d0816f5b0e5a46af6a95d4cf6f50e2d98165c016d68f498`  
		Last Modified: Sat, 08 Nov 2025 19:21:56 GMT  
		Size: 238.2 KB (238168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03575b79a75d094a0c7d949858201f0b533b78b9f4495072bdfb406004327d8`  
		Last Modified: Sat, 08 Nov 2025 23:04:52 GMT  
		Size: 292.0 MB (291981479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58b62a250e862e3e61c9de095e2f0048bacf37aba662c20155c437003d6eb04`  
		Last Modified: Sat, 08 Nov 2025 19:21:56 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a563f5c880a269b681e06dbdcc097924eae26c312ab98b6a00a29d1c2942f1d3`  
		Last Modified: Sat, 08 Nov 2025 19:21:56 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6eaf3eec605064a1dbae8cdec9cd29da950795c6e4aa9c47ee590a5a84b289`  
		Last Modified: Sat, 08 Nov 2025 19:21:56 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:74efade6d2af35edb4a5f79af119698b8e0397e3816b2a5d9bcb70198577c8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4246529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3bb33f74d526fc8c85b1090c27a9d6fb17f9dea9752d143e88dffd28cb71e9`

```dockerfile
```

-	Layers:
	-	`sha256:a2eb97c45fdf0626a99ad3e7e866ae2f98cc6c343207ec672b707f110df74d74`  
		Last Modified: Sat, 08 Nov 2025 22:13:11 GMT  
		Size: 4.2 MB (4220740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68cb61befcfe21dc26e866ba3e94403fd5ea54252533b89ef507c3f889fe1df8`  
		Last Modified: Sat, 08 Nov 2025 22:13:11 GMT  
		Size: 25.8 KB (25789 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.2`

```console
$ docker pull geonetwork@sha256:05ee577ee53a81cc23f8b0f5e98ebd354f255e3c049d238862a72972bf9b2540
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:4.2` - linux; amd64

```console
$ docker pull geonetwork@sha256:60d65aa51c4dcdb5e31ee73e2a8f070f170a2523841642799abe9a4aaef94d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.1 MB (364131932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4b00eb503ab50ed76c1d5253ca2f7aaa637bf4f7034909bd8d7d130ef33652`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:56:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:56:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:56:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:56:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:56:44 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:56:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='25896dbbd14240d789d1b88d66d76a534b42e857c8ec17d0bf031708d9836241';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:56:46 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:56:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:56:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:25:58 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Sat, 08 Nov 2025 18:25:58 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 08 Nov 2025 18:25:58 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 08 Nov 2025 18:25:58 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 08 Nov 2025 18:25:58 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:25:58 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Sat, 08 Nov 2025 18:25:58 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 08 Nov 2025 18:25:58 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Sat, 08 Nov 2025 18:25:58 GMT
WORKDIR /var/lib/jetty
# Sat, 08 Nov 2025 18:25:58 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Sat, 08 Nov 2025 18:25:58 GMT
USER jetty
# Sat, 08 Nov 2025 18:25:58 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 18:25:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:25:58 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Sat, 08 Nov 2025 19:21:19 GMT
ENV DATA_DIR=/catalogue-data
# Sat, 08 Nov 2025 19:21:19 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom         -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Sat, 08 Nov 2025 19:21:19 GMT
USER root
# Sat, 08 Nov 2025 19:21:19 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork # buildkit
# Sat, 08 Nov 2025 19:21:19 GMT
USER jetty
# Sat, 08 Nov 2025 19:21:19 GMT
ENV GN_FILE=geonetwork.war
# Sat, 08 Nov 2025 19:21:19 GMT
ENV GN_VERSION=4.2.14
# Sat, 08 Nov 2025 19:21:19 GMT
ENV GN_DOWNLOAD_MD5=1e53b8d5f98c28b1c08657c24f7f9581
# Sat, 08 Nov 2025 19:22:18 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Sat, 08 Nov 2025 19:22:18 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:22:18 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Sat, 08 Nov 2025 19:22:18 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Sat, 08 Nov 2025 19:22:18 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ff51bd88b17a4b71c3855e946e7d0a32ce8fd47acf57730e221abbf02a5500`  
		Last Modified: Sat, 08 Nov 2025 17:57:10 GMT  
		Size: 17.0 MB (16972115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d085363653f2a2c7b1fac6006bd16615f2db16ed021027b0ec645bfe99da07`  
		Last Modified: Sat, 08 Nov 2025 17:57:11 GMT  
		Size: 41.9 MB (41891236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccbd3e9ed5a3534b12f7269822387c33fd2c2c75e624afc9089be4bf02a9d66`  
		Last Modified: Sat, 08 Nov 2025 17:57:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767c2f322c6eed60599c95fb313afb8bd8918a5aafc2cb907c59e86c5259a703`  
		Last Modified: Sat, 08 Nov 2025 17:57:08 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e0033faf0f6466e1c0abfaa7cc166b5dbf7b244ff481967929b032c23de940`  
		Last Modified: Sat, 08 Nov 2025 18:26:13 GMT  
		Size: 10.4 MB (10364464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c75ae4b4cffcba9162f8ee542b8b385d4b777e4559246dccdba3c3bf9e9cef5`  
		Last Modified: Sat, 08 Nov 2025 18:26:13 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c46769972b97f1ed22c97133dbeb708f631ddae0c3b00352761057ae2aae04`  
		Last Modified: Sat, 08 Nov 2025 20:50:03 GMT  
		Size: 239.0 KB (238953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b93d7bfae58f5b3b5f17da769b4effb52295ea442e776c50abe7db9b65d8e3e`  
		Last Modified: Sun, 09 Nov 2025 23:05:12 GMT  
		Size: 264.9 MB (264936764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4afdfe11c14852a448cc19f65dfa5dbf760818eb8c8fa08dd29c29333081b72`  
		Last Modified: Sat, 08 Nov 2025 20:50:03 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2` - unknown; unknown

```console
$ docker pull geonetwork@sha256:e85f3ff2c8da0c72db5a054eb2e6b9aca9a9d792248ed0fad5d32d79293b92c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f230843e6c5ebf6a10420b165aa8f5e83fdac7b2de5f941ded6cf1e5490c5a4`

```dockerfile
```

-	Layers:
	-	`sha256:2f22519da769c044e9d8fcb69ad6df12f241ace01c302dc76086067a4d031ca3`  
		Last Modified: Sat, 08 Nov 2025 22:13:13 GMT  
		Size: 4.2 MB (4209822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2d06f45bb89b10cb3525a894f3b94fe3fe8590406e17d06a99f195a92b19bd0`  
		Last Modified: Sat, 08 Nov 2025 22:13:14 GMT  
		Size: 18.7 KB (18697 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.2` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:280e988f7d41db8a115953716960866c272f57f488caba566a6a80cefae08fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.3 MB (362280512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9ab20e2bad7ceef54238e350f1d4631e43bc15949779b295d9fe2c6af97bcc`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:53:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:53:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:53:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:55:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='25896dbbd14240d789d1b88d66d76a534b42e857c8ec17d0bf031708d9836241';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:55:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:55:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:55:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:26:06 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Sat, 08 Nov 2025 18:26:06 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 08 Nov 2025 18:26:06 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 08 Nov 2025 18:26:06 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 08 Nov 2025 18:26:06 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:26:06 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Sat, 08 Nov 2025 18:26:06 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 08 Nov 2025 18:26:06 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Sat, 08 Nov 2025 18:26:06 GMT
WORKDIR /var/lib/jetty
# Sat, 08 Nov 2025 18:26:06 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Sat, 08 Nov 2025 18:26:06 GMT
USER jetty
# Sat, 08 Nov 2025 18:26:06 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 18:26:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:26:06 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Sat, 08 Nov 2025 19:20:57 GMT
ENV DATA_DIR=/catalogue-data
# Sat, 08 Nov 2025 19:20:57 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom         -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Sat, 08 Nov 2025 19:20:57 GMT
USER root
# Sat, 08 Nov 2025 19:20:57 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork # buildkit
# Sat, 08 Nov 2025 19:20:57 GMT
USER jetty
# Sat, 08 Nov 2025 19:20:57 GMT
ENV GN_FILE=geonetwork.war
# Sat, 08 Nov 2025 19:20:57 GMT
ENV GN_VERSION=4.2.14
# Sat, 08 Nov 2025 19:20:57 GMT
ENV GN_DOWNLOAD_MD5=1e53b8d5f98c28b1c08657c24f7f9581
# Sat, 08 Nov 2025 19:22:06 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Sat, 08 Nov 2025 19:22:06 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:22:06 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Sat, 08 Nov 2025 19:22:06 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Sat, 08 Nov 2025 19:22:06 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7705e10346edc5a4be243017fe5fc1b710ad4d93c6ca9ff4c006dfddbf7c730b`  
		Last Modified: Sat, 08 Nov 2025 17:53:40 GMT  
		Size: 17.0 MB (16989327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71ec760f0edecd945494f78573e581ac956b186ac2427ae2556a154015d6ddb`  
		Last Modified: Sat, 08 Nov 2025 17:55:55 GMT  
		Size: 40.9 MB (40884346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707ff7a3bc37e72f31e6be8a17f71c4ae76d37e953e78a3bbfd2ace40f6970bd`  
		Last Modified: Sat, 08 Nov 2025 17:55:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d17d2cf675ca4803bedad41d2b12efb7f511d661215860b0a0856e84d3059d3`  
		Last Modified: Sat, 08 Nov 2025 17:55:52 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeb5c79ddcdc9a9dd6e34d7091cda21eec3ca0052abc67394620d7c8908166b`  
		Last Modified: Sat, 08 Nov 2025 18:26:19 GMT  
		Size: 10.4 MB (10364823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55b1db81728c1c6aa3bb6ecce8f6623bcb66f49fc36cc029e379e5af631eb3f`  
		Last Modified: Sat, 08 Nov 2025 18:26:06 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3654827057d51359a11e968a7fbad076bcf5ea84dab2f0a4e83135d4753d5ca4`  
		Last Modified: Sat, 08 Nov 2025 19:22:39 GMT  
		Size: 238.2 KB (238243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d62be7c17adbca49c61a9462f8514dc3981faab21530995a30048919bc581e`  
		Last Modified: Mon, 10 Nov 2025 07:24:54 GMT  
		Size: 264.9 MB (264936809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f86461d9185d323bae43e16c45a32fee4b10b928c8f926450f68be7f33973a`  
		Last Modified: Sat, 08 Nov 2025 19:22:39 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2` - unknown; unknown

```console
$ docker pull geonetwork@sha256:62d74ad42fbb6e1ad27a2f55ac478318cbbc2b7b0fd1682a75ee7cf44b1fd170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4229755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6006eeb10de934d0d87814db7406702856e8ad9b4cfb0eedd35b964f16c48b5`

```dockerfile
```

-	Layers:
	-	`sha256:16b43d50e7637de895eed0d43f74628faa4216f6af54ef341ee56008b68e4fa3`  
		Last Modified: Sat, 08 Nov 2025 22:13:18 GMT  
		Size: 4.2 MB (4210963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ef2aea03b35138b3c33db01a9b8e0012c1c9b85ba20882b9315a8d3ff4ea7b2`  
		Last Modified: Sat, 08 Nov 2025 22:13:19 GMT  
		Size: 18.8 KB (18792 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.2.14`

```console
$ docker pull geonetwork@sha256:05ee577ee53a81cc23f8b0f5e98ebd354f255e3c049d238862a72972bf9b2540
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:4.2.14` - linux; amd64

```console
$ docker pull geonetwork@sha256:60d65aa51c4dcdb5e31ee73e2a8f070f170a2523841642799abe9a4aaef94d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.1 MB (364131932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4b00eb503ab50ed76c1d5253ca2f7aaa637bf4f7034909bd8d7d130ef33652`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:56:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:56:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:56:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:56:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:56:44 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:56:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='25896dbbd14240d789d1b88d66d76a534b42e857c8ec17d0bf031708d9836241';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:56:46 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:56:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:56:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:25:58 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Sat, 08 Nov 2025 18:25:58 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 08 Nov 2025 18:25:58 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 08 Nov 2025 18:25:58 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 08 Nov 2025 18:25:58 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:25:58 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Sat, 08 Nov 2025 18:25:58 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 08 Nov 2025 18:25:58 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Sat, 08 Nov 2025 18:25:58 GMT
WORKDIR /var/lib/jetty
# Sat, 08 Nov 2025 18:25:58 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Sat, 08 Nov 2025 18:25:58 GMT
USER jetty
# Sat, 08 Nov 2025 18:25:58 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 18:25:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:25:58 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Sat, 08 Nov 2025 19:21:19 GMT
ENV DATA_DIR=/catalogue-data
# Sat, 08 Nov 2025 19:21:19 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom         -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Sat, 08 Nov 2025 19:21:19 GMT
USER root
# Sat, 08 Nov 2025 19:21:19 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork # buildkit
# Sat, 08 Nov 2025 19:21:19 GMT
USER jetty
# Sat, 08 Nov 2025 19:21:19 GMT
ENV GN_FILE=geonetwork.war
# Sat, 08 Nov 2025 19:21:19 GMT
ENV GN_VERSION=4.2.14
# Sat, 08 Nov 2025 19:21:19 GMT
ENV GN_DOWNLOAD_MD5=1e53b8d5f98c28b1c08657c24f7f9581
# Sat, 08 Nov 2025 19:22:18 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Sat, 08 Nov 2025 19:22:18 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:22:18 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Sat, 08 Nov 2025 19:22:18 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Sat, 08 Nov 2025 19:22:18 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ff51bd88b17a4b71c3855e946e7d0a32ce8fd47acf57730e221abbf02a5500`  
		Last Modified: Sat, 08 Nov 2025 17:57:10 GMT  
		Size: 17.0 MB (16972115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d085363653f2a2c7b1fac6006bd16615f2db16ed021027b0ec645bfe99da07`  
		Last Modified: Sat, 08 Nov 2025 17:57:11 GMT  
		Size: 41.9 MB (41891236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccbd3e9ed5a3534b12f7269822387c33fd2c2c75e624afc9089be4bf02a9d66`  
		Last Modified: Sat, 08 Nov 2025 17:57:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767c2f322c6eed60599c95fb313afb8bd8918a5aafc2cb907c59e86c5259a703`  
		Last Modified: Sat, 08 Nov 2025 17:57:08 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e0033faf0f6466e1c0abfaa7cc166b5dbf7b244ff481967929b032c23de940`  
		Last Modified: Sat, 08 Nov 2025 18:26:13 GMT  
		Size: 10.4 MB (10364464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c75ae4b4cffcba9162f8ee542b8b385d4b777e4559246dccdba3c3bf9e9cef5`  
		Last Modified: Sat, 08 Nov 2025 18:26:13 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c46769972b97f1ed22c97133dbeb708f631ddae0c3b00352761057ae2aae04`  
		Last Modified: Sat, 08 Nov 2025 20:50:03 GMT  
		Size: 239.0 KB (238953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b93d7bfae58f5b3b5f17da769b4effb52295ea442e776c50abe7db9b65d8e3e`  
		Last Modified: Sun, 09 Nov 2025 23:05:12 GMT  
		Size: 264.9 MB (264936764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4afdfe11c14852a448cc19f65dfa5dbf760818eb8c8fa08dd29c29333081b72`  
		Last Modified: Sat, 08 Nov 2025 20:50:03 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2.14` - unknown; unknown

```console
$ docker pull geonetwork@sha256:e85f3ff2c8da0c72db5a054eb2e6b9aca9a9d792248ed0fad5d32d79293b92c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f230843e6c5ebf6a10420b165aa8f5e83fdac7b2de5f941ded6cf1e5490c5a4`

```dockerfile
```

-	Layers:
	-	`sha256:2f22519da769c044e9d8fcb69ad6df12f241ace01c302dc76086067a4d031ca3`  
		Last Modified: Sat, 08 Nov 2025 22:13:13 GMT  
		Size: 4.2 MB (4209822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2d06f45bb89b10cb3525a894f3b94fe3fe8590406e17d06a99f195a92b19bd0`  
		Last Modified: Sat, 08 Nov 2025 22:13:14 GMT  
		Size: 18.7 KB (18697 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.2.14` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:280e988f7d41db8a115953716960866c272f57f488caba566a6a80cefae08fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.3 MB (362280512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9ab20e2bad7ceef54238e350f1d4631e43bc15949779b295d9fe2c6af97bcc`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:53:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:53:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:53:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:53:16 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 17:55:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='25896dbbd14240d789d1b88d66d76a534b42e857c8ec17d0bf031708d9836241';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sat, 08 Nov 2025 17:55:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:55:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:55:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:26:06 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Sat, 08 Nov 2025 18:26:06 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 08 Nov 2025 18:26:06 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 08 Nov 2025 18:26:06 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 08 Nov 2025 18:26:06 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:26:06 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Sat, 08 Nov 2025 18:26:06 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 08 Nov 2025 18:26:06 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Sat, 08 Nov 2025 18:26:06 GMT
WORKDIR /var/lib/jetty
# Sat, 08 Nov 2025 18:26:06 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Sat, 08 Nov 2025 18:26:06 GMT
USER jetty
# Sat, 08 Nov 2025 18:26:06 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 18:26:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:26:06 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Sat, 08 Nov 2025 19:20:57 GMT
ENV DATA_DIR=/catalogue-data
# Sat, 08 Nov 2025 19:20:57 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom         -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Sat, 08 Nov 2025 19:20:57 GMT
USER root
# Sat, 08 Nov 2025 19:20:57 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork # buildkit
# Sat, 08 Nov 2025 19:20:57 GMT
USER jetty
# Sat, 08 Nov 2025 19:20:57 GMT
ENV GN_FILE=geonetwork.war
# Sat, 08 Nov 2025 19:20:57 GMT
ENV GN_VERSION=4.2.14
# Sat, 08 Nov 2025 19:20:57 GMT
ENV GN_DOWNLOAD_MD5=1e53b8d5f98c28b1c08657c24f7f9581
# Sat, 08 Nov 2025 19:22:06 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Sat, 08 Nov 2025 19:22:06 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:22:06 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Sat, 08 Nov 2025 19:22:06 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Sat, 08 Nov 2025 19:22:06 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7705e10346edc5a4be243017fe5fc1b710ad4d93c6ca9ff4c006dfddbf7c730b`  
		Last Modified: Sat, 08 Nov 2025 17:53:40 GMT  
		Size: 17.0 MB (16989327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71ec760f0edecd945494f78573e581ac956b186ac2427ae2556a154015d6ddb`  
		Last Modified: Sat, 08 Nov 2025 17:55:55 GMT  
		Size: 40.9 MB (40884346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707ff7a3bc37e72f31e6be8a17f71c4ae76d37e953e78a3bbfd2ace40f6970bd`  
		Last Modified: Sat, 08 Nov 2025 17:55:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d17d2cf675ca4803bedad41d2b12efb7f511d661215860b0a0856e84d3059d3`  
		Last Modified: Sat, 08 Nov 2025 17:55:52 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeb5c79ddcdc9a9dd6e34d7091cda21eec3ca0052abc67394620d7c8908166b`  
		Last Modified: Sat, 08 Nov 2025 18:26:19 GMT  
		Size: 10.4 MB (10364823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55b1db81728c1c6aa3bb6ecce8f6623bcb66f49fc36cc029e379e5af631eb3f`  
		Last Modified: Sat, 08 Nov 2025 18:26:06 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3654827057d51359a11e968a7fbad076bcf5ea84dab2f0a4e83135d4753d5ca4`  
		Last Modified: Sat, 08 Nov 2025 19:22:39 GMT  
		Size: 238.2 KB (238243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d62be7c17adbca49c61a9462f8514dc3981faab21530995a30048919bc581e`  
		Last Modified: Mon, 10 Nov 2025 07:24:54 GMT  
		Size: 264.9 MB (264936809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f86461d9185d323bae43e16c45a32fee4b10b928c8f926450f68be7f33973a`  
		Last Modified: Sat, 08 Nov 2025 19:22:39 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2.14` - unknown; unknown

```console
$ docker pull geonetwork@sha256:62d74ad42fbb6e1ad27a2f55ac478318cbbc2b7b0fd1682a75ee7cf44b1fd170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4229755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6006eeb10de934d0d87814db7406702856e8ad9b4cfb0eedd35b964f16c48b5`

```dockerfile
```

-	Layers:
	-	`sha256:16b43d50e7637de895eed0d43f74628faa4216f6af54ef341ee56008b68e4fa3`  
		Last Modified: Sat, 08 Nov 2025 22:13:18 GMT  
		Size: 4.2 MB (4210963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ef2aea03b35138b3c33db01a9b8e0012c1c9b85ba20882b9315a8d3ff4ea7b2`  
		Last Modified: Sat, 08 Nov 2025 22:13:19 GMT  
		Size: 18.8 KB (18792 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.4`

```console
$ docker pull geonetwork@sha256:30033b7ef02432cd6813e1e9fa075ce07675851421d4490a3404884635dab9de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:4.4` - linux; amd64

```console
$ docker pull geonetwork@sha256:699e2cfc09ba7e0ef0d221b03527b651fdce80b4e927c537606e059f80de1b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.2 MB (396169507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c47d7abb026459f91a0a61675443713d93f73a81380b176ae7a373fdbe68c9`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:57:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:57:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:57:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:57:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:57:23 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Sat, 08 Nov 2025 17:57:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93454a64c922111e57a86659e5fd6d44406173226cf051aa6228af06a7a44a56';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:57:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:57:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:57:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:26:05 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Sat, 08 Nov 2025 18:26:05 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 08 Nov 2025 18:26:05 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 08 Nov 2025 18:26:05 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 08 Nov 2025 18:26:05 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:26:05 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Sat, 08 Nov 2025 18:26:05 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 08 Nov 2025 18:26:05 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Sat, 08 Nov 2025 18:26:05 GMT
WORKDIR /var/lib/jetty
# Sat, 08 Nov 2025 18:26:05 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Sat, 08 Nov 2025 18:26:05 GMT
USER jetty
# Sat, 08 Nov 2025 18:26:05 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 18:26:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:26:05 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Sat, 08 Nov 2025 19:21:21 GMT
ENV DATA_DIR=/catalogue-data
# Sat, 08 Nov 2025 19:21:21 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Sat, 08 Nov 2025 19:21:21 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Sat, 08 Nov 2025 19:21:21 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Sat, 08 Nov 2025 19:21:21 GMT
USER root
# Sat, 08 Nov 2025 19:21:21 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Sat, 08 Nov 2025 19:21:21 GMT
USER jetty
# Sat, 08 Nov 2025 19:21:21 GMT
ENV GN_FILE=geonetwork.war
# Sat, 08 Nov 2025 19:21:21 GMT
ENV GN_VERSION=4.4.9
# Sat, 08 Nov 2025 19:21:21 GMT
ENV GN_DOWNLOAD_MD5=03104df014c7a96dccf96e421267fd9f
# Sat, 08 Nov 2025 19:21:43 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Sat, 08 Nov 2025 19:21:43 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Sat, 08 Nov 2025 19:21:43 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:21:43 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Sat, 08 Nov 2025 19:21:43 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Sat, 08 Nov 2025 19:21:43 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Sat, 08 Nov 2025 19:21:43 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f89bfb3dd44266ed9543fe4604ff43b977ac927f5a38fc36e717be3eb1a36d`  
		Last Modified: Sat, 08 Nov 2025 17:57:47 GMT  
		Size: 17.0 MB (16972157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d8a69d2f75841282cb462236d1b5ce986bb6e141bd754efc97151cb24f1e27`  
		Last Modified: Sat, 08 Nov 2025 17:57:49 GMT  
		Size: 46.9 MB (46883770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa491fab65db66954d3ec2de490cefdbcfbb6d1539d4c15049f7ed4d8bbeea38`  
		Last Modified: Sat, 08 Nov 2025 17:57:43 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6abb69c3f3572d87d1ea62fa296ee988fda9b9d1c9d8f7d00a8b9902d34151`  
		Last Modified: Sat, 08 Nov 2025 17:57:43 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bf707f49abf0cf1342307382eeda957d815dda191e89abbf13bbad565421b8`  
		Last Modified: Sat, 08 Nov 2025 18:26:19 GMT  
		Size: 10.4 MB (10364488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57f29cc22f1af68be6c7c0ef3f6aa060910f54cb3392b9cda95b508055a0b47`  
		Last Modified: Sat, 08 Nov 2025 18:26:07 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ba39aaf3937f1b67cfb3c0d1ef4a020de1785827c9566f9d3000b0ed768e5f`  
		Last Modified: Sat, 08 Nov 2025 19:22:19 GMT  
		Size: 238.9 KB (238892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ce94c5e1b520f18a44835d4cebe74e8a927c991e9b3e434234abb0d10271ae`  
		Last Modified: Sat, 08 Nov 2025 23:05:19 GMT  
		Size: 292.0 MB (291981483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9982e2fae4417c8a89c6c62c8ff744d09ef33f300eb7fd8b7f994921631d27`  
		Last Modified: Sat, 08 Nov 2025 19:22:19 GMT  
		Size: 550.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab195e7da4a2251707291b71f4273a85303f2fec505af9f32a15bf3ec1c76c3`  
		Last Modified: Sat, 08 Nov 2025 19:22:19 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9ac4c42ec89ca62bf7afc579dcada7be447a20a6b865a977da970a7c95616a`  
		Last Modified: Sat, 08 Nov 2025 19:22:19 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:9c71731d0bf0847b72e315a4d18f0cead3458a2bb560e362ca47d650fb130691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41339941ec8ab8dc4b5a7f49dfc4d6a45ecb5d505fa329c1209870ff59505e1b`

```dockerfile
```

-	Layers:
	-	`sha256:1d157b650e63ed76dba73c752c8aff1987125550c82310ddd34de3bb2e9cee87`  
		Last Modified: Sat, 08 Nov 2025 22:13:05 GMT  
		Size: 4.2 MB (4219655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e19f5670a702c72d3c89b991842170f24ae8d01d94d68fbc3831f315064a00ac`  
		Last Modified: Sat, 08 Nov 2025 22:13:06 GMT  
		Size: 25.7 KB (25654 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:21f294eb7bcb019debff8c48c0bbb4cb09aaaf7eb36c201b9780117958393046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.7 MB (393664156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025a875c8a00116435a7f95242a8731ac351017b65c0a31b4bedaa6f471f2b99`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:57:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:57:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:57:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:57:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:57:32 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Sat, 08 Nov 2025 17:57:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93454a64c922111e57a86659e5fd6d44406173226cf051aa6228af06a7a44a56';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:57:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:57:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:57:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:26:17 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Sat, 08 Nov 2025 18:26:17 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 08 Nov 2025 18:26:17 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 08 Nov 2025 18:26:17 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 08 Nov 2025 18:26:17 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:26:17 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Sat, 08 Nov 2025 18:26:17 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 08 Nov 2025 18:26:17 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Sat, 08 Nov 2025 18:26:17 GMT
WORKDIR /var/lib/jetty
# Sat, 08 Nov 2025 18:26:17 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Sat, 08 Nov 2025 18:26:17 GMT
USER jetty
# Sat, 08 Nov 2025 18:26:17 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 18:26:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:26:17 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Sat, 08 Nov 2025 19:20:57 GMT
ENV DATA_DIR=/catalogue-data
# Sat, 08 Nov 2025 19:20:57 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Sat, 08 Nov 2025 19:20:57 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Sat, 08 Nov 2025 19:20:57 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Sat, 08 Nov 2025 19:20:57 GMT
USER root
# Sat, 08 Nov 2025 19:20:57 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Sat, 08 Nov 2025 19:20:57 GMT
USER jetty
# Sat, 08 Nov 2025 19:20:57 GMT
ENV GN_FILE=geonetwork.war
# Sat, 08 Nov 2025 19:20:57 GMT
ENV GN_VERSION=4.4.9
# Sat, 08 Nov 2025 19:20:57 GMT
ENV GN_DOWNLOAD_MD5=03104df014c7a96dccf96e421267fd9f
# Sat, 08 Nov 2025 19:21:18 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Sat, 08 Nov 2025 19:21:18 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Sat, 08 Nov 2025 19:21:18 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:21:19 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Sat, 08 Nov 2025 19:21:19 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Sat, 08 Nov 2025 19:21:19 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Sat, 08 Nov 2025 19:21:19 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f7654790c24728ffca0008db3fdf1df7faeb35641e71a0dbdd99dfb65ed007`  
		Last Modified: Sat, 08 Nov 2025 17:58:00 GMT  
		Size: 17.0 MB (16989385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9563970e8499be18387be96ca2b854d6c9ceec66e01fb7b4ec308468b5173701`  
		Last Modified: Sat, 08 Nov 2025 17:58:04 GMT  
		Size: 45.2 MB (45223033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a2ad96e4ba9ad2d9e7546a1385f36f4d4aefd9ac27762729c5c8b31f031ed5`  
		Last Modified: Sat, 08 Nov 2025 17:57:59 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb2bb049339afc486316d635a5e6027854bc90e756db1a4ebc2c0aed2190e14`  
		Last Modified: Sat, 08 Nov 2025 17:58:00 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bc309a635f2ee33d4caccce4f58593a67daa287b38e24728f5eb2a39b2ec48`  
		Last Modified: Sat, 08 Nov 2025 18:26:33 GMT  
		Size: 10.4 MB (10364809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe900a1b703153ab53dff2140bf884a1055f13b8de02489310fcbdbe4a9c8c70`  
		Last Modified: Sat, 08 Nov 2025 18:26:32 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0426a0f560b06fdd8d0816f5b0e5a46af6a95d4cf6f50e2d98165c016d68f498`  
		Last Modified: Sat, 08 Nov 2025 19:21:56 GMT  
		Size: 238.2 KB (238168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03575b79a75d094a0c7d949858201f0b533b78b9f4495072bdfb406004327d8`  
		Last Modified: Sat, 08 Nov 2025 23:04:52 GMT  
		Size: 292.0 MB (291981479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58b62a250e862e3e61c9de095e2f0048bacf37aba662c20155c437003d6eb04`  
		Last Modified: Sat, 08 Nov 2025 19:21:56 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a563f5c880a269b681e06dbdcc097924eae26c312ab98b6a00a29d1c2942f1d3`  
		Last Modified: Sat, 08 Nov 2025 19:21:56 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6eaf3eec605064a1dbae8cdec9cd29da950795c6e4aa9c47ee590a5a84b289`  
		Last Modified: Sat, 08 Nov 2025 19:21:56 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:74efade6d2af35edb4a5f79af119698b8e0397e3816b2a5d9bcb70198577c8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4246529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3bb33f74d526fc8c85b1090c27a9d6fb17f9dea9752d143e88dffd28cb71e9`

```dockerfile
```

-	Layers:
	-	`sha256:a2eb97c45fdf0626a99ad3e7e866ae2f98cc6c343207ec672b707f110df74d74`  
		Last Modified: Sat, 08 Nov 2025 22:13:11 GMT  
		Size: 4.2 MB (4220740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68cb61befcfe21dc26e866ba3e94403fd5ea54252533b89ef507c3f889fe1df8`  
		Last Modified: Sat, 08 Nov 2025 22:13:11 GMT  
		Size: 25.8 KB (25789 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.4.9`

```console
$ docker pull geonetwork@sha256:30033b7ef02432cd6813e1e9fa075ce07675851421d4490a3404884635dab9de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:4.4.9` - linux; amd64

```console
$ docker pull geonetwork@sha256:699e2cfc09ba7e0ef0d221b03527b651fdce80b4e927c537606e059f80de1b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.2 MB (396169507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c47d7abb026459f91a0a61675443713d93f73a81380b176ae7a373fdbe68c9`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:57:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:57:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:57:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:57:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:57:23 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Sat, 08 Nov 2025 17:57:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93454a64c922111e57a86659e5fd6d44406173226cf051aa6228af06a7a44a56';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:57:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:57:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:57:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:26:05 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Sat, 08 Nov 2025 18:26:05 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 08 Nov 2025 18:26:05 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 08 Nov 2025 18:26:05 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 08 Nov 2025 18:26:05 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:26:05 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Sat, 08 Nov 2025 18:26:05 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 08 Nov 2025 18:26:05 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Sat, 08 Nov 2025 18:26:05 GMT
WORKDIR /var/lib/jetty
# Sat, 08 Nov 2025 18:26:05 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Sat, 08 Nov 2025 18:26:05 GMT
USER jetty
# Sat, 08 Nov 2025 18:26:05 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 18:26:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:26:05 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Sat, 08 Nov 2025 19:21:21 GMT
ENV DATA_DIR=/catalogue-data
# Sat, 08 Nov 2025 19:21:21 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Sat, 08 Nov 2025 19:21:21 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Sat, 08 Nov 2025 19:21:21 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Sat, 08 Nov 2025 19:21:21 GMT
USER root
# Sat, 08 Nov 2025 19:21:21 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Sat, 08 Nov 2025 19:21:21 GMT
USER jetty
# Sat, 08 Nov 2025 19:21:21 GMT
ENV GN_FILE=geonetwork.war
# Sat, 08 Nov 2025 19:21:21 GMT
ENV GN_VERSION=4.4.9
# Sat, 08 Nov 2025 19:21:21 GMT
ENV GN_DOWNLOAD_MD5=03104df014c7a96dccf96e421267fd9f
# Sat, 08 Nov 2025 19:21:43 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Sat, 08 Nov 2025 19:21:43 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Sat, 08 Nov 2025 19:21:43 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:21:43 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Sat, 08 Nov 2025 19:21:43 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Sat, 08 Nov 2025 19:21:43 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Sat, 08 Nov 2025 19:21:43 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f89bfb3dd44266ed9543fe4604ff43b977ac927f5a38fc36e717be3eb1a36d`  
		Last Modified: Sat, 08 Nov 2025 17:57:47 GMT  
		Size: 17.0 MB (16972157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d8a69d2f75841282cb462236d1b5ce986bb6e141bd754efc97151cb24f1e27`  
		Last Modified: Sat, 08 Nov 2025 17:57:49 GMT  
		Size: 46.9 MB (46883770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa491fab65db66954d3ec2de490cefdbcfbb6d1539d4c15049f7ed4d8bbeea38`  
		Last Modified: Sat, 08 Nov 2025 17:57:43 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6abb69c3f3572d87d1ea62fa296ee988fda9b9d1c9d8f7d00a8b9902d34151`  
		Last Modified: Sat, 08 Nov 2025 17:57:43 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bf707f49abf0cf1342307382eeda957d815dda191e89abbf13bbad565421b8`  
		Last Modified: Sat, 08 Nov 2025 18:26:19 GMT  
		Size: 10.4 MB (10364488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57f29cc22f1af68be6c7c0ef3f6aa060910f54cb3392b9cda95b508055a0b47`  
		Last Modified: Sat, 08 Nov 2025 18:26:07 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ba39aaf3937f1b67cfb3c0d1ef4a020de1785827c9566f9d3000b0ed768e5f`  
		Last Modified: Sat, 08 Nov 2025 19:22:19 GMT  
		Size: 238.9 KB (238892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ce94c5e1b520f18a44835d4cebe74e8a927c991e9b3e434234abb0d10271ae`  
		Last Modified: Sat, 08 Nov 2025 23:05:19 GMT  
		Size: 292.0 MB (291981483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9982e2fae4417c8a89c6c62c8ff744d09ef33f300eb7fd8b7f994921631d27`  
		Last Modified: Sat, 08 Nov 2025 19:22:19 GMT  
		Size: 550.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab195e7da4a2251707291b71f4273a85303f2fec505af9f32a15bf3ec1c76c3`  
		Last Modified: Sat, 08 Nov 2025 19:22:19 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9ac4c42ec89ca62bf7afc579dcada7be447a20a6b865a977da970a7c95616a`  
		Last Modified: Sat, 08 Nov 2025 19:22:19 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4.9` - unknown; unknown

```console
$ docker pull geonetwork@sha256:9c71731d0bf0847b72e315a4d18f0cead3458a2bb560e362ca47d650fb130691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41339941ec8ab8dc4b5a7f49dfc4d6a45ecb5d505fa329c1209870ff59505e1b`

```dockerfile
```

-	Layers:
	-	`sha256:1d157b650e63ed76dba73c752c8aff1987125550c82310ddd34de3bb2e9cee87`  
		Last Modified: Sat, 08 Nov 2025 22:13:05 GMT  
		Size: 4.2 MB (4219655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e19f5670a702c72d3c89b991842170f24ae8d01d94d68fbc3831f315064a00ac`  
		Last Modified: Sat, 08 Nov 2025 22:13:06 GMT  
		Size: 25.7 KB (25654 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4.9` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:21f294eb7bcb019debff8c48c0bbb4cb09aaaf7eb36c201b9780117958393046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.7 MB (393664156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025a875c8a00116435a7f95242a8731ac351017b65c0a31b4bedaa6f471f2b99`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:57:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:57:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:57:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:57:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:57:32 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Sat, 08 Nov 2025 17:57:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93454a64c922111e57a86659e5fd6d44406173226cf051aa6228af06a7a44a56';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:57:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:57:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:57:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:26:17 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Sat, 08 Nov 2025 18:26:17 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 08 Nov 2025 18:26:17 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 08 Nov 2025 18:26:17 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 08 Nov 2025 18:26:17 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:26:17 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Sat, 08 Nov 2025 18:26:17 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 08 Nov 2025 18:26:17 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Sat, 08 Nov 2025 18:26:17 GMT
WORKDIR /var/lib/jetty
# Sat, 08 Nov 2025 18:26:17 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Sat, 08 Nov 2025 18:26:17 GMT
USER jetty
# Sat, 08 Nov 2025 18:26:17 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 18:26:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:26:17 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Sat, 08 Nov 2025 19:20:57 GMT
ENV DATA_DIR=/catalogue-data
# Sat, 08 Nov 2025 19:20:57 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Sat, 08 Nov 2025 19:20:57 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Sat, 08 Nov 2025 19:20:57 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Sat, 08 Nov 2025 19:20:57 GMT
USER root
# Sat, 08 Nov 2025 19:20:57 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Sat, 08 Nov 2025 19:20:57 GMT
USER jetty
# Sat, 08 Nov 2025 19:20:57 GMT
ENV GN_FILE=geonetwork.war
# Sat, 08 Nov 2025 19:20:57 GMT
ENV GN_VERSION=4.4.9
# Sat, 08 Nov 2025 19:20:57 GMT
ENV GN_DOWNLOAD_MD5=03104df014c7a96dccf96e421267fd9f
# Sat, 08 Nov 2025 19:21:18 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Sat, 08 Nov 2025 19:21:18 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Sat, 08 Nov 2025 19:21:18 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:21:19 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Sat, 08 Nov 2025 19:21:19 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Sat, 08 Nov 2025 19:21:19 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Sat, 08 Nov 2025 19:21:19 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f7654790c24728ffca0008db3fdf1df7faeb35641e71a0dbdd99dfb65ed007`  
		Last Modified: Sat, 08 Nov 2025 17:58:00 GMT  
		Size: 17.0 MB (16989385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9563970e8499be18387be96ca2b854d6c9ceec66e01fb7b4ec308468b5173701`  
		Last Modified: Sat, 08 Nov 2025 17:58:04 GMT  
		Size: 45.2 MB (45223033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a2ad96e4ba9ad2d9e7546a1385f36f4d4aefd9ac27762729c5c8b31f031ed5`  
		Last Modified: Sat, 08 Nov 2025 17:57:59 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb2bb049339afc486316d635a5e6027854bc90e756db1a4ebc2c0aed2190e14`  
		Last Modified: Sat, 08 Nov 2025 17:58:00 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bc309a635f2ee33d4caccce4f58593a67daa287b38e24728f5eb2a39b2ec48`  
		Last Modified: Sat, 08 Nov 2025 18:26:33 GMT  
		Size: 10.4 MB (10364809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe900a1b703153ab53dff2140bf884a1055f13b8de02489310fcbdbe4a9c8c70`  
		Last Modified: Sat, 08 Nov 2025 18:26:32 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0426a0f560b06fdd8d0816f5b0e5a46af6a95d4cf6f50e2d98165c016d68f498`  
		Last Modified: Sat, 08 Nov 2025 19:21:56 GMT  
		Size: 238.2 KB (238168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03575b79a75d094a0c7d949858201f0b533b78b9f4495072bdfb406004327d8`  
		Last Modified: Sat, 08 Nov 2025 23:04:52 GMT  
		Size: 292.0 MB (291981479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58b62a250e862e3e61c9de095e2f0048bacf37aba662c20155c437003d6eb04`  
		Last Modified: Sat, 08 Nov 2025 19:21:56 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a563f5c880a269b681e06dbdcc097924eae26c312ab98b6a00a29d1c2942f1d3`  
		Last Modified: Sat, 08 Nov 2025 19:21:56 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6eaf3eec605064a1dbae8cdec9cd29da950795c6e4aa9c47ee590a5a84b289`  
		Last Modified: Sat, 08 Nov 2025 19:21:56 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4.9` - unknown; unknown

```console
$ docker pull geonetwork@sha256:74efade6d2af35edb4a5f79af119698b8e0397e3816b2a5d9bcb70198577c8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4246529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3bb33f74d526fc8c85b1090c27a9d6fb17f9dea9752d143e88dffd28cb71e9`

```dockerfile
```

-	Layers:
	-	`sha256:a2eb97c45fdf0626a99ad3e7e866ae2f98cc6c343207ec672b707f110df74d74`  
		Last Modified: Sat, 08 Nov 2025 22:13:11 GMT  
		Size: 4.2 MB (4220740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68cb61befcfe21dc26e866ba3e94403fd5ea54252533b89ef507c3f889fe1df8`  
		Last Modified: Sat, 08 Nov 2025 22:13:11 GMT  
		Size: 25.8 KB (25789 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:latest`

```console
$ docker pull geonetwork@sha256:30033b7ef02432cd6813e1e9fa075ce07675851421d4490a3404884635dab9de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:latest` - linux; amd64

```console
$ docker pull geonetwork@sha256:699e2cfc09ba7e0ef0d221b03527b651fdce80b4e927c537606e059f80de1b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.2 MB (396169507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c47d7abb026459f91a0a61675443713d93f73a81380b176ae7a373fdbe68c9`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:57:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:57:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:57:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:57:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:57:23 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Sat, 08 Nov 2025 17:57:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93454a64c922111e57a86659e5fd6d44406173226cf051aa6228af06a7a44a56';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:57:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:57:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:57:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:26:05 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Sat, 08 Nov 2025 18:26:05 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 08 Nov 2025 18:26:05 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 08 Nov 2025 18:26:05 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 08 Nov 2025 18:26:05 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:26:05 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Sat, 08 Nov 2025 18:26:05 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 08 Nov 2025 18:26:05 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Sat, 08 Nov 2025 18:26:05 GMT
WORKDIR /var/lib/jetty
# Sat, 08 Nov 2025 18:26:05 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Sat, 08 Nov 2025 18:26:05 GMT
USER jetty
# Sat, 08 Nov 2025 18:26:05 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 18:26:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:26:05 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Sat, 08 Nov 2025 19:21:21 GMT
ENV DATA_DIR=/catalogue-data
# Sat, 08 Nov 2025 19:21:21 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Sat, 08 Nov 2025 19:21:21 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Sat, 08 Nov 2025 19:21:21 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Sat, 08 Nov 2025 19:21:21 GMT
USER root
# Sat, 08 Nov 2025 19:21:21 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Sat, 08 Nov 2025 19:21:21 GMT
USER jetty
# Sat, 08 Nov 2025 19:21:21 GMT
ENV GN_FILE=geonetwork.war
# Sat, 08 Nov 2025 19:21:21 GMT
ENV GN_VERSION=4.4.9
# Sat, 08 Nov 2025 19:21:21 GMT
ENV GN_DOWNLOAD_MD5=03104df014c7a96dccf96e421267fd9f
# Sat, 08 Nov 2025 19:21:43 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Sat, 08 Nov 2025 19:21:43 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Sat, 08 Nov 2025 19:21:43 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:21:43 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Sat, 08 Nov 2025 19:21:43 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Sat, 08 Nov 2025 19:21:43 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Sat, 08 Nov 2025 19:21:43 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f89bfb3dd44266ed9543fe4604ff43b977ac927f5a38fc36e717be3eb1a36d`  
		Last Modified: Sat, 08 Nov 2025 17:57:47 GMT  
		Size: 17.0 MB (16972157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d8a69d2f75841282cb462236d1b5ce986bb6e141bd754efc97151cb24f1e27`  
		Last Modified: Sat, 08 Nov 2025 17:57:49 GMT  
		Size: 46.9 MB (46883770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa491fab65db66954d3ec2de490cefdbcfbb6d1539d4c15049f7ed4d8bbeea38`  
		Last Modified: Sat, 08 Nov 2025 17:57:43 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6abb69c3f3572d87d1ea62fa296ee988fda9b9d1c9d8f7d00a8b9902d34151`  
		Last Modified: Sat, 08 Nov 2025 17:57:43 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bf707f49abf0cf1342307382eeda957d815dda191e89abbf13bbad565421b8`  
		Last Modified: Sat, 08 Nov 2025 18:26:19 GMT  
		Size: 10.4 MB (10364488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57f29cc22f1af68be6c7c0ef3f6aa060910f54cb3392b9cda95b508055a0b47`  
		Last Modified: Sat, 08 Nov 2025 18:26:07 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ba39aaf3937f1b67cfb3c0d1ef4a020de1785827c9566f9d3000b0ed768e5f`  
		Last Modified: Sat, 08 Nov 2025 19:22:19 GMT  
		Size: 238.9 KB (238892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ce94c5e1b520f18a44835d4cebe74e8a927c991e9b3e434234abb0d10271ae`  
		Last Modified: Sat, 08 Nov 2025 23:05:19 GMT  
		Size: 292.0 MB (291981483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9982e2fae4417c8a89c6c62c8ff744d09ef33f300eb7fd8b7f994921631d27`  
		Last Modified: Sat, 08 Nov 2025 19:22:19 GMT  
		Size: 550.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab195e7da4a2251707291b71f4273a85303f2fec505af9f32a15bf3ec1c76c3`  
		Last Modified: Sat, 08 Nov 2025 19:22:19 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9ac4c42ec89ca62bf7afc579dcada7be447a20a6b865a977da970a7c95616a`  
		Last Modified: Sat, 08 Nov 2025 19:22:19 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:latest` - unknown; unknown

```console
$ docker pull geonetwork@sha256:9c71731d0bf0847b72e315a4d18f0cead3458a2bb560e362ca47d650fb130691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41339941ec8ab8dc4b5a7f49dfc4d6a45ecb5d505fa329c1209870ff59505e1b`

```dockerfile
```

-	Layers:
	-	`sha256:1d157b650e63ed76dba73c752c8aff1987125550c82310ddd34de3bb2e9cee87`  
		Last Modified: Sat, 08 Nov 2025 22:13:05 GMT  
		Size: 4.2 MB (4219655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e19f5670a702c72d3c89b991842170f24ae8d01d94d68fbc3831f315064a00ac`  
		Last Modified: Sat, 08 Nov 2025 22:13:06 GMT  
		Size: 25.7 KB (25654 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:latest` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:21f294eb7bcb019debff8c48c0bbb4cb09aaaf7eb36c201b9780117958393046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.7 MB (393664156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025a875c8a00116435a7f95242a8731ac351017b65c0a31b4bedaa6f471f2b99`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:57:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:57:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:57:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:57:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:57:32 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Sat, 08 Nov 2025 17:57:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93454a64c922111e57a86659e5fd6d44406173226cf051aa6228af06a7a44a56';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:57:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:57:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:57:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:26:17 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Sat, 08 Nov 2025 18:26:17 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sat, 08 Nov 2025 18:26:17 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sat, 08 Nov 2025 18:26:17 GMT
ENV TMPDIR=/tmp/jetty
# Sat, 08 Nov 2025 18:26:17 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:26:17 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Sat, 08 Nov 2025 18:26:17 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Sat, 08 Nov 2025 18:26:17 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Sat, 08 Nov 2025 18:26:17 GMT
WORKDIR /var/lib/jetty
# Sat, 08 Nov 2025 18:26:17 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Sat, 08 Nov 2025 18:26:17 GMT
USER jetty
# Sat, 08 Nov 2025 18:26:17 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 18:26:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:26:17 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Sat, 08 Nov 2025 19:20:57 GMT
ENV DATA_DIR=/catalogue-data
# Sat, 08 Nov 2025 19:20:57 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Sat, 08 Nov 2025 19:20:57 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Sat, 08 Nov 2025 19:20:57 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Sat, 08 Nov 2025 19:20:57 GMT
USER root
# Sat, 08 Nov 2025 19:20:57 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Sat, 08 Nov 2025 19:20:57 GMT
USER jetty
# Sat, 08 Nov 2025 19:20:57 GMT
ENV GN_FILE=geonetwork.war
# Sat, 08 Nov 2025 19:20:57 GMT
ENV GN_VERSION=4.4.9
# Sat, 08 Nov 2025 19:20:57 GMT
ENV GN_DOWNLOAD_MD5=03104df014c7a96dccf96e421267fd9f
# Sat, 08 Nov 2025 19:21:18 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Sat, 08 Nov 2025 19:21:18 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Sat, 08 Nov 2025 19:21:18 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:21:19 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Sat, 08 Nov 2025 19:21:19 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Sat, 08 Nov 2025 19:21:19 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Sat, 08 Nov 2025 19:21:19 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f7654790c24728ffca0008db3fdf1df7faeb35641e71a0dbdd99dfb65ed007`  
		Last Modified: Sat, 08 Nov 2025 17:58:00 GMT  
		Size: 17.0 MB (16989385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9563970e8499be18387be96ca2b854d6c9ceec66e01fb7b4ec308468b5173701`  
		Last Modified: Sat, 08 Nov 2025 17:58:04 GMT  
		Size: 45.2 MB (45223033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a2ad96e4ba9ad2d9e7546a1385f36f4d4aefd9ac27762729c5c8b31f031ed5`  
		Last Modified: Sat, 08 Nov 2025 17:57:59 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb2bb049339afc486316d635a5e6027854bc90e756db1a4ebc2c0aed2190e14`  
		Last Modified: Sat, 08 Nov 2025 17:58:00 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bc309a635f2ee33d4caccce4f58593a67daa287b38e24728f5eb2a39b2ec48`  
		Last Modified: Sat, 08 Nov 2025 18:26:33 GMT  
		Size: 10.4 MB (10364809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe900a1b703153ab53dff2140bf884a1055f13b8de02489310fcbdbe4a9c8c70`  
		Last Modified: Sat, 08 Nov 2025 18:26:32 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0426a0f560b06fdd8d0816f5b0e5a46af6a95d4cf6f50e2d98165c016d68f498`  
		Last Modified: Sat, 08 Nov 2025 19:21:56 GMT  
		Size: 238.2 KB (238168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03575b79a75d094a0c7d949858201f0b533b78b9f4495072bdfb406004327d8`  
		Last Modified: Sat, 08 Nov 2025 23:04:52 GMT  
		Size: 292.0 MB (291981479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58b62a250e862e3e61c9de095e2f0048bacf37aba662c20155c437003d6eb04`  
		Last Modified: Sat, 08 Nov 2025 19:21:56 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a563f5c880a269b681e06dbdcc097924eae26c312ab98b6a00a29d1c2942f1d3`  
		Last Modified: Sat, 08 Nov 2025 19:21:56 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6eaf3eec605064a1dbae8cdec9cd29da950795c6e4aa9c47ee590a5a84b289`  
		Last Modified: Sat, 08 Nov 2025 19:21:56 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:latest` - unknown; unknown

```console
$ docker pull geonetwork@sha256:74efade6d2af35edb4a5f79af119698b8e0397e3816b2a5d9bcb70198577c8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4246529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3bb33f74d526fc8c85b1090c27a9d6fb17f9dea9752d143e88dffd28cb71e9`

```dockerfile
```

-	Layers:
	-	`sha256:a2eb97c45fdf0626a99ad3e7e866ae2f98cc6c343207ec672b707f110df74d74`  
		Last Modified: Sat, 08 Nov 2025 22:13:11 GMT  
		Size: 4.2 MB (4220740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68cb61befcfe21dc26e866ba3e94403fd5ea54252533b89ef507c3f889fe1df8`  
		Last Modified: Sat, 08 Nov 2025 22:13:11 GMT  
		Size: 25.8 KB (25789 bytes)  
		MIME: application/vnd.in-toto+json
