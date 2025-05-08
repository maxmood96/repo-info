## `tomcat:9-jdk21-temurin-noble`

```console
$ docker pull tomcat@sha256:4f86d0f775dc1e17dc20a52d45aeb627648c1678d4fbcfddb08fe6e25185821b
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

### `tomcat:9-jdk21-temurin-noble` - linux; amd64

```console
$ docker pull tomcat@sha256:c6629d6a67932222be6fa648a0ca213ff132e1416a77e8c1069d1682d4a7989e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.0 MB (224028166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee60fcb2c1eca53d67591035a743ad4da1d10ebac1514670fbe923a4d2c00160`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 09 Apr 2025 20:03:41 GMT
ARG RELEASE
# Wed, 09 Apr 2025 20:03:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Apr 2025 20:03:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Apr 2025 20:03:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 09 Apr 2025 20:03:41 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Wed, 09 Apr 2025 20:03:41 GMT
CMD ["/bin/bash"]
# Wed, 09 Apr 2025 20:03:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Apr 2025 20:03:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 20:03:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='974d3acef0b7193f541acb61b76e81670890551366625d4f6ca01b91ac152ce0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='31dba70ba928c78c20d62049ac000f79f7a7ab11f9d9c11e703f52d60aa64f93';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='2ddc0dc14b07d9e853875aac7f84c23826fff18b9cea618c93efe0bcc8f419c2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='d75f33ee7f9e5532bce263db83443ffed7d9bae7ff3ed41e48d137808adfe513';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='216edbccab2d677639c90d2cb09dfa39c257788a62b8b83d879528c447b9ad33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Apr 2025 20:03:41 GMT
CMD ["jshell"]
# Wed, 09 Apr 2025 20:03:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Apr 2025 20:03:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 20:03:41 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Apr 2025 20:03:41 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_MAJOR=9
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_VERSION=9.0.104
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_SHA512=b387fae59f1eda13a5c2336243514d9568057815689057ff920be696548ea6afbcfc0933934d3d6f8c4e2b5108322dc7509bfe934c49d05905c6ce87f1dff53c
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Apr 2025 20:03:41 GMT
ENTRYPOINT []
# Wed, 09 Apr 2025 20:03:41 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f526e30db5f3400aedfafd9fee4a897e6136cad2ba5377063a3ba2f4d9372697`  
		Last Modified: Thu, 08 May 2025 17:04:57 GMT  
		Size: 23.0 MB (22952890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bb17fdf011e86a2dc27b9b6d8df16cacad4a411aaf601bc9ab24f7f4b326db`  
		Last Modified: Thu, 08 May 2025 17:05:04 GMT  
		Size: 157.6 MB (157648162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4223556ed03c6bd1c69dff886afb2d3500c92850eaa663c9d88b1c0488b7f7a9`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0cc8efa6ea79682d3418b90549eda220179c60092f15c979408627839067c6c`  
		Last Modified: Thu, 08 May 2025 17:04:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6df55e2301a7fd6960e1c1159dc62d64cabe5afac5e04f370d2ebfac70135da`  
		Last Modified: Thu, 08 May 2025 17:09:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d0bd0581d5497cac4ad79bc2b362ef74c4c6672711feada04e8e8ea5bb3161`  
		Last Modified: Thu, 08 May 2025 17:09:56 GMT  
		Size: 13.7 MB (13706941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk21-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:02e1b019c83b6274ae9cf15591905c285685f1606168d5e34d930fb3289d1807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3447597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cfeeb0debffd8590847b1f1ecd139d0aa4ccf4f6bc8215a1fafe08804c4ad34`

```dockerfile
```

-	Layers:
	-	`sha256:f354cc7d779e50e3560eddfd792e5bdcd39d7a7ac0b312260bd5134f61b7f2b7`  
		Last Modified: Mon, 05 May 2025 17:05:50 GMT  
		Size: 3.4 MB (3414489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:680169b5e555791621783595eac77098a25732dcfc83a502197477aa75f98967`  
		Last Modified: Mon, 05 May 2025 17:05:49 GMT  
		Size: 33.1 KB (33108 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jdk21-temurin-noble` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:e91a27610038f9dfa2b4ae30266374897d5c95fc25123b3c3f546ffd3efc7f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.7 MB (222663577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188d4797ddb31ccb6b544df116f4e3e5fae5d5cd17cefbce8552a36951311982`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 09 Apr 2025 20:03:41 GMT
ARG RELEASE
# Wed, 09 Apr 2025 20:03:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Apr 2025 20:03:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Apr 2025 20:03:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 09 Apr 2025 20:03:41 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Wed, 09 Apr 2025 20:03:41 GMT
CMD ["/bin/bash"]
# Wed, 09 Apr 2025 20:03:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Apr 2025 20:03:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 20:03:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='974d3acef0b7193f541acb61b76e81670890551366625d4f6ca01b91ac152ce0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='31dba70ba928c78c20d62049ac000f79f7a7ab11f9d9c11e703f52d60aa64f93';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='2ddc0dc14b07d9e853875aac7f84c23826fff18b9cea618c93efe0bcc8f419c2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='d75f33ee7f9e5532bce263db83443ffed7d9bae7ff3ed41e48d137808adfe513';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='216edbccab2d677639c90d2cb09dfa39c257788a62b8b83d879528c447b9ad33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Apr 2025 20:03:41 GMT
CMD ["jshell"]
# Wed, 09 Apr 2025 20:03:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Apr 2025 20:03:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 20:03:41 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Apr 2025 20:03:41 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_MAJOR=9
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_VERSION=9.0.104
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_SHA512=b387fae59f1eda13a5c2336243514d9568057815689057ff920be696548ea6afbcfc0933934d3d6f8c4e2b5108322dc7509bfe934c49d05905c6ce87f1dff53c
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Apr 2025 20:03:41 GMT
ENTRYPOINT []
# Wed, 09 Apr 2025 20:03:41 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866e6e02a3bf59e32bfbd1d02232a5ba0268ea326e2ed72d9f05413d95c3dad2`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 24.2 MB (24163318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495e17cf917ed9f99f148bed91db100ec46f6f817f356eb12d8076b91dd4f456`  
		Last Modified: Thu, 08 May 2025 17:06:33 GMT  
		Size: 155.9 MB (155931746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966861f2a23809fda596d6f285cb6e4caa902d18bb726d1a7d3656620c2170e0`  
		Last Modified: Thu, 08 May 2025 17:06:18 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1b55ea8a34655b4a97b3358aa49763f45e877cea7287f1b3c34962306d2ccb`  
		Last Modified: Thu, 08 May 2025 17:06:18 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d58fcd48c923b99eb3dce85697c44377a28d168b742277d32532ae6791a08b0`  
		Last Modified: Thu, 08 May 2025 17:09:25 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33486be8fc71ae6b73e1842659758d5633453d0d2042a15151b05fac68da2386`  
		Last Modified: Thu, 08 May 2025 17:09:31 GMT  
		Size: 13.7 MB (13718992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk21-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:9cb211b897a69875a29210b9d0184f99a524aebaeb7d1fb3febc8e7db0868450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3579444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af392a6918f018c508e6f044136bb4d0b692403399091b7d047364e37079ef5`

```dockerfile
```

-	Layers:
	-	`sha256:35421318c54092cdbe011d7ed98bdc1a439a5140f001e0ebe982341ecd8271e1`  
		Last Modified: Mon, 05 May 2025 23:48:35 GMT  
		Size: 3.5 MB (3546106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c94421e9f9925867a8f0b39fad09030204ed2c6c86810c7afed1ad2808b1e77`  
		Last Modified: Mon, 05 May 2025 23:48:35 GMT  
		Size: 33.3 KB (33338 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jdk21-temurin-noble` - linux; ppc64le

```console
$ docker pull tomcat@sha256:937e1c41f6d5aef31b64ef727d84ab05b5f12cc2c741229879cc5bb348c9ff79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230039972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad2249c9f879bdb67766039ce7ffc00bcf6676b032504b00cbd406dc8f1a34b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 09 Apr 2025 20:03:41 GMT
ARG RELEASE
# Wed, 09 Apr 2025 20:03:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Apr 2025 20:03:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Apr 2025 20:03:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 09 Apr 2025 20:03:41 GMT
ADD file:d4d363297b0bc97147d6215ececd915564f3540c035d4c68fcdd781acaf0e4e7 in / 
# Wed, 09 Apr 2025 20:03:41 GMT
CMD ["/bin/bash"]
# Wed, 09 Apr 2025 20:03:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Apr 2025 20:03:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 20:03:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='974d3acef0b7193f541acb61b76e81670890551366625d4f6ca01b91ac152ce0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='31dba70ba928c78c20d62049ac000f79f7a7ab11f9d9c11e703f52d60aa64f93';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='2ddc0dc14b07d9e853875aac7f84c23826fff18b9cea618c93efe0bcc8f419c2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='d75f33ee7f9e5532bce263db83443ffed7d9bae7ff3ed41e48d137808adfe513';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='216edbccab2d677639c90d2cb09dfa39c257788a62b8b83d879528c447b9ad33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Apr 2025 20:03:41 GMT
CMD ["jshell"]
# Wed, 09 Apr 2025 20:03:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Apr 2025 20:03:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 20:03:41 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Apr 2025 20:03:41 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_MAJOR=9
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_VERSION=9.0.104
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_SHA512=b387fae59f1eda13a5c2336243514d9568057815689057ff920be696548ea6afbcfc0933934d3d6f8c4e2b5108322dc7509bfe934c49d05905c6ce87f1dff53c
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Apr 2025 20:03:41 GMT
ENTRYPOINT []
# Wed, 09 Apr 2025 20:03:41 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Thu, 08 May 2025 17:06:29 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a771c473cdefa85f44a1eb7423dd469274b8d77a56b43b501291b0d7983a261`  
		Last Modified: Thu, 08 May 2025 17:24:12 GMT  
		Size: 24.1 MB (24102003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de727d93a22ba5dee3341dcd349bbf3bf4932916d74744ad9a6943828dcaa74`  
		Last Modified: Thu, 08 May 2025 17:49:28 GMT  
		Size: 157.8 MB (157818226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a197be8f8f79bf0b7934753a1fc789761a8fd6c89a755525e27510d1a93e125`  
		Last Modified: Thu, 08 May 2025 17:49:33 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec532ef4e486f0e03a1d89dea161bafa7fcd9c6253ac43d4796066650ffe163`  
		Last Modified: Thu, 08 May 2025 17:49:34 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee5783ac5f83c8665715b54bcc8d5e7d3a25d3441cacf40f6c27b2fbdadebf`  
		Last Modified: Mon, 05 May 2025 20:42:29 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b836348657caed5af4c6c5f91f8b37ef8903e3a5a5bcd446305cccd5a92bea78`  
		Last Modified: Mon, 05 May 2025 20:58:06 GMT  
		Size: 13.8 MB (13776259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk21-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:e6e9262f87715d48c3d35384c9b2711648d81c52281e721f2480f837b5866bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3495768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9434ed5e31d0efa0b50758dd2473df3dd64e825a4b0210ab77c84bb44744cb5`

```dockerfile
```

-	Layers:
	-	`sha256:9c55ff2826b1e6da7a0b0de181206a07fbea73ce3b99f01c4ee85d10f716e8fc`  
		Last Modified: Mon, 05 May 2025 20:58:05 GMT  
		Size: 3.5 MB (3462564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d486c63bdecf88fa15e23bb164cccc727b515762317005b52cd197b2696a9eee`  
		Last Modified: Mon, 05 May 2025 20:58:05 GMT  
		Size: 33.2 KB (33204 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jdk21-temurin-noble` - linux; riscv64

```console
$ docker pull tomcat@sha256:7219b17298dcd474b2d7aad734a7bd7227d70e1592a7770369f71ce3b308c740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218766046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a6263db9574fb70e39ae668f5684fea55aeaf9ed998c32e1f994c25ccf5324`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 09 Apr 2025 20:03:41 GMT
ARG RELEASE
# Wed, 09 Apr 2025 20:03:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Apr 2025 20:03:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Apr 2025 20:03:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 09 Apr 2025 20:03:41 GMT
ADD file:a7f5e3a8aff782c57aa8346238f9dd99048f1bf1a67260c5949ae9396a429340 in / 
# Wed, 09 Apr 2025 20:03:41 GMT
CMD ["/bin/bash"]
# Wed, 09 Apr 2025 20:03:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Apr 2025 20:03:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 20:03:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='974d3acef0b7193f541acb61b76e81670890551366625d4f6ca01b91ac152ce0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='31dba70ba928c78c20d62049ac000f79f7a7ab11f9d9c11e703f52d60aa64f93';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='2ddc0dc14b07d9e853875aac7f84c23826fff18b9cea618c93efe0bcc8f419c2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='d75f33ee7f9e5532bce263db83443ffed7d9bae7ff3ed41e48d137808adfe513';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='216edbccab2d677639c90d2cb09dfa39c257788a62b8b83d879528c447b9ad33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Apr 2025 20:03:41 GMT
CMD ["jshell"]
# Wed, 09 Apr 2025 20:03:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Apr 2025 20:03:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 20:03:41 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Apr 2025 20:03:41 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_MAJOR=9
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_VERSION=9.0.104
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_SHA512=b387fae59f1eda13a5c2336243514d9568057815689057ff920be696548ea6afbcfc0933934d3d6f8c4e2b5108322dc7509bfe934c49d05905c6ce87f1dff53c
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Apr 2025 20:03:41 GMT
ENTRYPOINT []
# Wed, 09 Apr 2025 20:03:41 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:617ff4840b8ccb0dd209aefc32c58a25fc5e72effac2d6267be2d5e4f07db22b`  
		Last Modified: Thu, 08 May 2025 17:24:33 GMT  
		Size: 30.9 MB (30943987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c2920441738f4e0ecbf9aa256ef119cae802e2e88d4e659886b77b1d03afce`  
		Last Modified: Thu, 08 May 2025 17:24:34 GMT  
		Size: 20.1 MB (20140066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e64a5fe144e383a51ec766c3e2967e5daa0ed66c3153094f92a3e24378e245`  
		Last Modified: Thu, 08 May 2025 17:49:40 GMT  
		Size: 153.5 MB (153461517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9baf3f7dba9f1377d6539d02650accf6e0d76a6f4c634af4ded458047125201f`  
		Last Modified: Thu, 08 May 2025 17:50:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf0d3a67050f4c194e8a4e9c3fe228e87b2fb08b8e437a3f1cc84437591218c`  
		Last Modified: Thu, 08 May 2025 17:50:07 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417f4be126edfa0c636fb121c53f97aa2da55ac80185410eb30928825f6fef3c`  
		Last Modified: Mon, 05 May 2025 23:52:18 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71369c7bfdf292946ff8bb34de93d761d8326bd08c5681c868ae112879d78ed2`  
		Last Modified: Tue, 06 May 2025 00:19:40 GMT  
		Size: 14.2 MB (14217833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk21-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:54ae34ee2961f33bd501690270e54312ba76bcf0d4800bc6dec19d54812262ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3555535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9f97da93fb590ded5fda5dde3d7bc894f87cd1cc6d77501874663fa21c7b7e8`

```dockerfile
```

-	Layers:
	-	`sha256:f2d9f27d2beadfb2905dd257623f55d7ec27fd1bb13f006df475343b8561cc3c`  
		Last Modified: Tue, 06 May 2025 00:19:38 GMT  
		Size: 3.5 MB (3522331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6546e9e1b0a0e236b43a4e8eb55d73c87586298ad53663250860c319a7052ee`  
		Last Modified: Tue, 06 May 2025 00:19:38 GMT  
		Size: 33.2 KB (33204 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jdk21-temurin-noble` - linux; s390x

```console
$ docker pull tomcat@sha256:acb52007e2f816fe170116aac0eab4569dac912045f27ddb7241bac12d46bce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 MB (212741317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6612779c7fd5f516dd88245b9f712f1a3a7072a009e44251a96c9655d1b5060d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 09 Apr 2025 20:03:41 GMT
ARG RELEASE
# Wed, 09 Apr 2025 20:03:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Apr 2025 20:03:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Apr 2025 20:03:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 09 Apr 2025 20:03:41 GMT
ADD file:486993225aeae656f8d559f5c296f6c3164966e35f4b628d26e1da1b75592143 in / 
# Wed, 09 Apr 2025 20:03:41 GMT
CMD ["/bin/bash"]
# Wed, 09 Apr 2025 20:03:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Apr 2025 20:03:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 20:03:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='974d3acef0b7193f541acb61b76e81670890551366625d4f6ca01b91ac152ce0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='31dba70ba928c78c20d62049ac000f79f7a7ab11f9d9c11e703f52d60aa64f93';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='2ddc0dc14b07d9e853875aac7f84c23826fff18b9cea618c93efe0bcc8f419c2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='d75f33ee7f9e5532bce263db83443ffed7d9bae7ff3ed41e48d137808adfe513';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='216edbccab2d677639c90d2cb09dfa39c257788a62b8b83d879528c447b9ad33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Apr 2025 20:03:41 GMT
CMD ["jshell"]
# Wed, 09 Apr 2025 20:03:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Apr 2025 20:03:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 20:03:41 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Apr 2025 20:03:41 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_MAJOR=9
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_VERSION=9.0.104
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_SHA512=b387fae59f1eda13a5c2336243514d9568057815689057ff920be696548ea6afbcfc0933934d3d6f8c4e2b5108322dc7509bfe934c49d05905c6ce87f1dff53c
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://dlcdn.apache.org/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	curl -fL -o upstream-KEYS 'https://www.apache.org/dist/tomcat/tomcat-9/KEYS'; 	gpg --batch --import upstream-KEYS; 	printf '' > filtered-KEYS; 	for key in 		'DCFD35E0BF8CA7344752DE8B6FB21E8933C60243' 		'A9C5DF4D22E99998D9875A5110C01C5A2F6059E7' 		'48F8E69F6390C9F25CFEDCD268248959359E722B' 	; do 		gpg --batch --fingerprint "$key"; 		gpg --batch --export --armor "$key" >> filtered-KEYS; 	done; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --import filtered-KEYS; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 1777 logs temp work; 		catalina.sh version # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Apr 2025 20:03:41 GMT
ENTRYPOINT []
# Wed, 09 Apr 2025 20:03:41 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:52a1750d5fddc355cdc90a83890b7d582c7f145aa5d114d9582cd010b8ead145`  
		Last Modified: Thu, 08 May 2025 17:05:48 GMT  
		Size: 30.0 MB (29956186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a451b8ee538f96359905687bda902a9d41bf913379c02eccfffcf97272140dfd`  
		Last Modified: Thu, 08 May 2025 17:24:54 GMT  
		Size: 22.1 MB (22131264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a260285ebb9d0a6cbf78a949de236a06376318d0ab384f227418082bed749ebc`  
		Last Modified: Thu, 08 May 2025 17:49:40 GMT  
		Size: 146.9 MB (146922894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9edef1c1e50c33bb57a62edaf18d598dd6e920e735ae838f42ded56f393a1f3`  
		Last Modified: Thu, 08 May 2025 17:49:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951a0aa0d88ace136fafa8d3249ca0a71f0ca11af6e53ba071ac4cf354eb7482`  
		Last Modified: Thu, 08 May 2025 17:49:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b524795e0ad6656e70dfeda4c2fec1979691ffa92ed023b4ef74faeb2806b4`  
		Last Modified: Mon, 05 May 2025 18:55:42 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1e7e2b598503ef444a40130811b9290504b0d390e8eff5e6cdbb1cdf123218`  
		Last Modified: Mon, 05 May 2025 19:05:27 GMT  
		Size: 13.7 MB (13728328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jdk21-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:14193fd79a0f49528d3d82ad7532ee3ef1d8efa4781d0e20ac68fd4491322f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3393815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26caf465fe9d0e410d563e1089c89de0028a7f54aca9a2ff21f24129dbd754ff`

```dockerfile
```

-	Layers:
	-	`sha256:947a0296e3d8781cd29f86951df8200df14f57e8a7bca754d6321583208a874c`  
		Last Modified: Mon, 05 May 2025 19:05:27 GMT  
		Size: 3.4 MB (3360707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a34191d54bcf8ceacfe0fe9be8226c55e05f860e2ddd172ce4282a8d76e691f3`  
		Last Modified: Mon, 05 May 2025 19:05:27 GMT  
		Size: 33.1 KB (33108 bytes)  
		MIME: application/vnd.in-toto+json
