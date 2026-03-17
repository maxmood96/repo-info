## `tomcat:9-jre11-temurin-jammy`

```console
$ docker pull tomcat@sha256:c01f6535ac1c7d6b585037199a0b9433502f037740f1921201d729ba9d26e408
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

### `tomcat:9-jre11-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:33f5c87b4cd6c7ef5e150843bf56cd1cb13691aee35fcccd025233a47a15cb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 MB (107033532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee6ee94cecd88518f974c065c7bdfea70fa542c7595ad4a27fdd28534b5925f`
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
# Tue, 17 Feb 2026 20:19:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:19:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:19:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:19:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:19:30 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 17 Feb 2026 20:19:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d851e43d81ec6ff7f28efe28c42b4787a045e8f59cdcd6434dece98d8342eb8a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='9d6a8d3a33c308bbc7332e4c2e2f9a94fbbc56417863496061ef6defef9c5391';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='8cc849890ecee80b002171f54b6df7d14744b83ba44646f52f5ca927a85599b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='d64f2f707b3940789f3d75c8cf55a409e786c3ca4c0e85f3fedf42e1e3ef63ae';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='634f7ee49a6f1e8be64dfaf91b9c0306b5662d40bd5624010f6a9c4862e4e1b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:19:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:19:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:19:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 21:57:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Feb 2026 21:57:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:57:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Feb 2026 21:57:06 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Feb 2026 21:57:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:57:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:57:06 GMT
ENV TOMCAT_MAJOR=9
# Tue, 17 Feb 2026 21:57:06 GMT
ENV TOMCAT_VERSION=9.0.115
# Tue, 17 Feb 2026 21:57:06 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Tue, 17 Feb 2026 21:57:07 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Feb 2026 21:57:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:57:15 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Feb 2026 21:57:15 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Feb 2026 21:57:15 GMT
ENTRYPOINT []
# Tue, 17 Feb 2026 21:57:15 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4804f1fdba5db6263aa9cef2cb2eb349bccf7520ef2045a2f37adfe536110f36`  
		Last Modified: Tue, 17 Feb 2026 20:19:47 GMT  
		Size: 16.1 MB (16147760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ae4292e7310c9dd7a73ce342bbe0b5a4881140dce08e4d75bd5d4e9846c8ca`  
		Last Modified: Tue, 17 Feb 2026 20:19:48 GMT  
		Size: 47.3 MB (47304859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc16c48ad9961eda011a81c6f66754c89c3db758210c0ddcd1e7d6a252095929`  
		Last Modified: Tue, 17 Feb 2026 20:19:47 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541c74ca5ea93a4f9d16bda05779f9211ca9a5a01ca068b7967c4c099ab6bb58`  
		Last Modified: Tue, 17 Feb 2026 20:19:47 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff79654690185e29f054eade39c13d5936d00f6bd45f4f5c074a1e203fb2b41d`  
		Last Modified: Tue, 17 Feb 2026 21:57:26 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12956d342622406d69b78d8bcb3f6253c890546e1bb0cf485719ce234f9d26e`  
		Last Modified: Tue, 17 Feb 2026 21:57:27 GMT  
		Size: 13.8 MB (13811230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f0315a169f55a7f0645333394f15cb3c74acf91a963c5c24a17aad9b951acf`  
		Last Modified: Tue, 17 Feb 2026 21:57:27 GMT  
		Size: 229.7 KB (229676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:ab5670450f1607b099505a0194016a08a7438851ada861636fc73b5c3752f5d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3972855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23f8188e8dcd5c028a7cc216954ab57528132cb9e49991f3134460085b0690f`

```dockerfile
```

-	Layers:
	-	`sha256:c3882ecc4ddad3b6a89c61eed21d1cd9f634721b9b286be56e65f62f6ccdd98f`  
		Last Modified: Tue, 17 Feb 2026 21:57:27 GMT  
		Size: 4.0 MB (3951643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94bf698ae88a0f53b9b94e2bc0a9104f16fc854bad4a680a28d28efffc880f75`  
		Last Modified: Tue, 17 Feb 2026 21:57:26 GMT  
		Size: 21.2 KB (21212 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:1c328a7bc8ad8aa146d607a3e3753febf42818146a0fe9b7a44e34aa6026121d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101901125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91312f65d944acd445553b279f1a3e466310ca63285b95594980c8ad0c07bd8c`
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
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 17 Feb 2026 20:11:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d851e43d81ec6ff7f28efe28c42b4787a045e8f59cdcd6434dece98d8342eb8a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='9d6a8d3a33c308bbc7332e4c2e2f9a94fbbc56417863496061ef6defef9c5391';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='8cc849890ecee80b002171f54b6df7d14744b83ba44646f52f5ca927a85599b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='d64f2f707b3940789f3d75c8cf55a409e786c3ca4c0e85f3fedf42e1e3ef63ae';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='634f7ee49a6f1e8be64dfaf91b9c0306b5662d40bd5624010f6a9c4862e4e1b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:11:54 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:11:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:11:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 21:43:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Feb 2026 21:43:37 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:43:37 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Feb 2026 21:43:37 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Feb 2026 21:43:37 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:43:37 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:43:37 GMT
ENV TOMCAT_MAJOR=9
# Tue, 17 Feb 2026 21:43:37 GMT
ENV TOMCAT_VERSION=9.0.115
# Tue, 17 Feb 2026 21:43:37 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Tue, 17 Feb 2026 21:43:37 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Feb 2026 21:43:43 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:43:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Feb 2026 21:43:44 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Feb 2026 21:43:44 GMT
ENTRYPOINT []
# Tue, 17 Feb 2026 21:43:44 GMT
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
	-	`sha256:cc425d90925aaf19b768f8fe0ac1058c37bce60f13bdd77cd614427644ab40a6`  
		Last Modified: Tue, 17 Feb 2026 20:12:07 GMT  
		Size: 45.4 MB (45416589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f02f6c8e17287c2b3b5e2c418640acc5728b72027aca8522a633abbd0a9f665`  
		Last Modified: Tue, 17 Feb 2026 20:12:05 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d301d49a456c0ebc97d8d89f350d42472f8f21feb503941fbf7b9c034a03cad3`  
		Last Modified: Tue, 17 Feb 2026 20:12:05 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dbdad6d9182c6fd2f2c46cc49cdc03f3a1683e349e16bcd02f73e94fad143f`  
		Last Modified: Tue, 17 Feb 2026 21:43:52 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73eded82b4568fc52a100a0d94f72fe350d4f4f28fa2dc25338d96e54bfc05c4`  
		Last Modified: Tue, 17 Feb 2026 21:43:52 GMT  
		Size: 13.7 MB (13744454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64b991e381d5c38c2a681415e066f07d042c42495b180e9f82df27822847263`  
		Last Modified: Tue, 17 Feb 2026 21:43:52 GMT  
		Size: 202.4 KB (202390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:7c2f2132413208357852738cba78fef77bd8944ecdbbdc2270f602e007c0fb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3976574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef1bacae300c3686b53bb98fda31b82dc9ad058967d593ad2dd2b7592d7d621`

```dockerfile
```

-	Layers:
	-	`sha256:5009f5e09bcef500a8907d872b52e74f7ad899c9c2b9842a589d36941df8f9d4`  
		Last Modified: Tue, 17 Feb 2026 21:43:52 GMT  
		Size: 4.0 MB (3955241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af8bf2938465e2a74fc6acea5525a877d398d21e028caf8dbc57ba48bb62ab86`  
		Last Modified: Tue, 17 Feb 2026 21:43:52 GMT  
		Size: 21.3 KB (21333 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:afaddef442ec59b6fcbaaa38df0dd68d7bfd251638791f540ff9faf212091e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103151991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a6b779fde361e6c071bc4c8971b141fc1f83a68adfeaeea2a5f7c1427b9dca`
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
# Tue, 17 Mar 2026 01:24:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:24:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:24:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:24:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:24:04 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 17 Mar 2026 01:24:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d851e43d81ec6ff7f28efe28c42b4787a045e8f59cdcd6434dece98d8342eb8a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='9d6a8d3a33c308bbc7332e4c2e2f9a94fbbc56417863496061ef6defef9c5391';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='8cc849890ecee80b002171f54b6df7d14744b83ba44646f52f5ca927a85599b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='d64f2f707b3940789f3d75c8cf55a409e786c3ca4c0e85f3fedf42e1e3ef63ae';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='634f7ee49a6f1e8be64dfaf91b9c0306b5662d40bd5624010f6a9c4862e4e1b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 01:24:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:24:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:24:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 03:30:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Mar 2026 03:30:34 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:30:34 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Mar 2026 03:30:35 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Mar 2026 03:30:35 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Mar 2026 03:30:35 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Mar 2026 03:30:35 GMT
ENV TOMCAT_MAJOR=9
# Tue, 17 Mar 2026 03:30:35 GMT
ENV TOMCAT_VERSION=9.0.115
# Tue, 17 Mar 2026 03:30:35 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Tue, 17 Mar 2026 03:30:35 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Mar 2026 03:30:43 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:30:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Mar 2026 03:30:44 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Mar 2026 03:30:44 GMT
ENTRYPOINT []
# Tue, 17 Mar 2026 03:30:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aebabb6c4062c793d5e35e91d00d9d3a0e3235a157695f2846d4d1b8fb83b33`  
		Last Modified: Tue, 17 Mar 2026 01:24:21 GMT  
		Size: 16.1 MB (16073532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f3c4c48fa363061748e1b4b44defacb606e837013a6c35beab4c7fbd245f9b`  
		Last Modified: Tue, 17 Mar 2026 01:24:21 GMT  
		Size: 45.6 MB (45623171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec68e1314aafa981e4da279b49292e4e9c80859a2d52bd38b8a314f09fbf4df`  
		Last Modified: Tue, 17 Mar 2026 01:24:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce46d69c3bdd5ce9fcbb146b9ff025de4cc38e7e2535f5e6ad8c9d32289244df`  
		Last Modified: Tue, 17 Mar 2026 01:24:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc59473b83c5787eae3c0b60d805f19f58875b3cdc75ec06e76838d7b988c305`  
		Last Modified: Tue, 17 Mar 2026 03:30:52 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ac97cc65818efec36f9322e9c8c4f594e237a8e6ee5c2f34053691c4120271`  
		Last Modified: Tue, 17 Mar 2026 03:30:53 GMT  
		Size: 13.8 MB (13817558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a110de12090dcf0b03b0152dd90a742a4269303298cbaa839faccadc3ae011`  
		Last Modified: Tue, 17 Mar 2026 03:30:52 GMT  
		Size: 246.1 KB (246059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:236af6714c001c1db0ccd70764ebae660aaba3df6557b236dd08b768a299b161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3974978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87eb38072a313a8ab75d0a3b0307c21391da169c5d5a455b91ca285a983d4c52`

```dockerfile
```

-	Layers:
	-	`sha256:65d9581cd85d54e98d11e2b5a5b26e7caa571b91367e7b4bdb20b03ef9de65d4`  
		Last Modified: Tue, 17 Mar 2026 03:30:53 GMT  
		Size: 4.0 MB (3953617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcc53d3daf68bf7af95acae9237f9979072404b0fb1b45f757990bc37bcf0d88`  
		Last Modified: Tue, 17 Mar 2026 03:30:52 GMT  
		Size: 21.4 KB (21361 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:eb7108f34242c1377ee738a1d52c52006ad348ffeb21ae572367c2948aa88c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.9 MB (108919521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45448a08d2c8f0f34a73ad90eb0c5117e82e850c14d6bbe4e73f02cd073ed4ce`
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
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 17 Feb 2026 20:16:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d851e43d81ec6ff7f28efe28c42b4787a045e8f59cdcd6434dece98d8342eb8a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='9d6a8d3a33c308bbc7332e4c2e2f9a94fbbc56417863496061ef6defef9c5391';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='8cc849890ecee80b002171f54b6df7d14744b83ba44646f52f5ca927a85599b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='d64f2f707b3940789f3d75c8cf55a409e786c3ca4c0e85f3fedf42e1e3ef63ae';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='634f7ee49a6f1e8be64dfaf91b9c0306b5662d40bd5624010f6a9c4862e4e1b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:16:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:16:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:16:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Feb 2026 01:10:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 18 Feb 2026 01:10:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 01:10:15 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 18 Feb 2026 01:10:18 GMT
WORKDIR /usr/local/tomcat
# Wed, 18 Feb 2026 01:10:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 18 Feb 2026 01:10:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 18 Feb 2026 01:10:18 GMT
ENV TOMCAT_MAJOR=9
# Wed, 18 Feb 2026 01:10:18 GMT
ENV TOMCAT_VERSION=9.0.115
# Wed, 18 Feb 2026 01:10:18 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Wed, 18 Feb 2026 01:14:04 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 18 Feb 2026 01:14:13 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 01:14:15 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 18 Feb 2026 01:14:15 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 18 Feb 2026 01:14:15 GMT
ENTRYPOINT []
# Wed, 18 Feb 2026 01:14:15 GMT
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
	-	`sha256:74b8b60be8f316f9c091ab37569dcbb4b2cf44dbcf60e14c5c9474b601115c83`  
		Last Modified: Tue, 17 Feb 2026 20:16:52 GMT  
		Size: 42.8 MB (42752043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242e2010de0a4fb49175bd0415bbf2e3a9a93e1846edfef53300d477f247d190`  
		Last Modified: Tue, 17 Feb 2026 20:16:51 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76586b62d496f315bf452f8df1fd8a3528164c39f0cccdf7b7a696938ead7153`  
		Last Modified: Tue, 17 Feb 2026 20:16:51 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46294b951d84f568801e69eeab3956d82ae6f7029efe094379c5ff021fb4069`  
		Last Modified: Wed, 18 Feb 2026 01:10:53 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf38d85807b834fa620b134775d380337563311c9b3751bf272f5677750a252b`  
		Last Modified: Wed, 18 Feb 2026 01:14:45 GMT  
		Size: 13.8 MB (13840600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3bdbdabba4867eb136249c12fc5aebf68a1febd11954153426914ff608a95a`  
		Last Modified: Wed, 18 Feb 2026 01:14:45 GMT  
		Size: 259.0 KB (259021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:f8255b3c7f9e970c4653e517d050c97ba7180e8f79d5d99f3112ce7f5cea78a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3977002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab48511d825ef061a80056107d26f97bfd64dbd30f714e537481d90591bde41`

```dockerfile
```

-	Layers:
	-	`sha256:405633813f54f273b6cb2a694a110ee3cf0853743c357cc963586626958b2adc`  
		Last Modified: Wed, 18 Feb 2026 01:14:45 GMT  
		Size: 4.0 MB (3955737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49d2575d38b46b55dcb50b42336274686de758dbdefe841cdaff8abc85513a58`  
		Last Modified: Wed, 18 Feb 2026 01:14:45 GMT  
		Size: 21.3 KB (21265 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre11-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:9f932de30408668f23f3e411ea955ede7e081b66516f5b84e0a9dd47917ebec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.5 MB (99502858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:365a2f939007771e13f13f3c40792ac023f6e188fdbf90c5e4582659b860d437`
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
# Tue, 17 Feb 2026 20:12:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:12:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:12:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:12:17 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 17 Feb 2026 20:12:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d851e43d81ec6ff7f28efe28c42b4787a045e8f59cdcd6434dece98d8342eb8a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='9d6a8d3a33c308bbc7332e4c2e2f9a94fbbc56417863496061ef6defef9c5391';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='8cc849890ecee80b002171f54b6df7d14744b83ba44646f52f5ca927a85599b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='d64f2f707b3940789f3d75c8cf55a409e786c3ca4c0e85f3fedf42e1e3ef63ae';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='634f7ee49a6f1e8be64dfaf91b9c0306b5662d40bd5624010f6a9c4862e4e1b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:12:21 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:12:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 22:46:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Feb 2026 22:46:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:46:07 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Feb 2026 22:46:08 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Feb 2026 22:46:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 22:46:08 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 22:46:08 GMT
ENV TOMCAT_MAJOR=9
# Tue, 17 Feb 2026 22:46:08 GMT
ENV TOMCAT_VERSION=9.0.115
# Tue, 17 Feb 2026 22:46:08 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Tue, 17 Feb 2026 22:48:45 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Feb 2026 22:48:51 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 22:48:52 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Feb 2026 22:48:52 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Feb 2026 22:48:52 GMT
ENTRYPOINT []
# Tue, 17 Feb 2026 22:48:52 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4e2905dbd81d6a42c24ec5f7ce51f2d8f24a616b4fe2e90d0be791922a8d3b5f`  
		Last Modified: Tue, 10 Feb 2026 18:14:06 GMT  
		Size: 28.0 MB (28004382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73b5a836a80e76f7aacb936a6f06937407b800d97b6cda60dbcede34fcbad1a`  
		Last Modified: Tue, 17 Feb 2026 20:12:51 GMT  
		Size: 16.1 MB (16146973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac46e96a1c1493ec679787fc38892e73fae0dafe17b9d68b174e0ab4d1517d9`  
		Last Modified: Tue, 17 Feb 2026 20:12:51 GMT  
		Size: 41.3 MB (41310487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5c5de575eb2b1cea7f9e1752349e5e1fb749d27d2aa5b794cde5c296dc14cd`  
		Last Modified: Tue, 17 Feb 2026 20:12:49 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039becd43cb53ef7c781fef10a594c005353960e71cc7618c941df0770857963`  
		Last Modified: Tue, 17 Feb 2026 20:12:50 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d80beb27713979906001177109af936be4e97d02646f740b30af8c231092dc1`  
		Last Modified: Tue, 17 Feb 2026 22:46:42 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de868715ab593ac8e77aa9a70d475a42044e6303aa71c17de800bd0b35157d3`  
		Last Modified: Tue, 17 Feb 2026 22:49:12 GMT  
		Size: 13.8 MB (13807372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ed5324302dabcdee103e7a8592f6cd22386c1d390fb55d567c6e3c63bdc522`  
		Last Modified: Tue, 17 Feb 2026 22:49:12 GMT  
		Size: 231.0 KB (231002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:97e09394fbab3f0ac835fb8f26b6c26979ba046382a0d3c05045633a77e720f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3974452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296e5c70df17f15eba83289b4ea31c8256c9c42490674ce4e68804460aac1853`

```dockerfile
```

-	Layers:
	-	`sha256:5e7cb4370f9c1305211e9891f6ccee464526a7a7c7c0e5c77ba5fa2ba00d2e5c`  
		Last Modified: Tue, 17 Feb 2026 22:49:12 GMT  
		Size: 4.0 MB (3953240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd8305b6b4e0cb5d72dcd2d6f6d6e5e477a4c187193726db55595ca1631aee98`  
		Last Modified: Tue, 17 Feb 2026 22:49:12 GMT  
		Size: 21.2 KB (21212 bytes)  
		MIME: application/vnd.in-toto+json
