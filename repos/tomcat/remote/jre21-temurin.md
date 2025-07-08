## `tomcat:jre21-temurin`

```console
$ docker pull tomcat@sha256:0392f71bd7a2cbc666504dcd96b40ecc4b453a462bef988b28a62333c19d99c0
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

### `tomcat:jre21-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:6007dd3682addeec62bf5934a721b3187fad8ac0ae368a7b404df413b06a541c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115359071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d8cc2d303890d16455fdd427b2d24c1d31d56cdec33e05db8d09c0942f5a6d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='8fd14594d0ad8576ba9b698fd10df4a297c548cfdc81cfbe52ac660aeaf5e2b2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 04 Jul 2025 20:15:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 20:15:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_MAJOR=11
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_VERSION=11.0.9
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_SHA512=480ae04b5fa77e4f3f02d8e32b0ac5701390e9e0d3b2e57827defde8c364a5a4b3f37d25bc46a2538a4268babc7b61999a22314cb046360b2eb3f8109973a034
# Fri, 04 Jul 2025 20:15:48 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Jul 2025 20:15:48 GMT
ENTRYPOINT []
# Fri, 04 Jul 2025 20:15:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c435c063d543b912f39fc6e178600f6b62187fd7a34ab8dc5b5fcb1206dd2dd`  
		Last Modified: Wed, 02 Jul 2025 03:10:36 GMT  
		Size: 17.0 MB (16969494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6798510c0a2db2aee23c3cd77ae21513d0e29201f5a7b1fccea8c428beaf4905`  
		Last Modified: Wed, 02 Jul 2025 03:10:38 GMT  
		Size: 52.9 MB (52891084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5cadd8df76d038e3f113d905144cd7efa62929be4d443f95b87cc6f107a91e`  
		Last Modified: Wed, 02 Jul 2025 03:10:34 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491b99df4756a56b22d3dc6b877cdd97b034981ce870e7f2313ccc3f63cc5ebe`  
		Last Modified: Wed, 02 Jul 2025 03:10:34 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935fa16770267474ff186d9d2ef5a167b6add67de653a20db5be23a4464ed5e6`  
		Last Modified: Mon, 07 Jul 2025 21:05:04 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5502b0c06c68dfdfb727f87daa3eee177eef6e7b0a4d36c12d79728dfb7d8a50`  
		Last Modified: Mon, 07 Jul 2025 21:05:05 GMT  
		Size: 14.1 MB (14067118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d940319a58f4b2524d5d888cdf70249b22ea130f10a8b5a582609629bd8b8cb2`  
		Last Modified: Mon, 07 Jul 2025 21:05:05 GMT  
		Size: 1.7 MB (1710367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:559c98eaabc7b8bec654e9ca55133fbe5c7a3ee81feb97ec110a559b72afa3a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3376084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a8758bac904925334efe6d184b84c98516f9806ed68a800834dd57d4a3ac8b`

```dockerfile
```

-	Layers:
	-	`sha256:1d13d2ce7c5225239fc065c0694c288e73696ea80e600e2cd7b52a37adebb16a`  
		Last Modified: Mon, 07 Jul 2025 23:32:36 GMT  
		Size: 3.4 MB (3352010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:feb4cc5695deb9cd34d5426530343aed408053f07a1331b7b1f71c6247e607e1`  
		Last Modified: Mon, 07 Jul 2025 23:32:36 GMT  
		Size: 24.1 KB (24074 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:9e4cd700d0136836cefbfb8a8669c9cc1089ea77a489d40b9a31f0233cf81d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113779383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554f769d91c11c91965dbbc0ce370817fb8d7167391118a42bc14264f84646b7`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='8fd14594d0ad8576ba9b698fd10df4a297c548cfdc81cfbe52ac660aeaf5e2b2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 04 Jul 2025 20:15:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 20:15:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_MAJOR=11
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_VERSION=11.0.9
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_SHA512=480ae04b5fa77e4f3f02d8e32b0ac5701390e9e0d3b2e57827defde8c364a5a4b3f37d25bc46a2538a4268babc7b61999a22314cb046360b2eb3f8109973a034
# Fri, 04 Jul 2025 20:15:48 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Jul 2025 20:15:48 GMT
ENTRYPOINT []
# Fri, 04 Jul 2025 20:15:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2fa422bbd08bc40d85a4e1666805f0d0f323a1834f9494578f07cf2106f303`  
		Last Modified: Wed, 02 Jul 2025 05:07:14 GMT  
		Size: 17.0 MB (16988217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5debe69a504b4c2ab882ec6fcf7d2d47a2d074939b121a43f2d1594752b52463`  
		Last Modified: Wed, 02 Jul 2025 05:14:27 GMT  
		Size: 52.1 MB (52070804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffeee2216863cde6c6647a5098b5e4d04aad2a026305d5359e92a4b1bf9e46e`  
		Last Modified: Wed, 02 Jul 2025 05:14:24 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c8c5490283483e487a7dadfce6ab28484599ac9809b53dedc827f0f3f0e9ed`  
		Last Modified: Wed, 02 Jul 2025 05:14:24 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e010e8775cc784ff60e30bbab722ebf0ae7c4d744ece09db549c8cdc748af0`  
		Last Modified: Wed, 02 Jul 2025 14:33:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94b1c5afae121a1e4bd5fa49fca34395c011a3254c7baa5ed22181703d14a20`  
		Last Modified: Tue, 08 Jul 2025 05:21:06 GMT  
		Size: 14.1 MB (14071862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf64179c4b77e697049571fa130ed8f072dc3c7d097e734fd6e5907d5c705fc`  
		Last Modified: Tue, 08 Jul 2025 05:21:03 GMT  
		Size: 1.8 MB (1789838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:dab06da42dcf1187c05082e397512aa265336bdfec27dc4e9088b0d8735385af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3376908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3f7dca80efaaf305a5731e4439b1069b0e5919ca715db25cc45b11ce7b09b1`

```dockerfile
```

-	Layers:
	-	`sha256:5238b09b868d14a5a31f710ab8d1315d13ef35318bb2b0e384e107efe064b5c3`  
		Last Modified: Tue, 08 Jul 2025 08:31:21 GMT  
		Size: 3.4 MB (3352578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dac906e24ee7f0ff361c8b54a41db030e1b96e25e97bb621edff6f4c7660a651`  
		Last Modified: Tue, 08 Jul 2025 08:31:22 GMT  
		Size: 24.3 KB (24330 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:4577224eeb3a7a979c6d14b6f0b411a0ddc71dc509392fdcb76993f8a8db53ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122193004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f29661e00d96fb7763ac08fbb8e8ffac3a9e341c65698b67d7b3c486af3635d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:fca9cbe6eff6a6982a26900c08b4e2c5a46057e9e5386288e826ac4f2cb17b32 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='8fd14594d0ad8576ba9b698fd10df4a297c548cfdc81cfbe52ac660aeaf5e2b2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 04 Jul 2025 20:15:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 20:15:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_MAJOR=11
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_VERSION=11.0.9
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_SHA512=480ae04b5fa77e4f3f02d8e32b0ac5701390e9e0d3b2e57827defde8c364a5a4b3f37d25bc46a2538a4268babc7b61999a22314cb046360b2eb3f8109973a034
# Fri, 04 Jul 2025 20:15:48 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Jul 2025 20:15:48 GMT
ENTRYPOINT []
# Fri, 04 Jul 2025 20:15:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:384c99c6e2b4660fd65fc9823f13a263fb87d4aec3b8f2bd813a7a255bcf46f3`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 34.3 MB (34321506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0111803c0bfac8b5cf9f7f497b1d1327406384bede031585f6063cf0af7d1a63`  
		Last Modified: Wed, 02 Jul 2025 03:16:25 GMT  
		Size: 18.8 MB (18817031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5680bcd2bb65b0c231f2e7fdd32d653d5d32101362b3bb719c48cbd6f4d5d2fa`  
		Last Modified: Wed, 02 Jul 2025 03:28:23 GMT  
		Size: 52.9 MB (52915463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204d3cb531f827da9a35bae98e0b79f1ce05826133296f1b89604ae398b9203a`  
		Last Modified: Wed, 02 Jul 2025 03:28:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d02f908d404211c977b8c59ae1a7f64295e9850c5a268c113db4e2ae96f0c3`  
		Last Modified: Wed, 02 Jul 2025 03:28:20 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63f7d087f5d5f0ee4912dfd23e75ec3c1922c55cc387203dbb5c476ee979aa9`  
		Last Modified: Wed, 02 Jul 2025 14:52:26 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d717f78d43b42de0ffacbb5eb2389eb3eb01e5471740ce9a55baf4f9c642203`  
		Last Modified: Tue, 08 Jul 2025 00:13:24 GMT  
		Size: 14.1 MB (14087213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fc0d6898d13b9bc7a1df4a39496a5c0fd72a6c8cd89600ea32420e0e4974e2`  
		Last Modified: Tue, 08 Jul 2025 00:13:22 GMT  
		Size: 2.0 MB (2049146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:e3cf7e937e01a0df232dd90cd78cc7c8c6253fb9b5f183d9c4aa42301194dd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3380315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d73d1a3fb8890469a1a2398bb29c3a2d33ee034504da3a0a4770fb382f9948c`

```dockerfile
```

-	Layers:
	-	`sha256:a25bbc55285efcc8acea95cca9b12dd845ecb4d48bf7cbe84e9a10a613f861eb`  
		Last Modified: Tue, 08 Jul 2025 02:30:45 GMT  
		Size: 3.4 MB (3356135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73f94dcd3afcb63c670420f1a473c23ab618d3faf26fd82855aa227c2f14a490`  
		Last Modified: Tue, 08 Jul 2025 02:30:46 GMT  
		Size: 24.2 KB (24180 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin` - linux; riscv64

```console
$ docker pull tomcat@sha256:00adfb2186f760d9c2cf2cf1ddd16c017634f6cd7bad4c7cf7774ce32a09c526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117198519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d8456df1fa6c3eec6406e14c0597d2588ce63cfba4a51891f66afad731f56b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:202c5a7a84e813495c089800398f2ba18952221717db2c10e042ce4179ee6fc0 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='8fd14594d0ad8576ba9b698fd10df4a297c548cfdc81cfbe52ac660aeaf5e2b2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 04 Jul 2025 20:15:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 20:15:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_MAJOR=11
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_VERSION=11.0.9
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_SHA512=480ae04b5fa77e4f3f02d8e32b0ac5701390e9e0d3b2e57827defde8c364a5a4b3f37d25bc46a2538a4268babc7b61999a22314cb046360b2eb3f8109973a034
# Fri, 04 Jul 2025 20:15:48 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Jul 2025 20:15:48 GMT
ENTRYPOINT []
# Fri, 04 Jul 2025 20:15:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4ccdff8fdb11e14b8e0dab6804aeebce5855635c68b20f199dcf0efcd9b4c462`  
		Last Modified: Wed, 02 Jul 2025 01:17:14 GMT  
		Size: 31.0 MB (30951024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b112a889acb1550129c19c10a637af9d1912567df5d0ca30859202a60544b8`  
		Last Modified: Wed, 02 Jul 2025 03:35:12 GMT  
		Size: 17.9 MB (17863019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee7137937695ad37c739116a5cd7e3560ed08609a5886e283f70f8d0fe743a0`  
		Last Modified: Wed, 02 Jul 2025 03:44:24 GMT  
		Size: 50.7 MB (50666437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd59b7e928c6b5ad4e309c4899334b02cea1010db936df6047ed48faa0b1058`  
		Last Modified: Wed, 02 Jul 2025 03:44:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e35431ca226bf709fcb69bae6b46c613e13acf580c4a2bdb82d6a87c828ad`  
		Last Modified: Wed, 02 Jul 2025 03:44:20 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8509b9806c9e735d00659ccf8c86f4aee26940cb47711cf988f4556e9331ec0`  
		Last Modified: Wed, 02 Jul 2025 11:19:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a07b6c6da33b6e9171aff50b303ed553f3cf43bf55eeb25b1bf4854a450c677`  
		Last Modified: Tue, 08 Jul 2025 06:27:37 GMT  
		Size: 14.3 MB (14252941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b5d98fcb36e5e32786e245e84395e5051c6eb99c8a6b7ee683069260ec14f6`  
		Last Modified: Tue, 08 Jul 2025 06:27:37 GMT  
		Size: 3.5 MB (3462454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:7288d8d3794b0c9289adb6f83185c775a7b1ffca33c9916e04b5b97243f21d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3368317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b5e4da23b9aa4713710176afc2119b91f37552adebcdb39ce294ceb54a3a59`

```dockerfile
```

-	Layers:
	-	`sha256:ae02d6d477d50d1051c06e84e743544a8c5d1986e780bc8a0f588b0d55b06582`  
		Last Modified: Tue, 08 Jul 2025 08:31:29 GMT  
		Size: 3.3 MB (3344137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59411a951ded751ea215b7e288882e7fdcbb4c9524da5b46fcf483e11fb744b9`  
		Last Modified: Tue, 08 Jul 2025 08:31:29 GMT  
		Size: 24.2 KB (24180 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:939bcab76e2c85f61d310857aa7cdd1c66daef072aa67fb13c0d845ff571ea53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.8 MB (112784774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2d580c1da42c6d6ddc5adb97bfd43892e55be72294874f30faff2e12e2b468`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:80b0b0c2a08a762cf6a520d8428a5c769c29e72f4a51630adb2231f2816c50c4 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='8fd14594d0ad8576ba9b698fd10df4a297c548cfdc81cfbe52ac660aeaf5e2b2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 04 Jul 2025 20:15:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 20:15:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_MAJOR=11
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_VERSION=11.0.9
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_SHA512=480ae04b5fa77e4f3f02d8e32b0ac5701390e9e0d3b2e57827defde8c364a5a4b3f37d25bc46a2538a4268babc7b61999a22314cb046360b2eb3f8109973a034
# Fri, 04 Jul 2025 20:15:48 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Jul 2025 20:15:48 GMT
ENTRYPOINT []
# Fri, 04 Jul 2025 20:15:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:30d64ca13d9d94eb48bf3fece3e38a4e60931d72f1a8c633dec981e43a0515a4`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 29.9 MB (29925630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376d0f4302e30b01c4235de8a3d72897ca97f7a056bf7655f826977caaf40fa8`  
		Last Modified: Wed, 02 Jul 2025 04:17:12 GMT  
		Size: 17.6 MB (17582256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bdd19c86f8ce4ef8e00ace34b8f6c26d2f3f1021e0f334e37e11abfe60b5197`  
		Last Modified: Wed, 02 Jul 2025 04:23:21 GMT  
		Size: 49.5 MB (49471708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2927dc352bff771f750ba92249605855d59e0ceb892fb5fa860b65fa5769dfa`  
		Last Modified: Wed, 02 Jul 2025 04:23:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe852a730495e7de88704cb99d88c3511ca83b95f748f55933b0e482ebf60c20`  
		Last Modified: Wed, 02 Jul 2025 04:23:16 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615a6c9651b8945696401e4567d9bd6f62105ae977adb669ec2353795fa05f02`  
		Last Modified: Wed, 02 Jul 2025 07:20:14 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47afe886ac0839e8c36f6f3b2e549142b3ab04de69ae23ea075758fa7df6cba`  
		Last Modified: Tue, 08 Jul 2025 05:23:05 GMT  
		Size: 14.1 MB (14078375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35908626cca2cdc1818ee9f93d5f1f7c14749a11ce2e902d901c73f019b27edf`  
		Last Modified: Tue, 08 Jul 2025 05:23:05 GMT  
		Size: 1.7 MB (1724161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:9bb7b9a13872a3069397b42c7e9c34b370b575f72683b4cd7238ce5dea164044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3378283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0ce125f0c40d71dd60f040cec59c5b25771211c887ec96e961e3c181144d9a`

```dockerfile
```

-	Layers:
	-	`sha256:9e4c3b21396596dc0aacbd2af4f9b41b6f87cae0b68a70e5ea29ff19eceb16a8`  
		Last Modified: Tue, 08 Jul 2025 08:31:33 GMT  
		Size: 3.4 MB (3354209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0555d2f34ae9e9996ac3b0612623f704820a749f39e415f53db4cb19f7390568`  
		Last Modified: Tue, 08 Jul 2025 08:31:34 GMT  
		Size: 24.1 KB (24074 bytes)  
		MIME: application/vnd.in-toto+json
