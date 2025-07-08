## `tomcat:9-jre11-temurin-noble`

```console
$ docker pull tomcat@sha256:a5c6621fdf7d94803a1245f3df4d432ca99cd8d3dd63f15370357ff3859c4bfd
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

### `tomcat:9-jre11-temurin-noble` - linux; amd64

```console
$ docker pull tomcat@sha256:80627a6f1f918bc0bb4521133230227b3b64ebd713403aa879580c3e3bd3d482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109317425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f0051cea9d750c4bd1afa902fe3b0c95cf3944d4b635af8ce2ef7873baf245`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 04 Jul 2025 20:22:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Jul 2025 20:22:51 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 20:22:51 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 04 Jul 2025 20:22:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Jul 2025 20:22:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:22:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:22:51 GMT
ENV TOMCAT_MAJOR=9
# Fri, 04 Jul 2025 20:22:51 GMT
ENV TOMCAT_VERSION=9.0.107
# Fri, 04 Jul 2025 20:22:51 GMT
ENV TOMCAT_SHA512=1815837fa10083258b653dab1f3947fadbad377fa66546fa74aecea1439c6fed2ef4e40c86fa55e176d8c5739ad448196a7415ddfca6ff8d17c6fe8cdba0fefb
# Fri, 04 Jul 2025 20:22:51 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 04 Jul 2025 20:22:51 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Jul 2025 20:22:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 04 Jul 2025 20:22:51 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Jul 2025 20:22:51 GMT
ENTRYPOINT []
# Fri, 04 Jul 2025 20:22:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f2d144ace1993f175aaee9af1a08397bf41dfda9437311bb6a140d01ce7005`  
		Last Modified: Wed, 02 Jul 2025 03:10:17 GMT  
		Size: 17.0 MB (16969531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617aa07d699ea21ec5f12396f4b549439ec4397f843659c6ba406bdd5c69a1a2`  
		Last Modified: Wed, 02 Jul 2025 03:10:20 GMT  
		Size: 47.2 MB (47222162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf7468b1480a6470e6dc4d0e58366a1f11a8366fdf075b4e6bd097b593011f2`  
		Last Modified: Wed, 02 Jul 2025 03:10:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a882f602ac5b71ffd2d1bc195a6981eb67b785eb73156070f3f526a098688c`  
		Last Modified: Wed, 02 Jul 2025 03:10:16 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fba469f8eada461627123eff43c2c7c5287e0075b490ec1e4a7c7af51e02bb9`  
		Last Modified: Mon, 07 Jul 2025 21:05:23 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9283ed22d8468f7778b65590909713cddfb0cda9e6e664d4483f050534ed694`  
		Last Modified: Mon, 07 Jul 2025 21:05:24 GMT  
		Size: 13.7 MB (13694380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a1b2af949ae83c5f28529c94088083bd6e98d46e55951ec47b7db71ac4bcc5`  
		Last Modified: Mon, 07 Jul 2025 21:05:24 GMT  
		Size: 1.7 MB (1710344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:251662d916f1caa63c5510cc164b99882234e17a0018f2c75728986e888852a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3380710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472ca0452507dc9fcb5ca1d92e0726a33561b07ee30f60decab2a29b9b26d567`

```dockerfile
```

-	Layers:
	-	`sha256:877daae38f56d3d7f08e8f4c95fb402cf9f4f43e0b01e436e36d125479a2612f`  
		Last Modified: Mon, 07 Jul 2025 23:35:31 GMT  
		Size: 3.4 MB (3357572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee4f9d791d8bf035d4747a343b41e5728689f49e187803b660ef20e2bbfb7eeb`  
		Last Modified: Mon, 07 Jul 2025 23:35:31 GMT  
		Size: 23.1 KB (23138 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-noble` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:85cc6b36073660dfdc533d581da837f2dc58cb5a90760c4b6e04b872e1b49187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104613472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e08c2fde2fde6458ea8d6030ac9cdc8462d7c67e20c477da97a061ec05118d8`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:88b7ca184cec1707b10b6b543ddfa7abfcacc2605cdd5919877294ff5290aa3e in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 04 Jul 2025 20:22:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Jul 2025 20:22:51 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 20:22:51 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 04 Jul 2025 20:22:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Jul 2025 20:22:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:22:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:22:51 GMT
ENV TOMCAT_MAJOR=9
# Fri, 04 Jul 2025 20:22:51 GMT
ENV TOMCAT_VERSION=9.0.107
# Fri, 04 Jul 2025 20:22:51 GMT
ENV TOMCAT_SHA512=1815837fa10083258b653dab1f3947fadbad377fa66546fa74aecea1439c6fed2ef4e40c86fa55e176d8c5739ad448196a7415ddfca6ff8d17c6fe8cdba0fefb
# Fri, 04 Jul 2025 20:22:51 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 04 Jul 2025 20:22:51 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Jul 2025 20:22:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 04 Jul 2025 20:22:51 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Jul 2025 20:22:51 GMT
ENTRYPOINT []
# Fri, 04 Jul 2025 20:22:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:149362fdfa6e6a5d9f009b896da3be3172c395ba2287b57d4969f3f46e573055`  
		Last Modified: Fri, 20 Jun 2025 10:02:42 GMT  
		Size: 26.8 MB (26844462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87008fd131e34e3e3f4ffd352cf8db54b0e89603b6dc942d3c4f194b46bdfc32`  
		Last Modified: Wed, 02 Jul 2025 10:26:30 GMT  
		Size: 16.3 MB (16304975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fa52457cd802af6d0960b58bf981f237513d5651251e830594ef14513a80b`  
		Last Modified: Wed, 02 Jul 2025 10:30:00 GMT  
		Size: 45.3 MB (45336814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0426c07733eba6cc8ab9606feb907634304b48bafc85c983649604e9fa90ff0a`  
		Last Modified: Wed, 02 Jul 2025 10:29:58 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1564add0049589b384b57a0de987ea1ac1f19b5f7bb4deadac0434bf8fa5b1`  
		Last Modified: Wed, 02 Jul 2025 10:29:58 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0392244edc1afcbfb53f43c134261d856da8fca002bb9156ef66ec0122c36b8`  
		Last Modified: Wed, 02 Jul 2025 12:30:14 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9872a2b0f032074e53e822b44b0db8689e500d67e2744bffced61f52a41ad23`  
		Last Modified: Tue, 08 Jul 2025 03:58:29 GMT  
		Size: 13.6 MB (13630747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2e8e02137ad48367ec46432e59ff05a3e1e58527541addc14d2aba0e2d4f52`  
		Last Modified: Tue, 08 Jul 2025 03:58:28 GMT  
		Size: 2.5 MB (2493832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:bff7587cd86f141f61b3a96a55e72d7c5174346cf346ceb2e2cee9b98b4a45a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3384517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7bd78c97c150f5951a97b07b8985fb7755b70cbe3f8842344a088355bb6d50f`

```dockerfile
```

-	Layers:
	-	`sha256:1ed305212fc798755904eadea5dd60d80258b24ac775a5a2231510958f4492d7`  
		Last Modified: Tue, 08 Jul 2025 05:35:17 GMT  
		Size: 3.4 MB (3361215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:602f1bdb2b6aa289b6e73154044abf76030f69311e4f3423eae353cb04ba3641`  
		Last Modified: Tue, 08 Jul 2025 05:35:18 GMT  
		Size: 23.3 KB (23302 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-noble` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:b9963897fa6434d33b0c93d776b0d5fb22b67bbf6e6fc8ec2ddf2dc3d4b94f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106926822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fdd4fba3ccace5d40238efe8ad13016091091b656168b7f8d1fb08eb395da22`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 04 Jul 2025 20:22:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Jul 2025 20:22:51 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 20:22:51 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 04 Jul 2025 20:22:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Jul 2025 20:22:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:22:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:22:51 GMT
ENV TOMCAT_MAJOR=9
# Fri, 04 Jul 2025 20:22:51 GMT
ENV TOMCAT_VERSION=9.0.107
# Fri, 04 Jul 2025 20:22:51 GMT
ENV TOMCAT_SHA512=1815837fa10083258b653dab1f3947fadbad377fa66546fa74aecea1439c6fed2ef4e40c86fa55e176d8c5739ad448196a7415ddfca6ff8d17c6fe8cdba0fefb
# Fri, 04 Jul 2025 20:22:51 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 04 Jul 2025 20:22:51 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Jul 2025 20:22:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 04 Jul 2025 20:22:51 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Jul 2025 20:22:51 GMT
ENTRYPOINT []
# Fri, 04 Jul 2025 20:22:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2fa422bbd08bc40d85a4e1666805f0d0f323a1834f9494578f07cf2106f303`  
		Last Modified: Wed, 02 Jul 2025 05:07:14 GMT  
		Size: 17.0 MB (16988217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edcfc733e285d5961a55d35f4c39822237fc8aa02116de423cbfcba2cecac5a`  
		Last Modified: Wed, 02 Jul 2025 05:09:48 GMT  
		Size: 45.6 MB (45585144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3f660104562a87f4d60ec0207bfa44fb4a5925deb0ecf59e20cfed461c41d8`  
		Last Modified: Wed, 02 Jul 2025 05:09:44 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae25893049c054fae8b6bd05d6a0265cb127d4c150959b654777842ca1abd5b`  
		Last Modified: Wed, 02 Jul 2025 05:09:44 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0d68f9a932cf3920f597d0f26a95f4a4442bd30399e98eb43ad517f21af6d5`  
		Last Modified: Wed, 02 Jul 2025 14:36:46 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124646c8807564f518aab5113886f43b720c89bf2ea15460be5afeda72bf4f5c`  
		Last Modified: Tue, 08 Jul 2025 05:26:24 GMT  
		Size: 13.7 MB (13704939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c71203550e858c4a5245cbf602b71a30e9971045af13e55e914ed2568e17303`  
		Last Modified: Tue, 08 Jul 2025 05:26:23 GMT  
		Size: 1.8 MB (1789860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:fe6468946c6356f35a5bd3ab3fbc830621a925a0c1e6b1931a8d5c49fc3a10ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3382079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf12aa53482ee3e4fa2a2ebfe230d2695628498add491b6dd3693bb12d46946`

```dockerfile
```

-	Layers:
	-	`sha256:1ff2704d5ad3a3ac6db69c3399df2838eaa0adada782aae5940459b5b7764f45`  
		Last Modified: Tue, 08 Jul 2025 08:32:54 GMT  
		Size: 3.4 MB (3358722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ad6a7708a1d9dff2c81b1dc2de91eb936b498d310db72a2277bde684e0ce13f`  
		Last Modified: Tue, 08 Jul 2025 08:32:55 GMT  
		Size: 23.4 KB (23357 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-noble` - linux; ppc64le

```console
$ docker pull tomcat@sha256:ad854c6435e34352348575471d4bd0ad910240164c9b6a73586963104b0b1dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111596554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2457d041d7cac84b383a04d2d33a7886a3e1232109477766b3eff07b35b40d4`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:fca9cbe6eff6a6982a26900c08b4e2c5a46057e9e5386288e826ac4f2cb17b32 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 04 Jul 2025 20:22:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Jul 2025 20:22:51 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 20:22:51 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 04 Jul 2025 20:22:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Jul 2025 20:22:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:22:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:22:51 GMT
ENV TOMCAT_MAJOR=9
# Fri, 04 Jul 2025 20:22:51 GMT
ENV TOMCAT_VERSION=9.0.107
# Fri, 04 Jul 2025 20:22:51 GMT
ENV TOMCAT_SHA512=1815837fa10083258b653dab1f3947fadbad377fa66546fa74aecea1439c6fed2ef4e40c86fa55e176d8c5739ad448196a7415ddfca6ff8d17c6fe8cdba0fefb
# Fri, 04 Jul 2025 20:22:51 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 04 Jul 2025 20:22:51 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Jul 2025 20:22:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 04 Jul 2025 20:22:51 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Jul 2025 20:22:51 GMT
ENTRYPOINT []
# Fri, 04 Jul 2025 20:22:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:384c99c6e2b4660fd65fc9823f13a263fb87d4aec3b8f2bd813a7a255bcf46f3`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 34.3 MB (34321506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0111803c0bfac8b5cf9f7f497b1d1327406384bede031585f6063cf0af7d1a63`  
		Last Modified: Wed, 02 Jul 2025 03:16:25 GMT  
		Size: 18.8 MB (18817031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9cfa1b17f6e606e4167b37b6bbd538996a10b0e19bb9a37a6cf5115beb36ed`  
		Last Modified: Wed, 02 Jul 2025 03:20:39 GMT  
		Size: 42.7 MB (42677151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3ae8036d826d1d43f7248a121c1432015c5a696671348307114fb3af258413`  
		Last Modified: Wed, 02 Jul 2025 03:20:36 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f0243841a87340b25d50c15f44559440c91e2dc8555aaf82f585e5fdb0fbfa`  
		Last Modified: Wed, 02 Jul 2025 03:20:36 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03128a1ea07d0eda60f7512590cec783a1ad1be49140568edba5b3b5af990bb`  
		Last Modified: Wed, 02 Jul 2025 14:58:27 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110ea082a22bedc9040d667ebc9de67fde87a42641867fb3844379100ca5c211`  
		Last Modified: Tue, 08 Jul 2025 00:23:34 GMT  
		Size: 13.7 MB (13729013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2742846864d189a3a52afbf066ca7e60dc6b99fffe373283e58172849954db3a`  
		Last Modified: Tue, 08 Jul 2025 00:23:33 GMT  
		Size: 2.0 MB (2049210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:79aa86155b33ed53c4a43f3486e198c27fd25cf6608f7f550816552c72218092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3384911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4cad8ce5a6f81fe2b107a155cc4a4773ab70194a97a92597e63fe6baec11c2c`

```dockerfile
```

-	Layers:
	-	`sha256:e42cef4fd9d8f531a06b8e9385b5b4b4d9be0a069b6f2863aefe77895b46a5da`  
		Last Modified: Tue, 08 Jul 2025 02:32:15 GMT  
		Size: 3.4 MB (3361685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f05716256eafafabf64f630ab6e4f9d74dbd5ea4084976e398941d836b4a63c`  
		Last Modified: Tue, 08 Jul 2025 02:32:16 GMT  
		Size: 23.2 KB (23226 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-noble` - linux; s390x

```console
$ docker pull tomcat@sha256:1aa8cddbcfa5b18b97eaa8b594dbb863bbead277c454d7ab8a2435caefa96894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103779469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1212bbeef60181011d481238037d2e8d68641862b5ca5fe42df41eca0a714d12`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:80b0b0c2a08a762cf6a520d8428a5c769c29e72f4a51630adb2231f2816c50c4 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d854baf8fcf835e28142d1519b88a1367c117e01fa1c18e34f9a1435d02a0437';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='e486056040ea7878a6e676bf8fd9112128045b3c1e5230b5dcf73756fc63f7e5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='4cdccdb7da9590635bc9ef60c5c1d3b6c74dd7df2b8c2d265957c54cc6afa274';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='4f8d67bd58137bac307cd6a07f4454ca92dc21632505e9bd8e41652a741d10e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='b6770a1536d43510b42de8a5f4d1f8bfab098b46a99016c70bf8241ede773eb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jre_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 04 Jul 2025 20:22:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Jul 2025 20:22:51 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 20:22:51 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 04 Jul 2025 20:22:51 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Jul 2025 20:22:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:22:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:22:51 GMT
ENV TOMCAT_MAJOR=9
# Fri, 04 Jul 2025 20:22:51 GMT
ENV TOMCAT_VERSION=9.0.107
# Fri, 04 Jul 2025 20:22:51 GMT
ENV TOMCAT_SHA512=1815837fa10083258b653dab1f3947fadbad377fa66546fa74aecea1439c6fed2ef4e40c86fa55e176d8c5739ad448196a7415ddfca6ff8d17c6fe8cdba0fefb
# Fri, 04 Jul 2025 20:22:51 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 04 Jul 2025 20:22:51 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Jul 2025 20:22:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 04 Jul 2025 20:22:51 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Jul 2025 20:22:51 GMT
ENTRYPOINT []
# Fri, 04 Jul 2025 20:22:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:30d64ca13d9d94eb48bf3fece3e38a4e60931d72f1a8c633dec981e43a0515a4`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 29.9 MB (29925630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376d0f4302e30b01c4235de8a3d72897ca97f7a056bf7655f826977caaf40fa8`  
		Last Modified: Wed, 02 Jul 2025 04:17:12 GMT  
		Size: 17.6 MB (17582256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c6629089bf5c630b95295789de7feff5cfe6f2fc3b42074aa14a0258304f62`  
		Last Modified: Wed, 02 Jul 2025 04:17:45 GMT  
		Size: 40.8 MB (40839858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a7015eab858d65ba4eec48de336e6553f59a94d35b730683c1df686aa66804`  
		Last Modified: Wed, 02 Jul 2025 04:17:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932cfa64fbf7e1c415556fc7a692cac1716267c5887d8dd177bc254684080743`  
		Last Modified: Wed, 02 Jul 2025 04:17:41 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785baa6a189e77dd95a9cb4d66e95851e99cd289809e9a6fed18e7e46bdc87cb`  
		Last Modified: Wed, 02 Jul 2025 07:47:57 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8acbb88bb51576d937923eed126ee4558f6c66c04fc598f015a1362ce16d374`  
		Last Modified: Tue, 08 Jul 2025 05:30:09 GMT  
		Size: 13.7 MB (13704916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f8267ff76266e12fc5ea20326de536f39a603eeaf67efdfce21e7e79f5c39b`  
		Last Modified: Tue, 08 Jul 2025 05:30:08 GMT  
		Size: 1.7 MB (1724166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:3e93eff17b5399b3df404429959d411241a4fc3cb1a1926b1845571b822fc4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3382915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd25c6b79cd9920f53fb090a95ddc5ce0bdadbb3c77568cdc58717f3a3caf364`

```dockerfile
```

-	Layers:
	-	`sha256:2338298728a8b4e2e8419b50bcb6d860a06471255514f63709ba6e9c09c05cba`  
		Last Modified: Tue, 08 Jul 2025 08:33:02 GMT  
		Size: 3.4 MB (3359777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59820b19843d11b2ab9ccfcb1fab4466ca35448b491ecf67d7978f33bdbc5f60`  
		Last Modified: Tue, 08 Jul 2025 08:33:02 GMT  
		Size: 23.1 KB (23138 bytes)  
		MIME: application/vnd.in-toto+json
