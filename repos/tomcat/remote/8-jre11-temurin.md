## `tomcat:8-jre11-temurin`

```console
$ docker pull tomcat@sha256:391f8236fb617e269f759cd715c4d3d05d2bcfae0415640c4db3e770e253e82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; s390x

### `tomcat:8-jre11-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:2d3cf4b933e87dcbd3fc91a1cd5f4d401c424479c36a07a6dd68b6f42b1a667f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.5 MB (99503761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1a2b1a7e3bb4508216e0ee608758068ad9ba59d2be9fa5a007cb7492858157`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:55 GMT
ADD file:d2abf27fe2e8b0b5f4da68c018560c73e11c53098329246e3e6fe176698ef941 in / 
# Tue, 31 Aug 2021 01:20:56 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:26:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Aug 2021 03:31:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Sep 2021 23:20:01 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Mon, 13 Sep 2021 18:21:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eebf9b6b515fd139d45410ea4a0e7c18f015acba41e677cd7a57d1fe7a553681';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='21129821a148503333dcc9868f04f3c971290c75f07ca384b1ab5d906901ea80';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x)          ESUM='17932e94e7daa84057e20f99536cc66ab5ff52637b50bd5c1dfdcc1853aad0a9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|x86_64)          ESUM='e813e270b7ea0a13f9c400ce5abd4cb811aacbd536b8909e6c7f0e346f78348c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 13 Sep 2021 18:21:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Sep 2021 18:21:22 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Mon, 13 Sep 2021 19:25:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 13 Sep 2021 19:25:58 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Sep 2021 19:25:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 13 Sep 2021 19:25:59 GMT
WORKDIR /usr/local/tomcat
# Mon, 13 Sep 2021 19:26:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 13 Sep 2021 19:26:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 13 Sep 2021 19:36:02 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 13 Sep 2021 19:36:02 GMT
ENV TOMCAT_MAJOR=8
# Mon, 13 Sep 2021 19:36:02 GMT
ENV TOMCAT_VERSION=8.5.70
# Mon, 13 Sep 2021 19:36:03 GMT
ENV TOMCAT_SHA512=10d306a2ea27e10b914556678763e2b1295ffdaa3da042db586d39b9ab95640bd3e1b81627f96c61f400f2db98a7d4b4bbdf21dc3238c8d0025bf95b08f2f61c
# Mon, 13 Sep 2021 19:36:03 GMT
COPY dir:4ca3155cea4950a253a45f6641322467a1b50b9c7970feb1a7283673e39e6e8a in /usr/local/tomcat 
# Mon, 13 Sep 2021 19:36:07 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 13 Sep 2021 19:36:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 13 Sep 2021 19:36:09 GMT
EXPOSE 8080
# Mon, 13 Sep 2021 19:36:09 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:35807b77a593c1147d13dc926a91dcc3015616ff7307cc30442c5a8e07546283`  
		Last Modified: Sat, 28 Aug 2021 03:03:19 GMT  
		Size: 28.6 MB (28570074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74df1ad422e5a232e54d515fb2475eee78b57b25d905611bbceb50f364c0150c`  
		Last Modified: Tue, 31 Aug 2021 03:33:27 GMT  
		Size: 16.0 MB (16032853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cbfc14ccf6101c785c2d1ff53639357aedc16887c9c85b39529294a043a695e`  
		Last Modified: Mon, 13 Sep 2021 18:24:43 GMT  
		Size: 43.2 MB (43219906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a5d4f7a5417c56577d57524967f238c052385de0b5a61bf12826f50fedb77d`  
		Last Modified: Mon, 13 Sep 2021 18:24:36 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3361ef5865a4b8f2437560a6a94c7b32c21cad281c67446eac77081c6f8d437b`  
		Last Modified: Mon, 13 Sep 2021 19:47:11 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dba1ffd2b44d99565b44f7bf357e70d6e0d741dc3c3b743c563db23aa7c747a`  
		Last Modified: Mon, 13 Sep 2021 19:54:51 GMT  
		Size: 11.2 MB (11234890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c076baceb5f6641d9e276afe84e2fbfc270da6f8dc882beb6b9a5ab1ed3b9b`  
		Last Modified: Mon, 13 Sep 2021 19:54:51 GMT  
		Size: 445.6 KB (445575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54504f213814e7d20c5e02f8fd0d54aa030bd177e4e14f2d4b7a5b70c668967e`  
		Last Modified: Mon, 13 Sep 2021 19:54:51 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre11-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:cfab38369e66b13f99d795e293878d2190b89e4c81f5f499002432b1bf6f3b95
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92138159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1852897c30582cbcc21ef535f6ca9a0421bfc45c4ff94751b0b79eea70ca1ab7`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Aug 2021 01:42:23 GMT
ADD file:979855f79ebaca36cc7878f71b2326f1cd189970fdb223b37cd64ee12d1c9a2b in / 
# Tue, 31 Aug 2021 01:42:27 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:07:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 13 Sep 2021 17:42:08 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 13 Sep 2021 17:42:11 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Mon, 13 Sep 2021 17:43:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='eebf9b6b515fd139d45410ea4a0e7c18f015acba41e677cd7a57d1fe7a553681';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='21129821a148503333dcc9868f04f3c971290c75f07ca384b1ab5d906901ea80';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        s390x)          ESUM='17932e94e7daa84057e20f99536cc66ab5ff52637b50bd5c1dfdcc1853aad0a9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|x86_64)          ESUM='e813e270b7ea0a13f9c400ce5abd4cb811aacbd536b8909e6c7f0e346f78348c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 13 Sep 2021 17:43:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Sep 2021 17:43:10 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 14 Sep 2021 17:44:53 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 14 Sep 2021 17:44:54 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Sep 2021 17:44:56 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 14 Sep 2021 17:44:56 GMT
WORKDIR /usr/local/tomcat
# Tue, 14 Sep 2021 17:44:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 14 Sep 2021 17:44:58 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 14 Sep 2021 17:55:00 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 14 Sep 2021 17:55:01 GMT
ENV TOMCAT_MAJOR=8
# Tue, 14 Sep 2021 17:55:02 GMT
ENV TOMCAT_VERSION=8.5.71
# Tue, 14 Sep 2021 17:55:02 GMT
ENV TOMCAT_SHA512=292a3f856b0a8c1d11fd1ba252cabd94794201cda4f951dd0522764449bed90f2f43a4a667cd6d28ce13c3b2096736978d9df91709c168ba7133c51544446433
# Tue, 14 Sep 2021 17:55:04 GMT
COPY dir:362090bda62dc87c36573fb14cad0d3a27eddc8f1c9f2f40392acf3bfdcb1b37 in /usr/local/tomcat 
# Tue, 14 Sep 2021 17:55:15 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 Sep 2021 17:55:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 14 Sep 2021 17:55:18 GMT
EXPOSE 8080
# Tue, 14 Sep 2021 17:55:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9fbf86d355c92d30b8de4c0360b0d79e1100e392d0885b6b5b302a1c3781dbf1`  
		Last Modified: Tue, 31 Aug 2021 01:44:13 GMT  
		Size: 27.1 MB (27127470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d20a826ef27dc1821c9889c4347bca43c74e64a47d57bbe597f7b8c77bde134`  
		Last Modified: Mon, 13 Sep 2021 17:44:19 GMT  
		Size: 15.7 MB (15741174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69890c40480bd5ace67afbce9e0f4219b07298930518dc2395ce89518d662dfd`  
		Last Modified: Mon, 13 Sep 2021 17:44:47 GMT  
		Size: 37.6 MB (37564520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc85b2408a63ded7d17a0a1cfa174d3225ffe11c36e50687dd8cab4b2ec3f22`  
		Last Modified: Mon, 13 Sep 2021 17:44:41 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0580832d6a4aef85ca2675531cc326a734a1c7ff6f08f80876af9a5d50d4fe89`  
		Last Modified: Tue, 14 Sep 2021 17:59:10 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e189d3cc4e93cdcc0f95959f78b0348fb5ff6544b51c0e61b3a4cb0aa10350fc`  
		Last Modified: Tue, 14 Sep 2021 18:02:22 GMT  
		Size: 11.3 MB (11257680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75d3bb79c1e9513e9e95718a70d627bed13acba157746e24e847648fb919ba3`  
		Last Modified: Tue, 14 Sep 2021 18:02:22 GMT  
		Size: 446.9 KB (446855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ca3cd0d1742a57a8ade8838990b70f896bb66e613b431f4a1c3b437468a82a`  
		Last Modified: Tue, 14 Sep 2021 18:02:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
