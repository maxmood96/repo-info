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
$ docker pull geonetwork@sha256:bac3c8d478809cdda58dc71dfc32aef67aa7a8dee455b6698cd79246ed4096e6
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
$ docker pull geonetwork@sha256:e5ee99d2844bab3c9bf4343952364b8c7e740b747dc393b2e7bd8bfe6a3a602d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.1 MB (394134008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2170765dde92ba9dd79b916634973766a9980a6c47170ee91fa332d7a11e5100`
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
ENV TOMCAT_VERSION=9.0.90
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
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
	-	`sha256:d7e00fc5e414fea1042275ebc2c537d6eee04adead835cd35b9ca1cb599b7cc1`  
		Last Modified: Tue, 02 Jul 2024 07:10:54 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee4aadd175997f665f225d14190b3c1ff86e77c5337d3f755cd747b6180b716`  
		Last Modified: Tue, 02 Jul 2024 07:10:55 GMT  
		Size: 12.7 MB (12678754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b25e6c3da21c080a00569d7282ca1ad33f9d611ddaaa388f15fcc0db27c773d`  
		Last Modified: Tue, 02 Jul 2024 10:24:57 GMT  
		Size: 234.5 MB (234540650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2eede8d86b8ac50af7221a2cfb9ab07f6b39de6ec5755414c27020d34786dc`  
		Last Modified: Tue, 02 Jul 2024 10:24:54 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:4e3c9a793bd03e8a72ab2d1630e10338809693a2d22388707cbcef111edb884e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4203700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d703d149540965813ac363f6c81186f2cf11545a9e66d3a7ad14db10ee221b`

```dockerfile
```

-	Layers:
	-	`sha256:b8380102d31109b253c1961b596b7274210997d852febb9caadac41042302dea`  
		Last Modified: Tue, 02 Jul 2024 10:24:54 GMT  
		Size: 4.2 MB (4184466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a55a41411dbf8c8fae10e76a44f4cbae30403027fb40db92fc27bf96b26ed34`  
		Last Modified: Tue, 02 Jul 2024 10:24:53 GMT  
		Size: 19.2 KB (19234 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:43a3308bde28fbd6dfb0f158a7cfe20674f1b5e92fd164e06204a62cdb4f18a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.6 MB (388632868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a6343edd493eb040d5c675d009063f13e96d03d9a3411400a666eaad08a0ff`
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
ADD file:76d606bb5f897ff3ffe149c5d3d049c7ace15da77a61a7df4e558eceebd8d2bd in / 
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
ENV TOMCAT_VERSION=9.0.90
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
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
	-	`sha256:bb2b4ba5ac52e5e8a83a1f8dc3c79ed1f5409e3bc349a8c36b2cd4b9d3f6cb23`  
		Last Modified: Tue, 04 Jun 2024 01:38:51 GMT  
		Size: 27.5 MB (27534888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2e7d8e2026f154f12e834d8b72426c2f71c8a555d373336fddba91616868b7`  
		Last Modified: Wed, 05 Jun 2024 03:59:49 GMT  
		Size: 12.5 MB (12493203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95298bffd1c0ebd593eeb6754e0f5e5ba9ca25454af388f78cd657152f59cd01`  
		Last Modified: Wed, 05 Jun 2024 03:59:55 GMT  
		Size: 99.2 MB (99228750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d783cd2973ac4c20fae7efd4d2e605cff4de71ba08f4110510a1e7d7dc0239b5`  
		Last Modified: Wed, 05 Jun 2024 03:59:46 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160d32d80ad9bff0aadc9f16c0712d2e20cc58ddf491fba50571fccb3d0d77f9`  
		Last Modified: Wed, 05 Jun 2024 03:59:46 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74100269fc7beb2a5d4018be5dd2bf6efdd8e67fb196bf9ec8b743775ebc4d5e`  
		Last Modified: Fri, 28 Jun 2024 21:08:17 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77584de730899731c5a1dbcb3520dc215769824755aaf66d41a2b714ffa923f9`  
		Last Modified: Fri, 28 Jun 2024 21:08:18 GMT  
		Size: 14.8 MB (14844959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436df1fc18a76313a0106c5b0685c3dce1a4699b2612059dfe8bfbb6bbdb0a1a`  
		Last Modified: Fri, 28 Jun 2024 22:08:29 GMT  
		Size: 234.5 MB (234529688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2549c7b3f9b3e59cc4b497b768ea8f43ae6944b878d719849eed020fa24dbad`  
		Last Modified: Fri, 28 Jun 2024 22:08:23 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:381c4f3cc3d99ce567517b3757857ddea677c6eb6222a01b700c9f53984740ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6586a5c4b0782c5c84f8a48824367801d56317c115f9cc2c8b60ce5a3e316ff`

```dockerfile
```

-	Layers:
	-	`sha256:5ff4884c4405455d6a5997093436ad7a12033099f89b9c4b3131ce2994491e01`  
		Last Modified: Fri, 28 Jun 2024 22:08:24 GMT  
		Size: 4.2 MB (4189072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b744117d5c0d8c25cb56b617d7739100fd0f8cc6a7a44441d9d93c5ed9fc3ab1`  
		Last Modified: Fri, 28 Jun 2024 22:08:22 GMT  
		Size: 19.4 KB (19448 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:989d485a95ea7d995cd7879f37dc6499b64c985097881c764c039fa1df00c2b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393774450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93923f8bb8410a1e6f693112c9b244ef3414f0ad41ddd2c51322e47409c3096`
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
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
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
ENV TOMCAT_VERSION=9.0.90
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
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
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd918abfec0657ade8aeeffe2722e92948e13fa403fd238ae22b1a9881e9402`  
		Last Modified: Wed, 05 Jun 2024 04:55:01 GMT  
		Size: 12.8 MB (12847839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5b526820dcdae2e31487a780fd45e81ebd4980b3118f35e2acbc704533db78`  
		Last Modified: Wed, 05 Jun 2024 04:55:06 GMT  
		Size: 102.7 MB (102704149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef812ceaac9fe9a1b64b4cfc38b12c1cfbe4ab5b8a0b37f60299fe0d05e5f44`  
		Last Modified: Wed, 05 Jun 2024 04:55:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f4c9c3017a82e12289bd3d8fcf61cca4f319bc017cc0f19e0f196680418917`  
		Last Modified: Wed, 05 Jun 2024 04:55:00 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f85232d9fbefdb5ebf0a56659b08993f8b0b0ba6763743db4a0e4a00d43477`  
		Last Modified: Fri, 28 Jun 2024 21:46:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318f771fe831db88763407093d7d9f7fda8b92850ef612e19cac483aff56b463`  
		Last Modified: Fri, 28 Jun 2024 21:46:53 GMT  
		Size: 15.3 MB (15279637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0062c7efe2eb5d07c30f9598ebe3d32bdd8860ebf365c7c79a81f748b839dee9`  
		Last Modified: Fri, 28 Jun 2024 22:07:02 GMT  
		Size: 234.5 MB (234539139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fb9ed0b3e5f777f462e256d9758412b677ce73d213daff0ffc92d64fa79603`  
		Last Modified: Fri, 28 Jun 2024 22:06:58 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:3b9e1f8b096d39dc2fe891765d73868316afff7ee4ffc6ca7cbc154c55b69baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4206241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa213600b0221e5ac0f23c8cdbf94a9edb92787d117865055da6db5ff6a6e566`

```dockerfile
```

-	Layers:
	-	`sha256:25bf015fc2ecb7be7975edd4aa4f780ff4658ce193789b351ae77a6558f5966f`  
		Last Modified: Fri, 28 Jun 2024 22:06:56 GMT  
		Size: 4.2 MB (4186483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92a5be3d8475dfee4e996844d50747be17e456d1fd53cfa073af053a68af92f1`  
		Last Modified: Fri, 28 Jun 2024 22:06:56 GMT  
		Size: 19.8 KB (19758 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:2dfbfffde29392298c55ca86afc275a223772c3a647583372a0600d9d13c8f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.8 MB (400843310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff755656bbe50b6e9c19c49e6e24cc763e2c2da0993a95651ecee0e7958a6448`
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
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
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
ENV TOMCAT_VERSION=9.0.90
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
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
	-	`sha256:391f04f7f495cb5fc20be69876c8638cb8f316a2cddac5d48d77ca39244e6dea`  
		Last Modified: Wed, 05 Jun 2024 03:48:14 GMT  
		Size: 35.6 MB (35588332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82f84268a93862af92928dd1cc1dc31937bbffd50302e61f899397e5223399d`  
		Last Modified: Wed, 05 Jun 2024 04:00:20 GMT  
		Size: 13.8 MB (13766991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96f8afb54eaa4d0d1271da3f9226622e5393ff92e4b765aec30aa1fcaca113a`  
		Last Modified: Wed, 05 Jun 2024 04:00:24 GMT  
		Size: 101.1 MB (101071129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59900ccb04bc654c9922cbd79216a4488310d9308aea4ecffd1d72e4eddee950`  
		Last Modified: Wed, 05 Jun 2024 04:00:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc837f7bedc9361e014f8f1c0bd2abf18e18798493eeee096794e977342e60d7`  
		Last Modified: Wed, 05 Jun 2024 04:00:15 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853d47376be40723d6b984c2403558b16158849848790d7f94be84be255b0198`  
		Last Modified: Fri, 28 Jun 2024 21:16:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b798e3939c0e9aefadd4f8df0b4406c0da240a1c3e3173bde6b82cc05e33718`  
		Last Modified: Fri, 28 Jun 2024 21:16:54 GMT  
		Size: 15.8 MB (15836765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d91e9da7368175562d63f7aee9d751ceab2a00d0b371456d7a4cdf064770c16`  
		Last Modified: Fri, 28 Jun 2024 22:10:36 GMT  
		Size: 234.6 MB (234578714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286b89930f54634e708580e88a2248ca3c8adf372430ac02210f17f19f48d9b9`  
		Last Modified: Fri, 28 Jun 2024 22:10:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:8f20b314cf578e294488364e0adb9f805438807d7c32aaedb3d9fe5a3bdfe33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4209176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5e64934f53c8df3637a3f16b0f19c307be1d64433c3b23dd3ceb0c46e29366`

```dockerfile
```

-	Layers:
	-	`sha256:bea7eba575ba69267d9a72700494da48a0be7249244e5b35a1fbd0e20f027b8d`  
		Last Modified: Fri, 28 Jun 2024 22:10:30 GMT  
		Size: 4.2 MB (4189753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a8959b3d58dad6c4954be143a9071e580015be7cb296cff5fb7215220fffaca`  
		Last Modified: Fri, 28 Jun 2024 22:10:30 GMT  
		Size: 19.4 KB (19423 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3-postgres`

```console
$ docker pull geonetwork@sha256:e105c49950f75b721cb3ce119c0e53eff232363797162b269412c4840c4f151a
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
$ docker pull geonetwork@sha256:12f5ed53202af3d1c23b376d5aed3762630f5e765f40b45b42651736d5aa26fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.6 MB (407604979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9381ca4ba74bd653bd87246c5c811727b759a8a26011ab693a9cff2078d119d8`
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
ENV TOMCAT_VERSION=9.0.90
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
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
	-	`sha256:d7e00fc5e414fea1042275ebc2c537d6eee04adead835cd35b9ca1cb599b7cc1`  
		Last Modified: Tue, 02 Jul 2024 07:10:54 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee4aadd175997f665f225d14190b3c1ff86e77c5337d3f755cd747b6180b716`  
		Last Modified: Tue, 02 Jul 2024 07:10:55 GMT  
		Size: 12.7 MB (12678754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b25e6c3da21c080a00569d7282ca1ad33f9d611ddaaa388f15fcc0db27c773d`  
		Last Modified: Tue, 02 Jul 2024 10:24:57 GMT  
		Size: 234.5 MB (234540650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2eede8d86b8ac50af7221a2cfb9ab07f6b39de6ec5755414c27020d34786dc`  
		Last Modified: Tue, 02 Jul 2024 10:24:54 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27eff3114d71270fdb5e45c24f7d58d6e26bbeed86bc245baf04dfe26baa58d`  
		Last Modified: Tue, 02 Jul 2024 11:04:01 GMT  
		Size: 13.5 MB (13467612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c7516ff6e88a4ba93c51460a9f46457338dddfc4073b7b7555cf31653c027b`  
		Last Modified: Tue, 02 Jul 2024 11:04:00 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c067e9b4f50d72275a1e737598e7d3450be368c94e182fc47647abb21588fd`  
		Last Modified: Tue, 02 Jul 2024 11:04:00 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1176f817ae6d2f5b5fd19235477cbd9dd51e9a74d6030b3d5cf6b15e380d9f38`  
		Last Modified: Tue, 02 Jul 2024 11:04:00 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:65976ae06ed276445ef3b28a87ed4607a7df0aaf3ccfca5a17b40adfd0bd139e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5745459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f746c4bddce07c947d69d98cef7c757339664f72fafb7cd5bfb2fed534cd26`

```dockerfile
```

-	Layers:
	-	`sha256:ef9bb7e9ea9232d4883f1a21485e679083e1ad9e754589820e6f609ed91a60e6`  
		Last Modified: Tue, 02 Jul 2024 11:04:00 GMT  
		Size: 5.7 MB (5722365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1cbf459bd6aae55ca18b220ef088588100a9c957013cc84b95d6d0c2f73d257`  
		Last Modified: Tue, 02 Jul 2024 11:04:00 GMT  
		Size: 23.1 KB (23094 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:9583fc2415ee9d0e29a8b5744b0cf39fb8ef162c68f3bc0ba1bcab94f9a13a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.2 MB (401155479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f39fa471b5fedc7ef2b2e0104aed15f1b88d404f04659c873deb41d538ae57`
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
ADD file:76d606bb5f897ff3ffe149c5d3d049c7ace15da77a61a7df4e558eceebd8d2bd in / 
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
ENV TOMCAT_VERSION=9.0.90
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
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
	-	`sha256:bb2b4ba5ac52e5e8a83a1f8dc3c79ed1f5409e3bc349a8c36b2cd4b9d3f6cb23`  
		Last Modified: Tue, 04 Jun 2024 01:38:51 GMT  
		Size: 27.5 MB (27534888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2e7d8e2026f154f12e834d8b72426c2f71c8a555d373336fddba91616868b7`  
		Last Modified: Wed, 05 Jun 2024 03:59:49 GMT  
		Size: 12.5 MB (12493203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95298bffd1c0ebd593eeb6754e0f5e5ba9ca25454af388f78cd657152f59cd01`  
		Last Modified: Wed, 05 Jun 2024 03:59:55 GMT  
		Size: 99.2 MB (99228750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d783cd2973ac4c20fae7efd4d2e605cff4de71ba08f4110510a1e7d7dc0239b5`  
		Last Modified: Wed, 05 Jun 2024 03:59:46 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160d32d80ad9bff0aadc9f16c0712d2e20cc58ddf491fba50571fccb3d0d77f9`  
		Last Modified: Wed, 05 Jun 2024 03:59:46 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74100269fc7beb2a5d4018be5dd2bf6efdd8e67fb196bf9ec8b743775ebc4d5e`  
		Last Modified: Fri, 28 Jun 2024 21:08:17 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77584de730899731c5a1dbcb3520dc215769824755aaf66d41a2b714ffa923f9`  
		Last Modified: Fri, 28 Jun 2024 21:08:18 GMT  
		Size: 14.8 MB (14844959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436df1fc18a76313a0106c5b0685c3dce1a4699b2612059dfe8bfbb6bbdb0a1a`  
		Last Modified: Fri, 28 Jun 2024 22:08:29 GMT  
		Size: 234.5 MB (234529688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2549c7b3f9b3e59cc4b497b768ea8f43ae6944b878d719849eed020fa24dbad`  
		Last Modified: Fri, 28 Jun 2024 22:08:23 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acb4a28192b3c239c1417c04181718154853b58c249ae4c161c0221a8a72e66`  
		Last Modified: Fri, 28 Jun 2024 22:50:43 GMT  
		Size: 12.5 MB (12519250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3292858d28de9e4b7847e6cf0cc5f0eab198ca3e43fdd45f4d1b111bec4554b`  
		Last Modified: Fri, 28 Jun 2024 22:50:42 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f1fb4222c6228e173c3ea185c22bedf424bcfa8e6b3eba2417563419fa382f`  
		Last Modified: Fri, 28 Jun 2024 22:50:42 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6982b629891747df0a8def4a1a91afe8ea7aacc756fd171bc6e88d26a5a9dd`  
		Last Modified: Fri, 28 Jun 2024 22:50:42 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:1aed45904c4ddf7a6aa1dfd707d4f785fb976cde25bc2679aef27dd284c0a8bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e75fac632ec4d2ed62fa3802896018c8ec60013ca56c0290a2ea3d9c4d7ab0e0`

```dockerfile
```

-	Layers:
	-	`sha256:e0e543d9a4a74cfbd5b868c7f4d116ab0f3576d966f40253df9ad2d139fdd14c`  
		Last Modified: Fri, 28 Jun 2024 22:50:42 GMT  
		Size: 5.7 MB (5725680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d242dd36959b19523b4f589c36c354d979735eb49485b3aab438941f767126a3`  
		Last Modified: Fri, 28 Jun 2024 22:50:42 GMT  
		Size: 23.3 KB (23320 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:f9d6eba8db70c17adaf929daaeadfb669057383461f09325fa5707df18038505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.1 MB (407149577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c8d33b48304a3fe25be8717b17f6c25aa7ee3fb7e929bb9676f23d21decf4d5`
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
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
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
ENV TOMCAT_VERSION=9.0.90
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
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
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd918abfec0657ade8aeeffe2722e92948e13fa403fd238ae22b1a9881e9402`  
		Last Modified: Wed, 05 Jun 2024 04:55:01 GMT  
		Size: 12.8 MB (12847839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5b526820dcdae2e31487a780fd45e81ebd4980b3118f35e2acbc704533db78`  
		Last Modified: Wed, 05 Jun 2024 04:55:06 GMT  
		Size: 102.7 MB (102704149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef812ceaac9fe9a1b64b4cfc38b12c1cfbe4ab5b8a0b37f60299fe0d05e5f44`  
		Last Modified: Wed, 05 Jun 2024 04:55:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f4c9c3017a82e12289bd3d8fcf61cca4f319bc017cc0f19e0f196680418917`  
		Last Modified: Wed, 05 Jun 2024 04:55:00 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f85232d9fbefdb5ebf0a56659b08993f8b0b0ba6763743db4a0e4a00d43477`  
		Last Modified: Fri, 28 Jun 2024 21:46:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318f771fe831db88763407093d7d9f7fda8b92850ef612e19cac483aff56b463`  
		Last Modified: Fri, 28 Jun 2024 21:46:53 GMT  
		Size: 15.3 MB (15279637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0062c7efe2eb5d07c30f9598ebe3d32bdd8860ebf365c7c79a81f748b839dee9`  
		Last Modified: Fri, 28 Jun 2024 22:07:02 GMT  
		Size: 234.5 MB (234539139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fb9ed0b3e5f777f462e256d9758412b677ce73d213daff0ffc92d64fa79603`  
		Last Modified: Fri, 28 Jun 2024 22:06:58 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9909cb50b748de471ff27beba1e402b51a1fa24ea87c031e3b78bed85bd44ec0`  
		Last Modified: Fri, 28 Jun 2024 23:08:06 GMT  
		Size: 13.4 MB (13371761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd9d01e419a1c15157400f44656359abe3ebbb421ad2d8b779abccc77b3e294`  
		Last Modified: Fri, 28 Jun 2024 23:08:05 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29d21169c501f89edf5ed07a4d2e107e04cd5f946115645c4293b6b6a1ada24`  
		Last Modified: Fri, 28 Jun 2024 23:08:05 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926c78299a14d92d826095b9aa817f35f8d65366bd73c8f88f29cca34dfe720e`  
		Last Modified: Fri, 28 Jun 2024 23:08:06 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:760dffa6592f733791ef4032f6dc6f8e401439c5098b831544559e1b81cda9ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5754046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1695e6bb409e56bf3bfdfe8f80ebef683a17eca27d3e7cf3553755b693624203`

```dockerfile
```

-	Layers:
	-	`sha256:ca208a077d0ee63fa551d29650daa2dd620171f5526ccd161466fda8fc1634c1`  
		Last Modified: Fri, 28 Jun 2024 23:08:05 GMT  
		Size: 5.7 MB (5730429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b48bb8d93ba72ebd2fb2a82673d631d29aba65f90948de972b58b8a3433c845`  
		Last Modified: Fri, 28 Jun 2024 23:08:05 GMT  
		Size: 23.6 KB (23617 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:8efb740dd76a45a30c2a30b795de39fb377b84d994026c7180ac98a67f3f5295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.8 MB (414808113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6b247f422f949f308acf431cab02ec6be93616d32a4ab6784b2b3fd2c86382`
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
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
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
ENV TOMCAT_VERSION=9.0.90
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
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
	-	`sha256:391f04f7f495cb5fc20be69876c8638cb8f316a2cddac5d48d77ca39244e6dea`  
		Last Modified: Wed, 05 Jun 2024 03:48:14 GMT  
		Size: 35.6 MB (35588332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82f84268a93862af92928dd1cc1dc31937bbffd50302e61f899397e5223399d`  
		Last Modified: Wed, 05 Jun 2024 04:00:20 GMT  
		Size: 13.8 MB (13766991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96f8afb54eaa4d0d1271da3f9226622e5393ff92e4b765aec30aa1fcaca113a`  
		Last Modified: Wed, 05 Jun 2024 04:00:24 GMT  
		Size: 101.1 MB (101071129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59900ccb04bc654c9922cbd79216a4488310d9308aea4ecffd1d72e4eddee950`  
		Last Modified: Wed, 05 Jun 2024 04:00:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc837f7bedc9361e014f8f1c0bd2abf18e18798493eeee096794e977342e60d7`  
		Last Modified: Wed, 05 Jun 2024 04:00:15 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853d47376be40723d6b984c2403558b16158849848790d7f94be84be255b0198`  
		Last Modified: Fri, 28 Jun 2024 21:16:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b798e3939c0e9aefadd4f8df0b4406c0da240a1c3e3173bde6b82cc05e33718`  
		Last Modified: Fri, 28 Jun 2024 21:16:54 GMT  
		Size: 15.8 MB (15836765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d91e9da7368175562d63f7aee9d751ceab2a00d0b371456d7a4cdf064770c16`  
		Last Modified: Fri, 28 Jun 2024 22:10:36 GMT  
		Size: 234.6 MB (234578714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286b89930f54634e708580e88a2248ca3c8adf372430ac02210f17f19f48d9b9`  
		Last Modified: Fri, 28 Jun 2024 22:10:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92349d34efe36b909230a147da8135f66d515f5ee93031dc082f91487b9c05c`  
		Last Modified: Fri, 28 Jun 2024 22:51:01 GMT  
		Size: 14.0 MB (13961436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0717d03446a58008b145ed2b671ab88b4bc897e57cf58efcbe37dbf7bc87d91`  
		Last Modified: Fri, 28 Jun 2024 22:51:00 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbfbbca2af2f608f17a0706c342fd0aaac1e8150462452e6bdaa05baf46fe25`  
		Last Modified: Fri, 28 Jun 2024 22:51:00 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a835d57efaedbfc4ccb2157762db382dea430785dc6f260d2a9fe22c0341769`  
		Last Modified: Fri, 28 Jun 2024 22:51:01 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:3410e27ac0266bd4b44c517928b5524749d46e3ace195efe7df7ca7a9ceff2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5753648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147a36669c74579a6428c2939acadc077f1d2c3cc47f27d5a9da41fb459cba4a`

```dockerfile
```

-	Layers:
	-	`sha256:e3225ade187b1b20c9407e1241370df9b7fd39cdd23208a33af2a15aecac9339`  
		Last Modified: Fri, 28 Jun 2024 22:51:00 GMT  
		Size: 5.7 MB (5730364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af921df2e922ad8270df634a2efde1e07f15f65fdcf47632308bf465ee396535`  
		Last Modified: Fri, 28 Jun 2024 22:51:00 GMT  
		Size: 23.3 KB (23284 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12`

```console
$ docker pull geonetwork@sha256:bac3c8d478809cdda58dc71dfc32aef67aa7a8dee455b6698cd79246ed4096e6
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
$ docker pull geonetwork@sha256:e5ee99d2844bab3c9bf4343952364b8c7e740b747dc393b2e7bd8bfe6a3a602d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.1 MB (394134008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2170765dde92ba9dd79b916634973766a9980a6c47170ee91fa332d7a11e5100`
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
ENV TOMCAT_VERSION=9.0.90
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
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
	-	`sha256:d7e00fc5e414fea1042275ebc2c537d6eee04adead835cd35b9ca1cb599b7cc1`  
		Last Modified: Tue, 02 Jul 2024 07:10:54 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee4aadd175997f665f225d14190b3c1ff86e77c5337d3f755cd747b6180b716`  
		Last Modified: Tue, 02 Jul 2024 07:10:55 GMT  
		Size: 12.7 MB (12678754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b25e6c3da21c080a00569d7282ca1ad33f9d611ddaaa388f15fcc0db27c773d`  
		Last Modified: Tue, 02 Jul 2024 10:24:57 GMT  
		Size: 234.5 MB (234540650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2eede8d86b8ac50af7221a2cfb9ab07f6b39de6ec5755414c27020d34786dc`  
		Last Modified: Tue, 02 Jul 2024 10:24:54 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:4e3c9a793bd03e8a72ab2d1630e10338809693a2d22388707cbcef111edb884e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4203700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d703d149540965813ac363f6c81186f2cf11545a9e66d3a7ad14db10ee221b`

```dockerfile
```

-	Layers:
	-	`sha256:b8380102d31109b253c1961b596b7274210997d852febb9caadac41042302dea`  
		Last Modified: Tue, 02 Jul 2024 10:24:54 GMT  
		Size: 4.2 MB (4184466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a55a41411dbf8c8fae10e76a44f4cbae30403027fb40db92fc27bf96b26ed34`  
		Last Modified: Tue, 02 Jul 2024 10:24:53 GMT  
		Size: 19.2 KB (19234 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:43a3308bde28fbd6dfb0f158a7cfe20674f1b5e92fd164e06204a62cdb4f18a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.6 MB (388632868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a6343edd493eb040d5c675d009063f13e96d03d9a3411400a666eaad08a0ff`
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
ADD file:76d606bb5f897ff3ffe149c5d3d049c7ace15da77a61a7df4e558eceebd8d2bd in / 
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
ENV TOMCAT_VERSION=9.0.90
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
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
	-	`sha256:bb2b4ba5ac52e5e8a83a1f8dc3c79ed1f5409e3bc349a8c36b2cd4b9d3f6cb23`  
		Last Modified: Tue, 04 Jun 2024 01:38:51 GMT  
		Size: 27.5 MB (27534888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2e7d8e2026f154f12e834d8b72426c2f71c8a555d373336fddba91616868b7`  
		Last Modified: Wed, 05 Jun 2024 03:59:49 GMT  
		Size: 12.5 MB (12493203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95298bffd1c0ebd593eeb6754e0f5e5ba9ca25454af388f78cd657152f59cd01`  
		Last Modified: Wed, 05 Jun 2024 03:59:55 GMT  
		Size: 99.2 MB (99228750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d783cd2973ac4c20fae7efd4d2e605cff4de71ba08f4110510a1e7d7dc0239b5`  
		Last Modified: Wed, 05 Jun 2024 03:59:46 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160d32d80ad9bff0aadc9f16c0712d2e20cc58ddf491fba50571fccb3d0d77f9`  
		Last Modified: Wed, 05 Jun 2024 03:59:46 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74100269fc7beb2a5d4018be5dd2bf6efdd8e67fb196bf9ec8b743775ebc4d5e`  
		Last Modified: Fri, 28 Jun 2024 21:08:17 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77584de730899731c5a1dbcb3520dc215769824755aaf66d41a2b714ffa923f9`  
		Last Modified: Fri, 28 Jun 2024 21:08:18 GMT  
		Size: 14.8 MB (14844959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436df1fc18a76313a0106c5b0685c3dce1a4699b2612059dfe8bfbb6bbdb0a1a`  
		Last Modified: Fri, 28 Jun 2024 22:08:29 GMT  
		Size: 234.5 MB (234529688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2549c7b3f9b3e59cc4b497b768ea8f43ae6944b878d719849eed020fa24dbad`  
		Last Modified: Fri, 28 Jun 2024 22:08:23 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:381c4f3cc3d99ce567517b3757857ddea677c6eb6222a01b700c9f53984740ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6586a5c4b0782c5c84f8a48824367801d56317c115f9cc2c8b60ce5a3e316ff`

```dockerfile
```

-	Layers:
	-	`sha256:5ff4884c4405455d6a5997093436ad7a12033099f89b9c4b3131ce2994491e01`  
		Last Modified: Fri, 28 Jun 2024 22:08:24 GMT  
		Size: 4.2 MB (4189072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b744117d5c0d8c25cb56b617d7739100fd0f8cc6a7a44441d9d93c5ed9fc3ab1`  
		Last Modified: Fri, 28 Jun 2024 22:08:22 GMT  
		Size: 19.4 KB (19448 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:989d485a95ea7d995cd7879f37dc6499b64c985097881c764c039fa1df00c2b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393774450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93923f8bb8410a1e6f693112c9b244ef3414f0ad41ddd2c51322e47409c3096`
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
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
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
ENV TOMCAT_VERSION=9.0.90
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
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
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd918abfec0657ade8aeeffe2722e92948e13fa403fd238ae22b1a9881e9402`  
		Last Modified: Wed, 05 Jun 2024 04:55:01 GMT  
		Size: 12.8 MB (12847839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5b526820dcdae2e31487a780fd45e81ebd4980b3118f35e2acbc704533db78`  
		Last Modified: Wed, 05 Jun 2024 04:55:06 GMT  
		Size: 102.7 MB (102704149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef812ceaac9fe9a1b64b4cfc38b12c1cfbe4ab5b8a0b37f60299fe0d05e5f44`  
		Last Modified: Wed, 05 Jun 2024 04:55:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f4c9c3017a82e12289bd3d8fcf61cca4f319bc017cc0f19e0f196680418917`  
		Last Modified: Wed, 05 Jun 2024 04:55:00 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f85232d9fbefdb5ebf0a56659b08993f8b0b0ba6763743db4a0e4a00d43477`  
		Last Modified: Fri, 28 Jun 2024 21:46:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318f771fe831db88763407093d7d9f7fda8b92850ef612e19cac483aff56b463`  
		Last Modified: Fri, 28 Jun 2024 21:46:53 GMT  
		Size: 15.3 MB (15279637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0062c7efe2eb5d07c30f9598ebe3d32bdd8860ebf365c7c79a81f748b839dee9`  
		Last Modified: Fri, 28 Jun 2024 22:07:02 GMT  
		Size: 234.5 MB (234539139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fb9ed0b3e5f777f462e256d9758412b677ce73d213daff0ffc92d64fa79603`  
		Last Modified: Fri, 28 Jun 2024 22:06:58 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:3b9e1f8b096d39dc2fe891765d73868316afff7ee4ffc6ca7cbc154c55b69baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4206241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa213600b0221e5ac0f23c8cdbf94a9edb92787d117865055da6db5ff6a6e566`

```dockerfile
```

-	Layers:
	-	`sha256:25bf015fc2ecb7be7975edd4aa4f780ff4658ce193789b351ae77a6558f5966f`  
		Last Modified: Fri, 28 Jun 2024 22:06:56 GMT  
		Size: 4.2 MB (4186483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92a5be3d8475dfee4e996844d50747be17e456d1fd53cfa073af053a68af92f1`  
		Last Modified: Fri, 28 Jun 2024 22:06:56 GMT  
		Size: 19.8 KB (19758 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:2dfbfffde29392298c55ca86afc275a223772c3a647583372a0600d9d13c8f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.8 MB (400843310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff755656bbe50b6e9c19c49e6e24cc763e2c2da0993a95651ecee0e7958a6448`
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
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
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
ENV TOMCAT_VERSION=9.0.90
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
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
	-	`sha256:391f04f7f495cb5fc20be69876c8638cb8f316a2cddac5d48d77ca39244e6dea`  
		Last Modified: Wed, 05 Jun 2024 03:48:14 GMT  
		Size: 35.6 MB (35588332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82f84268a93862af92928dd1cc1dc31937bbffd50302e61f899397e5223399d`  
		Last Modified: Wed, 05 Jun 2024 04:00:20 GMT  
		Size: 13.8 MB (13766991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96f8afb54eaa4d0d1271da3f9226622e5393ff92e4b765aec30aa1fcaca113a`  
		Last Modified: Wed, 05 Jun 2024 04:00:24 GMT  
		Size: 101.1 MB (101071129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59900ccb04bc654c9922cbd79216a4488310d9308aea4ecffd1d72e4eddee950`  
		Last Modified: Wed, 05 Jun 2024 04:00:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc837f7bedc9361e014f8f1c0bd2abf18e18798493eeee096794e977342e60d7`  
		Last Modified: Wed, 05 Jun 2024 04:00:15 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853d47376be40723d6b984c2403558b16158849848790d7f94be84be255b0198`  
		Last Modified: Fri, 28 Jun 2024 21:16:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b798e3939c0e9aefadd4f8df0b4406c0da240a1c3e3173bde6b82cc05e33718`  
		Last Modified: Fri, 28 Jun 2024 21:16:54 GMT  
		Size: 15.8 MB (15836765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d91e9da7368175562d63f7aee9d751ceab2a00d0b371456d7a4cdf064770c16`  
		Last Modified: Fri, 28 Jun 2024 22:10:36 GMT  
		Size: 234.6 MB (234578714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286b89930f54634e708580e88a2248ca3c8adf372430ac02210f17f19f48d9b9`  
		Last Modified: Fri, 28 Jun 2024 22:10:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:8f20b314cf578e294488364e0adb9f805438807d7c32aaedb3d9fe5a3bdfe33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4209176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5e64934f53c8df3637a3f16b0f19c307be1d64433c3b23dd3ceb0c46e29366`

```dockerfile
```

-	Layers:
	-	`sha256:bea7eba575ba69267d9a72700494da48a0be7249244e5b35a1fbd0e20f027b8d`  
		Last Modified: Fri, 28 Jun 2024 22:10:30 GMT  
		Size: 4.2 MB (4189753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a8959b3d58dad6c4954be143a9071e580015be7cb296cff5fb7215220fffaca`  
		Last Modified: Fri, 28 Jun 2024 22:10:30 GMT  
		Size: 19.4 KB (19423 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12-postgres`

```console
$ docker pull geonetwork@sha256:e105c49950f75b721cb3ce119c0e53eff232363797162b269412c4840c4f151a
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
$ docker pull geonetwork@sha256:12f5ed53202af3d1c23b376d5aed3762630f5e765f40b45b42651736d5aa26fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.6 MB (407604979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9381ca4ba74bd653bd87246c5c811727b759a8a26011ab693a9cff2078d119d8`
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
ENV TOMCAT_VERSION=9.0.90
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
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
	-	`sha256:d7e00fc5e414fea1042275ebc2c537d6eee04adead835cd35b9ca1cb599b7cc1`  
		Last Modified: Tue, 02 Jul 2024 07:10:54 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee4aadd175997f665f225d14190b3c1ff86e77c5337d3f755cd747b6180b716`  
		Last Modified: Tue, 02 Jul 2024 07:10:55 GMT  
		Size: 12.7 MB (12678754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b25e6c3da21c080a00569d7282ca1ad33f9d611ddaaa388f15fcc0db27c773d`  
		Last Modified: Tue, 02 Jul 2024 10:24:57 GMT  
		Size: 234.5 MB (234540650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2eede8d86b8ac50af7221a2cfb9ab07f6b39de6ec5755414c27020d34786dc`  
		Last Modified: Tue, 02 Jul 2024 10:24:54 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27eff3114d71270fdb5e45c24f7d58d6e26bbeed86bc245baf04dfe26baa58d`  
		Last Modified: Tue, 02 Jul 2024 11:04:01 GMT  
		Size: 13.5 MB (13467612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c7516ff6e88a4ba93c51460a9f46457338dddfc4073b7b7555cf31653c027b`  
		Last Modified: Tue, 02 Jul 2024 11:04:00 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c067e9b4f50d72275a1e737598e7d3450be368c94e182fc47647abb21588fd`  
		Last Modified: Tue, 02 Jul 2024 11:04:00 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1176f817ae6d2f5b5fd19235477cbd9dd51e9a74d6030b3d5cf6b15e380d9f38`  
		Last Modified: Tue, 02 Jul 2024 11:04:00 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:65976ae06ed276445ef3b28a87ed4607a7df0aaf3ccfca5a17b40adfd0bd139e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5745459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f746c4bddce07c947d69d98cef7c757339664f72fafb7cd5bfb2fed534cd26`

```dockerfile
```

-	Layers:
	-	`sha256:ef9bb7e9ea9232d4883f1a21485e679083e1ad9e754589820e6f609ed91a60e6`  
		Last Modified: Tue, 02 Jul 2024 11:04:00 GMT  
		Size: 5.7 MB (5722365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1cbf459bd6aae55ca18b220ef088588100a9c957013cc84b95d6d0c2f73d257`  
		Last Modified: Tue, 02 Jul 2024 11:04:00 GMT  
		Size: 23.1 KB (23094 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:9583fc2415ee9d0e29a8b5744b0cf39fb8ef162c68f3bc0ba1bcab94f9a13a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.2 MB (401155479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f39fa471b5fedc7ef2b2e0104aed15f1b88d404f04659c873deb41d538ae57`
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
ADD file:76d606bb5f897ff3ffe149c5d3d049c7ace15da77a61a7df4e558eceebd8d2bd in / 
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
ENV TOMCAT_VERSION=9.0.90
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
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
	-	`sha256:bb2b4ba5ac52e5e8a83a1f8dc3c79ed1f5409e3bc349a8c36b2cd4b9d3f6cb23`  
		Last Modified: Tue, 04 Jun 2024 01:38:51 GMT  
		Size: 27.5 MB (27534888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2e7d8e2026f154f12e834d8b72426c2f71c8a555d373336fddba91616868b7`  
		Last Modified: Wed, 05 Jun 2024 03:59:49 GMT  
		Size: 12.5 MB (12493203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95298bffd1c0ebd593eeb6754e0f5e5ba9ca25454af388f78cd657152f59cd01`  
		Last Modified: Wed, 05 Jun 2024 03:59:55 GMT  
		Size: 99.2 MB (99228750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d783cd2973ac4c20fae7efd4d2e605cff4de71ba08f4110510a1e7d7dc0239b5`  
		Last Modified: Wed, 05 Jun 2024 03:59:46 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160d32d80ad9bff0aadc9f16c0712d2e20cc58ddf491fba50571fccb3d0d77f9`  
		Last Modified: Wed, 05 Jun 2024 03:59:46 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74100269fc7beb2a5d4018be5dd2bf6efdd8e67fb196bf9ec8b743775ebc4d5e`  
		Last Modified: Fri, 28 Jun 2024 21:08:17 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77584de730899731c5a1dbcb3520dc215769824755aaf66d41a2b714ffa923f9`  
		Last Modified: Fri, 28 Jun 2024 21:08:18 GMT  
		Size: 14.8 MB (14844959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436df1fc18a76313a0106c5b0685c3dce1a4699b2612059dfe8bfbb6bbdb0a1a`  
		Last Modified: Fri, 28 Jun 2024 22:08:29 GMT  
		Size: 234.5 MB (234529688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2549c7b3f9b3e59cc4b497b768ea8f43ae6944b878d719849eed020fa24dbad`  
		Last Modified: Fri, 28 Jun 2024 22:08:23 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acb4a28192b3c239c1417c04181718154853b58c249ae4c161c0221a8a72e66`  
		Last Modified: Fri, 28 Jun 2024 22:50:43 GMT  
		Size: 12.5 MB (12519250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3292858d28de9e4b7847e6cf0cc5f0eab198ca3e43fdd45f4d1b111bec4554b`  
		Last Modified: Fri, 28 Jun 2024 22:50:42 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f1fb4222c6228e173c3ea185c22bedf424bcfa8e6b3eba2417563419fa382f`  
		Last Modified: Fri, 28 Jun 2024 22:50:42 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6982b629891747df0a8def4a1a91afe8ea7aacc756fd171bc6e88d26a5a9dd`  
		Last Modified: Fri, 28 Jun 2024 22:50:42 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:1aed45904c4ddf7a6aa1dfd707d4f785fb976cde25bc2679aef27dd284c0a8bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e75fac632ec4d2ed62fa3802896018c8ec60013ca56c0290a2ea3d9c4d7ab0e0`

```dockerfile
```

-	Layers:
	-	`sha256:e0e543d9a4a74cfbd5b868c7f4d116ab0f3576d966f40253df9ad2d139fdd14c`  
		Last Modified: Fri, 28 Jun 2024 22:50:42 GMT  
		Size: 5.7 MB (5725680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d242dd36959b19523b4f589c36c354d979735eb49485b3aab438941f767126a3`  
		Last Modified: Fri, 28 Jun 2024 22:50:42 GMT  
		Size: 23.3 KB (23320 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:f9d6eba8db70c17adaf929daaeadfb669057383461f09325fa5707df18038505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.1 MB (407149577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c8d33b48304a3fe25be8717b17f6c25aa7ee3fb7e929bb9676f23d21decf4d5`
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
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
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
ENV TOMCAT_VERSION=9.0.90
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
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
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd918abfec0657ade8aeeffe2722e92948e13fa403fd238ae22b1a9881e9402`  
		Last Modified: Wed, 05 Jun 2024 04:55:01 GMT  
		Size: 12.8 MB (12847839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5b526820dcdae2e31487a780fd45e81ebd4980b3118f35e2acbc704533db78`  
		Last Modified: Wed, 05 Jun 2024 04:55:06 GMT  
		Size: 102.7 MB (102704149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef812ceaac9fe9a1b64b4cfc38b12c1cfbe4ab5b8a0b37f60299fe0d05e5f44`  
		Last Modified: Wed, 05 Jun 2024 04:55:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f4c9c3017a82e12289bd3d8fcf61cca4f319bc017cc0f19e0f196680418917`  
		Last Modified: Wed, 05 Jun 2024 04:55:00 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f85232d9fbefdb5ebf0a56659b08993f8b0b0ba6763743db4a0e4a00d43477`  
		Last Modified: Fri, 28 Jun 2024 21:46:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318f771fe831db88763407093d7d9f7fda8b92850ef612e19cac483aff56b463`  
		Last Modified: Fri, 28 Jun 2024 21:46:53 GMT  
		Size: 15.3 MB (15279637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0062c7efe2eb5d07c30f9598ebe3d32bdd8860ebf365c7c79a81f748b839dee9`  
		Last Modified: Fri, 28 Jun 2024 22:07:02 GMT  
		Size: 234.5 MB (234539139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fb9ed0b3e5f777f462e256d9758412b677ce73d213daff0ffc92d64fa79603`  
		Last Modified: Fri, 28 Jun 2024 22:06:58 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9909cb50b748de471ff27beba1e402b51a1fa24ea87c031e3b78bed85bd44ec0`  
		Last Modified: Fri, 28 Jun 2024 23:08:06 GMT  
		Size: 13.4 MB (13371761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd9d01e419a1c15157400f44656359abe3ebbb421ad2d8b779abccc77b3e294`  
		Last Modified: Fri, 28 Jun 2024 23:08:05 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29d21169c501f89edf5ed07a4d2e107e04cd5f946115645c4293b6b6a1ada24`  
		Last Modified: Fri, 28 Jun 2024 23:08:05 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926c78299a14d92d826095b9aa817f35f8d65366bd73c8f88f29cca34dfe720e`  
		Last Modified: Fri, 28 Jun 2024 23:08:06 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:760dffa6592f733791ef4032f6dc6f8e401439c5098b831544559e1b81cda9ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5754046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1695e6bb409e56bf3bfdfe8f80ebef683a17eca27d3e7cf3553755b693624203`

```dockerfile
```

-	Layers:
	-	`sha256:ca208a077d0ee63fa551d29650daa2dd620171f5526ccd161466fda8fc1634c1`  
		Last Modified: Fri, 28 Jun 2024 23:08:05 GMT  
		Size: 5.7 MB (5730429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b48bb8d93ba72ebd2fb2a82673d631d29aba65f90948de972b58b8a3433c845`  
		Last Modified: Fri, 28 Jun 2024 23:08:05 GMT  
		Size: 23.6 KB (23617 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:8efb740dd76a45a30c2a30b795de39fb377b84d994026c7180ac98a67f3f5295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.8 MB (414808113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6b247f422f949f308acf431cab02ec6be93616d32a4ab6784b2b3fd2c86382`
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
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
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
ENV TOMCAT_VERSION=9.0.90
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
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
	-	`sha256:391f04f7f495cb5fc20be69876c8638cb8f316a2cddac5d48d77ca39244e6dea`  
		Last Modified: Wed, 05 Jun 2024 03:48:14 GMT  
		Size: 35.6 MB (35588332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82f84268a93862af92928dd1cc1dc31937bbffd50302e61f899397e5223399d`  
		Last Modified: Wed, 05 Jun 2024 04:00:20 GMT  
		Size: 13.8 MB (13766991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96f8afb54eaa4d0d1271da3f9226622e5393ff92e4b765aec30aa1fcaca113a`  
		Last Modified: Wed, 05 Jun 2024 04:00:24 GMT  
		Size: 101.1 MB (101071129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59900ccb04bc654c9922cbd79216a4488310d9308aea4ecffd1d72e4eddee950`  
		Last Modified: Wed, 05 Jun 2024 04:00:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc837f7bedc9361e014f8f1c0bd2abf18e18798493eeee096794e977342e60d7`  
		Last Modified: Wed, 05 Jun 2024 04:00:15 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853d47376be40723d6b984c2403558b16158849848790d7f94be84be255b0198`  
		Last Modified: Fri, 28 Jun 2024 21:16:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b798e3939c0e9aefadd4f8df0b4406c0da240a1c3e3173bde6b82cc05e33718`  
		Last Modified: Fri, 28 Jun 2024 21:16:54 GMT  
		Size: 15.8 MB (15836765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d91e9da7368175562d63f7aee9d751ceab2a00d0b371456d7a4cdf064770c16`  
		Last Modified: Fri, 28 Jun 2024 22:10:36 GMT  
		Size: 234.6 MB (234578714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286b89930f54634e708580e88a2248ca3c8adf372430ac02210f17f19f48d9b9`  
		Last Modified: Fri, 28 Jun 2024 22:10:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92349d34efe36b909230a147da8135f66d515f5ee93031dc082f91487b9c05c`  
		Last Modified: Fri, 28 Jun 2024 22:51:01 GMT  
		Size: 14.0 MB (13961436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0717d03446a58008b145ed2b671ab88b4bc897e57cf58efcbe37dbf7bc87d91`  
		Last Modified: Fri, 28 Jun 2024 22:51:00 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbfbbca2af2f608f17a0706c342fd0aaac1e8150462452e6bdaa05baf46fe25`  
		Last Modified: Fri, 28 Jun 2024 22:51:00 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a835d57efaedbfc4ccb2157762db382dea430785dc6f260d2a9fe22c0341769`  
		Last Modified: Fri, 28 Jun 2024 22:51:01 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:3410e27ac0266bd4b44c517928b5524749d46e3ace195efe7df7ca7a9ceff2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5753648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147a36669c74579a6428c2939acadc077f1d2c3cc47f27d5a9da41fb459cba4a`

```dockerfile
```

-	Layers:
	-	`sha256:e3225ade187b1b20c9407e1241370df9b7fd39cdd23208a33af2a15aecac9339`  
		Last Modified: Fri, 28 Jun 2024 22:51:00 GMT  
		Size: 5.7 MB (5730364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af921df2e922ad8270df634a2efde1e07f15f65fdcf47632308bf465ee396535`  
		Last Modified: Fri, 28 Jun 2024 22:51:00 GMT  
		Size: 23.3 KB (23284 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12.11`

```console
$ docker pull geonetwork@sha256:bac3c8d478809cdda58dc71dfc32aef67aa7a8dee455b6698cd79246ed4096e6
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
$ docker pull geonetwork@sha256:e5ee99d2844bab3c9bf4343952364b8c7e740b747dc393b2e7bd8bfe6a3a602d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.1 MB (394134008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2170765dde92ba9dd79b916634973766a9980a6c47170ee91fa332d7a11e5100`
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
ENV TOMCAT_VERSION=9.0.90
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
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
	-	`sha256:d7e00fc5e414fea1042275ebc2c537d6eee04adead835cd35b9ca1cb599b7cc1`  
		Last Modified: Tue, 02 Jul 2024 07:10:54 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee4aadd175997f665f225d14190b3c1ff86e77c5337d3f755cd747b6180b716`  
		Last Modified: Tue, 02 Jul 2024 07:10:55 GMT  
		Size: 12.7 MB (12678754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b25e6c3da21c080a00569d7282ca1ad33f9d611ddaaa388f15fcc0db27c773d`  
		Last Modified: Tue, 02 Jul 2024 10:24:57 GMT  
		Size: 234.5 MB (234540650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2eede8d86b8ac50af7221a2cfb9ab07f6b39de6ec5755414c27020d34786dc`  
		Last Modified: Tue, 02 Jul 2024 10:24:54 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.11` - unknown; unknown

```console
$ docker pull geonetwork@sha256:4e3c9a793bd03e8a72ab2d1630e10338809693a2d22388707cbcef111edb884e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4203700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d703d149540965813ac363f6c81186f2cf11545a9e66d3a7ad14db10ee221b`

```dockerfile
```

-	Layers:
	-	`sha256:b8380102d31109b253c1961b596b7274210997d852febb9caadac41042302dea`  
		Last Modified: Tue, 02 Jul 2024 10:24:54 GMT  
		Size: 4.2 MB (4184466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a55a41411dbf8c8fae10e76a44f4cbae30403027fb40db92fc27bf96b26ed34`  
		Last Modified: Tue, 02 Jul 2024 10:24:53 GMT  
		Size: 19.2 KB (19234 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.11` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:43a3308bde28fbd6dfb0f158a7cfe20674f1b5e92fd164e06204a62cdb4f18a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.6 MB (388632868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a6343edd493eb040d5c675d009063f13e96d03d9a3411400a666eaad08a0ff`
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
ADD file:76d606bb5f897ff3ffe149c5d3d049c7ace15da77a61a7df4e558eceebd8d2bd in / 
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
ENV TOMCAT_VERSION=9.0.90
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
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
	-	`sha256:bb2b4ba5ac52e5e8a83a1f8dc3c79ed1f5409e3bc349a8c36b2cd4b9d3f6cb23`  
		Last Modified: Tue, 04 Jun 2024 01:38:51 GMT  
		Size: 27.5 MB (27534888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2e7d8e2026f154f12e834d8b72426c2f71c8a555d373336fddba91616868b7`  
		Last Modified: Wed, 05 Jun 2024 03:59:49 GMT  
		Size: 12.5 MB (12493203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95298bffd1c0ebd593eeb6754e0f5e5ba9ca25454af388f78cd657152f59cd01`  
		Last Modified: Wed, 05 Jun 2024 03:59:55 GMT  
		Size: 99.2 MB (99228750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d783cd2973ac4c20fae7efd4d2e605cff4de71ba08f4110510a1e7d7dc0239b5`  
		Last Modified: Wed, 05 Jun 2024 03:59:46 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160d32d80ad9bff0aadc9f16c0712d2e20cc58ddf491fba50571fccb3d0d77f9`  
		Last Modified: Wed, 05 Jun 2024 03:59:46 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74100269fc7beb2a5d4018be5dd2bf6efdd8e67fb196bf9ec8b743775ebc4d5e`  
		Last Modified: Fri, 28 Jun 2024 21:08:17 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77584de730899731c5a1dbcb3520dc215769824755aaf66d41a2b714ffa923f9`  
		Last Modified: Fri, 28 Jun 2024 21:08:18 GMT  
		Size: 14.8 MB (14844959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436df1fc18a76313a0106c5b0685c3dce1a4699b2612059dfe8bfbb6bbdb0a1a`  
		Last Modified: Fri, 28 Jun 2024 22:08:29 GMT  
		Size: 234.5 MB (234529688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2549c7b3f9b3e59cc4b497b768ea8f43ae6944b878d719849eed020fa24dbad`  
		Last Modified: Fri, 28 Jun 2024 22:08:23 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.11` - unknown; unknown

```console
$ docker pull geonetwork@sha256:381c4f3cc3d99ce567517b3757857ddea677c6eb6222a01b700c9f53984740ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6586a5c4b0782c5c84f8a48824367801d56317c115f9cc2c8b60ce5a3e316ff`

```dockerfile
```

-	Layers:
	-	`sha256:5ff4884c4405455d6a5997093436ad7a12033099f89b9c4b3131ce2994491e01`  
		Last Modified: Fri, 28 Jun 2024 22:08:24 GMT  
		Size: 4.2 MB (4189072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b744117d5c0d8c25cb56b617d7739100fd0f8cc6a7a44441d9d93c5ed9fc3ab1`  
		Last Modified: Fri, 28 Jun 2024 22:08:22 GMT  
		Size: 19.4 KB (19448 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.11` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:989d485a95ea7d995cd7879f37dc6499b64c985097881c764c039fa1df00c2b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393774450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93923f8bb8410a1e6f693112c9b244ef3414f0ad41ddd2c51322e47409c3096`
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
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
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
ENV TOMCAT_VERSION=9.0.90
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
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
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd918abfec0657ade8aeeffe2722e92948e13fa403fd238ae22b1a9881e9402`  
		Last Modified: Wed, 05 Jun 2024 04:55:01 GMT  
		Size: 12.8 MB (12847839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5b526820dcdae2e31487a780fd45e81ebd4980b3118f35e2acbc704533db78`  
		Last Modified: Wed, 05 Jun 2024 04:55:06 GMT  
		Size: 102.7 MB (102704149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef812ceaac9fe9a1b64b4cfc38b12c1cfbe4ab5b8a0b37f60299fe0d05e5f44`  
		Last Modified: Wed, 05 Jun 2024 04:55:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f4c9c3017a82e12289bd3d8fcf61cca4f319bc017cc0f19e0f196680418917`  
		Last Modified: Wed, 05 Jun 2024 04:55:00 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f85232d9fbefdb5ebf0a56659b08993f8b0b0ba6763743db4a0e4a00d43477`  
		Last Modified: Fri, 28 Jun 2024 21:46:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318f771fe831db88763407093d7d9f7fda8b92850ef612e19cac483aff56b463`  
		Last Modified: Fri, 28 Jun 2024 21:46:53 GMT  
		Size: 15.3 MB (15279637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0062c7efe2eb5d07c30f9598ebe3d32bdd8860ebf365c7c79a81f748b839dee9`  
		Last Modified: Fri, 28 Jun 2024 22:07:02 GMT  
		Size: 234.5 MB (234539139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fb9ed0b3e5f777f462e256d9758412b677ce73d213daff0ffc92d64fa79603`  
		Last Modified: Fri, 28 Jun 2024 22:06:58 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.11` - unknown; unknown

```console
$ docker pull geonetwork@sha256:3b9e1f8b096d39dc2fe891765d73868316afff7ee4ffc6ca7cbc154c55b69baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4206241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa213600b0221e5ac0f23c8cdbf94a9edb92787d117865055da6db5ff6a6e566`

```dockerfile
```

-	Layers:
	-	`sha256:25bf015fc2ecb7be7975edd4aa4f780ff4658ce193789b351ae77a6558f5966f`  
		Last Modified: Fri, 28 Jun 2024 22:06:56 GMT  
		Size: 4.2 MB (4186483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92a5be3d8475dfee4e996844d50747be17e456d1fd53cfa073af053a68af92f1`  
		Last Modified: Fri, 28 Jun 2024 22:06:56 GMT  
		Size: 19.8 KB (19758 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.11` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:2dfbfffde29392298c55ca86afc275a223772c3a647583372a0600d9d13c8f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.8 MB (400843310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff755656bbe50b6e9c19c49e6e24cc763e2c2da0993a95651ecee0e7958a6448`
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
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
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
ENV TOMCAT_VERSION=9.0.90
# Tue, 02 Apr 2024 10:10:05 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
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
	-	`sha256:391f04f7f495cb5fc20be69876c8638cb8f316a2cddac5d48d77ca39244e6dea`  
		Last Modified: Wed, 05 Jun 2024 03:48:14 GMT  
		Size: 35.6 MB (35588332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82f84268a93862af92928dd1cc1dc31937bbffd50302e61f899397e5223399d`  
		Last Modified: Wed, 05 Jun 2024 04:00:20 GMT  
		Size: 13.8 MB (13766991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96f8afb54eaa4d0d1271da3f9226622e5393ff92e4b765aec30aa1fcaca113a`  
		Last Modified: Wed, 05 Jun 2024 04:00:24 GMT  
		Size: 101.1 MB (101071129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59900ccb04bc654c9922cbd79216a4488310d9308aea4ecffd1d72e4eddee950`  
		Last Modified: Wed, 05 Jun 2024 04:00:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc837f7bedc9361e014f8f1c0bd2abf18e18798493eeee096794e977342e60d7`  
		Last Modified: Wed, 05 Jun 2024 04:00:15 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853d47376be40723d6b984c2403558b16158849848790d7f94be84be255b0198`  
		Last Modified: Fri, 28 Jun 2024 21:16:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b798e3939c0e9aefadd4f8df0b4406c0da240a1c3e3173bde6b82cc05e33718`  
		Last Modified: Fri, 28 Jun 2024 21:16:54 GMT  
		Size: 15.8 MB (15836765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d91e9da7368175562d63f7aee9d751ceab2a00d0b371456d7a4cdf064770c16`  
		Last Modified: Fri, 28 Jun 2024 22:10:36 GMT  
		Size: 234.6 MB (234578714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286b89930f54634e708580e88a2248ca3c8adf372430ac02210f17f19f48d9b9`  
		Last Modified: Fri, 28 Jun 2024 22:10:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.11` - unknown; unknown

```console
$ docker pull geonetwork@sha256:8f20b314cf578e294488364e0adb9f805438807d7c32aaedb3d9fe5a3bdfe33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4209176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5e64934f53c8df3637a3f16b0f19c307be1d64433c3b23dd3ceb0c46e29366`

```dockerfile
```

-	Layers:
	-	`sha256:bea7eba575ba69267d9a72700494da48a0be7249244e5b35a1fbd0e20f027b8d`  
		Last Modified: Fri, 28 Jun 2024 22:10:30 GMT  
		Size: 4.2 MB (4189753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a8959b3d58dad6c4954be143a9071e580015be7cb296cff5fb7215220fffaca`  
		Last Modified: Fri, 28 Jun 2024 22:10:30 GMT  
		Size: 19.4 KB (19423 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12.11-postgres`

```console
$ docker pull geonetwork@sha256:e105c49950f75b721cb3ce119c0e53eff232363797162b269412c4840c4f151a
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
$ docker pull geonetwork@sha256:12f5ed53202af3d1c23b376d5aed3762630f5e765f40b45b42651736d5aa26fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.6 MB (407604979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9381ca4ba74bd653bd87246c5c811727b759a8a26011ab693a9cff2078d119d8`
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
ENV TOMCAT_VERSION=9.0.90
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
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
	-	`sha256:d7e00fc5e414fea1042275ebc2c537d6eee04adead835cd35b9ca1cb599b7cc1`  
		Last Modified: Tue, 02 Jul 2024 07:10:54 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee4aadd175997f665f225d14190b3c1ff86e77c5337d3f755cd747b6180b716`  
		Last Modified: Tue, 02 Jul 2024 07:10:55 GMT  
		Size: 12.7 MB (12678754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b25e6c3da21c080a00569d7282ca1ad33f9d611ddaaa388f15fcc0db27c773d`  
		Last Modified: Tue, 02 Jul 2024 10:24:57 GMT  
		Size: 234.5 MB (234540650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2eede8d86b8ac50af7221a2cfb9ab07f6b39de6ec5755414c27020d34786dc`  
		Last Modified: Tue, 02 Jul 2024 10:24:54 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27eff3114d71270fdb5e45c24f7d58d6e26bbeed86bc245baf04dfe26baa58d`  
		Last Modified: Tue, 02 Jul 2024 11:04:01 GMT  
		Size: 13.5 MB (13467612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c7516ff6e88a4ba93c51460a9f46457338dddfc4073b7b7555cf31653c027b`  
		Last Modified: Tue, 02 Jul 2024 11:04:00 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c067e9b4f50d72275a1e737598e7d3450be368c94e182fc47647abb21588fd`  
		Last Modified: Tue, 02 Jul 2024 11:04:00 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1176f817ae6d2f5b5fd19235477cbd9dd51e9a74d6030b3d5cf6b15e380d9f38`  
		Last Modified: Tue, 02 Jul 2024 11:04:00 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.11-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:65976ae06ed276445ef3b28a87ed4607a7df0aaf3ccfca5a17b40adfd0bd139e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5745459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f746c4bddce07c947d69d98cef7c757339664f72fafb7cd5bfb2fed534cd26`

```dockerfile
```

-	Layers:
	-	`sha256:ef9bb7e9ea9232d4883f1a21485e679083e1ad9e754589820e6f609ed91a60e6`  
		Last Modified: Tue, 02 Jul 2024 11:04:00 GMT  
		Size: 5.7 MB (5722365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1cbf459bd6aae55ca18b220ef088588100a9c957013cc84b95d6d0c2f73d257`  
		Last Modified: Tue, 02 Jul 2024 11:04:00 GMT  
		Size: 23.1 KB (23094 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.11-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:9583fc2415ee9d0e29a8b5744b0cf39fb8ef162c68f3bc0ba1bcab94f9a13a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.2 MB (401155479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f39fa471b5fedc7ef2b2e0104aed15f1b88d404f04659c873deb41d538ae57`
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
ADD file:76d606bb5f897ff3ffe149c5d3d049c7ace15da77a61a7df4e558eceebd8d2bd in / 
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
ENV TOMCAT_VERSION=9.0.90
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
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
	-	`sha256:bb2b4ba5ac52e5e8a83a1f8dc3c79ed1f5409e3bc349a8c36b2cd4b9d3f6cb23`  
		Last Modified: Tue, 04 Jun 2024 01:38:51 GMT  
		Size: 27.5 MB (27534888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2e7d8e2026f154f12e834d8b72426c2f71c8a555d373336fddba91616868b7`  
		Last Modified: Wed, 05 Jun 2024 03:59:49 GMT  
		Size: 12.5 MB (12493203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95298bffd1c0ebd593eeb6754e0f5e5ba9ca25454af388f78cd657152f59cd01`  
		Last Modified: Wed, 05 Jun 2024 03:59:55 GMT  
		Size: 99.2 MB (99228750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d783cd2973ac4c20fae7efd4d2e605cff4de71ba08f4110510a1e7d7dc0239b5`  
		Last Modified: Wed, 05 Jun 2024 03:59:46 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160d32d80ad9bff0aadc9f16c0712d2e20cc58ddf491fba50571fccb3d0d77f9`  
		Last Modified: Wed, 05 Jun 2024 03:59:46 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74100269fc7beb2a5d4018be5dd2bf6efdd8e67fb196bf9ec8b743775ebc4d5e`  
		Last Modified: Fri, 28 Jun 2024 21:08:17 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77584de730899731c5a1dbcb3520dc215769824755aaf66d41a2b714ffa923f9`  
		Last Modified: Fri, 28 Jun 2024 21:08:18 GMT  
		Size: 14.8 MB (14844959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436df1fc18a76313a0106c5b0685c3dce1a4699b2612059dfe8bfbb6bbdb0a1a`  
		Last Modified: Fri, 28 Jun 2024 22:08:29 GMT  
		Size: 234.5 MB (234529688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2549c7b3f9b3e59cc4b497b768ea8f43ae6944b878d719849eed020fa24dbad`  
		Last Modified: Fri, 28 Jun 2024 22:08:23 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acb4a28192b3c239c1417c04181718154853b58c249ae4c161c0221a8a72e66`  
		Last Modified: Fri, 28 Jun 2024 22:50:43 GMT  
		Size: 12.5 MB (12519250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3292858d28de9e4b7847e6cf0cc5f0eab198ca3e43fdd45f4d1b111bec4554b`  
		Last Modified: Fri, 28 Jun 2024 22:50:42 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f1fb4222c6228e173c3ea185c22bedf424bcfa8e6b3eba2417563419fa382f`  
		Last Modified: Fri, 28 Jun 2024 22:50:42 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6982b629891747df0a8def4a1a91afe8ea7aacc756fd171bc6e88d26a5a9dd`  
		Last Modified: Fri, 28 Jun 2024 22:50:42 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.11-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:1aed45904c4ddf7a6aa1dfd707d4f785fb976cde25bc2679aef27dd284c0a8bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e75fac632ec4d2ed62fa3802896018c8ec60013ca56c0290a2ea3d9c4d7ab0e0`

```dockerfile
```

-	Layers:
	-	`sha256:e0e543d9a4a74cfbd5b868c7f4d116ab0f3576d966f40253df9ad2d139fdd14c`  
		Last Modified: Fri, 28 Jun 2024 22:50:42 GMT  
		Size: 5.7 MB (5725680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d242dd36959b19523b4f589c36c354d979735eb49485b3aab438941f767126a3`  
		Last Modified: Fri, 28 Jun 2024 22:50:42 GMT  
		Size: 23.3 KB (23320 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.11-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:f9d6eba8db70c17adaf929daaeadfb669057383461f09325fa5707df18038505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.1 MB (407149577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c8d33b48304a3fe25be8717b17f6c25aa7ee3fb7e929bb9676f23d21decf4d5`
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
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
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
ENV TOMCAT_VERSION=9.0.90
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
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
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd918abfec0657ade8aeeffe2722e92948e13fa403fd238ae22b1a9881e9402`  
		Last Modified: Wed, 05 Jun 2024 04:55:01 GMT  
		Size: 12.8 MB (12847839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5b526820dcdae2e31487a780fd45e81ebd4980b3118f35e2acbc704533db78`  
		Last Modified: Wed, 05 Jun 2024 04:55:06 GMT  
		Size: 102.7 MB (102704149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef812ceaac9fe9a1b64b4cfc38b12c1cfbe4ab5b8a0b37f60299fe0d05e5f44`  
		Last Modified: Wed, 05 Jun 2024 04:55:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f4c9c3017a82e12289bd3d8fcf61cca4f319bc017cc0f19e0f196680418917`  
		Last Modified: Wed, 05 Jun 2024 04:55:00 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f85232d9fbefdb5ebf0a56659b08993f8b0b0ba6763743db4a0e4a00d43477`  
		Last Modified: Fri, 28 Jun 2024 21:46:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318f771fe831db88763407093d7d9f7fda8b92850ef612e19cac483aff56b463`  
		Last Modified: Fri, 28 Jun 2024 21:46:53 GMT  
		Size: 15.3 MB (15279637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0062c7efe2eb5d07c30f9598ebe3d32bdd8860ebf365c7c79a81f748b839dee9`  
		Last Modified: Fri, 28 Jun 2024 22:07:02 GMT  
		Size: 234.5 MB (234539139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fb9ed0b3e5f777f462e256d9758412b677ce73d213daff0ffc92d64fa79603`  
		Last Modified: Fri, 28 Jun 2024 22:06:58 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9909cb50b748de471ff27beba1e402b51a1fa24ea87c031e3b78bed85bd44ec0`  
		Last Modified: Fri, 28 Jun 2024 23:08:06 GMT  
		Size: 13.4 MB (13371761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd9d01e419a1c15157400f44656359abe3ebbb421ad2d8b779abccc77b3e294`  
		Last Modified: Fri, 28 Jun 2024 23:08:05 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29d21169c501f89edf5ed07a4d2e107e04cd5f946115645c4293b6b6a1ada24`  
		Last Modified: Fri, 28 Jun 2024 23:08:05 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926c78299a14d92d826095b9aa817f35f8d65366bd73c8f88f29cca34dfe720e`  
		Last Modified: Fri, 28 Jun 2024 23:08:06 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.11-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:760dffa6592f733791ef4032f6dc6f8e401439c5098b831544559e1b81cda9ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5754046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1695e6bb409e56bf3bfdfe8f80ebef683a17eca27d3e7cf3553755b693624203`

```dockerfile
```

-	Layers:
	-	`sha256:ca208a077d0ee63fa551d29650daa2dd620171f5526ccd161466fda8fc1634c1`  
		Last Modified: Fri, 28 Jun 2024 23:08:05 GMT  
		Size: 5.7 MB (5730429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b48bb8d93ba72ebd2fb2a82673d631d29aba65f90948de972b58b8a3433c845`  
		Last Modified: Fri, 28 Jun 2024 23:08:05 GMT  
		Size: 23.6 KB (23617 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.11-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:8efb740dd76a45a30c2a30b795de39fb377b84d994026c7180ac98a67f3f5295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.8 MB (414808113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6b247f422f949f308acf431cab02ec6be93616d32a4ab6784b2b3fd2c86382`
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
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
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
ENV TOMCAT_VERSION=9.0.90
# Thu, 05 Oct 2023 16:23:50 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
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
	-	`sha256:391f04f7f495cb5fc20be69876c8638cb8f316a2cddac5d48d77ca39244e6dea`  
		Last Modified: Wed, 05 Jun 2024 03:48:14 GMT  
		Size: 35.6 MB (35588332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82f84268a93862af92928dd1cc1dc31937bbffd50302e61f899397e5223399d`  
		Last Modified: Wed, 05 Jun 2024 04:00:20 GMT  
		Size: 13.8 MB (13766991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96f8afb54eaa4d0d1271da3f9226622e5393ff92e4b765aec30aa1fcaca113a`  
		Last Modified: Wed, 05 Jun 2024 04:00:24 GMT  
		Size: 101.1 MB (101071129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59900ccb04bc654c9922cbd79216a4488310d9308aea4ecffd1d72e4eddee950`  
		Last Modified: Wed, 05 Jun 2024 04:00:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc837f7bedc9361e014f8f1c0bd2abf18e18798493eeee096794e977342e60d7`  
		Last Modified: Wed, 05 Jun 2024 04:00:15 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853d47376be40723d6b984c2403558b16158849848790d7f94be84be255b0198`  
		Last Modified: Fri, 28 Jun 2024 21:16:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b798e3939c0e9aefadd4f8df0b4406c0da240a1c3e3173bde6b82cc05e33718`  
		Last Modified: Fri, 28 Jun 2024 21:16:54 GMT  
		Size: 15.8 MB (15836765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d91e9da7368175562d63f7aee9d751ceab2a00d0b371456d7a4cdf064770c16`  
		Last Modified: Fri, 28 Jun 2024 22:10:36 GMT  
		Size: 234.6 MB (234578714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286b89930f54634e708580e88a2248ca3c8adf372430ac02210f17f19f48d9b9`  
		Last Modified: Fri, 28 Jun 2024 22:10:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92349d34efe36b909230a147da8135f66d515f5ee93031dc082f91487b9c05c`  
		Last Modified: Fri, 28 Jun 2024 22:51:01 GMT  
		Size: 14.0 MB (13961436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0717d03446a58008b145ed2b671ab88b4bc897e57cf58efcbe37dbf7bc87d91`  
		Last Modified: Fri, 28 Jun 2024 22:51:00 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbfbbca2af2f608f17a0706c342fd0aaac1e8150462452e6bdaa05baf46fe25`  
		Last Modified: Fri, 28 Jun 2024 22:51:00 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a835d57efaedbfc4ccb2157762db382dea430785dc6f260d2a9fe22c0341769`  
		Last Modified: Fri, 28 Jun 2024 22:51:01 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.11-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:3410e27ac0266bd4b44c517928b5524749d46e3ace195efe7df7ca7a9ceff2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5753648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147a36669c74579a6428c2939acadc077f1d2c3cc47f27d5a9da41fb459cba4a`

```dockerfile
```

-	Layers:
	-	`sha256:e3225ade187b1b20c9407e1241370df9b7fd39cdd23208a33af2a15aecac9339`  
		Last Modified: Fri, 28 Jun 2024 22:51:00 GMT  
		Size: 5.7 MB (5730364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af921df2e922ad8270df634a2efde1e07f15f65fdcf47632308bf465ee396535`  
		Last Modified: Fri, 28 Jun 2024 22:51:00 GMT  
		Size: 23.3 KB (23284 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4`

```console
$ docker pull geonetwork@sha256:94e49e0549680c5e655b3f7061fe488df1e48f69eb01511dbf2edcb05ba30310
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:4` - linux; amd64

```console
$ docker pull geonetwork@sha256:8ee2fc97ea1738ca35996d698dd773f1d8b63b8d4f50bc776abd10ed5e8cc1cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.0 MB (488041018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830528afbee6f9473e10fc06979d082a8889e6cbdc2acf0f0f7970192be89c85`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 15 Mar 2024 05:21:34 GMT
ARG RELEASE
# Fri, 15 Mar 2024 05:21:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 15 Mar 2024 05:21:34 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["/bin/bash"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["jshell"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_VERSION=9.4.54.v20240208
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.54.v20240208/jetty-home-9.4.54.v20240208.tar.gz
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
WORKDIR /var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
USER jetty
# Fri, 15 Mar 2024 05:21:34 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
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
	-	`sha256:24aeef90818f4bccf7d9bd6e0be8387a60d437936ced45ff5e61d80ef9778e94`  
		Last Modified: Wed, 05 Jun 2024 04:59:06 GMT  
		Size: 145.5 MB (145507603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0aa573dbf90a7e06817e01a23139b1f8b8093a2bb43b4050b665696d2aaaeb`  
		Last Modified: Wed, 05 Jun 2024 04:58:55 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780a38247a5709082a621a5e1fbb5742e9b82f20b9235f8c349dbbcdd41e108a`  
		Last Modified: Wed, 05 Jun 2024 04:58:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ed127625f83ec444fec38b0b727026c8f21c761495116c75dc3037a30598fc`  
		Last Modified: Fri, 28 Jun 2024 20:56:37 GMT  
		Size: 10.0 MB (10016385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864f11609f3fd19154163fd5bd3233c507fcc543fa8e8a01a4e36331955ff7aa`  
		Last Modified: Fri, 28 Jun 2024 20:56:36 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3b2a2e233dc5f88c7a255301fbd815476fe133ed69da26a69a7a8031167449`  
		Last Modified: Fri, 28 Jun 2024 22:01:08 GMT  
		Size: 245.2 KB (245173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4901c4849048870e3c5e2b06beee5f54522e229933dd44f58b35d383fe7065`  
		Last Modified: Fri, 28 Jun 2024 22:01:11 GMT  
		Size: 286.8 MB (286763023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2421c5e6fa1d811aab6fe1d73d54be1fd8cc555e25c86765721cc6998f7bc`  
		Last Modified: Fri, 28 Jun 2024 22:01:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e508dd540564f697742a8ddc66e5a383d080f9a3eddbe01ea1427210ce333fa`  
		Last Modified: Fri, 28 Jun 2024 22:01:08 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2c246230b5bd8f2c38db8576be72e0ca61eb28a79118cc158e9ba2997c474c`  
		Last Modified: Fri, 28 Jun 2024 22:01:09 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:10b5fc0fd8f8fe834e6e0fe91990973ca9038718119e23b617180133addff4f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4199714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bda5189c535fb9b2b074151d23179f2ba5429b3cd5dcf9f178e98e68fb20cd`

```dockerfile
```

-	Layers:
	-	`sha256:4a135e6108fd831a0b7355372f9b0e015396567a8412d0cda645107fc4ae090f`  
		Last Modified: Fri, 28 Jun 2024 22:01:08 GMT  
		Size: 4.2 MB (4174054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9181634f66b16ff77b191e2b4e53460fd6ce0458f449b9dd9a2823e07bf13216`  
		Last Modified: Fri, 28 Jun 2024 22:01:08 GMT  
		Size: 25.7 KB (25660 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:9e3c2e9122a9786c20dd09abc02a4b86980c480f5e34f0c63305c02456146e4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.3 MB (483321454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ecbc49bf790f8fb29cb1ad028db0d82a70c6665497c239776e113e152850ff`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 15 Mar 2024 05:21:34 GMT
ARG RELEASE
# Fri, 15 Mar 2024 05:21:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 15 Mar 2024 05:21:34 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["/bin/bash"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["jshell"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_VERSION=9.4.54.v20240208
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.54.v20240208/jetty-home-9.4.54.v20240208.tar.gz
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
WORKDIR /var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
USER jetty
# Fri, 15 Mar 2024 05:21:34 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
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
	-	`sha256:3294c18dc189f71e82fdd6779b6b0d69ba8defe38e3e26bb53031dfcf05f4add`  
		Last Modified: Wed, 05 Jun 2024 04:55:50 GMT  
		Size: 142.3 MB (142312188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3740768ca48a1b10a3ee451ba3bd551f320fa113d2505c2b877a1d3fd02a2f97`  
		Last Modified: Wed, 05 Jun 2024 04:55:41 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39f12d5bcae89c5e56ddf77b9c89b3bea51ce03ca339db4e9e846e4711e94ad`  
		Last Modified: Wed, 05 Jun 2024 04:55:41 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c24ea46ddb6e25d218f52432ef4bfc56436b2babf033f99ef25e09d514b662`  
		Last Modified: Fri, 28 Jun 2024 21:01:52 GMT  
		Size: 10.0 MB (10016315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f24f1da7328caf2e84f1313a1ddfa52d338df679e7459246c921303a39a939`  
		Last Modified: Fri, 28 Jun 2024 21:01:51 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d162f9b3ffd7ab9c27dca70cf2e7624e8aadb5b2cbb29cdaacedd9308e791d`  
		Last Modified: Fri, 28 Jun 2024 22:10:10 GMT  
		Size: 243.8 KB (243827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2452c019648c3f067c67337cf924382882920b138a122825b1cd77a4caa102d4`  
		Last Modified: Fri, 28 Jun 2024 22:10:17 GMT  
		Size: 286.8 MB (286763067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aa2e558d78f27f9c394da51eda167974da7cd0f6ce9dff772b8efe50e1e04e`  
		Last Modified: Fri, 28 Jun 2024 22:10:10 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb829a274aa00e7ceb10c717641a7b69bd72250e0d3469fc1047abdfd170065b`  
		Last Modified: Fri, 28 Jun 2024 22:10:10 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68af11bac0950ec0ed18caee0591cb8029ee55e6b337ea1af18183f352e6eee`  
		Last Modified: Fri, 28 Jun 2024 22:10:11 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:82aa627aa4950fbda7e6eea441f31c7f4c0fd8d8be7a68a48f853819702c4c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4200588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df680b3be880914c8429a3b07f8aaa81a5ca29a915cd83a65c01cf0421932dd`

```dockerfile
```

-	Layers:
	-	`sha256:3569d8bd16483a69609db6bd1c5286ea873d6d92dc7a5bb26d9d0253950dd8ba`  
		Last Modified: Fri, 28 Jun 2024 22:10:10 GMT  
		Size: 4.2 MB (4174363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcaeb0b68138f8a76091e5f43cd3dba7c2f49c0422cacde797e632b3756b6449`  
		Last Modified: Fri, 28 Jun 2024 22:10:10 GMT  
		Size: 26.2 KB (26225 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.2`

```console
$ docker pull geonetwork@sha256:201c334df76ef105db8482c1b593d7e985918d4814755cfd2697ab6906c52177
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:4.2` - linux; amd64

```console
$ docker pull geonetwork@sha256:721554644a8112aa7047e9db3550dd85186643be5aec15b2ffae0a8bc5845233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.3 MB (461306351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb683a4f85a446b4a5fabd4c7ef225a8aa76826f0224151ed1b564a904af6f4`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 15 Mar 2024 05:21:34 GMT
ARG RELEASE
# Fri, 15 Mar 2024 05:21:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 15 Mar 2024 05:21:34 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["/bin/bash"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_VERSION=9.4.54.v20240208
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.54.v20240208/jetty-home-9.4.54.v20240208.tar.gz
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
WORKDIR /var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
USER jetty
# Fri, 15 Mar 2024 05:21:34 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
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
	-	`sha256:86c361d921973a199295dea7b1a08340c6444ee42f6b23b2e924aa5100420f67`  
		Last Modified: Wed, 05 Jun 2024 04:57:54 GMT  
		Size: 103.6 MB (103602581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409c91c0433db39de61b0193a2498b60890893ce6b3cb2b9e1c751bfdc919224`  
		Last Modified: Wed, 05 Jun 2024 04:57:46 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd20a24d30f10019507281b17336eb76b4dd341fcbca56686e570a18717dda`  
		Last Modified: Wed, 05 Jun 2024 04:57:46 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a76b3a06a48a558f2a3cb2d6084a3b9c00a6c7f2a9adb6252e6466c5ef50f3`  
		Last Modified: Fri, 28 Jun 2024 20:56:36 GMT  
		Size: 10.0 MB (10015384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce440ea07f96bf41cb530f892e7b8764bb827cf0d5d869aa99db55b6a06fc7d3`  
		Last Modified: Fri, 28 Jun 2024 20:56:30 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97789c2b105cc8bab3aea822d4a04aa4e345ec1d7aa45423e67fae054e1afd9`  
		Last Modified: Fri, 28 Jun 2024 22:00:22 GMT  
		Size: 245.2 KB (245240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15e5235ceacc2c1ae37666fe0f4d51098f2a70a297558b60b41db14aacb675d`  
		Last Modified: Fri, 28 Jun 2024 22:00:26 GMT  
		Size: 301.9 MB (301934653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d953d003d5f9c34df4dcb0261ae9984f0308676ef6597e081683068678ae8e33`  
		Last Modified: Fri, 28 Jun 2024 22:00:22 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2` - unknown; unknown

```console
$ docker pull geonetwork@sha256:f2a6dc9980fa8c2fba6ac7518f4e7fb868b14b93f4610dd285db6e66ff9c6cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4354722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f870cd1dd1c45dcd4d1f0895fbfffd751ea50c212bc01525ae38ed048e962d`

```dockerfile
```

-	Layers:
	-	`sha256:4356ff8fc83d0967afd42145ee5600fb5b06b0b8dc2f2bce3f0292c887cf5753`  
		Last Modified: Fri, 28 Jun 2024 22:00:22 GMT  
		Size: 4.3 MB (4336045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63821a15ddcfa884a287ef7ecfb0fb2c246cf8b21d9a48fd39612680bc70735e`  
		Last Modified: Fri, 28 Jun 2024 22:00:22 GMT  
		Size: 18.7 KB (18677 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.2` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:5b06f2a3130d75064a9f8ac286a5172255cf322c6c72e5c8041ec1fb04e60a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.9 MB (458884589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d108e755f14ca354daca3d8fba108718c8225d06a42d608eff3bebde4408a5`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 15 Mar 2024 05:21:34 GMT
ARG RELEASE
# Fri, 15 Mar 2024 05:21:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 15 Mar 2024 05:21:34 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["/bin/bash"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_VERSION=9.4.54.v20240208
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.54.v20240208/jetty-home-9.4.54.v20240208.tar.gz
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
WORKDIR /var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
USER jetty
# Fri, 15 Mar 2024 05:21:34 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
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
	-	`sha256:727c12dbb48ee04e23f6425d3a3f8d3fe01949556a9e51d7c1739eac756214f9`  
		Last Modified: Fri, 28 Jun 2024 20:59:36 GMT  
		Size: 10.0 MB (10015279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daab1eb338ee30cf71f43cbccc9dbfcad4c6b0da1082f6e48bb51d3eb5b894ed`  
		Last Modified: Fri, 28 Jun 2024 20:59:36 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a461bbdf8c842cd3c6c71737f08392e0eee6697710976f2202ae277d496d21a`  
		Last Modified: Fri, 28 Jun 2024 22:08:13 GMT  
		Size: 243.9 KB (243886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f18edb1490baee03363fd0b5aa42b1f93679b46afb3f2ed1569efb68158ba27`  
		Last Modified: Fri, 28 Jun 2024 22:08:19 GMT  
		Size: 301.9 MB (301934705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5526709cea3b95919461f2796364b8cb113bf8201b5cf2b95e87b0a62c665c0d`  
		Last Modified: Fri, 28 Jun 2024 22:08:13 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2` - unknown; unknown

```console
$ docker pull geonetwork@sha256:6816bc14916513b4d7731371ced18bd7efaf1e089ca151280bd9bda65e44ef78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4355489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3a3a6c8a173771a700460b10febd2df0588fb96aef18a123218f1f39493436`

```dockerfile
```

-	Layers:
	-	`sha256:2de40796f24c3fe93d7cd3119bd13ddc567317ee4b000b29902bdd6c3952ddc9`  
		Last Modified: Fri, 28 Jun 2024 22:08:13 GMT  
		Size: 4.3 MB (4336330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df65a817fef535e7aa376093af6a200cde8825397920c678cd1db5f8aedb4a32`  
		Last Modified: Fri, 28 Jun 2024 22:08:12 GMT  
		Size: 19.2 KB (19159 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.2.10`

```console
$ docker pull geonetwork@sha256:201c334df76ef105db8482c1b593d7e985918d4814755cfd2697ab6906c52177
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:4.2.10` - linux; amd64

```console
$ docker pull geonetwork@sha256:721554644a8112aa7047e9db3550dd85186643be5aec15b2ffae0a8bc5845233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.3 MB (461306351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb683a4f85a446b4a5fabd4c7ef225a8aa76826f0224151ed1b564a904af6f4`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 15 Mar 2024 05:21:34 GMT
ARG RELEASE
# Fri, 15 Mar 2024 05:21:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 15 Mar 2024 05:21:34 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["/bin/bash"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_VERSION=9.4.54.v20240208
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.54.v20240208/jetty-home-9.4.54.v20240208.tar.gz
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
WORKDIR /var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
USER jetty
# Fri, 15 Mar 2024 05:21:34 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
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
	-	`sha256:86c361d921973a199295dea7b1a08340c6444ee42f6b23b2e924aa5100420f67`  
		Last Modified: Wed, 05 Jun 2024 04:57:54 GMT  
		Size: 103.6 MB (103602581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409c91c0433db39de61b0193a2498b60890893ce6b3cb2b9e1c751bfdc919224`  
		Last Modified: Wed, 05 Jun 2024 04:57:46 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd20a24d30f10019507281b17336eb76b4dd341fcbca56686e570a18717dda`  
		Last Modified: Wed, 05 Jun 2024 04:57:46 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a76b3a06a48a558f2a3cb2d6084a3b9c00a6c7f2a9adb6252e6466c5ef50f3`  
		Last Modified: Fri, 28 Jun 2024 20:56:36 GMT  
		Size: 10.0 MB (10015384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce440ea07f96bf41cb530f892e7b8764bb827cf0d5d869aa99db55b6a06fc7d3`  
		Last Modified: Fri, 28 Jun 2024 20:56:30 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97789c2b105cc8bab3aea822d4a04aa4e345ec1d7aa45423e67fae054e1afd9`  
		Last Modified: Fri, 28 Jun 2024 22:00:22 GMT  
		Size: 245.2 KB (245240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15e5235ceacc2c1ae37666fe0f4d51098f2a70a297558b60b41db14aacb675d`  
		Last Modified: Fri, 28 Jun 2024 22:00:26 GMT  
		Size: 301.9 MB (301934653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d953d003d5f9c34df4dcb0261ae9984f0308676ef6597e081683068678ae8e33`  
		Last Modified: Fri, 28 Jun 2024 22:00:22 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2.10` - unknown; unknown

```console
$ docker pull geonetwork@sha256:f2a6dc9980fa8c2fba6ac7518f4e7fb868b14b93f4610dd285db6e66ff9c6cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4354722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f870cd1dd1c45dcd4d1f0895fbfffd751ea50c212bc01525ae38ed048e962d`

```dockerfile
```

-	Layers:
	-	`sha256:4356ff8fc83d0967afd42145ee5600fb5b06b0b8dc2f2bce3f0292c887cf5753`  
		Last Modified: Fri, 28 Jun 2024 22:00:22 GMT  
		Size: 4.3 MB (4336045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63821a15ddcfa884a287ef7ecfb0fb2c246cf8b21d9a48fd39612680bc70735e`  
		Last Modified: Fri, 28 Jun 2024 22:00:22 GMT  
		Size: 18.7 KB (18677 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.2.10` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:5b06f2a3130d75064a9f8ac286a5172255cf322c6c72e5c8041ec1fb04e60a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.9 MB (458884589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d108e755f14ca354daca3d8fba108718c8225d06a42d608eff3bebde4408a5`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 15 Mar 2024 05:21:34 GMT
ARG RELEASE
# Fri, 15 Mar 2024 05:21:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 15 Mar 2024 05:21:34 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["/bin/bash"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_VERSION=9.4.54.v20240208
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.54.v20240208/jetty-home-9.4.54.v20240208.tar.gz
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
WORKDIR /var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
USER jetty
# Fri, 15 Mar 2024 05:21:34 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
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
	-	`sha256:727c12dbb48ee04e23f6425d3a3f8d3fe01949556a9e51d7c1739eac756214f9`  
		Last Modified: Fri, 28 Jun 2024 20:59:36 GMT  
		Size: 10.0 MB (10015279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daab1eb338ee30cf71f43cbccc9dbfcad4c6b0da1082f6e48bb51d3eb5b894ed`  
		Last Modified: Fri, 28 Jun 2024 20:59:36 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a461bbdf8c842cd3c6c71737f08392e0eee6697710976f2202ae277d496d21a`  
		Last Modified: Fri, 28 Jun 2024 22:08:13 GMT  
		Size: 243.9 KB (243886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f18edb1490baee03363fd0b5aa42b1f93679b46afb3f2ed1569efb68158ba27`  
		Last Modified: Fri, 28 Jun 2024 22:08:19 GMT  
		Size: 301.9 MB (301934705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5526709cea3b95919461f2796364b8cb113bf8201b5cf2b95e87b0a62c665c0d`  
		Last Modified: Fri, 28 Jun 2024 22:08:13 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2.10` - unknown; unknown

```console
$ docker pull geonetwork@sha256:6816bc14916513b4d7731371ced18bd7efaf1e089ca151280bd9bda65e44ef78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4355489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3a3a6c8a173771a700460b10febd2df0588fb96aef18a123218f1f39493436`

```dockerfile
```

-	Layers:
	-	`sha256:2de40796f24c3fe93d7cd3119bd13ddc567317ee4b000b29902bdd6c3952ddc9`  
		Last Modified: Fri, 28 Jun 2024 22:08:13 GMT  
		Size: 4.3 MB (4336330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df65a817fef535e7aa376093af6a200cde8825397920c678cd1db5f8aedb4a32`  
		Last Modified: Fri, 28 Jun 2024 22:08:12 GMT  
		Size: 19.2 KB (19159 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.4`

```console
$ docker pull geonetwork@sha256:94e49e0549680c5e655b3f7061fe488df1e48f69eb01511dbf2edcb05ba30310
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:4.4` - linux; amd64

```console
$ docker pull geonetwork@sha256:8ee2fc97ea1738ca35996d698dd773f1d8b63b8d4f50bc776abd10ed5e8cc1cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.0 MB (488041018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830528afbee6f9473e10fc06979d082a8889e6cbdc2acf0f0f7970192be89c85`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 15 Mar 2024 05:21:34 GMT
ARG RELEASE
# Fri, 15 Mar 2024 05:21:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 15 Mar 2024 05:21:34 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["/bin/bash"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["jshell"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_VERSION=9.4.54.v20240208
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.54.v20240208/jetty-home-9.4.54.v20240208.tar.gz
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
WORKDIR /var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
USER jetty
# Fri, 15 Mar 2024 05:21:34 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
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
	-	`sha256:24aeef90818f4bccf7d9bd6e0be8387a60d437936ced45ff5e61d80ef9778e94`  
		Last Modified: Wed, 05 Jun 2024 04:59:06 GMT  
		Size: 145.5 MB (145507603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0aa573dbf90a7e06817e01a23139b1f8b8093a2bb43b4050b665696d2aaaeb`  
		Last Modified: Wed, 05 Jun 2024 04:58:55 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780a38247a5709082a621a5e1fbb5742e9b82f20b9235f8c349dbbcdd41e108a`  
		Last Modified: Wed, 05 Jun 2024 04:58:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ed127625f83ec444fec38b0b727026c8f21c761495116c75dc3037a30598fc`  
		Last Modified: Fri, 28 Jun 2024 20:56:37 GMT  
		Size: 10.0 MB (10016385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864f11609f3fd19154163fd5bd3233c507fcc543fa8e8a01a4e36331955ff7aa`  
		Last Modified: Fri, 28 Jun 2024 20:56:36 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3b2a2e233dc5f88c7a255301fbd815476fe133ed69da26a69a7a8031167449`  
		Last Modified: Fri, 28 Jun 2024 22:01:08 GMT  
		Size: 245.2 KB (245173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4901c4849048870e3c5e2b06beee5f54522e229933dd44f58b35d383fe7065`  
		Last Modified: Fri, 28 Jun 2024 22:01:11 GMT  
		Size: 286.8 MB (286763023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2421c5e6fa1d811aab6fe1d73d54be1fd8cc555e25c86765721cc6998f7bc`  
		Last Modified: Fri, 28 Jun 2024 22:01:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e508dd540564f697742a8ddc66e5a383d080f9a3eddbe01ea1427210ce333fa`  
		Last Modified: Fri, 28 Jun 2024 22:01:08 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2c246230b5bd8f2c38db8576be72e0ca61eb28a79118cc158e9ba2997c474c`  
		Last Modified: Fri, 28 Jun 2024 22:01:09 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:10b5fc0fd8f8fe834e6e0fe91990973ca9038718119e23b617180133addff4f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4199714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bda5189c535fb9b2b074151d23179f2ba5429b3cd5dcf9f178e98e68fb20cd`

```dockerfile
```

-	Layers:
	-	`sha256:4a135e6108fd831a0b7355372f9b0e015396567a8412d0cda645107fc4ae090f`  
		Last Modified: Fri, 28 Jun 2024 22:01:08 GMT  
		Size: 4.2 MB (4174054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9181634f66b16ff77b191e2b4e53460fd6ce0458f449b9dd9a2823e07bf13216`  
		Last Modified: Fri, 28 Jun 2024 22:01:08 GMT  
		Size: 25.7 KB (25660 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:9e3c2e9122a9786c20dd09abc02a4b86980c480f5e34f0c63305c02456146e4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.3 MB (483321454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ecbc49bf790f8fb29cb1ad028db0d82a70c6665497c239776e113e152850ff`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 15 Mar 2024 05:21:34 GMT
ARG RELEASE
# Fri, 15 Mar 2024 05:21:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 15 Mar 2024 05:21:34 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["/bin/bash"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["jshell"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_VERSION=9.4.54.v20240208
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.54.v20240208/jetty-home-9.4.54.v20240208.tar.gz
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
WORKDIR /var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
USER jetty
# Fri, 15 Mar 2024 05:21:34 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
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
	-	`sha256:3294c18dc189f71e82fdd6779b6b0d69ba8defe38e3e26bb53031dfcf05f4add`  
		Last Modified: Wed, 05 Jun 2024 04:55:50 GMT  
		Size: 142.3 MB (142312188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3740768ca48a1b10a3ee451ba3bd551f320fa113d2505c2b877a1d3fd02a2f97`  
		Last Modified: Wed, 05 Jun 2024 04:55:41 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39f12d5bcae89c5e56ddf77b9c89b3bea51ce03ca339db4e9e846e4711e94ad`  
		Last Modified: Wed, 05 Jun 2024 04:55:41 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c24ea46ddb6e25d218f52432ef4bfc56436b2babf033f99ef25e09d514b662`  
		Last Modified: Fri, 28 Jun 2024 21:01:52 GMT  
		Size: 10.0 MB (10016315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f24f1da7328caf2e84f1313a1ddfa52d338df679e7459246c921303a39a939`  
		Last Modified: Fri, 28 Jun 2024 21:01:51 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d162f9b3ffd7ab9c27dca70cf2e7624e8aadb5b2cbb29cdaacedd9308e791d`  
		Last Modified: Fri, 28 Jun 2024 22:10:10 GMT  
		Size: 243.8 KB (243827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2452c019648c3f067c67337cf924382882920b138a122825b1cd77a4caa102d4`  
		Last Modified: Fri, 28 Jun 2024 22:10:17 GMT  
		Size: 286.8 MB (286763067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aa2e558d78f27f9c394da51eda167974da7cd0f6ce9dff772b8efe50e1e04e`  
		Last Modified: Fri, 28 Jun 2024 22:10:10 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb829a274aa00e7ceb10c717641a7b69bd72250e0d3469fc1047abdfd170065b`  
		Last Modified: Fri, 28 Jun 2024 22:10:10 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68af11bac0950ec0ed18caee0591cb8029ee55e6b337ea1af18183f352e6eee`  
		Last Modified: Fri, 28 Jun 2024 22:10:11 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:82aa627aa4950fbda7e6eea441f31c7f4c0fd8d8be7a68a48f853819702c4c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4200588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df680b3be880914c8429a3b07f8aaa81a5ca29a915cd83a65c01cf0421932dd`

```dockerfile
```

-	Layers:
	-	`sha256:3569d8bd16483a69609db6bd1c5286ea873d6d92dc7a5bb26d9d0253950dd8ba`  
		Last Modified: Fri, 28 Jun 2024 22:10:10 GMT  
		Size: 4.2 MB (4174363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcaeb0b68138f8a76091e5f43cd3dba7c2f49c0422cacde797e632b3756b6449`  
		Last Modified: Fri, 28 Jun 2024 22:10:10 GMT  
		Size: 26.2 KB (26225 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.4.5`

```console
$ docker pull geonetwork@sha256:94e49e0549680c5e655b3f7061fe488df1e48f69eb01511dbf2edcb05ba30310
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:4.4.5` - linux; amd64

```console
$ docker pull geonetwork@sha256:8ee2fc97ea1738ca35996d698dd773f1d8b63b8d4f50bc776abd10ed5e8cc1cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.0 MB (488041018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830528afbee6f9473e10fc06979d082a8889e6cbdc2acf0f0f7970192be89c85`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 15 Mar 2024 05:21:34 GMT
ARG RELEASE
# Fri, 15 Mar 2024 05:21:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 15 Mar 2024 05:21:34 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["/bin/bash"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["jshell"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_VERSION=9.4.54.v20240208
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.54.v20240208/jetty-home-9.4.54.v20240208.tar.gz
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
WORKDIR /var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
USER jetty
# Fri, 15 Mar 2024 05:21:34 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
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
	-	`sha256:24aeef90818f4bccf7d9bd6e0be8387a60d437936ced45ff5e61d80ef9778e94`  
		Last Modified: Wed, 05 Jun 2024 04:59:06 GMT  
		Size: 145.5 MB (145507603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0aa573dbf90a7e06817e01a23139b1f8b8093a2bb43b4050b665696d2aaaeb`  
		Last Modified: Wed, 05 Jun 2024 04:58:55 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780a38247a5709082a621a5e1fbb5742e9b82f20b9235f8c349dbbcdd41e108a`  
		Last Modified: Wed, 05 Jun 2024 04:58:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ed127625f83ec444fec38b0b727026c8f21c761495116c75dc3037a30598fc`  
		Last Modified: Fri, 28 Jun 2024 20:56:37 GMT  
		Size: 10.0 MB (10016385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864f11609f3fd19154163fd5bd3233c507fcc543fa8e8a01a4e36331955ff7aa`  
		Last Modified: Fri, 28 Jun 2024 20:56:36 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3b2a2e233dc5f88c7a255301fbd815476fe133ed69da26a69a7a8031167449`  
		Last Modified: Fri, 28 Jun 2024 22:01:08 GMT  
		Size: 245.2 KB (245173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4901c4849048870e3c5e2b06beee5f54522e229933dd44f58b35d383fe7065`  
		Last Modified: Fri, 28 Jun 2024 22:01:11 GMT  
		Size: 286.8 MB (286763023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2421c5e6fa1d811aab6fe1d73d54be1fd8cc555e25c86765721cc6998f7bc`  
		Last Modified: Fri, 28 Jun 2024 22:01:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e508dd540564f697742a8ddc66e5a383d080f9a3eddbe01ea1427210ce333fa`  
		Last Modified: Fri, 28 Jun 2024 22:01:08 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2c246230b5bd8f2c38db8576be72e0ca61eb28a79118cc158e9ba2997c474c`  
		Last Modified: Fri, 28 Jun 2024 22:01:09 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4.5` - unknown; unknown

```console
$ docker pull geonetwork@sha256:10b5fc0fd8f8fe834e6e0fe91990973ca9038718119e23b617180133addff4f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4199714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bda5189c535fb9b2b074151d23179f2ba5429b3cd5dcf9f178e98e68fb20cd`

```dockerfile
```

-	Layers:
	-	`sha256:4a135e6108fd831a0b7355372f9b0e015396567a8412d0cda645107fc4ae090f`  
		Last Modified: Fri, 28 Jun 2024 22:01:08 GMT  
		Size: 4.2 MB (4174054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9181634f66b16ff77b191e2b4e53460fd6ce0458f449b9dd9a2823e07bf13216`  
		Last Modified: Fri, 28 Jun 2024 22:01:08 GMT  
		Size: 25.7 KB (25660 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4.5` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:9e3c2e9122a9786c20dd09abc02a4b86980c480f5e34f0c63305c02456146e4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.3 MB (483321454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ecbc49bf790f8fb29cb1ad028db0d82a70c6665497c239776e113e152850ff`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 15 Mar 2024 05:21:34 GMT
ARG RELEASE
# Fri, 15 Mar 2024 05:21:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 15 Mar 2024 05:21:34 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["/bin/bash"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["jshell"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_VERSION=9.4.54.v20240208
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.54.v20240208/jetty-home-9.4.54.v20240208.tar.gz
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
WORKDIR /var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
USER jetty
# Fri, 15 Mar 2024 05:21:34 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
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
	-	`sha256:3294c18dc189f71e82fdd6779b6b0d69ba8defe38e3e26bb53031dfcf05f4add`  
		Last Modified: Wed, 05 Jun 2024 04:55:50 GMT  
		Size: 142.3 MB (142312188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3740768ca48a1b10a3ee451ba3bd551f320fa113d2505c2b877a1d3fd02a2f97`  
		Last Modified: Wed, 05 Jun 2024 04:55:41 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39f12d5bcae89c5e56ddf77b9c89b3bea51ce03ca339db4e9e846e4711e94ad`  
		Last Modified: Wed, 05 Jun 2024 04:55:41 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c24ea46ddb6e25d218f52432ef4bfc56436b2babf033f99ef25e09d514b662`  
		Last Modified: Fri, 28 Jun 2024 21:01:52 GMT  
		Size: 10.0 MB (10016315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f24f1da7328caf2e84f1313a1ddfa52d338df679e7459246c921303a39a939`  
		Last Modified: Fri, 28 Jun 2024 21:01:51 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d162f9b3ffd7ab9c27dca70cf2e7624e8aadb5b2cbb29cdaacedd9308e791d`  
		Last Modified: Fri, 28 Jun 2024 22:10:10 GMT  
		Size: 243.8 KB (243827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2452c019648c3f067c67337cf924382882920b138a122825b1cd77a4caa102d4`  
		Last Modified: Fri, 28 Jun 2024 22:10:17 GMT  
		Size: 286.8 MB (286763067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aa2e558d78f27f9c394da51eda167974da7cd0f6ce9dff772b8efe50e1e04e`  
		Last Modified: Fri, 28 Jun 2024 22:10:10 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb829a274aa00e7ceb10c717641a7b69bd72250e0d3469fc1047abdfd170065b`  
		Last Modified: Fri, 28 Jun 2024 22:10:10 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68af11bac0950ec0ed18caee0591cb8029ee55e6b337ea1af18183f352e6eee`  
		Last Modified: Fri, 28 Jun 2024 22:10:11 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4.5` - unknown; unknown

```console
$ docker pull geonetwork@sha256:82aa627aa4950fbda7e6eea441f31c7f4c0fd8d8be7a68a48f853819702c4c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4200588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df680b3be880914c8429a3b07f8aaa81a5ca29a915cd83a65c01cf0421932dd`

```dockerfile
```

-	Layers:
	-	`sha256:3569d8bd16483a69609db6bd1c5286ea873d6d92dc7a5bb26d9d0253950dd8ba`  
		Last Modified: Fri, 28 Jun 2024 22:10:10 GMT  
		Size: 4.2 MB (4174363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcaeb0b68138f8a76091e5f43cd3dba7c2f49c0422cacde797e632b3756b6449`  
		Last Modified: Fri, 28 Jun 2024 22:10:10 GMT  
		Size: 26.2 KB (26225 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:latest`

```console
$ docker pull geonetwork@sha256:94e49e0549680c5e655b3f7061fe488df1e48f69eb01511dbf2edcb05ba30310
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:latest` - linux; amd64

```console
$ docker pull geonetwork@sha256:8ee2fc97ea1738ca35996d698dd773f1d8b63b8d4f50bc776abd10ed5e8cc1cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.0 MB (488041018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830528afbee6f9473e10fc06979d082a8889e6cbdc2acf0f0f7970192be89c85`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 15 Mar 2024 05:21:34 GMT
ARG RELEASE
# Fri, 15 Mar 2024 05:21:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 15 Mar 2024 05:21:34 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["/bin/bash"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["jshell"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_VERSION=9.4.54.v20240208
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.54.v20240208/jetty-home-9.4.54.v20240208.tar.gz
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
WORKDIR /var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
USER jetty
# Fri, 15 Mar 2024 05:21:34 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
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
	-	`sha256:24aeef90818f4bccf7d9bd6e0be8387a60d437936ced45ff5e61d80ef9778e94`  
		Last Modified: Wed, 05 Jun 2024 04:59:06 GMT  
		Size: 145.5 MB (145507603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0aa573dbf90a7e06817e01a23139b1f8b8093a2bb43b4050b665696d2aaaeb`  
		Last Modified: Wed, 05 Jun 2024 04:58:55 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780a38247a5709082a621a5e1fbb5742e9b82f20b9235f8c349dbbcdd41e108a`  
		Last Modified: Wed, 05 Jun 2024 04:58:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ed127625f83ec444fec38b0b727026c8f21c761495116c75dc3037a30598fc`  
		Last Modified: Fri, 28 Jun 2024 20:56:37 GMT  
		Size: 10.0 MB (10016385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864f11609f3fd19154163fd5bd3233c507fcc543fa8e8a01a4e36331955ff7aa`  
		Last Modified: Fri, 28 Jun 2024 20:56:36 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3b2a2e233dc5f88c7a255301fbd815476fe133ed69da26a69a7a8031167449`  
		Last Modified: Fri, 28 Jun 2024 22:01:08 GMT  
		Size: 245.2 KB (245173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4901c4849048870e3c5e2b06beee5f54522e229933dd44f58b35d383fe7065`  
		Last Modified: Fri, 28 Jun 2024 22:01:11 GMT  
		Size: 286.8 MB (286763023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b2421c5e6fa1d811aab6fe1d73d54be1fd8cc555e25c86765721cc6998f7bc`  
		Last Modified: Fri, 28 Jun 2024 22:01:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e508dd540564f697742a8ddc66e5a383d080f9a3eddbe01ea1427210ce333fa`  
		Last Modified: Fri, 28 Jun 2024 22:01:08 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2c246230b5bd8f2c38db8576be72e0ca61eb28a79118cc158e9ba2997c474c`  
		Last Modified: Fri, 28 Jun 2024 22:01:09 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:latest` - unknown; unknown

```console
$ docker pull geonetwork@sha256:10b5fc0fd8f8fe834e6e0fe91990973ca9038718119e23b617180133addff4f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4199714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bda5189c535fb9b2b074151d23179f2ba5429b3cd5dcf9f178e98e68fb20cd`

```dockerfile
```

-	Layers:
	-	`sha256:4a135e6108fd831a0b7355372f9b0e015396567a8412d0cda645107fc4ae090f`  
		Last Modified: Fri, 28 Jun 2024 22:01:08 GMT  
		Size: 4.2 MB (4174054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9181634f66b16ff77b191e2b4e53460fd6ce0458f449b9dd9a2823e07bf13216`  
		Last Modified: Fri, 28 Jun 2024 22:01:08 GMT  
		Size: 25.7 KB (25660 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:latest` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:9e3c2e9122a9786c20dd09abc02a4b86980c480f5e34f0c63305c02456146e4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.3 MB (483321454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ecbc49bf790f8fb29cb1ad028db0d82a70c6665497c239776e113e152850ff`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 15 Mar 2024 05:21:34 GMT
ARG RELEASE
# Fri, 15 Mar 2024 05:21:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 15 Mar 2024 05:21:34 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 15 Mar 2024 05:21:34 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["/bin/bash"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
CMD ["jshell"]
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_VERSION=9.4.54.v20240208
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.54.v20240208/jetty-home-9.4.54.v20240208.tar.gz
# Fri, 15 Mar 2024 05:21:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Fri, 15 Mar 2024 05:21:34 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
WORKDIR /var/lib/jetty
# Fri, 15 Mar 2024 05:21:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Fri, 15 Mar 2024 05:21:34 GMT
USER jetty
# Fri, 15 Mar 2024 05:21:34 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 15 Mar 2024 05:21:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Mar 2024 05:21:34 GMT
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
	-	`sha256:3294c18dc189f71e82fdd6779b6b0d69ba8defe38e3e26bb53031dfcf05f4add`  
		Last Modified: Wed, 05 Jun 2024 04:55:50 GMT  
		Size: 142.3 MB (142312188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3740768ca48a1b10a3ee451ba3bd551f320fa113d2505c2b877a1d3fd02a2f97`  
		Last Modified: Wed, 05 Jun 2024 04:55:41 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39f12d5bcae89c5e56ddf77b9c89b3bea51ce03ca339db4e9e846e4711e94ad`  
		Last Modified: Wed, 05 Jun 2024 04:55:41 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c24ea46ddb6e25d218f52432ef4bfc56436b2babf033f99ef25e09d514b662`  
		Last Modified: Fri, 28 Jun 2024 21:01:52 GMT  
		Size: 10.0 MB (10016315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f24f1da7328caf2e84f1313a1ddfa52d338df679e7459246c921303a39a939`  
		Last Modified: Fri, 28 Jun 2024 21:01:51 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d162f9b3ffd7ab9c27dca70cf2e7624e8aadb5b2cbb29cdaacedd9308e791d`  
		Last Modified: Fri, 28 Jun 2024 22:10:10 GMT  
		Size: 243.8 KB (243827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2452c019648c3f067c67337cf924382882920b138a122825b1cd77a4caa102d4`  
		Last Modified: Fri, 28 Jun 2024 22:10:17 GMT  
		Size: 286.8 MB (286763067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aa2e558d78f27f9c394da51eda167974da7cd0f6ce9dff772b8efe50e1e04e`  
		Last Modified: Fri, 28 Jun 2024 22:10:10 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb829a274aa00e7ceb10c717641a7b69bd72250e0d3469fc1047abdfd170065b`  
		Last Modified: Fri, 28 Jun 2024 22:10:10 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68af11bac0950ec0ed18caee0591cb8029ee55e6b337ea1af18183f352e6eee`  
		Last Modified: Fri, 28 Jun 2024 22:10:11 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:latest` - unknown; unknown

```console
$ docker pull geonetwork@sha256:82aa627aa4950fbda7e6eea441f31c7f4c0fd8d8be7a68a48f853819702c4c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4200588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df680b3be880914c8429a3b07f8aaa81a5ca29a915cd83a65c01cf0421932dd`

```dockerfile
```

-	Layers:
	-	`sha256:3569d8bd16483a69609db6bd1c5286ea873d6d92dc7a5bb26d9d0253950dd8ba`  
		Last Modified: Fri, 28 Jun 2024 22:10:10 GMT  
		Size: 4.2 MB (4174363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcaeb0b68138f8a76091e5f43cd3dba7c2f49c0422cacde797e632b3756b6449`  
		Last Modified: Fri, 28 Jun 2024 22:10:10 GMT  
		Size: 26.2 KB (26225 bytes)  
		MIME: application/vnd.in-toto+json
