## `tomcat:9-jre8-temurin-jammy`

```console
$ docker pull tomcat@sha256:14cd8f036e46572692898600e3251b0ec6984e60d61583a20ed01eefa766ef53
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

### `tomcat:9-jre8-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:d90b879ea525d4fbd3cc7bbef9da581b59bc35e0dbf0e8fe20522d66cdbb4256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98220010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eafcd127115f5433168ebb8e5a595a8b5fd9a0ff52e7de3d8fae9e14f1791464`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 06 Aug 2024 08:03:42 GMT
ARG RELEASE
# Tue, 06 Aug 2024 08:03:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Aug 2024 08:03:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Aug 2024 08:03:42 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 06 Aug 2024 08:03:42 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 06 Aug 2024 08:03:42 GMT
CMD ["/bin/bash"]
# Tue, 06 Aug 2024 08:03:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 06 Aug 2024 08:03:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 08:03:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0ac516cc1eadffb4cd3cfc9736a33d58ea6a396bf85729036c973482f7c063d9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='8fbefff2c578f73d95118d830347589ddc9aa84510200a5a5001901c2dea4810';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='13bdefdeae6f18bc9c87bba18c853b8b12c5442ce07ff0a3956ce28776d695ff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='2991edbedee448c0f1edf131beca84b415dac64ea97365b9bfd85bc2f39893bb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 06 Aug 2024 08:03:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 06 Aug 2024 08:03:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 08:03:42 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
WORKDIR /usr/local/tomcat
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 08:03:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 08:03:42 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_MAJOR=9
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_VERSION=9.0.93
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_SHA512=3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d
# Tue, 06 Aug 2024 08:03:42 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 06 Aug 2024 08:03:42 GMT
ENTRYPOINT []
# Tue, 06 Aug 2024 08:03:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9bd9906fae2af9b98f929fef09d486905c0599093bb299b441e7eed58ada7`  
		Last Modified: Sat, 17 Aug 2024 01:10:02 GMT  
		Size: 12.9 MB (12870875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9767e5a1ec19ee77bf26b2ecf83fdb289d28cd8f0773eb7b263a2d2174bf40`  
		Last Modified: Sat, 17 Aug 2024 01:10:45 GMT  
		Size: 41.9 MB (41884530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b186f493caa57368974cf2a56c81e4f46f684abbc696ce93344bdba7820b7676`  
		Last Modified: Sat, 17 Aug 2024 01:10:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549fdae8215d87f93f320e0b858daecaf8ec8ca17d44c21986c5a17d9f682905`  
		Last Modified: Fri, 23 Aug 2024 19:25:15 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca55c35f306c8980b611fccf51cc04884b563aa66ba8e993c1fce9b409700dc6`  
		Last Modified: Fri, 23 Aug 2024 21:10:30 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fbf0948012fd56e10cd661d1380cae15fe5d6f5db4cd6477be2ac152e4e096`  
		Last Modified: Fri, 23 Aug 2024 21:10:31 GMT  
		Size: 12.8 MB (12803572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69697bf11373aa2b2791680942eba35e2d3a190f3f9acf3c58bf7a8634779aad`  
		Last Modified: Fri, 23 Aug 2024 21:10:30 GMT  
		Size: 217.9 KB (217880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:f13254407fc98b38a68ad8c527a659ae0005e22effe05c44ff45d64ba2faa54a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5fe12734b17ded312a24367831d3b3f7e0f0a1c6570d8b59e97a86b7ea055e`

```dockerfile
```

-	Layers:
	-	`sha256:354f6cc9b869c2a87160208094818d8c681babcd5939233eab417a3b40c4afc4`  
		Last Modified: Fri, 23 Aug 2024 21:10:30 GMT  
		Size: 3.5 MB (3549250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a933bfb331286687c9d894f6b9f3f31c149f830e96226868bc218447ae0761c`  
		Last Modified: Fri, 23 Aug 2024 21:10:30 GMT  
		Size: 21.9 KB (21861 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:cf4ee1b899b6a2f68374220720da6d481cb6e92d6b4c278d71a32ce95f599c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92510824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89e6fde6c8ff0f7359645556b70ce7271834dd41cf1bb6423a8149ad06059b7`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 06 Aug 2024 08:03:42 GMT
ARG RELEASE
# Tue, 06 Aug 2024 08:03:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Aug 2024 08:03:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Aug 2024 08:03:42 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 06 Aug 2024 08:03:42 GMT
ADD file:ef971273c60fcf0d0b0a4e71a5e5421060cd7c316f1d9af068a193c23dc81d31 in / 
# Tue, 06 Aug 2024 08:03:42 GMT
CMD ["/bin/bash"]
# Tue, 06 Aug 2024 08:03:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 06 Aug 2024 08:03:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 08:03:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0ac516cc1eadffb4cd3cfc9736a33d58ea6a396bf85729036c973482f7c063d9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='8fbefff2c578f73d95118d830347589ddc9aa84510200a5a5001901c2dea4810';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='13bdefdeae6f18bc9c87bba18c853b8b12c5442ce07ff0a3956ce28776d695ff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='2991edbedee448c0f1edf131beca84b415dac64ea97365b9bfd85bc2f39893bb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 06 Aug 2024 08:03:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 06 Aug 2024 08:03:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 08:03:42 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
WORKDIR /usr/local/tomcat
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 08:03:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 08:03:42 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_MAJOR=9
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_VERSION=9.0.93
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_SHA512=3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d
# Tue, 06 Aug 2024 08:03:42 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 06 Aug 2024 08:03:42 GMT
ENTRYPOINT []
# Tue, 06 Aug 2024 08:03:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f2a599e193acb4c0e6567f9f5e0b191f59e170d5062a49d73761ee20623e6788`  
		Last Modified: Fri, 09 Aug 2024 02:12:36 GMT  
		Size: 27.5 MB (27535050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b092dd5a78dc4cf071309a2972d23807d1b19451ad8ff7aae557e8af16e175a`  
		Last Modified: Sat, 17 Aug 2024 01:35:54 GMT  
		Size: 12.5 MB (12463290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e57402a2dc8e3f95d20f16b43585c483d233431d4ca91322fc3860a8f62147`  
		Last Modified: Sat, 17 Aug 2024 01:36:38 GMT  
		Size: 39.6 MB (39581654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c72650c4846b4a093b9b02de3b87d9491d9fdd586b54745b739348de0fb92a8`  
		Last Modified: Sat, 17 Aug 2024 01:36:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ed820591ff1da820cff9784f4f0d2dcf9b4b8c896e8dbad3479a7762b0d82a`  
		Last Modified: Fri, 23 Aug 2024 18:59:18 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304f5917a8dbd88db6394519142af95c6ce5e8a4fc2315588822d81398e06f4b`  
		Last Modified: Fri, 23 Aug 2024 22:37:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f892421a61842fa25fbda171c4f01f4a6945bfe53b0198802a07a0031b15b36a`  
		Last Modified: Fri, 23 Aug 2024 22:37:16 GMT  
		Size: 12.7 MB (12737064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b627d8759448753d38a9c7e042dcf10131bd4f50f8115bf9966902a91197877`  
		Last Modified: Fri, 23 Aug 2024 22:37:15 GMT  
		Size: 191.3 KB (191327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:7a1fde6a0d25aeb1a7b32b85a2866da121e493b137f529a825efdb89206e9518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314ad2cc928010c9fefff51bed92c0779f3df14692eb4db485f84eddb8d8c9d3`

```dockerfile
```

-	Layers:
	-	`sha256:fd7c3b1471442b9c2f28788a241ebcb8d2bc5f0868f855efdbc0bb9b6440c4f3`  
		Last Modified: Fri, 23 Aug 2024 22:37:16 GMT  
		Size: 3.6 MB (3553672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ed4c07c12b79cf27cd4491e90da4440a0ab9bd5a21795c29fc90c4342ec2656`  
		Last Modified: Fri, 23 Aug 2024 22:37:15 GMT  
		Size: 22.0 KB (21988 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:f050a234f13052b3137454f55840f2d57eb429fa962f18eb8aaad63f3eb18293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.1 MB (95096093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff589289a89a3b371d7373abe15d2d924a0a8e1537392c6a84f7b2b83d05aa5d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 06 Aug 2024 08:03:42 GMT
ARG RELEASE
# Tue, 06 Aug 2024 08:03:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Aug 2024 08:03:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Aug 2024 08:03:42 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 06 Aug 2024 08:03:42 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 06 Aug 2024 08:03:42 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0ac516cc1eadffb4cd3cfc9736a33d58ea6a396bf85729036c973482f7c063d9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='8fbefff2c578f73d95118d830347589ddc9aa84510200a5a5001901c2dea4810';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='13bdefdeae6f18bc9c87bba18c853b8b12c5442ce07ff0a3956ce28776d695ff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='2991edbedee448c0f1edf131beca84b415dac64ea97365b9bfd85bc2f39893bb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 06 Aug 2024 08:03:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 06 Aug 2024 08:03:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 08:03:42 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
WORKDIR /usr/local/tomcat
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 08:03:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 08:03:42 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_MAJOR=9
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_VERSION=9.0.93
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_SHA512=3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d
# Tue, 06 Aug 2024 08:03:42 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 06 Aug 2024 08:03:42 GMT
ENTRYPOINT []
# Tue, 06 Aug 2024 08:03:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a13fc23d23d50177fc33d5df0e5c516fdbaae7d5cb53c11d634dff7e6e365e`  
		Last Modified: Sat, 17 Aug 2024 01:33:12 GMT  
		Size: 12.8 MB (12813299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13943cfb982d5485f559e1e41c705e155dae062566151e89637df4ac861bf51`  
		Last Modified: Sat, 17 Aug 2024 01:33:49 GMT  
		Size: 40.9 MB (40856830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3360191bf4921dcdae3cc2285c2fad3a6f04a154ea28249f4f58ad62a64725bf`  
		Last Modified: Sat, 17 Aug 2024 01:33:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b3a4248864654ce3e18048693bd49d77e323e35ce5e94fddc9a726a2faaeeb`  
		Last Modified: Sat, 17 Aug 2024 01:33:45 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b7b7690b4316340cbb216295ebdc20939372eae5fd740f05f1dbfa6a7bc7ca`  
		Last Modified: Sat, 17 Aug 2024 12:51:36 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc76e7bc4ecac1c442b6d8b3ee15d872ecad1edb40c9a14a4004da2a93a895b`  
		Last Modified: Sat, 17 Aug 2024 12:51:36 GMT  
		Size: 12.8 MB (12809845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9b884c00b15e32f7e235ed54fdbeb18de966b9e71f490596221386ecaa5d3e`  
		Last Modified: Sat, 17 Aug 2024 12:51:36 GMT  
		Size: 216.8 KB (216814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:d02828a74b35bcdc1d3800fc643c5cfdd0924b34dbd5d88c938d525240aba60a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a56e86b3796bc29010b655b4af542c4c55d3e2474c32d0a3b40029c07fefb5f`

```dockerfile
```

-	Layers:
	-	`sha256:3ebe13fda7532a3ac225a7d911b9a8696bcc1e8e1b3ccbb8aa33f5101e763a83`  
		Last Modified: Sat, 17 Aug 2024 12:51:36 GMT  
		Size: 3.5 MB (3549530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5803bbe579bd89ef7ff9863adf4e358c4c568207317265a4b0f8de59eca8bb97`  
		Last Modified: Sat, 17 Aug 2024 12:51:36 GMT  
		Size: 22.5 KB (22504 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:18154831f302aac14d072cb34c3015e2043c40a856b4254d1d20cece47ef7583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103632721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41a7f4d556029ac475a9cfba62afe4c77b38731260c2e2018817d6d247ab2b4`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 06 Aug 2024 08:03:42 GMT
ARG RELEASE
# Tue, 06 Aug 2024 08:03:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Aug 2024 08:03:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Aug 2024 08:03:42 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 06 Aug 2024 08:03:42 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 06 Aug 2024 08:03:42 GMT
CMD ["/bin/bash"]
# Tue, 06 Aug 2024 08:03:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 06 Aug 2024 08:03:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 08:03:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0ac516cc1eadffb4cd3cfc9736a33d58ea6a396bf85729036c973482f7c063d9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='8fbefff2c578f73d95118d830347589ddc9aa84510200a5a5001901c2dea4810';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='13bdefdeae6f18bc9c87bba18c853b8b12c5442ce07ff0a3956ce28776d695ff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='2991edbedee448c0f1edf131beca84b415dac64ea97365b9bfd85bc2f39893bb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 06 Aug 2024 08:03:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 06 Aug 2024 08:03:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 08:03:42 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
WORKDIR /usr/local/tomcat
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 08:03:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 08:03:42 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_MAJOR=9
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_VERSION=9.0.93
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_SHA512=3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d
# Tue, 06 Aug 2024 08:03:42 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 06 Aug 2024 08:03:42 GMT
ENTRYPOINT []
# Tue, 06 Aug 2024 08:03:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2b9159aba5847bda25160889018a02e4997ea0539f37f28faa599fcc4e6e59`  
		Last Modified: Sat, 17 Aug 2024 00:59:09 GMT  
		Size: 13.7 MB (13715085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62029e3d25fd8b12f872a3e17d8463af1c36ebf0749e75b55a8ac0360e6bc1bb`  
		Last Modified: Sat, 17 Aug 2024 01:00:00 GMT  
		Size: 41.2 MB (41245903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f585b87b2954af7afa137274be8053457c80e767a9f5070368eb0c4e607f685`  
		Last Modified: Sat, 17 Aug 2024 00:59:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09db1f52d201b1d649b64dc07faf1e6b1e84e4ff0ada56322dd8829f119c4842`  
		Last Modified: Fri, 23 Aug 2024 19:21:52 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ef1e854538051a31798dedac3e2fb7570ef13026aef2be8b4976b6668940c7`  
		Last Modified: Sat, 24 Aug 2024 00:07:37 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b2e8fa3bcf7d3709443d7dcd09dc1201270d4cd9f14514006748bad52d5a97`  
		Last Modified: Sat, 24 Aug 2024 00:07:38 GMT  
		Size: 12.8 MB (12831995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9526de59963675d5d273b0839f25dc37f2d337a0b62d69f21a92891de1712d43`  
		Last Modified: Sat, 24 Aug 2024 00:07:38 GMT  
		Size: 249.7 KB (249654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:4541a722b93c20e534b593175a76c5a9250165d7189f83726f22f21dce0a2a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d71cb0118cc2484ad9d5966e4558cbcba8db5f3ade1d369d51fb09f3b5c78b`

```dockerfile
```

-	Layers:
	-	`sha256:eadb33dbfc401b759b3dfd5d87ae8bc6ba08172f1048ab135b9b4e116dab01d6`  
		Last Modified: Sat, 24 Aug 2024 00:07:38 GMT  
		Size: 3.6 MB (3553763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f180b4fb588df5d557cff933c0c3783abb9de88ae45187919caa97d15652a7f`  
		Last Modified: Sat, 24 Aug 2024 00:07:37 GMT  
		Size: 21.9 KB (21925 bytes)  
		MIME: application/vnd.in-toto+json
