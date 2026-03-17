## `tomcat:10-jre17-temurin-jammy`

```console
$ docker pull tomcat@sha256:87bd6d44f7c006229a60ebbdcd63de95808d11811aba160a9b7c2231642e6d31
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

### `tomcat:10-jre17-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:4be1e586b74fa5ef6721067b9472fe25220de51eba7bf51f736b41377c548cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107649752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e7522f534e43133f41ad9988d2481aa98eaa4cfd2a2f17720e5a7cf32e469f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:19:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:19:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:19:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:19:53 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:19:53 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Feb 2026 20:19:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:19:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:19:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:19:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 21:56:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Feb 2026 21:56:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:56:28 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Feb 2026 21:56:28 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Feb 2026 21:56:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:56:28 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:56:28 GMT
ENV TOMCAT_MAJOR=10
# Tue, 17 Feb 2026 21:56:28 GMT
ENV TOMCAT_VERSION=10.1.52
# Tue, 17 Feb 2026 21:56:28 GMT
ENV TOMCAT_SHA512=241183fe5dec15936205ec495b65e04218117affc10e90c5fbc56bce0b4f031ee944d468c128f0ae484fd1d5bd9bec22b65a95a8cfd94cb7fc1f12c7ef434d99
# Tue, 17 Feb 2026 21:56:43 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Feb 2026 21:56:51 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:56:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Feb 2026 21:56:51 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Feb 2026 21:56:51 GMT
ENTRYPOINT []
# Tue, 17 Feb 2026 21:56:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87feb9ceb63e3bd1223018985561715a1a2465cf9a71dfe129c73bf7ac820ff1`  
		Last Modified: Tue, 17 Feb 2026 20:20:10 GMT  
		Size: 16.1 MB (16147776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4378de8e79030df05f34e09e0ecb7a5313c1e330edc4380bb77541c0f0124e`  
		Last Modified: Tue, 17 Feb 2026 20:20:10 GMT  
		Size: 47.4 MB (47434764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc17c801dc54fceec28a1a4f4ed2b2ba1e05432b2bd80e7132f4e19a9594f47b`  
		Last Modified: Tue, 17 Feb 2026 20:20:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9acf020f113198a7e1c7e249274cf9c9165eb60413f2805dd3f47f2b18721`  
		Last Modified: Tue, 17 Feb 2026 20:20:09 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ca722b7e214a9a78dcfaa474c5478a7d8883d89c1b3738029dcab0cd1d3600`  
		Last Modified: Tue, 17 Feb 2026 21:57:02 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b17739a7789f861628b98342fce95e6741098fb72836b2435f05df7e75b0669`  
		Last Modified: Tue, 17 Feb 2026 21:57:03 GMT  
		Size: 14.3 MB (14297497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ab5c4f77a3d217c274afadf652bb1422ef910c9336271d4b0226ecdd655a53`  
		Last Modified: Tue, 17 Feb 2026 21:57:02 GMT  
		Size: 229.7 KB (229704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:39e32aacbb5ca5b7371e52b34e07efbb365b91ee3fa85aff206846054affe329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3962420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4d2ade3b36b04f2c1fafb83be58029d29d7cf3bb5889cb5115c97f777e59b6`

```dockerfile
```

-	Layers:
	-	`sha256:acf0ce01c3d71806f94e2304bed4f1d17046b758c76b43da39ee358673135faf`  
		Last Modified: Tue, 17 Feb 2026 21:57:02 GMT  
		Size: 3.9 MB (3941199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:added4145401db31a8f55cf9ab07885c9b0e07ff80b4c3068fc52eec98648d1c`  
		Last Modified: Tue, 17 Feb 2026 21:57:02 GMT  
		Size: 21.2 KB (21221 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre17-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:56f9340e60e268106a6461deb0b6993ff1b2967db0d40648ac06e708b6211b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102054249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ad20f0f4d34383c49c10e2829572821ed8e401247763dab53a490de53f22f6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 10 Feb 2026 17:41:55 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:41:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:41:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:41:55 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:41:58 GMT
ADD file:5c6b4f7fe4e36ff387edbef0b3a7c72fa9a66f82297c2c1a27259d6be00727bf in / 
# Tue, 10 Feb 2026 17:41:58 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:11:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:11:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:11:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:11:49 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Feb 2026 20:12:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 21:43:16 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Feb 2026 21:43:16 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:43:16 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Feb 2026 21:43:16 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Feb 2026 21:43:16 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:43:16 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:43:16 GMT
ENV TOMCAT_MAJOR=10
# Tue, 17 Feb 2026 21:43:16 GMT
ENV TOMCAT_VERSION=10.1.52
# Tue, 17 Feb 2026 21:43:16 GMT
ENV TOMCAT_SHA512=241183fe5dec15936205ec495b65e04218117affc10e90c5fbc56bce0b4f031ee944d468c128f0ae484fd1d5bd9bec22b65a95a8cfd94cb7fc1f12c7ef434d99
# Tue, 17 Feb 2026 21:43:16 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Feb 2026 21:43:23 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:43:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Feb 2026 21:43:24 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Feb 2026 21:43:24 GMT
ENTRYPOINT []
# Tue, 17 Feb 2026 21:43:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8994f3e4ab606dcbf77ca1a5364851191cbe725563408ee7cd2a667cb364bed0`  
		Last Modified: Tue, 10 Feb 2026 18:13:45 GMT  
		Size: 26.6 MB (26644404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdebecdfda6f37795a134fe223b77943d0c223cdcbb0164712d9bcdcdb2e364`  
		Last Modified: Tue, 17 Feb 2026 20:12:06 GMT  
		Size: 15.9 MB (15890645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b13f12cf644f04727ed3bcaa3e124d1172894ee51e71ce428faae9ce34c83c`  
		Last Modified: Tue, 17 Feb 2026 20:12:31 GMT  
		Size: 45.0 MB (45044355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6b24107adb5a61c80f1453f46f1b75679b57367a79573541e0f9e8fa4276e7`  
		Last Modified: Tue, 17 Feb 2026 20:12:29 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c68f040ae8ed0ff9d7a433200cdb9bb6f9aca0a9a91a4429072addbdccd305b`  
		Last Modified: Tue, 17 Feb 2026 20:12:29 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897f3aab39ff3fbb43bf6d9fa2bc264f6c7f29d7286b6a54269dd2c2d85ea853`  
		Last Modified: Tue, 17 Feb 2026 21:43:33 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6694086d03956efff3ad79cfe34a46d169f03fac33ef3ec7362a653658d46c80`  
		Last Modified: Tue, 17 Feb 2026 21:43:33 GMT  
		Size: 14.3 MB (14269843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb98b2a798036471f099e48cdfcdbb82a333d88e8fd83aae10d3a5408aa063a1`  
		Last Modified: Tue, 17 Feb 2026 21:43:33 GMT  
		Size: 202.4 KB (202361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:4733839253d16d6681da0198be0c3b721146aea83801e87a74cba3078e2f23b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d00ed14bf4628b00e3f32c1e0313dc442ca7b71adf9921d7203795a914ad7b`

```dockerfile
```

-	Layers:
	-	`sha256:f62c1b39bc4593aa7458d87b7d9e6b1dd457ec3b296e8b54e03a99a7cd8a21f6`  
		Last Modified: Tue, 17 Feb 2026 21:43:33 GMT  
		Size: 3.9 MB (3943534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a40aaba8f7a8fd42724f7473998e9d8e51d30152a685f6169bc3358d155c73e0`  
		Last Modified: Tue, 17 Feb 2026 21:43:33 GMT  
		Size: 21.3 KB (21340 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre17-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:7fc844e75a40d283b3c9818093dc7562f821562f9e45fd8ec41f2a6ee3e0b8df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104931048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc05df2138278704a65e4991de97f37fa8cb5aa212a5621387e13a99e14e6ee`
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
# Tue, 17 Mar 2026 01:24:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:24:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:24:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:24:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:24:17 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Mar 2026 01:24:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 01:24:21 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:24:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:24:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 03:29:50 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Mar 2026 03:29:50 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:29:50 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Mar 2026 03:29:50 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Mar 2026 03:29:50 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Mar 2026 03:29:50 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Mar 2026 03:29:50 GMT
ENV TOMCAT_MAJOR=10
# Tue, 17 Mar 2026 03:29:50 GMT
ENV TOMCAT_VERSION=10.1.52
# Tue, 17 Mar 2026 03:29:50 GMT
ENV TOMCAT_SHA512=241183fe5dec15936205ec495b65e04218117affc10e90c5fbc56bce0b4f031ee944d468c128f0ae484fd1d5bd9bec22b65a95a8cfd94cb7fc1f12c7ef434d99
# Tue, 17 Mar 2026 03:29:50 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Mar 2026 03:29:59 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:30:00 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Mar 2026 03:30:00 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Mar 2026 03:30:00 GMT
ENTRYPOINT []
# Tue, 17 Mar 2026 03:30:00 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962ff3a9e44a298002491adeb36eb584ccda2eae305116b890be005bdf028a32`  
		Last Modified: Tue, 17 Mar 2026 01:24:33 GMT  
		Size: 16.1 MB (16073508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf62962d30fa85f0a393ba2b88ed7030994f0dfde9bc76acf07fa1dce073d76b`  
		Last Modified: Tue, 17 Mar 2026 01:24:34 GMT  
		Size: 46.9 MB (46922068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6e05267fe05fe7df77eab3eb141f795abbf8d140204208e4033a35938d2e7e`  
		Last Modified: Tue, 17 Mar 2026 01:24:33 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df8a52c9bf0e659b5cec871191dfa0627d2e050ca28c43669e4d98d61cf0734`  
		Last Modified: Tue, 17 Mar 2026 01:24:33 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c789f18cdf9b495ffac9a5934a9cf9083a388d055678f888cd1279d80d7c6f5`  
		Last Modified: Tue, 17 Mar 2026 03:30:09 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa0ca81d5af09fade23f78f95e00ae4f10d8e9b6e89b4ad8e9da66a532eb23a`  
		Last Modified: Tue, 17 Mar 2026 03:30:09 GMT  
		Size: 14.3 MB (14297781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298fd692b6dbddac5781206f20054387ebb2638bf5dff869416801c2c5738940`  
		Last Modified: Tue, 17 Mar 2026 03:30:09 GMT  
		Size: 246.0 KB (246025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:0a595f737f40bf70add797659eeb1d5676760467e39b78dc40da2d2b1514d800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3963924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6e5e0f8138789ebd20f6c257c8239d16e75ae87b67eeaca902b94801611eac`

```dockerfile
```

-	Layers:
	-	`sha256:f8792c9fef0540e827bcf98b4e510d793e4f64b2b03b897a9290b5e093be28f0`  
		Last Modified: Tue, 17 Mar 2026 03:30:09 GMT  
		Size: 3.9 MB (3942555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37721de0d476ffc576ae8fc034c8bae57e9a9af31ff0693ad03545cca252f216`  
		Last Modified: Tue, 17 Mar 2026 03:30:09 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre17-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:81da9406efa4eba14736853efcab8b07ba9f6fe05376e7ad30631c8afd64785c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (113968825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf14ac049a9b1c14c9f754ab185c1d61432447444dd3f752d7a15f08823e9d5`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 10 Feb 2026 17:41:33 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:41:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:41:39 GMT
ADD file:0418bf4995f9b54380cc1e509e3f7d65bb07aed9a367528d0b1084f0a34f3bf3 in / 
# Tue, 10 Feb 2026 17:41:39 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:12:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:12:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:12:14 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Feb 2026 20:19:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:19:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:19:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:19:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Feb 2026 01:06:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 18 Feb 2026 01:06:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 01:06:20 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 18 Feb 2026 01:06:21 GMT
WORKDIR /usr/local/tomcat
# Wed, 18 Feb 2026 01:06:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 18 Feb 2026 01:06:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 18 Feb 2026 01:06:21 GMT
ENV TOMCAT_MAJOR=10
# Wed, 18 Feb 2026 01:06:21 GMT
ENV TOMCAT_VERSION=10.1.52
# Wed, 18 Feb 2026 01:06:21 GMT
ENV TOMCAT_SHA512=241183fe5dec15936205ec495b65e04218117affc10e90c5fbc56bce0b4f031ee944d468c128f0ae484fd1d5bd9bec22b65a95a8cfd94cb7fc1f12c7ef434d99
# Wed, 18 Feb 2026 01:09:32 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 18 Feb 2026 01:09:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 01:09:41 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 18 Feb 2026 01:09:41 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 18 Feb 2026 01:09:41 GMT
ENTRYPOINT []
# Wed, 18 Feb 2026 01:09:41 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:95401e425d899946469007a0ce4b02622cf84a67cdd684aa25d61d472fffc38f`  
		Last Modified: Tue, 10 Feb 2026 18:13:52 GMT  
		Size: 34.4 MB (34446102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09208b6847dfa6f5490506d2bee63693e328ebe8d9f225275578ecadc7fc35c0`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 17.6 MB (17619110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8303684a7a826717048188d2ff057664ca6a98321430f0aa53fb1b27f038b329`  
		Last Modified: Tue, 17 Feb 2026 20:19:41 GMT  
		Size: 47.3 MB (47331436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4510d40d77c8d8b57ca547880766c7f582d2aa4dc9e4959ad89cda6019870e6f`  
		Last Modified: Tue, 17 Feb 2026 20:19:38 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac997d838a9e36f770f7a140ce79875b841cc6e6ad27d09efd8d4264d9c11f0f`  
		Last Modified: Tue, 17 Feb 2026 20:19:38 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e448ce2f8dd41470f7214625c4e5e6141706666c5b8d0ccfc33ce42e215035`  
		Last Modified: Wed, 18 Feb 2026 01:06:48 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8859ed62e719eafa9bfe8b0ffc6e21a0606804cd8f9c4f16c3ac9b016babad`  
		Last Modified: Wed, 18 Feb 2026 01:10:01 GMT  
		Size: 14.3 MB (14310528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f395f7254370edbabb63e0ca3ea09193167831cb8cd9f9c5e91ba28efe07f09`  
		Last Modified: Wed, 18 Feb 2026 01:10:01 GMT  
		Size: 259.0 KB (259006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:e457d87fa6dbcdd0b9217d7abb7699078d7238ee1d58a9a227e89671f2c71cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3966560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83df2c262cac582fd428483de6563c718f3e71a12858612634d3f741253e71d3`

```dockerfile
```

-	Layers:
	-	`sha256:e1405128fc23a8a7f8faea1054b0a6455ffe912f90656a3e7a404cf2d3711f62`  
		Last Modified: Wed, 18 Feb 2026 01:10:00 GMT  
		Size: 3.9 MB (3945287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab756e4bb57bf5599e574be1732c526df0004b09ba0e467947a0f9cb34396cb1`  
		Last Modified: Wed, 18 Feb 2026 01:10:00 GMT  
		Size: 21.3 KB (21273 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre17-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:156f6852dde6220c75dc0ed77f0a9452bbcff712bceb68d923651c18ae68aafa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103094635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68006cdf16d1e27a8457fc5b5a638d2c65914f477163eaa027cb31f964525a2`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 10 Feb 2026 17:41:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:41:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:41:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:41:31 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:41:33 GMT
ADD file:682bbddd1f3d784d0c4ab5eef9460f0b47a94f3c62f629b59163a7f6543a159f in / 
# Tue, 10 Feb 2026 17:41:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:10:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:10:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:10:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:10:25 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:10:25 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Feb 2026 20:12:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:12:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:12:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 22:43:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Feb 2026 22:43:54 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:43:54 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Feb 2026 22:43:55 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Feb 2026 22:43:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 22:43:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 22:43:55 GMT
ENV TOMCAT_MAJOR=10
# Tue, 17 Feb 2026 22:43:55 GMT
ENV TOMCAT_VERSION=10.1.52
# Tue, 17 Feb 2026 22:43:55 GMT
ENV TOMCAT_SHA512=241183fe5dec15936205ec495b65e04218117affc10e90c5fbc56bce0b4f031ee944d468c128f0ae484fd1d5bd9bec22b65a95a8cfd94cb7fc1f12c7ef434d99
# Tue, 17 Feb 2026 22:45:57 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Feb 2026 22:46:01 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 22:46:02 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Feb 2026 22:46:02 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Feb 2026 22:46:02 GMT
ENTRYPOINT []
# Tue, 17 Feb 2026 22:46:02 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4e2905dbd81d6a42c24ec5f7ce51f2d8f24a616b4fe2e90d0be791922a8d3b5f`  
		Last Modified: Tue, 10 Feb 2026 18:14:06 GMT  
		Size: 28.0 MB (28004382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523cb06f330195795b372351c12383f3bda2bbf16f797add39b1a30af72a5414`  
		Last Modified: Tue, 17 Feb 2026 20:11:11 GMT  
		Size: 16.1 MB (16146864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ec0fed3b600a251c466c2c2944b66cac2f0ce62c1fff90221c74dab89482a8`  
		Last Modified: Tue, 17 Feb 2026 20:13:13 GMT  
		Size: 44.4 MB (44409704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52359af092ad3354cb9fefc702cd754d65e090955279b87669536610b52ca7d6`  
		Last Modified: Tue, 17 Feb 2026 20:13:11 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5ac8bf40469a9db12ed544a7a99d7cba5a7827137aad5d8ccde059f53a687c`  
		Last Modified: Tue, 17 Feb 2026 20:13:11 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235d0592d31a5cb3436b60fe5f56ae885bb9db06c781c5bf74ec49f1bcad8068`  
		Last Modified: Tue, 17 Feb 2026 22:44:18 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eae8a81e440ccde1dc24427f6bb1acb383b94dedb66420e143958ba2342561c`  
		Last Modified: Tue, 17 Feb 2026 22:46:23 GMT  
		Size: 14.3 MB (14300104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf76250a687e8789dfc220351a00e012a25d9f32380fd2601787bbb89b82c01`  
		Last Modified: Tue, 17 Feb 2026 22:46:23 GMT  
		Size: 230.9 KB (230940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:340163065a836fe8b4398c369d196103a3855e75e9fe63848336a8c06dbbc1ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c323809836d8673fa2d2da3a7e907c78047452baef03539736125292ac9a16`

```dockerfile
```

-	Layers:
	-	`sha256:ea821457d9f24ce61c9888b90c8aa145ff8aaa2980ebff95478963cb176c803e`  
		Last Modified: Tue, 17 Feb 2026 22:46:23 GMT  
		Size: 3.9 MB (3942790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c3514dfd01be66d1ae28d078442d279dbbb59a8ea6a93a95601bfc897c5b495`  
		Last Modified: Tue, 17 Feb 2026 22:46:23 GMT  
		Size: 21.2 KB (21221 bytes)  
		MIME: application/vnd.in-toto+json
