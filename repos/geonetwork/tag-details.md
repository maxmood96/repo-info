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
$ docker pull geonetwork@sha256:18fd80af67dfbb5ac858a7e3eb8c49a83c98e24d1baa8822394cbd10e0b9b85e
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
$ docker pull geonetwork@sha256:7a3e5ddad59927a808058315f648d4b0155de9c764457f2ef0eaab44d4762707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.5 MB (353487665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124873c0ed3953817f499bcf35b3babceb769c58b0ae6a2dd17d58f1e807b69a`
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
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
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
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f958f4e5767ee8cbfae4e4235c527c4131d6057a66355b614d894f1a0a4c17e`  
		Last Modified: Fri, 31 Jan 2025 01:29:51 GMT  
		Size: 17.0 MB (16962286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85bc3172399be429690fb80a0e29a164e651fe7c79af0a116a832cd9a452af4`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 54.7 MB (54722132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91352bec832ebb8bbef001417c3390a864883828fd1ea6d0304aa3540c5fcf42`  
		Last Modified: Fri, 31 Jan 2025 01:29:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b0a778c4b3fa7cb96f64bd0815f368a43af46f5675c73473ff21260609ed34`  
		Last Modified: Fri, 31 Jan 2025 01:29:50 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54052fc5a57ccf09bd3a191cac02a0119f6e89611349406e744f5300feac29c3`  
		Last Modified: Fri, 31 Jan 2025 02:16:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdf6e1898878b79d3b2e2b6f632ee60e22a70625ca700ad8b32bff5cba8a335`  
		Last Modified: Fri, 31 Jan 2025 02:16:44 GMT  
		Size: 17.5 MB (17498782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0739d463f54d427403a7a38f46c6949c6bf4e071eb4df931ad505b6c8ea30a2`  
		Last Modified: Fri, 31 Jan 2025 03:13:29 GMT  
		Size: 234.5 MB (234549547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801162cd369643515aa88b33493b35c8f42d1bf959b537c6546a55b3b89762cc`  
		Last Modified: Fri, 31 Jan 2025 03:13:22 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:582eca7c3d6b15a84faf1dc7a3852881d3dbec577c27d3caba0cbb04589532ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4201471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c43c19f72403f292a16acb32fd2a357d47a999bdc481f4d567782a43b018570`

```dockerfile
```

-	Layers:
	-	`sha256:b2a95fe06b52702501a8a2752ba4cd6bd33f0b736ae7348861da76fdea0e880c`  
		Last Modified: Fri, 31 Jan 2025 03:13:22 GMT  
		Size: 4.2 MB (4182336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71907960108916e6b067ee5773e40f204670660647e8c15ee07395735ee703b3`  
		Last Modified: Fri, 31 Jan 2025 03:13:21 GMT  
		Size: 19.1 KB (19135 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:27cca303f63cc4a6278c7d126582e35f676d89a757f3f09ddc51045d0d5947e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.3 MB (346252767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4b55cc593d835461d97f0c6f6a62d3a759da60241b93a1457f7ba11095d40c`
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
ADD file:786ab064bf2d82faf7ca3fbb6c2e6983bbdb3228800d6d64e5dec4a67f778a7a in / 
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
	-	`sha256:b25adda5718ef4d96696ce8f0e58cde58fbe9977456036f84293bba8f26c5567`  
		Last Modified: Tue, 19 Nov 2024 17:38:39 GMT  
		Size: 26.9 MB (26869639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a5eb6a2db557356b46da4a6e217de6ed249bca2210cdccd1a0430c803e8512`  
		Last Modified: Tue, 03 Dec 2024 07:45:24 GMT  
		Size: 16.3 MB (16299908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa44b4fc4334a27557f3a631a9438ca5ce8656e161b39e45ab2440b2d7aead1`  
		Last Modified: Fri, 31 Jan 2025 01:32:09 GMT  
		Size: 50.1 MB (50109725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d811e0afab0f1ffd85e4671f4a476cb71cbde9841a85d24ae45a1ad7b42f60a`  
		Last Modified: Fri, 31 Jan 2025 01:32:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd08c17ad27b6137eb1f45f5f4617278e0a8b0c6ef2a13aa6a4fee9ab4777e26`  
		Last Modified: Fri, 31 Jan 2025 01:32:07 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59de26424799b6d39429ee18f2ea2fd2556807bdfa7356ee01c8bbfdd836544`  
		Last Modified: Fri, 31 Jan 2025 02:47:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771e8c9a5f56f2bac23ee6b2b3ac39b5c48f8403916a0cd7b1d870f9089866aa`  
		Last Modified: Fri, 31 Jan 2025 02:47:44 GMT  
		Size: 18.4 MB (18432713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5d4a5029c50ca81c6c035b53fbd87a52e979c51b94471102c395f1ca6ac7b1`  
		Last Modified: Fri, 31 Jan 2025 03:19:09 GMT  
		Size: 234.5 MB (234537830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cac7095c2b17adc335169c93969115865dfcf1e601c57bbf0f705d71fd00bc`  
		Last Modified: Fri, 31 Jan 2025 03:19:04 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:1e291d03919b587cabf9f730140d9809704743e637fc00f145ba11df1c5d40c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4205830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5f149bc33d6edf48c568539c22f24d94501e3803dad4b7a7f59116d2ead599`

```dockerfile
```

-	Layers:
	-	`sha256:e209bee63b673072ef25d68974d939654f21457014fca4bc205240a4d4352721`  
		Last Modified: Fri, 31 Jan 2025 03:19:04 GMT  
		Size: 4.2 MB (4186627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37580501d8e67e8d8b5084ab8728f2d1210e57fd4e6093046f62e4702033b505`  
		Last Modified: Fri, 31 Jan 2025 03:19:03 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:cf4b2bb35b45817d735b15e365ab3c2bf31cf4c2ceb694de62e725b088fc3f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.4 MB (349429634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fbb98487a3e6ee93cc8e9441adea1569a1ea8652c05d5c8607c6c052e76b3a8`
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
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
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
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370f8a7b7cf214f61cc1a2546f38e47ba749cb698659b51aa07e70fcecbd7e2f`  
		Last Modified: Wed, 22 Jan 2025 20:53:10 GMT  
		Size: 17.0 MB (16982856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa15e6520d7251000b73f383a2c02ff5f96e0e795daa58fcb86fd6dbecba8106`  
		Last Modified: Wed, 22 Jan 2025 20:53:11 GMT  
		Size: 53.8 MB (53816345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c30897c18d1b536032f6028fe4eaa61fc240ac0410f58674601dace64a2d760`  
		Last Modified: Wed, 22 Jan 2025 20:53:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134a80a14402716f85166426a6c66a2cd42f08cfaa3717a5d71a96df25cd1589`  
		Last Modified: Wed, 22 Jan 2025 20:53:10 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118dc07b441e024431f76daf9cc5eef2f5ff138efab3f6685c4fbdcbe47f69f2`  
		Last Modified: Thu, 23 Jan 2025 02:03:09 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135b96f80d9968468d7a0c0be0cb140df633b0cc4454207548b3916afdb3e061`  
		Last Modified: Thu, 23 Jan 2025 02:03:10 GMT  
		Size: 15.2 MB (15181236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f64449a5834e236084ea0a4a4fbac3f3c32fef49a1eac9d76ba93b4710179c8`  
		Last Modified: Thu, 23 Jan 2025 04:04:46 GMT  
		Size: 234.6 MB (234553572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2ae097196b641e3a2ceef1432ce728955c08c96338ce6face41253503d2b34`  
		Last Modified: Thu, 23 Jan 2025 04:04:40 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:c4d1e232db2f684bf93cfa670ab03925e5f4d8bd7f73426e17e47794ab6707e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4203317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ff3231ce51259e922d4f44876dc934615fe3b2885d3310702ea940f417c1a6`

```dockerfile
```

-	Layers:
	-	`sha256:d1b4485c6d41818e8fb35bca7eddca9f33c38836d1c4d48cd77593b51885690e`  
		Last Modified: Thu, 23 Jan 2025 04:04:40 GMT  
		Size: 4.2 MB (4184090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25b5bb497423f931aacb5940954f7d182828aadd531a3282fc10c221e0ef44f4`  
		Last Modified: Thu, 23 Jan 2025 04:04:40 GMT  
		Size: 19.2 KB (19227 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:13bba8a0e36a966d56e15173f266410e89df7a02d4bec0a3ef9b64423065d657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.1 MB (356127371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b561782028a7c7cff8e57d5f3c3a1703c6d8fcd55ddf1d5a5e757be42576d718`
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
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
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
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb08691d29d174440113fb3d94aec487ff706b850acfce25b3870b67886fdc90`  
		Last Modified: Tue, 03 Dec 2024 04:44:50 GMT  
		Size: 18.8 MB (18845906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69b2fc5d3ba84e6de2d85f7e2d3e79aeb0199b6b959db9dfb1096f73e0d7441`  
		Last Modified: Wed, 22 Jan 2025 18:31:46 GMT  
		Size: 52.2 MB (52170489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7e296b62d1e3ea74e89331c7fe00e13e4ec9b10979b9b44c187cf58235e52`  
		Last Modified: Wed, 22 Jan 2025 18:31:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83acec15d6612c113f691aa6046970a02a05c2531417015cdf20954ea9186b64`  
		Last Modified: Wed, 22 Jan 2025 18:31:45 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb9ec006f44e057f6e3ce2c629e488f8fdd854385f6c4c5163b12f919c8368f`  
		Last Modified: Wed, 22 Jan 2025 21:54:33 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5963ebeba988c2be072f7be5b475b9b5eb304f7ccf6c1c042e78f460ac537c24`  
		Last Modified: Wed, 22 Jan 2025 21:54:34 GMT  
		Size: 16.1 MB (16145052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcdf36274e93607638f0293d1e72a99ae6e30ca967f244afbcd600bf20d112f`  
		Last Modified: Wed, 22 Jan 2025 22:25:11 GMT  
		Size: 234.6 MB (234574149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2b36263da4c5c485517df4274617f2071d46cf986a404e8ea777e0e03bf7d9`  
		Last Modified: Wed, 22 Jan 2025 22:25:01 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3` - unknown; unknown

```console
$ docker pull geonetwork@sha256:79094e512442540f6d3f6286da173a1a85291feb6bd4d83dba61b615d87c75bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4204706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e09cf848b5ac9205a2fb6f69f1f1d4294efdad20e4f3c82aea02b522c2409`

```dockerfile
```

-	Layers:
	-	`sha256:6b329a0ec56a883a69e813891621a5e4add3865cbec10736654f8a9dce3f439f`  
		Last Modified: Wed, 22 Jan 2025 22:25:01 GMT  
		Size: 4.2 MB (4185533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f3fb71482862490f330e4a6ab929f41c24415f96f7cdab9c5781210a13625c0`  
		Last Modified: Wed, 22 Jan 2025 22:25:00 GMT  
		Size: 19.2 KB (19173 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3-postgres`

```console
$ docker pull geonetwork@sha256:80553b2dda3dcaf3c6d34b5f58f97f3666997829b9aaba9783ece1fc76ff7d54
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
$ docker pull geonetwork@sha256:61516ea6e7063253ccc2af77006bb4bb5cec5660350d6752883338a289f12a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367320215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f046f6f410dcbfab73d486d28f8897c6fb7196e05b0f3aa38a5d12cc692a85`
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
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
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
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f958f4e5767ee8cbfae4e4235c527c4131d6057a66355b614d894f1a0a4c17e`  
		Last Modified: Fri, 31 Jan 2025 01:29:51 GMT  
		Size: 17.0 MB (16962286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85bc3172399be429690fb80a0e29a164e651fe7c79af0a116a832cd9a452af4`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 54.7 MB (54722132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91352bec832ebb8bbef001417c3390a864883828fd1ea6d0304aa3540c5fcf42`  
		Last Modified: Fri, 31 Jan 2025 01:29:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b0a778c4b3fa7cb96f64bd0815f368a43af46f5675c73473ff21260609ed34`  
		Last Modified: Fri, 31 Jan 2025 01:29:50 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54052fc5a57ccf09bd3a191cac02a0119f6e89611349406e744f5300feac29c3`  
		Last Modified: Fri, 31 Jan 2025 02:16:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdf6e1898878b79d3b2e2b6f632ee60e22a70625ca700ad8b32bff5cba8a335`  
		Last Modified: Fri, 31 Jan 2025 02:16:44 GMT  
		Size: 17.5 MB (17498782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0739d463f54d427403a7a38f46c6949c6bf4e071eb4df931ad505b6c8ea30a2`  
		Last Modified: Fri, 31 Jan 2025 03:13:29 GMT  
		Size: 234.5 MB (234549547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801162cd369643515aa88b33493b35c8f42d1bf959b537c6546a55b3b89762cc`  
		Last Modified: Fri, 31 Jan 2025 03:13:22 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e6cc2ace4997d2c654233fbbc198113eb5c1b18bda68dababd926d1ccf65bf`  
		Last Modified: Fri, 31 Jan 2025 04:09:36 GMT  
		Size: 13.8 MB (13829135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945eaf7c2e95e728e3f9ec60c25da31bff43efa6d7e89d1b65f450d0e5f851dc`  
		Last Modified: Fri, 31 Jan 2025 04:09:35 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a097d4f759827861e3f7044e8504ab8873157e2a90759651466c46ba8c7101`  
		Last Modified: Fri, 31 Jan 2025 04:09:35 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a303e47c9967d6ceced54a6232ce31796d94296b5ab0a3206b472f92157939`  
		Last Modified: Fri, 31 Jan 2025 04:09:35 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:6b5b008b322e9e3f7268db58256adf7ad034131b878ee04117a3d37268c2c3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5745604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97f2ac356654319efbc98c0866c10aea4866fb4d01c104a5bc3018818fb6b98`

```dockerfile
```

-	Layers:
	-	`sha256:833da23cd368bcb03556f236a4fe22d66e53264ac87c56fc71c6b86c7b3eb209`  
		Last Modified: Fri, 31 Jan 2025 04:09:36 GMT  
		Size: 5.7 MB (5722744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf6dc8c14e8d8feea68b9d7bf9aa24940a9e8b5b442e8b94eba8535b4d2fd32e`  
		Last Modified: Fri, 31 Jan 2025 04:09:35 GMT  
		Size: 22.9 KB (22860 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:c2cec46769a2e11c220282de0eeedfcf3eb432c356a4b1f5b45a11766f32612d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.2 MB (359167441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b91ce1a88d1999f378b4bc67bae037240bc539e0af7f18508bb40b2fec44ddd`
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
ADD file:786ab064bf2d82faf7ca3fbb6c2e6983bbdb3228800d6d64e5dec4a67f778a7a in / 
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
	-	`sha256:b25adda5718ef4d96696ce8f0e58cde58fbe9977456036f84293bba8f26c5567`  
		Last Modified: Tue, 19 Nov 2024 17:38:39 GMT  
		Size: 26.9 MB (26869639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a5eb6a2db557356b46da4a6e217de6ed249bca2210cdccd1a0430c803e8512`  
		Last Modified: Tue, 03 Dec 2024 07:45:24 GMT  
		Size: 16.3 MB (16299908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa44b4fc4334a27557f3a631a9438ca5ce8656e161b39e45ab2440b2d7aead1`  
		Last Modified: Fri, 31 Jan 2025 01:32:09 GMT  
		Size: 50.1 MB (50109725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d811e0afab0f1ffd85e4671f4a476cb71cbde9841a85d24ae45a1ad7b42f60a`  
		Last Modified: Fri, 31 Jan 2025 01:32:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd08c17ad27b6137eb1f45f5f4617278e0a8b0c6ef2a13aa6a4fee9ab4777e26`  
		Last Modified: Fri, 31 Jan 2025 01:32:07 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59de26424799b6d39429ee18f2ea2fd2556807bdfa7356ee01c8bbfdd836544`  
		Last Modified: Fri, 31 Jan 2025 02:47:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771e8c9a5f56f2bac23ee6b2b3ac39b5c48f8403916a0cd7b1d870f9089866aa`  
		Last Modified: Fri, 31 Jan 2025 02:47:44 GMT  
		Size: 18.4 MB (18432713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5d4a5029c50ca81c6c035b53fbd87a52e979c51b94471102c395f1ca6ac7b1`  
		Last Modified: Fri, 31 Jan 2025 03:19:09 GMT  
		Size: 234.5 MB (234537830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cac7095c2b17adc335169c93969115865dfcf1e601c57bbf0f705d71fd00bc`  
		Last Modified: Fri, 31 Jan 2025 03:19:04 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f54edda13a9e4feb68bb65745a76d765bde1150bb28378dba31d44cb5af203`  
		Last Modified: Fri, 31 Jan 2025 04:09:35 GMT  
		Size: 12.9 MB (12911260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda593896a9c8dc74857ae8206e1e0f548bc5991187c2445e182cebf8a17c1b3`  
		Last Modified: Fri, 31 Jan 2025 04:09:34 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c9cba22107ee5109964d57d12f90c355ee3a10155f6f1e479f64f274aac67a`  
		Last Modified: Fri, 31 Jan 2025 04:09:34 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0b285fffbbfd7283dc876652c615081d32d1af4bec2d2804e7569253fc4bd2`  
		Last Modified: Fri, 31 Jan 2025 04:09:35 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:428fbb6410735711f2ba89b7e570d213e3b2ff6dcade96afa401268d50c92657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09042f03c1dab45d38fea36ded5159977e13b82bc549e33acb44363096351a92`

```dockerfile
```

-	Layers:
	-	`sha256:8f09a3586e6961a791dddabae310250eeeadf6ada768e1a533acd3b10d749caa`  
		Last Modified: Fri, 31 Jan 2025 04:09:34 GMT  
		Size: 5.7 MB (5725767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:919fd879ae32b702f65f9038c31e48de786cd6d7afb1a9fba976b8ba44a961cc`  
		Last Modified: Fri, 31 Jan 2025 04:09:34 GMT  
		Size: 22.9 KB (22941 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:835cde54ff70414c918ec80c13f11bee514fd1761579a3c7ed11135b42bf24cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.2 MB (363242978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e455ebf09ba0bbbb13d36564150932a3b1c4f30f3f2a1594934a620a6df9f2ed`
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
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
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
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370f8a7b7cf214f61cc1a2546f38e47ba749cb698659b51aa07e70fcecbd7e2f`  
		Last Modified: Wed, 22 Jan 2025 20:53:10 GMT  
		Size: 17.0 MB (16982856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa15e6520d7251000b73f383a2c02ff5f96e0e795daa58fcb86fd6dbecba8106`  
		Last Modified: Wed, 22 Jan 2025 20:53:11 GMT  
		Size: 53.8 MB (53816345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c30897c18d1b536032f6028fe4eaa61fc240ac0410f58674601dace64a2d760`  
		Last Modified: Wed, 22 Jan 2025 20:53:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134a80a14402716f85166426a6c66a2cd42f08cfaa3717a5d71a96df25cd1589`  
		Last Modified: Wed, 22 Jan 2025 20:53:10 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118dc07b441e024431f76daf9cc5eef2f5ff138efab3f6685c4fbdcbe47f69f2`  
		Last Modified: Thu, 23 Jan 2025 02:03:09 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135b96f80d9968468d7a0c0be0cb140df633b0cc4454207548b3916afdb3e061`  
		Last Modified: Thu, 23 Jan 2025 02:03:10 GMT  
		Size: 15.2 MB (15181236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f64449a5834e236084ea0a4a4fbac3f3c32fef49a1eac9d76ba93b4710179c8`  
		Last Modified: Thu, 23 Jan 2025 04:04:46 GMT  
		Size: 234.6 MB (234553572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2ae097196b641e3a2ceef1432ce728955c08c96338ce6face41253503d2b34`  
		Last Modified: Thu, 23 Jan 2025 04:04:40 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7574f7f01d1438f41a3dbcb2652e32133b38427f9c9afb5471ca36395ad2b168`  
		Last Modified: Thu, 23 Jan 2025 05:02:03 GMT  
		Size: 13.8 MB (13809932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f431470c2c6ede2086074f17c208b5471ba08028d6f7083a2feaaa6711c49983`  
		Last Modified: Thu, 23 Jan 2025 05:02:03 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9673c24d9a18b25beb6d7c5fc6eade0d7f7026561ea0b9a9a831dada7faab69f`  
		Last Modified: Thu, 23 Jan 2025 05:02:03 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3007ea91d015e2e4882bfc55367c34610b7c2ff6b785432a03d4c79bdd8c2410`  
		Last Modified: Thu, 23 Jan 2025 05:02:03 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:5367cc256e947e14844049f7cc3d219645f96b953768744d7e9ee437d7861a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5753505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d56349c64c1ba725afbc2480ce1269cb9326b5280a7c5fa074e17332eab88c`

```dockerfile
```

-	Layers:
	-	`sha256:8ee0a74237992b7b988cbf222e2df2bcf2e6cb40f82fe5604da6f154a151f340`  
		Last Modified: Thu, 23 Jan 2025 05:02:02 GMT  
		Size: 5.7 MB (5730538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b29bc55361aeafd24558df2774d2c14298e40cdb61938d1fcb6b0c8b4af1d57`  
		Last Modified: Thu, 23 Jan 2025 05:02:01 GMT  
		Size: 23.0 KB (22967 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:8145bb343e9d0cf9dd75fe7a9bebfcce01f033c5f3979f2284ac743b891de52c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.5 MB (370474528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52db5f06cd19c80f775d949810deb4e05f5442a100b07a68b0e341de924b9f30`
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
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
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
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb08691d29d174440113fb3d94aec487ff706b850acfce25b3870b67886fdc90`  
		Last Modified: Tue, 03 Dec 2024 04:44:50 GMT  
		Size: 18.8 MB (18845906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69b2fc5d3ba84e6de2d85f7e2d3e79aeb0199b6b959db9dfb1096f73e0d7441`  
		Last Modified: Wed, 22 Jan 2025 18:31:46 GMT  
		Size: 52.2 MB (52170489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7e296b62d1e3ea74e89331c7fe00e13e4ec9b10979b9b44c187cf58235e52`  
		Last Modified: Wed, 22 Jan 2025 18:31:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83acec15d6612c113f691aa6046970a02a05c2531417015cdf20954ea9186b64`  
		Last Modified: Wed, 22 Jan 2025 18:31:45 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb9ec006f44e057f6e3ce2c629e488f8fdd854385f6c4c5163b12f919c8368f`  
		Last Modified: Wed, 22 Jan 2025 21:54:33 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5963ebeba988c2be072f7be5b475b9b5eb304f7ccf6c1c042e78f460ac537c24`  
		Last Modified: Wed, 22 Jan 2025 21:54:34 GMT  
		Size: 16.1 MB (16145052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcdf36274e93607638f0293d1e72a99ae6e30ca967f244afbcd600bf20d112f`  
		Last Modified: Wed, 22 Jan 2025 22:25:11 GMT  
		Size: 234.6 MB (234574149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2b36263da4c5c485517df4274617f2071d46cf986a404e8ea777e0e03bf7d9`  
		Last Modified: Wed, 22 Jan 2025 22:25:01 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e5645a831ba474385d17d488a16dad8bcc97feb775b5d12d1febf7693c4339`  
		Last Modified: Wed, 22 Jan 2025 23:10:30 GMT  
		Size: 14.3 MB (14343745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d116271cf9b42857b6fe081dcb50536cbabdf55908094e4c069ed9fd6b667ee`  
		Last Modified: Wed, 22 Jan 2025 23:10:29 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff09d1cb7c1c4330a22e8ab945cae9d434dbde756bdccd24483c0e68739f59f`  
		Last Modified: Wed, 22 Jan 2025 23:10:29 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b946049c4e63e186c2ce2daaf1ac691908ead6415039758edbe6c13fb7c694`  
		Last Modified: Wed, 22 Jan 2025 23:10:29 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:339f65d1b2f7c818958c1f4eb74ce0a5627208d3bcba0bdaab980a9e33265c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5751574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd625da954d0148cf61510ca5cf018cef6639a366614c39210ada6c9ba474b3`

```dockerfile
```

-	Layers:
	-	`sha256:39ce5d4cb34ccb4e57c6d74d281367919860894b9742074341af4bdf44673af4`  
		Last Modified: Wed, 22 Jan 2025 23:10:29 GMT  
		Size: 5.7 MB (5728674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd18b169f9a599226e809afd057fb7afe93f3dc81af8648a67b7986988f60412`  
		Last Modified: Wed, 22 Jan 2025 23:10:28 GMT  
		Size: 22.9 KB (22900 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12`

```console
$ docker pull geonetwork@sha256:18fd80af67dfbb5ac858a7e3eb8c49a83c98e24d1baa8822394cbd10e0b9b85e
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
$ docker pull geonetwork@sha256:7a3e5ddad59927a808058315f648d4b0155de9c764457f2ef0eaab44d4762707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.5 MB (353487665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124873c0ed3953817f499bcf35b3babceb769c58b0ae6a2dd17d58f1e807b69a`
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
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
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
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f958f4e5767ee8cbfae4e4235c527c4131d6057a66355b614d894f1a0a4c17e`  
		Last Modified: Fri, 31 Jan 2025 01:29:51 GMT  
		Size: 17.0 MB (16962286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85bc3172399be429690fb80a0e29a164e651fe7c79af0a116a832cd9a452af4`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 54.7 MB (54722132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91352bec832ebb8bbef001417c3390a864883828fd1ea6d0304aa3540c5fcf42`  
		Last Modified: Fri, 31 Jan 2025 01:29:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b0a778c4b3fa7cb96f64bd0815f368a43af46f5675c73473ff21260609ed34`  
		Last Modified: Fri, 31 Jan 2025 01:29:50 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54052fc5a57ccf09bd3a191cac02a0119f6e89611349406e744f5300feac29c3`  
		Last Modified: Fri, 31 Jan 2025 02:16:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdf6e1898878b79d3b2e2b6f632ee60e22a70625ca700ad8b32bff5cba8a335`  
		Last Modified: Fri, 31 Jan 2025 02:16:44 GMT  
		Size: 17.5 MB (17498782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0739d463f54d427403a7a38f46c6949c6bf4e071eb4df931ad505b6c8ea30a2`  
		Last Modified: Fri, 31 Jan 2025 03:13:29 GMT  
		Size: 234.5 MB (234549547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801162cd369643515aa88b33493b35c8f42d1bf959b537c6546a55b3b89762cc`  
		Last Modified: Fri, 31 Jan 2025 03:13:22 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:582eca7c3d6b15a84faf1dc7a3852881d3dbec577c27d3caba0cbb04589532ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4201471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c43c19f72403f292a16acb32fd2a357d47a999bdc481f4d567782a43b018570`

```dockerfile
```

-	Layers:
	-	`sha256:b2a95fe06b52702501a8a2752ba4cd6bd33f0b736ae7348861da76fdea0e880c`  
		Last Modified: Fri, 31 Jan 2025 03:13:22 GMT  
		Size: 4.2 MB (4182336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71907960108916e6b067ee5773e40f204670660647e8c15ee07395735ee703b3`  
		Last Modified: Fri, 31 Jan 2025 03:13:21 GMT  
		Size: 19.1 KB (19135 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:27cca303f63cc4a6278c7d126582e35f676d89a757f3f09ddc51045d0d5947e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.3 MB (346252767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4b55cc593d835461d97f0c6f6a62d3a759da60241b93a1457f7ba11095d40c`
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
ADD file:786ab064bf2d82faf7ca3fbb6c2e6983bbdb3228800d6d64e5dec4a67f778a7a in / 
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
	-	`sha256:b25adda5718ef4d96696ce8f0e58cde58fbe9977456036f84293bba8f26c5567`  
		Last Modified: Tue, 19 Nov 2024 17:38:39 GMT  
		Size: 26.9 MB (26869639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a5eb6a2db557356b46da4a6e217de6ed249bca2210cdccd1a0430c803e8512`  
		Last Modified: Tue, 03 Dec 2024 07:45:24 GMT  
		Size: 16.3 MB (16299908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa44b4fc4334a27557f3a631a9438ca5ce8656e161b39e45ab2440b2d7aead1`  
		Last Modified: Fri, 31 Jan 2025 01:32:09 GMT  
		Size: 50.1 MB (50109725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d811e0afab0f1ffd85e4671f4a476cb71cbde9841a85d24ae45a1ad7b42f60a`  
		Last Modified: Fri, 31 Jan 2025 01:32:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd08c17ad27b6137eb1f45f5f4617278e0a8b0c6ef2a13aa6a4fee9ab4777e26`  
		Last Modified: Fri, 31 Jan 2025 01:32:07 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59de26424799b6d39429ee18f2ea2fd2556807bdfa7356ee01c8bbfdd836544`  
		Last Modified: Fri, 31 Jan 2025 02:47:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771e8c9a5f56f2bac23ee6b2b3ac39b5c48f8403916a0cd7b1d870f9089866aa`  
		Last Modified: Fri, 31 Jan 2025 02:47:44 GMT  
		Size: 18.4 MB (18432713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5d4a5029c50ca81c6c035b53fbd87a52e979c51b94471102c395f1ca6ac7b1`  
		Last Modified: Fri, 31 Jan 2025 03:19:09 GMT  
		Size: 234.5 MB (234537830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cac7095c2b17adc335169c93969115865dfcf1e601c57bbf0f705d71fd00bc`  
		Last Modified: Fri, 31 Jan 2025 03:19:04 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:1e291d03919b587cabf9f730140d9809704743e637fc00f145ba11df1c5d40c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4205830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5f149bc33d6edf48c568539c22f24d94501e3803dad4b7a7f59116d2ead599`

```dockerfile
```

-	Layers:
	-	`sha256:e209bee63b673072ef25d68974d939654f21457014fca4bc205240a4d4352721`  
		Last Modified: Fri, 31 Jan 2025 03:19:04 GMT  
		Size: 4.2 MB (4186627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37580501d8e67e8d8b5084ab8728f2d1210e57fd4e6093046f62e4702033b505`  
		Last Modified: Fri, 31 Jan 2025 03:19:03 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:cf4b2bb35b45817d735b15e365ab3c2bf31cf4c2ceb694de62e725b088fc3f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.4 MB (349429634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fbb98487a3e6ee93cc8e9441adea1569a1ea8652c05d5c8607c6c052e76b3a8`
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
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
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
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370f8a7b7cf214f61cc1a2546f38e47ba749cb698659b51aa07e70fcecbd7e2f`  
		Last Modified: Wed, 22 Jan 2025 20:53:10 GMT  
		Size: 17.0 MB (16982856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa15e6520d7251000b73f383a2c02ff5f96e0e795daa58fcb86fd6dbecba8106`  
		Last Modified: Wed, 22 Jan 2025 20:53:11 GMT  
		Size: 53.8 MB (53816345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c30897c18d1b536032f6028fe4eaa61fc240ac0410f58674601dace64a2d760`  
		Last Modified: Wed, 22 Jan 2025 20:53:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134a80a14402716f85166426a6c66a2cd42f08cfaa3717a5d71a96df25cd1589`  
		Last Modified: Wed, 22 Jan 2025 20:53:10 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118dc07b441e024431f76daf9cc5eef2f5ff138efab3f6685c4fbdcbe47f69f2`  
		Last Modified: Thu, 23 Jan 2025 02:03:09 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135b96f80d9968468d7a0c0be0cb140df633b0cc4454207548b3916afdb3e061`  
		Last Modified: Thu, 23 Jan 2025 02:03:10 GMT  
		Size: 15.2 MB (15181236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f64449a5834e236084ea0a4a4fbac3f3c32fef49a1eac9d76ba93b4710179c8`  
		Last Modified: Thu, 23 Jan 2025 04:04:46 GMT  
		Size: 234.6 MB (234553572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2ae097196b641e3a2ceef1432ce728955c08c96338ce6face41253503d2b34`  
		Last Modified: Thu, 23 Jan 2025 04:04:40 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:c4d1e232db2f684bf93cfa670ab03925e5f4d8bd7f73426e17e47794ab6707e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4203317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ff3231ce51259e922d4f44876dc934615fe3b2885d3310702ea940f417c1a6`

```dockerfile
```

-	Layers:
	-	`sha256:d1b4485c6d41818e8fb35bca7eddca9f33c38836d1c4d48cd77593b51885690e`  
		Last Modified: Thu, 23 Jan 2025 04:04:40 GMT  
		Size: 4.2 MB (4184090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25b5bb497423f931aacb5940954f7d182828aadd531a3282fc10c221e0ef44f4`  
		Last Modified: Thu, 23 Jan 2025 04:04:40 GMT  
		Size: 19.2 KB (19227 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:13bba8a0e36a966d56e15173f266410e89df7a02d4bec0a3ef9b64423065d657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.1 MB (356127371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b561782028a7c7cff8e57d5f3c3a1703c6d8fcd55ddf1d5a5e757be42576d718`
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
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
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
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb08691d29d174440113fb3d94aec487ff706b850acfce25b3870b67886fdc90`  
		Last Modified: Tue, 03 Dec 2024 04:44:50 GMT  
		Size: 18.8 MB (18845906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69b2fc5d3ba84e6de2d85f7e2d3e79aeb0199b6b959db9dfb1096f73e0d7441`  
		Last Modified: Wed, 22 Jan 2025 18:31:46 GMT  
		Size: 52.2 MB (52170489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7e296b62d1e3ea74e89331c7fe00e13e4ec9b10979b9b44c187cf58235e52`  
		Last Modified: Wed, 22 Jan 2025 18:31:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83acec15d6612c113f691aa6046970a02a05c2531417015cdf20954ea9186b64`  
		Last Modified: Wed, 22 Jan 2025 18:31:45 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb9ec006f44e057f6e3ce2c629e488f8fdd854385f6c4c5163b12f919c8368f`  
		Last Modified: Wed, 22 Jan 2025 21:54:33 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5963ebeba988c2be072f7be5b475b9b5eb304f7ccf6c1c042e78f460ac537c24`  
		Last Modified: Wed, 22 Jan 2025 21:54:34 GMT  
		Size: 16.1 MB (16145052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcdf36274e93607638f0293d1e72a99ae6e30ca967f244afbcd600bf20d112f`  
		Last Modified: Wed, 22 Jan 2025 22:25:11 GMT  
		Size: 234.6 MB (234574149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2b36263da4c5c485517df4274617f2071d46cf986a404e8ea777e0e03bf7d9`  
		Last Modified: Wed, 22 Jan 2025 22:25:01 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:79094e512442540f6d3f6286da173a1a85291feb6bd4d83dba61b615d87c75bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4204706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e09cf848b5ac9205a2fb6f69f1f1d4294efdad20e4f3c82aea02b522c2409`

```dockerfile
```

-	Layers:
	-	`sha256:6b329a0ec56a883a69e813891621a5e4add3865cbec10736654f8a9dce3f439f`  
		Last Modified: Wed, 22 Jan 2025 22:25:01 GMT  
		Size: 4.2 MB (4185533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f3fb71482862490f330e4a6ab929f41c24415f96f7cdab9c5781210a13625c0`  
		Last Modified: Wed, 22 Jan 2025 22:25:00 GMT  
		Size: 19.2 KB (19173 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12-postgres`

```console
$ docker pull geonetwork@sha256:80553b2dda3dcaf3c6d34b5f58f97f3666997829b9aaba9783ece1fc76ff7d54
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
$ docker pull geonetwork@sha256:61516ea6e7063253ccc2af77006bb4bb5cec5660350d6752883338a289f12a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367320215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f046f6f410dcbfab73d486d28f8897c6fb7196e05b0f3aa38a5d12cc692a85`
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
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
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
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f958f4e5767ee8cbfae4e4235c527c4131d6057a66355b614d894f1a0a4c17e`  
		Last Modified: Fri, 31 Jan 2025 01:29:51 GMT  
		Size: 17.0 MB (16962286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85bc3172399be429690fb80a0e29a164e651fe7c79af0a116a832cd9a452af4`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 54.7 MB (54722132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91352bec832ebb8bbef001417c3390a864883828fd1ea6d0304aa3540c5fcf42`  
		Last Modified: Fri, 31 Jan 2025 01:29:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b0a778c4b3fa7cb96f64bd0815f368a43af46f5675c73473ff21260609ed34`  
		Last Modified: Fri, 31 Jan 2025 01:29:50 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54052fc5a57ccf09bd3a191cac02a0119f6e89611349406e744f5300feac29c3`  
		Last Modified: Fri, 31 Jan 2025 02:16:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdf6e1898878b79d3b2e2b6f632ee60e22a70625ca700ad8b32bff5cba8a335`  
		Last Modified: Fri, 31 Jan 2025 02:16:44 GMT  
		Size: 17.5 MB (17498782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0739d463f54d427403a7a38f46c6949c6bf4e071eb4df931ad505b6c8ea30a2`  
		Last Modified: Fri, 31 Jan 2025 03:13:29 GMT  
		Size: 234.5 MB (234549547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801162cd369643515aa88b33493b35c8f42d1bf959b537c6546a55b3b89762cc`  
		Last Modified: Fri, 31 Jan 2025 03:13:22 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e6cc2ace4997d2c654233fbbc198113eb5c1b18bda68dababd926d1ccf65bf`  
		Last Modified: Fri, 31 Jan 2025 04:09:36 GMT  
		Size: 13.8 MB (13829135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945eaf7c2e95e728e3f9ec60c25da31bff43efa6d7e89d1b65f450d0e5f851dc`  
		Last Modified: Fri, 31 Jan 2025 04:09:35 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a097d4f759827861e3f7044e8504ab8873157e2a90759651466c46ba8c7101`  
		Last Modified: Fri, 31 Jan 2025 04:09:35 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a303e47c9967d6ceced54a6232ce31796d94296b5ab0a3206b472f92157939`  
		Last Modified: Fri, 31 Jan 2025 04:09:35 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:6b5b008b322e9e3f7268db58256adf7ad034131b878ee04117a3d37268c2c3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5745604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97f2ac356654319efbc98c0866c10aea4866fb4d01c104a5bc3018818fb6b98`

```dockerfile
```

-	Layers:
	-	`sha256:833da23cd368bcb03556f236a4fe22d66e53264ac87c56fc71c6b86c7b3eb209`  
		Last Modified: Fri, 31 Jan 2025 04:09:36 GMT  
		Size: 5.7 MB (5722744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf6dc8c14e8d8feea68b9d7bf9aa24940a9e8b5b442e8b94eba8535b4d2fd32e`  
		Last Modified: Fri, 31 Jan 2025 04:09:35 GMT  
		Size: 22.9 KB (22860 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:c2cec46769a2e11c220282de0eeedfcf3eb432c356a4b1f5b45a11766f32612d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.2 MB (359167441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b91ce1a88d1999f378b4bc67bae037240bc539e0af7f18508bb40b2fec44ddd`
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
ADD file:786ab064bf2d82faf7ca3fbb6c2e6983bbdb3228800d6d64e5dec4a67f778a7a in / 
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
	-	`sha256:b25adda5718ef4d96696ce8f0e58cde58fbe9977456036f84293bba8f26c5567`  
		Last Modified: Tue, 19 Nov 2024 17:38:39 GMT  
		Size: 26.9 MB (26869639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a5eb6a2db557356b46da4a6e217de6ed249bca2210cdccd1a0430c803e8512`  
		Last Modified: Tue, 03 Dec 2024 07:45:24 GMT  
		Size: 16.3 MB (16299908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa44b4fc4334a27557f3a631a9438ca5ce8656e161b39e45ab2440b2d7aead1`  
		Last Modified: Fri, 31 Jan 2025 01:32:09 GMT  
		Size: 50.1 MB (50109725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d811e0afab0f1ffd85e4671f4a476cb71cbde9841a85d24ae45a1ad7b42f60a`  
		Last Modified: Fri, 31 Jan 2025 01:32:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd08c17ad27b6137eb1f45f5f4617278e0a8b0c6ef2a13aa6a4fee9ab4777e26`  
		Last Modified: Fri, 31 Jan 2025 01:32:07 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59de26424799b6d39429ee18f2ea2fd2556807bdfa7356ee01c8bbfdd836544`  
		Last Modified: Fri, 31 Jan 2025 02:47:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771e8c9a5f56f2bac23ee6b2b3ac39b5c48f8403916a0cd7b1d870f9089866aa`  
		Last Modified: Fri, 31 Jan 2025 02:47:44 GMT  
		Size: 18.4 MB (18432713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5d4a5029c50ca81c6c035b53fbd87a52e979c51b94471102c395f1ca6ac7b1`  
		Last Modified: Fri, 31 Jan 2025 03:19:09 GMT  
		Size: 234.5 MB (234537830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cac7095c2b17adc335169c93969115865dfcf1e601c57bbf0f705d71fd00bc`  
		Last Modified: Fri, 31 Jan 2025 03:19:04 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f54edda13a9e4feb68bb65745a76d765bde1150bb28378dba31d44cb5af203`  
		Last Modified: Fri, 31 Jan 2025 04:09:35 GMT  
		Size: 12.9 MB (12911260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda593896a9c8dc74857ae8206e1e0f548bc5991187c2445e182cebf8a17c1b3`  
		Last Modified: Fri, 31 Jan 2025 04:09:34 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c9cba22107ee5109964d57d12f90c355ee3a10155f6f1e479f64f274aac67a`  
		Last Modified: Fri, 31 Jan 2025 04:09:34 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0b285fffbbfd7283dc876652c615081d32d1af4bec2d2804e7569253fc4bd2`  
		Last Modified: Fri, 31 Jan 2025 04:09:35 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:428fbb6410735711f2ba89b7e570d213e3b2ff6dcade96afa401268d50c92657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09042f03c1dab45d38fea36ded5159977e13b82bc549e33acb44363096351a92`

```dockerfile
```

-	Layers:
	-	`sha256:8f09a3586e6961a791dddabae310250eeeadf6ada768e1a533acd3b10d749caa`  
		Last Modified: Fri, 31 Jan 2025 04:09:34 GMT  
		Size: 5.7 MB (5725767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:919fd879ae32b702f65f9038c31e48de786cd6d7afb1a9fba976b8ba44a961cc`  
		Last Modified: Fri, 31 Jan 2025 04:09:34 GMT  
		Size: 22.9 KB (22941 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:835cde54ff70414c918ec80c13f11bee514fd1761579a3c7ed11135b42bf24cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.2 MB (363242978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e455ebf09ba0bbbb13d36564150932a3b1c4f30f3f2a1594934a620a6df9f2ed`
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
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
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
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370f8a7b7cf214f61cc1a2546f38e47ba749cb698659b51aa07e70fcecbd7e2f`  
		Last Modified: Wed, 22 Jan 2025 20:53:10 GMT  
		Size: 17.0 MB (16982856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa15e6520d7251000b73f383a2c02ff5f96e0e795daa58fcb86fd6dbecba8106`  
		Last Modified: Wed, 22 Jan 2025 20:53:11 GMT  
		Size: 53.8 MB (53816345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c30897c18d1b536032f6028fe4eaa61fc240ac0410f58674601dace64a2d760`  
		Last Modified: Wed, 22 Jan 2025 20:53:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134a80a14402716f85166426a6c66a2cd42f08cfaa3717a5d71a96df25cd1589`  
		Last Modified: Wed, 22 Jan 2025 20:53:10 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118dc07b441e024431f76daf9cc5eef2f5ff138efab3f6685c4fbdcbe47f69f2`  
		Last Modified: Thu, 23 Jan 2025 02:03:09 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135b96f80d9968468d7a0c0be0cb140df633b0cc4454207548b3916afdb3e061`  
		Last Modified: Thu, 23 Jan 2025 02:03:10 GMT  
		Size: 15.2 MB (15181236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f64449a5834e236084ea0a4a4fbac3f3c32fef49a1eac9d76ba93b4710179c8`  
		Last Modified: Thu, 23 Jan 2025 04:04:46 GMT  
		Size: 234.6 MB (234553572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2ae097196b641e3a2ceef1432ce728955c08c96338ce6face41253503d2b34`  
		Last Modified: Thu, 23 Jan 2025 04:04:40 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7574f7f01d1438f41a3dbcb2652e32133b38427f9c9afb5471ca36395ad2b168`  
		Last Modified: Thu, 23 Jan 2025 05:02:03 GMT  
		Size: 13.8 MB (13809932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f431470c2c6ede2086074f17c208b5471ba08028d6f7083a2feaaa6711c49983`  
		Last Modified: Thu, 23 Jan 2025 05:02:03 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9673c24d9a18b25beb6d7c5fc6eade0d7f7026561ea0b9a9a831dada7faab69f`  
		Last Modified: Thu, 23 Jan 2025 05:02:03 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3007ea91d015e2e4882bfc55367c34610b7c2ff6b785432a03d4c79bdd8c2410`  
		Last Modified: Thu, 23 Jan 2025 05:02:03 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:5367cc256e947e14844049f7cc3d219645f96b953768744d7e9ee437d7861a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5753505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d56349c64c1ba725afbc2480ce1269cb9326b5280a7c5fa074e17332eab88c`

```dockerfile
```

-	Layers:
	-	`sha256:8ee0a74237992b7b988cbf222e2df2bcf2e6cb40f82fe5604da6f154a151f340`  
		Last Modified: Thu, 23 Jan 2025 05:02:02 GMT  
		Size: 5.7 MB (5730538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b29bc55361aeafd24558df2774d2c14298e40cdb61938d1fcb6b0c8b4af1d57`  
		Last Modified: Thu, 23 Jan 2025 05:02:01 GMT  
		Size: 23.0 KB (22967 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:8145bb343e9d0cf9dd75fe7a9bebfcce01f033c5f3979f2284ac743b891de52c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.5 MB (370474528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52db5f06cd19c80f775d949810deb4e05f5442a100b07a68b0e341de924b9f30`
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
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
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
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb08691d29d174440113fb3d94aec487ff706b850acfce25b3870b67886fdc90`  
		Last Modified: Tue, 03 Dec 2024 04:44:50 GMT  
		Size: 18.8 MB (18845906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69b2fc5d3ba84e6de2d85f7e2d3e79aeb0199b6b959db9dfb1096f73e0d7441`  
		Last Modified: Wed, 22 Jan 2025 18:31:46 GMT  
		Size: 52.2 MB (52170489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7e296b62d1e3ea74e89331c7fe00e13e4ec9b10979b9b44c187cf58235e52`  
		Last Modified: Wed, 22 Jan 2025 18:31:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83acec15d6612c113f691aa6046970a02a05c2531417015cdf20954ea9186b64`  
		Last Modified: Wed, 22 Jan 2025 18:31:45 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb9ec006f44e057f6e3ce2c629e488f8fdd854385f6c4c5163b12f919c8368f`  
		Last Modified: Wed, 22 Jan 2025 21:54:33 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5963ebeba988c2be072f7be5b475b9b5eb304f7ccf6c1c042e78f460ac537c24`  
		Last Modified: Wed, 22 Jan 2025 21:54:34 GMT  
		Size: 16.1 MB (16145052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcdf36274e93607638f0293d1e72a99ae6e30ca967f244afbcd600bf20d112f`  
		Last Modified: Wed, 22 Jan 2025 22:25:11 GMT  
		Size: 234.6 MB (234574149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2b36263da4c5c485517df4274617f2071d46cf986a404e8ea777e0e03bf7d9`  
		Last Modified: Wed, 22 Jan 2025 22:25:01 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e5645a831ba474385d17d488a16dad8bcc97feb775b5d12d1febf7693c4339`  
		Last Modified: Wed, 22 Jan 2025 23:10:30 GMT  
		Size: 14.3 MB (14343745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d116271cf9b42857b6fe081dcb50536cbabdf55908094e4c069ed9fd6b667ee`  
		Last Modified: Wed, 22 Jan 2025 23:10:29 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff09d1cb7c1c4330a22e8ab945cae9d434dbde756bdccd24483c0e68739f59f`  
		Last Modified: Wed, 22 Jan 2025 23:10:29 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b946049c4e63e186c2ce2daaf1ac691908ead6415039758edbe6c13fb7c694`  
		Last Modified: Wed, 22 Jan 2025 23:10:29 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:339f65d1b2f7c818958c1f4eb74ce0a5627208d3bcba0bdaab980a9e33265c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5751574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd625da954d0148cf61510ca5cf018cef6639a366614c39210ada6c9ba474b3`

```dockerfile
```

-	Layers:
	-	`sha256:39ce5d4cb34ccb4e57c6d74d281367919860894b9742074341af4bdf44673af4`  
		Last Modified: Wed, 22 Jan 2025 23:10:29 GMT  
		Size: 5.7 MB (5728674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd18b169f9a599226e809afd057fb7afe93f3dc81af8648a67b7986988f60412`  
		Last Modified: Wed, 22 Jan 2025 23:10:28 GMT  
		Size: 22.9 KB (22900 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12.12`

```console
$ docker pull geonetwork@sha256:18fd80af67dfbb5ac858a7e3eb8c49a83c98e24d1baa8822394cbd10e0b9b85e
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
$ docker pull geonetwork@sha256:7a3e5ddad59927a808058315f648d4b0155de9c764457f2ef0eaab44d4762707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.5 MB (353487665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124873c0ed3953817f499bcf35b3babceb769c58b0ae6a2dd17d58f1e807b69a`
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
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
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
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f958f4e5767ee8cbfae4e4235c527c4131d6057a66355b614d894f1a0a4c17e`  
		Last Modified: Fri, 31 Jan 2025 01:29:51 GMT  
		Size: 17.0 MB (16962286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85bc3172399be429690fb80a0e29a164e651fe7c79af0a116a832cd9a452af4`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 54.7 MB (54722132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91352bec832ebb8bbef001417c3390a864883828fd1ea6d0304aa3540c5fcf42`  
		Last Modified: Fri, 31 Jan 2025 01:29:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b0a778c4b3fa7cb96f64bd0815f368a43af46f5675c73473ff21260609ed34`  
		Last Modified: Fri, 31 Jan 2025 01:29:50 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54052fc5a57ccf09bd3a191cac02a0119f6e89611349406e744f5300feac29c3`  
		Last Modified: Fri, 31 Jan 2025 02:16:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdf6e1898878b79d3b2e2b6f632ee60e22a70625ca700ad8b32bff5cba8a335`  
		Last Modified: Fri, 31 Jan 2025 02:16:44 GMT  
		Size: 17.5 MB (17498782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0739d463f54d427403a7a38f46c6949c6bf4e071eb4df931ad505b6c8ea30a2`  
		Last Modified: Fri, 31 Jan 2025 03:13:29 GMT  
		Size: 234.5 MB (234549547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801162cd369643515aa88b33493b35c8f42d1bf959b537c6546a55b3b89762cc`  
		Last Modified: Fri, 31 Jan 2025 03:13:22 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:582eca7c3d6b15a84faf1dc7a3852881d3dbec577c27d3caba0cbb04589532ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4201471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c43c19f72403f292a16acb32fd2a357d47a999bdc481f4d567782a43b018570`

```dockerfile
```

-	Layers:
	-	`sha256:b2a95fe06b52702501a8a2752ba4cd6bd33f0b736ae7348861da76fdea0e880c`  
		Last Modified: Fri, 31 Jan 2025 03:13:22 GMT  
		Size: 4.2 MB (4182336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71907960108916e6b067ee5773e40f204670660647e8c15ee07395735ee703b3`  
		Last Modified: Fri, 31 Jan 2025 03:13:21 GMT  
		Size: 19.1 KB (19135 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:27cca303f63cc4a6278c7d126582e35f676d89a757f3f09ddc51045d0d5947e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.3 MB (346252767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4b55cc593d835461d97f0c6f6a62d3a759da60241b93a1457f7ba11095d40c`
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
ADD file:786ab064bf2d82faf7ca3fbb6c2e6983bbdb3228800d6d64e5dec4a67f778a7a in / 
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
	-	`sha256:b25adda5718ef4d96696ce8f0e58cde58fbe9977456036f84293bba8f26c5567`  
		Last Modified: Tue, 19 Nov 2024 17:38:39 GMT  
		Size: 26.9 MB (26869639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a5eb6a2db557356b46da4a6e217de6ed249bca2210cdccd1a0430c803e8512`  
		Last Modified: Tue, 03 Dec 2024 07:45:24 GMT  
		Size: 16.3 MB (16299908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa44b4fc4334a27557f3a631a9438ca5ce8656e161b39e45ab2440b2d7aead1`  
		Last Modified: Fri, 31 Jan 2025 01:32:09 GMT  
		Size: 50.1 MB (50109725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d811e0afab0f1ffd85e4671f4a476cb71cbde9841a85d24ae45a1ad7b42f60a`  
		Last Modified: Fri, 31 Jan 2025 01:32:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd08c17ad27b6137eb1f45f5f4617278e0a8b0c6ef2a13aa6a4fee9ab4777e26`  
		Last Modified: Fri, 31 Jan 2025 01:32:07 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59de26424799b6d39429ee18f2ea2fd2556807bdfa7356ee01c8bbfdd836544`  
		Last Modified: Fri, 31 Jan 2025 02:47:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771e8c9a5f56f2bac23ee6b2b3ac39b5c48f8403916a0cd7b1d870f9089866aa`  
		Last Modified: Fri, 31 Jan 2025 02:47:44 GMT  
		Size: 18.4 MB (18432713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5d4a5029c50ca81c6c035b53fbd87a52e979c51b94471102c395f1ca6ac7b1`  
		Last Modified: Fri, 31 Jan 2025 03:19:09 GMT  
		Size: 234.5 MB (234537830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cac7095c2b17adc335169c93969115865dfcf1e601c57bbf0f705d71fd00bc`  
		Last Modified: Fri, 31 Jan 2025 03:19:04 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:1e291d03919b587cabf9f730140d9809704743e637fc00f145ba11df1c5d40c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4205830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5f149bc33d6edf48c568539c22f24d94501e3803dad4b7a7f59116d2ead599`

```dockerfile
```

-	Layers:
	-	`sha256:e209bee63b673072ef25d68974d939654f21457014fca4bc205240a4d4352721`  
		Last Modified: Fri, 31 Jan 2025 03:19:04 GMT  
		Size: 4.2 MB (4186627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37580501d8e67e8d8b5084ab8728f2d1210e57fd4e6093046f62e4702033b505`  
		Last Modified: Fri, 31 Jan 2025 03:19:03 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:cf4b2bb35b45817d735b15e365ab3c2bf31cf4c2ceb694de62e725b088fc3f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.4 MB (349429634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fbb98487a3e6ee93cc8e9441adea1569a1ea8652c05d5c8607c6c052e76b3a8`
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
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
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
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370f8a7b7cf214f61cc1a2546f38e47ba749cb698659b51aa07e70fcecbd7e2f`  
		Last Modified: Wed, 22 Jan 2025 20:53:10 GMT  
		Size: 17.0 MB (16982856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa15e6520d7251000b73f383a2c02ff5f96e0e795daa58fcb86fd6dbecba8106`  
		Last Modified: Wed, 22 Jan 2025 20:53:11 GMT  
		Size: 53.8 MB (53816345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c30897c18d1b536032f6028fe4eaa61fc240ac0410f58674601dace64a2d760`  
		Last Modified: Wed, 22 Jan 2025 20:53:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134a80a14402716f85166426a6c66a2cd42f08cfaa3717a5d71a96df25cd1589`  
		Last Modified: Wed, 22 Jan 2025 20:53:10 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118dc07b441e024431f76daf9cc5eef2f5ff138efab3f6685c4fbdcbe47f69f2`  
		Last Modified: Thu, 23 Jan 2025 02:03:09 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135b96f80d9968468d7a0c0be0cb140df633b0cc4454207548b3916afdb3e061`  
		Last Modified: Thu, 23 Jan 2025 02:03:10 GMT  
		Size: 15.2 MB (15181236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f64449a5834e236084ea0a4a4fbac3f3c32fef49a1eac9d76ba93b4710179c8`  
		Last Modified: Thu, 23 Jan 2025 04:04:46 GMT  
		Size: 234.6 MB (234553572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2ae097196b641e3a2ceef1432ce728955c08c96338ce6face41253503d2b34`  
		Last Modified: Thu, 23 Jan 2025 04:04:40 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:c4d1e232db2f684bf93cfa670ab03925e5f4d8bd7f73426e17e47794ab6707e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4203317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ff3231ce51259e922d4f44876dc934615fe3b2885d3310702ea940f417c1a6`

```dockerfile
```

-	Layers:
	-	`sha256:d1b4485c6d41818e8fb35bca7eddca9f33c38836d1c4d48cd77593b51885690e`  
		Last Modified: Thu, 23 Jan 2025 04:04:40 GMT  
		Size: 4.2 MB (4184090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25b5bb497423f931aacb5940954f7d182828aadd531a3282fc10c221e0ef44f4`  
		Last Modified: Thu, 23 Jan 2025 04:04:40 GMT  
		Size: 19.2 KB (19227 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:13bba8a0e36a966d56e15173f266410e89df7a02d4bec0a3ef9b64423065d657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.1 MB (356127371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b561782028a7c7cff8e57d5f3c3a1703c6d8fcd55ddf1d5a5e757be42576d718`
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
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
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
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb08691d29d174440113fb3d94aec487ff706b850acfce25b3870b67886fdc90`  
		Last Modified: Tue, 03 Dec 2024 04:44:50 GMT  
		Size: 18.8 MB (18845906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69b2fc5d3ba84e6de2d85f7e2d3e79aeb0199b6b959db9dfb1096f73e0d7441`  
		Last Modified: Wed, 22 Jan 2025 18:31:46 GMT  
		Size: 52.2 MB (52170489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7e296b62d1e3ea74e89331c7fe00e13e4ec9b10979b9b44c187cf58235e52`  
		Last Modified: Wed, 22 Jan 2025 18:31:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83acec15d6612c113f691aa6046970a02a05c2531417015cdf20954ea9186b64`  
		Last Modified: Wed, 22 Jan 2025 18:31:45 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb9ec006f44e057f6e3ce2c629e488f8fdd854385f6c4c5163b12f919c8368f`  
		Last Modified: Wed, 22 Jan 2025 21:54:33 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5963ebeba988c2be072f7be5b475b9b5eb304f7ccf6c1c042e78f460ac537c24`  
		Last Modified: Wed, 22 Jan 2025 21:54:34 GMT  
		Size: 16.1 MB (16145052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcdf36274e93607638f0293d1e72a99ae6e30ca967f244afbcd600bf20d112f`  
		Last Modified: Wed, 22 Jan 2025 22:25:11 GMT  
		Size: 234.6 MB (234574149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2b36263da4c5c485517df4274617f2071d46cf986a404e8ea777e0e03bf7d9`  
		Last Modified: Wed, 22 Jan 2025 22:25:01 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12` - unknown; unknown

```console
$ docker pull geonetwork@sha256:79094e512442540f6d3f6286da173a1a85291feb6bd4d83dba61b615d87c75bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4204706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e09cf848b5ac9205a2fb6f69f1f1d4294efdad20e4f3c82aea02b522c2409`

```dockerfile
```

-	Layers:
	-	`sha256:6b329a0ec56a883a69e813891621a5e4add3865cbec10736654f8a9dce3f439f`  
		Last Modified: Wed, 22 Jan 2025 22:25:01 GMT  
		Size: 4.2 MB (4185533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f3fb71482862490f330e4a6ab929f41c24415f96f7cdab9c5781210a13625c0`  
		Last Modified: Wed, 22 Jan 2025 22:25:00 GMT  
		Size: 19.2 KB (19173 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:3.12.12-postgres`

```console
$ docker pull geonetwork@sha256:80553b2dda3dcaf3c6d34b5f58f97f3666997829b9aaba9783ece1fc76ff7d54
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
$ docker pull geonetwork@sha256:61516ea6e7063253ccc2af77006bb4bb5cec5660350d6752883338a289f12a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367320215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f046f6f410dcbfab73d486d28f8897c6fb7196e05b0f3aa38a5d12cc692a85`
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
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
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
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f958f4e5767ee8cbfae4e4235c527c4131d6057a66355b614d894f1a0a4c17e`  
		Last Modified: Fri, 31 Jan 2025 01:29:51 GMT  
		Size: 17.0 MB (16962286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85bc3172399be429690fb80a0e29a164e651fe7c79af0a116a832cd9a452af4`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 54.7 MB (54722132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91352bec832ebb8bbef001417c3390a864883828fd1ea6d0304aa3540c5fcf42`  
		Last Modified: Fri, 31 Jan 2025 01:29:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b0a778c4b3fa7cb96f64bd0815f368a43af46f5675c73473ff21260609ed34`  
		Last Modified: Fri, 31 Jan 2025 01:29:50 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54052fc5a57ccf09bd3a191cac02a0119f6e89611349406e744f5300feac29c3`  
		Last Modified: Fri, 31 Jan 2025 02:16:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdf6e1898878b79d3b2e2b6f632ee60e22a70625ca700ad8b32bff5cba8a335`  
		Last Modified: Fri, 31 Jan 2025 02:16:44 GMT  
		Size: 17.5 MB (17498782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0739d463f54d427403a7a38f46c6949c6bf4e071eb4df931ad505b6c8ea30a2`  
		Last Modified: Fri, 31 Jan 2025 03:13:29 GMT  
		Size: 234.5 MB (234549547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801162cd369643515aa88b33493b35c8f42d1bf959b537c6546a55b3b89762cc`  
		Last Modified: Fri, 31 Jan 2025 03:13:22 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e6cc2ace4997d2c654233fbbc198113eb5c1b18bda68dababd926d1ccf65bf`  
		Last Modified: Fri, 31 Jan 2025 04:09:36 GMT  
		Size: 13.8 MB (13829135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945eaf7c2e95e728e3f9ec60c25da31bff43efa6d7e89d1b65f450d0e5f851dc`  
		Last Modified: Fri, 31 Jan 2025 04:09:35 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a097d4f759827861e3f7044e8504ab8873157e2a90759651466c46ba8c7101`  
		Last Modified: Fri, 31 Jan 2025 04:09:35 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a303e47c9967d6ceced54a6232ce31796d94296b5ab0a3206b472f92157939`  
		Last Modified: Fri, 31 Jan 2025 04:09:35 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:6b5b008b322e9e3f7268db58256adf7ad034131b878ee04117a3d37268c2c3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5745604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97f2ac356654319efbc98c0866c10aea4866fb4d01c104a5bc3018818fb6b98`

```dockerfile
```

-	Layers:
	-	`sha256:833da23cd368bcb03556f236a4fe22d66e53264ac87c56fc71c6b86c7b3eb209`  
		Last Modified: Fri, 31 Jan 2025 04:09:36 GMT  
		Size: 5.7 MB (5722744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf6dc8c14e8d8feea68b9d7bf9aa24940a9e8b5b442e8b94eba8535b4d2fd32e`  
		Last Modified: Fri, 31 Jan 2025 04:09:35 GMT  
		Size: 22.9 KB (22860 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12-postgres` - linux; arm variant v7

```console
$ docker pull geonetwork@sha256:c2cec46769a2e11c220282de0eeedfcf3eb432c356a4b1f5b45a11766f32612d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.2 MB (359167441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b91ce1a88d1999f378b4bc67bae037240bc539e0af7f18508bb40b2fec44ddd`
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
ADD file:786ab064bf2d82faf7ca3fbb6c2e6983bbdb3228800d6d64e5dec4a67f778a7a in / 
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
	-	`sha256:b25adda5718ef4d96696ce8f0e58cde58fbe9977456036f84293bba8f26c5567`  
		Last Modified: Tue, 19 Nov 2024 17:38:39 GMT  
		Size: 26.9 MB (26869639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a5eb6a2db557356b46da4a6e217de6ed249bca2210cdccd1a0430c803e8512`  
		Last Modified: Tue, 03 Dec 2024 07:45:24 GMT  
		Size: 16.3 MB (16299908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa44b4fc4334a27557f3a631a9438ca5ce8656e161b39e45ab2440b2d7aead1`  
		Last Modified: Fri, 31 Jan 2025 01:32:09 GMT  
		Size: 50.1 MB (50109725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d811e0afab0f1ffd85e4671f4a476cb71cbde9841a85d24ae45a1ad7b42f60a`  
		Last Modified: Fri, 31 Jan 2025 01:32:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd08c17ad27b6137eb1f45f5f4617278e0a8b0c6ef2a13aa6a4fee9ab4777e26`  
		Last Modified: Fri, 31 Jan 2025 01:32:07 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59de26424799b6d39429ee18f2ea2fd2556807bdfa7356ee01c8bbfdd836544`  
		Last Modified: Fri, 31 Jan 2025 02:47:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771e8c9a5f56f2bac23ee6b2b3ac39b5c48f8403916a0cd7b1d870f9089866aa`  
		Last Modified: Fri, 31 Jan 2025 02:47:44 GMT  
		Size: 18.4 MB (18432713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5d4a5029c50ca81c6c035b53fbd87a52e979c51b94471102c395f1ca6ac7b1`  
		Last Modified: Fri, 31 Jan 2025 03:19:09 GMT  
		Size: 234.5 MB (234537830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cac7095c2b17adc335169c93969115865dfcf1e601c57bbf0f705d71fd00bc`  
		Last Modified: Fri, 31 Jan 2025 03:19:04 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f54edda13a9e4feb68bb65745a76d765bde1150bb28378dba31d44cb5af203`  
		Last Modified: Fri, 31 Jan 2025 04:09:35 GMT  
		Size: 12.9 MB (12911260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda593896a9c8dc74857ae8206e1e0f548bc5991187c2445e182cebf8a17c1b3`  
		Last Modified: Fri, 31 Jan 2025 04:09:34 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c9cba22107ee5109964d57d12f90c355ee3a10155f6f1e479f64f274aac67a`  
		Last Modified: Fri, 31 Jan 2025 04:09:34 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0b285fffbbfd7283dc876652c615081d32d1af4bec2d2804e7569253fc4bd2`  
		Last Modified: Fri, 31 Jan 2025 04:09:35 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:428fbb6410735711f2ba89b7e570d213e3b2ff6dcade96afa401268d50c92657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5748708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09042f03c1dab45d38fea36ded5159977e13b82bc549e33acb44363096351a92`

```dockerfile
```

-	Layers:
	-	`sha256:8f09a3586e6961a791dddabae310250eeeadf6ada768e1a533acd3b10d749caa`  
		Last Modified: Fri, 31 Jan 2025 04:09:34 GMT  
		Size: 5.7 MB (5725767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:919fd879ae32b702f65f9038c31e48de786cd6d7afb1a9fba976b8ba44a961cc`  
		Last Modified: Fri, 31 Jan 2025 04:09:34 GMT  
		Size: 22.9 KB (22941 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12-postgres` - linux; arm64 variant v8

```console
$ docker pull geonetwork@sha256:835cde54ff70414c918ec80c13f11bee514fd1761579a3c7ed11135b42bf24cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.2 MB (363242978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e455ebf09ba0bbbb13d36564150932a3b1c4f30f3f2a1594934a620a6df9f2ed`
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
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
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
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370f8a7b7cf214f61cc1a2546f38e47ba749cb698659b51aa07e70fcecbd7e2f`  
		Last Modified: Wed, 22 Jan 2025 20:53:10 GMT  
		Size: 17.0 MB (16982856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa15e6520d7251000b73f383a2c02ff5f96e0e795daa58fcb86fd6dbecba8106`  
		Last Modified: Wed, 22 Jan 2025 20:53:11 GMT  
		Size: 53.8 MB (53816345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c30897c18d1b536032f6028fe4eaa61fc240ac0410f58674601dace64a2d760`  
		Last Modified: Wed, 22 Jan 2025 20:53:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134a80a14402716f85166426a6c66a2cd42f08cfaa3717a5d71a96df25cd1589`  
		Last Modified: Wed, 22 Jan 2025 20:53:10 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118dc07b441e024431f76daf9cc5eef2f5ff138efab3f6685c4fbdcbe47f69f2`  
		Last Modified: Thu, 23 Jan 2025 02:03:09 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135b96f80d9968468d7a0c0be0cb140df633b0cc4454207548b3916afdb3e061`  
		Last Modified: Thu, 23 Jan 2025 02:03:10 GMT  
		Size: 15.2 MB (15181236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f64449a5834e236084ea0a4a4fbac3f3c32fef49a1eac9d76ba93b4710179c8`  
		Last Modified: Thu, 23 Jan 2025 04:04:46 GMT  
		Size: 234.6 MB (234553572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2ae097196b641e3a2ceef1432ce728955c08c96338ce6face41253503d2b34`  
		Last Modified: Thu, 23 Jan 2025 04:04:40 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7574f7f01d1438f41a3dbcb2652e32133b38427f9c9afb5471ca36395ad2b168`  
		Last Modified: Thu, 23 Jan 2025 05:02:03 GMT  
		Size: 13.8 MB (13809932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f431470c2c6ede2086074f17c208b5471ba08028d6f7083a2feaaa6711c49983`  
		Last Modified: Thu, 23 Jan 2025 05:02:03 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9673c24d9a18b25beb6d7c5fc6eade0d7f7026561ea0b9a9a831dada7faab69f`  
		Last Modified: Thu, 23 Jan 2025 05:02:03 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3007ea91d015e2e4882bfc55367c34610b7c2ff6b785432a03d4c79bdd8c2410`  
		Last Modified: Thu, 23 Jan 2025 05:02:03 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:5367cc256e947e14844049f7cc3d219645f96b953768744d7e9ee437d7861a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5753505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d56349c64c1ba725afbc2480ce1269cb9326b5280a7c5fa074e17332eab88c`

```dockerfile
```

-	Layers:
	-	`sha256:8ee0a74237992b7b988cbf222e2df2bcf2e6cb40f82fe5604da6f154a151f340`  
		Last Modified: Thu, 23 Jan 2025 05:02:02 GMT  
		Size: 5.7 MB (5730538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b29bc55361aeafd24558df2774d2c14298e40cdb61938d1fcb6b0c8b4af1d57`  
		Last Modified: Thu, 23 Jan 2025 05:02:01 GMT  
		Size: 23.0 KB (22967 bytes)  
		MIME: application/vnd.in-toto+json

### `geonetwork:3.12.12-postgres` - linux; ppc64le

```console
$ docker pull geonetwork@sha256:8145bb343e9d0cf9dd75fe7a9bebfcce01f033c5f3979f2284ac743b891de52c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.5 MB (370474528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52db5f06cd19c80f775d949810deb4e05f5442a100b07a68b0e341de924b9f30`
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
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
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
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 08 Aug 2024 11:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb08691d29d174440113fb3d94aec487ff706b850acfce25b3870b67886fdc90`  
		Last Modified: Tue, 03 Dec 2024 04:44:50 GMT  
		Size: 18.8 MB (18845906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69b2fc5d3ba84e6de2d85f7e2d3e79aeb0199b6b959db9dfb1096f73e0d7441`  
		Last Modified: Wed, 22 Jan 2025 18:31:46 GMT  
		Size: 52.2 MB (52170489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7e296b62d1e3ea74e89331c7fe00e13e4ec9b10979b9b44c187cf58235e52`  
		Last Modified: Wed, 22 Jan 2025 18:31:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83acec15d6612c113f691aa6046970a02a05c2531417015cdf20954ea9186b64`  
		Last Modified: Wed, 22 Jan 2025 18:31:45 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb9ec006f44e057f6e3ce2c629e488f8fdd854385f6c4c5163b12f919c8368f`  
		Last Modified: Wed, 22 Jan 2025 21:54:33 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5963ebeba988c2be072f7be5b475b9b5eb304f7ccf6c1c042e78f460ac537c24`  
		Last Modified: Wed, 22 Jan 2025 21:54:34 GMT  
		Size: 16.1 MB (16145052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcdf36274e93607638f0293d1e72a99ae6e30ca967f244afbcd600bf20d112f`  
		Last Modified: Wed, 22 Jan 2025 22:25:11 GMT  
		Size: 234.6 MB (234574149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2b36263da4c5c485517df4274617f2071d46cf986a404e8ea777e0e03bf7d9`  
		Last Modified: Wed, 22 Jan 2025 22:25:01 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e5645a831ba474385d17d488a16dad8bcc97feb775b5d12d1febf7693c4339`  
		Last Modified: Wed, 22 Jan 2025 23:10:30 GMT  
		Size: 14.3 MB (14343745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d116271cf9b42857b6fe081dcb50536cbabdf55908094e4c069ed9fd6b667ee`  
		Last Modified: Wed, 22 Jan 2025 23:10:29 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff09d1cb7c1c4330a22e8ab945cae9d434dbde756bdccd24483c0e68739f59f`  
		Last Modified: Wed, 22 Jan 2025 23:10:29 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b946049c4e63e186c2ce2daaf1ac691908ead6415039758edbe6c13fb7c694`  
		Last Modified: Wed, 22 Jan 2025 23:10:29 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:3.12.12-postgres` - unknown; unknown

```console
$ docker pull geonetwork@sha256:339f65d1b2f7c818958c1f4eb74ce0a5627208d3bcba0bdaab980a9e33265c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5751574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd625da954d0148cf61510ca5cf018cef6639a366614c39210ada6c9ba474b3`

```dockerfile
```

-	Layers:
	-	`sha256:39ce5d4cb34ccb4e57c6d74d281367919860894b9742074341af4bdf44673af4`  
		Last Modified: Wed, 22 Jan 2025 23:10:29 GMT  
		Size: 5.7 MB (5728674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd18b169f9a599226e809afd057fb7afe93f3dc81af8648a67b7986988f60412`  
		Last Modified: Wed, 22 Jan 2025 23:10:28 GMT  
		Size: 22.9 KB (22900 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4`

```console
$ docker pull geonetwork@sha256:c0574b2117c22c195220cc74cdce12c02554d125967a57f7ced7a12d80ac910d
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
$ docker pull geonetwork@sha256:306c8e1c3938b3bf8b168b9ee26f520d76bfe6573bf9cdc0f1f80cd40d5b8590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.1 MB (488135747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d7bbf9e6776d2bf4f62201bc9157b8003f2aa83c411628d36ab865af6e3bcd`
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
ENV JAVA_VERSION=jdk-11.0.25+9
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='191baa2e052627614022171400a917d28f0987dc54da48aaf07b06f552bb9884';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='f2087cc3abdd509b74facf8e43e81e36244d14c70dec080b8f3a662695417ca7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6bdd7da08c9f8fedded8da0411b6566c16cb9a904d164b68a0b7f11c8376673a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='0014ffdae26d2b8f840b4842e3f9d4edc3576b4a961770708273d8ecc86ba5b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='5fb661da82943f42a14bed94beda6d4dd3188987bd13b77e8b6f907054a73e9d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:17f4b72dcbb6206c43fe45c55101d1e9488f00e6908563d57ded36365e8f11e5`  
		Last Modified: Wed, 22 Jan 2025 20:56:53 GMT  
		Size: 142.4 MB (142386629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea9da366dca0f6592ba69e8a5b9560a31595ca67e7df454bdb5656b03d833d6`  
		Last Modified: Wed, 22 Jan 2025 20:56:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef5e6ad774f07f40e295b3f3aa2a431acc33b9ba03bbac13fda900c76835adc`  
		Last Modified: Wed, 22 Jan 2025 20:56:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8296cf795d4c4a693b559b5279bab139fadde2199e2d8ed3a01f0957279c143`  
		Last Modified: Thu, 23 Jan 2025 00:22:56 GMT  
		Size: 10.3 MB (10299581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b23b6c2583e9bc10e4c4c498e95cc18bdf98f5cbb768236be604d01bcb50944`  
		Last Modified: Thu, 23 Jan 2025 00:22:55 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f18543386fb6077f772de3d27b568f217feb97ffde4b4221de446e6365d702`  
		Last Modified: Thu, 23 Jan 2025 04:08:11 GMT  
		Size: 252.2 KB (252224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31dc9bde675b3228753200ebc03e08fd7f290d9f491e94befc433bcb643d5e0`  
		Last Modified: Thu, 23 Jan 2025 04:08:17 GMT  
		Size: 289.1 MB (289123464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25341fccb38a1efbafdac1e8cb27c72bcf70fc15d1d38da449c42e57ea2e5d5`  
		Last Modified: Thu, 23 Jan 2025 04:08:11 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fead5984f9abe1be214356b7dad75c30f445a279c10eeb34aa126a6300b2462f`  
		Last Modified: Thu, 23 Jan 2025 04:08:11 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c38cfe3b26ea3ab92720924a8038b2421a9cd59db38a148db040c6d2bdf5497`  
		Last Modified: Thu, 23 Jan 2025 04:08:12 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:dbb2dcb63844714572b9a40a72fb7e504ad5e497de2cd05c313a56bd68c34449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4719013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2329caf1e1f7bde08f0a5efba6529cac116b57856f60c507c44330a1d94cdc`

```dockerfile
```

-	Layers:
	-	`sha256:b666766c731b2565b2ef99a664805cfbda364ea4261d9ff9ca2d9658a1fec14e`  
		Last Modified: Thu, 23 Jan 2025 04:08:10 GMT  
		Size: 4.7 MB (4693179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01383a360ece76928383dadc2e5566ece8754daf1366b1d31a3a31f9505ec14f`  
		Last Modified: Thu, 23 Jan 2025 04:08:10 GMT  
		Size: 25.8 KB (25834 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.2`

```console
$ docker pull geonetwork@sha256:b6f6c09f710430a53b09cbf9ce013ee042c12bc805e2ae6f6c6ae4830f442f43
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
$ docker pull geonetwork@sha256:a180acadac903387a9755e21f92c6e61b010adccf05ffcfa480146db25eb272f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.6 MB (412641674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18159162b178ef406918d0195a33ec19eb722554a59d238ec6f9e8e1f9c4e475`
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
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 24 Oct 2024 11:02:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:4100167f0a58f3f4ff1b7006e119a3af3dfbe37c81082821d73df81bb18d64df`  
		Last Modified: Wed, 22 Jan 2025 20:50:39 GMT  
		Size: 53.8 MB (53816013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768370932609b8a09990b1de30acd5df6561802704d5d7d98e8ab0cca5bbeb70`  
		Last Modified: Wed, 22 Jan 2025 20:50:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ea0bce96b16782d065d0b2afdaf05e9f303cfc7ea9cdb61ea3187c90ddb8c4`  
		Last Modified: Wed, 22 Jan 2025 20:50:37 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c2ef100d233726289a0d8d9f21d07f37042cb63096757fab5a5fd25204da3a`  
		Last Modified: Thu, 23 Jan 2025 00:21:02 GMT  
		Size: 10.3 MB (10299576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0712c5425c00d5326785aaf604e6be93389bd92cf3676820621b79390185ef1`  
		Last Modified: Thu, 23 Jan 2025 00:21:01 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f479b4245b6632d5db17bf027e3b92708da963fde7864f2c991539411be08631`  
		Last Modified: Thu, 23 Jan 2025 04:06:52 GMT  
		Size: 252.3 KB (252275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39db58b805cc7a563a3870e09eed942a6bdf6b9cfe8eebc3169c890020467808`  
		Last Modified: Thu, 23 Jan 2025 04:06:59 GMT  
		Size: 302.2 MB (302200256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4f63b8112eabda2a8ad175faaa03d9988bc426bd671c286ee211296e26467b`  
		Last Modified: Thu, 23 Jan 2025 04:06:52 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2` - unknown; unknown

```console
$ docker pull geonetwork@sha256:111827162939270beff8877473509a6c8e101fd7cf53a242127a14d0af9cee16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4972962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9b74c348f8b0b7f439e2a37c9f194a813342faa48a7ac2d84095bf611947bb`

```dockerfile
```

-	Layers:
	-	`sha256:f2140dd593e53812b00a5655a711683b4f08f9e603e4465e9c16dbd6977c8cf1`  
		Last Modified: Thu, 23 Jan 2025 04:06:52 GMT  
		Size: 5.0 MB (4954155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb9b07af123aa15003582e0fade2147ab55d3a7480829ff17dc0d2243dc384fd`  
		Last Modified: Thu, 23 Jan 2025 04:06:51 GMT  
		Size: 18.8 KB (18807 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.2.11`

```console
$ docker pull geonetwork@sha256:b6f6c09f710430a53b09cbf9ce013ee042c12bc805e2ae6f6c6ae4830f442f43
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
$ docker pull geonetwork@sha256:a180acadac903387a9755e21f92c6e61b010adccf05ffcfa480146db25eb272f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.6 MB (412641674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18159162b178ef406918d0195a33ec19eb722554a59d238ec6f9e8e1f9c4e475`
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
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 24 Oct 2024 11:02:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
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
	-	`sha256:4100167f0a58f3f4ff1b7006e119a3af3dfbe37c81082821d73df81bb18d64df`  
		Last Modified: Wed, 22 Jan 2025 20:50:39 GMT  
		Size: 53.8 MB (53816013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768370932609b8a09990b1de30acd5df6561802704d5d7d98e8ab0cca5bbeb70`  
		Last Modified: Wed, 22 Jan 2025 20:50:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ea0bce96b16782d065d0b2afdaf05e9f303cfc7ea9cdb61ea3187c90ddb8c4`  
		Last Modified: Wed, 22 Jan 2025 20:50:37 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c2ef100d233726289a0d8d9f21d07f37042cb63096757fab5a5fd25204da3a`  
		Last Modified: Thu, 23 Jan 2025 00:21:02 GMT  
		Size: 10.3 MB (10299576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0712c5425c00d5326785aaf604e6be93389bd92cf3676820621b79390185ef1`  
		Last Modified: Thu, 23 Jan 2025 00:21:01 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f479b4245b6632d5db17bf027e3b92708da963fde7864f2c991539411be08631`  
		Last Modified: Thu, 23 Jan 2025 04:06:52 GMT  
		Size: 252.3 KB (252275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39db58b805cc7a563a3870e09eed942a6bdf6b9cfe8eebc3169c890020467808`  
		Last Modified: Thu, 23 Jan 2025 04:06:59 GMT  
		Size: 302.2 MB (302200256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4f63b8112eabda2a8ad175faaa03d9988bc426bd671c286ee211296e26467b`  
		Last Modified: Thu, 23 Jan 2025 04:06:52 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.2.11` - unknown; unknown

```console
$ docker pull geonetwork@sha256:111827162939270beff8877473509a6c8e101fd7cf53a242127a14d0af9cee16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4972962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9b74c348f8b0b7f439e2a37c9f194a813342faa48a7ac2d84095bf611947bb`

```dockerfile
```

-	Layers:
	-	`sha256:f2140dd593e53812b00a5655a711683b4f08f9e603e4465e9c16dbd6977c8cf1`  
		Last Modified: Thu, 23 Jan 2025 04:06:52 GMT  
		Size: 5.0 MB (4954155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb9b07af123aa15003582e0fade2147ab55d3a7480829ff17dc0d2243dc384fd`  
		Last Modified: Thu, 23 Jan 2025 04:06:51 GMT  
		Size: 18.8 KB (18807 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.4`

```console
$ docker pull geonetwork@sha256:c0574b2117c22c195220cc74cdce12c02554d125967a57f7ced7a12d80ac910d
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
$ docker pull geonetwork@sha256:306c8e1c3938b3bf8b168b9ee26f520d76bfe6573bf9cdc0f1f80cd40d5b8590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.1 MB (488135747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d7bbf9e6776d2bf4f62201bc9157b8003f2aa83c411628d36ab865af6e3bcd`
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
ENV JAVA_VERSION=jdk-11.0.25+9
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='191baa2e052627614022171400a917d28f0987dc54da48aaf07b06f552bb9884';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='f2087cc3abdd509b74facf8e43e81e36244d14c70dec080b8f3a662695417ca7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6bdd7da08c9f8fedded8da0411b6566c16cb9a904d164b68a0b7f11c8376673a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='0014ffdae26d2b8f840b4842e3f9d4edc3576b4a961770708273d8ecc86ba5b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='5fb661da82943f42a14bed94beda6d4dd3188987bd13b77e8b6f907054a73e9d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:17f4b72dcbb6206c43fe45c55101d1e9488f00e6908563d57ded36365e8f11e5`  
		Last Modified: Wed, 22 Jan 2025 20:56:53 GMT  
		Size: 142.4 MB (142386629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea9da366dca0f6592ba69e8a5b9560a31595ca67e7df454bdb5656b03d833d6`  
		Last Modified: Wed, 22 Jan 2025 20:56:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef5e6ad774f07f40e295b3f3aa2a431acc33b9ba03bbac13fda900c76835adc`  
		Last Modified: Wed, 22 Jan 2025 20:56:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8296cf795d4c4a693b559b5279bab139fadde2199e2d8ed3a01f0957279c143`  
		Last Modified: Thu, 23 Jan 2025 00:22:56 GMT  
		Size: 10.3 MB (10299581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b23b6c2583e9bc10e4c4c498e95cc18bdf98f5cbb768236be604d01bcb50944`  
		Last Modified: Thu, 23 Jan 2025 00:22:55 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f18543386fb6077f772de3d27b568f217feb97ffde4b4221de446e6365d702`  
		Last Modified: Thu, 23 Jan 2025 04:08:11 GMT  
		Size: 252.2 KB (252224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31dc9bde675b3228753200ebc03e08fd7f290d9f491e94befc433bcb643d5e0`  
		Last Modified: Thu, 23 Jan 2025 04:08:17 GMT  
		Size: 289.1 MB (289123464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25341fccb38a1efbafdac1e8cb27c72bcf70fc15d1d38da449c42e57ea2e5d5`  
		Last Modified: Thu, 23 Jan 2025 04:08:11 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fead5984f9abe1be214356b7dad75c30f445a279c10eeb34aa126a6300b2462f`  
		Last Modified: Thu, 23 Jan 2025 04:08:11 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c38cfe3b26ea3ab92720924a8038b2421a9cd59db38a148db040c6d2bdf5497`  
		Last Modified: Thu, 23 Jan 2025 04:08:12 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4` - unknown; unknown

```console
$ docker pull geonetwork@sha256:dbb2dcb63844714572b9a40a72fb7e504ad5e497de2cd05c313a56bd68c34449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4719013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2329caf1e1f7bde08f0a5efba6529cac116b57856f60c507c44330a1d94cdc`

```dockerfile
```

-	Layers:
	-	`sha256:b666766c731b2565b2ef99a664805cfbda364ea4261d9ff9ca2d9658a1fec14e`  
		Last Modified: Thu, 23 Jan 2025 04:08:10 GMT  
		Size: 4.7 MB (4693179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01383a360ece76928383dadc2e5566ece8754daf1366b1d31a3a31f9505ec14f`  
		Last Modified: Thu, 23 Jan 2025 04:08:10 GMT  
		Size: 25.8 KB (25834 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:4.4.6`

```console
$ docker pull geonetwork@sha256:c0574b2117c22c195220cc74cdce12c02554d125967a57f7ced7a12d80ac910d
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
$ docker pull geonetwork@sha256:306c8e1c3938b3bf8b168b9ee26f520d76bfe6573bf9cdc0f1f80cd40d5b8590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.1 MB (488135747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d7bbf9e6776d2bf4f62201bc9157b8003f2aa83c411628d36ab865af6e3bcd`
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
ENV JAVA_VERSION=jdk-11.0.25+9
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='191baa2e052627614022171400a917d28f0987dc54da48aaf07b06f552bb9884';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='f2087cc3abdd509b74facf8e43e81e36244d14c70dec080b8f3a662695417ca7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6bdd7da08c9f8fedded8da0411b6566c16cb9a904d164b68a0b7f11c8376673a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='0014ffdae26d2b8f840b4842e3f9d4edc3576b4a961770708273d8ecc86ba5b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='5fb661da82943f42a14bed94beda6d4dd3188987bd13b77e8b6f907054a73e9d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:17f4b72dcbb6206c43fe45c55101d1e9488f00e6908563d57ded36365e8f11e5`  
		Last Modified: Wed, 22 Jan 2025 20:56:53 GMT  
		Size: 142.4 MB (142386629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea9da366dca0f6592ba69e8a5b9560a31595ca67e7df454bdb5656b03d833d6`  
		Last Modified: Wed, 22 Jan 2025 20:56:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef5e6ad774f07f40e295b3f3aa2a431acc33b9ba03bbac13fda900c76835adc`  
		Last Modified: Wed, 22 Jan 2025 20:56:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8296cf795d4c4a693b559b5279bab139fadde2199e2d8ed3a01f0957279c143`  
		Last Modified: Thu, 23 Jan 2025 00:22:56 GMT  
		Size: 10.3 MB (10299581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b23b6c2583e9bc10e4c4c498e95cc18bdf98f5cbb768236be604d01bcb50944`  
		Last Modified: Thu, 23 Jan 2025 00:22:55 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f18543386fb6077f772de3d27b568f217feb97ffde4b4221de446e6365d702`  
		Last Modified: Thu, 23 Jan 2025 04:08:11 GMT  
		Size: 252.2 KB (252224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31dc9bde675b3228753200ebc03e08fd7f290d9f491e94befc433bcb643d5e0`  
		Last Modified: Thu, 23 Jan 2025 04:08:17 GMT  
		Size: 289.1 MB (289123464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25341fccb38a1efbafdac1e8cb27c72bcf70fc15d1d38da449c42e57ea2e5d5`  
		Last Modified: Thu, 23 Jan 2025 04:08:11 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fead5984f9abe1be214356b7dad75c30f445a279c10eeb34aa126a6300b2462f`  
		Last Modified: Thu, 23 Jan 2025 04:08:11 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c38cfe3b26ea3ab92720924a8038b2421a9cd59db38a148db040c6d2bdf5497`  
		Last Modified: Thu, 23 Jan 2025 04:08:12 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:4.4.6` - unknown; unknown

```console
$ docker pull geonetwork@sha256:dbb2dcb63844714572b9a40a72fb7e504ad5e497de2cd05c313a56bd68c34449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4719013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2329caf1e1f7bde08f0a5efba6529cac116b57856f60c507c44330a1d94cdc`

```dockerfile
```

-	Layers:
	-	`sha256:b666766c731b2565b2ef99a664805cfbda364ea4261d9ff9ca2d9658a1fec14e`  
		Last Modified: Thu, 23 Jan 2025 04:08:10 GMT  
		Size: 4.7 MB (4693179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01383a360ece76928383dadc2e5566ece8754daf1366b1d31a3a31f9505ec14f`  
		Last Modified: Thu, 23 Jan 2025 04:08:10 GMT  
		Size: 25.8 KB (25834 bytes)  
		MIME: application/vnd.in-toto+json

## `geonetwork:latest`

```console
$ docker pull geonetwork@sha256:c0574b2117c22c195220cc74cdce12c02554d125967a57f7ced7a12d80ac910d
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
$ docker pull geonetwork@sha256:306c8e1c3938b3bf8b168b9ee26f520d76bfe6573bf9cdc0f1f80cd40d5b8590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.1 MB (488135747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d7bbf9e6776d2bf4f62201bc9157b8003f2aa83c411628d36ab865af6e3bcd`
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
ENV JAVA_VERSION=jdk-11.0.25+9
# Thu, 24 Oct 2024 11:20:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='191baa2e052627614022171400a917d28f0987dc54da48aaf07b06f552bb9884';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='f2087cc3abdd509b74facf8e43e81e36244d14c70dec080b8f3a662695417ca7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6bdd7da08c9f8fedded8da0411b6566c16cb9a904d164b68a0b7f11c8376673a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='0014ffdae26d2b8f840b4842e3f9d4edc3576b4a961770708273d8ecc86ba5b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='5fb661da82943f42a14bed94beda6d4dd3188987bd13b77e8b6f907054a73e9d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:17f4b72dcbb6206c43fe45c55101d1e9488f00e6908563d57ded36365e8f11e5`  
		Last Modified: Wed, 22 Jan 2025 20:56:53 GMT  
		Size: 142.4 MB (142386629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea9da366dca0f6592ba69e8a5b9560a31595ca67e7df454bdb5656b03d833d6`  
		Last Modified: Wed, 22 Jan 2025 20:56:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef5e6ad774f07f40e295b3f3aa2a431acc33b9ba03bbac13fda900c76835adc`  
		Last Modified: Wed, 22 Jan 2025 20:56:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8296cf795d4c4a693b559b5279bab139fadde2199e2d8ed3a01f0957279c143`  
		Last Modified: Thu, 23 Jan 2025 00:22:56 GMT  
		Size: 10.3 MB (10299581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b23b6c2583e9bc10e4c4c498e95cc18bdf98f5cbb768236be604d01bcb50944`  
		Last Modified: Thu, 23 Jan 2025 00:22:55 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f18543386fb6077f772de3d27b568f217feb97ffde4b4221de446e6365d702`  
		Last Modified: Thu, 23 Jan 2025 04:08:11 GMT  
		Size: 252.2 KB (252224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31dc9bde675b3228753200ebc03e08fd7f290d9f491e94befc433bcb643d5e0`  
		Last Modified: Thu, 23 Jan 2025 04:08:17 GMT  
		Size: 289.1 MB (289123464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25341fccb38a1efbafdac1e8cb27c72bcf70fc15d1d38da449c42e57ea2e5d5`  
		Last Modified: Thu, 23 Jan 2025 04:08:11 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fead5984f9abe1be214356b7dad75c30f445a279c10eeb34aa126a6300b2462f`  
		Last Modified: Thu, 23 Jan 2025 04:08:11 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c38cfe3b26ea3ab92720924a8038b2421a9cd59db38a148db040c6d2bdf5497`  
		Last Modified: Thu, 23 Jan 2025 04:08:12 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `geonetwork:latest` - unknown; unknown

```console
$ docker pull geonetwork@sha256:dbb2dcb63844714572b9a40a72fb7e504ad5e497de2cd05c313a56bd68c34449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4719013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2329caf1e1f7bde08f0a5efba6529cac116b57856f60c507c44330a1d94cdc`

```dockerfile
```

-	Layers:
	-	`sha256:b666766c731b2565b2ef99a664805cfbda364ea4261d9ff9ca2d9658a1fec14e`  
		Last Modified: Thu, 23 Jan 2025 04:08:10 GMT  
		Size: 4.7 MB (4693179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01383a360ece76928383dadc2e5566ece8754daf1366b1d31a3a31f9505ec14f`  
		Last Modified: Thu, 23 Jan 2025 04:08:10 GMT  
		Size: 25.8 KB (25834 bytes)  
		MIME: application/vnd.in-toto+json
