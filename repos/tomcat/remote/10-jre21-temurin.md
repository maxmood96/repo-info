## `tomcat:10-jre21-temurin`

```console
$ docker pull tomcat@sha256:5c3ac127c619485e6b1d851bb22d5fa5312c5e1bbb4ee9751a615f711555e59b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `tomcat:10-jre21-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:0eac83d5462af9ded0c8473961b012a7038a453f95938de0b7e735854d5684e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126255806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f95eaf39425c5f2b1ed9507b84596f84f5547a9e653ed6961032cdae0c4911f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        riscv64)          ESUM='a8d219a4a97f9c53ba88cb8927910005d4f3d08a87ab1bdebff921ef41afa93d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 18 Feb 2025 15:03:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 18 Feb 2025 15:03:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 15:03:21 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 18 Feb 2025 15:03:21 GMT
WORKDIR /usr/local/tomcat
# Tue, 18 Feb 2025 15:03:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 15:03:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 15:03:21 GMT
ENV TOMCAT_MAJOR=10
# Tue, 18 Feb 2025 15:03:21 GMT
ENV TOMCAT_VERSION=10.1.36
# Tue, 18 Feb 2025 15:03:21 GMT
ENV TOMCAT_SHA512=972a406263fd540b135efae4b375543781b26104acb07114c3e535fe31e5b0a5c87ae6dff055e0e47877a3861070c264bb236686cf08bc08d98b7541e5d743c7
# Tue, 18 Feb 2025 15:03:21 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 18 Feb 2025 15:03:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 15:03:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 18 Feb 2025 15:03:21 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Feb 2025 15:03:21 GMT
ENTRYPOINT []
# Tue, 18 Feb 2025 15:03:21 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 03 Feb 2025 23:00:26 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab21fde7f674e1262f9a291fb3b148dce3986b16a6afe2b1077240af4411e8d`  
		Last Modified: Tue, 04 Feb 2025 07:16:41 GMT  
		Size: 17.0 MB (16962453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e1027cc04acbd0bbe96f77c4b07270e74687784095964c3f8e1145ed4062a0`  
		Last Modified: Tue, 04 Feb 2025 07:28:42 GMT  
		Size: 52.9 MB (52876121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb109d1b0266a0c777373e83c16fd3b583414425ea70ad73adbf43bf4b8a569e`  
		Last Modified: Tue, 04 Feb 2025 07:20:28 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f09a34126553bccc37644f98b45096297b0127f040e8492684976c77ec2b14a`  
		Last Modified: Tue, 04 Feb 2025 07:24:01 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1efd4859c501c0525fd38880aa57ac87cac7e6f7ebdcb6dc2c4e028a2ea15f0`  
		Last Modified: Wed, 19 Feb 2025 01:08:21 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570accbe11b3844c084b0e31bd7ca3d0ac6ca5dd4608ead3235bcb6dde387ef6`  
		Last Modified: Wed, 19 Feb 2025 01:08:36 GMT  
		Size: 13.8 MB (13827819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bbe363f0c5d9d54f6a8b9b0d3e4712b067cbed622305e031f2b82388fe9e3b`  
		Last Modified: Wed, 19 Feb 2025 01:08:36 GMT  
		Size: 12.8 MB (12832480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:05c1563eeea3c257d6cedd60ce9df9d4ec0ad87d20674fc87e01e8a6067d41e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3206738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab43d36203069c63acbea39c5751120223361f7b4229921eeb42fdca75e2d32`

```dockerfile
```

-	Layers:
	-	`sha256:b8006379ebb6c39c3c75552f4c9d3e57217590bc71204bfd37d6dd8742a8afeb`  
		Last Modified: Wed, 19 Feb 2025 03:31:37 GMT  
		Size: 3.2 MB (3183585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:642963f8cd789d34fe9e1e5483668bcd9e5e8ccd7ba5b9884ac06e45aea43c60`  
		Last Modified: Wed, 19 Feb 2025 03:31:38 GMT  
		Size: 23.2 KB (23153 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre21-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:3955be6233b09752e9aa255ce993465fd0d6201eb41cb3d8b94deb9dcb9b15c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124364227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e88ff4b136c58c02da15fa90960e0fe2732164ec3ea29cc88bdc878a25d5a3b2`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        riscv64)          ESUM='a8d219a4a97f9c53ba88cb8927910005d4f3d08a87ab1bdebff921ef41afa93d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 18 Feb 2025 15:03:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 18 Feb 2025 15:03:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 15:03:21 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 18 Feb 2025 15:03:21 GMT
WORKDIR /usr/local/tomcat
# Tue, 18 Feb 2025 15:03:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 15:03:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 15:03:21 GMT
ENV TOMCAT_MAJOR=10
# Tue, 18 Feb 2025 15:03:21 GMT
ENV TOMCAT_VERSION=10.1.36
# Tue, 18 Feb 2025 15:03:21 GMT
ENV TOMCAT_SHA512=972a406263fd540b135efae4b375543781b26104acb07114c3e535fe31e5b0a5c87ae6dff055e0e47877a3861070c264bb236686cf08bc08d98b7541e5d743c7
# Tue, 18 Feb 2025 15:03:21 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 18 Feb 2025 15:03:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 15:03:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 18 Feb 2025 15:03:21 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Feb 2025 15:03:21 GMT
ENTRYPOINT []
# Tue, 18 Feb 2025 15:03:21 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Tue, 04 Feb 2025 06:04:53 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 10:15:57 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cbfadccc4ef79b758e18dd8d1708943e6c36b0c9c7e7b94a5d7ff99d3d28af`  
		Last Modified: Tue, 04 Feb 2025 14:22:53 GMT  
		Size: 52.1 MB (52058738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8426c44160873d09bb23bdec752f80f9f6f3a7b054d0cd8a334eeb2c92fa0ed9`  
		Last Modified: Tue, 04 Feb 2025 10:53:38 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3daf2a897e045b94b8cf1d4c94f9dc6f09163273fbbf52afcd8dc60a445788`  
		Last Modified: Tue, 04 Feb 2025 13:37:13 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212ee034a146c65a6d1fdfbfcc76a4dea8b9a3fc21563811d2cd9443e32f75a3`  
		Last Modified: Wed, 05 Feb 2025 06:42:03 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1350baf9745865144f00955defd89c5a56e9afda9c5d3740bda587e558aa12f`  
		Last Modified: Wed, 19 Feb 2025 02:12:52 GMT  
		Size: 13.8 MB (13830359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6173ab83da82bd8ec3b730076e3e9e077c733dbc7b21fa9e349b8c83696958`  
		Last Modified: Wed, 19 Feb 2025 02:13:02 GMT  
		Size: 12.6 MB (12601485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:c39ff9695b4eab63b37fd61db1420e19cdfe87ee779cd7d44ceeae0b40102769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3207490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7d568a884032bb6f482686fa7411313a4f86b2ad124fe9eaff18da506d927e`

```dockerfile
```

-	Layers:
	-	`sha256:ace78f1e8d0e4d2630d2b15cf47cfa065de4b1c87ade20696f58a7911a90958f`  
		Last Modified: Wed, 19 Feb 2025 03:31:40 GMT  
		Size: 3.2 MB (3184117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec14a922c9ae1fa7168a2a30367907398ea95e032395ee25fcd7dc69ef500952`  
		Last Modified: Wed, 19 Feb 2025 03:31:40 GMT  
		Size: 23.4 KB (23373 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre21-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:958c7726b98cc5a35511f6846bf633227605eb4d6f4c240a5e556a48e352f070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133609099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f7eb97fb835b9a973273672860fb0aaa57b2dd165d26bc9d5e174643fb4402`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        riscv64)          ESUM='a8d219a4a97f9c53ba88cb8927910005d4f3d08a87ab1bdebff921ef41afa93d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 18 Feb 2025 15:03:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 18 Feb 2025 15:03:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 15:03:21 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 18 Feb 2025 15:03:21 GMT
WORKDIR /usr/local/tomcat
# Tue, 18 Feb 2025 15:03:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 15:03:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 15:03:21 GMT
ENV TOMCAT_MAJOR=10
# Tue, 18 Feb 2025 15:03:21 GMT
ENV TOMCAT_VERSION=10.1.36
# Tue, 18 Feb 2025 15:03:21 GMT
ENV TOMCAT_SHA512=972a406263fd540b135efae4b375543781b26104acb07114c3e535fe31e5b0a5c87ae6dff055e0e47877a3861070c264bb236686cf08bc08d98b7541e5d743c7
# Tue, 18 Feb 2025 15:03:21 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 18 Feb 2025 15:03:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 15:03:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 18 Feb 2025 15:03:21 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Feb 2025 15:03:21 GMT
ENTRYPOINT []
# Tue, 18 Feb 2025 15:03:21 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Tue, 04 Feb 2025 07:01:00 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c7b03d73f24fbf1ca191efda6fafe2355b68e6e070a54b70fec6dc3ac0c66e`  
		Last Modified: Tue, 04 Feb 2025 16:27:35 GMT  
		Size: 18.8 MB (18824340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d1493865fdf1e9a5582b5d1e4793eaed2e1b396db970c207a985911580f17b`  
		Last Modified: Tue, 04 Feb 2025 17:42:07 GMT  
		Size: 52.9 MB (52914997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefab98df9d7152b9f429edd18ec9006b680fc56e4768ccf49d0ea45c2e0c59d`  
		Last Modified: Tue, 04 Feb 2025 20:44:02 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3a35c2113b4662df012f10c9fb629d06ada579e3c0232186401cdb95dbad1e`  
		Last Modified: Tue, 04 Feb 2025 11:41:55 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ae6f2f658f7a279bca2813a3d0181a85a887d6cf9f0723ef4cc9d5b47f7b49`  
		Last Modified: Wed, 05 Feb 2025 12:50:23 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854822abc2ce45ed1a502e943a1935a993b9b80e47451958e39b76209d531c94`  
		Last Modified: Wed, 19 Feb 2025 02:25:30 GMT  
		Size: 13.8 MB (13843207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0abc88b976b1bd2d188938ada3bb1f65d6f234e79672802737253c8db49aead`  
		Last Modified: Wed, 19 Feb 2025 02:25:30 GMT  
		Size: 13.6 MB (13634087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:5ad42042e43c52918cf3c8e615e5fec99714c66afd35b10c81942a4f2886da1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3210789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05b276c3fbd96d3d93d99ca3e866e1b09b089ee8cf20358087b9ffe5d144835`

```dockerfile
```

-	Layers:
	-	`sha256:829b6f287091d2b84872c0fddbbfab37fd8179708a5ae713df30538debe4754d`  
		Last Modified: Wed, 19 Feb 2025 03:31:43 GMT  
		Size: 3.2 MB (3187548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60d72dd68251652d7de39de406fe26406e0ff88809eed6df8bcb7cc776a0110b`  
		Last Modified: Wed, 19 Feb 2025 03:31:43 GMT  
		Size: 23.2 KB (23241 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre21-temurin` - linux; riscv64

```console
$ docker pull tomcat@sha256:eb9f6cb18c6fed298e55d2f99b4af415e9a8e7743af58cff24c9a7c5519a6445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125144033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976ba9f2415510519282f0e24e179d37ae4305b56be8d0c1aefbd532924f1aab`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 27 Jan 2025 04:46:38 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:46:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:46:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:46:39 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:47:10 GMT
ADD file:69c46ae9666e78c27ca5b5f25cec1a5536ff16f17cb00104e5c77e722bd8d643 in / 
# Mon, 27 Jan 2025 04:47:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        riscv64)          ESUM='a8d219a4a97f9c53ba88cb8927910005d4f3d08a87ab1bdebff921ef41afa93d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Feb 2025 15:03:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Feb 2025 15:03:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Feb 2025 15:03:20 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Feb 2025 15:03:20 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Feb 2025 15:03:20 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Feb 2025 15:03:20 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Feb 2025 15:03:20 GMT
ENV TOMCAT_MAJOR=10
# Mon, 10 Feb 2025 15:03:20 GMT
ENV TOMCAT_VERSION=10.1.35
# Mon, 10 Feb 2025 15:03:20 GMT
ENV TOMCAT_SHA512=814500908e139fd984bbacf10ccf8ad400d129ce23a7ba47b771f0ca308b148e23a58c83eb924653f62ca2a0696c87fc6128c7a81def18b04c2f0c01f08009b9
# Mon, 10 Feb 2025 15:03:20 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Feb 2025 15:03:20 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 15:03:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Feb 2025 15:03:20 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Feb 2025 15:03:20 GMT
ENTRYPOINT []
# Mon, 10 Feb 2025 15:03:20 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6e1053d729cc1718daa9369927cf6ddfbf892a846041de0e610d1c77ade136c5`  
		Last Modified: Tue, 04 Feb 2025 07:00:41 GMT  
		Size: 31.0 MB (30983910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d426f87ee2be194a115f8eac0bc66ccf7efb2c0a509cd7e58933d92bc42969c7`  
		Last Modified: Wed, 05 Feb 2025 02:18:44 GMT  
		Size: 17.9 MB (17857942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106f41ec50b63050aa15a6caeb00adddf2b4f0c609643aa2a816f262de0edb31`  
		Last Modified: Wed, 05 Feb 2025 23:07:46 GMT  
		Size: 50.7 MB (50659994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11237b418844a1cafc905fb5df874530dbfce18fa8b73ee1e94672873954924f`  
		Last Modified: Wed, 05 Feb 2025 13:36:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196bf56f818043db847e82534e4107ab2d370f3f7aa12c726b7f75f8ac313935`  
		Last Modified: Wed, 05 Feb 2025 12:56:46 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40432f18bd62a55bb856dcd41e13d3638ef39f8572e65db17b2a2807f39759ce`  
		Last Modified: Sun, 09 Feb 2025 02:01:40 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41130243671f77675e9934d53d28c2dffe5dc350f06711803bd9e6e5a89ea9aa`  
		Last Modified: Wed, 12 Feb 2025 12:57:41 GMT  
		Size: 14.0 MB (14010811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540abf051be873189e414d669372a7a9bd7544b9ece6beab4f46bdb97047d466`  
		Last Modified: Sun, 16 Feb 2025 02:03:50 GMT  
		Size: 11.6 MB (11628731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:9a9d9f29ce1eeaf6812e09beb58538fc20c6ed698d1d729ae836628c73f73604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3199083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce16428d9c3aeba88b5bbf5c8d6e033cccbe7740d8224fc5e34db9cb2aa30d25`

```dockerfile
```

-	Layers:
	-	`sha256:37dea3b0959414ca112d7722fd9f59321474f6f1f53401dbee14da75d2761113`  
		Last Modified: Sun, 16 Feb 2025 02:03:52 GMT  
		Size: 3.2 MB (3175842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34e52859e4720041b61a6dc47d83545775723985f970f75625b9f8228874edf2`  
		Last Modified: Wed, 12 Feb 2025 12:57:45 GMT  
		Size: 23.2 KB (23241 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre21-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:88f69430c3a334b14c1ea693cc3091aecc3d310d6f1dd2725f8c0721d36e1fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (122966053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c23f823e6ce7ce147130f0ba19164332fdc27e330b0d78175063a3930c2c8cb2`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 27 Jan 2025 04:15:19 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:15:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:15:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:15:19 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:15:20 GMT
ADD file:1a65bb049384da7e51a2b1e9180f11d6ec22b1427da7ca5682814abd261ba57e in / 
# Mon, 27 Jan 2025 04:15:20 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        riscv64)          ESUM='a8d219a4a97f9c53ba88cb8927910005d4f3d08a87ab1bdebff921ef41afa93d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 18 Feb 2025 15:03:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 18 Feb 2025 15:03:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 15:03:21 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 18 Feb 2025 15:03:21 GMT
WORKDIR /usr/local/tomcat
# Tue, 18 Feb 2025 15:03:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 15:03:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 18 Feb 2025 15:03:21 GMT
ENV TOMCAT_MAJOR=10
# Tue, 18 Feb 2025 15:03:21 GMT
ENV TOMCAT_VERSION=10.1.36
# Tue, 18 Feb 2025 15:03:21 GMT
ENV TOMCAT_SHA512=972a406263fd540b135efae4b375543781b26104acb07114c3e535fe31e5b0a5c87ae6dff055e0e47877a3861070c264bb236686cf08bc08d98b7541e5d743c7
# Tue, 18 Feb 2025 15:03:21 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 18 Feb 2025 15:03:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 15:03:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 18 Feb 2025 15:03:21 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 18 Feb 2025 15:03:21 GMT
ENTRYPOINT []
# Tue, 18 Feb 2025 15:03:21 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8e1d25585ef2d346b71072d258a697a9d190e3c5754512c7cb978dbbe80911e6`  
		Last Modified: Tue, 04 Feb 2025 08:21:20 GMT  
		Size: 30.0 MB (30027563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d99804e9821e45800ab00828f52aba64f96835ac1dcd99956c5eae60156908a`  
		Last Modified: Tue, 04 Feb 2025 10:14:32 GMT  
		Size: 17.6 MB (17595734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9de6ffcc06fd168ab48b022ca8332f879c58295907a2a4f63b36b280c515c1e`  
		Last Modified: Wed, 05 Feb 2025 04:28:07 GMT  
		Size: 49.5 MB (49463175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ed1350b4fe6b91c7f4cf372a366be83e91d5c5a5f83d87c686d5e076b088ec`  
		Last Modified: Wed, 05 Feb 2025 04:28:07 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc317318c6b368c7e7951dcef797ef8c7db0b64ab5ca3bcc16562f544de7004`  
		Last Modified: Tue, 04 Feb 2025 16:27:50 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c432268e59726122cba8f3782f0fa913f0a71d0c9ecac24b746bea0e255d3a39`  
		Last Modified: Wed, 05 Feb 2025 12:50:20 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af83e74c3c6d8b683132f371165517cddff6a216592db1e7f2130190b881260`  
		Last Modified: Wed, 19 Feb 2025 02:17:21 GMT  
		Size: 13.8 MB (13839353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b0dd651b824373ef9a1949227ec380786e179f88c9e9522bd4d4c64693639f`  
		Last Modified: Wed, 19 Feb 2025 02:17:30 GMT  
		Size: 12.0 MB (12037584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre21-temurin` - unknown; unknown

```console
$ docker pull tomcat@sha256:c88ec1976d2a41e02986714516aa263608cbfff0580ec80aa7850710bca8fbc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3208937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0957a7ccaf543165792b07aac02257f2c055fb4ff97f18f7c800ac0536864d6`

```dockerfile
```

-	Layers:
	-	`sha256:b0e0fd3491caf9ba40f2a31aabbfee41041e94ed79136b6eee28022ce91b9dad`  
		Last Modified: Wed, 19 Feb 2025 03:31:47 GMT  
		Size: 3.2 MB (3185784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f973bccaf4bc3c9f9dc17fea7320ccdb73b748058110f8775afe88725025adee`  
		Last Modified: Wed, 19 Feb 2025 03:31:47 GMT  
		Size: 23.2 KB (23153 bytes)  
		MIME: application/vnd.in-toto+json
