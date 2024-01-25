## `tomcat:8-jre8-temurin-focal`

```console
$ docker pull tomcat@sha256:ee02543796d788d2da27195c4448028e24ba99afcd6b0ab6dd375e4594858713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `tomcat:8-jre8-temurin-focal` - linux; amd64

```console
$ docker pull tomcat@sha256:533ea74f44528c6f67ec8a733609b63bd182354e8e56e130c63cb21255b172af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.3 MB (99327263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090ae49b7cc3f5dce1c697d704b9230426a9eb82ee0c3e757fa79cb8a7e990cb`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:15:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:15:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:15:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:16:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:16:01 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Sat, 16 Dec 2023 10:16:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='37b997f12cd572da979283fccafec9ba903041a209605b50fcb46cc34f1a9917';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u392b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='91d31027da0d985be3549714389593d9e0da3da5057d87e3831c7c538b9a2a0f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_x64_linux_hotspot_8u392b08.tar.gz';          ;;        armhf|arm)          ESUM='877953bfabcdbcd000c11364d806456ca579a921085de2ca942280ebe168cac2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_arm_linux_hotspot_8u392b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='0ecb0aeb54fb9d3c9e1a7ea411490127e8e298d93219fafc4dd6051a5b74671f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u392b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Sat, 16 Dec 2023 10:16:53 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete."
# Sat, 16 Dec 2023 10:16:53 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:16:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 16:14:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 16 Dec 2023 16:14:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 16:14:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 16 Dec 2023 16:14:04 GMT
WORKDIR /usr/local/tomcat
# Sat, 16 Dec 2023 16:14:04 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 16 Dec 2023 16:14:04 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 16 Dec 2023 16:20:14 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Sat, 16 Dec 2023 16:20:14 GMT
ENV TOMCAT_MAJOR=8
# Tue, 09 Jan 2024 22:51:25 GMT
ENV TOMCAT_VERSION=8.5.98
# Tue, 09 Jan 2024 22:51:25 GMT
ENV TOMCAT_SHA512=12f58114fe608fdc5f06e99a4ba01852396169f89d08e1ecf96ace36dd685c439519433e7750bfa7523f12c14788a3b5cb9ee3835dd1cce37e2cee121d69625e
# Mon, 22 Jan 2024 23:16:52 GMT
COPY dir:919ae2b416b99b23dc18d3a480dff1169686468d820ac162d44573cccb745b30 in /usr/local/tomcat 
# Mon, 22 Jan 2024 23:16:57 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Jan 2024 23:16:58 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 22 Jan 2024 23:16:58 GMT
EXPOSE 8080
# Mon, 22 Jan 2024 23:16:58 GMT
ENTRYPOINT []
# Mon, 22 Jan 2024 23:16:58 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6a6404648d953a02729d22ecf5aa18fe7f6f8d40e669ba5c45fbe6db2cd987`  
		Last Modified: Sat, 16 Dec 2023 10:21:04 GMT  
		Size: 16.9 MB (16920196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95db54bbfb1c4da53d7f38a3c24266b33c51646f8baccf5f4c51d8f64b970aa9`  
		Last Modified: Sat, 16 Dec 2023 10:21:45 GMT  
		Size: 41.9 MB (41859101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c45db749066405eeb1cb1d1eeb82d91b8b28c6b7ba4ddec56a106cee4bb029`  
		Last Modified: Sat, 16 Dec 2023 10:21:40 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b91741e5492cdc4c55643015e5b77a596c4c2813ad271ac37df09d5d14fa63`  
		Last Modified: Sat, 16 Dec 2023 10:21:40 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb66b96ef51ff0d9896fef00f696a05abe0db64ab85feae27a4b311b9aaf576`  
		Last Modified: Sat, 16 Dec 2023 16:30:52 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25806204000284848a3331d76110a1412e89edf0d9eda26aca49c17fa6d425b8`  
		Last Modified: Mon, 22 Jan 2024 23:35:02 GMT  
		Size: 11.5 MB (11513002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3336af5cfc7228db2aa4ce9c43fbf4e31b47756c66ef575c1f6b419f2e06be0`  
		Last Modified: Mon, 22 Jan 2024 23:35:01 GMT  
		Size: 449.7 KB (449743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d2cd8bcd73056f08c17f4dbecd9f1c67eab86583eb2f7c2177d92312283607`  
		Last Modified: Mon, 22 Jan 2024 23:35:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-temurin-focal` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:7f0a18515eaef17aade6f3a7279df6584bc6b3301fc92fbfda8b9627bf29dbe8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91721067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7df5aae3656584eabc7331a01c603cf1009c7069cf56570f7fd00bc212dc626`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 13 Dec 2023 10:37:05 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:37:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:37:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:37:06 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:37:14 GMT
ADD file:195375389d64193c828c6d3f379c7e35ea85256eb1c51d2bfeab73432ea46064 in / 
# Wed, 13 Dec 2023 10:37:15 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:29:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 09:29:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 09:29:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 09:30:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 21:10:31 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 24 Jan 2024 21:11:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='782f842c22fe660c5acbea8c1d7b4e812fe658a9e48cd2e8e776d088c7ab32d3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1d8c109e96bdb35ffff667dfb911ce03fb9f0f924048dcc8fdbd45198b263ecd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='d613a775573fc17ee972e62b5120dc34d8cac1810bb352e71bc01980ce3c48a8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='dd828b761805c2caecac94fcab8ea39cdf41480f07053553dc37edde104861af';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 24 Jan 2024 21:11:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete."
# Wed, 24 Jan 2024 21:11:27 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 21:11:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jan 2024 22:02:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 24 Jan 2024 22:02:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:02:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 24 Jan 2024 22:02:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 24 Jan 2024 22:02:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 24 Jan 2024 22:02:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 24 Jan 2024 22:07:22 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 24 Jan 2024 22:07:22 GMT
ENV TOMCAT_MAJOR=8
# Wed, 24 Jan 2024 22:07:23 GMT
ENV TOMCAT_VERSION=8.5.98
# Wed, 24 Jan 2024 22:07:23 GMT
ENV TOMCAT_SHA512=12f58114fe608fdc5f06e99a4ba01852396169f89d08e1ecf96ace36dd685c439519433e7750bfa7523f12c14788a3b5cb9ee3835dd1cce37e2cee121d69625e
# Wed, 24 Jan 2024 22:07:23 GMT
COPY dir:1fe001244d25f2fb869a3d9e3e8c1cbf141f2bec51d7efa40d8d57afcd885257 in /usr/local/tomcat 
# Wed, 24 Jan 2024 22:07:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 22:07:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 24 Jan 2024 22:07:29 GMT
EXPOSE 8080
# Wed, 24 Jan 2024 22:07:29 GMT
ENTRYPOINT []
# Wed, 24 Jan 2024 22:07:29 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ba68304511cfd178c72d64196a05b1343fbdbed6093d7b4db0c0d223510c40ab`  
		Last Modified: Sat, 16 Dec 2023 09:27:50 GMT  
		Size: 24.6 MB (24600972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45dca1c5123b34dd759063c3ea5a85792ef1b887f6337f3fc1bf67a9a3971c6e`  
		Last Modified: Sat, 16 Dec 2023 09:33:39 GMT  
		Size: 15.7 MB (15659547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad808aa3f915a961497887ede24de244aba0e81e0c3f735177c76080c86a2c82`  
		Last Modified: Wed, 24 Jan 2024 21:14:42 GMT  
		Size: 39.6 MB (39570611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241e08f3fe0956c2bb2f7c690e43c4fdb5cf248bc04f826ce8e0f724da4b1cf7`  
		Last Modified: Wed, 24 Jan 2024 21:14:37 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ee09523fb694c914760be81dad1cb8d8fd8f830335b0289107e06ccf62ae2e`  
		Last Modified: Wed, 24 Jan 2024 21:14:37 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddf9e1df1f1762ebf1417659999e718716bf294e5d0051eaba7dbf443416514`  
		Last Modified: Wed, 24 Jan 2024 22:14:17 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ff54689413b1bacf8362cd7995570e019af0eaaeea5e95c2533076c6309f4f`  
		Last Modified: Wed, 24 Jan 2024 22:17:52 GMT  
		Size: 11.5 MB (11462429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed4fbe3ebaef81e07a6de3a00611dd25d6e431800b62a4d36e26279b0496e7b`  
		Last Modified: Wed, 24 Jan 2024 22:17:51 GMT  
		Size: 426.3 KB (426328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17fd214d5ba8f12f59c990a87d3e1f03b93c3485b9fee56a5170d18c633ba12`  
		Last Modified: Wed, 24 Jan 2024 22:17:51 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-temurin-focal` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:b66693dc6c737d8de1d360a68343387c68ba4a18ff6d20cbe20e755d876a4ab3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96797396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fa42d817b23acafd10e1fbf4c3b0feb6d3b61cee1f57ef9f72e57f1696e038`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:02:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:02:15 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Sat, 16 Dec 2023 10:02:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='37b997f12cd572da979283fccafec9ba903041a209605b50fcb46cc34f1a9917';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u392b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='91d31027da0d985be3549714389593d9e0da3da5057d87e3831c7c538b9a2a0f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_x64_linux_hotspot_8u392b08.tar.gz';          ;;        armhf|arm)          ESUM='877953bfabcdbcd000c11364d806456ca579a921085de2ca942280ebe168cac2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_arm_linux_hotspot_8u392b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='0ecb0aeb54fb9d3c9e1a7ea411490127e8e298d93219fafc4dd6051a5b74671f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u392b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Sat, 16 Dec 2023 10:02:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete."
# Sat, 16 Dec 2023 10:02:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:02:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 15:03:47 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 16 Dec 2023 15:03:47 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 15:03:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 16 Dec 2023 15:03:47 GMT
WORKDIR /usr/local/tomcat
# Sat, 16 Dec 2023 15:03:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 16 Dec 2023 15:03:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 16 Dec 2023 15:08:48 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Sat, 16 Dec 2023 15:08:48 GMT
ENV TOMCAT_MAJOR=8
# Tue, 09 Jan 2024 23:15:14 GMT
ENV TOMCAT_VERSION=8.5.98
# Tue, 09 Jan 2024 23:15:14 GMT
ENV TOMCAT_SHA512=12f58114fe608fdc5f06e99a4ba01852396169f89d08e1ecf96ace36dd685c439519433e7750bfa7523f12c14788a3b5cb9ee3835dd1cce37e2cee121d69625e
# Tue, 23 Jan 2024 00:01:28 GMT
COPY dir:bdb492cd8b2b9e97de028ccdd72871821369206a55f342499f10832f58f05be3 in /usr/local/tomcat 
# Tue, 23 Jan 2024 00:01:31 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jan 2024 00:01:32 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 23 Jan 2024 00:01:32 GMT
EXPOSE 8080
# Tue, 23 Jan 2024 00:01:32 GMT
ENTRYPOINT []
# Tue, 23 Jan 2024 00:01:32 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69f35fd155c9c0a485e63ad002a7b98a6ce1921e230d386f1cffd2c8c16878`  
		Last Modified: Sat, 16 Dec 2023 10:06:15 GMT  
		Size: 16.8 MB (16769031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972efbb5355605bd1c767d5dcde6521e9f4a65d5fc131991fc3fc2765f5b296c`  
		Last Modified: Sat, 16 Dec 2023 10:06:53 GMT  
		Size: 40.8 MB (40843989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65564342016555a11d4fe73450771971acc24e7f4cead917494041cea128a870`  
		Last Modified: Sat, 16 Dec 2023 10:06:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293ddc00a8b82e80cd076cb453963214d1bcf167354d57d4cb26fc4a0f64335a`  
		Last Modified: Sat, 16 Dec 2023 10:06:49 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cedfa21c94016c972db928bc6e1f4c1e41b1f10aadc662dd8334567b92d6d6`  
		Last Modified: Sat, 16 Dec 2023 15:19:14 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f504336b486df5627bfb48b7422d79e3cb3f92bb9ff8cd23990188cd58e72f07`  
		Last Modified: Tue, 23 Jan 2024 00:19:01 GMT  
		Size: 11.5 MB (11530830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4042cb9eb04a48e0c3433ceaefe13cdf9579918aee8f5007beb4f6542b20295`  
		Last Modified: Tue, 23 Jan 2024 00:19:00 GMT  
		Size: 449.2 KB (449205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9f1430445198979c5642d20d4892748611aadf8ed65e407ed6d44f38066b67`  
		Last Modified: Tue, 23 Jan 2024 00:19:00 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-temurin-focal` - linux; ppc64le

```console
$ docker pull tomcat@sha256:2f3fcc7dfecbf93268cccb4645f711b37f68c8e500062b39d8598c17dc7255f6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104804509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2955bb7413db62f424722c41a2ed71730c1c97a4727c12074a2af8209c73a8a6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 13 Dec 2023 10:36:32 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:36:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:36:35 GMT
ADD file:b7dcee8fbada51f19b857a4a8ef334aab211090abf4247194ddfeb1504df7420 in / 
# Wed, 13 Dec 2023 10:36:35 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:36:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:36:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:36:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:37:10 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:33:27 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 24 Jan 2024 20:36:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='782f842c22fe660c5acbea8c1d7b4e812fe658a9e48cd2e8e776d088c7ab32d3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1d8c109e96bdb35ffff667dfb911ce03fb9f0f924048dcc8fdbd45198b263ecd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='d613a775573fc17ee972e62b5120dc34d8cac1810bb352e71bc01980ce3c48a8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='dd828b761805c2caecac94fcab8ea39cdf41480f07053553dc37edde104861af';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 24 Jan 2024 20:36:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete."
# Wed, 24 Jan 2024 20:36:13 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:36:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jan 2024 22:26:50 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 24 Jan 2024 22:26:51 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:26:53 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 24 Jan 2024 22:26:54 GMT
WORKDIR /usr/local/tomcat
# Wed, 24 Jan 2024 22:26:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 24 Jan 2024 22:26:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 24 Jan 2024 22:41:44 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 24 Jan 2024 22:41:44 GMT
ENV TOMCAT_MAJOR=8
# Wed, 24 Jan 2024 22:41:45 GMT
ENV TOMCAT_VERSION=8.5.98
# Wed, 24 Jan 2024 22:41:45 GMT
ENV TOMCAT_SHA512=12f58114fe608fdc5f06e99a4ba01852396169f89d08e1ecf96ace36dd685c439519433e7750bfa7523f12c14788a3b5cb9ee3835dd1cce37e2cee121d69625e
# Wed, 24 Jan 2024 22:41:46 GMT
COPY dir:1e96d004613978f701ebf446c7bc6b9ad0504ef04167a41559184002390e78e0 in /usr/local/tomcat 
# Wed, 24 Jan 2024 22:41:54 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 22:41:57 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 24 Jan 2024 22:41:57 GMT
EXPOSE 8080
# Wed, 24 Jan 2024 22:41:58 GMT
ENTRYPOINT []
# Wed, 24 Jan 2024 22:41:58 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3cdeaacd390f730da6f0fb692f91fa6acafd7c373cd75524447a25371b6cf3b5`  
		Last Modified: Sat, 16 Dec 2023 10:34:06 GMT  
		Size: 33.3 MB (33314320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed67c1e92d231797f6ccdb5b8dfc66523da0505bda01ed804febc7f69bbc165`  
		Last Modified: Sat, 16 Dec 2023 10:43:55 GMT  
		Size: 18.2 MB (18215112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ce92a1258a56d95a3670e5b57114f5e31bf852d1aeb8c6caa449070686f5a0`  
		Last Modified: Wed, 24 Jan 2024 20:49:00 GMT  
		Size: 41.2 MB (41242134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96599886f67217181bd3b5edb9d1416e3801441e8d626f8151af82bbec1ec905`  
		Last Modified: Wed, 24 Jan 2024 20:48:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d025e9bf4db25ebccadb1ce8d6156dac7e5b17e5fe2ef55600818e749f7d9e43`  
		Last Modified: Wed, 24 Jan 2024 20:48:55 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6837a15828a4f95c8667f953cee65af51f41f9a983fea47e8908bc6405ff25c3`  
		Last Modified: Wed, 24 Jan 2024 22:54:14 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68838e0882e990671979d0e82609a993c50b2ed5b3fa7b7ab6bc1e7b5733822f`  
		Last Modified: Wed, 24 Jan 2024 22:59:23 GMT  
		Size: 11.6 MB (11556569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ba686f76e13ebdf5ecb09f9c1db41ab986e0d9ee6ca8e9a2547c85c032ed50`  
		Last Modified: Wed, 24 Jan 2024 22:59:22 GMT  
		Size: 475.2 KB (475195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938b0059db23c37e250b43b44a4315830d30a692a07215ef733671dcba61f87d`  
		Last Modified: Wed, 24 Jan 2024 22:59:22 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
