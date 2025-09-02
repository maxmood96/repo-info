## `tomcat:jre17`

```console
$ docker pull tomcat@sha256:35579b9d88c1c8e433fdadcce3d29ac5beabb101336b1e611b1ad5681bb6d8eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `tomcat:jre17` - linux; amd64

```console
$ docker pull tomcat@sha256:bacfb0e457d3665cf88992e45b13bfbd3315f8c66a295347d8ea26564fca74e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (107999932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e81b70c78c8d534c5aa124bedfbe9ec0c3e9d09a6a7d015b54b126671fe07c4`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        riscv64)          ESUM='f79ef9103ca89faae1d46794cd719b3a8d73079f63df977c92307b7ff9c3d726';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Aug 2025 20:03:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Aug 2025 20:03:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Aug 2025 20:03:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:03:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_MAJOR=11
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_VERSION=11.0.10
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_SHA512=404143be042016fcc8e2d9d960dafe39608899ad24c5f181bdade919100ba1d3206d55a79f20c8dc0c32905b1729f80354da94f7916af86c98ebe4b21cc9b4c2
# Wed, 06 Aug 2025 20:03:27 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 Aug 2025 20:03:27 GMT
ENTRYPOINT []
# Wed, 06 Aug 2025 20:03:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3be0c4ec271f85da17b218aaa58fca96e8c848939594c88a6ca597c087ccbf`  
		Last Modified: Mon, 01 Sep 2025 23:08:56 GMT  
		Size: 17.0 MB (16971713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac376c62e7660b6b4f2539cfb908a1eafe161ec0716fe534ee5a002a9a72c6e`  
		Last Modified: Mon, 01 Sep 2025 23:09:01 GMT  
		Size: 47.0 MB (46986047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21566037bd2066a0e57ae51436962b2809e2105c52235f3eb38a5351c17bff41`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c605f578e3a4fdaeb55897c0f7bc3c9d029f93fc9d51a5da206001ef6e72cbfc`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa8daeafe7a0dd7654fd9149158e55e176baa2a2e6b379833840cdbea773857`  
		Last Modified: Tue, 02 Sep 2025 01:13:14 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021c5fccf73e3c053aa3be95aac1b7fe2d4d1528b0e0649c26df31b82cf76912`  
		Last Modified: Tue, 02 Sep 2025 01:13:18 GMT  
		Size: 14.1 MB (14091799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ececdebe9177efec301bb7f4201b908dfb8711d407197dbc9b928279539d6d81`  
		Last Modified: Tue, 02 Sep 2025 01:13:09 GMT  
		Size: 224.7 KB (224665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:7d5643a4b22239ec21625515a3731ac8d110cf04300efaa61237e66a12f5dd59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3373683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810c9583003f820c933873da5868abbbee12bab8a6021d76154550f2ce8d1d37`

```dockerfile
```

-	Layers:
	-	`sha256:14b9f1a75e440a97089c939dbd8107d95ec1b4b307bdc11ec3c16d548de00953`  
		Last Modified: Tue, 02 Sep 2025 02:32:41 GMT  
		Size: 3.3 MB (3349600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:114acf4f4f49029fd1e8ea8699580e8d39d4e83834040d6538a41b5486b926be`  
		Last Modified: Tue, 02 Sep 2025 02:32:42 GMT  
		Size: 24.1 KB (24083 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:39bb59db54d30b5f7d175539f97bcbd589401f8f27cf989e6ff991fdf9cba176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102080379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27d7b9d4cf85450155aa868ba9a638a85d29d48016818aa9f4a6892121f86ca`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:cd43b2c2117454679b981355ba71c009d527d1ebe0a6c3fc69420af222fd6ee7 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        riscv64)          ESUM='f79ef9103ca89faae1d46794cd719b3a8d73079f63df977c92307b7ff9c3d726';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Aug 2025 20:03:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Aug 2025 20:03:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Aug 2025 20:03:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:03:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_MAJOR=11
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_VERSION=11.0.10
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_SHA512=404143be042016fcc8e2d9d960dafe39608899ad24c5f181bdade919100ba1d3206d55a79f20c8dc0c32905b1729f80354da94f7916af86c98ebe4b21cc9b4c2
# Wed, 06 Aug 2025 20:03:27 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 Aug 2025 20:03:27 GMT
ENTRYPOINT []
# Wed, 06 Aug 2025 20:03:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4e823e9332188e662391782d0d87ba101759880efca7a17d9a5a20e8906cc8d7`  
		Last Modified: Tue, 19 Aug 2025 17:59:44 GMT  
		Size: 26.9 MB (26851104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ec5a1c77b69aa8bd266738d17902d05a6735dd53a924bdc4748fdec9679522`  
		Last Modified: Tue, 02 Sep 2025 00:15:06 GMT  
		Size: 16.3 MB (16305648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a84fdfc6562cf08ab021eb549fc7ffb82ae19fdf22d35ec313d0fe72e7cfc33`  
		Last Modified: Tue, 02 Sep 2025 03:15:45 GMT  
		Size: 44.7 MB (44656828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3e3655d8e426ca45b2390c53ad05464e104f74db149dc769ff92af16d2fb47`  
		Last Modified: Tue, 02 Sep 2025 00:29:36 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486a12c21b78f8d0c65e635632525266e969bd22be0df91bf3ffd934c9ab95da`  
		Last Modified: Tue, 02 Sep 2025 00:29:39 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490148680bd11ab4e53ad7396c4f1a345b0ffcfb783b512e9f6ca72c1ac7d49c`  
		Last Modified: Tue, 02 Sep 2025 02:22:50 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b6d2d0572e582d1e71e50d9c0877dbc2e215a185519104a1fd1e3741403793`  
		Last Modified: Tue, 02 Sep 2025 02:22:51 GMT  
		Size: 14.1 MB (14067939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed69c4b24535d58c7b0276fb1f617c7b0f16b728673388ffabf52e1c863a296`  
		Last Modified: Tue, 02 Sep 2025 02:22:52 GMT  
		Size: 196.2 KB (196216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:580bde37255efc4dd5e44c9df507a8f826879f736c97f0c671e9f7452fe4ab26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3376276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05783b518de4718b7dd29dfb5b841bf6f0b7db19b2349deb926f954ae341b3d6`

```dockerfile
```

-	Layers:
	-	`sha256:1ca0654f1201c920293a06bdd5cbd8af4d1b2264e3955248f845c837fd5b9a56`  
		Last Modified: Tue, 02 Sep 2025 05:30:51 GMT  
		Size: 3.4 MB (3352004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4056a7a7a46d73d9fc888ad915f7ba21d50c622e6f90a570f7d5e69a247e5a85`  
		Last Modified: Tue, 02 Sep 2025 05:30:52 GMT  
		Size: 24.3 KB (24272 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:ef3e782fba786e99c78c3c61a2de00a4833abbc3f5fca59d3a05ed643ed7c48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106654003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f4fe610c5e52cd65c18fec604b466aee4366b09f2ed0c868d0d7793231cb00`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        riscv64)          ESUM='f79ef9103ca89faae1d46794cd719b3a8d73079f63df977c92307b7ff9c3d726';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Aug 2025 20:03:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Aug 2025 20:03:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Aug 2025 20:03:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:03:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_MAJOR=11
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_VERSION=11.0.10
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_SHA512=404143be042016fcc8e2d9d960dafe39608899ad24c5f181bdade919100ba1d3206d55a79f20c8dc0c32905b1729f80354da94f7916af86c98ebe4b21cc9b4c2
# Wed, 06 Aug 2025 20:03:27 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 Aug 2025 20:03:27 GMT
ENTRYPOINT []
# Wed, 06 Aug 2025 20:03:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82cb5b65623a0098d812fc3093e05fc877923cbe33814d2fdf26bfedfdc87fd`  
		Last Modified: Tue, 02 Sep 2025 01:00:01 GMT  
		Size: 17.0 MB (16988801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a23d60df9e5a17d9ece5f7731f81ba0f8466c274f2d78eb21513d0a7afc329`  
		Last Modified: Tue, 02 Sep 2025 01:04:57 GMT  
		Size: 46.5 MB (46481676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc4aab63f3b1588162d2f42a019109870aa752e7c48b653658e147d125e731f`  
		Last Modified: Tue, 02 Sep 2025 01:04:51 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c37e822c8d255bc5db86b34326a15caedc638bb36b552cd67e991b59fa27e0a`  
		Last Modified: Tue, 02 Sep 2025 01:04:51 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f889f3b9de15f2b6407ba16eb47d92ef0fbfc7110f6f83fd9706bb078fe1012`  
		Last Modified: Tue, 02 Sep 2025 09:40:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d51574fcf7cc78dce5773ff2a656e0527b4cf9559a580fba226575035111e3`  
		Last Modified: Tue, 02 Sep 2025 09:40:49 GMT  
		Size: 14.1 MB (14095481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820f30e87b19d372359fad776e52788037bb13308fe283b365639da167899d85`  
		Last Modified: Tue, 02 Sep 2025 09:40:47 GMT  
		Size: 225.2 KB (225160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:43d932c78e0d00ff3150f45c09c4dff6877d9df1fd1a447a00c3ef4d9c38e4d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3374507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee26697aa72afb2b2f79a259aef33f4c94ac8fe1ce41608f24f831726053ccb`

```dockerfile
```

-	Layers:
	-	`sha256:79afdf8ce82dff34a173f29fd4289c84db5c18e5245375497c2196f4e5ec6df2`  
		Last Modified: Tue, 02 Sep 2025 11:31:04 GMT  
		Size: 3.4 MB (3350168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87ead7718c62e63ae889148f3d4e925e4ce5f5aa02448751617c463b5303b8a0`  
		Last Modified: Tue, 02 Sep 2025 11:31:05 GMT  
		Size: 24.3 KB (24339 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17` - linux; ppc64le

```console
$ docker pull tomcat@sha256:5b958bc444bff8eacfe6879fc4b783f3605f8c6023657cb02d58f67d12186aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114336741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ebe0d6c439392d2c4ef25e74f968bfa17a76c5f5e03e9a11d6c614e909f065`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        riscv64)          ESUM='f79ef9103ca89faae1d46794cd719b3a8d73079f63df977c92307b7ff9c3d726';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Aug 2025 20:03:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Aug 2025 20:03:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Aug 2025 20:03:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:03:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_MAJOR=11
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_VERSION=11.0.10
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_SHA512=404143be042016fcc8e2d9d960dafe39608899ad24c5f181bdade919100ba1d3206d55a79f20c8dc0c32905b1729f80354da94f7916af86c98ebe4b21cc9b4c2
# Wed, 06 Aug 2025 20:03:27 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 Aug 2025 20:03:27 GMT
ENTRYPOINT []
# Wed, 06 Aug 2025 20:03:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85ac53e3ada2c73fae4a44e2b5328577d67806f9e18dabe8b55b2a62e771c8c`  
		Last Modified: Tue, 02 Sep 2025 00:16:49 GMT  
		Size: 18.8 MB (18814806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27508cc8acfb51284e58496b002264e3caa926a3e9d05de67c03cf2ed9a912c1`  
		Last Modified: Tue, 02 Sep 2025 00:26:47 GMT  
		Size: 46.8 MB (46826314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a55141f793c5cd0bfe5d0ef5e845e954f6dffb9003d18a7ada0adaea3d8310e`  
		Last Modified: Tue, 02 Sep 2025 00:26:40 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e8417b8f2033d277f6119bbd7b9485746d10b51b486069c7aa564b286885b1`  
		Last Modified: Tue, 02 Sep 2025 00:26:41 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a22c61bb053414331af2be4b2b111356d0ffad3198522999f677558d9849fa2`  
		Last Modified: Tue, 02 Sep 2025 09:55:01 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55e4aa6603f4cad7a8e6088b169c8c791df02d1df4ce441fd0e38ebfab5ab8b`  
		Last Modified: Tue, 02 Sep 2025 09:55:03 GMT  
		Size: 14.1 MB (14106876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ab68b810d549816dc4a33f50f6597769d141afc1ce35405e8f03cb512b0a38`  
		Last Modified: Tue, 02 Sep 2025 09:55:01 GMT  
		Size: 256.6 KB (256567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:15165458d6358f7631ef7ad594b259dfc9e8aba6282142bb914be8015fbe7bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3377914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21164896ccc4d3ee96eca3afb16211cf157e60b4522264fcc219da68dcc4229d`

```dockerfile
```

-	Layers:
	-	`sha256:1326891d1c34ce6d6663ad05de46185f69036622e772e49277646ad39a386348`  
		Last Modified: Tue, 02 Sep 2025 11:31:09 GMT  
		Size: 3.4 MB (3353725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a962503933ef9c808f0261aed833616998cb5f202246ab5f304ab8dea800b7d0`  
		Last Modified: Tue, 02 Sep 2025 11:31:10 GMT  
		Size: 24.2 KB (24189 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17` - linux; riscv64

```console
$ docker pull tomcat@sha256:b056672c2735867c4069a20a7a54f48a42ffa42e39aaf931495e44a24caf07d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107290022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84d80fcdc4294ea1d1e842ecd59f5b8408a31b86dff134d89a438ab8fbc0b90`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 30 Jul 2025 07:17:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:17:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:17:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:17:52 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:18:34 GMT
ADD file:07f3c32dd2b7f6af0f399701257442794654b72aa96759b98cb033a715461739 in / 
# Wed, 30 Jul 2025 07:18:38 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        riscv64)          ESUM='f79ef9103ca89faae1d46794cd719b3a8d73079f63df977c92307b7ff9c3d726';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Aug 2025 20:03:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Aug 2025 20:03:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Aug 2025 20:03:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:03:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_MAJOR=11
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_VERSION=11.0.10
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_SHA512=404143be042016fcc8e2d9d960dafe39608899ad24c5f181bdade919100ba1d3206d55a79f20c8dc0c32905b1729f80354da94f7916af86c98ebe4b21cc9b4c2
# Wed, 06 Aug 2025 20:03:27 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 Aug 2025 20:03:27 GMT
ENTRYPOINT []
# Wed, 06 Aug 2025 20:03:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b12e9b07091787c99b29dd2be63680c86c47e8be60a46566329007fb82cee41d`  
		Last Modified: Tue, 12 Aug 2025 17:05:53 GMT  
		Size: 31.0 MB (30951577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea48af681b8ec6db282cced99124adaf7d258d933ef637b46da596f62b231927`  
		Last Modified: Tue, 12 Aug 2025 17:44:15 GMT  
		Size: 17.9 MB (17863907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b74f9cf7baf6f7b0c1e77e289fc9e599a6ffcb5a0147ca52e1181bc1d94a64`  
		Last Modified: Tue, 12 Aug 2025 17:44:21 GMT  
		Size: 44.0 MB (43965964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0ebe902f842d3c6e3598288a8eedd60e9291f9a85e0ac6c175ede1ea22a0c0`  
		Last Modified: Tue, 12 Aug 2025 17:44:17 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9596ee74bb7018562fbf39d62d46df4645102ff2ea59e54dcad5d9d28c7a2ba`  
		Last Modified: Tue, 12 Aug 2025 17:44:15 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c54c64e3ed471209a19dfedb691b514cc1bb1f07a14e19fd78b3da80365be2`  
		Last Modified: Wed, 13 Aug 2025 08:21:16 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b1f4078f5f064718057b19e237ca4b97a8bc1a79fc208e3083d8bfad8ff46b`  
		Last Modified: Wed, 13 Aug 2025 08:21:20 GMT  
		Size: 14.3 MB (14277885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9506d22214805d68d9bdaf4f5f2ad9cbcec8214064cca96a1de9b1a7aa0d7b10`  
		Last Modified: Wed, 13 Aug 2025 08:21:30 GMT  
		Size: 228.0 KB (228045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:2d283b09522d5f5b122f8de7dbc457005b59167e7727bc0ae8b45782a76c0b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3365917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b85d2d8ce57fcb37f9ca3862023956293271e5ed69f7033940d2113d2fa844ee`

```dockerfile
```

-	Layers:
	-	`sha256:0b7cabdc54e336c235f78f91c56f53e72fd68a5b1b4060632850e7dd3e714930`  
		Last Modified: Wed, 13 Aug 2025 08:30:11 GMT  
		Size: 3.3 MB (3341727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:670d7a7ed37163fa017a9a5d3d66153ee5fd0397ca1122c247da061105e24a51`  
		Last Modified: Wed, 13 Aug 2025 08:30:12 GMT  
		Size: 24.2 KB (24190 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17` - linux; s390x

```console
$ docker pull tomcat@sha256:cf69b416dac8b6133b690b12edbbcbb99b13e5cf54c243c8a075307549b5c365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105823076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72175c0f853e3ed86340bd3452326f1c52c179ed8e1cda0eb1979005d723426f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:9c3c50a7bf89c14623163f11927acdf7c8624c7519f83f2d95bf5a99ea4d21f9 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2885b944da3793144d4a86a29524f4d7b68ba155f5c08afa444a3b40f7071892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='98f9d60be880b6ec551f5f1fcd784971aa573e8d8f5b9923fb0148c25afcd161';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='a8a5294e1c2353280525dfde607e71125fbdf767c6be85382a74d2d9d175d908';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='a0a3e94b278a869a2a03802cd549ca0ecdfe1f568175a8ddac113613ee9a8bb9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        riscv64)          ESUM='f79ef9103ca89faae1d46794cd719b3a8d73079f63df977c92307b7ff9c3d726';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='1cb3764ea019a8258c1faf646704da3c1cc6b604bc2af51fe958b078d9826794';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Aug 2025 20:03:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Aug 2025 20:03:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Aug 2025 20:03:27 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:03:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_MAJOR=11
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_VERSION=11.0.10
# Wed, 06 Aug 2025 20:03:27 GMT
ENV TOMCAT_SHA512=404143be042016fcc8e2d9d960dafe39608899ad24c5f181bdade919100ba1d3206d55a79f20c8dc0c32905b1729f80354da94f7916af86c98ebe4b21cc9b4c2
# Wed, 06 Aug 2025 20:03:27 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 06 Aug 2025 20:03:27 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 06 Aug 2025 20:03:27 GMT
ENTRYPOINT []
# Wed, 06 Aug 2025 20:03:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:80a64b6a7d961af355cc1a24ce954958de51e8bc2fb336684c1fbec689663c29`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 29.9 MB (29933009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d5f58fa09318554c52b155dcb73854bc79a0741b430e811ef3fa8a7793d23a`  
		Last Modified: Mon, 01 Sep 2025 23:13:45 GMT  
		Size: 17.6 MB (17580585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af589614fe8ccdc9d316159f4de5db85d1b820cc4e54d1dd25e666d343e7e696`  
		Last Modified: Mon, 01 Sep 2025 23:18:41 GMT  
		Size: 44.0 MB (43974081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c274808ed3f10f414487ac687cbc5926d36497ccc90cc67cb30bd039938189d4`  
		Last Modified: Mon, 01 Sep 2025 23:18:37 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85681033515f1be8c2f361544de6290e74653ee31db0f7c54df3d0e87a794d67`  
		Last Modified: Mon, 01 Sep 2025 23:18:37 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4267e1c45ffc359d55d63b1bf8bdb0b07ba5e0ab9a41a70aff0df8bc74bc1c`  
		Last Modified: Tue, 02 Sep 2025 02:45:11 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e65b1524b6580db7fce152b0db2474c3d80f7d4541408701877be5a9f583b6c`  
		Last Modified: Tue, 02 Sep 2025 02:45:12 GMT  
		Size: 14.1 MB (14100149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f9c4b774311a7b702b36e33c6f4002a573b9feb7d72d75828eab46a6671baf`  
		Last Modified: Tue, 02 Sep 2025 02:45:11 GMT  
		Size: 232.6 KB (232610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:5f3ffde22c6f41999e404a631210ad2523183cb19dda18ce3fac2d5498bc5f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3375883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441c39a2364a115c1a97f0eec8f1a804fbf9c4e91844b5b46219855e5124f1bb`

```dockerfile
```

-	Layers:
	-	`sha256:240552783b10472f9750095bd73ba46726f9bf2579329fb766db55c4e4c6720e`  
		Last Modified: Tue, 02 Sep 2025 05:31:05 GMT  
		Size: 3.4 MB (3351799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88a0a3796bac91cb3fa2f144f8b35f0c25496913d9f68a2350ff8db142644a6f`  
		Last Modified: Tue, 02 Sep 2025 05:31:05 GMT  
		Size: 24.1 KB (24084 bytes)  
		MIME: application/vnd.in-toto+json
