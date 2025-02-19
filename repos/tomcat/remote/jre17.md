## `tomcat:jre17`

```console
$ docker pull tomcat@sha256:285567721dc0749a453523b822d3b3a6425e344574cd529900f3062bbb9df2cf
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
$ docker pull tomcat@sha256:5d4339c273f89b300400105a8a3df398911cf330d9e26cffa92b2c52d0049964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120313106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06983d37e452362660410f76d4f40affbefbbf189cbe8adbfda67c016f61333`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 18 Feb 2025 11:56:33 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 18 Feb 2025 11:56:33 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 11:56:33 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
WORKDIR /usr/local/tomcat
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 11:56:33 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_MAJOR=11
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_VERSION=11.0.4
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_SHA512=1b86558c398086b080f5a2c298b8d55c32d958e0c41782b1bb384d12e8d76f23d54cd98affa177af3d3e6fdc4fd55bdbf7796f5fa5e2ceb6310be0a0fd1acf9a
# Tue, 18 Feb 2025 11:56:33 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Feb 2025 11:56:33 GMT
ENTRYPOINT []
# Tue, 18 Feb 2025 11:56:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 03 Feb 2025 23:00:26 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe46403441ac2f7f78a779417c34f07529970491dc25499a9f2321772006f90`  
		Last Modified: Tue, 04 Feb 2025 07:26:46 GMT  
		Size: 17.0 MB (16962484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4ee04af8786c03105915946c5bf4d14aa3901749a6e7e6f54d94d23bdab7c`  
		Last Modified: Tue, 04 Feb 2025 07:17:34 GMT  
		Size: 47.0 MB (46952663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da94a33fa1bc27770bb6588ff1cbef17c2cb37284348caf2ac38adc859173a`  
		Last Modified: Tue, 04 Feb 2025 07:23:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03e4717322c01c3bff3cfcbbfebaf8330f4f418957eac816b99ca0494b7bbd8`  
		Last Modified: Tue, 04 Feb 2025 07:15:16 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e50c43fc217bd83fec0e61838ddeb869a19d461e2012869eec99c6ee5dd7d0`  
		Last Modified: Wed, 19 Feb 2025 01:08:21 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714d55aa4ad43501b40276bf84750ebc995e63fd5f18dedcd9897e577eddcc43`  
		Last Modified: Wed, 19 Feb 2025 01:08:34 GMT  
		Size: 13.8 MB (13808658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c7cf68cc41f4dc13aa7c6a70b8712c18f5fa84c77dcc2ca4dc6d3a1fd508fb`  
		Last Modified: Wed, 19 Feb 2025 01:08:25 GMT  
		Size: 12.8 MB (12832368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:4e1b50bd589fc5dc52475f815b6d8367e40003034b9581065b467898b5ab546b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3206028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc849b8d9f2103a1c22cf35d279ddd333c3a3265dd2716141cee56030c0d1b46`

```dockerfile
```

-	Layers:
	-	`sha256:c6239497192cb0f5c21092dcb15e7e790e44b2b436ff8f190cf51c8ac1f2aa90`  
		Last Modified: Wed, 19 Feb 2025 03:34:37 GMT  
		Size: 3.2 MB (3181949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17771ff94f30df3e87caadede8f09220d70978e32b9c3007da4d93dcb6fec1d9`  
		Last Modified: Wed, 19 Feb 2025 03:34:37 GMT  
		Size: 24.1 KB (24079 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:051bbb14bb8dfd19782f00e9180ed5cd0c5df326f0c21b338c412b1982ba5d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113135307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0acc1182a75b0ec083d44849a8cad1222ad693808d7495ae17a5a977d07203`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:14 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:14 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:18 GMT
ADD file:22301ffa2fa465db7a0f07e0c3ddc488f07cc6a745c39e6f450fdbe37da97418 in / 
# Mon, 27 Jan 2025 04:14:18 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 18 Feb 2025 11:56:33 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 18 Feb 2025 11:56:33 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 11:56:33 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
WORKDIR /usr/local/tomcat
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 11:56:33 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_MAJOR=11
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_VERSION=11.0.4
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_SHA512=1b86558c398086b080f5a2c298b8d55c32d958e0c41782b1bb384d12e8d76f23d54cd98affa177af3d3e6fdc4fd55bdbf7796f5fa5e2ceb6310be0a0fd1acf9a
# Tue, 18 Feb 2025 11:56:33 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Feb 2025 11:56:33 GMT
ENTRYPOINT []
# Tue, 18 Feb 2025 11:56:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3492abb11babfb77cfc5a8904e67b22f4e4fd68c8d8a7fe1119861ed6503b36f`  
		Last Modified: Tue, 04 Feb 2025 08:31:36 GMT  
		Size: 26.9 MB (26874983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c78f4c1289c2528d1df38f88dd5b99ab818699237ae6309db38a8baf5b25bd`  
		Last Modified: Tue, 04 Feb 2025 13:24:50 GMT  
		Size: 16.3 MB (16294514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb9822e82d84e98a2dfc4b6c16a6eeaeb57cd48cac8ae15152492c7391137f7`  
		Last Modified: Tue, 04 Feb 2025 14:12:35 GMT  
		Size: 44.6 MB (44625639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d6ee82a8276c9755b475708acf6835a26fef2c2f63540ad4c03e72570c91a0`  
		Last Modified: Wed, 05 Feb 2025 01:13:04 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1ef011b373aa2375dc028e8b5a48e7d91eabc97074365ab6bf7146c72a9378`  
		Last Modified: Tue, 04 Feb 2025 22:01:16 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d02e133db5b7b8bf04f58984c88c7527a0d5543649de443715db6fd193571d`  
		Last Modified: Sun, 09 Feb 2025 02:02:00 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c0ca23adf281c4ee3fc60ee5c204dac19beaefe83a72166dc165290e544c30`  
		Last Modified: Wed, 19 Feb 2025 02:19:58 GMT  
		Size: 13.8 MB (13783927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045c6db034ce0c7e0c14007b4f84ef4aa48c3f736ad8e325893a3edd53bde87f`  
		Last Modified: Wed, 19 Feb 2025 02:19:56 GMT  
		Size: 11.6 MB (11553598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:99c42f58950678c21ce5d9dd279c2c2b0823388986ea5a9ecfb2045be841eda6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3208620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de6e5f79509c314fabb33b65e5c072ca1f103ddcb0ff6b8f454a0f0d32d5537`

```dockerfile
```

-	Layers:
	-	`sha256:b4b7192a7e92e77daf977c7e04f668d344d582da6b08f8d050fd60a7539d4da8`  
		Last Modified: Wed, 19 Feb 2025 03:34:40 GMT  
		Size: 3.2 MB (3184353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c49c38bdd6b2f2a48626164ae086b42bd8e43115cc09718a3c9f3d91a1ddd36`  
		Last Modified: Wed, 19 Feb 2025 03:34:40 GMT  
		Size: 24.3 KB (24267 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:c5b70cef2da1f610ccc5bbfa706365276529e49838cbc3db7bcf65de940ce3b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118750626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919308694f3b41eafed2a7ede2dd96120191e9bfa07c7613d463fb9f52f92f02`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 18 Feb 2025 11:56:33 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 18 Feb 2025 11:56:33 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 11:56:33 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
WORKDIR /usr/local/tomcat
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 11:56:33 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_MAJOR=11
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_VERSION=11.0.4
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_SHA512=1b86558c398086b080f5a2c298b8d55c32d958e0c41782b1bb384d12e8d76f23d54cd98affa177af3d3e6fdc4fd55bdbf7796f5fa5e2ceb6310be0a0fd1acf9a
# Tue, 18 Feb 2025 11:56:33 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Feb 2025 11:56:33 GMT
ENTRYPOINT []
# Tue, 18 Feb 2025 11:56:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Tue, 04 Feb 2025 06:04:53 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 10:15:57 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646bfcab524deb99e432714a7a838a5f6b98e7a47faa95240fd0168282b7a09d`  
		Last Modified: Tue, 04 Feb 2025 13:15:37 GMT  
		Size: 46.5 MB (46463804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01542aefa0dab0f76d7350aedf449d8ea2544f3d8946d83898cc3f5f2a2bcf8`  
		Last Modified: Tue, 04 Feb 2025 14:59:44 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d80fc1fa5adda672381a8947ac048a52838f4e7b8997a299cf54cb5e941da78`  
		Last Modified: Tue, 04 Feb 2025 14:04:57 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce464ad2f9aa344c63dd6298b049e6735ab8811a212af369191b7fa918ee6e7`  
		Last Modified: Wed, 05 Feb 2025 08:33:17 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcccae51f189e5949bf445bf05b37133e76b0fd36db1a86079bdc800b72f8c5`  
		Last Modified: Wed, 19 Feb 2025 02:11:48 GMT  
		Size: 13.8 MB (13811622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb11bc26604e46e379adff1afc1903fc6cd19304efeda2fec96b5eb0eab6cfb`  
		Last Modified: Wed, 19 Feb 2025 02:11:38 GMT  
		Size: 12.6 MB (12601554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:0551b6e8c4b0f694abd8394d88b61754c9387ecb84322d655975000504efa522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3206852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e170c506a6e4ff2f0bc400d661bf87a7211a9eac983db473804dd3c1b1787e`

```dockerfile
```

-	Layers:
	-	`sha256:c97afac05d06a9a0ba38d366b0f523f8d3004d99f856c755a7f24d2033654dbd`  
		Last Modified: Wed, 19 Feb 2025 03:34:42 GMT  
		Size: 3.2 MB (3182517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e5867c9534e6fcfbe9d1af1d6d4cc0be7008a0c4a0fb3dd536913393416787a`  
		Last Modified: Wed, 19 Feb 2025 03:34:42 GMT  
		Size: 24.3 KB (24335 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17` - linux; ppc64le

```console
$ docker pull tomcat@sha256:0986a0e1804602549033324d6746e40b3313db9b03721cd7ce7f4d385916671d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127445793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852e20b0fb69d5b43b6716432f08db4922753452f73a45af6c620a094160be33`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 18 Feb 2025 11:56:33 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 18 Feb 2025 11:56:33 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 11:56:33 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
WORKDIR /usr/local/tomcat
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 11:56:33 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_MAJOR=11
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_VERSION=11.0.4
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_SHA512=1b86558c398086b080f5a2c298b8d55c32d958e0c41782b1bb384d12e8d76f23d54cd98affa177af3d3e6fdc4fd55bdbf7796f5fa5e2ceb6310be0a0fd1acf9a
# Tue, 18 Feb 2025 11:56:33 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Feb 2025 11:56:33 GMT
ENTRYPOINT []
# Tue, 18 Feb 2025 11:56:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Tue, 04 Feb 2025 07:01:00 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c7b03d73f24fbf1ca191efda6fafe2355b68e6e070a54b70fec6dc3ac0c66e`  
		Last Modified: Tue, 04 Feb 2025 16:27:35 GMT  
		Size: 18.8 MB (18824340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7923544002ba5c478039d0fb05d43328a078cfead2ca01b99222d47980c7c6`  
		Last Modified: Tue, 04 Feb 2025 20:43:38 GMT  
		Size: 46.8 MB (46769578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce00765c25347a0fde9162df1266dd0dcc4a574d71c200b3368feb997f85640f`  
		Last Modified: Tue, 04 Feb 2025 22:01:30 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a6900b7983b5b05b04351ed2096896f7ea1e53c5bec4c6af0b0d2946f25269`  
		Last Modified: Tue, 04 Feb 2025 20:43:35 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cecb08943954f278f0104ee00823cad55b6b4fbc37460a566070a857486f9a`  
		Last Modified: Mon, 10 Feb 2025 05:39:39 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b620b4b2318682a16a1f51ef6b8dc88f3c8238f8add1a6a5864571edb59143dd`  
		Last Modified: Wed, 19 Feb 2025 02:23:53 GMT  
		Size: 13.8 MB (13825410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4233f04599428b979ff534ff1990f1e06bf50bfd7ed55b16eca8c5e5cf0606`  
		Last Modified: Wed, 19 Feb 2025 02:23:53 GMT  
		Size: 13.6 MB (13633997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:79eaf47633a7f98b398aea8f89f36b03eed82655afadce99e3dd45c660fd0293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3210115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b31d2d4817433d7163ae76292bf0de684c7602d3a4a834a3bab45ce65a2a84e`

```dockerfile
```

-	Layers:
	-	`sha256:60fd81d0eb64b870efd07947cb2a3436db9451a1987b899399464242e163282d`  
		Last Modified: Wed, 19 Feb 2025 03:34:44 GMT  
		Size: 3.2 MB (3185930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df8c7bb3db9b1ee0593fea7c82c6139f39c658192a96fcb7528e3951a9390a4e`  
		Last Modified: Wed, 19 Feb 2025 03:34:45 GMT  
		Size: 24.2 KB (24185 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17` - linux; riscv64

```console
$ docker pull tomcat@sha256:36c0426d08014352a5b831e37b94203a7020ca5971ba49517e57b8e70263d9ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118397851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228c57ac17ffeec25b807a9e24ca9e69f51b559f681f1cc72e936c555c435494`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 27 Jan 2025 04:46:38 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:46:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:46:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:46:39 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:47:10 GMT
ADD file:69c46ae9666e78c27ca5b5f25cec1a5536ff16f17cb00104e5c77e722bd8d643 in / 
# Mon, 27 Jan 2025 04:47:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Feb 2025 15:16:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Feb 2025 15:16:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Feb 2025 15:16:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Feb 2025 15:16:00 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Feb 2025 15:16:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Feb 2025 15:16:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Feb 2025 15:16:00 GMT
ENV TOMCAT_MAJOR=11
# Mon, 10 Feb 2025 15:16:00 GMT
ENV TOMCAT_VERSION=11.0.3
# Mon, 10 Feb 2025 15:16:00 GMT
ENV TOMCAT_SHA512=860701b16fcf0ab4674ff8c0a61f79b6427bb8bfc44a88f9251fe39f179f2912341f9621b97e38f31959b27ac3efff9e845b49017d954243bca00e23ea965114
# Mon, 10 Feb 2025 15:16:00 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Feb 2025 15:16:00 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 15:16:00 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Feb 2025 15:16:00 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Feb 2025 15:16:00 GMT
ENTRYPOINT []
# Mon, 10 Feb 2025 15:16:00 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6e1053d729cc1718daa9369927cf6ddfbf892a846041de0e610d1c77ade136c5`  
		Last Modified: Tue, 04 Feb 2025 07:00:41 GMT  
		Size: 31.0 MB (30983910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d426f87ee2be194a115f8eac0bc66ccf7efb2c0a509cd7e58933d92bc42969c7`  
		Last Modified: Wed, 05 Feb 2025 02:18:44 GMT  
		Size: 17.9 MB (17857942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cb4c7ccade82b6f9aea4755f3efb101f92ba9da34717a287a0aa97ef7d6406`  
		Last Modified: Tue, 04 Feb 2025 07:15:45 GMT  
		Size: 43.9 MB (43932362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f958e9b4f34503a84e90d91278f67fa4a769aaf7249ccab4177c9f67fe5daa9f`  
		Last Modified: Wed, 05 Feb 2025 00:47:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc0d60c4c93c647e2faf9282f7287f35c998a80b6c1f32918b797160114d17d`  
		Last Modified: Wed, 05 Feb 2025 02:18:48 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e758a1929058beba35f5fa9e91777df0df978059caca829de0b71c0fc97ee048`  
		Last Modified: Sun, 09 Feb 2025 02:02:25 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0be73bbe9cc64924e80bc7e9db3503d0dd0b0966498c399d546a79a9d3a2d1`  
		Last Modified: Sun, 16 Feb 2025 02:03:19 GMT  
		Size: 14.0 MB (13992326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ee3263a2c1357430d9783663f587f67d0a7bb68e225820c0ef8e6ab34d232b`  
		Last Modified: Sun, 16 Feb 2025 02:03:21 GMT  
		Size: 11.6 MB (11628666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:81a40111a033d8e4151a907dc86e8753dc9540868d1c846e7a5b63198fd86a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3198408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd6709fd91cd40ed6a95992deff45ac8f82d28c6756c1f36a8c87bf7354fd6e8`

```dockerfile
```

-	Layers:
	-	`sha256:d2b7dd87d0b3f87026f291317723ea82db49a864f4c3dd160dc52eb8ceb98b28`  
		Last Modified: Sun, 16 Feb 2025 02:03:24 GMT  
		Size: 3.2 MB (3174224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3f19f579c5dd72531358e2e8396865019043407d2b4aa32a6592d91ad44d921`  
		Last Modified: Sun, 16 Feb 2025 02:03:25 GMT  
		Size: 24.2 KB (24184 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17` - linux; s390x

```console
$ docker pull tomcat@sha256:c178add33462276a5d88c8b435f4202c800b8c77b7c2ba95dcaae8ed924e1ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.4 MB (117432659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea0939c0fa444d78498926c2e683a5623fc2eedb1b6ab0380d88f086bfe20962`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 27 Jan 2025 04:15:19 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:15:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:15:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:15:19 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:15:20 GMT
ADD file:1a65bb049384da7e51a2b1e9180f11d6ec22b1427da7ca5682814abd261ba57e in / 
# Mon, 27 Jan 2025 04:15:20 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 18 Feb 2025 11:56:33 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 18 Feb 2025 11:56:33 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 11:56:33 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
WORKDIR /usr/local/tomcat
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 11:56:33 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_MAJOR=11
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_VERSION=11.0.4
# Tue, 18 Feb 2025 11:56:33 GMT
ENV TOMCAT_SHA512=1b86558c398086b080f5a2c298b8d55c32d958e0c41782b1bb384d12e8d76f23d54cd98affa177af3d3e6fdc4fd55bdbf7796f5fa5e2ceb6310be0a0fd1acf9a
# Tue, 18 Feb 2025 11:56:33 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 18 Feb 2025 11:56:33 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Feb 2025 11:56:33 GMT
ENTRYPOINT []
# Tue, 18 Feb 2025 11:56:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8e1d25585ef2d346b71072d258a697a9d190e3c5754512c7cb978dbbe80911e6`  
		Last Modified: Tue, 04 Feb 2025 08:21:20 GMT  
		Size: 30.0 MB (30027563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d99804e9821e45800ab00828f52aba64f96835ac1dcd99956c5eae60156908a`  
		Last Modified: Tue, 04 Feb 2025 10:14:32 GMT  
		Size: 17.6 MB (17595734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76f586508df29c2f90180df73edd502236daafc282ab28c56c09d06e4015113`  
		Last Modified: Wed, 05 Feb 2025 01:13:09 GMT  
		Size: 43.9 MB (43949891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1789143ae082f8a6e9b11dba5c7de77fa63a56c9669e1ee0c8b6392641dd362`  
		Last Modified: Tue, 04 Feb 2025 10:15:36 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f2400ff57c712af3bad329ea198535724736e379ebfa51cc03f4929918ec27`  
		Last Modified: Tue, 04 Feb 2025 22:01:44 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd95ca595522ffaf87e5939ec8ee72d417d3f1025bbe4e36423dd717890a31b`  
		Last Modified: Sun, 09 Feb 2025 02:02:33 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054f7b2331ee0ebe0c92b5d389603de4fcdf6ae5e1caa1b17579100132a35369`  
		Last Modified: Wed, 19 Feb 2025 02:15:58 GMT  
		Size: 13.8 MB (13819320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ade1a2619c8cae71d59fd700c8d3b0112bc3250625422e9d5de44d09d4e265c`  
		Last Modified: Wed, 19 Feb 2025 02:16:05 GMT  
		Size: 12.0 MB (12037508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:d14ff66b0c73f683308a6f02c6a6ee54267b0028cd58af1c3bb65531eafa5210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3208227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6cb4b460a1bd7dad176032f78bd24ae3e17d7f3cc5acbc2eba46123c4da3117`

```dockerfile
```

-	Layers:
	-	`sha256:64a09345df7543fc606dd5fbb6ec19fee63a09900fbe5d555bc181a17503c02e`  
		Last Modified: Wed, 19 Feb 2025 03:34:49 GMT  
		Size: 3.2 MB (3184148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9d16674e3ecf5381b85689683f51043ead779f8cde08c1331b10692fd55426e`  
		Last Modified: Wed, 19 Feb 2025 03:34:49 GMT  
		Size: 24.1 KB (24079 bytes)  
		MIME: application/vnd.in-toto+json
