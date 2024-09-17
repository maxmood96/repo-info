## `tomcat:jre11-temurin-jammy`

```console
$ docker pull tomcat@sha256:72d7afb32856afb3a631a870706b31528559eab3a491c06b069ae5cc8c73509a
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

### `tomcat:jre11-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:530a698f8646ec058b8f95aed7e9fd508d153277ed991e8cc1dd977a53ca10ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.4 MB (106427176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4706fb1ed8463b4356c52b074ca99006580ab8ce977c226cf93de6791f89df`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
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
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9bd9906fae2af9b98f929fef09d486905c0599093bb299b441e7eed58ada7`  
		Last Modified: Sat, 17 Aug 2024 01:10:02 GMT  
		Size: 12.9 MB (12870875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a880dee0d8e92fc9854fd2480b4c183eba1429a09ed63d9e60edad44fa8edf01`  
		Last Modified: Sat, 17 Aug 2024 01:12:06 GMT  
		Size: 47.2 MB (47198423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5deab9cbd68168c5b0fe4bf55d9d3be31e0a75abb267f5e59e8973d11616df`  
		Last Modified: Sat, 17 Aug 2024 01:11:59 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c142282fae08f434334ed5f1bd8f2abe5c67c7c9c3611c0c18f80b49bb4ffc`  
		Last Modified: Fri, 23 Aug 2024 19:26:26 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9dd568cbd6bfe81bed23902af5572f807011397951261941dfda383edb943d`  
		Last Modified: Wed, 11 Sep 2024 19:54:53 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cc96029ead9001d205f81eacc194401b8f042c9d957cadfb30f8f7d9f0f563`  
		Last Modified: Wed, 11 Sep 2024 19:54:54 GMT  
		Size: 12.9 MB (12949111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb359507029d4e98ad8a532826e4a6d4722b2d10c6aed79a8e5019aab3ae3c41`  
		Last Modified: Wed, 11 Sep 2024 19:54:54 GMT  
		Size: 3.0 MB (2965583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:1df530f8b80d10e3df0c35ce8fd5089d5ba3bd71f987327f911e4c5e561648dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3555713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b76f2cc723c011138b8502f7f12f6475769fc53bcfd254cb33c3fc931c1dae`

```dockerfile
```

-	Layers:
	-	`sha256:52d4bd87a3e4a01831072792eaebc7bd4d52dc760efbd4a0d8e4f73afdc231b2`  
		Last Modified: Wed, 11 Sep 2024 19:54:54 GMT  
		Size: 3.5 MB (3533623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b141c3a01281e14270139d5054b49f6f864e4ca4910bdd01ca656096fc1a3a2c`  
		Last Modified: Wed, 11 Sep 2024 19:54:53 GMT  
		Size: 22.1 KB (22090 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre11-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:cef3ebbd8ce67ea2dcec850619f70175a235df79c3cda9de2bd9873f46e7b326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98436101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1156851c0692b163557366bb75539acc6aa28bbe169ff2cb869c4efe6dfd4867`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 11 Sep 2024 02:03:19 GMT
ARG RELEASE
# Wed, 11 Sep 2024 02:03:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 02:03:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 02:03:19 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 02:03:19 GMT
ADD file:291158c1d919b2d4290b5112a77dc0f7bdf0d45caa53b3556390707d29d2796a in / 
# Wed, 11 Sep 2024 02:03:19 GMT
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
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:35baf9f88f9b2cb840329dab5e6720d4fc535f9c150ca402cd7cd955065cd481`  
		Last Modified: Fri, 13 Sep 2024 12:45:25 GMT  
		Size: 27.5 MB (27534027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31edfebc2dc37b7fcd5adfb6ee3872ba74788ba24e8c2c3a40107b9fd85153c`  
		Last Modified: Tue, 17 Sep 2024 01:23:55 GMT  
		Size: 12.5 MB (12463235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7afd409eab60981e29c8a6688ad5a9f38412d8e808d6c93d1adf8ceda230a2`  
		Last Modified: Tue, 17 Sep 2024 01:25:46 GMT  
		Size: 45.3 MB (45320254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde853a21068fadf8fa2378cc65c78bec7c0344869f42fb55d9587313044ce96`  
		Last Modified: Tue, 17 Sep 2024 01:25:39 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d461f10508d6b5b73c53ba5b08248e2a7ecb4246162ec8d15344a0dab64e5c7a`  
		Last Modified: Tue, 17 Sep 2024 01:25:39 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f6f74df4ba9b3f06db5fbb61e8ea14c0e2567631fed1bd18199787197c9f5b`  
		Last Modified: Tue, 17 Sep 2024 03:08:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdb8043f2c891d075f0305480a45df487ae01f286e2ff5b6052f28503e63875`  
		Last Modified: Tue, 17 Sep 2024 03:08:30 GMT  
		Size: 12.9 MB (12925183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606c98a53f6a3f3a8e8d21b3b787a0a95131e4f288a907d6a9ad5e7f9c2b0668`  
		Last Modified: Tue, 17 Sep 2024 03:08:30 GMT  
		Size: 190.9 KB (190931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:4a48c118f76b786e61e0bf4cebe9e7108193b2764a9d978ab3e36bf25dbce82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3555190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c879a2eb502bf082c1afe9b0de5ff989040516ddc735c13b53fc45d21fd46a4`

```dockerfile
```

-	Layers:
	-	`sha256:545a075456ecc4392305e4ec624fbbc42b0b7df2648f14a722ed61ec274127cb`  
		Last Modified: Tue, 17 Sep 2024 03:08:28 GMT  
		Size: 3.5 MB (3532966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecfee76c10bc83dbcac0c938a7f4df48d2f35360f5aec27dc541165bfbe3fef0`  
		Last Modified: Tue, 17 Sep 2024 03:08:28 GMT  
		Size: 22.2 KB (22224 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre11-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:894065df5f0a69dddbb298b722cb1b12aac74f6f04c406937efb65a662b35a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102527879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8366c418c592a386c32b10a3b8fcfd463bbd1eda232130a1daa83bfa995b825`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
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
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a13fc23d23d50177fc33d5df0e5c516fdbaae7d5cb53c11d634dff7e6e365e`  
		Last Modified: Sat, 17 Aug 2024 01:33:12 GMT  
		Size: 12.8 MB (12813299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4dbb8ab7ebb70bbdbb49ab2085d99ae87968ea251f304e9fa059e7155f13e5`  
		Last Modified: Sat, 17 Aug 2024 01:35:00 GMT  
		Size: 45.6 MB (45557024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ed86303b2ff16bd4b17f7c739a9055711b72b99e566885505d9258cd44e26c`  
		Last Modified: Sat, 17 Aug 2024 01:34:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604cf0e08e3afff9c340aa7610394aaab11665931337af35d9c0e0f3b770c4b`  
		Last Modified: Fri, 23 Aug 2024 19:44:09 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6259602b4bdb820044feec66e63aa4e89b14e7807e2f2c8e326582d864b902a`  
		Last Modified: Wed, 11 Sep 2024 19:58:19 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9102cec92f0c6dc746b90de85511e2c2e02c69cb21d1489cf29f259c5fba8ad6`  
		Last Modified: Wed, 11 Sep 2024 19:58:20 GMT  
		Size: 13.0 MB (12951407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b393eaf224588c9c5e6b20f74fc4457d053c240b2cd4b11da745bf33e24e519e`  
		Last Modified: Wed, 11 Sep 2024 19:58:20 GMT  
		Size: 2.8 MB (2806569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:5cbb470515df242adcc2a42929c4706f64bc0619ffbafcbc360f511a1ac443b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3556662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da765bcdb95d177b68ca22db101cafe9536838783bedfc8770f3967f2513e7a`

```dockerfile
```

-	Layers:
	-	`sha256:9f52de7262ffc7d0f30f8257a46aa6b0cba0496bf7440d1679d0fe28009bd85c`  
		Last Modified: Wed, 11 Sep 2024 19:58:19 GMT  
		Size: 3.5 MB (3533915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e01f8e8d77ef59249c8a7e1de8a9820068b528b1331ab616aee7ba1234dee16`  
		Last Modified: Wed, 11 Sep 2024 19:58:19 GMT  
		Size: 22.7 KB (22747 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre11-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:60c7954f82aaa56cb6ad387576b4f919a562957c7499cdc848b2520e9914d5d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108269144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09509d66af006e8d45820b4963d515d163dc0bd8d84fc24bf5cd1ac38de0c66a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
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
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2b9159aba5847bda25160889018a02e4997ea0539f37f28faa599fcc4e6e59`  
		Last Modified: Sat, 17 Aug 2024 00:59:09 GMT  
		Size: 13.7 MB (13715085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b50c4b0fab19a16a502b1681ff9177a05eed203d81aa04a49df18907898c34`  
		Last Modified: Sat, 17 Aug 2024 01:01:26 GMT  
		Size: 42.7 MB (42652048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338034862f9398ecf41f81f3eb5a9837d4cbe84271d6141f09462837e4a51105`  
		Last Modified: Sat, 17 Aug 2024 01:01:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a3378494275db0692fa539ce9a900d0fdd467054c1b7a1322760ca73ff5eb2`  
		Last Modified: Fri, 23 Aug 2024 19:23:06 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df85bb8d0400455b03632cf7e76047dd9515b646b930e4f79fecd9a6ea319311`  
		Last Modified: Wed, 11 Sep 2024 20:01:47 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b065dcb7ea76c6074d042aa4e5e4881a4d7b6f264e54d668bf8c7872de92153f`  
		Last Modified: Wed, 11 Sep 2024 20:01:48 GMT  
		Size: 13.0 MB (12963293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce73df3f19ed4994d8937fec83b66664bfa82b9f68986f96e11afe3fa805acf`  
		Last Modified: Wed, 11 Sep 2024 20:01:48 GMT  
		Size: 3.3 MB (3348604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:fb3425404591ce30578f5d6738c8bae5edcd1940351d7517ce8f198546b28027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3560301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2470833c9b1fc6ce74414d95867ea6814d5ad9ea10dca6fb53507d5e3e855f1a`

```dockerfile
```

-	Layers:
	-	`sha256:f06473400dce959d806ffb5497dc9a4a6ed9ca079b59d38b78461ca6adbc55b5`  
		Last Modified: Wed, 11 Sep 2024 20:01:48 GMT  
		Size: 3.5 MB (3538142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba7b9166c455bff202a836e6312fb33237ffcd2048d871f49e541d6da7c8665`  
		Last Modified: Wed, 11 Sep 2024 20:01:47 GMT  
		Size: 22.2 KB (22159 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre11-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:15b041b839c9f98fd1d4e538d8eb2633db38bc2cd518a943147d024a5ce012e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98016939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791fdc8078fd148e76e3528d32498aa7bbd8168780452621d386bfef4906a9f1`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:24 GMT
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
# Tue, 13 Aug 2024 09:28:24 GMT
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
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f487d2bc1de52e44ed06dfc0c18b748d484f1eb638bdc1cbf599195a96c480be`  
		Last Modified: Sat, 17 Aug 2024 01:32:19 GMT  
		Size: 13.0 MB (12955186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c53d190393eca7947899727783f31b4d629b8cb328dd252d9cf9e1f57f52823`  
		Last Modified: Sat, 17 Aug 2024 01:33:01 GMT  
		Size: 40.8 MB (40817132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7494c9a7e12442d8d3b7e7296f1a1231b234cdff9fa8892908bd413186609079`  
		Last Modified: Sat, 17 Aug 2024 01:32:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a24efbce9923f1d97c259e8e4ad520ca7f8b4fca7b20ac51689a5644df5f9a4`  
		Last Modified: Fri, 23 Aug 2024 19:47:07 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2693898fdcb675dd3363bcfccfd2f6097f3e419ba8f383c0ef4e45be4b265a3d`  
		Last Modified: Wed, 11 Sep 2024 19:59:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1596d3a29acf89766752c399f7c73f3fccc4a43d652ec9f71bd70cbf2e4c53ef`  
		Last Modified: Wed, 11 Sep 2024 19:59:41 GMT  
		Size: 13.0 MB (12952962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecd16dedc0c77855354653efcdc542004fa5fa22afa210d2f3b9406ab2ab171`  
		Last Modified: Wed, 11 Sep 2024 19:59:41 GMT  
		Size: 2.7 MB (2650685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre11-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:3cfd7e54c1337e983f0639a536050f607fc7c5b6107e688ba4a57d4ea929da81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3556853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c500fc6a10894afca9866b540f769c1d0bc5e74bf5b431de5b30d8f5de051880`

```dockerfile
```

-	Layers:
	-	`sha256:6bb9a4f7a40f34603bb2a9ac7e65a68e8cc54575501117ac835caab8ce553bcc`  
		Last Modified: Wed, 11 Sep 2024 19:59:41 GMT  
		Size: 3.5 MB (3534745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a0aee72eb30412f5e89699eca8485bdf7039bf546d9d8e6b1e3f1da0a48f174`  
		Last Modified: Wed, 11 Sep 2024 19:59:41 GMT  
		Size: 22.1 KB (22108 bytes)  
		MIME: application/vnd.in-toto+json
