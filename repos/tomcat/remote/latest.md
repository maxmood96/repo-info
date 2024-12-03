## `tomcat:latest`

```console
$ docker pull tomcat@sha256:f34513a8874f6d7d0c60c7de2c3ef0d8404c16d9469824b607ad6929a60baad9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `tomcat:latest` - linux; amd64

```console
$ docker pull tomcat@sha256:cb79b37c69313d89fab32d74fc7d8da13b5c434a582a121039ba851d45e4ea5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224079073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe34209851fffde4cc148ce88cace4fd563ce1908725d166da4bfe50c449e56`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ARG RELEASE
# Wed, 23 Oct 2024 15:41:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Oct 2024 15:41:32 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c654d98404c073b8a7e66bffb27f4ae3e7ede47d13284c132d40a83144bfd8c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='6482639ed9fd22aa2e704cc366848b1b3e1586d2bf1213869c43e80bca58fe5c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='3c6f4c358facfb6c19d90faf02bfe0fc7512d6b0e80ac18146bbd7e0d01deeef';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        riscv64)          ESUM='2f1b3e401e36de803398dfb9818861f9f14ca8ae7db650ea0946ab048fefe3b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='51a7ca42cc2e8cb5f3e7a326c28912ee84ff0791a1ca66650a8c53af07510a7c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
# Sun, 10 Nov 2024 21:03:31 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sun, 10 Nov 2024 21:03:31 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 10 Nov 2024 21:03:31 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sun, 10 Nov 2024 21:03:31 GMT
WORKDIR /usr/local/tomcat
# Sun, 10 Nov 2024 21:03:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sun, 10 Nov 2024 21:03:31 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sun, 10 Nov 2024 21:03:31 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sun, 10 Nov 2024 21:03:31 GMT
ENV TOMCAT_MAJOR=11
# Sun, 10 Nov 2024 21:03:31 GMT
ENV TOMCAT_VERSION=11.0.1
# Sun, 10 Nov 2024 21:03:31 GMT
ENV TOMCAT_SHA512=dce8800532c9dcb079d456e9ea561ac9b7c854a8c50dfcd78339d077f9db127d86dba339db3fcea16c75039c9201c3446ecd4807efe0d42fcf005d2061cbc090
# Sun, 10 Nov 2024 21:03:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Sun, 10 Nov 2024 21:03:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sun, 10 Nov 2024 21:03:31 GMT
EXPOSE map[8080/tcp:{}]
# Sun, 10 Nov 2024 21:03:31 GMT
ENTRYPOINT []
# Sun, 10 Nov 2024 21:03:31 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2afd91a87d1b2f93bb0c4f021644ade815979248b1f68bcae88b1b2f809336`  
		Last Modified: Tue, 03 Dec 2024 02:30:28 GMT  
		Size: 22.9 MB (22948552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e9bbcfa697ca9d2056ad0c815e6da943a4356633738d01b99b5faa2ebef7ca`  
		Last Modified: Tue, 03 Dec 2024 02:30:30 GMT  
		Size: 157.6 MB (157585711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11be3e61358234818e215b9d11d1584bb7cf33bbbe329ccff717d555f1be2994`  
		Last Modified: Tue, 03 Dec 2024 02:30:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9d1e181a2a2b6ed242e21c8a4d40d33cf851fd5522737a9aaa8a708d215f94`  
		Last Modified: Tue, 03 Dec 2024 02:30:28 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00e60e1b13b1db7c3b485554cb51f3a04c499ab5ff2234f82dc1e5bf7021d1c`  
		Last Modified: Tue, 03 Dec 2024 03:25:17 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1806023ac192290be1d336ddc50c98ba1d95b74e98349bd33e411ba87245b4f9`  
		Last Modified: Tue, 03 Dec 2024 03:25:18 GMT  
		Size: 13.8 MB (13790197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:latest` - unknown; unknown

```console
$ docker pull tomcat@sha256:f583f89916fce5f1eef561e96b41ad52f14b64886af912f6be69db6114055395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3454438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029c4c48f8c0faabf2cdd0bcfe65e51fa611bcbdc2222e9c41180deea9a8bd27`

```dockerfile
```

-	Layers:
	-	`sha256:c4ff1dcbb2aa26c5def00aeeabdd5b6d8d669ca1e1905313cfc104e52f0c04ea`  
		Last Modified: Tue, 03 Dec 2024 03:25:17 GMT  
		Size: 3.4 MB (3421481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa909aa39c21d964c5f5afc4dad1fd816dc877697ed52a5919d600f340ad063a`  
		Last Modified: Tue, 03 Dec 2024 03:25:17 GMT  
		Size: 33.0 KB (32957 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:latest` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:740528418461f87f7db7620e3a15ba8d53053f354ee431af4e19e7707bd9cbbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.7 MB (222654050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb790d5e068f38d2065ee2e2c4420ad44f3b7eadfb0786afa4de7b86da2bd91d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c654d98404c073b8a7e66bffb27f4ae3e7ede47d13284c132d40a83144bfd8c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='6482639ed9fd22aa2e704cc366848b1b3e1586d2bf1213869c43e80bca58fe5c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='3c6f4c358facfb6c19d90faf02bfe0fc7512d6b0e80ac18146bbd7e0d01deeef';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        riscv64)          ESUM='2f1b3e401e36de803398dfb9818861f9f14ca8ae7db650ea0946ab048fefe3b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='51a7ca42cc2e8cb5f3e7a326c28912ee84ff0791a1ca66650a8c53af07510a7c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
# Sun, 10 Nov 2024 21:03:31 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sun, 10 Nov 2024 21:03:31 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 10 Nov 2024 21:03:31 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sun, 10 Nov 2024 21:03:31 GMT
WORKDIR /usr/local/tomcat
# Sun, 10 Nov 2024 21:03:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sun, 10 Nov 2024 21:03:31 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sun, 10 Nov 2024 21:03:31 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sun, 10 Nov 2024 21:03:31 GMT
ENV TOMCAT_MAJOR=11
# Sun, 10 Nov 2024 21:03:31 GMT
ENV TOMCAT_VERSION=11.0.1
# Sun, 10 Nov 2024 21:03:31 GMT
ENV TOMCAT_SHA512=dce8800532c9dcb079d456e9ea561ac9b7c854a8c50dfcd78339d077f9db127d86dba339db3fcea16c75039c9201c3446ecd4807efe0d42fcf005d2061cbc090
# Sun, 10 Nov 2024 21:03:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Sun, 10 Nov 2024 21:03:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sun, 10 Nov 2024 21:03:31 GMT
EXPOSE map[8080/tcp:{}]
# Sun, 10 Nov 2024 21:03:31 GMT
ENTRYPOINT []
# Sun, 10 Nov 2024 21:03:31 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a900d84d7bc826cc48aa6025b009b9237a6520a839e83739c6a27d99c7a9693`  
		Last Modified: Sat, 16 Nov 2024 03:10:20 GMT  
		Size: 24.2 MB (24159194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfbb8418c3ad13a95669807340252c75f023c3057e450d2c87b6c8906dd4922`  
		Last Modified: Sat, 16 Nov 2024 03:11:48 GMT  
		Size: 155.8 MB (155805615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84dac08c17b5311af42ed8611c1153da10a0c41ce51bf543e7ff1f9ec17987ce`  
		Last Modified: Sat, 16 Nov 2024 03:11:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7471846698628d290fdd8f4137291e55137d46a9af551cf7ae968f0e5465231c`  
		Last Modified: Sat, 16 Nov 2024 03:11:44 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81fcb998339ad52d0872df50aea42af5b44b03763d4d73c1155b1d97870117e`  
		Last Modified: Sat, 16 Nov 2024 05:01:40 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc957150d93cbaaa23dee5ddb9dd7e7185bd9a3923fcd235b2c63951a30eacc`  
		Last Modified: Sat, 16 Nov 2024 05:01:41 GMT  
		Size: 13.8 MB (13794171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:latest` - unknown; unknown

```console
$ docker pull tomcat@sha256:292abf2e7c561454c931699ba1fd81b02ab51d8471805a669e978e3c8a4fbc28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3586522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f75bae1b46d28d801e6978290083b9d53f3bb1cf9dacb9ffc1b6387a0edec46`

```dockerfile
```

-	Layers:
	-	`sha256:fdc059ff1536788a23c215c424671f0e678dcfd49ec08066b970f09bd83de83d`  
		Last Modified: Sat, 16 Nov 2024 05:01:41 GMT  
		Size: 3.6 MB (3553287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e60c5510967dee116d9caf969b3d0ade16928a93367200ee257774634c8143a7`  
		Last Modified: Sat, 16 Nov 2024 05:01:40 GMT  
		Size: 33.2 KB (33235 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:latest` - linux; ppc64le

```console
$ docker pull tomcat@sha256:dbbf6dfe09d0bc77336cb2b6beb42617fb0d3d0b58d6eef074590319c46bd6c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 MB (230120976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb6ba4333020f99aa4a06086fb3f24e6bdd311acd9bc49c4f35bd996f673eb3`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 16 Oct 2024 09:26:09 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:26:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:26:12 GMT
ADD file:8427b57c40c05cd946f6695dbd1754b0a521a98decd2cdc16eeb114c7128804a in / 
# Wed, 16 Oct 2024 09:26:12 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c654d98404c073b8a7e66bffb27f4ae3e7ede47d13284c132d40a83144bfd8c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='6482639ed9fd22aa2e704cc366848b1b3e1586d2bf1213869c43e80bca58fe5c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='3c6f4c358facfb6c19d90faf02bfe0fc7512d6b0e80ac18146bbd7e0d01deeef';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        riscv64)          ESUM='2f1b3e401e36de803398dfb9818861f9f14ca8ae7db650ea0946ab048fefe3b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='51a7ca42cc2e8cb5f3e7a326c28912ee84ff0791a1ca66650a8c53af07510a7c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
# Sun, 10 Nov 2024 21:03:31 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sun, 10 Nov 2024 21:03:31 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 10 Nov 2024 21:03:31 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sun, 10 Nov 2024 21:03:31 GMT
WORKDIR /usr/local/tomcat
# Sun, 10 Nov 2024 21:03:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sun, 10 Nov 2024 21:03:31 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sun, 10 Nov 2024 21:03:31 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sun, 10 Nov 2024 21:03:31 GMT
ENV TOMCAT_MAJOR=11
# Sun, 10 Nov 2024 21:03:31 GMT
ENV TOMCAT_VERSION=11.0.1
# Sun, 10 Nov 2024 21:03:31 GMT
ENV TOMCAT_SHA512=dce8800532c9dcb079d456e9ea561ac9b7c854a8c50dfcd78339d077f9db127d86dba339db3fcea16c75039c9201c3446ecd4807efe0d42fcf005d2061cbc090
# Sun, 10 Nov 2024 21:03:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Sun, 10 Nov 2024 21:03:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sun, 10 Nov 2024 21:03:31 GMT
EXPOSE map[8080/tcp:{}]
# Sun, 10 Nov 2024 21:03:31 GMT
ENTRYPOINT []
# Sun, 10 Nov 2024 21:03:31 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:991986948126e836a79c1084e3bee33549a43b83cabfe16234aef5b4b30d86f9`  
		Last Modified: Wed, 16 Oct 2024 12:48:24 GMT  
		Size: 34.4 MB (34388822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001f25193f6b4b2c7bb207881b32867e140196a5ddd093c3556ed0479f21cfa1`  
		Last Modified: Sat, 16 Nov 2024 03:02:41 GMT  
		Size: 24.1 MB (24123710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d266be0075c7469ff026951a758565bf46318d94e8e569b3ca13a8eede6e63`  
		Last Modified: Sat, 16 Nov 2024 03:04:46 GMT  
		Size: 157.8 MB (157769201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01064b227b1bbc6cc83a0912bf49635f66d347db2b5a7f4d10cdc0618bd9ee9`  
		Last Modified: Sat, 16 Nov 2024 03:04:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fa406da175dc22648ee27e85f5826b585300fccbe3bc941281e77d3dfae2ab`  
		Last Modified: Sat, 16 Nov 2024 03:04:41 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18b06a4483fa3e71a40cba8abb07097e8795ffd6cdbc13dae0c59b8b8e476bf`  
		Last Modified: Sat, 16 Nov 2024 04:18:58 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b37e94b3aea86e31f7d45ba33b8d6930bf459fccf3840ed895dde73a65ffa4`  
		Last Modified: Sat, 16 Nov 2024 04:19:00 GMT  
		Size: 13.8 MB (13836598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:latest` - unknown; unknown

```console
$ docker pull tomcat@sha256:66da2ca32137024737dba777c12b1d186090d42411cfe81dcd3ae63930ad38d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3502660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc32ff4fb3dc9d947338f1ec060f6764e6ca8224d416ced3ab6e2da00fc4d2a`

```dockerfile
```

-	Layers:
	-	`sha256:de5701396d681bdd61648262e6b2a4b4caae59bf1c41235c5c22d12b41a51f49`  
		Last Modified: Sat, 16 Nov 2024 04:18:58 GMT  
		Size: 3.5 MB (3469583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8e7db22db3b07ec60a9d85cc48e692a59130ed59d7a78c3a029984dd5ad7fac`  
		Last Modified: Sat, 16 Nov 2024 04:18:58 GMT  
		Size: 33.1 KB (33077 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:latest` - linux; riscv64

```console
$ docker pull tomcat@sha256:08d02c170a622796bdd784e518e840ab869958d3d821c0391cc442ba70b4d276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218441225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed13537c7919057794e80b5a25f8561f7df6035b043d9844602186484d3a7c61`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 16 Oct 2024 10:27:02 GMT
ARG RELEASE
# Wed, 16 Oct 2024 10:27:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 10:27:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 10:27:03 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 10:27:43 GMT
ADD file:c7a07ab82f7f269608b3c78a3d2b0cd74630ea7220aee252fb2a61f78978b08f in / 
# Wed, 16 Oct 2024 10:27:46 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c654d98404c073b8a7e66bffb27f4ae3e7ede47d13284c132d40a83144bfd8c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='6482639ed9fd22aa2e704cc366848b1b3e1586d2bf1213869c43e80bca58fe5c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='3c6f4c358facfb6c19d90faf02bfe0fc7512d6b0e80ac18146bbd7e0d01deeef';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        riscv64)          ESUM='2f1b3e401e36de803398dfb9818861f9f14ca8ae7db650ea0946ab048fefe3b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='51a7ca42cc2e8cb5f3e7a326c28912ee84ff0791a1ca66650a8c53af07510a7c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
# Sun, 10 Nov 2024 21:03:31 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sun, 10 Nov 2024 21:03:31 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 10 Nov 2024 21:03:31 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sun, 10 Nov 2024 21:03:31 GMT
WORKDIR /usr/local/tomcat
# Sun, 10 Nov 2024 21:03:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sun, 10 Nov 2024 21:03:31 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sun, 10 Nov 2024 21:03:31 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sun, 10 Nov 2024 21:03:31 GMT
ENV TOMCAT_MAJOR=11
# Sun, 10 Nov 2024 21:03:31 GMT
ENV TOMCAT_VERSION=11.0.1
# Sun, 10 Nov 2024 21:03:31 GMT
ENV TOMCAT_SHA512=dce8800532c9dcb079d456e9ea561ac9b7c854a8c50dfcd78339d077f9db127d86dba339db3fcea16c75039c9201c3446ecd4807efe0d42fcf005d2061cbc090
# Sun, 10 Nov 2024 21:03:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Sun, 10 Nov 2024 21:03:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sun, 10 Nov 2024 21:03:31 GMT
EXPOSE map[8080/tcp:{}]
# Sun, 10 Nov 2024 21:03:31 GMT
ENTRYPOINT []
# Sun, 10 Nov 2024 21:03:31 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ee732b5fddd0a964c04b11ad9b9ec9f70f7df9e1e96825973cdf803cf1fba8e5`  
		Last Modified: Wed, 16 Oct 2024 12:48:30 GMT  
		Size: 31.0 MB (30980747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c251c6a2899e7644ba563148cdf09327aa837220b5924f7dcc4a0528f2a39643`  
		Last Modified: Sat, 16 Nov 2024 04:47:44 GMT  
		Size: 20.1 MB (20136777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60cfa127faed0597792d0e0fb5eac6b4fc1cf90e85f9aa2c6f0290ab2fc7ca8`  
		Last Modified: Sat, 16 Nov 2024 04:59:28 GMT  
		Size: 153.3 MB (153340918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c4e1ff0caf4b4b152b2b07a9e775927363c3d198acbcfd6319305f776ab2e6`  
		Last Modified: Sat, 16 Nov 2024 04:59:06 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f5d32525ff32ff734c86c1458f0d212588eb85d6a5d6e1d3d3231a48aa80d`  
		Last Modified: Sat, 16 Nov 2024 04:59:07 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740c3d484aa66bc41f4d86c12596342493598d1f68ceb959532c790db5c1a0cb`  
		Last Modified: Sat, 16 Nov 2024 08:11:21 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e1a3ffb40aad98da4487252725cd5f2a8092f80a4df037808c59b5789ea13e`  
		Last Modified: Sat, 16 Nov 2024 08:11:23 GMT  
		Size: 14.0 MB (13980137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:latest` - unknown; unknown

```console
$ docker pull tomcat@sha256:4b8f6bc2f4bb2c0c795904a766486a33dbb45fc2dc0b4a19ce8a526a4dad412a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3562539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d80b118c6e9f84fd5dcdce28dad5d6604de820ecaa9cea84a93a9423f55fd9b`

```dockerfile
```

-	Layers:
	-	`sha256:76c045bd3386b6969527810393a61e2c79bf9e3da77807cfb729c64410d04297`  
		Last Modified: Sat, 16 Nov 2024 08:11:22 GMT  
		Size: 3.5 MB (3529463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cf3ad2721cec39fbc6e91ec2ae70167a03c1921d61e64317aa2eb824994526a`  
		Last Modified: Sat, 16 Nov 2024 08:11:21 GMT  
		Size: 33.1 KB (33076 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:latest` - linux; s390x

```console
$ docker pull tomcat@sha256:20876202414123c2e4335c20f4bd631b236f5b323a1048af8724cde900ceba03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.9 MB (212852122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa575b58e8c7c0e34d84026389b5fd7bf2e4ce8e19334c83a33e7ce768916262`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:33 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:33 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:34 GMT
ADD file:1c592b6de2557bde912d6291330e1604327193966f24da30f3ecf513f06fd372 in / 
# Wed, 16 Oct 2024 09:25:34 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c654d98404c073b8a7e66bffb27f4ae3e7ede47d13284c132d40a83144bfd8c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='6482639ed9fd22aa2e704cc366848b1b3e1586d2bf1213869c43e80bca58fe5c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='3c6f4c358facfb6c19d90faf02bfe0fc7512d6b0e80ac18146bbd7e0d01deeef';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        riscv64)          ESUM='2f1b3e401e36de803398dfb9818861f9f14ca8ae7db650ea0946ab048fefe3b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='51a7ca42cc2e8cb5f3e7a326c28912ee84ff0791a1ca66650a8c53af07510a7c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
# Sun, 10 Nov 2024 21:03:31 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sun, 10 Nov 2024 21:03:31 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 10 Nov 2024 21:03:31 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sun, 10 Nov 2024 21:03:31 GMT
WORKDIR /usr/local/tomcat
# Sun, 10 Nov 2024 21:03:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sun, 10 Nov 2024 21:03:31 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sun, 10 Nov 2024 21:03:31 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sun, 10 Nov 2024 21:03:31 GMT
ENV TOMCAT_MAJOR=11
# Sun, 10 Nov 2024 21:03:31 GMT
ENV TOMCAT_VERSION=11.0.1
# Sun, 10 Nov 2024 21:03:31 GMT
ENV TOMCAT_SHA512=dce8800532c9dcb079d456e9ea561ac9b7c854a8c50dfcd78339d077f9db127d86dba339db3fcea16c75039c9201c3446ecd4807efe0d42fcf005d2061cbc090
# Sun, 10 Nov 2024 21:03:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Sun, 10 Nov 2024 21:03:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sun, 10 Nov 2024 21:03:31 GMT
EXPOSE map[8080/tcp:{}]
# Sun, 10 Nov 2024 21:03:31 GMT
ENTRYPOINT []
# Sun, 10 Nov 2024 21:03:31 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4d3763c838a1509ac75e9b37aa0fba11067b054033fda0d642f7e32e542b7994`  
		Last Modified: Wed, 16 Oct 2024 12:48:36 GMT  
		Size: 30.0 MB (30021284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b2aa4a2ac6ac217d3990eff03dbba965ca4d16cdad20e3d86e3b31b6bc12c3`  
		Last Modified: Sat, 16 Nov 2024 02:59:35 GMT  
		Size: 22.2 MB (22151236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244cc0ec802c493c4f3e5216e3e0c8642007c742c8e0222ca56ebecb8fb4c8e1`  
		Last Modified: Sat, 16 Nov 2024 03:01:28 GMT  
		Size: 146.9 MB (146869598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13bb6a6e6c68358a5bd74bad82257116787c082ff6cda93af6ec464f36feb75b`  
		Last Modified: Sat, 16 Nov 2024 03:01:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c34abcdbf61b8b983fd236c7939fcd088648982b06a28053a971742822f37b2`  
		Last Modified: Sat, 16 Nov 2024 03:01:21 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cae0fbc4006fd8a721da9b6faad69d06f752caa737dd7ba2c8276b20832086`  
		Last Modified: Sat, 16 Nov 2024 03:54:07 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46c3041ad3ef9a1683ad0bc489f47bb4c293cf1f3813efc346e70fbd736db80`  
		Last Modified: Sat, 16 Nov 2024 03:54:07 GMT  
		Size: 13.8 MB (13807360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:latest` - unknown; unknown

```console
$ docker pull tomcat@sha256:8f13a8265d9f6b377c412793b8efd3e3a9a0db0280344ff5d1a0a3a8d980c120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3400541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbbf8b45a2a798617e05222438521e5ff6eb7adfe45fa32681f70a263e1ae660`

```dockerfile
```

-	Layers:
	-	`sha256:b6be15c0df92a404c133aa1096ba647322f6c74e19d405345cded22eac9e4bb9`  
		Last Modified: Sat, 16 Nov 2024 03:54:07 GMT  
		Size: 3.4 MB (3367584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a514067c5426933978e4c59d85923ec4f22bfeb832dca7690996bef1b43441e0`  
		Last Modified: Sat, 16 Nov 2024 03:54:07 GMT  
		Size: 33.0 KB (32957 bytes)  
		MIME: application/vnd.in-toto+json
