## `tomcat:8-jre8-temurin`

```console
$ docker pull tomcat@sha256:8a9da1aeefc4e3c9a6163f39265c353f63fe17b9eb2ef3ce239fff6744feaceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `tomcat:8-jre8-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:4a085d6d67dd527f3d036a773e601413b6b461581d44dd8b9fde7cebe631ab11
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96340248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86f856d0885d4c1451836639dca3d0b5108f2efa9eb43e99deecccc0ca9def8`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 18:44:11 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Wed, 02 Nov 2022 18:44:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='65b8bd74382d6514d2458ff4375468651791a55a186a5bffe0803204801e9c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_aarch64_linux_hotspot_8u345b01.tar.gz';          ;;        armhf|arm)          ESUM='a9dd1ea4280a85158191101688bbf1920c4676a3849e22dc7783fb61f60d6199';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_arm_linux_hotspot_8u345b01.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='0e58c3fb39303969d7d6ff660c0b63997ab0ee68af3452f3d17f2892c61a58f6';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_ppc64le_linux_hotspot_8u345b01.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='2422a8831fe414b9dba4c443ee3562431dfcde27577124f0db58ec903afc262a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jre_x64_linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Wed, 02 Nov 2022 18:44:35 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 02 Nov 2022 21:36:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 02 Nov 2022 21:36:24 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 21:36:25 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 02 Nov 2022 21:36:25 GMT
WORKDIR /usr/local/tomcat
# Wed, 02 Nov 2022 21:36:25 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 02 Nov 2022 21:36:25 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 02 Nov 2022 21:41:50 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 02 Nov 2022 21:41:50 GMT
ENV TOMCAT_MAJOR=8
# Wed, 02 Nov 2022 21:41:50 GMT
ENV TOMCAT_VERSION=8.5.83
# Wed, 02 Nov 2022 21:41:50 GMT
ENV TOMCAT_SHA512=57cbe9608a9c4e88135e5f5480812e8d57690d5f3f6c43a7c05fe647bddb7c3b684bf0fc0efebad399d05e80c6d20c43d5ecdf38ec58f123e6653e443f9054e3
# Wed, 02 Nov 2022 21:41:50 GMT
COPY dir:a5a8d7bc3935693fb8f740c2e6c10693135049c4761e73301f945a0f26d3d655 in /usr/local/tomcat 
# Wed, 02 Nov 2022 21:41:54 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 21:41:55 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 02 Nov 2022 21:41:56 GMT
EXPOSE 8080
# Wed, 02 Nov 2022 21:41:56 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f6cffbfdc2d641772a8c4f5a5fced2035f06961b7cad3dd7730f7ae46646c4`  
		Last Modified: Wed, 02 Nov 2022 18:49:11 GMT  
		Size: 41.8 MB (41807960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4537b44552d4a025e814d7b3a2f3705de8e9b440b75f1f323049eb7dc4b65d`  
		Last Modified: Wed, 02 Nov 2022 18:49:06 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ea0c1080d375a7798ef4884e1bb3e495e7b601896f9f2cdaf96f542cb2537d`  
		Last Modified: Wed, 02 Nov 2022 21:50:46 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0bd5f4162116c701bfe1b14c698ddc235dc8897dd1feb1dd0dcb647902aa063`  
		Last Modified: Wed, 02 Nov 2022 21:57:13 GMT  
		Size: 11.2 MB (11214557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f76a71503de6d1d592715a4531a9d4e45c3bd0ce987bd4b2cd2bdb3644f6df`  
		Last Modified: Wed, 02 Nov 2022 21:57:12 GMT  
		Size: 452.7 KB (452656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d6e790f7a734962fb7056d236942313726c017cbb31c1c737a175afb4024d3`  
		Last Modified: Wed, 02 Nov 2022 21:57:12 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:bc0747f51a714dd8cf19f73f3228ff27a17243e0bf630495f789f5accce1f45a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90151678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f9a4ca17ba7db93b977e5196c08d1058b856d867405043d151b9ccb00770c6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 02 Nov 2022 17:58:54 GMT
ADD file:3acaa98e676fc52121edd2feea0fc71a60614dbf081f3db61809aab25af42a8c in / 
# Wed, 02 Nov 2022 17:58:54 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:35:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:35:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:35:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:35:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:58:15 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 22:59:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 22:59:08 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 04 Nov 2022 23:33:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Nov 2022 23:33:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Nov 2022 23:33:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 04 Nov 2022 23:33:41 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Nov 2022 23:33:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Nov 2022 23:33:41 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Nov 2022 23:42:46 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 04 Nov 2022 23:42:46 GMT
ENV TOMCAT_MAJOR=8
# Fri, 04 Nov 2022 23:42:46 GMT
ENV TOMCAT_VERSION=8.5.83
# Fri, 04 Nov 2022 23:42:46 GMT
ENV TOMCAT_SHA512=57cbe9608a9c4e88135e5f5480812e8d57690d5f3f6c43a7c05fe647bddb7c3b684bf0fc0efebad399d05e80c6d20c43d5ecdf38ec58f123e6653e443f9054e3
# Fri, 04 Nov 2022 23:42:47 GMT
COPY dir:b645cda3ab3d875c0debe71e4d3ec07f566fd09bdfec0b69a7dea133dcded2e4 in /usr/local/tomcat 
# Fri, 04 Nov 2022 23:42:51 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:42:52 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 04 Nov 2022 23:42:53 GMT
EXPOSE 8080
# Fri, 04 Nov 2022 23:42:53 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c3a947801223d5dd57236bed8663245ffddcbb4700ba3aec7edc7865fd8cd9d7`  
		Last Modified: Wed, 02 Nov 2022 18:00:26 GMT  
		Size: 27.0 MB (27020159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0829db637b9792b59814837768853e2024fa2d0f3ed5e36053294ccab7a0dd6`  
		Last Modified: Wed, 02 Nov 2022 18:45:01 GMT  
		Size: 12.0 MB (12012626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:064e271d2360704d4839e1b892ac7121bfd35579980379557f6eb248fceb3346`  
		Last Modified: Fri, 04 Nov 2022 23:05:03 GMT  
		Size: 39.5 MB (39542760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433df5ff31ea4843c8939a0e9745c6af9c11ada0eece853f2912545e4e627b04`  
		Last Modified: Fri, 04 Nov 2022 23:04:56 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed1d60f5512cafe30e89635a6f203fa90662dd9234e0c02188026f149525f8f`  
		Last Modified: Fri, 04 Nov 2022 23:58:32 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140cfbfd1a6477637bcd26bd8c1ff95b6499b0527f8b582be350f67ebbb7d5df`  
		Last Modified: Sat, 05 Nov 2022 00:06:44 GMT  
		Size: 11.1 MB (11148651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a2a0553ef7cba1ee7326931d560af5a9c490dc4af3b1242c6589e446208dd0`  
		Last Modified: Sat, 05 Nov 2022 00:06:43 GMT  
		Size: 427.1 KB (427087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7405a380e9012705cc38c7719136cc5b8e157ec285868d543eee420f78b78f8f`  
		Last Modified: Sat, 05 Nov 2022 00:06:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:15f74747dbe0a546d8d79256e05e387513dc9edf01ff8a2d011c4efeb48e2826
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93260710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcabf85436c2fcb88f2b5b65c4d02cda6098266ae17277b2725bd36969e662e8`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:39:49 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 22:40:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 22:40:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 04 Nov 2022 23:51:43 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Nov 2022 23:51:43 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Nov 2022 23:51:43 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 04 Nov 2022 23:51:44 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Nov 2022 23:51:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Nov 2022 23:51:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Nov 2022 23:57:34 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 04 Nov 2022 23:57:34 GMT
ENV TOMCAT_MAJOR=8
# Fri, 04 Nov 2022 23:57:34 GMT
ENV TOMCAT_VERSION=8.5.83
# Fri, 04 Nov 2022 23:57:34 GMT
ENV TOMCAT_SHA512=57cbe9608a9c4e88135e5f5480812e8d57690d5f3f6c43a7c05fe647bddb7c3b684bf0fc0efebad399d05e80c6d20c43d5ecdf38ec58f123e6653e443f9054e3
# Fri, 04 Nov 2022 23:57:35 GMT
COPY dir:d92f27c831d9585d25c6d8d0085e329f9c90251aa0e27301ca7160bfd41db101 in /usr/local/tomcat 
# Fri, 04 Nov 2022 23:57:38 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:57:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 04 Nov 2022 23:57:39 GMT
EXPOSE 8080
# Fri, 04 Nov 2022 23:57:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd66203f631549955cf8c4f71f60bc148efa34d467138bc7406e9b20cfd155c1`  
		Last Modified: Fri, 04 Nov 2022 22:44:50 GMT  
		Size: 40.8 MB (40807347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14c8761d4b12ec391f3de7086ce2d5554b3a25b4073842d4d4c2b52f617a52d`  
		Last Modified: Fri, 04 Nov 2022 22:44:46 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e28fdabedd020cfc0b3b9e48fcddb3e82d68fc443da502f2598b296aa9a8b0`  
		Last Modified: Sat, 05 Nov 2022 00:05:57 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485ce1fcf59fec494e17304572f9a6383c8910d2f40e6322fd9f1095b7a5f72b`  
		Last Modified: Sat, 05 Nov 2022 00:12:11 GMT  
		Size: 11.2 MB (11222416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf9ffb9e64f84207b505adcd11a1fb9b358ccff7749eb90d200e5e42c355dd0`  
		Last Modified: Sat, 05 Nov 2022 00:12:11 GMT  
		Size: 452.0 KB (452002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65da4e695be2664d065ca5f4fe08a03a46a7bb060ad8dbf99cc0a13f5a0b037a`  
		Last Modified: Sat, 05 Nov 2022 00:12:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:8de298502d092924e6e601bff44d67820456109fad542ef705004075fce5d2f1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101915130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19fe426bbcda9913128adc55a84a916a5f8fb7add160a46f581652bc87ccfc0f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 02 Nov 2022 18:17:30 GMT
ADD file:e50d53011f99a82c70508eaba072b194b6498693db105f1b1e78adb85ea2f07a in / 
# Wed, 02 Nov 2022 18:17:33 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:55:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:55:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:55:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:56:04 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:17:18 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:18:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:18:26 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 05 Nov 2022 00:18:11 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 05 Nov 2022 00:18:12 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:18:13 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 05 Nov 2022 00:18:13 GMT
WORKDIR /usr/local/tomcat
# Sat, 05 Nov 2022 00:18:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 05 Nov 2022 00:18:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 05 Nov 2022 00:32:12 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Sat, 05 Nov 2022 00:32:13 GMT
ENV TOMCAT_MAJOR=8
# Sat, 05 Nov 2022 00:32:13 GMT
ENV TOMCAT_VERSION=8.5.83
# Sat, 05 Nov 2022 00:32:14 GMT
ENV TOMCAT_SHA512=57cbe9608a9c4e88135e5f5480812e8d57690d5f3f6c43a7c05fe647bddb7c3b684bf0fc0efebad399d05e80c6d20c43d5ecdf38ec58f123e6653e443f9054e3
# Sat, 05 Nov 2022 00:32:15 GMT
COPY dir:2fda4b7c9700d2bf0ebb71a30e51c9e0651b958e2b6d1e096d19623f8f8506ca in /usr/local/tomcat 
# Sat, 05 Nov 2022 00:32:23 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:32:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 05 Nov 2022 00:32:26 GMT
EXPOSE 8080
# Sat, 05 Nov 2022 00:32:26 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:02f24970cf7d1a154c6565b42f393ba6a0e2c23a067c7571a6004bf88a1de8db`  
		Last Modified: Wed, 02 Nov 2022 18:18:59 GMT  
		Size: 35.7 MB (35707582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03873e196fa2aab86a981e0b5a73ace2c40cf4cd3da88abc4c2a4ce980ef6bc`  
		Last Modified: Wed, 02 Nov 2022 19:03:58 GMT  
		Size: 13.3 MB (13263240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77caf72d771e3770bb4b742ba76794160bc2a415a266012f4b3f48678e33dacd`  
		Last Modified: Fri, 04 Nov 2022 23:26:36 GMT  
		Size: 41.2 MB (41216665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12044dfe27fa028727095dd29c6e5fcda09571dd556c7beb6f09dfac06b7cb1`  
		Last Modified: Fri, 04 Nov 2022 23:26:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bc09e3fc9cc34490a7e07ee6774d0a8e5424d487c2fae85eab9f774f19b5eb`  
		Last Modified: Sat, 05 Nov 2022 00:46:30 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb71abe46414f0480250721de9d6d559abd7ec372573332aa18724ea04e8d98b`  
		Last Modified: Sat, 05 Nov 2022 00:54:28 GMT  
		Size: 11.2 MB (11243335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ba0fe2dcc64bdf73f702fb32739a9677a55c44de83e16401f788fd60dfa73d`  
		Last Modified: Sat, 05 Nov 2022 00:54:26 GMT  
		Size: 483.8 KB (483846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9f14f364aa6e51f667e9c3e08077ebfdcbb5205e95a5a5d8cd13a55c8bb701`  
		Last Modified: Sat, 05 Nov 2022 00:54:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
