## `tomcat:jre25-temurin-jammy`

```console
$ docker pull tomcat@sha256:7fc4b420850a757bd6cce45b0f223213d9c4084cb0c0753e203468b9f1738b77
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

### `tomcat:jre25-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:c8b59dcab1e2cc041b8f4263406a1c3566eed4c92e7782817f204ea72cea1fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118215767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdacc3a6735997a513f09bb26da95eab434df40817bffee3a4d849ebbe1d472c`
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
# Fri, 20 Mar 2026 21:01:30 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 20 Mar 2026 21:01:30 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 21:01:30 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 20 Mar 2026 21:01:30 GMT
WORKDIR /usr/local/tomcat
# Fri, 20 Mar 2026 21:01:30 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 20 Mar 2026 21:01:30 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 20 Mar 2026 21:01:30 GMT
ENV TOMCAT_MAJOR=11
# Fri, 20 Mar 2026 21:01:30 GMT
ENV TOMCAT_VERSION=11.0.20
# Fri, 20 Mar 2026 21:01:30 GMT
ENV TOMCAT_SHA512=8edf12ae9ffb837d1fa1542beae9a80b40419c341963eabed074f2f11d8168e0a82307d5fdc010102db5ee2b983b404816b13435f8c6810b7684fe7b3c19191d
# Fri, 20 Mar 2026 21:01:30 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 20 Mar 2026 21:01:37 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Mar 2026 21:01:37 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 20 Mar 2026 21:01:37 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 20 Mar 2026 21:01:37 GMT
ENTRYPOINT []
# Fri, 20 Mar 2026 21:01:37 GMT
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
	-	`sha256:e9059b86963606a9e1fd15beb09a17895d859246ce8b7d1aca44b81762d47fd2`  
		Last Modified: Fri, 20 Mar 2026 21:01:45 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9cbfae065137d6bb94e5ef7ae441f9487061f13ca0f83e5a4055815960cee9`  
		Last Modified: Fri, 20 Mar 2026 21:01:46 GMT  
		Size: 14.3 MB (14330329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89166cbc766e3751ab45e2b4413c40a0872b2fcbaac288a79a6e65fa21b165fe`  
		Last Modified: Fri, 20 Mar 2026 21:01:45 GMT  
		Size: 231.1 KB (231051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:f32bb6e4f1cb31efaa664d7abb5d1f474035313bdbd09f12f96dd5022b07c5af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc43dbb155085f4c79ae43264b3e9a9e7d991d9e944fb8679c37199259c8e6a`

```dockerfile
```

-	Layers:
	-	`sha256:ca7c06bd4bd94dc0ed42410fb42b82e704a5758dc18f70d8e74175ddfd448b65`  
		Last Modified: Fri, 20 Mar 2026 21:01:46 GMT  
		Size: 3.7 MB (3709674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9a6c4985ba1781f27c3ad07c8ef72524f3d1299bf10999c855a43fb4c8cf533`  
		Last Modified: Fri, 20 Mar 2026 21:01:45 GMT  
		Size: 21.5 KB (21537 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre25-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:e8b594436462c0f69bf8698877b6b8d6ac9dbebddb21a11a4013d5dc1be97e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (114975178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db221ff0d2e7c3660e69ce548ee268c532e6c40bad7809f3cfe2aeae31f1596d`
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
# Fri, 20 Mar 2026 21:06:13 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 20 Mar 2026 21:06:13 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 21:06:13 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 20 Mar 2026 21:06:13 GMT
WORKDIR /usr/local/tomcat
# Fri, 20 Mar 2026 21:06:13 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 20 Mar 2026 21:06:13 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 20 Mar 2026 21:06:13 GMT
ENV TOMCAT_MAJOR=11
# Fri, 20 Mar 2026 21:06:13 GMT
ENV TOMCAT_VERSION=11.0.20
# Fri, 20 Mar 2026 21:06:13 GMT
ENV TOMCAT_SHA512=8edf12ae9ffb837d1fa1542beae9a80b40419c341963eabed074f2f11d8168e0a82307d5fdc010102db5ee2b983b404816b13435f8c6810b7684fe7b3c19191d
# Fri, 20 Mar 2026 21:06:13 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 20 Mar 2026 21:06:20 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Mar 2026 21:06:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 20 Mar 2026 21:06:21 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 20 Mar 2026 21:06:21 GMT
ENTRYPOINT []
# Fri, 20 Mar 2026 21:06:21 GMT
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
	-	`sha256:810b8261308d1c9e350b7433ea85eea4644c3912a524450e5282561b9677c06f`  
		Last Modified: Fri, 20 Mar 2026 21:06:30 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0bf82048d24685558b27a9574b981523265592ace112791831b939aef9714f`  
		Last Modified: Fri, 20 Mar 2026 21:06:30 GMT  
		Size: 14.3 MB (14330806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81088adcc405adbb25463634e3f1ebdb2797bc42634627ecaea51fed2e41a12`  
		Last Modified: Fri, 20 Mar 2026 21:06:30 GMT  
		Size: 230.0 KB (229959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:d6cfbf5aac588c92cb6b3e74ac53f666af541b3b27eca45eea0af55d7464b2c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2eba5fc980587f6cd2967b5203189ea0cbfb02145f67bf7a7dc536f91b27d7`

```dockerfile
```

-	Layers:
	-	`sha256:1864e37b1eb5c284351145d241cad2cbfc165050558baacf2369b36f6dd4f8d4`  
		Last Modified: Fri, 20 Mar 2026 21:06:30 GMT  
		Size: 3.7 MB (3709337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0758134ed720dea70c84594dbe339459174a881d1a1a4a58681a65573c04aaa`  
		Last Modified: Fri, 20 Mar 2026 21:06:30 GMT  
		Size: 21.7 KB (21697 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre25-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:f7e2cc5b587747544ef695aa859f472c5810079788e33a7b51ad89882e935e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123086631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f91178efcc767d07068ce0972ae027adf71964fa20b10f530cbd53121b8f2c4`
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
ENV TOMCAT_MAJOR=11
# Fri, 20 Mar 2026 20:59:39 GMT
ENV TOMCAT_VERSION=11.0.20
# Fri, 20 Mar 2026 20:59:39 GMT
ENV TOMCAT_SHA512=8edf12ae9ffb837d1fa1542beae9a80b40419c341963eabed074f2f11d8168e0a82307d5fdc010102db5ee2b983b404816b13435f8c6810b7684fe7b3c19191d
# Fri, 20 Mar 2026 20:59:40 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 20 Mar 2026 20:59:54 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Mar 2026 20:59:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 20 Mar 2026 20:59:56 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 20 Mar 2026 20:59:56 GMT
ENTRYPOINT []
# Fri, 20 Mar 2026 20:59:56 GMT
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
	-	`sha256:0a91ec957eb46a4d65cc1dd41cf143a20309e91f8b78dfa61efb3625033c8733`  
		Last Modified: Fri, 20 Mar 2026 21:00:18 GMT  
		Size: 14.3 MB (14346229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713af7633a5017f89fafd37a5c4e77997b94e1681ea8e315ce29a41d848c2321`  
		Last Modified: Fri, 20 Mar 2026 21:00:17 GMT  
		Size: 264.6 KB (264572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:38be59b0e5e008665fa771885b2b7d4f0aff9d12b94e6e90d43cfd3384b160a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3734614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98da85c9f7b2fa01e710e7745515055aa8366e39cf9d22d90005799988274bec`

```dockerfile
```

-	Layers:
	-	`sha256:d31910329df33b310084bbd838a54d398f0e288b0d524eb08af7a3a5f68a2827`  
		Last Modified: Fri, 20 Mar 2026 21:00:17 GMT  
		Size: 3.7 MB (3713020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:505ef8dab5d86178b65027e76d641adf22852179c2c22b4e119caa67fd1f0fd0`  
		Last Modified: Fri, 20 Mar 2026 21:00:17 GMT  
		Size: 21.6 KB (21594 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre25-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:c97c38400c57d45f9611d819f4aac9c99783c9239cceca8d67d3caf4a9594b80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114394111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312cf06dee575d33f91b390bea9214617c817af3685a2ab0907015f56e6a7352`
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
ENV TOMCAT_MAJOR=11
# Fri, 20 Mar 2026 21:00:20 GMT
ENV TOMCAT_VERSION=11.0.20
# Fri, 20 Mar 2026 21:00:20 GMT
ENV TOMCAT_SHA512=8edf12ae9ffb837d1fa1542beae9a80b40419c341963eabed074f2f11d8168e0a82307d5fdc010102db5ee2b983b404816b13435f8c6810b7684fe7b3c19191d
# Fri, 20 Mar 2026 21:00:20 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 20 Mar 2026 21:00:23 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Mar 2026 21:00:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 20 Mar 2026 21:00:24 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 20 Mar 2026 21:00:24 GMT
ENTRYPOINT []
# Fri, 20 Mar 2026 21:00:24 GMT
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
	-	`sha256:3afba17ef5d44fa69386cc8ebac90dfc06e3a0045ed5997369b0c23b54735408`  
		Last Modified: Fri, 20 Mar 2026 21:00:38 GMT  
		Size: 14.3 MB (14333114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fdc937626abba9af001dc53d568ef31564e358dd7ac9395852727624c7f705`  
		Last Modified: Fri, 20 Mar 2026 21:00:38 GMT  
		Size: 231.6 KB (231632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:7b6832e5609f5c38c038294eff531c2841bd5875ec4c3941bfdc0e1126312dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be57ee18f6d77ab11e5e5503619afbc32ae5da6a7d7df95420298d1cf8b7db5`

```dockerfile
```

-	Layers:
	-	`sha256:c5b1117fec1f8e62f53c6a2b575706333bebd22734355e20eaacb23ef8c1dae7`  
		Last Modified: Fri, 20 Mar 2026 21:00:38 GMT  
		Size: 3.7 MB (3710659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d3bb3602a3e8a9afa33c9ada5e7c1a0385d05bb339219e6fcf6276ad86ee60b`  
		Last Modified: Fri, 20 Mar 2026 21:00:38 GMT  
		Size: 21.5 KB (21537 bytes)  
		MIME: application/vnd.in-toto+json
