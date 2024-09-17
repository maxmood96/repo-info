## `tomcat:10-jre17-temurin-jammy`

```console
$ docker pull tomcat@sha256:8bfb0ce94318830dd795ab883a308e9e3e7fed70bb6ee50c60c828245ac2b56c
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

### `tomcat:10-jre17-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:db4e3ce239f9930140d185f075b2cac1fc5dad48cc1afad54f067c4429e88fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 MB (106509065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd737b34ad35faf387830e4f8906c73a6d3f47bb386ee48f6be396dac2bc8dd`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 02:03:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 11 Sep 2024 02:03:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Sep 2024 02:03:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
WORKDIR /usr/local/tomcat
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 02:03:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 02:03:19 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_MAJOR=10
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_VERSION=10.1.29
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_SHA512=792a0a56963fe67ec88536a7b9bc338d9e9dc0b1c5d66e89fce62040f148c7be7d4e70e06c0d23d0b5338068eca87cd2669244364ba0aa900ffdcf3eb82bc8a9
# Wed, 11 Sep 2024 02:03:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 11 Sep 2024 02:03:19 GMT
ENTRYPOINT []
# Wed, 11 Sep 2024 02:03:19 GMT
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
	-	`sha256:a32d681e6b995fe897bf388fc57befba67a3692e3f94f2493558cea4f6aab3b4`  
		Last Modified: Sat, 17 Aug 2024 01:13:28 GMT  
		Size: 47.3 MB (47280215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabdd0a18314116a0ebaebbd74aa891cbb1da4650890b6187e36c306bbdca902`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5161e45ecd8d096f978edcb483c5ed70580526e02a1f8155653ca1c6c192f097`  
		Last Modified: Fri, 23 Aug 2024 19:27:49 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc641b5ce9fb06eb360d5f2ceee4f8a86287c6b32f623f40932f35680634c174`  
		Last Modified: Wed, 11 Sep 2024 19:54:49 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801440b95074df7c2504f46fad75f3eacd4fb508d8f10c5f47185a253edd006a`  
		Last Modified: Wed, 11 Sep 2024 19:54:49 GMT  
		Size: 12.9 MB (12949186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ecfab76823521a212a5a94a90b318658e8118d7082f1a5764cd6aafa982a28`  
		Last Modified: Wed, 11 Sep 2024 19:54:49 GMT  
		Size: 3.0 MB (2965606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:4049bd43c77765dc187fad773ee24c41a26a0b6f90f19d596d20070e2913fe83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3555665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89362a4d832682a021d5ce6c38b1cc4118c386dbb0f8aeb5372883e6356d6baf`

```dockerfile
```

-	Layers:
	-	`sha256:e2e71d9300a918abe2e6fde7e7ca7673d23bf503062fbfe25b04e0f6e02980f5`  
		Last Modified: Wed, 11 Sep 2024 19:54:49 GMT  
		Size: 3.5 MB (3533623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8c2e857bd4fb58c3e28e73c510a28a010ee849d22b24457a1f5d87b99a5b23c`  
		Last Modified: Wed, 11 Sep 2024 19:54:49 GMT  
		Size: 22.0 KB (22042 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre17-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:6c812ae9f18433503350c30362fd9e795b1da2258613098bcade5c8f62041231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98060421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96ec7496712a78de1c8554cde224d9d8f6e5700b92bc65e86c2fb4538898c52`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 11 Sep 2024 02:03:19 GMT
ARG RELEASE
# Wed, 11 Sep 2024 02:03:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 02:03:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 02:03:19 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 02:03:19 GMT
ADD file:291158c1d919b2d4290b5112a77dc0f7bdf0d45caa53b3556390707d29d2796a in / 
# Wed, 11 Sep 2024 02:03:19 GMT
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 02:03:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 11 Sep 2024 02:03:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Sep 2024 02:03:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
WORKDIR /usr/local/tomcat
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 02:03:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 02:03:19 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_MAJOR=10
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_VERSION=10.1.29
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_SHA512=792a0a56963fe67ec88536a7b9bc338d9e9dc0b1c5d66e89fce62040f148c7be7d4e70e06c0d23d0b5338068eca87cd2669244364ba0aa900ffdcf3eb82bc8a9
# Wed, 11 Sep 2024 02:03:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 11 Sep 2024 02:03:19 GMT
ENTRYPOINT []
# Wed, 11 Sep 2024 02:03:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:35baf9f88f9b2cb840329dab5e6720d4fc535f9c150ca402cd7cd955065cd481`  
		Last Modified: Fri, 13 Sep 2024 12:45:25 GMT  
		Size: 27.5 MB (27534027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31edfebc2dc37b7fcd5adfb6ee3872ba74788ba24e8c2c3a40107b9fd85153c`  
		Last Modified: Tue, 17 Sep 2024 01:23:55 GMT  
		Size: 12.5 MB (12463235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650644a6a2fde723a4a4bcffecfac704fce0ff7d478e6f657d1eeb5a5eab378e`  
		Last Modified: Tue, 17 Sep 2024 01:27:00 GMT  
		Size: 44.9 MB (44944565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c257ea7b249dc09b593008183263e52497de07baff400a64f68a321dde2ade5a`  
		Last Modified: Tue, 17 Sep 2024 01:26:53 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e4647891223776c0385d2437e9e9e9f1b6465ba5ec6f4c8e6b7c944d0c0012`  
		Last Modified: Tue, 17 Sep 2024 01:26:53 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bf6726675b69bd78bc581d13877b38b5b25aad2133fada72ad673874d439a9`  
		Last Modified: Tue, 17 Sep 2024 03:07:20 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6e6a7e0154b858bdf00726bb688b68ec9766c4b3b61386d6b1d0db3b27d5d7`  
		Last Modified: Tue, 17 Sep 2024 03:07:21 GMT  
		Size: 12.9 MB (12925214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39215a188ebc3ce70f30caa361a2b3048c4ce42b2aa046c9c7ecd784ae0c53c9`  
		Last Modified: Tue, 17 Sep 2024 03:07:21 GMT  
		Size: 190.9 KB (190910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:6727b14c1d61b991f481fb68e2c5188152794a6067f4e80ff2bfa994320dc545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3555189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67f1d703e9973f73797bb974f8bed62a1d8ffdb001ea81545c31a5961f0ce7e`

```dockerfile
```

-	Layers:
	-	`sha256:cf54ac119de591b2f6405306f89bf994a4db78a3658640f69e4685578b682847`  
		Last Modified: Tue, 17 Sep 2024 03:07:20 GMT  
		Size: 3.5 MB (3532966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a43047607481553bfdb008e379da231f5bb2f3f36098c3e0908c4955ffc9ea3b`  
		Last Modified: Tue, 17 Sep 2024 03:07:20 GMT  
		Size: 22.2 KB (22223 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre17-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:7366dd55268abbf88669764cedd34ee1dc785d93f548a77e1b434db67b05b973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103717159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ab2e4068af214b8e756b621a60dde25fb42b3bee1664522d70d66117d7de82`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 02:03:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 11 Sep 2024 02:03:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Sep 2024 02:03:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
WORKDIR /usr/local/tomcat
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 02:03:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 02:03:19 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_MAJOR=10
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_VERSION=10.1.29
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_SHA512=792a0a56963fe67ec88536a7b9bc338d9e9dc0b1c5d66e89fce62040f148c7be7d4e70e06c0d23d0b5338068eca87cd2669244364ba0aa900ffdcf3eb82bc8a9
# Wed, 11 Sep 2024 02:03:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 11 Sep 2024 02:03:19 GMT
ENTRYPOINT []
# Wed, 11 Sep 2024 02:03:19 GMT
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
	-	`sha256:fe26b7a9fc390ef63cf055e6e311a50e2bb6c11bc64c80f450417a71eb7ba031`  
		Last Modified: Sat, 17 Aug 2024 01:36:13 GMT  
		Size: 46.7 MB (46746294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a5437d6fef2529f65b67ce9b2a75371cef52e384174649eac3424168e5c623`  
		Last Modified: Sat, 17 Aug 2024 01:36:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7525b10c4bd14139ded90d85ae282e53b2795402b1d01d327856dc57969f13e3`  
		Last Modified: Fri, 23 Aug 2024 19:45:19 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59fdc9d04a5f50e858ab3196d0cca13d0e8d16479550ca290efc18ce593d94b`  
		Last Modified: Wed, 11 Sep 2024 19:57:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1426f8fb873da542fd5199b3e016452540f12941fc8e16ab5b26f28d2bf2bdc`  
		Last Modified: Wed, 11 Sep 2024 19:57:13 GMT  
		Size: 13.0 MB (12951427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4a385e53beb4ba2bc923ac9eedc67626e9990644ca9529fd743e0d0cb0c117`  
		Last Modified: Wed, 11 Sep 2024 19:57:13 GMT  
		Size: 2.8 MB (2806559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:665f1a5192e4709dd2c17af01c671d28393db5760cd3931822797c4b2ecaf575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3556662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9187194e061d9937501d43a3d221f28daa46c6282c557e3d9f5d385a54d3ace`

```dockerfile
```

-	Layers:
	-	`sha256:a8a37536bb5ce3f60f66b11db73e614642e1d5cc8ab7ed713dca2b9c667a1367`  
		Last Modified: Wed, 11 Sep 2024 19:57:13 GMT  
		Size: 3.5 MB (3533915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e192da05abb49ec62085d6fecde9638f343f92966563fabe6f56308d4fc0ac69`  
		Last Modified: Wed, 11 Sep 2024 19:57:12 GMT  
		Size: 22.7 KB (22747 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre17-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:321511a6a8c943ca2702249f19ce9add03716a7969b554881c093c31c17d9866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112733021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb22d62cbbb9c60e1b140ebca6c160db29b5556973c05e9fc2f1c2b720e738d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 02:03:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 11 Sep 2024 02:03:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Sep 2024 02:03:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
WORKDIR /usr/local/tomcat
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 02:03:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 02:03:19 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_MAJOR=10
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_VERSION=10.1.29
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_SHA512=792a0a56963fe67ec88536a7b9bc338d9e9dc0b1c5d66e89fce62040f148c7be7d4e70e06c0d23d0b5338068eca87cd2669244364ba0aa900ffdcf3eb82bc8a9
# Wed, 11 Sep 2024 02:03:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 11 Sep 2024 02:03:19 GMT
ENTRYPOINT []
# Wed, 11 Sep 2024 02:03:19 GMT
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
	-	`sha256:c8df1510f2e515b4ef656dd9c93352c60dc24965dd8ee75c31bc74018cb42aeb`  
		Last Modified: Sat, 17 Aug 2024 01:02:58 GMT  
		Size: 47.1 MB (47116012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6716094041a01730dfc01fdf740d805f8100542358fe6f56639974b95f13ce`  
		Last Modified: Sat, 17 Aug 2024 01:02:50 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ff4fd572d6d5509077d991254c470c69c62db63e9060083f4f1902323d94df`  
		Last Modified: Fri, 23 Aug 2024 19:24:39 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadfba30a5f95d9ff3fd9ba4b1aef3e1e58bec1aed2482f9b7b4595b4295e522`  
		Last Modified: Wed, 11 Sep 2024 19:59:18 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f850e7b22ba3344baedc0183687567b9033af0dec53246c438234a1d4b2518`  
		Last Modified: Wed, 11 Sep 2024 19:59:19 GMT  
		Size: 13.0 MB (12963282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b027cb7c4d2db7191a79f2ebc39e318d739456704e477f92137502ace6d83`  
		Last Modified: Wed, 11 Sep 2024 19:59:18 GMT  
		Size: 3.3 MB (3348526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:fed6f52992db4588130ce669554d89977cca371f4d2314a762bd80ea201aad63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3560302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8820d222dfce27c33ff5a77fdeea8f5782b4a830a63bccefc8aee6540605a4`

```dockerfile
```

-	Layers:
	-	`sha256:82af1c16d092f97cb51beb3d5875e3d91256ec63dca6ad4a1dc9a9ab0e7de2c9`  
		Last Modified: Wed, 11 Sep 2024 19:59:18 GMT  
		Size: 3.5 MB (3538142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f8de4af45a3eb8ec9000ff8d98857e70257532b0714bbe4666701d464ffe1f9`  
		Last Modified: Wed, 11 Sep 2024 19:59:18 GMT  
		Size: 22.2 KB (22160 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre17-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:b39fffa6912deea17f32133f2513d4e7ebb05453ec3726b852d0195d67a3b120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101063964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f46146b655d45b9d0ef1161540a71161fa8c71ba26b265108e8fc677745e043`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:24 GMT
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
# Tue, 13 Aug 2024 09:28:24 GMT
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
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 02:03:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 11 Sep 2024 02:03:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Sep 2024 02:03:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
WORKDIR /usr/local/tomcat
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 02:03:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 02:03:19 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_MAJOR=10
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_VERSION=10.1.29
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_SHA512=792a0a56963fe67ec88536a7b9bc338d9e9dc0b1c5d66e89fce62040f148c7be7d4e70e06c0d23d0b5338068eca87cd2669244364ba0aa900ffdcf3eb82bc8a9
# Wed, 11 Sep 2024 02:03:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 11 Sep 2024 02:03:19 GMT
ENTRYPOINT []
# Wed, 11 Sep 2024 02:03:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f487d2bc1de52e44ed06dfc0c18b748d484f1eb638bdc1cbf599195a96c480be`  
		Last Modified: Sat, 17 Aug 2024 01:32:19 GMT  
		Size: 13.0 MB (12955186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb43b5eb6b749b20cbc0d4d49fa146e13299ac7c636c67f6b885928ff809d1d`  
		Last Modified: Sat, 17 Aug 2024 01:34:05 GMT  
		Size: 43.9 MB (43864131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa6e76a567ef01fbd878046dfba9c29424f4011e53ee93496f2d3290648a8d1`  
		Last Modified: Sat, 17 Aug 2024 01:34:00 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436b27d7c7e10a663ee6272640668b780b0fc626cf34c50e8fbae3c0488723b1`  
		Last Modified: Fri, 23 Aug 2024 19:47:54 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a33754f6fde17c99b71aef2f9f028a8700d64459d7b48e5e04774bac5e885bb`  
		Last Modified: Wed, 11 Sep 2024 19:58:10 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db442f42745b1c2232c9cc0c97bf07689cbc1224c683a56454187bf87fe1ce7`  
		Last Modified: Wed, 11 Sep 2024 19:58:10 GMT  
		Size: 13.0 MB (12952990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51555e8ea37e3fd79963369e0e51d7ba477a7d4c434fa5918460435d19223ce8`  
		Last Modified: Wed, 11 Sep 2024 19:58:10 GMT  
		Size: 2.7 MB (2650682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:53d5f2938cf588ca51b05e5591a59e611a0b73678971ec6ebc67cfa67fcba55c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3556853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3e80d64d851cae14885a1b4c508396a33d50f0a5ec70a124c4bd0f40fc2aab`

```dockerfile
```

-	Layers:
	-	`sha256:d51290677d17b8d88548325654638b890b36d1657bf859ba3b5f83321f26e34f`  
		Last Modified: Wed, 11 Sep 2024 19:58:10 GMT  
		Size: 3.5 MB (3534745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e32d933b72d58e6048366b14ee79bbace44cc6190def43d6edf0ece586d3d3c3`  
		Last Modified: Wed, 11 Sep 2024 19:58:10 GMT  
		Size: 22.1 KB (22108 bytes)  
		MIME: application/vnd.in-toto+json
