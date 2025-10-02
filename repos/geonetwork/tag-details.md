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
-	[`geonetwork:4.2.13`](#geonetwork4213)
-	[`geonetwork:4.4`](#geonetwork44)
-	[`geonetwork:4.4.8`](#geonetwork448)
-	[`geonetwork:latest`](#geonetworklatest)

## `geonetwork:3`

```console
$ docker pull geonetwork@sha256:6ff23bcc16fb342622dd1f2821e8c9da4f2586218eb9529cf000453538af6c53
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
$ docker pull geonetwork@sha256:bba90e970016f277e51eb28013672b6bedeb1c86968ec8adc6208759bb7da5f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.9 MB (349942124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea41ee04c6e9c612209cac646b7095b78d6e1c386f1c8920c5fbd3f7a94ea52`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 08 Aug 2024 11:50:27 GMT
ARG RELEASE
# Thu, 08 Aug 2024 11:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 Aug 2024 11:50:27 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_MAJOR=9
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT []
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_FILE=geonetwork.war
# Thu, 08 Aug 2024 11:50:27 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_VERSION=3.12.12
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb43857d5308a40718704288d12cb0f13a2c0c288decd5254238b35963ff9d7`  
		Last Modified: Mon, 15 Sep 2025 22:12:45 GMT  
		Size: 17.0 MB (16971774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75cee9f1f2e7610dad4413b9e913bd37b54330c43a35bd3c85ad28bad82617e`  
		Last Modified: Mon, 15 Sep 2025 22:12:50 GMT  
		Size: 54.7 MB (54739675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f3133ac8c49679b26388b308a6a3d27b36b06ec1443730b47518fd4134e813`  
		Last Modified: Mon, 15 Sep 2025 22:12:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b9ab2fa29f411732853d26d15ae764cec2feb5409374d10d1f97a71cbdca0a`  
		Last Modified: Mon, 15 Sep 2025 22:12:42 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63659d25f5259532448b0e29feb98f5066b8c91afd81f9a305b8872f34de7b9f`  
		Last Modified: Mon, 15 Sep 2025 23:23:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785c4ea8b033f125e3207bafec2320bedc6febf7b3aaab0a6cdd03ff510056f4`  
		Last Modified: Mon, 15 Sep 2025 23:23:49 GMT  
		Size: 14.0 MB (13954095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173897eb680420e3ea53b3e2e818df472917c72343c77e24f09d07144481ce98`  
		Last Modified: Tue, 16 Sep 2025 01:12:18 GMT  
		Size: 234.6 MB (234550180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8b55d57ba34b04ef3fe52c648ff02b834fff92bd0f68a461c9d72842e5aeed`  
		Last Modified: Tue, 16 Sep 2025 00:54:35 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:584eaee7049d5f2a3aba286df73aa6318a1c036d7331d8cbee172a1513790bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788ecd9aec4cea58c4770f0954bf5c484c1c216d11e193bf8d4b14b0f9054e4d`

```dockerfile
```

-	Layers:
	-	`sha256:33e8833dc193fddeabec9158e20d8f98e1573c6ba4a7f0514a3cee467da64b02`  
		Last Modified: Tue, 16 Sep 2025 03:12:30 GMT  
		Size: 4.4 MB (4359721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da4cb59af9c56ef5941a73471ff2bf4ae0b7ff7457c8fbd0baa2c6919ba2dcf8`  
		Last Modified: Tue, 16 Sep 2025 03:12:31 GMT  
		Size: 19.1 KB (19136 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:bdfba7c4627a02d766547c7f42ba240734761d8b4475bd763f463e7532b994a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.5 MB (343465760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc8d8c577cce7d5a3a699d749de5e373f0b3876e46ed7c4401682b619c1e30d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 08 Aug 2024 11:50:27 GMT
ARG RELEASE
# Thu, 08 Aug 2024 11:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 Aug 2024 11:50:27 GMT
ADD file:51076814e2aa1389d29f1b4c38eee0cfbb1d321f099c50e09b19452198f65032 in / 
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_MAJOR=9
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT []
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_FILE=geonetwork.war
# Thu, 08 Aug 2024 11:50:27 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_VERSION=3.12.12
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6c9f3e8be363989d138b8e3a1316487da5ee2b8384d3c6b0f9b1a8290f57caff`  
		Last Modified: Tue, 30 Sep 2025 17:07:34 GMT  
		Size: 26.9 MB (26851149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8256622f04cb21ac626f3652bc38fd100329ea6c631e2be7bc387bc03dd3db4e`  
		Last Modified: Thu, 02 Oct 2025 01:12:06 GMT  
		Size: 18.1 MB (18087038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7571f83f8225c088a30f1f928e7faab2958c61d4e0f21e841d05453d3fdef785`  
		Last Modified: Thu, 02 Oct 2025 01:12:11 GMT  
		Size: 50.1 MB (50123714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d8f3d99eebd3bbf209e4dff2ace919de2f05151555b21f48f120b0aed538a3`  
		Last Modified: Thu, 02 Oct 2025 01:12:05 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae14e8c0418c50502562376b3258f0dce4388713a374bd97c8285836d8a7408`  
		Last Modified: Thu, 02 Oct 2025 01:12:05 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417643604d378baecc97ba6be5d5b074629d671ce957256989003fd293f1a522`  
		Last Modified: Thu, 02 Oct 2025 02:19:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70dc23121b75674d8c12cab58dcc746932e1b217fc881c2588730b37e2d4531`  
		Last Modified: Thu, 02 Oct 2025 02:19:04 GMT  
		Size: 13.9 MB (13862417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6112f8f480482b90a5605caf697f8efb2eb9017f8ce6219858eaff1f5415fb`  
		Last Modified: Thu, 02 Oct 2025 04:12:12 GMT  
		Size: 234.5 MB (234538491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1301d8918150c620037ebf4085a5de9fd0ac1adcc64732bfc904faabf942ed`  
		Last Modified: Thu, 02 Oct 2025 03:17:09 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:fdfe246f036a27f050ba67c45ff87ae00742111727346f43ed264b12945aab06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4382906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395c3bfae6de8a9173cbe8c9a2c1604d8297bd3cccd68a2b230fe7256668c24a`

```dockerfile
```

-	Layers:
	-	`sha256:0a1e4639ebd72f9ec88a1c9d066daf4b3c76a29b754bf97c30549e6d10bfb3ca`  
		Last Modified: Thu, 02 Oct 2025 06:12:27 GMT  
		Size: 4.4 MB (4363698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7db65d5eb81993e79b4beedf12c4db39325d5be0f924b0ab0b9adee2cea4ca55`  
		Last Modified: Thu, 02 Oct 2025 06:12:27 GMT  
		Size: 19.2 KB (19208 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:5de1254105f301f8ef66c23fb62a670fde9962cbd3916a0102ba822f4d99b22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.4 MB (350431794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d69394b6229a68529c0f39f9e5de2d81d8164aae084ac40f442e2a471e4486`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 08 Aug 2024 11:50:27 GMT
ARG RELEASE
# Thu, 08 Aug 2024 11:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 Aug 2024 11:50:27 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_MAJOR=9
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT []
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_FILE=geonetwork.war
# Thu, 08 Aug 2024 11:50:27 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_VERSION=3.12.12
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419aaa52607f6ef7a03a295c57fe451241093bacec0b8cbd975e95351624d644`  
		Last Modified: Thu, 02 Oct 2025 01:17:02 GMT  
		Size: 19.2 MB (19206364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ec6c766cb339fe7639e7b17d5743545c0002c3dbb08b75eae759be43211807`  
		Last Modified: Thu, 02 Oct 2025 01:17:05 GMT  
		Size: 53.8 MB (53839370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfa9f945462c02f1fde3906d24c8d0bed5c81c07e533c43e49ea449b2244882`  
		Last Modified: Thu, 02 Oct 2025 01:17:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a22966219fd178174a348aca3c91573a3628dd260afb986e17e85a311bd26b`  
		Last Modified: Thu, 02 Oct 2025 01:17:01 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1831ecb6e291ee4ccc5493128b2b650933fcbb7e1359ebc1d0f72bbc79ae3da`  
		Last Modified: Thu, 02 Oct 2025 02:35:56 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93d3b51040369a32308c5b88da3ea8d19afb8487c4c69c909e0bedd5958470a`  
		Last Modified: Thu, 02 Oct 2025 02:35:58 GMT  
		Size: 14.0 MB (13967139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042d35bc28459ceceaafd7168528451db2074e5c6ca99d9d32d5556f5b1801fb`  
		Last Modified: Thu, 02 Oct 2025 04:15:03 GMT  
		Size: 234.6 MB (234554394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422f93d4ddf037144c5ff55646da96edb70fcbe480727ab5db0cf9f354f151b4`  
		Last Modified: Thu, 02 Oct 2025 03:24:59 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:caba546f35dc88dfe7d3b87bf35e6d5fc0d483043f43a50612dbb98dc1a84d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37acf6bade05d2782e21cc093e1fe59e152e73cdd6000e529520e2fef3e1ead8`

```dockerfile
```

-	Layers:
	-	`sha256:3bf1dbe931159ea352164a68ae1733beb002a733a93cd5ea7592b3b09b9ead6c`  
		Last Modified: Thu, 02 Oct 2025 06:12:32 GMT  
		Size: 4.4 MB (4360875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39cdf0068fcae66488a1d0b36d6fefba288b8f4a15147179c2ded3aad0c008a9`  
		Last Modified: Thu, 02 Oct 2025 06:12:33 GMT  
		Size: 19.2 KB (19228 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:2a04f31cdb00c576e9028076f8a6526a06f19fb75ab6518ae6e10b5e5e350f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.9 MB (353886776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c551566530972de12b906c58ab851e881a7137722c9b915f14d879483895d5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 08 Aug 2024 11:50:27 GMT
ARG RELEASE
# Thu, 08 Aug 2024 11:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 Aug 2024 11:50:27 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_MAJOR=9
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT []
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_FILE=geonetwork.war
# Thu, 08 Aug 2024 11:50:27 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_VERSION=3.12.12
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3102a54c6b2b7ecf7a7216123f26003eec1ece4dbee7d4985813592023f98cd3`  
		Last Modified: Mon, 15 Sep 2025 22:13:52 GMT  
		Size: 18.8 MB (18814803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fbd3108988f496e4134a4862d953a8c993115aeccbb0a4057f7261d82396f3`  
		Last Modified: Mon, 15 Sep 2025 22:13:58 GMT  
		Size: 52.2 MB (52167313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67ce08f3159aea036fc5ac087e7103091b6388431976c3e34a6e95daa24b83d`  
		Last Modified: Mon, 15 Sep 2025 22:13:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbefdb3dada19d520a48d2cd4aaf1451c5e151919b1df3ee0bf25d3b0fac385`  
		Last Modified: Mon, 15 Sep 2025 22:13:51 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af087b3e0dccc7cdae8cdd274abc54dec7b15e61c2a1475ecfc6c9297674b7f0`  
		Last Modified: Tue, 16 Sep 2025 00:28:42 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358d701de1f162895b6f87b8496b0d7ead71378b25d6584ee754e5f826187519`  
		Last Modified: Tue, 16 Sep 2025 00:28:44 GMT  
		Size: 14.0 MB (14023884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c36ea3b4c50fd203f3c2b0da5f1e30aa7afb5677c533820911d63bdacca68fb`  
		Last Modified: Tue, 16 Sep 2025 02:14:19 GMT  
		Size: 234.6 MB (234574700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a680493fd4eaaee1dae63e060d5078672b4e0ba9bf14ff5c94e13b6b5354a23c`  
		Last Modified: Tue, 16 Sep 2025 02:06:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:21341da91042e9145a0e194aa78ad75bf6e1d9d8309b5cfa594eaff1dee7c07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c14f29832050380d8398911ae7a11d5ec04b37f6bca09364b675ea95a6a2f1`

```dockerfile
```

-	Layers:
	-	`sha256:1382358527e701f1c00db7ac939c68c3812197c7298e1f21a0f236fb3f37a7fa`  
		Last Modified: Tue, 16 Sep 2025 03:12:47 GMT  
		Size: 4.4 MB (4362462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7549a28ab9f36050e10b7812e1844b16e944af68bb16106a201acb3f654fdb58`  
		Last Modified: Tue, 16 Sep 2025 03:12:48 GMT  
		Size: 19.2 KB (19174 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3-postgres`

```console
$ docker pull geonetwork@sha256:5bbed4c51b2c330c356310e70c9851038054b3ce810891da2645fa52ade2f14e
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
$ docker pull geonetwork@sha256:d28a249bf70dff7cf9e3f5fcd5cba3c7a6c7f4842a236b675d4f754584208317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.9 MB (363889462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1e525ba137bf1e68802272b7ba7a9a6fa5be66328ee04c5f2850c2984277e8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 08 Aug 2024 11:50:27 GMT
ARG RELEASE
# Thu, 08 Aug 2024 11:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 Aug 2024 11:50:27 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_MAJOR=9
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT []
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_FILE=geonetwork.war
# Thu, 08 Aug 2024 11:50:27 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_VERSION=3.12.12
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb43857d5308a40718704288d12cb0f13a2c0c288decd5254238b35963ff9d7`  
		Last Modified: Mon, 15 Sep 2025 22:12:45 GMT  
		Size: 17.0 MB (16971774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75cee9f1f2e7610dad4413b9e913bd37b54330c43a35bd3c85ad28bad82617e`  
		Last Modified: Mon, 15 Sep 2025 22:12:50 GMT  
		Size: 54.7 MB (54739675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f3133ac8c49679b26388b308a6a3d27b36b06ec1443730b47518fd4134e813`  
		Last Modified: Mon, 15 Sep 2025 22:12:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b9ab2fa29f411732853d26d15ae764cec2feb5409374d10d1f97a71cbdca0a`  
		Last Modified: Mon, 15 Sep 2025 22:12:42 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63659d25f5259532448b0e29feb98f5066b8c91afd81f9a305b8872f34de7b9f`  
		Last Modified: Mon, 15 Sep 2025 23:23:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785c4ea8b033f125e3207bafec2320bedc6febf7b3aaab0a6cdd03ff510056f4`  
		Last Modified: Mon, 15 Sep 2025 23:23:49 GMT  
		Size: 14.0 MB (13954095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173897eb680420e3ea53b3e2e818df472917c72343c77e24f09d07144481ce98`  
		Last Modified: Tue, 16 Sep 2025 01:12:18 GMT  
		Size: 234.6 MB (234550180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8b55d57ba34b04ef3fe52c648ff02b834fff92bd0f68a461c9d72842e5aeed`  
		Last Modified: Tue, 16 Sep 2025 00:54:35 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b53f35934b1dfe4b534788a1e3b140dfed57b5abe2fd67eae2afb3c4e81db1`  
		Last Modified: Tue, 16 Sep 2025 01:12:54 GMT  
		Size: 13.9 MB (13943929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6767f00a91a304e754e504a4ae2e4a62b073709370a852bb45d6ac8e453d6a7`  
		Last Modified: Tue, 16 Sep 2025 01:12:53 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4bc6e9905bac16a8297aa82645b83ad990e20a462e0d9096a157be7cb610a7`  
		Last Modified: Tue, 16 Sep 2025 01:12:53 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26ef08397cd361fc5a452abe0b2b9cd6c5ef181da92a64558e51d8f7d9f9615`  
		Last Modified: Tue, 16 Sep 2025 01:12:53 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:9327a4a9bf2eef1a209559fabe7b313015b1b8dc447046a5707130594c8b9df4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5937234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ec30f439c2f2ce6fd018c001112bd35fd5f3e7f70cddea77256df5cd8af047`

```dockerfile
```

-	Layers:
	-	`sha256:b46774ae17f7c5a50de86793a2eb8b4f9706377f6a5a06b9ebfc176dc679f56c`  
		Last Modified: Tue, 16 Sep 2025 03:12:46 GMT  
		Size: 5.9 MB (5914372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcc521891e26f29893ee09369461d1e64730cc522b9ab3eae35fbb78ea224615`  
		Last Modified: Tue, 16 Sep 2025 03:12:47 GMT  
		Size: 22.9 KB (22862 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:8b3d0b45f6ea9a87f2563134f6c3f8f59f76995f0f74d2945df992c739a3ab92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.5 MB (356473761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:999e51fdf19e26743b9b659e27478193020681b0dfc27023295c67e855275359`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 08 Aug 2024 11:50:27 GMT
ARG RELEASE
# Thu, 08 Aug 2024 11:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 Aug 2024 11:50:27 GMT
ADD file:51076814e2aa1389d29f1b4c38eee0cfbb1d321f099c50e09b19452198f65032 in / 
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_MAJOR=9
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT []
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_FILE=geonetwork.war
# Thu, 08 Aug 2024 11:50:27 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_VERSION=3.12.12
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6c9f3e8be363989d138b8e3a1316487da5ee2b8384d3c6b0f9b1a8290f57caff`  
		Last Modified: Tue, 30 Sep 2025 17:07:34 GMT  
		Size: 26.9 MB (26851149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8256622f04cb21ac626f3652bc38fd100329ea6c631e2be7bc387bc03dd3db4e`  
		Last Modified: Thu, 02 Oct 2025 01:12:06 GMT  
		Size: 18.1 MB (18087038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7571f83f8225c088a30f1f928e7faab2958c61d4e0f21e841d05453d3fdef785`  
		Last Modified: Thu, 02 Oct 2025 01:12:11 GMT  
		Size: 50.1 MB (50123714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d8f3d99eebd3bbf209e4dff2ace919de2f05151555b21f48f120b0aed538a3`  
		Last Modified: Thu, 02 Oct 2025 01:12:05 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae14e8c0418c50502562376b3258f0dce4388713a374bd97c8285836d8a7408`  
		Last Modified: Thu, 02 Oct 2025 01:12:05 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417643604d378baecc97ba6be5d5b074629d671ce957256989003fd293f1a522`  
		Last Modified: Thu, 02 Oct 2025 02:19:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70dc23121b75674d8c12cab58dcc746932e1b217fc881c2588730b37e2d4531`  
		Last Modified: Thu, 02 Oct 2025 02:19:04 GMT  
		Size: 13.9 MB (13862417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6112f8f480482b90a5605caf697f8efb2eb9017f8ce6219858eaff1f5415fb`  
		Last Modified: Thu, 02 Oct 2025 04:12:12 GMT  
		Size: 234.5 MB (234538491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1301d8918150c620037ebf4085a5de9fd0ac1adcc64732bfc904faabf942ed`  
		Last Modified: Thu, 02 Oct 2025 03:17:09 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8f3b4ad3cae3bb25587d2ba768b77f68b57ff3117fbf936a9fe70b6e3e41c8`  
		Last Modified: Thu, 02 Oct 2025 04:13:11 GMT  
		Size: 13.0 MB (13004591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73dc455ea18f17b9b01f68da4d5c80e5c86e18abf6d9fad5279c730cb5563e1`  
		Last Modified: Thu, 02 Oct 2025 04:13:09 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7af8d9bf38e6e2b183b9aa24927c70dea8a39c57030f63ee4472116397b5fad`  
		Last Modified: Thu, 02 Oct 2025 04:13:10 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881489fbe3371ef6d2a30a249ca557a070d45f81330d108b827bce4ead9ed483`  
		Last Modified: Thu, 02 Oct 2025 04:13:10 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:4584fea87a2fa321de90285bf309f29a053806e8e636725b84ddd3d93ba5206d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5940031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed64611efdf82eee700833a9e5b34332ea05e811f1d42b78d1e0214ded5d6801`

```dockerfile
```

-	Layers:
	-	`sha256:465984ecd1437617d92d682c849814ac13f6d83ed695789bc14bf37cd8a3cf22`  
		Last Modified: Thu, 02 Oct 2025 06:12:38 GMT  
		Size: 5.9 MB (5917085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15eed2f620624217e0135f6e2af6abdb01f8d604ff08fa70234a088f859dc557`  
		Last Modified: Thu, 02 Oct 2025 06:12:39 GMT  
		Size: 22.9 KB (22946 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:214a9c83cc720fb7d4d8d5b6807238a546d9f29f67d47d2104318f75a1bcd05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.3 MB (364344294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25cc4bebe385dd8f94221c4bc48f808af1d5dbac73fba93dd28295d63107369`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 08 Aug 2024 11:50:27 GMT
ARG RELEASE
# Thu, 08 Aug 2024 11:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 Aug 2024 11:50:27 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_MAJOR=9
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT []
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_FILE=geonetwork.war
# Thu, 08 Aug 2024 11:50:27 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_VERSION=3.12.12
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419aaa52607f6ef7a03a295c57fe451241093bacec0b8cbd975e95351624d644`  
		Last Modified: Thu, 02 Oct 2025 01:17:02 GMT  
		Size: 19.2 MB (19206364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ec6c766cb339fe7639e7b17d5743545c0002c3dbb08b75eae759be43211807`  
		Last Modified: Thu, 02 Oct 2025 01:17:05 GMT  
		Size: 53.8 MB (53839370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfa9f945462c02f1fde3906d24c8d0bed5c81c07e533c43e49ea449b2244882`  
		Last Modified: Thu, 02 Oct 2025 01:17:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a22966219fd178174a348aca3c91573a3628dd260afb986e17e85a311bd26b`  
		Last Modified: Thu, 02 Oct 2025 01:17:01 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1831ecb6e291ee4ccc5493128b2b650933fcbb7e1359ebc1d0f72bbc79ae3da`  
		Last Modified: Thu, 02 Oct 2025 02:35:56 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93d3b51040369a32308c5b88da3ea8d19afb8487c4c69c909e0bedd5958470a`  
		Last Modified: Thu, 02 Oct 2025 02:35:58 GMT  
		Size: 14.0 MB (13967139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042d35bc28459ceceaafd7168528451db2074e5c6ca99d9d32d5556f5b1801fb`  
		Last Modified: Thu, 02 Oct 2025 04:15:03 GMT  
		Size: 234.6 MB (234554394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422f93d4ddf037144c5ff55646da96edb70fcbe480727ab5db0cf9f354f151b4`  
		Last Modified: Thu, 02 Oct 2025 03:24:59 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049718d1ba3b4d745a0bc2b920733784f06924877edacfd6f1a37ff6c82df75d`  
		Last Modified: Thu, 02 Oct 2025 04:15:07 GMT  
		Size: 13.9 MB (13909087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b182e83f66e5dd1ab40d1e11b26995a81a1801d7aa847eb6a50ef18b37363d9`  
		Last Modified: Thu, 02 Oct 2025 04:15:03 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80bb68085d388e240aa2ad12f146313463b62fb070fc43d6190d310062d979d`  
		Last Modified: Thu, 02 Oct 2025 04:15:03 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca56c98fbdb06aa5382db810af8762f80fce32c030664a21307a2cd4b0898a86`  
		Last Modified: Thu, 02 Oct 2025 04:15:03 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:fc38214c8d984e2b0da08f5aa7e785c74d8e8b36e35d580dd95bc00790153ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5944547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ab0a2eb24500c2c7aac2f656252cad7136c53bc148472848d635dd17ba1790`

```dockerfile
```

-	Layers:
	-	`sha256:58de8c42bbe2c864253049f8bbc0d940918fc6ca71b4ceda478a34839825887e`  
		Last Modified: Thu, 02 Oct 2025 06:12:44 GMT  
		Size: 5.9 MB (5921578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaf9c1cac8de2308fbf42133e4517dd9781126c245376afebf82d5e267cd9d6f`  
		Last Modified: Thu, 02 Oct 2025 06:12:44 GMT  
		Size: 23.0 KB (22969 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:519216f2c26e4a6ec0937c5f7b963b0eba919208632102c89d85368dba624f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.3 MB (368322073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b712572d65858cb5e6c385a603ee9f1168fe78845ca160a72d45d1303113a00`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 08 Aug 2024 11:50:27 GMT
ARG RELEASE
# Thu, 08 Aug 2024 11:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 Aug 2024 11:50:27 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_MAJOR=9
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT []
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_FILE=geonetwork.war
# Thu, 08 Aug 2024 11:50:27 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_VERSION=3.12.12
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3102a54c6b2b7ecf7a7216123f26003eec1ece4dbee7d4985813592023f98cd3`  
		Last Modified: Mon, 15 Sep 2025 22:13:52 GMT  
		Size: 18.8 MB (18814803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fbd3108988f496e4134a4862d953a8c993115aeccbb0a4057f7261d82396f3`  
		Last Modified: Mon, 15 Sep 2025 22:13:58 GMT  
		Size: 52.2 MB (52167313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67ce08f3159aea036fc5ac087e7103091b6388431976c3e34a6e95daa24b83d`  
		Last Modified: Mon, 15 Sep 2025 22:13:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbefdb3dada19d520a48d2cd4aaf1451c5e151919b1df3ee0bf25d3b0fac385`  
		Last Modified: Mon, 15 Sep 2025 22:13:51 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af087b3e0dccc7cdae8cdd274abc54dec7b15e61c2a1475ecfc6c9297674b7f0`  
		Last Modified: Tue, 16 Sep 2025 00:28:42 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358d701de1f162895b6f87b8496b0d7ead71378b25d6584ee754e5f826187519`  
		Last Modified: Tue, 16 Sep 2025 00:28:44 GMT  
		Size: 14.0 MB (14023884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c36ea3b4c50fd203f3c2b0da5f1e30aa7afb5677c533820911d63bdacca68fb`  
		Last Modified: Tue, 16 Sep 2025 02:14:19 GMT  
		Size: 234.6 MB (234574700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a680493fd4eaaee1dae63e060d5078672b4e0ba9bf14ff5c94e13b6b5354a23c`  
		Last Modified: Tue, 16 Sep 2025 02:06:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b7d653d188805c367b4ab4bb7cfeb8fa9b21aad24613194df6cbc018ca3269`  
		Last Modified: Tue, 16 Sep 2025 02:11:00 GMT  
		Size: 14.4 MB (14431881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ebaa000666aea8abefdf43440a01bf6cd99abbc1da3ed063eab15c051a2ed7`  
		Last Modified: Tue, 16 Sep 2025 02:10:58 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba86205687b8ddf753034b3ef200a9d51d5127042b97e6dfed3a302e260e4d1`  
		Last Modified: Tue, 16 Sep 2025 02:10:59 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d805ef473a5d69012fc9db8b6d38ada4d03601913e174358a14af032f7eb10`  
		Last Modified: Tue, 16 Sep 2025 02:10:59 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:510198cc6a6b030ef7cbb68dbfd6f98973f31ce402c86b74310ce9ca030f9d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0a5038f5b825eb7672a59c18a1e5d8748817ff0d0b0677b1b6ed50308a0b85`

```dockerfile
```

-	Layers:
	-	`sha256:0d4b7acca116c5c85ebb9cfccf7396d6d25f498c9ec137257e441be6e8421be9`  
		Last Modified: Tue, 16 Sep 2025 03:13:08 GMT  
		Size: 5.9 MB (5919870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18cbe6eecd4014ae52d5468b4466b207c1fad086222af2e714b412f43dbe3334`  
		Last Modified: Tue, 16 Sep 2025 03:13:09 GMT  
		Size: 22.9 KB (22902 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12`

```console
$ docker pull geonetwork@sha256:6ff23bcc16fb342622dd1f2821e8c9da4f2586218eb9529cf000453538af6c53
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
$ docker pull geonetwork@sha256:bba90e970016f277e51eb28013672b6bedeb1c86968ec8adc6208759bb7da5f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.9 MB (349942124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea41ee04c6e9c612209cac646b7095b78d6e1c386f1c8920c5fbd3f7a94ea52`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 08 Aug 2024 11:50:27 GMT
ARG RELEASE
# Thu, 08 Aug 2024 11:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 Aug 2024 11:50:27 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_MAJOR=9
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT []
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_FILE=geonetwork.war
# Thu, 08 Aug 2024 11:50:27 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_VERSION=3.12.12
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb43857d5308a40718704288d12cb0f13a2c0c288decd5254238b35963ff9d7`  
		Last Modified: Mon, 15 Sep 2025 22:12:45 GMT  
		Size: 17.0 MB (16971774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75cee9f1f2e7610dad4413b9e913bd37b54330c43a35bd3c85ad28bad82617e`  
		Last Modified: Mon, 15 Sep 2025 22:12:50 GMT  
		Size: 54.7 MB (54739675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f3133ac8c49679b26388b308a6a3d27b36b06ec1443730b47518fd4134e813`  
		Last Modified: Mon, 15 Sep 2025 22:12:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b9ab2fa29f411732853d26d15ae764cec2feb5409374d10d1f97a71cbdca0a`  
		Last Modified: Mon, 15 Sep 2025 22:12:42 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63659d25f5259532448b0e29feb98f5066b8c91afd81f9a305b8872f34de7b9f`  
		Last Modified: Mon, 15 Sep 2025 23:23:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785c4ea8b033f125e3207bafec2320bedc6febf7b3aaab0a6cdd03ff510056f4`  
		Last Modified: Mon, 15 Sep 2025 23:23:49 GMT  
		Size: 14.0 MB (13954095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173897eb680420e3ea53b3e2e818df472917c72343c77e24f09d07144481ce98`  
		Last Modified: Tue, 16 Sep 2025 01:12:18 GMT  
		Size: 234.6 MB (234550180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8b55d57ba34b04ef3fe52c648ff02b834fff92bd0f68a461c9d72842e5aeed`  
		Last Modified: Tue, 16 Sep 2025 00:54:35 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:584eaee7049d5f2a3aba286df73aa6318a1c036d7331d8cbee172a1513790bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788ecd9aec4cea58c4770f0954bf5c484c1c216d11e193bf8d4b14b0f9054e4d`

```dockerfile
```

-	Layers:
	-	`sha256:33e8833dc193fddeabec9158e20d8f98e1573c6ba4a7f0514a3cee467da64b02`  
		Last Modified: Tue, 16 Sep 2025 03:12:30 GMT  
		Size: 4.4 MB (4359721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da4cb59af9c56ef5941a73471ff2bf4ae0b7ff7457c8fbd0baa2c6919ba2dcf8`  
		Last Modified: Tue, 16 Sep 2025 03:12:31 GMT  
		Size: 19.1 KB (19136 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:bdfba7c4627a02d766547c7f42ba240734761d8b4475bd763f463e7532b994a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.5 MB (343465760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc8d8c577cce7d5a3a699d749de5e373f0b3876e46ed7c4401682b619c1e30d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 08 Aug 2024 11:50:27 GMT
ARG RELEASE
# Thu, 08 Aug 2024 11:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 Aug 2024 11:50:27 GMT
ADD file:51076814e2aa1389d29f1b4c38eee0cfbb1d321f099c50e09b19452198f65032 in / 
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_MAJOR=9
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT []
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_FILE=geonetwork.war
# Thu, 08 Aug 2024 11:50:27 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_VERSION=3.12.12
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6c9f3e8be363989d138b8e3a1316487da5ee2b8384d3c6b0f9b1a8290f57caff`  
		Last Modified: Tue, 30 Sep 2025 17:07:34 GMT  
		Size: 26.9 MB (26851149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8256622f04cb21ac626f3652bc38fd100329ea6c631e2be7bc387bc03dd3db4e`  
		Last Modified: Thu, 02 Oct 2025 01:12:06 GMT  
		Size: 18.1 MB (18087038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7571f83f8225c088a30f1f928e7faab2958c61d4e0f21e841d05453d3fdef785`  
		Last Modified: Thu, 02 Oct 2025 01:12:11 GMT  
		Size: 50.1 MB (50123714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d8f3d99eebd3bbf209e4dff2ace919de2f05151555b21f48f120b0aed538a3`  
		Last Modified: Thu, 02 Oct 2025 01:12:05 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae14e8c0418c50502562376b3258f0dce4388713a374bd97c8285836d8a7408`  
		Last Modified: Thu, 02 Oct 2025 01:12:05 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417643604d378baecc97ba6be5d5b074629d671ce957256989003fd293f1a522`  
		Last Modified: Thu, 02 Oct 2025 02:19:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70dc23121b75674d8c12cab58dcc746932e1b217fc881c2588730b37e2d4531`  
		Last Modified: Thu, 02 Oct 2025 02:19:04 GMT  
		Size: 13.9 MB (13862417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6112f8f480482b90a5605caf697f8efb2eb9017f8ce6219858eaff1f5415fb`  
		Last Modified: Thu, 02 Oct 2025 04:12:12 GMT  
		Size: 234.5 MB (234538491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1301d8918150c620037ebf4085a5de9fd0ac1adcc64732bfc904faabf942ed`  
		Last Modified: Thu, 02 Oct 2025 03:17:09 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:fdfe246f036a27f050ba67c45ff87ae00742111727346f43ed264b12945aab06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4382906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395c3bfae6de8a9173cbe8c9a2c1604d8297bd3cccd68a2b230fe7256668c24a`

```dockerfile
```

-	Layers:
	-	`sha256:0a1e4639ebd72f9ec88a1c9d066daf4b3c76a29b754bf97c30549e6d10bfb3ca`  
		Last Modified: Thu, 02 Oct 2025 06:12:27 GMT  
		Size: 4.4 MB (4363698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7db65d5eb81993e79b4beedf12c4db39325d5be0f924b0ab0b9adee2cea4ca55`  
		Last Modified: Thu, 02 Oct 2025 06:12:27 GMT  
		Size: 19.2 KB (19208 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:5de1254105f301f8ef66c23fb62a670fde9962cbd3916a0102ba822f4d99b22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.4 MB (350431794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d69394b6229a68529c0f39f9e5de2d81d8164aae084ac40f442e2a471e4486`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 08 Aug 2024 11:50:27 GMT
ARG RELEASE
# Thu, 08 Aug 2024 11:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 Aug 2024 11:50:27 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_MAJOR=9
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT []
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_FILE=geonetwork.war
# Thu, 08 Aug 2024 11:50:27 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_VERSION=3.12.12
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419aaa52607f6ef7a03a295c57fe451241093bacec0b8cbd975e95351624d644`  
		Last Modified: Thu, 02 Oct 2025 01:17:02 GMT  
		Size: 19.2 MB (19206364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ec6c766cb339fe7639e7b17d5743545c0002c3dbb08b75eae759be43211807`  
		Last Modified: Thu, 02 Oct 2025 01:17:05 GMT  
		Size: 53.8 MB (53839370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfa9f945462c02f1fde3906d24c8d0bed5c81c07e533c43e49ea449b2244882`  
		Last Modified: Thu, 02 Oct 2025 01:17:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a22966219fd178174a348aca3c91573a3628dd260afb986e17e85a311bd26b`  
		Last Modified: Thu, 02 Oct 2025 01:17:01 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1831ecb6e291ee4ccc5493128b2b650933fcbb7e1359ebc1d0f72bbc79ae3da`  
		Last Modified: Thu, 02 Oct 2025 02:35:56 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93d3b51040369a32308c5b88da3ea8d19afb8487c4c69c909e0bedd5958470a`  
		Last Modified: Thu, 02 Oct 2025 02:35:58 GMT  
		Size: 14.0 MB (13967139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042d35bc28459ceceaafd7168528451db2074e5c6ca99d9d32d5556f5b1801fb`  
		Last Modified: Thu, 02 Oct 2025 04:15:03 GMT  
		Size: 234.6 MB (234554394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422f93d4ddf037144c5ff55646da96edb70fcbe480727ab5db0cf9f354f151b4`  
		Last Modified: Thu, 02 Oct 2025 03:24:59 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:caba546f35dc88dfe7d3b87bf35e6d5fc0d483043f43a50612dbb98dc1a84d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37acf6bade05d2782e21cc093e1fe59e152e73cdd6000e529520e2fef3e1ead8`

```dockerfile
```

-	Layers:
	-	`sha256:3bf1dbe931159ea352164a68ae1733beb002a733a93cd5ea7592b3b09b9ead6c`  
		Last Modified: Thu, 02 Oct 2025 06:12:32 GMT  
		Size: 4.4 MB (4360875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39cdf0068fcae66488a1d0b36d6fefba288b8f4a15147179c2ded3aad0c008a9`  
		Last Modified: Thu, 02 Oct 2025 06:12:33 GMT  
		Size: 19.2 KB (19228 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:2a04f31cdb00c576e9028076f8a6526a06f19fb75ab6518ae6e10b5e5e350f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.9 MB (353886776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c551566530972de12b906c58ab851e881a7137722c9b915f14d879483895d5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 08 Aug 2024 11:50:27 GMT
ARG RELEASE
# Thu, 08 Aug 2024 11:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 Aug 2024 11:50:27 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_MAJOR=9
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT []
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_FILE=geonetwork.war
# Thu, 08 Aug 2024 11:50:27 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_VERSION=3.12.12
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3102a54c6b2b7ecf7a7216123f26003eec1ece4dbee7d4985813592023f98cd3`  
		Last Modified: Mon, 15 Sep 2025 22:13:52 GMT  
		Size: 18.8 MB (18814803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fbd3108988f496e4134a4862d953a8c993115aeccbb0a4057f7261d82396f3`  
		Last Modified: Mon, 15 Sep 2025 22:13:58 GMT  
		Size: 52.2 MB (52167313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67ce08f3159aea036fc5ac087e7103091b6388431976c3e34a6e95daa24b83d`  
		Last Modified: Mon, 15 Sep 2025 22:13:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbefdb3dada19d520a48d2cd4aaf1451c5e151919b1df3ee0bf25d3b0fac385`  
		Last Modified: Mon, 15 Sep 2025 22:13:51 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af087b3e0dccc7cdae8cdd274abc54dec7b15e61c2a1475ecfc6c9297674b7f0`  
		Last Modified: Tue, 16 Sep 2025 00:28:42 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358d701de1f162895b6f87b8496b0d7ead71378b25d6584ee754e5f826187519`  
		Last Modified: Tue, 16 Sep 2025 00:28:44 GMT  
		Size: 14.0 MB (14023884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c36ea3b4c50fd203f3c2b0da5f1e30aa7afb5677c533820911d63bdacca68fb`  
		Last Modified: Tue, 16 Sep 2025 02:14:19 GMT  
		Size: 234.6 MB (234574700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a680493fd4eaaee1dae63e060d5078672b4e0ba9bf14ff5c94e13b6b5354a23c`  
		Last Modified: Tue, 16 Sep 2025 02:06:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:21341da91042e9145a0e194aa78ad75bf6e1d9d8309b5cfa594eaff1dee7c07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c14f29832050380d8398911ae7a11d5ec04b37f6bca09364b675ea95a6a2f1`

```dockerfile
```

-	Layers:
	-	`sha256:1382358527e701f1c00db7ac939c68c3812197c7298e1f21a0f236fb3f37a7fa`  
		Last Modified: Tue, 16 Sep 2025 03:12:47 GMT  
		Size: 4.4 MB (4362462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7549a28ab9f36050e10b7812e1844b16e944af68bb16106a201acb3f654fdb58`  
		Last Modified: Tue, 16 Sep 2025 03:12:48 GMT  
		Size: 19.2 KB (19174 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12-postgres`

```console
$ docker pull geonetwork@sha256:5bbed4c51b2c330c356310e70c9851038054b3ce810891da2645fa52ade2f14e
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
$ docker pull geonetwork@sha256:d28a249bf70dff7cf9e3f5fcd5cba3c7a6c7f4842a236b675d4f754584208317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.9 MB (363889462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1e525ba137bf1e68802272b7ba7a9a6fa5be66328ee04c5f2850c2984277e8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 08 Aug 2024 11:50:27 GMT
ARG RELEASE
# Thu, 08 Aug 2024 11:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 Aug 2024 11:50:27 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_MAJOR=9
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT []
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_FILE=geonetwork.war
# Thu, 08 Aug 2024 11:50:27 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_VERSION=3.12.12
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb43857d5308a40718704288d12cb0f13a2c0c288decd5254238b35963ff9d7`  
		Last Modified: Mon, 15 Sep 2025 22:12:45 GMT  
		Size: 17.0 MB (16971774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75cee9f1f2e7610dad4413b9e913bd37b54330c43a35bd3c85ad28bad82617e`  
		Last Modified: Mon, 15 Sep 2025 22:12:50 GMT  
		Size: 54.7 MB (54739675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f3133ac8c49679b26388b308a6a3d27b36b06ec1443730b47518fd4134e813`  
		Last Modified: Mon, 15 Sep 2025 22:12:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b9ab2fa29f411732853d26d15ae764cec2feb5409374d10d1f97a71cbdca0a`  
		Last Modified: Mon, 15 Sep 2025 22:12:42 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63659d25f5259532448b0e29feb98f5066b8c91afd81f9a305b8872f34de7b9f`  
		Last Modified: Mon, 15 Sep 2025 23:23:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785c4ea8b033f125e3207bafec2320bedc6febf7b3aaab0a6cdd03ff510056f4`  
		Last Modified: Mon, 15 Sep 2025 23:23:49 GMT  
		Size: 14.0 MB (13954095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173897eb680420e3ea53b3e2e818df472917c72343c77e24f09d07144481ce98`  
		Last Modified: Tue, 16 Sep 2025 01:12:18 GMT  
		Size: 234.6 MB (234550180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8b55d57ba34b04ef3fe52c648ff02b834fff92bd0f68a461c9d72842e5aeed`  
		Last Modified: Tue, 16 Sep 2025 00:54:35 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b53f35934b1dfe4b534788a1e3b140dfed57b5abe2fd67eae2afb3c4e81db1`  
		Last Modified: Tue, 16 Sep 2025 01:12:54 GMT  
		Size: 13.9 MB (13943929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6767f00a91a304e754e504a4ae2e4a62b073709370a852bb45d6ac8e453d6a7`  
		Last Modified: Tue, 16 Sep 2025 01:12:53 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4bc6e9905bac16a8297aa82645b83ad990e20a462e0d9096a157be7cb610a7`  
		Last Modified: Tue, 16 Sep 2025 01:12:53 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26ef08397cd361fc5a452abe0b2b9cd6c5ef181da92a64558e51d8f7d9f9615`  
		Last Modified: Tue, 16 Sep 2025 01:12:53 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:9327a4a9bf2eef1a209559fabe7b313015b1b8dc447046a5707130594c8b9df4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5937234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ec30f439c2f2ce6fd018c001112bd35fd5f3e7f70cddea77256df5cd8af047`

```dockerfile
```

-	Layers:
	-	`sha256:b46774ae17f7c5a50de86793a2eb8b4f9706377f6a5a06b9ebfc176dc679f56c`  
		Last Modified: Tue, 16 Sep 2025 03:12:46 GMT  
		Size: 5.9 MB (5914372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcc521891e26f29893ee09369461d1e64730cc522b9ab3eae35fbb78ea224615`  
		Last Modified: Tue, 16 Sep 2025 03:12:47 GMT  
		Size: 22.9 KB (22862 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:8b3d0b45f6ea9a87f2563134f6c3f8f59f76995f0f74d2945df992c739a3ab92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.5 MB (356473761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:999e51fdf19e26743b9b659e27478193020681b0dfc27023295c67e855275359`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 08 Aug 2024 11:50:27 GMT
ARG RELEASE
# Thu, 08 Aug 2024 11:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 Aug 2024 11:50:27 GMT
ADD file:51076814e2aa1389d29f1b4c38eee0cfbb1d321f099c50e09b19452198f65032 in / 
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_MAJOR=9
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT []
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_FILE=geonetwork.war
# Thu, 08 Aug 2024 11:50:27 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_VERSION=3.12.12
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6c9f3e8be363989d138b8e3a1316487da5ee2b8384d3c6b0f9b1a8290f57caff`  
		Last Modified: Tue, 30 Sep 2025 17:07:34 GMT  
		Size: 26.9 MB (26851149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8256622f04cb21ac626f3652bc38fd100329ea6c631e2be7bc387bc03dd3db4e`  
		Last Modified: Thu, 02 Oct 2025 01:12:06 GMT  
		Size: 18.1 MB (18087038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7571f83f8225c088a30f1f928e7faab2958c61d4e0f21e841d05453d3fdef785`  
		Last Modified: Thu, 02 Oct 2025 01:12:11 GMT  
		Size: 50.1 MB (50123714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d8f3d99eebd3bbf209e4dff2ace919de2f05151555b21f48f120b0aed538a3`  
		Last Modified: Thu, 02 Oct 2025 01:12:05 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae14e8c0418c50502562376b3258f0dce4388713a374bd97c8285836d8a7408`  
		Last Modified: Thu, 02 Oct 2025 01:12:05 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417643604d378baecc97ba6be5d5b074629d671ce957256989003fd293f1a522`  
		Last Modified: Thu, 02 Oct 2025 02:19:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70dc23121b75674d8c12cab58dcc746932e1b217fc881c2588730b37e2d4531`  
		Last Modified: Thu, 02 Oct 2025 02:19:04 GMT  
		Size: 13.9 MB (13862417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6112f8f480482b90a5605caf697f8efb2eb9017f8ce6219858eaff1f5415fb`  
		Last Modified: Thu, 02 Oct 2025 04:12:12 GMT  
		Size: 234.5 MB (234538491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1301d8918150c620037ebf4085a5de9fd0ac1adcc64732bfc904faabf942ed`  
		Last Modified: Thu, 02 Oct 2025 03:17:09 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8f3b4ad3cae3bb25587d2ba768b77f68b57ff3117fbf936a9fe70b6e3e41c8`  
		Last Modified: Thu, 02 Oct 2025 04:13:11 GMT  
		Size: 13.0 MB (13004591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73dc455ea18f17b9b01f68da4d5c80e5c86e18abf6d9fad5279c730cb5563e1`  
		Last Modified: Thu, 02 Oct 2025 04:13:09 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7af8d9bf38e6e2b183b9aa24927c70dea8a39c57030f63ee4472116397b5fad`  
		Last Modified: Thu, 02 Oct 2025 04:13:10 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881489fbe3371ef6d2a30a249ca557a070d45f81330d108b827bce4ead9ed483`  
		Last Modified: Thu, 02 Oct 2025 04:13:10 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:4584fea87a2fa321de90285bf309f29a053806e8e636725b84ddd3d93ba5206d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5940031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed64611efdf82eee700833a9e5b34332ea05e811f1d42b78d1e0214ded5d6801`

```dockerfile
```

-	Layers:
	-	`sha256:465984ecd1437617d92d682c849814ac13f6d83ed695789bc14bf37cd8a3cf22`  
		Last Modified: Thu, 02 Oct 2025 06:12:38 GMT  
		Size: 5.9 MB (5917085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15eed2f620624217e0135f6e2af6abdb01f8d604ff08fa70234a088f859dc557`  
		Last Modified: Thu, 02 Oct 2025 06:12:39 GMT  
		Size: 22.9 KB (22946 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:214a9c83cc720fb7d4d8d5b6807238a546d9f29f67d47d2104318f75a1bcd05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.3 MB (364344294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25cc4bebe385dd8f94221c4bc48f808af1d5dbac73fba93dd28295d63107369`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 08 Aug 2024 11:50:27 GMT
ARG RELEASE
# Thu, 08 Aug 2024 11:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 Aug 2024 11:50:27 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_MAJOR=9
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT []
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_FILE=geonetwork.war
# Thu, 08 Aug 2024 11:50:27 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_VERSION=3.12.12
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419aaa52607f6ef7a03a295c57fe451241093bacec0b8cbd975e95351624d644`  
		Last Modified: Thu, 02 Oct 2025 01:17:02 GMT  
		Size: 19.2 MB (19206364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ec6c766cb339fe7639e7b17d5743545c0002c3dbb08b75eae759be43211807`  
		Last Modified: Thu, 02 Oct 2025 01:17:05 GMT  
		Size: 53.8 MB (53839370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfa9f945462c02f1fde3906d24c8d0bed5c81c07e533c43e49ea449b2244882`  
		Last Modified: Thu, 02 Oct 2025 01:17:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a22966219fd178174a348aca3c91573a3628dd260afb986e17e85a311bd26b`  
		Last Modified: Thu, 02 Oct 2025 01:17:01 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1831ecb6e291ee4ccc5493128b2b650933fcbb7e1359ebc1d0f72bbc79ae3da`  
		Last Modified: Thu, 02 Oct 2025 02:35:56 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93d3b51040369a32308c5b88da3ea8d19afb8487c4c69c909e0bedd5958470a`  
		Last Modified: Thu, 02 Oct 2025 02:35:58 GMT  
		Size: 14.0 MB (13967139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042d35bc28459ceceaafd7168528451db2074e5c6ca99d9d32d5556f5b1801fb`  
		Last Modified: Thu, 02 Oct 2025 04:15:03 GMT  
		Size: 234.6 MB (234554394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422f93d4ddf037144c5ff55646da96edb70fcbe480727ab5db0cf9f354f151b4`  
		Last Modified: Thu, 02 Oct 2025 03:24:59 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049718d1ba3b4d745a0bc2b920733784f06924877edacfd6f1a37ff6c82df75d`  
		Last Modified: Thu, 02 Oct 2025 04:15:07 GMT  
		Size: 13.9 MB (13909087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b182e83f66e5dd1ab40d1e11b26995a81a1801d7aa847eb6a50ef18b37363d9`  
		Last Modified: Thu, 02 Oct 2025 04:15:03 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80bb68085d388e240aa2ad12f146313463b62fb070fc43d6190d310062d979d`  
		Last Modified: Thu, 02 Oct 2025 04:15:03 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca56c98fbdb06aa5382db810af8762f80fce32c030664a21307a2cd4b0898a86`  
		Last Modified: Thu, 02 Oct 2025 04:15:03 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:fc38214c8d984e2b0da08f5aa7e785c74d8e8b36e35d580dd95bc00790153ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5944547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ab0a2eb24500c2c7aac2f656252cad7136c53bc148472848d635dd17ba1790`

```dockerfile
```

-	Layers:
	-	`sha256:58de8c42bbe2c864253049f8bbc0d940918fc6ca71b4ceda478a34839825887e`  
		Last Modified: Thu, 02 Oct 2025 06:12:44 GMT  
		Size: 5.9 MB (5921578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaf9c1cac8de2308fbf42133e4517dd9781126c245376afebf82d5e267cd9d6f`  
		Last Modified: Thu, 02 Oct 2025 06:12:44 GMT  
		Size: 23.0 KB (22969 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:519216f2c26e4a6ec0937c5f7b963b0eba919208632102c89d85368dba624f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.3 MB (368322073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b712572d65858cb5e6c385a603ee9f1168fe78845ca160a72d45d1303113a00`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 08 Aug 2024 11:50:27 GMT
ARG RELEASE
# Thu, 08 Aug 2024 11:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 Aug 2024 11:50:27 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_MAJOR=9
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT []
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_FILE=geonetwork.war
# Thu, 08 Aug 2024 11:50:27 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_VERSION=3.12.12
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3102a54c6b2b7ecf7a7216123f26003eec1ece4dbee7d4985813592023f98cd3`  
		Last Modified: Mon, 15 Sep 2025 22:13:52 GMT  
		Size: 18.8 MB (18814803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fbd3108988f496e4134a4862d953a8c993115aeccbb0a4057f7261d82396f3`  
		Last Modified: Mon, 15 Sep 2025 22:13:58 GMT  
		Size: 52.2 MB (52167313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67ce08f3159aea036fc5ac087e7103091b6388431976c3e34a6e95daa24b83d`  
		Last Modified: Mon, 15 Sep 2025 22:13:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbefdb3dada19d520a48d2cd4aaf1451c5e151919b1df3ee0bf25d3b0fac385`  
		Last Modified: Mon, 15 Sep 2025 22:13:51 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af087b3e0dccc7cdae8cdd274abc54dec7b15e61c2a1475ecfc6c9297674b7f0`  
		Last Modified: Tue, 16 Sep 2025 00:28:42 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358d701de1f162895b6f87b8496b0d7ead71378b25d6584ee754e5f826187519`  
		Last Modified: Tue, 16 Sep 2025 00:28:44 GMT  
		Size: 14.0 MB (14023884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c36ea3b4c50fd203f3c2b0da5f1e30aa7afb5677c533820911d63bdacca68fb`  
		Last Modified: Tue, 16 Sep 2025 02:14:19 GMT  
		Size: 234.6 MB (234574700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a680493fd4eaaee1dae63e060d5078672b4e0ba9bf14ff5c94e13b6b5354a23c`  
		Last Modified: Tue, 16 Sep 2025 02:06:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b7d653d188805c367b4ab4bb7cfeb8fa9b21aad24613194df6cbc018ca3269`  
		Last Modified: Tue, 16 Sep 2025 02:11:00 GMT  
		Size: 14.4 MB (14431881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ebaa000666aea8abefdf43440a01bf6cd99abbc1da3ed063eab15c051a2ed7`  
		Last Modified: Tue, 16 Sep 2025 02:10:58 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba86205687b8ddf753034b3ef200a9d51d5127042b97e6dfed3a302e260e4d1`  
		Last Modified: Tue, 16 Sep 2025 02:10:59 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d805ef473a5d69012fc9db8b6d38ada4d03601913e174358a14af032f7eb10`  
		Last Modified: Tue, 16 Sep 2025 02:10:59 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:510198cc6a6b030ef7cbb68dbfd6f98973f31ce402c86b74310ce9ca030f9d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0a5038f5b825eb7672a59c18a1e5d8748817ff0d0b0677b1b6ed50308a0b85`

```dockerfile
```

-	Layers:
	-	`sha256:0d4b7acca116c5c85ebb9cfccf7396d6d25f498c9ec137257e441be6e8421be9`  
		Last Modified: Tue, 16 Sep 2025 03:13:08 GMT  
		Size: 5.9 MB (5919870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18cbe6eecd4014ae52d5468b4466b207c1fad086222af2e714b412f43dbe3334`  
		Last Modified: Tue, 16 Sep 2025 03:13:09 GMT  
		Size: 22.9 KB (22902 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12.12`

```console
$ docker pull geonetwork@sha256:6ff23bcc16fb342622dd1f2821e8c9da4f2586218eb9529cf000453538af6c53
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
$ docker pull geonetwork@sha256:bba90e970016f277e51eb28013672b6bedeb1c86968ec8adc6208759bb7da5f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.9 MB (349942124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea41ee04c6e9c612209cac646b7095b78d6e1c386f1c8920c5fbd3f7a94ea52`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 08 Aug 2024 11:50:27 GMT
ARG RELEASE
# Thu, 08 Aug 2024 11:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 Aug 2024 11:50:27 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_MAJOR=9
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT []
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_FILE=geonetwork.war
# Thu, 08 Aug 2024 11:50:27 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_VERSION=3.12.12
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb43857d5308a40718704288d12cb0f13a2c0c288decd5254238b35963ff9d7`  
		Last Modified: Mon, 15 Sep 2025 22:12:45 GMT  
		Size: 17.0 MB (16971774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75cee9f1f2e7610dad4413b9e913bd37b54330c43a35bd3c85ad28bad82617e`  
		Last Modified: Mon, 15 Sep 2025 22:12:50 GMT  
		Size: 54.7 MB (54739675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f3133ac8c49679b26388b308a6a3d27b36b06ec1443730b47518fd4134e813`  
		Last Modified: Mon, 15 Sep 2025 22:12:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b9ab2fa29f411732853d26d15ae764cec2feb5409374d10d1f97a71cbdca0a`  
		Last Modified: Mon, 15 Sep 2025 22:12:42 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63659d25f5259532448b0e29feb98f5066b8c91afd81f9a305b8872f34de7b9f`  
		Last Modified: Mon, 15 Sep 2025 23:23:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785c4ea8b033f125e3207bafec2320bedc6febf7b3aaab0a6cdd03ff510056f4`  
		Last Modified: Mon, 15 Sep 2025 23:23:49 GMT  
		Size: 14.0 MB (13954095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173897eb680420e3ea53b3e2e818df472917c72343c77e24f09d07144481ce98`  
		Last Modified: Tue, 16 Sep 2025 01:12:18 GMT  
		Size: 234.6 MB (234550180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8b55d57ba34b04ef3fe52c648ff02b834fff92bd0f68a461c9d72842e5aeed`  
		Last Modified: Tue, 16 Sep 2025 00:54:35 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:584eaee7049d5f2a3aba286df73aa6318a1c036d7331d8cbee172a1513790bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788ecd9aec4cea58c4770f0954bf5c484c1c216d11e193bf8d4b14b0f9054e4d`

```dockerfile
```

-	Layers:
	-	`sha256:33e8833dc193fddeabec9158e20d8f98e1573c6ba4a7f0514a3cee467da64b02`  
		Last Modified: Tue, 16 Sep 2025 03:12:30 GMT  
		Size: 4.4 MB (4359721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da4cb59af9c56ef5941a73471ff2bf4ae0b7ff7457c8fbd0baa2c6919ba2dcf8`  
		Last Modified: Tue, 16 Sep 2025 03:12:31 GMT  
		Size: 19.1 KB (19136 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:bdfba7c4627a02d766547c7f42ba240734761d8b4475bd763f463e7532b994a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.5 MB (343465760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc8d8c577cce7d5a3a699d749de5e373f0b3876e46ed7c4401682b619c1e30d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 08 Aug 2024 11:50:27 GMT
ARG RELEASE
# Thu, 08 Aug 2024 11:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 Aug 2024 11:50:27 GMT
ADD file:51076814e2aa1389d29f1b4c38eee0cfbb1d321f099c50e09b19452198f65032 in / 
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_MAJOR=9
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT []
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_FILE=geonetwork.war
# Thu, 08 Aug 2024 11:50:27 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_VERSION=3.12.12
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6c9f3e8be363989d138b8e3a1316487da5ee2b8384d3c6b0f9b1a8290f57caff`  
		Last Modified: Tue, 30 Sep 2025 17:07:34 GMT  
		Size: 26.9 MB (26851149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8256622f04cb21ac626f3652bc38fd100329ea6c631e2be7bc387bc03dd3db4e`  
		Last Modified: Thu, 02 Oct 2025 01:12:06 GMT  
		Size: 18.1 MB (18087038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7571f83f8225c088a30f1f928e7faab2958c61d4e0f21e841d05453d3fdef785`  
		Last Modified: Thu, 02 Oct 2025 01:12:11 GMT  
		Size: 50.1 MB (50123714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d8f3d99eebd3bbf209e4dff2ace919de2f05151555b21f48f120b0aed538a3`  
		Last Modified: Thu, 02 Oct 2025 01:12:05 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae14e8c0418c50502562376b3258f0dce4388713a374bd97c8285836d8a7408`  
		Last Modified: Thu, 02 Oct 2025 01:12:05 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417643604d378baecc97ba6be5d5b074629d671ce957256989003fd293f1a522`  
		Last Modified: Thu, 02 Oct 2025 02:19:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70dc23121b75674d8c12cab58dcc746932e1b217fc881c2588730b37e2d4531`  
		Last Modified: Thu, 02 Oct 2025 02:19:04 GMT  
		Size: 13.9 MB (13862417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6112f8f480482b90a5605caf697f8efb2eb9017f8ce6219858eaff1f5415fb`  
		Last Modified: Thu, 02 Oct 2025 04:12:12 GMT  
		Size: 234.5 MB (234538491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1301d8918150c620037ebf4085a5de9fd0ac1adcc64732bfc904faabf942ed`  
		Last Modified: Thu, 02 Oct 2025 03:17:09 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:fdfe246f036a27f050ba67c45ff87ae00742111727346f43ed264b12945aab06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4382906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395c3bfae6de8a9173cbe8c9a2c1604d8297bd3cccd68a2b230fe7256668c24a`

```dockerfile
```

-	Layers:
	-	`sha256:0a1e4639ebd72f9ec88a1c9d066daf4b3c76a29b754bf97c30549e6d10bfb3ca`  
		Last Modified: Thu, 02 Oct 2025 06:12:27 GMT  
		Size: 4.4 MB (4363698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7db65d5eb81993e79b4beedf12c4db39325d5be0f924b0ab0b9adee2cea4ca55`  
		Last Modified: Thu, 02 Oct 2025 06:12:27 GMT  
		Size: 19.2 KB (19208 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:5de1254105f301f8ef66c23fb62a670fde9962cbd3916a0102ba822f4d99b22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.4 MB (350431794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d69394b6229a68529c0f39f9e5de2d81d8164aae084ac40f442e2a471e4486`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 08 Aug 2024 11:50:27 GMT
ARG RELEASE
# Thu, 08 Aug 2024 11:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 Aug 2024 11:50:27 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_MAJOR=9
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT []
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_FILE=geonetwork.war
# Thu, 08 Aug 2024 11:50:27 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_VERSION=3.12.12
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419aaa52607f6ef7a03a295c57fe451241093bacec0b8cbd975e95351624d644`  
		Last Modified: Thu, 02 Oct 2025 01:17:02 GMT  
		Size: 19.2 MB (19206364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ec6c766cb339fe7639e7b17d5743545c0002c3dbb08b75eae759be43211807`  
		Last Modified: Thu, 02 Oct 2025 01:17:05 GMT  
		Size: 53.8 MB (53839370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfa9f945462c02f1fde3906d24c8d0bed5c81c07e533c43e49ea449b2244882`  
		Last Modified: Thu, 02 Oct 2025 01:17:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a22966219fd178174a348aca3c91573a3628dd260afb986e17e85a311bd26b`  
		Last Modified: Thu, 02 Oct 2025 01:17:01 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1831ecb6e291ee4ccc5493128b2b650933fcbb7e1359ebc1d0f72bbc79ae3da`  
		Last Modified: Thu, 02 Oct 2025 02:35:56 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93d3b51040369a32308c5b88da3ea8d19afb8487c4c69c909e0bedd5958470a`  
		Last Modified: Thu, 02 Oct 2025 02:35:58 GMT  
		Size: 14.0 MB (13967139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042d35bc28459ceceaafd7168528451db2074e5c6ca99d9d32d5556f5b1801fb`  
		Last Modified: Thu, 02 Oct 2025 04:15:03 GMT  
		Size: 234.6 MB (234554394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422f93d4ddf037144c5ff55646da96edb70fcbe480727ab5db0cf9f354f151b4`  
		Last Modified: Thu, 02 Oct 2025 03:24:59 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:caba546f35dc88dfe7d3b87bf35e6d5fc0d483043f43a50612dbb98dc1a84d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37acf6bade05d2782e21cc093e1fe59e152e73cdd6000e529520e2fef3e1ead8`

```dockerfile
```

-	Layers:
	-	`sha256:3bf1dbe931159ea352164a68ae1733beb002a733a93cd5ea7592b3b09b9ead6c`  
		Last Modified: Thu, 02 Oct 2025 06:12:32 GMT  
		Size: 4.4 MB (4360875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39cdf0068fcae66488a1d0b36d6fefba288b8f4a15147179c2ded3aad0c008a9`  
		Last Modified: Thu, 02 Oct 2025 06:12:33 GMT  
		Size: 19.2 KB (19228 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:2a04f31cdb00c576e9028076f8a6526a06f19fb75ab6518ae6e10b5e5e350f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.9 MB (353886776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c551566530972de12b906c58ab851e881a7137722c9b915f14d879483895d5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 08 Aug 2024 11:50:27 GMT
ARG RELEASE
# Thu, 08 Aug 2024 11:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 Aug 2024 11:50:27 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_MAJOR=9
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT []
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_FILE=geonetwork.war
# Thu, 08 Aug 2024 11:50:27 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_VERSION=3.12.12
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3102a54c6b2b7ecf7a7216123f26003eec1ece4dbee7d4985813592023f98cd3`  
		Last Modified: Mon, 15 Sep 2025 22:13:52 GMT  
		Size: 18.8 MB (18814803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fbd3108988f496e4134a4862d953a8c993115aeccbb0a4057f7261d82396f3`  
		Last Modified: Mon, 15 Sep 2025 22:13:58 GMT  
		Size: 52.2 MB (52167313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67ce08f3159aea036fc5ac087e7103091b6388431976c3e34a6e95daa24b83d`  
		Last Modified: Mon, 15 Sep 2025 22:13:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbefdb3dada19d520a48d2cd4aaf1451c5e151919b1df3ee0bf25d3b0fac385`  
		Last Modified: Mon, 15 Sep 2025 22:13:51 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af087b3e0dccc7cdae8cdd274abc54dec7b15e61c2a1475ecfc6c9297674b7f0`  
		Last Modified: Tue, 16 Sep 2025 00:28:42 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358d701de1f162895b6f87b8496b0d7ead71378b25d6584ee754e5f826187519`  
		Last Modified: Tue, 16 Sep 2025 00:28:44 GMT  
		Size: 14.0 MB (14023884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c36ea3b4c50fd203f3c2b0da5f1e30aa7afb5677c533820911d63bdacca68fb`  
		Last Modified: Tue, 16 Sep 2025 02:14:19 GMT  
		Size: 234.6 MB (234574700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a680493fd4eaaee1dae63e060d5078672b4e0ba9bf14ff5c94e13b6b5354a23c`  
		Last Modified: Tue, 16 Sep 2025 02:06:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:21341da91042e9145a0e194aa78ad75bf6e1d9d8309b5cfa594eaff1dee7c07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c14f29832050380d8398911ae7a11d5ec04b37f6bca09364b675ea95a6a2f1`

```dockerfile
```

-	Layers:
	-	`sha256:1382358527e701f1c00db7ac939c68c3812197c7298e1f21a0f236fb3f37a7fa`  
		Last Modified: Tue, 16 Sep 2025 03:12:47 GMT  
		Size: 4.4 MB (4362462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7549a28ab9f36050e10b7812e1844b16e944af68bb16106a201acb3f654fdb58`  
		Last Modified: Tue, 16 Sep 2025 03:12:48 GMT  
		Size: 19.2 KB (19174 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12.12-postgres`

```console
$ docker pull geonetwork@sha256:5bbed4c51b2c330c356310e70c9851038054b3ce810891da2645fa52ade2f14e
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
$ docker pull geonetwork@sha256:d28a249bf70dff7cf9e3f5fcd5cba3c7a6c7f4842a236b675d4f754584208317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.9 MB (363889462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1e525ba137bf1e68802272b7ba7a9a6fa5be66328ee04c5f2850c2984277e8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 08 Aug 2024 11:50:27 GMT
ARG RELEASE
# Thu, 08 Aug 2024 11:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 Aug 2024 11:50:27 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_MAJOR=9
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT []
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_FILE=geonetwork.war
# Thu, 08 Aug 2024 11:50:27 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_VERSION=3.12.12
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb43857d5308a40718704288d12cb0f13a2c0c288decd5254238b35963ff9d7`  
		Last Modified: Mon, 15 Sep 2025 22:12:45 GMT  
		Size: 17.0 MB (16971774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75cee9f1f2e7610dad4413b9e913bd37b54330c43a35bd3c85ad28bad82617e`  
		Last Modified: Mon, 15 Sep 2025 22:12:50 GMT  
		Size: 54.7 MB (54739675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f3133ac8c49679b26388b308a6a3d27b36b06ec1443730b47518fd4134e813`  
		Last Modified: Mon, 15 Sep 2025 22:12:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b9ab2fa29f411732853d26d15ae764cec2feb5409374d10d1f97a71cbdca0a`  
		Last Modified: Mon, 15 Sep 2025 22:12:42 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63659d25f5259532448b0e29feb98f5066b8c91afd81f9a305b8872f34de7b9f`  
		Last Modified: Mon, 15 Sep 2025 23:23:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785c4ea8b033f125e3207bafec2320bedc6febf7b3aaab0a6cdd03ff510056f4`  
		Last Modified: Mon, 15 Sep 2025 23:23:49 GMT  
		Size: 14.0 MB (13954095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173897eb680420e3ea53b3e2e818df472917c72343c77e24f09d07144481ce98`  
		Last Modified: Tue, 16 Sep 2025 01:12:18 GMT  
		Size: 234.6 MB (234550180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8b55d57ba34b04ef3fe52c648ff02b834fff92bd0f68a461c9d72842e5aeed`  
		Last Modified: Tue, 16 Sep 2025 00:54:35 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b53f35934b1dfe4b534788a1e3b140dfed57b5abe2fd67eae2afb3c4e81db1`  
		Last Modified: Tue, 16 Sep 2025 01:12:54 GMT  
		Size: 13.9 MB (13943929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6767f00a91a304e754e504a4ae2e4a62b073709370a852bb45d6ac8e453d6a7`  
		Last Modified: Tue, 16 Sep 2025 01:12:53 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4bc6e9905bac16a8297aa82645b83ad990e20a462e0d9096a157be7cb610a7`  
		Last Modified: Tue, 16 Sep 2025 01:12:53 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26ef08397cd361fc5a452abe0b2b9cd6c5ef181da92a64558e51d8f7d9f9615`  
		Last Modified: Tue, 16 Sep 2025 01:12:53 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:9327a4a9bf2eef1a209559fabe7b313015b1b8dc447046a5707130594c8b9df4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5937234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ec30f439c2f2ce6fd018c001112bd35fd5f3e7f70cddea77256df5cd8af047`

```dockerfile
```

-	Layers:
	-	`sha256:b46774ae17f7c5a50de86793a2eb8b4f9706377f6a5a06b9ebfc176dc679f56c`  
		Last Modified: Tue, 16 Sep 2025 03:12:46 GMT  
		Size: 5.9 MB (5914372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcc521891e26f29893ee09369461d1e64730cc522b9ab3eae35fbb78ea224615`  
		Last Modified: Tue, 16 Sep 2025 03:12:47 GMT  
		Size: 22.9 KB (22862 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:8b3d0b45f6ea9a87f2563134f6c3f8f59f76995f0f74d2945df992c739a3ab92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.5 MB (356473761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:999e51fdf19e26743b9b659e27478193020681b0dfc27023295c67e855275359`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 08 Aug 2024 11:50:27 GMT
ARG RELEASE
# Thu, 08 Aug 2024 11:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 Aug 2024 11:50:27 GMT
ADD file:51076814e2aa1389d29f1b4c38eee0cfbb1d321f099c50e09b19452198f65032 in / 
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_MAJOR=9
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT []
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_FILE=geonetwork.war
# Thu, 08 Aug 2024 11:50:27 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_VERSION=3.12.12
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6c9f3e8be363989d138b8e3a1316487da5ee2b8384d3c6b0f9b1a8290f57caff`  
		Last Modified: Tue, 30 Sep 2025 17:07:34 GMT  
		Size: 26.9 MB (26851149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8256622f04cb21ac626f3652bc38fd100329ea6c631e2be7bc387bc03dd3db4e`  
		Last Modified: Thu, 02 Oct 2025 01:12:06 GMT  
		Size: 18.1 MB (18087038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7571f83f8225c088a30f1f928e7faab2958c61d4e0f21e841d05453d3fdef785`  
		Last Modified: Thu, 02 Oct 2025 01:12:11 GMT  
		Size: 50.1 MB (50123714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d8f3d99eebd3bbf209e4dff2ace919de2f05151555b21f48f120b0aed538a3`  
		Last Modified: Thu, 02 Oct 2025 01:12:05 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae14e8c0418c50502562376b3258f0dce4388713a374bd97c8285836d8a7408`  
		Last Modified: Thu, 02 Oct 2025 01:12:05 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417643604d378baecc97ba6be5d5b074629d671ce957256989003fd293f1a522`  
		Last Modified: Thu, 02 Oct 2025 02:19:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70dc23121b75674d8c12cab58dcc746932e1b217fc881c2588730b37e2d4531`  
		Last Modified: Thu, 02 Oct 2025 02:19:04 GMT  
		Size: 13.9 MB (13862417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6112f8f480482b90a5605caf697f8efb2eb9017f8ce6219858eaff1f5415fb`  
		Last Modified: Thu, 02 Oct 2025 04:12:12 GMT  
		Size: 234.5 MB (234538491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1301d8918150c620037ebf4085a5de9fd0ac1adcc64732bfc904faabf942ed`  
		Last Modified: Thu, 02 Oct 2025 03:17:09 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8f3b4ad3cae3bb25587d2ba768b77f68b57ff3117fbf936a9fe70b6e3e41c8`  
		Last Modified: Thu, 02 Oct 2025 04:13:11 GMT  
		Size: 13.0 MB (13004591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73dc455ea18f17b9b01f68da4d5c80e5c86e18abf6d9fad5279c730cb5563e1`  
		Last Modified: Thu, 02 Oct 2025 04:13:09 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7af8d9bf38e6e2b183b9aa24927c70dea8a39c57030f63ee4472116397b5fad`  
		Last Modified: Thu, 02 Oct 2025 04:13:10 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881489fbe3371ef6d2a30a249ca557a070d45f81330d108b827bce4ead9ed483`  
		Last Modified: Thu, 02 Oct 2025 04:13:10 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:4584fea87a2fa321de90285bf309f29a053806e8e636725b84ddd3d93ba5206d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5940031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed64611efdf82eee700833a9e5b34332ea05e811f1d42b78d1e0214ded5d6801`

```dockerfile
```

-	Layers:
	-	`sha256:465984ecd1437617d92d682c849814ac13f6d83ed695789bc14bf37cd8a3cf22`  
		Last Modified: Thu, 02 Oct 2025 06:12:38 GMT  
		Size: 5.9 MB (5917085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15eed2f620624217e0135f6e2af6abdb01f8d604ff08fa70234a088f859dc557`  
		Last Modified: Thu, 02 Oct 2025 06:12:39 GMT  
		Size: 22.9 KB (22946 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:214a9c83cc720fb7d4d8d5b6807238a546d9f29f67d47d2104318f75a1bcd05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.3 MB (364344294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25cc4bebe385dd8f94221c4bc48f808af1d5dbac73fba93dd28295d63107369`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 08 Aug 2024 11:50:27 GMT
ARG RELEASE
# Thu, 08 Aug 2024 11:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 Aug 2024 11:50:27 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_MAJOR=9
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT []
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_FILE=geonetwork.war
# Thu, 08 Aug 2024 11:50:27 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_VERSION=3.12.12
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419aaa52607f6ef7a03a295c57fe451241093bacec0b8cbd975e95351624d644`  
		Last Modified: Thu, 02 Oct 2025 01:17:02 GMT  
		Size: 19.2 MB (19206364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ec6c766cb339fe7639e7b17d5743545c0002c3dbb08b75eae759be43211807`  
		Last Modified: Thu, 02 Oct 2025 01:17:05 GMT  
		Size: 53.8 MB (53839370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfa9f945462c02f1fde3906d24c8d0bed5c81c07e533c43e49ea449b2244882`  
		Last Modified: Thu, 02 Oct 2025 01:17:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a22966219fd178174a348aca3c91573a3628dd260afb986e17e85a311bd26b`  
		Last Modified: Thu, 02 Oct 2025 01:17:01 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1831ecb6e291ee4ccc5493128b2b650933fcbb7e1359ebc1d0f72bbc79ae3da`  
		Last Modified: Thu, 02 Oct 2025 02:35:56 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93d3b51040369a32308c5b88da3ea8d19afb8487c4c69c909e0bedd5958470a`  
		Last Modified: Thu, 02 Oct 2025 02:35:58 GMT  
		Size: 14.0 MB (13967139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042d35bc28459ceceaafd7168528451db2074e5c6ca99d9d32d5556f5b1801fb`  
		Last Modified: Thu, 02 Oct 2025 04:15:03 GMT  
		Size: 234.6 MB (234554394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422f93d4ddf037144c5ff55646da96edb70fcbe480727ab5db0cf9f354f151b4`  
		Last Modified: Thu, 02 Oct 2025 03:24:59 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049718d1ba3b4d745a0bc2b920733784f06924877edacfd6f1a37ff6c82df75d`  
		Last Modified: Thu, 02 Oct 2025 04:15:07 GMT  
		Size: 13.9 MB (13909087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b182e83f66e5dd1ab40d1e11b26995a81a1801d7aa847eb6a50ef18b37363d9`  
		Last Modified: Thu, 02 Oct 2025 04:15:03 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80bb68085d388e240aa2ad12f146313463b62fb070fc43d6190d310062d979d`  
		Last Modified: Thu, 02 Oct 2025 04:15:03 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca56c98fbdb06aa5382db810af8762f80fce32c030664a21307a2cd4b0898a86`  
		Last Modified: Thu, 02 Oct 2025 04:15:03 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:fc38214c8d984e2b0da08f5aa7e785c74d8e8b36e35d580dd95bc00790153ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5944547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ab0a2eb24500c2c7aac2f656252cad7136c53bc148472848d635dd17ba1790`

```dockerfile
```

-	Layers:
	-	`sha256:58de8c42bbe2c864253049f8bbc0d940918fc6ca71b4ceda478a34839825887e`  
		Last Modified: Thu, 02 Oct 2025 06:12:44 GMT  
		Size: 5.9 MB (5921578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaf9c1cac8de2308fbf42133e4517dd9781126c245376afebf82d5e267cd9d6f`  
		Last Modified: Thu, 02 Oct 2025 06:12:44 GMT  
		Size: 23.0 KB (22969 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:519216f2c26e4a6ec0937c5f7b963b0eba919208632102c89d85368dba624f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.3 MB (368322073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b712572d65858cb5e6c385a603ee9f1168fe78845ca160a72d45d1303113a00`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 08 Aug 2024 11:50:27 GMT
ARG RELEASE
# Thu, 08 Aug 2024 11:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 11:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 08 Aug 2024 11:50:27 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 11:50:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_MAJOR=9
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT []
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_FILE=geonetwork.war
# Thu, 08 Aug 2024 11:50:27 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Thu, 08 Aug 2024 11:50:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_VERSION=3.12.12
# Thu, 08 Aug 2024 11:50:27 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat/webapps
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
# Thu, 08 Aug 2024 11:50:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Aug 2024 11:50:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 08 Aug 2024 11:50:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3102a54c6b2b7ecf7a7216123f26003eec1ece4dbee7d4985813592023f98cd3`  
		Last Modified: Mon, 15 Sep 2025 22:13:52 GMT  
		Size: 18.8 MB (18814803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fbd3108988f496e4134a4862d953a8c993115aeccbb0a4057f7261d82396f3`  
		Last Modified: Mon, 15 Sep 2025 22:13:58 GMT  
		Size: 52.2 MB (52167313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67ce08f3159aea036fc5ac087e7103091b6388431976c3e34a6e95daa24b83d`  
		Last Modified: Mon, 15 Sep 2025 22:13:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbefdb3dada19d520a48d2cd4aaf1451c5e151919b1df3ee0bf25d3b0fac385`  
		Last Modified: Mon, 15 Sep 2025 22:13:51 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af087b3e0dccc7cdae8cdd274abc54dec7b15e61c2a1475ecfc6c9297674b7f0`  
		Last Modified: Tue, 16 Sep 2025 00:28:42 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358d701de1f162895b6f87b8496b0d7ead71378b25d6584ee754e5f826187519`  
		Last Modified: Tue, 16 Sep 2025 00:28:44 GMT  
		Size: 14.0 MB (14023884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c36ea3b4c50fd203f3c2b0da5f1e30aa7afb5677c533820911d63bdacca68fb`  
		Last Modified: Tue, 16 Sep 2025 02:14:19 GMT  
		Size: 234.6 MB (234574700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a680493fd4eaaee1dae63e060d5078672b4e0ba9bf14ff5c94e13b6b5354a23c`  
		Last Modified: Tue, 16 Sep 2025 02:06:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b7d653d188805c367b4ab4bb7cfeb8fa9b21aad24613194df6cbc018ca3269`  
		Last Modified: Tue, 16 Sep 2025 02:11:00 GMT  
		Size: 14.4 MB (14431881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ebaa000666aea8abefdf43440a01bf6cd99abbc1da3ed063eab15c051a2ed7`  
		Last Modified: Tue, 16 Sep 2025 02:10:58 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba86205687b8ddf753034b3ef200a9d51d5127042b97e6dfed3a302e260e4d1`  
		Last Modified: Tue, 16 Sep 2025 02:10:59 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d805ef473a5d69012fc9db8b6d38ada4d03601913e174358a14af032f7eb10`  
		Last Modified: Tue, 16 Sep 2025 02:10:59 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:510198cc6a6b030ef7cbb68dbfd6f98973f31ce402c86b74310ce9ca030f9d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0a5038f5b825eb7672a59c18a1e5d8748817ff0d0b0677b1b6ed50308a0b85`

```dockerfile
```

-	Layers:
	-	`sha256:0d4b7acca116c5c85ebb9cfccf7396d6d25f498c9ec137257e441be6e8421be9`  
		Last Modified: Tue, 16 Sep 2025 03:13:08 GMT  
		Size: 5.9 MB (5919870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18cbe6eecd4014ae52d5468b4466b207c1fad086222af2e714b412f43dbe3334`  
		Last Modified: Tue, 16 Sep 2025 03:13:09 GMT  
		Size: 22.9 KB (22902 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4`

```console
$ docker pull geonetwork@sha256:06fe6b18cb88d7d0ecf996bcc3c3ce71909c34535f3a22f65a9bcc701dbfc416
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:4` - linux; amd64

```console
$ docker pull geonetwork@sha256:14f4c37fd41e1df44ce3a5d01958642493bb0fc782c2fc59a351e2f8b17301bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.2 MB (394235037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0338873ce41c80654f7ee007bab0426dcd364a131b15c1d1a2d9b50b05377465`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 03 Jun 2025 10:28:37 GMT
ARG RELEASE
# Tue, 03 Jun 2025 10:28:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 10:28:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 10:28:37 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 10:28:37 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 10:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:28:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ddbd5d7ef14aa06784fb94d1e0e7177868dfdd0aa216a8a2e654869968ef7392';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='761a0a87ca2b1e75eb5208565a56a4c3f49e02a5d4c00ce6a4930d015660e5d1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='05b791574d7174d2c8e033c4c987411b167d2ff9b5e954926b82295310f93e4d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e3a2e957a06909ccff8eb81e892e952080905831cdcbe41825c041430e205e3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='e5a611a198a7c9f7bc16258f5357e80932de9a21751bd68960dd02a0949084b1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
WORKDIR /var/lib/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
USER jetty
# Tue, 03 Jun 2025 10:28:37 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 03 Jun 2025 10:28:37 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 03 Jun 2025 10:28:37 GMT
USER root
# Tue, 03 Jun 2025 10:28:37 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
USER jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_FILE=geonetwork.war
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_VERSION=4.4.8
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_DOWNLOAD_MD5=0e36d39ac451ca3f75b5271626ec8074
# Tue, 03 Jun 2025 10:28:37 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 03 Jun 2025 10:28:37 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202b6d722eed4ab5d2bfa3ba17d989bd8d7dc4a291c1209e2eb7ef260604281f`  
		Last Modified: Mon, 15 Sep 2025 22:12:58 GMT  
		Size: 17.0 MB (16971594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce5eb149e836d7d4430090f75d3d4bd794384e90dda677b729d5ac70afb1f2c`  
		Last Modified: Mon, 15 Sep 2025 22:13:36 GMT  
		Size: 47.2 MB (47234885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535ddd21308e15867ddc44e02fc5b6e35cb88a8e2417c12ec3bf48bbe02d4ec8`  
		Last Modified: Mon, 15 Sep 2025 22:13:33 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3861023d4c48e4065afc71a57eeffbcac94e91bf1d69cb2d54915b9e60c28e`  
		Last Modified: Mon, 15 Sep 2025 22:13:33 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a8ffa92d4ec47f6ec198f4efa9b8f2cc88f8acb82a3e35ebb4c0baf1700935`  
		Last Modified: Mon, 15 Sep 2025 23:15:55 GMT  
		Size: 10.4 MB (10364405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70f3ed43e3e70c0f1b3c693897cee7f7fe3f6997a39e9a0ed68cb594bd6b76b`  
		Last Modified: Mon, 15 Sep 2025 23:15:54 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befdb1c29114f77e5d59d9857f126c91141a432d94980d5d39a1f7bc4efcd128`  
		Last Modified: Tue, 16 Sep 2025 00:15:55 GMT  
		Size: 238.8 KB (238787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8897772089027280ac6298a82c119c4c79297b4d3968483c3dbc4d47370c4ad3`  
		Last Modified: Tue, 16 Sep 2025 03:38:19 GMT  
		Size: 289.7 MB (289696347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9670489202686236ba4f606a292b29370a70cee7c88241e444e8c2421465f538`  
		Last Modified: Tue, 16 Sep 2025 00:15:55 GMT  
		Size: 551.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fedd504ecffdf7085dd4db8731709a3e45acc7bf57a6d82abee338f692403f6`  
		Last Modified: Tue, 16 Sep 2025 00:15:55 GMT  
		Size: 568.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3e04be7365c34c497f31c494cd539737a75fc43208861ac83ab879a4519e94`  
		Last Modified: Tue, 16 Sep 2025 00:15:55 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:561d64151aef79e30047f5628d74b05649047daa4b56671144761fc1d8237689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f27daa75562651f8f2331a6b87e782f09555162e2d8707969db5d6c31172ab77`

```dockerfile
```

-	Layers:
	-	`sha256:ae5f325e38502485d46de8494a7935ddd51d9ed84d8aea675d96821573be2480`  
		Last Modified: Tue, 16 Sep 2025 03:13:06 GMT  
		Size: 4.2 MB (4213244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8c238cb776cc89a0f1ddca1cbeaa507e68f00234a57430fdd9445b7d1aec8db`  
		Last Modified: Tue, 16 Sep 2025 03:13:07 GMT  
		Size: 25.7 KB (25698 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:012c162bd18ee436f33e3bd17f5890f3e38ea0c0b3bf84b12b175eae19a92710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.0 MB (393962388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee5e66d206846256ef206d50bb5faeb605f7d4042ef0ae6a02e958df6e6e752`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 03 Jun 2025 10:28:37 GMT
ARG RELEASE
# Tue, 03 Jun 2025 10:28:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 10:28:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 10:28:37 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 10:28:37 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 10:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:28:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ddbd5d7ef14aa06784fb94d1e0e7177868dfdd0aa216a8a2e654869968ef7392';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='761a0a87ca2b1e75eb5208565a56a4c3f49e02a5d4c00ce6a4930d015660e5d1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='05b791574d7174d2c8e033c4c987411b167d2ff9b5e954926b82295310f93e4d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e3a2e957a06909ccff8eb81e892e952080905831cdcbe41825c041430e205e3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='e5a611a198a7c9f7bc16258f5357e80932de9a21751bd68960dd02a0949084b1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
WORKDIR /var/lib/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
USER jetty
# Tue, 03 Jun 2025 10:28:37 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 03 Jun 2025 10:28:37 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 03 Jun 2025 10:28:37 GMT
USER root
# Tue, 03 Jun 2025 10:28:37 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
USER jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_FILE=geonetwork.war
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_VERSION=4.4.8
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_DOWNLOAD_MD5=0e36d39ac451ca3f75b5271626ec8074
# Tue, 03 Jun 2025 10:28:37 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 03 Jun 2025 10:28:37 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7731212bf16a96e9cb24502ab375b27ada010043b25bf48d09e8b324370001e8`  
		Last Modified: Thu, 02 Oct 2025 01:17:28 GMT  
		Size: 19.2 MB (19206374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55762cbc95ee6f07f07f03fbb2cdb97df1629c2f9df3c6834b628117c453a907`  
		Last Modified: Thu, 02 Oct 2025 01:17:29 GMT  
		Size: 45.6 MB (45589778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed220bd0328f6ca80c2bca119afdc8f1af8e48b1490f7aa6ba403e2cda20ba5`  
		Last Modified: Thu, 02 Oct 2025 01:17:26 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709644d6a90ce830acdafadc19cca22af78d1a354f4572cdf9fce33f006eed51`  
		Last Modified: Thu, 02 Oct 2025 01:17:26 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70b18f62015d2f668fd8e4c0a64052a350365bac3cc8df650e2004d058800c9`  
		Last Modified: Thu, 02 Oct 2025 03:24:38 GMT  
		Size: 10.4 MB (10364710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d4218282b53cef890af53cfb8f6262f43b3ffeb187cd391a56561dcaef9b60`  
		Last Modified: Thu, 02 Oct 2025 03:24:37 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21b387850edccdf7364680f57f0e8b20812cc6500d916d4067490a1a343dd3c`  
		Last Modified: Thu, 02 Oct 2025 04:20:42 GMT  
		Size: 238.0 KB (238033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce5ae6009fd11533f11c1fe43bec513e05bd7e3e766a7e31345d01a8c584b7e`  
		Last Modified: Thu, 02 Oct 2025 11:01:05 GMT  
		Size: 289.7 MB (289696344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44f4973c0ec7ebf87996e6d3afc79a69f159ef5cc0eda547488e32cd076660d`  
		Last Modified: Thu, 02 Oct 2025 04:20:41 GMT  
		Size: 552.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6dc92b2fea399a70cd408bcecdb0a32a508d769204df39aaa336ddd3ec9080`  
		Last Modified: Thu, 02 Oct 2025 04:20:41 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a604142bd6fc1b3d0cbf7eaff7209cccf1f5af6cc8b1c3096fbc444e8f91f88`  
		Last Modified: Thu, 02 Oct 2025 04:20:41 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:3563e5a9b3da739ea982afc8e2155075bc4d7042032a81d812c093a06efbd9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651ba0ed744e3bb394f43f141009baea7d472bb49bbdbb3a7b13adc453ab6ab1`

```dockerfile
```

-	Layers:
	-	`sha256:0041b647a3cad450933480f74d9a9d5d1fafc06e12d8b7b7832528ac13c31ca4`  
		Last Modified: Thu, 02 Oct 2025 06:12:53 GMT  
		Size: 4.2 MB (4214329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b315e7de7c93c7c053f0c1651338c7435c96a6d96a22745a0d2681068dd169a`  
		Last Modified: Thu, 02 Oct 2025 06:12:54 GMT  
		Size: 25.8 KB (25832 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.2`

```console
$ docker pull geonetwork@sha256:bc983b55df721d6da8da489d910380df46267ca28e399e03998fe85395b7e0a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:4.2` - linux; amd64

```console
$ docker pull geonetwork@sha256:4e20d50b934aad7d5f03dbe5440040909456e2df9f8af1776fed0dde9001d892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.6 MB (363585200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383acbd62650cb3a9f12c2064d4b59d8742f1a06057e1ebea472cc3fd362dceb`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 03 Jun 2025 10:28:37 GMT
ARG RELEASE
# Tue, 03 Jun 2025 10:28:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 10:28:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 10:28:37 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 10:28:37 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 10:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:28:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6e83ffc37da053352ccaa2fd3bd7d813b9674d87aa01b35ac3e54903cd33b0d8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='c34506736ab52768c59660a5d4246b94f57543c79b7e4b53d322dda3ec4a9302';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='48547114cef3ce1ab8e80c8140430d8fb2f23359d52ad6d7a0af28f5fe9c81f8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='15391b2d1bf613abd739f6ad6eeb728f4803d901cceae0d83f6bbd00da7751bf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
WORKDIR /var/lib/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
USER jetty
# Tue, 03 Jun 2025 10:28:37 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom         -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Tue, 03 Jun 2025 10:28:37 GMT
USER root
# Tue, 03 Jun 2025 10:28:37 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
USER jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_FILE=geonetwork.war
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_VERSION=4.2.13
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_DOWNLOAD_MD5=2d75699a23192b4b1a81b90e346caea4
# Tue, 03 Jun 2025 10:28:37 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 03 Jun 2025 10:28:37 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202b6d722eed4ab5d2bfa3ba17d989bd8d7dc4a291c1209e2eb7ef260604281f`  
		Last Modified: Mon, 15 Sep 2025 22:12:58 GMT  
		Size: 17.0 MB (16971594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d178208e0a66813e04b64140b58feaa80374f7eb14cd99c1d071bdefc6fe782c`  
		Last Modified: Mon, 15 Sep 2025 22:13:01 GMT  
		Size: 41.9 MB (41878392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4666affe668460e4a397b5422be9f6bcb8d26280ce8436c066c26b8c2974d25`  
		Last Modified: Mon, 15 Sep 2025 22:12:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afdc05c4356999ee157d23190905a4036a9c537863ec25ac74c0e20874bdc45`  
		Last Modified: Mon, 15 Sep 2025 22:12:57 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7d80620558a237424e562b4187676b3911984d478142f13997529bd2399a69`  
		Last Modified: Tue, 16 Sep 2025 00:14:42 GMT  
		Size: 10.4 MB (10364383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c0942e4f329d80476012520c809f299f227d20ad8dd4f2237370f288353073`  
		Last Modified: Mon, 15 Sep 2025 23:15:36 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d34c16bcbe3d23b88c83f3cf0380ce6dcee29ffd579b99ceb204c075b248244`  
		Last Modified: Tue, 16 Sep 2025 00:15:52 GMT  
		Size: 238.9 KB (238852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c9bd4d953b4051a0e508deb8f9c42f52afdf89ca1d773c44d4cc685b172051`  
		Last Modified: Tue, 16 Sep 2025 01:14:06 GMT  
		Size: 264.4 MB (264403279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4870430769e93da77bee9868a16b1f16d33e0d397f95bedcf32a2be4470545c2`  
		Last Modified: Tue, 16 Sep 2025 00:15:52 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2` - unknown; unknown

```console
$ docker pull geonetwork@sha256:a0bf6cb9bd0f1d1b412a27653bf1a12b8e50bd1a60d1946e487ebe677a9c3fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81d08a5ed1809d85edd3d9023d64781199cca89e4a2cb95713c471169be7c2b`

```dockerfile
```

-	Layers:
	-	`sha256:20cb4cc7b2a89147c747f58529150baa7c245defc455976d4bc7c096f7c869b0`  
		Last Modified: Tue, 16 Sep 2025 03:13:16 GMT  
		Size: 4.2 MB (4209793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e7d15e295b3186d65492ad5a2ed4aa3d76a288910697a8e51c0695620bae8b3`  
		Last Modified: Tue, 16 Sep 2025 03:13:17 GMT  
		Size: 18.7 KB (18739 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.2` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:81eb6b725323299b86499e0efc9cf7986ef1b0cf47308a2e6572e6300e6d7e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.0 MB (363959321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebee9bd3156dfe280d25fb5575108f6da01986bef93c92a872242712c8d566c`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 03 Jun 2025 10:28:37 GMT
ARG RELEASE
# Tue, 03 Jun 2025 10:28:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 10:28:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 10:28:37 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 10:28:37 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 10:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:28:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6e83ffc37da053352ccaa2fd3bd7d813b9674d87aa01b35ac3e54903cd33b0d8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='c34506736ab52768c59660a5d4246b94f57543c79b7e4b53d322dda3ec4a9302';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='48547114cef3ce1ab8e80c8140430d8fb2f23359d52ad6d7a0af28f5fe9c81f8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='15391b2d1bf613abd739f6ad6eeb728f4803d901cceae0d83f6bbd00da7751bf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
WORKDIR /var/lib/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
USER jetty
# Tue, 03 Jun 2025 10:28:37 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom         -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Tue, 03 Jun 2025 10:28:37 GMT
USER root
# Tue, 03 Jun 2025 10:28:37 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
USER jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_FILE=geonetwork.war
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_VERSION=4.2.13
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_DOWNLOAD_MD5=2d75699a23192b4b1a81b90e346caea4
# Tue, 03 Jun 2025 10:28:37 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 03 Jun 2025 10:28:37 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d713d9f39663d7803c802171de8a663ea6fdff2423b056951976cb86e10f4216`  
		Last Modified: Thu, 02 Oct 2025 01:17:06 GMT  
		Size: 19.2 MB (19206399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b3ab79b8c7bf00d47fadbb7f1e0942a7696c3b95236a2f7c74f71e75bd292c`  
		Last Modified: Thu, 02 Oct 2025 01:17:22 GMT  
		Size: 40.9 MB (40880052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12940e96e665f92ef75cca9e1dae2fc33f62da9f85df9d10b4196c8665409dd9`  
		Last Modified: Thu, 02 Oct 2025 01:17:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2accb1c47183434b3da35f5c777564d1fab2c1f35c5fa4736802568cd072dddd`  
		Last Modified: Thu, 02 Oct 2025 01:17:01 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd65492b14858e55567a9804301df1585b4ebfcb52b0f19da7b3fc40b3160fc3`  
		Last Modified: Thu, 02 Oct 2025 03:23:54 GMT  
		Size: 10.4 MB (10364723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637314682e031cf02a46781a51ef1293630df06c58f67cf7f958f19d7d616843`  
		Last Modified: Thu, 02 Oct 2025 03:23:53 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce66da3116306108c8dc2f362745c88297349636cbc6fce1754ef3159a9e6c52`  
		Last Modified: Thu, 02 Oct 2025 03:25:00 GMT  
		Size: 238.1 KB (238113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6267638dc4b07810c1b954e5d1f2194c2c73a32ebd81dcbd3b51d7b1d7f7efcb`  
		Last Modified: Thu, 02 Oct 2025 03:24:42 GMT  
		Size: 264.4 MB (264403206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7eebe2db69ae7099ed7c4ca84ca78516567c95e5179a4d486266e0fa95604d1`  
		Last Modified: Thu, 02 Oct 2025 03:25:00 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2` - unknown; unknown

```console
$ docker pull geonetwork@sha256:7642074be86a5fdbc275218132a138769e4c6578aac5cd09355773ec147e7a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4229769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fabe0d5232d826c67f383edebf49891ae0624495eb80db8a4fbd02e6c37dbb4`

```dockerfile
```

-	Layers:
	-	`sha256:b5868e3e786fd700f1b74d2e8675be1798369d0ac2a4017d8a9faa7d7c3a8d07`  
		Last Modified: Thu, 02 Oct 2025 06:13:00 GMT  
		Size: 4.2 MB (4210934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bd64393f9238847c3ecc8e0150dc5d05989c6fe1643a5536b54a411bc127cd3`  
		Last Modified: Thu, 02 Oct 2025 06:13:01 GMT  
		Size: 18.8 KB (18835 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.2.13`

```console
$ docker pull geonetwork@sha256:bc983b55df721d6da8da489d910380df46267ca28e399e03998fe85395b7e0a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:4.2.13` - linux; amd64

```console
$ docker pull geonetwork@sha256:4e20d50b934aad7d5f03dbe5440040909456e2df9f8af1776fed0dde9001d892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.6 MB (363585200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383acbd62650cb3a9f12c2064d4b59d8742f1a06057e1ebea472cc3fd362dceb`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 03 Jun 2025 10:28:37 GMT
ARG RELEASE
# Tue, 03 Jun 2025 10:28:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 10:28:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 10:28:37 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 10:28:37 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 10:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:28:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6e83ffc37da053352ccaa2fd3bd7d813b9674d87aa01b35ac3e54903cd33b0d8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='c34506736ab52768c59660a5d4246b94f57543c79b7e4b53d322dda3ec4a9302';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='48547114cef3ce1ab8e80c8140430d8fb2f23359d52ad6d7a0af28f5fe9c81f8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='15391b2d1bf613abd739f6ad6eeb728f4803d901cceae0d83f6bbd00da7751bf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
WORKDIR /var/lib/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
USER jetty
# Tue, 03 Jun 2025 10:28:37 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom         -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Tue, 03 Jun 2025 10:28:37 GMT
USER root
# Tue, 03 Jun 2025 10:28:37 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
USER jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_FILE=geonetwork.war
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_VERSION=4.2.13
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_DOWNLOAD_MD5=2d75699a23192b4b1a81b90e346caea4
# Tue, 03 Jun 2025 10:28:37 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 03 Jun 2025 10:28:37 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202b6d722eed4ab5d2bfa3ba17d989bd8d7dc4a291c1209e2eb7ef260604281f`  
		Last Modified: Mon, 15 Sep 2025 22:12:58 GMT  
		Size: 17.0 MB (16971594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d178208e0a66813e04b64140b58feaa80374f7eb14cd99c1d071bdefc6fe782c`  
		Last Modified: Mon, 15 Sep 2025 22:13:01 GMT  
		Size: 41.9 MB (41878392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4666affe668460e4a397b5422be9f6bcb8d26280ce8436c066c26b8c2974d25`  
		Last Modified: Mon, 15 Sep 2025 22:12:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afdc05c4356999ee157d23190905a4036a9c537863ec25ac74c0e20874bdc45`  
		Last Modified: Mon, 15 Sep 2025 22:12:57 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7d80620558a237424e562b4187676b3911984d478142f13997529bd2399a69`  
		Last Modified: Tue, 16 Sep 2025 00:14:42 GMT  
		Size: 10.4 MB (10364383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c0942e4f329d80476012520c809f299f227d20ad8dd4f2237370f288353073`  
		Last Modified: Mon, 15 Sep 2025 23:15:36 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d34c16bcbe3d23b88c83f3cf0380ce6dcee29ffd579b99ceb204c075b248244`  
		Last Modified: Tue, 16 Sep 2025 00:15:52 GMT  
		Size: 238.9 KB (238852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c9bd4d953b4051a0e508deb8f9c42f52afdf89ca1d773c44d4cc685b172051`  
		Last Modified: Tue, 16 Sep 2025 01:14:06 GMT  
		Size: 264.4 MB (264403279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4870430769e93da77bee9868a16b1f16d33e0d397f95bedcf32a2be4470545c2`  
		Last Modified: Tue, 16 Sep 2025 00:15:52 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2.13` - unknown; unknown

```console
$ docker pull geonetwork@sha256:a0bf6cb9bd0f1d1b412a27653bf1a12b8e50bd1a60d1946e487ebe677a9c3fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81d08a5ed1809d85edd3d9023d64781199cca89e4a2cb95713c471169be7c2b`

```dockerfile
```

-	Layers:
	-	`sha256:20cb4cc7b2a89147c747f58529150baa7c245defc455976d4bc7c096f7c869b0`  
		Last Modified: Tue, 16 Sep 2025 03:13:16 GMT  
		Size: 4.2 MB (4209793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e7d15e295b3186d65492ad5a2ed4aa3d76a288910697a8e51c0695620bae8b3`  
		Last Modified: Tue, 16 Sep 2025 03:13:17 GMT  
		Size: 18.7 KB (18739 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.2.13` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:81eb6b725323299b86499e0efc9cf7986ef1b0cf47308a2e6572e6300e6d7e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.0 MB (363959321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebee9bd3156dfe280d25fb5575108f6da01986bef93c92a872242712c8d566c`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 03 Jun 2025 10:28:37 GMT
ARG RELEASE
# Tue, 03 Jun 2025 10:28:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 10:28:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 10:28:37 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 10:28:37 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 10:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:28:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6e83ffc37da053352ccaa2fd3bd7d813b9674d87aa01b35ac3e54903cd33b0d8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='c34506736ab52768c59660a5d4246b94f57543c79b7e4b53d322dda3ec4a9302';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='48547114cef3ce1ab8e80c8140430d8fb2f23359d52ad6d7a0af28f5fe9c81f8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='15391b2d1bf613abd739f6ad6eeb728f4803d901cceae0d83f6bbd00da7751bf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
WORKDIR /var/lib/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
USER jetty
# Tue, 03 Jun 2025 10:28:37 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom         -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Tue, 03 Jun 2025 10:28:37 GMT
USER root
# Tue, 03 Jun 2025 10:28:37 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
USER jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_FILE=geonetwork.war
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_VERSION=4.2.13
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_DOWNLOAD_MD5=2d75699a23192b4b1a81b90e346caea4
# Tue, 03 Jun 2025 10:28:37 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 03 Jun 2025 10:28:37 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d713d9f39663d7803c802171de8a663ea6fdff2423b056951976cb86e10f4216`  
		Last Modified: Thu, 02 Oct 2025 01:17:06 GMT  
		Size: 19.2 MB (19206399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b3ab79b8c7bf00d47fadbb7f1e0942a7696c3b95236a2f7c74f71e75bd292c`  
		Last Modified: Thu, 02 Oct 2025 01:17:22 GMT  
		Size: 40.9 MB (40880052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12940e96e665f92ef75cca9e1dae2fc33f62da9f85df9d10b4196c8665409dd9`  
		Last Modified: Thu, 02 Oct 2025 01:17:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2accb1c47183434b3da35f5c777564d1fab2c1f35c5fa4736802568cd072dddd`  
		Last Modified: Thu, 02 Oct 2025 01:17:01 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd65492b14858e55567a9804301df1585b4ebfcb52b0f19da7b3fc40b3160fc3`  
		Last Modified: Thu, 02 Oct 2025 03:23:54 GMT  
		Size: 10.4 MB (10364723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637314682e031cf02a46781a51ef1293630df06c58f67cf7f958f19d7d616843`  
		Last Modified: Thu, 02 Oct 2025 03:23:53 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce66da3116306108c8dc2f362745c88297349636cbc6fce1754ef3159a9e6c52`  
		Last Modified: Thu, 02 Oct 2025 03:25:00 GMT  
		Size: 238.1 KB (238113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6267638dc4b07810c1b954e5d1f2194c2c73a32ebd81dcbd3b51d7b1d7f7efcb`  
		Last Modified: Thu, 02 Oct 2025 03:24:42 GMT  
		Size: 264.4 MB (264403206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7eebe2db69ae7099ed7c4ca84ca78516567c95e5179a4d486266e0fa95604d1`  
		Last Modified: Thu, 02 Oct 2025 03:25:00 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2.13` - unknown; unknown

```console
$ docker pull geonetwork@sha256:7642074be86a5fdbc275218132a138769e4c6578aac5cd09355773ec147e7a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4229769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fabe0d5232d826c67f383edebf49891ae0624495eb80db8a4fbd02e6c37dbb4`

```dockerfile
```

-	Layers:
	-	`sha256:b5868e3e786fd700f1b74d2e8675be1798369d0ac2a4017d8a9faa7d7c3a8d07`  
		Last Modified: Thu, 02 Oct 2025 06:13:00 GMT  
		Size: 4.2 MB (4210934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bd64393f9238847c3ecc8e0150dc5d05989c6fe1643a5536b54a411bc127cd3`  
		Last Modified: Thu, 02 Oct 2025 06:13:01 GMT  
		Size: 18.8 KB (18835 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.4`

```console
$ docker pull geonetwork@sha256:06fe6b18cb88d7d0ecf996bcc3c3ce71909c34535f3a22f65a9bcc701dbfc416
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:4.4` - linux; amd64

```console
$ docker pull geonetwork@sha256:14f4c37fd41e1df44ce3a5d01958642493bb0fc782c2fc59a351e2f8b17301bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.2 MB (394235037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0338873ce41c80654f7ee007bab0426dcd364a131b15c1d1a2d9b50b05377465`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 03 Jun 2025 10:28:37 GMT
ARG RELEASE
# Tue, 03 Jun 2025 10:28:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 10:28:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 10:28:37 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 10:28:37 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 10:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:28:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ddbd5d7ef14aa06784fb94d1e0e7177868dfdd0aa216a8a2e654869968ef7392';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='761a0a87ca2b1e75eb5208565a56a4c3f49e02a5d4c00ce6a4930d015660e5d1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='05b791574d7174d2c8e033c4c987411b167d2ff9b5e954926b82295310f93e4d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e3a2e957a06909ccff8eb81e892e952080905831cdcbe41825c041430e205e3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='e5a611a198a7c9f7bc16258f5357e80932de9a21751bd68960dd02a0949084b1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
WORKDIR /var/lib/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
USER jetty
# Tue, 03 Jun 2025 10:28:37 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 03 Jun 2025 10:28:37 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 03 Jun 2025 10:28:37 GMT
USER root
# Tue, 03 Jun 2025 10:28:37 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
USER jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_FILE=geonetwork.war
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_VERSION=4.4.8
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_DOWNLOAD_MD5=0e36d39ac451ca3f75b5271626ec8074
# Tue, 03 Jun 2025 10:28:37 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 03 Jun 2025 10:28:37 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202b6d722eed4ab5d2bfa3ba17d989bd8d7dc4a291c1209e2eb7ef260604281f`  
		Last Modified: Mon, 15 Sep 2025 22:12:58 GMT  
		Size: 17.0 MB (16971594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce5eb149e836d7d4430090f75d3d4bd794384e90dda677b729d5ac70afb1f2c`  
		Last Modified: Mon, 15 Sep 2025 22:13:36 GMT  
		Size: 47.2 MB (47234885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535ddd21308e15867ddc44e02fc5b6e35cb88a8e2417c12ec3bf48bbe02d4ec8`  
		Last Modified: Mon, 15 Sep 2025 22:13:33 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3861023d4c48e4065afc71a57eeffbcac94e91bf1d69cb2d54915b9e60c28e`  
		Last Modified: Mon, 15 Sep 2025 22:13:33 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a8ffa92d4ec47f6ec198f4efa9b8f2cc88f8acb82a3e35ebb4c0baf1700935`  
		Last Modified: Mon, 15 Sep 2025 23:15:55 GMT  
		Size: 10.4 MB (10364405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70f3ed43e3e70c0f1b3c693897cee7f7fe3f6997a39e9a0ed68cb594bd6b76b`  
		Last Modified: Mon, 15 Sep 2025 23:15:54 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befdb1c29114f77e5d59d9857f126c91141a432d94980d5d39a1f7bc4efcd128`  
		Last Modified: Tue, 16 Sep 2025 00:15:55 GMT  
		Size: 238.8 KB (238787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8897772089027280ac6298a82c119c4c79297b4d3968483c3dbc4d47370c4ad3`  
		Last Modified: Tue, 16 Sep 2025 03:38:19 GMT  
		Size: 289.7 MB (289696347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9670489202686236ba4f606a292b29370a70cee7c88241e444e8c2421465f538`  
		Last Modified: Tue, 16 Sep 2025 00:15:55 GMT  
		Size: 551.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fedd504ecffdf7085dd4db8731709a3e45acc7bf57a6d82abee338f692403f6`  
		Last Modified: Tue, 16 Sep 2025 00:15:55 GMT  
		Size: 568.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3e04be7365c34c497f31c494cd539737a75fc43208861ac83ab879a4519e94`  
		Last Modified: Tue, 16 Sep 2025 00:15:55 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:561d64151aef79e30047f5628d74b05649047daa4b56671144761fc1d8237689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f27daa75562651f8f2331a6b87e782f09555162e2d8707969db5d6c31172ab77`

```dockerfile
```

-	Layers:
	-	`sha256:ae5f325e38502485d46de8494a7935ddd51d9ed84d8aea675d96821573be2480`  
		Last Modified: Tue, 16 Sep 2025 03:13:06 GMT  
		Size: 4.2 MB (4213244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8c238cb776cc89a0f1ddca1cbeaa507e68f00234a57430fdd9445b7d1aec8db`  
		Last Modified: Tue, 16 Sep 2025 03:13:07 GMT  
		Size: 25.7 KB (25698 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:012c162bd18ee436f33e3bd17f5890f3e38ea0c0b3bf84b12b175eae19a92710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.0 MB (393962388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee5e66d206846256ef206d50bb5faeb605f7d4042ef0ae6a02e958df6e6e752`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 03 Jun 2025 10:28:37 GMT
ARG RELEASE
# Tue, 03 Jun 2025 10:28:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 10:28:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 10:28:37 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 10:28:37 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 10:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:28:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ddbd5d7ef14aa06784fb94d1e0e7177868dfdd0aa216a8a2e654869968ef7392';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='761a0a87ca2b1e75eb5208565a56a4c3f49e02a5d4c00ce6a4930d015660e5d1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='05b791574d7174d2c8e033c4c987411b167d2ff9b5e954926b82295310f93e4d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e3a2e957a06909ccff8eb81e892e952080905831cdcbe41825c041430e205e3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='e5a611a198a7c9f7bc16258f5357e80932de9a21751bd68960dd02a0949084b1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
WORKDIR /var/lib/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
USER jetty
# Tue, 03 Jun 2025 10:28:37 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 03 Jun 2025 10:28:37 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 03 Jun 2025 10:28:37 GMT
USER root
# Tue, 03 Jun 2025 10:28:37 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
USER jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_FILE=geonetwork.war
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_VERSION=4.4.8
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_DOWNLOAD_MD5=0e36d39ac451ca3f75b5271626ec8074
# Tue, 03 Jun 2025 10:28:37 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 03 Jun 2025 10:28:37 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7731212bf16a96e9cb24502ab375b27ada010043b25bf48d09e8b324370001e8`  
		Last Modified: Thu, 02 Oct 2025 01:17:28 GMT  
		Size: 19.2 MB (19206374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55762cbc95ee6f07f07f03fbb2cdb97df1629c2f9df3c6834b628117c453a907`  
		Last Modified: Thu, 02 Oct 2025 01:17:29 GMT  
		Size: 45.6 MB (45589778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed220bd0328f6ca80c2bca119afdc8f1af8e48b1490f7aa6ba403e2cda20ba5`  
		Last Modified: Thu, 02 Oct 2025 01:17:26 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709644d6a90ce830acdafadc19cca22af78d1a354f4572cdf9fce33f006eed51`  
		Last Modified: Thu, 02 Oct 2025 01:17:26 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70b18f62015d2f668fd8e4c0a64052a350365bac3cc8df650e2004d058800c9`  
		Last Modified: Thu, 02 Oct 2025 03:24:38 GMT  
		Size: 10.4 MB (10364710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d4218282b53cef890af53cfb8f6262f43b3ffeb187cd391a56561dcaef9b60`  
		Last Modified: Thu, 02 Oct 2025 03:24:37 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21b387850edccdf7364680f57f0e8b20812cc6500d916d4067490a1a343dd3c`  
		Last Modified: Thu, 02 Oct 2025 04:20:42 GMT  
		Size: 238.0 KB (238033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce5ae6009fd11533f11c1fe43bec513e05bd7e3e766a7e31345d01a8c584b7e`  
		Last Modified: Thu, 02 Oct 2025 11:01:05 GMT  
		Size: 289.7 MB (289696344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44f4973c0ec7ebf87996e6d3afc79a69f159ef5cc0eda547488e32cd076660d`  
		Last Modified: Thu, 02 Oct 2025 04:20:41 GMT  
		Size: 552.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6dc92b2fea399a70cd408bcecdb0a32a508d769204df39aaa336ddd3ec9080`  
		Last Modified: Thu, 02 Oct 2025 04:20:41 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a604142bd6fc1b3d0cbf7eaff7209cccf1f5af6cc8b1c3096fbc444e8f91f88`  
		Last Modified: Thu, 02 Oct 2025 04:20:41 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:3563e5a9b3da739ea982afc8e2155075bc4d7042032a81d812c093a06efbd9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651ba0ed744e3bb394f43f141009baea7d472bb49bbdbb3a7b13adc453ab6ab1`

```dockerfile
```

-	Layers:
	-	`sha256:0041b647a3cad450933480f74d9a9d5d1fafc06e12d8b7b7832528ac13c31ca4`  
		Last Modified: Thu, 02 Oct 2025 06:12:53 GMT  
		Size: 4.2 MB (4214329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b315e7de7c93c7c053f0c1651338c7435c96a6d96a22745a0d2681068dd169a`  
		Last Modified: Thu, 02 Oct 2025 06:12:54 GMT  
		Size: 25.8 KB (25832 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.4.8`

```console
$ docker pull geonetwork@sha256:06fe6b18cb88d7d0ecf996bcc3c3ce71909c34535f3a22f65a9bcc701dbfc416
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:4.4.8` - linux; amd64

```console
$ docker pull geonetwork@sha256:14f4c37fd41e1df44ce3a5d01958642493bb0fc782c2fc59a351e2f8b17301bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.2 MB (394235037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0338873ce41c80654f7ee007bab0426dcd364a131b15c1d1a2d9b50b05377465`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 03 Jun 2025 10:28:37 GMT
ARG RELEASE
# Tue, 03 Jun 2025 10:28:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 10:28:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 10:28:37 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 10:28:37 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 10:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:28:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ddbd5d7ef14aa06784fb94d1e0e7177868dfdd0aa216a8a2e654869968ef7392';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='761a0a87ca2b1e75eb5208565a56a4c3f49e02a5d4c00ce6a4930d015660e5d1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='05b791574d7174d2c8e033c4c987411b167d2ff9b5e954926b82295310f93e4d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e3a2e957a06909ccff8eb81e892e952080905831cdcbe41825c041430e205e3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='e5a611a198a7c9f7bc16258f5357e80932de9a21751bd68960dd02a0949084b1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
WORKDIR /var/lib/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
USER jetty
# Tue, 03 Jun 2025 10:28:37 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 03 Jun 2025 10:28:37 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 03 Jun 2025 10:28:37 GMT
USER root
# Tue, 03 Jun 2025 10:28:37 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
USER jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_FILE=geonetwork.war
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_VERSION=4.4.8
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_DOWNLOAD_MD5=0e36d39ac451ca3f75b5271626ec8074
# Tue, 03 Jun 2025 10:28:37 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 03 Jun 2025 10:28:37 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202b6d722eed4ab5d2bfa3ba17d989bd8d7dc4a291c1209e2eb7ef260604281f`  
		Last Modified: Mon, 15 Sep 2025 22:12:58 GMT  
		Size: 17.0 MB (16971594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce5eb149e836d7d4430090f75d3d4bd794384e90dda677b729d5ac70afb1f2c`  
		Last Modified: Mon, 15 Sep 2025 22:13:36 GMT  
		Size: 47.2 MB (47234885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535ddd21308e15867ddc44e02fc5b6e35cb88a8e2417c12ec3bf48bbe02d4ec8`  
		Last Modified: Mon, 15 Sep 2025 22:13:33 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3861023d4c48e4065afc71a57eeffbcac94e91bf1d69cb2d54915b9e60c28e`  
		Last Modified: Mon, 15 Sep 2025 22:13:33 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a8ffa92d4ec47f6ec198f4efa9b8f2cc88f8acb82a3e35ebb4c0baf1700935`  
		Last Modified: Mon, 15 Sep 2025 23:15:55 GMT  
		Size: 10.4 MB (10364405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70f3ed43e3e70c0f1b3c693897cee7f7fe3f6997a39e9a0ed68cb594bd6b76b`  
		Last Modified: Mon, 15 Sep 2025 23:15:54 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befdb1c29114f77e5d59d9857f126c91141a432d94980d5d39a1f7bc4efcd128`  
		Last Modified: Tue, 16 Sep 2025 00:15:55 GMT  
		Size: 238.8 KB (238787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8897772089027280ac6298a82c119c4c79297b4d3968483c3dbc4d47370c4ad3`  
		Last Modified: Tue, 16 Sep 2025 03:38:19 GMT  
		Size: 289.7 MB (289696347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9670489202686236ba4f606a292b29370a70cee7c88241e444e8c2421465f538`  
		Last Modified: Tue, 16 Sep 2025 00:15:55 GMT  
		Size: 551.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fedd504ecffdf7085dd4db8731709a3e45acc7bf57a6d82abee338f692403f6`  
		Last Modified: Tue, 16 Sep 2025 00:15:55 GMT  
		Size: 568.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3e04be7365c34c497f31c494cd539737a75fc43208861ac83ab879a4519e94`  
		Last Modified: Tue, 16 Sep 2025 00:15:55 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4.8` - unknown; unknown

```console
$ docker pull geonetwork@sha256:561d64151aef79e30047f5628d74b05649047daa4b56671144761fc1d8237689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f27daa75562651f8f2331a6b87e782f09555162e2d8707969db5d6c31172ab77`

```dockerfile
```

-	Layers:
	-	`sha256:ae5f325e38502485d46de8494a7935ddd51d9ed84d8aea675d96821573be2480`  
		Last Modified: Tue, 16 Sep 2025 03:13:06 GMT  
		Size: 4.2 MB (4213244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8c238cb776cc89a0f1ddca1cbeaa507e68f00234a57430fdd9445b7d1aec8db`  
		Last Modified: Tue, 16 Sep 2025 03:13:07 GMT  
		Size: 25.7 KB (25698 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4.8` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:012c162bd18ee436f33e3bd17f5890f3e38ea0c0b3bf84b12b175eae19a92710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.0 MB (393962388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee5e66d206846256ef206d50bb5faeb605f7d4042ef0ae6a02e958df6e6e752`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 03 Jun 2025 10:28:37 GMT
ARG RELEASE
# Tue, 03 Jun 2025 10:28:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 10:28:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 10:28:37 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 10:28:37 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 10:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:28:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ddbd5d7ef14aa06784fb94d1e0e7177868dfdd0aa216a8a2e654869968ef7392';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='761a0a87ca2b1e75eb5208565a56a4c3f49e02a5d4c00ce6a4930d015660e5d1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='05b791574d7174d2c8e033c4c987411b167d2ff9b5e954926b82295310f93e4d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e3a2e957a06909ccff8eb81e892e952080905831cdcbe41825c041430e205e3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='e5a611a198a7c9f7bc16258f5357e80932de9a21751bd68960dd02a0949084b1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
WORKDIR /var/lib/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
USER jetty
# Tue, 03 Jun 2025 10:28:37 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 03 Jun 2025 10:28:37 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 03 Jun 2025 10:28:37 GMT
USER root
# Tue, 03 Jun 2025 10:28:37 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
USER jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_FILE=geonetwork.war
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_VERSION=4.4.8
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_DOWNLOAD_MD5=0e36d39ac451ca3f75b5271626ec8074
# Tue, 03 Jun 2025 10:28:37 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 03 Jun 2025 10:28:37 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7731212bf16a96e9cb24502ab375b27ada010043b25bf48d09e8b324370001e8`  
		Last Modified: Thu, 02 Oct 2025 01:17:28 GMT  
		Size: 19.2 MB (19206374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55762cbc95ee6f07f07f03fbb2cdb97df1629c2f9df3c6834b628117c453a907`  
		Last Modified: Thu, 02 Oct 2025 01:17:29 GMT  
		Size: 45.6 MB (45589778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed220bd0328f6ca80c2bca119afdc8f1af8e48b1490f7aa6ba403e2cda20ba5`  
		Last Modified: Thu, 02 Oct 2025 01:17:26 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709644d6a90ce830acdafadc19cca22af78d1a354f4572cdf9fce33f006eed51`  
		Last Modified: Thu, 02 Oct 2025 01:17:26 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70b18f62015d2f668fd8e4c0a64052a350365bac3cc8df650e2004d058800c9`  
		Last Modified: Thu, 02 Oct 2025 03:24:38 GMT  
		Size: 10.4 MB (10364710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d4218282b53cef890af53cfb8f6262f43b3ffeb187cd391a56561dcaef9b60`  
		Last Modified: Thu, 02 Oct 2025 03:24:37 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21b387850edccdf7364680f57f0e8b20812cc6500d916d4067490a1a343dd3c`  
		Last Modified: Thu, 02 Oct 2025 04:20:42 GMT  
		Size: 238.0 KB (238033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce5ae6009fd11533f11c1fe43bec513e05bd7e3e766a7e31345d01a8c584b7e`  
		Last Modified: Thu, 02 Oct 2025 11:01:05 GMT  
		Size: 289.7 MB (289696344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44f4973c0ec7ebf87996e6d3afc79a69f159ef5cc0eda547488e32cd076660d`  
		Last Modified: Thu, 02 Oct 2025 04:20:41 GMT  
		Size: 552.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6dc92b2fea399a70cd408bcecdb0a32a508d769204df39aaa336ddd3ec9080`  
		Last Modified: Thu, 02 Oct 2025 04:20:41 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a604142bd6fc1b3d0cbf7eaff7209cccf1f5af6cc8b1c3096fbc444e8f91f88`  
		Last Modified: Thu, 02 Oct 2025 04:20:41 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4.8` - unknown; unknown

```console
$ docker pull geonetwork@sha256:3563e5a9b3da739ea982afc8e2155075bc4d7042032a81d812c093a06efbd9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651ba0ed744e3bb394f43f141009baea7d472bb49bbdbb3a7b13adc453ab6ab1`

```dockerfile
```

-	Layers:
	-	`sha256:0041b647a3cad450933480f74d9a9d5d1fafc06e12d8b7b7832528ac13c31ca4`  
		Last Modified: Thu, 02 Oct 2025 06:12:53 GMT  
		Size: 4.2 MB (4214329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b315e7de7c93c7c053f0c1651338c7435c96a6d96a22745a0d2681068dd169a`  
		Last Modified: Thu, 02 Oct 2025 06:12:54 GMT  
		Size: 25.8 KB (25832 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:latest`

```console
$ docker pull geonetwork@sha256:06fe6b18cb88d7d0ecf996bcc3c3ce71909c34535f3a22f65a9bcc701dbfc416
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:latest` - linux; amd64

```console
$ docker pull geonetwork@sha256:14f4c37fd41e1df44ce3a5d01958642493bb0fc782c2fc59a351e2f8b17301bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.2 MB (394235037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0338873ce41c80654f7ee007bab0426dcd364a131b15c1d1a2d9b50b05377465`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 03 Jun 2025 10:28:37 GMT
ARG RELEASE
# Tue, 03 Jun 2025 10:28:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 10:28:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 10:28:37 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 10:28:37 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 10:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:28:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ddbd5d7ef14aa06784fb94d1e0e7177868dfdd0aa216a8a2e654869968ef7392';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='761a0a87ca2b1e75eb5208565a56a4c3f49e02a5d4c00ce6a4930d015660e5d1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='05b791574d7174d2c8e033c4c987411b167d2ff9b5e954926b82295310f93e4d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e3a2e957a06909ccff8eb81e892e952080905831cdcbe41825c041430e205e3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='e5a611a198a7c9f7bc16258f5357e80932de9a21751bd68960dd02a0949084b1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
WORKDIR /var/lib/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
USER jetty
# Tue, 03 Jun 2025 10:28:37 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 03 Jun 2025 10:28:37 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 03 Jun 2025 10:28:37 GMT
USER root
# Tue, 03 Jun 2025 10:28:37 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
USER jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_FILE=geonetwork.war
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_VERSION=4.4.8
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_DOWNLOAD_MD5=0e36d39ac451ca3f75b5271626ec8074
# Tue, 03 Jun 2025 10:28:37 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 03 Jun 2025 10:28:37 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202b6d722eed4ab5d2bfa3ba17d989bd8d7dc4a291c1209e2eb7ef260604281f`  
		Last Modified: Mon, 15 Sep 2025 22:12:58 GMT  
		Size: 17.0 MB (16971594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce5eb149e836d7d4430090f75d3d4bd794384e90dda677b729d5ac70afb1f2c`  
		Last Modified: Mon, 15 Sep 2025 22:13:36 GMT  
		Size: 47.2 MB (47234885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535ddd21308e15867ddc44e02fc5b6e35cb88a8e2417c12ec3bf48bbe02d4ec8`  
		Last Modified: Mon, 15 Sep 2025 22:13:33 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3861023d4c48e4065afc71a57eeffbcac94e91bf1d69cb2d54915b9e60c28e`  
		Last Modified: Mon, 15 Sep 2025 22:13:33 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a8ffa92d4ec47f6ec198f4efa9b8f2cc88f8acb82a3e35ebb4c0baf1700935`  
		Last Modified: Mon, 15 Sep 2025 23:15:55 GMT  
		Size: 10.4 MB (10364405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70f3ed43e3e70c0f1b3c693897cee7f7fe3f6997a39e9a0ed68cb594bd6b76b`  
		Last Modified: Mon, 15 Sep 2025 23:15:54 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befdb1c29114f77e5d59d9857f126c91141a432d94980d5d39a1f7bc4efcd128`  
		Last Modified: Tue, 16 Sep 2025 00:15:55 GMT  
		Size: 238.8 KB (238787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8897772089027280ac6298a82c119c4c79297b4d3968483c3dbc4d47370c4ad3`  
		Last Modified: Tue, 16 Sep 2025 03:38:19 GMT  
		Size: 289.7 MB (289696347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9670489202686236ba4f606a292b29370a70cee7c88241e444e8c2421465f538`  
		Last Modified: Tue, 16 Sep 2025 00:15:55 GMT  
		Size: 551.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fedd504ecffdf7085dd4db8731709a3e45acc7bf57a6d82abee338f692403f6`  
		Last Modified: Tue, 16 Sep 2025 00:15:55 GMT  
		Size: 568.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3e04be7365c34c497f31c494cd539737a75fc43208861ac83ab879a4519e94`  
		Last Modified: Tue, 16 Sep 2025 00:15:55 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:latest` - unknown; unknown

```console
$ docker pull geonetwork@sha256:561d64151aef79e30047f5628d74b05649047daa4b56671144761fc1d8237689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f27daa75562651f8f2331a6b87e782f09555162e2d8707969db5d6c31172ab77`

```dockerfile
```

-	Layers:
	-	`sha256:ae5f325e38502485d46de8494a7935ddd51d9ed84d8aea675d96821573be2480`  
		Last Modified: Tue, 16 Sep 2025 03:13:06 GMT  
		Size: 4.2 MB (4213244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8c238cb776cc89a0f1ddca1cbeaa507e68f00234a57430fdd9445b7d1aec8db`  
		Last Modified: Tue, 16 Sep 2025 03:13:07 GMT  
		Size: 25.7 KB (25698 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:latest` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:012c162bd18ee436f33e3bd17f5890f3e38ea0c0b3bf84b12b175eae19a92710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.0 MB (393962388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee5e66d206846256ef206d50bb5faeb605f7d4042ef0ae6a02e958df6e6e752`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 03 Jun 2025 10:28:37 GMT
ARG RELEASE
# Tue, 03 Jun 2025 10:28:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 10:28:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 10:28:37 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 10:28:37 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 10:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:28:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ddbd5d7ef14aa06784fb94d1e0e7177868dfdd0aa216a8a2e654869968ef7392';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='761a0a87ca2b1e75eb5208565a56a4c3f49e02a5d4c00ce6a4930d015660e5d1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='05b791574d7174d2c8e033c4c987411b167d2ff9b5e954926b82295310f93e4d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e3a2e957a06909ccff8eb81e892e952080905831cdcbe41825c041430e205e3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='e5a611a198a7c9f7bc16258f5357e80932de9a21751bd68960dd02a0949084b1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 03 Jun 2025 10:28:37 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
WORKDIR /var/lib/jetty
# Tue, 03 Jun 2025 10:28:37 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
USER jetty
# Tue, 03 Jun 2025 10:28:37 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 03 Jun 2025 10:28:37 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 03 Jun 2025 10:28:37 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 03 Jun 2025 10:28:37 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 03 Jun 2025 10:28:37 GMT
USER root
# Tue, 03 Jun 2025 10:28:37 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
USER jetty
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_FILE=geonetwork.war
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_VERSION=4.4.8
# Tue, 03 Jun 2025 10:28:37 GMT
ENV GN_DOWNLOAD_MD5=0e36d39ac451ca3f75b5271626ec8074
# Tue, 03 Jun 2025 10:28:37 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Tue, 03 Jun 2025 10:28:37 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 03 Jun 2025 10:28:37 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Tue, 03 Jun 2025 10:28:37 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7731212bf16a96e9cb24502ab375b27ada010043b25bf48d09e8b324370001e8`  
		Last Modified: Thu, 02 Oct 2025 01:17:28 GMT  
		Size: 19.2 MB (19206374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55762cbc95ee6f07f07f03fbb2cdb97df1629c2f9df3c6834b628117c453a907`  
		Last Modified: Thu, 02 Oct 2025 01:17:29 GMT  
		Size: 45.6 MB (45589778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed220bd0328f6ca80c2bca119afdc8f1af8e48b1490f7aa6ba403e2cda20ba5`  
		Last Modified: Thu, 02 Oct 2025 01:17:26 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709644d6a90ce830acdafadc19cca22af78d1a354f4572cdf9fce33f006eed51`  
		Last Modified: Thu, 02 Oct 2025 01:17:26 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70b18f62015d2f668fd8e4c0a64052a350365bac3cc8df650e2004d058800c9`  
		Last Modified: Thu, 02 Oct 2025 03:24:38 GMT  
		Size: 10.4 MB (10364710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d4218282b53cef890af53cfb8f6262f43b3ffeb187cd391a56561dcaef9b60`  
		Last Modified: Thu, 02 Oct 2025 03:24:37 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21b387850edccdf7364680f57f0e8b20812cc6500d916d4067490a1a343dd3c`  
		Last Modified: Thu, 02 Oct 2025 04:20:42 GMT  
		Size: 238.0 KB (238033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce5ae6009fd11533f11c1fe43bec513e05bd7e3e766a7e31345d01a8c584b7e`  
		Last Modified: Thu, 02 Oct 2025 11:01:05 GMT  
		Size: 289.7 MB (289696344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44f4973c0ec7ebf87996e6d3afc79a69f159ef5cc0eda547488e32cd076660d`  
		Last Modified: Thu, 02 Oct 2025 04:20:41 GMT  
		Size: 552.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6dc92b2fea399a70cd408bcecdb0a32a508d769204df39aaa336ddd3ec9080`  
		Last Modified: Thu, 02 Oct 2025 04:20:41 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a604142bd6fc1b3d0cbf7eaff7209cccf1f5af6cc8b1c3096fbc444e8f91f88`  
		Last Modified: Thu, 02 Oct 2025 04:20:41 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:latest` - unknown; unknown

```console
$ docker pull geonetwork@sha256:3563e5a9b3da739ea982afc8e2155075bc4d7042032a81d812c093a06efbd9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4240161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651ba0ed744e3bb394f43f141009baea7d472bb49bbdbb3a7b13adc453ab6ab1`

```dockerfile
```

-	Layers:
	-	`sha256:0041b647a3cad450933480f74d9a9d5d1fafc06e12d8b7b7832528ac13c31ca4`  
		Last Modified: Thu, 02 Oct 2025 06:12:53 GMT  
		Size: 4.2 MB (4214329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b315e7de7c93c7c053f0c1651338c7435c96a6d96a22745a0d2681068dd169a`  
		Last Modified: Thu, 02 Oct 2025 06:12:54 GMT  
		Size: 25.8 KB (25832 bytes)  
		MIME: application/vnd.in-toto+json
