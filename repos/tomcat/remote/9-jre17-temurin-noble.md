## `tomcat:9-jre17-temurin-noble`

```console
$ docker pull tomcat@sha256:07c4be59e41d6e9c41a7bb0939f94cbc5c7a1f31c7f85a5bafca23edc6f01859
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

### `tomcat:9-jre17-temurin-noble` - linux; amd64

```console
$ docker pull tomcat@sha256:bca83d9b6c49aec14ba66dd7531a93e63173a7a0f2fa79b0c355ceb4e0277a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105254131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7fd3683f02ee7b00ede2e17b655f6014cbf8db528f7b317deea345157bb2cb`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 08 Oct 2024 14:03:39 GMT
ARG RELEASE
# Tue, 08 Oct 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Oct 2024 14:03:39 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Tue, 08 Oct 2024 14:03:39 GMT
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
# Tue, 08 Oct 2024 14:03:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 14:03:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
WORKDIR /usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_MAJOR=9
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_VERSION=9.0.96
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_SHA512=ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93
# Tue, 08 Oct 2024 14:03:39 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 08 Oct 2024 14:03:39 GMT
ENTRYPOINT []
# Tue, 08 Oct 2024 14:03:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beb5331d363596b1827b1acf45f54c2c7746f8406636b8d72b09022b11fb7b3`  
		Last Modified: Fri, 11 Oct 2024 23:56:25 GMT  
		Size: 13.8 MB (13771214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a5bfb8d4474120f18cd4e2e21c2fb6e7d9144d3bfb8f8fdf9016d706eebb88`  
		Last Modified: Fri, 11 Oct 2024 23:57:59 GMT  
		Size: 47.3 MB (47280244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14688e11a21ea2eaa960947d01105ba680fe07492d6eac637d88f964f9396719`  
		Last Modified: Fri, 11 Oct 2024 23:57:53 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057686f76905cbfe0bc06f7c1af90d04d9dd676958004abc9661ee80c48c23db`  
		Last Modified: Fri, 11 Oct 2024 23:57:53 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f8e1dc9ad840b7ff5db6a0455823fbc33ee9cd46410852b9a48a1860cc1e3a`  
		Last Modified: Sat, 12 Oct 2024 01:56:28 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83a82029587f307c6cab896483c8e22068999617c22a3f5d8701ef0498e3ac3`  
		Last Modified: Sat, 12 Oct 2024 01:56:28 GMT  
		Size: 13.4 MB (13374008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d6c6358d2334c88eef14624b92a02ce40a6d51cf8135b31b06a01c688974bc`  
		Last Modified: Sat, 12 Oct 2024 01:56:28 GMT  
		Size: 212.9 KB (212918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:acfb04cc267ca968c2fb712a9d3cae722234cc8a2dc0c1220f5ac2c1e7786212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3071595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487540854fcce4b721c44ec54276877acf67926c62c0c9bae19b210bb5e0a2ec`

```dockerfile
```

-	Layers:
	-	`sha256:802e44e6dbd382a8e66a12c98f31ad3949a624847cd7e38905ba3e811c886bf4`  
		Last Modified: Sat, 12 Oct 2024 01:56:28 GMT  
		Size: 3.0 MB (3047806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d87c6a9483045f8024bcbdf775dfc25e132ed0b2e814f11b6a011b3b33ed9635`  
		Last Modified: Sat, 12 Oct 2024 01:56:28 GMT  
		Size: 23.8 KB (23789 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-noble` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:641f617b2ee4cb4465482aaad433135fa4c614cbcf8a2c55d5b5e77b9e77440c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.3 MB (99314125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228f8c5df015a13962bd5adcaf5d7304862f0db7b68fcbeafbd75f26d7ab82b1`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 08 Oct 2024 14:03:39 GMT
ARG RELEASE
# Tue, 08 Oct 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Oct 2024 14:03:39 GMT
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Tue, 08 Oct 2024 14:03:39 GMT
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
# Tue, 08 Oct 2024 14:03:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 14:03:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
WORKDIR /usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_MAJOR=9
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_VERSION=9.0.96
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_SHA512=ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93
# Tue, 08 Oct 2024 14:03:39 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 08 Oct 2024 14:03:39 GMT
ENTRYPOINT []
# Tue, 08 Oct 2024 14:03:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:02c8f8f0873a74c67ece25c25d14882bda4d283742faf5b1b57c79636c7bb7a3`  
		Last Modified: Wed, 16 Oct 2024 01:28:34 GMT  
		Size: 27.7 MB (27734804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249e0f259e41b9eabe172538e41f6fdd2856d872ba698b9d718ebdc1e63a1f0f`  
		Last Modified: Wed, 16 Oct 2024 01:33:46 GMT  
		Size: 13.1 MB (13135129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c95f3aded7a12b20c10607f78d42ca2bae0a23e0d4d2feab28d2bf3a2c6d9e`  
		Last Modified: Wed, 16 Oct 2024 01:36:48 GMT  
		Size: 44.9 MB (44944613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9676ddaebcff1a6d4fa93605e8803600b235c44ceb017373a5fb57c5bc59051`  
		Last Modified: Wed, 16 Oct 2024 01:36:41 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbc510c38d8a368f823d80afe3f16970e0a7f101eceeb8c8fe31a098f8c3247`  
		Last Modified: Wed, 16 Oct 2024 01:36:41 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b4dbce2f0a657068248637f22df61c18313244ff8c082332c7e27fd765ac90`  
		Last Modified: Wed, 16 Oct 2024 03:23:32 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98afc448d23166217004d10f38ae110d81ca64c7c026eb46a4e0b219aaa2932c`  
		Last Modified: Wed, 16 Oct 2024 03:24:51 GMT  
		Size: 13.3 MB (13313228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1ee13cf8c25453fe7da68aebeb7076dc30a93debac00563834b6690141353f`  
		Last Modified: Wed, 16 Oct 2024 03:24:51 GMT  
		Size: 183.9 KB (183882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:e30b500e71374e758417f2b32b12fe6f8ddad585947a392e4dc3594da2145b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3074144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6baf41cf721c3dcb0c5915973955ff33c1652aab28fbca84bdd655b332871d44`

```dockerfile
```

-	Layers:
	-	`sha256:ff51b3e851fab8b525316a88effc8c11fd2d1b4c784cacbff6ebd4dd5dcda4d0`  
		Last Modified: Wed, 16 Oct 2024 03:24:51 GMT  
		Size: 3.1 MB (3050173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f9c4afcdb26d61e19910888e3b3c1961e0f3b5db1bb8f14f8a06ba2647873c9`  
		Last Modified: Wed, 16 Oct 2024 03:24:50 GMT  
		Size: 24.0 KB (23971 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-noble` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:494637bbfff3d2c1781360324fdf21f82453a6165e42d645f2f84eac4b24b5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104100159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7acac76e257b3f99bfb5d0698bed92418e09212179cf3e76ec9b0ca422308540`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 08 Oct 2024 14:03:39 GMT
ARG RELEASE
# Tue, 08 Oct 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Oct 2024 14:03:39 GMT
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
# Tue, 08 Oct 2024 14:03:39 GMT
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
# Tue, 08 Oct 2024 14:03:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 14:03:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
WORKDIR /usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_MAJOR=9
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_VERSION=9.0.96
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_SHA512=ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93
# Tue, 08 Oct 2024 14:03:39 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 08 Oct 2024 14:03:39 GMT
ENTRYPOINT []
# Tue, 08 Oct 2024 14:03:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:bbc050e99a562418305b0d9003042b38fc24f8c8c94687cf4c69ed6cd001161e`  
		Last Modified: Sat, 12 Oct 2024 00:07:49 GMT  
		Size: 30.0 MB (29953586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056e93bad04245da5d01c9d3de3081a8ad7d5bcd80abdd0ada262fae4f313b5c`  
		Last Modified: Sat, 12 Oct 2024 00:13:29 GMT  
		Size: 13.8 MB (13798544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853caa3c083513913a4d356cb3b39b0ac3d2ff47322ba38de443873ed51c1f68`  
		Last Modified: Sat, 12 Oct 2024 00:14:55 GMT  
		Size: 46.7 MB (46746340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d32be1f4c71b504e23e7beb4a37f97a9e4d4f1cec32b76f05137236953e697`  
		Last Modified: Sat, 12 Oct 2024 00:14:50 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec015029a7bc743e5d90cd9ef1afef6560543090947520b51dcb935fa7f532a`  
		Last Modified: Sat, 12 Oct 2024 00:14:50 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414fc7720ee96d4150bf05aecf6f92a639d192a2e6822d5564b89b860630508e`  
		Last Modified: Sat, 12 Oct 2024 07:32:16 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c058e01d6c607dadd444a121daf9a14ca27f4e8205b6a452dcf9d6d1a3422459`  
		Last Modified: Sat, 12 Oct 2024 07:33:53 GMT  
		Size: 13.4 MB (13386548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c597bf648be1166d9505fd693a4ed3079094c3fd1ac3195df71d0684b6a33b6`  
		Last Modified: Sat, 12 Oct 2024 07:33:50 GMT  
		Size: 212.7 KB (212671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:7fee9cc4f4bd9399d6d381b93a74a59cfcbf91254472ca2211e10c8448fc0f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3072360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca0c9389eed84c585a4de2467dc5db5b9d6187cda99008752c3bfde1ef4f1d3`

```dockerfile
```

-	Layers:
	-	`sha256:7aadad2bcc2bdcd9c5980c46abe86ae03cbd8926d21301173ecb2c04592e7f5f`  
		Last Modified: Sat, 12 Oct 2024 07:33:50 GMT  
		Size: 3.0 MB (3048333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7846e3eedf992a4590b3dc4b708bfbf63b7474fa732120428f282725ecda6aa`  
		Last Modified: Sat, 12 Oct 2024 07:33:49 GMT  
		Size: 24.0 KB (24027 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-noble` - linux; ppc64le

```console
$ docker pull tomcat@sha256:5d51bfe4ca259ea43bb3cec58793881e1b66485f92765bb509cbb9e250da3bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111201301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2063b5e1175acd7ae11430da197d25913d881234e25d4daea0c4a03ac92cce9`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 08 Oct 2024 14:03:39 GMT
ARG RELEASE
# Tue, 08 Oct 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Oct 2024 14:03:39 GMT
ADD file:6ec0ebf9a019b7c00b0121b97e89fcad881460415f8dcb9bb94b1cc7f5d0a5bc in / 
# Tue, 08 Oct 2024 14:03:39 GMT
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
# Tue, 08 Oct 2024 14:03:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 14:03:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
WORKDIR /usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_MAJOR=9
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_VERSION=9.0.96
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_SHA512=ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93
# Tue, 08 Oct 2024 14:03:39 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 08 Oct 2024 14:03:39 GMT
ENTRYPOINT []
# Tue, 08 Oct 2024 14:03:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:870d99e54f9cdff4b5ba4448d967491786519e8cbf54f10bd271e5dd32285ceb`  
		Last Modified: Fri, 11 Oct 2024 23:47:07 GMT  
		Size: 35.5 MB (35513269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15086c23dcc309fa9386aa3f0907d6689b8bc489e8f1311ca8248bffcaf162db`  
		Last Modified: Fri, 11 Oct 2024 23:55:29 GMT  
		Size: 14.9 MB (14914320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bd243e7d3899c2c3d67a069f49da5561814c1a0f6c7dfb63efbf448720c7c4`  
		Last Modified: Fri, 11 Oct 2024 23:57:10 GMT  
		Size: 47.1 MB (47115959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a5fbf9a5b2ec71e98a276a8fb513c9eac5b03647af7c9831298bad13c47a3d`  
		Last Modified: Fri, 11 Oct 2024 23:57:02 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0fa5e8a336b50515a04ee64f90f7ce01029f39c7ac6c91ff187c4486108fab`  
		Last Modified: Fri, 11 Oct 2024 23:57:02 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4122c1f8575d53652bd63e79c25b6b4b38c171c9d134e335a53919e4689f6d04`  
		Last Modified: Sat, 12 Oct 2024 05:08:15 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12887b470956b471a2b4f57f026aea4dfe11a9509d8ce362614647a448a29f1`  
		Last Modified: Sat, 12 Oct 2024 05:10:22 GMT  
		Size: 13.4 MB (13411460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6e533a69e3792280eb59f7d0de4a67088a1eb65bdd4de64eb2f8a400c6d9b8`  
		Last Modified: Sat, 12 Oct 2024 05:10:21 GMT  
		Size: 243.8 KB (243825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:3d421b6f3261be071e17eaa97fd4fae6aa3227ba2101588ab07c59950e91d600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3075635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaae2edce162162e8ed5f279081ebed1e0cb70031b9fe2921f485d6cd8cb3632`

```dockerfile
```

-	Layers:
	-	`sha256:04a64422071707f4509e71a4bcc696ed3ad091db4c4d62f5328f93ff5429e4d5`  
		Last Modified: Sat, 12 Oct 2024 05:10:21 GMT  
		Size: 3.1 MB (3051741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eacb2c752820c878f380478ef780bfc023d916ef73b9988f7f8a2c2e2710aeaa`  
		Last Modified: Sat, 12 Oct 2024 05:10:21 GMT  
		Size: 23.9 KB (23894 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-noble` - linux; s390x

```console
$ docker pull tomcat@sha256:d74e787f0d9b7759432f4378416226837f985746995e99d0fc7a42b271dc46a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102330688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0bd991c35dee5dfeabae513d8b2fce51c8956533a395e84bf21708e7e0bf71`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 08 Oct 2024 14:03:39 GMT
ARG RELEASE
# Tue, 08 Oct 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Oct 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Oct 2024 14:03:39 GMT
ADD file:77ba16e2cf3c210906ec7587ab14314afc15cb73af4337fde69ac35187fdb263 in / 
# Tue, 08 Oct 2024 14:03:39 GMT
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
# Tue, 08 Oct 2024 14:03:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 14:03:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
WORKDIR /usr/local/tomcat
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 08 Oct 2024 14:03:39 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_MAJOR=9
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_VERSION=9.0.96
# Tue, 08 Oct 2024 14:03:39 GMT
ENV TOMCAT_SHA512=ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93
# Tue, 08 Oct 2024 14:03:39 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 08 Oct 2024 14:03:39 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 08 Oct 2024 14:03:39 GMT
ENTRYPOINT []
# Tue, 08 Oct 2024 14:03:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:fbce550314e6331afd2ad455e770bf99838b047eaec77c6d995b82c2ba1a18ae`  
		Last Modified: Wed, 16 Oct 2024 01:17:45 GMT  
		Size: 30.7 MB (30661606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4154e706a872d69678b9815a958201c73822602cf188b0f18fdec44d1c455483`  
		Last Modified: Wed, 16 Oct 2024 01:26:30 GMT  
		Size: 14.2 MB (14195095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580e723ef2ab7ae3a6a652a907eaadac623182fae6ebc26c70e5502347c1ac62`  
		Last Modified: Wed, 16 Oct 2024 01:28:10 GMT  
		Size: 43.9 MB (43864344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4f02f05ac3875e0fdc3b606700c8cc014ab06f2339a3cf363abac3b7845af5`  
		Last Modified: Wed, 16 Oct 2024 01:28:04 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4480171c898d0eb09820ffc37ce92233a320e1eb71bc2c81d8a2361950244090`  
		Last Modified: Wed, 16 Oct 2024 01:28:03 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41e141e5ce76efceb4da270c5622044e77d7a20332ed6fe2ec80b9b43ed46f0`  
		Last Modified: Wed, 16 Oct 2024 03:02:04 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8464dbf5bb1d56f2d9699c2823e6928701953ebdfaba9cd8befca4ed7c66ef64`  
		Last Modified: Wed, 16 Oct 2024 03:04:10 GMT  
		Size: 13.4 MB (13386794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76daea59cf4dbbb35a2d490fabc6b7e05630c6fc9c3120ba78bc523db9ad9a8`  
		Last Modified: Wed, 16 Oct 2024 03:04:10 GMT  
		Size: 220.4 KB (220379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:679ac49e62d95b8aa612d492d6d76ceec36e6159de7e9cb6d323476ea3173598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3073825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840cc12aed3a260a882ce965a7a3f40f8ef535262565d20d5465a65d6c47840f`

```dockerfile
```

-	Layers:
	-	`sha256:0f394a57b1518b2c839507f279ded5d0b51d06449f052c39fc54535674c5dd15`  
		Last Modified: Wed, 16 Oct 2024 03:04:09 GMT  
		Size: 3.1 MB (3050013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d246e60a0667bd6755f67ee2042de27d8cf3c613de4244348120fa8739d0ce`  
		Last Modified: Wed, 16 Oct 2024 03:04:09 GMT  
		Size: 23.8 KB (23812 bytes)  
		MIME: application/vnd.in-toto+json
