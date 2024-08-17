## `tomcat:9-jre17-temurin-jammy`

```console
$ docker pull tomcat@sha256:870efba3784aca22e6aab22dd57fcc43b97c4e4ed8e3f9320a73ee4895163965
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `tomcat:9-jre17-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:238a3038d220e840a4424c262fadceb1c04cc1f05b5bc09a609816093036b902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103616196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b2225c873fba1a8c841f4ab9895f1b193c0f7bca0effe26468044ee0228998`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 06 Aug 2024 08:03:42 GMT
ARG RELEASE
# Tue, 06 Aug 2024 08:03:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Aug 2024 08:03:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Aug 2024 08:03:42 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 06 Aug 2024 08:03:42 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 06 Aug 2024 08:03:42 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 06 Aug 2024 08:03:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 06 Aug 2024 08:03:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 08:03:42 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
WORKDIR /usr/local/tomcat
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 08:03:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 08:03:42 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_MAJOR=9
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_VERSION=9.0.93
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_SHA512=3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d
# Tue, 06 Aug 2024 08:03:42 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 06 Aug 2024 08:03:42 GMT
ENTRYPOINT []
# Tue, 06 Aug 2024 08:03:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9bd9906fae2af9b98f929fef09d486905c0599093bb299b441e7eed58ada7`  
		Last Modified: Sat, 17 Aug 2024 01:10:02 GMT  
		Size: 12.9 MB (12870875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32d681e6b995fe897bf388fc57befba67a3692e3f94f2493558cea4f6aab3b4`  
		Last Modified: Sat, 17 Aug 2024 01:13:28 GMT  
		Size: 47.3 MB (47280215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabdd0a18314116a0ebaebbd74aa891cbb1da4650890b6187e36c306bbdca902`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd24317609f1b5444d777c0434ab11020010745e5fa797d14158b433e7d085e`  
		Last Modified: Sat, 17 Aug 2024 01:13:21 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa87cff4f93508603288b46410e816df2d59fb6bb25f117e08d2dde306b57326`  
		Last Modified: Sat, 17 Aug 2024 04:07:38 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a86890c39ea6f593a2051c45ee2c8a5a8dd1dcc144c5c02ee6d44b14f554a9d`  
		Last Modified: Sat, 17 Aug 2024 04:07:39 GMT  
		Size: 12.8 MB (12804336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251d4e189e9aefc02322eb75a820a94fbc5219d9db2fe235f6fda7165faee1e2`  
		Last Modified: Sat, 17 Aug 2024 04:07:39 GMT  
		Size: 217.8 KB (217829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:f1b96ce6d6b84b43136e8859ac24d1a9a8a3cdf66298534929eb3695ca37d10a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3550680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68736b01a2bf86415d45b55ea6277b7a1d21d3425953b45e76f46304ff617eb9`

```dockerfile
```

-	Layers:
	-	`sha256:f3909a91486b33ff57778326c78e1be0c3edaf3b6fab01ec019710fb5afbed8d`  
		Last Modified: Sat, 17 Aug 2024 04:07:38 GMT  
		Size: 3.5 MB (3528848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60f56b5af750096ccfed388c5cd70d792fbb5a2c2d702ff97241cdd0524628ed`  
		Last Modified: Sat, 17 Aug 2024 04:07:38 GMT  
		Size: 21.8 KB (21832 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:2fde581529b2bf497cb38a47ed46365f1ed77c0698e72f2664194a422afbe844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97873542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f66074146c7ea97ea61f9f9a9ad18ff61081f6a00510ee68df5853712677aa1`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 06 Aug 2024 08:03:42 GMT
ARG RELEASE
# Tue, 06 Aug 2024 08:03:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Aug 2024 08:03:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Aug 2024 08:03:42 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 06 Aug 2024 08:03:42 GMT
ADD file:ef971273c60fcf0d0b0a4e71a5e5421060cd7c316f1d9af068a193c23dc81d31 in / 
# Tue, 06 Aug 2024 08:03:42 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 06 Aug 2024 08:03:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 06 Aug 2024 08:03:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 08:03:42 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
WORKDIR /usr/local/tomcat
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 08:03:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 08:03:42 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_MAJOR=9
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_VERSION=9.0.93
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_SHA512=3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d
# Tue, 06 Aug 2024 08:03:42 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 06 Aug 2024 08:03:42 GMT
ENTRYPOINT []
# Tue, 06 Aug 2024 08:03:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f2a599e193acb4c0e6567f9f5e0b191f59e170d5062a49d73761ee20623e6788`  
		Last Modified: Fri, 09 Aug 2024 02:12:36 GMT  
		Size: 27.5 MB (27535050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b092dd5a78dc4cf071309a2972d23807d1b19451ad8ff7aae557e8af16e175a`  
		Last Modified: Sat, 17 Aug 2024 01:35:54 GMT  
		Size: 12.5 MB (12463290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8308c7b76aa51393531244b73fd89897b6afbfa6c6c4171da12982614da4dc35`  
		Last Modified: Sat, 17 Aug 2024 01:39:26 GMT  
		Size: 44.9 MB (44944545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c641e075d513f73e58e24690d8ff37ba4f4f34273aae222d9908e3043b55d5f`  
		Last Modified: Sat, 17 Aug 2024 01:39:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8805834ac6a76c6634ad79bfdb9b866ec9a4abd3e9c5d80c103ba630d73d74f8`  
		Last Modified: Sat, 17 Aug 2024 01:39:21 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21003cf2a8e02d4c5e1e0a464e97637299f515a690a72b5a8ae348caba548634`  
		Last Modified: Sat, 17 Aug 2024 05:15:10 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfd53a7ca8351fd79fd70f39a23df6d1ce4ce65e03aa2e3fcd202f91d8ea53e`  
		Last Modified: Sat, 17 Aug 2024 05:17:24 GMT  
		Size: 12.7 MB (12737515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1529b0decfc5696cdb63db10b3d4297517196a41914707aba38f5f1dfca633fa`  
		Last Modified: Sat, 17 Aug 2024 05:17:23 GMT  
		Size: 190.9 KB (190915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:b3449830bb5865f288021e7ad089f5acd38888345873058fa5e98a931cd627e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3552079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3139973f97afacdf3b7c3fcfbc8f8e14500fceb8adf842145daba57964b04206`

```dockerfile
```

-	Layers:
	-	`sha256:829f526f1f483da95a91bea10150f42b69b124296c207d32880a7b5b85e2b87e`  
		Last Modified: Sat, 17 Aug 2024 05:17:24 GMT  
		Size: 3.5 MB (3530071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e64e62eabb50e01d82532502751d9c7b0b71002c598e87bfa406a7657c82648`  
		Last Modified: Sat, 17 Aug 2024 05:17:23 GMT  
		Size: 22.0 KB (22008 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:48e6d567754f1007ceecc8a30d24a36731e41167ec59eb9d8813afb7642bcb99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (100984971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef0b136472466cffacd29c35efc22a0ee8e36dfde0268c0f5b10069b6cd44e1`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 06 Aug 2024 08:03:42 GMT
ARG RELEASE
# Tue, 06 Aug 2024 08:03:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Aug 2024 08:03:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Aug 2024 08:03:42 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 06 Aug 2024 08:03:42 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 06 Aug 2024 08:03:42 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 06 Aug 2024 08:03:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 06 Aug 2024 08:03:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 08:03:42 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
WORKDIR /usr/local/tomcat
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 08:03:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 08:03:42 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_MAJOR=9
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_VERSION=9.0.93
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_SHA512=3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d
# Tue, 06 Aug 2024 08:03:42 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 06 Aug 2024 08:03:42 GMT
ENTRYPOINT []
# Tue, 06 Aug 2024 08:03:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a13fc23d23d50177fc33d5df0e5c516fdbaae7d5cb53c11d634dff7e6e365e`  
		Last Modified: Sat, 17 Aug 2024 01:33:12 GMT  
		Size: 12.8 MB (12813299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe26b7a9fc390ef63cf055e6e311a50e2bb6c11bc64c80f450417a71eb7ba031`  
		Last Modified: Sat, 17 Aug 2024 01:36:13 GMT  
		Size: 46.7 MB (46746294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a5437d6fef2529f65b67ce9b2a75371cef52e384174649eac3424168e5c623`  
		Last Modified: Sat, 17 Aug 2024 01:36:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560407f77d279e68f72a6b12199439583872a1ea3f7441297485cd75f35c2820`  
		Last Modified: Sat, 17 Aug 2024 01:36:08 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9403e3111d8493384f1f79b77f885b4c7e027aa5fd34e99f6a18834f7d8ad4fd`  
		Last Modified: Sat, 17 Aug 2024 12:47:00 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef73f692048d7863b60cdc79a8c8c5bc08b84652e055783fbf46548de2c3cde`  
		Last Modified: Sat, 17 Aug 2024 12:49:44 GMT  
		Size: 12.8 MB (12809246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4467c4a475d5ee766b0116968a6fe53a9c6cd800098aa6496b4d93fa876bf313`  
		Last Modified: Sat, 17 Aug 2024 12:49:44 GMT  
		Size: 216.8 KB (216794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:a04ccf9515eab94f49aa44ea19d218ae06d3c93f1436ebde7472445a56a6b93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3551654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4925158aba18e4eb1c13c2a5d5305e860904f95e07d13aa2174608685534b36a`

```dockerfile
```

-	Layers:
	-	`sha256:5769ce00f828da15e3a430049341f5759ea47edc01247a5510ed5358d0a97bb8`  
		Last Modified: Sat, 17 Aug 2024 12:49:44 GMT  
		Size: 3.5 MB (3529128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5359a5eb005f1293453862ee10173003cee110af4e7a436fcf2f85a0cf5a518`  
		Last Modified: Sat, 17 Aug 2024 12:49:43 GMT  
		Size: 22.5 KB (22526 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:3e0101ddf4c9329965285dff4cf56f195b300603988941616762b096f20c806b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109503269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91d0d9c9d3926658967dda611c3062e02a930bafc3f1da66ba631c60ba378aa`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 06 Aug 2024 08:03:42 GMT
ARG RELEASE
# Tue, 06 Aug 2024 08:03:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Aug 2024 08:03:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Aug 2024 08:03:42 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 06 Aug 2024 08:03:42 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 06 Aug 2024 08:03:42 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 06 Aug 2024 08:03:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 06 Aug 2024 08:03:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 08:03:42 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
WORKDIR /usr/local/tomcat
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 08:03:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 08:03:42 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_MAJOR=9
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_VERSION=9.0.93
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_SHA512=3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d
# Tue, 06 Aug 2024 08:03:42 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 06 Aug 2024 08:03:42 GMT
ENTRYPOINT []
# Tue, 06 Aug 2024 08:03:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2b9159aba5847bda25160889018a02e4997ea0539f37f28faa599fcc4e6e59`  
		Last Modified: Sat, 17 Aug 2024 00:59:09 GMT  
		Size: 13.7 MB (13715085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8df1510f2e515b4ef656dd9c93352c60dc24965dd8ee75c31bc74018cb42aeb`  
		Last Modified: Sat, 17 Aug 2024 01:02:58 GMT  
		Size: 47.1 MB (47116012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6716094041a01730dfc01fdf740d805f8100542358fe6f56639974b95f13ce`  
		Last Modified: Sat, 17 Aug 2024 01:02:50 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d88e63af0e9c74b520244f1440e8b5e318223ed76ca89660474f005d8a79e9`  
		Last Modified: Sat, 17 Aug 2024 01:02:51 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b4f0cb6e5b5272d3dd6404b808d3376dd3fb50647c00c9902e09ffab5670e9`  
		Last Modified: Sat, 17 Aug 2024 12:02:56 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c264de1317d7447334f207b2c7ea4f884cd357e506deca52c36e47b4c324ed5`  
		Last Modified: Sat, 17 Aug 2024 12:07:54 GMT  
		Size: 12.8 MB (12832694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedd9aec58f2f1d1dd745bba908b3eacb59fd9311202582bcdfec56974fac784`  
		Last Modified: Sat, 17 Aug 2024 12:07:54 GMT  
		Size: 249.6 KB (249604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:adf223d57ea630bfa79c1c2ab2a7da1bf14109a03eec7ef9bdfff178395701a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3555306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f33374d86c91dfbdbab8b622ed8cd61175bbab63d694547213f34ad1e33c458`

```dockerfile
```

-	Layers:
	-	`sha256:f3cdc30bf3b9caaa7ea18a9478949b19b36348e31e0bfcd0451120364d3e5ed1`  
		Last Modified: Sat, 17 Aug 2024 12:07:54 GMT  
		Size: 3.5 MB (3533361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e08df8486b9848c932e3fa23e0cc514da05cc9237ffdd27601406566072f385`  
		Last Modified: Sat, 17 Aug 2024 12:07:53 GMT  
		Size: 21.9 KB (21945 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:711cbaa23cf2df1c35313eb2a9566aeb50d2faa4fdf0af31d7a38290119dec76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.5 MB (98479500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0411e8c859c810f2f9f279901a8eb4fd99df27df81f9a4e7e5a2f1538b9054c0`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 06 Aug 2024 08:03:42 GMT
ARG RELEASE
# Tue, 06 Aug 2024 08:03:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Aug 2024 08:03:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Aug 2024 08:03:42 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 06 Aug 2024 08:03:42 GMT
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
# Tue, 06 Aug 2024 08:03:42 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Tue, 06 Aug 2024 08:03:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 06 Aug 2024 08:03:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 08:03:42 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
WORKDIR /usr/local/tomcat
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 08:03:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 08:03:42 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_MAJOR=9
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_VERSION=9.0.93
# Tue, 06 Aug 2024 08:03:42 GMT
ENV TOMCAT_SHA512=3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d
# Tue, 06 Aug 2024 08:03:42 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 06 Aug 2024 08:03:42 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 06 Aug 2024 08:03:42 GMT
ENTRYPOINT []
# Tue, 06 Aug 2024 08:03:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f487d2bc1de52e44ed06dfc0c18b748d484f1eb638bdc1cbf599195a96c480be`  
		Last Modified: Sat, 17 Aug 2024 01:32:19 GMT  
		Size: 13.0 MB (12955186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb43b5eb6b749b20cbc0d4d49fa146e13299ac7c636c67f6b885928ff809d1d`  
		Last Modified: Sat, 17 Aug 2024 01:34:05 GMT  
		Size: 43.9 MB (43864131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa6e76a567ef01fbd878046dfba9c29424f4011e53ee93496f2d3290648a8d1`  
		Last Modified: Sat, 17 Aug 2024 01:34:00 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f152c41373f13a6fbf7703ffb492e133e88fb9ea9ba931a661e32db4a7fb3e39`  
		Last Modified: Sat, 17 Aug 2024 01:33:59 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1581871c9509f9dc76c7aff9723ea0141828fdee1edba900632f9141eb39a4`  
		Last Modified: Sat, 17 Aug 2024 07:55:00 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb8c35cc7e1a3f5bd5ac09ddbf26767d4d64e80d11797bb69599f638f6a7a53`  
		Last Modified: Sat, 17 Aug 2024 07:58:45 GMT  
		Size: 12.8 MB (12800188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4001619dba6415ec1ba5ad85941f0f26d56170ab91fdd1ae5c62a5dcc01eafd0`  
		Last Modified: Sat, 17 Aug 2024 07:58:45 GMT  
		Size: 219.3 KB (219263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:1fb2f0931b3b195518810ce23dbb015a49dcf5377a684fc7497def010221573b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3551869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be684fcd88d9af9a312dd8717600677cd2e63a6adc077d10222fefdf976aeb7`

```dockerfile
```

-	Layers:
	-	`sha256:df281d384f90542e5a57298a62a999a56b156672948205b8407ec016a098df11`  
		Last Modified: Sat, 17 Aug 2024 07:58:45 GMT  
		Size: 3.5 MB (3529970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:503f2aaa53c1d61eaed2d5f260e1cdc8111914b31688a4241565440d93045fa9`  
		Last Modified: Sat, 17 Aug 2024 07:58:45 GMT  
		Size: 21.9 KB (21899 bytes)  
		MIME: application/vnd.in-toto+json
