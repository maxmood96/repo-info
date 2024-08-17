## `tomcat:jre17-temurin-jammy`

```console
$ docker pull tomcat@sha256:2d82fb6a0cec6d1b36672ebb244f786a57cc7fdd3a82ed4d9aed2e2091f9c848
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

### `tomcat:jre17-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:9439204561b8b8653ccf4581b14db03f6582a373a40d163e59ac5d8af47300a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103772096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8538e6373fb771157adb47a65241978efc60e46aa9429832140ed39af279ec4f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 06 Aug 2024 18:01:07 GMT
ARG RELEASE
# Tue, 06 Aug 2024 18:01:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Aug 2024 18:01:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Aug 2024 18:01:07 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 06 Aug 2024 18:01:07 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 06 Aug 2024 18:01:07 GMT
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
	-	`sha256:2c864d9cb41f42368ff8c833862ee66e527965273569b7b660fbcd06fecd7d37`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068c2b63bb79f39191d7c8508cafae088638c9ddf7af8eb2f0c98544fdb3beae`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 13.0 MB (12960238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47726dd10df99decd36b121ef5565df106f90bfb1349a54b18e35ed0887c9b21`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 217.8 KB (217828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:008cef1fd37eb0d2a2beff349311609e9b2949ba7ace792d02502f30367a3ab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3553816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14a28ffb8c0b1f517d4e0ded83c8112ebd477ab336ca13725ce0d30c0177b34`

```dockerfile
```

-	Layers:
	-	`sha256:93155ced030a0eda4bea9ea7f58ce7ebf4fa5e8149809bf3760ccab5d95f2213`  
		Last Modified: Sat, 17 Aug 2024 04:07:33 GMT  
		Size: 3.5 MB (3531735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaad8945fc5e5821cfe8331db8ac8342de783fa20914afdddc833ff1184d663b`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 22.1 KB (22081 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:7a0484d0924fa2c836ed768f95d44d13fefb17a9eb3c6bf6aa40d59083159b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98070042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb77e6f99acfdb3565b79818d292f6166ce7802c935ef8e716242ee03994553b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 06 Aug 2024 18:01:07 GMT
ARG RELEASE
# Tue, 06 Aug 2024 18:01:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Aug 2024 18:01:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Aug 2024 18:01:07 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 06 Aug 2024 18:01:07 GMT
ADD file:ef971273c60fcf0d0b0a4e71a5e5421060cd7c316f1d9af068a193c23dc81d31 in / 
# Tue, 06 Aug 2024 18:01:07 GMT
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
	-	`sha256:26437c75f2463c43e93d57e3b82f05494c4729e204df737d8efdccc9110352e7`  
		Last Modified: Sat, 17 Aug 2024 05:15:11 GMT  
		Size: 12.9 MB (12934009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17182094c8866f658f7a92aa61cb81794e5db9dd15c32c0ba16f1d66452bea3`  
		Last Modified: Sat, 17 Aug 2024 05:15:10 GMT  
		Size: 190.9 KB (190921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:b1711fd3d529bb0a08538015ab6be898e729c47813783177e7b173531e997b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3555190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d3629c210cbb5a55f9833c656c471cfeab415f19376f6653c8b2eae9ff29a8`

```dockerfile
```

-	Layers:
	-	`sha256:8d19a3f2a1b4230135fe7906bb9dce008bf1d1bb124748948abefc73e95686d3`  
		Last Modified: Sat, 17 Aug 2024 05:15:10 GMT  
		Size: 3.5 MB (3532966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8844b29886631daff99cd83c1fc7a096bef17af36a42040a983b01d15c84fd2e`  
		Last Modified: Sat, 17 Aug 2024 05:15:10 GMT  
		Size: 22.2 KB (22224 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:677fbe16fda7121a1647d7b094358f91b085da3caea914dfc7cd6f2988ed0ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101137491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b2ea9af63a4b3cd8b34b34e461f1985badc559268612cb9661b9b5b9b3f95b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 06 Aug 2024 18:01:07 GMT
ARG RELEASE
# Tue, 06 Aug 2024 18:01:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Aug 2024 18:01:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Aug 2024 18:01:07 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 06 Aug 2024 18:01:07 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 06 Aug 2024 18:01:07 GMT
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
	-	`sha256:770a8f70b3e95f37901fe95f63fe4c58a754e12100bba2c936a4946209c05cad`  
		Last Modified: Sat, 17 Aug 2024 12:47:01 GMT  
		Size: 13.0 MB (12961772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0227cb065e7ffc0eef563e674bf05a8014b58f52da45a033f6e05c7e5044399`  
		Last Modified: Sat, 17 Aug 2024 12:47:00 GMT  
		Size: 216.8 KB (216788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:ea444b82f6e119ce8b61373f83232327bfc985be6ccdda2ee47c6173175219ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3554772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777bcecef76ca0c55dbe5947b937016e200f3fc65c8400c21eb064fe9f50ff6c`

```dockerfile
```

-	Layers:
	-	`sha256:74424e1b14363576a201456f2d2049c266ef0619f07928df6fc106edfc491989`  
		Last Modified: Sat, 17 Aug 2024 12:47:01 GMT  
		Size: 3.5 MB (3532027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be479d98057eb0fcf8cbf1a15eb0f99d6c2f488405c691362514af415816863c`  
		Last Modified: Sat, 17 Aug 2024 12:47:00 GMT  
		Size: 22.7 KB (22745 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:7f727d9dd6b533eb5edadcb405e1429957a89ae1703b06b1653d8480ac1c3d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109644119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7201b9156cf7ccb7b6767ecc6a66ab108bfb6f46842a418269bf668d048e10b6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 06 Aug 2024 18:01:07 GMT
ARG RELEASE
# Tue, 06 Aug 2024 18:01:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Aug 2024 18:01:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Aug 2024 18:01:07 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 06 Aug 2024 18:01:07 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 06 Aug 2024 18:01:07 GMT
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
	-	`sha256:09873dff4f0f5930294f70ff08b6644ad4d39b7747614fad9b43e67e04bc821a`  
		Last Modified: Sat, 17 Aug 2024 12:02:57 GMT  
		Size: 13.0 MB (12973522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dee9159fd4de0b1da99770d98cb79ec7512ddc1c31b83b5a8747fa941540faf`  
		Last Modified: Sat, 17 Aug 2024 12:02:56 GMT  
		Size: 249.6 KB (249626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:b839fbdd141e35bcd1de43779b5125f17d9e70e6d7a637f44422931807d77156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3558412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7963b860f02203842de355fb8f5c9a544dd5fdc9b79b06178e780e8d0c67e6`

```dockerfile
```

-	Layers:
	-	`sha256:2bd2a40bb241a31b8f8ba9a1acc1b9cce9ce2d0da16b93150c705f3dd15c3b13`  
		Last Modified: Sat, 17 Aug 2024 12:02:56 GMT  
		Size: 3.5 MB (3536254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92d6c743c3a0df4966e94d47ccb7e76c9db286a8e4c033a9de708e65da25ddf7`  
		Last Modified: Sat, 17 Aug 2024 12:02:56 GMT  
		Size: 22.2 KB (22158 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:a124e530fc11d3d2158f7f8547234255adda20d97a52049cf008bcd2f9c2cbe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.6 MB (98642602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf924f0bf5fbe174ba122df4e4838fcbec4fd235980990a77937f49512b94758`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 06 Aug 2024 18:01:07 GMT
ARG RELEASE
# Tue, 06 Aug 2024 18:01:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Aug 2024 18:01:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Aug 2024 18:01:07 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 06 Aug 2024 18:01:07 GMT
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
# Tue, 06 Aug 2024 18:01:07 GMT
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
	-	`sha256:cf0e4281b9d6626e05ca9d0f2381bed01fa85dec4e10ba6a4f6dd7c1b1c345cc`  
		Last Modified: Sat, 17 Aug 2024 07:55:00 GMT  
		Size: 13.0 MB (12963273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38785f1b4c45eafa034f1a99940d68d02673a912f86af485c61d956e894212d`  
		Last Modified: Sat, 17 Aug 2024 07:55:00 GMT  
		Size: 219.3 KB (219280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:ce01558aa5ac9fb9da4b789ea3e55cbea0ef3b44b411094179f21d42e1bdb193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3554963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470810cadc9e6e9e86455985da12ba9e047a0b17a82ca90ac6b0cab9d1ed454d`

```dockerfile
```

-	Layers:
	-	`sha256:d8e0bbe1b90bf669dc494e3baacd970ad744610731a11b35d4049fafa46d6e8c`  
		Last Modified: Sat, 17 Aug 2024 07:55:00 GMT  
		Size: 3.5 MB (3532857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20b9ecc22a2ec7a536443aa44cb6df49f0fae16434cf52ee9aaa35df67f9cb28`  
		Last Modified: Sat, 17 Aug 2024 07:55:00 GMT  
		Size: 22.1 KB (22106 bytes)  
		MIME: application/vnd.in-toto+json
