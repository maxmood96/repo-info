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
-	[`geonetwork:4.2.11`](#geonetwork4211)
-	[`geonetwork:4.4`](#geonetwork44)
-	[`geonetwork:4.4.6`](#geonetwork446)
-	[`geonetwork:latest`](#geonetworklatest)

## `geonetwork:3`

```console
$ docker pull geonetwork@sha256:26daa1bdb8e6dd5a53b761da2507e7bf8d52ab1bd9fec264ba78613512195f34
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
$ docker pull geonetwork@sha256:55d32c41df7dda5d01d244518a39a8efd66ca1f8dacf70342644f9840d57a985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.1 MB (352071367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a96f5dbe2d0fd895c543eafb6edba9a310cbc5cf6d222eb49d0b7b2f8412601`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
ENV TOMCAT_VERSION=9.0.98
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf840d2daa3eb8b3016ca6635c15fb8f178208e505fb676e76ace6ea3b3534`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 17.0 MB (16962462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bcf242e2cd7186fbb8ec27adaecb134c076ded9d04d4b4f50188d3377363fa`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 54.7 MB (54722130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbb498e39ab864221fac952c72984834e2f9c2fad49d1b082b90ff46757b97a`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c4f25076233e29d409cb09dc11eb0ae49cc3d34d2928ed4e53896cef85dad9`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c9070f2fda7201e5e887c691799627ea8969098733cd4da18a103c40e898fe`  
		Last Modified: Tue, 04 Feb 2025 05:20:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7318aca335fa855898a2bef82160041b752eecc37d669e28c85af5c66b31f4f7`  
		Last Modified: Tue, 04 Feb 2025 05:20:25 GMT  
		Size: 16.1 MB (16080361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d289cf14f224b4d9ea27487002075d27e48396b991145b6fb15037ca567bfea2`  
		Last Modified: Tue, 04 Feb 2025 06:18:20 GMT  
		Size: 234.5 MB (234549173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e812b3269d43e6702f351e5aac098f4330d584e2e415f1a70707924352f0aab`  
		Last Modified: Tue, 04 Feb 2025 06:18:17 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:7de17c7c61fece3e923851ebbf6f785fe05a3898c5ca38b4d9ea7442565c495d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4205425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0a78b9e0c35bb07e8f2894689cae694d02209e0e14143dbc32c3c87b851ee5`

```dockerfile
```

-	Layers:
	-	`sha256:8d8b4355afdfabe7201304873a2abf41facc68982b190fd71520b786babf615f`  
		Last Modified: Tue, 04 Feb 2025 06:18:17 GMT  
		Size: 4.2 MB (4186290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:120ca7a93438a54072711f7b1b05b9b46f7a0a4ae2fafe9c5cdb272dd56715ec`  
		Last Modified: Tue, 04 Feb 2025 06:18:17 GMT  
		Size: 19.1 KB (19135 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:d677b364c1cb5339e779323ab9ca09535140361b58b97e26499c04813ecca0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.5 MB (343532758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af243d36dba26dff4a4013876692f15fb621269e199d5026613eaec0eaa31eab`
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
ADD file:22301ffa2fa465db7a0f07e0c3ddc488f07cc6a745c39e6f450fdbe37da97418 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
ENV TOMCAT_VERSION=9.0.98
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
	-	`sha256:3492abb11babfb77cfc5a8904e67b22f4e4fd68c8d8a7fe1119861ed6503b36f`  
		Last Modified: Mon, 27 Jan 2025 05:10:02 GMT  
		Size: 26.9 MB (26874983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c78f4c1289c2528d1df38f88dd5b99ab818699237ae6309db38a8baf5b25bd`  
		Last Modified: Tue, 04 Feb 2025 10:52:47 GMT  
		Size: 16.3 MB (16294514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd04386e7b4c558003e659198d668f38a63b763ab2d532a0d352bb2c6dc2de3`  
		Last Modified: Tue, 04 Feb 2025 10:52:48 GMT  
		Size: 50.1 MB (50110162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3cb3465d9ab3ed9b850e687081ae7ef6afe27ebc09c1747f340ddf610f65d4`  
		Last Modified: Tue, 04 Feb 2025 10:52:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48126a60eb89b6332b66809612a7b8c210f7e3ae72d25bfdaff0d9ba0ea5d49e`  
		Last Modified: Tue, 04 Feb 2025 10:52:47 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3140698e7502eacf4043be14bb2f12c3417230b9f478476172aff8d57541e3b9`  
		Last Modified: Tue, 04 Feb 2025 18:43:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc54e25d0d82a26d8287326c4a8b957781dad0f2c64dc92b344e006a919e374`  
		Last Modified: Tue, 04 Feb 2025 18:43:29 GMT  
		Size: 15.7 MB (15712753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbe9db29e8b6ff71f4a1252be55a4ad9b5507a3af0b98a98ab29d79b3dbb36f`  
		Last Modified: Wed, 05 Feb 2025 01:41:02 GMT  
		Size: 234.5 MB (234537394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf7af9853ab1df3e568b458c822f602c1b00c00ee4a4dc6447a8e410b322c8b`  
		Last Modified: Wed, 05 Feb 2025 01:40:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:0bd5554a478046cb4005f5973a57d29b517bd18e120739b6fb6278b31eb41b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4209176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffffe17287550a54e6c0ca3546da4a14c3132de33368c0e95667d7e1cc498d1`

```dockerfile
```

-	Layers:
	-	`sha256:9a1619cb67d22a8550b78d3491207567768f3966d34d19c67e8f6e60fc7852cf`  
		Last Modified: Wed, 05 Feb 2025 01:40:57 GMT  
		Size: 4.2 MB (4189973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad77e08874bc8b05921f566180ee6928ef6e5268fb6e3cee48d3e292cf626aed`  
		Last Modified: Wed, 05 Feb 2025 01:40:56 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:0d03f72d18f4217e3acd6e7f9f2b0de9a63db46a78ffc2e0fd97e0481e77cc24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.3 MB (350313636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d2c10114cfcc4fbc66b6187ce414000236987796e85db2e24730ec087241ab`
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
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
ENV TOMCAT_VERSION=9.0.98
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a85dd745d889d39a94396575766058502783b6a6cf858e5c73a30aa91c01d5c`  
		Last Modified: Tue, 04 Feb 2025 09:17:45 GMT  
		Size: 53.8 MB (53826713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51108ceee1cec37e38142fc7aa62dbcc2ab0d863b93ad10efcb799c946e4867e`  
		Last Modified: Tue, 04 Feb 2025 09:17:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636940c42609be169b1c74123f576d6a6f6e2a98c59795aab9b3ca1dbaa4dfbc`  
		Last Modified: Tue, 04 Feb 2025 09:17:43 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84af9f53935b2d40bea6f2c52fb8e3fc074c1b8cacb45b1df2c46420bee575a7`  
		Last Modified: Tue, 04 Feb 2025 22:54:09 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f64a1f0e7c6f92b6044440f17ef8649b05a876ef71056b1f017d3ef1197dff`  
		Last Modified: Tue, 04 Feb 2025 22:54:10 GMT  
		Size: 16.1 MB (16059610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6508670148b455d28e383099cd29659eca971c68bb0e890f24e326545228a8ba`  
		Last Modified: Wed, 05 Feb 2025 06:29:06 GMT  
		Size: 234.6 MB (234553364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dc8de2eb15a0729ecccfaed29a7711e0b36a21107ee7932d2fd8d24c94ab08`  
		Last Modified: Wed, 05 Feb 2025 06:29:01 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:7fd89349ddb19aa2b945322dacd154cb733e2d713e84d4584f3324bde0efa0a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4206675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a92456a7806c6f30efb5e70e083c23ce3f69e967660e3752fe3d17075530c2`

```dockerfile
```

-	Layers:
	-	`sha256:3375b308e629a20889784f319752a94584e17c4b08ff6a52af2164fdbe04e7f3`  
		Last Modified: Wed, 05 Feb 2025 06:29:01 GMT  
		Size: 4.2 MB (4187448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1755718e29dbafac810e3140c8ada927d7e8e655d56469b49c92f7ec28012ba8`  
		Last Modified: Wed, 05 Feb 2025 06:29:00 GMT  
		Size: 19.2 KB (19227 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:cfbd86efa1a2e827b7baf89bc428ec3f100f1d61d80dd66bb98a9ff774bfc79c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.3 MB (356265951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0146a977a6cdd83c98e484d889318859ec57ebd0cc52c3662a4b0f98c01e074`
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
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
ENV TOMCAT_VERSION=9.0.98
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c7b03d73f24fbf1ca191efda6fafe2355b68e6e070a54b70fec6dc3ac0c66e`  
		Last Modified: Tue, 04 Feb 2025 07:33:35 GMT  
		Size: 18.8 MB (18824340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4dc055eb2ce25e2475c115e50b0f25a266a775c2cc5fc6ff326027c388b8f05`  
		Last Modified: Tue, 04 Feb 2025 07:33:38 GMT  
		Size: 52.2 MB (52174003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c506bccab0df478619ab2a85ab4cccf56a3e406da9689a8b126fcf970d3b0a0`  
		Last Modified: Tue, 04 Feb 2025 07:33:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f462ee40978f69b9fb6cb11bc79402ca598cb494a9cfc5dfd9e5829747697d59`  
		Last Modified: Tue, 04 Feb 2025 07:33:33 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef759b119de3abf9e00fefe29fa8b1dada269259e1455bf298637e444a26253`  
		Last Modified: Tue, 04 Feb 2025 20:04:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c040b8c2cbc60f4ff1edd3494d8548ba3063ea230836ad37f2b7aea704c242`  
		Last Modified: Tue, 04 Feb 2025 20:04:52 GMT  
		Size: 16.3 MB (16300862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c511ddc80fe5d8d5ba3830cd23c69127801a98d8dc2d1e4ba731d83ca8e8794`  
		Last Modified: Wed, 05 Feb 2025 01:43:26 GMT  
		Size: 234.6 MB (234573974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032f051d731ad78bbec11a75acea26256857e2da1500c867be3fe78b448c44c1`  
		Last Modified: Wed, 05 Feb 2025 01:43:17 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:a570ec1d6fe2c7ea23c3435e734e56a3449170d7d68f6218c3e2a4e1061765ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25cc5cb48e058c4b4c75717d600f58c4380efd7110af86a3fdec437ce52d06cb`

```dockerfile
```

-	Layers:
	-	`sha256:7d1b2ee1ca7877fca9109349f34dc12a6ee8ec32e89b0a8caf5ade6189176089`  
		Last Modified: Wed, 05 Feb 2025 01:43:18 GMT  
		Size: 4.2 MB (4188891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dcea8240c0fc7969d2046bbaaf5e78b37b8ef6160695618ab18b720a9ecf259`  
		Last Modified: Wed, 05 Feb 2025 01:43:17 GMT  
		Size: 19.2 KB (19173 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3-postgres`

```console
$ docker pull geonetwork@sha256:6d3e1ca76c09ed8a666e6e98ca43d204a7089f76567683e8713a5dcd057c37eb
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
$ docker pull geonetwork@sha256:e16e72f5843659839a2ab29bb2f7a351ac3b9b7ab0cfbad6500197438386d2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.9 MB (365903180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ae5b22ae5cd307f75f45bd6db40a2af07e89102d75ae7c71e5b1a0089a5532`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
ENV TOMCAT_VERSION=9.0.98
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf840d2daa3eb8b3016ca6635c15fb8f178208e505fb676e76ace6ea3b3534`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 17.0 MB (16962462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bcf242e2cd7186fbb8ec27adaecb134c076ded9d04d4b4f50188d3377363fa`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 54.7 MB (54722130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbb498e39ab864221fac952c72984834e2f9c2fad49d1b082b90ff46757b97a`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c4f25076233e29d409cb09dc11eb0ae49cc3d34d2928ed4e53896cef85dad9`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c9070f2fda7201e5e887c691799627ea8969098733cd4da18a103c40e898fe`  
		Last Modified: Tue, 04 Feb 2025 05:20:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7318aca335fa855898a2bef82160041b752eecc37d669e28c85af5c66b31f4f7`  
		Last Modified: Tue, 04 Feb 2025 05:20:25 GMT  
		Size: 16.1 MB (16080361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d289cf14f224b4d9ea27487002075d27e48396b991145b6fb15037ca567bfea2`  
		Last Modified: Tue, 04 Feb 2025 06:18:20 GMT  
		Size: 234.5 MB (234549173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e812b3269d43e6702f351e5aac098f4330d584e2e415f1a70707924352f0aab`  
		Last Modified: Tue, 04 Feb 2025 06:18:17 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a9f5c38effd88f1b0d93a161b72fba9a81fd45c81100a926fac3ba70c63a01`  
		Last Modified: Tue, 04 Feb 2025 07:14:44 GMT  
		Size: 13.8 MB (13828398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3410782ee62c1b4100f2d08c0a6f29d7a2a80c34aefc7263bb987aa21011c88`  
		Last Modified: Tue, 04 Feb 2025 07:14:43 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585b1ab02494f1fec297725d9666dd98b537c1033eb4b1cda6f25f118f3a4a95`  
		Last Modified: Tue, 04 Feb 2025 07:14:43 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b08b38ef9c462ecc39d756ef345b13f0191cafc567476bb28bbeee84ac77bc1`  
		Last Modified: Tue, 04 Feb 2025 07:14:43 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:c74d25e06279145d43cc623b1629cc560df07eeb529f1fb98cffdce0b25f8273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ee8cca534404a1095604352884226ce57db215a70fc7ce9c134432340840bf`

```dockerfile
```

-	Layers:
	-	`sha256:87d7300ce2135f54c1ba95485072b80a498e761dbc29d8cee67eaaaa1e1d96ab`  
		Last Modified: Tue, 04 Feb 2025 07:14:43 GMT  
		Size: 5.7 MB (5726698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2029389360b6fd60038938277616ee83cd93c98a716f10c874e68dc7618b6039`  
		Last Modified: Tue, 04 Feb 2025 07:14:43 GMT  
		Size: 22.9 KB (22860 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:a9f655636d8dc43d20b981dbfa20af057d4117b4c2d548b52523bc63f13e6d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.4 MB (356447245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e91b1bea4dbe08977685a917c48954053b18679bee2dfa4b527f8582fd9fb0`
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
ADD file:22301ffa2fa465db7a0f07e0c3ddc488f07cc6a745c39e6f450fdbe37da97418 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
ENV TOMCAT_VERSION=9.0.98
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
	-	`sha256:3492abb11babfb77cfc5a8904e67b22f4e4fd68c8d8a7fe1119861ed6503b36f`  
		Last Modified: Mon, 27 Jan 2025 05:10:02 GMT  
		Size: 26.9 MB (26874983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c78f4c1289c2528d1df38f88dd5b99ab818699237ae6309db38a8baf5b25bd`  
		Last Modified: Tue, 04 Feb 2025 10:52:47 GMT  
		Size: 16.3 MB (16294514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd04386e7b4c558003e659198d668f38a63b763ab2d532a0d352bb2c6dc2de3`  
		Last Modified: Tue, 04 Feb 2025 10:52:48 GMT  
		Size: 50.1 MB (50110162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3cb3465d9ab3ed9b850e687081ae7ef6afe27ebc09c1747f340ddf610f65d4`  
		Last Modified: Tue, 04 Feb 2025 10:52:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48126a60eb89b6332b66809612a7b8c210f7e3ae72d25bfdaff0d9ba0ea5d49e`  
		Last Modified: Tue, 04 Feb 2025 10:52:47 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3140698e7502eacf4043be14bb2f12c3417230b9f478476172aff8d57541e3b9`  
		Last Modified: Tue, 04 Feb 2025 18:43:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc54e25d0d82a26d8287326c4a8b957781dad0f2c64dc92b344e006a919e374`  
		Last Modified: Tue, 04 Feb 2025 18:43:29 GMT  
		Size: 15.7 MB (15712753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbe9db29e8b6ff71f4a1252be55a4ad9b5507a3af0b98a98ab29d79b3dbb36f`  
		Last Modified: Wed, 05 Feb 2025 01:41:02 GMT  
		Size: 234.5 MB (234537394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf7af9853ab1df3e568b458c822f602c1b00c00ee4a4dc6447a8e410b322c8b`  
		Last Modified: Wed, 05 Feb 2025 01:40:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135e1b44a591eb1395937c5cb25cdb09d80d305c3722afcf4c1e89b012537f94`  
		Last Modified: Wed, 05 Feb 2025 11:17:15 GMT  
		Size: 12.9 MB (12911068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472cec41a4fc38342e74ae741f590ab8916e4ee98163366241000f5d46526e02`  
		Last Modified: Wed, 05 Feb 2025 11:17:15 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d996a0169560e1d87ca0e85512f9bf4c16c9b89df582e38263f9f10df77f37`  
		Last Modified: Wed, 05 Feb 2025 11:17:15 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8462a605bd1e5de68b845cb7b66a0b968f8447969f59b8801f7cc5c195d49058`  
		Last Modified: Wed, 05 Feb 2025 11:17:15 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:a714fcf6daeff7bea37aac3f1b201cf477127c08ae5c85555273d76156a42c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7640deaa69f2e5be474e0fa05638ba3df384a3d128d08f3ab434da3bddeaa1`

```dockerfile
```

-	Layers:
	-	`sha256:36d1c98c01de6624900aeb1e58028e083c66bfb0a79a936c767e5b0c376484c5`  
		Last Modified: Wed, 05 Feb 2025 11:17:15 GMT  
		Size: 5.7 MB (5729121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e8c4652621d911ccb08372db3945846a42ba009d74af0454d547ad1479f83e`  
		Last Modified: Wed, 05 Feb 2025 11:17:15 GMT  
		Size: 22.9 KB (22941 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:f2d2fa3f434c512313f097ab7e27bf358b8984f5da127d247d48b63274b60472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.1 MB (364127270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3851574eb9b77de504b0df41f22ea6e32518d8d6cbb64bea0e142687a370dc`
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
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
ENV TOMCAT_VERSION=9.0.98
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a85dd745d889d39a94396575766058502783b6a6cf858e5c73a30aa91c01d5c`  
		Last Modified: Tue, 04 Feb 2025 09:17:45 GMT  
		Size: 53.8 MB (53826713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51108ceee1cec37e38142fc7aa62dbcc2ab0d863b93ad10efcb799c946e4867e`  
		Last Modified: Tue, 04 Feb 2025 09:17:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636940c42609be169b1c74123f576d6a6f6e2a98c59795aab9b3ca1dbaa4dfbc`  
		Last Modified: Tue, 04 Feb 2025 09:17:43 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84af9f53935b2d40bea6f2c52fb8e3fc074c1b8cacb45b1df2c46420bee575a7`  
		Last Modified: Tue, 04 Feb 2025 22:54:09 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f64a1f0e7c6f92b6044440f17ef8649b05a876ef71056b1f017d3ef1197dff`  
		Last Modified: Tue, 04 Feb 2025 22:54:10 GMT  
		Size: 16.1 MB (16059610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6508670148b455d28e383099cd29659eca971c68bb0e890f24e326545228a8ba`  
		Last Modified: Wed, 05 Feb 2025 06:29:06 GMT  
		Size: 234.6 MB (234553364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dc8de2eb15a0729ecccfaed29a7711e0b36a21107ee7932d2fd8d24c94ab08`  
		Last Modified: Wed, 05 Feb 2025 06:29:01 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32f47eacb28dbd4899a7f929ce805d71935d25db4f144b43f153386399cd8df`  
		Last Modified: Wed, 05 Feb 2025 15:39:06 GMT  
		Size: 13.8 MB (13810211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b1489331a7a7c76a31e7ee4c4eede8f4d0337ff153d760a2f54ed61a398855`  
		Last Modified: Wed, 05 Feb 2025 15:39:05 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44bd91d74bd08186bacc6287843f9b2b8243766cc6ca5daba04f6c93de6d1fd`  
		Last Modified: Wed, 05 Feb 2025 15:39:05 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37ac9811a8d9812daee6b503eefc10c0e553d5ba428088603bb8717503f0e3f`  
		Last Modified: Wed, 05 Feb 2025 15:39:05 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:06bbdd09a9920ec7611ca42c87130230c78fc7233fef133b1030890b6c255391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5756867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae56f6463c1e946138f9447a6582c3d95f1f99e120bf5c871bfa145303bd010`

```dockerfile
```

-	Layers:
	-	`sha256:4caab86a04ef8d1a69ab395e2568a8279111bd8d836ed95b19406be0e6fddcee`  
		Last Modified: Wed, 05 Feb 2025 15:39:06 GMT  
		Size: 5.7 MB (5733900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb715ef320c046b70d0335de7add662c1933a1dc30d6cf65ae9dbc48d8c8ef46`  
		Last Modified: Wed, 05 Feb 2025 15:39:05 GMT  
		Size: 23.0 KB (22967 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:558c951389192419e24923f96f193fbbd7bc16aace011f6d5de8c7db65a33b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.6 MB (370590696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63e8d41e7e7bf107d497ead0d977753bdec70bf3d5d5da667237468c389d9d3`
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
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
ENV TOMCAT_VERSION=9.0.98
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c7b03d73f24fbf1ca191efda6fafe2355b68e6e070a54b70fec6dc3ac0c66e`  
		Last Modified: Tue, 04 Feb 2025 07:33:35 GMT  
		Size: 18.8 MB (18824340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4dc055eb2ce25e2475c115e50b0f25a266a775c2cc5fc6ff326027c388b8f05`  
		Last Modified: Tue, 04 Feb 2025 07:33:38 GMT  
		Size: 52.2 MB (52174003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c506bccab0df478619ab2a85ab4cccf56a3e406da9689a8b126fcf970d3b0a0`  
		Last Modified: Tue, 04 Feb 2025 07:33:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f462ee40978f69b9fb6cb11bc79402ca598cb494a9cfc5dfd9e5829747697d59`  
		Last Modified: Tue, 04 Feb 2025 07:33:33 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef759b119de3abf9e00fefe29fa8b1dada269259e1455bf298637e444a26253`  
		Last Modified: Tue, 04 Feb 2025 20:04:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c040b8c2cbc60f4ff1edd3494d8548ba3063ea230836ad37f2b7aea704c242`  
		Last Modified: Tue, 04 Feb 2025 20:04:52 GMT  
		Size: 16.3 MB (16300862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c511ddc80fe5d8d5ba3830cd23c69127801a98d8dc2d1e4ba731d83ca8e8794`  
		Last Modified: Wed, 05 Feb 2025 01:43:26 GMT  
		Size: 234.6 MB (234573974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032f051d731ad78bbec11a75acea26256857e2da1500c867be3fe78b448c44c1`  
		Last Modified: Wed, 05 Feb 2025 01:43:17 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97a0e6aded0d3e739ae2d8f49e7d00ecb1bf8a3301a4b926cc410c6001a1607`  
		Last Modified: Wed, 05 Feb 2025 11:08:35 GMT  
		Size: 14.3 MB (14321327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b070b62a550b4ac3ebbcf838b3b8ece03ef9a4ec1f56b7a6142fa19bdfab2b98`  
		Last Modified: Wed, 05 Feb 2025 11:08:35 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4eb9e67b57e2b3d8749af4d188653dbb9aceead66da0b0aef84052481998853`  
		Last Modified: Wed, 05 Feb 2025 11:08:35 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98f4a348c73a40a24efc2551a23c5fcb9438929b4b8f33723e9701b866b980d`  
		Last Modified: Wed, 05 Feb 2025 11:08:35 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:5adea92c14cdecc67ffccaffec6588376d98326ddb3514bf2d5268332b946dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5754944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766627d713762f4b6eadd9887c92b61153a9ba3e92bfd46f944034319d29bcfd`

```dockerfile
```

-	Layers:
	-	`sha256:61d0982774f93c467ecdfd150c6fcc62d512ce56c76a9a08dbd3a65cd6af5d90`  
		Last Modified: Wed, 05 Feb 2025 11:08:35 GMT  
		Size: 5.7 MB (5732044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06686c82c616dc6faf2c68328b4efbdf121359287dbf2a83c1e69fd9bb47dd15`  
		Last Modified: Wed, 05 Feb 2025 11:08:34 GMT  
		Size: 22.9 KB (22900 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12`

```console
$ docker pull geonetwork@sha256:26daa1bdb8e6dd5a53b761da2507e7bf8d52ab1bd9fec264ba78613512195f34
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
$ docker pull geonetwork@sha256:55d32c41df7dda5d01d244518a39a8efd66ca1f8dacf70342644f9840d57a985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.1 MB (352071367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a96f5dbe2d0fd895c543eafb6edba9a310cbc5cf6d222eb49d0b7b2f8412601`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
ENV TOMCAT_VERSION=9.0.98
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf840d2daa3eb8b3016ca6635c15fb8f178208e505fb676e76ace6ea3b3534`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 17.0 MB (16962462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bcf242e2cd7186fbb8ec27adaecb134c076ded9d04d4b4f50188d3377363fa`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 54.7 MB (54722130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbb498e39ab864221fac952c72984834e2f9c2fad49d1b082b90ff46757b97a`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c4f25076233e29d409cb09dc11eb0ae49cc3d34d2928ed4e53896cef85dad9`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c9070f2fda7201e5e887c691799627ea8969098733cd4da18a103c40e898fe`  
		Last Modified: Tue, 04 Feb 2025 05:20:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7318aca335fa855898a2bef82160041b752eecc37d669e28c85af5c66b31f4f7`  
		Last Modified: Tue, 04 Feb 2025 05:20:25 GMT  
		Size: 16.1 MB (16080361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d289cf14f224b4d9ea27487002075d27e48396b991145b6fb15037ca567bfea2`  
		Last Modified: Tue, 04 Feb 2025 06:18:20 GMT  
		Size: 234.5 MB (234549173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e812b3269d43e6702f351e5aac098f4330d584e2e415f1a70707924352f0aab`  
		Last Modified: Tue, 04 Feb 2025 06:18:17 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:7de17c7c61fece3e923851ebbf6f785fe05a3898c5ca38b4d9ea7442565c495d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4205425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0a78b9e0c35bb07e8f2894689cae694d02209e0e14143dbc32c3c87b851ee5`

```dockerfile
```

-	Layers:
	-	`sha256:8d8b4355afdfabe7201304873a2abf41facc68982b190fd71520b786babf615f`  
		Last Modified: Tue, 04 Feb 2025 06:18:17 GMT  
		Size: 4.2 MB (4186290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:120ca7a93438a54072711f7b1b05b9b46f7a0a4ae2fafe9c5cdb272dd56715ec`  
		Last Modified: Tue, 04 Feb 2025 06:18:17 GMT  
		Size: 19.1 KB (19135 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:d677b364c1cb5339e779323ab9ca09535140361b58b97e26499c04813ecca0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.5 MB (343532758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af243d36dba26dff4a4013876692f15fb621269e199d5026613eaec0eaa31eab`
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
ADD file:22301ffa2fa465db7a0f07e0c3ddc488f07cc6a745c39e6f450fdbe37da97418 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
ENV TOMCAT_VERSION=9.0.98
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
	-	`sha256:3492abb11babfb77cfc5a8904e67b22f4e4fd68c8d8a7fe1119861ed6503b36f`  
		Last Modified: Mon, 27 Jan 2025 05:10:02 GMT  
		Size: 26.9 MB (26874983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c78f4c1289c2528d1df38f88dd5b99ab818699237ae6309db38a8baf5b25bd`  
		Last Modified: Tue, 04 Feb 2025 10:52:47 GMT  
		Size: 16.3 MB (16294514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd04386e7b4c558003e659198d668f38a63b763ab2d532a0d352bb2c6dc2de3`  
		Last Modified: Tue, 04 Feb 2025 10:52:48 GMT  
		Size: 50.1 MB (50110162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3cb3465d9ab3ed9b850e687081ae7ef6afe27ebc09c1747f340ddf610f65d4`  
		Last Modified: Tue, 04 Feb 2025 10:52:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48126a60eb89b6332b66809612a7b8c210f7e3ae72d25bfdaff0d9ba0ea5d49e`  
		Last Modified: Tue, 04 Feb 2025 10:52:47 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3140698e7502eacf4043be14bb2f12c3417230b9f478476172aff8d57541e3b9`  
		Last Modified: Tue, 04 Feb 2025 18:43:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc54e25d0d82a26d8287326c4a8b957781dad0f2c64dc92b344e006a919e374`  
		Last Modified: Tue, 04 Feb 2025 18:43:29 GMT  
		Size: 15.7 MB (15712753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbe9db29e8b6ff71f4a1252be55a4ad9b5507a3af0b98a98ab29d79b3dbb36f`  
		Last Modified: Wed, 05 Feb 2025 01:41:02 GMT  
		Size: 234.5 MB (234537394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf7af9853ab1df3e568b458c822f602c1b00c00ee4a4dc6447a8e410b322c8b`  
		Last Modified: Wed, 05 Feb 2025 01:40:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:0bd5554a478046cb4005f5973a57d29b517bd18e120739b6fb6278b31eb41b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4209176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffffe17287550a54e6c0ca3546da4a14c3132de33368c0e95667d7e1cc498d1`

```dockerfile
```

-	Layers:
	-	`sha256:9a1619cb67d22a8550b78d3491207567768f3966d34d19c67e8f6e60fc7852cf`  
		Last Modified: Wed, 05 Feb 2025 01:40:57 GMT  
		Size: 4.2 MB (4189973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad77e08874bc8b05921f566180ee6928ef6e5268fb6e3cee48d3e292cf626aed`  
		Last Modified: Wed, 05 Feb 2025 01:40:56 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:0d03f72d18f4217e3acd6e7f9f2b0de9a63db46a78ffc2e0fd97e0481e77cc24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.3 MB (350313636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d2c10114cfcc4fbc66b6187ce414000236987796e85db2e24730ec087241ab`
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
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
ENV TOMCAT_VERSION=9.0.98
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a85dd745d889d39a94396575766058502783b6a6cf858e5c73a30aa91c01d5c`  
		Last Modified: Tue, 04 Feb 2025 09:17:45 GMT  
		Size: 53.8 MB (53826713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51108ceee1cec37e38142fc7aa62dbcc2ab0d863b93ad10efcb799c946e4867e`  
		Last Modified: Tue, 04 Feb 2025 09:17:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636940c42609be169b1c74123f576d6a6f6e2a98c59795aab9b3ca1dbaa4dfbc`  
		Last Modified: Tue, 04 Feb 2025 09:17:43 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84af9f53935b2d40bea6f2c52fb8e3fc074c1b8cacb45b1df2c46420bee575a7`  
		Last Modified: Tue, 04 Feb 2025 22:54:09 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f64a1f0e7c6f92b6044440f17ef8649b05a876ef71056b1f017d3ef1197dff`  
		Last Modified: Tue, 04 Feb 2025 22:54:10 GMT  
		Size: 16.1 MB (16059610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6508670148b455d28e383099cd29659eca971c68bb0e890f24e326545228a8ba`  
		Last Modified: Wed, 05 Feb 2025 06:29:06 GMT  
		Size: 234.6 MB (234553364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dc8de2eb15a0729ecccfaed29a7711e0b36a21107ee7932d2fd8d24c94ab08`  
		Last Modified: Wed, 05 Feb 2025 06:29:01 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:7fd89349ddb19aa2b945322dacd154cb733e2d713e84d4584f3324bde0efa0a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4206675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a92456a7806c6f30efb5e70e083c23ce3f69e967660e3752fe3d17075530c2`

```dockerfile
```

-	Layers:
	-	`sha256:3375b308e629a20889784f319752a94584e17c4b08ff6a52af2164fdbe04e7f3`  
		Last Modified: Wed, 05 Feb 2025 06:29:01 GMT  
		Size: 4.2 MB (4187448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1755718e29dbafac810e3140c8ada927d7e8e655d56469b49c92f7ec28012ba8`  
		Last Modified: Wed, 05 Feb 2025 06:29:00 GMT  
		Size: 19.2 KB (19227 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:cfbd86efa1a2e827b7baf89bc428ec3f100f1d61d80dd66bb98a9ff774bfc79c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.3 MB (356265951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0146a977a6cdd83c98e484d889318859ec57ebd0cc52c3662a4b0f98c01e074`
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
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
ENV TOMCAT_VERSION=9.0.98
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c7b03d73f24fbf1ca191efda6fafe2355b68e6e070a54b70fec6dc3ac0c66e`  
		Last Modified: Tue, 04 Feb 2025 07:33:35 GMT  
		Size: 18.8 MB (18824340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4dc055eb2ce25e2475c115e50b0f25a266a775c2cc5fc6ff326027c388b8f05`  
		Last Modified: Tue, 04 Feb 2025 07:33:38 GMT  
		Size: 52.2 MB (52174003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c506bccab0df478619ab2a85ab4cccf56a3e406da9689a8b126fcf970d3b0a0`  
		Last Modified: Tue, 04 Feb 2025 07:33:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f462ee40978f69b9fb6cb11bc79402ca598cb494a9cfc5dfd9e5829747697d59`  
		Last Modified: Tue, 04 Feb 2025 07:33:33 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef759b119de3abf9e00fefe29fa8b1dada269259e1455bf298637e444a26253`  
		Last Modified: Tue, 04 Feb 2025 20:04:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c040b8c2cbc60f4ff1edd3494d8548ba3063ea230836ad37f2b7aea704c242`  
		Last Modified: Tue, 04 Feb 2025 20:04:52 GMT  
		Size: 16.3 MB (16300862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c511ddc80fe5d8d5ba3830cd23c69127801a98d8dc2d1e4ba731d83ca8e8794`  
		Last Modified: Wed, 05 Feb 2025 01:43:26 GMT  
		Size: 234.6 MB (234573974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032f051d731ad78bbec11a75acea26256857e2da1500c867be3fe78b448c44c1`  
		Last Modified: Wed, 05 Feb 2025 01:43:17 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:a570ec1d6fe2c7ea23c3435e734e56a3449170d7d68f6218c3e2a4e1061765ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25cc5cb48e058c4b4c75717d600f58c4380efd7110af86a3fdec437ce52d06cb`

```dockerfile
```

-	Layers:
	-	`sha256:7d1b2ee1ca7877fca9109349f34dc12a6ee8ec32e89b0a8caf5ade6189176089`  
		Last Modified: Wed, 05 Feb 2025 01:43:18 GMT  
		Size: 4.2 MB (4188891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dcea8240c0fc7969d2046bbaaf5e78b37b8ef6160695618ab18b720a9ecf259`  
		Last Modified: Wed, 05 Feb 2025 01:43:17 GMT  
		Size: 19.2 KB (19173 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12-postgres`

```console
$ docker pull geonetwork@sha256:6d3e1ca76c09ed8a666e6e98ca43d204a7089f76567683e8713a5dcd057c37eb
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
$ docker pull geonetwork@sha256:e16e72f5843659839a2ab29bb2f7a351ac3b9b7ab0cfbad6500197438386d2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.9 MB (365903180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ae5b22ae5cd307f75f45bd6db40a2af07e89102d75ae7c71e5b1a0089a5532`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
ENV TOMCAT_VERSION=9.0.98
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf840d2daa3eb8b3016ca6635c15fb8f178208e505fb676e76ace6ea3b3534`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 17.0 MB (16962462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bcf242e2cd7186fbb8ec27adaecb134c076ded9d04d4b4f50188d3377363fa`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 54.7 MB (54722130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbb498e39ab864221fac952c72984834e2f9c2fad49d1b082b90ff46757b97a`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c4f25076233e29d409cb09dc11eb0ae49cc3d34d2928ed4e53896cef85dad9`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c9070f2fda7201e5e887c691799627ea8969098733cd4da18a103c40e898fe`  
		Last Modified: Tue, 04 Feb 2025 05:20:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7318aca335fa855898a2bef82160041b752eecc37d669e28c85af5c66b31f4f7`  
		Last Modified: Tue, 04 Feb 2025 05:20:25 GMT  
		Size: 16.1 MB (16080361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d289cf14f224b4d9ea27487002075d27e48396b991145b6fb15037ca567bfea2`  
		Last Modified: Tue, 04 Feb 2025 06:18:20 GMT  
		Size: 234.5 MB (234549173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e812b3269d43e6702f351e5aac098f4330d584e2e415f1a70707924352f0aab`  
		Last Modified: Tue, 04 Feb 2025 06:18:17 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a9f5c38effd88f1b0d93a161b72fba9a81fd45c81100a926fac3ba70c63a01`  
		Last Modified: Tue, 04 Feb 2025 07:14:44 GMT  
		Size: 13.8 MB (13828398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3410782ee62c1b4100f2d08c0a6f29d7a2a80c34aefc7263bb987aa21011c88`  
		Last Modified: Tue, 04 Feb 2025 07:14:43 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585b1ab02494f1fec297725d9666dd98b537c1033eb4b1cda6f25f118f3a4a95`  
		Last Modified: Tue, 04 Feb 2025 07:14:43 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b08b38ef9c462ecc39d756ef345b13f0191cafc567476bb28bbeee84ac77bc1`  
		Last Modified: Tue, 04 Feb 2025 07:14:43 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:c74d25e06279145d43cc623b1629cc560df07eeb529f1fb98cffdce0b25f8273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ee8cca534404a1095604352884226ce57db215a70fc7ce9c134432340840bf`

```dockerfile
```

-	Layers:
	-	`sha256:87d7300ce2135f54c1ba95485072b80a498e761dbc29d8cee67eaaaa1e1d96ab`  
		Last Modified: Tue, 04 Feb 2025 07:14:43 GMT  
		Size: 5.7 MB (5726698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2029389360b6fd60038938277616ee83cd93c98a716f10c874e68dc7618b6039`  
		Last Modified: Tue, 04 Feb 2025 07:14:43 GMT  
		Size: 22.9 KB (22860 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:a9f655636d8dc43d20b981dbfa20af057d4117b4c2d548b52523bc63f13e6d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.4 MB (356447245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e91b1bea4dbe08977685a917c48954053b18679bee2dfa4b527f8582fd9fb0`
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
ADD file:22301ffa2fa465db7a0f07e0c3ddc488f07cc6a745c39e6f450fdbe37da97418 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
ENV TOMCAT_VERSION=9.0.98
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
	-	`sha256:3492abb11babfb77cfc5a8904e67b22f4e4fd68c8d8a7fe1119861ed6503b36f`  
		Last Modified: Mon, 27 Jan 2025 05:10:02 GMT  
		Size: 26.9 MB (26874983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c78f4c1289c2528d1df38f88dd5b99ab818699237ae6309db38a8baf5b25bd`  
		Last Modified: Tue, 04 Feb 2025 10:52:47 GMT  
		Size: 16.3 MB (16294514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd04386e7b4c558003e659198d668f38a63b763ab2d532a0d352bb2c6dc2de3`  
		Last Modified: Tue, 04 Feb 2025 10:52:48 GMT  
		Size: 50.1 MB (50110162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3cb3465d9ab3ed9b850e687081ae7ef6afe27ebc09c1747f340ddf610f65d4`  
		Last Modified: Tue, 04 Feb 2025 10:52:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48126a60eb89b6332b66809612a7b8c210f7e3ae72d25bfdaff0d9ba0ea5d49e`  
		Last Modified: Tue, 04 Feb 2025 10:52:47 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3140698e7502eacf4043be14bb2f12c3417230b9f478476172aff8d57541e3b9`  
		Last Modified: Tue, 04 Feb 2025 18:43:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc54e25d0d82a26d8287326c4a8b957781dad0f2c64dc92b344e006a919e374`  
		Last Modified: Tue, 04 Feb 2025 18:43:29 GMT  
		Size: 15.7 MB (15712753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbe9db29e8b6ff71f4a1252be55a4ad9b5507a3af0b98a98ab29d79b3dbb36f`  
		Last Modified: Wed, 05 Feb 2025 01:41:02 GMT  
		Size: 234.5 MB (234537394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf7af9853ab1df3e568b458c822f602c1b00c00ee4a4dc6447a8e410b322c8b`  
		Last Modified: Wed, 05 Feb 2025 01:40:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135e1b44a591eb1395937c5cb25cdb09d80d305c3722afcf4c1e89b012537f94`  
		Last Modified: Wed, 05 Feb 2025 11:17:15 GMT  
		Size: 12.9 MB (12911068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472cec41a4fc38342e74ae741f590ab8916e4ee98163366241000f5d46526e02`  
		Last Modified: Wed, 05 Feb 2025 11:17:15 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d996a0169560e1d87ca0e85512f9bf4c16c9b89df582e38263f9f10df77f37`  
		Last Modified: Wed, 05 Feb 2025 11:17:15 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8462a605bd1e5de68b845cb7b66a0b968f8447969f59b8801f7cc5c195d49058`  
		Last Modified: Wed, 05 Feb 2025 11:17:15 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:a714fcf6daeff7bea37aac3f1b201cf477127c08ae5c85555273d76156a42c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7640deaa69f2e5be474e0fa05638ba3df384a3d128d08f3ab434da3bddeaa1`

```dockerfile
```

-	Layers:
	-	`sha256:36d1c98c01de6624900aeb1e58028e083c66bfb0a79a936c767e5b0c376484c5`  
		Last Modified: Wed, 05 Feb 2025 11:17:15 GMT  
		Size: 5.7 MB (5729121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e8c4652621d911ccb08372db3945846a42ba009d74af0454d547ad1479f83e`  
		Last Modified: Wed, 05 Feb 2025 11:17:15 GMT  
		Size: 22.9 KB (22941 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:f2d2fa3f434c512313f097ab7e27bf358b8984f5da127d247d48b63274b60472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.1 MB (364127270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3851574eb9b77de504b0df41f22ea6e32518d8d6cbb64bea0e142687a370dc`
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
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
ENV TOMCAT_VERSION=9.0.98
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a85dd745d889d39a94396575766058502783b6a6cf858e5c73a30aa91c01d5c`  
		Last Modified: Tue, 04 Feb 2025 09:17:45 GMT  
		Size: 53.8 MB (53826713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51108ceee1cec37e38142fc7aa62dbcc2ab0d863b93ad10efcb799c946e4867e`  
		Last Modified: Tue, 04 Feb 2025 09:17:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636940c42609be169b1c74123f576d6a6f6e2a98c59795aab9b3ca1dbaa4dfbc`  
		Last Modified: Tue, 04 Feb 2025 09:17:43 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84af9f53935b2d40bea6f2c52fb8e3fc074c1b8cacb45b1df2c46420bee575a7`  
		Last Modified: Tue, 04 Feb 2025 22:54:09 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f64a1f0e7c6f92b6044440f17ef8649b05a876ef71056b1f017d3ef1197dff`  
		Last Modified: Tue, 04 Feb 2025 22:54:10 GMT  
		Size: 16.1 MB (16059610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6508670148b455d28e383099cd29659eca971c68bb0e890f24e326545228a8ba`  
		Last Modified: Wed, 05 Feb 2025 06:29:06 GMT  
		Size: 234.6 MB (234553364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dc8de2eb15a0729ecccfaed29a7711e0b36a21107ee7932d2fd8d24c94ab08`  
		Last Modified: Wed, 05 Feb 2025 06:29:01 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32f47eacb28dbd4899a7f929ce805d71935d25db4f144b43f153386399cd8df`  
		Last Modified: Wed, 05 Feb 2025 15:39:06 GMT  
		Size: 13.8 MB (13810211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b1489331a7a7c76a31e7ee4c4eede8f4d0337ff153d760a2f54ed61a398855`  
		Last Modified: Wed, 05 Feb 2025 15:39:05 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44bd91d74bd08186bacc6287843f9b2b8243766cc6ca5daba04f6c93de6d1fd`  
		Last Modified: Wed, 05 Feb 2025 15:39:05 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37ac9811a8d9812daee6b503eefc10c0e553d5ba428088603bb8717503f0e3f`  
		Last Modified: Wed, 05 Feb 2025 15:39:05 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:06bbdd09a9920ec7611ca42c87130230c78fc7233fef133b1030890b6c255391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5756867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae56f6463c1e946138f9447a6582c3d95f1f99e120bf5c871bfa145303bd010`

```dockerfile
```

-	Layers:
	-	`sha256:4caab86a04ef8d1a69ab395e2568a8279111bd8d836ed95b19406be0e6fddcee`  
		Last Modified: Wed, 05 Feb 2025 15:39:06 GMT  
		Size: 5.7 MB (5733900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb715ef320c046b70d0335de7add662c1933a1dc30d6cf65ae9dbc48d8c8ef46`  
		Last Modified: Wed, 05 Feb 2025 15:39:05 GMT  
		Size: 23.0 KB (22967 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:558c951389192419e24923f96f193fbbd7bc16aace011f6d5de8c7db65a33b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.6 MB (370590696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63e8d41e7e7bf107d497ead0d977753bdec70bf3d5d5da667237468c389d9d3`
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
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
ENV TOMCAT_VERSION=9.0.98
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c7b03d73f24fbf1ca191efda6fafe2355b68e6e070a54b70fec6dc3ac0c66e`  
		Last Modified: Tue, 04 Feb 2025 07:33:35 GMT  
		Size: 18.8 MB (18824340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4dc055eb2ce25e2475c115e50b0f25a266a775c2cc5fc6ff326027c388b8f05`  
		Last Modified: Tue, 04 Feb 2025 07:33:38 GMT  
		Size: 52.2 MB (52174003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c506bccab0df478619ab2a85ab4cccf56a3e406da9689a8b126fcf970d3b0a0`  
		Last Modified: Tue, 04 Feb 2025 07:33:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f462ee40978f69b9fb6cb11bc79402ca598cb494a9cfc5dfd9e5829747697d59`  
		Last Modified: Tue, 04 Feb 2025 07:33:33 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef759b119de3abf9e00fefe29fa8b1dada269259e1455bf298637e444a26253`  
		Last Modified: Tue, 04 Feb 2025 20:04:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c040b8c2cbc60f4ff1edd3494d8548ba3063ea230836ad37f2b7aea704c242`  
		Last Modified: Tue, 04 Feb 2025 20:04:52 GMT  
		Size: 16.3 MB (16300862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c511ddc80fe5d8d5ba3830cd23c69127801a98d8dc2d1e4ba731d83ca8e8794`  
		Last Modified: Wed, 05 Feb 2025 01:43:26 GMT  
		Size: 234.6 MB (234573974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032f051d731ad78bbec11a75acea26256857e2da1500c867be3fe78b448c44c1`  
		Last Modified: Wed, 05 Feb 2025 01:43:17 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97a0e6aded0d3e739ae2d8f49e7d00ecb1bf8a3301a4b926cc410c6001a1607`  
		Last Modified: Wed, 05 Feb 2025 11:08:35 GMT  
		Size: 14.3 MB (14321327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b070b62a550b4ac3ebbcf838b3b8ece03ef9a4ec1f56b7a6142fa19bdfab2b98`  
		Last Modified: Wed, 05 Feb 2025 11:08:35 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4eb9e67b57e2b3d8749af4d188653dbb9aceead66da0b0aef84052481998853`  
		Last Modified: Wed, 05 Feb 2025 11:08:35 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98f4a348c73a40a24efc2551a23c5fcb9438929b4b8f33723e9701b866b980d`  
		Last Modified: Wed, 05 Feb 2025 11:08:35 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:5adea92c14cdecc67ffccaffec6588376d98326ddb3514bf2d5268332b946dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5754944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766627d713762f4b6eadd9887c92b61153a9ba3e92bfd46f944034319d29bcfd`

```dockerfile
```

-	Layers:
	-	`sha256:61d0982774f93c467ecdfd150c6fcc62d512ce56c76a9a08dbd3a65cd6af5d90`  
		Last Modified: Wed, 05 Feb 2025 11:08:35 GMT  
		Size: 5.7 MB (5732044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06686c82c616dc6faf2c68328b4efbdf121359287dbf2a83c1e69fd9bb47dd15`  
		Last Modified: Wed, 05 Feb 2025 11:08:34 GMT  
		Size: 22.9 KB (22900 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12.12`

```console
$ docker pull geonetwork@sha256:26daa1bdb8e6dd5a53b761da2507e7bf8d52ab1bd9fec264ba78613512195f34
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
$ docker pull geonetwork@sha256:55d32c41df7dda5d01d244518a39a8efd66ca1f8dacf70342644f9840d57a985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.1 MB (352071367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a96f5dbe2d0fd895c543eafb6edba9a310cbc5cf6d222eb49d0b7b2f8412601`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
ENV TOMCAT_VERSION=9.0.98
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf840d2daa3eb8b3016ca6635c15fb8f178208e505fb676e76ace6ea3b3534`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 17.0 MB (16962462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bcf242e2cd7186fbb8ec27adaecb134c076ded9d04d4b4f50188d3377363fa`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 54.7 MB (54722130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbb498e39ab864221fac952c72984834e2f9c2fad49d1b082b90ff46757b97a`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c4f25076233e29d409cb09dc11eb0ae49cc3d34d2928ed4e53896cef85dad9`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c9070f2fda7201e5e887c691799627ea8969098733cd4da18a103c40e898fe`  
		Last Modified: Tue, 04 Feb 2025 05:20:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7318aca335fa855898a2bef82160041b752eecc37d669e28c85af5c66b31f4f7`  
		Last Modified: Tue, 04 Feb 2025 05:20:25 GMT  
		Size: 16.1 MB (16080361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d289cf14f224b4d9ea27487002075d27e48396b991145b6fb15037ca567bfea2`  
		Last Modified: Tue, 04 Feb 2025 06:18:20 GMT  
		Size: 234.5 MB (234549173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e812b3269d43e6702f351e5aac098f4330d584e2e415f1a70707924352f0aab`  
		Last Modified: Tue, 04 Feb 2025 06:18:17 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:7de17c7c61fece3e923851ebbf6f785fe05a3898c5ca38b4d9ea7442565c495d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4205425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0a78b9e0c35bb07e8f2894689cae694d02209e0e14143dbc32c3c87b851ee5`

```dockerfile
```

-	Layers:
	-	`sha256:8d8b4355afdfabe7201304873a2abf41facc68982b190fd71520b786babf615f`  
		Last Modified: Tue, 04 Feb 2025 06:18:17 GMT  
		Size: 4.2 MB (4186290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:120ca7a93438a54072711f7b1b05b9b46f7a0a4ae2fafe9c5cdb272dd56715ec`  
		Last Modified: Tue, 04 Feb 2025 06:18:17 GMT  
		Size: 19.1 KB (19135 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:d677b364c1cb5339e779323ab9ca09535140361b58b97e26499c04813ecca0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.5 MB (343532758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af243d36dba26dff4a4013876692f15fb621269e199d5026613eaec0eaa31eab`
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
ADD file:22301ffa2fa465db7a0f07e0c3ddc488f07cc6a745c39e6f450fdbe37da97418 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
ENV TOMCAT_VERSION=9.0.98
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
	-	`sha256:3492abb11babfb77cfc5a8904e67b22f4e4fd68c8d8a7fe1119861ed6503b36f`  
		Last Modified: Mon, 27 Jan 2025 05:10:02 GMT  
		Size: 26.9 MB (26874983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c78f4c1289c2528d1df38f88dd5b99ab818699237ae6309db38a8baf5b25bd`  
		Last Modified: Tue, 04 Feb 2025 10:52:47 GMT  
		Size: 16.3 MB (16294514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd04386e7b4c558003e659198d668f38a63b763ab2d532a0d352bb2c6dc2de3`  
		Last Modified: Tue, 04 Feb 2025 10:52:48 GMT  
		Size: 50.1 MB (50110162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3cb3465d9ab3ed9b850e687081ae7ef6afe27ebc09c1747f340ddf610f65d4`  
		Last Modified: Tue, 04 Feb 2025 10:52:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48126a60eb89b6332b66809612a7b8c210f7e3ae72d25bfdaff0d9ba0ea5d49e`  
		Last Modified: Tue, 04 Feb 2025 10:52:47 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3140698e7502eacf4043be14bb2f12c3417230b9f478476172aff8d57541e3b9`  
		Last Modified: Tue, 04 Feb 2025 18:43:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc54e25d0d82a26d8287326c4a8b957781dad0f2c64dc92b344e006a919e374`  
		Last Modified: Tue, 04 Feb 2025 18:43:29 GMT  
		Size: 15.7 MB (15712753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbe9db29e8b6ff71f4a1252be55a4ad9b5507a3af0b98a98ab29d79b3dbb36f`  
		Last Modified: Wed, 05 Feb 2025 01:41:02 GMT  
		Size: 234.5 MB (234537394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf7af9853ab1df3e568b458c822f602c1b00c00ee4a4dc6447a8e410b322c8b`  
		Last Modified: Wed, 05 Feb 2025 01:40:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:0bd5554a478046cb4005f5973a57d29b517bd18e120739b6fb6278b31eb41b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4209176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffffe17287550a54e6c0ca3546da4a14c3132de33368c0e95667d7e1cc498d1`

```dockerfile
```

-	Layers:
	-	`sha256:9a1619cb67d22a8550b78d3491207567768f3966d34d19c67e8f6e60fc7852cf`  
		Last Modified: Wed, 05 Feb 2025 01:40:57 GMT  
		Size: 4.2 MB (4189973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad77e08874bc8b05921f566180ee6928ef6e5268fb6e3cee48d3e292cf626aed`  
		Last Modified: Wed, 05 Feb 2025 01:40:56 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:0d03f72d18f4217e3acd6e7f9f2b0de9a63db46a78ffc2e0fd97e0481e77cc24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.3 MB (350313636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d2c10114cfcc4fbc66b6187ce414000236987796e85db2e24730ec087241ab`
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
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
ENV TOMCAT_VERSION=9.0.98
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a85dd745d889d39a94396575766058502783b6a6cf858e5c73a30aa91c01d5c`  
		Last Modified: Tue, 04 Feb 2025 09:17:45 GMT  
		Size: 53.8 MB (53826713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51108ceee1cec37e38142fc7aa62dbcc2ab0d863b93ad10efcb799c946e4867e`  
		Last Modified: Tue, 04 Feb 2025 09:17:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636940c42609be169b1c74123f576d6a6f6e2a98c59795aab9b3ca1dbaa4dfbc`  
		Last Modified: Tue, 04 Feb 2025 09:17:43 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84af9f53935b2d40bea6f2c52fb8e3fc074c1b8cacb45b1df2c46420bee575a7`  
		Last Modified: Tue, 04 Feb 2025 22:54:09 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f64a1f0e7c6f92b6044440f17ef8649b05a876ef71056b1f017d3ef1197dff`  
		Last Modified: Tue, 04 Feb 2025 22:54:10 GMT  
		Size: 16.1 MB (16059610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6508670148b455d28e383099cd29659eca971c68bb0e890f24e326545228a8ba`  
		Last Modified: Wed, 05 Feb 2025 06:29:06 GMT  
		Size: 234.6 MB (234553364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dc8de2eb15a0729ecccfaed29a7711e0b36a21107ee7932d2fd8d24c94ab08`  
		Last Modified: Wed, 05 Feb 2025 06:29:01 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:7fd89349ddb19aa2b945322dacd154cb733e2d713e84d4584f3324bde0efa0a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4206675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a92456a7806c6f30efb5e70e083c23ce3f69e967660e3752fe3d17075530c2`

```dockerfile
```

-	Layers:
	-	`sha256:3375b308e629a20889784f319752a94584e17c4b08ff6a52af2164fdbe04e7f3`  
		Last Modified: Wed, 05 Feb 2025 06:29:01 GMT  
		Size: 4.2 MB (4187448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1755718e29dbafac810e3140c8ada927d7e8e655d56469b49c92f7ec28012ba8`  
		Last Modified: Wed, 05 Feb 2025 06:29:00 GMT  
		Size: 19.2 KB (19227 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:cfbd86efa1a2e827b7baf89bc428ec3f100f1d61d80dd66bb98a9ff774bfc79c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.3 MB (356265951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0146a977a6cdd83c98e484d889318859ec57ebd0cc52c3662a4b0f98c01e074`
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
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
ENV TOMCAT_VERSION=9.0.98
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c7b03d73f24fbf1ca191efda6fafe2355b68e6e070a54b70fec6dc3ac0c66e`  
		Last Modified: Tue, 04 Feb 2025 07:33:35 GMT  
		Size: 18.8 MB (18824340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4dc055eb2ce25e2475c115e50b0f25a266a775c2cc5fc6ff326027c388b8f05`  
		Last Modified: Tue, 04 Feb 2025 07:33:38 GMT  
		Size: 52.2 MB (52174003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c506bccab0df478619ab2a85ab4cccf56a3e406da9689a8b126fcf970d3b0a0`  
		Last Modified: Tue, 04 Feb 2025 07:33:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f462ee40978f69b9fb6cb11bc79402ca598cb494a9cfc5dfd9e5829747697d59`  
		Last Modified: Tue, 04 Feb 2025 07:33:33 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef759b119de3abf9e00fefe29fa8b1dada269259e1455bf298637e444a26253`  
		Last Modified: Tue, 04 Feb 2025 20:04:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c040b8c2cbc60f4ff1edd3494d8548ba3063ea230836ad37f2b7aea704c242`  
		Last Modified: Tue, 04 Feb 2025 20:04:52 GMT  
		Size: 16.3 MB (16300862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c511ddc80fe5d8d5ba3830cd23c69127801a98d8dc2d1e4ba731d83ca8e8794`  
		Last Modified: Wed, 05 Feb 2025 01:43:26 GMT  
		Size: 234.6 MB (234573974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032f051d731ad78bbec11a75acea26256857e2da1500c867be3fe78b448c44c1`  
		Last Modified: Wed, 05 Feb 2025 01:43:17 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:a570ec1d6fe2c7ea23c3435e734e56a3449170d7d68f6218c3e2a4e1061765ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25cc5cb48e058c4b4c75717d600f58c4380efd7110af86a3fdec437ce52d06cb`

```dockerfile
```

-	Layers:
	-	`sha256:7d1b2ee1ca7877fca9109349f34dc12a6ee8ec32e89b0a8caf5ade6189176089`  
		Last Modified: Wed, 05 Feb 2025 01:43:18 GMT  
		Size: 4.2 MB (4188891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dcea8240c0fc7969d2046bbaaf5e78b37b8ef6160695618ab18b720a9ecf259`  
		Last Modified: Wed, 05 Feb 2025 01:43:17 GMT  
		Size: 19.2 KB (19173 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12.12-postgres`

```console
$ docker pull geonetwork@sha256:6d3e1ca76c09ed8a666e6e98ca43d204a7089f76567683e8713a5dcd057c37eb
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
$ docker pull geonetwork@sha256:e16e72f5843659839a2ab29bb2f7a351ac3b9b7ab0cfbad6500197438386d2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.9 MB (365903180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ae5b22ae5cd307f75f45bd6db40a2af07e89102d75ae7c71e5b1a0089a5532`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
ENV TOMCAT_VERSION=9.0.98
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf840d2daa3eb8b3016ca6635c15fb8f178208e505fb676e76ace6ea3b3534`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 17.0 MB (16962462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bcf242e2cd7186fbb8ec27adaecb134c076ded9d04d4b4f50188d3377363fa`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 54.7 MB (54722130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbb498e39ab864221fac952c72984834e2f9c2fad49d1b082b90ff46757b97a`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c4f25076233e29d409cb09dc11eb0ae49cc3d34d2928ed4e53896cef85dad9`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c9070f2fda7201e5e887c691799627ea8969098733cd4da18a103c40e898fe`  
		Last Modified: Tue, 04 Feb 2025 05:20:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7318aca335fa855898a2bef82160041b752eecc37d669e28c85af5c66b31f4f7`  
		Last Modified: Tue, 04 Feb 2025 05:20:25 GMT  
		Size: 16.1 MB (16080361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d289cf14f224b4d9ea27487002075d27e48396b991145b6fb15037ca567bfea2`  
		Last Modified: Tue, 04 Feb 2025 06:18:20 GMT  
		Size: 234.5 MB (234549173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e812b3269d43e6702f351e5aac098f4330d584e2e415f1a70707924352f0aab`  
		Last Modified: Tue, 04 Feb 2025 06:18:17 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a9f5c38effd88f1b0d93a161b72fba9a81fd45c81100a926fac3ba70c63a01`  
		Last Modified: Tue, 04 Feb 2025 07:14:44 GMT  
		Size: 13.8 MB (13828398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3410782ee62c1b4100f2d08c0a6f29d7a2a80c34aefc7263bb987aa21011c88`  
		Last Modified: Tue, 04 Feb 2025 07:14:43 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585b1ab02494f1fec297725d9666dd98b537c1033eb4b1cda6f25f118f3a4a95`  
		Last Modified: Tue, 04 Feb 2025 07:14:43 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b08b38ef9c462ecc39d756ef345b13f0191cafc567476bb28bbeee84ac77bc1`  
		Last Modified: Tue, 04 Feb 2025 07:14:43 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:c74d25e06279145d43cc623b1629cc560df07eeb529f1fb98cffdce0b25f8273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ee8cca534404a1095604352884226ce57db215a70fc7ce9c134432340840bf`

```dockerfile
```

-	Layers:
	-	`sha256:87d7300ce2135f54c1ba95485072b80a498e761dbc29d8cee67eaaaa1e1d96ab`  
		Last Modified: Tue, 04 Feb 2025 07:14:43 GMT  
		Size: 5.7 MB (5726698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2029389360b6fd60038938277616ee83cd93c98a716f10c874e68dc7618b6039`  
		Last Modified: Tue, 04 Feb 2025 07:14:43 GMT  
		Size: 22.9 KB (22860 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:a9f655636d8dc43d20b981dbfa20af057d4117b4c2d548b52523bc63f13e6d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.4 MB (356447245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e91b1bea4dbe08977685a917c48954053b18679bee2dfa4b527f8582fd9fb0`
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
ADD file:22301ffa2fa465db7a0f07e0c3ddc488f07cc6a745c39e6f450fdbe37da97418 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
ENV TOMCAT_VERSION=9.0.98
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
	-	`sha256:3492abb11babfb77cfc5a8904e67b22f4e4fd68c8d8a7fe1119861ed6503b36f`  
		Last Modified: Mon, 27 Jan 2025 05:10:02 GMT  
		Size: 26.9 MB (26874983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c78f4c1289c2528d1df38f88dd5b99ab818699237ae6309db38a8baf5b25bd`  
		Last Modified: Tue, 04 Feb 2025 10:52:47 GMT  
		Size: 16.3 MB (16294514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd04386e7b4c558003e659198d668f38a63b763ab2d532a0d352bb2c6dc2de3`  
		Last Modified: Tue, 04 Feb 2025 10:52:48 GMT  
		Size: 50.1 MB (50110162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3cb3465d9ab3ed9b850e687081ae7ef6afe27ebc09c1747f340ddf610f65d4`  
		Last Modified: Tue, 04 Feb 2025 10:52:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48126a60eb89b6332b66809612a7b8c210f7e3ae72d25bfdaff0d9ba0ea5d49e`  
		Last Modified: Tue, 04 Feb 2025 10:52:47 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3140698e7502eacf4043be14bb2f12c3417230b9f478476172aff8d57541e3b9`  
		Last Modified: Tue, 04 Feb 2025 18:43:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc54e25d0d82a26d8287326c4a8b957781dad0f2c64dc92b344e006a919e374`  
		Last Modified: Tue, 04 Feb 2025 18:43:29 GMT  
		Size: 15.7 MB (15712753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbe9db29e8b6ff71f4a1252be55a4ad9b5507a3af0b98a98ab29d79b3dbb36f`  
		Last Modified: Wed, 05 Feb 2025 01:41:02 GMT  
		Size: 234.5 MB (234537394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf7af9853ab1df3e568b458c822f602c1b00c00ee4a4dc6447a8e410b322c8b`  
		Last Modified: Wed, 05 Feb 2025 01:40:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135e1b44a591eb1395937c5cb25cdb09d80d305c3722afcf4c1e89b012537f94`  
		Last Modified: Wed, 05 Feb 2025 11:17:15 GMT  
		Size: 12.9 MB (12911068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472cec41a4fc38342e74ae741f590ab8916e4ee98163366241000f5d46526e02`  
		Last Modified: Wed, 05 Feb 2025 11:17:15 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d996a0169560e1d87ca0e85512f9bf4c16c9b89df582e38263f9f10df77f37`  
		Last Modified: Wed, 05 Feb 2025 11:17:15 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8462a605bd1e5de68b845cb7b66a0b968f8447969f59b8801f7cc5c195d49058`  
		Last Modified: Wed, 05 Feb 2025 11:17:15 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:a714fcf6daeff7bea37aac3f1b201cf477127c08ae5c85555273d76156a42c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7640deaa69f2e5be474e0fa05638ba3df384a3d128d08f3ab434da3bddeaa1`

```dockerfile
```

-	Layers:
	-	`sha256:36d1c98c01de6624900aeb1e58028e083c66bfb0a79a936c767e5b0c376484c5`  
		Last Modified: Wed, 05 Feb 2025 11:17:15 GMT  
		Size: 5.7 MB (5729121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e8c4652621d911ccb08372db3945846a42ba009d74af0454d547ad1479f83e`  
		Last Modified: Wed, 05 Feb 2025 11:17:15 GMT  
		Size: 22.9 KB (22941 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:f2d2fa3f434c512313f097ab7e27bf358b8984f5da127d247d48b63274b60472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.1 MB (364127270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3851574eb9b77de504b0df41f22ea6e32518d8d6cbb64bea0e142687a370dc`
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
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
ENV TOMCAT_VERSION=9.0.98
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a85dd745d889d39a94396575766058502783b6a6cf858e5c73a30aa91c01d5c`  
		Last Modified: Tue, 04 Feb 2025 09:17:45 GMT  
		Size: 53.8 MB (53826713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51108ceee1cec37e38142fc7aa62dbcc2ab0d863b93ad10efcb799c946e4867e`  
		Last Modified: Tue, 04 Feb 2025 09:17:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636940c42609be169b1c74123f576d6a6f6e2a98c59795aab9b3ca1dbaa4dfbc`  
		Last Modified: Tue, 04 Feb 2025 09:17:43 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84af9f53935b2d40bea6f2c52fb8e3fc074c1b8cacb45b1df2c46420bee575a7`  
		Last Modified: Tue, 04 Feb 2025 22:54:09 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f64a1f0e7c6f92b6044440f17ef8649b05a876ef71056b1f017d3ef1197dff`  
		Last Modified: Tue, 04 Feb 2025 22:54:10 GMT  
		Size: 16.1 MB (16059610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6508670148b455d28e383099cd29659eca971c68bb0e890f24e326545228a8ba`  
		Last Modified: Wed, 05 Feb 2025 06:29:06 GMT  
		Size: 234.6 MB (234553364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dc8de2eb15a0729ecccfaed29a7711e0b36a21107ee7932d2fd8d24c94ab08`  
		Last Modified: Wed, 05 Feb 2025 06:29:01 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32f47eacb28dbd4899a7f929ce805d71935d25db4f144b43f153386399cd8df`  
		Last Modified: Wed, 05 Feb 2025 15:39:06 GMT  
		Size: 13.8 MB (13810211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b1489331a7a7c76a31e7ee4c4eede8f4d0337ff153d760a2f54ed61a398855`  
		Last Modified: Wed, 05 Feb 2025 15:39:05 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44bd91d74bd08186bacc6287843f9b2b8243766cc6ca5daba04f6c93de6d1fd`  
		Last Modified: Wed, 05 Feb 2025 15:39:05 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37ac9811a8d9812daee6b503eefc10c0e553d5ba428088603bb8717503f0e3f`  
		Last Modified: Wed, 05 Feb 2025 15:39:05 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:06bbdd09a9920ec7611ca42c87130230c78fc7233fef133b1030890b6c255391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5756867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae56f6463c1e946138f9447a6582c3d95f1f99e120bf5c871bfa145303bd010`

```dockerfile
```

-	Layers:
	-	`sha256:4caab86a04ef8d1a69ab395e2568a8279111bd8d836ed95b19406be0e6fddcee`  
		Last Modified: Wed, 05 Feb 2025 15:39:06 GMT  
		Size: 5.7 MB (5733900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb715ef320c046b70d0335de7add662c1933a1dc30d6cf65ae9dbc48d8c8ef46`  
		Last Modified: Wed, 05 Feb 2025 15:39:05 GMT  
		Size: 23.0 KB (22967 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:558c951389192419e24923f96f193fbbd7bc16aace011f6d5de8c7db65a33b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.6 MB (370590696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63e8d41e7e7bf107d497ead0d977753bdec70bf3d5d5da667237468c389d9d3`
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
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
ENV TOMCAT_VERSION=9.0.98
# Thu, 08 Aug 2024 11:50:27 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
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
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c7b03d73f24fbf1ca191efda6fafe2355b68e6e070a54b70fec6dc3ac0c66e`  
		Last Modified: Tue, 04 Feb 2025 07:33:35 GMT  
		Size: 18.8 MB (18824340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4dc055eb2ce25e2475c115e50b0f25a266a775c2cc5fc6ff326027c388b8f05`  
		Last Modified: Tue, 04 Feb 2025 07:33:38 GMT  
		Size: 52.2 MB (52174003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c506bccab0df478619ab2a85ab4cccf56a3e406da9689a8b126fcf970d3b0a0`  
		Last Modified: Tue, 04 Feb 2025 07:33:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f462ee40978f69b9fb6cb11bc79402ca598cb494a9cfc5dfd9e5829747697d59`  
		Last Modified: Tue, 04 Feb 2025 07:33:33 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef759b119de3abf9e00fefe29fa8b1dada269259e1455bf298637e444a26253`  
		Last Modified: Tue, 04 Feb 2025 20:04:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c040b8c2cbc60f4ff1edd3494d8548ba3063ea230836ad37f2b7aea704c242`  
		Last Modified: Tue, 04 Feb 2025 20:04:52 GMT  
		Size: 16.3 MB (16300862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c511ddc80fe5d8d5ba3830cd23c69127801a98d8dc2d1e4ba731d83ca8e8794`  
		Last Modified: Wed, 05 Feb 2025 01:43:26 GMT  
		Size: 234.6 MB (234573974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032f051d731ad78bbec11a75acea26256857e2da1500c867be3fe78b448c44c1`  
		Last Modified: Wed, 05 Feb 2025 01:43:17 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97a0e6aded0d3e739ae2d8f49e7d00ecb1bf8a3301a4b926cc410c6001a1607`  
		Last Modified: Wed, 05 Feb 2025 11:08:35 GMT  
		Size: 14.3 MB (14321327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b070b62a550b4ac3ebbcf838b3b8ece03ef9a4ec1f56b7a6142fa19bdfab2b98`  
		Last Modified: Wed, 05 Feb 2025 11:08:35 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4eb9e67b57e2b3d8749af4d188653dbb9aceead66da0b0aef84052481998853`  
		Last Modified: Wed, 05 Feb 2025 11:08:35 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98f4a348c73a40a24efc2551a23c5fcb9438929b4b8f33723e9701b866b980d`  
		Last Modified: Wed, 05 Feb 2025 11:08:35 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:5adea92c14cdecc67ffccaffec6588376d98326ddb3514bf2d5268332b946dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5754944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766627d713762f4b6eadd9887c92b61153a9ba3e92bfd46f944034319d29bcfd`

```dockerfile
```

-	Layers:
	-	`sha256:61d0982774f93c467ecdfd150c6fcc62d512ce56c76a9a08dbd3a65cd6af5d90`  
		Last Modified: Wed, 05 Feb 2025 11:08:35 GMT  
		Size: 5.7 MB (5732044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06686c82c616dc6faf2c68328b4efbdf121359287dbf2a83c1e69fd9bb47dd15`  
		Last Modified: Wed, 05 Feb 2025 11:08:34 GMT  
		Size: 22.9 KB (22900 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4`

```console
$ docker pull geonetwork@sha256:de8edfec283b81c76bd3a7adc58bdff0ff57d48eba26b260bcc040a17a11e9ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:4` - linux; amd64

```console
$ docker pull geonetwork@sha256:c46a8cbe54433bc52ef223cb93d65ffbca08c857caaed020dd16b71768ea8c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.1 MB (493054297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04bfe6d405887cef9c8cb04f9e9de2d03ee190c20d54c913eef3e7104589cd2`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Oct 2024 11:20:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 11:20:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='79d574328f6960d40349996ef8c5949581f9e533dc76f134857c4125c78558ff';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Oct 2024 11:20:12 GMT
CMD ["jshell"]
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_VERSION=9.4.57.v20241219
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.57.v20241219/jetty-home-9.4.57.v20241219.tar.gz
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
WORKDIR /var/lib/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
USER jetty
# Thu, 24 Oct 2024 11:20:12 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 24 Oct 2024 11:20:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 24 Oct 2024 11:20:12 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 24 Oct 2024 11:20:12 GMT
ENV DATA_DIR=/catalogue-data
# Thu, 24 Oct 2024 11:20:12 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Thu, 24 Oct 2024 11:20:12 GMT
USER root
# Thu, 24 Oct 2024 11:20:12 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
USER jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_FILE=geonetwork.war
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_VERSION=4.4.6
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_DOWNLOAD_MD5=ad596d3348872506c78daa05edb14782
# Thu, 24 Oct 2024 11:20:12 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Thu, 24 Oct 2024 11:20:12 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 24 Oct 2024 11:20:12 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57720219966e918f1a532346498cfbfb342979a0f5ef1c523ba9e60e4ef5ab63`  
		Last Modified: Fri, 31 Jan 2025 01:30:17 GMT  
		Size: 20.3 MB (20251237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec2b4dbdfccae2f0821bf0672520a085237394280af05d3fa21c12397b754d0`  
		Last Modified: Fri, 31 Jan 2025 01:30:19 GMT  
		Size: 145.6 MB (145609067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae877ab777ef84fc2dae1668033dcb1343246ee291a5ff14fba9cf841202dff`  
		Last Modified: Fri, 31 Jan 2025 01:30:15 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7b6bd77aa73b02a876a07119cd314e85e8eb53687bb5153edd5e074e76a94`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ad00986e7c30ead99fef5802d9a4efbe8f1546cca93a1148026a22e743b9e2`  
		Last Modified: Fri, 31 Jan 2025 02:14:50 GMT  
		Size: 10.3 MB (10299713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7be791f756f430948ac42b83f87ed680794a78f83e76bb3e2951c3f82f1764e`  
		Last Modified: Fri, 31 Jan 2025 02:14:39 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c33c31bb10a6c2e6d4328e36915ea0e696d90a3531f480d41681ab3fedcca6f`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 254.4 KB (254351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40996a68fb9db773e3171dcc9a6da39ef6a5b513115eaca51fc3accf2bf4cebb`  
		Last Modified: Fri, 31 Jan 2025 03:12:44 GMT  
		Size: 289.1 MB (289123480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c0fae08b476dc0d5942cbcd81799c7c87c2909d8b07222e5bdda8947e1b25b`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 551.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a217fe03d135d2cb18223aea9add78499a414590b7f78a5d93d4ee74c016b3`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 568.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca2b4aa497fdd66ff0f245297c2bed0afdec7ce077a8bd98a76e797c8769920`  
		Last Modified: Fri, 31 Jan 2025 03:12:41 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:fcdea2617189080e1f2a9fa6c11001e06ac78b700c23638548057c0282877973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c46cd06ff58aee08c44b7d0e18129489db4b3283d55ddb858afd28bcbefc2f`

```dockerfile
```

-	Layers:
	-	`sha256:100255f77dbf0901761711d0a42bce8f2fdbf26e9fe6a605b7b44833cc24afeb`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 4.7 MB (4691021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9db15a999cbf82b93b3140fc01779fc48f5c68c027c08871ea62d5e1b0a63239`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 25.7 KB (25700 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:7c88ee544a39062628f8ed3a3e563aad8167664219838dbb535fd278ebf713f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.1 MB (488139632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04346d672fe5f872f51b6129bcfb6cc323c8af1c23a2b04434c52c4ce881585a`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Oct 2024 11:20:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 11:20:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='79d574328f6960d40349996ef8c5949581f9e533dc76f134857c4125c78558ff';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Oct 2024 11:20:12 GMT
CMD ["jshell"]
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_VERSION=9.4.57.v20241219
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.57.v20241219/jetty-home-9.4.57.v20241219.tar.gz
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
WORKDIR /var/lib/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
USER jetty
# Thu, 24 Oct 2024 11:20:12 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 24 Oct 2024 11:20:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 24 Oct 2024 11:20:12 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 24 Oct 2024 11:20:12 GMT
ENV DATA_DIR=/catalogue-data
# Thu, 24 Oct 2024 11:20:12 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Thu, 24 Oct 2024 11:20:12 GMT
USER root
# Thu, 24 Oct 2024 11:20:12 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
USER jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_FILE=geonetwork.war
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_VERSION=4.4.6
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_DOWNLOAD_MD5=ad596d3348872506c78daa05edb14782
# Thu, 24 Oct 2024 11:20:12 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Thu, 24 Oct 2024 11:20:12 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 24 Oct 2024 11:20:12 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c529ed0cdd6ba59828bb5288f63e6f174c4cbf1b5499595c7338b9b52066229`  
		Last Modified: Fri, 31 Jan 2025 01:35:16 GMT  
		Size: 142.4 MB (142390502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0628f645ce6b92ee9bbe4a6bb14c29263b9a0de9205b6250eb5a8ae122e196`  
		Last Modified: Fri, 31 Jan 2025 01:35:13 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948a71537099de96aed8d9ae3bf948c5d51700abaef7a8cb429b09e6579ab012`  
		Last Modified: Fri, 31 Jan 2025 01:35:13 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83cff723577cb2d244e05fdf013d80137c7dd0cf6ef4f02ad1e11bd3fefb38c`  
		Last Modified: Fri, 31 Jan 2025 03:06:30 GMT  
		Size: 10.3 MB (10299567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d408fec3bd3fb508fbd995fe95df3755475bcc84339224a7931421eeb829aba9`  
		Last Modified: Fri, 31 Jan 2025 03:06:29 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdc1dc019a7debf2fd24e2ac298ab62e6fd2b3c6773f96180a1a9be8009849c`  
		Last Modified: Fri, 31 Jan 2025 06:25:53 GMT  
		Size: 252.2 KB (252232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6006f64aa90b63ee49bca05c45f495f4f5671be59fa98631657c60967f28076`  
		Last Modified: Fri, 31 Jan 2025 06:26:00 GMT  
		Size: 289.1 MB (289123479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81aa306e301b86cf896fdf8d2d145fdc68659c9ed56cad3ecc7db62c8d63dae`  
		Last Modified: Fri, 31 Jan 2025 06:25:53 GMT  
		Size: 551.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680f993856df2bb099b85345cdf1749b81d79428676a98f262afc01627c86b1c`  
		Last Modified: Fri, 31 Jan 2025 06:25:53 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff865023c18da52df5a02e421a11a4eeef431396c7be4fba14295fb169e2d3b`  
		Last Modified: Fri, 31 Jan 2025 06:25:54 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:fc9d5042d3382526cb9a2c13442da2ec4b7d9e875f6bd58247fe73d274abe161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4719013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a99371d9a642755c507f039430208525bf1e1e071af55ecc045b25318c7e74`

```dockerfile
```

-	Layers:
	-	`sha256:79dbcd3a543e09ecdd2f6dd63f975128d81220fb6ff9382b9312331b49388abd`  
		Last Modified: Fri, 31 Jan 2025 06:25:54 GMT  
		Size: 4.7 MB (4693179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a39e3b6b12071113d382aa0fa2d4699b72073e309e3e4dbc7538a4be3076f48`  
		Last Modified: Fri, 31 Jan 2025 06:25:53 GMT  
		Size: 25.8 KB (25834 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.2`

```console
$ docker pull geonetwork@sha256:054805bcfe33791038aeba6af2c1f9bc234772d63501dc2eb1d6c07b1f820cb4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:4.2` - linux; amd64

```console
$ docker pull geonetwork@sha256:e4c18e6512e30f23d91a0a86bce7c559b15f6d77577c1ecdf7496b6a2c893d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.2 MB (415243764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7509637536b7bc6819d23cedcaa55559fccad2cb449bf06ad17ab2288698e4a2`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Oct 2024 11:02:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 11:02:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Oct 2024 11:02:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 24 Oct 2024 11:02:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JETTY_VERSION=9.4.57.v20241219
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 24 Oct 2024 11:02:49 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 24 Oct 2024 11:02:49 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.57.v20241219/jetty-home-9.4.57.v20241219.tar.gz
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 24 Oct 2024 11:02:49 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
WORKDIR /var/lib/jetty
# Thu, 24 Oct 2024 11:02:49 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
USER jetty
# Thu, 24 Oct 2024 11:02:49 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 24 Oct 2024 11:02:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 24 Oct 2024 11:02:49 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 24 Oct 2024 11:02:49 GMT
ENV DATA_DIR=/catalogue-data
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Thu, 24 Oct 2024 11:02:49 GMT
USER root
# Thu, 24 Oct 2024 11:02:49 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
USER jetty
# Thu, 24 Oct 2024 11:02:49 GMT
ENV GN_FILE=geonetwork.war
# Thu, 24 Oct 2024 11:02:49 GMT
ENV GN_VERSION=4.2.11
# Thu, 24 Oct 2024 11:02:49 GMT
ENV GN_DOWNLOAD_MD5=3d04a0d032354034b58aad689735829c
# Thu, 24 Oct 2024 11:02:49 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Thu, 24 Oct 2024 11:02:49 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 24 Oct 2024 11:02:49 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736914ed604909486ca1980aa7b186717adddcfe25f28e3666e4c1e5946430fa`  
		Last Modified: Fri, 31 Jan 2025 01:29:40 GMT  
		Size: 20.3 MB (20251205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af6a6fc29da83ffbb26cbf026cc38b929d37f46d627da4435bfbb490407da1a`  
		Last Modified: Fri, 31 Jan 2025 01:29:41 GMT  
		Size: 54.7 MB (54722218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea49627b2936faf3b2b48d821266f89e3471ce8dbeee974c18bfb09103361cbf`  
		Last Modified: Fri, 31 Jan 2025 01:29:40 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f80771ae776ef9edec8befd7b8a77e535f88b02dd8c9c2b1b99ff58001a3ac3`  
		Last Modified: Fri, 31 Jan 2025 01:29:40 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2d61c366107443a000c9a72db5b62001af2eca91dc0e39b7b92da60cf249de`  
		Last Modified: Fri, 31 Jan 2025 02:14:41 GMT  
		Size: 10.3 MB (10299700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2213bfd366e20ffbe2c992ae08a37260534d020a4a5192d4cbc5979f92b01b9d`  
		Last Modified: Fri, 31 Jan 2025 02:14:41 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b468999b1c9c4d5ae8d371888ee4866f0251400cbe55612a8f0498cee0ee4b97`  
		Last Modified: Fri, 31 Jan 2025 03:13:42 GMT  
		Size: 254.4 KB (254383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ca637fb77c4461bbcb419883138b2609c473fe0e47ddfc9d461988e7c4fd59`  
		Last Modified: Fri, 31 Jan 2025 03:13:51 GMT  
		Size: 302.2 MB (302200099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4980298ad6fff3e0fd2ebf873ea97d4e097433da350109e16a52f7c11066b6e9`  
		Last Modified: Fri, 31 Jan 2025 03:13:41 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2` - unknown; unknown

```console
$ docker pull geonetwork@sha256:14078614075191f9cc654c6136deb6bd562f21d2a86e343d0bf17b7b27c2102c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c958725fe25ed2772f9e33b4bf87a6fcd4fc576d3f16ef13c4a321d27b4746`

```dockerfile
```

-	Layers:
	-	`sha256:e9fd7b3bf8c42cd7f07fc14014874f91632a24cb509adc22ccd26d6df2f64955`  
		Last Modified: Fri, 31 Jan 2025 03:13:41 GMT  
		Size: 5.0 MB (4951945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1117ccc1f8777b26d43bed9f8fa829d3583aea42d5f9b6ec1a04b28f038bf53e`  
		Last Modified: Fri, 31 Jan 2025 03:13:41 GMT  
		Size: 18.7 KB (18712 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.2` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:af6405d268ee329fe9a7f8274c5ed175622df6711f7e9cd073620db6c90b300c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.7 MB (412653220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de91757cad9e3295a11d57dc5c591f52bdfba306da28c6dbe2ef84f61163301`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Oct 2024 11:02:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 11:02:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Oct 2024 11:02:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 24 Oct 2024 11:02:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JETTY_VERSION=9.4.57.v20241219
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 24 Oct 2024 11:02:49 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 24 Oct 2024 11:02:49 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.57.v20241219/jetty-home-9.4.57.v20241219.tar.gz
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 24 Oct 2024 11:02:49 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
WORKDIR /var/lib/jetty
# Thu, 24 Oct 2024 11:02:49 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
USER jetty
# Thu, 24 Oct 2024 11:02:49 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 24 Oct 2024 11:02:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 24 Oct 2024 11:02:49 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 24 Oct 2024 11:02:49 GMT
ENV DATA_DIR=/catalogue-data
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Thu, 24 Oct 2024 11:02:49 GMT
USER root
# Thu, 24 Oct 2024 11:02:49 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
USER jetty
# Thu, 24 Oct 2024 11:02:49 GMT
ENV GN_FILE=geonetwork.war
# Thu, 24 Oct 2024 11:02:49 GMT
ENV GN_VERSION=4.2.11
# Thu, 24 Oct 2024 11:02:49 GMT
ENV GN_DOWNLOAD_MD5=3d04a0d032354034b58aad689735829c
# Thu, 24 Oct 2024 11:02:49 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Thu, 24 Oct 2024 11:02:49 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 24 Oct 2024 11:02:49 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7232184dfd406ed5b54e851a280bd7323b4701402a9406613f30c349c9bd4067`  
		Last Modified: Fri, 31 Jan 2025 01:31:05 GMT  
		Size: 53.8 MB (53827736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8e7a9d07a5550096d72bd6f01a2e7ac4d6573d0271dfef0d0eb4c25347615f`  
		Last Modified: Fri, 31 Jan 2025 01:31:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59fadb503713a054d231da462f0785d432bd94db269c05d507788edfb27bdf64`  
		Last Modified: Fri, 31 Jan 2025 01:31:04 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fb211f810759b32ccf119a4e3bf16820464bd0c50bbae4d121acc86b861caa`  
		Last Modified: Fri, 31 Jan 2025 03:04:44 GMT  
		Size: 10.3 MB (10299538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37213f5c537af8946c73645592d86765ea988522b196712e3ac5dbc37fdcd7b`  
		Last Modified: Fri, 31 Jan 2025 03:04:43 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e831d82bb6dfcf4e30002cb2041193aedb2316448ca912ca80c9bf477d0519ba`  
		Last Modified: Fri, 31 Jan 2025 06:24:36 GMT  
		Size: 252.3 KB (252264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7145d11260c830136dda387c648e8648d55c42d70c2eb1293b7e583b7cf2146`  
		Last Modified: Fri, 31 Jan 2025 06:24:44 GMT  
		Size: 302.2 MB (302200131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d9971c6c3e3a149e55faf328ab7239ff8487886b4acc9b39029b26afa9c9fe`  
		Last Modified: Fri, 31 Jan 2025 06:24:36 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2` - unknown; unknown

```console
$ docker pull geonetwork@sha256:aa266403c1a3b04502d75123c0e63295a55fb31be2b785c7d974f4304aaed2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4972962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc806736dbbb36d6437d72cfab2c6c3b9416638e7923cbd3cc74c8f3b8db331`

```dockerfile
```

-	Layers:
	-	`sha256:89642cc1c554ec5771f7ff64c7625a7cfa3089dbe6c8f10d5c1721008b0e8813`  
		Last Modified: Fri, 31 Jan 2025 06:24:36 GMT  
		Size: 5.0 MB (4954155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2eddecc61d2b295bddd06bf2eb62e29432e942b13aaf469c6ae48ad774906aa`  
		Last Modified: Fri, 31 Jan 2025 06:24:35 GMT  
		Size: 18.8 KB (18807 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.2.11`

```console
$ docker pull geonetwork@sha256:054805bcfe33791038aeba6af2c1f9bc234772d63501dc2eb1d6c07b1f820cb4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:4.2.11` - linux; amd64

```console
$ docker pull geonetwork@sha256:e4c18e6512e30f23d91a0a86bce7c559b15f6d77577c1ecdf7496b6a2c893d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.2 MB (415243764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7509637536b7bc6819d23cedcaa55559fccad2cb449bf06ad17ab2288698e4a2`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Oct 2024 11:02:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 11:02:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Oct 2024 11:02:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 24 Oct 2024 11:02:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JETTY_VERSION=9.4.57.v20241219
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 24 Oct 2024 11:02:49 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 24 Oct 2024 11:02:49 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.57.v20241219/jetty-home-9.4.57.v20241219.tar.gz
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 24 Oct 2024 11:02:49 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
WORKDIR /var/lib/jetty
# Thu, 24 Oct 2024 11:02:49 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
USER jetty
# Thu, 24 Oct 2024 11:02:49 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 24 Oct 2024 11:02:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 24 Oct 2024 11:02:49 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 24 Oct 2024 11:02:49 GMT
ENV DATA_DIR=/catalogue-data
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Thu, 24 Oct 2024 11:02:49 GMT
USER root
# Thu, 24 Oct 2024 11:02:49 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
USER jetty
# Thu, 24 Oct 2024 11:02:49 GMT
ENV GN_FILE=geonetwork.war
# Thu, 24 Oct 2024 11:02:49 GMT
ENV GN_VERSION=4.2.11
# Thu, 24 Oct 2024 11:02:49 GMT
ENV GN_DOWNLOAD_MD5=3d04a0d032354034b58aad689735829c
# Thu, 24 Oct 2024 11:02:49 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Thu, 24 Oct 2024 11:02:49 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 24 Oct 2024 11:02:49 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736914ed604909486ca1980aa7b186717adddcfe25f28e3666e4c1e5946430fa`  
		Last Modified: Fri, 31 Jan 2025 01:29:40 GMT  
		Size: 20.3 MB (20251205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af6a6fc29da83ffbb26cbf026cc38b929d37f46d627da4435bfbb490407da1a`  
		Last Modified: Fri, 31 Jan 2025 01:29:41 GMT  
		Size: 54.7 MB (54722218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea49627b2936faf3b2b48d821266f89e3471ce8dbeee974c18bfb09103361cbf`  
		Last Modified: Fri, 31 Jan 2025 01:29:40 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f80771ae776ef9edec8befd7b8a77e535f88b02dd8c9c2b1b99ff58001a3ac3`  
		Last Modified: Fri, 31 Jan 2025 01:29:40 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2d61c366107443a000c9a72db5b62001af2eca91dc0e39b7b92da60cf249de`  
		Last Modified: Fri, 31 Jan 2025 02:14:41 GMT  
		Size: 10.3 MB (10299700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2213bfd366e20ffbe2c992ae08a37260534d020a4a5192d4cbc5979f92b01b9d`  
		Last Modified: Fri, 31 Jan 2025 02:14:41 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b468999b1c9c4d5ae8d371888ee4866f0251400cbe55612a8f0498cee0ee4b97`  
		Last Modified: Fri, 31 Jan 2025 03:13:42 GMT  
		Size: 254.4 KB (254383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ca637fb77c4461bbcb419883138b2609c473fe0e47ddfc9d461988e7c4fd59`  
		Last Modified: Fri, 31 Jan 2025 03:13:51 GMT  
		Size: 302.2 MB (302200099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4980298ad6fff3e0fd2ebf873ea97d4e097433da350109e16a52f7c11066b6e9`  
		Last Modified: Fri, 31 Jan 2025 03:13:41 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2.11` - unknown; unknown

```console
$ docker pull geonetwork@sha256:14078614075191f9cc654c6136deb6bd562f21d2a86e343d0bf17b7b27c2102c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c958725fe25ed2772f9e33b4bf87a6fcd4fc576d3f16ef13c4a321d27b4746`

```dockerfile
```

-	Layers:
	-	`sha256:e9fd7b3bf8c42cd7f07fc14014874f91632a24cb509adc22ccd26d6df2f64955`  
		Last Modified: Fri, 31 Jan 2025 03:13:41 GMT  
		Size: 5.0 MB (4951945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1117ccc1f8777b26d43bed9f8fa829d3583aea42d5f9b6ec1a04b28f038bf53e`  
		Last Modified: Fri, 31 Jan 2025 03:13:41 GMT  
		Size: 18.7 KB (18712 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.2.11` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:af6405d268ee329fe9a7f8274c5ed175622df6711f7e9cd073620db6c90b300c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.7 MB (412653220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de91757cad9e3295a11d57dc5c591f52bdfba306da28c6dbe2ef84f61163301`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Oct 2024 11:02:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 11:02:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Oct 2024 11:02:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 24 Oct 2024 11:02:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='c555750ee41799d30553bd9744c1ab9b8e6b2a2ea83195619a11ef30cc4154f4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JETTY_VERSION=9.4.57.v20241219
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 24 Oct 2024 11:02:49 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 24 Oct 2024 11:02:49 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.57.v20241219/jetty-home-9.4.57.v20241219.tar.gz
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 24 Oct 2024 11:02:49 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
WORKDIR /var/lib/jetty
# Thu, 24 Oct 2024 11:02:49 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
USER jetty
# Thu, 24 Oct 2024 11:02:49 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 24 Oct 2024 11:02:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 24 Oct 2024 11:02:49 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 24 Oct 2024 11:02:49 GMT
ENV DATA_DIR=/catalogue-data
# Thu, 24 Oct 2024 11:02:49 GMT
ENV JAVA_OPTS=-Dorg.eclipse.jetty.annotations.AnnotationParser.LEVEL=OFF         -Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/var/lib/jetty/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Thu, 24 Oct 2024 11:02:49 GMT
USER root
# Thu, 24 Oct 2024 11:02:49 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /var/lib/jetty/webapps/geonetwork &&     chown -R jetty:jetty /var/lib/jetty/webapps/geonetwork # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
USER jetty
# Thu, 24 Oct 2024 11:02:49 GMT
ENV GN_FILE=geonetwork.war
# Thu, 24 Oct 2024 11:02:49 GMT
ENV GN_VERSION=4.2.11
# Thu, 24 Oct 2024 11:02:49 GMT
ENV GN_DOWNLOAD_MD5=3d04a0d032354034b58aad689735829c
# Thu, 24 Oct 2024 11:02:49 GMT
RUN cd /var/lib/jetty/webapps/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Thu, 24 Oct 2024 11:02:49 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Thu, 24 Oct 2024 11:02:49 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 24 Oct 2024 11:02:49 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7232184dfd406ed5b54e851a280bd7323b4701402a9406613f30c349c9bd4067`  
		Last Modified: Fri, 31 Jan 2025 01:31:05 GMT  
		Size: 53.8 MB (53827736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8e7a9d07a5550096d72bd6f01a2e7ac4d6573d0271dfef0d0eb4c25347615f`  
		Last Modified: Fri, 31 Jan 2025 01:31:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59fadb503713a054d231da462f0785d432bd94db269c05d507788edfb27bdf64`  
		Last Modified: Fri, 31 Jan 2025 01:31:04 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fb211f810759b32ccf119a4e3bf16820464bd0c50bbae4d121acc86b861caa`  
		Last Modified: Fri, 31 Jan 2025 03:04:44 GMT  
		Size: 10.3 MB (10299538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37213f5c537af8946c73645592d86765ea988522b196712e3ac5dbc37fdcd7b`  
		Last Modified: Fri, 31 Jan 2025 03:04:43 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e831d82bb6dfcf4e30002cb2041193aedb2316448ca912ca80c9bf477d0519ba`  
		Last Modified: Fri, 31 Jan 2025 06:24:36 GMT  
		Size: 252.3 KB (252264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7145d11260c830136dda387c648e8648d55c42d70c2eb1293b7e583b7cf2146`  
		Last Modified: Fri, 31 Jan 2025 06:24:44 GMT  
		Size: 302.2 MB (302200131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d9971c6c3e3a149e55faf328ab7239ff8487886b4acc9b39029b26afa9c9fe`  
		Last Modified: Fri, 31 Jan 2025 06:24:36 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2.11` - unknown; unknown

```console
$ docker pull geonetwork@sha256:aa266403c1a3b04502d75123c0e63295a55fb31be2b785c7d974f4304aaed2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4972962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc806736dbbb36d6437d72cfab2c6c3b9416638e7923cbd3cc74c8f3b8db331`

```dockerfile
```

-	Layers:
	-	`sha256:89642cc1c554ec5771f7ff64c7625a7cfa3089dbe6c8f10d5c1721008b0e8813`  
		Last Modified: Fri, 31 Jan 2025 06:24:36 GMT  
		Size: 5.0 MB (4954155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2eddecc61d2b295bddd06bf2eb62e29432e942b13aaf469c6ae48ad774906aa`  
		Last Modified: Fri, 31 Jan 2025 06:24:35 GMT  
		Size: 18.8 KB (18807 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.4`

```console
$ docker pull geonetwork@sha256:de8edfec283b81c76bd3a7adc58bdff0ff57d48eba26b260bcc040a17a11e9ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:4.4` - linux; amd64

```console
$ docker pull geonetwork@sha256:c46a8cbe54433bc52ef223cb93d65ffbca08c857caaed020dd16b71768ea8c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.1 MB (493054297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04bfe6d405887cef9c8cb04f9e9de2d03ee190c20d54c913eef3e7104589cd2`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Oct 2024 11:20:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 11:20:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='79d574328f6960d40349996ef8c5949581f9e533dc76f134857c4125c78558ff';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Oct 2024 11:20:12 GMT
CMD ["jshell"]
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_VERSION=9.4.57.v20241219
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.57.v20241219/jetty-home-9.4.57.v20241219.tar.gz
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
WORKDIR /var/lib/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
USER jetty
# Thu, 24 Oct 2024 11:20:12 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 24 Oct 2024 11:20:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 24 Oct 2024 11:20:12 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 24 Oct 2024 11:20:12 GMT
ENV DATA_DIR=/catalogue-data
# Thu, 24 Oct 2024 11:20:12 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Thu, 24 Oct 2024 11:20:12 GMT
USER root
# Thu, 24 Oct 2024 11:20:12 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
USER jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_FILE=geonetwork.war
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_VERSION=4.4.6
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_DOWNLOAD_MD5=ad596d3348872506c78daa05edb14782
# Thu, 24 Oct 2024 11:20:12 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Thu, 24 Oct 2024 11:20:12 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 24 Oct 2024 11:20:12 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57720219966e918f1a532346498cfbfb342979a0f5ef1c523ba9e60e4ef5ab63`  
		Last Modified: Fri, 31 Jan 2025 01:30:17 GMT  
		Size: 20.3 MB (20251237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec2b4dbdfccae2f0821bf0672520a085237394280af05d3fa21c12397b754d0`  
		Last Modified: Fri, 31 Jan 2025 01:30:19 GMT  
		Size: 145.6 MB (145609067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae877ab777ef84fc2dae1668033dcb1343246ee291a5ff14fba9cf841202dff`  
		Last Modified: Fri, 31 Jan 2025 01:30:15 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7b6bd77aa73b02a876a07119cd314e85e8eb53687bb5153edd5e074e76a94`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ad00986e7c30ead99fef5802d9a4efbe8f1546cca93a1148026a22e743b9e2`  
		Last Modified: Fri, 31 Jan 2025 02:14:50 GMT  
		Size: 10.3 MB (10299713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7be791f756f430948ac42b83f87ed680794a78f83e76bb3e2951c3f82f1764e`  
		Last Modified: Fri, 31 Jan 2025 02:14:39 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c33c31bb10a6c2e6d4328e36915ea0e696d90a3531f480d41681ab3fedcca6f`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 254.4 KB (254351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40996a68fb9db773e3171dcc9a6da39ef6a5b513115eaca51fc3accf2bf4cebb`  
		Last Modified: Fri, 31 Jan 2025 03:12:44 GMT  
		Size: 289.1 MB (289123480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c0fae08b476dc0d5942cbcd81799c7c87c2909d8b07222e5bdda8947e1b25b`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 551.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a217fe03d135d2cb18223aea9add78499a414590b7f78a5d93d4ee74c016b3`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 568.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca2b4aa497fdd66ff0f245297c2bed0afdec7ce077a8bd98a76e797c8769920`  
		Last Modified: Fri, 31 Jan 2025 03:12:41 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:fcdea2617189080e1f2a9fa6c11001e06ac78b700c23638548057c0282877973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c46cd06ff58aee08c44b7d0e18129489db4b3283d55ddb858afd28bcbefc2f`

```dockerfile
```

-	Layers:
	-	`sha256:100255f77dbf0901761711d0a42bce8f2fdbf26e9fe6a605b7b44833cc24afeb`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 4.7 MB (4691021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9db15a999cbf82b93b3140fc01779fc48f5c68c027c08871ea62d5e1b0a63239`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 25.7 KB (25700 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:7c88ee544a39062628f8ed3a3e563aad8167664219838dbb535fd278ebf713f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.1 MB (488139632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04346d672fe5f872f51b6129bcfb6cc323c8af1c23a2b04434c52c4ce881585a`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Oct 2024 11:20:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 11:20:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='79d574328f6960d40349996ef8c5949581f9e533dc76f134857c4125c78558ff';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Oct 2024 11:20:12 GMT
CMD ["jshell"]
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_VERSION=9.4.57.v20241219
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.57.v20241219/jetty-home-9.4.57.v20241219.tar.gz
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
WORKDIR /var/lib/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
USER jetty
# Thu, 24 Oct 2024 11:20:12 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 24 Oct 2024 11:20:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 24 Oct 2024 11:20:12 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 24 Oct 2024 11:20:12 GMT
ENV DATA_DIR=/catalogue-data
# Thu, 24 Oct 2024 11:20:12 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Thu, 24 Oct 2024 11:20:12 GMT
USER root
# Thu, 24 Oct 2024 11:20:12 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
USER jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_FILE=geonetwork.war
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_VERSION=4.4.6
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_DOWNLOAD_MD5=ad596d3348872506c78daa05edb14782
# Thu, 24 Oct 2024 11:20:12 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Thu, 24 Oct 2024 11:20:12 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 24 Oct 2024 11:20:12 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c529ed0cdd6ba59828bb5288f63e6f174c4cbf1b5499595c7338b9b52066229`  
		Last Modified: Fri, 31 Jan 2025 01:35:16 GMT  
		Size: 142.4 MB (142390502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0628f645ce6b92ee9bbe4a6bb14c29263b9a0de9205b6250eb5a8ae122e196`  
		Last Modified: Fri, 31 Jan 2025 01:35:13 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948a71537099de96aed8d9ae3bf948c5d51700abaef7a8cb429b09e6579ab012`  
		Last Modified: Fri, 31 Jan 2025 01:35:13 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83cff723577cb2d244e05fdf013d80137c7dd0cf6ef4f02ad1e11bd3fefb38c`  
		Last Modified: Fri, 31 Jan 2025 03:06:30 GMT  
		Size: 10.3 MB (10299567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d408fec3bd3fb508fbd995fe95df3755475bcc84339224a7931421eeb829aba9`  
		Last Modified: Fri, 31 Jan 2025 03:06:29 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdc1dc019a7debf2fd24e2ac298ab62e6fd2b3c6773f96180a1a9be8009849c`  
		Last Modified: Fri, 31 Jan 2025 06:25:53 GMT  
		Size: 252.2 KB (252232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6006f64aa90b63ee49bca05c45f495f4f5671be59fa98631657c60967f28076`  
		Last Modified: Fri, 31 Jan 2025 06:26:00 GMT  
		Size: 289.1 MB (289123479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81aa306e301b86cf896fdf8d2d145fdc68659c9ed56cad3ecc7db62c8d63dae`  
		Last Modified: Fri, 31 Jan 2025 06:25:53 GMT  
		Size: 551.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680f993856df2bb099b85345cdf1749b81d79428676a98f262afc01627c86b1c`  
		Last Modified: Fri, 31 Jan 2025 06:25:53 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff865023c18da52df5a02e421a11a4eeef431396c7be4fba14295fb169e2d3b`  
		Last Modified: Fri, 31 Jan 2025 06:25:54 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:fc9d5042d3382526cb9a2c13442da2ec4b7d9e875f6bd58247fe73d274abe161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4719013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a99371d9a642755c507f039430208525bf1e1e071af55ecc045b25318c7e74`

```dockerfile
```

-	Layers:
	-	`sha256:79dbcd3a543e09ecdd2f6dd63f975128d81220fb6ff9382b9312331b49388abd`  
		Last Modified: Fri, 31 Jan 2025 06:25:54 GMT  
		Size: 4.7 MB (4693179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a39e3b6b12071113d382aa0fa2d4699b72073e309e3e4dbc7538a4be3076f48`  
		Last Modified: Fri, 31 Jan 2025 06:25:53 GMT  
		Size: 25.8 KB (25834 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.4.6`

```console
$ docker pull geonetwork@sha256:de8edfec283b81c76bd3a7adc58bdff0ff57d48eba26b260bcc040a17a11e9ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:4.4.6` - linux; amd64

```console
$ docker pull geonetwork@sha256:c46a8cbe54433bc52ef223cb93d65ffbca08c857caaed020dd16b71768ea8c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.1 MB (493054297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04bfe6d405887cef9c8cb04f9e9de2d03ee190c20d54c913eef3e7104589cd2`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Oct 2024 11:20:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 11:20:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='79d574328f6960d40349996ef8c5949581f9e533dc76f134857c4125c78558ff';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Oct 2024 11:20:12 GMT
CMD ["jshell"]
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_VERSION=9.4.57.v20241219
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.57.v20241219/jetty-home-9.4.57.v20241219.tar.gz
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
WORKDIR /var/lib/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
USER jetty
# Thu, 24 Oct 2024 11:20:12 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 24 Oct 2024 11:20:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 24 Oct 2024 11:20:12 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 24 Oct 2024 11:20:12 GMT
ENV DATA_DIR=/catalogue-data
# Thu, 24 Oct 2024 11:20:12 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Thu, 24 Oct 2024 11:20:12 GMT
USER root
# Thu, 24 Oct 2024 11:20:12 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
USER jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_FILE=geonetwork.war
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_VERSION=4.4.6
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_DOWNLOAD_MD5=ad596d3348872506c78daa05edb14782
# Thu, 24 Oct 2024 11:20:12 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Thu, 24 Oct 2024 11:20:12 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 24 Oct 2024 11:20:12 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57720219966e918f1a532346498cfbfb342979a0f5ef1c523ba9e60e4ef5ab63`  
		Last Modified: Fri, 31 Jan 2025 01:30:17 GMT  
		Size: 20.3 MB (20251237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec2b4dbdfccae2f0821bf0672520a085237394280af05d3fa21c12397b754d0`  
		Last Modified: Fri, 31 Jan 2025 01:30:19 GMT  
		Size: 145.6 MB (145609067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae877ab777ef84fc2dae1668033dcb1343246ee291a5ff14fba9cf841202dff`  
		Last Modified: Fri, 31 Jan 2025 01:30:15 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7b6bd77aa73b02a876a07119cd314e85e8eb53687bb5153edd5e074e76a94`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ad00986e7c30ead99fef5802d9a4efbe8f1546cca93a1148026a22e743b9e2`  
		Last Modified: Fri, 31 Jan 2025 02:14:50 GMT  
		Size: 10.3 MB (10299713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7be791f756f430948ac42b83f87ed680794a78f83e76bb3e2951c3f82f1764e`  
		Last Modified: Fri, 31 Jan 2025 02:14:39 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c33c31bb10a6c2e6d4328e36915ea0e696d90a3531f480d41681ab3fedcca6f`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 254.4 KB (254351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40996a68fb9db773e3171dcc9a6da39ef6a5b513115eaca51fc3accf2bf4cebb`  
		Last Modified: Fri, 31 Jan 2025 03:12:44 GMT  
		Size: 289.1 MB (289123480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c0fae08b476dc0d5942cbcd81799c7c87c2909d8b07222e5bdda8947e1b25b`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 551.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a217fe03d135d2cb18223aea9add78499a414590b7f78a5d93d4ee74c016b3`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 568.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca2b4aa497fdd66ff0f245297c2bed0afdec7ce077a8bd98a76e797c8769920`  
		Last Modified: Fri, 31 Jan 2025 03:12:41 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4.6` - unknown; unknown

```console
$ docker pull geonetwork@sha256:fcdea2617189080e1f2a9fa6c11001e06ac78b700c23638548057c0282877973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c46cd06ff58aee08c44b7d0e18129489db4b3283d55ddb858afd28bcbefc2f`

```dockerfile
```

-	Layers:
	-	`sha256:100255f77dbf0901761711d0a42bce8f2fdbf26e9fe6a605b7b44833cc24afeb`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 4.7 MB (4691021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9db15a999cbf82b93b3140fc01779fc48f5c68c027c08871ea62d5e1b0a63239`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 25.7 KB (25700 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4.6` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:7c88ee544a39062628f8ed3a3e563aad8167664219838dbb535fd278ebf713f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.1 MB (488139632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04346d672fe5f872f51b6129bcfb6cc323c8af1c23a2b04434c52c4ce881585a`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Oct 2024 11:20:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 11:20:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='79d574328f6960d40349996ef8c5949581f9e533dc76f134857c4125c78558ff';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Oct 2024 11:20:12 GMT
CMD ["jshell"]
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_VERSION=9.4.57.v20241219
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.57.v20241219/jetty-home-9.4.57.v20241219.tar.gz
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
WORKDIR /var/lib/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
USER jetty
# Thu, 24 Oct 2024 11:20:12 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 24 Oct 2024 11:20:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 24 Oct 2024 11:20:12 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 24 Oct 2024 11:20:12 GMT
ENV DATA_DIR=/catalogue-data
# Thu, 24 Oct 2024 11:20:12 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Thu, 24 Oct 2024 11:20:12 GMT
USER root
# Thu, 24 Oct 2024 11:20:12 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
USER jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_FILE=geonetwork.war
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_VERSION=4.4.6
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_DOWNLOAD_MD5=ad596d3348872506c78daa05edb14782
# Thu, 24 Oct 2024 11:20:12 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Thu, 24 Oct 2024 11:20:12 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 24 Oct 2024 11:20:12 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c529ed0cdd6ba59828bb5288f63e6f174c4cbf1b5499595c7338b9b52066229`  
		Last Modified: Fri, 31 Jan 2025 01:35:16 GMT  
		Size: 142.4 MB (142390502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0628f645ce6b92ee9bbe4a6bb14c29263b9a0de9205b6250eb5a8ae122e196`  
		Last Modified: Fri, 31 Jan 2025 01:35:13 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948a71537099de96aed8d9ae3bf948c5d51700abaef7a8cb429b09e6579ab012`  
		Last Modified: Fri, 31 Jan 2025 01:35:13 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83cff723577cb2d244e05fdf013d80137c7dd0cf6ef4f02ad1e11bd3fefb38c`  
		Last Modified: Fri, 31 Jan 2025 03:06:30 GMT  
		Size: 10.3 MB (10299567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d408fec3bd3fb508fbd995fe95df3755475bcc84339224a7931421eeb829aba9`  
		Last Modified: Fri, 31 Jan 2025 03:06:29 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdc1dc019a7debf2fd24e2ac298ab62e6fd2b3c6773f96180a1a9be8009849c`  
		Last Modified: Fri, 31 Jan 2025 06:25:53 GMT  
		Size: 252.2 KB (252232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6006f64aa90b63ee49bca05c45f495f4f5671be59fa98631657c60967f28076`  
		Last Modified: Fri, 31 Jan 2025 06:26:00 GMT  
		Size: 289.1 MB (289123479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81aa306e301b86cf896fdf8d2d145fdc68659c9ed56cad3ecc7db62c8d63dae`  
		Last Modified: Fri, 31 Jan 2025 06:25:53 GMT  
		Size: 551.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680f993856df2bb099b85345cdf1749b81d79428676a98f262afc01627c86b1c`  
		Last Modified: Fri, 31 Jan 2025 06:25:53 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff865023c18da52df5a02e421a11a4eeef431396c7be4fba14295fb169e2d3b`  
		Last Modified: Fri, 31 Jan 2025 06:25:54 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4.6` - unknown; unknown

```console
$ docker pull geonetwork@sha256:fc9d5042d3382526cb9a2c13442da2ec4b7d9e875f6bd58247fe73d274abe161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4719013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a99371d9a642755c507f039430208525bf1e1e071af55ecc045b25318c7e74`

```dockerfile
```

-	Layers:
	-	`sha256:79dbcd3a543e09ecdd2f6dd63f975128d81220fb6ff9382b9312331b49388abd`  
		Last Modified: Fri, 31 Jan 2025 06:25:54 GMT  
		Size: 4.7 MB (4693179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a39e3b6b12071113d382aa0fa2d4699b72073e309e3e4dbc7538a4be3076f48`  
		Last Modified: Fri, 31 Jan 2025 06:25:53 GMT  
		Size: 25.8 KB (25834 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:latest`

```console
$ docker pull geonetwork@sha256:de8edfec283b81c76bd3a7adc58bdff0ff57d48eba26b260bcc040a17a11e9ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `geonetwork:latest` - linux; amd64

```console
$ docker pull geonetwork@sha256:c46a8cbe54433bc52ef223cb93d65ffbca08c857caaed020dd16b71768ea8c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.1 MB (493054297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04bfe6d405887cef9c8cb04f9e9de2d03ee190c20d54c913eef3e7104589cd2`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Oct 2024 11:20:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 11:20:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='79d574328f6960d40349996ef8c5949581f9e533dc76f134857c4125c78558ff';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Oct 2024 11:20:12 GMT
CMD ["jshell"]
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_VERSION=9.4.57.v20241219
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.57.v20241219/jetty-home-9.4.57.v20241219.tar.gz
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
WORKDIR /var/lib/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
USER jetty
# Thu, 24 Oct 2024 11:20:12 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 24 Oct 2024 11:20:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 24 Oct 2024 11:20:12 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 24 Oct 2024 11:20:12 GMT
ENV DATA_DIR=/catalogue-data
# Thu, 24 Oct 2024 11:20:12 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Thu, 24 Oct 2024 11:20:12 GMT
USER root
# Thu, 24 Oct 2024 11:20:12 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
USER jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_FILE=geonetwork.war
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_VERSION=4.4.6
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_DOWNLOAD_MD5=ad596d3348872506c78daa05edb14782
# Thu, 24 Oct 2024 11:20:12 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Thu, 24 Oct 2024 11:20:12 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 24 Oct 2024 11:20:12 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57720219966e918f1a532346498cfbfb342979a0f5ef1c523ba9e60e4ef5ab63`  
		Last Modified: Fri, 31 Jan 2025 01:30:17 GMT  
		Size: 20.3 MB (20251237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec2b4dbdfccae2f0821bf0672520a085237394280af05d3fa21c12397b754d0`  
		Last Modified: Fri, 31 Jan 2025 01:30:19 GMT  
		Size: 145.6 MB (145609067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae877ab777ef84fc2dae1668033dcb1343246ee291a5ff14fba9cf841202dff`  
		Last Modified: Fri, 31 Jan 2025 01:30:15 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7b6bd77aa73b02a876a07119cd314e85e8eb53687bb5153edd5e074e76a94`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ad00986e7c30ead99fef5802d9a4efbe8f1546cca93a1148026a22e743b9e2`  
		Last Modified: Fri, 31 Jan 2025 02:14:50 GMT  
		Size: 10.3 MB (10299713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7be791f756f430948ac42b83f87ed680794a78f83e76bb3e2951c3f82f1764e`  
		Last Modified: Fri, 31 Jan 2025 02:14:39 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c33c31bb10a6c2e6d4328e36915ea0e696d90a3531f480d41681ab3fedcca6f`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 254.4 KB (254351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40996a68fb9db773e3171dcc9a6da39ef6a5b513115eaca51fc3accf2bf4cebb`  
		Last Modified: Fri, 31 Jan 2025 03:12:44 GMT  
		Size: 289.1 MB (289123480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c0fae08b476dc0d5942cbcd81799c7c87c2909d8b07222e5bdda8947e1b25b`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 551.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a217fe03d135d2cb18223aea9add78499a414590b7f78a5d93d4ee74c016b3`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 568.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca2b4aa497fdd66ff0f245297c2bed0afdec7ce077a8bd98a76e797c8769920`  
		Last Modified: Fri, 31 Jan 2025 03:12:41 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:latest` - unknown; unknown

```console
$ docker pull geonetwork@sha256:fcdea2617189080e1f2a9fa6c11001e06ac78b700c23638548057c0282877973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4716721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c46cd06ff58aee08c44b7d0e18129489db4b3283d55ddb858afd28bcbefc2f`

```dockerfile
```

-	Layers:
	-	`sha256:100255f77dbf0901761711d0a42bce8f2fdbf26e9fe6a605b7b44833cc24afeb`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 4.7 MB (4691021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9db15a999cbf82b93b3140fc01779fc48f5c68c027c08871ea62d5e1b0a63239`  
		Last Modified: Fri, 31 Jan 2025 03:12:40 GMT  
		Size: 25.7 KB (25700 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:latest` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:7c88ee544a39062628f8ed3a3e563aad8167664219838dbb535fd278ebf713f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.1 MB (488139632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04346d672fe5f872f51b6129bcfb6cc323c8af1c23a2b04434c52c4ce881585a`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 24 Oct 2024 11:20:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 11:20:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='79d574328f6960d40349996ef8c5949581f9e533dc76f134857c4125c78558ff';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 24 Oct 2024 11:20:12 GMT
CMD ["jshell"]
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_VERSION=9.4.57.v20241219
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.57.v20241219/jetty-home-9.4.57.v20241219.tar.gz
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
WORKDIR /var/lib/jetty
# Thu, 24 Oct 2024 11:20:12 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
USER jetty
# Thu, 24 Oct 2024 11:20:12 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 24 Oct 2024 11:20:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 24 Oct 2024 11:20:12 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 24 Oct 2024 11:20:12 GMT
ENV DATA_DIR=/catalogue-data
# Thu, 24 Oct 2024 11:20:12 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Thu, 24 Oct 2024 11:20:12 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Thu, 24 Oct 2024 11:20:12 GMT
USER root
# Thu, 24 Oct 2024 11:20:12 GMT
RUN apt-get -y update &&     apt-get -y install --no-install-recommends         curl         unzip &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p ${DATA_DIR} &&     chown -R jetty:jetty ${DATA_DIR} &&     mkdir -p /opt/geonetwork &&     chown -R jetty:jetty /opt/geonetwork # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
USER jetty
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_FILE=geonetwork.war
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_VERSION=4.4.6
# Thu, 24 Oct 2024 11:20:12 GMT
ENV GN_DOWNLOAD_MD5=ad596d3348872506c78daa05edb14782
# Thu, 24 Oct 2024 11:20:12 GMT
RUN cd /opt/geonetwork/ &&      curl -fSL -o geonetwork.war      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c &&      unzip -q geonetwork.war &&      rm geonetwork.war # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
COPY jetty/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
RUN java -jar /usr/local/jetty/start.jar --create-startd --add-module=http-forwarded # buildkit
# Thu, 24 Oct 2024 11:20:12 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Thu, 24 Oct 2024 11:20:12 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
# Thu, 24 Oct 2024 11:20:12 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c529ed0cdd6ba59828bb5288f63e6f174c4cbf1b5499595c7338b9b52066229`  
		Last Modified: Fri, 31 Jan 2025 01:35:16 GMT  
		Size: 142.4 MB (142390502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0628f645ce6b92ee9bbe4a6bb14c29263b9a0de9205b6250eb5a8ae122e196`  
		Last Modified: Fri, 31 Jan 2025 01:35:13 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948a71537099de96aed8d9ae3bf948c5d51700abaef7a8cb429b09e6579ab012`  
		Last Modified: Fri, 31 Jan 2025 01:35:13 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83cff723577cb2d244e05fdf013d80137c7dd0cf6ef4f02ad1e11bd3fefb38c`  
		Last Modified: Fri, 31 Jan 2025 03:06:30 GMT  
		Size: 10.3 MB (10299567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d408fec3bd3fb508fbd995fe95df3755475bcc84339224a7931421eeb829aba9`  
		Last Modified: Fri, 31 Jan 2025 03:06:29 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdc1dc019a7debf2fd24e2ac298ab62e6fd2b3c6773f96180a1a9be8009849c`  
		Last Modified: Fri, 31 Jan 2025 06:25:53 GMT  
		Size: 252.2 KB (252232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6006f64aa90b63ee49bca05c45f495f4f5671be59fa98631657c60967f28076`  
		Last Modified: Fri, 31 Jan 2025 06:26:00 GMT  
		Size: 289.1 MB (289123479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81aa306e301b86cf896fdf8d2d145fdc68659c9ed56cad3ecc7db62c8d63dae`  
		Last Modified: Fri, 31 Jan 2025 06:25:53 GMT  
		Size: 551.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680f993856df2bb099b85345cdf1749b81d79428676a98f262afc01627c86b1c`  
		Last Modified: Fri, 31 Jan 2025 06:25:53 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff865023c18da52df5a02e421a11a4eeef431396c7be4fba14295fb169e2d3b`  
		Last Modified: Fri, 31 Jan 2025 06:25:54 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:latest` - unknown; unknown

```console
$ docker pull geonetwork@sha256:fc9d5042d3382526cb9a2c13442da2ec4b7d9e875f6bd58247fe73d274abe161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4719013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a99371d9a642755c507f039430208525bf1e1e071af55ecc045b25318c7e74`

```dockerfile
```

-	Layers:
	-	`sha256:79dbcd3a543e09ecdd2f6dd63f975128d81220fb6ff9382b9312331b49388abd`  
		Last Modified: Fri, 31 Jan 2025 06:25:54 GMT  
		Size: 4.7 MB (4693179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a39e3b6b12071113d382aa0fa2d4699b72073e309e3e4dbc7538a4be3076f48`  
		Last Modified: Fri, 31 Jan 2025 06:25:53 GMT  
		Size: 25.8 KB (25834 bytes)  
		MIME: application/vnd.in-toto+json
