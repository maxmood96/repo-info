## `tomcat:8-jre8`

```console
$ docker pull tomcat@sha256:c66e834f87a588d6d790ff623a0091afa8ef11e64c11024184274344b5bda76c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `tomcat:8-jre8` - linux; amd64

```console
$ docker pull tomcat@sha256:e57e7c6f7416204fee059c9170b31af1c70b5c3cf73aa90fe0736262a114b2c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97116162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f7bbfb842161c6f1f4c267b23b15a932a58455b5adb43ddc84bafce06d76e4`
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
# Wed, 17 Jan 2024 10:46:45 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 17 Jan 2024 10:46:45 GMT
ENV TOMCAT_MAJOR=8
# Wed, 17 Jan 2024 10:46:45 GMT
ENV TOMCAT_VERSION=8.5.98
# Wed, 17 Jan 2024 10:46:45 GMT
ENV TOMCAT_SHA512=12f58114fe608fdc5f06e99a4ba01852396169f89d08e1ecf96ace36dd685c439519433e7750bfa7523f12c14788a3b5cb9ee3835dd1cce37e2cee121d69625e
# Mon, 22 Jan 2024 23:16:00 GMT
COPY dir:367ac9ec8d367ef8d49cffcaf630215e05ea983d7b5a4d34b4ba43fd8addbf98 in /usr/local/tomcat 
# Mon, 22 Jan 2024 23:16:05 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Jan 2024 23:16:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 22 Jan 2024 23:16:06 GMT
EXPOSE 8080
# Mon, 22 Jan 2024 23:16:06 GMT
ENTRYPOINT []
# Mon, 22 Jan 2024 23:16:06 GMT
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
	-	`sha256:19d3eb5d1aa9c775fbec6f27efc317f70005e05275986575cc16649006a7cad5`  
		Last Modified: Mon, 22 Jan 2024 23:34:24 GMT  
		Size: 11.4 MB (11447639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cea789b59406e2cf084f1c3baf9e19f73d2cdb7f25f284626a0aa4f4f85cbcb`  
		Last Modified: Mon, 22 Jan 2024 23:34:23 GMT  
		Size: 455.7 KB (455736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe2eb0952cde1dcead6eec9e4cc61fb398cb9bb7616842ddbea82c9f13ca1c9`  
		Last Modified: Mon, 22 Jan 2024 23:34:23 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:f5c640cafbaac3a0a84e0eb81d5de30064d27eb289f107ad2caadddf2071d529
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91404362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76732eb3ee895de3fb6186b30f4515d32d1af1805b6f9b0c74483816a8acee2`
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
# Wed, 24 Jan 2024 22:06:32 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 24 Jan 2024 22:06:33 GMT
ENV TOMCAT_MAJOR=8
# Wed, 24 Jan 2024 22:06:33 GMT
ENV TOMCAT_VERSION=8.5.98
# Wed, 24 Jan 2024 22:06:33 GMT
ENV TOMCAT_SHA512=12f58114fe608fdc5f06e99a4ba01852396169f89d08e1ecf96ace36dd685c439519433e7750bfa7523f12c14788a3b5cb9ee3835dd1cce37e2cee121d69625e
# Wed, 24 Jan 2024 22:06:33 GMT
COPY dir:95e98b9b0617e04c44287c1a4ed1b11c2731c4d77e8a99689e8249fb3ffb7bc4 in /usr/local/tomcat 
# Wed, 24 Jan 2024 22:06:38 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 22:06:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 24 Jan 2024 22:06:39 GMT
EXPOSE 8080
# Wed, 24 Jan 2024 22:06:39 GMT
ENTRYPOINT []
# Wed, 24 Jan 2024 22:06:39 GMT
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
	-	`sha256:c14c5090b8eb988cc2e2cab5dc58d05d2b819cd1a2fe46af6bbcc77e580c761f`  
		Last Modified: Wed, 24 Jan 2024 22:17:16 GMT  
		Size: 11.4 MB (11381084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5677931382f0b934c2b94e25a244b16587d933b646282cfe3ea9f03b8f18a7`  
		Last Modified: Wed, 24 Jan 2024 22:17:15 GMT  
		Size: 430.4 KB (430375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1c958ada6d7e96a62feb35e08779e322ae0c97ebd4c4623bc390037ec84f6a`  
		Last Modified: Wed, 24 Jan 2024 22:17:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:d3693e2addde0823602a041fadd611988dc646348d35af113253c735d473378e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94003355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76596c3eb5d5f94fe5bd3a1daef4e5f45639128e3a878a025e2395377ea4a229`
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
# Wed, 17 Jan 2024 14:09:48 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 17 Jan 2024 14:09:48 GMT
ENV TOMCAT_MAJOR=8
# Wed, 17 Jan 2024 14:09:48 GMT
ENV TOMCAT_VERSION=8.5.98
# Wed, 17 Jan 2024 14:09:48 GMT
ENV TOMCAT_SHA512=12f58114fe608fdc5f06e99a4ba01852396169f89d08e1ecf96ace36dd685c439519433e7750bfa7523f12c14788a3b5cb9ee3835dd1cce37e2cee121d69625e
# Tue, 23 Jan 2024 00:00:48 GMT
COPY dir:e24c5f76cb38feaafdf2931acf0e34dd77912ca8dd65f679d0bfca299e7a3b10 in /usr/local/tomcat 
# Tue, 23 Jan 2024 00:00:51 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jan 2024 00:00:52 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 23 Jan 2024 00:00:52 GMT
EXPOSE 8080
# Tue, 23 Jan 2024 00:00:52 GMT
ENTRYPOINT []
# Tue, 23 Jan 2024 00:00:52 GMT
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
	-	`sha256:4937c1f63f7eb92a308aa0311dbdeffc161430dd38c409969e6fba7bbbde00f6`  
		Last Modified: Tue, 23 Jan 2024 00:18:26 GMT  
		Size: 11.5 MB (11454951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65304a4ffe4820219d241b186ba940d9a304f55ecfee646357d33669873baaff`  
		Last Modified: Tue, 23 Jan 2024 00:18:25 GMT  
		Size: 454.9 KB (454890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2a8acd94c0835962386c9aba3fbf0840c30f0de27a7d9544bb8774196d49f0`  
		Last Modified: Tue, 23 Jan 2024 00:18:25 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8` - linux; ppc64le

```console
$ docker pull tomcat@sha256:498a8e31ee56b2c009bb6d6a29fa36cf87ae833d0f9702d2269199f895a8c56a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102632163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41705957822e25f876325eb1d69a9e41208847f644a0472144c0d81ed3627fdf`
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
# Wed, 24 Jan 2024 22:40:00 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 24 Jan 2024 22:40:01 GMT
ENV TOMCAT_MAJOR=8
# Wed, 24 Jan 2024 22:40:01 GMT
ENV TOMCAT_VERSION=8.5.98
# Wed, 24 Jan 2024 22:40:01 GMT
ENV TOMCAT_SHA512=12f58114fe608fdc5f06e99a4ba01852396169f89d08e1ecf96ace36dd685c439519433e7750bfa7523f12c14788a3b5cb9ee3835dd1cce37e2cee121d69625e
# Wed, 24 Jan 2024 22:40:02 GMT
COPY dir:471bf3141983cc07fda361f4d03f9228d83819af23f8a705ee0da708f1444ac8 in /usr/local/tomcat 
# Wed, 24 Jan 2024 22:40:09 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 22:40:12 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 24 Jan 2024 22:40:12 GMT
EXPOSE 8080
# Wed, 24 Jan 2024 22:40:12 GMT
ENTRYPOINT []
# Wed, 24 Jan 2024 22:40:13 GMT
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
	-	`sha256:c2266806d399efbd0faf17aac0ffb9aa9b912714f569bcee90ff53ee7c9fad93`  
		Last Modified: Wed, 24 Jan 2024 22:58:42 GMT  
		Size: 11.5 MB (11476118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9876c69e999553ccd4a1524bfae082c808056d46c3032b5d923365f3a677d98`  
		Last Modified: Wed, 24 Jan 2024 22:58:41 GMT  
		Size: 487.1 KB (487063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7e471ccc2152459c7a3192bd9247c9e4d5c90f104fa7d630d00b5429d1605c`  
		Last Modified: Wed, 24 Jan 2024 22:58:40 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
