## `tomcat:10-jre25-temurin-jammy`

```console
$ docker pull tomcat@sha256:cc934401ef6036205df25988d07fe3b6f2a841c4efbe2d8447674e477db35a1b
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
$ docker pull tomcat@sha256:4d34d83411d85aaf951f1fc76cc84a980ade92a3af0fc2bca207dae4b7e0a6c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118693344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd11b668fc5d3b3fa6779679c3d77556fbeffe725b029a5643defcfe4ed3a13`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:29:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:29:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:29:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:29:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:29:32 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:29:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Apr 2026 23:29:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:29:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:29:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:37:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 23:37:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:37:44 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 23:37:44 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 23:37:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 23:37:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 23:37:44 GMT
ENV TOMCAT_MAJOR=10
# Tue, 12 May 2026 23:37:44 GMT
ENV TOMCAT_VERSION=10.1.55
# Tue, 12 May 2026 23:37:44 GMT
ENV TOMCAT_SHA512=f36af12391a277e5c3a802a8e1a2a1e4354cd461b547d2e1a33ac0ab88d707d3fb2591e034a17b7d3a6b965a4c977a97dbf29bb81a3867e85aeec3d8d189e22e
# Tue, 12 May 2026 23:37:44 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 23:37:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 23:37:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 23:37:49 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 23:37:49 GMT
ENTRYPOINT []
# Tue, 12 May 2026 23:37:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2163368e5d72fbd8ff367d4e75341133d7d6f2e0803ae9767457a5b2d3bfd51e`  
		Last Modified: Thu, 30 Apr 2026 23:30:05 GMT  
		Size: 11.4 MB (11406200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bfbb181a4e3f2f4c48687eba9c3def1eddebd4cab5d2206cacffa36bb720cc`  
		Last Modified: Thu, 30 Apr 2026 23:30:06 GMT  
		Size: 63.0 MB (63010594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b3669d69b5182a0d63996ff6b4770086cd3d11e8867474dbd9d4ab6b06c5ab`  
		Last Modified: Thu, 30 Apr 2026 23:30:05 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612eef9635a2031d8397e2847c88ef4d1e7393104024839036cf6814cbb9569e`  
		Last Modified: Tue, 12 May 2026 23:37:58 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c535021ade6836c0ede260295aea69a667d0ed9a828983bd1a07032acc4473a`  
		Last Modified: Tue, 12 May 2026 23:37:58 GMT  
		Size: 14.3 MB (14324071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55aa3c7534def7e46df0ca15ceb822ce63a94e61ae1d9a3e32a8200726c03c92`  
		Last Modified: Tue, 12 May 2026 23:37:58 GMT  
		Size: 213.5 KB (213465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:550248f1dbda3aab6782e2af7874fc449add78fdd63706e9f4da8aa61eebe1af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a669ea8bb3ebd12855ad45a5d32a81f42d4f872b716f48560d3a34c8604c1c6`

```dockerfile
```

-	Layers:
	-	`sha256:9de92d001d5d23dbb0a2b4f8ab6684764b79062d0780553a4835f0821685cf67`  
		Last Modified: Tue, 12 May 2026 23:37:58 GMT  
		Size: 3.7 MB (3708290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3d2e74b139977ff66f54a061faa819bc0887a8253b003d50d9234626fb87e9`  
		Last Modified: Tue, 12 May 2026 23:37:58 GMT  
		Size: 21.2 KB (21208 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre25-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:3b65ea968bac6da82ec9d82ff9370733309808d9eba5cdb9887e799f11d82ad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115413380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc9157716d7c2779c17846032857d8dba58f65f5b13f6988af3e1d70c2cf74c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:30:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:30:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:30:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:30:07 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:30:07 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:30:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Apr 2026 23:30:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:30:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:30:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:37:25 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 23:37:25 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:37:25 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 23:37:25 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 23:37:25 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 23:37:25 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 23:37:25 GMT
ENV TOMCAT_MAJOR=10
# Tue, 12 May 2026 23:37:25 GMT
ENV TOMCAT_VERSION=10.1.55
# Tue, 12 May 2026 23:37:25 GMT
ENV TOMCAT_SHA512=f36af12391a277e5c3a802a8e1a2a1e4354cd461b547d2e1a33ac0ab88d707d3fb2591e034a17b7d3a6b965a4c977a97dbf29bb81a3867e85aeec3d8d189e22e
# Tue, 12 May 2026 23:37:26 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 23:37:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 23:37:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 23:37:34 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 23:37:34 GMT
ENTRYPOINT []
# Tue, 12 May 2026 23:37:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02b3899d3f6fdf65e2db872c173618ee50fa5f9b0bd944c52e93838eea6dcc9`  
		Last Modified: Thu, 30 Apr 2026 23:30:44 GMT  
		Size: 11.4 MB (11354768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9dbdbb8f943d19f73506d6644410734cbffa8c6646657eb1542fc8e6b10ed1`  
		Last Modified: Thu, 30 Apr 2026 23:30:45 GMT  
		Size: 61.9 MB (61912753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c085cc1723eb9ff96dc6aab8baf1e039501becc056f4e1721c359a2afbbf56a`  
		Last Modified: Thu, 30 Apr 2026 23:30:44 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec18c5191dec031bb3d4a3a551f6076be658a3c3751f2db955445c08a1f62709`  
		Last Modified: Tue, 12 May 2026 23:37:42 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244cd6a50450ed1641f90b717d0f883cd6a42621e59f017057e0ee323b00d755`  
		Last Modified: Tue, 12 May 2026 23:37:43 GMT  
		Size: 14.3 MB (14324287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a66f511faf2acd979878f16878f7c644d4f33732530aee66c6779b3a79f570`  
		Last Modified: Tue, 12 May 2026 23:37:42 GMT  
		Size: 212.5 KB (212510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:f44fcc47d256aa3ff3ab9b7ff5bcc360b19a8cea79ccb05b8edaddce8dfcd115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda833d9d5c99862e90b9aaaf38665e1d0280ca99a0b5a7973f683d4a1faf574`

```dockerfile
```

-	Layers:
	-	`sha256:c0f65d6d3c18a3dc62fa6f729c3c07927ef25701963041c3c9a863da5d3c21fc`  
		Last Modified: Tue, 12 May 2026 23:37:43 GMT  
		Size: 3.7 MB (3707941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2de6f63301fe06bdbf0dd9fdee97dabeecc26c50b407117ea61852240e7e815d`  
		Last Modified: Tue, 12 May 2026 23:37:42 GMT  
		Size: 21.4 KB (21358 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre25-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:df40d0e45d394891d0bfe35d477d37be4a70fdb090735e642b5ce58967fcfaf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123537097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23d3b02d9fe2b073d34c1f624ddd9b9bf50d92ba025cb868c783030c2935711`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:29:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:29:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:29:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:29:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:29:15 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:30:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Apr 2026 23:30:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:30:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:30:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 01:20:55 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 01:20:55 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 01:20:55 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 01:20:55 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 01:20:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 01:20:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 01:20:55 GMT
ENV TOMCAT_MAJOR=10
# Tue, 12 May 2026 01:20:55 GMT
ENV TOMCAT_VERSION=10.1.55
# Tue, 12 May 2026 01:20:55 GMT
ENV TOMCAT_SHA512=f36af12391a277e5c3a802a8e1a2a1e4354cd461b547d2e1a33ac0ab88d707d3fb2591e034a17b7d3a6b965a4c977a97dbf29bb81a3867e85aeec3d8d189e22e
# Tue, 12 May 2026 23:47:50 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 23:47:58 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 23:48:00 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 23:48:00 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 23:48:00 GMT
ENTRYPOINT []
# Tue, 12 May 2026 23:48:00 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09adfae83adada80107491fe4b68740c3c81f0dcd7f5f8a379f33016c2ae35d0`  
		Last Modified: Thu, 30 Apr 2026 23:30:53 GMT  
		Size: 11.9 MB (11894721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa7ef2c458aa59e2cc03df20d01c2230c7cec40ca28809e356d1a404c60ecfc`  
		Last Modified: Thu, 30 Apr 2026 23:30:54 GMT  
		Size: 62.4 MB (62411008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae5c112c97b47fce4c11c5348b61c72ff73d12a0d923784830535efa0a59945`  
		Last Modified: Thu, 30 Apr 2026 23:30:52 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0404e286a70da2e4331e177bee8e93096f1020d0ce22c23ccdf32b3bf6810c`  
		Last Modified: Tue, 12 May 2026 01:21:34 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24335638cb73579a1190eac2d119a11c40f67d6b0ceac33e964841f11f9e82c`  
		Last Modified: Tue, 12 May 2026 23:48:22 GMT  
		Size: 14.3 MB (14337281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36499d1649ae8a7b4bca5dd79a3fd6620ca0f84f862359b829d340534ebb8386`  
		Last Modified: Tue, 12 May 2026 23:48:22 GMT  
		Size: 243.2 KB (243171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:eae29aa2e3b7d22caec47626c174b4c2580f8ed566c27db286841e0923f5404c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8e2c0c8ab8ce4480f212674c85075c556b157f4525d60b1f169343944f70ca`

```dockerfile
```

-	Layers:
	-	`sha256:a211a4d5e92e5f80563164f874d74c4e4fba372bc29cfd8fde1a6135b11338b3`  
		Last Modified: Tue, 12 May 2026 23:48:22 GMT  
		Size: 3.7 MB (3711630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b06991171378d1c9f8f090f90498742957966d85a82c88ecf1350e5cde240e02`  
		Last Modified: Tue, 12 May 2026 23:48:21 GMT  
		Size: 21.3 KB (21262 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre25-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:90790986e20e868c10f526858b60967d03b4b3530cad81fdd779bbed3887868d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114745290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a487f0aa8746b321d1e41ce784f49ae69e397b3b4bc571e81509262d43f431`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:26:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:26:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:26:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:26:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:26:14 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:26:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Apr 2026 23:26:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:26:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:26:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:41:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 23:41:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:41:59 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 23:42:00 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 23:42:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 23:42:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 23:42:00 GMT
ENV TOMCAT_MAJOR=10
# Tue, 12 May 2026 23:42:00 GMT
ENV TOMCAT_VERSION=10.1.55
# Tue, 12 May 2026 23:42:00 GMT
ENV TOMCAT_SHA512=f36af12391a277e5c3a802a8e1a2a1e4354cd461b547d2e1a33ac0ab88d707d3fb2591e034a17b7d3a6b965a4c977a97dbf29bb81a3867e85aeec3d8d189e22e
# Tue, 12 May 2026 23:42:00 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 23:42:08 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 23:42:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 23:42:09 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 23:42:09 GMT
ENTRYPOINT []
# Tue, 12 May 2026 23:42:09 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc592beaf1d2de55c24bb557cd1fdaa1b9991cb09f89a8b207ac1c161b01186`  
		Last Modified: Thu, 30 Apr 2026 23:26:44 GMT  
		Size: 11.5 MB (11499427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cad66dd9d61f17530c822d80df1d1242c16da3019c260e2ab54defcf554cc7d`  
		Last Modified: Thu, 30 Apr 2026 23:26:45 GMT  
		Size: 60.5 MB (60500540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a17d43fe3f5462d687fe571cdf5035bf481a2306154f593df2b329df33e0c6`  
		Last Modified: Thu, 30 Apr 2026 23:26:43 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3276c4e31eb222b34708a0a5fe2fb68bbc680bedd3e1a895cd85364e841f5c6f`  
		Last Modified: Tue, 12 May 2026 23:42:35 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33d67f9aa08358eaad9131af724e8eeae5bac0f257dedd751a840fce49b218a`  
		Last Modified: Tue, 12 May 2026 23:42:36 GMT  
		Size: 14.3 MB (14325777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4635d1765afb7322d25288244f664c61316aa46aedba22ad59ca6c2943413011`  
		Last Modified: Tue, 12 May 2026 23:42:35 GMT  
		Size: 214.7 KB (214730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:1f59e97bbb95e482d157fefd4d9f85e883596a946a6dffce3c3703cc8ae0af4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa5b85dd0fd3012fd22e52974e0a1aa638056121d36a445f9ed56c1cac94607`

```dockerfile
```

-	Layers:
	-	`sha256:21ca0bb99a588da067d0c67753c717c081b368de0a7385493fa4f2fd3b430b6b`  
		Last Modified: Tue, 12 May 2026 23:42:35 GMT  
		Size: 3.7 MB (3709275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8770bca8ba4e83c64fe6aa01239aa405b33473eab68b3b218456cd66a76d8bd`  
		Last Modified: Tue, 12 May 2026 23:42:35 GMT  
		Size: 21.2 KB (21210 bytes)  
		MIME: application/vnd.in-toto+json
