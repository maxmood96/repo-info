## `tomcat:jre25`

```console
$ docker pull tomcat@sha256:af91027b66b59ec45f0c633fb60cb0de97d576629f6164129d7151628e8e6cb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `tomcat:jre25` - linux; amd64

```console
$ docker pull tomcat@sha256:59c88305828bd29b7a8b08fdb1d931f20267221827d3e9aab0bd930d136ec0f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126944720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1664ac695143d7d0b12dcee87a764d7c62a44f24ad7c085daf4b3b07e998132e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:21:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:21:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:21:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:21:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 22:21:31 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:21:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='0be0aa0a9578d229c2de2e9e05741d1c0726185a2017f8ce2249989f79dc9562';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 05 Feb 2026 22:21:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:21:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:21:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 23:26:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 05 Feb 2026 23:26:17 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:26:17 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 05 Feb 2026 23:26:17 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Feb 2026 23:26:17 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 05 Feb 2026 23:26:17 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 05 Feb 2026 23:26:17 GMT
ENV TOMCAT_MAJOR=11
# Thu, 05 Feb 2026 23:26:17 GMT
ENV TOMCAT_VERSION=11.0.18
# Thu, 05 Feb 2026 23:26:17 GMT
ENV TOMCAT_SHA512=e428203454e57962296e6e95705e46a1406d15569f67ea0cbd417f38fcad85e81de6fa1be62cfa660ec746312aefb87c39127eef7348e6f78cb57e9afb862ed4
# Thu, 05 Feb 2026 23:26:18 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 05 Feb 2026 23:26:23 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 23:26:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 05 Feb 2026 23:26:23 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 05 Feb 2026 23:26:23 GMT
ENTRYPOINT []
# Thu, 05 Feb 2026 23:26:23 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42012bbbfe11ad7bd6d43c1529d10aff32af295e63e8eac3e41fc41ad4157aa6`  
		Last Modified: Thu, 05 Feb 2026 22:22:04 GMT  
		Size: 20.0 MB (19969824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2446dbab5b0b25939ade360fc30b2ce6e68f9341fe011fcf428c5df21c02723b`  
		Last Modified: Thu, 05 Feb 2026 22:22:05 GMT  
		Size: 62.7 MB (62739917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7072f8f8de8d8ab33e099ae47e4e949bc40d7314faa2935320e93642cc79dfbc`  
		Last Modified: Thu, 05 Feb 2026 22:22:03 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f558078e4e15d8b9ff524340d57e6de3c9f3f100a6b873b7c87b1433492fa73f`  
		Last Modified: Thu, 05 Feb 2026 23:26:33 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853632895258f9899ea5e979aab94c9c3499b55f4c43b0d72a98b2035d974c0b`  
		Last Modified: Thu, 05 Feb 2026 23:26:33 GMT  
		Size: 14.3 MB (14298453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e02e8305d9f674038803a1f2edf6f3434b1dc3719d22039b6f93f7acba7bd9f`  
		Last Modified: Thu, 05 Feb 2026 23:26:33 GMT  
		Size: 208.0 KB (207998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre25` - unknown; unknown

```console
$ docker pull tomcat@sha256:3e5461ff78c7d29939b493c423a38a407b87a8987cb1940672c132877f523f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c732acf149e0a82010a345f668d6ab01e7224b9760e46aeed9f05e5afef062dd`

```dockerfile
```

-	Layers:
	-	`sha256:7ed7ba998621e102f900dd9081bdb59ea16181aca11734a607bb8084685bcc5f`  
		Last Modified: Thu, 05 Feb 2026 23:26:33 GMT  
		Size: 3.1 MB (3128596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea976e9fb842b137827e077ed21ebf88da21821089ecc08706df37b728045360`  
		Last Modified: Thu, 05 Feb 2026 23:26:32 GMT  
		Size: 24.0 KB (24032 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre25` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:8fa0dd1a2d8714c9accb82e6d2bf3dcdb3833a22f8c3bece242d31d911e8fc58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124635020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11965827e41c66efb4d78f88ad89d29699429e6e671edf4c8a89ff7288fb41e0`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:20:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:20:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:20:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:20:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 22:20:39 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:20:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='0be0aa0a9578d229c2de2e9e05741d1c0726185a2017f8ce2249989f79dc9562';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 05 Feb 2026 22:20:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:20:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:20:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 23:37:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 05 Feb 2026 23:37:35 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:37:35 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 05 Feb 2026 23:37:35 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Feb 2026 23:37:35 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 05 Feb 2026 23:37:35 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 05 Feb 2026 23:37:35 GMT
ENV TOMCAT_MAJOR=11
# Thu, 05 Feb 2026 23:37:35 GMT
ENV TOMCAT_VERSION=11.0.18
# Thu, 05 Feb 2026 23:37:35 GMT
ENV TOMCAT_SHA512=e428203454e57962296e6e95705e46a1406d15569f67ea0cbd417f38fcad85e81de6fa1be62cfa660ec746312aefb87c39127eef7348e6f78cb57e9afb862ed4
# Thu, 05 Feb 2026 23:37:35 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 05 Feb 2026 23:37:41 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 23:37:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 05 Feb 2026 23:37:42 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 05 Feb 2026 23:37:42 GMT
ENTRYPOINT []
# Thu, 05 Feb 2026 23:37:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9e06a13c36f8c36519ee375be98a76e16828d561bafce2d603cfdf3dee3302`  
		Last Modified: Thu, 05 Feb 2026 22:21:10 GMT  
		Size: 19.6 MB (19553926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1a04807beff52e0f164347af0435132f0316e0ff3391dccb372b58a9fcf627`  
		Last Modified: Thu, 05 Feb 2026 22:21:12 GMT  
		Size: 61.7 MB (61703395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df62165a91bde2aacaadb757c5de858035f27a40a0f353502ee19c71a85358e`  
		Last Modified: Thu, 05 Feb 2026 22:21:10 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f075398c9b1cc2028e98da176ffd411f42277591ba93cfb58cde08e306c50c5e`  
		Last Modified: Thu, 05 Feb 2026 23:37:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ee390575de5f38f541b191a421c54ac12cd840f7c961246a6a9cbdf63ad44d`  
		Last Modified: Thu, 05 Feb 2026 23:37:51 GMT  
		Size: 14.3 MB (14303775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad08571cda89cf49494c6605a3c43d321ba6cf20c1fba65f0fcb4a10ab11c047`  
		Last Modified: Thu, 05 Feb 2026 23:37:51 GMT  
		Size: 207.6 KB (207586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre25` - unknown; unknown

```console
$ docker pull tomcat@sha256:d0f40d2d40a83e6d20bc9c4f62948a5f634ac8a067fe2481af2c1bce6aaee3ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3153431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3689a16ec5800131d16befa9c2a95dbd2cfe173792e76e2d7b2a213eea41aa8e`

```dockerfile
```

-	Layers:
	-	`sha256:a72b748e31f01d257232eddffb4af8230513754e2adc283b40bbf62fc5986cae`  
		Last Modified: Thu, 05 Feb 2026 23:37:51 GMT  
		Size: 3.1 MB (3129142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf6412ddce5bb8b368abb0c48d06387100f4922825ce1730bbce883645b73d7`  
		Last Modified: Thu, 05 Feb 2026 23:37:51 GMT  
		Size: 24.3 KB (24289 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre25` - linux; ppc64le

```console
$ docker pull tomcat@sha256:1bf641d663acbb85b114c65512db94b2ca4e06f5c30a003c4736dfb2759e8d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132558652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7be97fce8db2ca59b0720ff182f638ef3a345917feb6e99a37c61cea4cedbfa`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:35:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:35:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 22:35:21 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:36:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='0be0aa0a9578d229c2de2e9e05741d1c0726185a2017f8ce2249989f79dc9562';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 05 Feb 2026 22:36:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:36:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:36:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 06 Feb 2026 00:57:08 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 06 Feb 2026 00:57:08 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:57:08 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 06 Feb 2026 00:57:09 GMT
WORKDIR /usr/local/tomcat
# Fri, 06 Feb 2026 00:57:09 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 06 Feb 2026 00:57:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 06 Feb 2026 00:57:09 GMT
ENV TOMCAT_MAJOR=11
# Fri, 06 Feb 2026 00:57:09 GMT
ENV TOMCAT_VERSION=11.0.18
# Fri, 06 Feb 2026 00:57:09 GMT
ENV TOMCAT_SHA512=e428203454e57962296e6e95705e46a1406d15569f67ea0cbd417f38fcad85e81de6fa1be62cfa660ec746312aefb87c39127eef7348e6f78cb57e9afb862ed4
# Fri, 06 Feb 2026 00:57:09 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 06 Feb 2026 00:57:24 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Feb 2026 00:57:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 06 Feb 2026 00:57:27 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 06 Feb 2026 00:57:27 GMT
ENTRYPOINT []
# Fri, 06 Feb 2026 00:57:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ff668804b4ac673521b2d97971b5e175d654de15faa616d71f627c3e76a7a5`  
		Last Modified: Thu, 05 Feb 2026 22:36:38 GMT  
		Size: 21.5 MB (21535422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a07a7642714a5f5330a7237b4d073791cfcb554f2e57b53bb91929674a8ee3`  
		Last Modified: Thu, 05 Feb 2026 22:36:39 GMT  
		Size: 62.2 MB (62160975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1cfd62a8647a91c61a639177dcbe3488f2e5019cfeb6ff30b86fb38b0837ee`  
		Last Modified: Thu, 05 Feb 2026 22:36:36 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f6bf24e52279317b7e5363a19addb1243deba52296492ce6378faecd11d770`  
		Last Modified: Fri, 06 Feb 2026 00:57:59 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b349725acd479a1003bdba282c511e1da5365afd25f4f696ccb5b6c38eb115b`  
		Last Modified: Fri, 06 Feb 2026 00:57:59 GMT  
		Size: 14.3 MB (14314302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc8defd952778dd1d423d019801be7187d760d997994c88d76a668a29f362d6`  
		Last Modified: Fri, 06 Feb 2026 00:57:59 GMT  
		Size: 239.3 KB (239276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre25` - unknown; unknown

```console
$ docker pull tomcat@sha256:588e01cab44010510a1f0f6c513a7926fb5e262f7490dc8967970f918cda7749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8371c0b09ea2222dc560865537ee1eeadc9e72b7ef2502dbd7434c1f3f12aa68`

```dockerfile
```

-	Layers:
	-	`sha256:d80675d3d18a71ff45ec2ec2a4055bf904bbe6c735b9772be021c8ed5479908d`  
		Last Modified: Fri, 06 Feb 2026 00:57:59 GMT  
		Size: 3.1 MB (3131941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c49b48bdfb28d496a6be30a8096e4090fb8dc69912389c2140c1d35880d8fbcd`  
		Last Modified: Fri, 06 Feb 2026 00:57:59 GMT  
		Size: 24.1 KB (24139 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre25` - linux; riscv64

```console
$ docker pull tomcat@sha256:688545eec0dd04420f9fa86e3d3e432f5f0da8581c9090f73c1dbf407f47ef9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132568570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873544af1861c46d8cfaea348d686c63397970107e820dc1e26b28566672f261`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 13 Jan 2026 06:14:56 GMT
ARG RELEASE
# Tue, 13 Jan 2026 06:14:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 06:14:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 06:14:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 06:15:46 GMT
ADD file:8d0655de001e92042901c645c76202ac355acb6fa186561e7344a0829ffd983d in / 
# Tue, 13 Jan 2026 06:15:51 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 18:37:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 19 Jan 2026 18:37:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Jan 2026 18:37:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 19 Jan 2026 18:37:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Jan 2026 18:37:47 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Sun, 08 Feb 2026 00:37:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='0be0aa0a9578d229c2de2e9e05741d1c0726185a2017f8ce2249989f79dc9562';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 08 Feb 2026 00:37:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 08 Feb 2026 00:37:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 08 Feb 2026 00:37:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Feb 2026 13:44:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 09 Feb 2026 13:44:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 13:44:59 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 09 Feb 2026 13:44:59 GMT
WORKDIR /usr/local/tomcat
# Mon, 09 Feb 2026 13:44:59 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 09 Feb 2026 13:44:59 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 09 Feb 2026 13:44:59 GMT
ENV TOMCAT_MAJOR=11
# Mon, 09 Feb 2026 13:44:59 GMT
ENV TOMCAT_VERSION=11.0.18
# Mon, 09 Feb 2026 13:44:59 GMT
ENV TOMCAT_SHA512=e428203454e57962296e6e95705e46a1406d15569f67ea0cbd417f38fcad85e81de6fa1be62cfa660ec746312aefb87c39127eef7348e6f78cb57e9afb862ed4
# Mon, 09 Feb 2026 13:45:02 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 09 Feb 2026 13:46:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 13:46:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 09 Feb 2026 13:46:29 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 09 Feb 2026 13:46:29 GMT
ENTRYPOINT []
# Mon, 09 Feb 2026 13:46:29 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f151392858868452ec0f1f8d2947624e8dcdecf23bce587cfbd7c38a3264f9df`  
		Last Modified: Tue, 13 Jan 2026 06:36:06 GMT  
		Size: 31.0 MB (30953090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef99bb7a393dfd3bc0f32efd5dee5d956223c9ac454ba962e7a3148dba3efdee`  
		Last Modified: Mon, 19 Jan 2026 18:42:30 GMT  
		Size: 11.6 MB (11570389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cfdb109467641f22cf85fa40a0af00867485143be5d58e62f43071fb0fbbc1`  
		Last Modified: Sun, 08 Feb 2026 00:40:13 GMT  
		Size: 61.4 MB (61447165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9123fc57661c72923a5de44840dd87dd54cefa61c126df2d8a3a5eb38be0789`  
		Last Modified: Sun, 08 Feb 2026 00:40:03 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7118bd4e99b21202fd47f5ed33170ecb32050df7e9fccdde6954fd1cce2167d`  
		Last Modified: Mon, 09 Feb 2026 13:48:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80796c012c03b747fd0e289c7ea88ce878cdfef5e3d3288785893cbb972c3c40`  
		Last Modified: Mon, 09 Feb 2026 13:48:36 GMT  
		Size: 14.5 MB (14487882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ed6397d5463040dcba4e0db94624b6658d84e86aeebb504b60b504a5378b78`  
		Last Modified: Mon, 09 Feb 2026 13:48:36 GMT  
		Size: 14.1 MB (14107527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre25` - unknown; unknown

```console
$ docker pull tomcat@sha256:24f4668732b836902c74248f8c86343fe5991f9ba085cdc3503e4dc9047afef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3144779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19612ec4f3ba3a9e7d111d48b40de4ac46b1039fb3a9efe9df571a13bf083499`

```dockerfile
```

-	Layers:
	-	`sha256:236fb2bdb20bd01b19c1a91a0b377a8290b73d77d999d11e4bd1625f47e1fe7e`  
		Last Modified: Mon, 09 Feb 2026 13:48:32 GMT  
		Size: 3.1 MB (3120637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:977229c9c0a9ac69eab22f8ec754ea0a6dfad8a182bd78e2e78373b3ce368d84`  
		Last Modified: Mon, 09 Feb 2026 13:48:31 GMT  
		Size: 24.1 KB (24142 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre25` - linux; s390x

```console
$ docker pull tomcat@sha256:1dc931afe3453e57b815e4c824973fd16a42d2821f7091378dbaf1c9e91aaca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123888512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293ec314c987b20d0239f4037fec813ac4b5e3456a730a1ae1cf87a2d674927a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 13 Jan 2026 06:29:20 GMT
ARG RELEASE
# Tue, 13 Jan 2026 06:29:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 06:29:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 06:29:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 06:29:22 GMT
ADD file:55a7874afa0094b7b4c6edc68b58164a34177fa761bc6e673ddb0c846b91f26f in / 
# Tue, 13 Jan 2026 06:29:22 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:25:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:25:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:25:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:25:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 22:25:17 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:25:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='0be0aa0a9578d229c2de2e9e05741d1c0726185a2017f8ce2249989f79dc9562';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 05 Feb 2026 22:25:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:25:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:25:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 23:15:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 05 Feb 2026 23:15:24 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:15:24 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 05 Feb 2026 23:15:24 GMT
WORKDIR /usr/local/tomcat
# Thu, 05 Feb 2026 23:15:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 05 Feb 2026 23:15:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 05 Feb 2026 23:15:24 GMT
ENV TOMCAT_MAJOR=11
# Thu, 05 Feb 2026 23:15:24 GMT
ENV TOMCAT_VERSION=11.0.18
# Thu, 05 Feb 2026 23:15:24 GMT
ENV TOMCAT_SHA512=e428203454e57962296e6e95705e46a1406d15569f67ea0cbd417f38fcad85e81de6fa1be62cfa660ec746312aefb87c39127eef7348e6f78cb57e9afb862ed4
# Thu, 05 Feb 2026 23:15:24 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 05 Feb 2026 23:15:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 23:15:30 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 05 Feb 2026 23:15:30 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 05 Feb 2026 23:15:30 GMT
ENTRYPOINT []
# Thu, 05 Feb 2026 23:15:30 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:88318e41cf944fd93c8b2fdfaeb1378b17ed0e2440ef9811f9820449bf19a6ad`  
		Last Modified: Tue, 13 Jan 2026 06:36:13 GMT  
		Size: 29.9 MB (29909204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08fb122795d8a61934eab679b33feab1bbcbef315676225a38774a7f14af536`  
		Last Modified: Thu, 05 Feb 2026 22:26:12 GMT  
		Size: 19.1 MB (19096168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff20fd9953e14052fb833c12f396d564dd1f219b9ddbfa073f3757bf1651f8b5`  
		Last Modified: Thu, 05 Feb 2026 22:26:13 GMT  
		Size: 60.4 MB (60354570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c54541ba4c3e48ffe8469bbb04d524a54a05cde6abe889283c2188f6bc8dd8c`  
		Last Modified: Thu, 05 Feb 2026 22:26:11 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c539b61a0838f835cd4c94c0c56912f06f80c24ee5940b713f0fed0c513b45a7`  
		Last Modified: Thu, 05 Feb 2026 23:15:44 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23591145b7f98dcc8a3555d58012cf0b495371b7acf1a6e1470b6a72625fc89c`  
		Last Modified: Thu, 05 Feb 2026 23:15:45 GMT  
		Size: 14.3 MB (14310559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce0633ab2c7e6e128a32860d9cf712bde8ad560a99c8be0389f293767e99136`  
		Last Modified: Thu, 05 Feb 2026 23:15:44 GMT  
		Size: 215.5 KB (215494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre25` - unknown; unknown

```console
$ docker pull tomcat@sha256:ff3c8497ef6a0892148702c6a6d127cffeda5e55b7935f0bd569e19b377718d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74232ba8726d50c31dc27611ed285423eb54dd62265cb3a4628f3b58f5b8a35f`

```dockerfile
```

-	Layers:
	-	`sha256:706c7dbc73ddab1a51c4d2166e8c8fd744b9db6624f1a07adc3fc4b84b2627bb`  
		Last Modified: Thu, 05 Feb 2026 23:15:45 GMT  
		Size: 3.1 MB (3130193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e67d010a08ea7685761a3254a80051b5e49cdccbb88bfaf790c02987f5b6572`  
		Last Modified: Thu, 05 Feb 2026 23:15:44 GMT  
		Size: 24.0 KB (24032 bytes)  
		MIME: application/vnd.in-toto+json
