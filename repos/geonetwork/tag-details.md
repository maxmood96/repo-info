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
-	[`geonetwork:4.2.15`](#geonetwork4215)
-	[`geonetwork:4.4`](#geonetwork44)
-	[`geonetwork:4.4.10`](#geonetwork4410)
-	[`geonetwork:latest`](#geonetworklatest)

## `geonetwork:3`

```console
$ docker pull geonetwork@sha256:9789440b2725d089e764fc64e59d6bb47a61b4a517489d1d11c6ca64f041131d
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
$ docker pull geonetwork@sha256:4589e8d06b2ecf93cb5815577c48616d44ad7d18f7fe44f24322deb8806a64b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350966474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ab5c115067ba6f79ce1e888139ab5e95d1ee8ae4465282b7be1e9c3a2fa009`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:25:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:25:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:25:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:25:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:25:37 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:25:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:25:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:25:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:25:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 21:45:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 21:45:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:45:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 21:45:06 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 21:45:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:45:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:45:06 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 21:45:06 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 21:45:06 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 21:45:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 12 May 2026 21:45:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 21:45:31 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 21:45:31 GMT
ENTRYPOINT []
# Tue, 12 May 2026 21:45:31 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:11:37 GMT
ENV GN_FILE=geonetwork.war
# Tue, 12 May 2026 22:11:37 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 12 May 2026 22:11:37 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 12 May 2026 22:11:37 GMT
ENV GN_VERSION=3.12.12
# Tue, 12 May 2026 22:11:37 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 12 May 2026 22:11:37 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 12 May 2026 22:12:30 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 12 May 2026 22:12:30 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:12:30 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:12:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:12:30 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6468ff6de61997fbb57dae533eb5b211f02f4c796a195d654eb8f3f268e3b2d7`  
		Last Modified: Tue, 12 May 2026 21:25:54 GMT  
		Size: 17.0 MB (16984059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339c2234aca20e36345fe207e5f8bdf331d4faffd0bcfa8bfb0d3ea5f7247660`  
		Last Modified: Tue, 12 May 2026 21:25:55 GMT  
		Size: 55.2 MB (55200425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca9a652b5c28fcd17f575d8b27ceb1d8d26ee076a79f8d155096293533f766f`  
		Last Modified: Tue, 12 May 2026 21:25:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad155729b83d2b2c4c36d4ccad016d99690aa6c74d72f3ae29775904ff79d53`  
		Last Modified: Tue, 12 May 2026 21:25:53 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f37c125cbd268a3d67e091a1008d8b7371b3567bcbc0811a04492e7fe07dfc`  
		Last Modified: Tue, 12 May 2026 21:45:39 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f324bc94893300bd0727f8017cd10fc2dfaeb4b0425106df31069a4de32c8f1`  
		Last Modified: Tue, 12 May 2026 21:45:40 GMT  
		Size: 14.5 MB (14495571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5fe163481e5c8d68eaecfed72774c935e6b62eb9a47b916cf26d49877942b0`  
		Last Modified: Tue, 12 May 2026 22:12:56 GMT  
		Size: 234.6 MB (234550314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a1d54a67a655034ac0e70c8d30c249f3a5a48d97ebe208149a8f33ec131200`  
		Last Modified: Tue, 12 May 2026 22:12:51 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:2fbccdf3503145cd97f7b606589d24d93c2bc1e56bdb2c78d9ecba9de8cbd70e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4379489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4506ebd5b4d81a6eacafacbcf055817c350e9b0933da712a517b6b46e67d2af`

```dockerfile
```

-	Layers:
	-	`sha256:6f874835e97e4175c37330379d3f8b5c494a284a9cb6ba307799accd09e48901`  
		Last Modified: Tue, 12 May 2026 22:12:52 GMT  
		Size: 4.4 MB (4360396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef92e0f7e67c5f7a4e361412ca77a74d924c9f75f5de943d3303a5526c2ff4e0`  
		Last Modified: Tue, 12 May 2026 22:12:51 GMT  
		Size: 19.1 KB (19093 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:19cd503b643d3310e64af0cfe3c4657fd3ba9f613a0cdf2c58c3c28bdd3bed51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.2 MB (342191674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6693549d31e7ccf1533853dd3f6d1c08905141dffc290640c2a19fab2d2be89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:36:59 GMT
ARG RELEASE
# Wed, 20 May 2026 01:36:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:36:59 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:02 GMT
ADD file:6d117ff682b1d31146902ad551197b012e75561d62d92d029219fcbf5c493c35 in / 
# Wed, 20 May 2026 01:37:02 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:10:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:10:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:10:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:24 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:10:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:10:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:10:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:10:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 09:17:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 09:17:51 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 09:17:51 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 09:17:51 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 09:17:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:17:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:17:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 09:17:51 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 09:17:51 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 09:18:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Jun 2026 09:18:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 09:18:18 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 09:18:18 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 09:18:18 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 10:13:59 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 10:13:59 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Jun 2026 10:13:59 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 10:13:59 GMT
ENV GN_VERSION=3.12.12
# Tue, 02 Jun 2026 10:13:59 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 02 Jun 2026 10:13:59 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Jun 2026 10:16:36 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Jun 2026 10:16:36 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:16:36 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:16:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 10:16:36 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a2dede8d0e9ca179460cb274dab10c5c4b741cf1544b130df872809a4467e3e4`  
		Last Modified: Wed, 20 May 2026 02:15:37 GMT  
		Size: 26.9 MB (26859709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1d8b94ff08bb8b6de5b69ca5ebb6596cb3713544241d873713c2dd960f2ba9`  
		Last Modified: Tue, 02 Jun 2026 08:10:46 GMT  
		Size: 16.3 MB (16310665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd4cadfd61450b68b7ba220950558346f412256c24c92139b4a1eae532972bd`  
		Last Modified: Tue, 02 Jun 2026 08:10:47 GMT  
		Size: 50.5 MB (50541133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ca58a0a1017272272bdac970286540e1b6e4900ec0ee9e46940c06e120635b`  
		Last Modified: Tue, 02 Jun 2026 08:10:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d8e4ec41df605824c47490458a8ea88b9ed06e4c3cff7af3b9f72b4a04a075`  
		Last Modified: Tue, 02 Jun 2026 08:10:45 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d9988c7a00bfe4dd42888ef010c804f87de8652835b1e43d40afe028975477`  
		Last Modified: Tue, 02 Jun 2026 09:18:27 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7953c7fc5f8a3d6eba9a7df364349bd70a30e1fd7e43a3656f7cdbe1d41beb9e`  
		Last Modified: Tue, 02 Jun 2026 09:18:27 GMT  
		Size: 13.9 MB (13938429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048a8040985022fd6fdd3a200f3e51a1e7155e1ca4c634b32ec4cb28665e1c35`  
		Last Modified: Tue, 02 Jun 2026 10:17:02 GMT  
		Size: 234.5 MB (234538609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fb05d09b3a938bb05b5be8b380f57378b4891f0b3cc9a648f953fcb9fa96fa`  
		Last Modified: Tue, 02 Jun 2026 10:16:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:4e970d0d380879b736d0480f2fca912b641694f7ef6c2de1b18ceca9bfa4b4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94bf0c27ac5a13950a9a6f0823798593d9e5110b1680bcd888e008af39a7050`

```dockerfile
```

-	Layers:
	-	`sha256:3e6852aaa4f0736ea207a5be89a7e88e08f08a9c82b9e79d8f01eb445bc4903e`  
		Last Modified: Tue, 02 Jun 2026 10:16:57 GMT  
		Size: 4.4 MB (4364401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:721d96f3fc826a2572ff4ddf0a9e1358ff9edfc1e9a76aab5df7f9d8ed874142`  
		Last Modified: Tue, 02 Jun 2026 10:16:57 GMT  
		Size: 19.2 KB (19164 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:b88f65ace8badb292d51aeaa30cf9e3177bf516ed8828dcb403eb2e32238fd86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.2 MB (349221652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0423ff84455bf5976ce7c427d6521b951b553cf0f744db92df5ab71c32d2bafd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:25:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:25:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:25:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:25:08 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:25:08 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:25:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:25:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:25:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:25:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 21:44:56 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 21:44:56 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:44:56 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 21:44:56 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 21:44:56 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:44:56 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:44:56 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 21:44:56 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 21:44:56 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 21:45:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 12 May 2026 21:45:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 21:45:34 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 21:45:34 GMT
ENTRYPOINT []
# Tue, 12 May 2026 21:45:34 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:11:14 GMT
ENV GN_FILE=geonetwork.war
# Tue, 12 May 2026 22:11:14 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 12 May 2026 22:11:14 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 12 May 2026 22:11:14 GMT
ENV GN_VERSION=3.12.12
# Tue, 12 May 2026 22:11:14 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 12 May 2026 22:11:14 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 12 May 2026 22:12:13 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 12 May 2026 22:12:13 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:12:13 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:12:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:12:13 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0538e749f64d2984e6efd547a87ea84a6ba0dbb5f4c255b9ba010cacb0886fc`  
		Last Modified: Tue, 12 May 2026 21:25:25 GMT  
		Size: 17.0 MB (16997475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cddb2c3802f31fa3e655f7e4ad109e3235f7f8a9f58fb967c41df675f75d85`  
		Last Modified: Tue, 12 May 2026 21:25:26 GMT  
		Size: 54.3 MB (54277488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e295b1abecbb3e5825a0a71662ffaa142104e444d23a9b2bc2c224b0409aac8`  
		Last Modified: Tue, 12 May 2026 21:25:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0515372a9c71502d75368adcb1cca347d99d015b4821bc36e1781a6bbab277b0`  
		Last Modified: Tue, 12 May 2026 21:25:24 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5734ef22cd5b6bd8d266cfceb27b9b485a04263f4e40cdf0bf1e7721f1da0516`  
		Last Modified: Tue, 12 May 2026 21:45:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65a130873fe21a16e9effed70025491fb784c45cd414def179f7a273ba0b9ee`  
		Last Modified: Tue, 12 May 2026 21:45:44 GMT  
		Size: 14.5 MB (14513282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d6dc5c297e09a949928869d350b410719ffe9db37a643c0eb24aeb7661b2da`  
		Last Modified: Tue, 12 May 2026 22:12:40 GMT  
		Size: 234.6 MB (234554495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab7d8d9f4c070cdbaf9c2b82532fe7e8f423bdb69664bb0b7ac0fc1dfdd217c`  
		Last Modified: Tue, 12 May 2026 22:12:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:5ae0536e5c243eb8b6666621ff1e113f323f3a86cb815c627b32f38e6421162b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5fddb25ed26c5e010d36e5a031812fecdf21e9f2473ac6b593989afb23456ee`

```dockerfile
```

-	Layers:
	-	`sha256:b245258abf11d2d95083292a60eb204d6117b3692282d58c9bb8932382391c6e`  
		Last Modified: Tue, 12 May 2026 22:12:35 GMT  
		Size: 4.4 MB (4361560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffdaf87df68a9288152bb955237f43640004b24753aba23d750ca46707ca0c3e`  
		Last Modified: Tue, 12 May 2026 22:12:35 GMT  
		Size: 19.2 KB (19185 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:cab6e984f278797eaccb05a26886d5a96763d049dc5642c1c3abd9e6264257d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.1 MB (355060433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44cd8c76d1338dff700dde94f13c851abbeafc92afcef2a6776a30f698cc0ba6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:24:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:24:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:24:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:24:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:24:32 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:24:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:24:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:24:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:24:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 21:43:57 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 21:43:57 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:43:57 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 21:43:57 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 21:43:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:43:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:43:57 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 21:43:57 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 21:43:57 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 21:45:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 12 May 2026 21:45:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 21:45:14 GMT
ENTRYPOINT []
# Tue, 12 May 2026 21:45:14 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:10:50 GMT
ENV GN_FILE=geonetwork.war
# Tue, 12 May 2026 22:10:50 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 12 May 2026 22:10:50 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 12 May 2026 22:10:50 GMT
ENV GN_VERSION=3.12.12
# Tue, 12 May 2026 22:10:50 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 12 May 2026 22:10:50 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 12 May 2026 22:11:59 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 12 May 2026 22:12:00 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:12:00 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:12:00 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb1e5ca7560d1a0a165fab55641320f02313ed8b7d7549036b7a5913ef35bb9`  
		Last Modified: Tue, 12 May 2026 21:25:16 GMT  
		Size: 18.8 MB (18813402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143da93ed5ff2f7cf49329c446cad440a86250bb6ec397cd1c9edae039dcc43e`  
		Last Modified: Tue, 12 May 2026 21:25:17 GMT  
		Size: 52.7 MB (52670362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e5a505f96555f416a61ebef0a1c2f5bc9f77d0cb1569eb00063a06485893b3`  
		Last Modified: Tue, 12 May 2026 21:25:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a01f6bc440df96f1c53520828ef16850047c001edea5083a04a88f23c1c5bf0`  
		Last Modified: Tue, 12 May 2026 21:25:15 GMT  
		Size: 2.5 KB (2483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7142d4eb2c896d06b098675c07f0d40ae5afbb02cb682b097cb02e96089032f4`  
		Last Modified: Tue, 12 May 2026 21:45:32 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bd4128d71af0430585d6cd4fa250e7c4ab5d47ad6b202ad9205751a17a8651`  
		Last Modified: Tue, 12 May 2026 21:45:32 GMT  
		Size: 14.7 MB (14684400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce85acc52d6459738048139ca5be5485fbe74df87135bc54a6426abf88dc99f0`  
		Last Modified: Tue, 12 May 2026 22:12:53 GMT  
		Size: 234.6 MB (234574967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94664a504d7c39a859c67d861f4a2f99d49a24931dc53d909a77ba1538db590`  
		Last Modified: Tue, 12 May 2026 22:12:48 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:2aa4131b673d710e350a674bb5e1e80f6d8a0be7d3e39900818e2236266c6f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4382274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a868e4c825b1f46fa09d8391cef38391f97a95ad504b2d57e5c62b24b6b4f5`

```dockerfile
```

-	Layers:
	-	`sha256:a159cc1f2afd001726717c9349efdcfb4e8e3d897f2c0223629017995133d59f`  
		Last Modified: Tue, 12 May 2026 22:12:48 GMT  
		Size: 4.4 MB (4363143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23e0cdb20c2c6152e5ed89c7b3de369aca57b455bcc0352a0d59d2bc5b79aa35`  
		Last Modified: Tue, 12 May 2026 22:12:47 GMT  
		Size: 19.1 KB (19131 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3-postgres`

```console
$ docker pull geonetwork@sha256:a12118ac88ef0f948e080326813504d709781ec1cc62f1fcf326d374bde6f13e
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
$ docker pull geonetwork@sha256:ed790e575788a3f5fb27559308691096b97509076f543469b4bae184a94a2c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.9 MB (364916177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e57b260f939dfb2fc8b81e1b50dff0647dcb9d7b1d62df3f8860fbf80919cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:25:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:25:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:25:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:25:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:25:37 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:25:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:25:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:25:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:25:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 21:45:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 21:45:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:45:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 21:45:06 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 21:45:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:45:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:45:06 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 21:45:06 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 21:45:06 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 21:45:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 12 May 2026 21:45:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 21:45:31 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 21:45:31 GMT
ENTRYPOINT []
# Tue, 12 May 2026 21:45:31 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:11:37 GMT
ENV GN_FILE=geonetwork.war
# Tue, 12 May 2026 22:11:37 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 12 May 2026 22:11:37 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 12 May 2026 22:11:37 GMT
ENV GN_VERSION=3.12.12
# Tue, 12 May 2026 22:11:37 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 12 May 2026 22:11:37 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 12 May 2026 22:12:30 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 12 May 2026 22:12:30 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:12:30 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:12:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:12:30 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:32:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 22:32:30 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 12 May 2026 22:32:30 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 12 May 2026 22:32:30 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:32:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:32:30 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6468ff6de61997fbb57dae533eb5b211f02f4c796a195d654eb8f3f268e3b2d7`  
		Last Modified: Tue, 12 May 2026 21:25:54 GMT  
		Size: 17.0 MB (16984059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339c2234aca20e36345fe207e5f8bdf331d4faffd0bcfa8bfb0d3ea5f7247660`  
		Last Modified: Tue, 12 May 2026 21:25:55 GMT  
		Size: 55.2 MB (55200425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca9a652b5c28fcd17f575d8b27ceb1d8d26ee076a79f8d155096293533f766f`  
		Last Modified: Tue, 12 May 2026 21:25:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad155729b83d2b2c4c36d4ccad016d99690aa6c74d72f3ae29775904ff79d53`  
		Last Modified: Tue, 12 May 2026 21:25:53 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f37c125cbd268a3d67e091a1008d8b7371b3567bcbc0811a04492e7fe07dfc`  
		Last Modified: Tue, 12 May 2026 21:45:39 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f324bc94893300bd0727f8017cd10fc2dfaeb4b0425106df31069a4de32c8f1`  
		Last Modified: Tue, 12 May 2026 21:45:40 GMT  
		Size: 14.5 MB (14495571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5fe163481e5c8d68eaecfed72774c935e6b62eb9a47b916cf26d49877942b0`  
		Last Modified: Tue, 12 May 2026 22:12:56 GMT  
		Size: 234.6 MB (234550314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a1d54a67a655034ac0e70c8d30c249f3a5a48d97ebe208149a8f33ec131200`  
		Last Modified: Tue, 12 May 2026 22:12:51 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e88e56f9fed90d419e7ab44f88bbcf6c7e3543a65bc7c5e86f5e3709bd10836`  
		Last Modified: Tue, 12 May 2026 22:32:46 GMT  
		Size: 13.9 MB (13946293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b39623982ed16daf05cdab7e2ed902adf01ed19bd58618708cec7a2d18be69`  
		Last Modified: Tue, 12 May 2026 22:32:46 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555edc6209f32e2727ccda36e097b62fedf447ab770caeb3a3c15f10c985efc1`  
		Last Modified: Tue, 12 May 2026 22:32:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5685f4edbc0ca1d2ef2caffe200d2b60dcd427efd672496d7ed25e475e45a322`  
		Last Modified: Tue, 12 May 2026 22:32:46 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:cb1f6eef136c2df13f134eccddcebc63057cf46e817b87467b410b70d2fbad99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5937870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e037b0271fa1d668136298f1f6757d3d6059c0508229dcded7fa8fc2c40bc598`

```dockerfile
```

-	Layers:
	-	`sha256:922de90e47602072aba3064fd53bc42049ce7201e6e70c50b7f65fc2d7a62f63`  
		Last Modified: Tue, 12 May 2026 22:32:46 GMT  
		Size: 5.9 MB (5915051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecae5ab16643e2891d2f9823ab2ede58cf11bbd5c88e014a9208d477e811eac1`  
		Last Modified: Tue, 12 May 2026 22:32:45 GMT  
		Size: 22.8 KB (22819 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:a39a57cba9a5f86742b244766cea13d4b27a4b7ea54bdc6649b661840c430ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355645618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa565e99774fff64bf9c7c5eec0befdd94d0ac3f20e440b189c03e2684e81efd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:30 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:30 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:33 GMT
ADD file:341ecc672c4413d50e9543a8a38e44f8686dbdcc696b241b06e6b5b3a3ad57f6 in / 
# Fri, 10 Apr 2026 06:56:33 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:25:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:25:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:25:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:25:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:25:19 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:25:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:25:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:25:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:25:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 21:41:30 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 21:41:30 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:41:30 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 21:41:30 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 21:41:30 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:41:30 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:41:30 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 21:41:30 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 21:41:30 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 21:42:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 12 May 2026 21:42:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 21:42:05 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 21:42:05 GMT
ENTRYPOINT []
# Tue, 12 May 2026 21:42:05 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:10:04 GMT
ENV GN_FILE=geonetwork.war
# Tue, 12 May 2026 22:10:04 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 12 May 2026 22:10:04 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 12 May 2026 22:10:04 GMT
ENV GN_VERSION=3.12.12
# Tue, 12 May 2026 22:10:04 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 12 May 2026 22:10:04 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 12 May 2026 22:11:02 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 12 May 2026 22:11:02 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:11:02 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:11:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:11:02 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:32:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 22:32:47 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 12 May 2026 22:32:48 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 12 May 2026 22:32:48 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:32:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:32:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:03a6f28563c3f1bd861a0bd521bea32abc15b3b1362797f0ee963f0cfbe31325`  
		Last Modified: Fri, 10 Apr 2026 09:34:31 GMT  
		Size: 26.9 MB (26859689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc01e78d4f28120684db62d0c13848a2c47a90b4fb68385186bf163372d6dcd`  
		Last Modified: Tue, 12 May 2026 21:25:43 GMT  
		Size: 16.3 MB (16310658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314aff8dd69eb471f7bc3b2c6e00d9d590100e384421a27575b5a9c16fcc2530`  
		Last Modified: Tue, 12 May 2026 21:25:44 GMT  
		Size: 50.5 MB (50541097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c9cab56f09f319ecbe936bd634e4506c6827eb30c0e5ba0f6084f2daf431e4`  
		Last Modified: Tue, 12 May 2026 21:25:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b048c86b77dbec3881bda06a1a6fc5ddd23bdfe7c0c8ccc0743eefce777793`  
		Last Modified: Tue, 12 May 2026 21:25:42 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84712c77de502b6c663565aeb232264b0e37f7c3fef3bb663ae4ea90d7bc06`  
		Last Modified: Tue, 12 May 2026 21:42:14 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4b95f9dc1393f4a7df88fe19a6c713eaf277a2ee4c2f7a97b943b127d06289`  
		Last Modified: Tue, 12 May 2026 21:42:14 GMT  
		Size: 14.4 MB (14382253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eaf1e174eb25da60216643d12b7d643301ee5c237d74e5a308011820d368a67`  
		Last Modified: Tue, 12 May 2026 22:11:28 GMT  
		Size: 234.5 MB (234538612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865ec06f9669e67fd4652a68144b75e6dfff5179a45ad12c2b4e664835912dd0`  
		Last Modified: Tue, 12 May 2026 22:11:23 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2e1ad2ea5d917ab8b5de5f6aa9800c4b4d30e8885c9f30754466ceecd47a57`  
		Last Modified: Tue, 12 May 2026 22:33:02 GMT  
		Size: 13.0 MB (13006761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fdf3d0fae7ee28973646cca8e7116a8fbcf330982749a0d0bd9f2a47ecbc2d`  
		Last Modified: Tue, 12 May 2026 22:33:02 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7f10c5c4cc1f068c7b29d0866d26ef2078e248386fb0ed618b34f3ce6f55df`  
		Last Modified: Tue, 12 May 2026 22:33:02 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd946b037efb83446a9612742f9e7c3470ca33b09d4b8cfb640f75c6270ce5a`  
		Last Modified: Tue, 12 May 2026 22:33:02 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:a92aadfc58cb8453792760dc8a96a4826bf167133c3a841ef306b7cd40ae4f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5940670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea4e863034396340b35bed1a572ab310d430e90207b8180c9736a3a0b04d238`

```dockerfile
```

-	Layers:
	-	`sha256:bca380caa1d4f15a2423ce02593ed4281907a9df2e6657173f303b5759f7fc6e`  
		Last Modified: Tue, 12 May 2026 22:33:02 GMT  
		Size: 5.9 MB (5917766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e74aa826474c7bce1851fe5bc98ebe467b2dc442a9b3672e69956333d805c24`  
		Last Modified: Tue, 12 May 2026 22:33:02 GMT  
		Size: 22.9 KB (22904 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:82836217e5a56028eb4eecaa88f2896f221c1a8760e3786351c8a04583169225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.1 MB (363137435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dbc730e9f1bd92c9165a4fcc1146b0d7483f87655850e0b4c294a31ebf42d79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:25:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:25:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:25:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:25:08 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:25:08 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:25:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:25:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:25:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:25:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 21:44:56 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 21:44:56 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:44:56 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 21:44:56 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 21:44:56 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:44:56 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:44:56 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 21:44:56 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 21:44:56 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 21:45:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 12 May 2026 21:45:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 21:45:34 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 21:45:34 GMT
ENTRYPOINT []
# Tue, 12 May 2026 21:45:34 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:11:14 GMT
ENV GN_FILE=geonetwork.war
# Tue, 12 May 2026 22:11:14 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 12 May 2026 22:11:14 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 12 May 2026 22:11:14 GMT
ENV GN_VERSION=3.12.12
# Tue, 12 May 2026 22:11:14 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 12 May 2026 22:11:14 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 12 May 2026 22:12:13 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 12 May 2026 22:12:13 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:12:13 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:12:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:12:13 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:32:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 22:32:43 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 12 May 2026 22:32:43 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 12 May 2026 22:32:43 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:32:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:32:43 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0538e749f64d2984e6efd547a87ea84a6ba0dbb5f4c255b9ba010cacb0886fc`  
		Last Modified: Tue, 12 May 2026 21:25:25 GMT  
		Size: 17.0 MB (16997475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cddb2c3802f31fa3e655f7e4ad109e3235f7f8a9f58fb967c41df675f75d85`  
		Last Modified: Tue, 12 May 2026 21:25:26 GMT  
		Size: 54.3 MB (54277488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e295b1abecbb3e5825a0a71662ffaa142104e444d23a9b2bc2c224b0409aac8`  
		Last Modified: Tue, 12 May 2026 21:25:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0515372a9c71502d75368adcb1cca347d99d015b4821bc36e1781a6bbab277b0`  
		Last Modified: Tue, 12 May 2026 21:25:24 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5734ef22cd5b6bd8d266cfceb27b9b485a04263f4e40cdf0bf1e7721f1da0516`  
		Last Modified: Tue, 12 May 2026 21:45:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65a130873fe21a16e9effed70025491fb784c45cd414def179f7a273ba0b9ee`  
		Last Modified: Tue, 12 May 2026 21:45:44 GMT  
		Size: 14.5 MB (14513282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d6dc5c297e09a949928869d350b410719ffe9db37a643c0eb24aeb7661b2da`  
		Last Modified: Tue, 12 May 2026 22:12:40 GMT  
		Size: 234.6 MB (234554495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab7d8d9f4c070cdbaf9c2b82532fe7e8f423bdb69664bb0b7ac0fc1dfdd217c`  
		Last Modified: Tue, 12 May 2026 22:12:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaef5a8b667acf9a5ea66b50c93b31b39c43ed0cd507488a86bf541c2bbe2a9e`  
		Last Modified: Tue, 12 May 2026 22:32:58 GMT  
		Size: 13.9 MB (13912369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fdad0a795dd65cad35842ef93efe0fd2833878ebf51935b217565778711c124`  
		Last Modified: Tue, 12 May 2026 22:32:57 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed7e39eeb9b2357a019ce36b3af08839ab852d9d0b63bbc700f6b647687d29c`  
		Last Modified: Tue, 12 May 2026 22:32:57 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f240dc1b10522295af5cf3f8e87db603170a14e072132ef96c86dd6a38bc2536`  
		Last Modified: Tue, 12 May 2026 22:32:57 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:253cce54810daed743fc67aa638b29f630b0f380097f74105c10f73ec909f4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5945184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585923176439dba0f5f894e286b99743bbc763cffac09ebe578b4e300baa2d22`

```dockerfile
```

-	Layers:
	-	`sha256:cfe5231f13265346dd47975797e020757fc621809334f6f4191ae36d9135d9ce`  
		Last Modified: Tue, 12 May 2026 22:32:58 GMT  
		Size: 5.9 MB (5922259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c303636c4347d641970b587a4b659c728088d353d1f3acd210a3fc65ae54ab69`  
		Last Modified: Tue, 12 May 2026 22:32:57 GMT  
		Size: 22.9 KB (22925 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:b1adb84c24cac0f7e8f9e99fdb353a8cb14e077522c57553d297b6cfb3a22cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.5 MB (369501983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bfbaf19b08dba012d9ed57f7cbf19be2a4a985e4e30699312fe07a1cf9e886`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:24:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:24:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:24:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:24:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:24:32 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:24:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:24:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:24:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:24:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 21:43:57 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 21:43:57 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:43:57 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 21:43:57 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 21:43:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:43:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:43:57 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 21:43:57 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 21:43:57 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 21:45:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 12 May 2026 21:45:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 21:45:14 GMT
ENTRYPOINT []
# Tue, 12 May 2026 21:45:14 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:10:50 GMT
ENV GN_FILE=geonetwork.war
# Tue, 12 May 2026 22:10:50 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 12 May 2026 22:10:50 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 12 May 2026 22:10:50 GMT
ENV GN_VERSION=3.12.12
# Tue, 12 May 2026 22:10:50 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 12 May 2026 22:10:50 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 12 May 2026 22:11:59 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 12 May 2026 22:12:00 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:12:00 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:12:00 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:31:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 22:31:01 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 12 May 2026 22:31:01 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 12 May 2026 22:31:01 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:31:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:31:01 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb1e5ca7560d1a0a165fab55641320f02313ed8b7d7549036b7a5913ef35bb9`  
		Last Modified: Tue, 12 May 2026 21:25:16 GMT  
		Size: 18.8 MB (18813402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143da93ed5ff2f7cf49329c446cad440a86250bb6ec397cd1c9edae039dcc43e`  
		Last Modified: Tue, 12 May 2026 21:25:17 GMT  
		Size: 52.7 MB (52670362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e5a505f96555f416a61ebef0a1c2f5bc9f77d0cb1569eb00063a06485893b3`  
		Last Modified: Tue, 12 May 2026 21:25:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a01f6bc440df96f1c53520828ef16850047c001edea5083a04a88f23c1c5bf0`  
		Last Modified: Tue, 12 May 2026 21:25:15 GMT  
		Size: 2.5 KB (2483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7142d4eb2c896d06b098675c07f0d40ae5afbb02cb682b097cb02e96089032f4`  
		Last Modified: Tue, 12 May 2026 21:45:32 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bd4128d71af0430585d6cd4fa250e7c4ab5d47ad6b202ad9205751a17a8651`  
		Last Modified: Tue, 12 May 2026 21:45:32 GMT  
		Size: 14.7 MB (14684400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce85acc52d6459738048139ca5be5485fbe74df87135bc54a6426abf88dc99f0`  
		Last Modified: Tue, 12 May 2026 22:12:53 GMT  
		Size: 234.6 MB (234574967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94664a504d7c39a859c67d861f4a2f99d49a24931dc53d909a77ba1538db590`  
		Last Modified: Tue, 12 May 2026 22:12:48 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec813b16c815c58bb1b974c85c4b4913fe729704eb02d96589a8daa6e81f67c6`  
		Last Modified: Tue, 12 May 2026 22:31:31 GMT  
		Size: 14.4 MB (14438132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e5e9553e4f1ca8333ec0b067b64b164be8c3deb4855ea79f9827597be83be8`  
		Last Modified: Tue, 12 May 2026 22:31:30 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c48e329f6fa3b54da4505c71bf6fc8f0b87adcb1efc5bbbdfc0056b0ec3a84`  
		Last Modified: Tue, 12 May 2026 22:31:30 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e81e3c39d2d7707083fd7328c94847ca512fd4870701534d97dabce4a4864c9`  
		Last Modified: Tue, 12 May 2026 22:31:31 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:2936fc9bd34fc7fffce4959b0789803ea8c8e2f664fda4f800e8ea319c972b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5943409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f687c1f1858b85e0d656545e500f6113b71b88f6e6fe3c93d6159477a08e607`

```dockerfile
```

-	Layers:
	-	`sha256:cf4b9fb81129af235282769d633dfac293cebdb60f92e41b36ed8a550c16bb5d`  
		Last Modified: Tue, 12 May 2026 22:31:31 GMT  
		Size: 5.9 MB (5920551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6c3caa8a3ada44dc29019b5e5b6b41b9d5208e7b6a8e374cfbc69e4b4d504c0`  
		Last Modified: Tue, 12 May 2026 22:31:30 GMT  
		Size: 22.9 KB (22858 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12`

```console
$ docker pull geonetwork@sha256:9789440b2725d089e764fc64e59d6bb47a61b4a517489d1d11c6ca64f041131d
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
$ docker pull geonetwork@sha256:4589e8d06b2ecf93cb5815577c48616d44ad7d18f7fe44f24322deb8806a64b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350966474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ab5c115067ba6f79ce1e888139ab5e95d1ee8ae4465282b7be1e9c3a2fa009`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:25:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:25:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:25:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:25:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:25:37 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:25:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:25:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:25:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:25:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 21:45:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 21:45:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:45:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 21:45:06 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 21:45:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:45:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:45:06 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 21:45:06 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 21:45:06 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 21:45:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 12 May 2026 21:45:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 21:45:31 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 21:45:31 GMT
ENTRYPOINT []
# Tue, 12 May 2026 21:45:31 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:11:37 GMT
ENV GN_FILE=geonetwork.war
# Tue, 12 May 2026 22:11:37 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 12 May 2026 22:11:37 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 12 May 2026 22:11:37 GMT
ENV GN_VERSION=3.12.12
# Tue, 12 May 2026 22:11:37 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 12 May 2026 22:11:37 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 12 May 2026 22:12:30 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 12 May 2026 22:12:30 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:12:30 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:12:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:12:30 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6468ff6de61997fbb57dae533eb5b211f02f4c796a195d654eb8f3f268e3b2d7`  
		Last Modified: Tue, 12 May 2026 21:25:54 GMT  
		Size: 17.0 MB (16984059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339c2234aca20e36345fe207e5f8bdf331d4faffd0bcfa8bfb0d3ea5f7247660`  
		Last Modified: Tue, 12 May 2026 21:25:55 GMT  
		Size: 55.2 MB (55200425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca9a652b5c28fcd17f575d8b27ceb1d8d26ee076a79f8d155096293533f766f`  
		Last Modified: Tue, 12 May 2026 21:25:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad155729b83d2b2c4c36d4ccad016d99690aa6c74d72f3ae29775904ff79d53`  
		Last Modified: Tue, 12 May 2026 21:25:53 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f37c125cbd268a3d67e091a1008d8b7371b3567bcbc0811a04492e7fe07dfc`  
		Last Modified: Tue, 12 May 2026 21:45:39 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f324bc94893300bd0727f8017cd10fc2dfaeb4b0425106df31069a4de32c8f1`  
		Last Modified: Tue, 12 May 2026 21:45:40 GMT  
		Size: 14.5 MB (14495571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5fe163481e5c8d68eaecfed72774c935e6b62eb9a47b916cf26d49877942b0`  
		Last Modified: Tue, 12 May 2026 22:12:56 GMT  
		Size: 234.6 MB (234550314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a1d54a67a655034ac0e70c8d30c249f3a5a48d97ebe208149a8f33ec131200`  
		Last Modified: Tue, 12 May 2026 22:12:51 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:2fbccdf3503145cd97f7b606589d24d93c2bc1e56bdb2c78d9ecba9de8cbd70e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4379489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4506ebd5b4d81a6eacafacbcf055817c350e9b0933da712a517b6b46e67d2af`

```dockerfile
```

-	Layers:
	-	`sha256:6f874835e97e4175c37330379d3f8b5c494a284a9cb6ba307799accd09e48901`  
		Last Modified: Tue, 12 May 2026 22:12:52 GMT  
		Size: 4.4 MB (4360396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef92e0f7e67c5f7a4e361412ca77a74d924c9f75f5de943d3303a5526c2ff4e0`  
		Last Modified: Tue, 12 May 2026 22:12:51 GMT  
		Size: 19.1 KB (19093 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:19cd503b643d3310e64af0cfe3c4657fd3ba9f613a0cdf2c58c3c28bdd3bed51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.2 MB (342191674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6693549d31e7ccf1533853dd3f6d1c08905141dffc290640c2a19fab2d2be89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:36:59 GMT
ARG RELEASE
# Wed, 20 May 2026 01:36:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:36:59 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:02 GMT
ADD file:6d117ff682b1d31146902ad551197b012e75561d62d92d029219fcbf5c493c35 in / 
# Wed, 20 May 2026 01:37:02 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:10:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:10:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:10:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:24 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:10:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:10:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:10:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:10:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 09:17:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 09:17:51 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 09:17:51 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 09:17:51 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 09:17:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:17:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:17:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 09:17:51 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 09:17:51 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 09:18:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Jun 2026 09:18:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 09:18:18 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 09:18:18 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 09:18:18 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 10:13:59 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 10:13:59 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Jun 2026 10:13:59 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 10:13:59 GMT
ENV GN_VERSION=3.12.12
# Tue, 02 Jun 2026 10:13:59 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 02 Jun 2026 10:13:59 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Jun 2026 10:16:36 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Jun 2026 10:16:36 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:16:36 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:16:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 10:16:36 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a2dede8d0e9ca179460cb274dab10c5c4b741cf1544b130df872809a4467e3e4`  
		Last Modified: Wed, 20 May 2026 02:15:37 GMT  
		Size: 26.9 MB (26859709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1d8b94ff08bb8b6de5b69ca5ebb6596cb3713544241d873713c2dd960f2ba9`  
		Last Modified: Tue, 02 Jun 2026 08:10:46 GMT  
		Size: 16.3 MB (16310665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd4cadfd61450b68b7ba220950558346f412256c24c92139b4a1eae532972bd`  
		Last Modified: Tue, 02 Jun 2026 08:10:47 GMT  
		Size: 50.5 MB (50541133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ca58a0a1017272272bdac970286540e1b6e4900ec0ee9e46940c06e120635b`  
		Last Modified: Tue, 02 Jun 2026 08:10:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d8e4ec41df605824c47490458a8ea88b9ed06e4c3cff7af3b9f72b4a04a075`  
		Last Modified: Tue, 02 Jun 2026 08:10:45 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d9988c7a00bfe4dd42888ef010c804f87de8652835b1e43d40afe028975477`  
		Last Modified: Tue, 02 Jun 2026 09:18:27 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7953c7fc5f8a3d6eba9a7df364349bd70a30e1fd7e43a3656f7cdbe1d41beb9e`  
		Last Modified: Tue, 02 Jun 2026 09:18:27 GMT  
		Size: 13.9 MB (13938429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048a8040985022fd6fdd3a200f3e51a1e7155e1ca4c634b32ec4cb28665e1c35`  
		Last Modified: Tue, 02 Jun 2026 10:17:02 GMT  
		Size: 234.5 MB (234538609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fb05d09b3a938bb05b5be8b380f57378b4891f0b3cc9a648f953fcb9fa96fa`  
		Last Modified: Tue, 02 Jun 2026 10:16:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:4e970d0d380879b736d0480f2fca912b641694f7ef6c2de1b18ceca9bfa4b4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94bf0c27ac5a13950a9a6f0823798593d9e5110b1680bcd888e008af39a7050`

```dockerfile
```

-	Layers:
	-	`sha256:3e6852aaa4f0736ea207a5be89a7e88e08f08a9c82b9e79d8f01eb445bc4903e`  
		Last Modified: Tue, 02 Jun 2026 10:16:57 GMT  
		Size: 4.4 MB (4364401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:721d96f3fc826a2572ff4ddf0a9e1358ff9edfc1e9a76aab5df7f9d8ed874142`  
		Last Modified: Tue, 02 Jun 2026 10:16:57 GMT  
		Size: 19.2 KB (19164 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:b88f65ace8badb292d51aeaa30cf9e3177bf516ed8828dcb403eb2e32238fd86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.2 MB (349221652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0423ff84455bf5976ce7c427d6521b951b553cf0f744db92df5ab71c32d2bafd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:25:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:25:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:25:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:25:08 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:25:08 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:25:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:25:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:25:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:25:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 21:44:56 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 21:44:56 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:44:56 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 21:44:56 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 21:44:56 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:44:56 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:44:56 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 21:44:56 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 21:44:56 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 21:45:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 12 May 2026 21:45:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 21:45:34 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 21:45:34 GMT
ENTRYPOINT []
# Tue, 12 May 2026 21:45:34 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:11:14 GMT
ENV GN_FILE=geonetwork.war
# Tue, 12 May 2026 22:11:14 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 12 May 2026 22:11:14 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 12 May 2026 22:11:14 GMT
ENV GN_VERSION=3.12.12
# Tue, 12 May 2026 22:11:14 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 12 May 2026 22:11:14 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 12 May 2026 22:12:13 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 12 May 2026 22:12:13 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:12:13 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:12:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:12:13 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0538e749f64d2984e6efd547a87ea84a6ba0dbb5f4c255b9ba010cacb0886fc`  
		Last Modified: Tue, 12 May 2026 21:25:25 GMT  
		Size: 17.0 MB (16997475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cddb2c3802f31fa3e655f7e4ad109e3235f7f8a9f58fb967c41df675f75d85`  
		Last Modified: Tue, 12 May 2026 21:25:26 GMT  
		Size: 54.3 MB (54277488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e295b1abecbb3e5825a0a71662ffaa142104e444d23a9b2bc2c224b0409aac8`  
		Last Modified: Tue, 12 May 2026 21:25:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0515372a9c71502d75368adcb1cca347d99d015b4821bc36e1781a6bbab277b0`  
		Last Modified: Tue, 12 May 2026 21:25:24 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5734ef22cd5b6bd8d266cfceb27b9b485a04263f4e40cdf0bf1e7721f1da0516`  
		Last Modified: Tue, 12 May 2026 21:45:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65a130873fe21a16e9effed70025491fb784c45cd414def179f7a273ba0b9ee`  
		Last Modified: Tue, 12 May 2026 21:45:44 GMT  
		Size: 14.5 MB (14513282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d6dc5c297e09a949928869d350b410719ffe9db37a643c0eb24aeb7661b2da`  
		Last Modified: Tue, 12 May 2026 22:12:40 GMT  
		Size: 234.6 MB (234554495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab7d8d9f4c070cdbaf9c2b82532fe7e8f423bdb69664bb0b7ac0fc1dfdd217c`  
		Last Modified: Tue, 12 May 2026 22:12:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:5ae0536e5c243eb8b6666621ff1e113f323f3a86cb815c627b32f38e6421162b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5fddb25ed26c5e010d36e5a031812fecdf21e9f2473ac6b593989afb23456ee`

```dockerfile
```

-	Layers:
	-	`sha256:b245258abf11d2d95083292a60eb204d6117b3692282d58c9bb8932382391c6e`  
		Last Modified: Tue, 12 May 2026 22:12:35 GMT  
		Size: 4.4 MB (4361560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffdaf87df68a9288152bb955237f43640004b24753aba23d750ca46707ca0c3e`  
		Last Modified: Tue, 12 May 2026 22:12:35 GMT  
		Size: 19.2 KB (19185 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:cab6e984f278797eaccb05a26886d5a96763d049dc5642c1c3abd9e6264257d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.1 MB (355060433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44cd8c76d1338dff700dde94f13c851abbeafc92afcef2a6776a30f698cc0ba6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:24:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:24:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:24:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:24:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:24:32 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:24:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:24:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:24:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:24:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 21:43:57 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 21:43:57 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:43:57 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 21:43:57 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 21:43:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:43:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:43:57 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 21:43:57 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 21:43:57 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 21:45:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 12 May 2026 21:45:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 21:45:14 GMT
ENTRYPOINT []
# Tue, 12 May 2026 21:45:14 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:10:50 GMT
ENV GN_FILE=geonetwork.war
# Tue, 12 May 2026 22:10:50 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 12 May 2026 22:10:50 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 12 May 2026 22:10:50 GMT
ENV GN_VERSION=3.12.12
# Tue, 12 May 2026 22:10:50 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 12 May 2026 22:10:50 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 12 May 2026 22:11:59 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 12 May 2026 22:12:00 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:12:00 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:12:00 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb1e5ca7560d1a0a165fab55641320f02313ed8b7d7549036b7a5913ef35bb9`  
		Last Modified: Tue, 12 May 2026 21:25:16 GMT  
		Size: 18.8 MB (18813402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143da93ed5ff2f7cf49329c446cad440a86250bb6ec397cd1c9edae039dcc43e`  
		Last Modified: Tue, 12 May 2026 21:25:17 GMT  
		Size: 52.7 MB (52670362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e5a505f96555f416a61ebef0a1c2f5bc9f77d0cb1569eb00063a06485893b3`  
		Last Modified: Tue, 12 May 2026 21:25:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a01f6bc440df96f1c53520828ef16850047c001edea5083a04a88f23c1c5bf0`  
		Last Modified: Tue, 12 May 2026 21:25:15 GMT  
		Size: 2.5 KB (2483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7142d4eb2c896d06b098675c07f0d40ae5afbb02cb682b097cb02e96089032f4`  
		Last Modified: Tue, 12 May 2026 21:45:32 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bd4128d71af0430585d6cd4fa250e7c4ab5d47ad6b202ad9205751a17a8651`  
		Last Modified: Tue, 12 May 2026 21:45:32 GMT  
		Size: 14.7 MB (14684400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce85acc52d6459738048139ca5be5485fbe74df87135bc54a6426abf88dc99f0`  
		Last Modified: Tue, 12 May 2026 22:12:53 GMT  
		Size: 234.6 MB (234574967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94664a504d7c39a859c67d861f4a2f99d49a24931dc53d909a77ba1538db590`  
		Last Modified: Tue, 12 May 2026 22:12:48 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:2aa4131b673d710e350a674bb5e1e80f6d8a0be7d3e39900818e2236266c6f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4382274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a868e4c825b1f46fa09d8391cef38391f97a95ad504b2d57e5c62b24b6b4f5`

```dockerfile
```

-	Layers:
	-	`sha256:a159cc1f2afd001726717c9349efdcfb4e8e3d897f2c0223629017995133d59f`  
		Last Modified: Tue, 12 May 2026 22:12:48 GMT  
		Size: 4.4 MB (4363143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23e0cdb20c2c6152e5ed89c7b3de369aca57b455bcc0352a0d59d2bc5b79aa35`  
		Last Modified: Tue, 12 May 2026 22:12:47 GMT  
		Size: 19.1 KB (19131 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12-postgres`

```console
$ docker pull geonetwork@sha256:a12118ac88ef0f948e080326813504d709781ec1cc62f1fcf326d374bde6f13e
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
$ docker pull geonetwork@sha256:ed790e575788a3f5fb27559308691096b97509076f543469b4bae184a94a2c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.9 MB (364916177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e57b260f939dfb2fc8b81e1b50dff0647dcb9d7b1d62df3f8860fbf80919cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:25:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:25:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:25:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:25:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:25:37 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:25:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:25:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:25:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:25:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 21:45:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 21:45:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:45:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 21:45:06 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 21:45:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:45:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:45:06 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 21:45:06 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 21:45:06 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 21:45:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 12 May 2026 21:45:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 21:45:31 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 21:45:31 GMT
ENTRYPOINT []
# Tue, 12 May 2026 21:45:31 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:11:37 GMT
ENV GN_FILE=geonetwork.war
# Tue, 12 May 2026 22:11:37 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 12 May 2026 22:11:37 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 12 May 2026 22:11:37 GMT
ENV GN_VERSION=3.12.12
# Tue, 12 May 2026 22:11:37 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 12 May 2026 22:11:37 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 12 May 2026 22:12:30 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 12 May 2026 22:12:30 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:12:30 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:12:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:12:30 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:32:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 22:32:30 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 12 May 2026 22:32:30 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 12 May 2026 22:32:30 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:32:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:32:30 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6468ff6de61997fbb57dae533eb5b211f02f4c796a195d654eb8f3f268e3b2d7`  
		Last Modified: Tue, 12 May 2026 21:25:54 GMT  
		Size: 17.0 MB (16984059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339c2234aca20e36345fe207e5f8bdf331d4faffd0bcfa8bfb0d3ea5f7247660`  
		Last Modified: Tue, 12 May 2026 21:25:55 GMT  
		Size: 55.2 MB (55200425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca9a652b5c28fcd17f575d8b27ceb1d8d26ee076a79f8d155096293533f766f`  
		Last Modified: Tue, 12 May 2026 21:25:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad155729b83d2b2c4c36d4ccad016d99690aa6c74d72f3ae29775904ff79d53`  
		Last Modified: Tue, 12 May 2026 21:25:53 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f37c125cbd268a3d67e091a1008d8b7371b3567bcbc0811a04492e7fe07dfc`  
		Last Modified: Tue, 12 May 2026 21:45:39 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f324bc94893300bd0727f8017cd10fc2dfaeb4b0425106df31069a4de32c8f1`  
		Last Modified: Tue, 12 May 2026 21:45:40 GMT  
		Size: 14.5 MB (14495571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5fe163481e5c8d68eaecfed72774c935e6b62eb9a47b916cf26d49877942b0`  
		Last Modified: Tue, 12 May 2026 22:12:56 GMT  
		Size: 234.6 MB (234550314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a1d54a67a655034ac0e70c8d30c249f3a5a48d97ebe208149a8f33ec131200`  
		Last Modified: Tue, 12 May 2026 22:12:51 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e88e56f9fed90d419e7ab44f88bbcf6c7e3543a65bc7c5e86f5e3709bd10836`  
		Last Modified: Tue, 12 May 2026 22:32:46 GMT  
		Size: 13.9 MB (13946293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b39623982ed16daf05cdab7e2ed902adf01ed19bd58618708cec7a2d18be69`  
		Last Modified: Tue, 12 May 2026 22:32:46 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555edc6209f32e2727ccda36e097b62fedf447ab770caeb3a3c15f10c985efc1`  
		Last Modified: Tue, 12 May 2026 22:32:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5685f4edbc0ca1d2ef2caffe200d2b60dcd427efd672496d7ed25e475e45a322`  
		Last Modified: Tue, 12 May 2026 22:32:46 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:cb1f6eef136c2df13f134eccddcebc63057cf46e817b87467b410b70d2fbad99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5937870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e037b0271fa1d668136298f1f6757d3d6059c0508229dcded7fa8fc2c40bc598`

```dockerfile
```

-	Layers:
	-	`sha256:922de90e47602072aba3064fd53bc42049ce7201e6e70c50b7f65fc2d7a62f63`  
		Last Modified: Tue, 12 May 2026 22:32:46 GMT  
		Size: 5.9 MB (5915051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecae5ab16643e2891d2f9823ab2ede58cf11bbd5c88e014a9208d477e811eac1`  
		Last Modified: Tue, 12 May 2026 22:32:45 GMT  
		Size: 22.8 KB (22819 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:a39a57cba9a5f86742b244766cea13d4b27a4b7ea54bdc6649b661840c430ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355645618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa565e99774fff64bf9c7c5eec0befdd94d0ac3f20e440b189c03e2684e81efd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:30 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:30 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:33 GMT
ADD file:341ecc672c4413d50e9543a8a38e44f8686dbdcc696b241b06e6b5b3a3ad57f6 in / 
# Fri, 10 Apr 2026 06:56:33 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:25:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:25:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:25:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:25:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:25:19 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:25:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:25:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:25:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:25:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 21:41:30 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 21:41:30 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:41:30 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 21:41:30 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 21:41:30 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:41:30 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:41:30 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 21:41:30 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 21:41:30 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 21:42:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 12 May 2026 21:42:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 21:42:05 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 21:42:05 GMT
ENTRYPOINT []
# Tue, 12 May 2026 21:42:05 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:10:04 GMT
ENV GN_FILE=geonetwork.war
# Tue, 12 May 2026 22:10:04 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 12 May 2026 22:10:04 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 12 May 2026 22:10:04 GMT
ENV GN_VERSION=3.12.12
# Tue, 12 May 2026 22:10:04 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 12 May 2026 22:10:04 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 12 May 2026 22:11:02 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 12 May 2026 22:11:02 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:11:02 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:11:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:11:02 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:32:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 22:32:47 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 12 May 2026 22:32:48 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 12 May 2026 22:32:48 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:32:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:32:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:03a6f28563c3f1bd861a0bd521bea32abc15b3b1362797f0ee963f0cfbe31325`  
		Last Modified: Fri, 10 Apr 2026 09:34:31 GMT  
		Size: 26.9 MB (26859689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc01e78d4f28120684db62d0c13848a2c47a90b4fb68385186bf163372d6dcd`  
		Last Modified: Tue, 12 May 2026 21:25:43 GMT  
		Size: 16.3 MB (16310658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314aff8dd69eb471f7bc3b2c6e00d9d590100e384421a27575b5a9c16fcc2530`  
		Last Modified: Tue, 12 May 2026 21:25:44 GMT  
		Size: 50.5 MB (50541097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c9cab56f09f319ecbe936bd634e4506c6827eb30c0e5ba0f6084f2daf431e4`  
		Last Modified: Tue, 12 May 2026 21:25:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b048c86b77dbec3881bda06a1a6fc5ddd23bdfe7c0c8ccc0743eefce777793`  
		Last Modified: Tue, 12 May 2026 21:25:42 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84712c77de502b6c663565aeb232264b0e37f7c3fef3bb663ae4ea90d7bc06`  
		Last Modified: Tue, 12 May 2026 21:42:14 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4b95f9dc1393f4a7df88fe19a6c713eaf277a2ee4c2f7a97b943b127d06289`  
		Last Modified: Tue, 12 May 2026 21:42:14 GMT  
		Size: 14.4 MB (14382253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eaf1e174eb25da60216643d12b7d643301ee5c237d74e5a308011820d368a67`  
		Last Modified: Tue, 12 May 2026 22:11:28 GMT  
		Size: 234.5 MB (234538612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865ec06f9669e67fd4652a68144b75e6dfff5179a45ad12c2b4e664835912dd0`  
		Last Modified: Tue, 12 May 2026 22:11:23 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2e1ad2ea5d917ab8b5de5f6aa9800c4b4d30e8885c9f30754466ceecd47a57`  
		Last Modified: Tue, 12 May 2026 22:33:02 GMT  
		Size: 13.0 MB (13006761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fdf3d0fae7ee28973646cca8e7116a8fbcf330982749a0d0bd9f2a47ecbc2d`  
		Last Modified: Tue, 12 May 2026 22:33:02 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7f10c5c4cc1f068c7b29d0866d26ef2078e248386fb0ed618b34f3ce6f55df`  
		Last Modified: Tue, 12 May 2026 22:33:02 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd946b037efb83446a9612742f9e7c3470ca33b09d4b8cfb640f75c6270ce5a`  
		Last Modified: Tue, 12 May 2026 22:33:02 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:a92aadfc58cb8453792760dc8a96a4826bf167133c3a841ef306b7cd40ae4f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5940670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea4e863034396340b35bed1a572ab310d430e90207b8180c9736a3a0b04d238`

```dockerfile
```

-	Layers:
	-	`sha256:bca380caa1d4f15a2423ce02593ed4281907a9df2e6657173f303b5759f7fc6e`  
		Last Modified: Tue, 12 May 2026 22:33:02 GMT  
		Size: 5.9 MB (5917766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e74aa826474c7bce1851fe5bc98ebe467b2dc442a9b3672e69956333d805c24`  
		Last Modified: Tue, 12 May 2026 22:33:02 GMT  
		Size: 22.9 KB (22904 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:82836217e5a56028eb4eecaa88f2896f221c1a8760e3786351c8a04583169225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.1 MB (363137435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dbc730e9f1bd92c9165a4fcc1146b0d7483f87655850e0b4c294a31ebf42d79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:25:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:25:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:25:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:25:08 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:25:08 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:25:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:25:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:25:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:25:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 21:44:56 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 21:44:56 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:44:56 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 21:44:56 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 21:44:56 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:44:56 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:44:56 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 21:44:56 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 21:44:56 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 21:45:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 12 May 2026 21:45:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 21:45:34 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 21:45:34 GMT
ENTRYPOINT []
# Tue, 12 May 2026 21:45:34 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:11:14 GMT
ENV GN_FILE=geonetwork.war
# Tue, 12 May 2026 22:11:14 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 12 May 2026 22:11:14 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 12 May 2026 22:11:14 GMT
ENV GN_VERSION=3.12.12
# Tue, 12 May 2026 22:11:14 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 12 May 2026 22:11:14 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 12 May 2026 22:12:13 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 12 May 2026 22:12:13 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:12:13 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:12:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:12:13 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:32:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 22:32:43 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 12 May 2026 22:32:43 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 12 May 2026 22:32:43 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:32:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:32:43 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0538e749f64d2984e6efd547a87ea84a6ba0dbb5f4c255b9ba010cacb0886fc`  
		Last Modified: Tue, 12 May 2026 21:25:25 GMT  
		Size: 17.0 MB (16997475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cddb2c3802f31fa3e655f7e4ad109e3235f7f8a9f58fb967c41df675f75d85`  
		Last Modified: Tue, 12 May 2026 21:25:26 GMT  
		Size: 54.3 MB (54277488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e295b1abecbb3e5825a0a71662ffaa142104e444d23a9b2bc2c224b0409aac8`  
		Last Modified: Tue, 12 May 2026 21:25:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0515372a9c71502d75368adcb1cca347d99d015b4821bc36e1781a6bbab277b0`  
		Last Modified: Tue, 12 May 2026 21:25:24 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5734ef22cd5b6bd8d266cfceb27b9b485a04263f4e40cdf0bf1e7721f1da0516`  
		Last Modified: Tue, 12 May 2026 21:45:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65a130873fe21a16e9effed70025491fb784c45cd414def179f7a273ba0b9ee`  
		Last Modified: Tue, 12 May 2026 21:45:44 GMT  
		Size: 14.5 MB (14513282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d6dc5c297e09a949928869d350b410719ffe9db37a643c0eb24aeb7661b2da`  
		Last Modified: Tue, 12 May 2026 22:12:40 GMT  
		Size: 234.6 MB (234554495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab7d8d9f4c070cdbaf9c2b82532fe7e8f423bdb69664bb0b7ac0fc1dfdd217c`  
		Last Modified: Tue, 12 May 2026 22:12:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaef5a8b667acf9a5ea66b50c93b31b39c43ed0cd507488a86bf541c2bbe2a9e`  
		Last Modified: Tue, 12 May 2026 22:32:58 GMT  
		Size: 13.9 MB (13912369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fdad0a795dd65cad35842ef93efe0fd2833878ebf51935b217565778711c124`  
		Last Modified: Tue, 12 May 2026 22:32:57 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed7e39eeb9b2357a019ce36b3af08839ab852d9d0b63bbc700f6b647687d29c`  
		Last Modified: Tue, 12 May 2026 22:32:57 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f240dc1b10522295af5cf3f8e87db603170a14e072132ef96c86dd6a38bc2536`  
		Last Modified: Tue, 12 May 2026 22:32:57 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:253cce54810daed743fc67aa638b29f630b0f380097f74105c10f73ec909f4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5945184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585923176439dba0f5f894e286b99743bbc763cffac09ebe578b4e300baa2d22`

```dockerfile
```

-	Layers:
	-	`sha256:cfe5231f13265346dd47975797e020757fc621809334f6f4191ae36d9135d9ce`  
		Last Modified: Tue, 12 May 2026 22:32:58 GMT  
		Size: 5.9 MB (5922259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c303636c4347d641970b587a4b659c728088d353d1f3acd210a3fc65ae54ab69`  
		Last Modified: Tue, 12 May 2026 22:32:57 GMT  
		Size: 22.9 KB (22925 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:b1adb84c24cac0f7e8f9e99fdb353a8cb14e077522c57553d297b6cfb3a22cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.5 MB (369501983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bfbaf19b08dba012d9ed57f7cbf19be2a4a985e4e30699312fe07a1cf9e886`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:24:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:24:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:24:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:24:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:24:32 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:24:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:24:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:24:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:24:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 21:43:57 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 21:43:57 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:43:57 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 21:43:57 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 21:43:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:43:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:43:57 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 21:43:57 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 21:43:57 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 21:45:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 12 May 2026 21:45:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 21:45:14 GMT
ENTRYPOINT []
# Tue, 12 May 2026 21:45:14 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:10:50 GMT
ENV GN_FILE=geonetwork.war
# Tue, 12 May 2026 22:10:50 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 12 May 2026 22:10:50 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 12 May 2026 22:10:50 GMT
ENV GN_VERSION=3.12.12
# Tue, 12 May 2026 22:10:50 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 12 May 2026 22:10:50 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 12 May 2026 22:11:59 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 12 May 2026 22:12:00 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:12:00 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:12:00 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:31:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 22:31:01 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 12 May 2026 22:31:01 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 12 May 2026 22:31:01 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:31:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:31:01 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb1e5ca7560d1a0a165fab55641320f02313ed8b7d7549036b7a5913ef35bb9`  
		Last Modified: Tue, 12 May 2026 21:25:16 GMT  
		Size: 18.8 MB (18813402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143da93ed5ff2f7cf49329c446cad440a86250bb6ec397cd1c9edae039dcc43e`  
		Last Modified: Tue, 12 May 2026 21:25:17 GMT  
		Size: 52.7 MB (52670362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e5a505f96555f416a61ebef0a1c2f5bc9f77d0cb1569eb00063a06485893b3`  
		Last Modified: Tue, 12 May 2026 21:25:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a01f6bc440df96f1c53520828ef16850047c001edea5083a04a88f23c1c5bf0`  
		Last Modified: Tue, 12 May 2026 21:25:15 GMT  
		Size: 2.5 KB (2483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7142d4eb2c896d06b098675c07f0d40ae5afbb02cb682b097cb02e96089032f4`  
		Last Modified: Tue, 12 May 2026 21:45:32 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bd4128d71af0430585d6cd4fa250e7c4ab5d47ad6b202ad9205751a17a8651`  
		Last Modified: Tue, 12 May 2026 21:45:32 GMT  
		Size: 14.7 MB (14684400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce85acc52d6459738048139ca5be5485fbe74df87135bc54a6426abf88dc99f0`  
		Last Modified: Tue, 12 May 2026 22:12:53 GMT  
		Size: 234.6 MB (234574967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94664a504d7c39a859c67d861f4a2f99d49a24931dc53d909a77ba1538db590`  
		Last Modified: Tue, 12 May 2026 22:12:48 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec813b16c815c58bb1b974c85c4b4913fe729704eb02d96589a8daa6e81f67c6`  
		Last Modified: Tue, 12 May 2026 22:31:31 GMT  
		Size: 14.4 MB (14438132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e5e9553e4f1ca8333ec0b067b64b164be8c3deb4855ea79f9827597be83be8`  
		Last Modified: Tue, 12 May 2026 22:31:30 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c48e329f6fa3b54da4505c71bf6fc8f0b87adcb1efc5bbbdfc0056b0ec3a84`  
		Last Modified: Tue, 12 May 2026 22:31:30 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e81e3c39d2d7707083fd7328c94847ca512fd4870701534d97dabce4a4864c9`  
		Last Modified: Tue, 12 May 2026 22:31:31 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:2936fc9bd34fc7fffce4959b0789803ea8c8e2f664fda4f800e8ea319c972b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5943409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f687c1f1858b85e0d656545e500f6113b71b88f6e6fe3c93d6159477a08e607`

```dockerfile
```

-	Layers:
	-	`sha256:cf4b9fb81129af235282769d633dfac293cebdb60f92e41b36ed8a550c16bb5d`  
		Last Modified: Tue, 12 May 2026 22:31:31 GMT  
		Size: 5.9 MB (5920551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6c3caa8a3ada44dc29019b5e5b6b41b9d5208e7b6a8e374cfbc69e4b4d504c0`  
		Last Modified: Tue, 12 May 2026 22:31:30 GMT  
		Size: 22.9 KB (22858 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12.12`

```console
$ docker pull geonetwork@sha256:9789440b2725d089e764fc64e59d6bb47a61b4a517489d1d11c6ca64f041131d
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
$ docker pull geonetwork@sha256:4589e8d06b2ecf93cb5815577c48616d44ad7d18f7fe44f24322deb8806a64b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350966474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ab5c115067ba6f79ce1e888139ab5e95d1ee8ae4465282b7be1e9c3a2fa009`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:25:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:25:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:25:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:25:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:25:37 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:25:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:25:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:25:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:25:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 21:45:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 21:45:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:45:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 21:45:06 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 21:45:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:45:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:45:06 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 21:45:06 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 21:45:06 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 21:45:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 12 May 2026 21:45:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 21:45:31 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 21:45:31 GMT
ENTRYPOINT []
# Tue, 12 May 2026 21:45:31 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:11:37 GMT
ENV GN_FILE=geonetwork.war
# Tue, 12 May 2026 22:11:37 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 12 May 2026 22:11:37 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 12 May 2026 22:11:37 GMT
ENV GN_VERSION=3.12.12
# Tue, 12 May 2026 22:11:37 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 12 May 2026 22:11:37 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 12 May 2026 22:12:30 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 12 May 2026 22:12:30 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:12:30 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:12:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:12:30 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6468ff6de61997fbb57dae533eb5b211f02f4c796a195d654eb8f3f268e3b2d7`  
		Last Modified: Tue, 12 May 2026 21:25:54 GMT  
		Size: 17.0 MB (16984059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339c2234aca20e36345fe207e5f8bdf331d4faffd0bcfa8bfb0d3ea5f7247660`  
		Last Modified: Tue, 12 May 2026 21:25:55 GMT  
		Size: 55.2 MB (55200425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca9a652b5c28fcd17f575d8b27ceb1d8d26ee076a79f8d155096293533f766f`  
		Last Modified: Tue, 12 May 2026 21:25:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad155729b83d2b2c4c36d4ccad016d99690aa6c74d72f3ae29775904ff79d53`  
		Last Modified: Tue, 12 May 2026 21:25:53 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f37c125cbd268a3d67e091a1008d8b7371b3567bcbc0811a04492e7fe07dfc`  
		Last Modified: Tue, 12 May 2026 21:45:39 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f324bc94893300bd0727f8017cd10fc2dfaeb4b0425106df31069a4de32c8f1`  
		Last Modified: Tue, 12 May 2026 21:45:40 GMT  
		Size: 14.5 MB (14495571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5fe163481e5c8d68eaecfed72774c935e6b62eb9a47b916cf26d49877942b0`  
		Last Modified: Tue, 12 May 2026 22:12:56 GMT  
		Size: 234.6 MB (234550314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a1d54a67a655034ac0e70c8d30c249f3a5a48d97ebe208149a8f33ec131200`  
		Last Modified: Tue, 12 May 2026 22:12:51 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:2fbccdf3503145cd97f7b606589d24d93c2bc1e56bdb2c78d9ecba9de8cbd70e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4379489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4506ebd5b4d81a6eacafacbcf055817c350e9b0933da712a517b6b46e67d2af`

```dockerfile
```

-	Layers:
	-	`sha256:6f874835e97e4175c37330379d3f8b5c494a284a9cb6ba307799accd09e48901`  
		Last Modified: Tue, 12 May 2026 22:12:52 GMT  
		Size: 4.4 MB (4360396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef92e0f7e67c5f7a4e361412ca77a74d924c9f75f5de943d3303a5526c2ff4e0`  
		Last Modified: Tue, 12 May 2026 22:12:51 GMT  
		Size: 19.1 KB (19093 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:19cd503b643d3310e64af0cfe3c4657fd3ba9f613a0cdf2c58c3c28bdd3bed51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.2 MB (342191674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6693549d31e7ccf1533853dd3f6d1c08905141dffc290640c2a19fab2d2be89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:36:59 GMT
ARG RELEASE
# Wed, 20 May 2026 01:36:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:36:59 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:02 GMT
ADD file:6d117ff682b1d31146902ad551197b012e75561d62d92d029219fcbf5c493c35 in / 
# Wed, 20 May 2026 01:37:02 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:10:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:10:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:10:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:24 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:10:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:10:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:10:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:10:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 09:17:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 09:17:51 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 09:17:51 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 09:17:51 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 09:17:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:17:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:17:51 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 09:17:51 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 09:17:51 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 09:18:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Jun 2026 09:18:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 09:18:18 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 09:18:18 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 09:18:18 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 10:13:59 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 10:13:59 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Jun 2026 10:13:59 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 10:13:59 GMT
ENV GN_VERSION=3.12.12
# Tue, 02 Jun 2026 10:13:59 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 02 Jun 2026 10:13:59 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Jun 2026 10:16:36 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Jun 2026 10:16:36 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:16:36 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:16:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 10:16:36 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a2dede8d0e9ca179460cb274dab10c5c4b741cf1544b130df872809a4467e3e4`  
		Last Modified: Wed, 20 May 2026 02:15:37 GMT  
		Size: 26.9 MB (26859709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1d8b94ff08bb8b6de5b69ca5ebb6596cb3713544241d873713c2dd960f2ba9`  
		Last Modified: Tue, 02 Jun 2026 08:10:46 GMT  
		Size: 16.3 MB (16310665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd4cadfd61450b68b7ba220950558346f412256c24c92139b4a1eae532972bd`  
		Last Modified: Tue, 02 Jun 2026 08:10:47 GMT  
		Size: 50.5 MB (50541133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ca58a0a1017272272bdac970286540e1b6e4900ec0ee9e46940c06e120635b`  
		Last Modified: Tue, 02 Jun 2026 08:10:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d8e4ec41df605824c47490458a8ea88b9ed06e4c3cff7af3b9f72b4a04a075`  
		Last Modified: Tue, 02 Jun 2026 08:10:45 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d9988c7a00bfe4dd42888ef010c804f87de8652835b1e43d40afe028975477`  
		Last Modified: Tue, 02 Jun 2026 09:18:27 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7953c7fc5f8a3d6eba9a7df364349bd70a30e1fd7e43a3656f7cdbe1d41beb9e`  
		Last Modified: Tue, 02 Jun 2026 09:18:27 GMT  
		Size: 13.9 MB (13938429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048a8040985022fd6fdd3a200f3e51a1e7155e1ca4c634b32ec4cb28665e1c35`  
		Last Modified: Tue, 02 Jun 2026 10:17:02 GMT  
		Size: 234.5 MB (234538609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fb05d09b3a938bb05b5be8b380f57378b4891f0b3cc9a648f953fcb9fa96fa`  
		Last Modified: Tue, 02 Jun 2026 10:16:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:4e970d0d380879b736d0480f2fca912b641694f7ef6c2de1b18ceca9bfa4b4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94bf0c27ac5a13950a9a6f0823798593d9e5110b1680bcd888e008af39a7050`

```dockerfile
```

-	Layers:
	-	`sha256:3e6852aaa4f0736ea207a5be89a7e88e08f08a9c82b9e79d8f01eb445bc4903e`  
		Last Modified: Tue, 02 Jun 2026 10:16:57 GMT  
		Size: 4.4 MB (4364401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:721d96f3fc826a2572ff4ddf0a9e1358ff9edfc1e9a76aab5df7f9d8ed874142`  
		Last Modified: Tue, 02 Jun 2026 10:16:57 GMT  
		Size: 19.2 KB (19164 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:b88f65ace8badb292d51aeaa30cf9e3177bf516ed8828dcb403eb2e32238fd86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.2 MB (349221652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0423ff84455bf5976ce7c427d6521b951b553cf0f744db92df5ab71c32d2bafd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:25:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:25:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:25:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:25:08 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:25:08 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:25:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:25:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:25:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:25:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 21:44:56 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 21:44:56 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:44:56 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 21:44:56 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 21:44:56 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:44:56 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:44:56 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 21:44:56 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 21:44:56 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 21:45:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 12 May 2026 21:45:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 21:45:34 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 21:45:34 GMT
ENTRYPOINT []
# Tue, 12 May 2026 21:45:34 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:11:14 GMT
ENV GN_FILE=geonetwork.war
# Tue, 12 May 2026 22:11:14 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 12 May 2026 22:11:14 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 12 May 2026 22:11:14 GMT
ENV GN_VERSION=3.12.12
# Tue, 12 May 2026 22:11:14 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 12 May 2026 22:11:14 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 12 May 2026 22:12:13 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 12 May 2026 22:12:13 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:12:13 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:12:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:12:13 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0538e749f64d2984e6efd547a87ea84a6ba0dbb5f4c255b9ba010cacb0886fc`  
		Last Modified: Tue, 12 May 2026 21:25:25 GMT  
		Size: 17.0 MB (16997475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cddb2c3802f31fa3e655f7e4ad109e3235f7f8a9f58fb967c41df675f75d85`  
		Last Modified: Tue, 12 May 2026 21:25:26 GMT  
		Size: 54.3 MB (54277488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e295b1abecbb3e5825a0a71662ffaa142104e444d23a9b2bc2c224b0409aac8`  
		Last Modified: Tue, 12 May 2026 21:25:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0515372a9c71502d75368adcb1cca347d99d015b4821bc36e1781a6bbab277b0`  
		Last Modified: Tue, 12 May 2026 21:25:24 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5734ef22cd5b6bd8d266cfceb27b9b485a04263f4e40cdf0bf1e7721f1da0516`  
		Last Modified: Tue, 12 May 2026 21:45:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65a130873fe21a16e9effed70025491fb784c45cd414def179f7a273ba0b9ee`  
		Last Modified: Tue, 12 May 2026 21:45:44 GMT  
		Size: 14.5 MB (14513282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d6dc5c297e09a949928869d350b410719ffe9db37a643c0eb24aeb7661b2da`  
		Last Modified: Tue, 12 May 2026 22:12:40 GMT  
		Size: 234.6 MB (234554495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab7d8d9f4c070cdbaf9c2b82532fe7e8f423bdb69664bb0b7ac0fc1dfdd217c`  
		Last Modified: Tue, 12 May 2026 22:12:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:5ae0536e5c243eb8b6666621ff1e113f323f3a86cb815c627b32f38e6421162b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5fddb25ed26c5e010d36e5a031812fecdf21e9f2473ac6b593989afb23456ee`

```dockerfile
```

-	Layers:
	-	`sha256:b245258abf11d2d95083292a60eb204d6117b3692282d58c9bb8932382391c6e`  
		Last Modified: Tue, 12 May 2026 22:12:35 GMT  
		Size: 4.4 MB (4361560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffdaf87df68a9288152bb955237f43640004b24753aba23d750ca46707ca0c3e`  
		Last Modified: Tue, 12 May 2026 22:12:35 GMT  
		Size: 19.2 KB (19185 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:cab6e984f278797eaccb05a26886d5a96763d049dc5642c1c3abd9e6264257d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.1 MB (355060433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44cd8c76d1338dff700dde94f13c851abbeafc92afcef2a6776a30f698cc0ba6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:24:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:24:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:24:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:24:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:24:32 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:24:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:24:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:24:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:24:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 21:43:57 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 21:43:57 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:43:57 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 21:43:57 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 21:43:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:43:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:43:57 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 21:43:57 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 21:43:57 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 21:45:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 12 May 2026 21:45:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 21:45:14 GMT
ENTRYPOINT []
# Tue, 12 May 2026 21:45:14 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:10:50 GMT
ENV GN_FILE=geonetwork.war
# Tue, 12 May 2026 22:10:50 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 12 May 2026 22:10:50 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 12 May 2026 22:10:50 GMT
ENV GN_VERSION=3.12.12
# Tue, 12 May 2026 22:10:50 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 12 May 2026 22:10:50 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 12 May 2026 22:11:59 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 12 May 2026 22:12:00 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:12:00 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:12:00 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb1e5ca7560d1a0a165fab55641320f02313ed8b7d7549036b7a5913ef35bb9`  
		Last Modified: Tue, 12 May 2026 21:25:16 GMT  
		Size: 18.8 MB (18813402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143da93ed5ff2f7cf49329c446cad440a86250bb6ec397cd1c9edae039dcc43e`  
		Last Modified: Tue, 12 May 2026 21:25:17 GMT  
		Size: 52.7 MB (52670362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e5a505f96555f416a61ebef0a1c2f5bc9f77d0cb1569eb00063a06485893b3`  
		Last Modified: Tue, 12 May 2026 21:25:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a01f6bc440df96f1c53520828ef16850047c001edea5083a04a88f23c1c5bf0`  
		Last Modified: Tue, 12 May 2026 21:25:15 GMT  
		Size: 2.5 KB (2483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7142d4eb2c896d06b098675c07f0d40ae5afbb02cb682b097cb02e96089032f4`  
		Last Modified: Tue, 12 May 2026 21:45:32 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bd4128d71af0430585d6cd4fa250e7c4ab5d47ad6b202ad9205751a17a8651`  
		Last Modified: Tue, 12 May 2026 21:45:32 GMT  
		Size: 14.7 MB (14684400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce85acc52d6459738048139ca5be5485fbe74df87135bc54a6426abf88dc99f0`  
		Last Modified: Tue, 12 May 2026 22:12:53 GMT  
		Size: 234.6 MB (234574967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94664a504d7c39a859c67d861f4a2f99d49a24931dc53d909a77ba1538db590`  
		Last Modified: Tue, 12 May 2026 22:12:48 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:2aa4131b673d710e350a674bb5e1e80f6d8a0be7d3e39900818e2236266c6f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4382274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a868e4c825b1f46fa09d8391cef38391f97a95ad504b2d57e5c62b24b6b4f5`

```dockerfile
```

-	Layers:
	-	`sha256:a159cc1f2afd001726717c9349efdcfb4e8e3d897f2c0223629017995133d59f`  
		Last Modified: Tue, 12 May 2026 22:12:48 GMT  
		Size: 4.4 MB (4363143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23e0cdb20c2c6152e5ed89c7b3de369aca57b455bcc0352a0d59d2bc5b79aa35`  
		Last Modified: Tue, 12 May 2026 22:12:47 GMT  
		Size: 19.1 KB (19131 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12.12-postgres`

```console
$ docker pull geonetwork@sha256:a12118ac88ef0f948e080326813504d709781ec1cc62f1fcf326d374bde6f13e
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
$ docker pull geonetwork@sha256:ed790e575788a3f5fb27559308691096b97509076f543469b4bae184a94a2c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.9 MB (364916177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e57b260f939dfb2fc8b81e1b50dff0647dcb9d7b1d62df3f8860fbf80919cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:25:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:25:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:25:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:25:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:25:37 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:25:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:25:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:25:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:25:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 21:45:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 21:45:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:45:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 21:45:06 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 21:45:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:45:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:45:06 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 21:45:06 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 21:45:06 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 21:45:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 12 May 2026 21:45:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 21:45:31 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 21:45:31 GMT
ENTRYPOINT []
# Tue, 12 May 2026 21:45:31 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:11:37 GMT
ENV GN_FILE=geonetwork.war
# Tue, 12 May 2026 22:11:37 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 12 May 2026 22:11:37 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 12 May 2026 22:11:37 GMT
ENV GN_VERSION=3.12.12
# Tue, 12 May 2026 22:11:37 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 12 May 2026 22:11:37 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 12 May 2026 22:12:30 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 12 May 2026 22:12:30 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:12:30 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:12:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:12:30 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:32:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 22:32:30 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 12 May 2026 22:32:30 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 12 May 2026 22:32:30 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:32:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:32:30 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6468ff6de61997fbb57dae533eb5b211f02f4c796a195d654eb8f3f268e3b2d7`  
		Last Modified: Tue, 12 May 2026 21:25:54 GMT  
		Size: 17.0 MB (16984059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339c2234aca20e36345fe207e5f8bdf331d4faffd0bcfa8bfb0d3ea5f7247660`  
		Last Modified: Tue, 12 May 2026 21:25:55 GMT  
		Size: 55.2 MB (55200425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca9a652b5c28fcd17f575d8b27ceb1d8d26ee076a79f8d155096293533f766f`  
		Last Modified: Tue, 12 May 2026 21:25:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad155729b83d2b2c4c36d4ccad016d99690aa6c74d72f3ae29775904ff79d53`  
		Last Modified: Tue, 12 May 2026 21:25:53 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f37c125cbd268a3d67e091a1008d8b7371b3567bcbc0811a04492e7fe07dfc`  
		Last Modified: Tue, 12 May 2026 21:45:39 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f324bc94893300bd0727f8017cd10fc2dfaeb4b0425106df31069a4de32c8f1`  
		Last Modified: Tue, 12 May 2026 21:45:40 GMT  
		Size: 14.5 MB (14495571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5fe163481e5c8d68eaecfed72774c935e6b62eb9a47b916cf26d49877942b0`  
		Last Modified: Tue, 12 May 2026 22:12:56 GMT  
		Size: 234.6 MB (234550314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a1d54a67a655034ac0e70c8d30c249f3a5a48d97ebe208149a8f33ec131200`  
		Last Modified: Tue, 12 May 2026 22:12:51 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e88e56f9fed90d419e7ab44f88bbcf6c7e3543a65bc7c5e86f5e3709bd10836`  
		Last Modified: Tue, 12 May 2026 22:32:46 GMT  
		Size: 13.9 MB (13946293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b39623982ed16daf05cdab7e2ed902adf01ed19bd58618708cec7a2d18be69`  
		Last Modified: Tue, 12 May 2026 22:32:46 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555edc6209f32e2727ccda36e097b62fedf447ab770caeb3a3c15f10c985efc1`  
		Last Modified: Tue, 12 May 2026 22:32:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5685f4edbc0ca1d2ef2caffe200d2b60dcd427efd672496d7ed25e475e45a322`  
		Last Modified: Tue, 12 May 2026 22:32:46 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:cb1f6eef136c2df13f134eccddcebc63057cf46e817b87467b410b70d2fbad99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5937870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e037b0271fa1d668136298f1f6757d3d6059c0508229dcded7fa8fc2c40bc598`

```dockerfile
```

-	Layers:
	-	`sha256:922de90e47602072aba3064fd53bc42049ce7201e6e70c50b7f65fc2d7a62f63`  
		Last Modified: Tue, 12 May 2026 22:32:46 GMT  
		Size: 5.9 MB (5915051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecae5ab16643e2891d2f9823ab2ede58cf11bbd5c88e014a9208d477e811eac1`  
		Last Modified: Tue, 12 May 2026 22:32:45 GMT  
		Size: 22.8 KB (22819 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:a39a57cba9a5f86742b244766cea13d4b27a4b7ea54bdc6649b661840c430ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355645618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa565e99774fff64bf9c7c5eec0befdd94d0ac3f20e440b189c03e2684e81efd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:30 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:30 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:33 GMT
ADD file:341ecc672c4413d50e9543a8a38e44f8686dbdcc696b241b06e6b5b3a3ad57f6 in / 
# Fri, 10 Apr 2026 06:56:33 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:25:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:25:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:25:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:25:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:25:19 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:25:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:25:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:25:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:25:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 21:41:30 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 21:41:30 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:41:30 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 21:41:30 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 21:41:30 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:41:30 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:41:30 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 21:41:30 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 21:41:30 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 21:42:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 12 May 2026 21:42:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 21:42:05 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 21:42:05 GMT
ENTRYPOINT []
# Tue, 12 May 2026 21:42:05 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:10:04 GMT
ENV GN_FILE=geonetwork.war
# Tue, 12 May 2026 22:10:04 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 12 May 2026 22:10:04 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 12 May 2026 22:10:04 GMT
ENV GN_VERSION=3.12.12
# Tue, 12 May 2026 22:10:04 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 12 May 2026 22:10:04 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 12 May 2026 22:11:02 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 12 May 2026 22:11:02 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:11:02 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:11:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:11:02 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:32:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 22:32:47 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 12 May 2026 22:32:48 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 12 May 2026 22:32:48 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:32:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:32:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:03a6f28563c3f1bd861a0bd521bea32abc15b3b1362797f0ee963f0cfbe31325`  
		Last Modified: Fri, 10 Apr 2026 09:34:31 GMT  
		Size: 26.9 MB (26859689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc01e78d4f28120684db62d0c13848a2c47a90b4fb68385186bf163372d6dcd`  
		Last Modified: Tue, 12 May 2026 21:25:43 GMT  
		Size: 16.3 MB (16310658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314aff8dd69eb471f7bc3b2c6e00d9d590100e384421a27575b5a9c16fcc2530`  
		Last Modified: Tue, 12 May 2026 21:25:44 GMT  
		Size: 50.5 MB (50541097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c9cab56f09f319ecbe936bd634e4506c6827eb30c0e5ba0f6084f2daf431e4`  
		Last Modified: Tue, 12 May 2026 21:25:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b048c86b77dbec3881bda06a1a6fc5ddd23bdfe7c0c8ccc0743eefce777793`  
		Last Modified: Tue, 12 May 2026 21:25:42 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84712c77de502b6c663565aeb232264b0e37f7c3fef3bb663ae4ea90d7bc06`  
		Last Modified: Tue, 12 May 2026 21:42:14 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4b95f9dc1393f4a7df88fe19a6c713eaf277a2ee4c2f7a97b943b127d06289`  
		Last Modified: Tue, 12 May 2026 21:42:14 GMT  
		Size: 14.4 MB (14382253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eaf1e174eb25da60216643d12b7d643301ee5c237d74e5a308011820d368a67`  
		Last Modified: Tue, 12 May 2026 22:11:28 GMT  
		Size: 234.5 MB (234538612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865ec06f9669e67fd4652a68144b75e6dfff5179a45ad12c2b4e664835912dd0`  
		Last Modified: Tue, 12 May 2026 22:11:23 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2e1ad2ea5d917ab8b5de5f6aa9800c4b4d30e8885c9f30754466ceecd47a57`  
		Last Modified: Tue, 12 May 2026 22:33:02 GMT  
		Size: 13.0 MB (13006761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fdf3d0fae7ee28973646cca8e7116a8fbcf330982749a0d0bd9f2a47ecbc2d`  
		Last Modified: Tue, 12 May 2026 22:33:02 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7f10c5c4cc1f068c7b29d0866d26ef2078e248386fb0ed618b34f3ce6f55df`  
		Last Modified: Tue, 12 May 2026 22:33:02 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd946b037efb83446a9612742f9e7c3470ca33b09d4b8cfb640f75c6270ce5a`  
		Last Modified: Tue, 12 May 2026 22:33:02 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:a92aadfc58cb8453792760dc8a96a4826bf167133c3a841ef306b7cd40ae4f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5940670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea4e863034396340b35bed1a572ab310d430e90207b8180c9736a3a0b04d238`

```dockerfile
```

-	Layers:
	-	`sha256:bca380caa1d4f15a2423ce02593ed4281907a9df2e6657173f303b5759f7fc6e`  
		Last Modified: Tue, 12 May 2026 22:33:02 GMT  
		Size: 5.9 MB (5917766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e74aa826474c7bce1851fe5bc98ebe467b2dc442a9b3672e69956333d805c24`  
		Last Modified: Tue, 12 May 2026 22:33:02 GMT  
		Size: 22.9 KB (22904 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:82836217e5a56028eb4eecaa88f2896f221c1a8760e3786351c8a04583169225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.1 MB (363137435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dbc730e9f1bd92c9165a4fcc1146b0d7483f87655850e0b4c294a31ebf42d79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:25:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:25:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:25:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:25:08 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:25:08 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:25:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:25:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:25:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:25:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 21:44:56 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 21:44:56 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:44:56 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 21:44:56 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 21:44:56 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:44:56 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:44:56 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 21:44:56 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 21:44:56 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 21:45:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 12 May 2026 21:45:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 21:45:34 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 21:45:34 GMT
ENTRYPOINT []
# Tue, 12 May 2026 21:45:34 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:11:14 GMT
ENV GN_FILE=geonetwork.war
# Tue, 12 May 2026 22:11:14 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 12 May 2026 22:11:14 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 12 May 2026 22:11:14 GMT
ENV GN_VERSION=3.12.12
# Tue, 12 May 2026 22:11:14 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 12 May 2026 22:11:14 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 12 May 2026 22:12:13 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 12 May 2026 22:12:13 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:12:13 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:12:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:12:13 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:32:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 22:32:43 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 12 May 2026 22:32:43 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 12 May 2026 22:32:43 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:32:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:32:43 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0538e749f64d2984e6efd547a87ea84a6ba0dbb5f4c255b9ba010cacb0886fc`  
		Last Modified: Tue, 12 May 2026 21:25:25 GMT  
		Size: 17.0 MB (16997475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cddb2c3802f31fa3e655f7e4ad109e3235f7f8a9f58fb967c41df675f75d85`  
		Last Modified: Tue, 12 May 2026 21:25:26 GMT  
		Size: 54.3 MB (54277488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e295b1abecbb3e5825a0a71662ffaa142104e444d23a9b2bc2c224b0409aac8`  
		Last Modified: Tue, 12 May 2026 21:25:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0515372a9c71502d75368adcb1cca347d99d015b4821bc36e1781a6bbab277b0`  
		Last Modified: Tue, 12 May 2026 21:25:24 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5734ef22cd5b6bd8d266cfceb27b9b485a04263f4e40cdf0bf1e7721f1da0516`  
		Last Modified: Tue, 12 May 2026 21:45:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65a130873fe21a16e9effed70025491fb784c45cd414def179f7a273ba0b9ee`  
		Last Modified: Tue, 12 May 2026 21:45:44 GMT  
		Size: 14.5 MB (14513282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d6dc5c297e09a949928869d350b410719ffe9db37a643c0eb24aeb7661b2da`  
		Last Modified: Tue, 12 May 2026 22:12:40 GMT  
		Size: 234.6 MB (234554495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab7d8d9f4c070cdbaf9c2b82532fe7e8f423bdb69664bb0b7ac0fc1dfdd217c`  
		Last Modified: Tue, 12 May 2026 22:12:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaef5a8b667acf9a5ea66b50c93b31b39c43ed0cd507488a86bf541c2bbe2a9e`  
		Last Modified: Tue, 12 May 2026 22:32:58 GMT  
		Size: 13.9 MB (13912369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fdad0a795dd65cad35842ef93efe0fd2833878ebf51935b217565778711c124`  
		Last Modified: Tue, 12 May 2026 22:32:57 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed7e39eeb9b2357a019ce36b3af08839ab852d9d0b63bbc700f6b647687d29c`  
		Last Modified: Tue, 12 May 2026 22:32:57 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f240dc1b10522295af5cf3f8e87db603170a14e072132ef96c86dd6a38bc2536`  
		Last Modified: Tue, 12 May 2026 22:32:57 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:253cce54810daed743fc67aa638b29f630b0f380097f74105c10f73ec909f4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5945184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585923176439dba0f5f894e286b99743bbc763cffac09ebe578b4e300baa2d22`

```dockerfile
```

-	Layers:
	-	`sha256:cfe5231f13265346dd47975797e020757fc621809334f6f4191ae36d9135d9ce`  
		Last Modified: Tue, 12 May 2026 22:32:58 GMT  
		Size: 5.9 MB (5922259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c303636c4347d641970b587a4b659c728088d353d1f3acd210a3fc65ae54ab69`  
		Last Modified: Tue, 12 May 2026 22:32:57 GMT  
		Size: 22.9 KB (22925 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:b1adb84c24cac0f7e8f9e99fdb353a8cb14e077522c57553d297b6cfb3a22cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.5 MB (369501983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bfbaf19b08dba012d9ed57f7cbf19be2a4a985e4e30699312fe07a1cf9e886`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:24:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:24:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:24:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:24:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:24:32 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:24:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:24:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:24:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:24:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 21:43:57 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 21:43:57 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:43:57 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 21:43:57 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 21:43:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:43:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 21:43:57 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 21:43:57 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 21:43:57 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 21:45:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 12 May 2026 21:45:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 21:45:14 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 21:45:14 GMT
ENTRYPOINT []
# Tue, 12 May 2026 21:45:14 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:10:50 GMT
ENV GN_FILE=geonetwork.war
# Tue, 12 May 2026 22:10:50 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 12 May 2026 22:10:50 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 12 May 2026 22:10:50 GMT
ENV GN_VERSION=3.12.12
# Tue, 12 May 2026 22:10:50 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 12 May 2026 22:10:50 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 12 May 2026 22:11:59 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 12 May 2026 22:12:00 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:12:00 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:12:00 GMT
CMD ["catalina.sh" "run"]
# Tue, 12 May 2026 22:31:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 22:31:01 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 12 May 2026 22:31:01 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 12 May 2026 22:31:01 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 12 May 2026 22:31:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 22:31:01 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb1e5ca7560d1a0a165fab55641320f02313ed8b7d7549036b7a5913ef35bb9`  
		Last Modified: Tue, 12 May 2026 21:25:16 GMT  
		Size: 18.8 MB (18813402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143da93ed5ff2f7cf49329c446cad440a86250bb6ec397cd1c9edae039dcc43e`  
		Last Modified: Tue, 12 May 2026 21:25:17 GMT  
		Size: 52.7 MB (52670362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e5a505f96555f416a61ebef0a1c2f5bc9f77d0cb1569eb00063a06485893b3`  
		Last Modified: Tue, 12 May 2026 21:25:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a01f6bc440df96f1c53520828ef16850047c001edea5083a04a88f23c1c5bf0`  
		Last Modified: Tue, 12 May 2026 21:25:15 GMT  
		Size: 2.5 KB (2483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7142d4eb2c896d06b098675c07f0d40ae5afbb02cb682b097cb02e96089032f4`  
		Last Modified: Tue, 12 May 2026 21:45:32 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bd4128d71af0430585d6cd4fa250e7c4ab5d47ad6b202ad9205751a17a8651`  
		Last Modified: Tue, 12 May 2026 21:45:32 GMT  
		Size: 14.7 MB (14684400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce85acc52d6459738048139ca5be5485fbe74df87135bc54a6426abf88dc99f0`  
		Last Modified: Tue, 12 May 2026 22:12:53 GMT  
		Size: 234.6 MB (234574967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94664a504d7c39a859c67d861f4a2f99d49a24931dc53d909a77ba1538db590`  
		Last Modified: Tue, 12 May 2026 22:12:48 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec813b16c815c58bb1b974c85c4b4913fe729704eb02d96589a8daa6e81f67c6`  
		Last Modified: Tue, 12 May 2026 22:31:31 GMT  
		Size: 14.4 MB (14438132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e5e9553e4f1ca8333ec0b067b64b164be8c3deb4855ea79f9827597be83be8`  
		Last Modified: Tue, 12 May 2026 22:31:30 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c48e329f6fa3b54da4505c71bf6fc8f0b87adcb1efc5bbbdfc0056b0ec3a84`  
		Last Modified: Tue, 12 May 2026 22:31:30 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e81e3c39d2d7707083fd7328c94847ca512fd4870701534d97dabce4a4864c9`  
		Last Modified: Tue, 12 May 2026 22:31:31 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:2936fc9bd34fc7fffce4959b0789803ea8c8e2f664fda4f800e8ea319c972b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5943409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f687c1f1858b85e0d656545e500f6113b71b88f6e6fe3c93d6159477a08e607`

```dockerfile
```

-	Layers:
	-	`sha256:cf4b9fb81129af235282769d633dfac293cebdb60f92e41b36ed8a550c16bb5d`  
		Last Modified: Tue, 12 May 2026 22:31:31 GMT  
		Size: 5.9 MB (5920551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6c3caa8a3ada44dc29019b5e5b6b41b9d5208e7b6a8e374cfbc69e4b4d504c0`  
		Last Modified: Tue, 12 May 2026 22:31:30 GMT  
		Size: 22.9 KB (22858 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4`

```console
$ docker pull geonetwork@sha256:1c1bb0e4bc2c32b181602971a6760636e3e5659afe2b296818456cac0f620686
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `geonetwork:4` - linux; amd64

```console
$ docker pull geonetwork@sha256:091af31e85652383cba9f4069a718b61b48d928a87e46f59844abcbf701e7867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.6 MB (420631421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97663e8ce8f8d9e4597905e2e90ad25341bf99d0913b271d80e514d0b39775fe`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 29 Apr 2026 22:45:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:45:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:45:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:45:18 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Apr 2026 22:45:18 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:45:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:45:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:45:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:45:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 11 May 2026 23:28:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 11 May 2026 23:28:32 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:28:32 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 11 May 2026 23:28:32 GMT
WORKDIR /usr/local/tomcat
# Mon, 11 May 2026 23:28:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:28:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:28:32 GMT
ENV TOMCAT_MAJOR=9
# Mon, 11 May 2026 23:28:32 GMT
ENV TOMCAT_VERSION=9.0.118
# Mon, 11 May 2026 23:28:32 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Mon, 11 May 2026 23:28:32 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 11 May 2026 23:28:36 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:28:36 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 11 May 2026 23:28:36 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 11 May 2026 23:28:36 GMT
ENTRYPOINT []
# Mon, 11 May 2026 23:28:36 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:18:58 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 19:18:58 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 26 May 2026 19:18:58 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 26 May 2026 19:18:58 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 26 May 2026 19:18:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 26 May 2026 19:18:58 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 19:18:58 GMT
ENV GN_VERSION=4.4.10
# Tue, 26 May 2026 19:18:58 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 26 May 2026 19:19:24 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 19:19:24 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 26 May 2026 19:19:24 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 19:19:24 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 19:19:24 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 19:19:24 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:19:24 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf23ab6a8436ea4cc30c42c9eced3d7a9a42b066275648f8f1fbb0208b18c8fc`  
		Last Modified: Wed, 29 Apr 2026 22:45:34 GMT  
		Size: 17.0 MB (16983441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a14539c3f6df146437a21e07161e034b17f23dbe26ca23f9476c502b4c11df`  
		Last Modified: Wed, 29 Apr 2026 22:45:35 GMT  
		Size: 47.3 MB (47344091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288fd19c92924e5275f173c7e37ab77f791d263774ab4012d94aea4a7e017433`  
		Last Modified: Wed, 29 Apr 2026 22:45:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50069af557289dad3f81803ec84242ee38d92cc0440cca83f780e8ba4d498e4f`  
		Last Modified: Wed, 29 Apr 2026 22:45:33 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7ca595c1cdc53dff58e2b3a6153107fc81a7268f73191a74be7e474e14ed59`  
		Last Modified: Mon, 11 May 2026 23:28:44 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06493eda4e9a7d2b23bf3e6636af3dacc96c09641e54154aa1946effb90c6486`  
		Last Modified: Mon, 11 May 2026 23:28:45 GMT  
		Size: 13.8 MB (13796197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac16f181866752eb755aa0be0d49e0fe46f5415546b23a6f482aa911fb62975b`  
		Last Modified: Mon, 11 May 2026 23:28:44 GMT  
		Size: 224.7 KB (224711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301652bb5925b1827b165b5ab4b526f115ffcad9a18ed4c498248e1755b3918d`  
		Last Modified: Tue, 26 May 2026 19:19:46 GMT  
		Size: 801.2 KB (801153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580faf8d93c7ad4fe54e0ec31866eac5bdc1d7e623801f5f9fcea16079322838`  
		Last Modified: Tue, 26 May 2026 19:19:55 GMT  
		Size: 311.7 MB (311742287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65305e31e8a7d274d5b7e4aaaa51a87fd1498f829c54093d35e445ff8432921`  
		Last Modified: Tue, 26 May 2026 19:19:46 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78547240fa108460cca624821bdd9bdaa40632e77c3fe9f0183748660167ccc`  
		Last Modified: Tue, 26 May 2026 19:19:46 GMT  
		Size: 3.0 KB (3011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb9962a2ec25c6c14736c7c6bab123c904c35de138290510354b31b9690b017`  
		Last Modified: Tue, 26 May 2026 19:19:47 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:3500ea7c70984ba06a2209b87ef42a131983e9d2aab874dffeca07534346eedd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4218988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b0d9bf6f1cd55e1fee3b5172d5253154a0c9d87600f18eb3df04fac8031b2ea`

```dockerfile
```

-	Layers:
	-	`sha256:0aa54fecf16260834bc09fe1d7beb85e6184c1982119163848018902641d4190`  
		Last Modified: Tue, 26 May 2026 19:19:46 GMT  
		Size: 4.2 MB (4193558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4b9e3ae3f53beaacd9e2c7e102d2ba0eb7ec37661ca6ec2b3252b2ec29be58a`  
		Last Modified: Tue, 26 May 2026 19:19:46 GMT  
		Size: 25.4 KB (25430 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:078815e148dbfc72f5ef0f2d9a49b7046d0257250ed9c9f07f77e21fddc40a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.0 MB (415010904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9973dcb48dc41326f20fc607a2bf8b7095b78c2ef6196bf851cefc30506a50d`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:30 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:30 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:33 GMT
ADD file:341ecc672c4413d50e9543a8a38e44f8686dbdcc696b241b06e6b5b3a3ad57f6 in / 
# Fri, 10 Apr 2026 06:56:33 GMT
CMD ["/bin/bash"]
# Wed, 29 Apr 2026 22:45:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:45:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:45:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:45:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Apr 2026 22:45:50 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:45:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:45:54 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:45:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:45:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 11 May 2026 23:32:02 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 11 May 2026 23:32:02 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:32:02 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 11 May 2026 23:32:02 GMT
WORKDIR /usr/local/tomcat
# Mon, 11 May 2026 23:32:02 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:32:02 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:32:02 GMT
ENV TOMCAT_MAJOR=9
# Mon, 11 May 2026 23:32:02 GMT
ENV TOMCAT_VERSION=9.0.118
# Mon, 11 May 2026 23:32:02 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Mon, 11 May 2026 23:32:02 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 11 May 2026 23:32:08 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:32:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 11 May 2026 23:32:09 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 11 May 2026 23:32:09 GMT
ENTRYPOINT []
# Mon, 11 May 2026 23:32:09 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:22:49 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 19:22:49 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 26 May 2026 19:22:49 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 26 May 2026 19:22:49 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 26 May 2026 19:22:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 26 May 2026 19:22:49 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 19:22:49 GMT
ENV GN_VERSION=4.4.10
# Tue, 26 May 2026 19:22:49 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 26 May 2026 19:23:44 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 19:23:44 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 26 May 2026 19:23:44 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 19:23:44 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 19:23:44 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 19:23:44 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:23:44 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:03a6f28563c3f1bd861a0bd521bea32abc15b3b1362797f0ee963f0cfbe31325`  
		Last Modified: Fri, 10 Apr 2026 09:34:31 GMT  
		Size: 26.9 MB (26859689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3dcebaf2b2fcd539a30bc10bd91bbc7ef20caf11f1c358662e4ed783f9f102`  
		Last Modified: Wed, 29 Apr 2026 22:46:06 GMT  
		Size: 16.3 MB (16309684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f053e6426c790097075d4ca7bfd3ab90c6a6e96cdbbccf290cdb2a94445589`  
		Last Modified: Wed, 29 Apr 2026 22:46:07 GMT  
		Size: 45.5 MB (45452102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea68a1289a7d5d8edf9eded1c36c22635133ba55845322243cb20a0b0cdcdfd`  
		Last Modified: Wed, 29 Apr 2026 22:46:05 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34376f25195e52a2212871c8527277aa3bcd48be13afd35392696de749a7a56`  
		Last Modified: Wed, 29 Apr 2026 22:46:05 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9812430188f562534646d2616ab7a65aef552bef4d7fd50d0e646c38d49dc06d`  
		Last Modified: Mon, 11 May 2026 23:32:17 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5afef3c660b5106444ad7cd8e6b3e51ab20027742bb52a87a417e02564ecae`  
		Last Modified: Mon, 11 May 2026 23:32:18 GMT  
		Size: 13.7 MB (13730071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd5af756627697b9d0312dbc503baac6d124035a1ea54aded41bc3a7589a911`  
		Last Modified: Mon, 11 May 2026 23:32:17 GMT  
		Size: 196.5 KB (196474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df79545c33f0948e9238aeab008fdd4e07fa85179907a8e2aa7f4b25c805d40b`  
		Last Modified: Tue, 26 May 2026 19:24:08 GMT  
		Size: 714.0 KB (714029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cd9539d0d70e20b02dc1518f9f953d8d819677c19f89db82675cd65ce657f2`  
		Last Modified: Tue, 26 May 2026 19:24:14 GMT  
		Size: 311.7 MB (311742286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e394ae6b2e407c562fbe0e21dd720578e26f7d2cff2055a5dac4bcde2d7a681`  
		Last Modified: Tue, 26 May 2026 19:24:08 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03763171bafc34b7dc363c05ccc5209710063fdbefbdb05fd102d21b3137f298`  
		Last Modified: Tue, 26 May 2026 19:24:08 GMT  
		Size: 3.0 KB (3013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b60e92c376f95b932802a553ffa89296a702df5a94746caf99c8fc4ca9ef556`  
		Last Modified: Tue, 26 May 2026 19:24:09 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:f2f23a094e649ef271989597d3e1f365ce133cf849ec19eae366afcafe5255ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4222684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f040fd7f77614559a95cc3d01b878885e05b17195674b5ae76c5d6cb3853f05`

```dockerfile
```

-	Layers:
	-	`sha256:dd940f32ec01e09e6f7ff39f8d4618e0bd460de603d3aa769fa37296b1ed3bf7`  
		Last Modified: Tue, 26 May 2026 19:24:08 GMT  
		Size: 4.2 MB (4197161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbe94d55c25c0cd7b8b730338a6123f8d64c2808749991e6941171e807d7edd9`  
		Last Modified: Tue, 26 May 2026 19:24:08 GMT  
		Size: 25.5 KB (25523 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:b892c23b10e16891b1f3ebb00d9df9bdacca8ec34c8e187aa5ae6144a5342c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.1 MB (418108296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65f865a438974b29477b13b9b7acf8047b2c5e3414b4a04b835b71c655ebf42`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 29 Apr 2026 22:45:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:45:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:45:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:45:43 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Apr 2026 22:45:43 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:45:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:45:46 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:45:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:45:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 11 May 2026 23:27:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 11 May 2026 23:27:54 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:27:54 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 11 May 2026 23:27:54 GMT
WORKDIR /usr/local/tomcat
# Mon, 11 May 2026 23:27:54 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:27:54 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:27:54 GMT
ENV TOMCAT_MAJOR=9
# Mon, 11 May 2026 23:27:54 GMT
ENV TOMCAT_VERSION=9.0.118
# Mon, 11 May 2026 23:27:54 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Mon, 11 May 2026 23:27:54 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 11 May 2026 23:28:01 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:28:02 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 11 May 2026 23:28:02 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 11 May 2026 23:28:02 GMT
ENTRYPOINT []
# Mon, 11 May 2026 23:28:02 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:19:08 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 19:19:08 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 26 May 2026 19:19:08 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 26 May 2026 19:19:08 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 26 May 2026 19:19:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 26 May 2026 19:19:08 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 19:19:08 GMT
ENV GN_VERSION=4.4.10
# Tue, 26 May 2026 19:19:08 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 26 May 2026 19:20:20 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 19:20:20 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 26 May 2026 19:20:20 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 19:20:20 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 19:20:20 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 19:20:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:20:20 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340297f35e2c376c99270f2485ce4edd3c92de46a0bbef95a9bce7a944b35238`  
		Last Modified: Wed, 29 Apr 2026 22:45:59 GMT  
		Size: 17.0 MB (16996253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a8f9d2e0cdee350d3ed81afb01002bf9e394770886cecaed65f94e9470854`  
		Last Modified: Wed, 29 Apr 2026 22:46:00 GMT  
		Size: 45.7 MB (45660771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8b082d384d013a651b9a297183b301e82f6a59914d0873722ee08ae517b26e`  
		Last Modified: Wed, 29 Apr 2026 22:45:58 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08b5a1d9756317e6e8d13806e18cd14d78e5909594672612e96f2e3669b4f15`  
		Last Modified: Wed, 29 Apr 2026 22:45:58 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccb01e6b7b0d3a577dc45fc8232d7b6818325ffd7c939319446fd423064d38c`  
		Last Modified: Mon, 11 May 2026 23:28:11 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56c6f243e717ed8ba18b3c43492501aa31eb08d7c0df5075474090ed42d5d25`  
		Last Modified: Mon, 11 May 2026 23:28:11 GMT  
		Size: 13.8 MB (13805554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da79f66c4b83e2df5f98493f6db136efc253662ed6bc3b524de0003aaadcd61`  
		Last Modified: Mon, 11 May 2026 23:28:11 GMT  
		Size: 225.3 KB (225280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc0e8f9e38ddd9b7f35374c4e54287f9e77e32f49d9ee062b0d381934467ed5`  
		Last Modified: Tue, 26 May 2026 19:20:45 GMT  
		Size: 795.8 KB (795754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bde8402bddd9ebda751686e1c0caec51c340a6cbe8afe3c0c709704532e8f7e`  
		Last Modified: Tue, 26 May 2026 19:20:52 GMT  
		Size: 311.7 MB (311742326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59445f2b0af00976dca76cca13d75abc90c8755185a479a1cef6b3b0e56648c`  
		Last Modified: Tue, 26 May 2026 19:20:45 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff795d7978acc5515e1d3183acce6dc5ecf30ba249554f0329c769a5a9f10edf`  
		Last Modified: Tue, 26 May 2026 19:20:45 GMT  
		Size: 3.0 KB (3014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acd7f4b488604821d030d1151546d2721d1c968e01fe3f77b7ef85fa84f6252`  
		Last Modified: Tue, 26 May 2026 19:20:46 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:02233406faf8b5d980db73662d831319c86dc7a8630d8f41b2cb5a14b56ae715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4220197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c691eeb4dc4eb0c780cad66e7c54f472f4bb685e5bcb8f6b44ce873b1c7b5c`

```dockerfile
```

-	Layers:
	-	`sha256:6625220a3d7971d6beed82f28f2797e32db30a4c4c6cb94cf87c52c4f1343454`  
		Last Modified: Tue, 26 May 2026 19:20:45 GMT  
		Size: 4.2 MB (4194648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9de6fce6dbd22d640264b16c99c9b4891344a3d1fadaa2dc3935f7eeca6cd3d6`  
		Last Modified: Tue, 26 May 2026 19:20:45 GMT  
		Size: 25.5 KB (25549 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:065fbac665c5ccbd330eb99e634a931dda7a5f6c8654e613f247c00abaf0c3ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.7 MB (422738247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3532be992ebcedf7f8b743a45f584148c462a8ab96e1b968cbc74d747a5617f`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:12:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:12:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:12:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:12:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:12:34 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:45:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:45:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:45:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:45:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 01:22:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 01:22:58 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 01:22:58 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 01:22:58 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 01:22:58 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 01:22:58 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 01:22:58 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 01:22:58 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 01:22:58 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 01:22:59 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 01:23:07 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 01:23:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 01:23:09 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 01:23:09 GMT
ENTRYPOINT []
# Tue, 12 May 2026 01:23:09 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 20:22:54 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 20:22:54 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 26 May 2026 20:22:54 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 26 May 2026 20:22:54 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 26 May 2026 20:22:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 26 May 2026 20:22:54 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 20:22:54 GMT
ENV GN_VERSION=4.4.10
# Tue, 26 May 2026 20:22:54 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 26 May 2026 20:23:13 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 20:23:14 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 26 May 2026 20:23:14 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 20:23:15 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 20:23:15 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 20:23:15 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 20:23:15 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13718497a6adee31aa098ce2c85aca5feeb60aa6f13ee0ac169b2a181311f2cd`  
		Last Modified: Wed, 15 Apr 2026 21:13:20 GMT  
		Size: 18.8 MB (18813307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777cb69b760c692aaca637d1f978ca71a27e8f712772ebee4f24d36075f9e119`  
		Last Modified: Wed, 29 Apr 2026 22:46:19 GMT  
		Size: 42.8 MB (42813437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7f006dbd4d35f9dc4139ef666a81408417cd773080cdf49bb5876a1228c7a0`  
		Last Modified: Wed, 29 Apr 2026 22:46:18 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62105aa809cab5140e7f62bdbab1c9624ce547772bb7b5e7b61d334457d61a3b`  
		Last Modified: Wed, 29 Apr 2026 22:46:18 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64ac7edd53aaec8649090cca5b03990f58f860ea148a5da89d274fb41c41609`  
		Last Modified: Tue, 12 May 2026 01:23:33 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3125d2db6abf2edbd83717983bb17c1b31afcfaa662341d3dd858d0a812e4f6`  
		Last Modified: Tue, 12 May 2026 01:23:33 GMT  
		Size: 13.8 MB (13831958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f12f88f8c1d63dbca0713f1ac021902a8ec4b59a5003b102e4f0dc3bdcdb67`  
		Last Modified: Tue, 12 May 2026 01:23:33 GMT  
		Size: 256.7 KB (256653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0837cc78d6d0d644b064b7d8664e3978efb5e9abb3360bd237b6dbb67bacfb0`  
		Last Modified: Tue, 26 May 2026 20:24:02 GMT  
		Size: 959.8 KB (959838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390e02e08f47bb475b2a002d2732c6fab3e0a7213c996b6b76ec098b8531b347`  
		Last Modified: Tue, 26 May 2026 20:24:09 GMT  
		Size: 311.7 MB (311742307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311d5798f7d276ef1904ae9961d12de257c80ac83afcf7920ac3bbc39c6e47f6`  
		Last Modified: Tue, 26 May 2026 20:24:02 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894173186f8c6225d36ea08a8379237ec9a3cc1b95dbff3b17e7d076a70068d9`  
		Last Modified: Tue, 26 May 2026 20:24:02 GMT  
		Size: 3.0 KB (3016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7beb0611be5018411ef263cfb2b79f931a40b221ba55629c055508565bedbb4d`  
		Last Modified: Tue, 26 May 2026 20:24:03 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:706b4b5a7348d850ea13e80a6ad9dde29cc228708e6976584d7f1f64978ad4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4223112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3135bcb3a1755a7cd165f5843f0dfafd495327ae4161f2f7b7dcbf752eac8f75`

```dockerfile
```

-	Layers:
	-	`sha256:338eada16d2652193771bb358aeab313bdcbc4a8b56a987797f3f275ff190038`  
		Last Modified: Tue, 26 May 2026 20:24:02 GMT  
		Size: 4.2 MB (4197637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bae2cd05343a8d4a072e7b8f8407f9904236e48fb6ea27bb33a0a7732a791a1`  
		Last Modified: Tue, 26 May 2026 20:24:02 GMT  
		Size: 25.5 KB (25475 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4` - linux; s390x

```console
$ docker pull geonetwork@sha256:b7ea2a6440ebdc6e96b122291b8edce2b37d979511458c56dbe605bdd9a6fbab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.5 MB (415480524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2418672e41bacffd94b20e96aae257b1238fda21e72b7797a8d9038a2b68b2d`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:50:27 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:50:29 GMT
ADD file:41defd98c44eed6fc946fd94496a94164879f2ad4f63d66a5c1e213cc2259ad1 in / 
# Fri, 10 Apr 2026 06:50:29 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:44:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:44:12 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:43:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:43:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:43:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:43:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 11 May 2026 23:52:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 11 May 2026 23:52:35 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:52:35 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 11 May 2026 23:52:35 GMT
WORKDIR /usr/local/tomcat
# Mon, 11 May 2026 23:52:35 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:52:35 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:52:35 GMT
ENV TOMCAT_MAJOR=9
# Mon, 11 May 2026 23:52:35 GMT
ENV TOMCAT_VERSION=9.0.118
# Mon, 11 May 2026 23:52:35 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Mon, 11 May 2026 23:52:35 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 11 May 2026 23:52:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:52:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 11 May 2026 23:52:39 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 11 May 2026 23:52:39 GMT
ENTRYPOINT []
# Mon, 11 May 2026 23:52:39 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 20:00:27 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 20:00:27 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 26 May 2026 20:00:27 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 26 May 2026 20:00:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 26 May 2026 20:00:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 26 May 2026 20:00:27 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 20:00:27 GMT
ENV GN_VERSION=4.4.10
# Tue, 26 May 2026 20:00:27 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 26 May 2026 20:00:46 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 20:00:46 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 26 May 2026 20:00:46 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 20:00:46 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 20:00:46 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 20:00:46 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 20:00:46 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:ef1c26d09a5f9962879f732e212c4246a41e8473f6120efb435886357c85dd5a`  
		Last Modified: Fri, 10 Apr 2026 09:34:53 GMT  
		Size: 29.9 MB (29912147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5a3498cd625b1c7f2fe4f65685d4036d3cad9b92fdc3a7c30d047b0511431d`  
		Last Modified: Wed, 15 Apr 2026 20:44:43 GMT  
		Size: 17.6 MB (17579116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb83646d8cec7253c91045c8e0b103abc33d9faba0838653791cc13cfd2131d`  
		Last Modified: Wed, 29 Apr 2026 22:43:50 GMT  
		Size: 41.4 MB (41358769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d1ad21b5f4affc0bdf817bc13bc1b05c5e24c5728fc980722be40acf096d52`  
		Last Modified: Wed, 29 Apr 2026 22:43:49 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55a0630eea6b0c3f15ae53ad6c9f09b28ec02d6d14461bd65f1672e3066b8b8`  
		Last Modified: Wed, 29 Apr 2026 22:43:50 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef363bd4cee4e70ac0af7fd7af4b7e52eeba57c7a34b82803d8b38577887af9c`  
		Last Modified: Mon, 11 May 2026 23:52:52 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df865499b28393bd025d1ee75ad7d094381abf897ec9598f6926505a2beded93`  
		Last Modified: Mon, 11 May 2026 23:52:52 GMT  
		Size: 13.8 MB (13804833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74fe6edaae19a35d37b18d5121fa781cb38333b11d3dc82ea8cba63c14db5aa`  
		Last Modified: Mon, 11 May 2026 23:52:52 GMT  
		Size: 232.9 KB (232950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aea2f91b5b2d9900add721a42ab843517ae01adde6c3463235ab3e137725200`  
		Last Modified: Tue, 26 May 2026 20:01:48 GMT  
		Size: 843.8 KB (843799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1571be11b97395ab029de35d8b10c01eed74e123359af9b5d04290fd87d309`  
		Last Modified: Tue, 26 May 2026 20:01:54 GMT  
		Size: 311.7 MB (311742343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886e5a4b0db6f174fcde33323e4fac33c45cf45d2247ec34a062c37f0a0af2a9`  
		Last Modified: Tue, 26 May 2026 20:01:48 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e49d70370c8456159089603d94e0524719b9de002afe100cee3aaab89c88e5e`  
		Last Modified: Tue, 26 May 2026 20:01:48 GMT  
		Size: 3.0 KB (3013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c01440357dabb831ad91c416559f54c00951ff6e2088f72b26246ca053e65ae`  
		Last Modified: Tue, 26 May 2026 20:01:49 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:4c6791c4a2fb4f87bd89cf0514da8f74b41734151b1784c74dd913baf768603f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4221193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84ef0d33fb600070830a943fc3f30191ef63f78212ffacd313669917141df84`

```dockerfile
```

-	Layers:
	-	`sha256:b95bfa55a71f73c618ff7074b52701aa296b286e4f8cf72c67836f0bc2e2b37d`  
		Last Modified: Tue, 26 May 2026 20:01:48 GMT  
		Size: 4.2 MB (4195763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d3b55ef5c7d3537471dbce478b79dcc2fd257b48859a212457a4fecd438ef79`  
		Last Modified: Tue, 26 May 2026 20:01:48 GMT  
		Size: 25.4 KB (25430 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.2`

```console
$ docker pull geonetwork@sha256:a05085d2fe16743d08b1ff7b8014c38eab657824a3045a3311d6b55a0c0bf3b1
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

### `geonetwork:4.2` - linux; amd64

```console
$ docker pull geonetwork@sha256:face7f40fac91a737063365d87c6a14dd5a42cac35d0d87616584d167dc597ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.7 MB (368697437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8f7ad789aeb4a1df2e3fa3ecb97b40ef0541979ce57186a4e6c9d756a52e78`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:26:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:26:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:26:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:26:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:26:00 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:26:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8eef3d4a837bb7a9e45d30a7579d84d5b76a4321f4376573311e6bf89e48f9b0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='d5e50cb002600007dbdfac523605d26196607fa5212db0942ef05cdce9fe2892';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='5f0693c6c8ca0eb8df969bb1053b1926b1e7c57a3f90c6f9e8d493395e76a329';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='4f724a0fce1117521a3a3e55ebb0281d56f6c9a066092bc3186ee40d8cd955a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:26:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:26:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:26:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 22:10:29 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 22:10:29 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 22:10:29 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 22:10:29 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:10:29 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 22:10:29 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 22:10:29 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 22:10:29 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 22:10:29 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 22:10:29 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 22:10:32 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 22:10:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 22:10:33 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 22:10:33 GMT
ENTRYPOINT []
# Tue, 12 May 2026 22:10:33 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:18:54 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 19:18:54 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom         -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Tue, 26 May 2026 19:18:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /usr/local/tomcat/webapps/geonetwork # buildkit
# Tue, 26 May 2026 19:18:54 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 19:18:54 GMT
ENV GN_VERSION=4.2.15
# Tue, 26 May 2026 19:18:54 GMT
ENV GN_DOWNLOAD_MD5=79cd931ac7fc0be044ec1f2dd44f3f96
# Tue, 26 May 2026 19:20:08 GMT
RUN set -eux;     cd /usr/local/tomcat/webapps/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 19:20:08 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 19:20:08 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 19:20:08 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 19:20:08 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:20:08 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33abfee870deb3c761ef29f79f7108403b0c8f6f62e8bb7bc24f7e18713303c8`  
		Last Modified: Tue, 12 May 2026 21:26:13 GMT  
		Size: 17.0 MB (16984064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fd86ab74982c95df0d144145a16be34730720255fe1875829f07a6669f38cd`  
		Last Modified: Tue, 12 May 2026 21:26:14 GMT  
		Size: 42.3 MB (42337232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64be910d3bfc7e8229417bf478baf545ebbd4b83b0b662ee6db8199d1a75251`  
		Last Modified: Tue, 12 May 2026 21:26:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c801c9e61a240be9754abb6945db4dfee648800391abfa63c77a7565c47557`  
		Last Modified: Tue, 12 May 2026 21:26:12 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5521b52231aac6c33cec32b775bd6fd422ab19a0bafceda1a16b9c5718a821b`  
		Last Modified: Tue, 12 May 2026 22:10:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf329df12d156bddde8e5ed85343ffb1a37a534c57bd1fa73e7a028fe65b8e8`  
		Last Modified: Tue, 12 May 2026 22:10:42 GMT  
		Size: 13.8 MB (13795426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1b2d1d0c65de1c253694f41d2b5d27f8c9ad47ef20954438606acec9a084c4`  
		Last Modified: Tue, 12 May 2026 22:10:42 GMT  
		Size: 224.8 KB (224810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2272f0c3497b979207d8e01d2a0e6a928ce2edfe92ae023b8257ad07cc18e7`  
		Last Modified: Tue, 26 May 2026 19:20:30 GMT  
		Size: 239.1 KB (239075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafc0311a36fc9aabe0b19bcc0f9d8a9e7ccacb1a82d1830ec4b6bb44bb6e1e7`  
		Last Modified: Tue, 26 May 2026 19:20:36 GMT  
		Size: 265.4 MB (265378556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c12639c6db7d8b464ed7124b78d094a0abc7f864416d8f108b9677e527e3b83`  
		Last Modified: Tue, 26 May 2026 19:20:30 GMT  
		Size: 1.5 KB (1504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0326c0ccd31d13c018c81b503cb9a74954ccc13531083e1bfaebb11bac7b48c4`  
		Last Modified: Tue, 26 May 2026 19:20:30 GMT  
		Size: 999.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2` - unknown; unknown

```console
$ docker pull geonetwork@sha256:3eefb39e06eefc6b0a79fc48dc22e65aa4a6fd79e7f282e44ee8a26d32503dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4202467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa193483150c04fdf486e87a7b71fa30c7c25287a8862ef5cabefc7fff9a727`

```dockerfile
```

-	Layers:
	-	`sha256:f8058215f71b1c9791804599d35cba8d531799e657fb95c7980eac1d57744ac5`  
		Last Modified: Tue, 26 May 2026 19:20:30 GMT  
		Size: 4.2 MB (4180789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15128c00361f59675bf3198ad656a76bf00fee0836fb0c9658dbe7b98ba96aff`  
		Last Modified: Tue, 26 May 2026 19:20:30 GMT  
		Size: 21.7 KB (21678 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.2` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:6a12db0b2faa69be54580469159f53eadb057fa49eca87f219561773fbbaf490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.5 MB (362478283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996727574c95d614de43053db5d3627ca9f2bfb630c3c0f91321994d7ef92c5b`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:30 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:30 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:33 GMT
ADD file:341ecc672c4413d50e9543a8a38e44f8686dbdcc696b241b06e6b5b3a3ad57f6 in / 
# Fri, 10 Apr 2026 06:56:33 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:26:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:26:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:26:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:26:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:26:36 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:26:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8eef3d4a837bb7a9e45d30a7579d84d5b76a4321f4376573311e6bf89e48f9b0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='d5e50cb002600007dbdfac523605d26196607fa5212db0942ef05cdce9fe2892';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='5f0693c6c8ca0eb8df969bb1053b1926b1e7c57a3f90c6f9e8d493395e76a329';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='4f724a0fce1117521a3a3e55ebb0281d56f6c9a066092bc3186ee40d8cd955a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:26:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:26:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:26:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 22:09:13 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 22:09:13 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 22:09:13 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 22:09:13 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:09:13 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 22:09:13 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 22:09:13 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 22:09:13 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 22:09:13 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 22:09:13 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 22:09:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 22:09:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 22:09:21 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 22:09:21 GMT
ENTRYPOINT []
# Tue, 12 May 2026 22:09:21 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:22:47 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 19:22:47 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom         -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Tue, 26 May 2026 19:22:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /usr/local/tomcat/webapps/geonetwork # buildkit
# Tue, 26 May 2026 19:22:47 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 19:22:47 GMT
ENV GN_VERSION=4.2.15
# Tue, 26 May 2026 19:22:47 GMT
ENV GN_DOWNLOAD_MD5=79cd931ac7fc0be044ec1f2dd44f3f96
# Tue, 26 May 2026 19:23:19 GMT
RUN set -eux;     cd /usr/local/tomcat/webapps/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 19:23:19 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 19:23:19 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 19:23:19 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 19:23:19 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:23:19 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:03a6f28563c3f1bd861a0bd521bea32abc15b3b1362797f0ee963f0cfbe31325`  
		Last Modified: Fri, 10 Apr 2026 09:34:31 GMT  
		Size: 26.9 MB (26859689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d6583703b067512ec399871388e06f946275b9fc2089cea0831dc05c6d42ce`  
		Last Modified: Tue, 12 May 2026 21:26:58 GMT  
		Size: 16.3 MB (16310544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24db8ad3b895582d531f43c1bba6830c1619b5af45379d90c6e23dba30a1c307`  
		Last Modified: Tue, 12 May 2026 21:26:59 GMT  
		Size: 39.8 MB (39772094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66ebfade72c1d1c1d2f9d5fea174a4f736377f63d0e9adec7e47b95fb73a083`  
		Last Modified: Tue, 12 May 2026 21:26:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c664c5544aa0e802217879a6d98de4534cd5151186c6297dbddaaea0155e36f7`  
		Last Modified: Tue, 12 May 2026 21:26:57 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265b28c1c18f6f6f2c2393377fab14703a3f1bfba209b5331b483bc8f766a5f6`  
		Last Modified: Tue, 12 May 2026 22:09:30 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5163af829dee1910bf8215756e6a18c305b24883aa4a4dad751c1915a66fac`  
		Last Modified: Tue, 12 May 2026 22:09:30 GMT  
		Size: 13.7 MB (13728884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71057eb7a57e8dc9240b0fc767c272795a2410fa1ae33937f4c58f1c414d3fce`  
		Last Modified: Tue, 12 May 2026 22:09:30 GMT  
		Size: 196.6 KB (196631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46292eb8911ca6621c2cfdb9bff7a66a50775dfff3db83d0ca27bbb7456c1b9b`  
		Last Modified: Tue, 26 May 2026 19:23:42 GMT  
		Size: 226.6 KB (226609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44fb9551472ffbf437c5ea42c6b3d88fc898bb3f30e5b9ac02faa61b0a19a87`  
		Last Modified: Tue, 26 May 2026 19:23:47 GMT  
		Size: 265.4 MB (265378532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852575738256d3efe5ef7bdb0d2d38e7370363458958d95f5988f8fa5a8304b2`  
		Last Modified: Tue, 26 May 2026 19:23:42 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c877983dbec8e1839b0ca0ced6be970c6febaa589e4c129a6563cb9e27d1f3a`  
		Last Modified: Tue, 26 May 2026 19:23:42 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2` - unknown; unknown

```console
$ docker pull geonetwork@sha256:5f499bf9aea670aaccd438eb71b8b290613ea9ba6a24822e7953803195fb10a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb33129c41572ab8d7b1f52fa78d430170c9dbc5100cf424c4deff7e8c64a35`

```dockerfile
```

-	Layers:
	-	`sha256:b5d65f052bb0ee49b0da2c6d6b3e55a4471fc3555e7a6a68aa9b76e86f902c33`  
		Last Modified: Tue, 26 May 2026 19:23:42 GMT  
		Size: 4.2 MB (4186780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50bd44a6bacc9f09c3045f370ac890b20940137a6d2e17ac02db69609bfceb03`  
		Last Modified: Tue, 26 May 2026 19:23:42 GMT  
		Size: 21.8 KB (21756 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.2` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:cc0e5801872d6428f189a6413b7258a1845cb65e8d0a560fe4a634b672248663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.8 MB (366833282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a52cd38875094765938650abc5f3bed09ce213ffc16f26647b9668bae8baa45`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:26:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:26:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:26:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:26:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:26:02 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:26:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8eef3d4a837bb7a9e45d30a7579d84d5b76a4321f4376573311e6bf89e48f9b0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='d5e50cb002600007dbdfac523605d26196607fa5212db0942ef05cdce9fe2892';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='5f0693c6c8ca0eb8df969bb1053b1926b1e7c57a3f90c6f9e8d493395e76a329';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='4f724a0fce1117521a3a3e55ebb0281d56f6c9a066092bc3186ee40d8cd955a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:26:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:26:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:26:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 22:10:12 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 22:10:12 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 22:10:12 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 22:10:13 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:10:13 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 22:10:13 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 22:10:13 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 22:10:13 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 22:10:13 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 22:10:13 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 22:10:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 22:10:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 22:10:20 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 22:10:20 GMT
ENTRYPOINT []
# Tue, 12 May 2026 22:10:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:19:07 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 19:19:07 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom         -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Tue, 26 May 2026 19:19:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /usr/local/tomcat/webapps/geonetwork # buildkit
# Tue, 26 May 2026 19:19:07 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 19:19:07 GMT
ENV GN_VERSION=4.2.15
# Tue, 26 May 2026 19:19:07 GMT
ENV GN_DOWNLOAD_MD5=79cd931ac7fc0be044ec1f2dd44f3f96
# Tue, 26 May 2026 19:20:09 GMT
RUN set -eux;     cd /usr/local/tomcat/webapps/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 19:20:09 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 19:20:09 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 19:20:09 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 19:20:09 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:20:09 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7746ead8bf3fc66cd94a81f8f77658aaf8a979318b7f92926e4502b5f21122ca`  
		Last Modified: Tue, 12 May 2026 21:26:16 GMT  
		Size: 17.0 MB (16997507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164abf015d7f4deff1ea843960d85ff9f8c61f5d7e7406e6b09c690122255cd1`  
		Last Modified: Tue, 12 May 2026 21:26:16 GMT  
		Size: 41.3 MB (41307612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012c4a5b70289a60f5f556c214705513c4d4b562642d638db51348295cef8f9a`  
		Last Modified: Tue, 12 May 2026 21:26:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e1b5f22335c0e983d38b92e1f26d67d1dec9f062689f9211065fc6d1e9e02c`  
		Last Modified: Tue, 12 May 2026 21:26:15 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b9858c4ac458d0467d3edd0eff33576f5d45179e458c73f57efd70a10b3b8c`  
		Last Modified: Tue, 12 May 2026 22:10:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8944894ca41bec2bdbc3329e258371e32acd0e10981327d5339ee40a7daabf8f`  
		Last Modified: Tue, 12 May 2026 22:10:30 GMT  
		Size: 13.8 MB (13804912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4106647bfe223cfcfbdaf9fdd3bfcd1333a4cc7e6e578a77979a37d338f1a356`  
		Last Modified: Tue, 12 May 2026 22:10:29 GMT  
		Size: 225.3 KB (225317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678f166d4d94ff4545657dca18996379c8fe1f0cb1a48d3e551389351bb3f93a`  
		Last Modified: Tue, 26 May 2026 19:20:31 GMT  
		Size: 238.3 KB (238290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119215e20a11c81078af1d7ec77115104397c1536ccad4410ddfdc473c4b3e7d`  
		Last Modified: Tue, 26 May 2026 19:20:37 GMT  
		Size: 265.4 MB (265378563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced8b4db44c2391bbf975167f19d648a4d249ee5f63151f831f5556f1768ae24`  
		Last Modified: Tue, 26 May 2026 19:20:31 GMT  
		Size: 1.5 KB (1505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f118615710f6dd69653dece083de4a5caa1aa60f0eef386d6978f526662e7dd9`  
		Last Modified: Tue, 26 May 2026 19:20:31 GMT  
		Size: 999.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2` - unknown; unknown

```console
$ docker pull geonetwork@sha256:5a51851e6c465efa700318c629c840c26f24c56aa3ce5de352a009dbadfd8d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4203702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d634a511812cf91dbcd893fae190e14c54ac7acf6ee69fa97196b896e980a279`

```dockerfile
```

-	Layers:
	-	`sha256:f41d248110b25c8dbb590a62a61b04c46e83d87194ef0a4f1b68673fd1eca397`  
		Last Modified: Tue, 26 May 2026 19:20:31 GMT  
		Size: 4.2 MB (4181929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b09e4d1a9ef44d486cc4bc7bceee7bc7bdba06376ee06027d5175f53fda07d1`  
		Last Modified: Tue, 26 May 2026 19:20:31 GMT  
		Size: 21.8 KB (21773 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.2` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:d911b40392c9c160fb215948c9b4e21e7eeafc8d82dec641d2fe4664d6f2a8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.6 MB (374610520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427405aac066abb23a810c5068695198cfc29070e50452fb445a482c9c7ca989`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:24:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:24:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:24:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:24:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:24:32 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:27:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8eef3d4a837bb7a9e45d30a7579d84d5b76a4321f4376573311e6bf89e48f9b0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='d5e50cb002600007dbdfac523605d26196607fa5212db0942ef05cdce9fe2892';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='5f0693c6c8ca0eb8df969bb1053b1926b1e7c57a3f90c6f9e8d493395e76a329';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='4f724a0fce1117521a3a3e55ebb0281d56f6c9a066092bc3186ee40d8cd955a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:27:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:27:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:27:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 22:09:29 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 22:09:29 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 22:09:29 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 22:09:32 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:09:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 22:09:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 22:09:32 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 22:09:32 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 22:09:32 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 22:09:33 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 22:09:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 22:09:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 22:09:44 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 22:09:44 GMT
ENTRYPOINT []
# Tue, 12 May 2026 22:09:44 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 20:22:13 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 20:22:13 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom         -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Tue, 26 May 2026 20:22:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /usr/local/tomcat/webapps/geonetwork # buildkit
# Tue, 26 May 2026 20:22:13 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 20:22:13 GMT
ENV GN_VERSION=4.2.15
# Tue, 26 May 2026 20:22:13 GMT
ENV GN_DOWNLOAD_MD5=79cd931ac7fc0be044ec1f2dd44f3f96
# Tue, 26 May 2026 20:22:32 GMT
RUN set -eux;     cd /usr/local/tomcat/webapps/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 20:22:32 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 20:22:33 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 20:22:33 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 20:22:33 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 20:22:33 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb1e5ca7560d1a0a165fab55641320f02313ed8b7d7549036b7a5913ef35bb9`  
		Last Modified: Tue, 12 May 2026 21:25:16 GMT  
		Size: 18.8 MB (18813402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2819dacb96e17aa4ec53ff84c83bc66254a8ec89320ab127acd8fe5af348c6`  
		Last Modified: Tue, 12 May 2026 21:28:19 GMT  
		Size: 41.7 MB (41741551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1076e7e80cdeada102ee02d0c583c48c447bcc29ef916494fd2a0a1b1f72729`  
		Last Modified: Tue, 12 May 2026 21:28:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cc2ffed3a11d5178bf55daae8d1c2121e7758577dfcbe6b4482244d7b17734`  
		Last Modified: Tue, 12 May 2026 21:28:18 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542cb2211a02fe074d35f07f341ec0c5cda33089a75fdccb2410af709dd2a96b`  
		Last Modified: Tue, 12 May 2026 22:10:19 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5dd083c9cde15bfb885aebc235c8c309d9e12c101b6b396c0944cda236e68a`  
		Last Modified: Tue, 12 May 2026 22:10:20 GMT  
		Size: 13.8 MB (13831242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da01f83bf4d78bd15acd5553885c67f5f0040fbc7f8e02c5fde1edc0480595f9`  
		Last Modified: Tue, 12 May 2026 22:10:19 GMT  
		Size: 256.7 KB (256657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221221da7d50cc2c4c49e59c14a054fa0dd42074a86391292127f50f39c5789b`  
		Last Modified: Tue, 26 May 2026 20:23:21 GMT  
		Size: 269.6 KB (269642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64765807682b0ac15c48c90496c8f112754b428aa9d929813fbbc31d80ef2e2f`  
		Last Modified: Tue, 26 May 2026 20:23:28 GMT  
		Size: 265.4 MB (265378551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb960faa776d3d010c49f39591f171d512c4c71b7ad06da180967d4fd182437b`  
		Last Modified: Tue, 26 May 2026 20:23:22 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f649e5e982171ffb7aaf173dbe645f1ae11e88de0e3e9a23dbda25704dab51c7`  
		Last Modified: Tue, 26 May 2026 20:23:22 GMT  
		Size: 999.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2` - unknown; unknown

```console
$ docker pull geonetwork@sha256:9849aedcb2b957e6a727829c7f0cada93102b011e30ad5706452be073648d6bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4207258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe39241c7a0e2478c1faa167ccf988b68e4d3e906dd6114cd3f7d1bc8ff166b`

```dockerfile
```

-	Layers:
	-	`sha256:1aefdcd53966da25b89de81065b1126433c47b3190da1ae067a1deeadbf5e57d`  
		Last Modified: Tue, 26 May 2026 20:23:22 GMT  
		Size: 4.2 MB (4185546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:311569eda509f36c27687b259c0da0ca1ba7c84e8523c9acf434d964c44c8f33`  
		Last Modified: Tue, 26 May 2026 20:23:21 GMT  
		Size: 21.7 KB (21712 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.2.15`

```console
$ docker pull geonetwork@sha256:a05085d2fe16743d08b1ff7b8014c38eab657824a3045a3311d6b55a0c0bf3b1
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

### `geonetwork:4.2.15` - linux; amd64

```console
$ docker pull geonetwork@sha256:face7f40fac91a737063365d87c6a14dd5a42cac35d0d87616584d167dc597ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.7 MB (368697437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8f7ad789aeb4a1df2e3fa3ecb97b40ef0541979ce57186a4e6c9d756a52e78`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:26:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:26:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:26:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:26:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:26:00 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:26:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8eef3d4a837bb7a9e45d30a7579d84d5b76a4321f4376573311e6bf89e48f9b0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='d5e50cb002600007dbdfac523605d26196607fa5212db0942ef05cdce9fe2892';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='5f0693c6c8ca0eb8df969bb1053b1926b1e7c57a3f90c6f9e8d493395e76a329';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='4f724a0fce1117521a3a3e55ebb0281d56f6c9a066092bc3186ee40d8cd955a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:26:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:26:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:26:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 22:10:29 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 22:10:29 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 22:10:29 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 22:10:29 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:10:29 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 22:10:29 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 22:10:29 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 22:10:29 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 22:10:29 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 22:10:29 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 22:10:32 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 22:10:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 22:10:33 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 22:10:33 GMT
ENTRYPOINT []
# Tue, 12 May 2026 22:10:33 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:18:54 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 19:18:54 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom         -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Tue, 26 May 2026 19:18:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /usr/local/tomcat/webapps/geonetwork # buildkit
# Tue, 26 May 2026 19:18:54 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 19:18:54 GMT
ENV GN_VERSION=4.2.15
# Tue, 26 May 2026 19:18:54 GMT
ENV GN_DOWNLOAD_MD5=79cd931ac7fc0be044ec1f2dd44f3f96
# Tue, 26 May 2026 19:20:08 GMT
RUN set -eux;     cd /usr/local/tomcat/webapps/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 19:20:08 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 19:20:08 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 19:20:08 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 19:20:08 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:20:08 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33abfee870deb3c761ef29f79f7108403b0c8f6f62e8bb7bc24f7e18713303c8`  
		Last Modified: Tue, 12 May 2026 21:26:13 GMT  
		Size: 17.0 MB (16984064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fd86ab74982c95df0d144145a16be34730720255fe1875829f07a6669f38cd`  
		Last Modified: Tue, 12 May 2026 21:26:14 GMT  
		Size: 42.3 MB (42337232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64be910d3bfc7e8229417bf478baf545ebbd4b83b0b662ee6db8199d1a75251`  
		Last Modified: Tue, 12 May 2026 21:26:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c801c9e61a240be9754abb6945db4dfee648800391abfa63c77a7565c47557`  
		Last Modified: Tue, 12 May 2026 21:26:12 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5521b52231aac6c33cec32b775bd6fd422ab19a0bafceda1a16b9c5718a821b`  
		Last Modified: Tue, 12 May 2026 22:10:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf329df12d156bddde8e5ed85343ffb1a37a534c57bd1fa73e7a028fe65b8e8`  
		Last Modified: Tue, 12 May 2026 22:10:42 GMT  
		Size: 13.8 MB (13795426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1b2d1d0c65de1c253694f41d2b5d27f8c9ad47ef20954438606acec9a084c4`  
		Last Modified: Tue, 12 May 2026 22:10:42 GMT  
		Size: 224.8 KB (224810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2272f0c3497b979207d8e01d2a0e6a928ce2edfe92ae023b8257ad07cc18e7`  
		Last Modified: Tue, 26 May 2026 19:20:30 GMT  
		Size: 239.1 KB (239075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafc0311a36fc9aabe0b19bcc0f9d8a9e7ccacb1a82d1830ec4b6bb44bb6e1e7`  
		Last Modified: Tue, 26 May 2026 19:20:36 GMT  
		Size: 265.4 MB (265378556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c12639c6db7d8b464ed7124b78d094a0abc7f864416d8f108b9677e527e3b83`  
		Last Modified: Tue, 26 May 2026 19:20:30 GMT  
		Size: 1.5 KB (1504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0326c0ccd31d13c018c81b503cb9a74954ccc13531083e1bfaebb11bac7b48c4`  
		Last Modified: Tue, 26 May 2026 19:20:30 GMT  
		Size: 999.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2.15` - unknown; unknown

```console
$ docker pull geonetwork@sha256:3eefb39e06eefc6b0a79fc48dc22e65aa4a6fd79e7f282e44ee8a26d32503dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4202467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa193483150c04fdf486e87a7b71fa30c7c25287a8862ef5cabefc7fff9a727`

```dockerfile
```

-	Layers:
	-	`sha256:f8058215f71b1c9791804599d35cba8d531799e657fb95c7980eac1d57744ac5`  
		Last Modified: Tue, 26 May 2026 19:20:30 GMT  
		Size: 4.2 MB (4180789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15128c00361f59675bf3198ad656a76bf00fee0836fb0c9658dbe7b98ba96aff`  
		Last Modified: Tue, 26 May 2026 19:20:30 GMT  
		Size: 21.7 KB (21678 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.2.15` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:6a12db0b2faa69be54580469159f53eadb057fa49eca87f219561773fbbaf490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.5 MB (362478283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996727574c95d614de43053db5d3627ca9f2bfb630c3c0f91321994d7ef92c5b`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:30 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:30 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:33 GMT
ADD file:341ecc672c4413d50e9543a8a38e44f8686dbdcc696b241b06e6b5b3a3ad57f6 in / 
# Fri, 10 Apr 2026 06:56:33 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:26:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:26:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:26:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:26:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:26:36 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:26:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8eef3d4a837bb7a9e45d30a7579d84d5b76a4321f4376573311e6bf89e48f9b0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='d5e50cb002600007dbdfac523605d26196607fa5212db0942ef05cdce9fe2892';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='5f0693c6c8ca0eb8df969bb1053b1926b1e7c57a3f90c6f9e8d493395e76a329';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='4f724a0fce1117521a3a3e55ebb0281d56f6c9a066092bc3186ee40d8cd955a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:26:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:26:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:26:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 22:09:13 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 22:09:13 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 22:09:13 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 22:09:13 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:09:13 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 22:09:13 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 22:09:13 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 22:09:13 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 22:09:13 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 22:09:13 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 22:09:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 22:09:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 22:09:21 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 22:09:21 GMT
ENTRYPOINT []
# Tue, 12 May 2026 22:09:21 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:22:47 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 19:22:47 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom         -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Tue, 26 May 2026 19:22:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /usr/local/tomcat/webapps/geonetwork # buildkit
# Tue, 26 May 2026 19:22:47 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 19:22:47 GMT
ENV GN_VERSION=4.2.15
# Tue, 26 May 2026 19:22:47 GMT
ENV GN_DOWNLOAD_MD5=79cd931ac7fc0be044ec1f2dd44f3f96
# Tue, 26 May 2026 19:23:19 GMT
RUN set -eux;     cd /usr/local/tomcat/webapps/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 19:23:19 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 19:23:19 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 19:23:19 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 19:23:19 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:23:19 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:03a6f28563c3f1bd861a0bd521bea32abc15b3b1362797f0ee963f0cfbe31325`  
		Last Modified: Fri, 10 Apr 2026 09:34:31 GMT  
		Size: 26.9 MB (26859689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d6583703b067512ec399871388e06f946275b9fc2089cea0831dc05c6d42ce`  
		Last Modified: Tue, 12 May 2026 21:26:58 GMT  
		Size: 16.3 MB (16310544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24db8ad3b895582d531f43c1bba6830c1619b5af45379d90c6e23dba30a1c307`  
		Last Modified: Tue, 12 May 2026 21:26:59 GMT  
		Size: 39.8 MB (39772094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66ebfade72c1d1c1d2f9d5fea174a4f736377f63d0e9adec7e47b95fb73a083`  
		Last Modified: Tue, 12 May 2026 21:26:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c664c5544aa0e802217879a6d98de4534cd5151186c6297dbddaaea0155e36f7`  
		Last Modified: Tue, 12 May 2026 21:26:57 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265b28c1c18f6f6f2c2393377fab14703a3f1bfba209b5331b483bc8f766a5f6`  
		Last Modified: Tue, 12 May 2026 22:09:30 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5163af829dee1910bf8215756e6a18c305b24883aa4a4dad751c1915a66fac`  
		Last Modified: Tue, 12 May 2026 22:09:30 GMT  
		Size: 13.7 MB (13728884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71057eb7a57e8dc9240b0fc767c272795a2410fa1ae33937f4c58f1c414d3fce`  
		Last Modified: Tue, 12 May 2026 22:09:30 GMT  
		Size: 196.6 KB (196631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46292eb8911ca6621c2cfdb9bff7a66a50775dfff3db83d0ca27bbb7456c1b9b`  
		Last Modified: Tue, 26 May 2026 19:23:42 GMT  
		Size: 226.6 KB (226609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44fb9551472ffbf437c5ea42c6b3d88fc898bb3f30e5b9ac02faa61b0a19a87`  
		Last Modified: Tue, 26 May 2026 19:23:47 GMT  
		Size: 265.4 MB (265378532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852575738256d3efe5ef7bdb0d2d38e7370363458958d95f5988f8fa5a8304b2`  
		Last Modified: Tue, 26 May 2026 19:23:42 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c877983dbec8e1839b0ca0ced6be970c6febaa589e4c129a6563cb9e27d1f3a`  
		Last Modified: Tue, 26 May 2026 19:23:42 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2.15` - unknown; unknown

```console
$ docker pull geonetwork@sha256:5f499bf9aea670aaccd438eb71b8b290613ea9ba6a24822e7953803195fb10a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb33129c41572ab8d7b1f52fa78d430170c9dbc5100cf424c4deff7e8c64a35`

```dockerfile
```

-	Layers:
	-	`sha256:b5d65f052bb0ee49b0da2c6d6b3e55a4471fc3555e7a6a68aa9b76e86f902c33`  
		Last Modified: Tue, 26 May 2026 19:23:42 GMT  
		Size: 4.2 MB (4186780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50bd44a6bacc9f09c3045f370ac890b20940137a6d2e17ac02db69609bfceb03`  
		Last Modified: Tue, 26 May 2026 19:23:42 GMT  
		Size: 21.8 KB (21756 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.2.15` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:cc0e5801872d6428f189a6413b7258a1845cb65e8d0a560fe4a634b672248663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.8 MB (366833282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a52cd38875094765938650abc5f3bed09ce213ffc16f26647b9668bae8baa45`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:26:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:26:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:26:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:26:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:26:02 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:26:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8eef3d4a837bb7a9e45d30a7579d84d5b76a4321f4376573311e6bf89e48f9b0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='d5e50cb002600007dbdfac523605d26196607fa5212db0942ef05cdce9fe2892';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='5f0693c6c8ca0eb8df969bb1053b1926b1e7c57a3f90c6f9e8d493395e76a329';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='4f724a0fce1117521a3a3e55ebb0281d56f6c9a066092bc3186ee40d8cd955a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:26:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:26:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:26:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 22:10:12 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 22:10:12 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 22:10:12 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 22:10:13 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:10:13 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 22:10:13 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 22:10:13 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 22:10:13 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 22:10:13 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 22:10:13 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 22:10:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 22:10:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 22:10:20 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 22:10:20 GMT
ENTRYPOINT []
# Tue, 12 May 2026 22:10:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:19:07 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 19:19:07 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom         -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Tue, 26 May 2026 19:19:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /usr/local/tomcat/webapps/geonetwork # buildkit
# Tue, 26 May 2026 19:19:07 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 19:19:07 GMT
ENV GN_VERSION=4.2.15
# Tue, 26 May 2026 19:19:07 GMT
ENV GN_DOWNLOAD_MD5=79cd931ac7fc0be044ec1f2dd44f3f96
# Tue, 26 May 2026 19:20:09 GMT
RUN set -eux;     cd /usr/local/tomcat/webapps/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 19:20:09 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 19:20:09 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 19:20:09 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 19:20:09 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:20:09 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7746ead8bf3fc66cd94a81f8f77658aaf8a979318b7f92926e4502b5f21122ca`  
		Last Modified: Tue, 12 May 2026 21:26:16 GMT  
		Size: 17.0 MB (16997507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164abf015d7f4deff1ea843960d85ff9f8c61f5d7e7406e6b09c690122255cd1`  
		Last Modified: Tue, 12 May 2026 21:26:16 GMT  
		Size: 41.3 MB (41307612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012c4a5b70289a60f5f556c214705513c4d4b562642d638db51348295cef8f9a`  
		Last Modified: Tue, 12 May 2026 21:26:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e1b5f22335c0e983d38b92e1f26d67d1dec9f062689f9211065fc6d1e9e02c`  
		Last Modified: Tue, 12 May 2026 21:26:15 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b9858c4ac458d0467d3edd0eff33576f5d45179e458c73f57efd70a10b3b8c`  
		Last Modified: Tue, 12 May 2026 22:10:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8944894ca41bec2bdbc3329e258371e32acd0e10981327d5339ee40a7daabf8f`  
		Last Modified: Tue, 12 May 2026 22:10:30 GMT  
		Size: 13.8 MB (13804912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4106647bfe223cfcfbdaf9fdd3bfcd1333a4cc7e6e578a77979a37d338f1a356`  
		Last Modified: Tue, 12 May 2026 22:10:29 GMT  
		Size: 225.3 KB (225317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678f166d4d94ff4545657dca18996379c8fe1f0cb1a48d3e551389351bb3f93a`  
		Last Modified: Tue, 26 May 2026 19:20:31 GMT  
		Size: 238.3 KB (238290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119215e20a11c81078af1d7ec77115104397c1536ccad4410ddfdc473c4b3e7d`  
		Last Modified: Tue, 26 May 2026 19:20:37 GMT  
		Size: 265.4 MB (265378563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced8b4db44c2391bbf975167f19d648a4d249ee5f63151f831f5556f1768ae24`  
		Last Modified: Tue, 26 May 2026 19:20:31 GMT  
		Size: 1.5 KB (1505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f118615710f6dd69653dece083de4a5caa1aa60f0eef386d6978f526662e7dd9`  
		Last Modified: Tue, 26 May 2026 19:20:31 GMT  
		Size: 999.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2.15` - unknown; unknown

```console
$ docker pull geonetwork@sha256:5a51851e6c465efa700318c629c840c26f24c56aa3ce5de352a009dbadfd8d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4203702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d634a511812cf91dbcd893fae190e14c54ac7acf6ee69fa97196b896e980a279`

```dockerfile
```

-	Layers:
	-	`sha256:f41d248110b25c8dbb590a62a61b04c46e83d87194ef0a4f1b68673fd1eca397`  
		Last Modified: Tue, 26 May 2026 19:20:31 GMT  
		Size: 4.2 MB (4181929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b09e4d1a9ef44d486cc4bc7bceee7bc7bdba06376ee06027d5175f53fda07d1`  
		Last Modified: Tue, 26 May 2026 19:20:31 GMT  
		Size: 21.8 KB (21773 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.2.15` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:d911b40392c9c160fb215948c9b4e21e7eeafc8d82dec641d2fe4664d6f2a8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.6 MB (374610520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427405aac066abb23a810c5068695198cfc29070e50452fb445a482c9c7ca989`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 21:24:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:24:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:24:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:24:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 21:24:32 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:27:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8eef3d4a837bb7a9e45d30a7579d84d5b76a4321f4376573311e6bf89e48f9b0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='d5e50cb002600007dbdfac523605d26196607fa5212db0942ef05cdce9fe2892';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='5f0693c6c8ca0eb8df969bb1053b1926b1e7c57a3f90c6f9e8d493395e76a329';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='4f724a0fce1117521a3a3e55ebb0281d56f6c9a066092bc3186ee40d8cd955a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 12 May 2026 21:27:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:27:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:27:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 22:09:29 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 22:09:29 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 22:09:29 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 22:09:32 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 22:09:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 22:09:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 22:09:32 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 22:09:32 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 22:09:32 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 22:09:33 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 22:09:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 22:09:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 22:09:44 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 22:09:44 GMT
ENTRYPOINT []
# Tue, 12 May 2026 22:09:44 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 20:22:13 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 20:22:13 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom         -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Tue, 26 May 2026 20:22:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /usr/local/tomcat/webapps/geonetwork # buildkit
# Tue, 26 May 2026 20:22:13 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 20:22:13 GMT
ENV GN_VERSION=4.2.15
# Tue, 26 May 2026 20:22:13 GMT
ENV GN_DOWNLOAD_MD5=79cd931ac7fc0be044ec1f2dd44f3f96
# Tue, 26 May 2026 20:22:32 GMT
RUN set -eux;     cd /usr/local/tomcat/webapps/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 20:22:32 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 20:22:33 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 20:22:33 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 20:22:33 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 20:22:33 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb1e5ca7560d1a0a165fab55641320f02313ed8b7d7549036b7a5913ef35bb9`  
		Last Modified: Tue, 12 May 2026 21:25:16 GMT  
		Size: 18.8 MB (18813402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2819dacb96e17aa4ec53ff84c83bc66254a8ec89320ab127acd8fe5af348c6`  
		Last Modified: Tue, 12 May 2026 21:28:19 GMT  
		Size: 41.7 MB (41741551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1076e7e80cdeada102ee02d0c583c48c447bcc29ef916494fd2a0a1b1f72729`  
		Last Modified: Tue, 12 May 2026 21:28:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cc2ffed3a11d5178bf55daae8d1c2121e7758577dfcbe6b4482244d7b17734`  
		Last Modified: Tue, 12 May 2026 21:28:18 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542cb2211a02fe074d35f07f341ec0c5cda33089a75fdccb2410af709dd2a96b`  
		Last Modified: Tue, 12 May 2026 22:10:19 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5dd083c9cde15bfb885aebc235c8c309d9e12c101b6b396c0944cda236e68a`  
		Last Modified: Tue, 12 May 2026 22:10:20 GMT  
		Size: 13.8 MB (13831242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da01f83bf4d78bd15acd5553885c67f5f0040fbc7f8e02c5fde1edc0480595f9`  
		Last Modified: Tue, 12 May 2026 22:10:19 GMT  
		Size: 256.7 KB (256657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221221da7d50cc2c4c49e59c14a054fa0dd42074a86391292127f50f39c5789b`  
		Last Modified: Tue, 26 May 2026 20:23:21 GMT  
		Size: 269.6 KB (269642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64765807682b0ac15c48c90496c8f112754b428aa9d929813fbbc31d80ef2e2f`  
		Last Modified: Tue, 26 May 2026 20:23:28 GMT  
		Size: 265.4 MB (265378551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb960faa776d3d010c49f39591f171d512c4c71b7ad06da180967d4fd182437b`  
		Last Modified: Tue, 26 May 2026 20:23:22 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f649e5e982171ffb7aaf173dbe645f1ae11e88de0e3e9a23dbda25704dab51c7`  
		Last Modified: Tue, 26 May 2026 20:23:22 GMT  
		Size: 999.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2.15` - unknown; unknown

```console
$ docker pull geonetwork@sha256:9849aedcb2b957e6a727829c7f0cada93102b011e30ad5706452be073648d6bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4207258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe39241c7a0e2478c1faa167ccf988b68e4d3e906dd6114cd3f7d1bc8ff166b`

```dockerfile
```

-	Layers:
	-	`sha256:1aefdcd53966da25b89de81065b1126433c47b3190da1ae067a1deeadbf5e57d`  
		Last Modified: Tue, 26 May 2026 20:23:22 GMT  
		Size: 4.2 MB (4185546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:311569eda509f36c27687b259c0da0ca1ba7c84e8523c9acf434d964c44c8f33`  
		Last Modified: Tue, 26 May 2026 20:23:21 GMT  
		Size: 21.7 KB (21712 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.4`

```console
$ docker pull geonetwork@sha256:1c1bb0e4bc2c32b181602971a6760636e3e5659afe2b296818456cac0f620686
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `geonetwork:4.4` - linux; amd64

```console
$ docker pull geonetwork@sha256:091af31e85652383cba9f4069a718b61b48d928a87e46f59844abcbf701e7867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.6 MB (420631421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97663e8ce8f8d9e4597905e2e90ad25341bf99d0913b271d80e514d0b39775fe`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 29 Apr 2026 22:45:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:45:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:45:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:45:18 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Apr 2026 22:45:18 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:45:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:45:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:45:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:45:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 11 May 2026 23:28:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 11 May 2026 23:28:32 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:28:32 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 11 May 2026 23:28:32 GMT
WORKDIR /usr/local/tomcat
# Mon, 11 May 2026 23:28:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:28:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:28:32 GMT
ENV TOMCAT_MAJOR=9
# Mon, 11 May 2026 23:28:32 GMT
ENV TOMCAT_VERSION=9.0.118
# Mon, 11 May 2026 23:28:32 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Mon, 11 May 2026 23:28:32 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 11 May 2026 23:28:36 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:28:36 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 11 May 2026 23:28:36 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 11 May 2026 23:28:36 GMT
ENTRYPOINT []
# Mon, 11 May 2026 23:28:36 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:18:58 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 19:18:58 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 26 May 2026 19:18:58 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 26 May 2026 19:18:58 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 26 May 2026 19:18:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 26 May 2026 19:18:58 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 19:18:58 GMT
ENV GN_VERSION=4.4.10
# Tue, 26 May 2026 19:18:58 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 26 May 2026 19:19:24 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 19:19:24 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 26 May 2026 19:19:24 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 19:19:24 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 19:19:24 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 19:19:24 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:19:24 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf23ab6a8436ea4cc30c42c9eced3d7a9a42b066275648f8f1fbb0208b18c8fc`  
		Last Modified: Wed, 29 Apr 2026 22:45:34 GMT  
		Size: 17.0 MB (16983441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a14539c3f6df146437a21e07161e034b17f23dbe26ca23f9476c502b4c11df`  
		Last Modified: Wed, 29 Apr 2026 22:45:35 GMT  
		Size: 47.3 MB (47344091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288fd19c92924e5275f173c7e37ab77f791d263774ab4012d94aea4a7e017433`  
		Last Modified: Wed, 29 Apr 2026 22:45:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50069af557289dad3f81803ec84242ee38d92cc0440cca83f780e8ba4d498e4f`  
		Last Modified: Wed, 29 Apr 2026 22:45:33 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7ca595c1cdc53dff58e2b3a6153107fc81a7268f73191a74be7e474e14ed59`  
		Last Modified: Mon, 11 May 2026 23:28:44 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06493eda4e9a7d2b23bf3e6636af3dacc96c09641e54154aa1946effb90c6486`  
		Last Modified: Mon, 11 May 2026 23:28:45 GMT  
		Size: 13.8 MB (13796197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac16f181866752eb755aa0be0d49e0fe46f5415546b23a6f482aa911fb62975b`  
		Last Modified: Mon, 11 May 2026 23:28:44 GMT  
		Size: 224.7 KB (224711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301652bb5925b1827b165b5ab4b526f115ffcad9a18ed4c498248e1755b3918d`  
		Last Modified: Tue, 26 May 2026 19:19:46 GMT  
		Size: 801.2 KB (801153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580faf8d93c7ad4fe54e0ec31866eac5bdc1d7e623801f5f9fcea16079322838`  
		Last Modified: Tue, 26 May 2026 19:19:55 GMT  
		Size: 311.7 MB (311742287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65305e31e8a7d274d5b7e4aaaa51a87fd1498f829c54093d35e445ff8432921`  
		Last Modified: Tue, 26 May 2026 19:19:46 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78547240fa108460cca624821bdd9bdaa40632e77c3fe9f0183748660167ccc`  
		Last Modified: Tue, 26 May 2026 19:19:46 GMT  
		Size: 3.0 KB (3011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb9962a2ec25c6c14736c7c6bab123c904c35de138290510354b31b9690b017`  
		Last Modified: Tue, 26 May 2026 19:19:47 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:3500ea7c70984ba06a2209b87ef42a131983e9d2aab874dffeca07534346eedd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4218988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b0d9bf6f1cd55e1fee3b5172d5253154a0c9d87600f18eb3df04fac8031b2ea`

```dockerfile
```

-	Layers:
	-	`sha256:0aa54fecf16260834bc09fe1d7beb85e6184c1982119163848018902641d4190`  
		Last Modified: Tue, 26 May 2026 19:19:46 GMT  
		Size: 4.2 MB (4193558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4b9e3ae3f53beaacd9e2c7e102d2ba0eb7ec37661ca6ec2b3252b2ec29be58a`  
		Last Modified: Tue, 26 May 2026 19:19:46 GMT  
		Size: 25.4 KB (25430 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:078815e148dbfc72f5ef0f2d9a49b7046d0257250ed9c9f07f77e21fddc40a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.0 MB (415010904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9973dcb48dc41326f20fc607a2bf8b7095b78c2ef6196bf851cefc30506a50d`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:30 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:30 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:33 GMT
ADD file:341ecc672c4413d50e9543a8a38e44f8686dbdcc696b241b06e6b5b3a3ad57f6 in / 
# Fri, 10 Apr 2026 06:56:33 GMT
CMD ["/bin/bash"]
# Wed, 29 Apr 2026 22:45:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:45:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:45:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:45:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Apr 2026 22:45:50 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:45:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:45:54 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:45:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:45:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 11 May 2026 23:32:02 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 11 May 2026 23:32:02 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:32:02 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 11 May 2026 23:32:02 GMT
WORKDIR /usr/local/tomcat
# Mon, 11 May 2026 23:32:02 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:32:02 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:32:02 GMT
ENV TOMCAT_MAJOR=9
# Mon, 11 May 2026 23:32:02 GMT
ENV TOMCAT_VERSION=9.0.118
# Mon, 11 May 2026 23:32:02 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Mon, 11 May 2026 23:32:02 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 11 May 2026 23:32:08 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:32:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 11 May 2026 23:32:09 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 11 May 2026 23:32:09 GMT
ENTRYPOINT []
# Mon, 11 May 2026 23:32:09 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:22:49 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 19:22:49 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 26 May 2026 19:22:49 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 26 May 2026 19:22:49 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 26 May 2026 19:22:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 26 May 2026 19:22:49 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 19:22:49 GMT
ENV GN_VERSION=4.4.10
# Tue, 26 May 2026 19:22:49 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 26 May 2026 19:23:44 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 19:23:44 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 26 May 2026 19:23:44 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 19:23:44 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 19:23:44 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 19:23:44 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:23:44 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:03a6f28563c3f1bd861a0bd521bea32abc15b3b1362797f0ee963f0cfbe31325`  
		Last Modified: Fri, 10 Apr 2026 09:34:31 GMT  
		Size: 26.9 MB (26859689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3dcebaf2b2fcd539a30bc10bd91bbc7ef20caf11f1c358662e4ed783f9f102`  
		Last Modified: Wed, 29 Apr 2026 22:46:06 GMT  
		Size: 16.3 MB (16309684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f053e6426c790097075d4ca7bfd3ab90c6a6e96cdbbccf290cdb2a94445589`  
		Last Modified: Wed, 29 Apr 2026 22:46:07 GMT  
		Size: 45.5 MB (45452102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea68a1289a7d5d8edf9eded1c36c22635133ba55845322243cb20a0b0cdcdfd`  
		Last Modified: Wed, 29 Apr 2026 22:46:05 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34376f25195e52a2212871c8527277aa3bcd48be13afd35392696de749a7a56`  
		Last Modified: Wed, 29 Apr 2026 22:46:05 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9812430188f562534646d2616ab7a65aef552bef4d7fd50d0e646c38d49dc06d`  
		Last Modified: Mon, 11 May 2026 23:32:17 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5afef3c660b5106444ad7cd8e6b3e51ab20027742bb52a87a417e02564ecae`  
		Last Modified: Mon, 11 May 2026 23:32:18 GMT  
		Size: 13.7 MB (13730071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd5af756627697b9d0312dbc503baac6d124035a1ea54aded41bc3a7589a911`  
		Last Modified: Mon, 11 May 2026 23:32:17 GMT  
		Size: 196.5 KB (196474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df79545c33f0948e9238aeab008fdd4e07fa85179907a8e2aa7f4b25c805d40b`  
		Last Modified: Tue, 26 May 2026 19:24:08 GMT  
		Size: 714.0 KB (714029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cd9539d0d70e20b02dc1518f9f953d8d819677c19f89db82675cd65ce657f2`  
		Last Modified: Tue, 26 May 2026 19:24:14 GMT  
		Size: 311.7 MB (311742286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e394ae6b2e407c562fbe0e21dd720578e26f7d2cff2055a5dac4bcde2d7a681`  
		Last Modified: Tue, 26 May 2026 19:24:08 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03763171bafc34b7dc363c05ccc5209710063fdbefbdb05fd102d21b3137f298`  
		Last Modified: Tue, 26 May 2026 19:24:08 GMT  
		Size: 3.0 KB (3013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b60e92c376f95b932802a553ffa89296a702df5a94746caf99c8fc4ca9ef556`  
		Last Modified: Tue, 26 May 2026 19:24:09 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:f2f23a094e649ef271989597d3e1f365ce133cf849ec19eae366afcafe5255ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4222684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f040fd7f77614559a95cc3d01b878885e05b17195674b5ae76c5d6cb3853f05`

```dockerfile
```

-	Layers:
	-	`sha256:dd940f32ec01e09e6f7ff39f8d4618e0bd460de603d3aa769fa37296b1ed3bf7`  
		Last Modified: Tue, 26 May 2026 19:24:08 GMT  
		Size: 4.2 MB (4197161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbe94d55c25c0cd7b8b730338a6123f8d64c2808749991e6941171e807d7edd9`  
		Last Modified: Tue, 26 May 2026 19:24:08 GMT  
		Size: 25.5 KB (25523 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:b892c23b10e16891b1f3ebb00d9df9bdacca8ec34c8e187aa5ae6144a5342c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.1 MB (418108296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65f865a438974b29477b13b9b7acf8047b2c5e3414b4a04b835b71c655ebf42`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 29 Apr 2026 22:45:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:45:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:45:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:45:43 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Apr 2026 22:45:43 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:45:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:45:46 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:45:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:45:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 11 May 2026 23:27:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 11 May 2026 23:27:54 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:27:54 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 11 May 2026 23:27:54 GMT
WORKDIR /usr/local/tomcat
# Mon, 11 May 2026 23:27:54 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:27:54 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:27:54 GMT
ENV TOMCAT_MAJOR=9
# Mon, 11 May 2026 23:27:54 GMT
ENV TOMCAT_VERSION=9.0.118
# Mon, 11 May 2026 23:27:54 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Mon, 11 May 2026 23:27:54 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 11 May 2026 23:28:01 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:28:02 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 11 May 2026 23:28:02 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 11 May 2026 23:28:02 GMT
ENTRYPOINT []
# Mon, 11 May 2026 23:28:02 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:19:08 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 19:19:08 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 26 May 2026 19:19:08 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 26 May 2026 19:19:08 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 26 May 2026 19:19:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 26 May 2026 19:19:08 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 19:19:08 GMT
ENV GN_VERSION=4.4.10
# Tue, 26 May 2026 19:19:08 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 26 May 2026 19:20:20 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 19:20:20 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 26 May 2026 19:20:20 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 19:20:20 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 19:20:20 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 19:20:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:20:20 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340297f35e2c376c99270f2485ce4edd3c92de46a0bbef95a9bce7a944b35238`  
		Last Modified: Wed, 29 Apr 2026 22:45:59 GMT  
		Size: 17.0 MB (16996253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a8f9d2e0cdee350d3ed81afb01002bf9e394770886cecaed65f94e9470854`  
		Last Modified: Wed, 29 Apr 2026 22:46:00 GMT  
		Size: 45.7 MB (45660771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8b082d384d013a651b9a297183b301e82f6a59914d0873722ee08ae517b26e`  
		Last Modified: Wed, 29 Apr 2026 22:45:58 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08b5a1d9756317e6e8d13806e18cd14d78e5909594672612e96f2e3669b4f15`  
		Last Modified: Wed, 29 Apr 2026 22:45:58 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccb01e6b7b0d3a577dc45fc8232d7b6818325ffd7c939319446fd423064d38c`  
		Last Modified: Mon, 11 May 2026 23:28:11 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56c6f243e717ed8ba18b3c43492501aa31eb08d7c0df5075474090ed42d5d25`  
		Last Modified: Mon, 11 May 2026 23:28:11 GMT  
		Size: 13.8 MB (13805554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da79f66c4b83e2df5f98493f6db136efc253662ed6bc3b524de0003aaadcd61`  
		Last Modified: Mon, 11 May 2026 23:28:11 GMT  
		Size: 225.3 KB (225280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc0e8f9e38ddd9b7f35374c4e54287f9e77e32f49d9ee062b0d381934467ed5`  
		Last Modified: Tue, 26 May 2026 19:20:45 GMT  
		Size: 795.8 KB (795754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bde8402bddd9ebda751686e1c0caec51c340a6cbe8afe3c0c709704532e8f7e`  
		Last Modified: Tue, 26 May 2026 19:20:52 GMT  
		Size: 311.7 MB (311742326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59445f2b0af00976dca76cca13d75abc90c8755185a479a1cef6b3b0e56648c`  
		Last Modified: Tue, 26 May 2026 19:20:45 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff795d7978acc5515e1d3183acce6dc5ecf30ba249554f0329c769a5a9f10edf`  
		Last Modified: Tue, 26 May 2026 19:20:45 GMT  
		Size: 3.0 KB (3014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acd7f4b488604821d030d1151546d2721d1c968e01fe3f77b7ef85fa84f6252`  
		Last Modified: Tue, 26 May 2026 19:20:46 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:02233406faf8b5d980db73662d831319c86dc7a8630d8f41b2cb5a14b56ae715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4220197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c691eeb4dc4eb0c780cad66e7c54f472f4bb685e5bcb8f6b44ce873b1c7b5c`

```dockerfile
```

-	Layers:
	-	`sha256:6625220a3d7971d6beed82f28f2797e32db30a4c4c6cb94cf87c52c4f1343454`  
		Last Modified: Tue, 26 May 2026 19:20:45 GMT  
		Size: 4.2 MB (4194648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9de6fce6dbd22d640264b16c99c9b4891344a3d1fadaa2dc3935f7eeca6cd3d6`  
		Last Modified: Tue, 26 May 2026 19:20:45 GMT  
		Size: 25.5 KB (25549 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:065fbac665c5ccbd330eb99e634a931dda7a5f6c8654e613f247c00abaf0c3ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.7 MB (422738247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3532be992ebcedf7f8b743a45f584148c462a8ab96e1b968cbc74d747a5617f`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:12:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:12:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:12:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:12:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:12:34 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:45:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:45:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:45:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:45:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 01:22:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 01:22:58 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 01:22:58 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 01:22:58 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 01:22:58 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 01:22:58 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 01:22:58 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 01:22:58 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 01:22:58 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 01:22:59 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 01:23:07 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 01:23:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 01:23:09 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 01:23:09 GMT
ENTRYPOINT []
# Tue, 12 May 2026 01:23:09 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 20:22:54 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 20:22:54 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 26 May 2026 20:22:54 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 26 May 2026 20:22:54 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 26 May 2026 20:22:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 26 May 2026 20:22:54 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 20:22:54 GMT
ENV GN_VERSION=4.4.10
# Tue, 26 May 2026 20:22:54 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 26 May 2026 20:23:13 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 20:23:14 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 26 May 2026 20:23:14 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 20:23:15 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 20:23:15 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 20:23:15 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 20:23:15 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13718497a6adee31aa098ce2c85aca5feeb60aa6f13ee0ac169b2a181311f2cd`  
		Last Modified: Wed, 15 Apr 2026 21:13:20 GMT  
		Size: 18.8 MB (18813307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777cb69b760c692aaca637d1f978ca71a27e8f712772ebee4f24d36075f9e119`  
		Last Modified: Wed, 29 Apr 2026 22:46:19 GMT  
		Size: 42.8 MB (42813437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7f006dbd4d35f9dc4139ef666a81408417cd773080cdf49bb5876a1228c7a0`  
		Last Modified: Wed, 29 Apr 2026 22:46:18 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62105aa809cab5140e7f62bdbab1c9624ce547772bb7b5e7b61d334457d61a3b`  
		Last Modified: Wed, 29 Apr 2026 22:46:18 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64ac7edd53aaec8649090cca5b03990f58f860ea148a5da89d274fb41c41609`  
		Last Modified: Tue, 12 May 2026 01:23:33 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3125d2db6abf2edbd83717983bb17c1b31afcfaa662341d3dd858d0a812e4f6`  
		Last Modified: Tue, 12 May 2026 01:23:33 GMT  
		Size: 13.8 MB (13831958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f12f88f8c1d63dbca0713f1ac021902a8ec4b59a5003b102e4f0dc3bdcdb67`  
		Last Modified: Tue, 12 May 2026 01:23:33 GMT  
		Size: 256.7 KB (256653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0837cc78d6d0d644b064b7d8664e3978efb5e9abb3360bd237b6dbb67bacfb0`  
		Last Modified: Tue, 26 May 2026 20:24:02 GMT  
		Size: 959.8 KB (959838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390e02e08f47bb475b2a002d2732c6fab3e0a7213c996b6b76ec098b8531b347`  
		Last Modified: Tue, 26 May 2026 20:24:09 GMT  
		Size: 311.7 MB (311742307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311d5798f7d276ef1904ae9961d12de257c80ac83afcf7920ac3bbc39c6e47f6`  
		Last Modified: Tue, 26 May 2026 20:24:02 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894173186f8c6225d36ea08a8379237ec9a3cc1b95dbff3b17e7d076a70068d9`  
		Last Modified: Tue, 26 May 2026 20:24:02 GMT  
		Size: 3.0 KB (3016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7beb0611be5018411ef263cfb2b79f931a40b221ba55629c055508565bedbb4d`  
		Last Modified: Tue, 26 May 2026 20:24:03 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:706b4b5a7348d850ea13e80a6ad9dde29cc228708e6976584d7f1f64978ad4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4223112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3135bcb3a1755a7cd165f5843f0dfafd495327ae4161f2f7b7dcbf752eac8f75`

```dockerfile
```

-	Layers:
	-	`sha256:338eada16d2652193771bb358aeab313bdcbc4a8b56a987797f3f275ff190038`  
		Last Modified: Tue, 26 May 2026 20:24:02 GMT  
		Size: 4.2 MB (4197637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bae2cd05343a8d4a072e7b8f8407f9904236e48fb6ea27bb33a0a7732a791a1`  
		Last Modified: Tue, 26 May 2026 20:24:02 GMT  
		Size: 25.5 KB (25475 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4` - linux; s390x

```console
$ docker pull geonetwork@sha256:b7ea2a6440ebdc6e96b122291b8edce2b37d979511458c56dbe605bdd9a6fbab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.5 MB (415480524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2418672e41bacffd94b20e96aae257b1238fda21e72b7797a8d9038a2b68b2d`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:50:27 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:50:29 GMT
ADD file:41defd98c44eed6fc946fd94496a94164879f2ad4f63d66a5c1e213cc2259ad1 in / 
# Fri, 10 Apr 2026 06:50:29 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:44:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:44:12 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:43:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:43:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:43:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:43:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 11 May 2026 23:52:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 11 May 2026 23:52:35 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:52:35 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 11 May 2026 23:52:35 GMT
WORKDIR /usr/local/tomcat
# Mon, 11 May 2026 23:52:35 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:52:35 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:52:35 GMT
ENV TOMCAT_MAJOR=9
# Mon, 11 May 2026 23:52:35 GMT
ENV TOMCAT_VERSION=9.0.118
# Mon, 11 May 2026 23:52:35 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Mon, 11 May 2026 23:52:35 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 11 May 2026 23:52:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:52:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 11 May 2026 23:52:39 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 11 May 2026 23:52:39 GMT
ENTRYPOINT []
# Mon, 11 May 2026 23:52:39 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 20:00:27 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 20:00:27 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 26 May 2026 20:00:27 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 26 May 2026 20:00:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 26 May 2026 20:00:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 26 May 2026 20:00:27 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 20:00:27 GMT
ENV GN_VERSION=4.4.10
# Tue, 26 May 2026 20:00:27 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 26 May 2026 20:00:46 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 20:00:46 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 26 May 2026 20:00:46 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 20:00:46 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 20:00:46 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 20:00:46 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 20:00:46 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:ef1c26d09a5f9962879f732e212c4246a41e8473f6120efb435886357c85dd5a`  
		Last Modified: Fri, 10 Apr 2026 09:34:53 GMT  
		Size: 29.9 MB (29912147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5a3498cd625b1c7f2fe4f65685d4036d3cad9b92fdc3a7c30d047b0511431d`  
		Last Modified: Wed, 15 Apr 2026 20:44:43 GMT  
		Size: 17.6 MB (17579116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb83646d8cec7253c91045c8e0b103abc33d9faba0838653791cc13cfd2131d`  
		Last Modified: Wed, 29 Apr 2026 22:43:50 GMT  
		Size: 41.4 MB (41358769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d1ad21b5f4affc0bdf817bc13bc1b05c5e24c5728fc980722be40acf096d52`  
		Last Modified: Wed, 29 Apr 2026 22:43:49 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55a0630eea6b0c3f15ae53ad6c9f09b28ec02d6d14461bd65f1672e3066b8b8`  
		Last Modified: Wed, 29 Apr 2026 22:43:50 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef363bd4cee4e70ac0af7fd7af4b7e52eeba57c7a34b82803d8b38577887af9c`  
		Last Modified: Mon, 11 May 2026 23:52:52 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df865499b28393bd025d1ee75ad7d094381abf897ec9598f6926505a2beded93`  
		Last Modified: Mon, 11 May 2026 23:52:52 GMT  
		Size: 13.8 MB (13804833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74fe6edaae19a35d37b18d5121fa781cb38333b11d3dc82ea8cba63c14db5aa`  
		Last Modified: Mon, 11 May 2026 23:52:52 GMT  
		Size: 232.9 KB (232950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aea2f91b5b2d9900add721a42ab843517ae01adde6c3463235ab3e137725200`  
		Last Modified: Tue, 26 May 2026 20:01:48 GMT  
		Size: 843.8 KB (843799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1571be11b97395ab029de35d8b10c01eed74e123359af9b5d04290fd87d309`  
		Last Modified: Tue, 26 May 2026 20:01:54 GMT  
		Size: 311.7 MB (311742343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886e5a4b0db6f174fcde33323e4fac33c45cf45d2247ec34a062c37f0a0af2a9`  
		Last Modified: Tue, 26 May 2026 20:01:48 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e49d70370c8456159089603d94e0524719b9de002afe100cee3aaab89c88e5e`  
		Last Modified: Tue, 26 May 2026 20:01:48 GMT  
		Size: 3.0 KB (3013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c01440357dabb831ad91c416559f54c00951ff6e2088f72b26246ca053e65ae`  
		Last Modified: Tue, 26 May 2026 20:01:49 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:4c6791c4a2fb4f87bd89cf0514da8f74b41734151b1784c74dd913baf768603f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4221193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84ef0d33fb600070830a943fc3f30191ef63f78212ffacd313669917141df84`

```dockerfile
```

-	Layers:
	-	`sha256:b95bfa55a71f73c618ff7074b52701aa296b286e4f8cf72c67836f0bc2e2b37d`  
		Last Modified: Tue, 26 May 2026 20:01:48 GMT  
		Size: 4.2 MB (4195763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d3b55ef5c7d3537471dbce478b79dcc2fd257b48859a212457a4fecd438ef79`  
		Last Modified: Tue, 26 May 2026 20:01:48 GMT  
		Size: 25.4 KB (25430 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.4.10`

```console
$ docker pull geonetwork@sha256:1c1bb0e4bc2c32b181602971a6760636e3e5659afe2b296818456cac0f620686
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `geonetwork:4.4.10` - linux; amd64

```console
$ docker pull geonetwork@sha256:091af31e85652383cba9f4069a718b61b48d928a87e46f59844abcbf701e7867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.6 MB (420631421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97663e8ce8f8d9e4597905e2e90ad25341bf99d0913b271d80e514d0b39775fe`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 29 Apr 2026 22:45:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:45:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:45:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:45:18 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Apr 2026 22:45:18 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:45:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:45:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:45:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:45:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 11 May 2026 23:28:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 11 May 2026 23:28:32 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:28:32 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 11 May 2026 23:28:32 GMT
WORKDIR /usr/local/tomcat
# Mon, 11 May 2026 23:28:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:28:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:28:32 GMT
ENV TOMCAT_MAJOR=9
# Mon, 11 May 2026 23:28:32 GMT
ENV TOMCAT_VERSION=9.0.118
# Mon, 11 May 2026 23:28:32 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Mon, 11 May 2026 23:28:32 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 11 May 2026 23:28:36 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:28:36 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 11 May 2026 23:28:36 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 11 May 2026 23:28:36 GMT
ENTRYPOINT []
# Mon, 11 May 2026 23:28:36 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:18:58 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 19:18:58 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 26 May 2026 19:18:58 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 26 May 2026 19:18:58 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 26 May 2026 19:18:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 26 May 2026 19:18:58 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 19:18:58 GMT
ENV GN_VERSION=4.4.10
# Tue, 26 May 2026 19:18:58 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 26 May 2026 19:19:24 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 19:19:24 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 26 May 2026 19:19:24 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 19:19:24 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 19:19:24 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 19:19:24 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:19:24 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf23ab6a8436ea4cc30c42c9eced3d7a9a42b066275648f8f1fbb0208b18c8fc`  
		Last Modified: Wed, 29 Apr 2026 22:45:34 GMT  
		Size: 17.0 MB (16983441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a14539c3f6df146437a21e07161e034b17f23dbe26ca23f9476c502b4c11df`  
		Last Modified: Wed, 29 Apr 2026 22:45:35 GMT  
		Size: 47.3 MB (47344091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288fd19c92924e5275f173c7e37ab77f791d263774ab4012d94aea4a7e017433`  
		Last Modified: Wed, 29 Apr 2026 22:45:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50069af557289dad3f81803ec84242ee38d92cc0440cca83f780e8ba4d498e4f`  
		Last Modified: Wed, 29 Apr 2026 22:45:33 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7ca595c1cdc53dff58e2b3a6153107fc81a7268f73191a74be7e474e14ed59`  
		Last Modified: Mon, 11 May 2026 23:28:44 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06493eda4e9a7d2b23bf3e6636af3dacc96c09641e54154aa1946effb90c6486`  
		Last Modified: Mon, 11 May 2026 23:28:45 GMT  
		Size: 13.8 MB (13796197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac16f181866752eb755aa0be0d49e0fe46f5415546b23a6f482aa911fb62975b`  
		Last Modified: Mon, 11 May 2026 23:28:44 GMT  
		Size: 224.7 KB (224711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301652bb5925b1827b165b5ab4b526f115ffcad9a18ed4c498248e1755b3918d`  
		Last Modified: Tue, 26 May 2026 19:19:46 GMT  
		Size: 801.2 KB (801153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580faf8d93c7ad4fe54e0ec31866eac5bdc1d7e623801f5f9fcea16079322838`  
		Last Modified: Tue, 26 May 2026 19:19:55 GMT  
		Size: 311.7 MB (311742287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65305e31e8a7d274d5b7e4aaaa51a87fd1498f829c54093d35e445ff8432921`  
		Last Modified: Tue, 26 May 2026 19:19:46 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78547240fa108460cca624821bdd9bdaa40632e77c3fe9f0183748660167ccc`  
		Last Modified: Tue, 26 May 2026 19:19:46 GMT  
		Size: 3.0 KB (3011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb9962a2ec25c6c14736c7c6bab123c904c35de138290510354b31b9690b017`  
		Last Modified: Tue, 26 May 2026 19:19:47 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4.10` - unknown; unknown

```console
$ docker pull geonetwork@sha256:3500ea7c70984ba06a2209b87ef42a131983e9d2aab874dffeca07534346eedd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4218988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b0d9bf6f1cd55e1fee3b5172d5253154a0c9d87600f18eb3df04fac8031b2ea`

```dockerfile
```

-	Layers:
	-	`sha256:0aa54fecf16260834bc09fe1d7beb85e6184c1982119163848018902641d4190`  
		Last Modified: Tue, 26 May 2026 19:19:46 GMT  
		Size: 4.2 MB (4193558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4b9e3ae3f53beaacd9e2c7e102d2ba0eb7ec37661ca6ec2b3252b2ec29be58a`  
		Last Modified: Tue, 26 May 2026 19:19:46 GMT  
		Size: 25.4 KB (25430 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4.10` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:078815e148dbfc72f5ef0f2d9a49b7046d0257250ed9c9f07f77e21fddc40a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.0 MB (415010904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9973dcb48dc41326f20fc607a2bf8b7095b78c2ef6196bf851cefc30506a50d`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:30 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:30 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:33 GMT
ADD file:341ecc672c4413d50e9543a8a38e44f8686dbdcc696b241b06e6b5b3a3ad57f6 in / 
# Fri, 10 Apr 2026 06:56:33 GMT
CMD ["/bin/bash"]
# Wed, 29 Apr 2026 22:45:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:45:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:45:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:45:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Apr 2026 22:45:50 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:45:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:45:54 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:45:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:45:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 11 May 2026 23:32:02 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 11 May 2026 23:32:02 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:32:02 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 11 May 2026 23:32:02 GMT
WORKDIR /usr/local/tomcat
# Mon, 11 May 2026 23:32:02 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:32:02 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:32:02 GMT
ENV TOMCAT_MAJOR=9
# Mon, 11 May 2026 23:32:02 GMT
ENV TOMCAT_VERSION=9.0.118
# Mon, 11 May 2026 23:32:02 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Mon, 11 May 2026 23:32:02 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 11 May 2026 23:32:08 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:32:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 11 May 2026 23:32:09 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 11 May 2026 23:32:09 GMT
ENTRYPOINT []
# Mon, 11 May 2026 23:32:09 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:22:49 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 19:22:49 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 26 May 2026 19:22:49 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 26 May 2026 19:22:49 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 26 May 2026 19:22:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 26 May 2026 19:22:49 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 19:22:49 GMT
ENV GN_VERSION=4.4.10
# Tue, 26 May 2026 19:22:49 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 26 May 2026 19:23:44 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 19:23:44 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 26 May 2026 19:23:44 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 19:23:44 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 19:23:44 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 19:23:44 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:23:44 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:03a6f28563c3f1bd861a0bd521bea32abc15b3b1362797f0ee963f0cfbe31325`  
		Last Modified: Fri, 10 Apr 2026 09:34:31 GMT  
		Size: 26.9 MB (26859689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3dcebaf2b2fcd539a30bc10bd91bbc7ef20caf11f1c358662e4ed783f9f102`  
		Last Modified: Wed, 29 Apr 2026 22:46:06 GMT  
		Size: 16.3 MB (16309684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f053e6426c790097075d4ca7bfd3ab90c6a6e96cdbbccf290cdb2a94445589`  
		Last Modified: Wed, 29 Apr 2026 22:46:07 GMT  
		Size: 45.5 MB (45452102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea68a1289a7d5d8edf9eded1c36c22635133ba55845322243cb20a0b0cdcdfd`  
		Last Modified: Wed, 29 Apr 2026 22:46:05 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34376f25195e52a2212871c8527277aa3bcd48be13afd35392696de749a7a56`  
		Last Modified: Wed, 29 Apr 2026 22:46:05 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9812430188f562534646d2616ab7a65aef552bef4d7fd50d0e646c38d49dc06d`  
		Last Modified: Mon, 11 May 2026 23:32:17 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5afef3c660b5106444ad7cd8e6b3e51ab20027742bb52a87a417e02564ecae`  
		Last Modified: Mon, 11 May 2026 23:32:18 GMT  
		Size: 13.7 MB (13730071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd5af756627697b9d0312dbc503baac6d124035a1ea54aded41bc3a7589a911`  
		Last Modified: Mon, 11 May 2026 23:32:17 GMT  
		Size: 196.5 KB (196474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df79545c33f0948e9238aeab008fdd4e07fa85179907a8e2aa7f4b25c805d40b`  
		Last Modified: Tue, 26 May 2026 19:24:08 GMT  
		Size: 714.0 KB (714029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cd9539d0d70e20b02dc1518f9f953d8d819677c19f89db82675cd65ce657f2`  
		Last Modified: Tue, 26 May 2026 19:24:14 GMT  
		Size: 311.7 MB (311742286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e394ae6b2e407c562fbe0e21dd720578e26f7d2cff2055a5dac4bcde2d7a681`  
		Last Modified: Tue, 26 May 2026 19:24:08 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03763171bafc34b7dc363c05ccc5209710063fdbefbdb05fd102d21b3137f298`  
		Last Modified: Tue, 26 May 2026 19:24:08 GMT  
		Size: 3.0 KB (3013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b60e92c376f95b932802a553ffa89296a702df5a94746caf99c8fc4ca9ef556`  
		Last Modified: Tue, 26 May 2026 19:24:09 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4.10` - unknown; unknown

```console
$ docker pull geonetwork@sha256:f2f23a094e649ef271989597d3e1f365ce133cf849ec19eae366afcafe5255ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4222684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f040fd7f77614559a95cc3d01b878885e05b17195674b5ae76c5d6cb3853f05`

```dockerfile
```

-	Layers:
	-	`sha256:dd940f32ec01e09e6f7ff39f8d4618e0bd460de603d3aa769fa37296b1ed3bf7`  
		Last Modified: Tue, 26 May 2026 19:24:08 GMT  
		Size: 4.2 MB (4197161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbe94d55c25c0cd7b8b730338a6123f8d64c2808749991e6941171e807d7edd9`  
		Last Modified: Tue, 26 May 2026 19:24:08 GMT  
		Size: 25.5 KB (25523 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4.10` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:b892c23b10e16891b1f3ebb00d9df9bdacca8ec34c8e187aa5ae6144a5342c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.1 MB (418108296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65f865a438974b29477b13b9b7acf8047b2c5e3414b4a04b835b71c655ebf42`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 29 Apr 2026 22:45:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:45:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:45:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:45:43 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Apr 2026 22:45:43 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:45:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:45:46 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:45:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:45:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 11 May 2026 23:27:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 11 May 2026 23:27:54 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:27:54 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 11 May 2026 23:27:54 GMT
WORKDIR /usr/local/tomcat
# Mon, 11 May 2026 23:27:54 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:27:54 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:27:54 GMT
ENV TOMCAT_MAJOR=9
# Mon, 11 May 2026 23:27:54 GMT
ENV TOMCAT_VERSION=9.0.118
# Mon, 11 May 2026 23:27:54 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Mon, 11 May 2026 23:27:54 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 11 May 2026 23:28:01 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:28:02 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 11 May 2026 23:28:02 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 11 May 2026 23:28:02 GMT
ENTRYPOINT []
# Mon, 11 May 2026 23:28:02 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:19:08 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 19:19:08 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 26 May 2026 19:19:08 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 26 May 2026 19:19:08 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 26 May 2026 19:19:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 26 May 2026 19:19:08 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 19:19:08 GMT
ENV GN_VERSION=4.4.10
# Tue, 26 May 2026 19:19:08 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 26 May 2026 19:20:20 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 19:20:20 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 26 May 2026 19:20:20 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 19:20:20 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 19:20:20 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 19:20:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:20:20 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340297f35e2c376c99270f2485ce4edd3c92de46a0bbef95a9bce7a944b35238`  
		Last Modified: Wed, 29 Apr 2026 22:45:59 GMT  
		Size: 17.0 MB (16996253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a8f9d2e0cdee350d3ed81afb01002bf9e394770886cecaed65f94e9470854`  
		Last Modified: Wed, 29 Apr 2026 22:46:00 GMT  
		Size: 45.7 MB (45660771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8b082d384d013a651b9a297183b301e82f6a59914d0873722ee08ae517b26e`  
		Last Modified: Wed, 29 Apr 2026 22:45:58 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08b5a1d9756317e6e8d13806e18cd14d78e5909594672612e96f2e3669b4f15`  
		Last Modified: Wed, 29 Apr 2026 22:45:58 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccb01e6b7b0d3a577dc45fc8232d7b6818325ffd7c939319446fd423064d38c`  
		Last Modified: Mon, 11 May 2026 23:28:11 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56c6f243e717ed8ba18b3c43492501aa31eb08d7c0df5075474090ed42d5d25`  
		Last Modified: Mon, 11 May 2026 23:28:11 GMT  
		Size: 13.8 MB (13805554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da79f66c4b83e2df5f98493f6db136efc253662ed6bc3b524de0003aaadcd61`  
		Last Modified: Mon, 11 May 2026 23:28:11 GMT  
		Size: 225.3 KB (225280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc0e8f9e38ddd9b7f35374c4e54287f9e77e32f49d9ee062b0d381934467ed5`  
		Last Modified: Tue, 26 May 2026 19:20:45 GMT  
		Size: 795.8 KB (795754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bde8402bddd9ebda751686e1c0caec51c340a6cbe8afe3c0c709704532e8f7e`  
		Last Modified: Tue, 26 May 2026 19:20:52 GMT  
		Size: 311.7 MB (311742326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59445f2b0af00976dca76cca13d75abc90c8755185a479a1cef6b3b0e56648c`  
		Last Modified: Tue, 26 May 2026 19:20:45 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff795d7978acc5515e1d3183acce6dc5ecf30ba249554f0329c769a5a9f10edf`  
		Last Modified: Tue, 26 May 2026 19:20:45 GMT  
		Size: 3.0 KB (3014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acd7f4b488604821d030d1151546d2721d1c968e01fe3f77b7ef85fa84f6252`  
		Last Modified: Tue, 26 May 2026 19:20:46 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4.10` - unknown; unknown

```console
$ docker pull geonetwork@sha256:02233406faf8b5d980db73662d831319c86dc7a8630d8f41b2cb5a14b56ae715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4220197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c691eeb4dc4eb0c780cad66e7c54f472f4bb685e5bcb8f6b44ce873b1c7b5c`

```dockerfile
```

-	Layers:
	-	`sha256:6625220a3d7971d6beed82f28f2797e32db30a4c4c6cb94cf87c52c4f1343454`  
		Last Modified: Tue, 26 May 2026 19:20:45 GMT  
		Size: 4.2 MB (4194648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9de6fce6dbd22d640264b16c99c9b4891344a3d1fadaa2dc3935f7eeca6cd3d6`  
		Last Modified: Tue, 26 May 2026 19:20:45 GMT  
		Size: 25.5 KB (25549 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4.10` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:065fbac665c5ccbd330eb99e634a931dda7a5f6c8654e613f247c00abaf0c3ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.7 MB (422738247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3532be992ebcedf7f8b743a45f584148c462a8ab96e1b968cbc74d747a5617f`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:12:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:12:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:12:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:12:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:12:34 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:45:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:45:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:45:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:45:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 01:22:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 01:22:58 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 01:22:58 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 01:22:58 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 01:22:58 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 01:22:58 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 01:22:58 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 01:22:58 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 01:22:58 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 01:22:59 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 01:23:07 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 01:23:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 01:23:09 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 01:23:09 GMT
ENTRYPOINT []
# Tue, 12 May 2026 01:23:09 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 20:22:54 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 20:22:54 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 26 May 2026 20:22:54 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 26 May 2026 20:22:54 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 26 May 2026 20:22:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 26 May 2026 20:22:54 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 20:22:54 GMT
ENV GN_VERSION=4.4.10
# Tue, 26 May 2026 20:22:54 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 26 May 2026 20:23:13 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 20:23:14 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 26 May 2026 20:23:14 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 20:23:15 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 20:23:15 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 20:23:15 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 20:23:15 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13718497a6adee31aa098ce2c85aca5feeb60aa6f13ee0ac169b2a181311f2cd`  
		Last Modified: Wed, 15 Apr 2026 21:13:20 GMT  
		Size: 18.8 MB (18813307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777cb69b760c692aaca637d1f978ca71a27e8f712772ebee4f24d36075f9e119`  
		Last Modified: Wed, 29 Apr 2026 22:46:19 GMT  
		Size: 42.8 MB (42813437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7f006dbd4d35f9dc4139ef666a81408417cd773080cdf49bb5876a1228c7a0`  
		Last Modified: Wed, 29 Apr 2026 22:46:18 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62105aa809cab5140e7f62bdbab1c9624ce547772bb7b5e7b61d334457d61a3b`  
		Last Modified: Wed, 29 Apr 2026 22:46:18 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64ac7edd53aaec8649090cca5b03990f58f860ea148a5da89d274fb41c41609`  
		Last Modified: Tue, 12 May 2026 01:23:33 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3125d2db6abf2edbd83717983bb17c1b31afcfaa662341d3dd858d0a812e4f6`  
		Last Modified: Tue, 12 May 2026 01:23:33 GMT  
		Size: 13.8 MB (13831958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f12f88f8c1d63dbca0713f1ac021902a8ec4b59a5003b102e4f0dc3bdcdb67`  
		Last Modified: Tue, 12 May 2026 01:23:33 GMT  
		Size: 256.7 KB (256653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0837cc78d6d0d644b064b7d8664e3978efb5e9abb3360bd237b6dbb67bacfb0`  
		Last Modified: Tue, 26 May 2026 20:24:02 GMT  
		Size: 959.8 KB (959838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390e02e08f47bb475b2a002d2732c6fab3e0a7213c996b6b76ec098b8531b347`  
		Last Modified: Tue, 26 May 2026 20:24:09 GMT  
		Size: 311.7 MB (311742307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311d5798f7d276ef1904ae9961d12de257c80ac83afcf7920ac3bbc39c6e47f6`  
		Last Modified: Tue, 26 May 2026 20:24:02 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894173186f8c6225d36ea08a8379237ec9a3cc1b95dbff3b17e7d076a70068d9`  
		Last Modified: Tue, 26 May 2026 20:24:02 GMT  
		Size: 3.0 KB (3016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7beb0611be5018411ef263cfb2b79f931a40b221ba55629c055508565bedbb4d`  
		Last Modified: Tue, 26 May 2026 20:24:03 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4.10` - unknown; unknown

```console
$ docker pull geonetwork@sha256:706b4b5a7348d850ea13e80a6ad9dde29cc228708e6976584d7f1f64978ad4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4223112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3135bcb3a1755a7cd165f5843f0dfafd495327ae4161f2f7b7dcbf752eac8f75`

```dockerfile
```

-	Layers:
	-	`sha256:338eada16d2652193771bb358aeab313bdcbc4a8b56a987797f3f275ff190038`  
		Last Modified: Tue, 26 May 2026 20:24:02 GMT  
		Size: 4.2 MB (4197637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bae2cd05343a8d4a072e7b8f8407f9904236e48fb6ea27bb33a0a7732a791a1`  
		Last Modified: Tue, 26 May 2026 20:24:02 GMT  
		Size: 25.5 KB (25475 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4.10` - linux; s390x

```console
$ docker pull geonetwork@sha256:b7ea2a6440ebdc6e96b122291b8edce2b37d979511458c56dbe605bdd9a6fbab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.5 MB (415480524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2418672e41bacffd94b20e96aae257b1238fda21e72b7797a8d9038a2b68b2d`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:50:27 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:50:29 GMT
ADD file:41defd98c44eed6fc946fd94496a94164879f2ad4f63d66a5c1e213cc2259ad1 in / 
# Fri, 10 Apr 2026 06:50:29 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:44:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:44:12 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:43:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:43:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:43:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:43:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 11 May 2026 23:52:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 11 May 2026 23:52:35 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:52:35 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 11 May 2026 23:52:35 GMT
WORKDIR /usr/local/tomcat
# Mon, 11 May 2026 23:52:35 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:52:35 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:52:35 GMT
ENV TOMCAT_MAJOR=9
# Mon, 11 May 2026 23:52:35 GMT
ENV TOMCAT_VERSION=9.0.118
# Mon, 11 May 2026 23:52:35 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Mon, 11 May 2026 23:52:35 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 11 May 2026 23:52:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:52:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 11 May 2026 23:52:39 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 11 May 2026 23:52:39 GMT
ENTRYPOINT []
# Mon, 11 May 2026 23:52:39 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 20:00:27 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 20:00:27 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 26 May 2026 20:00:27 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 26 May 2026 20:00:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 26 May 2026 20:00:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 26 May 2026 20:00:27 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 20:00:27 GMT
ENV GN_VERSION=4.4.10
# Tue, 26 May 2026 20:00:27 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 26 May 2026 20:00:46 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 20:00:46 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 26 May 2026 20:00:46 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 20:00:46 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 20:00:46 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 20:00:46 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 20:00:46 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:ef1c26d09a5f9962879f732e212c4246a41e8473f6120efb435886357c85dd5a`  
		Last Modified: Fri, 10 Apr 2026 09:34:53 GMT  
		Size: 29.9 MB (29912147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5a3498cd625b1c7f2fe4f65685d4036d3cad9b92fdc3a7c30d047b0511431d`  
		Last Modified: Wed, 15 Apr 2026 20:44:43 GMT  
		Size: 17.6 MB (17579116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb83646d8cec7253c91045c8e0b103abc33d9faba0838653791cc13cfd2131d`  
		Last Modified: Wed, 29 Apr 2026 22:43:50 GMT  
		Size: 41.4 MB (41358769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d1ad21b5f4affc0bdf817bc13bc1b05c5e24c5728fc980722be40acf096d52`  
		Last Modified: Wed, 29 Apr 2026 22:43:49 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55a0630eea6b0c3f15ae53ad6c9f09b28ec02d6d14461bd65f1672e3066b8b8`  
		Last Modified: Wed, 29 Apr 2026 22:43:50 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef363bd4cee4e70ac0af7fd7af4b7e52eeba57c7a34b82803d8b38577887af9c`  
		Last Modified: Mon, 11 May 2026 23:52:52 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df865499b28393bd025d1ee75ad7d094381abf897ec9598f6926505a2beded93`  
		Last Modified: Mon, 11 May 2026 23:52:52 GMT  
		Size: 13.8 MB (13804833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74fe6edaae19a35d37b18d5121fa781cb38333b11d3dc82ea8cba63c14db5aa`  
		Last Modified: Mon, 11 May 2026 23:52:52 GMT  
		Size: 232.9 KB (232950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aea2f91b5b2d9900add721a42ab843517ae01adde6c3463235ab3e137725200`  
		Last Modified: Tue, 26 May 2026 20:01:48 GMT  
		Size: 843.8 KB (843799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1571be11b97395ab029de35d8b10c01eed74e123359af9b5d04290fd87d309`  
		Last Modified: Tue, 26 May 2026 20:01:54 GMT  
		Size: 311.7 MB (311742343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886e5a4b0db6f174fcde33323e4fac33c45cf45d2247ec34a062c37f0a0af2a9`  
		Last Modified: Tue, 26 May 2026 20:01:48 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e49d70370c8456159089603d94e0524719b9de002afe100cee3aaab89c88e5e`  
		Last Modified: Tue, 26 May 2026 20:01:48 GMT  
		Size: 3.0 KB (3013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c01440357dabb831ad91c416559f54c00951ff6e2088f72b26246ca053e65ae`  
		Last Modified: Tue, 26 May 2026 20:01:49 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4.10` - unknown; unknown

```console
$ docker pull geonetwork@sha256:4c6791c4a2fb4f87bd89cf0514da8f74b41734151b1784c74dd913baf768603f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4221193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84ef0d33fb600070830a943fc3f30191ef63f78212ffacd313669917141df84`

```dockerfile
```

-	Layers:
	-	`sha256:b95bfa55a71f73c618ff7074b52701aa296b286e4f8cf72c67836f0bc2e2b37d`  
		Last Modified: Tue, 26 May 2026 20:01:48 GMT  
		Size: 4.2 MB (4195763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d3b55ef5c7d3537471dbce478b79dcc2fd257b48859a212457a4fecd438ef79`  
		Last Modified: Tue, 26 May 2026 20:01:48 GMT  
		Size: 25.4 KB (25430 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:latest`

```console
$ docker pull geonetwork@sha256:1c1bb0e4bc2c32b181602971a6760636e3e5659afe2b296818456cac0f620686
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `geonetwork:latest` - linux; amd64

```console
$ docker pull geonetwork@sha256:091af31e85652383cba9f4069a718b61b48d928a87e46f59844abcbf701e7867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.6 MB (420631421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97663e8ce8f8d9e4597905e2e90ad25341bf99d0913b271d80e514d0b39775fe`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 29 Apr 2026 22:45:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:45:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:45:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:45:18 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Apr 2026 22:45:18 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:45:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:45:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:45:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:45:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 11 May 2026 23:28:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 11 May 2026 23:28:32 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:28:32 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 11 May 2026 23:28:32 GMT
WORKDIR /usr/local/tomcat
# Mon, 11 May 2026 23:28:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:28:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:28:32 GMT
ENV TOMCAT_MAJOR=9
# Mon, 11 May 2026 23:28:32 GMT
ENV TOMCAT_VERSION=9.0.118
# Mon, 11 May 2026 23:28:32 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Mon, 11 May 2026 23:28:32 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 11 May 2026 23:28:36 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:28:36 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 11 May 2026 23:28:36 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 11 May 2026 23:28:36 GMT
ENTRYPOINT []
# Mon, 11 May 2026 23:28:36 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:18:58 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 19:18:58 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 26 May 2026 19:18:58 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 26 May 2026 19:18:58 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 26 May 2026 19:18:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 26 May 2026 19:18:58 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 19:18:58 GMT
ENV GN_VERSION=4.4.10
# Tue, 26 May 2026 19:18:58 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 26 May 2026 19:19:24 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 19:19:24 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 26 May 2026 19:19:24 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 19:19:24 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 19:19:24 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 19:19:24 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:19:24 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf23ab6a8436ea4cc30c42c9eced3d7a9a42b066275648f8f1fbb0208b18c8fc`  
		Last Modified: Wed, 29 Apr 2026 22:45:34 GMT  
		Size: 17.0 MB (16983441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a14539c3f6df146437a21e07161e034b17f23dbe26ca23f9476c502b4c11df`  
		Last Modified: Wed, 29 Apr 2026 22:45:35 GMT  
		Size: 47.3 MB (47344091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288fd19c92924e5275f173c7e37ab77f791d263774ab4012d94aea4a7e017433`  
		Last Modified: Wed, 29 Apr 2026 22:45:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50069af557289dad3f81803ec84242ee38d92cc0440cca83f780e8ba4d498e4f`  
		Last Modified: Wed, 29 Apr 2026 22:45:33 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7ca595c1cdc53dff58e2b3a6153107fc81a7268f73191a74be7e474e14ed59`  
		Last Modified: Mon, 11 May 2026 23:28:44 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06493eda4e9a7d2b23bf3e6636af3dacc96c09641e54154aa1946effb90c6486`  
		Last Modified: Mon, 11 May 2026 23:28:45 GMT  
		Size: 13.8 MB (13796197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac16f181866752eb755aa0be0d49e0fe46f5415546b23a6f482aa911fb62975b`  
		Last Modified: Mon, 11 May 2026 23:28:44 GMT  
		Size: 224.7 KB (224711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301652bb5925b1827b165b5ab4b526f115ffcad9a18ed4c498248e1755b3918d`  
		Last Modified: Tue, 26 May 2026 19:19:46 GMT  
		Size: 801.2 KB (801153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580faf8d93c7ad4fe54e0ec31866eac5bdc1d7e623801f5f9fcea16079322838`  
		Last Modified: Tue, 26 May 2026 19:19:55 GMT  
		Size: 311.7 MB (311742287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65305e31e8a7d274d5b7e4aaaa51a87fd1498f829c54093d35e445ff8432921`  
		Last Modified: Tue, 26 May 2026 19:19:46 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78547240fa108460cca624821bdd9bdaa40632e77c3fe9f0183748660167ccc`  
		Last Modified: Tue, 26 May 2026 19:19:46 GMT  
		Size: 3.0 KB (3011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb9962a2ec25c6c14736c7c6bab123c904c35de138290510354b31b9690b017`  
		Last Modified: Tue, 26 May 2026 19:19:47 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:latest` - unknown; unknown

```console
$ docker pull geonetwork@sha256:3500ea7c70984ba06a2209b87ef42a131983e9d2aab874dffeca07534346eedd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4218988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b0d9bf6f1cd55e1fee3b5172d5253154a0c9d87600f18eb3df04fac8031b2ea`

```dockerfile
```

-	Layers:
	-	`sha256:0aa54fecf16260834bc09fe1d7beb85e6184c1982119163848018902641d4190`  
		Last Modified: Tue, 26 May 2026 19:19:46 GMT  
		Size: 4.2 MB (4193558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4b9e3ae3f53beaacd9e2c7e102d2ba0eb7ec37661ca6ec2b3252b2ec29be58a`  
		Last Modified: Tue, 26 May 2026 19:19:46 GMT  
		Size: 25.4 KB (25430 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:latest` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:078815e148dbfc72f5ef0f2d9a49b7046d0257250ed9c9f07f77e21fddc40a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.0 MB (415010904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9973dcb48dc41326f20fc607a2bf8b7095b78c2ef6196bf851cefc30506a50d`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:30 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:30 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:33 GMT
ADD file:341ecc672c4413d50e9543a8a38e44f8686dbdcc696b241b06e6b5b3a3ad57f6 in / 
# Fri, 10 Apr 2026 06:56:33 GMT
CMD ["/bin/bash"]
# Wed, 29 Apr 2026 22:45:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:45:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:45:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:45:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Apr 2026 22:45:50 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:45:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:45:54 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:45:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:45:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 11 May 2026 23:32:02 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 11 May 2026 23:32:02 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:32:02 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 11 May 2026 23:32:02 GMT
WORKDIR /usr/local/tomcat
# Mon, 11 May 2026 23:32:02 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:32:02 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:32:02 GMT
ENV TOMCAT_MAJOR=9
# Mon, 11 May 2026 23:32:02 GMT
ENV TOMCAT_VERSION=9.0.118
# Mon, 11 May 2026 23:32:02 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Mon, 11 May 2026 23:32:02 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 11 May 2026 23:32:08 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:32:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 11 May 2026 23:32:09 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 11 May 2026 23:32:09 GMT
ENTRYPOINT []
# Mon, 11 May 2026 23:32:09 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:22:49 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 19:22:49 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 26 May 2026 19:22:49 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 26 May 2026 19:22:49 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 26 May 2026 19:22:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 26 May 2026 19:22:49 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 19:22:49 GMT
ENV GN_VERSION=4.4.10
# Tue, 26 May 2026 19:22:49 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 26 May 2026 19:23:44 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 19:23:44 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 26 May 2026 19:23:44 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 19:23:44 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 19:23:44 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 19:23:44 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:23:44 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:03a6f28563c3f1bd861a0bd521bea32abc15b3b1362797f0ee963f0cfbe31325`  
		Last Modified: Fri, 10 Apr 2026 09:34:31 GMT  
		Size: 26.9 MB (26859689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3dcebaf2b2fcd539a30bc10bd91bbc7ef20caf11f1c358662e4ed783f9f102`  
		Last Modified: Wed, 29 Apr 2026 22:46:06 GMT  
		Size: 16.3 MB (16309684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f053e6426c790097075d4ca7bfd3ab90c6a6e96cdbbccf290cdb2a94445589`  
		Last Modified: Wed, 29 Apr 2026 22:46:07 GMT  
		Size: 45.5 MB (45452102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea68a1289a7d5d8edf9eded1c36c22635133ba55845322243cb20a0b0cdcdfd`  
		Last Modified: Wed, 29 Apr 2026 22:46:05 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34376f25195e52a2212871c8527277aa3bcd48be13afd35392696de749a7a56`  
		Last Modified: Wed, 29 Apr 2026 22:46:05 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9812430188f562534646d2616ab7a65aef552bef4d7fd50d0e646c38d49dc06d`  
		Last Modified: Mon, 11 May 2026 23:32:17 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5afef3c660b5106444ad7cd8e6b3e51ab20027742bb52a87a417e02564ecae`  
		Last Modified: Mon, 11 May 2026 23:32:18 GMT  
		Size: 13.7 MB (13730071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd5af756627697b9d0312dbc503baac6d124035a1ea54aded41bc3a7589a911`  
		Last Modified: Mon, 11 May 2026 23:32:17 GMT  
		Size: 196.5 KB (196474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df79545c33f0948e9238aeab008fdd4e07fa85179907a8e2aa7f4b25c805d40b`  
		Last Modified: Tue, 26 May 2026 19:24:08 GMT  
		Size: 714.0 KB (714029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cd9539d0d70e20b02dc1518f9f953d8d819677c19f89db82675cd65ce657f2`  
		Last Modified: Tue, 26 May 2026 19:24:14 GMT  
		Size: 311.7 MB (311742286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e394ae6b2e407c562fbe0e21dd720578e26f7d2cff2055a5dac4bcde2d7a681`  
		Last Modified: Tue, 26 May 2026 19:24:08 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03763171bafc34b7dc363c05ccc5209710063fdbefbdb05fd102d21b3137f298`  
		Last Modified: Tue, 26 May 2026 19:24:08 GMT  
		Size: 3.0 KB (3013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b60e92c376f95b932802a553ffa89296a702df5a94746caf99c8fc4ca9ef556`  
		Last Modified: Tue, 26 May 2026 19:24:09 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:latest` - unknown; unknown

```console
$ docker pull geonetwork@sha256:f2f23a094e649ef271989597d3e1f365ce133cf849ec19eae366afcafe5255ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4222684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f040fd7f77614559a95cc3d01b878885e05b17195674b5ae76c5d6cb3853f05`

```dockerfile
```

-	Layers:
	-	`sha256:dd940f32ec01e09e6f7ff39f8d4618e0bd460de603d3aa769fa37296b1ed3bf7`  
		Last Modified: Tue, 26 May 2026 19:24:08 GMT  
		Size: 4.2 MB (4197161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbe94d55c25c0cd7b8b730338a6123f8d64c2808749991e6941171e807d7edd9`  
		Last Modified: Tue, 26 May 2026 19:24:08 GMT  
		Size: 25.5 KB (25523 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:latest` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:b892c23b10e16891b1f3ebb00d9df9bdacca8ec34c8e187aa5ae6144a5342c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.1 MB (418108296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65f865a438974b29477b13b9b7acf8047b2c5e3414b4a04b835b71c655ebf42`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 29 Apr 2026 22:45:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:45:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:45:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:45:43 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Apr 2026 22:45:43 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:45:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:45:46 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:45:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:45:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 11 May 2026 23:27:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 11 May 2026 23:27:54 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:27:54 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 11 May 2026 23:27:54 GMT
WORKDIR /usr/local/tomcat
# Mon, 11 May 2026 23:27:54 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:27:54 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:27:54 GMT
ENV TOMCAT_MAJOR=9
# Mon, 11 May 2026 23:27:54 GMT
ENV TOMCAT_VERSION=9.0.118
# Mon, 11 May 2026 23:27:54 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Mon, 11 May 2026 23:27:54 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 11 May 2026 23:28:01 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:28:02 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 11 May 2026 23:28:02 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 11 May 2026 23:28:02 GMT
ENTRYPOINT []
# Mon, 11 May 2026 23:28:02 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:19:08 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 19:19:08 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 26 May 2026 19:19:08 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 26 May 2026 19:19:08 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 26 May 2026 19:19:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 26 May 2026 19:19:08 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 19:19:08 GMT
ENV GN_VERSION=4.4.10
# Tue, 26 May 2026 19:19:08 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 26 May 2026 19:20:20 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 19:20:20 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 26 May 2026 19:20:20 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 19:20:20 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 19:20:20 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 19:20:20 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 19:20:20 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340297f35e2c376c99270f2485ce4edd3c92de46a0bbef95a9bce7a944b35238`  
		Last Modified: Wed, 29 Apr 2026 22:45:59 GMT  
		Size: 17.0 MB (16996253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a8f9d2e0cdee350d3ed81afb01002bf9e394770886cecaed65f94e9470854`  
		Last Modified: Wed, 29 Apr 2026 22:46:00 GMT  
		Size: 45.7 MB (45660771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8b082d384d013a651b9a297183b301e82f6a59914d0873722ee08ae517b26e`  
		Last Modified: Wed, 29 Apr 2026 22:45:58 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08b5a1d9756317e6e8d13806e18cd14d78e5909594672612e96f2e3669b4f15`  
		Last Modified: Wed, 29 Apr 2026 22:45:58 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccb01e6b7b0d3a577dc45fc8232d7b6818325ffd7c939319446fd423064d38c`  
		Last Modified: Mon, 11 May 2026 23:28:11 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56c6f243e717ed8ba18b3c43492501aa31eb08d7c0df5075474090ed42d5d25`  
		Last Modified: Mon, 11 May 2026 23:28:11 GMT  
		Size: 13.8 MB (13805554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da79f66c4b83e2df5f98493f6db136efc253662ed6bc3b524de0003aaadcd61`  
		Last Modified: Mon, 11 May 2026 23:28:11 GMT  
		Size: 225.3 KB (225280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc0e8f9e38ddd9b7f35374c4e54287f9e77e32f49d9ee062b0d381934467ed5`  
		Last Modified: Tue, 26 May 2026 19:20:45 GMT  
		Size: 795.8 KB (795754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bde8402bddd9ebda751686e1c0caec51c340a6cbe8afe3c0c709704532e8f7e`  
		Last Modified: Tue, 26 May 2026 19:20:52 GMT  
		Size: 311.7 MB (311742326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59445f2b0af00976dca76cca13d75abc90c8755185a479a1cef6b3b0e56648c`  
		Last Modified: Tue, 26 May 2026 19:20:45 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff795d7978acc5515e1d3183acce6dc5ecf30ba249554f0329c769a5a9f10edf`  
		Last Modified: Tue, 26 May 2026 19:20:45 GMT  
		Size: 3.0 KB (3014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acd7f4b488604821d030d1151546d2721d1c968e01fe3f77b7ef85fa84f6252`  
		Last Modified: Tue, 26 May 2026 19:20:46 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:latest` - unknown; unknown

```console
$ docker pull geonetwork@sha256:02233406faf8b5d980db73662d831319c86dc7a8630d8f41b2cb5a14b56ae715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4220197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c691eeb4dc4eb0c780cad66e7c54f472f4bb685e5bcb8f6b44ce873b1c7b5c`

```dockerfile
```

-	Layers:
	-	`sha256:6625220a3d7971d6beed82f28f2797e32db30a4c4c6cb94cf87c52c4f1343454`  
		Last Modified: Tue, 26 May 2026 19:20:45 GMT  
		Size: 4.2 MB (4194648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9de6fce6dbd22d640264b16c99c9b4891344a3d1fadaa2dc3935f7eeca6cd3d6`  
		Last Modified: Tue, 26 May 2026 19:20:45 GMT  
		Size: 25.5 KB (25549 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:latest` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:065fbac665c5ccbd330eb99e634a931dda7a5f6c8654e613f247c00abaf0c3ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.7 MB (422738247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3532be992ebcedf7f8b743a45f584148c462a8ab96e1b968cbc74d747a5617f`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:12:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:12:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:12:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:12:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:12:34 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:45:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:45:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:45:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:45:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 01:22:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 01:22:58 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 01:22:58 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 01:22:58 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 01:22:58 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 01:22:58 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 01:22:58 GMT
ENV TOMCAT_MAJOR=9
# Tue, 12 May 2026 01:22:58 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 12 May 2026 01:22:58 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 12 May 2026 01:22:59 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 01:23:07 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 01:23:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 01:23:09 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 01:23:09 GMT
ENTRYPOINT []
# Tue, 12 May 2026 01:23:09 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 20:22:54 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 20:22:54 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 26 May 2026 20:22:54 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 26 May 2026 20:22:54 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 26 May 2026 20:22:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 26 May 2026 20:22:54 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 20:22:54 GMT
ENV GN_VERSION=4.4.10
# Tue, 26 May 2026 20:22:54 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 26 May 2026 20:23:13 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 20:23:14 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 26 May 2026 20:23:14 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 20:23:15 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 20:23:15 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 20:23:15 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 20:23:15 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13718497a6adee31aa098ce2c85aca5feeb60aa6f13ee0ac169b2a181311f2cd`  
		Last Modified: Wed, 15 Apr 2026 21:13:20 GMT  
		Size: 18.8 MB (18813307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777cb69b760c692aaca637d1f978ca71a27e8f712772ebee4f24d36075f9e119`  
		Last Modified: Wed, 29 Apr 2026 22:46:19 GMT  
		Size: 42.8 MB (42813437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7f006dbd4d35f9dc4139ef666a81408417cd773080cdf49bb5876a1228c7a0`  
		Last Modified: Wed, 29 Apr 2026 22:46:18 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62105aa809cab5140e7f62bdbab1c9624ce547772bb7b5e7b61d334457d61a3b`  
		Last Modified: Wed, 29 Apr 2026 22:46:18 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64ac7edd53aaec8649090cca5b03990f58f860ea148a5da89d274fb41c41609`  
		Last Modified: Tue, 12 May 2026 01:23:33 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3125d2db6abf2edbd83717983bb17c1b31afcfaa662341d3dd858d0a812e4f6`  
		Last Modified: Tue, 12 May 2026 01:23:33 GMT  
		Size: 13.8 MB (13831958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f12f88f8c1d63dbca0713f1ac021902a8ec4b59a5003b102e4f0dc3bdcdb67`  
		Last Modified: Tue, 12 May 2026 01:23:33 GMT  
		Size: 256.7 KB (256653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0837cc78d6d0d644b064b7d8664e3978efb5e9abb3360bd237b6dbb67bacfb0`  
		Last Modified: Tue, 26 May 2026 20:24:02 GMT  
		Size: 959.8 KB (959838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390e02e08f47bb475b2a002d2732c6fab3e0a7213c996b6b76ec098b8531b347`  
		Last Modified: Tue, 26 May 2026 20:24:09 GMT  
		Size: 311.7 MB (311742307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311d5798f7d276ef1904ae9961d12de257c80ac83afcf7920ac3bbc39c6e47f6`  
		Last Modified: Tue, 26 May 2026 20:24:02 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894173186f8c6225d36ea08a8379237ec9a3cc1b95dbff3b17e7d076a70068d9`  
		Last Modified: Tue, 26 May 2026 20:24:02 GMT  
		Size: 3.0 KB (3016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7beb0611be5018411ef263cfb2b79f931a40b221ba55629c055508565bedbb4d`  
		Last Modified: Tue, 26 May 2026 20:24:03 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:latest` - unknown; unknown

```console
$ docker pull geonetwork@sha256:706b4b5a7348d850ea13e80a6ad9dde29cc228708e6976584d7f1f64978ad4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4223112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3135bcb3a1755a7cd165f5843f0dfafd495327ae4161f2f7b7dcbf752eac8f75`

```dockerfile
```

-	Layers:
	-	`sha256:338eada16d2652193771bb358aeab313bdcbc4a8b56a987797f3f275ff190038`  
		Last Modified: Tue, 26 May 2026 20:24:02 GMT  
		Size: 4.2 MB (4197637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bae2cd05343a8d4a072e7b8f8407f9904236e48fb6ea27bb33a0a7732a791a1`  
		Last Modified: Tue, 26 May 2026 20:24:02 GMT  
		Size: 25.5 KB (25475 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:latest` - linux; s390x

```console
$ docker pull geonetwork@sha256:b7ea2a6440ebdc6e96b122291b8edce2b37d979511458c56dbe605bdd9a6fbab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.5 MB (415480524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2418672e41bacffd94b20e96aae257b1238fda21e72b7797a8d9038a2b68b2d`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 06:50:27 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:50:29 GMT
ADD file:41defd98c44eed6fc946fd94496a94164879f2ad4f63d66a5c1e213cc2259ad1 in / 
# Fri, 10 Apr 2026 06:50:29 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:44:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:44:12 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:43:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 Apr 2026 22:43:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:43:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:43:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 11 May 2026 23:52:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 11 May 2026 23:52:35 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:52:35 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 11 May 2026 23:52:35 GMT
WORKDIR /usr/local/tomcat
# Mon, 11 May 2026 23:52:35 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:52:35 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 11 May 2026 23:52:35 GMT
ENV TOMCAT_MAJOR=9
# Mon, 11 May 2026 23:52:35 GMT
ENV TOMCAT_VERSION=9.0.118
# Mon, 11 May 2026 23:52:35 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Mon, 11 May 2026 23:52:35 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 11 May 2026 23:52:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:52:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 11 May 2026 23:52:39 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 11 May 2026 23:52:39 GMT
ENTRYPOINT []
# Mon, 11 May 2026 23:52:39 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 20:00:27 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 26 May 2026 20:00:27 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 26 May 2026 20:00:27 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 26 May 2026 20:00:27 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 26 May 2026 20:00:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 26 May 2026 20:00:27 GMT
ENV GN_FILE=geonetwork.war
# Tue, 26 May 2026 20:00:27 GMT
ENV GN_VERSION=4.4.10
# Tue, 26 May 2026 20:00:27 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 26 May 2026 20:00:46 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 26 May 2026 20:00:46 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 26 May 2026 20:00:46 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 26 May 2026 20:00:46 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 26 May 2026 20:00:46 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 26 May 2026 20:00:46 GMT
CMD ["catalina.sh" "run"]
# Tue, 26 May 2026 20:00:46 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:ef1c26d09a5f9962879f732e212c4246a41e8473f6120efb435886357c85dd5a`  
		Last Modified: Fri, 10 Apr 2026 09:34:53 GMT  
		Size: 29.9 MB (29912147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5a3498cd625b1c7f2fe4f65685d4036d3cad9b92fdc3a7c30d047b0511431d`  
		Last Modified: Wed, 15 Apr 2026 20:44:43 GMT  
		Size: 17.6 MB (17579116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb83646d8cec7253c91045c8e0b103abc33d9faba0838653791cc13cfd2131d`  
		Last Modified: Wed, 29 Apr 2026 22:43:50 GMT  
		Size: 41.4 MB (41358769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d1ad21b5f4affc0bdf817bc13bc1b05c5e24c5728fc980722be40acf096d52`  
		Last Modified: Wed, 29 Apr 2026 22:43:49 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55a0630eea6b0c3f15ae53ad6c9f09b28ec02d6d14461bd65f1672e3066b8b8`  
		Last Modified: Wed, 29 Apr 2026 22:43:50 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef363bd4cee4e70ac0af7fd7af4b7e52eeba57c7a34b82803d8b38577887af9c`  
		Last Modified: Mon, 11 May 2026 23:52:52 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df865499b28393bd025d1ee75ad7d094381abf897ec9598f6926505a2beded93`  
		Last Modified: Mon, 11 May 2026 23:52:52 GMT  
		Size: 13.8 MB (13804833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74fe6edaae19a35d37b18d5121fa781cb38333b11d3dc82ea8cba63c14db5aa`  
		Last Modified: Mon, 11 May 2026 23:52:52 GMT  
		Size: 232.9 KB (232950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aea2f91b5b2d9900add721a42ab843517ae01adde6c3463235ab3e137725200`  
		Last Modified: Tue, 26 May 2026 20:01:48 GMT  
		Size: 843.8 KB (843799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1571be11b97395ab029de35d8b10c01eed74e123359af9b5d04290fd87d309`  
		Last Modified: Tue, 26 May 2026 20:01:54 GMT  
		Size: 311.7 MB (311742343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886e5a4b0db6f174fcde33323e4fac33c45cf45d2247ec34a062c37f0a0af2a9`  
		Last Modified: Tue, 26 May 2026 20:01:48 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e49d70370c8456159089603d94e0524719b9de002afe100cee3aaab89c88e5e`  
		Last Modified: Tue, 26 May 2026 20:01:48 GMT  
		Size: 3.0 KB (3013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c01440357dabb831ad91c416559f54c00951ff6e2088f72b26246ca053e65ae`  
		Last Modified: Tue, 26 May 2026 20:01:49 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:latest` - unknown; unknown

```console
$ docker pull geonetwork@sha256:4c6791c4a2fb4f87bd89cf0514da8f74b41734151b1784c74dd913baf768603f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4221193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84ef0d33fb600070830a943fc3f30191ef63f78212ffacd313669917141df84`

```dockerfile
```

-	Layers:
	-	`sha256:b95bfa55a71f73c618ff7074b52701aa296b286e4f8cf72c67836f0bc2e2b37d`  
		Last Modified: Tue, 26 May 2026 20:01:48 GMT  
		Size: 4.2 MB (4195763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d3b55ef5c7d3537471dbce478b79dcc2fd257b48859a212457a4fecd438ef79`  
		Last Modified: Tue, 26 May 2026 20:01:48 GMT  
		Size: 25.4 KB (25430 bytes)  
		MIME: application/vnd.in-toto+json
