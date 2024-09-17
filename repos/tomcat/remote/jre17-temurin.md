## `tomcat:jre17-temurin`

```console
$ docker pull tomcat@sha256:b9da63abf0ac168f9b594d93d66b952e351b855dee0acaff70a721a19cb7e48d
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

### `tomcat:jre17-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:78feac8c09cbef4f188b30562b17ef1709d08d735077e0c6ea1684f22a2d0f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107220867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847a7add555ddda1a681983162041a642ead129065065319507fa443c6f0e84e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:01 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:03 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 27 Aug 2024 15:55:03 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='2d1ed42918305a1a0754a6e1e9294c7d4d7fda4bff6dba7bc5682037d860dbc9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 02:03:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 11 Sep 2024 02:03:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Sep 2024 02:03:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
WORKDIR /usr/local/tomcat
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 02:03:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 02:03:19 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_MAJOR=10
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_VERSION=10.1.29
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_SHA512=792a0a56963fe67ec88536a7b9bc338d9e9dc0b1c5d66e89fce62040f148c7be7d4e70e06c0d23d0b5338068eca87cd2669244364ba0aa900ffdcf3eb82bc8a9
# Wed, 11 Sep 2024 02:03:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 11 Sep 2024 02:03:19 GMT
ENTRYPOINT []
# Wed, 11 Sep 2024 02:03:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:32b824d45c6101d459f5d3c13ab8658b6f79713f3bd64e363d3f6bc98faf5d6d`  
		Last Modified: Tue, 27 Aug 2024 21:43:22 GMT  
		Size: 30.6 MB (30611547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a316f85472e42ddf39be81d37cefcaa87cad98b7ca1710864ef2b8e67e9713b`  
		Last Modified: Tue, 17 Sep 2024 01:07:39 GMT  
		Size: 16.2 MB (16177262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc61f93074679710412ad3cef2fc06379271ccc3fe6224c6048a7940bcd3e31`  
		Last Modified: Tue, 17 Sep 2024 01:10:41 GMT  
		Size: 47.3 MB (47280241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd40a8ba9b9816e6e92a048771912e0203fb0c2366490934aebed10ad169c831`  
		Last Modified: Tue, 17 Sep 2024 01:10:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b1b7b9b07ec925dc69ff02361ed98cf596d711625c013abe78af64e96f6d36`  
		Last Modified: Tue, 17 Sep 2024 01:10:35 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c6cda65247a5983779ac13edb9d72bb019b894353ab919be33b450cd4add40`  
		Last Modified: Tue, 17 Sep 2024 03:02:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f229d4ab82ed5691eace182d00035ccd868bfd9e422a42f9683e3893ecaea188`  
		Last Modified: Tue, 17 Sep 2024 03:02:31 GMT  
		Size: 12.9 MB (12937056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f9d75dcdf9b22243adc83fe45093a4ee015f83a3eb6440bfb4298ff46c532e`  
		Last Modified: Tue, 17 Sep 2024 03:02:31 GMT  
		Size: 212.3 KB (212289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:a836458467d7c861196ea99fb55032b382db21d6332e5088a82de04e1939fd29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3009443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b57c91ae41840998ecb4d4db496eea68fcc7caf5f7b257d48dfe1fe5219619`

```dockerfile
```

-	Layers:
	-	`sha256:c9bee5c8c74de79e5350de85d6875c788ef692934f05a5d72ef55ee1d68bb3fd`  
		Last Modified: Tue, 17 Sep 2024 03:02:31 GMT  
		Size: 3.0 MB (2984865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc2b278026d4ff2f49e45f2fec93c1713615e69ce7343d96ed18c1ceea569190`  
		Last Modified: Tue, 17 Sep 2024 03:02:31 GMT  
		Size: 24.6 KB (24578 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:7ff70b84bbd7835d6cd26c3303baa40bb53de44c2b370eedbf516622a5f77810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100694794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1300a7f2f45baffc515f35f740d6eb9db67506b7a47029ace82f325542a7a8`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:10 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:14 GMT
ADD file:0efc83f80e5e3a9125a702063e487f836d2e0ff9a88f4d0330897d15e445d415 in / 
# Tue, 27 Aug 2024 15:55:14 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='2d1ed42918305a1a0754a6e1e9294c7d4d7fda4bff6dba7bc5682037d860dbc9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 02:03:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 11 Sep 2024 02:03:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Sep 2024 02:03:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
WORKDIR /usr/local/tomcat
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 02:03:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 02:03:19 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_MAJOR=10
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_VERSION=10.1.29
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_SHA512=792a0a56963fe67ec88536a7b9bc338d9e9dc0b1c5d66e89fce62040f148c7be7d4e70e06c0d23d0b5338068eca87cd2669244364ba0aa900ffdcf3eb82bc8a9
# Wed, 11 Sep 2024 02:03:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 11 Sep 2024 02:03:19 GMT
ENTRYPOINT []
# Wed, 11 Sep 2024 02:03:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3662f20bd36fe3ab5035e3d6d75d4a5a27e32e29abe306052959223600a1522c`  
		Last Modified: Tue, 17 Sep 2024 01:24:15 GMT  
		Size: 27.7 MB (27731977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4be6c7fa81e4d16783a207dc0e7aee5ebe57ddded3444a61cd47351170b177`  
		Last Modified: Tue, 17 Sep 2024 01:24:14 GMT  
		Size: 14.9 MB (14919849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb5ee99fba8901cd1091f21e0771db2ac6014b4eb0508c7bdc318f269f1c71a`  
		Last Modified: Tue, 17 Sep 2024 01:27:16 GMT  
		Size: 44.9 MB (44944602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490d33daf96fc0ab2c879086e9c5a27d327a63e823a83f17dd18b32e8a7cf03c`  
		Last Modified: Tue, 17 Sep 2024 01:27:08 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ee14ccde45b437267316bc18c42cbecda3190c45b4b1036912cbfd7857eafb`  
		Last Modified: Tue, 17 Sep 2024 01:27:08 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c6200e099cb1c6b8b8b70918d7af087bc658381513dba0508513d082c6e4f0`  
		Last Modified: Tue, 17 Sep 2024 03:06:45 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a290b280decdd15fc51f88ea9471f8996f849a78285a7d3c132da0d952d5d298`  
		Last Modified: Tue, 17 Sep 2024 03:06:46 GMT  
		Size: 12.9 MB (12912493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae382ed85b0b817ed89d43dd2caddd1889ccae62f3339e2734a85dd523f7e9b9`  
		Last Modified: Tue, 17 Sep 2024 03:06:46 GMT  
		Size: 183.4 KB (183403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:c53364071e593b6298afb9e22c4df7c800a2183680f22c8c7cb3c35ad2dfc09f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3010946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7247bbe3cdb605b5b36770eb978cf85d73dfa3752fe4a7b0691aff62715b9e23`

```dockerfile
```

-	Layers:
	-	`sha256:2bd0a8f103d1cb4b1d67f5f21908fe37d4815f3047065dd24ebce8bd07388cf2`  
		Last Modified: Tue, 17 Sep 2024 03:06:45 GMT  
		Size: 3.0 MB (2986163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410c24664229d837ac4808fb7d21e82b33f29fb2de18004269d4e518dc23785b`  
		Last Modified: Tue, 17 Sep 2024 03:06:45 GMT  
		Size: 24.8 KB (24783 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:7b712228d08245f34d74cd0ea6b605ffd93c5d81c4f0b74ffbfb7117712d69fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120157748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f158658dab2005527a6040caef6d47c4a7e7cbdfd7f04029d7ee47bbe68a4b5`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 01 Aug 2024 15:33:35 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:33:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:33:36 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:33:38 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 01 Aug 2024 15:33:38 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='2d1ed42918305a1a0754a6e1e9294c7d4d7fda4bff6dba7bc5682037d860dbc9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 02:03:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 11 Sep 2024 02:03:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Sep 2024 02:03:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
WORKDIR /usr/local/tomcat
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 02:03:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 02:03:19 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_MAJOR=10
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_VERSION=10.1.29
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_SHA512=792a0a56963fe67ec88536a7b9bc338d9e9dc0b1c5d66e89fce62040f148c7be7d4e70e06c0d23d0b5338068eca87cd2669244364ba0aa900ffdcf3eb82bc8a9
# Wed, 11 Sep 2024 02:03:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 11 Sep 2024 02:03:19 GMT
ENTRYPOINT []
# Wed, 11 Sep 2024 02:03:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923b74992e2f6b4e4be4f1c2bf6930b93c7593d6c834159867d3bd8ea14005ff`  
		Last Modified: Sat, 17 Aug 2024 01:33:27 GMT  
		Size: 13.8 MB (13795899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169b61747edd8caded770386f82148a86bed83337fc5d5d3c98d9068fd166940`  
		Last Modified: Fri, 23 Aug 2024 19:45:30 GMT  
		Size: 46.7 MB (46746370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57a7471d94a9e3dbc7a2319293c1c0b9855c26bf4faf9308850b20ef0f92ba1`  
		Last Modified: Fri, 23 Aug 2024 19:45:25 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1428cdfeb2dcadba80a0f2b8c442b1e07d23961a8a4813d0d54d2201653d5cc1`  
		Last Modified: Fri, 23 Aug 2024 19:45:25 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a27ba38a0a3d5439dc7bd5658d20d6e34d557128ec8806537557948d541734`  
		Last Modified: Wed, 11 Sep 2024 19:56:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b5ba899fb4b340b805c650b2038e925f70111174cdda60fc1291196e9e475b`  
		Last Modified: Wed, 11 Sep 2024 19:56:45 GMT  
		Size: 12.9 MB (12940754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b7785686d102734630cb2a2116fa16875483527bb090b8e0c2c10e365351d4`  
		Last Modified: Wed, 11 Sep 2024 19:56:45 GMT  
		Size: 16.8 MB (16762225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:09f8c6ba86d3bdfd013329a901655916f4a6ebc3f912c8173bb89c7d755d1514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3011216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d6e49907460c76656249a3c7d43a47167c20d481754eeabee0d829c2a8f2f0`

```dockerfile
```

-	Layers:
	-	`sha256:ac882b1bbdcaba1b36a5c2fd037783aadb94ce2672f7eb3d2233693c68b1a89b`  
		Last Modified: Wed, 11 Sep 2024 19:56:44 GMT  
		Size: 3.0 MB (2985875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb6c42026eebafd2764ef6dc122b2834b0fdf7adbd8980b73f95b66a7b9f907b`  
		Last Modified: Wed, 11 Sep 2024 19:56:44 GMT  
		Size: 25.3 KB (25341 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:78baca5b5b1eeb5f93a00e75416bd8510cc5f9b7be6979e5509e85c862e48dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129134019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817269bbbf78ebe994539a1c65ef8e3b104062f37750e06cf2ab92589a63eebb`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:51 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 01 Aug 2024 14:23:55 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='2d1ed42918305a1a0754a6e1e9294c7d4d7fda4bff6dba7bc5682037d860dbc9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 02:03:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 11 Sep 2024 02:03:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Sep 2024 02:03:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
WORKDIR /usr/local/tomcat
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 02:03:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 02:03:19 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_MAJOR=10
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_VERSION=10.1.29
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_SHA512=792a0a56963fe67ec88536a7b9bc338d9e9dc0b1c5d66e89fce62040f148c7be7d4e70e06c0d23d0b5338068eca87cd2669244364ba0aa900ffdcf3eb82bc8a9
# Wed, 11 Sep 2024 02:03:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 11 Sep 2024 02:03:19 GMT
ENTRYPOINT []
# Wed, 11 Sep 2024 02:03:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6e87eba78bda982d63d6dcd89b529540108dd7b3549a594cdc780cc6e61b5b37`  
		Last Modified: Tue, 06 Aug 2024 02:06:20 GMT  
		Size: 35.6 MB (35627737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e370ad6ca2bf55a99908be5c652053972a6818bb55965d7aa787af36e351327d`  
		Last Modified: Sat, 17 Aug 2024 00:59:29 GMT  
		Size: 14.9 MB (14944549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1acca8f93f6854140ee2ff4f7d3d40759829db3ec8812cd92e5a44dc1f3f635`  
		Last Modified: Fri, 23 Aug 2024 19:24:53 GMT  
		Size: 47.1 MB (47115930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587bf46278c0c5588e309dff98fe0345f4b2aa1449ff288d729917b80425470d`  
		Last Modified: Fri, 23 Aug 2024 19:24:46 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f123e8a5665cb70a30d1677fe33f18bb247e6a0aa7284e71736f74a18555158a`  
		Last Modified: Fri, 23 Aug 2024 19:24:46 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460e3700f677858912fef4404e6c71500914456f97de74557f58534f1ea0c9d9`  
		Last Modified: Wed, 11 Sep 2024 19:58:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9c5b1e8cfc134696e92ea6a751261d6c9d9392d7df173fe748a66285cc59a5`  
		Last Modified: Wed, 11 Sep 2024 19:58:32 GMT  
		Size: 13.0 MB (12954955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9bc19fc37dd4a16c4cce6033293f51ba9550044c6f38b02bdaaff91a3e64c4`  
		Last Modified: Wed, 11 Sep 2024 19:58:32 GMT  
		Size: 18.5 MB (18488376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:8e24ac70d7ec021ac743bc37c099642d790da16545d38899f5bcadcb5806f2b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5feb9b0f344558c8a5870e4fa2c7373f42882f331c09ec6bc39c1afa2efc4a74`

```dockerfile
```

-	Layers:
	-	`sha256:3200a6d61ae578b8125a7dbba1f0eb30977104be254174f4e316fe6e631b3a88`  
		Last Modified: Wed, 11 Sep 2024 19:58:31 GMT  
		Size: 3.0 MB (2989265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aecf02202402cae25b3b46fa9cee6e9c74c6f45799ef6c615489658bc3631bdf`  
		Last Modified: Wed, 11 Sep 2024 19:58:31 GMT  
		Size: 24.7 KB (24706 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:a66061cf6fc9f5a6a8d5db544c94dcb43a9ba346df8d49f49af2f8407d476c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (103985283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc96bc91528bf5edd0b3b8987a9a84a6f5d7423200143ccd2acf5be8a20c8d1e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:05 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:08 GMT
ADD file:55ce2834630c73439274688061a6b2ad0d6952c2435dc51250026e14f139275d in / 
# Tue, 27 Aug 2024 15:55:08 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='2d1ed42918305a1a0754a6e1e9294c7d4d7fda4bff6dba7bc5682037d860dbc9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Sep 2024 02:03:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 11 Sep 2024 02:03:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Sep 2024 02:03:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
WORKDIR /usr/local/tomcat
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 02:03:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 11 Sep 2024 02:03:19 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_MAJOR=10
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_VERSION=10.1.29
# Wed, 11 Sep 2024 02:03:19 GMT
ENV TOMCAT_SHA512=792a0a56963fe67ec88536a7b9bc338d9e9dc0b1c5d66e89fce62040f148c7be7d4e70e06c0d23d0b5338068eca87cd2669244364ba0aa900ffdcf3eb82bc8a9
# Wed, 11 Sep 2024 02:03:19 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 11 Sep 2024 02:03:19 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 11 Sep 2024 02:03:19 GMT
ENTRYPOINT []
# Wed, 11 Sep 2024 02:03:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1ebdf4a84a853f3e1fae6f15bd5f734d2925697002b9b26792d25b2080fac7e6`  
		Last Modified: Tue, 17 Sep 2024 01:29:05 GMT  
		Size: 30.7 MB (30665390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa806051defda3e7a36ed8367d52c08e84f30e5a78265c4e79116ac5c645d6f`  
		Last Modified: Tue, 17 Sep 2024 01:39:06 GMT  
		Size: 16.3 MB (16280949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2127748ebbbd5d2be41b7fe32ffe2b5f26cce9255c0d9ee5e97484a6c24275b2`  
		Last Modified: Tue, 17 Sep 2024 01:40:37 GMT  
		Size: 43.9 MB (43864331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb00f4d7906f6ac8022c74c2d07a6947a4fbab96d5ef4b1ab18e5d5f5fa61c4`  
		Last Modified: Tue, 17 Sep 2024 01:40:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767a30c5510443bb511d921e5bfa881ab492292a95949ccd2d1d3de0508e1651`  
		Last Modified: Tue, 17 Sep 2024 01:40:31 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401e926ccfb203da69459f64ad28f266b79ec45ee55adf83d218cdd69a00d3da`  
		Last Modified: Tue, 17 Sep 2024 06:20:42 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c99dcbd653f51c29f6ac2e9a53190c075ccca56c8ab52af16fc7070cf2d01ee`  
		Last Modified: Tue, 17 Sep 2024 06:20:43 GMT  
		Size: 12.9 MB (12948347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07497625e1e6139baa53fb5f36838ae396cd8df2825dc0518a74a90d3ea0dc77`  
		Last Modified: Tue, 17 Sep 2024 06:20:43 GMT  
		Size: 223.8 KB (223795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:23dfaa0338adfb7c4847c4ca82d8d87273a0225b6e7e04a8f9903ede63dd573b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3011196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a23ebcfa120b6535a8d8e0a31d845ae94b028041251f4cd8b2a8c3267d0590`

```dockerfile
```

-	Layers:
	-	`sha256:4f3b3274837297c539fafd7c3d484079a853da70a6f1d29f9222a3eae3cf789d`  
		Last Modified: Tue, 17 Sep 2024 06:20:42 GMT  
		Size: 3.0 MB (2986594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8740fbb3c46c1502b336e374b207f81ba38c635e7f139577bc51b368a1cd898`  
		Last Modified: Tue, 17 Sep 2024 06:20:42 GMT  
		Size: 24.6 KB (24602 bytes)  
		MIME: application/vnd.in-toto+json
