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
$ docker pull geonetwork@sha256:cb26d353170e6b3eae87dda2b3c4b72250578132fa61b64902db528ba8197194
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
$ docker pull geonetwork@sha256:8a662a8e86f77c0eebc5ed196cb48f828b8234331cf022da7112f847705ba5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.5 MB (350505114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f1015be7de71de3d70cb23c18c4ffd63e5c1f114ce77c143504b49d54058dd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:13:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:13:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:13:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:13:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:13:59 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:14:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:14:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:14:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:14:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 09:20:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 09:20:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 09:20:15 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 09:20:15 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 09:20:15 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:20:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:20:15 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 09:20:15 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 09:20:15 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 09:20:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Jun 2026 09:20:38 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 09:20:38 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 09:20:38 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 09:20:38 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 10:18:46 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 10:18:46 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Jun 2026 10:18:46 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 10:18:46 GMT
ENV GN_VERSION=3.12.12
# Tue, 02 Jun 2026 10:18:46 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 02 Jun 2026 10:18:46 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Jun 2026 10:21:33 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Jun 2026 10:21:33 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:21:33 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:21:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 10:21:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d626348eec3a68143ac7cd0a6634adeccef97b9eb7a032bcc7d0cef5f8285d`  
		Last Modified: Tue, 02 Jun 2026 08:14:14 GMT  
		Size: 17.0 MB (16984251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5707a967e0439bbf45d99425ed29ad8d3becd9d15f8b5eaa332b3d5e9e4477b6`  
		Last Modified: Tue, 02 Jun 2026 08:14:15 GMT  
		Size: 55.2 MB (55200456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8992f58138a42d0304eba727e4c06c8e09e5343560ccd363242a2236eea1a9`  
		Last Modified: Tue, 02 Jun 2026 08:14:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6156d9eb6a345480d38c560b95e0a563acb7992de4c3ca5c87513811b3095b82`  
		Last Modified: Tue, 02 Jun 2026 08:14:14 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef8ad0895180f07049805cfdbee35b6c44fa7f7d11228ae4a46ccd082bdfb2d`  
		Last Modified: Tue, 02 Jun 2026 09:20:47 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122e8f0d3e6628291d3b43177a1830130f4eb0fa2230c8430b2d679cad18fc33`  
		Last Modified: Tue, 02 Jun 2026 09:20:47 GMT  
		Size: 14.0 MB (14034048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61db8eccffe64a18c8a87a2aaca01c884ee9bda5c27fc7cb01f5fe6296b08e5d`  
		Last Modified: Tue, 02 Jun 2026 10:21:59 GMT  
		Size: 234.6 MB (234550425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f048b1eb30b86bbdf2d290866de06934abf78713326ac99c123e4d02d9e2e70`  
		Last Modified: Tue, 02 Jun 2026 10:21:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:350ee2d8fc1b0b9ed379d6354b5dee7bfa432d7d6432df21a634ac8a4e7141ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4379511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46f8121372b4265fdbb93cf59b096d5fdf343bd0d375c1c3db4e1ab633cbb677`

```dockerfile
```

-	Layers:
	-	`sha256:41ee1bd80c8227bf07dc3bf4d7310e99f925d72043389590ec7fcd5309d9baa3`  
		Last Modified: Tue, 02 Jun 2026 10:21:53 GMT  
		Size: 4.4 MB (4360418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caa4ce7ba21b20ec4aedd8b3bb086e8586a2339fbf5e26fbe5155a08a01f74ec`  
		Last Modified: Tue, 02 Jun 2026 10:21:53 GMT  
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
$ docker pull geonetwork@sha256:eeb37ae30637fe0c95d6b72ec259cd856cb0bd6e8a65b9473bbe3d268f23c13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.8 MB (348751933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3030c62ad0ec0874c0bf59237136c289ddc48a513c52f8b0e6de5d323580466f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:15:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:15:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:15:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:15:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:15:24 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:15:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:15:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:15:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:15:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 09:29:22 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 09:29:22 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 09:29:22 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 09:29:22 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 09:29:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:29:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:29:22 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 09:29:22 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 09:29:22 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 09:29:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Jun 2026 09:29:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 09:29:49 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 09:29:49 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 09:29:49 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 10:15:36 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 10:15:36 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Jun 2026 10:15:36 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 10:15:36 GMT
ENV GN_VERSION=3.12.12
# Tue, 02 Jun 2026 10:15:36 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 02 Jun 2026 10:15:36 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Jun 2026 10:18:00 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Jun 2026 10:18:00 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:18:00 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:18:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 10:18:00 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab110e6d63137368eeacacd99b16eb78cfc6271be04d9600931c38644c992261`  
		Last Modified: Tue, 02 Jun 2026 08:15:40 GMT  
		Size: 17.0 MB (16997536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcefc1210a461c08953484fddcf25ec0fd5eecedd8609238356a152f3cad5d8`  
		Last Modified: Tue, 02 Jun 2026 08:15:41 GMT  
		Size: 54.3 MB (54277497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8924b2c1ef32e60b93ebd7f7ad1ab5ce46508e22d42097f7206c4ff58fb8ec95`  
		Last Modified: Tue, 02 Jun 2026 08:15:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3478717f2d1fd7b23ae3c0c5ee7e0478b158105010b3f1434e65ad459082ed`  
		Last Modified: Tue, 02 Jun 2026 08:15:39 GMT  
		Size: 2.5 KB (2484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d378e08ee54cb1c196aa65eb7c72e988ce6f7c57af5b04ee650d6f79cd04bb`  
		Last Modified: Tue, 02 Jun 2026 09:29:58 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b49df80cdfc0bdc5b2045768e8872ce1fc65b1efc752e0829fa8197df004f49`  
		Last Modified: Tue, 02 Jun 2026 09:29:59 GMT  
		Size: 14.0 MB (14042962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814029ba2327b904586a76040b03d18dc003ef4253feb1729049c3eadb5b237`  
		Last Modified: Tue, 02 Jun 2026 10:18:26 GMT  
		Size: 234.6 MB (234554405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa21e2f55c2d4a0c872c9e592e184a563668547601d42dd06bee3d5c2d34126`  
		Last Modified: Tue, 02 Jun 2026 10:18:21 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:618b32286975c8407424e1e1d7216cbac1e3403115f6f9fb7c72de1938e48ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b972747f50a26c83441ef6b796ea3f2a239ad65b2984dac1e7d4ae95f20e65a`

```dockerfile
```

-	Layers:
	-	`sha256:560c74eb9ca8ffaf07f1b69045192e21b37d023d7674a86876b16054427e1023`  
		Last Modified: Tue, 02 Jun 2026 10:18:21 GMT  
		Size: 4.4 MB (4361574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88ac7e70cb30158d8aadd5b6524c1cf384d03be7f7cb5237ebeee49460c58397`  
		Last Modified: Tue, 02 Jun 2026 10:18:21 GMT  
		Size: 19.2 KB (19185 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:1723e1cf65285704dbaed451779b0e9abf9b5e97a46f5ae045a7a1ee82d28545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.6 MB (354626549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24177fa31883ea1516321248e9696b70816fa062bd565165b7f60810497e05a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:10:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:10:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:10:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:10:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:10:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:10:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:10:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:26:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:26:34 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:26:34 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:26:34 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:26:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:26:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:26:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:26:34 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:26:34 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:27:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Jun 2026 10:27:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:27:53 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:27:53 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:27:53 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 12:13:47 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 12:13:47 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Jun 2026 12:13:47 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 12:13:47 GMT
ENV GN_VERSION=3.12.12
# Tue, 02 Jun 2026 12:13:47 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 02 Jun 2026 12:13:47 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Jun 2026 12:15:26 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Jun 2026 12:15:26 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 12:15:26 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 12:15:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 12:15:26 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef700e09ef3cf16d19218622a73899db0a8b42f33bfb19159bb4aa3576d5d21e`  
		Last Modified: Tue, 02 Jun 2026 08:10:42 GMT  
		Size: 18.8 MB (18813426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55d72b407fef39fa8814e430e4e2abf5a1cb6bb489417114169923011d31013`  
		Last Modified: Tue, 02 Jun 2026 08:10:44 GMT  
		Size: 52.7 MB (52670407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c627c23154e2a083d18c82d27d0653b1fbc6634ebb7f9fa305fbf926ed54fc`  
		Last Modified: Tue, 02 Jun 2026 08:10:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9936e589c30a5062ee9c1e1bcb1c1199b9777ac2ee1014f8649ddacc2163ce59`  
		Last Modified: Tue, 02 Jun 2026 08:10:41 GMT  
		Size: 2.5 KB (2484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d14c780d90f0cb147556d42aaff3742ee51c206f030b920374b79369c86eaed`  
		Last Modified: Tue, 02 Jun 2026 10:28:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90239c53cae997be1c44516f7a186ce795513affca342e8d08b18bdf335c4f94`  
		Last Modified: Tue, 02 Jun 2026 10:28:13 GMT  
		Size: 14.3 MB (14250688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99965b57ef70f8c05fb29fc31333abb28609abb5fba4096b2485688b9dfa3f9`  
		Last Modified: Tue, 02 Jun 2026 12:16:13 GMT  
		Size: 234.6 MB (234574800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28b6ef4fa678d84405bef337a68b597faedfa6a6dc78d6399a94226225e9e3a`  
		Last Modified: Tue, 02 Jun 2026 12:16:06 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:e560585afc926d2db24b8edfe025ef9b8447d66ecf6bed78d58a950394abf79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4382296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85dfd67c75083cdad844ae49e7c4b0c1de1a9eccc2a51b6c0b5efcc50a1acc4`

```dockerfile
```

-	Layers:
	-	`sha256:4388928b7ca786c3e332873e258211c0b3a7767da7718d85d6334ecb3f384bd1`  
		Last Modified: Tue, 02 Jun 2026 12:16:06 GMT  
		Size: 4.4 MB (4363165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8ff5a5dacb77c3e5f0a6e7b00433c4d1674ef5c50412a74ddefc54a3429fc31`  
		Last Modified: Tue, 02 Jun 2026 12:16:06 GMT  
		Size: 19.1 KB (19131 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3-postgres`

```console
$ docker pull geonetwork@sha256:7e643d08d39fa5afef38734747f9cc2e0210267a3b2c030df7f5a55ac2e83d7c
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
$ docker pull geonetwork@sha256:fa991a7af8407399d8018eced766e757bdf06b44fe606df6617a83e290eab222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.5 MB (364453401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cadac27da1a99e938d092d585c395fce16badbe50df90a28bcc355b546425cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:13:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:13:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:13:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:13:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:13:59 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:14:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:14:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:14:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:14:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 09:20:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 09:20:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 09:20:15 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 09:20:15 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 09:20:15 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:20:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:20:15 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 09:20:15 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 09:20:15 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 09:20:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Jun 2026 09:20:38 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 09:20:38 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 09:20:38 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 09:20:38 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 10:18:46 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 10:18:46 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Jun 2026 10:18:46 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 10:18:46 GMT
ENV GN_VERSION=3.12.12
# Tue, 02 Jun 2026 10:18:46 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 02 Jun 2026 10:18:46 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Jun 2026 10:21:33 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Jun 2026 10:21:33 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:21:33 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:21:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 10:21:33 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:12:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 11:12:38 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 02 Jun 2026 11:12:38 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 02 Jun 2026 11:12:38 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:12:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 11:12:38 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d626348eec3a68143ac7cd0a6634adeccef97b9eb7a032bcc7d0cef5f8285d`  
		Last Modified: Tue, 02 Jun 2026 08:14:14 GMT  
		Size: 17.0 MB (16984251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5707a967e0439bbf45d99425ed29ad8d3becd9d15f8b5eaa332b3d5e9e4477b6`  
		Last Modified: Tue, 02 Jun 2026 08:14:15 GMT  
		Size: 55.2 MB (55200456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8992f58138a42d0304eba727e4c06c8e09e5343560ccd363242a2236eea1a9`  
		Last Modified: Tue, 02 Jun 2026 08:14:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6156d9eb6a345480d38c560b95e0a563acb7992de4c3ca5c87513811b3095b82`  
		Last Modified: Tue, 02 Jun 2026 08:14:14 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef8ad0895180f07049805cfdbee35b6c44fa7f7d11228ae4a46ccd082bdfb2d`  
		Last Modified: Tue, 02 Jun 2026 09:20:47 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122e8f0d3e6628291d3b43177a1830130f4eb0fa2230c8430b2d679cad18fc33`  
		Last Modified: Tue, 02 Jun 2026 09:20:47 GMT  
		Size: 14.0 MB (14034048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61db8eccffe64a18c8a87a2aaca01c884ee9bda5c27fc7cb01f5fe6296b08e5d`  
		Last Modified: Tue, 02 Jun 2026 10:21:59 GMT  
		Size: 234.6 MB (234550425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f048b1eb30b86bbdf2d290866de06934abf78713326ac99c123e4d02d9e2e70`  
		Last Modified: Tue, 02 Jun 2026 10:21:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41aa9a2eacab96d28e6c7a8bfb96f13d77c089881abac4963ca846055ecde12`  
		Last Modified: Tue, 02 Jun 2026 11:12:54 GMT  
		Size: 13.9 MB (13944877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef71ba2ccc05bcc6ebf92c4a55c31a74abe4e4f15dafd28c03b726389fccd103`  
		Last Modified: Tue, 02 Jun 2026 11:12:54 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4dcb6e7935d0d69ac6b99d5aa3ef227e96188ebd3708bfa1ce039d999d277e7`  
		Last Modified: Tue, 02 Jun 2026 11:12:54 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a933f5b3cfbc7972552f6ba893cb061818c2165c5650ed0a26d331d51a475517`  
		Last Modified: Tue, 02 Jun 2026 11:12:54 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:085b320fefd84664d4b561cb6c90cfb77e0accc6a1774fb82b5f90eb77335bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5937887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dbe3b4fbd01408e145641f5da498c1db27a2f02dd181a73cb8236bc61e29b9`

```dockerfile
```

-	Layers:
	-	`sha256:551208eacb9cca92f10cbde3a3561db45a1f6d24df0995f98aed00025b563e45`  
		Last Modified: Tue, 02 Jun 2026 11:12:54 GMT  
		Size: 5.9 MB (5915069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfe63011f74aeb8d861246242f0034ded8ca83c563af35b83b961d243b8aa9e1`  
		Last Modified: Tue, 02 Jun 2026 11:12:53 GMT  
		Size: 22.8 KB (22818 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:fb3eaa4858f89d32974c11193e2e1cbec63edf03522acb507af84563025bc133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.2 MB (355214752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0778a9a784b38a1885676c4de52842cfcafeb29fd0f9f0085035b6bb8540257b`
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
# Tue, 02 Jun 2026 11:58:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 11:58:55 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 02 Jun 2026 11:58:55 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 02 Jun 2026 11:58:55 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:58:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 11:58:55 GMT
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
	-	`sha256:f0a6b7154bb6d508e62db3307ac2a9635cf9a6b5f1cc354abc229e8459176ba5`  
		Last Modified: Tue, 02 Jun 2026 11:59:11 GMT  
		Size: 13.0 MB (13019661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0383e0b9b2e14e1c014e3fc291693f1aa390b6aeeb8f5225c57fb1f116b4b3`  
		Last Modified: Tue, 02 Jun 2026 11:59:10 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ac43eb524602d7e60322f549844d3a1255d38dc847eef001f81eb171c32198`  
		Last Modified: Tue, 02 Jun 2026 11:59:10 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535c2c378579e3ee4e6b5ee423a4499b7ff4563b49f733a32f0f9ec4cc0a8995`  
		Last Modified: Tue, 02 Jun 2026 11:59:10 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:0a00b119e3df006bb64aad56a0c6cdd77f52deeb7522f32e54e980847c909a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5940692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5f4e96045ca6c118f4da8896ff99cabda34520f556c41440c3517dea0b2565`

```dockerfile
```

-	Layers:
	-	`sha256:55f619a4ade54433985193bf3b7483a53ccb7c9e02b3014e3ee277285d059121`  
		Last Modified: Tue, 02 Jun 2026 11:59:10 GMT  
		Size: 5.9 MB (5917788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed88097d79378d899390a0c096470715000d57dd48d4776c9d5dd721aa2ba03a`  
		Last Modified: Tue, 02 Jun 2026 11:59:10 GMT  
		Size: 22.9 KB (22904 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:a0442cf02c7f2571a3c96837a74ae95259795ab702df01c9a66e2a86776ba231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.7 MB (362675228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a7f8b0b01fae5df0cbf41fe78f68d15a16c3ccbdca700ab62cb771324297a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:15:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:15:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:15:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:15:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:15:24 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:15:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:15:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:15:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:15:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 09:29:22 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 09:29:22 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 09:29:22 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 09:29:22 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 09:29:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:29:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:29:22 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 09:29:22 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 09:29:22 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 09:29:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Jun 2026 09:29:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 09:29:49 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 09:29:49 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 09:29:49 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 10:15:36 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 10:15:36 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Jun 2026 10:15:36 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 10:15:36 GMT
ENV GN_VERSION=3.12.12
# Tue, 02 Jun 2026 10:15:36 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 02 Jun 2026 10:15:36 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Jun 2026 10:18:00 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Jun 2026 10:18:00 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:18:00 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:18:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 10:18:00 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:12:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 11:12:40 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 02 Jun 2026 11:12:40 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 02 Jun 2026 11:12:40 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:12:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 11:12:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab110e6d63137368eeacacd99b16eb78cfc6271be04d9600931c38644c992261`  
		Last Modified: Tue, 02 Jun 2026 08:15:40 GMT  
		Size: 17.0 MB (16997536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcefc1210a461c08953484fddcf25ec0fd5eecedd8609238356a152f3cad5d8`  
		Last Modified: Tue, 02 Jun 2026 08:15:41 GMT  
		Size: 54.3 MB (54277497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8924b2c1ef32e60b93ebd7f7ad1ab5ce46508e22d42097f7206c4ff58fb8ec95`  
		Last Modified: Tue, 02 Jun 2026 08:15:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3478717f2d1fd7b23ae3c0c5ee7e0478b158105010b3f1434e65ad459082ed`  
		Last Modified: Tue, 02 Jun 2026 08:15:39 GMT  
		Size: 2.5 KB (2484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d378e08ee54cb1c196aa65eb7c72e988ce6f7c57af5b04ee650d6f79cd04bb`  
		Last Modified: Tue, 02 Jun 2026 09:29:58 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b49df80cdfc0bdc5b2045768e8872ce1fc65b1efc752e0829fa8197df004f49`  
		Last Modified: Tue, 02 Jun 2026 09:29:59 GMT  
		Size: 14.0 MB (14042962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814029ba2327b904586a76040b03d18dc003ef4253feb1729049c3eadb5b237`  
		Last Modified: Tue, 02 Jun 2026 10:18:26 GMT  
		Size: 234.6 MB (234554405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa21e2f55c2d4a0c872c9e592e184a563668547601d42dd06bee3d5c2d34126`  
		Last Modified: Tue, 02 Jun 2026 10:18:21 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd7fa112850548b52ea4a5118ec9a2382e5b84e83370040067513ca7997293c`  
		Last Modified: Tue, 02 Jun 2026 11:12:56 GMT  
		Size: 13.9 MB (13919884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1db82b48fb4ce8aee0c62f7096a5959798cff7154e0f84a95d99e8f184203ce`  
		Last Modified: Tue, 02 Jun 2026 11:12:55 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0e75213f1a6a9cc7384258accba6786302e1c2193954d01375242b97096ac9`  
		Last Modified: Tue, 02 Jun 2026 11:12:55 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f11dacd96937679d1c1f429f6df904c73188ef92b3be9ab225ce9708a1ed668`  
		Last Modified: Tue, 02 Jun 2026 11:12:55 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:b99375b44548ef5869f54a8f9a873b0fa7c177a5f493cab9f7d9e79bee2c973c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5945203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e4dd5d6fd2c92f8dd5a2d9faa87512847f590691fae8a6a592804043337399`

```dockerfile
```

-	Layers:
	-	`sha256:6ed73ab7898a696b8a97a8cdaae42fb54ac1a888fb91c2171604269eed5540ed`  
		Last Modified: Tue, 02 Jun 2026 11:12:55 GMT  
		Size: 5.9 MB (5922277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94762734f42c3f0a62554b5696a90f2cf3d352cb14f53759076f68dc5f302593`  
		Last Modified: Tue, 02 Jun 2026 11:12:55 GMT  
		Size: 22.9 KB (22926 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:b1ef708a99b31a0753019c7875c19ba457ef35288e85d1b1965c4ad64953e0cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.1 MB (369070549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbac3869df5481f4999c3f52ce49e6fc387e6934a537e6d5d49e5a8347a836b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:10:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:10:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:10:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:10:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:10:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:10:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:10:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:26:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:26:34 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:26:34 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:26:34 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:26:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:26:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:26:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:26:34 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:26:34 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:27:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Jun 2026 10:27:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:27:53 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:27:53 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:27:53 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 12:13:47 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 12:13:47 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Jun 2026 12:13:47 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 12:13:47 GMT
ENV GN_VERSION=3.12.12
# Tue, 02 Jun 2026 12:13:47 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 02 Jun 2026 12:13:47 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Jun 2026 12:15:26 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Jun 2026 12:15:26 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 12:15:26 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 12:15:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 12:15:26 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 13:09:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 13:09:09 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 02 Jun 2026 13:09:09 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 02 Jun 2026 13:09:09 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 13:09:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 13:09:09 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef700e09ef3cf16d19218622a73899db0a8b42f33bfb19159bb4aa3576d5d21e`  
		Last Modified: Tue, 02 Jun 2026 08:10:42 GMT  
		Size: 18.8 MB (18813426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55d72b407fef39fa8814e430e4e2abf5a1cb6bb489417114169923011d31013`  
		Last Modified: Tue, 02 Jun 2026 08:10:44 GMT  
		Size: 52.7 MB (52670407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c627c23154e2a083d18c82d27d0653b1fbc6634ebb7f9fa305fbf926ed54fc`  
		Last Modified: Tue, 02 Jun 2026 08:10:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9936e589c30a5062ee9c1e1bcb1c1199b9777ac2ee1014f8649ddacc2163ce59`  
		Last Modified: Tue, 02 Jun 2026 08:10:41 GMT  
		Size: 2.5 KB (2484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d14c780d90f0cb147556d42aaff3742ee51c206f030b920374b79369c86eaed`  
		Last Modified: Tue, 02 Jun 2026 10:28:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90239c53cae997be1c44516f7a186ce795513affca342e8d08b18bdf335c4f94`  
		Last Modified: Tue, 02 Jun 2026 10:28:13 GMT  
		Size: 14.3 MB (14250688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99965b57ef70f8c05fb29fc31333abb28609abb5fba4096b2485688b9dfa3f9`  
		Last Modified: Tue, 02 Jun 2026 12:16:13 GMT  
		Size: 234.6 MB (234574800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28b6ef4fa678d84405bef337a68b597faedfa6a6dc78d6399a94226225e9e3a`  
		Last Modified: Tue, 02 Jun 2026 12:16:06 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82611a6196ed1d26821f84420d83aab48632b7fd682537ef4c51fc303ba46714`  
		Last Modified: Tue, 02 Jun 2026 13:09:39 GMT  
		Size: 14.4 MB (14440582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d888d4e9378ba16ffd5099330a63909f5f924e4d63798d74a8856d2e718b4b33`  
		Last Modified: Tue, 02 Jun 2026 13:09:39 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458b7518f5485eca0d690367e0a30691f9a0538e10a8117d0086010dd369a133`  
		Last Modified: Tue, 02 Jun 2026 13:09:39 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f9fc3d833ec36a3efb726142fe4316bceb038525a3ee2aae7157560799edd4`  
		Last Modified: Tue, 02 Jun 2026 13:09:39 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:279d5fde08c2ca72df74b19c73ada44d1ce1e37ef81ed74966f3cb9f34715fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5943424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8df88ca7729cd1cc60feb84b1b4d2814ea53f71d8a8f1d70070610963c625cd`

```dockerfile
```

-	Layers:
	-	`sha256:63ecf9fbe5a372905b0d81d252a29c50ea339cbd0d1b2177e1c15aa432029d66`  
		Last Modified: Tue, 02 Jun 2026 13:09:39 GMT  
		Size: 5.9 MB (5920565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d6f02b14d3b06798bfedf7117ec3761dbfb1e5e0904d8742f4c4b5a3e1e0611`  
		Last Modified: Tue, 02 Jun 2026 13:09:38 GMT  
		Size: 22.9 KB (22859 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12`

```console
$ docker pull geonetwork@sha256:cb26d353170e6b3eae87dda2b3c4b72250578132fa61b64902db528ba8197194
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
$ docker pull geonetwork@sha256:8a662a8e86f77c0eebc5ed196cb48f828b8234331cf022da7112f847705ba5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.5 MB (350505114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f1015be7de71de3d70cb23c18c4ffd63e5c1f114ce77c143504b49d54058dd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:13:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:13:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:13:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:13:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:13:59 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:14:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:14:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:14:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:14:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 09:20:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 09:20:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 09:20:15 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 09:20:15 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 09:20:15 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:20:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:20:15 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 09:20:15 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 09:20:15 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 09:20:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Jun 2026 09:20:38 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 09:20:38 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 09:20:38 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 09:20:38 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 10:18:46 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 10:18:46 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Jun 2026 10:18:46 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 10:18:46 GMT
ENV GN_VERSION=3.12.12
# Tue, 02 Jun 2026 10:18:46 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 02 Jun 2026 10:18:46 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Jun 2026 10:21:33 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Jun 2026 10:21:33 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:21:33 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:21:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 10:21:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d626348eec3a68143ac7cd0a6634adeccef97b9eb7a032bcc7d0cef5f8285d`  
		Last Modified: Tue, 02 Jun 2026 08:14:14 GMT  
		Size: 17.0 MB (16984251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5707a967e0439bbf45d99425ed29ad8d3becd9d15f8b5eaa332b3d5e9e4477b6`  
		Last Modified: Tue, 02 Jun 2026 08:14:15 GMT  
		Size: 55.2 MB (55200456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8992f58138a42d0304eba727e4c06c8e09e5343560ccd363242a2236eea1a9`  
		Last Modified: Tue, 02 Jun 2026 08:14:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6156d9eb6a345480d38c560b95e0a563acb7992de4c3ca5c87513811b3095b82`  
		Last Modified: Tue, 02 Jun 2026 08:14:14 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef8ad0895180f07049805cfdbee35b6c44fa7f7d11228ae4a46ccd082bdfb2d`  
		Last Modified: Tue, 02 Jun 2026 09:20:47 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122e8f0d3e6628291d3b43177a1830130f4eb0fa2230c8430b2d679cad18fc33`  
		Last Modified: Tue, 02 Jun 2026 09:20:47 GMT  
		Size: 14.0 MB (14034048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61db8eccffe64a18c8a87a2aaca01c884ee9bda5c27fc7cb01f5fe6296b08e5d`  
		Last Modified: Tue, 02 Jun 2026 10:21:59 GMT  
		Size: 234.6 MB (234550425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f048b1eb30b86bbdf2d290866de06934abf78713326ac99c123e4d02d9e2e70`  
		Last Modified: Tue, 02 Jun 2026 10:21:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:350ee2d8fc1b0b9ed379d6354b5dee7bfa432d7d6432df21a634ac8a4e7141ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4379511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46f8121372b4265fdbb93cf59b096d5fdf343bd0d375c1c3db4e1ab633cbb677`

```dockerfile
```

-	Layers:
	-	`sha256:41ee1bd80c8227bf07dc3bf4d7310e99f925d72043389590ec7fcd5309d9baa3`  
		Last Modified: Tue, 02 Jun 2026 10:21:53 GMT  
		Size: 4.4 MB (4360418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caa4ce7ba21b20ec4aedd8b3bb086e8586a2339fbf5e26fbe5155a08a01f74ec`  
		Last Modified: Tue, 02 Jun 2026 10:21:53 GMT  
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
$ docker pull geonetwork@sha256:eeb37ae30637fe0c95d6b72ec259cd856cb0bd6e8a65b9473bbe3d268f23c13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.8 MB (348751933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3030c62ad0ec0874c0bf59237136c289ddc48a513c52f8b0e6de5d323580466f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:15:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:15:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:15:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:15:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:15:24 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:15:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:15:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:15:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:15:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 09:29:22 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 09:29:22 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 09:29:22 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 09:29:22 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 09:29:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:29:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:29:22 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 09:29:22 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 09:29:22 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 09:29:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Jun 2026 09:29:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 09:29:49 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 09:29:49 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 09:29:49 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 10:15:36 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 10:15:36 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Jun 2026 10:15:36 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 10:15:36 GMT
ENV GN_VERSION=3.12.12
# Tue, 02 Jun 2026 10:15:36 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 02 Jun 2026 10:15:36 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Jun 2026 10:18:00 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Jun 2026 10:18:00 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:18:00 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:18:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 10:18:00 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab110e6d63137368eeacacd99b16eb78cfc6271be04d9600931c38644c992261`  
		Last Modified: Tue, 02 Jun 2026 08:15:40 GMT  
		Size: 17.0 MB (16997536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcefc1210a461c08953484fddcf25ec0fd5eecedd8609238356a152f3cad5d8`  
		Last Modified: Tue, 02 Jun 2026 08:15:41 GMT  
		Size: 54.3 MB (54277497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8924b2c1ef32e60b93ebd7f7ad1ab5ce46508e22d42097f7206c4ff58fb8ec95`  
		Last Modified: Tue, 02 Jun 2026 08:15:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3478717f2d1fd7b23ae3c0c5ee7e0478b158105010b3f1434e65ad459082ed`  
		Last Modified: Tue, 02 Jun 2026 08:15:39 GMT  
		Size: 2.5 KB (2484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d378e08ee54cb1c196aa65eb7c72e988ce6f7c57af5b04ee650d6f79cd04bb`  
		Last Modified: Tue, 02 Jun 2026 09:29:58 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b49df80cdfc0bdc5b2045768e8872ce1fc65b1efc752e0829fa8197df004f49`  
		Last Modified: Tue, 02 Jun 2026 09:29:59 GMT  
		Size: 14.0 MB (14042962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814029ba2327b904586a76040b03d18dc003ef4253feb1729049c3eadb5b237`  
		Last Modified: Tue, 02 Jun 2026 10:18:26 GMT  
		Size: 234.6 MB (234554405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa21e2f55c2d4a0c872c9e592e184a563668547601d42dd06bee3d5c2d34126`  
		Last Modified: Tue, 02 Jun 2026 10:18:21 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:618b32286975c8407424e1e1d7216cbac1e3403115f6f9fb7c72de1938e48ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b972747f50a26c83441ef6b796ea3f2a239ad65b2984dac1e7d4ae95f20e65a`

```dockerfile
```

-	Layers:
	-	`sha256:560c74eb9ca8ffaf07f1b69045192e21b37d023d7674a86876b16054427e1023`  
		Last Modified: Tue, 02 Jun 2026 10:18:21 GMT  
		Size: 4.4 MB (4361574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88ac7e70cb30158d8aadd5b6524c1cf384d03be7f7cb5237ebeee49460c58397`  
		Last Modified: Tue, 02 Jun 2026 10:18:21 GMT  
		Size: 19.2 KB (19185 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:1723e1cf65285704dbaed451779b0e9abf9b5e97a46f5ae045a7a1ee82d28545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.6 MB (354626549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24177fa31883ea1516321248e9696b70816fa062bd565165b7f60810497e05a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:10:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:10:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:10:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:10:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:10:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:10:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:10:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:26:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:26:34 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:26:34 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:26:34 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:26:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:26:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:26:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:26:34 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:26:34 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:27:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Jun 2026 10:27:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:27:53 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:27:53 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:27:53 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 12:13:47 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 12:13:47 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Jun 2026 12:13:47 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 12:13:47 GMT
ENV GN_VERSION=3.12.12
# Tue, 02 Jun 2026 12:13:47 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 02 Jun 2026 12:13:47 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Jun 2026 12:15:26 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Jun 2026 12:15:26 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 12:15:26 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 12:15:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 12:15:26 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef700e09ef3cf16d19218622a73899db0a8b42f33bfb19159bb4aa3576d5d21e`  
		Last Modified: Tue, 02 Jun 2026 08:10:42 GMT  
		Size: 18.8 MB (18813426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55d72b407fef39fa8814e430e4e2abf5a1cb6bb489417114169923011d31013`  
		Last Modified: Tue, 02 Jun 2026 08:10:44 GMT  
		Size: 52.7 MB (52670407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c627c23154e2a083d18c82d27d0653b1fbc6634ebb7f9fa305fbf926ed54fc`  
		Last Modified: Tue, 02 Jun 2026 08:10:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9936e589c30a5062ee9c1e1bcb1c1199b9777ac2ee1014f8649ddacc2163ce59`  
		Last Modified: Tue, 02 Jun 2026 08:10:41 GMT  
		Size: 2.5 KB (2484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d14c780d90f0cb147556d42aaff3742ee51c206f030b920374b79369c86eaed`  
		Last Modified: Tue, 02 Jun 2026 10:28:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90239c53cae997be1c44516f7a186ce795513affca342e8d08b18bdf335c4f94`  
		Last Modified: Tue, 02 Jun 2026 10:28:13 GMT  
		Size: 14.3 MB (14250688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99965b57ef70f8c05fb29fc31333abb28609abb5fba4096b2485688b9dfa3f9`  
		Last Modified: Tue, 02 Jun 2026 12:16:13 GMT  
		Size: 234.6 MB (234574800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28b6ef4fa678d84405bef337a68b597faedfa6a6dc78d6399a94226225e9e3a`  
		Last Modified: Tue, 02 Jun 2026 12:16:06 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:e560585afc926d2db24b8edfe025ef9b8447d66ecf6bed78d58a950394abf79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4382296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85dfd67c75083cdad844ae49e7c4b0c1de1a9eccc2a51b6c0b5efcc50a1acc4`

```dockerfile
```

-	Layers:
	-	`sha256:4388928b7ca786c3e332873e258211c0b3a7767da7718d85d6334ecb3f384bd1`  
		Last Modified: Tue, 02 Jun 2026 12:16:06 GMT  
		Size: 4.4 MB (4363165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8ff5a5dacb77c3e5f0a6e7b00433c4d1674ef5c50412a74ddefc54a3429fc31`  
		Last Modified: Tue, 02 Jun 2026 12:16:06 GMT  
		Size: 19.1 KB (19131 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12-postgres`

```console
$ docker pull geonetwork@sha256:7e643d08d39fa5afef38734747f9cc2e0210267a3b2c030df7f5a55ac2e83d7c
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
$ docker pull geonetwork@sha256:fa991a7af8407399d8018eced766e757bdf06b44fe606df6617a83e290eab222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.5 MB (364453401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cadac27da1a99e938d092d585c395fce16badbe50df90a28bcc355b546425cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:13:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:13:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:13:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:13:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:13:59 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:14:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:14:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:14:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:14:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 09:20:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 09:20:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 09:20:15 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 09:20:15 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 09:20:15 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:20:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:20:15 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 09:20:15 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 09:20:15 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 09:20:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Jun 2026 09:20:38 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 09:20:38 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 09:20:38 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 09:20:38 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 10:18:46 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 10:18:46 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Jun 2026 10:18:46 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 10:18:46 GMT
ENV GN_VERSION=3.12.12
# Tue, 02 Jun 2026 10:18:46 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 02 Jun 2026 10:18:46 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Jun 2026 10:21:33 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Jun 2026 10:21:33 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:21:33 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:21:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 10:21:33 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:12:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 11:12:38 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 02 Jun 2026 11:12:38 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 02 Jun 2026 11:12:38 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:12:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 11:12:38 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d626348eec3a68143ac7cd0a6634adeccef97b9eb7a032bcc7d0cef5f8285d`  
		Last Modified: Tue, 02 Jun 2026 08:14:14 GMT  
		Size: 17.0 MB (16984251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5707a967e0439bbf45d99425ed29ad8d3becd9d15f8b5eaa332b3d5e9e4477b6`  
		Last Modified: Tue, 02 Jun 2026 08:14:15 GMT  
		Size: 55.2 MB (55200456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8992f58138a42d0304eba727e4c06c8e09e5343560ccd363242a2236eea1a9`  
		Last Modified: Tue, 02 Jun 2026 08:14:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6156d9eb6a345480d38c560b95e0a563acb7992de4c3ca5c87513811b3095b82`  
		Last Modified: Tue, 02 Jun 2026 08:14:14 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef8ad0895180f07049805cfdbee35b6c44fa7f7d11228ae4a46ccd082bdfb2d`  
		Last Modified: Tue, 02 Jun 2026 09:20:47 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122e8f0d3e6628291d3b43177a1830130f4eb0fa2230c8430b2d679cad18fc33`  
		Last Modified: Tue, 02 Jun 2026 09:20:47 GMT  
		Size: 14.0 MB (14034048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61db8eccffe64a18c8a87a2aaca01c884ee9bda5c27fc7cb01f5fe6296b08e5d`  
		Last Modified: Tue, 02 Jun 2026 10:21:59 GMT  
		Size: 234.6 MB (234550425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f048b1eb30b86bbdf2d290866de06934abf78713326ac99c123e4d02d9e2e70`  
		Last Modified: Tue, 02 Jun 2026 10:21:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41aa9a2eacab96d28e6c7a8bfb96f13d77c089881abac4963ca846055ecde12`  
		Last Modified: Tue, 02 Jun 2026 11:12:54 GMT  
		Size: 13.9 MB (13944877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef71ba2ccc05bcc6ebf92c4a55c31a74abe4e4f15dafd28c03b726389fccd103`  
		Last Modified: Tue, 02 Jun 2026 11:12:54 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4dcb6e7935d0d69ac6b99d5aa3ef227e96188ebd3708bfa1ce039d999d277e7`  
		Last Modified: Tue, 02 Jun 2026 11:12:54 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a933f5b3cfbc7972552f6ba893cb061818c2165c5650ed0a26d331d51a475517`  
		Last Modified: Tue, 02 Jun 2026 11:12:54 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:085b320fefd84664d4b561cb6c90cfb77e0accc6a1774fb82b5f90eb77335bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5937887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dbe3b4fbd01408e145641f5da498c1db27a2f02dd181a73cb8236bc61e29b9`

```dockerfile
```

-	Layers:
	-	`sha256:551208eacb9cca92f10cbde3a3561db45a1f6d24df0995f98aed00025b563e45`  
		Last Modified: Tue, 02 Jun 2026 11:12:54 GMT  
		Size: 5.9 MB (5915069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfe63011f74aeb8d861246242f0034ded8ca83c563af35b83b961d243b8aa9e1`  
		Last Modified: Tue, 02 Jun 2026 11:12:53 GMT  
		Size: 22.8 KB (22818 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:fb3eaa4858f89d32974c11193e2e1cbec63edf03522acb507af84563025bc133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.2 MB (355214752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0778a9a784b38a1885676c4de52842cfcafeb29fd0f9f0085035b6bb8540257b`
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
# Tue, 02 Jun 2026 11:58:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 11:58:55 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 02 Jun 2026 11:58:55 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 02 Jun 2026 11:58:55 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:58:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 11:58:55 GMT
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
	-	`sha256:f0a6b7154bb6d508e62db3307ac2a9635cf9a6b5f1cc354abc229e8459176ba5`  
		Last Modified: Tue, 02 Jun 2026 11:59:11 GMT  
		Size: 13.0 MB (13019661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0383e0b9b2e14e1c014e3fc291693f1aa390b6aeeb8f5225c57fb1f116b4b3`  
		Last Modified: Tue, 02 Jun 2026 11:59:10 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ac43eb524602d7e60322f549844d3a1255d38dc847eef001f81eb171c32198`  
		Last Modified: Tue, 02 Jun 2026 11:59:10 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535c2c378579e3ee4e6b5ee423a4499b7ff4563b49f733a32f0f9ec4cc0a8995`  
		Last Modified: Tue, 02 Jun 2026 11:59:10 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:0a00b119e3df006bb64aad56a0c6cdd77f52deeb7522f32e54e980847c909a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5940692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5f4e96045ca6c118f4da8896ff99cabda34520f556c41440c3517dea0b2565`

```dockerfile
```

-	Layers:
	-	`sha256:55f619a4ade54433985193bf3b7483a53ccb7c9e02b3014e3ee277285d059121`  
		Last Modified: Tue, 02 Jun 2026 11:59:10 GMT  
		Size: 5.9 MB (5917788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed88097d79378d899390a0c096470715000d57dd48d4776c9d5dd721aa2ba03a`  
		Last Modified: Tue, 02 Jun 2026 11:59:10 GMT  
		Size: 22.9 KB (22904 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:a0442cf02c7f2571a3c96837a74ae95259795ab702df01c9a66e2a86776ba231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.7 MB (362675228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a7f8b0b01fae5df0cbf41fe78f68d15a16c3ccbdca700ab62cb771324297a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:15:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:15:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:15:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:15:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:15:24 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:15:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:15:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:15:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:15:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 09:29:22 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 09:29:22 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 09:29:22 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 09:29:22 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 09:29:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:29:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:29:22 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 09:29:22 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 09:29:22 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 09:29:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Jun 2026 09:29:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 09:29:49 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 09:29:49 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 09:29:49 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 10:15:36 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 10:15:36 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Jun 2026 10:15:36 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 10:15:36 GMT
ENV GN_VERSION=3.12.12
# Tue, 02 Jun 2026 10:15:36 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 02 Jun 2026 10:15:36 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Jun 2026 10:18:00 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Jun 2026 10:18:00 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:18:00 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:18:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 10:18:00 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:12:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 11:12:40 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 02 Jun 2026 11:12:40 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 02 Jun 2026 11:12:40 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:12:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 11:12:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab110e6d63137368eeacacd99b16eb78cfc6271be04d9600931c38644c992261`  
		Last Modified: Tue, 02 Jun 2026 08:15:40 GMT  
		Size: 17.0 MB (16997536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcefc1210a461c08953484fddcf25ec0fd5eecedd8609238356a152f3cad5d8`  
		Last Modified: Tue, 02 Jun 2026 08:15:41 GMT  
		Size: 54.3 MB (54277497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8924b2c1ef32e60b93ebd7f7ad1ab5ce46508e22d42097f7206c4ff58fb8ec95`  
		Last Modified: Tue, 02 Jun 2026 08:15:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3478717f2d1fd7b23ae3c0c5ee7e0478b158105010b3f1434e65ad459082ed`  
		Last Modified: Tue, 02 Jun 2026 08:15:39 GMT  
		Size: 2.5 KB (2484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d378e08ee54cb1c196aa65eb7c72e988ce6f7c57af5b04ee650d6f79cd04bb`  
		Last Modified: Tue, 02 Jun 2026 09:29:58 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b49df80cdfc0bdc5b2045768e8872ce1fc65b1efc752e0829fa8197df004f49`  
		Last Modified: Tue, 02 Jun 2026 09:29:59 GMT  
		Size: 14.0 MB (14042962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814029ba2327b904586a76040b03d18dc003ef4253feb1729049c3eadb5b237`  
		Last Modified: Tue, 02 Jun 2026 10:18:26 GMT  
		Size: 234.6 MB (234554405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa21e2f55c2d4a0c872c9e592e184a563668547601d42dd06bee3d5c2d34126`  
		Last Modified: Tue, 02 Jun 2026 10:18:21 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd7fa112850548b52ea4a5118ec9a2382e5b84e83370040067513ca7997293c`  
		Last Modified: Tue, 02 Jun 2026 11:12:56 GMT  
		Size: 13.9 MB (13919884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1db82b48fb4ce8aee0c62f7096a5959798cff7154e0f84a95d99e8f184203ce`  
		Last Modified: Tue, 02 Jun 2026 11:12:55 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0e75213f1a6a9cc7384258accba6786302e1c2193954d01375242b97096ac9`  
		Last Modified: Tue, 02 Jun 2026 11:12:55 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f11dacd96937679d1c1f429f6df904c73188ef92b3be9ab225ce9708a1ed668`  
		Last Modified: Tue, 02 Jun 2026 11:12:55 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:b99375b44548ef5869f54a8f9a873b0fa7c177a5f493cab9f7d9e79bee2c973c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5945203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e4dd5d6fd2c92f8dd5a2d9faa87512847f590691fae8a6a592804043337399`

```dockerfile
```

-	Layers:
	-	`sha256:6ed73ab7898a696b8a97a8cdaae42fb54ac1a888fb91c2171604269eed5540ed`  
		Last Modified: Tue, 02 Jun 2026 11:12:55 GMT  
		Size: 5.9 MB (5922277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94762734f42c3f0a62554b5696a90f2cf3d352cb14f53759076f68dc5f302593`  
		Last Modified: Tue, 02 Jun 2026 11:12:55 GMT  
		Size: 22.9 KB (22926 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:b1ef708a99b31a0753019c7875c19ba457ef35288e85d1b1965c4ad64953e0cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.1 MB (369070549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbac3869df5481f4999c3f52ce49e6fc387e6934a537e6d5d49e5a8347a836b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:10:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:10:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:10:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:10:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:10:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:10:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:10:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:26:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:26:34 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:26:34 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:26:34 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:26:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:26:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:26:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:26:34 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:26:34 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:27:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Jun 2026 10:27:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:27:53 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:27:53 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:27:53 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 12:13:47 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 12:13:47 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Jun 2026 12:13:47 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 12:13:47 GMT
ENV GN_VERSION=3.12.12
# Tue, 02 Jun 2026 12:13:47 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 02 Jun 2026 12:13:47 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Jun 2026 12:15:26 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Jun 2026 12:15:26 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 12:15:26 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 12:15:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 12:15:26 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 13:09:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 13:09:09 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 02 Jun 2026 13:09:09 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 02 Jun 2026 13:09:09 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 13:09:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 13:09:09 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef700e09ef3cf16d19218622a73899db0a8b42f33bfb19159bb4aa3576d5d21e`  
		Last Modified: Tue, 02 Jun 2026 08:10:42 GMT  
		Size: 18.8 MB (18813426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55d72b407fef39fa8814e430e4e2abf5a1cb6bb489417114169923011d31013`  
		Last Modified: Tue, 02 Jun 2026 08:10:44 GMT  
		Size: 52.7 MB (52670407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c627c23154e2a083d18c82d27d0653b1fbc6634ebb7f9fa305fbf926ed54fc`  
		Last Modified: Tue, 02 Jun 2026 08:10:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9936e589c30a5062ee9c1e1bcb1c1199b9777ac2ee1014f8649ddacc2163ce59`  
		Last Modified: Tue, 02 Jun 2026 08:10:41 GMT  
		Size: 2.5 KB (2484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d14c780d90f0cb147556d42aaff3742ee51c206f030b920374b79369c86eaed`  
		Last Modified: Tue, 02 Jun 2026 10:28:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90239c53cae997be1c44516f7a186ce795513affca342e8d08b18bdf335c4f94`  
		Last Modified: Tue, 02 Jun 2026 10:28:13 GMT  
		Size: 14.3 MB (14250688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99965b57ef70f8c05fb29fc31333abb28609abb5fba4096b2485688b9dfa3f9`  
		Last Modified: Tue, 02 Jun 2026 12:16:13 GMT  
		Size: 234.6 MB (234574800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28b6ef4fa678d84405bef337a68b597faedfa6a6dc78d6399a94226225e9e3a`  
		Last Modified: Tue, 02 Jun 2026 12:16:06 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82611a6196ed1d26821f84420d83aab48632b7fd682537ef4c51fc303ba46714`  
		Last Modified: Tue, 02 Jun 2026 13:09:39 GMT  
		Size: 14.4 MB (14440582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d888d4e9378ba16ffd5099330a63909f5f924e4d63798d74a8856d2e718b4b33`  
		Last Modified: Tue, 02 Jun 2026 13:09:39 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458b7518f5485eca0d690367e0a30691f9a0538e10a8117d0086010dd369a133`  
		Last Modified: Tue, 02 Jun 2026 13:09:39 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f9fc3d833ec36a3efb726142fe4316bceb038525a3ee2aae7157560799edd4`  
		Last Modified: Tue, 02 Jun 2026 13:09:39 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:279d5fde08c2ca72df74b19c73ada44d1ce1e37ef81ed74966f3cb9f34715fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5943424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8df88ca7729cd1cc60feb84b1b4d2814ea53f71d8a8f1d70070610963c625cd`

```dockerfile
```

-	Layers:
	-	`sha256:63ecf9fbe5a372905b0d81d252a29c50ea339cbd0d1b2177e1c15aa432029d66`  
		Last Modified: Tue, 02 Jun 2026 13:09:39 GMT  
		Size: 5.9 MB (5920565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d6f02b14d3b06798bfedf7117ec3761dbfb1e5e0904d8742f4c4b5a3e1e0611`  
		Last Modified: Tue, 02 Jun 2026 13:09:38 GMT  
		Size: 22.9 KB (22859 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12.12`

```console
$ docker pull geonetwork@sha256:cb26d353170e6b3eae87dda2b3c4b72250578132fa61b64902db528ba8197194
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
$ docker pull geonetwork@sha256:8a662a8e86f77c0eebc5ed196cb48f828b8234331cf022da7112f847705ba5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.5 MB (350505114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f1015be7de71de3d70cb23c18c4ffd63e5c1f114ce77c143504b49d54058dd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:13:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:13:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:13:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:13:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:13:59 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:14:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:14:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:14:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:14:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 09:20:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 09:20:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 09:20:15 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 09:20:15 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 09:20:15 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:20:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:20:15 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 09:20:15 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 09:20:15 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 09:20:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Jun 2026 09:20:38 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 09:20:38 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 09:20:38 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 09:20:38 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 10:18:46 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 10:18:46 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Jun 2026 10:18:46 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 10:18:46 GMT
ENV GN_VERSION=3.12.12
# Tue, 02 Jun 2026 10:18:46 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 02 Jun 2026 10:18:46 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Jun 2026 10:21:33 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Jun 2026 10:21:33 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:21:33 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:21:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 10:21:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d626348eec3a68143ac7cd0a6634adeccef97b9eb7a032bcc7d0cef5f8285d`  
		Last Modified: Tue, 02 Jun 2026 08:14:14 GMT  
		Size: 17.0 MB (16984251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5707a967e0439bbf45d99425ed29ad8d3becd9d15f8b5eaa332b3d5e9e4477b6`  
		Last Modified: Tue, 02 Jun 2026 08:14:15 GMT  
		Size: 55.2 MB (55200456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8992f58138a42d0304eba727e4c06c8e09e5343560ccd363242a2236eea1a9`  
		Last Modified: Tue, 02 Jun 2026 08:14:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6156d9eb6a345480d38c560b95e0a563acb7992de4c3ca5c87513811b3095b82`  
		Last Modified: Tue, 02 Jun 2026 08:14:14 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef8ad0895180f07049805cfdbee35b6c44fa7f7d11228ae4a46ccd082bdfb2d`  
		Last Modified: Tue, 02 Jun 2026 09:20:47 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122e8f0d3e6628291d3b43177a1830130f4eb0fa2230c8430b2d679cad18fc33`  
		Last Modified: Tue, 02 Jun 2026 09:20:47 GMT  
		Size: 14.0 MB (14034048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61db8eccffe64a18c8a87a2aaca01c884ee9bda5c27fc7cb01f5fe6296b08e5d`  
		Last Modified: Tue, 02 Jun 2026 10:21:59 GMT  
		Size: 234.6 MB (234550425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f048b1eb30b86bbdf2d290866de06934abf78713326ac99c123e4d02d9e2e70`  
		Last Modified: Tue, 02 Jun 2026 10:21:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:350ee2d8fc1b0b9ed379d6354b5dee7bfa432d7d6432df21a634ac8a4e7141ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4379511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46f8121372b4265fdbb93cf59b096d5fdf343bd0d375c1c3db4e1ab633cbb677`

```dockerfile
```

-	Layers:
	-	`sha256:41ee1bd80c8227bf07dc3bf4d7310e99f925d72043389590ec7fcd5309d9baa3`  
		Last Modified: Tue, 02 Jun 2026 10:21:53 GMT  
		Size: 4.4 MB (4360418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caa4ce7ba21b20ec4aedd8b3bb086e8586a2339fbf5e26fbe5155a08a01f74ec`  
		Last Modified: Tue, 02 Jun 2026 10:21:53 GMT  
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
$ docker pull geonetwork@sha256:eeb37ae30637fe0c95d6b72ec259cd856cb0bd6e8a65b9473bbe3d268f23c13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.8 MB (348751933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3030c62ad0ec0874c0bf59237136c289ddc48a513c52f8b0e6de5d323580466f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:15:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:15:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:15:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:15:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:15:24 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:15:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:15:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:15:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:15:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 09:29:22 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 09:29:22 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 09:29:22 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 09:29:22 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 09:29:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:29:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:29:22 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 09:29:22 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 09:29:22 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 09:29:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Jun 2026 09:29:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 09:29:49 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 09:29:49 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 09:29:49 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 10:15:36 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 10:15:36 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Jun 2026 10:15:36 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 10:15:36 GMT
ENV GN_VERSION=3.12.12
# Tue, 02 Jun 2026 10:15:36 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 02 Jun 2026 10:15:36 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Jun 2026 10:18:00 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Jun 2026 10:18:00 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:18:00 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:18:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 10:18:00 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab110e6d63137368eeacacd99b16eb78cfc6271be04d9600931c38644c992261`  
		Last Modified: Tue, 02 Jun 2026 08:15:40 GMT  
		Size: 17.0 MB (16997536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcefc1210a461c08953484fddcf25ec0fd5eecedd8609238356a152f3cad5d8`  
		Last Modified: Tue, 02 Jun 2026 08:15:41 GMT  
		Size: 54.3 MB (54277497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8924b2c1ef32e60b93ebd7f7ad1ab5ce46508e22d42097f7206c4ff58fb8ec95`  
		Last Modified: Tue, 02 Jun 2026 08:15:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3478717f2d1fd7b23ae3c0c5ee7e0478b158105010b3f1434e65ad459082ed`  
		Last Modified: Tue, 02 Jun 2026 08:15:39 GMT  
		Size: 2.5 KB (2484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d378e08ee54cb1c196aa65eb7c72e988ce6f7c57af5b04ee650d6f79cd04bb`  
		Last Modified: Tue, 02 Jun 2026 09:29:58 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b49df80cdfc0bdc5b2045768e8872ce1fc65b1efc752e0829fa8197df004f49`  
		Last Modified: Tue, 02 Jun 2026 09:29:59 GMT  
		Size: 14.0 MB (14042962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814029ba2327b904586a76040b03d18dc003ef4253feb1729049c3eadb5b237`  
		Last Modified: Tue, 02 Jun 2026 10:18:26 GMT  
		Size: 234.6 MB (234554405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa21e2f55c2d4a0c872c9e592e184a563668547601d42dd06bee3d5c2d34126`  
		Last Modified: Tue, 02 Jun 2026 10:18:21 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:618b32286975c8407424e1e1d7216cbac1e3403115f6f9fb7c72de1938e48ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b972747f50a26c83441ef6b796ea3f2a239ad65b2984dac1e7d4ae95f20e65a`

```dockerfile
```

-	Layers:
	-	`sha256:560c74eb9ca8ffaf07f1b69045192e21b37d023d7674a86876b16054427e1023`  
		Last Modified: Tue, 02 Jun 2026 10:18:21 GMT  
		Size: 4.4 MB (4361574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88ac7e70cb30158d8aadd5b6524c1cf384d03be7f7cb5237ebeee49460c58397`  
		Last Modified: Tue, 02 Jun 2026 10:18:21 GMT  
		Size: 19.2 KB (19185 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:1723e1cf65285704dbaed451779b0e9abf9b5e97a46f5ae045a7a1ee82d28545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.6 MB (354626549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24177fa31883ea1516321248e9696b70816fa062bd565165b7f60810497e05a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:10:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:10:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:10:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:10:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:10:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:10:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:10:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:26:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:26:34 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:26:34 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:26:34 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:26:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:26:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:26:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:26:34 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:26:34 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:27:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Jun 2026 10:27:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:27:53 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:27:53 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:27:53 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 12:13:47 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 12:13:47 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Jun 2026 12:13:47 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 12:13:47 GMT
ENV GN_VERSION=3.12.12
# Tue, 02 Jun 2026 12:13:47 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 02 Jun 2026 12:13:47 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Jun 2026 12:15:26 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Jun 2026 12:15:26 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 12:15:26 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 12:15:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 12:15:26 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef700e09ef3cf16d19218622a73899db0a8b42f33bfb19159bb4aa3576d5d21e`  
		Last Modified: Tue, 02 Jun 2026 08:10:42 GMT  
		Size: 18.8 MB (18813426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55d72b407fef39fa8814e430e4e2abf5a1cb6bb489417114169923011d31013`  
		Last Modified: Tue, 02 Jun 2026 08:10:44 GMT  
		Size: 52.7 MB (52670407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c627c23154e2a083d18c82d27d0653b1fbc6634ebb7f9fa305fbf926ed54fc`  
		Last Modified: Tue, 02 Jun 2026 08:10:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9936e589c30a5062ee9c1e1bcb1c1199b9777ac2ee1014f8649ddacc2163ce59`  
		Last Modified: Tue, 02 Jun 2026 08:10:41 GMT  
		Size: 2.5 KB (2484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d14c780d90f0cb147556d42aaff3742ee51c206f030b920374b79369c86eaed`  
		Last Modified: Tue, 02 Jun 2026 10:28:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90239c53cae997be1c44516f7a186ce795513affca342e8d08b18bdf335c4f94`  
		Last Modified: Tue, 02 Jun 2026 10:28:13 GMT  
		Size: 14.3 MB (14250688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99965b57ef70f8c05fb29fc31333abb28609abb5fba4096b2485688b9dfa3f9`  
		Last Modified: Tue, 02 Jun 2026 12:16:13 GMT  
		Size: 234.6 MB (234574800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28b6ef4fa678d84405bef337a68b597faedfa6a6dc78d6399a94226225e9e3a`  
		Last Modified: Tue, 02 Jun 2026 12:16:06 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:e560585afc926d2db24b8edfe025ef9b8447d66ecf6bed78d58a950394abf79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4382296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85dfd67c75083cdad844ae49e7c4b0c1de1a9eccc2a51b6c0b5efcc50a1acc4`

```dockerfile
```

-	Layers:
	-	`sha256:4388928b7ca786c3e332873e258211c0b3a7767da7718d85d6334ecb3f384bd1`  
		Last Modified: Tue, 02 Jun 2026 12:16:06 GMT  
		Size: 4.4 MB (4363165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8ff5a5dacb77c3e5f0a6e7b00433c4d1674ef5c50412a74ddefc54a3429fc31`  
		Last Modified: Tue, 02 Jun 2026 12:16:06 GMT  
		Size: 19.1 KB (19131 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12.12-postgres`

```console
$ docker pull geonetwork@sha256:7e643d08d39fa5afef38734747f9cc2e0210267a3b2c030df7f5a55ac2e83d7c
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
$ docker pull geonetwork@sha256:fa991a7af8407399d8018eced766e757bdf06b44fe606df6617a83e290eab222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.5 MB (364453401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cadac27da1a99e938d092d585c395fce16badbe50df90a28bcc355b546425cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:13:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:13:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:13:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:13:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:13:59 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:14:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:14:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:14:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:14:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 09:20:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 09:20:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 09:20:15 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 09:20:15 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 09:20:15 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:20:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:20:15 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 09:20:15 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 09:20:15 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 09:20:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Jun 2026 09:20:38 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 09:20:38 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 09:20:38 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 09:20:38 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 10:18:46 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 10:18:46 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Jun 2026 10:18:46 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 10:18:46 GMT
ENV GN_VERSION=3.12.12
# Tue, 02 Jun 2026 10:18:46 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 02 Jun 2026 10:18:46 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Jun 2026 10:21:33 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Jun 2026 10:21:33 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:21:33 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:21:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 10:21:33 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:12:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 11:12:38 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 02 Jun 2026 11:12:38 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 02 Jun 2026 11:12:38 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:12:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 11:12:38 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d626348eec3a68143ac7cd0a6634adeccef97b9eb7a032bcc7d0cef5f8285d`  
		Last Modified: Tue, 02 Jun 2026 08:14:14 GMT  
		Size: 17.0 MB (16984251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5707a967e0439bbf45d99425ed29ad8d3becd9d15f8b5eaa332b3d5e9e4477b6`  
		Last Modified: Tue, 02 Jun 2026 08:14:15 GMT  
		Size: 55.2 MB (55200456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8992f58138a42d0304eba727e4c06c8e09e5343560ccd363242a2236eea1a9`  
		Last Modified: Tue, 02 Jun 2026 08:14:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6156d9eb6a345480d38c560b95e0a563acb7992de4c3ca5c87513811b3095b82`  
		Last Modified: Tue, 02 Jun 2026 08:14:14 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef8ad0895180f07049805cfdbee35b6c44fa7f7d11228ae4a46ccd082bdfb2d`  
		Last Modified: Tue, 02 Jun 2026 09:20:47 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122e8f0d3e6628291d3b43177a1830130f4eb0fa2230c8430b2d679cad18fc33`  
		Last Modified: Tue, 02 Jun 2026 09:20:47 GMT  
		Size: 14.0 MB (14034048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61db8eccffe64a18c8a87a2aaca01c884ee9bda5c27fc7cb01f5fe6296b08e5d`  
		Last Modified: Tue, 02 Jun 2026 10:21:59 GMT  
		Size: 234.6 MB (234550425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f048b1eb30b86bbdf2d290866de06934abf78713326ac99c123e4d02d9e2e70`  
		Last Modified: Tue, 02 Jun 2026 10:21:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41aa9a2eacab96d28e6c7a8bfb96f13d77c089881abac4963ca846055ecde12`  
		Last Modified: Tue, 02 Jun 2026 11:12:54 GMT  
		Size: 13.9 MB (13944877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef71ba2ccc05bcc6ebf92c4a55c31a74abe4e4f15dafd28c03b726389fccd103`  
		Last Modified: Tue, 02 Jun 2026 11:12:54 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4dcb6e7935d0d69ac6b99d5aa3ef227e96188ebd3708bfa1ce039d999d277e7`  
		Last Modified: Tue, 02 Jun 2026 11:12:54 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a933f5b3cfbc7972552f6ba893cb061818c2165c5650ed0a26d331d51a475517`  
		Last Modified: Tue, 02 Jun 2026 11:12:54 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:085b320fefd84664d4b561cb6c90cfb77e0accc6a1774fb82b5f90eb77335bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5937887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dbe3b4fbd01408e145641f5da498c1db27a2f02dd181a73cb8236bc61e29b9`

```dockerfile
```

-	Layers:
	-	`sha256:551208eacb9cca92f10cbde3a3561db45a1f6d24df0995f98aed00025b563e45`  
		Last Modified: Tue, 02 Jun 2026 11:12:54 GMT  
		Size: 5.9 MB (5915069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfe63011f74aeb8d861246242f0034ded8ca83c563af35b83b961d243b8aa9e1`  
		Last Modified: Tue, 02 Jun 2026 11:12:53 GMT  
		Size: 22.8 KB (22818 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:fb3eaa4858f89d32974c11193e2e1cbec63edf03522acb507af84563025bc133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.2 MB (355214752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0778a9a784b38a1885676c4de52842cfcafeb29fd0f9f0085035b6bb8540257b`
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
# Tue, 02 Jun 2026 11:58:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 11:58:55 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 02 Jun 2026 11:58:55 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 02 Jun 2026 11:58:55 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:58:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 11:58:55 GMT
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
	-	`sha256:f0a6b7154bb6d508e62db3307ac2a9635cf9a6b5f1cc354abc229e8459176ba5`  
		Last Modified: Tue, 02 Jun 2026 11:59:11 GMT  
		Size: 13.0 MB (13019661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0383e0b9b2e14e1c014e3fc291693f1aa390b6aeeb8f5225c57fb1f116b4b3`  
		Last Modified: Tue, 02 Jun 2026 11:59:10 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ac43eb524602d7e60322f549844d3a1255d38dc847eef001f81eb171c32198`  
		Last Modified: Tue, 02 Jun 2026 11:59:10 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535c2c378579e3ee4e6b5ee423a4499b7ff4563b49f733a32f0f9ec4cc0a8995`  
		Last Modified: Tue, 02 Jun 2026 11:59:10 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:0a00b119e3df006bb64aad56a0c6cdd77f52deeb7522f32e54e980847c909a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5940692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5f4e96045ca6c118f4da8896ff99cabda34520f556c41440c3517dea0b2565`

```dockerfile
```

-	Layers:
	-	`sha256:55f619a4ade54433985193bf3b7483a53ccb7c9e02b3014e3ee277285d059121`  
		Last Modified: Tue, 02 Jun 2026 11:59:10 GMT  
		Size: 5.9 MB (5917788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed88097d79378d899390a0c096470715000d57dd48d4776c9d5dd721aa2ba03a`  
		Last Modified: Tue, 02 Jun 2026 11:59:10 GMT  
		Size: 22.9 KB (22904 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:a0442cf02c7f2571a3c96837a74ae95259795ab702df01c9a66e2a86776ba231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.7 MB (362675228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a7f8b0b01fae5df0cbf41fe78f68d15a16c3ccbdca700ab62cb771324297a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:15:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:15:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:15:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:15:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:15:24 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:15:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:15:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:15:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:15:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 09:29:22 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 09:29:22 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 09:29:22 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 09:29:22 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 09:29:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:29:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 09:29:22 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 09:29:22 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 09:29:22 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 09:29:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Jun 2026 09:29:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 09:29:49 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 09:29:49 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 09:29:49 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 10:15:36 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 10:15:36 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Jun 2026 10:15:36 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 10:15:36 GMT
ENV GN_VERSION=3.12.12
# Tue, 02 Jun 2026 10:15:36 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 02 Jun 2026 10:15:36 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Jun 2026 10:18:00 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Jun 2026 10:18:00 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:18:00 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:18:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 10:18:00 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:12:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 11:12:40 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 02 Jun 2026 11:12:40 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 02 Jun 2026 11:12:40 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:12:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 11:12:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab110e6d63137368eeacacd99b16eb78cfc6271be04d9600931c38644c992261`  
		Last Modified: Tue, 02 Jun 2026 08:15:40 GMT  
		Size: 17.0 MB (16997536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcefc1210a461c08953484fddcf25ec0fd5eecedd8609238356a152f3cad5d8`  
		Last Modified: Tue, 02 Jun 2026 08:15:41 GMT  
		Size: 54.3 MB (54277497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8924b2c1ef32e60b93ebd7f7ad1ab5ce46508e22d42097f7206c4ff58fb8ec95`  
		Last Modified: Tue, 02 Jun 2026 08:15:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3478717f2d1fd7b23ae3c0c5ee7e0478b158105010b3f1434e65ad459082ed`  
		Last Modified: Tue, 02 Jun 2026 08:15:39 GMT  
		Size: 2.5 KB (2484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d378e08ee54cb1c196aa65eb7c72e988ce6f7c57af5b04ee650d6f79cd04bb`  
		Last Modified: Tue, 02 Jun 2026 09:29:58 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b49df80cdfc0bdc5b2045768e8872ce1fc65b1efc752e0829fa8197df004f49`  
		Last Modified: Tue, 02 Jun 2026 09:29:59 GMT  
		Size: 14.0 MB (14042962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814029ba2327b904586a76040b03d18dc003ef4253feb1729049c3eadb5b237`  
		Last Modified: Tue, 02 Jun 2026 10:18:26 GMT  
		Size: 234.6 MB (234554405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa21e2f55c2d4a0c872c9e592e184a563668547601d42dd06bee3d5c2d34126`  
		Last Modified: Tue, 02 Jun 2026 10:18:21 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd7fa112850548b52ea4a5118ec9a2382e5b84e83370040067513ca7997293c`  
		Last Modified: Tue, 02 Jun 2026 11:12:56 GMT  
		Size: 13.9 MB (13919884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1db82b48fb4ce8aee0c62f7096a5959798cff7154e0f84a95d99e8f184203ce`  
		Last Modified: Tue, 02 Jun 2026 11:12:55 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0e75213f1a6a9cc7384258accba6786302e1c2193954d01375242b97096ac9`  
		Last Modified: Tue, 02 Jun 2026 11:12:55 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f11dacd96937679d1c1f429f6df904c73188ef92b3be9ab225ce9708a1ed668`  
		Last Modified: Tue, 02 Jun 2026 11:12:55 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:b99375b44548ef5869f54a8f9a873b0fa7c177a5f493cab9f7d9e79bee2c973c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5945203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e4dd5d6fd2c92f8dd5a2d9faa87512847f590691fae8a6a592804043337399`

```dockerfile
```

-	Layers:
	-	`sha256:6ed73ab7898a696b8a97a8cdaae42fb54ac1a888fb91c2171604269eed5540ed`  
		Last Modified: Tue, 02 Jun 2026 11:12:55 GMT  
		Size: 5.9 MB (5922277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94762734f42c3f0a62554b5696a90f2cf3d352cb14f53759076f68dc5f302593`  
		Last Modified: Tue, 02 Jun 2026 11:12:55 GMT  
		Size: 22.9 KB (22926 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:b1ef708a99b31a0753019c7875c19ba457ef35288e85d1b1965c4ad64953e0cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.1 MB (369070549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbac3869df5481f4999c3f52ce49e6fc387e6934a537e6d5d49e5a8347a836b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:10:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:10:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:10:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:10:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='ac93b4b75d6c0592c83030dbbeeaed46f5fbfccb276cf26c86aab3e49bba090e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:10:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:10:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:10:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:26:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:26:34 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:26:34 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:26:34 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:26:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:26:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:26:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:26:34 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:26:34 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:27:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 02 Jun 2026 10:27:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:27:53 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:27:53 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:27:53 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 12:13:47 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 12:13:47 GMT
ENV DATA_DIR=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data
# Tue, 02 Jun 2026 12:13:47 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -server -Xms512m -Xmx2024m -XX:NewSize=512m -XX:MaxNewSize=1024m -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 12:13:47 GMT
ENV GN_VERSION=3.12.12
# Tue, 02 Jun 2026 12:13:47 GMT
ENV GN_DOWNLOAD_MD5=c9d2a15f5cecbd31fa6697c3f52f0180
# Tue, 02 Jun 2026 12:13:47 GMT
WORKDIR /usr/local/tomcat/webapps
# Tue, 02 Jun 2026 12:15:26 GMT
RUN apt-get update &&      apt-get install -y --no-install-recommends           unzip           curl &&     rm -rf /var/lib/apt/lists/* &&      curl -fSL -o $GN_FILE      https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download &&      echo "${GN_DOWNLOAD_MD5} *${GN_FILE}" | md5sum -c &&      mkdir -p geonetwork &&      unzip -e $GN_FILE -d geonetwork &&      rm $GN_FILE # buildkit
# Tue, 02 Jun 2026 12:15:26 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 12:15:26 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 12:15:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 12:15:26 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 13:09:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 13:09:09 GMT
RUN sed -i -e 's#<import resource="../config-db/${geonetwork.db.type:h2}.xml"/>#<!--<import resource="../config-db/${geonetwork.db.type:h2}.xml"/-->#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" && sed -i -e 's#<!--<import resource="../config-db/postgres.xml"/>-->#<import resource="../config-db/postgres.xml"/>#g' "${CATALINA_HOME}/webapps/geonetwork/WEB-INF/config-node/srv.xml" # buildkit
# Tue, 02 Jun 2026 13:09:09 GMT
COPY ./jdbc.properties /usr/local/tomcat/webapps/geonetwork/WEB-INF/config-db/jdbc.properties # buildkit
# Tue, 02 Jun 2026 13:09:09 GMT
COPY ./docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 13:09:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 13:09:09 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef700e09ef3cf16d19218622a73899db0a8b42f33bfb19159bb4aa3576d5d21e`  
		Last Modified: Tue, 02 Jun 2026 08:10:42 GMT  
		Size: 18.8 MB (18813426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55d72b407fef39fa8814e430e4e2abf5a1cb6bb489417114169923011d31013`  
		Last Modified: Tue, 02 Jun 2026 08:10:44 GMT  
		Size: 52.7 MB (52670407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c627c23154e2a083d18c82d27d0653b1fbc6634ebb7f9fa305fbf926ed54fc`  
		Last Modified: Tue, 02 Jun 2026 08:10:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9936e589c30a5062ee9c1e1bcb1c1199b9777ac2ee1014f8649ddacc2163ce59`  
		Last Modified: Tue, 02 Jun 2026 08:10:41 GMT  
		Size: 2.5 KB (2484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d14c780d90f0cb147556d42aaff3742ee51c206f030b920374b79369c86eaed`  
		Last Modified: Tue, 02 Jun 2026 10:28:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90239c53cae997be1c44516f7a186ce795513affca342e8d08b18bdf335c4f94`  
		Last Modified: Tue, 02 Jun 2026 10:28:13 GMT  
		Size: 14.3 MB (14250688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99965b57ef70f8c05fb29fc31333abb28609abb5fba4096b2485688b9dfa3f9`  
		Last Modified: Tue, 02 Jun 2026 12:16:13 GMT  
		Size: 234.6 MB (234574800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28b6ef4fa678d84405bef337a68b597faedfa6a6dc78d6399a94226225e9e3a`  
		Last Modified: Tue, 02 Jun 2026 12:16:06 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82611a6196ed1d26821f84420d83aab48632b7fd682537ef4c51fc303ba46714`  
		Last Modified: Tue, 02 Jun 2026 13:09:39 GMT  
		Size: 14.4 MB (14440582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d888d4e9378ba16ffd5099330a63909f5f924e4d63798d74a8856d2e718b4b33`  
		Last Modified: Tue, 02 Jun 2026 13:09:39 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458b7518f5485eca0d690367e0a30691f9a0538e10a8117d0086010dd369a133`  
		Last Modified: Tue, 02 Jun 2026 13:09:39 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f9fc3d833ec36a3efb726142fe4316bceb038525a3ee2aae7157560799edd4`  
		Last Modified: Tue, 02 Jun 2026 13:09:39 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:279d5fde08c2ca72df74b19c73ada44d1ce1e37ef81ed74966f3cb9f34715fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5943424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8df88ca7729cd1cc60feb84b1b4d2814ea53f71d8a8f1d70070610963c625cd`

```dockerfile
```

-	Layers:
	-	`sha256:63ecf9fbe5a372905b0d81d252a29c50ea339cbd0d1b2177e1c15aa432029d66`  
		Last Modified: Tue, 02 Jun 2026 13:09:39 GMT  
		Size: 5.9 MB (5920565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d6f02b14d3b06798bfedf7117ec3761dbfb1e5e0904d8742f4c4b5a3e1e0611`  
		Last Modified: Tue, 02 Jun 2026 13:09:38 GMT  
		Size: 22.9 KB (22859 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4`

```console
$ docker pull geonetwork@sha256:5f67da2cc43bd7718e2e0676f25d3b91db7d97c2187ded37db1d83b3e1c44427
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
$ docker pull geonetwork@sha256:1570ebc4c8d8cae30c2ee5340843640ffa9879405b5716b9063589070972e6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.1 MB (420070202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dc43286c71acc45160e65bec64543ed1d40274e354fdb64655bda3dede6b29`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:14:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:14:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:14:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:14:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:14:19 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 02 Jun 2026 08:14:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:14:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:14:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:14:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:17:46 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:17:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:17:46 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:17:46 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:17:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:17:46 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:17:46 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:17:46 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:17:46 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:17:46 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 10:17:50 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:17:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:17:51 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:17:51 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:17:51 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:13:09 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 11:13:09 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 02 Jun 2026 11:13:09 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 02 Jun 2026 11:13:09 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 11:13:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 02 Jun 2026 11:13:09 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 11:13:09 GMT
ENV GN_VERSION=4.4.10
# Tue, 02 Jun 2026 11:13:09 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 02 Jun 2026 11:13:21 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 11:13:21 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 02 Jun 2026 11:13:21 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 11:13:21 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:13:21 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 11:13:21 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:13:21 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9e436cd644d0619bdfd1c8d1dce9e824e836e6102bf4a4c26919785ffe2a7c`  
		Last Modified: Tue, 02 Jun 2026 08:14:35 GMT  
		Size: 17.0 MB (16984112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abe231f9a275556a3c449f9746da9863dbbea3001e50afdbf5209553a0533c2`  
		Last Modified: Tue, 02 Jun 2026 08:14:36 GMT  
		Size: 47.3 MB (47344216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f689e05e256f3387912f6eab83ac21ffe596b6aa357a513c261ad13b21d283`  
		Last Modified: Tue, 02 Jun 2026 08:14:34 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5e34d12e53e20283e3eaeab1e665797d41b9b9ca6c3b47599a697790b15acb`  
		Last Modified: Tue, 02 Jun 2026 08:14:34 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b12c99159fc66956c2d9b5f3ac562fb93293b4f0ac571b0e57c73f17e7bfdbc`  
		Last Modified: Tue, 02 Jun 2026 10:17:59 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328a1e80cac330b8fd4cbe150711db3a5abd2333338c94c45dae5cff116eb841`  
		Last Modified: Tue, 02 Jun 2026 10:17:59 GMT  
		Size: 13.8 MB (13796163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b0b2346d28acc1f3441f42c9a41c27c0d9217183a6cb1662035858276ab3af`  
		Last Modified: Tue, 02 Jun 2026 10:17:59 GMT  
		Size: 224.8 KB (224833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631e6695a5c2e9c5433e05ca7109c40ad41585acc223c064807c7d7bdd6dc8e1`  
		Last Modified: Tue, 02 Jun 2026 11:13:44 GMT  
		Size: 239.2 KB (239211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34f6d9f937ddbf71a730e33bf0de46f6b661b62fd745421480f32221210968a`  
		Last Modified: Tue, 02 Jun 2026 11:13:51 GMT  
		Size: 311.7 MB (311742293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfdf3d2859f9d8424ea7bf91e8997d328dc41984fb42867f418064ea2487f22`  
		Last Modified: Tue, 02 Jun 2026 11:13:44 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904fe9ae87726911c9251a8b694e0db164afe48ddfd76b876cc5c751d0cf0be2`  
		Last Modified: Tue, 02 Jun 2026 11:13:44 GMT  
		Size: 3.0 KB (3013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ac3509e51ad06df68519ef10a212abe04b754f8f9bf2e785ba89fdea8a64ab`  
		Last Modified: Tue, 02 Jun 2026 11:13:45 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:bcd3bd1d3e14dbe7402887856277c2dc5324cef64b143b11244a603ca61bfe7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4219006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be50188d7bae4be76a3085cd1218ce37da8710d7eb25627a8f2e4a41b377483e`

```dockerfile
```

-	Layers:
	-	`sha256:955e2a3dcc94ad31b3cf1bdf1bc505d56756b274f8c6dab096adf4fa38ed0b17`  
		Last Modified: Tue, 02 Jun 2026 11:13:44 GMT  
		Size: 4.2 MB (4193576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:824708be85a603e7d03834925cdc488d2492aaf2676ef0436d0b4d6079c3d583`  
		Last Modified: Tue, 02 Jun 2026 11:13:44 GMT  
		Size: 25.4 KB (25430 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:48672a66b22db2e0a6a080edc7fcda4f72b51018cb534aacbfb506fe2e48ac41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.5 MB (414526279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997ae873464f8038256b1e1f8c38043d2d0f858d9e888aa62e1d70d763efabc4`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
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
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 02 Jun 2026 08:12:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:12:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:12:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:12:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:13:26 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:13:26 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:13:26 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:13:26 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:13:26 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:13:26 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:13:26 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:13:26 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:13:26 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:13:27 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 10:13:32 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:13:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:13:33 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:13:33 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:13:33 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:11:38 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 11:11:38 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 02 Jun 2026 11:11:38 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 02 Jun 2026 11:11:38 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 11:11:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 02 Jun 2026 11:11:38 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 11:11:38 GMT
ENV GN_VERSION=4.4.10
# Tue, 02 Jun 2026 11:11:38 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 02 Jun 2026 11:13:27 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 11:13:27 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 02 Jun 2026 11:13:27 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 11:13:27 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:13:27 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 11:13:27 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:13:27 GMT
VOLUME [/catalogue-data]
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
	-	`sha256:a763aa8647dee2704dbccddf100af5e050e07be63b2091352322da501dfbaeed`  
		Last Modified: Tue, 02 Jun 2026 08:13:03 GMT  
		Size: 45.5 MB (45454025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce71c5b0eb84b76e19875d5a01ece3a180b99ea3e5d3b749c53692b2767e3c00`  
		Last Modified: Tue, 02 Jun 2026 08:13:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a437059cd3dbdb7d8a53d4964b178c30acdb400c5d84e6e28913d7ff76de3c1`  
		Last Modified: Tue, 02 Jun 2026 08:13:01 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273a3f3cdc146550c02e7329c464a66778b96b407606914d90d5859e7f59582d`  
		Last Modified: Tue, 02 Jun 2026 10:13:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d00a83829a70306b914f1f06e4d228eee0528f75ea07c900f77b513fd6d2687`  
		Last Modified: Tue, 02 Jun 2026 10:13:41 GMT  
		Size: 13.7 MB (13730088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8591662de7c4b4f561acb1dbb592e6eaa7f8d2a4121831ac8d3ff3eca4e6b449`  
		Last Modified: Tue, 02 Jun 2026 10:13:41 GMT  
		Size: 196.5 KB (196506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6721ba9b0a083d0801ac0c20f69e0dd674e9b3eb8a07b31f81de134d1810189c`  
		Last Modified: Tue, 02 Jun 2026 11:13:52 GMT  
		Size: 226.4 KB (226408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f28a16af03b29f9c6bb827df7b6ccaab84a679b76483cf6b774c3a2226007b`  
		Last Modified: Tue, 02 Jun 2026 11:13:58 GMT  
		Size: 311.7 MB (311742307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02adf392821be303350cc5ba7f6cb7d9bdc39c212a32b10b5f563392b70bffd`  
		Last Modified: Tue, 02 Jun 2026 11:13:52 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08109080f302519f9109ebb24ba352f31ec448283e66b08d714627ea7e32e783`  
		Last Modified: Tue, 02 Jun 2026 11:13:52 GMT  
		Size: 3.0 KB (3016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeb7723f52d6bd1f9743c10628d1730f1718c8aa598c4d03ab818c380589c23`  
		Last Modified: Tue, 02 Jun 2026 11:13:53 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:36090bc31adc9322f761df9782ad44aad6ddd259ab0d5f66e98adb9d85bdf44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4222701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36846105faa0e4a1f4207d1101a38583582d34b13a26de9574ccc4f0359ac03e`

```dockerfile
```

-	Layers:
	-	`sha256:d9f76d562b08f9c8c41540a0ac0426d5e1cdf86523a76b88bc663b7b5fae912e`  
		Last Modified: Tue, 02 Jun 2026 11:13:52 GMT  
		Size: 4.2 MB (4197179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e01fe87e0d3cf12ec30a888f05820dd55440e10252a36e8c2280c7be846736a`  
		Last Modified: Tue, 02 Jun 2026 11:13:51 GMT  
		Size: 25.5 KB (25522 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:9676808067bb17308a14f06f9e857a05af791997b1b76ae7407bfc4ec3578381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.6 MB (417551650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9c1ce65405f2b22e9a97cd1a6842dadcb4706ff1dbad48fde134b9705543b3`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:15:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:15:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:15:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:15:43 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:15:43 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 02 Jun 2026 08:15:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:15:48 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:15:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:15:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:14:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:14:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:14:03 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:14:03 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:14:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:14:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:14:03 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:14:03 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:14:03 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:14:03 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 10:14:08 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:14:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:14:09 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:14:09 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:14:09 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:13:04 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 11:13:04 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 02 Jun 2026 11:13:04 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 02 Jun 2026 11:13:04 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 11:13:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 02 Jun 2026 11:13:04 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 11:13:04 GMT
ENV GN_VERSION=4.4.10
# Tue, 02 Jun 2026 11:13:04 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 02 Jun 2026 11:13:18 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 11:13:18 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 02 Jun 2026 11:13:18 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 11:13:18 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:13:18 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 11:13:18 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:13:18 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77acf8a2fd2a14aa128b125e15d261df4fd4f487386a6ac710a99968b2ed8d60`  
		Last Modified: Tue, 02 Jun 2026 08:16:00 GMT  
		Size: 17.0 MB (16997549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e07080645b5dbe3f11ea303d9cef4b4ac977a37efb6d74f92b3f69ded5806d`  
		Last Modified: Tue, 02 Jun 2026 08:16:01 GMT  
		Size: 45.7 MB (45659671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a181db84648310ad9c72731e407b7e06733928683e3ff6e8dfd6c50535d2f74f`  
		Last Modified: Tue, 02 Jun 2026 08:15:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ef243a4acfe4609f9532dec8a35af094f6898a9fba63b1f0a1a16ec457df5c`  
		Last Modified: Tue, 02 Jun 2026 08:15:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7790686ff36b34814640358cae09b83fb719b6ad854894f2582a7d261fd7b5c2`  
		Last Modified: Tue, 02 Jun 2026 10:14:17 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967c3d5f7725f795501d2f608262ba31047ef094db7f89fffb0054f9c2a4ddaf`  
		Last Modified: Tue, 02 Jun 2026 10:14:18 GMT  
		Size: 13.8 MB (13805557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135ba0c297a795416529870fe8e06d5e61ea32c4b717ec3e761809c8be3e7fba`  
		Last Modified: Tue, 02 Jun 2026 10:14:17 GMT  
		Size: 225.1 KB (225133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e42b762b4b42d36927c23c79fa2b1fbb493bd5f5f947ff2030fc89582c79e8`  
		Last Modified: Tue, 02 Jun 2026 11:13:42 GMT  
		Size: 238.4 KB (238420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dad06061b9135ac54d43e6166ed5b64a1ed261a151357cc2e40a155dbee617`  
		Last Modified: Tue, 02 Jun 2026 11:13:50 GMT  
		Size: 311.7 MB (311742343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ad0e9b31522ca2d2867af09ff0295a27534d6b944e82444403d676ec991869`  
		Last Modified: Tue, 02 Jun 2026 11:13:42 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e02ee9d670430ec4fc79c123f360dd0a2cdc68537b9386955c8e42f0589323`  
		Last Modified: Tue, 02 Jun 2026 11:13:42 GMT  
		Size: 3.0 KB (3014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bd61185368c5cbc16f5753636d8291fcc8e628eb8ea151e1f3645ddc3f5d46`  
		Last Modified: Tue, 02 Jun 2026 11:13:43 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:17b5950d45a383497c3d42691f7f753f0ba140f028ba66a162df54395d1d1056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4220215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5573828472fd131d82084b2e3968931d3b6fdd186e8b9e130017822a1017be67`

```dockerfile
```

-	Layers:
	-	`sha256:329a5eb203f3614de3aecd40c53e9d8889938303b5a5709ee0cde9541303a4e0`  
		Last Modified: Tue, 02 Jun 2026 11:13:42 GMT  
		Size: 4.2 MB (4194666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a2308185e4ec060c856aab2a590654a1b72a4fb390b9518548e2fa92eebc9d0`  
		Last Modified: Tue, 02 Jun 2026 11:13:42 GMT  
		Size: 25.5 KB (25549 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:9457b2ebac2d8732e4077e1a44c8a96d3d07fcdfc85c4c81a6a53527db0e9784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.0 MB (422047651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0b120f44c545db492728f2787537047bd7c139c2731d78e73a2581d6c0ce0f`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:10:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:10:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:10:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 02 Jun 2026 08:11:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:11:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:11:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:11:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 11:12:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 11:12:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 11:12:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 11:12:06 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 11:12:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 11:12:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 11:12:06 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 11:12:06 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 11:12:06 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 11:13:46 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 11:13:54 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 11:13:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 11:13:56 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 11:13:56 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 11:13:56 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 12:12:28 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 12:12:28 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 02 Jun 2026 12:12:28 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 02 Jun 2026 12:12:28 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 12:12:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 02 Jun 2026 12:12:28 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 12:12:28 GMT
ENV GN_VERSION=4.4.10
# Tue, 02 Jun 2026 12:12:28 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 02 Jun 2026 12:13:40 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 12:13:43 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 02 Jun 2026 12:13:45 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 12:13:45 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 12:13:45 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 12:13:45 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 12:13:45 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef700e09ef3cf16d19218622a73899db0a8b42f33bfb19159bb4aa3576d5d21e`  
		Last Modified: Tue, 02 Jun 2026 08:10:42 GMT  
		Size: 18.8 MB (18813426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdb8ec1de5532c097eb41fb0f92ecb54f818737f9cf46998385c39953db727e`  
		Last Modified: Tue, 02 Jun 2026 08:11:40 GMT  
		Size: 42.8 MB (42813392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff385880e28b2054d84e0b5800e2140ec87b662269f8c33bcd8221e0872b169`  
		Last Modified: Tue, 02 Jun 2026 08:11:38 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488cf18986ce3513c802f428d34a1e7fb7ee6c03d85b6e178526bcbc122bd6e3`  
		Last Modified: Tue, 02 Jun 2026 08:11:38 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33f5563bc4dd12556380a3e559556fb88cfe44d0aadda72376aa21cb7784938`  
		Last Modified: Tue, 02 Jun 2026 11:12:33 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb655d0ba9a3e96868a29850c89743ca0cdb1bbd5c76c36e15569c186138a8e`  
		Last Modified: Tue, 02 Jun 2026 11:14:17 GMT  
		Size: 13.8 MB (13831827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c30463ec1bb4e3f75e206871f12591f78f5e5217c358e3799c9c69ea6ba20f7`  
		Last Modified: Tue, 02 Jun 2026 11:14:17 GMT  
		Size: 256.5 KB (256542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af15e78091e72109de7dd175a418eed89175b349517f7e90d762a8aa0d0fb706`  
		Last Modified: Tue, 02 Jun 2026 12:14:30 GMT  
		Size: 269.5 KB (269514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e31bfb989f5171fe0d81f03e3a597a2f95888867968a1f62d497c409276d22d`  
		Last Modified: Tue, 02 Jun 2026 12:14:37 GMT  
		Size: 311.7 MB (311742284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f9f010d38a32ee70a3e1a2420f3678cf67a11733ad6c4ad223b35c0337cfa3`  
		Last Modified: Tue, 02 Jun 2026 12:14:30 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdbf0a6709e1f87fa8d249bbb9d025846fbc006af781c4328f31ddb0451c80d`  
		Last Modified: Tue, 02 Jun 2026 12:14:30 GMT  
		Size: 3.0 KB (3011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d2848fa6c2f8e5f88594c387255ca4daad50e2439baa15162236cc3cbbffd7`  
		Last Modified: Tue, 02 Jun 2026 12:14:32 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:f37a20e07996edbedb981c3209e83bb3f372f1e942ec169f199799aa1a5f2f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4223131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0788a3898cd2932321d4fa23bff9244322493780755bf93b3faf357b5bfcf12f`

```dockerfile
```

-	Layers:
	-	`sha256:8684538b5cc2d6e1e794744b22fc3aa063a1cfcf02eea00414b9f8db775dde64`  
		Last Modified: Tue, 02 Jun 2026 12:14:30 GMT  
		Size: 4.2 MB (4197655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d217c800893f99b60fee07af80703030ede3a5a27badcc7a7ecb1e7b2794118e`  
		Last Modified: Tue, 02 Jun 2026 12:14:30 GMT  
		Size: 25.5 KB (25476 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4` - linux; s390x

```console
$ docker pull geonetwork@sha256:3fb6dcdf8c1eb326fa2fc1cd5a788e85710bc09ba33e66c920e972b87417c42d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.9 MB (414888372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394b71d0074453a02f912f7ed6a3491b11977512891e01e1fd812a2fa7c08765`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:09 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:11 GMT
ADD file:b574b1e436c2db4e4d66f69c75e47a9aebf0da1ad375147eb2c0b7ff76c6ab7e in / 
# Wed, 20 May 2026 01:37:11 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:10:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:10:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:10:07 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:07 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 02 Jun 2026 08:10:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:10:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:10:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:10:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:13:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:13:34 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:13:34 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:13:34 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:13:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:13:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:13:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:13:34 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:13:34 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:13:34 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 10:13:38 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:13:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:13:39 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:13:39 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:13:39 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:10:11 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 11:10:11 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 02 Jun 2026 11:10:11 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 02 Jun 2026 11:10:11 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 11:10:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 02 Jun 2026 11:10:11 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 11:10:11 GMT
ENV GN_VERSION=4.4.10
# Tue, 02 Jun 2026 11:10:11 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 02 Jun 2026 11:12:29 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 11:12:29 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 02 Jun 2026 11:12:29 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 11:12:29 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:12:29 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 11:12:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:12:29 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:c8ebd0a624851e8502e41ee64db2b6a45537554969784d82ebbc91c905cbc2ef`  
		Last Modified: Wed, 20 May 2026 02:16:00 GMT  
		Size: 29.9 MB (29912835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256477a86eb77158be04768dcbdcc986e9666c7a5b72ecdd17f52da12bff8924`  
		Last Modified: Tue, 02 Jun 2026 08:10:28 GMT  
		Size: 17.6 MB (17579962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07875ed48ad40d3c0543f9e9ea54996649cbd5597e8d1caf025c1c702b28a76c`  
		Last Modified: Tue, 02 Jun 2026 08:10:28 GMT  
		Size: 41.4 MB (41358655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99876fbee0a85bc5276f8602f18bfb73f8a7de6d05d8c26412a5ad9543c3cefb`  
		Last Modified: Tue, 02 Jun 2026 08:10:27 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158613312c3340f8af5e729ceedd638f9ce909bb97569d3c1f29818acb14f350`  
		Last Modified: Tue, 02 Jun 2026 08:10:27 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b047d5bb1171f63cbbc0d937f6fc6398fc0addfbd11018eb69ad8776a260d181`  
		Last Modified: Tue, 02 Jun 2026 10:13:53 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d9eb03dc287b7f8872fe628b54a1c10a62b0737238843f5b2be5ebbd6ef6c9`  
		Last Modified: Tue, 02 Jun 2026 10:13:54 GMT  
		Size: 13.8 MB (13804806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db08f77ae0b24a458200e7c5fce15ebe74d7c4a6ba1619d147e1ad151f1c7b39`  
		Last Modified: Tue, 02 Jun 2026 10:13:54 GMT  
		Size: 232.9 KB (232888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f43029b9c1851bfb00de7905064677271138d641836163322ad91decc7a77dc`  
		Last Modified: Tue, 02 Jun 2026 11:13:04 GMT  
		Size: 250.4 KB (250355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d3f5e2af58cac314ceeae7255474ed86aba9a12cbe7fab268e01975d773a5b`  
		Last Modified: Tue, 02 Jun 2026 11:13:10 GMT  
		Size: 311.7 MB (311742306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a8cdabbaeafc4f00d6257baf2931a6763df06d8189ec9c36afda75e37e43ee`  
		Last Modified: Tue, 02 Jun 2026 11:13:04 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7a33ae0ff34c47f7676733829015b39cc2930e6eabcac0e0a66bcedaa0fda1`  
		Last Modified: Tue, 02 Jun 2026 11:13:04 GMT  
		Size: 3.0 KB (3011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e4be60be430f49ea60798957b3c5ce2223c96981d980dc562629836a9bdab0`  
		Last Modified: Tue, 02 Jun 2026 11:13:05 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:c30ed70c67aba79e0d2b4355d7e639ec3515f1cae33676d41c91a5de6d4703cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4221211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e79df7d80504c0fba1c6bb14ca72b3ca841aa6f07df2b16f838d174e2ac128b`

```dockerfile
```

-	Layers:
	-	`sha256:842d02fe1880cdda8c402c29012c564b266f219ca4d36f1c63aa68defd9c9624`  
		Last Modified: Tue, 02 Jun 2026 11:13:04 GMT  
		Size: 4.2 MB (4195781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b80aa58ac825f28b1227878b09a8d61d0a5d5db82c8d97f895181f83cceee59a`  
		Last Modified: Tue, 02 Jun 2026 11:13:04 GMT  
		Size: 25.4 KB (25430 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.2`

```console
$ docker pull geonetwork@sha256:a2bdd1fb91cfd632ddec8c8b6ddb15287a112aa49d4ee31e2e3c2ad4f9b020e2
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
$ docker pull geonetwork@sha256:ad309bcf4669fc76df3dcb4e561b0007f2aafb32c12e1d6a3a321e754be55a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.7 MB (368697720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798d23af069f64c665a49172a8c6eb5376eef05fe03daf8430999c9aa5fb8a5b`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:14:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:14:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:14:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:14:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:14:01 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:14:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8eef3d4a837bb7a9e45d30a7579d84d5b76a4321f4376573311e6bf89e48f9b0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='d5e50cb002600007dbdfac523605d26196607fa5212db0942ef05cdce9fe2892';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='5f0693c6c8ca0eb8df969bb1053b1926b1e7c57a3f90c6f9e8d493395e76a329';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='4f724a0fce1117521a3a3e55ebb0281d56f6c9a066092bc3186ee40d8cd955a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:14:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:14:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:14:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:17:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:17:45 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:17:45 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:17:45 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:17:45 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:17:45 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:17:45 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:17:45 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:17:45 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:17:45 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 10:17:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:17:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:17:50 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:17:50 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:17:50 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:12:45 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 11:12:45 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom         -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Tue, 02 Jun 2026 11:12:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /usr/local/tomcat/webapps/geonetwork # buildkit
# Tue, 02 Jun 2026 11:12:45 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 11:12:45 GMT
ENV GN_VERSION=4.2.15
# Tue, 02 Jun 2026 11:12:45 GMT
ENV GN_DOWNLOAD_MD5=79cd931ac7fc0be044ec1f2dd44f3f96
# Tue, 02 Jun 2026 11:14:02 GMT
RUN set -eux;     cd /usr/local/tomcat/webapps/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 11:14:02 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 11:14:02 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:14:02 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 11:14:02 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:14:02 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0479b3e13d15e71a0f435758770a5bcee00c798f2a9ab9fdfbbb8245d9e6b0`  
		Last Modified: Tue, 02 Jun 2026 08:14:15 GMT  
		Size: 17.0 MB (16984214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17efb44c2b8a615e6468091efd764e243e65d77675a221c02a9df8fe3d7a2f0b`  
		Last Modified: Tue, 02 Jun 2026 08:14:16 GMT  
		Size: 42.3 MB (42337307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29e182498b72a950819bac859beca14639bb03e5124aea6677dbde85b5b357`  
		Last Modified: Tue, 02 Jun 2026 08:14:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11300bc126caeb5bb43b2e98e866b8a6cd6caa4b473af2c47ab51c8730f25c7`  
		Last Modified: Tue, 02 Jun 2026 08:14:14 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691ee125fcab62010d19f9a78ab1171dc4c77f798a30f0b32f76869cc97aa71b`  
		Last Modified: Tue, 02 Jun 2026 10:17:58 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad57802f83e8bf92cd0389884f0b6bc2ab6c2f027e8bec1d757484061be7084c`  
		Last Modified: Tue, 02 Jun 2026 10:17:58 GMT  
		Size: 13.8 MB (13795386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4e8de817f8e31241f0553a172dd18b1b2a474b4a4a38bbee7a305dc155b0f3`  
		Last Modified: Tue, 02 Jun 2026 10:17:58 GMT  
		Size: 225.0 KB (224969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07fc36e15e89e7e537561e4c1cafa22234dda8483e0df4d0e4b3f1179c9c5d2e`  
		Last Modified: Tue, 02 Jun 2026 11:14:22 GMT  
		Size: 239.2 KB (239191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f810babc4af991ceff431dde885450fa9cabf75ba4031e65983f84a059a00d`  
		Last Modified: Tue, 02 Jun 2026 11:14:28 GMT  
		Size: 265.4 MB (265378551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb9dad7d8854284a085ebdac3a549797dcf453e07cb1265e00ba319389f345f`  
		Last Modified: Tue, 02 Jun 2026 11:14:22 GMT  
		Size: 1.5 KB (1504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19bc2f98ff950b5120a64acbfdb729ee8de8871b3fce561e8412825ffad37c08`  
		Last Modified: Tue, 02 Jun 2026 11:14:22 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2` - unknown; unknown

```console
$ docker pull geonetwork@sha256:97cb2aefabf788b6589c21592c9817d9af1cc734e01be04fd768e64538681098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4202486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d167cdecda26e82b283755503f4b5471139dfe76438e34d8bce55936d162e15b`

```dockerfile
```

-	Layers:
	-	`sha256:9d76afa445f75a5689048d94a68f4ff6734a906324604b844b7e4041129a96a3`  
		Last Modified: Tue, 02 Jun 2026 11:14:22 GMT  
		Size: 4.2 MB (4180807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a4d14838b6773dff85dadac622da79ab0f58e602653c7e77e21cc139427c2f9`  
		Last Modified: Tue, 02 Jun 2026 11:14:22 GMT  
		Size: 21.7 KB (21679 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.2` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:8865feeefa26eef93e502a7ad12ff48e7906ece6229a4ccb614792f03e12780b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.5 MB (362478629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb588c41d7c9a0caf822c26876eb3607059640778903c66f961a904795b427bb`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
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
# Tue, 02 Jun 2026 08:11:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8eef3d4a837bb7a9e45d30a7579d84d5b76a4321f4376573311e6bf89e48f9b0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='d5e50cb002600007dbdfac523605d26196607fa5212db0942ef05cdce9fe2892';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='5f0693c6c8ca0eb8df969bb1053b1926b1e7c57a3f90c6f9e8d493395e76a329';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='4f724a0fce1117521a3a3e55ebb0281d56f6c9a066092bc3186ee40d8cd955a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:11:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:11:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:11:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:13:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:13:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:13:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:13:27 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:13:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:13:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:13:27 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:13:27 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:13:27 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:13:28 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 10:13:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:13:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:13:33 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:13:33 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:13:33 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:59:47 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 11:59:47 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom         -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Tue, 02 Jun 2026 11:59:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /usr/local/tomcat/webapps/geonetwork # buildkit
# Tue, 02 Jun 2026 11:59:47 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 11:59:47 GMT
ENV GN_VERSION=4.2.15
# Tue, 02 Jun 2026 11:59:47 GMT
ENV GN_DOWNLOAD_MD5=79cd931ac7fc0be044ec1f2dd44f3f96
# Tue, 02 Jun 2026 11:59:59 GMT
RUN set -eux;     cd /usr/local/tomcat/webapps/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 11:59:59 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 12:00:00 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 12:00:00 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 12:00:00 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 12:00:00 GMT
VOLUME [/catalogue-data]
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
	-	`sha256:45fbb4984a6e1707623e8de675bb6912310f961632c5f296ff2f7c1276486711`  
		Last Modified: Tue, 02 Jun 2026 08:11:30 GMT  
		Size: 39.8 MB (39772162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648e0043f0ec3bdfed16be171cdf133b7fc37c0df172ab1f07f7114e26e4e37f`  
		Last Modified: Tue, 02 Jun 2026 08:11:28 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccce2fa2fc7b9cc58de46128fd7ed1993111ef550a6f415d4043a516aca9cb0`  
		Last Modified: Tue, 02 Jun 2026 08:11:29 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ff9095b787afc1f4ae7f40d406fd883ac0fcf0ea30efc51ed3942fc9b8a32a`  
		Last Modified: Tue, 02 Jun 2026 10:13:42 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b1e072c8e9c98154f57bf7b28213a5fd539170c4f2c324deeca385848afc97`  
		Last Modified: Tue, 02 Jun 2026 10:13:43 GMT  
		Size: 13.7 MB (13728909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6613b3b45a5785cdc439f1d9f7d124c39b014b7b22b5b06568f5bda3d0aae32d`  
		Last Modified: Tue, 02 Jun 2026 10:13:42 GMT  
		Size: 196.7 KB (196702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72b8c0248b93f6716b99f971d471f7b9203fd24954e053aa25110ef937bbc26`  
		Last Modified: Tue, 02 Jun 2026 12:00:22 GMT  
		Size: 226.6 KB (226632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4102d0e154d5457391d22672cbca85bec316a9415e0d39d198945db45b9704f`  
		Last Modified: Tue, 02 Jun 2026 12:00:28 GMT  
		Size: 265.4 MB (265378551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca649f2cad665c148459cf79486c2ccde02db471d30edcdc5e7975c67a249525`  
		Last Modified: Tue, 02 Jun 2026 12:00:23 GMT  
		Size: 1.5 KB (1505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa8b8bae8d1756cd15d88f397fa1faebd70c337266086ac58cfd0b93a021594`  
		Last Modified: Tue, 02 Jun 2026 12:00:24 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2` - unknown; unknown

```console
$ docker pull geonetwork@sha256:da28308a6731e8c19c900d2f0badf3b65796ba132e8ef331429b6f338c0af52d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15bbcfd505cef9e652666e0dc110a45680c877e75b7a4676a652003611ff590f`

```dockerfile
```

-	Layers:
	-	`sha256:eb9cfc9746bbaece03babfdd26fa11d97fb09fdc1ccd84bbc0aa0174ee99faf5`  
		Last Modified: Tue, 02 Jun 2026 12:00:25 GMT  
		Size: 4.2 MB (4186798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1199355f64dd3b487fe09e4321e304cc29ca93be01fceaed29b1bcf43066a9d7`  
		Last Modified: Tue, 02 Jun 2026 12:00:22 GMT  
		Size: 21.8 KB (21756 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.2` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:3b37c9c47200579b0ea94b882ea28a3555d24b75d7252bb60641d06ba2afa640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.8 MB (366834080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:961b70e3d0f63d26e4ff6d48a16343d9ddd8805c976850385e6a876420c1f6c6`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:15:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:15:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:15:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:15:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:15:37 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:15:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8eef3d4a837bb7a9e45d30a7579d84d5b76a4321f4376573311e6bf89e48f9b0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='d5e50cb002600007dbdfac523605d26196607fa5212db0942ef05cdce9fe2892';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='5f0693c6c8ca0eb8df969bb1053b1926b1e7c57a3f90c6f9e8d493395e76a329';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='4f724a0fce1117521a3a3e55ebb0281d56f6c9a066092bc3186ee40d8cd955a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:15:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:15:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:15:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:14:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:14:10 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:14:10 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:14:10 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:14:10 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:14:10 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:14:10 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:14:10 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:14:10 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:14:11 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 10:14:16 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:14:17 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:14:17 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:14:17 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:14:17 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:12:49 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 11:12:49 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom         -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Tue, 02 Jun 2026 11:12:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /usr/local/tomcat/webapps/geonetwork # buildkit
# Tue, 02 Jun 2026 11:12:49 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 11:12:49 GMT
ENV GN_VERSION=4.2.15
# Tue, 02 Jun 2026 11:12:49 GMT
ENV GN_DOWNLOAD_MD5=79cd931ac7fc0be044ec1f2dd44f3f96
# Tue, 02 Jun 2026 11:14:23 GMT
RUN set -eux;     cd /usr/local/tomcat/webapps/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 11:14:23 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 11:14:23 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:14:23 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 11:14:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:14:23 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b329a7430443d5df5aad2e2ad97c50d599c75cce9df284a0633cf6ceb7032724`  
		Last Modified: Tue, 02 Jun 2026 08:15:52 GMT  
		Size: 17.0 MB (16997547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6623f5e1a5902ef1c0cb5a8adcf2e22e984262d948bd64fe4143d84b1177ebff`  
		Last Modified: Tue, 02 Jun 2026 08:15:53 GMT  
		Size: 41.3 MB (41307665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3a0cde34343924fa3e2176c86920ad2dbbfaf33a7474993f578aab65e5db4c`  
		Last Modified: Tue, 02 Jun 2026 08:15:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed8fb59333c63a788842fa58d383cfe8e2cc9b4576ec7ab0b3284bac7011418`  
		Last Modified: Tue, 02 Jun 2026 08:15:51 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cca27d21ea94bcc057e406d9d3704338e86433f0b28581640f1e219c0b2d822`  
		Last Modified: Tue, 02 Jun 2026 10:14:26 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca3abf3793fd2b736cd82f9dff963698eaf85713607bd424b6fb80531bfca13`  
		Last Modified: Tue, 02 Jun 2026 10:14:26 GMT  
		Size: 13.8 MB (13804940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072ca9824b811766dc8db6ab0aee22dac3d1beb49ecee3f9828e86fb74dc74e1`  
		Last Modified: Tue, 02 Jun 2026 10:14:26 GMT  
		Size: 225.3 KB (225345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e104961322b115b8bf1381bd328d06c999fa7140c2f1eaf7631abfc8a8a855a6`  
		Last Modified: Tue, 02 Jun 2026 11:14:46 GMT  
		Size: 238.3 KB (238350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a642755c3f4f3b58cb714b055872c7d104ae26b9ba25a55acb8b404776032d`  
		Last Modified: Tue, 02 Jun 2026 11:14:52 GMT  
		Size: 265.4 MB (265378530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0e75f7162e46188b11ff931d9e11d4b9307df728c2cbc62981efd0eb7309b6`  
		Last Modified: Tue, 02 Jun 2026 11:14:46 GMT  
		Size: 1.5 KB (1504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923b101c3ee4f7bc445b0ba52477a5dda095c8a32423ae89f46178001f40f076`  
		Last Modified: Tue, 02 Jun 2026 11:14:46 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2` - unknown; unknown

```console
$ docker pull geonetwork@sha256:6734be826f253cdb2f456e874ec8ba0e1c2b9392281b5583a49425032c1a8079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4203721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a6c673ee2f004ff9a4f1ff66b6ec7380eee0acf1cebedbff266622e36c6f2b`

```dockerfile
```

-	Layers:
	-	`sha256:f097898aa1876eb894b9d202994e64b0d31ce2d75c015e2bb02a433fc7a8848d`  
		Last Modified: Tue, 02 Jun 2026 11:14:46 GMT  
		Size: 4.2 MB (4181947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62c88e1a483e9888ff80fd2064c2560d4b3bc3919d09f65cd2a94b19ed6ae893`  
		Last Modified: Tue, 02 Jun 2026 11:14:46 GMT  
		Size: 21.8 KB (21774 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.2` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:a42fb64194061d24638afe39428a7832d6141ee8d6131a7fbc713603c1cec027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.6 MB (374610155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2515a676aa78d6cd63e3f1dfe05feba00860b54a379732951a1117bc0e020b60`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:10:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:10:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:10:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:10:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8eef3d4a837bb7a9e45d30a7579d84d5b76a4321f4376573311e6bf89e48f9b0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='d5e50cb002600007dbdfac523605d26196607fa5212db0942ef05cdce9fe2892';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='5f0693c6c8ca0eb8df969bb1053b1926b1e7c57a3f90c6f9e8d493395e76a329';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='4f724a0fce1117521a3a3e55ebb0281d56f6c9a066092bc3186ee40d8cd955a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:10:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:10:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:10:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 11:13:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 11:13:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 11:13:44 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 11:13:46 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 11:13:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 11:13:46 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 11:13:46 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 11:13:46 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 11:13:46 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 11:13:47 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 11:13:55 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 11:13:58 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 11:13:58 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 11:13:58 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 11:13:58 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 12:12:25 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 12:12:25 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom         -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Tue, 02 Jun 2026 12:12:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /usr/local/tomcat/webapps/geonetwork # buildkit
# Tue, 02 Jun 2026 12:12:25 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 12:12:25 GMT
ENV GN_VERSION=4.2.15
# Tue, 02 Jun 2026 12:12:25 GMT
ENV GN_DOWNLOAD_MD5=79cd931ac7fc0be044ec1f2dd44f3f96
# Tue, 02 Jun 2026 12:12:41 GMT
RUN set -eux;     cd /usr/local/tomcat/webapps/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 12:12:41 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 12:12:42 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 12:12:42 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 12:12:42 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 12:12:42 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef700e09ef3cf16d19218622a73899db0a8b42f33bfb19159bb4aa3576d5d21e`  
		Last Modified: Tue, 02 Jun 2026 08:10:42 GMT  
		Size: 18.8 MB (18813426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e4b75c87c150c6f53f06f1566df4335bed19c5f9edd3676a9de1e980e9cd63`  
		Last Modified: Tue, 02 Jun 2026 08:11:01 GMT  
		Size: 41.7 MB (41741610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213a3dcef22845a4990897dca945276e1fc80ee4353a7aa2e6d459fc70920868`  
		Last Modified: Tue, 02 Jun 2026 08:11:00 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c254997e8b0374b9cde75c911358cb185fb313947c0db4337543d4114f3b5a`  
		Last Modified: Tue, 02 Jun 2026 08:11:00 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2927aa1b99c345a3a13fb9843fb7777fdb45154263fd019e2b86ad94cbf9f8`  
		Last Modified: Tue, 02 Jun 2026 11:14:18 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75aa39257d999bb9587e0e6284ad01ddf5e4ccf85638cccbd9ff382d62f688be`  
		Last Modified: Tue, 02 Jun 2026 11:14:18 GMT  
		Size: 13.8 MB (13831231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248b7757f93cdcbb0d13b921fa4f8d2cd46c7938aed6cddf730b25343a30418c`  
		Last Modified: Tue, 02 Jun 2026 11:14:18 GMT  
		Size: 256.5 KB (256509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81f9ebc13ab977ad1cebaacbe3205adf952f8f5d24d841d11b62a241d9d26fe`  
		Last Modified: Tue, 02 Jun 2026 12:13:24 GMT  
		Size: 269.5 KB (269454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af26e918be7b590acb7a0e6f7ed1a2bcac0d290bd8f8080044ae394df478f0ee`  
		Last Modified: Tue, 02 Jun 2026 12:13:31 GMT  
		Size: 265.4 MB (265378531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3951e1c18f6269d460bc82b8d090a59ecee09a09194af85f7efcb307455f3a64`  
		Last Modified: Tue, 02 Jun 2026 12:13:24 GMT  
		Size: 1.5 KB (1502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234a35af9cade8d4596dd1be58379ca9968d75243f32193237eb19e44234ccf6`  
		Last Modified: Tue, 02 Jun 2026 12:13:24 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2` - unknown; unknown

```console
$ docker pull geonetwork@sha256:ed321ca47787c0ba953bbf7c68ac3eba65ad37043c700732719d1adb94f93825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4207277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:812a158d7ecdce9d5a2390f78702ee10a4eff8b7ae6fb80395d79b6ce7ba1363`

```dockerfile
```

-	Layers:
	-	`sha256:37082b510786050d5d065379349af3beb3679f62cf7aacbea6146202a5d70e79`  
		Last Modified: Tue, 02 Jun 2026 12:13:24 GMT  
		Size: 4.2 MB (4185564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:625c463f03e14ae33d0b4761ab0c8bd94ee2febc5e56e0f1a1bede439572eeb3`  
		Last Modified: Tue, 02 Jun 2026 12:13:24 GMT  
		Size: 21.7 KB (21713 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.2.15`

```console
$ docker pull geonetwork@sha256:a2bdd1fb91cfd632ddec8c8b6ddb15287a112aa49d4ee31e2e3c2ad4f9b020e2
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
$ docker pull geonetwork@sha256:ad309bcf4669fc76df3dcb4e561b0007f2aafb32c12e1d6a3a321e754be55a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.7 MB (368697720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798d23af069f64c665a49172a8c6eb5376eef05fe03daf8430999c9aa5fb8a5b`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:14:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:14:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:14:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:14:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:14:01 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:14:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8eef3d4a837bb7a9e45d30a7579d84d5b76a4321f4376573311e6bf89e48f9b0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='d5e50cb002600007dbdfac523605d26196607fa5212db0942ef05cdce9fe2892';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='5f0693c6c8ca0eb8df969bb1053b1926b1e7c57a3f90c6f9e8d493395e76a329';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='4f724a0fce1117521a3a3e55ebb0281d56f6c9a066092bc3186ee40d8cd955a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:14:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:14:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:14:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:17:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:17:45 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:17:45 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:17:45 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:17:45 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:17:45 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:17:45 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:17:45 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:17:45 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:17:45 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 10:17:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:17:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:17:50 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:17:50 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:17:50 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:12:45 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 11:12:45 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom         -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Tue, 02 Jun 2026 11:12:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /usr/local/tomcat/webapps/geonetwork # buildkit
# Tue, 02 Jun 2026 11:12:45 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 11:12:45 GMT
ENV GN_VERSION=4.2.15
# Tue, 02 Jun 2026 11:12:45 GMT
ENV GN_DOWNLOAD_MD5=79cd931ac7fc0be044ec1f2dd44f3f96
# Tue, 02 Jun 2026 11:14:02 GMT
RUN set -eux;     cd /usr/local/tomcat/webapps/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 11:14:02 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 11:14:02 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:14:02 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 11:14:02 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:14:02 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0479b3e13d15e71a0f435758770a5bcee00c798f2a9ab9fdfbbb8245d9e6b0`  
		Last Modified: Tue, 02 Jun 2026 08:14:15 GMT  
		Size: 17.0 MB (16984214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17efb44c2b8a615e6468091efd764e243e65d77675a221c02a9df8fe3d7a2f0b`  
		Last Modified: Tue, 02 Jun 2026 08:14:16 GMT  
		Size: 42.3 MB (42337307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29e182498b72a950819bac859beca14639bb03e5124aea6677dbde85b5b357`  
		Last Modified: Tue, 02 Jun 2026 08:14:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11300bc126caeb5bb43b2e98e866b8a6cd6caa4b473af2c47ab51c8730f25c7`  
		Last Modified: Tue, 02 Jun 2026 08:14:14 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691ee125fcab62010d19f9a78ab1171dc4c77f798a30f0b32f76869cc97aa71b`  
		Last Modified: Tue, 02 Jun 2026 10:17:58 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad57802f83e8bf92cd0389884f0b6bc2ab6c2f027e8bec1d757484061be7084c`  
		Last Modified: Tue, 02 Jun 2026 10:17:58 GMT  
		Size: 13.8 MB (13795386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4e8de817f8e31241f0553a172dd18b1b2a474b4a4a38bbee7a305dc155b0f3`  
		Last Modified: Tue, 02 Jun 2026 10:17:58 GMT  
		Size: 225.0 KB (224969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07fc36e15e89e7e537561e4c1cafa22234dda8483e0df4d0e4b3f1179c9c5d2e`  
		Last Modified: Tue, 02 Jun 2026 11:14:22 GMT  
		Size: 239.2 KB (239191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f810babc4af991ceff431dde885450fa9cabf75ba4031e65983f84a059a00d`  
		Last Modified: Tue, 02 Jun 2026 11:14:28 GMT  
		Size: 265.4 MB (265378551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb9dad7d8854284a085ebdac3a549797dcf453e07cb1265e00ba319389f345f`  
		Last Modified: Tue, 02 Jun 2026 11:14:22 GMT  
		Size: 1.5 KB (1504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19bc2f98ff950b5120a64acbfdb729ee8de8871b3fce561e8412825ffad37c08`  
		Last Modified: Tue, 02 Jun 2026 11:14:22 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2.15` - unknown; unknown

```console
$ docker pull geonetwork@sha256:97cb2aefabf788b6589c21592c9817d9af1cc734e01be04fd768e64538681098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4202486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d167cdecda26e82b283755503f4b5471139dfe76438e34d8bce55936d162e15b`

```dockerfile
```

-	Layers:
	-	`sha256:9d76afa445f75a5689048d94a68f4ff6734a906324604b844b7e4041129a96a3`  
		Last Modified: Tue, 02 Jun 2026 11:14:22 GMT  
		Size: 4.2 MB (4180807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a4d14838b6773dff85dadac622da79ab0f58e602653c7e77e21cc139427c2f9`  
		Last Modified: Tue, 02 Jun 2026 11:14:22 GMT  
		Size: 21.7 KB (21679 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.2.15` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:8865feeefa26eef93e502a7ad12ff48e7906ece6229a4ccb614792f03e12780b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.5 MB (362478629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb588c41d7c9a0caf822c26876eb3607059640778903c66f961a904795b427bb`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
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
# Tue, 02 Jun 2026 08:11:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8eef3d4a837bb7a9e45d30a7579d84d5b76a4321f4376573311e6bf89e48f9b0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='d5e50cb002600007dbdfac523605d26196607fa5212db0942ef05cdce9fe2892';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='5f0693c6c8ca0eb8df969bb1053b1926b1e7c57a3f90c6f9e8d493395e76a329';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='4f724a0fce1117521a3a3e55ebb0281d56f6c9a066092bc3186ee40d8cd955a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:11:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:11:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:11:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:13:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:13:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:13:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:13:27 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:13:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:13:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:13:27 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:13:27 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:13:27 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:13:28 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 10:13:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:13:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:13:33 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:13:33 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:13:33 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:59:47 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 11:59:47 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom         -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Tue, 02 Jun 2026 11:59:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /usr/local/tomcat/webapps/geonetwork # buildkit
# Tue, 02 Jun 2026 11:59:47 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 11:59:47 GMT
ENV GN_VERSION=4.2.15
# Tue, 02 Jun 2026 11:59:47 GMT
ENV GN_DOWNLOAD_MD5=79cd931ac7fc0be044ec1f2dd44f3f96
# Tue, 02 Jun 2026 11:59:59 GMT
RUN set -eux;     cd /usr/local/tomcat/webapps/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 11:59:59 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 12:00:00 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 12:00:00 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 12:00:00 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 12:00:00 GMT
VOLUME [/catalogue-data]
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
	-	`sha256:45fbb4984a6e1707623e8de675bb6912310f961632c5f296ff2f7c1276486711`  
		Last Modified: Tue, 02 Jun 2026 08:11:30 GMT  
		Size: 39.8 MB (39772162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648e0043f0ec3bdfed16be171cdf133b7fc37c0df172ab1f07f7114e26e4e37f`  
		Last Modified: Tue, 02 Jun 2026 08:11:28 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccce2fa2fc7b9cc58de46128fd7ed1993111ef550a6f415d4043a516aca9cb0`  
		Last Modified: Tue, 02 Jun 2026 08:11:29 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ff9095b787afc1f4ae7f40d406fd883ac0fcf0ea30efc51ed3942fc9b8a32a`  
		Last Modified: Tue, 02 Jun 2026 10:13:42 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b1e072c8e9c98154f57bf7b28213a5fd539170c4f2c324deeca385848afc97`  
		Last Modified: Tue, 02 Jun 2026 10:13:43 GMT  
		Size: 13.7 MB (13728909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6613b3b45a5785cdc439f1d9f7d124c39b014b7b22b5b06568f5bda3d0aae32d`  
		Last Modified: Tue, 02 Jun 2026 10:13:42 GMT  
		Size: 196.7 KB (196702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72b8c0248b93f6716b99f971d471f7b9203fd24954e053aa25110ef937bbc26`  
		Last Modified: Tue, 02 Jun 2026 12:00:22 GMT  
		Size: 226.6 KB (226632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4102d0e154d5457391d22672cbca85bec316a9415e0d39d198945db45b9704f`  
		Last Modified: Tue, 02 Jun 2026 12:00:28 GMT  
		Size: 265.4 MB (265378551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca649f2cad665c148459cf79486c2ccde02db471d30edcdc5e7975c67a249525`  
		Last Modified: Tue, 02 Jun 2026 12:00:23 GMT  
		Size: 1.5 KB (1505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa8b8bae8d1756cd15d88f397fa1faebd70c337266086ac58cfd0b93a021594`  
		Last Modified: Tue, 02 Jun 2026 12:00:24 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2.15` - unknown; unknown

```console
$ docker pull geonetwork@sha256:da28308a6731e8c19c900d2f0badf3b65796ba132e8ef331429b6f338c0af52d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4208554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15bbcfd505cef9e652666e0dc110a45680c877e75b7a4676a652003611ff590f`

```dockerfile
```

-	Layers:
	-	`sha256:eb9cfc9746bbaece03babfdd26fa11d97fb09fdc1ccd84bbc0aa0174ee99faf5`  
		Last Modified: Tue, 02 Jun 2026 12:00:25 GMT  
		Size: 4.2 MB (4186798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1199355f64dd3b487fe09e4321e304cc29ca93be01fceaed29b1bcf43066a9d7`  
		Last Modified: Tue, 02 Jun 2026 12:00:22 GMT  
		Size: 21.8 KB (21756 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.2.15` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:3b37c9c47200579b0ea94b882ea28a3555d24b75d7252bb60641d06ba2afa640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.8 MB (366834080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:961b70e3d0f63d26e4ff6d48a16343d9ddd8805c976850385e6a876420c1f6c6`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:15:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:15:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:15:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:15:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:15:37 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:15:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8eef3d4a837bb7a9e45d30a7579d84d5b76a4321f4376573311e6bf89e48f9b0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='d5e50cb002600007dbdfac523605d26196607fa5212db0942ef05cdce9fe2892';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='5f0693c6c8ca0eb8df969bb1053b1926b1e7c57a3f90c6f9e8d493395e76a329';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='4f724a0fce1117521a3a3e55ebb0281d56f6c9a066092bc3186ee40d8cd955a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:15:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:15:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:15:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:14:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:14:10 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:14:10 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:14:10 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:14:10 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:14:10 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:14:10 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:14:10 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:14:10 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:14:11 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 10:14:16 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:14:17 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:14:17 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:14:17 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:14:17 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:12:49 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 11:12:49 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom         -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Tue, 02 Jun 2026 11:12:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /usr/local/tomcat/webapps/geonetwork # buildkit
# Tue, 02 Jun 2026 11:12:49 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 11:12:49 GMT
ENV GN_VERSION=4.2.15
# Tue, 02 Jun 2026 11:12:49 GMT
ENV GN_DOWNLOAD_MD5=79cd931ac7fc0be044ec1f2dd44f3f96
# Tue, 02 Jun 2026 11:14:23 GMT
RUN set -eux;     cd /usr/local/tomcat/webapps/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 11:14:23 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 11:14:23 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:14:23 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 11:14:23 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:14:23 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b329a7430443d5df5aad2e2ad97c50d599c75cce9df284a0633cf6ceb7032724`  
		Last Modified: Tue, 02 Jun 2026 08:15:52 GMT  
		Size: 17.0 MB (16997547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6623f5e1a5902ef1c0cb5a8adcf2e22e984262d948bd64fe4143d84b1177ebff`  
		Last Modified: Tue, 02 Jun 2026 08:15:53 GMT  
		Size: 41.3 MB (41307665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3a0cde34343924fa3e2176c86920ad2dbbfaf33a7474993f578aab65e5db4c`  
		Last Modified: Tue, 02 Jun 2026 08:15:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed8fb59333c63a788842fa58d383cfe8e2cc9b4576ec7ab0b3284bac7011418`  
		Last Modified: Tue, 02 Jun 2026 08:15:51 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cca27d21ea94bcc057e406d9d3704338e86433f0b28581640f1e219c0b2d822`  
		Last Modified: Tue, 02 Jun 2026 10:14:26 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca3abf3793fd2b736cd82f9dff963698eaf85713607bd424b6fb80531bfca13`  
		Last Modified: Tue, 02 Jun 2026 10:14:26 GMT  
		Size: 13.8 MB (13804940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072ca9824b811766dc8db6ab0aee22dac3d1beb49ecee3f9828e86fb74dc74e1`  
		Last Modified: Tue, 02 Jun 2026 10:14:26 GMT  
		Size: 225.3 KB (225345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e104961322b115b8bf1381bd328d06c999fa7140c2f1eaf7631abfc8a8a855a6`  
		Last Modified: Tue, 02 Jun 2026 11:14:46 GMT  
		Size: 238.3 KB (238350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a642755c3f4f3b58cb714b055872c7d104ae26b9ba25a55acb8b404776032d`  
		Last Modified: Tue, 02 Jun 2026 11:14:52 GMT  
		Size: 265.4 MB (265378530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0e75f7162e46188b11ff931d9e11d4b9307df728c2cbc62981efd0eb7309b6`  
		Last Modified: Tue, 02 Jun 2026 11:14:46 GMT  
		Size: 1.5 KB (1504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923b101c3ee4f7bc445b0ba52477a5dda095c8a32423ae89f46178001f40f076`  
		Last Modified: Tue, 02 Jun 2026 11:14:46 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2.15` - unknown; unknown

```console
$ docker pull geonetwork@sha256:6734be826f253cdb2f456e874ec8ba0e1c2b9392281b5583a49425032c1a8079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4203721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a6c673ee2f004ff9a4f1ff66b6ec7380eee0acf1cebedbff266622e36c6f2b`

```dockerfile
```

-	Layers:
	-	`sha256:f097898aa1876eb894b9d202994e64b0d31ce2d75c015e2bb02a433fc7a8848d`  
		Last Modified: Tue, 02 Jun 2026 11:14:46 GMT  
		Size: 4.2 MB (4181947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62c88e1a483e9888ff80fd2064c2560d4b3bc3919d09f65cd2a94b19ed6ae893`  
		Last Modified: Tue, 02 Jun 2026 11:14:46 GMT  
		Size: 21.8 KB (21774 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.2.15` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:a42fb64194061d24638afe39428a7832d6141ee8d6131a7fbc713603c1cec027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.6 MB (374610155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2515a676aa78d6cd63e3f1dfe05feba00860b54a379732951a1117bc0e020b60`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:10:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:10:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:10:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 08:10:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8eef3d4a837bb7a9e45d30a7579d84d5b76a4321f4376573311e6bf89e48f9b0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_linux_hotspot_8u492b09.tar.gz';          ;;        arm64)          ESUM='d5e50cb002600007dbdfac523605d26196607fa5212db0942ef05cdce9fe2892';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        armhf)          ESUM='5f0693c6c8ca0eb8df969bb1053b1926b1e7c57a3f90c6f9e8d493395e76a329';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_arm_linux_hotspot_8u492b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='4f724a0fce1117521a3a3e55ebb0281d56f6c9a066092bc3186ee40d8cd955a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 02 Jun 2026 08:10:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:10:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:10:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 11:13:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 11:13:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 11:13:44 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 11:13:46 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 11:13:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 11:13:46 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 11:13:46 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 11:13:46 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 11:13:46 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 11:13:47 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 11:13:55 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 11:13:58 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 11:13:58 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 11:13:58 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 11:13:58 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 12:12:25 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 12:12:25 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom         -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC         -Dgeonetwork.resources.dir=/catalogue-data/resources         -Dgeonetwork.data.dir=/catalogue-data         -Dgeonetwork.codeList.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/codelist         -Dgeonetwork.schema.dir=/usr/local/tomcat/webapps/geonetwork/WEB-INF/data/config/schema_plugins
# Tue, 02 Jun 2026 12:12:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /usr/local/tomcat/webapps/geonetwork # buildkit
# Tue, 02 Jun 2026 12:12:25 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 12:12:25 GMT
ENV GN_VERSION=4.2.15
# Tue, 02 Jun 2026 12:12:25 GMT
ENV GN_DOWNLOAD_MD5=79cd931ac7fc0be044ec1f2dd44f3f96
# Tue, 02 Jun 2026 12:12:41 GMT
RUN set -eux;     cd /usr/local/tomcat/webapps/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 12:12:41 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 12:12:42 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 12:12:42 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 12:12:42 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 12:12:42 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef700e09ef3cf16d19218622a73899db0a8b42f33bfb19159bb4aa3576d5d21e`  
		Last Modified: Tue, 02 Jun 2026 08:10:42 GMT  
		Size: 18.8 MB (18813426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e4b75c87c150c6f53f06f1566df4335bed19c5f9edd3676a9de1e980e9cd63`  
		Last Modified: Tue, 02 Jun 2026 08:11:01 GMT  
		Size: 41.7 MB (41741610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213a3dcef22845a4990897dca945276e1fc80ee4353a7aa2e6d459fc70920868`  
		Last Modified: Tue, 02 Jun 2026 08:11:00 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c254997e8b0374b9cde75c911358cb185fb313947c0db4337543d4114f3b5a`  
		Last Modified: Tue, 02 Jun 2026 08:11:00 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2927aa1b99c345a3a13fb9843fb7777fdb45154263fd019e2b86ad94cbf9f8`  
		Last Modified: Tue, 02 Jun 2026 11:14:18 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75aa39257d999bb9587e0e6284ad01ddf5e4ccf85638cccbd9ff382d62f688be`  
		Last Modified: Tue, 02 Jun 2026 11:14:18 GMT  
		Size: 13.8 MB (13831231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248b7757f93cdcbb0d13b921fa4f8d2cd46c7938aed6cddf730b25343a30418c`  
		Last Modified: Tue, 02 Jun 2026 11:14:18 GMT  
		Size: 256.5 KB (256509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81f9ebc13ab977ad1cebaacbe3205adf952f8f5d24d841d11b62a241d9d26fe`  
		Last Modified: Tue, 02 Jun 2026 12:13:24 GMT  
		Size: 269.5 KB (269454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af26e918be7b590acb7a0e6f7ed1a2bcac0d290bd8f8080044ae394df478f0ee`  
		Last Modified: Tue, 02 Jun 2026 12:13:31 GMT  
		Size: 265.4 MB (265378531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3951e1c18f6269d460bc82b8d090a59ecee09a09194af85f7efcb307455f3a64`  
		Last Modified: Tue, 02 Jun 2026 12:13:24 GMT  
		Size: 1.5 KB (1502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234a35af9cade8d4596dd1be58379ca9968d75243f32193237eb19e44234ccf6`  
		Last Modified: Tue, 02 Jun 2026 12:13:24 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2.15` - unknown; unknown

```console
$ docker pull geonetwork@sha256:ed321ca47787c0ba953bbf7c68ac3eba65ad37043c700732719d1adb94f93825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4207277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:812a158d7ecdce9d5a2390f78702ee10a4eff8b7ae6fb80395d79b6ce7ba1363`

```dockerfile
```

-	Layers:
	-	`sha256:37082b510786050d5d065379349af3beb3679f62cf7aacbea6146202a5d70e79`  
		Last Modified: Tue, 02 Jun 2026 12:13:24 GMT  
		Size: 4.2 MB (4185564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:625c463f03e14ae33d0b4761ab0c8bd94ee2febc5e56e0f1a1bede439572eeb3`  
		Last Modified: Tue, 02 Jun 2026 12:13:24 GMT  
		Size: 21.7 KB (21713 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.4`

```console
$ docker pull geonetwork@sha256:5f67da2cc43bd7718e2e0676f25d3b91db7d97c2187ded37db1d83b3e1c44427
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
$ docker pull geonetwork@sha256:1570ebc4c8d8cae30c2ee5340843640ffa9879405b5716b9063589070972e6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.1 MB (420070202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dc43286c71acc45160e65bec64543ed1d40274e354fdb64655bda3dede6b29`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:14:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:14:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:14:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:14:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:14:19 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 02 Jun 2026 08:14:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:14:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:14:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:14:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:17:46 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:17:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:17:46 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:17:46 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:17:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:17:46 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:17:46 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:17:46 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:17:46 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:17:46 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 10:17:50 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:17:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:17:51 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:17:51 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:17:51 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:13:09 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 11:13:09 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 02 Jun 2026 11:13:09 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 02 Jun 2026 11:13:09 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 11:13:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 02 Jun 2026 11:13:09 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 11:13:09 GMT
ENV GN_VERSION=4.4.10
# Tue, 02 Jun 2026 11:13:09 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 02 Jun 2026 11:13:21 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 11:13:21 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 02 Jun 2026 11:13:21 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 11:13:21 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:13:21 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 11:13:21 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:13:21 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9e436cd644d0619bdfd1c8d1dce9e824e836e6102bf4a4c26919785ffe2a7c`  
		Last Modified: Tue, 02 Jun 2026 08:14:35 GMT  
		Size: 17.0 MB (16984112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abe231f9a275556a3c449f9746da9863dbbea3001e50afdbf5209553a0533c2`  
		Last Modified: Tue, 02 Jun 2026 08:14:36 GMT  
		Size: 47.3 MB (47344216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f689e05e256f3387912f6eab83ac21ffe596b6aa357a513c261ad13b21d283`  
		Last Modified: Tue, 02 Jun 2026 08:14:34 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5e34d12e53e20283e3eaeab1e665797d41b9b9ca6c3b47599a697790b15acb`  
		Last Modified: Tue, 02 Jun 2026 08:14:34 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b12c99159fc66956c2d9b5f3ac562fb93293b4f0ac571b0e57c73f17e7bfdbc`  
		Last Modified: Tue, 02 Jun 2026 10:17:59 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328a1e80cac330b8fd4cbe150711db3a5abd2333338c94c45dae5cff116eb841`  
		Last Modified: Tue, 02 Jun 2026 10:17:59 GMT  
		Size: 13.8 MB (13796163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b0b2346d28acc1f3441f42c9a41c27c0d9217183a6cb1662035858276ab3af`  
		Last Modified: Tue, 02 Jun 2026 10:17:59 GMT  
		Size: 224.8 KB (224833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631e6695a5c2e9c5433e05ca7109c40ad41585acc223c064807c7d7bdd6dc8e1`  
		Last Modified: Tue, 02 Jun 2026 11:13:44 GMT  
		Size: 239.2 KB (239211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34f6d9f937ddbf71a730e33bf0de46f6b661b62fd745421480f32221210968a`  
		Last Modified: Tue, 02 Jun 2026 11:13:51 GMT  
		Size: 311.7 MB (311742293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfdf3d2859f9d8424ea7bf91e8997d328dc41984fb42867f418064ea2487f22`  
		Last Modified: Tue, 02 Jun 2026 11:13:44 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904fe9ae87726911c9251a8b694e0db164afe48ddfd76b876cc5c751d0cf0be2`  
		Last Modified: Tue, 02 Jun 2026 11:13:44 GMT  
		Size: 3.0 KB (3013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ac3509e51ad06df68519ef10a212abe04b754f8f9bf2e785ba89fdea8a64ab`  
		Last Modified: Tue, 02 Jun 2026 11:13:45 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:bcd3bd1d3e14dbe7402887856277c2dc5324cef64b143b11244a603ca61bfe7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4219006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be50188d7bae4be76a3085cd1218ce37da8710d7eb25627a8f2e4a41b377483e`

```dockerfile
```

-	Layers:
	-	`sha256:955e2a3dcc94ad31b3cf1bdf1bc505d56756b274f8c6dab096adf4fa38ed0b17`  
		Last Modified: Tue, 02 Jun 2026 11:13:44 GMT  
		Size: 4.2 MB (4193576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:824708be85a603e7d03834925cdc488d2492aaf2676ef0436d0b4d6079c3d583`  
		Last Modified: Tue, 02 Jun 2026 11:13:44 GMT  
		Size: 25.4 KB (25430 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:48672a66b22db2e0a6a080edc7fcda4f72b51018cb534aacbfb506fe2e48ac41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.5 MB (414526279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997ae873464f8038256b1e1f8c38043d2d0f858d9e888aa62e1d70d763efabc4`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
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
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 02 Jun 2026 08:12:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:12:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:12:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:12:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:13:26 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:13:26 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:13:26 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:13:26 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:13:26 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:13:26 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:13:26 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:13:26 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:13:26 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:13:27 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 10:13:32 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:13:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:13:33 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:13:33 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:13:33 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:11:38 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 11:11:38 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 02 Jun 2026 11:11:38 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 02 Jun 2026 11:11:38 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 11:11:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 02 Jun 2026 11:11:38 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 11:11:38 GMT
ENV GN_VERSION=4.4.10
# Tue, 02 Jun 2026 11:11:38 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 02 Jun 2026 11:13:27 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 11:13:27 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 02 Jun 2026 11:13:27 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 11:13:27 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:13:27 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 11:13:27 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:13:27 GMT
VOLUME [/catalogue-data]
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
	-	`sha256:a763aa8647dee2704dbccddf100af5e050e07be63b2091352322da501dfbaeed`  
		Last Modified: Tue, 02 Jun 2026 08:13:03 GMT  
		Size: 45.5 MB (45454025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce71c5b0eb84b76e19875d5a01ece3a180b99ea3e5d3b749c53692b2767e3c00`  
		Last Modified: Tue, 02 Jun 2026 08:13:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a437059cd3dbdb7d8a53d4964b178c30acdb400c5d84e6e28913d7ff76de3c1`  
		Last Modified: Tue, 02 Jun 2026 08:13:01 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273a3f3cdc146550c02e7329c464a66778b96b407606914d90d5859e7f59582d`  
		Last Modified: Tue, 02 Jun 2026 10:13:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d00a83829a70306b914f1f06e4d228eee0528f75ea07c900f77b513fd6d2687`  
		Last Modified: Tue, 02 Jun 2026 10:13:41 GMT  
		Size: 13.7 MB (13730088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8591662de7c4b4f561acb1dbb592e6eaa7f8d2a4121831ac8d3ff3eca4e6b449`  
		Last Modified: Tue, 02 Jun 2026 10:13:41 GMT  
		Size: 196.5 KB (196506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6721ba9b0a083d0801ac0c20f69e0dd674e9b3eb8a07b31f81de134d1810189c`  
		Last Modified: Tue, 02 Jun 2026 11:13:52 GMT  
		Size: 226.4 KB (226408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f28a16af03b29f9c6bb827df7b6ccaab84a679b76483cf6b774c3a2226007b`  
		Last Modified: Tue, 02 Jun 2026 11:13:58 GMT  
		Size: 311.7 MB (311742307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02adf392821be303350cc5ba7f6cb7d9bdc39c212a32b10b5f563392b70bffd`  
		Last Modified: Tue, 02 Jun 2026 11:13:52 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08109080f302519f9109ebb24ba352f31ec448283e66b08d714627ea7e32e783`  
		Last Modified: Tue, 02 Jun 2026 11:13:52 GMT  
		Size: 3.0 KB (3016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeb7723f52d6bd1f9743c10628d1730f1718c8aa598c4d03ab818c380589c23`  
		Last Modified: Tue, 02 Jun 2026 11:13:53 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:36090bc31adc9322f761df9782ad44aad6ddd259ab0d5f66e98adb9d85bdf44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4222701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36846105faa0e4a1f4207d1101a38583582d34b13a26de9574ccc4f0359ac03e`

```dockerfile
```

-	Layers:
	-	`sha256:d9f76d562b08f9c8c41540a0ac0426d5e1cdf86523a76b88bc663b7b5fae912e`  
		Last Modified: Tue, 02 Jun 2026 11:13:52 GMT  
		Size: 4.2 MB (4197179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e01fe87e0d3cf12ec30a888f05820dd55440e10252a36e8c2280c7be846736a`  
		Last Modified: Tue, 02 Jun 2026 11:13:51 GMT  
		Size: 25.5 KB (25522 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:9676808067bb17308a14f06f9e857a05af791997b1b76ae7407bfc4ec3578381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.6 MB (417551650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9c1ce65405f2b22e9a97cd1a6842dadcb4706ff1dbad48fde134b9705543b3`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:15:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:15:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:15:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:15:43 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:15:43 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 02 Jun 2026 08:15:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:15:48 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:15:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:15:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:14:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:14:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:14:03 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:14:03 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:14:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:14:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:14:03 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:14:03 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:14:03 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:14:03 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 10:14:08 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:14:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:14:09 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:14:09 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:14:09 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:13:04 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 11:13:04 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 02 Jun 2026 11:13:04 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 02 Jun 2026 11:13:04 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 11:13:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 02 Jun 2026 11:13:04 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 11:13:04 GMT
ENV GN_VERSION=4.4.10
# Tue, 02 Jun 2026 11:13:04 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 02 Jun 2026 11:13:18 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 11:13:18 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 02 Jun 2026 11:13:18 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 11:13:18 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:13:18 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 11:13:18 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:13:18 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77acf8a2fd2a14aa128b125e15d261df4fd4f487386a6ac710a99968b2ed8d60`  
		Last Modified: Tue, 02 Jun 2026 08:16:00 GMT  
		Size: 17.0 MB (16997549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e07080645b5dbe3f11ea303d9cef4b4ac977a37efb6d74f92b3f69ded5806d`  
		Last Modified: Tue, 02 Jun 2026 08:16:01 GMT  
		Size: 45.7 MB (45659671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a181db84648310ad9c72731e407b7e06733928683e3ff6e8dfd6c50535d2f74f`  
		Last Modified: Tue, 02 Jun 2026 08:15:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ef243a4acfe4609f9532dec8a35af094f6898a9fba63b1f0a1a16ec457df5c`  
		Last Modified: Tue, 02 Jun 2026 08:15:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7790686ff36b34814640358cae09b83fb719b6ad854894f2582a7d261fd7b5c2`  
		Last Modified: Tue, 02 Jun 2026 10:14:17 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967c3d5f7725f795501d2f608262ba31047ef094db7f89fffb0054f9c2a4ddaf`  
		Last Modified: Tue, 02 Jun 2026 10:14:18 GMT  
		Size: 13.8 MB (13805557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135ba0c297a795416529870fe8e06d5e61ea32c4b717ec3e761809c8be3e7fba`  
		Last Modified: Tue, 02 Jun 2026 10:14:17 GMT  
		Size: 225.1 KB (225133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e42b762b4b42d36927c23c79fa2b1fbb493bd5f5f947ff2030fc89582c79e8`  
		Last Modified: Tue, 02 Jun 2026 11:13:42 GMT  
		Size: 238.4 KB (238420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dad06061b9135ac54d43e6166ed5b64a1ed261a151357cc2e40a155dbee617`  
		Last Modified: Tue, 02 Jun 2026 11:13:50 GMT  
		Size: 311.7 MB (311742343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ad0e9b31522ca2d2867af09ff0295a27534d6b944e82444403d676ec991869`  
		Last Modified: Tue, 02 Jun 2026 11:13:42 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e02ee9d670430ec4fc79c123f360dd0a2cdc68537b9386955c8e42f0589323`  
		Last Modified: Tue, 02 Jun 2026 11:13:42 GMT  
		Size: 3.0 KB (3014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bd61185368c5cbc16f5753636d8291fcc8e628eb8ea151e1f3645ddc3f5d46`  
		Last Modified: Tue, 02 Jun 2026 11:13:43 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:17b5950d45a383497c3d42691f7f753f0ba140f028ba66a162df54395d1d1056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4220215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5573828472fd131d82084b2e3968931d3b6fdd186e8b9e130017822a1017be67`

```dockerfile
```

-	Layers:
	-	`sha256:329a5eb203f3614de3aecd40c53e9d8889938303b5a5709ee0cde9541303a4e0`  
		Last Modified: Tue, 02 Jun 2026 11:13:42 GMT  
		Size: 4.2 MB (4194666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a2308185e4ec060c856aab2a590654a1b72a4fb390b9518548e2fa92eebc9d0`  
		Last Modified: Tue, 02 Jun 2026 11:13:42 GMT  
		Size: 25.5 KB (25549 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:9457b2ebac2d8732e4077e1a44c8a96d3d07fcdfc85c4c81a6a53527db0e9784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.0 MB (422047651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0b120f44c545db492728f2787537047bd7c139c2731d78e73a2581d6c0ce0f`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:10:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:10:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:10:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 02 Jun 2026 08:11:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:11:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:11:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:11:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 11:12:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 11:12:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 11:12:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 11:12:06 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 11:12:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 11:12:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 11:12:06 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 11:12:06 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 11:12:06 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 11:13:46 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 11:13:54 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 11:13:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 11:13:56 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 11:13:56 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 11:13:56 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 12:12:28 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 12:12:28 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 02 Jun 2026 12:12:28 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 02 Jun 2026 12:12:28 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 12:12:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 02 Jun 2026 12:12:28 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 12:12:28 GMT
ENV GN_VERSION=4.4.10
# Tue, 02 Jun 2026 12:12:28 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 02 Jun 2026 12:13:40 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 12:13:43 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 02 Jun 2026 12:13:45 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 12:13:45 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 12:13:45 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 12:13:45 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 12:13:45 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef700e09ef3cf16d19218622a73899db0a8b42f33bfb19159bb4aa3576d5d21e`  
		Last Modified: Tue, 02 Jun 2026 08:10:42 GMT  
		Size: 18.8 MB (18813426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdb8ec1de5532c097eb41fb0f92ecb54f818737f9cf46998385c39953db727e`  
		Last Modified: Tue, 02 Jun 2026 08:11:40 GMT  
		Size: 42.8 MB (42813392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff385880e28b2054d84e0b5800e2140ec87b662269f8c33bcd8221e0872b169`  
		Last Modified: Tue, 02 Jun 2026 08:11:38 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488cf18986ce3513c802f428d34a1e7fb7ee6c03d85b6e178526bcbc122bd6e3`  
		Last Modified: Tue, 02 Jun 2026 08:11:38 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33f5563bc4dd12556380a3e559556fb88cfe44d0aadda72376aa21cb7784938`  
		Last Modified: Tue, 02 Jun 2026 11:12:33 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb655d0ba9a3e96868a29850c89743ca0cdb1bbd5c76c36e15569c186138a8e`  
		Last Modified: Tue, 02 Jun 2026 11:14:17 GMT  
		Size: 13.8 MB (13831827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c30463ec1bb4e3f75e206871f12591f78f5e5217c358e3799c9c69ea6ba20f7`  
		Last Modified: Tue, 02 Jun 2026 11:14:17 GMT  
		Size: 256.5 KB (256542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af15e78091e72109de7dd175a418eed89175b349517f7e90d762a8aa0d0fb706`  
		Last Modified: Tue, 02 Jun 2026 12:14:30 GMT  
		Size: 269.5 KB (269514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e31bfb989f5171fe0d81f03e3a597a2f95888867968a1f62d497c409276d22d`  
		Last Modified: Tue, 02 Jun 2026 12:14:37 GMT  
		Size: 311.7 MB (311742284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f9f010d38a32ee70a3e1a2420f3678cf67a11733ad6c4ad223b35c0337cfa3`  
		Last Modified: Tue, 02 Jun 2026 12:14:30 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdbf0a6709e1f87fa8d249bbb9d025846fbc006af781c4328f31ddb0451c80d`  
		Last Modified: Tue, 02 Jun 2026 12:14:30 GMT  
		Size: 3.0 KB (3011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d2848fa6c2f8e5f88594c387255ca4daad50e2439baa15162236cc3cbbffd7`  
		Last Modified: Tue, 02 Jun 2026 12:14:32 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:f37a20e07996edbedb981c3209e83bb3f372f1e942ec169f199799aa1a5f2f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4223131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0788a3898cd2932321d4fa23bff9244322493780755bf93b3faf357b5bfcf12f`

```dockerfile
```

-	Layers:
	-	`sha256:8684538b5cc2d6e1e794744b22fc3aa063a1cfcf02eea00414b9f8db775dde64`  
		Last Modified: Tue, 02 Jun 2026 12:14:30 GMT  
		Size: 4.2 MB (4197655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d217c800893f99b60fee07af80703030ede3a5a27badcc7a7ecb1e7b2794118e`  
		Last Modified: Tue, 02 Jun 2026 12:14:30 GMT  
		Size: 25.5 KB (25476 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4` - linux; s390x

```console
$ docker pull geonetwork@sha256:3fb6dcdf8c1eb326fa2fc1cd5a788e85710bc09ba33e66c920e972b87417c42d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.9 MB (414888372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394b71d0074453a02f912f7ed6a3491b11977512891e01e1fd812a2fa7c08765`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:09 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:11 GMT
ADD file:b574b1e436c2db4e4d66f69c75e47a9aebf0da1ad375147eb2c0b7ff76c6ab7e in / 
# Wed, 20 May 2026 01:37:11 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:10:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:10:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:10:07 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:07 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 02 Jun 2026 08:10:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:10:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:10:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:10:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:13:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:13:34 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:13:34 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:13:34 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:13:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:13:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:13:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:13:34 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:13:34 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:13:34 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 10:13:38 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:13:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:13:39 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:13:39 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:13:39 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:10:11 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 11:10:11 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 02 Jun 2026 11:10:11 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 02 Jun 2026 11:10:11 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 11:10:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 02 Jun 2026 11:10:11 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 11:10:11 GMT
ENV GN_VERSION=4.4.10
# Tue, 02 Jun 2026 11:10:11 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 02 Jun 2026 11:12:29 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 11:12:29 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 02 Jun 2026 11:12:29 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 11:12:29 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:12:29 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 11:12:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:12:29 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:c8ebd0a624851e8502e41ee64db2b6a45537554969784d82ebbc91c905cbc2ef`  
		Last Modified: Wed, 20 May 2026 02:16:00 GMT  
		Size: 29.9 MB (29912835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256477a86eb77158be04768dcbdcc986e9666c7a5b72ecdd17f52da12bff8924`  
		Last Modified: Tue, 02 Jun 2026 08:10:28 GMT  
		Size: 17.6 MB (17579962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07875ed48ad40d3c0543f9e9ea54996649cbd5597e8d1caf025c1c702b28a76c`  
		Last Modified: Tue, 02 Jun 2026 08:10:28 GMT  
		Size: 41.4 MB (41358655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99876fbee0a85bc5276f8602f18bfb73f8a7de6d05d8c26412a5ad9543c3cefb`  
		Last Modified: Tue, 02 Jun 2026 08:10:27 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158613312c3340f8af5e729ceedd638f9ce909bb97569d3c1f29818acb14f350`  
		Last Modified: Tue, 02 Jun 2026 08:10:27 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b047d5bb1171f63cbbc0d937f6fc6398fc0addfbd11018eb69ad8776a260d181`  
		Last Modified: Tue, 02 Jun 2026 10:13:53 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d9eb03dc287b7f8872fe628b54a1c10a62b0737238843f5b2be5ebbd6ef6c9`  
		Last Modified: Tue, 02 Jun 2026 10:13:54 GMT  
		Size: 13.8 MB (13804806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db08f77ae0b24a458200e7c5fce15ebe74d7c4a6ba1619d147e1ad151f1c7b39`  
		Last Modified: Tue, 02 Jun 2026 10:13:54 GMT  
		Size: 232.9 KB (232888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f43029b9c1851bfb00de7905064677271138d641836163322ad91decc7a77dc`  
		Last Modified: Tue, 02 Jun 2026 11:13:04 GMT  
		Size: 250.4 KB (250355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d3f5e2af58cac314ceeae7255474ed86aba9a12cbe7fab268e01975d773a5b`  
		Last Modified: Tue, 02 Jun 2026 11:13:10 GMT  
		Size: 311.7 MB (311742306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a8cdabbaeafc4f00d6257baf2931a6763df06d8189ec9c36afda75e37e43ee`  
		Last Modified: Tue, 02 Jun 2026 11:13:04 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7a33ae0ff34c47f7676733829015b39cc2930e6eabcac0e0a66bcedaa0fda1`  
		Last Modified: Tue, 02 Jun 2026 11:13:04 GMT  
		Size: 3.0 KB (3011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e4be60be430f49ea60798957b3c5ce2223c96981d980dc562629836a9bdab0`  
		Last Modified: Tue, 02 Jun 2026 11:13:05 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:c30ed70c67aba79e0d2b4355d7e639ec3515f1cae33676d41c91a5de6d4703cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4221211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e79df7d80504c0fba1c6bb14ca72b3ca841aa6f07df2b16f838d174e2ac128b`

```dockerfile
```

-	Layers:
	-	`sha256:842d02fe1880cdda8c402c29012c564b266f219ca4d36f1c63aa68defd9c9624`  
		Last Modified: Tue, 02 Jun 2026 11:13:04 GMT  
		Size: 4.2 MB (4195781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b80aa58ac825f28b1227878b09a8d61d0a5d5db82c8d97f895181f83cceee59a`  
		Last Modified: Tue, 02 Jun 2026 11:13:04 GMT  
		Size: 25.4 KB (25430 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.4.10`

```console
$ docker pull geonetwork@sha256:5f67da2cc43bd7718e2e0676f25d3b91db7d97c2187ded37db1d83b3e1c44427
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
$ docker pull geonetwork@sha256:1570ebc4c8d8cae30c2ee5340843640ffa9879405b5716b9063589070972e6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.1 MB (420070202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dc43286c71acc45160e65bec64543ed1d40274e354fdb64655bda3dede6b29`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:14:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:14:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:14:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:14:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:14:19 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 02 Jun 2026 08:14:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:14:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:14:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:14:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:17:46 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:17:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:17:46 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:17:46 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:17:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:17:46 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:17:46 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:17:46 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:17:46 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:17:46 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 10:17:50 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:17:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:17:51 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:17:51 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:17:51 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:13:09 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 11:13:09 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 02 Jun 2026 11:13:09 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 02 Jun 2026 11:13:09 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 11:13:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 02 Jun 2026 11:13:09 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 11:13:09 GMT
ENV GN_VERSION=4.4.10
# Tue, 02 Jun 2026 11:13:09 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 02 Jun 2026 11:13:21 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 11:13:21 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 02 Jun 2026 11:13:21 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 11:13:21 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:13:21 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 11:13:21 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:13:21 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9e436cd644d0619bdfd1c8d1dce9e824e836e6102bf4a4c26919785ffe2a7c`  
		Last Modified: Tue, 02 Jun 2026 08:14:35 GMT  
		Size: 17.0 MB (16984112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abe231f9a275556a3c449f9746da9863dbbea3001e50afdbf5209553a0533c2`  
		Last Modified: Tue, 02 Jun 2026 08:14:36 GMT  
		Size: 47.3 MB (47344216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f689e05e256f3387912f6eab83ac21ffe596b6aa357a513c261ad13b21d283`  
		Last Modified: Tue, 02 Jun 2026 08:14:34 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5e34d12e53e20283e3eaeab1e665797d41b9b9ca6c3b47599a697790b15acb`  
		Last Modified: Tue, 02 Jun 2026 08:14:34 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b12c99159fc66956c2d9b5f3ac562fb93293b4f0ac571b0e57c73f17e7bfdbc`  
		Last Modified: Tue, 02 Jun 2026 10:17:59 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328a1e80cac330b8fd4cbe150711db3a5abd2333338c94c45dae5cff116eb841`  
		Last Modified: Tue, 02 Jun 2026 10:17:59 GMT  
		Size: 13.8 MB (13796163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b0b2346d28acc1f3441f42c9a41c27c0d9217183a6cb1662035858276ab3af`  
		Last Modified: Tue, 02 Jun 2026 10:17:59 GMT  
		Size: 224.8 KB (224833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631e6695a5c2e9c5433e05ca7109c40ad41585acc223c064807c7d7bdd6dc8e1`  
		Last Modified: Tue, 02 Jun 2026 11:13:44 GMT  
		Size: 239.2 KB (239211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34f6d9f937ddbf71a730e33bf0de46f6b661b62fd745421480f32221210968a`  
		Last Modified: Tue, 02 Jun 2026 11:13:51 GMT  
		Size: 311.7 MB (311742293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfdf3d2859f9d8424ea7bf91e8997d328dc41984fb42867f418064ea2487f22`  
		Last Modified: Tue, 02 Jun 2026 11:13:44 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904fe9ae87726911c9251a8b694e0db164afe48ddfd76b876cc5c751d0cf0be2`  
		Last Modified: Tue, 02 Jun 2026 11:13:44 GMT  
		Size: 3.0 KB (3013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ac3509e51ad06df68519ef10a212abe04b754f8f9bf2e785ba89fdea8a64ab`  
		Last Modified: Tue, 02 Jun 2026 11:13:45 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4.10` - unknown; unknown

```console
$ docker pull geonetwork@sha256:bcd3bd1d3e14dbe7402887856277c2dc5324cef64b143b11244a603ca61bfe7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4219006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be50188d7bae4be76a3085cd1218ce37da8710d7eb25627a8f2e4a41b377483e`

```dockerfile
```

-	Layers:
	-	`sha256:955e2a3dcc94ad31b3cf1bdf1bc505d56756b274f8c6dab096adf4fa38ed0b17`  
		Last Modified: Tue, 02 Jun 2026 11:13:44 GMT  
		Size: 4.2 MB (4193576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:824708be85a603e7d03834925cdc488d2492aaf2676ef0436d0b4d6079c3d583`  
		Last Modified: Tue, 02 Jun 2026 11:13:44 GMT  
		Size: 25.4 KB (25430 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4.10` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:48672a66b22db2e0a6a080edc7fcda4f72b51018cb534aacbfb506fe2e48ac41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.5 MB (414526279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997ae873464f8038256b1e1f8c38043d2d0f858d9e888aa62e1d70d763efabc4`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
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
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 02 Jun 2026 08:12:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:12:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:12:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:12:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:13:26 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:13:26 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:13:26 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:13:26 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:13:26 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:13:26 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:13:26 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:13:26 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:13:26 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:13:27 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 10:13:32 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:13:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:13:33 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:13:33 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:13:33 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:11:38 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 11:11:38 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 02 Jun 2026 11:11:38 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 02 Jun 2026 11:11:38 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 11:11:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 02 Jun 2026 11:11:38 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 11:11:38 GMT
ENV GN_VERSION=4.4.10
# Tue, 02 Jun 2026 11:11:38 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 02 Jun 2026 11:13:27 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 11:13:27 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 02 Jun 2026 11:13:27 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 11:13:27 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:13:27 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 11:13:27 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:13:27 GMT
VOLUME [/catalogue-data]
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
	-	`sha256:a763aa8647dee2704dbccddf100af5e050e07be63b2091352322da501dfbaeed`  
		Last Modified: Tue, 02 Jun 2026 08:13:03 GMT  
		Size: 45.5 MB (45454025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce71c5b0eb84b76e19875d5a01ece3a180b99ea3e5d3b749c53692b2767e3c00`  
		Last Modified: Tue, 02 Jun 2026 08:13:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a437059cd3dbdb7d8a53d4964b178c30acdb400c5d84e6e28913d7ff76de3c1`  
		Last Modified: Tue, 02 Jun 2026 08:13:01 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273a3f3cdc146550c02e7329c464a66778b96b407606914d90d5859e7f59582d`  
		Last Modified: Tue, 02 Jun 2026 10:13:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d00a83829a70306b914f1f06e4d228eee0528f75ea07c900f77b513fd6d2687`  
		Last Modified: Tue, 02 Jun 2026 10:13:41 GMT  
		Size: 13.7 MB (13730088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8591662de7c4b4f561acb1dbb592e6eaa7f8d2a4121831ac8d3ff3eca4e6b449`  
		Last Modified: Tue, 02 Jun 2026 10:13:41 GMT  
		Size: 196.5 KB (196506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6721ba9b0a083d0801ac0c20f69e0dd674e9b3eb8a07b31f81de134d1810189c`  
		Last Modified: Tue, 02 Jun 2026 11:13:52 GMT  
		Size: 226.4 KB (226408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f28a16af03b29f9c6bb827df7b6ccaab84a679b76483cf6b774c3a2226007b`  
		Last Modified: Tue, 02 Jun 2026 11:13:58 GMT  
		Size: 311.7 MB (311742307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02adf392821be303350cc5ba7f6cb7d9bdc39c212a32b10b5f563392b70bffd`  
		Last Modified: Tue, 02 Jun 2026 11:13:52 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08109080f302519f9109ebb24ba352f31ec448283e66b08d714627ea7e32e783`  
		Last Modified: Tue, 02 Jun 2026 11:13:52 GMT  
		Size: 3.0 KB (3016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeb7723f52d6bd1f9743c10628d1730f1718c8aa598c4d03ab818c380589c23`  
		Last Modified: Tue, 02 Jun 2026 11:13:53 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4.10` - unknown; unknown

```console
$ docker pull geonetwork@sha256:36090bc31adc9322f761df9782ad44aad6ddd259ab0d5f66e98adb9d85bdf44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4222701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36846105faa0e4a1f4207d1101a38583582d34b13a26de9574ccc4f0359ac03e`

```dockerfile
```

-	Layers:
	-	`sha256:d9f76d562b08f9c8c41540a0ac0426d5e1cdf86523a76b88bc663b7b5fae912e`  
		Last Modified: Tue, 02 Jun 2026 11:13:52 GMT  
		Size: 4.2 MB (4197179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e01fe87e0d3cf12ec30a888f05820dd55440e10252a36e8c2280c7be846736a`  
		Last Modified: Tue, 02 Jun 2026 11:13:51 GMT  
		Size: 25.5 KB (25522 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4.10` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:9676808067bb17308a14f06f9e857a05af791997b1b76ae7407bfc4ec3578381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.6 MB (417551650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9c1ce65405f2b22e9a97cd1a6842dadcb4706ff1dbad48fde134b9705543b3`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:15:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:15:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:15:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:15:43 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:15:43 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 02 Jun 2026 08:15:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:15:48 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:15:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:15:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:14:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:14:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:14:03 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:14:03 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:14:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:14:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:14:03 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:14:03 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:14:03 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:14:03 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 10:14:08 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:14:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:14:09 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:14:09 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:14:09 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:13:04 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 11:13:04 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 02 Jun 2026 11:13:04 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 02 Jun 2026 11:13:04 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 11:13:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 02 Jun 2026 11:13:04 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 11:13:04 GMT
ENV GN_VERSION=4.4.10
# Tue, 02 Jun 2026 11:13:04 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 02 Jun 2026 11:13:18 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 11:13:18 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 02 Jun 2026 11:13:18 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 11:13:18 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:13:18 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 11:13:18 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:13:18 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77acf8a2fd2a14aa128b125e15d261df4fd4f487386a6ac710a99968b2ed8d60`  
		Last Modified: Tue, 02 Jun 2026 08:16:00 GMT  
		Size: 17.0 MB (16997549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e07080645b5dbe3f11ea303d9cef4b4ac977a37efb6d74f92b3f69ded5806d`  
		Last Modified: Tue, 02 Jun 2026 08:16:01 GMT  
		Size: 45.7 MB (45659671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a181db84648310ad9c72731e407b7e06733928683e3ff6e8dfd6c50535d2f74f`  
		Last Modified: Tue, 02 Jun 2026 08:15:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ef243a4acfe4609f9532dec8a35af094f6898a9fba63b1f0a1a16ec457df5c`  
		Last Modified: Tue, 02 Jun 2026 08:15:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7790686ff36b34814640358cae09b83fb719b6ad854894f2582a7d261fd7b5c2`  
		Last Modified: Tue, 02 Jun 2026 10:14:17 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967c3d5f7725f795501d2f608262ba31047ef094db7f89fffb0054f9c2a4ddaf`  
		Last Modified: Tue, 02 Jun 2026 10:14:18 GMT  
		Size: 13.8 MB (13805557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135ba0c297a795416529870fe8e06d5e61ea32c4b717ec3e761809c8be3e7fba`  
		Last Modified: Tue, 02 Jun 2026 10:14:17 GMT  
		Size: 225.1 KB (225133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e42b762b4b42d36927c23c79fa2b1fbb493bd5f5f947ff2030fc89582c79e8`  
		Last Modified: Tue, 02 Jun 2026 11:13:42 GMT  
		Size: 238.4 KB (238420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dad06061b9135ac54d43e6166ed5b64a1ed261a151357cc2e40a155dbee617`  
		Last Modified: Tue, 02 Jun 2026 11:13:50 GMT  
		Size: 311.7 MB (311742343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ad0e9b31522ca2d2867af09ff0295a27534d6b944e82444403d676ec991869`  
		Last Modified: Tue, 02 Jun 2026 11:13:42 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e02ee9d670430ec4fc79c123f360dd0a2cdc68537b9386955c8e42f0589323`  
		Last Modified: Tue, 02 Jun 2026 11:13:42 GMT  
		Size: 3.0 KB (3014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bd61185368c5cbc16f5753636d8291fcc8e628eb8ea151e1f3645ddc3f5d46`  
		Last Modified: Tue, 02 Jun 2026 11:13:43 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4.10` - unknown; unknown

```console
$ docker pull geonetwork@sha256:17b5950d45a383497c3d42691f7f753f0ba140f028ba66a162df54395d1d1056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4220215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5573828472fd131d82084b2e3968931d3b6fdd186e8b9e130017822a1017be67`

```dockerfile
```

-	Layers:
	-	`sha256:329a5eb203f3614de3aecd40c53e9d8889938303b5a5709ee0cde9541303a4e0`  
		Last Modified: Tue, 02 Jun 2026 11:13:42 GMT  
		Size: 4.2 MB (4194666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a2308185e4ec060c856aab2a590654a1b72a4fb390b9518548e2fa92eebc9d0`  
		Last Modified: Tue, 02 Jun 2026 11:13:42 GMT  
		Size: 25.5 KB (25549 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4.10` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:9457b2ebac2d8732e4077e1a44c8a96d3d07fcdfc85c4c81a6a53527db0e9784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.0 MB (422047651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0b120f44c545db492728f2787537047bd7c139c2731d78e73a2581d6c0ce0f`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:10:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:10:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:10:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 02 Jun 2026 08:11:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:11:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:11:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:11:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 11:12:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 11:12:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 11:12:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 11:12:06 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 11:12:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 11:12:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 11:12:06 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 11:12:06 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 11:12:06 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 11:13:46 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 11:13:54 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 11:13:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 11:13:56 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 11:13:56 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 11:13:56 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 12:12:28 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 12:12:28 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 02 Jun 2026 12:12:28 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 02 Jun 2026 12:12:28 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 12:12:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 02 Jun 2026 12:12:28 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 12:12:28 GMT
ENV GN_VERSION=4.4.10
# Tue, 02 Jun 2026 12:12:28 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 02 Jun 2026 12:13:40 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 12:13:43 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 02 Jun 2026 12:13:45 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 12:13:45 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 12:13:45 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 12:13:45 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 12:13:45 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef700e09ef3cf16d19218622a73899db0a8b42f33bfb19159bb4aa3576d5d21e`  
		Last Modified: Tue, 02 Jun 2026 08:10:42 GMT  
		Size: 18.8 MB (18813426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdb8ec1de5532c097eb41fb0f92ecb54f818737f9cf46998385c39953db727e`  
		Last Modified: Tue, 02 Jun 2026 08:11:40 GMT  
		Size: 42.8 MB (42813392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff385880e28b2054d84e0b5800e2140ec87b662269f8c33bcd8221e0872b169`  
		Last Modified: Tue, 02 Jun 2026 08:11:38 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488cf18986ce3513c802f428d34a1e7fb7ee6c03d85b6e178526bcbc122bd6e3`  
		Last Modified: Tue, 02 Jun 2026 08:11:38 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33f5563bc4dd12556380a3e559556fb88cfe44d0aadda72376aa21cb7784938`  
		Last Modified: Tue, 02 Jun 2026 11:12:33 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb655d0ba9a3e96868a29850c89743ca0cdb1bbd5c76c36e15569c186138a8e`  
		Last Modified: Tue, 02 Jun 2026 11:14:17 GMT  
		Size: 13.8 MB (13831827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c30463ec1bb4e3f75e206871f12591f78f5e5217c358e3799c9c69ea6ba20f7`  
		Last Modified: Tue, 02 Jun 2026 11:14:17 GMT  
		Size: 256.5 KB (256542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af15e78091e72109de7dd175a418eed89175b349517f7e90d762a8aa0d0fb706`  
		Last Modified: Tue, 02 Jun 2026 12:14:30 GMT  
		Size: 269.5 KB (269514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e31bfb989f5171fe0d81f03e3a597a2f95888867968a1f62d497c409276d22d`  
		Last Modified: Tue, 02 Jun 2026 12:14:37 GMT  
		Size: 311.7 MB (311742284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f9f010d38a32ee70a3e1a2420f3678cf67a11733ad6c4ad223b35c0337cfa3`  
		Last Modified: Tue, 02 Jun 2026 12:14:30 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdbf0a6709e1f87fa8d249bbb9d025846fbc006af781c4328f31ddb0451c80d`  
		Last Modified: Tue, 02 Jun 2026 12:14:30 GMT  
		Size: 3.0 KB (3011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d2848fa6c2f8e5f88594c387255ca4daad50e2439baa15162236cc3cbbffd7`  
		Last Modified: Tue, 02 Jun 2026 12:14:32 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4.10` - unknown; unknown

```console
$ docker pull geonetwork@sha256:f37a20e07996edbedb981c3209e83bb3f372f1e942ec169f199799aa1a5f2f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4223131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0788a3898cd2932321d4fa23bff9244322493780755bf93b3faf357b5bfcf12f`

```dockerfile
```

-	Layers:
	-	`sha256:8684538b5cc2d6e1e794744b22fc3aa063a1cfcf02eea00414b9f8db775dde64`  
		Last Modified: Tue, 02 Jun 2026 12:14:30 GMT  
		Size: 4.2 MB (4197655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d217c800893f99b60fee07af80703030ede3a5a27badcc7a7ecb1e7b2794118e`  
		Last Modified: Tue, 02 Jun 2026 12:14:30 GMT  
		Size: 25.5 KB (25476 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:4.4.10` - linux; s390x

```console
$ docker pull geonetwork@sha256:3fb6dcdf8c1eb326fa2fc1cd5a788e85710bc09ba33e66c920e972b87417c42d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.9 MB (414888372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394b71d0074453a02f912f7ed6a3491b11977512891e01e1fd812a2fa7c08765`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:09 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:11 GMT
ADD file:b574b1e436c2db4e4d66f69c75e47a9aebf0da1ad375147eb2c0b7ff76c6ab7e in / 
# Wed, 20 May 2026 01:37:11 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:10:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:10:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:10:07 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:07 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 02 Jun 2026 08:10:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:10:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:10:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:10:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:13:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:13:34 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:13:34 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:13:34 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:13:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:13:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:13:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:13:34 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:13:34 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:13:34 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 10:13:38 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:13:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:13:39 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:13:39 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:13:39 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:10:11 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 11:10:11 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 02 Jun 2026 11:10:11 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 02 Jun 2026 11:10:11 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 11:10:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 02 Jun 2026 11:10:11 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 11:10:11 GMT
ENV GN_VERSION=4.4.10
# Tue, 02 Jun 2026 11:10:11 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 02 Jun 2026 11:12:29 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 11:12:29 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 02 Jun 2026 11:12:29 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 11:12:29 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:12:29 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 11:12:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:12:29 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:c8ebd0a624851e8502e41ee64db2b6a45537554969784d82ebbc91c905cbc2ef`  
		Last Modified: Wed, 20 May 2026 02:16:00 GMT  
		Size: 29.9 MB (29912835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256477a86eb77158be04768dcbdcc986e9666c7a5b72ecdd17f52da12bff8924`  
		Last Modified: Tue, 02 Jun 2026 08:10:28 GMT  
		Size: 17.6 MB (17579962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07875ed48ad40d3c0543f9e9ea54996649cbd5597e8d1caf025c1c702b28a76c`  
		Last Modified: Tue, 02 Jun 2026 08:10:28 GMT  
		Size: 41.4 MB (41358655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99876fbee0a85bc5276f8602f18bfb73f8a7de6d05d8c26412a5ad9543c3cefb`  
		Last Modified: Tue, 02 Jun 2026 08:10:27 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158613312c3340f8af5e729ceedd638f9ce909bb97569d3c1f29818acb14f350`  
		Last Modified: Tue, 02 Jun 2026 08:10:27 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b047d5bb1171f63cbbc0d937f6fc6398fc0addfbd11018eb69ad8776a260d181`  
		Last Modified: Tue, 02 Jun 2026 10:13:53 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d9eb03dc287b7f8872fe628b54a1c10a62b0737238843f5b2be5ebbd6ef6c9`  
		Last Modified: Tue, 02 Jun 2026 10:13:54 GMT  
		Size: 13.8 MB (13804806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db08f77ae0b24a458200e7c5fce15ebe74d7c4a6ba1619d147e1ad151f1c7b39`  
		Last Modified: Tue, 02 Jun 2026 10:13:54 GMT  
		Size: 232.9 KB (232888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f43029b9c1851bfb00de7905064677271138d641836163322ad91decc7a77dc`  
		Last Modified: Tue, 02 Jun 2026 11:13:04 GMT  
		Size: 250.4 KB (250355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d3f5e2af58cac314ceeae7255474ed86aba9a12cbe7fab268e01975d773a5b`  
		Last Modified: Tue, 02 Jun 2026 11:13:10 GMT  
		Size: 311.7 MB (311742306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a8cdabbaeafc4f00d6257baf2931a6763df06d8189ec9c36afda75e37e43ee`  
		Last Modified: Tue, 02 Jun 2026 11:13:04 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7a33ae0ff34c47f7676733829015b39cc2930e6eabcac0e0a66bcedaa0fda1`  
		Last Modified: Tue, 02 Jun 2026 11:13:04 GMT  
		Size: 3.0 KB (3011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e4be60be430f49ea60798957b3c5ce2223c96981d980dc562629836a9bdab0`  
		Last Modified: Tue, 02 Jun 2026 11:13:05 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4.10` - unknown; unknown

```console
$ docker pull geonetwork@sha256:c30ed70c67aba79e0d2b4355d7e639ec3515f1cae33676d41c91a5de6d4703cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4221211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e79df7d80504c0fba1c6bb14ca72b3ca841aa6f07df2b16f838d174e2ac128b`

```dockerfile
```

-	Layers:
	-	`sha256:842d02fe1880cdda8c402c29012c564b266f219ca4d36f1c63aa68defd9c9624`  
		Last Modified: Tue, 02 Jun 2026 11:13:04 GMT  
		Size: 4.2 MB (4195781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b80aa58ac825f28b1227878b09a8d61d0a5d5db82c8d97f895181f83cceee59a`  
		Last Modified: Tue, 02 Jun 2026 11:13:04 GMT  
		Size: 25.4 KB (25430 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:latest`

```console
$ docker pull geonetwork@sha256:5f67da2cc43bd7718e2e0676f25d3b91db7d97c2187ded37db1d83b3e1c44427
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
$ docker pull geonetwork@sha256:1570ebc4c8d8cae30c2ee5340843640ffa9879405b5716b9063589070972e6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.1 MB (420070202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dc43286c71acc45160e65bec64543ed1d40274e354fdb64655bda3dede6b29`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:14:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:14:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:14:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:14:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:14:19 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 02 Jun 2026 08:14:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:14:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:14:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:14:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:17:46 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:17:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:17:46 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:17:46 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:17:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:17:46 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:17:46 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:17:46 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:17:46 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:17:46 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 10:17:50 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:17:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:17:51 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:17:51 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:17:51 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:13:09 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 11:13:09 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 02 Jun 2026 11:13:09 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 02 Jun 2026 11:13:09 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 11:13:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 02 Jun 2026 11:13:09 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 11:13:09 GMT
ENV GN_VERSION=4.4.10
# Tue, 02 Jun 2026 11:13:09 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 02 Jun 2026 11:13:21 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 11:13:21 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 02 Jun 2026 11:13:21 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 11:13:21 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:13:21 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 11:13:21 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:13:21 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9e436cd644d0619bdfd1c8d1dce9e824e836e6102bf4a4c26919785ffe2a7c`  
		Last Modified: Tue, 02 Jun 2026 08:14:35 GMT  
		Size: 17.0 MB (16984112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abe231f9a275556a3c449f9746da9863dbbea3001e50afdbf5209553a0533c2`  
		Last Modified: Tue, 02 Jun 2026 08:14:36 GMT  
		Size: 47.3 MB (47344216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f689e05e256f3387912f6eab83ac21ffe596b6aa357a513c261ad13b21d283`  
		Last Modified: Tue, 02 Jun 2026 08:14:34 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5e34d12e53e20283e3eaeab1e665797d41b9b9ca6c3b47599a697790b15acb`  
		Last Modified: Tue, 02 Jun 2026 08:14:34 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b12c99159fc66956c2d9b5f3ac562fb93293b4f0ac571b0e57c73f17e7bfdbc`  
		Last Modified: Tue, 02 Jun 2026 10:17:59 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328a1e80cac330b8fd4cbe150711db3a5abd2333338c94c45dae5cff116eb841`  
		Last Modified: Tue, 02 Jun 2026 10:17:59 GMT  
		Size: 13.8 MB (13796163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b0b2346d28acc1f3441f42c9a41c27c0d9217183a6cb1662035858276ab3af`  
		Last Modified: Tue, 02 Jun 2026 10:17:59 GMT  
		Size: 224.8 KB (224833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631e6695a5c2e9c5433e05ca7109c40ad41585acc223c064807c7d7bdd6dc8e1`  
		Last Modified: Tue, 02 Jun 2026 11:13:44 GMT  
		Size: 239.2 KB (239211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34f6d9f937ddbf71a730e33bf0de46f6b661b62fd745421480f32221210968a`  
		Last Modified: Tue, 02 Jun 2026 11:13:51 GMT  
		Size: 311.7 MB (311742293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfdf3d2859f9d8424ea7bf91e8997d328dc41984fb42867f418064ea2487f22`  
		Last Modified: Tue, 02 Jun 2026 11:13:44 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904fe9ae87726911c9251a8b694e0db164afe48ddfd76b876cc5c751d0cf0be2`  
		Last Modified: Tue, 02 Jun 2026 11:13:44 GMT  
		Size: 3.0 KB (3013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ac3509e51ad06df68519ef10a212abe04b754f8f9bf2e785ba89fdea8a64ab`  
		Last Modified: Tue, 02 Jun 2026 11:13:45 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:latest` - unknown; unknown

```console
$ docker pull geonetwork@sha256:bcd3bd1d3e14dbe7402887856277c2dc5324cef64b143b11244a603ca61bfe7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4219006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be50188d7bae4be76a3085cd1218ce37da8710d7eb25627a8f2e4a41b377483e`

```dockerfile
```

-	Layers:
	-	`sha256:955e2a3dcc94ad31b3cf1bdf1bc505d56756b274f8c6dab096adf4fa38ed0b17`  
		Last Modified: Tue, 02 Jun 2026 11:13:44 GMT  
		Size: 4.2 MB (4193576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:824708be85a603e7d03834925cdc488d2492aaf2676ef0436d0b4d6079c3d583`  
		Last Modified: Tue, 02 Jun 2026 11:13:44 GMT  
		Size: 25.4 KB (25430 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:latest` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:48672a66b22db2e0a6a080edc7fcda4f72b51018cb534aacbfb506fe2e48ac41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.5 MB (414526279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997ae873464f8038256b1e1f8c38043d2d0f858d9e888aa62e1d70d763efabc4`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
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
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 02 Jun 2026 08:12:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:12:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:12:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:12:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:13:26 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:13:26 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:13:26 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:13:26 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:13:26 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:13:26 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:13:26 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:13:26 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:13:26 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:13:27 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 10:13:32 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:13:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:13:33 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:13:33 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:13:33 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:11:38 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 11:11:38 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 02 Jun 2026 11:11:38 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 02 Jun 2026 11:11:38 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 11:11:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 02 Jun 2026 11:11:38 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 11:11:38 GMT
ENV GN_VERSION=4.4.10
# Tue, 02 Jun 2026 11:11:38 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 02 Jun 2026 11:13:27 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 11:13:27 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 02 Jun 2026 11:13:27 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 11:13:27 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:13:27 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 11:13:27 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:13:27 GMT
VOLUME [/catalogue-data]
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
	-	`sha256:a763aa8647dee2704dbccddf100af5e050e07be63b2091352322da501dfbaeed`  
		Last Modified: Tue, 02 Jun 2026 08:13:03 GMT  
		Size: 45.5 MB (45454025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce71c5b0eb84b76e19875d5a01ece3a180b99ea3e5d3b749c53692b2767e3c00`  
		Last Modified: Tue, 02 Jun 2026 08:13:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a437059cd3dbdb7d8a53d4964b178c30acdb400c5d84e6e28913d7ff76de3c1`  
		Last Modified: Tue, 02 Jun 2026 08:13:01 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273a3f3cdc146550c02e7329c464a66778b96b407606914d90d5859e7f59582d`  
		Last Modified: Tue, 02 Jun 2026 10:13:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d00a83829a70306b914f1f06e4d228eee0528f75ea07c900f77b513fd6d2687`  
		Last Modified: Tue, 02 Jun 2026 10:13:41 GMT  
		Size: 13.7 MB (13730088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8591662de7c4b4f561acb1dbb592e6eaa7f8d2a4121831ac8d3ff3eca4e6b449`  
		Last Modified: Tue, 02 Jun 2026 10:13:41 GMT  
		Size: 196.5 KB (196506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6721ba9b0a083d0801ac0c20f69e0dd674e9b3eb8a07b31f81de134d1810189c`  
		Last Modified: Tue, 02 Jun 2026 11:13:52 GMT  
		Size: 226.4 KB (226408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f28a16af03b29f9c6bb827df7b6ccaab84a679b76483cf6b774c3a2226007b`  
		Last Modified: Tue, 02 Jun 2026 11:13:58 GMT  
		Size: 311.7 MB (311742307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02adf392821be303350cc5ba7f6cb7d9bdc39c212a32b10b5f563392b70bffd`  
		Last Modified: Tue, 02 Jun 2026 11:13:52 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08109080f302519f9109ebb24ba352f31ec448283e66b08d714627ea7e32e783`  
		Last Modified: Tue, 02 Jun 2026 11:13:52 GMT  
		Size: 3.0 KB (3016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeb7723f52d6bd1f9743c10628d1730f1718c8aa598c4d03ab818c380589c23`  
		Last Modified: Tue, 02 Jun 2026 11:13:53 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:latest` - unknown; unknown

```console
$ docker pull geonetwork@sha256:36090bc31adc9322f761df9782ad44aad6ddd259ab0d5f66e98adb9d85bdf44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4222701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36846105faa0e4a1f4207d1101a38583582d34b13a26de9574ccc4f0359ac03e`

```dockerfile
```

-	Layers:
	-	`sha256:d9f76d562b08f9c8c41540a0ac0426d5e1cdf86523a76b88bc663b7b5fae912e`  
		Last Modified: Tue, 02 Jun 2026 11:13:52 GMT  
		Size: 4.2 MB (4197179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e01fe87e0d3cf12ec30a888f05820dd55440e10252a36e8c2280c7be846736a`  
		Last Modified: Tue, 02 Jun 2026 11:13:51 GMT  
		Size: 25.5 KB (25522 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:latest` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:9676808067bb17308a14f06f9e857a05af791997b1b76ae7407bfc4ec3578381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.6 MB (417551650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9c1ce65405f2b22e9a97cd1a6842dadcb4706ff1dbad48fde134b9705543b3`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:15:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:15:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:15:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:15:43 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:15:43 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 02 Jun 2026 08:15:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:15:48 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:15:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:15:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:14:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:14:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:14:03 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:14:03 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:14:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:14:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:14:03 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:14:03 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:14:03 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:14:03 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 10:14:08 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:14:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:14:09 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:14:09 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:14:09 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:13:04 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 11:13:04 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 02 Jun 2026 11:13:04 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 02 Jun 2026 11:13:04 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 11:13:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 02 Jun 2026 11:13:04 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 11:13:04 GMT
ENV GN_VERSION=4.4.10
# Tue, 02 Jun 2026 11:13:04 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 02 Jun 2026 11:13:18 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 11:13:18 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 02 Jun 2026 11:13:18 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 11:13:18 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:13:18 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 11:13:18 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:13:18 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77acf8a2fd2a14aa128b125e15d261df4fd4f487386a6ac710a99968b2ed8d60`  
		Last Modified: Tue, 02 Jun 2026 08:16:00 GMT  
		Size: 17.0 MB (16997549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e07080645b5dbe3f11ea303d9cef4b4ac977a37efb6d74f92b3f69ded5806d`  
		Last Modified: Tue, 02 Jun 2026 08:16:01 GMT  
		Size: 45.7 MB (45659671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a181db84648310ad9c72731e407b7e06733928683e3ff6e8dfd6c50535d2f74f`  
		Last Modified: Tue, 02 Jun 2026 08:15:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ef243a4acfe4609f9532dec8a35af094f6898a9fba63b1f0a1a16ec457df5c`  
		Last Modified: Tue, 02 Jun 2026 08:15:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7790686ff36b34814640358cae09b83fb719b6ad854894f2582a7d261fd7b5c2`  
		Last Modified: Tue, 02 Jun 2026 10:14:17 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967c3d5f7725f795501d2f608262ba31047ef094db7f89fffb0054f9c2a4ddaf`  
		Last Modified: Tue, 02 Jun 2026 10:14:18 GMT  
		Size: 13.8 MB (13805557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135ba0c297a795416529870fe8e06d5e61ea32c4b717ec3e761809c8be3e7fba`  
		Last Modified: Tue, 02 Jun 2026 10:14:17 GMT  
		Size: 225.1 KB (225133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e42b762b4b42d36927c23c79fa2b1fbb493bd5f5f947ff2030fc89582c79e8`  
		Last Modified: Tue, 02 Jun 2026 11:13:42 GMT  
		Size: 238.4 KB (238420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dad06061b9135ac54d43e6166ed5b64a1ed261a151357cc2e40a155dbee617`  
		Last Modified: Tue, 02 Jun 2026 11:13:50 GMT  
		Size: 311.7 MB (311742343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ad0e9b31522ca2d2867af09ff0295a27534d6b944e82444403d676ec991869`  
		Last Modified: Tue, 02 Jun 2026 11:13:42 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e02ee9d670430ec4fc79c123f360dd0a2cdc68537b9386955c8e42f0589323`  
		Last Modified: Tue, 02 Jun 2026 11:13:42 GMT  
		Size: 3.0 KB (3014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bd61185368c5cbc16f5753636d8291fcc8e628eb8ea151e1f3645ddc3f5d46`  
		Last Modified: Tue, 02 Jun 2026 11:13:43 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:latest` - unknown; unknown

```console
$ docker pull geonetwork@sha256:17b5950d45a383497c3d42691f7f753f0ba140f028ba66a162df54395d1d1056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4220215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5573828472fd131d82084b2e3968931d3b6fdd186e8b9e130017822a1017be67`

```dockerfile
```

-	Layers:
	-	`sha256:329a5eb203f3614de3aecd40c53e9d8889938303b5a5709ee0cde9541303a4e0`  
		Last Modified: Tue, 02 Jun 2026 11:13:42 GMT  
		Size: 4.2 MB (4194666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a2308185e4ec060c856aab2a590654a1b72a4fb390b9518548e2fa92eebc9d0`  
		Last Modified: Tue, 02 Jun 2026 11:13:42 GMT  
		Size: 25.5 KB (25549 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:latest` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:9457b2ebac2d8732e4077e1a44c8a96d3d07fcdfc85c4c81a6a53527db0e9784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.0 MB (422047651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0b120f44c545db492728f2787537047bd7c139c2731d78e73a2581d6c0ce0f`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:10:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:10:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:10:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:09 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 02 Jun 2026 08:11:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:11:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:11:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:11:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 11:12:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 11:12:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 11:12:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 11:12:06 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 11:12:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 11:12:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 11:12:06 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 11:12:06 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 11:12:06 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 11:13:46 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 11:13:54 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 11:13:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 11:13:56 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 11:13:56 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 11:13:56 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 12:12:28 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 12:12:28 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 02 Jun 2026 12:12:28 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 02 Jun 2026 12:12:28 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 12:12:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 02 Jun 2026 12:12:28 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 12:12:28 GMT
ENV GN_VERSION=4.4.10
# Tue, 02 Jun 2026 12:12:28 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 02 Jun 2026 12:13:40 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 12:13:43 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 02 Jun 2026 12:13:45 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 12:13:45 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 12:13:45 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 12:13:45 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 12:13:45 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef700e09ef3cf16d19218622a73899db0a8b42f33bfb19159bb4aa3576d5d21e`  
		Last Modified: Tue, 02 Jun 2026 08:10:42 GMT  
		Size: 18.8 MB (18813426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdb8ec1de5532c097eb41fb0f92ecb54f818737f9cf46998385c39953db727e`  
		Last Modified: Tue, 02 Jun 2026 08:11:40 GMT  
		Size: 42.8 MB (42813392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff385880e28b2054d84e0b5800e2140ec87b662269f8c33bcd8221e0872b169`  
		Last Modified: Tue, 02 Jun 2026 08:11:38 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488cf18986ce3513c802f428d34a1e7fb7ee6c03d85b6e178526bcbc122bd6e3`  
		Last Modified: Tue, 02 Jun 2026 08:11:38 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33f5563bc4dd12556380a3e559556fb88cfe44d0aadda72376aa21cb7784938`  
		Last Modified: Tue, 02 Jun 2026 11:12:33 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb655d0ba9a3e96868a29850c89743ca0cdb1bbd5c76c36e15569c186138a8e`  
		Last Modified: Tue, 02 Jun 2026 11:14:17 GMT  
		Size: 13.8 MB (13831827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c30463ec1bb4e3f75e206871f12591f78f5e5217c358e3799c9c69ea6ba20f7`  
		Last Modified: Tue, 02 Jun 2026 11:14:17 GMT  
		Size: 256.5 KB (256542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af15e78091e72109de7dd175a418eed89175b349517f7e90d762a8aa0d0fb706`  
		Last Modified: Tue, 02 Jun 2026 12:14:30 GMT  
		Size: 269.5 KB (269514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e31bfb989f5171fe0d81f03e3a597a2f95888867968a1f62d497c409276d22d`  
		Last Modified: Tue, 02 Jun 2026 12:14:37 GMT  
		Size: 311.7 MB (311742284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f9f010d38a32ee70a3e1a2420f3678cf67a11733ad6c4ad223b35c0337cfa3`  
		Last Modified: Tue, 02 Jun 2026 12:14:30 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdbf0a6709e1f87fa8d249bbb9d025846fbc006af781c4328f31ddb0451c80d`  
		Last Modified: Tue, 02 Jun 2026 12:14:30 GMT  
		Size: 3.0 KB (3011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d2848fa6c2f8e5f88594c387255ca4daad50e2439baa15162236cc3cbbffd7`  
		Last Modified: Tue, 02 Jun 2026 12:14:32 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:latest` - unknown; unknown

```console
$ docker pull geonetwork@sha256:f37a20e07996edbedb981c3209e83bb3f372f1e942ec169f199799aa1a5f2f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4223131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0788a3898cd2932321d4fa23bff9244322493780755bf93b3faf357b5bfcf12f`

```dockerfile
```

-	Layers:
	-	`sha256:8684538b5cc2d6e1e794744b22fc3aa063a1cfcf02eea00414b9f8db775dde64`  
		Last Modified: Tue, 02 Jun 2026 12:14:30 GMT  
		Size: 4.2 MB (4197655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d217c800893f99b60fee07af80703030ede3a5a27badcc7a7ecb1e7b2794118e`  
		Last Modified: Tue, 02 Jun 2026 12:14:30 GMT  
		Size: 25.5 KB (25476 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:latest` - linux; s390x

```console
$ docker pull geonetwork@sha256:3fb6dcdf8c1eb326fa2fc1cd5a788e85710bc09ba33e66c920e972b87417c42d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.9 MB (414888372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394b71d0074453a02f912f7ed6a3491b11977512891e01e1fd812a2fa7c08765`
-	Entrypoint: `["\/geonetwork-entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 May 2026 01:37:09 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:11 GMT
ADD file:b574b1e436c2db4e4d66f69c75e47a9aebf0da1ad375147eb2c0b7ff76c6ab7e in / 
# Wed, 20 May 2026 01:37:11 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:10:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:10:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:10:07 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:07 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 02 Jun 2026 08:10:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        arm64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        armhf)          ESUM='5d3e988cdc8291779068c957c01d339f26178ff65d13af4671107b169e80a69f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_arm_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64el)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:10:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:10:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:10:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 10:13:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 02 Jun 2026 10:13:34 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 10:13:34 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 02 Jun 2026 10:13:34 GMT
WORKDIR /usr/local/tomcat
# Tue, 02 Jun 2026 10:13:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:13:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 02 Jun 2026 10:13:34 GMT
ENV TOMCAT_MAJOR=9
# Tue, 02 Jun 2026 10:13:34 GMT
ENV TOMCAT_VERSION=9.0.118
# Tue, 02 Jun 2026 10:13:34 GMT
ENV TOMCAT_SHA512=737367433486757ccd687329d99b1188506cdec57a53a29b415173909c38cdf9da4fc9fd73b8cd17cd0a8def8610ad43bab8e84393dc904a0bd1121da8cab2fc
# Tue, 02 Jun 2026 10:13:34 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 02 Jun 2026 10:13:38 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:13:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 02 Jun 2026 10:13:39 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 10:13:39 GMT
ENTRYPOINT []
# Tue, 02 Jun 2026 10:13:39 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:10:11 GMT
ENV DATA_DIR=/catalogue-data
# Tue, 02 Jun 2026 11:10:11 GMT
ENV WEBAPP_CONTEXT_PATH=/geonetwork
# Tue, 02 Jun 2026 11:10:11 GMT
ENV GN_CONFIG_PROPERTIES=-Dgeonetwork.dir=/catalogue-data         -Dgeonetwork.formatter.dir=/catalogue-data/data/formatter         -Dgeonetwork.schema.dir=/opt/geonetwork/WEB-INF/data/config/schema_plugins         -Dgeonetwork.indexConfig.dir=/opt/geonetwork/WEB-INF/data/config/index
# Tue, 02 Jun 2026 11:10:11 GMT
ENV JAVA_OPTS=-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true         -Xms512M -Xss512M -Xmx2G -XX:+UseConcMarkSweepGC
# Tue, 02 Jun 2026 11:10:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         curl         unzip     ;     rm -rf /var/lib/apt/lists/*;     mkdir -p "${DATA_DIR}";     mkdir -p /opt/geonetwork;     mkdir -p /usr/local/tomcat/conf/Catalina/localhost # buildkit
# Tue, 02 Jun 2026 11:10:11 GMT
ENV GN_FILE=geonetwork.war
# Tue, 02 Jun 2026 11:10:11 GMT
ENV GN_VERSION=4.4.10
# Tue, 02 Jun 2026 11:10:11 GMT
ENV GN_DOWNLOAD_MD5=920136a8a502e52fd1bfa1417df83a05
# Tue, 02 Jun 2026 11:12:29 GMT
RUN set -eux;     cd /opt/geonetwork/;     curl -fSL -o geonetwork.war         "https://sourceforge.net/projects/geonetwork/files/GeoNetwork_opensource/v${GN_VERSION}/${GN_FILE}/download";     echo "${GN_DOWNLOAD_MD5} *geonetwork.war" | md5sum -c;     unzip -q geonetwork.war;     rm geonetwork.war # buildkit
# Tue, 02 Jun 2026 11:12:29 GMT
COPY tomcat/geonetwork_context_template.xml /usr/local/share/geonetwork/geonetwork_context_template.xml # buildkit
# Tue, 02 Jun 2026 11:12:29 GMT
COPY tomcat/server.xml /usr/local/tomcat/conf/server.xml # buildkit
# Tue, 02 Jun 2026 11:12:29 GMT
COPY ./docker-entrypoint.sh /geonetwork-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 11:12:29 GMT
ENTRYPOINT ["/geonetwork-entrypoint.sh"]
# Tue, 02 Jun 2026 11:12:29 GMT
CMD ["catalina.sh" "run"]
# Tue, 02 Jun 2026 11:12:29 GMT
VOLUME [/catalogue-data]
```

-	Layers:
	-	`sha256:c8ebd0a624851e8502e41ee64db2b6a45537554969784d82ebbc91c905cbc2ef`  
		Last Modified: Wed, 20 May 2026 02:16:00 GMT  
		Size: 29.9 MB (29912835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256477a86eb77158be04768dcbdcc986e9666c7a5b72ecdd17f52da12bff8924`  
		Last Modified: Tue, 02 Jun 2026 08:10:28 GMT  
		Size: 17.6 MB (17579962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07875ed48ad40d3c0543f9e9ea54996649cbd5597e8d1caf025c1c702b28a76c`  
		Last Modified: Tue, 02 Jun 2026 08:10:28 GMT  
		Size: 41.4 MB (41358655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99876fbee0a85bc5276f8602f18bfb73f8a7de6d05d8c26412a5ad9543c3cefb`  
		Last Modified: Tue, 02 Jun 2026 08:10:27 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158613312c3340f8af5e729ceedd638f9ce909bb97569d3c1f29818acb14f350`  
		Last Modified: Tue, 02 Jun 2026 08:10:27 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b047d5bb1171f63cbbc0d937f6fc6398fc0addfbd11018eb69ad8776a260d181`  
		Last Modified: Tue, 02 Jun 2026 10:13:53 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d9eb03dc287b7f8872fe628b54a1c10a62b0737238843f5b2be5ebbd6ef6c9`  
		Last Modified: Tue, 02 Jun 2026 10:13:54 GMT  
		Size: 13.8 MB (13804806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db08f77ae0b24a458200e7c5fce15ebe74d7c4a6ba1619d147e1ad151f1c7b39`  
		Last Modified: Tue, 02 Jun 2026 10:13:54 GMT  
		Size: 232.9 KB (232888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f43029b9c1851bfb00de7905064677271138d641836163322ad91decc7a77dc`  
		Last Modified: Tue, 02 Jun 2026 11:13:04 GMT  
		Size: 250.4 KB (250355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d3f5e2af58cac314ceeae7255474ed86aba9a12cbe7fab268e01975d773a5b`  
		Last Modified: Tue, 02 Jun 2026 11:13:10 GMT  
		Size: 311.7 MB (311742306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a8cdabbaeafc4f00d6257baf2931a6763df06d8189ec9c36afda75e37e43ee`  
		Last Modified: Tue, 02 Jun 2026 11:13:04 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7a33ae0ff34c47f7676733829015b39cc2930e6eabcac0e0a66bcedaa0fda1`  
		Last Modified: Tue, 02 Jun 2026 11:13:04 GMT  
		Size: 3.0 KB (3011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e4be60be430f49ea60798957b3c5ce2223c96981d980dc562629836a9bdab0`  
		Last Modified: Tue, 02 Jun 2026 11:13:05 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:latest` - unknown; unknown

```console
$ docker pull geonetwork@sha256:c30ed70c67aba79e0d2b4355d7e639ec3515f1cae33676d41c91a5de6d4703cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4221211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e79df7d80504c0fba1c6bb14ca72b3ca841aa6f07df2b16f838d174e2ac128b`

```dockerfile
```

-	Layers:
	-	`sha256:842d02fe1880cdda8c402c29012c564b266f219ca4d36f1c63aa68defd9c9624`  
		Last Modified: Tue, 02 Jun 2026 11:13:04 GMT  
		Size: 4.2 MB (4195781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b80aa58ac825f28b1227878b09a8d61d0a5d5db82c8d97f895181f83cceee59a`  
		Last Modified: Tue, 02 Jun 2026 11:13:04 GMT  
		Size: 25.4 KB (25430 bytes)  
		MIME: application/vnd.in-toto+json
