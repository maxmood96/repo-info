## `tomcat:9-jre8-temurin-jammy`

```console
$ docker pull tomcat@sha256:bdc1cbadaca2577e1236942f7453a9284ec6fdedfbe8e806b9687bd336202bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `tomcat:9-jre8-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:18e86f8cce8f8f8a3f9e4c8aae71241f614bd422c1cff377ab2a22180a6093be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98072296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d286b2b4de4a47a4d6598e6de8a1ad0118f70deee376ad20d4011f3c061860`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:14:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 07:14:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 07:14:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 07:14:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:14:56 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Wed, 17 Jan 2024 07:15:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='37b997f12cd572da979283fccafec9ba903041a209605b50fcb46cc34f1a9917';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u392b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='91d31027da0d985be3549714389593d9e0da3da5057d87e3831c7c538b9a2a0f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_x64_linux_hotspot_8u392b08.tar.gz';          ;;        armhf|arm)          ESUM='877953bfabcdbcd000c11364d806456ca579a921085de2ca942280ebe168cac2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_arm_linux_hotspot_8u392b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='0ecb0aeb54fb9d3c9e1a7ea411490127e8e298d93219fafc4dd6051a5b74671f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u392b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 17 Jan 2024 07:15:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete."
# Wed, 17 Jan 2024 07:15:22 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 17 Jan 2024 07:15:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 17 Jan 2024 10:42:52 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 17 Jan 2024 10:42:52 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 10:42:53 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 17 Jan 2024 10:42:53 GMT
WORKDIR /usr/local/tomcat
# Wed, 17 Jan 2024 10:42:53 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 17 Jan 2024 10:42:53 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 17 Jan 2024 10:42:53 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 17 Jan 2024 10:42:53 GMT
ENV TOMCAT_MAJOR=9
# Wed, 17 Jan 2024 10:42:53 GMT
ENV TOMCAT_VERSION=9.0.85
# Wed, 17 Jan 2024 10:42:53 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Mon, 22 Jan 2024 23:06:40 GMT
COPY dir:4825d2cf078068e100daae9fb87564bc799530832789b2e16eef40313f533834 in /usr/local/tomcat 
# Mon, 22 Jan 2024 23:06:45 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Jan 2024 23:06:47 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 22 Jan 2024 23:06:47 GMT
EXPOSE 8080
# Mon, 22 Jan 2024 23:06:47 GMT
ENTRYPOINT []
# Mon, 22 Jan 2024 23:06:47 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e4f12b52933eaf22480862af2278c73cca667e35d95f7c2fa7d5b1e66cdc58`  
		Last Modified: Wed, 17 Jan 2024 07:19:01 GMT  
		Size: 12.9 MB (12906285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb202fd260cf6b946be6821bde7699efcb24174c9d6b0d4fcf29ee9a2d9dd86`  
		Last Modified: Wed, 17 Jan 2024 07:19:28 GMT  
		Size: 41.9 MB (41858191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced85cd837a1e5cd2d0bdcc5cf0b9b5c53aa068ecacff4fe40ce4efbbfb43b58`  
		Last Modified: Wed, 17 Jan 2024 07:19:24 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95bfcc3d8b9c5579d67347096a318ec59c1f637f4a02a8319077c4b4cc1ceb1d`  
		Last Modified: Wed, 17 Jan 2024 07:19:24 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a77671dd69f5e96e399bd077b1e5c59f72e0e9f0d9f57afcd29604c248749d`  
		Last Modified: Wed, 17 Jan 2024 11:27:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9730e5707d7341aae5c717c62432ea8de231b9c235d773cb80c9ebf7e0edd4ae`  
		Last Modified: Mon, 22 Jan 2024 23:28:48 GMT  
		Size: 12.4 MB (12403776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf0bbceeb11b6331f1cfce68817f9cd8cc23852637dc74b5ec62c13617219a8`  
		Last Modified: Mon, 22 Jan 2024 23:28:47 GMT  
		Size: 455.7 KB (455734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa23b2969ba635fbb13001839625ed1ee5ababac8ba638b9b3750b7ffdb99162`  
		Last Modified: Mon, 22 Jan 2024 23:28:47 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:b33e0f3d5e93ab28bd44d43e3000867583ec4d37a76f1343e2f06819948875e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92359879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e27fe37011ab3491e545910d5f0685440eca20300f784a61f7e5e06d411abeb`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 11 Jan 2024 17:30:37 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:30:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:30:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:30:37 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:30:39 GMT
ADD file:7c2f93ce47dedf9ba449bf11d41e9930af9fa209725f5772dc09f8c8100b5626 in / 
# Thu, 11 Jan 2024 17:30:40 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 09:39:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:39:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:39:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 09:40:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 21:10:55 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 24 Jan 2024 21:11:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='782f842c22fe660c5acbea8c1d7b4e812fe658a9e48cd2e8e776d088c7ab32d3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1d8c109e96bdb35ffff667dfb911ce03fb9f0f924048dcc8fdbd45198b263ecd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='d613a775573fc17ee972e62b5120dc34d8cac1810bb352e71bc01980ce3c48a8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='dd828b761805c2caecac94fcab8ea39cdf41480f07053553dc37edde104861af';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 24 Jan 2024 21:11:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete."
# Wed, 24 Jan 2024 21:11:38 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 21:11:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jan 2024 22:01:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 24 Jan 2024 22:01:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:01:29 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 24 Jan 2024 22:01:29 GMT
WORKDIR /usr/local/tomcat
# Wed, 24 Jan 2024 22:01:29 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 24 Jan 2024 22:01:29 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 24 Jan 2024 22:01:29 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 24 Jan 2024 22:01:29 GMT
ENV TOMCAT_MAJOR=9
# Wed, 24 Jan 2024 22:01:30 GMT
ENV TOMCAT_VERSION=9.0.85
# Wed, 24 Jan 2024 22:01:30 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Wed, 24 Jan 2024 22:01:30 GMT
COPY dir:a9808c7cf1868690030b04c4d2a9332e5af7ca71fe8ac4674c80d771bcc73f03 in /usr/local/tomcat 
# Wed, 24 Jan 2024 22:01:35 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 22:01:37 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 24 Jan 2024 22:01:37 GMT
EXPOSE 8080
# Wed, 24 Jan 2024 22:01:37 GMT
ENTRYPOINT []
# Wed, 24 Jan 2024 22:01:37 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cea537175db3d13760d71d7a8baa0a5e82491345696d2da089429926cceccffe`  
		Last Modified: Fri, 12 Jan 2024 04:33:34 GMT  
		Size: 27.5 MB (27525460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c76525c6d0fb13a7cef6ae1ed97048d26d601bc0e9c8122dd8f09146633951b`  
		Last Modified: Wed, 17 Jan 2024 09:43:20 GMT  
		Size: 12.5 MB (12495255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b28143a4eec31695cb28880577252f9362c074e9a72a2c716077fb3a59951a7`  
		Last Modified: Wed, 24 Jan 2024 21:14:57 GMT  
		Size: 39.6 MB (39571008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdf3ab189facfaf60e9088940e5160bf6c161e6fade07e3600d9397e357abbd`  
		Last Modified: Wed, 24 Jan 2024 21:14:52 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c0efdabbca683327179910bd7c39c281296971e0b15c5c7353c9916694a22a7`  
		Last Modified: Wed, 24 Jan 2024 21:14:52 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e28592da52d5963405ad7bba24fda61a3ce6d8b6427338d968401bb4473db0`  
		Last Modified: Wed, 24 Jan 2024 22:13:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559721ccfd06f9068b3ea3a032dad791cc68f27b9fbc0e205d90959bda58ca51`  
		Last Modified: Wed, 24 Jan 2024 22:13:38 GMT  
		Size: 12.3 MB (12336596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba4693022e7b503cbcd8d7b177a6de5293e887ec1ba9f0ff2126cf1fc49041f`  
		Last Modified: Wed, 24 Jan 2024 22:13:37 GMT  
		Size: 430.4 KB (430378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937721b9f3145cfc5ce385475f8627ee9a7b0e7e81b80d33db4303e78188c284`  
		Last Modified: Wed, 24 Jan 2024 22:13:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:38aa8c8f66fca441c2c4135b01430df9dd8657fb5d1e5f984de86aa04f2b290e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (94959323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5496c1821816c4697f757c1dc0ee7f6a6a46e2acf2db4374d9e0a75db684e1c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 06:57:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 06:57:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 06:57:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 06:57:53 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 06:57:53 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Wed, 17 Jan 2024 06:58:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='37b997f12cd572da979283fccafec9ba903041a209605b50fcb46cc34f1a9917';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u392b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='91d31027da0d985be3549714389593d9e0da3da5057d87e3831c7c538b9a2a0f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_x64_linux_hotspot_8u392b08.tar.gz';          ;;        armhf|arm)          ESUM='877953bfabcdbcd000c11364d806456ca579a921085de2ca942280ebe168cac2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_arm_linux_hotspot_8u392b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='0ecb0aeb54fb9d3c9e1a7ea411490127e8e298d93219fafc4dd6051a5b74671f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u392b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 17 Jan 2024 06:58:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete."
# Wed, 17 Jan 2024 06:58:12 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 17 Jan 2024 06:58:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 17 Jan 2024 14:06:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 17 Jan 2024 14:06:45 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 14:06:46 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 17 Jan 2024 14:06:46 GMT
WORKDIR /usr/local/tomcat
# Wed, 17 Jan 2024 14:06:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 17 Jan 2024 14:06:46 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 17 Jan 2024 14:06:46 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 17 Jan 2024 14:06:46 GMT
ENV TOMCAT_MAJOR=9
# Wed, 17 Jan 2024 14:06:46 GMT
ENV TOMCAT_VERSION=9.0.85
# Wed, 17 Jan 2024 14:06:46 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Mon, 22 Jan 2024 23:53:32 GMT
COPY dir:da191927260ae7b91a95335eb0e9071b05def5d9042d0e513ad0b202932ce361 in /usr/local/tomcat 
# Mon, 22 Jan 2024 23:53:35 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Jan 2024 23:53:37 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 22 Jan 2024 23:53:37 GMT
EXPOSE 8080
# Mon, 22 Jan 2024 23:53:37 GMT
ENTRYPOINT []
# Mon, 22 Jan 2024 23:53:37 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7847c91c5f9018c3a6f03ce61a2b202d22d91f08283f1981203f8dbbb742edf7`  
		Last Modified: Wed, 17 Jan 2024 07:01:02 GMT  
		Size: 12.8 MB (12849375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e04bcea3bae4c5b3400d62e7f2adb35bb590a725c3bf61547985e57dbde60f`  
		Last Modified: Wed, 17 Jan 2024 07:01:22 GMT  
		Size: 40.8 MB (40843328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdde23d7522eeb98dc99941da2a0b61585bb36ada880e4fb453fd540341de0ce`  
		Last Modified: Wed, 17 Jan 2024 07:01:18 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f79ead2b65a3e8909608b31312410526074d218456817fecc2bc571a9ab3fe`  
		Last Modified: Wed, 17 Jan 2024 07:01:18 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e051790f174b7092ac8b9f24a5977f6f71b75cf3efb9b9aa4cfc8156235cae3`  
		Last Modified: Wed, 17 Jan 2024 14:49:10 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6023e37e4d5c310d87534037e59bfdad33412e4950b74c71d69feb7d2c34648f`  
		Last Modified: Tue, 23 Jan 2024 00:12:55 GMT  
		Size: 12.4 MB (12410923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dab00e9f6362ee4a356efafd78c5ea98bf2ce0fdcda378b6eda4b5d43891d33`  
		Last Modified: Tue, 23 Jan 2024 00:12:54 GMT  
		Size: 454.9 KB (454883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b1ac395715fd5169907c830779839d148a657fc6fbc12642810ed4a32f5ae5`  
		Last Modified: Tue, 23 Jan 2024 00:12:54 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:fa9eb8e841a33559c560e77a872e5de08d44a4265c54852c692b2e8170168cbd
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103587364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9453dfb0f029dbf9e63377f674e4ee51ed4655cf099b638b61924d0e6ce43a6f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 11 Jan 2024 17:10:02 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:10:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:10:06 GMT
ADD file:4da6fb9ba29da03fa46ed73abfae01fa7c87f2c26044ee297c88359085392aef in / 
# Thu, 11 Jan 2024 17:10:06 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:29:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 07:29:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 07:29:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 07:30:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:33:48 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 24 Jan 2024 20:36:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='782f842c22fe660c5acbea8c1d7b4e812fe658a9e48cd2e8e776d088c7ab32d3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1d8c109e96bdb35ffff667dfb911ce03fb9f0f924048dcc8fdbd45198b263ecd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='d613a775573fc17ee972e62b5120dc34d8cac1810bb352e71bc01980ce3c48a8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='dd828b761805c2caecac94fcab8ea39cdf41480f07053553dc37edde104861af';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 24 Jan 2024 20:36:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete."
# Wed, 24 Jan 2024 20:36:26 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:36:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jan 2024 22:24:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 24 Jan 2024 22:25:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:25:01 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 24 Jan 2024 22:25:02 GMT
WORKDIR /usr/local/tomcat
# Wed, 24 Jan 2024 22:25:02 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 24 Jan 2024 22:25:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 24 Jan 2024 22:25:03 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 24 Jan 2024 22:25:03 GMT
ENV TOMCAT_MAJOR=9
# Wed, 24 Jan 2024 22:25:04 GMT
ENV TOMCAT_VERSION=9.0.85
# Wed, 24 Jan 2024 22:25:04 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Wed, 24 Jan 2024 22:25:05 GMT
COPY dir:8d0088604c980287d68c511930e9c881df621f643a90f3a4ce6117ef0be59627 in /usr/local/tomcat 
# Wed, 24 Jan 2024 22:25:13 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 22:25:15 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 24 Jan 2024 22:25:15 GMT
EXPOSE 8080
# Wed, 24 Jan 2024 22:25:16 GMT
ENTRYPOINT []
# Wed, 24 Jan 2024 22:25:17 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:898e4a5fe680690395e7fd9d920dfa248b7508ec0573741c491bf250179ddbda`  
		Last Modified: Wed, 17 Jan 2024 05:26:53 GMT  
		Size: 35.7 MB (35657152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f85bd9b095b5879a3465b7ad0b393d5c09a45f44fa356c1d64ce36e5c6517e`  
		Last Modified: Wed, 17 Jan 2024 07:36:37 GMT  
		Size: 13.8 MB (13769329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e93f1c25952a8f90b56e60ecd19db13e898f75478a31f8a418ccbc089860f4`  
		Last Modified: Wed, 24 Jan 2024 20:49:15 GMT  
		Size: 41.2 MB (41241321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612649d5228a84e31c8498d8dc3b349cf781f264c25e82f0b64d2513d05ce028`  
		Last Modified: Wed, 24 Jan 2024 20:49:10 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74282da48f20875de2869ffbed7c9abc9898e332b331f604cd3c8c7a8b05869c`  
		Last Modified: Wed, 24 Jan 2024 20:49:10 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8621aa4c05d230edc119de027fd81ba59c7ce75ead57a0cc198a61df50c8e926`  
		Last Modified: Wed, 24 Jan 2024 22:53:30 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b47988ce992689760972f0fe69f3e2a6bf3d89364492d76c6e633c7f9940ea4`  
		Last Modified: Wed, 24 Jan 2024 22:53:32 GMT  
		Size: 12.4 MB (12431327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c05f28972a45d27c58c181247b4cd985acb099fb01285af4ef73db0cc7e122f`  
		Last Modified: Wed, 24 Jan 2024 22:53:31 GMT  
		Size: 487.1 KB (487053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b6f51c9bc09c407e3806e79469ab4a506b34061664a7e64d5de37dcabe9400`  
		Last Modified: Wed, 24 Jan 2024 22:53:30 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
