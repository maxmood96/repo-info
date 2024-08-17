## `tomcat:10-jre17-temurin`

```console
$ docker pull tomcat@sha256:ae241a4a9f23a88473e9239db190e1eb24c80d1741b02d84d7233a91bcc810b6
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

### `tomcat:10-jre17-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:f99b0846904189a96f028dc062d7eb2d5695d5f8d9c98133a8e99f5d4b153182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107574111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1630732a70808b862ee77ca7f54f5d34d0bacce7c20f4c7c47a83e5b727d0cfc`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
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
# Tue, 06 Aug 2024 18:01:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 06 Aug 2024 18:01:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:01:07 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 06 Aug 2024 18:01:07 GMT
WORKDIR /usr/local/tomcat
# Tue, 06 Aug 2024 18:01:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 18:01:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 18:01:07 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Tue, 06 Aug 2024 18:01:07 GMT
ENV TOMCAT_MAJOR=10
# Tue, 06 Aug 2024 18:01:07 GMT
ENV TOMCAT_VERSION=10.1.28
# Tue, 06 Aug 2024 18:01:07 GMT
ENV TOMCAT_SHA512=b3177fb594e909364abc8074338de24f0441514ee81fa13bcc0b23126a5e3980cc5a6a96aab3b49798ba58d42087bf2c5db7cee3e494cc6653a6c70d872117e5
# Tue, 06 Aug 2024 18:01:07 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 06 Aug 2024 18:01:07 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 18:01:07 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 06 Aug 2024 18:01:07 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 06 Aug 2024 18:01:07 GMT
ENTRYPOINT []
# Tue, 06 Aug 2024 18:01:07 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72f7ee7417d7dc1d181843bc32c8c5d47822e3ae0ac08aa7c72ac09055040c2`  
		Last Modified: Tue, 23 Jul 2024 01:08:59 GMT  
		Size: 13.8 MB (13765598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced013eec6cb5fa5c1146b85b09e19552a5b54474297bbaeba8a333739bbbbef`  
		Last Modified: Tue, 23 Jul 2024 01:09:03 GMT  
		Size: 47.3 MB (47280194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73663ebb99d0b0749c0e265014cd2e9a976615d5b102f5d5d69b141899661e7f`  
		Last Modified: Tue, 23 Jul 2024 01:08:57 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36083ab7049b9d911a90609cf0790cf4715c8edc0c0ec4a7447210b0f302e562`  
		Last Modified: Thu, 25 Jul 2024 17:30:44 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f9b40f507b5e19288caa22d3e4c976b7334b50a222a0d7b82469a37b5fcb60`  
		Last Modified: Wed, 07 Aug 2024 00:52:32 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af50dd088b7ef1fe74e33dd0270782cb5fded67989bc30e75b870d549d02ee1`  
		Last Modified: Wed, 07 Aug 2024 00:52:32 GMT  
		Size: 12.9 MB (12948010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3fec18c0fe2cb6c819644a14dd9f3dec7c08e3b36b829fbccd7d5b33e07116`  
		Last Modified: Wed, 07 Aug 2024 00:52:32 GMT  
		Size: 3.0 MB (3011455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:f1e175cf956a6144b8d7446f8e95a5eaf658ffd2a1c0c34e1dcd214fae435f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3006062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f7e186fd2c009dba61a8b18cc3823f228ee80b494fe094e6516c80f0bce426`

```dockerfile
```

-	Layers:
	-	`sha256:ca5163bf6fcb281309f00dc68b9113bab1e05c14d08bbb70296bb27ef244ac62`  
		Last Modified: Wed, 07 Aug 2024 00:52:32 GMT  
		Size: 3.0 MB (2981482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c21ca51e0339ce9cb36acc65597fbfc2c610d74c5ed444f35299094cc9f1fe`  
		Last Modified: Wed, 07 Aug 2024 00:52:32 GMT  
		Size: 24.6 KB (24580 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre17-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:b62f4739612c80136f0a635ef07f8b0f360b58f88863957d245c12fd847d8e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98875810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c81c121cb3138005d2e4552d9511a96096ebbd8c9f37092dbbceec03d8c490`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 01 Aug 2024 15:22:41 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:22:42 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:22:44 GMT
ADD file:7bcbd2cb56e3985e9aa22bb8b43873f12d7f999600db594761eaf685a9177b7e in / 
# Thu, 01 Aug 2024 15:22:45 GMT
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
# Tue, 06 Aug 2024 18:01:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 06 Aug 2024 18:01:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:01:07 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 06 Aug 2024 18:01:07 GMT
WORKDIR /usr/local/tomcat
# Tue, 06 Aug 2024 18:01:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 18:01:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 18:01:07 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Tue, 06 Aug 2024 18:01:07 GMT
ENV TOMCAT_MAJOR=10
# Tue, 06 Aug 2024 18:01:07 GMT
ENV TOMCAT_VERSION=10.1.28
# Tue, 06 Aug 2024 18:01:07 GMT
ENV TOMCAT_SHA512=b3177fb594e909364abc8074338de24f0441514ee81fa13bcc0b23126a5e3980cc5a6a96aab3b49798ba58d42087bf2c5db7cee3e494cc6653a6c70d872117e5
# Tue, 06 Aug 2024 18:01:07 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 06 Aug 2024 18:01:07 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 18:01:07 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 06 Aug 2024 18:01:07 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 06 Aug 2024 18:01:07 GMT
ENTRYPOINT []
# Tue, 06 Aug 2024 18:01:07 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:dad4e753fc73fa87bcedddc090f436866b477fd660d61da6b81071b41ab85948`  
		Last Modified: Tue, 06 Aug 2024 02:06:08 GMT  
		Size: 27.7 MB (27689240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2daaa1493be2e58f55d0a68251ec270ec90fc978014e06ec0db5af0cbf608a44`  
		Last Modified: Sat, 17 Aug 2024 01:36:13 GMT  
		Size: 13.1 MB (13133360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ee938d854e55e20d7f539d11b0c3539e3417a0c6aee7e59f4fd8c5360a9bef`  
		Last Modified: Sat, 17 Aug 2024 01:39:40 GMT  
		Size: 44.9 MB (44944646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30942943fc671541b1f6e63959ba51c282ff5a906b2321d8b4900013b9c6d405`  
		Last Modified: Sat, 17 Aug 2024 01:39:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2065363134e65e9759706dd5fc18178b9b856ce219fd88910f5c28f2204ac098`  
		Last Modified: Sat, 17 Aug 2024 01:39:33 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd6662cf18f89503a16b31da9edf82b311629559142607994e36fa8dbaea8ba`  
		Last Modified: Sat, 17 Aug 2024 02:26:17 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10948abb2fd680aee30b98841e6e3177f6322ff355c3cd84dbe04d351b15f6ac`  
		Last Modified: Sat, 17 Aug 2024 05:14:34 GMT  
		Size: 12.9 MB (12924008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96aa7029501fcdd2d5a34eb7a3f982872ea2d2847cef8637711a5db3663d8f2`  
		Last Modified: Sat, 17 Aug 2024 05:14:33 GMT  
		Size: 182.3 KB (182331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:3dbff1cb2c2fa130ab87b0df57fc45c433e6f69098e066910ea502f28bbfe691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3007584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5c553880d30d7b2a954908607a0b723e70247771bf54599364790a1de676ed`

```dockerfile
```

-	Layers:
	-	`sha256:de70320e3be092d2dd999847fd1c5bae45053130f463b784c9338726f7a94eb4`  
		Last Modified: Sat, 17 Aug 2024 05:14:33 GMT  
		Size: 3.0 MB (2982800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e18b8ef42e1134f8e0d5303a640e3cb88c24570530831f85bff0e3b8dfa8fda`  
		Last Modified: Sat, 17 Aug 2024 05:14:33 GMT  
		Size: 24.8 KB (24784 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre17-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:cdd207a9f80bae0dad85c469f98308f34550945ecad2d20aa731a313192af1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.2 MB (106216130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266e74e26d9854fd21192bd7e2b38b9c15981172c10e84bde60e6d67bc15f1e1`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
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
# Tue, 06 Aug 2024 18:01:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 06 Aug 2024 18:01:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:01:07 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 06 Aug 2024 18:01:07 GMT
WORKDIR /usr/local/tomcat
# Tue, 06 Aug 2024 18:01:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 18:01:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 18:01:07 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Tue, 06 Aug 2024 18:01:07 GMT
ENV TOMCAT_MAJOR=10
# Tue, 06 Aug 2024 18:01:07 GMT
ENV TOMCAT_VERSION=10.1.28
# Tue, 06 Aug 2024 18:01:07 GMT
ENV TOMCAT_SHA512=b3177fb594e909364abc8074338de24f0441514ee81fa13bcc0b23126a5e3980cc5a6a96aab3b49798ba58d42087bf2c5db7cee3e494cc6653a6c70d872117e5
# Tue, 06 Aug 2024 18:01:07 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 06 Aug 2024 18:01:07 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 18:01:07 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 06 Aug 2024 18:01:07 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 06 Aug 2024 18:01:07 GMT
ENTRYPOINT []
# Tue, 06 Aug 2024 18:01:07 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ee6568921bf59d9276710834a5fc50acb0da4a9d04950ae5ec695828c86dd4`  
		Last Modified: Tue, 23 Jul 2024 04:14:15 GMT  
		Size: 13.8 MB (13795443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e1b72ba4c1374ee7def94c45e1f16cacc330b2d3e90ca790d283de5db18cb8`  
		Last Modified: Tue, 23 Jul 2024 04:14:18 GMT  
		Size: 46.7 MB (46746369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e9b14b806a8f1a54d78e10962c1460615fa346fbea1aeb53c168a9807e5a7e`  
		Last Modified: Tue, 23 Jul 2024 04:14:13 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85331be2ec25884f920b5a4938bc420e89eddfe3915d32e7aab3ec5460a9adb`  
		Last Modified: Thu, 25 Jul 2024 17:46:26 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3b59b43989e28a2d54dbed5a37f1ee96bc284a19e6bc342d4ea05fd0a9f81b`  
		Last Modified: Fri, 26 Jul 2024 19:59:48 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f7e95db97668120eab571f49e161061194d54df1a695fcfb0f9da1e2809779`  
		Last Modified: Wed, 07 Aug 2024 00:53:52 GMT  
		Size: 13.0 MB (12951211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef351c8b7e97ba99b4e335ae98bef33304a87a104897ad4b169bd9a39a74385`  
		Last Modified: Wed, 07 Aug 2024 00:53:51 GMT  
		Size: 2.8 MB (2812898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:b294838d5da704381e64e9bcbfcd6af2dddbb037af19cd4bbf9418ec6c1244f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3008003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ec1049e4f1d74dcbb6cc3fdbb0581f7363c419ce55cf7576d6c57fcc33f91a`

```dockerfile
```

-	Layers:
	-	`sha256:f129076b167766cce31af117ce84e1bb51a7e3598b48867492b0db5b92b37d69`  
		Last Modified: Wed, 07 Aug 2024 00:53:51 GMT  
		Size: 3.0 MB (2982664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0a98b851d8d3077c55ecae07e930c4f5ccd8894ab572e0296a604469b5933fd`  
		Last Modified: Wed, 07 Aug 2024 00:53:51 GMT  
		Size: 25.3 KB (25339 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre17-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:a02b75f072c340c6299053d3b9ff8a5507f474c3db5612a081b2d0e546bfe709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (113996786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5add4095eeca0a6630400a805fbb3cd4959d7f739ef8b1cfaeef6cb33a5f8ae`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:24 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:28 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Fri, 07 Jun 2024 12:00:29 GMT
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
# Tue, 06 Aug 2024 18:01:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 06 Aug 2024 18:01:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:01:07 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 06 Aug 2024 18:01:07 GMT
WORKDIR /usr/local/tomcat
# Tue, 06 Aug 2024 18:01:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 18:01:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 18:01:07 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Tue, 06 Aug 2024 18:01:07 GMT
ENV TOMCAT_MAJOR=10
# Tue, 06 Aug 2024 18:01:07 GMT
ENV TOMCAT_VERSION=10.1.28
# Tue, 06 Aug 2024 18:01:07 GMT
ENV TOMCAT_SHA512=b3177fb594e909364abc8074338de24f0441514ee81fa13bcc0b23126a5e3980cc5a6a96aab3b49798ba58d42087bf2c5db7cee3e494cc6653a6c70d872117e5
# Tue, 06 Aug 2024 18:01:07 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 06 Aug 2024 18:01:07 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 18:01:07 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 06 Aug 2024 18:01:07 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 06 Aug 2024 18:01:07 GMT
ENTRYPOINT []
# Tue, 06 Aug 2024 18:01:07 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a6b87acc0a568209f5593370b5b6bcffdf1ec82a13216fce26023e6eac0aaea8`  
		Last Modified: Sun, 09 Jun 2024 02:03:40 GMT  
		Size: 35.6 MB (35626958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9074cdf27e23156680daa103ed33f6d64f3a455ee0f828ee2acc7e1e3ecbd1`  
		Last Modified: Tue, 23 Jul 2024 01:44:29 GMT  
		Size: 14.9 MB (14944088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bf0c83db43ddf51099ddc1c575522caf0ff95c642f649e753ba9875e29c711`  
		Last Modified: Tue, 23 Jul 2024 01:44:33 GMT  
		Size: 47.1 MB (47115878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7497b1bcb31820572cfbdbe7d720db91159022fbc3746beea2a7427be5679709`  
		Last Modified: Tue, 23 Jul 2024 01:44:25 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0755665ec42637ebdacff0d7ca65d15dca78f2f1549511ba0b164cd37f21263`  
		Last Modified: Thu, 25 Jul 2024 17:25:36 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4e91d5b4b12d20a74411d91561773cfc9a84ea2c360f4f33d5f10c37e14a84`  
		Last Modified: Fri, 26 Jul 2024 20:06:04 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650f22ac3648f988dcae4471b1e7817a7b3b719a287d7da2d9bc1cba92dd85ad`  
		Last Modified: Wed, 07 Aug 2024 00:55:32 GMT  
		Size: 13.0 MB (12965041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77090cd6d6735cc34df94fd2b2e49061659a21f857bee0982b06ec3242438f9c`  
		Last Modified: Wed, 07 Aug 2024 00:55:32 GMT  
		Size: 3.3 MB (3342594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:d4a90aa777d1c0cd38a82938fca7d8da0b1375b79074371455516fd6c28b1b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3010758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9c82666966c5b403541a756dc89fcca5d04b3de625844c5c9b15db8b0eaa92`

```dockerfile
```

-	Layers:
	-	`sha256:20b7cf1371777ffffd78c5983b7eec8bca867e9c4b3b7262c79ef47d6db96afe`  
		Last Modified: Wed, 07 Aug 2024 00:55:31 GMT  
		Size: 3.0 MB (2986054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3af7c0be21bf825cac40e453c19455f188e5dfe03f0e4392510e4e219e7b6de2`  
		Last Modified: Wed, 07 Aug 2024 00:55:31 GMT  
		Size: 24.7 KB (24704 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre17-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:197b8f0f2447e9117b5167d41dc25caba98de3061549f5d0d6526c9633a67c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104504754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0571a5ce8c650abdf79a6a8dfea5b1965bf8b1e32bf3d1793f6e4363275dc020`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:41 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:43 GMT
ADD file:25fd4d5892ebbc4a423c330fe39c4ea6e82588ffbcb191cf41477a4446e164e0 in / 
# Fri, 07 Jun 2024 12:00:43 GMT
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
# Tue, 06 Aug 2024 18:01:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 06 Aug 2024 18:01:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:01:07 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 06 Aug 2024 18:01:07 GMT
WORKDIR /usr/local/tomcat
# Tue, 06 Aug 2024 18:01:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 18:01:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 06 Aug 2024 18:01:07 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Tue, 06 Aug 2024 18:01:07 GMT
ENV TOMCAT_MAJOR=10
# Tue, 06 Aug 2024 18:01:07 GMT
ENV TOMCAT_VERSION=10.1.28
# Tue, 06 Aug 2024 18:01:07 GMT
ENV TOMCAT_SHA512=b3177fb594e909364abc8074338de24f0441514ee81fa13bcc0b23126a5e3980cc5a6a96aab3b49798ba58d42087bf2c5db7cee3e494cc6653a6c70d872117e5
# Tue, 06 Aug 2024 18:01:07 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 06 Aug 2024 18:01:07 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 18:01:07 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 06 Aug 2024 18:01:07 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 06 Aug 2024 18:01:07 GMT
ENTRYPOINT []
# Tue, 06 Aug 2024 18:01:07 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a92fbd042f28db16ac0b86e8841e492b886d701356ad15137dd1c8c01886aed5`  
		Last Modified: Sun, 09 Jun 2024 02:03:37 GMT  
		Size: 30.7 MB (30691272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f36cd9731e810f906a537246269ce46d4c6df5640b17be8e106679c9d9d10e4`  
		Last Modified: Tue, 23 Jul 2024 02:44:02 GMT  
		Size: 14.2 MB (14217406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0004675adb54a0b2db3644bb0f74bef7fe76f255eede3924644974de9f485b`  
		Last Modified: Tue, 23 Jul 2024 02:44:06 GMT  
		Size: 43.9 MB (43864344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c794a7e9c0de13d13e0e09e5cf7b7676cb93e132df8976e54a7ec9a7ccf41710`  
		Last Modified: Tue, 23 Jul 2024 02:44:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ac26e5f8f3381edea4c52990d1a21e381c4a3b00fb347c920259b1033f5aca`  
		Last Modified: Thu, 25 Jul 2024 17:48:58 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a57fe5287dd1fdb3ca3923a0c4198487fde7653e551381b2706255e6ac39bf`  
		Last Modified: Fri, 26 Jul 2024 20:07:47 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aaf8c889b1a90d4191d2777863eba277480768f06b3309f59abc15273b42dbb`  
		Last Modified: Wed, 07 Aug 2024 09:25:37 GMT  
		Size: 13.0 MB (12956894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92795462e5967c9c8c83a4c41d7fb589ec2f7ef8bf82d234db1e34d3a884415f`  
		Last Modified: Wed, 07 Aug 2024 09:25:37 GMT  
		Size: 2.8 MB (2772608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre17-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:1d684c0b02a94ac6cd631b55a752843937a514d6566763f3825eae973f1431d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3007815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ddda037b68c3f93e579373da2e5baf90353dc9e0751c460f22de67b54ee3912`

```dockerfile
```

-	Layers:
	-	`sha256:11633dc82ebe76d177e95ee65ecf701727a7583b83d74e8c372688ddee3be1d6`  
		Last Modified: Wed, 07 Aug 2024 09:25:37 GMT  
		Size: 3.0 MB (2983211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f9370f56675ddc2b65b033a4975a094d294102aa1d0e9481f42567236944cac`  
		Last Modified: Wed, 07 Aug 2024 09:25:37 GMT  
		Size: 24.6 KB (24604 bytes)  
		MIME: application/vnd.in-toto+json
