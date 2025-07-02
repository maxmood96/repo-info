## `tomcat:10-jre21-temurin-noble`

```console
$ docker pull tomcat@sha256:521454f9d1a1dde914421cffd7916f9b53119b4ddc1371fdf652e1dce6fa65b1
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

### `tomcat:10-jre21-temurin-noble` - linux; amd64

```console
$ docker pull tomcat@sha256:b48ef858eef0cd6ba9fc9b2774c9a39f2faf6af99f92f4f72564ed3f75f7f79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113863868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02636d357e6fc05c10ce8bbd7f825fb8b7fd9ecbd0831ca985e37c71e22e080`
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
# Tue, 10 Jun 2025 02:03:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 10 Jun 2025 02:03:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Jun 2025 02:03:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 10 Jun 2025 02:03:19 GMT
WORKDIR /usr/local/tomcat
# Tue, 10 Jun 2025 02:03:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 02:03:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 02:03:19 GMT
ENV TOMCAT_MAJOR=10
# Tue, 10 Jun 2025 02:03:19 GMT
ENV TOMCAT_VERSION=10.1.42
# Tue, 10 Jun 2025 02:03:19 GMT
ENV TOMCAT_SHA512=eb09be6df829ebc1fb8851282888966101e878b2c4a507623f3acabc2a1337b89271b4ad7b9361f0bf4bcfe7b5cfec93617bd716043c68afef029c080fff6546
# Tue, 10 Jun 2025 02:03:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 10 Jun 2025 02:03:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 02:03:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 10 Jun 2025 02:03:19 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Jun 2025 02:03:19 GMT
ENTRYPOINT []
# Tue, 10 Jun 2025 02:03:19 GMT
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
	-	`sha256:4c7cc78b341e3242368862e3cf840fec29e4095c330e6ccc030dc7fee731bec3`  
		Last Modified: Wed, 02 Jul 2025 05:12:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0286f22b54c71c50323cc91bd719bb48febc3be2113164c0328c06682f2a15`  
		Last Modified: Wed, 02 Jul 2025 05:12:18 GMT  
		Size: 14.1 MB (14057660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ba97934deae5da1bda125fa0eb15366a587e46ea18011e2f9853c30eec0375`  
		Last Modified: Wed, 02 Jul 2025 05:12:16 GMT  
		Size: 224.6 KB (224622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre21-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:065b4bb857b32d1340bb26df57ca41e115cbd79a83f178c69e33d1f56ad30d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3374297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6b5c36ee8a2b5078fbd963d84388feb0ea8bd0d0f1e6325628e9e360012a38`

```dockerfile
```

-	Layers:
	-	`sha256:5a8753d64aecadf4d7be2e3a18c95a29b9031a7e5310a6fbf155f86d5a416f25`  
		Last Modified: Wed, 02 Jul 2025 08:30:34 GMT  
		Size: 3.4 MB (3351148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4da9b64a239de17f36113fc6b159c9111aa64981a2a2900809ebbe876eeb8b64`  
		Last Modified: Wed, 02 Jul 2025 08:30:35 GMT  
		Size: 23.1 KB (23149 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre21-temurin-noble` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:e2eff37f651f80ea40c779a62592d8082feee4b916c829df823b3f987ef2ffca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112200980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8633c72e500e45bd8d3d99287e0de06d72669ad159fb9938d3bd213f2eb776d4`
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
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
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
# Tue, 10 Jun 2025 02:03:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 10 Jun 2025 02:03:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Jun 2025 02:03:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 10 Jun 2025 02:03:19 GMT
WORKDIR /usr/local/tomcat
# Tue, 10 Jun 2025 02:03:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 02:03:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 02:03:19 GMT
ENV TOMCAT_MAJOR=10
# Tue, 10 Jun 2025 02:03:19 GMT
ENV TOMCAT_VERSION=10.1.42
# Tue, 10 Jun 2025 02:03:19 GMT
ENV TOMCAT_SHA512=eb09be6df829ebc1fb8851282888966101e878b2c4a507623f3acabc2a1337b89271b4ad7b9361f0bf4bcfe7b5cfec93617bd716043c68afef029c080fff6546
# Tue, 10 Jun 2025 02:03:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 10 Jun 2025 02:03:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 02:03:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 10 Jun 2025 02:03:19 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Jun 2025 02:03:19 GMT
ENTRYPOINT []
# Tue, 10 Jun 2025 02:03:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb5cdde15082c2c264c46bd2f1aa0a8ad43d7590dd7374853ce1748ae4259a4`  
		Last Modified: Tue, 03 Jun 2025 13:30:28 GMT  
		Size: 17.0 MB (16988306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5911347bfc36c43690c78dbee1e4214c6e79e6c2b6bae6572423040611ba80da`  
		Last Modified: Tue, 03 Jun 2025 13:30:30 GMT  
		Size: 52.1 MB (52070812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06763e1dbf3e148227fb25ab13d25e10e5ae8fcef8987f96fed0240d4ddc176b`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720d536b8cff2c9920c7cc9f8410384ff797ae6e3f12ba749e6295cc4c780c62`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd2c3debe0b0a3a6a9052f48e560d43e668d79c600e030367fef057dd4ce52c`  
		Last Modified: Tue, 03 Jun 2025 14:38:44 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9698196856a34cc538189aa52cfc35855758df48e1faa44fddacb4313351d6e8`  
		Last Modified: Tue, 10 Jun 2025 18:45:31 GMT  
		Size: 14.1 MB (14062195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c1a601a3d2daf10b65241b8f4b7780e9ecdf6b243d2e4fefbd5719e626f589`  
		Last Modified: Tue, 10 Jun 2025 18:45:29 GMT  
		Size: 225.1 KB (225124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre21-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:2ac5680310f09f04eb4d1a9aaf75913b511b15b1afdcb4b0f2223afaa836e932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3375049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd4e73582e678bb686371dc9c5ccb1f3d93efbb249d54324f42a091cd49f48a`

```dockerfile
```

-	Layers:
	-	`sha256:43dfbbed76d4b0081c67cd67968bbd25fd1168256461d8494635ac3f2a2ced48`  
		Last Modified: Tue, 10 Jun 2025 20:31:49 GMT  
		Size: 3.4 MB (3351680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef67ca5e8c11749e313a19a4de6e50756b218bc16a0d7560c1dc9c901751bd7a`  
		Last Modified: Tue, 10 Jun 2025 20:31:50 GMT  
		Size: 23.4 KB (23369 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre21-temurin-noble` - linux; ppc64le

```console
$ docker pull tomcat@sha256:ef517850ac2e7596e10835335199e2b3b6879c937a1063ceb5469e0925eca13c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120390764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0181979cf7b0786b812ebbfb03f4b51c9176734e9b3bdae381c22a615110405b`
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
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
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
# Tue, 10 Jun 2025 02:03:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 10 Jun 2025 02:03:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Jun 2025 02:03:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 10 Jun 2025 02:03:19 GMT
WORKDIR /usr/local/tomcat
# Tue, 10 Jun 2025 02:03:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 02:03:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 02:03:19 GMT
ENV TOMCAT_MAJOR=10
# Tue, 10 Jun 2025 02:03:19 GMT
ENV TOMCAT_VERSION=10.1.42
# Tue, 10 Jun 2025 02:03:19 GMT
ENV TOMCAT_SHA512=eb09be6df829ebc1fb8851282888966101e878b2c4a507623f3acabc2a1337b89271b4ad7b9361f0bf4bcfe7b5cfec93617bd716043c68afef029c080fff6546
# Tue, 10 Jun 2025 02:03:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 10 Jun 2025 02:03:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 02:03:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 10 Jun 2025 02:03:19 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Jun 2025 02:03:19 GMT
ENTRYPOINT []
# Tue, 10 Jun 2025 02:03:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Tue, 03 Jun 2025 13:31:13 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2357cdb0b572402f44522ed5512cbdd3414537099dc31df3241d54f1a1546d`  
		Last Modified: Tue, 03 Jun 2025 14:27:57 GMT  
		Size: 18.8 MB (18817014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cbc2a6d6e1c9f6da01815a94e672f8b40ee79c764aacb344f910dafb2a4300`  
		Last Modified: Tue, 03 Jun 2025 14:31:02 GMT  
		Size: 52.9 MB (52915558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4c5b5d378cc606319ce152a4c502ab535d22a49c20acfde553e536359140c0`  
		Last Modified: Tue, 03 Jun 2025 14:30:50 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b81e427a463f5c2a5b3c459b9aabbafbaaca7f0cc6d368a76bcc8cfb5954a9b`  
		Last Modified: Tue, 03 Jun 2025 14:30:50 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26085e116bc17015c230edefbef879ff1356074c0b9fe8ce7e9676ea9802c344`  
		Last Modified: Wed, 04 Jun 2025 04:50:07 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbc41e5d4e59c48e28f61bd7f5fadc94d1b9e94b0afd11d7414172a2f722355`  
		Last Modified: Tue, 10 Jun 2025 18:35:23 GMT  
		Size: 14.1 MB (14073839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c73c8596115e83de20fff4513fef2e4b14514ff0debffc49268e7c3f1d0ef56`  
		Last Modified: Tue, 10 Jun 2025 18:35:21 GMT  
		Size: 256.5 KB (256498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre21-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:fafce243e3ff2c2f71cc5249efc94f9990a2053332dcd42efaf3ace6fee28b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3378492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba6597cc20b92966de9822c4fe2832e6a8e3e641c159aacfcac91d37dfbaf5c`

```dockerfile
```

-	Layers:
	-	`sha256:5774a1f461d2cbc80b7a85e101d5311a6c2ff3bba82d6ef428d99cb3ee5c25e9`  
		Last Modified: Tue, 10 Jun 2025 20:31:55 GMT  
		Size: 3.4 MB (3355255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f64512dfddadadc5a1b1915da4bba6a81cdee7e9699f1762d0c9ccb97d626bb`  
		Last Modified: Tue, 10 Jun 2025 20:31:55 GMT  
		Size: 23.2 KB (23237 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre21-temurin-noble` - linux; riscv64

```console
$ docker pull tomcat@sha256:28e2f0644b70deecaf8736cba8395451ee0412406cdd14a28c6fa2877795da95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (113951092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f63cdcb24b5ac71125ee236ed5805a120d61e3aae1d2ec248f8e406ea157ea`
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
ADD file:f68263cf915d0f5d61ab9caa83da511fc9ef55d936429cb8fb542906fc38a8fa in / 
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
# Tue, 10 Jun 2025 02:03:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 10 Jun 2025 02:03:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Jun 2025 02:03:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 10 Jun 2025 02:03:19 GMT
WORKDIR /usr/local/tomcat
# Tue, 10 Jun 2025 02:03:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 02:03:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 02:03:19 GMT
ENV TOMCAT_MAJOR=10
# Tue, 10 Jun 2025 02:03:19 GMT
ENV TOMCAT_VERSION=10.1.42
# Tue, 10 Jun 2025 02:03:19 GMT
ENV TOMCAT_SHA512=eb09be6df829ebc1fb8851282888966101e878b2c4a507623f3acabc2a1337b89271b4ad7b9361f0bf4bcfe7b5cfec93617bd716043c68afef029c080fff6546
# Tue, 10 Jun 2025 02:03:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 10 Jun 2025 02:03:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 02:03:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 10 Jun 2025 02:03:19 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Jun 2025 02:03:19 GMT
ENTRYPOINT []
# Tue, 10 Jun 2025 02:03:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4ac2db62b9f8401057b5c4ebae4764d70573ec599f6a1f0b5dc2c4491ed8e39a`  
		Last Modified: Tue, 03 Jun 2025 13:37:40 GMT  
		Size: 30.9 MB (30947484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785db385a4c09f3f0d016378c5cdd94ffd969fb8371cf481c628798e8ed47951`  
		Last Modified: Tue, 03 Jun 2025 14:30:04 GMT  
		Size: 17.9 MB (17862845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0cd0f7401282a236c945f62e0b3c640ace9c3df9cea1b28f1fe9827cce3c171`  
		Last Modified: Tue, 03 Jun 2025 14:31:04 GMT  
		Size: 50.7 MB (50666417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb67482c862807538de98190bf6437dd2905d56eca1c43a4c6345b132aeb94c0`  
		Last Modified: Tue, 03 Jun 2025 14:30:51 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da18f3ea76c257ad3ef05715a91d8f06fd283630b7faeb7bcf6acdfa96fde333`  
		Last Modified: Tue, 03 Jun 2025 14:30:51 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a991d6fc6ab6536e9723cee3fc759d78b3c51c54e8fd3383b7e482e59a4cf50`  
		Last Modified: Tue, 03 Jun 2025 13:42:44 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f43dbfc1156218e2eabf6fd5264bc08eb552a859318c3718f644d2440197e6`  
		Last Modified: Tue, 10 Jun 2025 18:17:19 GMT  
		Size: 14.2 MB (14243950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2bc4f1ddf30512f9816e43c794490a6720dea0e7f10e3d24fc732fb2ed2d13`  
		Last Modified: Tue, 10 Jun 2025 18:17:17 GMT  
		Size: 227.8 KB (227755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre21-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:264be44d2952a7ca812bc5bc4c19d1533e5bc2c526de4aeee0cdc10b75eb5fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3366494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e06cfcea9c7506392a607ce606f6e73923b1245f8221e2cb49b37268217f18`

```dockerfile
```

-	Layers:
	-	`sha256:4aa019e38f630339610e13ed04702dce01737f29aa715506bede1fffb9546b24`  
		Last Modified: Tue, 10 Jun 2025 20:32:00 GMT  
		Size: 3.3 MB (3343257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35b7a099d32edb774237b55589d2e5a34f18fcdb63ef467b76d310d9170eeb5a`  
		Last Modified: Tue, 10 Jun 2025 20:32:01 GMT  
		Size: 23.2 KB (23237 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre21-temurin-noble` - linux; s390x

```console
$ docker pull tomcat@sha256:14f3bb5b21ca28611480b25191ec519f9c7e77ce859882388c48ddd5107855db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 MB (111282275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d68916c441ee9f58c65975dc2aac1234b7a903e8e4860ec469987bddf0a96f`
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
# Tue, 10 Jun 2025 02:03:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 10 Jun 2025 02:03:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Jun 2025 02:03:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 10 Jun 2025 02:03:19 GMT
WORKDIR /usr/local/tomcat
# Tue, 10 Jun 2025 02:03:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 02:03:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 02:03:19 GMT
ENV TOMCAT_MAJOR=10
# Tue, 10 Jun 2025 02:03:19 GMT
ENV TOMCAT_VERSION=10.1.42
# Tue, 10 Jun 2025 02:03:19 GMT
ENV TOMCAT_SHA512=eb09be6df829ebc1fb8851282888966101e878b2c4a507623f3acabc2a1337b89271b4ad7b9361f0bf4bcfe7b5cfec93617bd716043c68afef029c080fff6546
# Tue, 10 Jun 2025 02:03:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 10 Jun 2025 02:03:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 02:03:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 10 Jun 2025 02:03:19 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Jun 2025 02:03:19 GMT
ENTRYPOINT []
# Tue, 10 Jun 2025 02:03:19 GMT
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
	-	`sha256:ae7e94991bc91c1cce87d74077c4083319b695cc6e3256dff50336b52f0baaa0`  
		Last Modified: Wed, 02 Jul 2025 07:22:10 GMT  
		Size: 14.1 MB (14067488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713afe9f0d59428e79625e3c11244a1c21b338c481fe0dc7ca22c18760eb0eeb`  
		Last Modified: Wed, 02 Jul 2025 07:22:09 GMT  
		Size: 232.5 KB (232549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre21-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:df35531ac66b2f82bd23f6e1b073f026a9c3f73f0c2e1a55e19ce499afe6def6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3376495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57eda2b0878b72000cb7b5bc8011c5414489d07ff0c4607811983dd0bbdcd700`

```dockerfile
```

-	Layers:
	-	`sha256:bfc2b147066f3ed78708da247f76f546a6c6b4a8838ab1e0c10d5696a792f975`  
		Last Modified: Wed, 02 Jul 2025 08:30:55 GMT  
		Size: 3.4 MB (3353347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd0f1a1eb55f99b9a069176f336ffe7f28d06cb98fb13c6115b44697762d0fff`  
		Last Modified: Wed, 02 Jul 2025 08:30:56 GMT  
		Size: 23.1 KB (23148 bytes)  
		MIME: application/vnd.in-toto+json
