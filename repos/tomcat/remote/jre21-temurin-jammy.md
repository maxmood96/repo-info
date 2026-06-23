## `tomcat:jre21-temurin-jammy`

```console
$ docker pull tomcat@sha256:0182cae195c96c912148b0c8b1472ab829513ed352a2a8257e99763ec70518c6
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

### `tomcat:jre21-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:22eb9fffdf981708209cd476786f91c4407ca1870940cf5cd43c41cb942009a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116376527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:287a5e77e4b3bb0162147381c8468c65e5183fc3df94258bfc96cf8419d34489`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:16:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:16:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:16:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:16:08 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:16:08 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 15 May 2026 21:16:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:16:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:16:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:16:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 23:11:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 22 Jun 2026 23:11:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 23:11:15 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 22 Jun 2026 23:11:15 GMT
WORKDIR /usr/local/tomcat
# Mon, 22 Jun 2026 23:11:15 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 22 Jun 2026 23:11:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 22 Jun 2026 23:11:15 GMT
ENV TOMCAT_MAJOR=11
# Mon, 22 Jun 2026 23:11:15 GMT
ENV TOMCAT_VERSION=11.0.23
# Mon, 22 Jun 2026 23:11:15 GMT
ENV TOMCAT_SHA512=f5acb7a1e5ad60dea682ffe16cf075596f0e7b62e460828eb176639714d125ab08c763753fb709e3626ce6f42712c281b4ccf54930354aa07325550d6e6cbdac
# Mon, 22 Jun 2026 23:11:15 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 22 Jun 2026 23:11:20 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 23:11:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 22 Jun 2026 23:11:21 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 22 Jun 2026 23:11:21 GMT
ENTRYPOINT []
# Mon, 22 Jun 2026 23:11:21 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5a0b6cb36c205fa8c9ef45406ef43ec624251108a5888140648cc4b33c6c55`  
		Last Modified: Fri, 15 May 2026 21:16:25 GMT  
		Size: 16.2 MB (16152745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49518c28c0b3c62624726aad57e80683d40b375b2400643477eee9fb6a278c98`  
		Last Modified: Fri, 15 May 2026 21:16:26 GMT  
		Size: 53.1 MB (53122802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41162acdcc29a9fd0a1e7740bb879e5192914f5814a43217fbc9222a7521947e`  
		Last Modified: Fri, 15 May 2026 21:16:24 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed0fd558ca3b009513993bf77af60ee5c03ce381c4d86b75dbda8fd93467027`  
		Last Modified: Fri, 15 May 2026 21:16:25 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b6d27b5c1af9a53cc9e8cc5bb4f4a92df71cf2796e9a867721dadbfd4cb29e`  
		Last Modified: Mon, 22 Jun 2026 23:11:30 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed652c2779fd4b91e88939a8a3b92620f5c863f95e8f81e93547f5733e122648`  
		Last Modified: Mon, 22 Jun 2026 23:11:30 GMT  
		Size: 14.4 MB (14384254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9423c693bb772ce1c4d4aa9807393f19680b94ea05b40a223354f98859a5a50`  
		Last Modified: Mon, 22 Jun 2026 23:11:30 GMT  
		Size: 3.0 MB (2977397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:c125f15e41de27f969bb4ea537ed6fd9104fc30274a83a8d7c7e0c567d9e0e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3966851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ccc5119f80e99d971f3f5b76ac04403f14329235b4fba3b9f0844a68de6e18`

```dockerfile
```

-	Layers:
	-	`sha256:36e53727ad8e6e5176dd9d15f8b2671041753b3373c5a9e777a6cff9e7ebe574`  
		Last Modified: Mon, 22 Jun 2026 23:11:30 GMT  
		Size: 3.9 MB (3945301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bab6f5d3dbf0aa4e0cb5aa67838af135820f0a021c7514bc6fd6f24b46d20cfc`  
		Last Modified: Mon, 22 Jun 2026 23:11:30 GMT  
		Size: 21.6 KB (21550 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:23550faa93530349b103e39fb71981a84669a8f3e46ebb43e1e0d8de506f3881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113207369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c927d2fe47d1900843eca9f76a59ef483781c6cf997da2ac3e8adf254bec149c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:15:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:15:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:15:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:15:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:15:49 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 15 May 2026 21:16:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:16:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:16:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:16:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 23:10:33 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 22 Jun 2026 23:10:33 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 23:10:33 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 22 Jun 2026 23:10:33 GMT
WORKDIR /usr/local/tomcat
# Mon, 22 Jun 2026 23:10:33 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 22 Jun 2026 23:10:33 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 22 Jun 2026 23:10:33 GMT
ENV TOMCAT_MAJOR=11
# Mon, 22 Jun 2026 23:10:33 GMT
ENV TOMCAT_VERSION=11.0.23
# Mon, 22 Jun 2026 23:10:33 GMT
ENV TOMCAT_SHA512=f5acb7a1e5ad60dea682ffe16cf075596f0e7b62e460828eb176639714d125ab08c763753fb709e3626ce6f42712c281b4ccf54930354aa07325550d6e6cbdac
# Mon, 22 Jun 2026 23:10:33 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 22 Jun 2026 23:10:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 23:10:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 22 Jun 2026 23:10:40 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 22 Jun 2026 23:10:40 GMT
ENTRYPOINT []
# Mon, 22 Jun 2026 23:10:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57ad989666c9e0dfc45a5f5a1a6ec026fe709513407113fd1d938cb641e13ca`  
		Last Modified: Fri, 15 May 2026 21:16:03 GMT  
		Size: 16.1 MB (16076205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2cd678502086cef6dba8f3127d023e5cdce1664a09143a8511e49ecc27f1c7`  
		Last Modified: Fri, 15 May 2026 21:16:28 GMT  
		Size: 52.3 MB (52314965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5318b9fee19514f8672bc32ae5b580b0eb3db47498220a70a4aee4675c2f79`  
		Last Modified: Fri, 15 May 2026 21:16:26 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671fab38f8b8067234c315c0ed43db9cd49bf63d19d293012dc0fb862a82caa6`  
		Last Modified: Fri, 15 May 2026 21:16:26 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac13c7a72d969f6d62f7d7593dbcf83b32b6e406d8bd91d4ae1fd387a040d67`  
		Last Modified: Mon, 22 Jun 2026 23:10:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24485a82caa9ead2e7f02ccb71b3290fc5703994f11824c550fa46fa31449ea5`  
		Last Modified: Mon, 22 Jun 2026 23:10:50 GMT  
		Size: 14.4 MB (14383671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfaa16a8ebc1ee367a860148b0911259e63134da340b336fb822454ed398fac`  
		Last Modified: Mon, 22 Jun 2026 23:10:49 GMT  
		Size: 2.8 MB (2823262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:dc08159e6c0fb05d09001dc216d79f6b3f729a2482dbe824f21c47b5f04c6b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3966691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656744ead962625e8ed3b5cf48c3814101549a90910b05dcc9a4f6e684189f02`

```dockerfile
```

-	Layers:
	-	`sha256:f772570c93ac9d45ca488b635159dcb29fde2741dc3052528853268a634c0c35`  
		Last Modified: Mon, 22 Jun 2026 23:10:49 GMT  
		Size: 3.9 MB (3944982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ba11421a23a324fb501d81c4b780cd65c84fee49fac179503d87eb37bd2c5c9`  
		Last Modified: Mon, 22 Jun 2026 23:10:49 GMT  
		Size: 21.7 KB (21709 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:d6bc4c0e65ddc79b534d2d2e7e020831e02729c8dc609f2d31a10932d0998fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.2 MB (123176777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78e583829b68c013524e66f063dd4ca4b6f3dbf1fabe941b8dc64304f0778e1`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 09 May 2026 04:51:05 GMT
ARG RELEASE
# Sat, 09 May 2026 04:51:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:51:05 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:51:11 GMT
ADD file:bd6823713e9d7c2f4ea7ca1d6d549e2bed56e8ce1fc6f98e14f6eb3a3371ebfa in / 
# Sat, 09 May 2026 04:51:12 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:10:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:10:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:10:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:10:20 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:10:20 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 15 May 2026 21:13:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:13:46 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:13:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:13:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 23:10:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 22 Jun 2026 23:10:51 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 23:10:51 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 22 Jun 2026 23:10:52 GMT
WORKDIR /usr/local/tomcat
# Mon, 22 Jun 2026 23:10:52 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 22 Jun 2026 23:10:52 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 22 Jun 2026 23:10:52 GMT
ENV TOMCAT_MAJOR=11
# Mon, 22 Jun 2026 23:10:52 GMT
ENV TOMCAT_VERSION=11.0.23
# Mon, 22 Jun 2026 23:10:52 GMT
ENV TOMCAT_SHA512=f5acb7a1e5ad60dea682ffe16cf075596f0e7b62e460828eb176639714d125ab08c763753fb709e3626ce6f42712c281b4ccf54930354aa07325550d6e6cbdac
# Mon, 22 Jun 2026 23:10:52 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 22 Jun 2026 23:11:01 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 23:11:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 22 Jun 2026 23:11:03 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 22 Jun 2026 23:11:03 GMT
ENTRYPOINT []
# Mon, 22 Jun 2026 23:11:03 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6970bf2b5ef1698cb51975b1a652f6511f8fd9f88ae7b247e3ee32591d975e63`  
		Last Modified: Sat, 09 May 2026 05:25:11 GMT  
		Size: 34.6 MB (34646720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74563760a17437dfb610242b605ae18edc6feef6143f0f512cfd8f6e66afb898`  
		Last Modified: Fri, 15 May 2026 21:10:51 GMT  
		Size: 17.6 MB (17625928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51bd9a51d9fa4b694f311f377fa7acde8bd891ae93584ee47df6fbed41829f`  
		Last Modified: Fri, 15 May 2026 21:14:14 GMT  
		Size: 53.1 MB (53148924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6dd6ef94452a9bf7433252b7d8b34ac784765754304b966e47be88e4dd4289`  
		Last Modified: Fri, 15 May 2026 21:14:12 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca9e140d2130996acc30c3942f62b2df386f454d719afedff4de995c0f455e9`  
		Last Modified: Fri, 15 May 2026 21:14:12 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22c76314f51121f8da5889228af870f143ea9843b234f9f32f3ef4209888b72`  
		Last Modified: Mon, 22 Jun 2026 23:11:35 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7a5b661d3031065372042b72bd0299d6e15e73c57e2b6944338a3900bdcaf3`  
		Last Modified: Mon, 22 Jun 2026 23:11:35 GMT  
		Size: 14.4 MB (14396209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4675742f8a605e68591227ac9f364b13836108d804e2b46e64af7ed372d6294b`  
		Last Modified: Mon, 22 Jun 2026 23:11:35 GMT  
		Size: 3.4 MB (3356353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:93c04cb69a6ba31826a2c4483be506a09b5fabc5ad61e9b594b105dc78eaa6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3971003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac5547294324532d065e331c860d8ae445ea155c13e5c4e68664c3790a73e89`

```dockerfile
```

-	Layers:
	-	`sha256:63b4185f4c990c13d40737cc860b2fc6a15c063ed13bce840f4619fa7f61cec3`  
		Last Modified: Mon, 22 Jun 2026 23:11:35 GMT  
		Size: 3.9 MB (3949395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:225231fa86d64fc287a77fd2c6ca12cfb6c032f5e7d7bb761efe4332076ed5ed`  
		Last Modified: Mon, 22 Jun 2026 23:11:35 GMT  
		Size: 21.6 KB (21608 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre21-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:cb77735ab385cc8f364477d10ae35b041954ca3874923d76d95eb3b618802c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111072257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc738e784151af66166830831d60a047f92ec8032b1a4851c7ed0233b6cb7baf`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 09 May 2026 04:50:49 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:51 GMT
ADD file:17ca3274b34edf79b2d4401a24984fb8dc339a8298f0e3703af025f51b67336b in / 
# Sat, 09 May 2026 04:50:51 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:12:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:12:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:12:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:12:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:12:14 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 15 May 2026 21:13:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 15 May 2026 21:13:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 21:13:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 21:13:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 23:09:43 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 22 Jun 2026 23:09:43 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 23:09:43 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 22 Jun 2026 23:09:43 GMT
WORKDIR /usr/local/tomcat
# Mon, 22 Jun 2026 23:09:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 22 Jun 2026 23:09:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 22 Jun 2026 23:09:43 GMT
ENV TOMCAT_MAJOR=11
# Mon, 22 Jun 2026 23:09:43 GMT
ENV TOMCAT_VERSION=11.0.23
# Mon, 22 Jun 2026 23:09:43 GMT
ENV TOMCAT_SHA512=f5acb7a1e5ad60dea682ffe16cf075596f0e7b62e460828eb176639714d125ab08c763753fb709e3626ce6f42712c281b4ccf54930354aa07325550d6e6cbdac
# Mon, 22 Jun 2026 23:09:45 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 22 Jun 2026 23:09:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 23:09:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 22 Jun 2026 23:09:50 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 22 Jun 2026 23:09:50 GMT
ENTRYPOINT []
# Mon, 22 Jun 2026 23:09:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c8acb84faa73cc102915433858f425bdd6749804de64fd2e27d5f491f005a91b`  
		Last Modified: Sat, 09 May 2026 05:25:25 GMT  
		Size: 28.2 MB (28202305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408cb997e338ec619cbc0e124d371f4da963043155539b97992361ce020bfd40`  
		Last Modified: Fri, 15 May 2026 21:13:18 GMT  
		Size: 16.2 MB (16151221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ec73ceb9d0904687d4f1f290e71a922be8d5c98fa5b99f8cd8db65450b2f7d`  
		Last Modified: Fri, 15 May 2026 21:14:30 GMT  
		Size: 49.7 MB (49668499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2eaae3a999974e2635a9b6948ea7f4257007216542f9073da05ee58efd9882`  
		Last Modified: Fri, 15 May 2026 21:14:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e619a55d6cda64904d8392ccef88a47bf744661114096424fa7db60ffb730501`  
		Last Modified: Fri, 15 May 2026 21:14:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45a4d6523f4bcd7a1ce423e9559d7a58699f9c0a47619baad35030af033c6eb`  
		Last Modified: Mon, 22 Jun 2026 23:10:04 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca121725c4ec98d0e67eb9b9334da478e3bbbefa06debbe2251fda5c4112eae4`  
		Last Modified: Mon, 22 Jun 2026 23:10:04 GMT  
		Size: 14.4 MB (14386338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d714fc9d9e339abbd6a1318084edd3b2bd6b2ed92f12e440515f9fd49b795f43`  
		Last Modified: Mon, 22 Jun 2026 23:10:04 GMT  
		Size: 2.7 MB (2661247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre21-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:e06e0033fce546ed3dc2c28f1abbaeac96237fbcdab6dd3f7105d93f3fa4bd47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20c57fa149f3d455a6af3a62eb1f2d54f8b3b699809972bb09f900ca383613e`

```dockerfile
```

-	Layers:
	-	`sha256:4ffe53729c7a29c81ac6dbcdc966882491748db3db7ed4d23f0531fb6f31ef06`  
		Last Modified: Mon, 22 Jun 2026 23:10:04 GMT  
		Size: 3.9 MB (3946892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:778f9bb4ef431e95b67568384c88e9e5918b9ef996cb18c97908934f685ab9f7`  
		Last Modified: Mon, 22 Jun 2026 23:10:04 GMT  
		Size: 21.6 KB (21550 bytes)  
		MIME: application/vnd.in-toto+json
