## `tomcat:jre17`

```console
$ docker pull tomcat@sha256:99cfe9510a7f0579f4d666242b3a700de48540495a54be21ebc1c312c0291534
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

### `tomcat:jre17` - linux; amd64

```console
$ docker pull tomcat@sha256:0ed3286e24b878e16f8cdae40a62f8972734c1ca6df76bf93901b6f201a9b298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107515282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc50f4f71a2d68ecaa1c7415b87edc6de79ac8a90b85d59f7fe01fc2549851a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ARG RELEASE
# Wed, 23 Oct 2024 15:41:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Oct 2024 15:41:32 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 13 Jan 2025 19:02:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 13 Jan 2025 19:02:34 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Jan 2025 19:02:34 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
WORKDIR /usr/local/tomcat
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 13 Jan 2025 19:02:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_MAJOR=11
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_VERSION=11.0.2
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_SHA512=635d0b704d47a97050e3de995d372ef361ddb7589efbc53003afd6ac692d8db4a4125ae5dcc01af9e7371e8e598c98982e2a25617179b6ba0a04406299cca544
# Mon, 13 Jan 2025 19:02:34 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 13 Jan 2025 19:02:34 GMT
ENTRYPOINT []
# Mon, 13 Jan 2025 19:02:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8102a0b8aebb9e83cf9b49babb681033fba25f145e468519031ad5707f50183`  
		Last Modified: Tue, 03 Dec 2024 02:30:19 GMT  
		Size: 17.0 MB (16966381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e948b4564476a47332ef63d2b656fcb32b4f8aabfde1e9783e2991a957f2f314`  
		Last Modified: Tue, 03 Dec 2024 02:30:20 GMT  
		Size: 46.9 MB (46941841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584d1027889dd7e727c0c5421e5f0e2bcdf156cc2f260f28fe85c1d48018ed81`  
		Last Modified: Tue, 03 Dec 2024 02:30:18 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac37ec29a9a744ee416c3d313bafb8a47e50e62524ca8773b9515782f326873`  
		Last Modified: Tue, 03 Dec 2024 02:30:19 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab822307bbfde9b0670ce82282bc1ec20abd5627a2d2b591882a4b72df9caa8`  
		Last Modified: Tue, 14 Jan 2025 02:19:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c485bba4770898bfab5530a331a444904d8acc327892d2dfe0462bbe086f1e`  
		Last Modified: Tue, 14 Jan 2025 02:19:29 GMT  
		Size: 13.6 MB (13629018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55fbeb21a7d94a1fabb63e490a242e07497ae14c935a3411ec76810a7cf2d72`  
		Last Modified: Tue, 14 Jan 2025 02:19:29 GMT  
		Size: 223.4 KB (223428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:35bf96d5d1b13bdc7cf28608a8941eba3ba657eae1d73f73996cc218081b2f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3204626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04803f6253250dacef71e840c624ec0f52970390a0a02ae37e039b3c9a0bc4a2`

```dockerfile
```

-	Layers:
	-	`sha256:3a9456777b2fd38d665820e78d01ee29d62f4c198d82ff88752f2af81cfed0b8`  
		Last Modified: Tue, 14 Jan 2025 02:19:29 GMT  
		Size: 3.2 MB (3180548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acf52f206e1fd9f5450ee93c70e961d6daa41c53feeac88af8879147c0ed1a4b`  
		Last Modified: Tue, 14 Jan 2025 02:19:29 GMT  
		Size: 24.1 KB (24078 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:290d7d31ebd112f1a1d54473af2609c02a5a51825e2934353424255a5e7bf079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.5 MB (99533117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512fd042ee2c763b859bd0cc943165fcec25de561cbed7fcd7567ea5c1b91ffb`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:20 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:23 GMT
ADD file:e936767f044e9a1b6b2475ee575c7d052960fd234a0ce2b100a12bc3713dfe95 in / 
# Mon, 16 Sep 2024 06:23:23 GMT
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
# Tue, 17 Sep 2024 14:03:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Sep 2024 14:03:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Sep 2024 14:03:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Sep 2024 14:03:18 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Sep 2024 14:03:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Sep 2024 14:03:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Sep 2024 14:03:18 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Tue, 17 Sep 2024 14:03:18 GMT
ENV TOMCAT_MAJOR=10
# Tue, 17 Sep 2024 14:03:18 GMT
ENV TOMCAT_VERSION=10.1.30
# Tue, 17 Sep 2024 14:03:18 GMT
ENV TOMCAT_SHA512=9e5f46fdb984d9e48f2608d78352173b7e9b72c384ca0886a9384120d96d2c9302c26d2314e646152605e5e4b044f705feaaf13146b0e72dd535a9625c7746dd
# Tue, 17 Sep 2024 14:03:18 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Sep 2024 14:03:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Sep 2024 14:03:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Sep 2024 14:03:18 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Sep 2024 14:03:18 GMT
ENTRYPOINT []
# Tue, 17 Sep 2024 14:03:18 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:14a14d2fa7e19fd928b03aea8bd113a191e791e874e3d77bc5db711ed52c3073`  
		Last Modified: Wed, 02 Oct 2024 01:43:48 GMT  
		Size: 27.7 MB (27731844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5afde08068e6888b550cae3a7ffda1ff056862f0e466bdb789146e4038eea`  
		Last Modified: Wed, 02 Oct 2024 01:50:03 GMT  
		Size: 13.1 MB (13134649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d04aacc0a46606926847ea3cbc2ad828e91a589f0bb25aab5ab6998999b7d16`  
		Last Modified: Wed, 02 Oct 2024 01:53:01 GMT  
		Size: 44.9 MB (44944625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d258318e17c487bf628eb22e5db10f5b7e356ad8618c5ed71639999570933816`  
		Last Modified: Wed, 02 Oct 2024 01:52:53 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2a41967fbb1e1d8cb84af7fc7396eabbd5b8c4020a700ab34004ff5117b6ef`  
		Last Modified: Wed, 02 Oct 2024 01:52:53 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f324cebf996231241857441d15247a05b9b8af3d240b16a3ba606761f5f4e1`  
		Last Modified: Wed, 02 Oct 2024 05:34:40 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42e449c96edca74e1f4ed29a7eafdc35b1a88f35539e28e7f0c9a833719a5ee`  
		Last Modified: Wed, 02 Oct 2024 05:34:42 GMT  
		Size: 13.5 MB (13535987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a576a9912a5e85b60b6c95ca467ded71b21d7b08f1e5e40d3d1dac6c18bb06`  
		Last Modified: Wed, 02 Oct 2024 05:34:41 GMT  
		Size: 183.5 KB (183540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:c7fe8f42371bb247de72aa2ebb64d879104e3069c7b41579fca3dba601210baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3077854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b028146bdb4a2b0d0f7280865f899e1e3665587189b97413b361fca8f29d3f39`

```dockerfile
```

-	Layers:
	-	`sha256:79e8da54356cf58d1a4351a58e8f756625b0b87901aea5014ce5bab02a394bcd`  
		Last Modified: Wed, 02 Oct 2024 05:34:41 GMT  
		Size: 3.1 MB (3053065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07ca250020966e9310dafe32638b0252453ad6f9cfbd32fd0ee96777a76323b7`  
		Last Modified: Wed, 02 Oct 2024 05:34:40 GMT  
		Size: 24.8 KB (24789 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:e7bd49e187d56f6bdd798d285b2fc162eeae4807b75e0f72849c249318df423d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104275679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f0227a7aaf67856718bdc4496b3a965495655dbca9c9afae10cba19a230c73`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
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
# Tue, 17 Sep 2024 14:03:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Sep 2024 14:03:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Sep 2024 14:03:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Sep 2024 14:03:18 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Sep 2024 14:03:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Sep 2024 14:03:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Sep 2024 14:03:18 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Tue, 17 Sep 2024 14:03:18 GMT
ENV TOMCAT_MAJOR=10
# Tue, 17 Sep 2024 14:03:18 GMT
ENV TOMCAT_VERSION=10.1.30
# Tue, 17 Sep 2024 14:03:18 GMT
ENV TOMCAT_SHA512=9e5f46fdb984d9e48f2608d78352173b7e9b72c384ca0886a9384120d96d2c9302c26d2314e646152605e5e4b044f705feaaf13146b0e72dd535a9625c7746dd
# Tue, 17 Sep 2024 14:03:18 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Sep 2024 14:03:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Sep 2024 14:03:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Sep 2024 14:03:18 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Sep 2024 14:03:18 GMT
ENTRYPOINT []
# Tue, 17 Sep 2024 14:03:18 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:43cc87cb0cd1fc1c0b6c8670fa2a07f84e6af2cd95bce48b7909b42cca8e5fc1`  
		Last Modified: Fri, 20 Sep 2024 15:05:59 GMT  
		Size: 30.0 MB (29952705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705b8718ddb3ba1d94fa724eee408800a407ccd169899af243b9cfc2ab5481c`  
		Last Modified: Wed, 02 Oct 2024 01:25:17 GMT  
		Size: 13.8 MB (13798035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ef2dea2cc9c0dbe3c64710e5ffdcfb21a0f8380212beac56d44e94e1a2802c`  
		Last Modified: Wed, 02 Oct 2024 01:28:02 GMT  
		Size: 46.7 MB (46746360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97ec3778b444f1bb64b53a5f58cb73e31648e1389c755d55b65d2c634c1cd2f`  
		Last Modified: Wed, 02 Oct 2024 01:27:57 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f4ca8e8b83ad911aeec2a1f3687e6b549782de3f86048819e24bbc9604a9fd`  
		Last Modified: Wed, 02 Oct 2024 01:27:57 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a048a6e5e950d28537247e59cee0c1b682511903da99d5f3a1e2674d985a8651`  
		Last Modified: Wed, 02 Oct 2024 07:53:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8932b85657fadf113608c0502fcd3e01c99f6ece48e724848eb09f7416b80248`  
		Last Modified: Wed, 02 Oct 2024 07:53:52 GMT  
		Size: 13.6 MB (13563893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e65181976bdda52f19be872b314137b9678e5052bf0b5d7838184f5cefa3bba`  
		Last Modified: Wed, 02 Oct 2024 07:53:52 GMT  
		Size: 212.2 KB (212214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:e0a36e121546411dd9c38ebcd8f48b98146e792978a35461c2c9bd57f92c843b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3076094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5551e8efe33ecdcbf31699348df645c4af4af8704405ad17ef3f8c8444f6180c`

```dockerfile
```

-	Layers:
	-	`sha256:58f55914db1b0df6abc932e3f7fa8d568c07fa097b1dd123f28d9837bb6eb1e6`  
		Last Modified: Wed, 02 Oct 2024 07:53:52 GMT  
		Size: 3.1 MB (3051237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e652af0ddf45793ef89fcfaac9bc916e3d1f17b2cd4a6cce4b1425fd611e4469`  
		Last Modified: Wed, 02 Oct 2024 07:53:51 GMT  
		Size: 24.9 KB (24857 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17` - linux; ppc64le

```console
$ docker pull tomcat@sha256:1e431efaff2dfc76c68763189cdc966600fa5b0691935d93540fc83be058394b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111372602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8218647eb324eface5869705dd4fa9f7c0fdd8567a9d542f14cac8aa5adf809`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 16 Sep 2024 06:25:02 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:25:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:25:05 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Mon, 16 Sep 2024 06:25:05 GMT
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
# Tue, 17 Sep 2024 14:03:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Sep 2024 14:03:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Sep 2024 14:03:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Sep 2024 14:03:18 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Sep 2024 14:03:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Sep 2024 14:03:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Sep 2024 14:03:18 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Tue, 17 Sep 2024 14:03:18 GMT
ENV TOMCAT_MAJOR=10
# Tue, 17 Sep 2024 14:03:18 GMT
ENV TOMCAT_VERSION=10.1.30
# Tue, 17 Sep 2024 14:03:18 GMT
ENV TOMCAT_SHA512=9e5f46fdb984d9e48f2608d78352173b7e9b72c384ca0886a9384120d96d2c9302c26d2314e646152605e5e4b044f705feaaf13146b0e72dd535a9625c7746dd
# Tue, 17 Sep 2024 14:03:18 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Sep 2024 14:03:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Sep 2024 14:03:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Sep 2024 14:03:18 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Sep 2024 14:03:18 GMT
ENTRYPOINT []
# Tue, 17 Sep 2024 14:03:18 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d3b933ab36d7d3de2d3d18b1141e06a388bb6b545afd828222778b868adbc114`  
		Last Modified: Wed, 02 Oct 2024 01:55:43 GMT  
		Size: 35.5 MB (35517922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8142fb4132be3efdcf8ea435bb4f9c7886f7dd7050b7ff796718a886a738003`  
		Last Modified: Wed, 02 Oct 2024 02:05:51 GMT  
		Size: 14.9 MB (14913665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d5247616b4f0fc80abbd7e66348a0a0253768c45003f5a96c6b420f1efedf0`  
		Last Modified: Wed, 02 Oct 2024 02:09:10 GMT  
		Size: 47.1 MB (47115926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf20b52a14238b175f5496a2e7cc60362f45a1aec129264f53db239340b4b506`  
		Last Modified: Wed, 02 Oct 2024 02:09:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e15b6f8de343b8659db095e0c611681df28b6f59a2af240be6695f101078794`  
		Last Modified: Wed, 02 Oct 2024 02:09:03 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7f4be5be97cd9a485fb8150c5419f9d2f48bddf53017333cc1d106155e1588`  
		Last Modified: Wed, 02 Oct 2024 08:18:05 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0929530aaadb09563a59262183a2e783ed834bc96e634ddd69352fa3a9458cf8`  
		Last Modified: Wed, 02 Oct 2024 08:18:07 GMT  
		Size: 13.6 MB (13579175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecdcc9c798e5936081a304a2812a5c8ee16d78dfc4aef231fafea07fa6479fe`  
		Last Modified: Wed, 02 Oct 2024 08:18:06 GMT  
		Size: 243.4 KB (243441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:517ad664110bbe418b17fcca4eb8843dbd545e374b66708df74d64650e4f456e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3079334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6605b400b428ee458bc6ff6a501210a8d6ad7549b8593a806904cf0cb3db5b1e`

```dockerfile
```

-	Layers:
	-	`sha256:663ce3612c47085bdc5dfeff6768af53804f63957d46c4c7d6b40c43977bce1c`  
		Last Modified: Wed, 02 Oct 2024 08:18:05 GMT  
		Size: 3.1 MB (3054627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d176510f6da69e4ced8b87bb0310da03622e05c7c0ef1f9a4a20538c07c2d213`  
		Last Modified: Wed, 02 Oct 2024 08:18:05 GMT  
		Size: 24.7 KB (24707 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17` - linux; s390x

```console
$ docker pull tomcat@sha256:3c2b2b24083355a807254dd9de78096f407a1bf29682a19381ef7987130b3e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105450840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d021ef0f4d480c2c64fd3476803e6b3a0ed6aad52d3296569b2a6a340123e341`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ARG RELEASE
# Wed, 23 Oct 2024 15:41:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Oct 2024 15:41:32 GMT
ADD file:1c391e128b3c5e552a1401f9520290446bf94ba089c2d74a5d661001d3d8b60c in / 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 13 Jan 2025 19:02:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 13 Jan 2025 19:02:34 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Jan 2025 19:02:34 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
WORKDIR /usr/local/tomcat
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 13 Jan 2025 19:02:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_MAJOR=11
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_VERSION=11.0.2
# Mon, 13 Jan 2025 19:02:34 GMT
ENV TOMCAT_SHA512=635d0b704d47a97050e3de995d372ef361ddb7589efbc53003afd6ac692d8db4a4125ae5dcc01af9e7371e8e598c98982e2a25617179b6ba0a04406299cca544
# Mon, 13 Jan 2025 19:02:34 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 13 Jan 2025 19:02:34 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 13 Jan 2025 19:02:34 GMT
ENTRYPOINT []
# Mon, 13 Jan 2025 19:02:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:755503a8fb36d6a0d08275c3792ab81b69fdff95054dff0aa932d6dc30107609`  
		Last Modified: Tue, 19 Nov 2024 17:38:58 GMT  
		Size: 30.0 MB (30020826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4797233a5c5384584920c35814bc8b38ea24dccbedde0a0e68b3fb1a30877a17`  
		Last Modified: Tue, 03 Dec 2024 04:16:13 GMT  
		Size: 17.6 MB (17613148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f49ac462dc7df24c27528f6dbc7e7a49aacfd9321fb6ab19e8b559ca5276243`  
		Last Modified: Tue, 03 Dec 2024 04:18:43 GMT  
		Size: 43.9 MB (43943329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc68cdf062c4ef192ce7bc29659fcb607e1ce2dfc8407f7644a12cd0637e9ca1`  
		Last Modified: Tue, 03 Dec 2024 04:18:42 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd40b7424c2750e273da54bf82dbd4fc14eba1e75eec5fb97a54b18337a20b4`  
		Last Modified: Tue, 03 Dec 2024 04:18:42 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5489ef5fac09a50fb836cb6a05697baee54030aed73438232cb65e8d0dedb20a`  
		Last Modified: Tue, 14 Jan 2025 08:11:35 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855278382ef1c9bcf95f57ce1af0d61a415511246513565c49b98ebe08a73dbc`  
		Last Modified: Tue, 14 Jan 2025 08:11:36 GMT  
		Size: 13.6 MB (13639399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6352ba81ba4a9545d4d03bb0b5e539268b479cc0680f9b2df5dbfc4b2c27c672`  
		Last Modified: Tue, 14 Jan 2025 08:11:35 GMT  
		Size: 231.5 KB (231493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:2da141e2f8deadedd9f80468bc0b8933e273cf81abdb3c70ef1a373b44fca792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3206825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c7ac3bfbe25d477d998883bb0a628e2be2758bf374e2cfef694621dab519ce`

```dockerfile
```

-	Layers:
	-	`sha256:1e2029965982f2d225520904e521c347e525a16f53a63531e6071be74d6b8c6a`  
		Last Modified: Tue, 14 Jan 2025 08:11:35 GMT  
		Size: 3.2 MB (3182747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac01b7ad67dede9666b6ddb1f2af4ccecb5c82b76ea38eb143f6a9dc160a9182`  
		Last Modified: Tue, 14 Jan 2025 08:11:35 GMT  
		Size: 24.1 KB (24078 bytes)  
		MIME: application/vnd.in-toto+json
