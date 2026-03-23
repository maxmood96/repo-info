## `tomcat:10-jre25-temurin-jammy`

```console
$ docker pull tomcat@sha256:8f22fa621e1618494b75d53be3aab64224a15e6b8fa2db49ea10a691e0ef8ac7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `tomcat:10-jre25-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:4614920a788c904461bf6276addcc620ec79eb779e1f8a59929ed0ebe45cbcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118197508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95721d3501954ed6aae21015d08401e633f18e3615b467b9d927949cb2db011a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:23:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:23:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:23:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:23:35 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:23:35 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 17 Mar 2026 01:23:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 01:23:54 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:23:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:23:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 23 Mar 2026 22:04:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 23 Mar 2026 22:04:32 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 22:04:32 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 23 Mar 2026 22:04:32 GMT
WORKDIR /usr/local/tomcat
# Mon, 23 Mar 2026 22:04:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 23 Mar 2026 22:04:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 23 Mar 2026 22:04:32 GMT
ENV TOMCAT_MAJOR=10
# Mon, 23 Mar 2026 22:04:32 GMT
ENV TOMCAT_VERSION=10.1.53
# Mon, 23 Mar 2026 22:04:32 GMT
ENV TOMCAT_SHA512=0b21ad1e61b3163125866e8f5f317b23886998fccb4398f305c39a0bc1f688f6c566ab040da9f559ab50af4d699bda771d1ca89e229ead052336559a25753b45
# Mon, 23 Mar 2026 22:04:32 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 23 Mar 2026 22:04:38 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 22:04:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 23 Mar 2026 22:04:39 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 23 Mar 2026 22:04:39 GMT
ENTRYPOINT []
# Mon, 23 Mar 2026 22:04:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44daa92e1c11ca52a7a54f215387d0ad2c4af549cff6eb649ceb78733944fafd`  
		Last Modified: Tue, 17 Mar 2026 01:24:09 GMT  
		Size: 11.4 MB (11405077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470590ea775c66ca982599be4630940d51286c92d4084968ed3995c43f4295c6`  
		Last Modified: Tue, 17 Mar 2026 01:24:11 GMT  
		Size: 62.7 MB (62708272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c4beb2895c684784cd3d998919c3e324aa19a17016f005449cecfd56eb34bd`  
		Last Modified: Tue, 17 Mar 2026 01:24:06 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe082cab5c32d0a5b587034d15326726dec483e981d6cecc0ef0ae98e72c88e2`  
		Last Modified: Mon, 23 Mar 2026 22:04:48 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5551a54b885f9fff9ccffa87e4af763fa6fb3472928bc4eaf40763787d0d83`  
		Last Modified: Mon, 23 Mar 2026 22:04:49 GMT  
		Size: 14.3 MB (14312071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431cab29fa722805ab0ba9cc4721d9b62a2326a30704b904fd1c399b9ab4fa4a`  
		Last Modified: Mon, 23 Mar 2026 22:04:48 GMT  
		Size: 231.1 KB (231050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:d1d7e26a501c6ad73c9658568cbb1cf13cc5a79bf9e8ca9ddb92ddbd9de2b5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c137dab81fd563b5b597cd44c549468ffe41433e7a8cf4d1ec2d1df41b14405c`

```dockerfile
```

-	Layers:
	-	`sha256:1f65101e779673639ca7592d7e3875f61a3b17ea4aff0ab47a0a0fd999063d1d`  
		Last Modified: Mon, 23 Mar 2026 22:04:48 GMT  
		Size: 3.7 MB (3709354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:748709d9a1d9ff6ae9876af5d85111b900b9203989be824950d914c91e78de56`  
		Last Modified: Mon, 23 Mar 2026 22:04:48 GMT  
		Size: 21.2 KB (21212 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre25-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:9881452cb936106de68be86061298a90a4567f2465fd0ef54f3d97a184aa9d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (114956946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736daf6fff881b01bef2427fe04d735b78584df5a1c20f9539c6850a0d07fa82`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:25:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:25:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:25:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:25:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:25:03 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 17 Mar 2026 01:25:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 01:25:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:25:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:25:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 23 Mar 2026 22:04:43 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 23 Mar 2026 22:04:43 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 22:04:43 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 23 Mar 2026 22:04:43 GMT
WORKDIR /usr/local/tomcat
# Mon, 23 Mar 2026 22:04:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 23 Mar 2026 22:04:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 23 Mar 2026 22:04:43 GMT
ENV TOMCAT_MAJOR=10
# Mon, 23 Mar 2026 22:04:43 GMT
ENV TOMCAT_VERSION=10.1.53
# Mon, 23 Mar 2026 22:04:43 GMT
ENV TOMCAT_SHA512=0b21ad1e61b3163125866e8f5f317b23886998fccb4398f305c39a0bc1f688f6c566ab040da9f559ab50af4d699bda771d1ca89e229ead052336559a25753b45
# Mon, 23 Mar 2026 22:04:43 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 23 Mar 2026 22:04:50 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 22:04:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 23 Mar 2026 22:04:51 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 23 Mar 2026 22:04:51 GMT
ENTRYPOINT []
# Mon, 23 Mar 2026 22:04:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f624e573b3a7b5405d838f185ec5fbcc027f717d6de99fcb3ea59bc7ab2bd42`  
		Last Modified: Tue, 17 Mar 2026 01:25:39 GMT  
		Size: 11.4 MB (11353553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876f51126dd3ec8d3d88ab6fe11d76b099b10c5a1476ac75cdb14f4cdf7896a2`  
		Last Modified: Tue, 17 Mar 2026 01:25:41 GMT  
		Size: 61.7 MB (61669317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb29dbbcf7f4798144a0b93b2acff13e19344328cf8718c53e6766aea4867f01`  
		Last Modified: Tue, 17 Mar 2026 01:25:39 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf3720dd3b874cffd9a985fb8b1f1aebe758532147c6a5e3816b5381c8f0e81`  
		Last Modified: Mon, 23 Mar 2026 22:05:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137f552d16856deac74802395e6babcfbf9fc430587389f3ab02b266180b6588`  
		Last Modified: Mon, 23 Mar 2026 22:05:00 GMT  
		Size: 14.3 MB (14312604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5187b18198bc997a7aede4f6fbf10439b58a4887993d2f097c7e736d253f924`  
		Last Modified: Mon, 23 Mar 2026 22:05:00 GMT  
		Size: 229.9 KB (229930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:86770f0be0de434c0d7f70d6642b7420e501df0b35e71834d26f1e970bf9b766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4372c8b2cdd033408e834f531e357aa1fa3badb6dd1a8887762b5b5826fc3e`

```dockerfile
```

-	Layers:
	-	`sha256:e378522c94f6a777060ecf3a4edd25adc4fd849ff47f0213db8b572f23ffdadc`  
		Last Modified: Mon, 23 Mar 2026 22:05:00 GMT  
		Size: 3.7 MB (3709005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e0a8b1791da39fa1a5541dbf6c82f648c0d4192e8cc7711a7c458120055d456`  
		Last Modified: Mon, 23 Mar 2026 22:05:00 GMT  
		Size: 21.4 KB (21360 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre25-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:ac23180cbb1d82c6aa0ee86bfaaa477dd6f52b36dee598dcd69e4670c14a7215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123064197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d5c05333c4b9d457f973f545678a5f2a8ec34a7388b274e3712a9cba9db499`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 24 Feb 2026 07:34:11 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:34:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:34:16 GMT
ADD file:8cdc5dcac981a23986a941c048f55a86d8ba46328e91ad30db9af43286781c61 in / 
# Tue, 24 Feb 2026 07:34:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 08:40:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 08:40:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 08:40:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 08:40:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 08:40:15 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 17 Mar 2026 08:40:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 08:40:45 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 08:40:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 08:40:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 20 Mar 2026 20:59:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 20 Mar 2026 20:59:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 20:59:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 20 Mar 2026 20:59:39 GMT
WORKDIR /usr/local/tomcat
# Fri, 20 Mar 2026 20:59:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 20 Mar 2026 20:59:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 20 Mar 2026 20:59:39 GMT
ENV TOMCAT_MAJOR=10
# Fri, 20 Mar 2026 20:59:39 GMT
ENV TOMCAT_VERSION=10.1.53
# Fri, 20 Mar 2026 20:59:39 GMT
ENV TOMCAT_SHA512=0b21ad1e61b3163125866e8f5f317b23886998fccb4398f305c39a0bc1f688f6c566ab040da9f559ab50af4d699bda771d1ca89e229ead052336559a25753b45
# Mon, 23 Mar 2026 22:03:06 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 23 Mar 2026 22:03:15 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 22:03:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 23 Mar 2026 22:03:18 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 23 Mar 2026 22:03:18 GMT
ENTRYPOINT []
# Mon, 23 Mar 2026 22:03:18 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:31e4dc9ee1718c21d378c7cdb3929e157eabf4d70fe4bbe2e6b8ec5289e836dc`  
		Last Modified: Tue, 24 Feb 2026 08:08:05 GMT  
		Size: 34.5 MB (34453448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f1b3a275c4e3fa405da3e9b005e9021435a22e49e97d4b911f23dd0aba7c2d`  
		Last Modified: Tue, 17 Mar 2026 08:41:22 GMT  
		Size: 11.9 MB (11892875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bd2cd31b5c09f834d91c1954f1e70f2c852a131cef1590c2e566c81b42ca62`  
		Last Modified: Tue, 17 Mar 2026 08:41:23 GMT  
		Size: 62.1 MB (62126989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afa3a18270687eb7dec7bce2eb815c7133d2ef5b22f687d3ed126f27a90028b`  
		Last Modified: Tue, 17 Mar 2026 08:41:21 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16614066aca216077572814f4fb29a6d3c4aaa254bf9f680b9d5bee1b3d59d2b`  
		Last Modified: Fri, 20 Mar 2026 21:00:17 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936bf0f194099cfe999e97ac63668b1f93c631103f9a9dac490fcc7ec5712cec`  
		Last Modified: Mon, 23 Mar 2026 22:03:39 GMT  
		Size: 14.3 MB (14323830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab46231845cea4ea58b1b227c386cc4598df2c3708a53aeff9d84eeb8b80874`  
		Last Modified: Mon, 23 Mar 2026 22:03:39 GMT  
		Size: 264.5 KB (264537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:ae93a128a124d28dd2ff077a2690c94f4b31ac531e452853d639fe0aa4c6ada3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3733959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08fce82f033458f7aaf9c4f7ebb3050b9ff562788ed5d0321c63d88e72adae3d`

```dockerfile
```

-	Layers:
	-	`sha256:7b60fffee22c66663495ccbcf8a802da11fb5591cef73961649c97be8ebf735a`  
		Last Modified: Mon, 23 Mar 2026 22:03:39 GMT  
		Size: 3.7 MB (3712694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0603a31449e034b50a3032b55b55f41eb8cbc4e11568fa1a1e42c9cd20cb7717`  
		Last Modified: Mon, 23 Mar 2026 22:03:39 GMT  
		Size: 21.3 KB (21265 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre25-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:f768601e40aa5115e8f40397e719690dd9414d280cff7e8134d23bc93fb2cbdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114374326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab6b6909a09a8c8294f5a5a3017b3d6ed0a692f4cb47cdf58769437e08cbf63`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:34 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:36 GMT
ADD file:03057d2fc9102d77c6c1ba39821174f9277c7aeb8de5358b12c437097e81cdb8 in / 
# Tue, 24 Feb 2026 07:33:36 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:23:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:23:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:23:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 02:23:45 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:23:45 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 17 Mar 2026 02:23:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 02:23:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 02:23:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 02:23:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 20 Mar 2026 21:00:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 20 Mar 2026 21:00:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 21:00:20 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 20 Mar 2026 21:00:20 GMT
WORKDIR /usr/local/tomcat
# Fri, 20 Mar 2026 21:00:20 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 20 Mar 2026 21:00:20 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 20 Mar 2026 21:00:20 GMT
ENV TOMCAT_MAJOR=10
# Fri, 20 Mar 2026 21:00:20 GMT
ENV TOMCAT_VERSION=10.1.53
# Fri, 20 Mar 2026 21:00:20 GMT
ENV TOMCAT_SHA512=0b21ad1e61b3163125866e8f5f317b23886998fccb4398f305c39a0bc1f688f6c566ab040da9f559ab50af4d699bda771d1ca89e229ead052336559a25753b45
# Mon, 23 Mar 2026 22:03:28 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 23 Mar 2026 22:03:32 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 22:03:32 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 23 Mar 2026 22:03:32 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 23 Mar 2026 22:03:32 GMT
ENTRYPOINT []
# Mon, 23 Mar 2026 22:03:32 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b108e2a3f64e047295acfb714c51eedfbd4912d55d53e8bbbad5c2ac52fdf289`  
		Last Modified: Tue, 24 Feb 2026 08:08:19 GMT  
		Size: 28.0 MB (28007102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b508d67a1e77ccd082ca229acf8d3d1215ad36f7331f30b45345a429173893`  
		Last Modified: Tue, 17 Mar 2026 02:24:17 GMT  
		Size: 11.5 MB (11497785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635745ee48f6a7a9b0ada985f7acb88bcbbf102a102098b0432c207a08b16fde`  
		Last Modified: Tue, 17 Mar 2026 02:24:18 GMT  
		Size: 60.3 MB (60321960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7ee3ed000edf49a8e4d61c40869a27dc84790abf9c101d2792b3c85a997c7c`  
		Last Modified: Tue, 17 Mar 2026 02:24:17 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755ac56965f3ed47bac1b01e079ef3d5facad02298a17720a7c4d6af165d6b28`  
		Last Modified: Fri, 20 Mar 2026 21:00:38 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6cc3de327c6590aaed2b5b2b89ba238873cdea48e2d7b66a47320596bc7550`  
		Last Modified: Mon, 23 Mar 2026 22:03:46 GMT  
		Size: 14.3 MB (14313318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849955e655f9d749a7de7062f6ced0a67a1ba63ed2ab95221d1d841dc951e7bb`  
		Last Modified: Mon, 23 Mar 2026 22:03:46 GMT  
		Size: 231.6 KB (231643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:8a4140fbab640f669cdf97f986fcf5c593c2bab4ad2fd21361353f081d017d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fe09139257abc3b59ce5691611884fe4c6d81aac0280e21fe3a32839897e2f`

```dockerfile
```

-	Layers:
	-	`sha256:9196b0b99082993b0f80522bd8907b6f7bf7a766d58e82e469c9c9107c59e59b`  
		Last Modified: Mon, 23 Mar 2026 22:03:46 GMT  
		Size: 3.7 MB (3710339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e50698e0476b1ebaa46f07ceffe91c7b28a6de31abc043be4d1b83856a6c4ac`  
		Last Modified: Mon, 23 Mar 2026 22:03:46 GMT  
		Size: 21.2 KB (21212 bytes)  
		MIME: application/vnd.in-toto+json
