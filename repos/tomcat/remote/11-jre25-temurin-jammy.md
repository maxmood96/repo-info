## `tomcat:11-jre25-temurin-jammy`

```console
$ docker pull tomcat@sha256:4bb2c5f98c6c8337e6e2670f47310bcab99ba848d5f2a1bda81a0cba35b9ac30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `tomcat:11-jre25-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:c1113191319385e10d8e45f04b7fde527cbf9fee1d2ef500e40a6f9d6ab18fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 MB (117955107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae68105b8e54410654918e9ea4bda5201f220927cc04511a8d91c6c5f1d16a6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Fri, 26 Sep 2025 12:51:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 12:51:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 12:51:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
ENV JAVA_VERSION=jdk-25+36
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5e3de13a1487ecc90f8b0cddc83a6cd4e053b4cd48ddcfe5d1f19178e6089fba';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_x64_linux_hotspot_25_36.tar.gz';          ;;        arm64)          ESUM='939a1517971985363b2b57b8c6008f4bd48b91f565366d6eb3bae3aa503a05e2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64el)          ESUM='f593d6c435f6498cfbdb1ca07d7b1fa33829b159abb31b992b6234c324794dad';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='485af5746df1bf3cd46da4e7f771e6d1eae5a31db695ab819c4c2401688a6871';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_s390x_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 26 Sep 2025 16:59:31 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 26 Sep 2025 16:59:31 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 16:59:31 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 26 Sep 2025 16:59:31 GMT
WORKDIR /usr/local/tomcat
# Fri, 26 Sep 2025 16:59:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 26 Sep 2025 16:59:31 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 26 Sep 2025 16:59:31 GMT
ENV TOMCAT_MAJOR=11
# Fri, 26 Sep 2025 16:59:31 GMT
ENV TOMCAT_VERSION=11.0.11
# Fri, 26 Sep 2025 16:59:31 GMT
ENV TOMCAT_SHA512=a26b2269530fd2fc834e9b1544962f6524cf87925de43b05ad050e66b5eaa76a4ad754a2c5fc4f851baf75a0ea1b0ed8f51082300393a4c35d8c2da0d7c535bd
# Fri, 26 Sep 2025 16:59:31 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 26 Sep 2025 16:59:31 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Sep 2025 16:59:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 26 Sep 2025 16:59:31 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 26 Sep 2025 16:59:31 GMT
ENTRYPOINT []
# Fri, 26 Sep 2025 16:59:31 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225489f525bf01be6503fa86691040d1adbbfbcaed2802478d162abfe1c04acb`  
		Last Modified: Fri, 26 Sep 2025 17:05:02 GMT  
		Size: 11.4 MB (11404500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ad39ae790cb1c9ef37862ff3eb5857f5233fa5b74cc165132b5b26b99bcec5`  
		Last Modified: Fri, 26 Sep 2025 17:05:04 GMT  
		Size: 62.7 MB (62683564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98dcf201d32f88894966977115a5a21679abf023c9f887b96dcf34b05541a0e8`  
		Last Modified: Fri, 26 Sep 2025 17:04:55 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624ea0dd81db1a5bd873d46cf678c6081ef6d357f3235b3d1b7e18529f832e61`  
		Last Modified: Fri, 26 Sep 2025 23:11:24 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fa12769610ddf91075fc71e268f7eeba82a47c23b9a49d75e6b80a6cb52f1b`  
		Last Modified: Fri, 26 Sep 2025 23:11:26 GMT  
		Size: 14.1 MB (14114124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c26ed7652deef5128d84455c4d2953378f3ab8705046f88cebede45b18359a`  
		Last Modified: Fri, 26 Sep 2025 23:11:24 GMT  
		Size: 213.5 KB (213468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:c7ad23a32fba97631e365f68ab2688732f6f1977e8b5325b3de08e1524d6a2f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d7af79a2d95d1c97799f40660bfb3ae722d503b31a253b7b2375d550cf9bb3`

```dockerfile
```

-	Layers:
	-	`sha256:431e606866f5ec4d82ba7ad7ea870a1f69af333a61b04048b02b4157fafe6853`  
		Last Modified: Sat, 27 Sep 2025 02:31:54 GMT  
		Size: 3.7 MB (3711079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:537458c8873f15c560c8759936fc2cfe48210a4248bcf6119da05fc60dcb2576`  
		Last Modified: Sat, 27 Sep 2025 02:31:55 GMT  
		Size: 21.6 KB (21568 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre25-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:f36acbdf13c38dfd1387309706ff511a5756436372aac7e251f42c0c6df19b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114671061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c46c13078d5f16ed2bb7cf849ed308b896a8191a7ba11365bea3c2aa08f8acb`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Fri, 26 Sep 2025 12:51:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 12:51:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 12:51:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
ENV JAVA_VERSION=jdk-25+36
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5e3de13a1487ecc90f8b0cddc83a6cd4e053b4cd48ddcfe5d1f19178e6089fba';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_x64_linux_hotspot_25_36.tar.gz';          ;;        arm64)          ESUM='939a1517971985363b2b57b8c6008f4bd48b91f565366d6eb3bae3aa503a05e2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64el)          ESUM='f593d6c435f6498cfbdb1ca07d7b1fa33829b159abb31b992b6234c324794dad';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='485af5746df1bf3cd46da4e7f771e6d1eae5a31db695ab819c4c2401688a6871';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_s390x_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 26 Sep 2025 16:59:31 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 26 Sep 2025 16:59:31 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 16:59:31 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 26 Sep 2025 16:59:31 GMT
WORKDIR /usr/local/tomcat
# Fri, 26 Sep 2025 16:59:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 26 Sep 2025 16:59:31 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 26 Sep 2025 16:59:31 GMT
ENV TOMCAT_MAJOR=11
# Fri, 26 Sep 2025 16:59:31 GMT
ENV TOMCAT_VERSION=11.0.11
# Fri, 26 Sep 2025 16:59:31 GMT
ENV TOMCAT_SHA512=a26b2269530fd2fc834e9b1544962f6524cf87925de43b05ad050e66b5eaa76a4ad754a2c5fc4f851baf75a0ea1b0ed8f51082300393a4c35d8c2da0d7c535bd
# Fri, 26 Sep 2025 16:59:31 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 26 Sep 2025 16:59:31 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Sep 2025 16:59:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 26 Sep 2025 16:59:31 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 26 Sep 2025 16:59:31 GMT
ENTRYPOINT []
# Fri, 26 Sep 2025 16:59:31 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c857690c2976c5cdc9dbba75b5b47f842e69228aa753933fb6e20014982c2b`  
		Last Modified: Fri, 26 Sep 2025 16:59:04 GMT  
		Size: 11.4 MB (11357662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453fdd4c29d2ae2bdd389d7ec0ac818116174fb4ddbcbbfb2e6f9c273807eb99`  
		Last Modified: Fri, 26 Sep 2025 16:59:15 GMT  
		Size: 61.6 MB (61620532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50effcf62f1eaa9e108ae03139d1966027044522fb23a1b1f330fae1875b321b`  
		Last Modified: Fri, 26 Sep 2025 16:59:04 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c43ae5fc35aa2787dfd83198e5a128efd93b9506196b869c2c242f9187f965`  
		Last Modified: Fri, 26 Sep 2025 23:11:12 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403201c553ce6fdb568f8ffeebff0c9d92c41b63b8f22b9f4ee729deb04bf683`  
		Last Modified: Fri, 26 Sep 2025 23:11:14 GMT  
		Size: 14.1 MB (14116319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534b0b2bab2c0ab1f55543626e1d24926a9c5e85cc3ffd3edcae7fac74985061`  
		Last Modified: Fri, 26 Sep 2025 23:11:12 GMT  
		Size: 212.6 KB (212563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:173f8bd9deef4c335ac1d5c986c2bddb404a0983109e346e2171441c4c55e1e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ade10c3b9150daf79b011f9a8e66b0f3af35819819b2c77585a004f61a26197`

```dockerfile
```

-	Layers:
	-	`sha256:97ff6ddb30b886c1145cb88c801f189783430f55b95ebd5424ad744728e6cf6d`  
		Last Modified: Sat, 27 Sep 2025 02:31:59 GMT  
		Size: 3.7 MB (3710742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c707e5263279e8e2b20d5da65b1a7142dd5de142cd6fc4976a92e0104c443924`  
		Last Modified: Sat, 27 Sep 2025 02:32:00 GMT  
		Size: 21.7 KB (21728 bytes)  
		MIME: application/vnd.in-toto+json
