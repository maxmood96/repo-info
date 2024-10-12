## `tomcat:10-jre11-temurin`

```console
$ docker pull tomcat@sha256:a898919b9c9a0d700365b3ffbcf7dc393c46bf30fc06a82fb677f3f3ffe5d96d
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

### `tomcat:10-jre11-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:c103520e9553142205817f890e279973cba94cf608cef0ac65b144d5974589c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105355943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b75c29818cc200a8271545fd9d6df4ed56f6ccee7904f0ff6d98b154b12b451`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 09 Oct 2024 17:25:06 GMT
ARG RELEASE
# Wed, 09 Oct 2024 17:25:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 17:25:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 17:25:06 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 09 Oct 2024 17:25:06 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Wed, 09 Oct 2024 17:25:06 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Oct 2024 17:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:25:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_MAJOR=10
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_VERSION=10.1.31
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_SHA512=0e3d423a843e2d9ba4f28a9f0a2f1073d5a1389557dfda041759f8df968bace63cd6948bd76df2727b5133ddb7c33e05dab43cea1d519ca0b6d519461152cce9
# Wed, 09 Oct 2024 17:25:06 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Oct 2024 17:25:06 GMT
ENTRYPOINT []
# Wed, 09 Oct 2024 17:25:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beb5331d363596b1827b1acf45f54c2c7746f8406636b8d72b09022b11fb7b3`  
		Last Modified: Fri, 11 Oct 2024 23:56:25 GMT  
		Size: 13.8 MB (13771214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3f7d473d8492c41afafe20c6e5adcdaccbc46ecd729c2a15103e7b18cc820b`  
		Last Modified: Fri, 11 Oct 2024 23:57:22 GMT  
		Size: 47.2 MB (47199045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa4cff389c024487e678fae0b0727a22bb6fa9a2e9c990448012a7eb0530f15`  
		Last Modified: Fri, 11 Oct 2024 23:57:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f8c278d0520357f911c1148d39ca98bb8a255e6c403759c358fae1e7e2ae82`  
		Last Modified: Fri, 11 Oct 2024 23:57:16 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f8e1dc9ad840b7ff5db6a0455823fbc33ee9cd46410852b9a48a1860cc1e3a`  
		Last Modified: Sat, 12 Oct 2024 01:56:28 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b6b53ca43bd6501fe133d54e61cd8718caf6a7ff670e5374677e49e9d74ec8`  
		Last Modified: Sat, 12 Oct 2024 01:56:28 GMT  
		Size: 13.6 MB (13557014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cee13b8eebe62e2ad6674cd9dbf988951f7e1fcb8102e416b32cb16833e2394`  
		Last Modified: Sat, 12 Oct 2024 01:56:28 GMT  
		Size: 212.9 KB (212923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:9f151f648613a63515bf864d4b2862e38f18f4415b040f7e17db13d44f720da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3087756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6efdca639a17acb00376769552a254aeaadc44248956d4e9506731927a014364`

```dockerfile
```

-	Layers:
	-	`sha256:19730487afe89a54e13107a4a30e59778aeed4493fc6866ff95e84645f73c35c`  
		Last Modified: Sat, 12 Oct 2024 01:56:28 GMT  
		Size: 3.1 MB (3064150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af5be459e6791e644ce6a9b515e25c496c2aace37fe417e2aec35d2ec15c2cea`  
		Last Modified: Sat, 12 Oct 2024 01:56:28 GMT  
		Size: 23.6 KB (23606 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:e76c6ecbf6008c6027b1251bceb7a46827cde0dac996256990c97e96da2a62b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99908556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5d83e2d2ff721c5cd51a311c5a47f1eb3caabb4134391b4ee143672cc56a72`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 09 Oct 2024 17:25:06 GMT
ARG RELEASE
# Wed, 09 Oct 2024 17:25:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 17:25:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 17:25:06 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 09 Oct 2024 17:25:06 GMT
ADD file:a30667697f58d730cc31ae308b1ba41bf25987733d14114fca71a90447988801 in / 
# Wed, 09 Oct 2024 17:25:06 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Oct 2024 17:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:25:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_MAJOR=10
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_VERSION=10.1.31
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_SHA512=0e3d423a843e2d9ba4f28a9f0a2f1073d5a1389557dfda041759f8df968bace63cd6948bd76df2727b5133ddb7c33e05dab43cea1d519ca0b6d519461152cce9
# Wed, 09 Oct 2024 17:25:06 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Oct 2024 17:25:06 GMT
ENTRYPOINT []
# Wed, 09 Oct 2024 17:25:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ebc4eee72d0a91a5a59ea1b60758bd4ff0e56e71e15430000cf9a33bd0b45ca2`  
		Last Modified: Sat, 12 Oct 2024 00:33:04 GMT  
		Size: 27.7 MB (27734482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3d31f15da95226160d2c4d971d0721ec4463223129e41bcf869d34fcb64e5a`  
		Last Modified: Sat, 12 Oct 2024 00:33:02 GMT  
		Size: 13.1 MB (13135136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4f43687d51fee953ef8d45b8cd53e6d9eb6ebce2aa57c98579ca232eb9d185`  
		Last Modified: Sat, 12 Oct 2024 00:34:01 GMT  
		Size: 45.3 MB (45320943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71074f5d0711028fdecc7ff7111d96ee01cb2947f86516893285d2c649256d72`  
		Last Modified: Sat, 12 Oct 2024 00:33:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1044ec4cb8cf787b28bc4e5e76b16f2860ebe65b14eee3addadb27b3148150`  
		Last Modified: Sat, 12 Oct 2024 00:33:54 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b027ddeeaedfcf70bd27e08eb8ee49cd27977400d7bdb5851eb8fe69b3d1b7f`  
		Last Modified: Sat, 12 Oct 2024 02:12:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84419cb543e7a5c69ded30b5fc1f0220a58bfd478a47a535ac7470b9ea49831`  
		Last Modified: Sat, 12 Oct 2024 02:12:45 GMT  
		Size: 13.5 MB (13531680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696181f872082d3313b05e2962bfad656ea916c69148f2fde19d5c90feed37fb`  
		Last Modified: Sat, 12 Oct 2024 02:12:45 GMT  
		Size: 183.8 KB (183847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:c50258832f105fbe92c9de1ba23f1945168f964a35dfcf10e076f2e89e12f38c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3091648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77094b1da51630b52f4b62275b91eb868c6b4a745327350430b54a020de941d9`

```dockerfile
```

-	Layers:
	-	`sha256:42352d22c8206801e29a9eb2d16cc7550df43fbdc222a66a6e81c8712a3d15b5`  
		Last Modified: Sat, 12 Oct 2024 02:12:44 GMT  
		Size: 3.1 MB (3067782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daab481dd7e921e991f8f6242c116eab4032014f3e295b4e0e1b9c83caa0ba9a`  
		Last Modified: Sat, 12 Oct 2024 02:12:43 GMT  
		Size: 23.9 KB (23866 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:3181aa25ef3d3c9e17e38f5155e4926b2e5c3c33a718ac080dfc19212d2e12a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103084065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33fa948194a940bb68dba1859777ae3abdb156b7c31df6a70227389bc27fd536`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 09 Oct 2024 17:25:06 GMT
ARG RELEASE
# Wed, 09 Oct 2024 17:25:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 17:25:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 17:25:06 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 09 Oct 2024 17:25:06 GMT
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
# Wed, 09 Oct 2024 17:25:06 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Oct 2024 17:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:25:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_MAJOR=10
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_VERSION=10.1.31
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_SHA512=0e3d423a843e2d9ba4f28a9f0a2f1073d5a1389557dfda041759f8df968bace63cd6948bd76df2727b5133ddb7c33e05dab43cea1d519ca0b6d519461152cce9
# Wed, 09 Oct 2024 17:25:06 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Oct 2024 17:25:06 GMT
ENTRYPOINT []
# Wed, 09 Oct 2024 17:25:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:bbc050e99a562418305b0d9003042b38fc24f8c8c94687cf4c69ed6cd001161e`  
		Last Modified: Sat, 12 Oct 2024 00:07:49 GMT  
		Size: 30.0 MB (29953586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056e93bad04245da5d01c9d3de3081a8ad7d5bcd80abdd0ada262fae4f313b5c`  
		Last Modified: Sat, 12 Oct 2024 00:13:29 GMT  
		Size: 13.8 MB (13798544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3860a0e0eb09022a77ced58131844a4f2d46e7c01d7c0f7a7ba1fa0fc3d132b5`  
		Last Modified: Sat, 12 Oct 2024 00:14:20 GMT  
		Size: 45.6 MB (45557180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cf82f1bcce38d91a99de4dadfddc1084f20272d9b6db8b6a2f0fc4d7bb3dbb`  
		Last Modified: Sat, 12 Oct 2024 00:14:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fca13db07011dae250054b123b8203f6f22425760cdc3c04e02888b4e064f30`  
		Last Modified: Sat, 12 Oct 2024 00:14:15 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e53e5592b58f1913c62aab730aef47c4fd60c3d9bcda24043f5abcb4daafee3`  
		Last Modified: Sat, 12 Oct 2024 07:32:54 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a110776b2debca4861704c28068513b3139c9aa0cf052f6f34190032e0634b5`  
		Last Modified: Sat, 12 Oct 2024 07:32:55 GMT  
		Size: 13.6 MB (13559533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83dbfd07b9c50a9dde62f2d0b8d332cf5049bf6f3173d34aa7bb4d67cf994d8c`  
		Last Modified: Sat, 12 Oct 2024 07:32:54 GMT  
		Size: 212.8 KB (212756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:36e185d00bfe927471defde4531cba9b17775e15d0ec4eee84c4a38b68160fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3089217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c53f6c3781d8dabc049ea682696bbd3027b1ba4abf510354d69dde3d45e69b6`

```dockerfile
```

-	Layers:
	-	`sha256:3f168b5bac1c288984d63efbf83d63a3a531e20e4f52bfacc879bed46d634d47`  
		Last Modified: Sat, 12 Oct 2024 07:32:54 GMT  
		Size: 3.1 MB (3065296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1931082e56d58220c46a8fd7f25739a8765bffdd5a70d4511d521788ea4f2bbf`  
		Last Modified: Sat, 12 Oct 2024 07:32:54 GMT  
		Size: 23.9 KB (23921 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:5d289c7b214a29541c2d1452f40fd234044d96bb7d7fdce3477aa5232c36950d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106896292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196a8af1bd198bd9c80b92c50b1b9ee5971474e829924f059a6b44e291fddb0b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 09 Oct 2024 17:25:06 GMT
ARG RELEASE
# Wed, 09 Oct 2024 17:25:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 17:25:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 17:25:06 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 09 Oct 2024 17:25:06 GMT
ADD file:6ec0ebf9a019b7c00b0121b97e89fcad881460415f8dcb9bb94b1cc7f5d0a5bc in / 
# Wed, 09 Oct 2024 17:25:06 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Oct 2024 17:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:25:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_MAJOR=10
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_VERSION=10.1.31
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_SHA512=0e3d423a843e2d9ba4f28a9f0a2f1073d5a1389557dfda041759f8df968bace63cd6948bd76df2727b5133ddb7c33e05dab43cea1d519ca0b6d519461152cce9
# Wed, 09 Oct 2024 17:25:06 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Oct 2024 17:25:06 GMT
ENTRYPOINT []
# Wed, 09 Oct 2024 17:25:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:870d99e54f9cdff4b5ba4448d967491786519e8cbf54f10bd271e5dd32285ceb`  
		Last Modified: Fri, 11 Oct 2024 23:47:07 GMT  
		Size: 35.5 MB (35513269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15086c23dcc309fa9386aa3f0907d6689b8bc489e8f1311ca8248bffcaf162db`  
		Last Modified: Fri, 11 Oct 2024 23:55:29 GMT  
		Size: 14.9 MB (14914320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2373cf9b2627fb4edb71d9e405f6d160fa93be539f961b28b7fa5fe0688d1b65`  
		Last Modified: Fri, 11 Oct 2024 23:56:29 GMT  
		Size: 42.7 MB (42652104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d047bc9221ecdb10b22fc99b492c6170f4dc8ec2f56c118086ba0a9c7dd3d6db`  
		Last Modified: Fri, 11 Oct 2024 23:56:22 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a5df3c39fe820131c64cd3c3f6f5d9bb3d2413b2bcff6e10753285e00beb16`  
		Last Modified: Fri, 11 Oct 2024 23:56:22 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71695d936cd6474be8eac9f3c8247b0773de234d184a93f8c3f836cbfb3ae28c`  
		Last Modified: Sat, 12 Oct 2024 05:09:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5a842664e4b74daeb0d53ae241cc2f2163681a2608cc3821b61b9e654d3b7b`  
		Last Modified: Sat, 12 Oct 2024 05:09:01 GMT  
		Size: 13.6 MB (13570251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63db2c7d8e4bb474c099fef00a0f6276c86a0be3a0414385370d16a6969306bf`  
		Last Modified: Sat, 12 Oct 2024 05:09:01 GMT  
		Size: 243.9 KB (243877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:b63c243093b3383aee9f16f7d317c6b90d4aecd7a5928db912d162fe39db8847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3091881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b49a998477ed5aae8184cff131246a2ed2bcb7e8f720c59d87fa4b273557fc6`

```dockerfile
```

-	Layers:
	-	`sha256:5fa6bc2af565405556ecbe0fdd72c775651637aab2f001874a17d83562077645`  
		Last Modified: Sat, 12 Oct 2024 05:09:00 GMT  
		Size: 3.1 MB (3068091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a40e5ffa9197617850df21f59db56386af6feaf9f69a4d6b88161c496fa8551a`  
		Last Modified: Sat, 12 Oct 2024 05:09:00 GMT  
		Size: 23.8 KB (23790 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre11-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:61c1d47947574287c5498d6c36aafcf64f94c938ac7b108b122e002b0e7f2256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.5 MB (99466244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81df9755704dafe753b730e339eda1c2dd2e8ff26a28794455ec7cc5cfe07941`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 09 Oct 2024 17:25:06 GMT
ARG RELEASE
# Wed, 09 Oct 2024 17:25:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 17:25:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 17:25:06 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 09 Oct 2024 17:25:06 GMT
ADD file:ed84c120e781b2f48856752e1e38d21db0bed5e09a2a64f961f004a4906abcb6 in / 
# Wed, 09 Oct 2024 17:25:06 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Oct 2024 17:25:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Oct 2024 17:25:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Oct 2024 17:25:06 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_MAJOR=10
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_VERSION=10.1.31
# Wed, 09 Oct 2024 17:25:06 GMT
ENV TOMCAT_SHA512=0e3d423a843e2d9ba4f28a9f0a2f1073d5a1389557dfda041759f8df968bace63cd6948bd76df2727b5133ddb7c33e05dab43cea1d519ca0b6d519461152cce9
# Wed, 09 Oct 2024 17:25:06 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Oct 2024 17:25:06 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Oct 2024 17:25:06 GMT
ENTRYPOINT []
# Wed, 09 Oct 2024 17:25:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:220da50193dc0598aa4f0418f3c1f89ed396983e85b2032ceeac1e4e044e443a`  
		Last Modified: Sat, 12 Oct 2024 00:18:34 GMT  
		Size: 30.7 MB (30663130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828f4b3060da0149631cc385d58c57350144169b82f0600be0bfca3031687fa1`  
		Last Modified: Sat, 12 Oct 2024 00:25:46 GMT  
		Size: 14.2 MB (14195098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486869d9c1abdd6b1c24f35034f0dd8739f977eae223bf9f465aaeddbed0dd75`  
		Last Modified: Sat, 12 Oct 2024 00:26:07 GMT  
		Size: 40.8 MB (40817330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b5b18f76f974e74439280589c12c19f270f47596f75451ecd6d61f6ad910f4`  
		Last Modified: Sat, 12 Oct 2024 00:26:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e8260d2638105631b8f199221c4d4700c8a7a07c7390528536e08228caadb`  
		Last Modified: Sat, 12 Oct 2024 00:26:01 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948370548c1add29eede31471976d0a678020c565e7b661be330a1c0875aa6bb`  
		Last Modified: Sat, 12 Oct 2024 02:08:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7485a8879eb2572a695b87eead6110076e1b35eac63680fda0c8ec2b08178f`  
		Last Modified: Sat, 12 Oct 2024 02:08:52 GMT  
		Size: 13.6 MB (13567762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69815bf9e8df1fc4c45edce732895003b90d4449acf628ea2c873629bccbed0`  
		Last Modified: Sat, 12 Oct 2024 02:08:52 GMT  
		Size: 220.5 KB (220454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre11-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:39e78243e8d17fa44f193b9296d1056cd45fa1e8d6feddbd50d02a28516e3577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3090071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c46b152aebe53f64dfd1bffe8ed04448a9eaef7b1b62c24dae34b404ef63ae8`

```dockerfile
```

-	Layers:
	-	`sha256:24cd8e3e3a620f5fb22e696d6cd389de126937e60fdc08983363da0e3aa2fb81`  
		Last Modified: Sat, 12 Oct 2024 02:08:51 GMT  
		Size: 3.1 MB (3066363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f55bcab270c5800e0b6d5cb3b842589ccb3789ebc569df54c33514f153df144`  
		Last Modified: Sat, 12 Oct 2024 02:08:51 GMT  
		Size: 23.7 KB (23708 bytes)  
		MIME: application/vnd.in-toto+json
