## `tomcat:11-jdk17-temurin-jammy`

```console
$ docker pull tomcat@sha256:dfff4773ef34beca91eba9ca5a87cf084e52c5873bef15e4acc7790fcdc3296a
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

### `tomcat:11-jdk17-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:7259b6ca2834c9774ae67359860b25f6f96fd02844c8569cbecdc004064ae044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.2 MB (209190786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe09d957ea02d7f72043f9f49f0b20e3301a4f66a1b14a8c1e1ed7ff61527fb`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Tue, 13 May 2025 08:03:30 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 13 May 2025 08:03:30 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 08:03:30 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 13 May 2025 08:03:30 GMT
WORKDIR /usr/local/tomcat
# Tue, 13 May 2025 08:03:30 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 13 May 2025 08:03:30 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 13 May 2025 08:03:30 GMT
ENV TOMCAT_MAJOR=11
# Tue, 13 May 2025 08:03:30 GMT
ENV TOMCAT_VERSION=11.0.7
# Tue, 13 May 2025 08:03:30 GMT
ENV TOMCAT_SHA512=50dd1addd3745e4484295358d2b84220a17c32f69ab3868fdea71748b06751a616db72fe21b03f6576fede373dad62931e84a9a2e65baca61fc68dbf7281c246
# Tue, 13 May 2025 08:03:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-11/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 13 May 2025 08:03:30 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 13 May 2025 08:03:30 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 13 May 2025 08:03:30 GMT
ENTRYPOINT []
# Tue, 13 May 2025 08:03:30 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0fe557244d0ccdf12070ab3445dea5551cfccd224b57677d31bdc3f4b6f23`  
		Last Modified: Tue, 03 Jun 2025 13:31:19 GMT  
		Size: 20.7 MB (20695089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1a2fd77bc51863277a75436242197b369979cb36a4451f5b5b0986c1dff0d4`  
		Last Modified: Tue, 03 Jun 2025 13:31:07 GMT  
		Size: 144.6 MB (144646739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4749f9bc6d7a96c663cac97551da8e1fe1cd9eec208f1ae28c9b3f2d79e6e51`  
		Last Modified: Tue, 03 Jun 2025 13:31:18 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62937f7c5c08ea52a3a6925c5396dcc6d50f93096e25db31930654a48ba3de36`  
		Last Modified: Tue, 03 Jun 2025 13:30:55 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cc077a6c1f9e2ea4e6414f6759bc7af7bfafc97dd35962ffc69165c1e88579`  
		Last Modified: Tue, 03 Jun 2025 13:37:26 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6262e719d31a945ae3f1f12cda8e86a206c93ff1c315e5313555c40b424b99`  
		Last Modified: Tue, 03 Jun 2025 15:46:57 GMT  
		Size: 14.3 MB (14313313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jdk17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:3845d76389f7653b868d585048c9577e65aabf42f177a3863fadcaae5e048997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4071079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b1dfa968b3ed3b45c2b72f228e459dc0f16d03d8903954da6244665ec16d4a`

```dockerfile
```

-	Layers:
	-	`sha256:30e216fb212f768a4e2eaa23f171d0cebe4229bd1236382a7f1e378301aefea3`  
		Last Modified: Tue, 03 Jun 2025 14:30:53 GMT  
		Size: 4.0 MB (4040631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f18176210999a57177dd1413dc0da67a6d3f733b85b47ca561afb9c9b929d6e`  
		Last Modified: Tue, 03 Jun 2025 14:30:54 GMT  
		Size: 30.4 KB (30448 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jdk17-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:cecb2f79d2fd59a9ec1c69f2e174c6698c54ac9ad8644b23131cd97492f93c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (204010534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0a4cf2196f454d6559cd6610d515c182966ab38d966235a4dee62784e5e463`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:a68d8d0994670732edac30efcee96eec3850856e5c33c1c7fee7fdc59173ac3d in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Tue, 13 May 2025 08:03:30 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 13 May 2025 08:03:30 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 08:03:30 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 13 May 2025 08:03:30 GMT
WORKDIR /usr/local/tomcat
# Tue, 13 May 2025 08:03:30 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 13 May 2025 08:03:30 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 13 May 2025 08:03:30 GMT
ENV TOMCAT_MAJOR=11
# Tue, 13 May 2025 08:03:30 GMT
ENV TOMCAT_VERSION=11.0.7
# Tue, 13 May 2025 08:03:30 GMT
ENV TOMCAT_SHA512=50dd1addd3745e4484295358d2b84220a17c32f69ab3868fdea71748b06751a616db72fe21b03f6576fede373dad62931e84a9a2e65baca61fc68dbf7281c246
# Tue, 13 May 2025 08:03:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-11/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 13 May 2025 08:03:30 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 13 May 2025 08:03:30 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 13 May 2025 08:03:30 GMT
ENTRYPOINT []
# Tue, 13 May 2025 08:03:30 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f35c50ead1843adba7d4d13281d31bc17c201a55b8bd1a3961e1bcfd131b762d`  
		Last Modified: Tue, 03 Jun 2025 13:42:56 GMT  
		Size: 26.6 MB (26640475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7900403615b3016a4ed577f803f95753dd37fb0ec7691a7dc425d434de02581d`  
		Last Modified: Tue, 03 Jun 2025 14:51:37 GMT  
		Size: 21.0 MB (20989296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2fe77c10494ee47f7d4c0e7490c0de235c65ec33464f90bac33f2d23983324`  
		Last Modified: Tue, 03 Jun 2025 14:51:41 GMT  
		Size: 142.1 MB (142121474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87300700c1f4296c78f154d0df6a79ae996f323424c213aa4b1cdf59f172ca9c`  
		Last Modified: Tue, 03 Jun 2025 14:51:35 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fa2b3bd0e6617ccb6daa50572aa2a2a0a4f19eb3ca23b016f0d0de840feaab`  
		Last Modified: Tue, 03 Jun 2025 14:51:36 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f816964300d291d2ab9e271ef0b985aa04db68a528a20eececa2288559930c11`  
		Last Modified: Tue, 03 Jun 2025 05:35:08 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913355281dbeb9324d6042c57e57954d3f54eb02421a860844c5335a9a790254`  
		Last Modified: Tue, 03 Jun 2025 05:35:09 GMT  
		Size: 14.3 MB (14256642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jdk17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:0bb12b45296a6527362e9186956be5cb784d09fe3da10edaeac65bad0c2e928b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3990448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c45cd3ab138582d8b34e48fb3aac0b771d00baa7be54cfe998ac877db9c3ab`

```dockerfile
```

-	Layers:
	-	`sha256:79ab81d9fd922a181d01caf6d4b7523dba8d0357c34041668eb019215ca24b6f`  
		Last Modified: Tue, 03 Jun 2025 14:30:59 GMT  
		Size: 4.0 MB (3959898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15ca98ef24bcad59ccf37904a76755afd536a657b5ee11a13f383563955b41b1`  
		Last Modified: Tue, 03 Jun 2025 14:31:00 GMT  
		Size: 30.6 KB (30550 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jdk17-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:44b3dbff3e72d8f54b43e6412254d5eb4fa292830e77e029e55a6d24d35ed97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207249993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eca19f87f3e9d365a73522c67b151c419523680920290f9421cec0f65fcbf76`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Tue, 13 May 2025 08:03:30 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 13 May 2025 08:03:30 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 08:03:30 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 13 May 2025 08:03:30 GMT
WORKDIR /usr/local/tomcat
# Tue, 13 May 2025 08:03:30 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 13 May 2025 08:03:30 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 13 May 2025 08:03:30 GMT
ENV TOMCAT_MAJOR=11
# Tue, 13 May 2025 08:03:30 GMT
ENV TOMCAT_VERSION=11.0.7
# Tue, 13 May 2025 08:03:30 GMT
ENV TOMCAT_SHA512=50dd1addd3745e4484295358d2b84220a17c32f69ab3868fdea71748b06751a616db72fe21b03f6576fede373dad62931e84a9a2e65baca61fc68dbf7281c246
# Tue, 13 May 2025 08:03:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-11/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 13 May 2025 08:03:30 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 13 May 2025 08:03:30 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 13 May 2025 08:03:30 GMT
ENTRYPOINT []
# Tue, 13 May 2025 08:03:30 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20b2418d7bbcc708e67cfff8627daf7b6f435fc432ff16ab231e708e65c6b74`  
		Last Modified: Tue, 03 Jun 2025 13:35:04 GMT  
		Size: 22.1 MB (22070032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdaf34cedc9f3788294775a0dd88f82b79f5f5984c48ce79559bd624d0a692fa`  
		Last Modified: Tue, 03 Jun 2025 13:35:18 GMT  
		Size: 143.5 MB (143512494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f339ca92bbfd1652d123732783350dead0c02bef916d33d2156a29606eb3252`  
		Last Modified: Tue, 03 Jun 2025 13:35:02 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1491aa6e7adb28a726f982823828ce808954484f3f7e07d78577cb27dc1f168`  
		Last Modified: Tue, 03 Jun 2025 13:35:02 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0609efaf1af4b278d086989622fa78c0c22b525f3b0f3cae3a776e7097cd840`  
		Last Modified: Tue, 03 Jun 2025 14:34:12 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed85fdf439f7c53a68b1ad2443c2fc86a65b7d277632e135a056ca086778816`  
		Last Modified: Tue, 03 Jun 2025 12:34:15 GMT  
		Size: 14.3 MB (14309244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jdk17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:7640eb7d05bf8658f22e070b9549eb7de65b3ad2b49e0d36ac29ac84c6b17042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4166695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf318986d58e340938a1a307ad93d358bbabf38c24c03ad072366693974bedb`

```dockerfile
```

-	Layers:
	-	`sha256:f837cb7c530dd000b814d389a402ef4935fb22031fc661b7107b6f48d04d1632`  
		Last Modified: Tue, 03 Jun 2025 14:31:10 GMT  
		Size: 4.1 MB (4136113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46e31d7e96277126c8356c5dc3469022b55b1d1b27fef3d4b7a85fbb5fc34358`  
		Last Modified: Tue, 03 Jun 2025 14:31:12 GMT  
		Size: 30.6 KB (30582 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jdk17-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:af09195d61ea67b29db844c94656789ebbc4a9703185e7bb12ff39b6ff200741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.7 MB (215668532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0f358921cdeba33d7cb513749bf34741d623247f7b20ab997a171152ecbc33`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Tue, 13 May 2025 08:03:30 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 13 May 2025 08:03:30 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 08:03:30 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 13 May 2025 08:03:30 GMT
WORKDIR /usr/local/tomcat
# Tue, 13 May 2025 08:03:30 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 13 May 2025 08:03:30 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 13 May 2025 08:03:30 GMT
ENV TOMCAT_MAJOR=11
# Tue, 13 May 2025 08:03:30 GMT
ENV TOMCAT_VERSION=11.0.7
# Tue, 13 May 2025 08:03:30 GMT
ENV TOMCAT_SHA512=50dd1addd3745e4484295358d2b84220a17c32f69ab3868fdea71748b06751a616db72fe21b03f6576fede373dad62931e84a9a2e65baca61fc68dbf7281c246
# Tue, 13 May 2025 08:03:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-11/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 13 May 2025 08:03:30 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 13 May 2025 08:03:30 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 13 May 2025 08:03:30 GMT
ENTRYPOINT []
# Tue, 13 May 2025 08:03:30 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25b605481eaa5f7f44a2e46b3dd11395d4cd7c42c940fb3e638882d37bbb6b1`  
		Last Modified: Tue, 03 Jun 2025 14:41:50 GMT  
		Size: 22.6 MB (22581320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e48a87b997b39b2d446156fa374fcca5a607e864b487d84a9c6e57b7f2d245`  
		Last Modified: Tue, 03 Jun 2025 14:52:08 GMT  
		Size: 144.3 MB (144288990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf75e8e7680dbf9232233c00ea9bb8ab4d892949482b7d11d87d41d88a82042`  
		Last Modified: Tue, 03 Jun 2025 14:52:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe670b1586dc10256ab92db4bd03f6893f0252ca2428e58e59e28bfc3c5ad86`  
		Last Modified: Tue, 03 Jun 2025 14:52:01 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa1258326d780fa08b49539c474203f66798bbbfb9b6636b4078813977ea8a9`  
		Last Modified: Wed, 04 Jun 2025 21:39:09 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8cbcc1e22377e3110d71111ad292c3db3551ac26015560fff9014910f21b70`  
		Last Modified: Tue, 03 Jun 2025 07:22:11 GMT  
		Size: 14.4 MB (14355220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jdk17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:ec45cd534e8afe7b47f46be6319f3b3ec8aa63a769eaa3b05566e7b72b7cbd96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1afcdb0ba36fb242c440b2b0dea6fca0de833b2965f4b9de74decaeb46e6585`

```dockerfile
```

-	Layers:
	-	`sha256:c424e7f946dc234a2e0442da717a2efdf3d47dca66327f7de77d706cc712fb02`  
		Last Modified: Tue, 03 Jun 2025 14:31:17 GMT  
		Size: 4.1 MB (4068191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc4025221b1ff4201565084e96b6cffbfdbb453123a6e59ac9a840c537bc2a9`  
		Last Modified: Tue, 03 Jun 2025 14:31:18 GMT  
		Size: 30.5 KB (30496 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jdk17-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:d7e16ca897a361586a0b510aeaa9bb8ab046bea7f3ae7a1b4f890c7ee428d9d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.4 MB (197412592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8584b22770b9fe8b61d613b52dca6ff41a5648ab9dea3ca0104133b6415a44`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Tue, 13 May 2025 08:03:30 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 13 May 2025 08:03:30 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 08:03:30 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 13 May 2025 08:03:30 GMT
WORKDIR /usr/local/tomcat
# Tue, 13 May 2025 08:03:30 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 13 May 2025 08:03:30 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 13 May 2025 08:03:30 GMT
ENV TOMCAT_MAJOR=11
# Tue, 13 May 2025 08:03:30 GMT
ENV TOMCAT_VERSION=11.0.7
# Tue, 13 May 2025 08:03:30 GMT
ENV TOMCAT_SHA512=50dd1addd3745e4484295358d2b84220a17c32f69ab3868fdea71748b06751a616db72fe21b03f6576fede373dad62931e84a9a2e65baca61fc68dbf7281c246
# Tue, 13 May 2025 08:03:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-11/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Tue, 13 May 2025 08:03:30 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 13 May 2025 08:03:30 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 13 May 2025 08:03:30 GMT
ENTRYPOINT []
# Tue, 13 May 2025 08:03:30 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431a24ad72c11c866728f8b35fd9f9c833af98db35d0a24bd69f47a21b8d17e7`  
		Last Modified: Tue, 03 Jun 2025 14:52:22 GMT  
		Size: 20.4 MB (20413037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f64e485a16cb9a11bed35da69ca861ea6bca1f7988b9dcbdacadeb71712824`  
		Last Modified: Tue, 03 Jun 2025 14:52:28 GMT  
		Size: 134.7 MB (134680790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c12988f2080c5dfbd427428a540acabdb575e6f7956ccab6bf33ce4688b5e`  
		Last Modified: Tue, 03 Jun 2025 14:52:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689628cf2a9cb0fd55cff7cfa693c4a335ffb1fc81768cd5550ef28c57a3e172`  
		Last Modified: Tue, 03 Jun 2025 14:52:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb79c358d412175e6abdb5b44815310d80b93d5760f03a870311deba138d118`  
		Last Modified: Wed, 04 Jun 2025 23:16:21 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09b7204ea453ed9fee72a3a539d4e95b55498caae3084d1e5bcc91f96acc0ac`  
		Last Modified: Tue, 03 Jun 2025 05:41:26 GMT  
		Size: 14.3 MB (14315523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jdk17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:3a6d5e7587acda9aa6b7cecf8019f5dd04e61d3a9b8a0957e9b70aa46a1270d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb32d0bb015858db47efefe1a9f3d7fd8366762812bbe224a9e89e4656f91dbf`

```dockerfile
```

-	Layers:
	-	`sha256:36bc608a544ddc8a2865dce1ffa5167bae65f3203ea604563abb27e1ebf7763a`  
		Last Modified: Tue, 03 Jun 2025 14:31:23 GMT  
		Size: 4.0 MB (3965627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9742ccfd8fa732c8c37ca6a94b3ff29113aa5258b01d11203194597ba775dfea`  
		Last Modified: Tue, 03 Jun 2025 14:31:24 GMT  
		Size: 30.4 KB (30448 bytes)  
		MIME: application/vnd.in-toto+json
