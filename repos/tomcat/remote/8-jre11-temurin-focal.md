## `tomcat:8-jre11-temurin-focal`

```console
$ docker pull tomcat@sha256:9fdf0d9dad19d4c3f993b554eab7a23423d1a0ef4ed1dfd32e69231005701352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:8-jre11-temurin-focal` - linux; amd64

```console
$ docker pull tomcat@sha256:3cc1c60e60013adb24be2503a24f0c7873821f87b985a887f9dbb57cb34f02ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103696804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69e1b0b8ee3ea51cb67e620925c9793d3a8b5a3a2a682319675981feeee0326`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 02:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Aug 2023 02:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 02:34:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 03 Aug 2023 02:35:46 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 02:36:29 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Thu, 03 Aug 2023 02:36:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 03 Aug 2023 02:36:58 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 03 Aug 2023 05:20:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 03 Aug 2023 05:20:24 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 05:20:25 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 03 Aug 2023 05:20:25 GMT
WORKDIR /usr/local/tomcat
# Thu, 03 Aug 2023 05:20:25 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 03 Aug 2023 05:20:25 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 03 Aug 2023 05:23:38 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 03 Aug 2023 05:23:38 GMT
ENV TOMCAT_MAJOR=8
# Thu, 03 Aug 2023 05:23:38 GMT
ENV TOMCAT_VERSION=8.5.91
# Thu, 03 Aug 2023 05:23:38 GMT
ENV TOMCAT_SHA512=9e6770e9c9c3b630011c0f0e320b31bb0ea3700d52247a12d544ea25f9ee4d93613ad6ccb7939f97fb05e1760978a7547eccb16352d73fa28886134ba58f3f8c
# Thu, 03 Aug 2023 05:23:38 GMT
COPY dir:28a359ef4cad20c892a4153791f38d22760cbcc3f8d4a7a12f578de7143df8b8 in /usr/local/tomcat 
# Thu, 03 Aug 2023 05:24:13 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 05:24:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 03 Aug 2023 05:24:14 GMT
EXPOSE 8080
# Thu, 03 Aug 2023 05:24:14 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80386a9626c5ee35081325cf50aa5eb65bc1931df6941c0b98c39f5b6b565044`  
		Last Modified: Thu, 03 Aug 2023 02:40:22 GMT  
		Size: 16.4 MB (16413423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04860b6b47ca7a87950102eefba9cfc184ce7b65bc90f9770b3c629dca061919`  
		Last Modified: Thu, 03 Aug 2023 02:41:29 GMT  
		Size: 46.9 MB (46865017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a09e3439ecdbabcb1e2ba84471abffb8fb0cacdae0715cbd1e2eb44bf926c54`  
		Last Modified: Thu, 03 Aug 2023 02:41:23 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:867542b3c6357b16ac67f5836897c0e67bd4154c15fbef3c9551d80e9ad62305`  
		Last Modified: Thu, 03 Aug 2023 05:29:02 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eab6f65f1f328d133caced9d7128a6fdb23f7a75af3695743e441ec7de45427`  
		Last Modified: Thu, 03 Aug 2023 05:30:45 GMT  
		Size: 11.4 MB (11388773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62838a2d5796d8a70930ec69fa6bf5f31a1ae8eec4b7196062b3b603f456aeeb`  
		Last Modified: Thu, 03 Aug 2023 05:30:44 GMT  
		Size: 448.5 KB (448456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1abd4332bdd70d5eb46bbf04fd9238d79cc16c507e7ba533876b1fc7a7e62c`  
		Last Modified: Thu, 03 Aug 2023 05:30:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre11-temurin-focal` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:e022239d72f3eadff163b924c060539a02e4b08b849f1f8209b18eb09fdbbee2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97028798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8edd1934e02d624846a3c2af80e77bc22fe04c1e99fe18b0913028c5dc9c61a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:45 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:49 GMT
ADD file:60aa8465a6ba5538decc41365cc9b78ae86131e8c2cfc9177b4a336354ead988 in / 
# Tue, 01 Aug 2023 06:16:50 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 01:27:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Aug 2023 01:27:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 01:27:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 18:57:54 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 18:59:47 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Tue, 08 Aug 2023 19:00:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 08 Aug 2023 19:00:26 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 08 Aug 2023 19:00:26 GMT
COPY file:0673fe0a4a716089bcd96321c8de60149aea8a94ae7c4ba827ecc4a74a9789a3 in / 
# Tue, 08 Aug 2023 19:00:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Aug 2023 19:59:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 08 Aug 2023 19:59:54 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 19:59:55 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 08 Aug 2023 19:59:55 GMT
WORKDIR /usr/local/tomcat
# Tue, 08 Aug 2023 19:59:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 08 Aug 2023 19:59:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 08 Aug 2023 20:04:53 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 08 Aug 2023 20:04:53 GMT
ENV TOMCAT_MAJOR=8
# Tue, 08 Aug 2023 20:04:53 GMT
ENV TOMCAT_VERSION=8.5.91
# Tue, 08 Aug 2023 20:04:53 GMT
ENV TOMCAT_SHA512=9e6770e9c9c3b630011c0f0e320b31bb0ea3700d52247a12d544ea25f9ee4d93613ad6ccb7939f97fb05e1760978a7547eccb16352d73fa28886134ba58f3f8c
# Tue, 08 Aug 2023 20:04:54 GMT
COPY dir:6f984bac88768f5fa911b445d0fffc4ac0f2d31f287afe5f3ae8891e578102cd in /usr/local/tomcat 
# Tue, 08 Aug 2023 20:04:58 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 20:04:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 08 Aug 2023 20:05:00 GMT
EXPOSE 8080
# Tue, 08 Aug 2023 20:05:00 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c429b4536d4b2ab209b0a779f71ba68570f10acf9dd806c7e2011fce49bd5c97`  
		Last Modified: Wed, 02 Aug 2023 04:28:29 GMT  
		Size: 24.6 MB (24591882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cd3a8f320fb2da0d9f7694604e369817023cd4b7b62173714bbff7cad25aae`  
		Last Modified: Tue, 08 Aug 2023 19:02:31 GMT  
		Size: 15.7 MB (15659457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0093c473b1e40e62fd206d1bcc43b34fda02661fab4df01550be92363fc4e61`  
		Last Modified: Tue, 08 Aug 2023 19:04:38 GMT  
		Size: 45.0 MB (45013323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817239aeee7f7e1a21412276af40721187ad513f91fb0d6201ff50ca317dbc8d`  
		Last Modified: Tue, 08 Aug 2023 19:04:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d608892800d60bed5a437e51ed21bd19aa4cc11078dfa8249c7898220d96ba`  
		Last Modified: Tue, 08 Aug 2023 19:04:30 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2392821bf79567d376d96301d22e8895e3c004907a55ebd487e806fd96fa4965`  
		Last Modified: Tue, 08 Aug 2023 20:13:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31dd17c2d14e3972d55c4ba4729a9710a8216ed0abb63475ac0237da22d26d0b`  
		Last Modified: Tue, 08 Aug 2023 20:17:33 GMT  
		Size: 11.3 MB (11336788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da005fdf05eaa5de27f3cdb20701a8f6756c0fb619564453c53161766e7bbf17`  
		Last Modified: Tue, 08 Aug 2023 20:17:32 GMT  
		Size: 426.2 KB (426224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b68ac2db40c6a89e252a24993230afe4179863ed7c098851b3e3eccda732fe41`  
		Last Modified: Tue, 08 Aug 2023 20:17:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre11-temurin-focal` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:aeeb739bda47d7611cc2f0050e9555d39548a255150fb405ec3853b6f0d75935
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100515633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e431b728d91d9bc2c99c43a457acec0b809be327eaa4c93747df6b0a82ebcc4a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 01:05:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Aug 2023 01:05:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 01:05:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 03 Aug 2023 01:05:58 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 01:06:22 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Thu, 03 Aug 2023 01:06:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 03 Aug 2023 01:06:48 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 03 Aug 2023 06:08:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 03 Aug 2023 06:08:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 06:08:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 03 Aug 2023 06:08:42 GMT
WORKDIR /usr/local/tomcat
# Thu, 03 Aug 2023 06:08:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 03 Aug 2023 06:08:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 03 Aug 2023 06:13:03 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 03 Aug 2023 06:13:03 GMT
ENV TOMCAT_MAJOR=8
# Thu, 03 Aug 2023 06:13:03 GMT
ENV TOMCAT_VERSION=8.5.91
# Thu, 03 Aug 2023 06:13:03 GMT
ENV TOMCAT_SHA512=9e6770e9c9c3b630011c0f0e320b31bb0ea3700d52247a12d544ea25f9ee4d93613ad6ccb7939f97fb05e1760978a7547eccb16352d73fa28886134ba58f3f8c
# Thu, 03 Aug 2023 06:13:03 GMT
COPY dir:3da29d335a655f1bcba39aa4195b998b896e927fcbb89687ef4232d4bd16246d in /usr/local/tomcat 
# Thu, 03 Aug 2023 06:13:07 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 06:13:08 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 03 Aug 2023 06:13:08 GMT
EXPOSE 8080
# Thu, 03 Aug 2023 06:13:08 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f221141d5aed1dcc474efaed0a5cf9edc344638b5ca5ddaadfd26d4442e4773c`  
		Last Modified: Thu, 03 Aug 2023 01:10:30 GMT  
		Size: 16.3 MB (16269103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e874c8ace01fc91ec21335866ba36fc0760799c476b8d62be9b970d837bfc2`  
		Last Modified: Thu, 03 Aug 2023 01:11:37 GMT  
		Size: 45.2 MB (45190743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bedee65e45384bfebd48289ea3c88ed60790c081fac203e9c25b7f8b7e7daf09`  
		Last Modified: Thu, 03 Aug 2023 01:11:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e98d8deecafd4c91d1b59b7a8716dd0ed05a263de9485be78442583e4fe6c77`  
		Last Modified: Thu, 03 Aug 2023 06:19:34 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be094ae0a1e8bf9d2113e9fda9f83ce69c464e76a12077b0cecf2b997a407739`  
		Last Modified: Thu, 03 Aug 2023 06:22:11 GMT  
		Size: 11.4 MB (11405224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25638e7d6704e15318a22b1de7ed6440a4ca6c8f95409521ed568d54b8c21d7`  
		Last Modified: Thu, 03 Aug 2023 06:22:10 GMT  
		Size: 449.5 KB (449515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bf899e3939fb906245abc24eb13072e11b017735aab012ead82b8ee4667b96`  
		Last Modified: Thu, 03 Aug 2023 06:22:10 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre11-temurin-focal` - linux; ppc64le

```console
$ docker pull tomcat@sha256:c0e7c804a4db74a82302eb15df4ce11837c12e10d122c410b081ecd8d18e35b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105154055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f566c52fefa8c2824eb433b2e9e864340e5c675636927f6ad054c0b2dde3436`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:36 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:37 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:20:40 GMT
ADD file:822df76493d1d533c1a283ab7bb20ce81309f57279422a0eebb2ffb9fab55963 in / 
# Tue, 01 Aug 2023 06:20:40 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 02:44:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Aug 2023 02:44:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 02:44:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 03 Aug 2023 02:45:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 02:46:15 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Thu, 03 Aug 2023 02:46:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 03 Aug 2023 02:47:02 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 03 Aug 2023 04:46:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 03 Aug 2023 04:46:25 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 04:46:26 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 03 Aug 2023 04:46:27 GMT
WORKDIR /usr/local/tomcat
# Thu, 03 Aug 2023 04:46:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 03 Aug 2023 04:46:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 03 Aug 2023 04:53:11 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 03 Aug 2023 04:53:12 GMT
ENV TOMCAT_MAJOR=8
# Thu, 03 Aug 2023 04:53:13 GMT
ENV TOMCAT_VERSION=8.5.91
# Thu, 03 Aug 2023 04:53:13 GMT
ENV TOMCAT_SHA512=9e6770e9c9c3b630011c0f0e320b31bb0ea3700d52247a12d544ea25f9ee4d93613ad6ccb7939f97fb05e1760978a7547eccb16352d73fa28886134ba58f3f8c
# Thu, 03 Aug 2023 04:53:14 GMT
COPY dir:1fcc8f6998f34c5fb90f01f65dc909682d84e2264c9a86fd114e106329558786 in /usr/local/tomcat 
# Thu, 03 Aug 2023 04:53:24 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 04:53:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 03 Aug 2023 04:53:28 GMT
EXPOSE 8080
# Thu, 03 Aug 2023 04:53:29 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:be0253994e7bea97e6b44cdeec04bf996c8dd3380e70409de3783a1d1971e747`  
		Last Modified: Thu, 03 Aug 2023 02:50:24 GMT  
		Size: 33.3 MB (33306772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab4160c85fcddd5046334857d93707f8292d83756ad21d08b5eced240c8af95`  
		Last Modified: Thu, 03 Aug 2023 02:50:20 GMT  
		Size: 17.6 MB (17648858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe3c6c09e43025e9ef9918c5336fba832cfe614008179ff6ddabc4711d6cdd5`  
		Last Modified: Thu, 03 Aug 2023 02:52:10 GMT  
		Size: 42.3 MB (42295464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3459f0ad5efaba29ef643a84d8711e34e9c842dc479681ea94e7a1cb19f09adb`  
		Last Modified: Thu, 03 Aug 2023 02:51:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f60baa644c668f797aad0199da7fd3c6eadd55e2f140d1614d40ec3387ffd44`  
		Last Modified: Thu, 03 Aug 2023 05:00:14 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bb1b381634b5ce294936a74dec62a6238dd39b331d3312246a521f06c357b6`  
		Last Modified: Thu, 03 Aug 2023 05:02:35 GMT  
		Size: 11.4 MB (11428255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3254f51b84bbd818d95eb5e21be8afce26305c5782205d89165a37d422f7c2a`  
		Last Modified: Thu, 03 Aug 2023 05:02:34 GMT  
		Size: 474.2 KB (474246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0848aacb89cb0979db92ebafc15b5a2de4989fdb34f3d743abf25a97126b2f72`  
		Last Modified: Thu, 03 Aug 2023 05:02:33 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre11-temurin-focal` - linux; s390x

```console
$ docker pull tomcat@sha256:bf4755c1c3cc1abee8a7043899eeacbb1dfcdab283fad65ec1571fec1dc968a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96141910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e325bac03d231a5361ebc6d7033c0ec8c721c8e69215a72815c5c295248ab59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 01 Aug 2023 06:17:39 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:17:41 GMT
ADD file:36efc3ec29bb54e0987fe91be1aa7cc849909b3cd2534af3de2d3d07a03804cf in / 
# Tue, 01 Aug 2023 06:17:41 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 00:24:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Aug 2023 00:24:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 00:24:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 19:42:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 19:42:13 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Tue, 08 Aug 2023 19:43:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 08 Aug 2023 19:43:25 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 08 Aug 2023 19:43:25 GMT
COPY file:0673fe0a4a716089bcd96321c8de60149aea8a94ae7c4ba827ecc4a74a9789a3 in / 
# Tue, 08 Aug 2023 19:43:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Aug 2023 20:12:43 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 08 Aug 2023 20:12:43 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 20:12:43 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 08 Aug 2023 20:12:43 GMT
WORKDIR /usr/local/tomcat
# Tue, 08 Aug 2023 20:12:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 08 Aug 2023 20:12:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 08 Aug 2023 20:15:45 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 08 Aug 2023 20:15:45 GMT
ENV TOMCAT_MAJOR=8
# Tue, 08 Aug 2023 20:15:45 GMT
ENV TOMCAT_VERSION=8.5.91
# Tue, 08 Aug 2023 20:15:45 GMT
ENV TOMCAT_SHA512=9e6770e9c9c3b630011c0f0e320b31bb0ea3700d52247a12d544ea25f9ee4d93613ad6ccb7939f97fb05e1760978a7547eccb16352d73fa28886134ba58f3f8c
# Tue, 08 Aug 2023 20:15:46 GMT
COPY dir:546591ae27b19b34eacb7eae235eb6d50dcd875393c7cf66e908f23e293c8175 in /usr/local/tomcat 
# Tue, 08 Aug 2023 20:15:50 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 20:15:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 08 Aug 2023 20:15:51 GMT
EXPOSE 8080
# Tue, 08 Aug 2023 20:15:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:365fa2124eb5f6f369204f3fe0210d9965952628707dfacd4194a8e15caf0420`  
		Last Modified: Thu, 03 Aug 2023 00:03:37 GMT  
		Size: 27.0 MB (27014233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4bb71ff7cf2cdfba432549f8f118e2394ed9d63653317801c650fc5cdf556b`  
		Last Modified: Tue, 08 Aug 2023 19:46:12 GMT  
		Size: 16.6 MB (16643421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b7901e3458852aefab0cd7d218de7885480a6c539089b6d1bc425a7e6a489b`  
		Last Modified: Tue, 08 Aug 2023 19:46:59 GMT  
		Size: 40.6 MB (40631841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af005abe8cb8ae8675c28b7ac9276cc6cc1b953d703ad5cac418014baf282b49`  
		Last Modified: Tue, 08 Aug 2023 19:46:53 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14908469414e656acb57200767a120077fc216e320ee1f07a5736ea867bccbb8`  
		Last Modified: Tue, 08 Aug 2023 19:46:53 GMT  
		Size: 667.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd67a1a27d8a36c762448550e585fae105d10dc714ce0b7d8827a73609df593`  
		Last Modified: Tue, 08 Aug 2023 20:20:34 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694c643e1d17557cf2ddd2a779dd283d3440a0b1f6b6654075633f53c5097f3d`  
		Last Modified: Tue, 08 Aug 2023 20:22:22 GMT  
		Size: 11.4 MB (11399837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86b4a7cf801badf7b542c4424c04d6ae750a3ce4dc3c27a11c2a221d8a50640`  
		Last Modified: Tue, 08 Aug 2023 20:22:22 GMT  
		Size: 451.4 KB (451449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bfab3f04f3886a29a59545b096d289e4c89b1abef5623896da1e15ce4ebb8e`  
		Last Modified: Tue, 08 Aug 2023 20:22:21 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
