## `tomcat:jre21-temurin-noble`

```console
$ docker pull tomcat@sha256:a46468c4a117d5a86d4d1112488511cf42754d67256d0bd677a2e80a32afad89
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

### `tomcat:jre21-temurin-noble` - linux; amd64

```console
$ docker pull tomcat@sha256:f761726293627434fdf3710f23bdfebaacbd5ea56c959c20361765079231dff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113363950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5a172f027584430f6615d5e4586e65a3a2bc575ca2271019688a99b2175804`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='553dda64b3b1c3c16f8afe402377ffebe64fb4a1721a46ed426a91fd18185e62';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='e4d02c33aeaf8e1148c1c505e129a709c5bc1889e855d4fb4f001b1780db42b4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='ae9ad61578da420fa7aeb01d3f6909da8a74d54a31bb8ba090a263cfadf221cc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        riscv64)          ESUM='c6fe71bb6ce61366242073e3904c4f51613252a885d54be81c65d3fadd2c5b7c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='19f457a67c281dac23a1b39794912db6353ee4ba45f9299e58b0251a4faf3141';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sun, 10 Nov 2024 21:03:31 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f4e1e5964a2670bf6585bd717c828a78fd1fb5260797f91c08e9dcf80f368e`  
		Last Modified: Thu, 24 Oct 2024 00:58:16 GMT  
		Size: 17.0 MB (16965841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bbfd397c32e987af3d1cd2385bdb0707c819d2b8fa85532ae58d499020251d`  
		Last Modified: Thu, 24 Oct 2024 00:58:17 GMT  
		Size: 52.9 MB (52870634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49417b731e328b9fa6b0857e3c9afff455ea3af6fb5ba8db3cfc0ebb6371cb47`  
		Last Modified: Thu, 24 Oct 2024 00:58:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de562bd73c0a386558dcbd6263edec485eea0ab5153e60c2deffc22c60b036de`  
		Last Modified: Thu, 24 Oct 2024 00:58:16 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea14f5ada9b49050ba172bd347aed8dcfe33ea99cbfa58df4f9bed7baa3b2b48`  
		Last Modified: Mon, 11 Nov 2024 20:49:10 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3613cc6742233143faa0eef3ff1005db988188151e4e8b59b3c25c7f3a03688`  
		Last Modified: Mon, 11 Nov 2024 20:49:11 GMT  
		Size: 13.6 MB (13551425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35aabfe232a44abd407396da399c854b42838184d0b96306b570029bc8376c34`  
		Last Modified: Mon, 11 Nov 2024 20:49:10 GMT  
		Size: 223.0 KB (223042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:591448b1904a56515e48c2f338f880beb4212f757c575d15df63ef4a6bab1d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3211168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ddf17d91de82e91bd154d2439ae3b2db29eee76c284b13e02ea228620e55e5`

```dockerfile
```

-	Layers:
	-	`sha256:c780c02988ac148c40993448f242b3d25f3b3ac4d36cbf23a1b301c8514f0c45`  
		Last Modified: Mon, 11 Nov 2024 20:49:10 GMT  
		Size: 3.2 MB (3186583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e46199db0b0d8818815ef6fb46505040f212a847d7fc540c71fcc6270a46d34`  
		Last Modified: Mon, 11 Nov 2024 20:49:10 GMT  
		Size: 24.6 KB (24585 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-noble` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:3a4118307963bec6b917b51bc301f8320e71b011873136a7d8299facf8c1c400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111683263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b444040d4cc89c6644b7a4d08cc3e7db42c07a8e07ceb6bef9076f4507adf3b1`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='553dda64b3b1c3c16f8afe402377ffebe64fb4a1721a46ed426a91fd18185e62';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='e4d02c33aeaf8e1148c1c505e129a709c5bc1889e855d4fb4f001b1780db42b4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='ae9ad61578da420fa7aeb01d3f6909da8a74d54a31bb8ba090a263cfadf221cc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        riscv64)          ESUM='c6fe71bb6ce61366242073e3904c4f51613252a885d54be81c65d3fadd2c5b7c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='19f457a67c281dac23a1b39794912db6353ee4ba45f9299e58b0251a4faf3141';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sun, 10 Nov 2024 21:03:31 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e2f7d4d887134d9aff4c6177e18f66336c5f3549bb3d16b0c27622e2b8b22c`  
		Last Modified: Thu, 24 Oct 2024 00:59:40 GMT  
		Size: 17.0 MB (16980397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f433545459dd4dc6b933ae31372c4a3ec04903ba6d8dadb260d4020bf01633b1`  
		Last Modified: Thu, 24 Oct 2024 01:18:21 GMT  
		Size: 52.0 MB (52035470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ef7e02195399c72372fe0305c9bd08ac4e735673063381c17ec50b56f25ee9`  
		Last Modified: Thu, 24 Oct 2024 01:18:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18762520b10fd2f80afbc9ce76528c07cc1b41ee1aadf8a0acba4d1ef70b5ea4`  
		Last Modified: Thu, 24 Oct 2024 01:18:19 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6280ad5164412b43bb59dc1008277c64915fa3d21699cd3d71327c0d540046`  
		Last Modified: Mon, 11 Nov 2024 20:49:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fa194aa173a0e00f0999e7156b96970eaafab30d89b54b5baf3a37fa580994`  
		Last Modified: Mon, 11 Nov 2024 20:49:01 GMT  
		Size: 13.6 MB (13555485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029d02ea8c739b251e502a37c5a9bbd88a1189347fcc7314f61923182e011139`  
		Last Modified: Mon, 11 Nov 2024 20:49:00 GMT  
		Size: 223.4 KB (223423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:b825d6df3d1eff8886208acd1bc0ea6cd376ff739ae2e7b1fe2fc406eb11706c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3211991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7beb93c3011bedfa7629f85a94c7782651f1ced470fa012f510d968796e025a`

```dockerfile
```

-	Layers:
	-	`sha256:7e3081fbeec2911a6210b63d89e25abaacc535f8fc9dfd308bfaf3234d241966`  
		Last Modified: Mon, 11 Nov 2024 20:49:00 GMT  
		Size: 3.2 MB (3187150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a3f915af4c91b69ba62536d47dfad547271daf648c9ba00c16d88867a31b39`  
		Last Modified: Mon, 11 Nov 2024 20:49:00 GMT  
		Size: 24.8 KB (24841 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-noble` - linux; ppc64le

```console
$ docker pull tomcat@sha256:d70e65643551327105e5ac7ae6cb696553ae9a3d4553d459cc5af1c3be43ef9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119979235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a3584980349d764815a96d632abaeaafaf903bccf8e2a3ab075f91304f5e1b`
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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='553dda64b3b1c3c16f8afe402377ffebe64fb4a1721a46ed426a91fd18185e62';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='e4d02c33aeaf8e1148c1c505e129a709c5bc1889e855d4fb4f001b1780db42b4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='ae9ad61578da420fa7aeb01d3f6909da8a74d54a31bb8ba090a263cfadf221cc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        riscv64)          ESUM='c6fe71bb6ce61366242073e3904c4f51613252a885d54be81c65d3fadd2c5b7c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='19f457a67c281dac23a1b39794912db6353ee4ba45f9299e58b0251a4faf3141';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sun, 10 Nov 2024 21:03:31 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:fa4ad667811bd0f6cf0781e97a793020501b77190fe2f1e993ed8ff99f2f6957`  
		Last Modified: Sat, 16 Nov 2024 02:58:20 GMT  
		Size: 18.8 MB (18845383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd528c9176d76d9d78034154d36169ed08715a43d2fb819da314711183d3496`  
		Last Modified: Sat, 16 Nov 2024 03:05:37 GMT  
		Size: 52.9 MB (52917702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c4aed05ebfe334a09b7a7afac94a81a038bdad64db4826ae231121c1565fce`  
		Last Modified: Sat, 16 Nov 2024 03:05:35 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713c93cc2e98b3314becc8313284accab4f9127f285cd252ae79a447e1207f77`  
		Last Modified: Sat, 16 Nov 2024 03:05:35 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c1a4ab9d52b743b4f00c00b2ab970af0c6c65fe36170936f7a6400ecdea4b6`  
		Last Modified: Sat, 16 Nov 2024 04:54:50 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e55797388a58f486678e74b611ea47d64d146bc34339cfd371a85e87b5f0231`  
		Last Modified: Sat, 16 Nov 2024 04:54:51 GMT  
		Size: 13.6 MB (13569489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662ce60a78ef05101a9526f257f93c99c3073cbb199ad4bb8bb76c81a66a537a`  
		Last Modified: Sat, 16 Nov 2024 04:54:51 GMT  
		Size: 255.2 KB (255196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:336cdcd1c2d3ebf06fb5d8191aa1a1b4b9ec0b80f873552a6c7fc98d192e6eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3215269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ccd9c4830da5c8663425b4be992b9e90d69d2878ed8a109a83a01265ccb640f`

```dockerfile
```

-	Layers:
	-	`sha256:d0a1da3d9cb39ae3a3c0a72b4e4dd52cf773234d45d93a953ffd96a812dec8d3`  
		Last Modified: Sat, 16 Nov 2024 04:54:50 GMT  
		Size: 3.2 MB (3190578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5dbd8e85cd55e17d18d23bf8830b897af99cf6149f7f5be5c08743be17af8b9`  
		Last Modified: Sat, 16 Nov 2024 04:54:50 GMT  
		Size: 24.7 KB (24691 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-noble` - linux; riscv64

```console
$ docker pull tomcat@sha256:6bde4219472438fea74e10e62fcb8e026cece3aeac903109abfc8ed8194c3c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113412243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e056bf752b6c96b15f643b7080a12d0583a5768a99fedcc6e7ba9de4665f90`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 11 Oct 2024 04:10:39 GMT
ARG RELEASE
# Fri, 11 Oct 2024 04:10:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 04:10:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 04:10:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 04:11:12 GMT
ADD file:008d2e9e73153005eafa485b2ecca3ca9fd6996da5b5c99a52a7376427350f8d in / 
# Fri, 11 Oct 2024 04:11:15 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='553dda64b3b1c3c16f8afe402377ffebe64fb4a1721a46ed426a91fd18185e62';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='e4d02c33aeaf8e1148c1c505e129a709c5bc1889e855d4fb4f001b1780db42b4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='ae9ad61578da420fa7aeb01d3f6909da8a74d54a31bb8ba090a263cfadf221cc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        riscv64)          ESUM='c6fe71bb6ce61366242073e3904c4f51613252a885d54be81c65d3fadd2c5b7c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='19f457a67c281dac23a1b39794912db6353ee4ba45f9299e58b0251a4faf3141';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sun, 10 Nov 2024 21:03:31 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:53300d777b1a34c849b57f3a3ccdc52f3ad795ea045079e7bcca5f63efab0327`  
		Last Modified: Fri, 11 Oct 2024 05:07:42 GMT  
		Size: 31.0 MB (30951587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b034b6bf1d610e42b01c0ae38777b5345955d3015ac8af26f0d4cd3b1c9326`  
		Last Modified: Thu, 24 Oct 2024 01:08:07 GMT  
		Size: 17.9 MB (17861495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7d58d5ad0b07c0da11d9a887d80aaf7fc31655bca47228fd5aeb77926bbb08`  
		Last Modified: Thu, 24 Oct 2024 01:18:02 GMT  
		Size: 50.6 MB (50631761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b9a0864c173941c5028734fc678f62280885919ae1796c4712bf748c90c48c`  
		Last Modified: Thu, 24 Oct 2024 01:17:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9128bad2f3b793a9312d64d8a79a4cf4bfb442f3468eedd185e1ab0694fee474`  
		Last Modified: Thu, 24 Oct 2024 01:17:54 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30449cb394c817b69148cd6b4d4123128db476cf20296a64950aafb0d038867a`  
		Last Modified: Thu, 24 Oct 2024 03:12:04 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295aa9fa21387e9b99eb091168d6ceee6fbabd821b6ec13ed4b18ff61230a209`  
		Last Modified: Mon, 11 Nov 2024 21:01:57 GMT  
		Size: 13.7 MB (13739005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62590aa6690f0863026a68501c2c4eab7ce68cd9aee59da9a2579199f94fa708`  
		Last Modified: Mon, 11 Nov 2024 21:01:55 GMT  
		Size: 225.8 KB (225752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:cac06f3e778a84716f96b55df31a724edc6bc7cc5e9995784f43f5b6e496a5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3203571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad33684ca10ef80a19c6095370cbc9af1f88ecc274d7e1a4888de06a6aa4566`

```dockerfile
```

-	Layers:
	-	`sha256:ce816d073ef55a3671d73df0b100d6aaac58efdfd87528fc6a742eabde8def27`  
		Last Modified: Mon, 11 Nov 2024 21:01:55 GMT  
		Size: 3.2 MB (3178880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d683c7cbc2782e5e44fda16a9de8465dd180363703387c312553861044a70c5e`  
		Last Modified: Mon, 11 Nov 2024 21:01:54 GMT  
		Size: 24.7 KB (24691 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-noble` - linux; s390x

```console
$ docker pull tomcat@sha256:dd7e8d3dc021b042bddab5d94bfcc938cd2a24b066c47ac81f3745eb0d755229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110895510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b598d13620913b4677136ed3c9a66d5c8240ab35b949096b9bf5e51383a7d0ef`
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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='553dda64b3b1c3c16f8afe402377ffebe64fb4a1721a46ed426a91fd18185e62';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='e4d02c33aeaf8e1148c1c505e129a709c5bc1889e855d4fb4f001b1780db42b4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='ae9ad61578da420fa7aeb01d3f6909da8a74d54a31bb8ba090a263cfadf221cc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        riscv64)          ESUM='c6fe71bb6ce61366242073e3904c4f51613252a885d54be81c65d3fadd2c5b7c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='19f457a67c281dac23a1b39794912db6353ee4ba45f9299e58b0251a4faf3141';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sun, 10 Nov 2024 21:03:31 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:f845038dbacd71c7a90fc09ab3576d8c8efc94076ad0ba4354f3b478332e4d6d`  
		Last Modified: Sat, 16 Nov 2024 02:57:37 GMT  
		Size: 17.6 MB (17612457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f662b276a95da2e6e2a14ffb7098bf35259ab7183b9646184f32e05ffd491e0`  
		Last Modified: Sat, 16 Nov 2024 03:02:13 GMT  
		Size: 49.5 MB (49467186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12441017c67006f53ece422b3e1dd5a1601245437acde575ff4a3ea437b13d7a`  
		Last Modified: Sat, 16 Nov 2024 03:02:12 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5de4c0cc94ba7ac5fdef44e5e4d3efcec3619c0679ad6e5c7eaec03f53aec06`  
		Last Modified: Sat, 16 Nov 2024 03:02:12 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14e63e5076cba142541e8d5a29a43c6805a8a262396f6ae6e0a1fe335355d5a`  
		Last Modified: Sat, 16 Nov 2024 04:52:30 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e21c9d6b8b8ccb2bd383b6e0b28ba9b78003a695c0f5665b71ca75d4f16520c`  
		Last Modified: Sat, 16 Nov 2024 04:52:32 GMT  
		Size: 13.6 MB (13560643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84dd36ab30c03f80e47641d80c15351a254d1b9f8fecb026cca74d6fe506a17`  
		Last Modified: Sat, 16 Nov 2024 04:52:31 GMT  
		Size: 231.3 KB (231295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:df609dded2c64b13f7790be31cd39769ad6e5312adb893aa25b72409e9401146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3213386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bd554162e7b4f3e155650e1c10a38bae5663c0cf87008f6f760c3624fd876b`

```dockerfile
```

-	Layers:
	-	`sha256:a40d51f8ecc89b45f40e4a0584243143cbea9fa39aa0a40d82d17276d3564fe7`  
		Last Modified: Sat, 16 Nov 2024 04:52:30 GMT  
		Size: 3.2 MB (3188802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ba02f04d8114b5462e1c372a136733a720bc00aa2cc11584e406d3fec476b2`  
		Last Modified: Sat, 16 Nov 2024 04:52:30 GMT  
		Size: 24.6 KB (24584 bytes)  
		MIME: application/vnd.in-toto+json
