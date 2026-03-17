## `tomcat:9-jre8-temurin-jammy`

```console
$ docker pull tomcat@sha256:17a03eacb16b529ecafa3383d898f8644c3c730415a2e9acd6f041999a60658f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `tomcat:9-jre8-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:8f718db9b1fbd52aacad79352e3ec0242641750d850a466a7a1257dd45af33f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102059692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f048c915dbc64d365e31d70b57281adfe82897d9f2b9e7082462d208d1c22649`
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
# Tue, 17 Feb 2026 20:18:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:18:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:18:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:18:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:18:55 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 17 Feb 2026 20:18:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='01672ca52509f4cb1ffa8aed905808fed7b984f3e279cb13d90a6e865ff6199f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='46496dfa7e58784adf96a3a2bd1ac8be9fda2d8749a9c52bf74fb582aa1449e2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='29c93e29421b9f77bc95305834f3239313466fd988111b5cf409fd9a2f727cff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='b563c5c90dcff0c1cf5a1bdc3110e560c979254a17e696902e922631264cf342';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 17 Feb 2026 20:18:58 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:18:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:18:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 21:57:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Feb 2026 21:57:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:57:19 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Feb 2026 21:57:19 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Feb 2026 21:57:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:57:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:57:19 GMT
ENV TOMCAT_MAJOR=9
# Tue, 17 Feb 2026 21:57:19 GMT
ENV TOMCAT_VERSION=9.0.115
# Tue, 17 Feb 2026 21:57:19 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Tue, 17 Feb 2026 21:57:20 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Feb 2026 21:57:27 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:57:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Feb 2026 21:57:27 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Feb 2026 21:57:27 GMT
ENTRYPOINT []
# Tue, 17 Feb 2026 21:57:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19485500effe774d88eb31279162f221fad8592432db590bd76aaa25086979ad`  
		Last Modified: Tue, 17 Feb 2026 20:19:10 GMT  
		Size: 16.1 MB (16147866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517b3a95c42c62ed220ad559a440c8815efc942fe4cfed71b3df4a7a2a825a3c`  
		Last Modified: Tue, 17 Feb 2026 20:19:10 GMT  
		Size: 42.3 MB (42331715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70da753b4e04e4b5349f555b8f1fb22daf0bf95a9886bee2b7af17ab61605aab`  
		Last Modified: Tue, 17 Feb 2026 20:19:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dddf1cda97b9cbd1e5af091f8a520ab30154ea9b1f80e37d90dd9b418bec902`  
		Last Modified: Tue, 17 Feb 2026 20:18:50 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be0e420f6951ed88ed9ab9f5401a95ab9c8a7b5e76ad94afbdf4298f80487aa`  
		Last Modified: Tue, 17 Feb 2026 21:57:36 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e111429191a4b5330a38ad60f831893cc543149b09982a75cacf1602878001d`  
		Last Modified: Tue, 17 Feb 2026 21:57:36 GMT  
		Size: 13.8 MB (13810429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef85aba5d9a6643cdfb7d5d29afe7d6e2c08057a03275f457cdbfce377ec0bf`  
		Last Modified: Tue, 17 Feb 2026 21:57:36 GMT  
		Size: 229.7 KB (229701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:304fb96d37946d3e1c1a7e4024fe62794e107f814d5629264a3954decb1a9240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3989204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2180a2bb3d21e71af5ef3eded5fac008a1f9e2bce89a95f35812544571777701`

```dockerfile
```

-	Layers:
	-	`sha256:e10b31ac12737ccc1357d02922665d48a05cbb6835226cd607d3a83e5728d7a0`  
		Last Modified: Tue, 17 Feb 2026 21:57:36 GMT  
		Size: 4.0 MB (3968009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de165bf86842a3836dedfe90b791e978fa50ceb74a6c50b5087d7ab24904b44b`  
		Last Modified: Tue, 17 Feb 2026 21:57:36 GMT  
		Size: 21.2 KB (21195 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:7dec4e2ec66115eca8b3f790acd1f7fcda2e2973896599f784ceac766a080df4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96252432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc78d3c1f92eec09cd217df716079c9fb6a32c5538065fc2abbd368cab0a3721`
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
# Tue, 17 Feb 2026 20:12:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:12:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:12:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:12:05 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 17 Feb 2026 20:12:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='01672ca52509f4cb1ffa8aed905808fed7b984f3e279cb13d90a6e865ff6199f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='46496dfa7e58784adf96a3a2bd1ac8be9fda2d8749a9c52bf74fb582aa1449e2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='29c93e29421b9f77bc95305834f3239313466fd988111b5cf409fd9a2f727cff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='b563c5c90dcff0c1cf5a1bdc3110e560c979254a17e696902e922631264cf342';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 17 Feb 2026 20:12:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:12:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 21:43:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Feb 2026 21:43:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:43:44 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Feb 2026 21:43:44 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Feb 2026 21:43:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:43:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:43:44 GMT
ENV TOMCAT_MAJOR=9
# Tue, 17 Feb 2026 21:43:44 GMT
ENV TOMCAT_VERSION=9.0.115
# Tue, 17 Feb 2026 21:43:44 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Tue, 17 Feb 2026 21:43:44 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Feb 2026 21:43:51 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:43:52 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Feb 2026 21:43:52 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Feb 2026 21:43:52 GMT
ENTRYPOINT []
# Tue, 17 Feb 2026 21:43:52 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8994f3e4ab606dcbf77ca1a5364851191cbe725563408ee7cd2a667cb364bed0`  
		Last Modified: Tue, 10 Feb 2026 18:13:45 GMT  
		Size: 26.6 MB (26644404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd536de969d0fd9c45d2db47f84e158936a73ae21e56f10850e3a54d84898b9`  
		Last Modified: Tue, 17 Feb 2026 20:12:29 GMT  
		Size: 15.9 MB (15890746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8f0abc05adb29920ce97f1b533c27b986ebdc8867ee3bc08e0ed45f7c6c64d`  
		Last Modified: Tue, 17 Feb 2026 20:12:33 GMT  
		Size: 39.8 MB (39768483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8b93b8f4aeeb58eb64a6fec53578b2dc206aeaf196d2e86a4cbb4b90bdd8eb`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f942f1870a4cc51bfe2c50e227d7fead2a8d00de8ff2dbafb4f31075d9c6f12a`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75e8f172810500dd6564b2df37cc8497022ff35bb4473c104024b909b0adfc4`  
		Last Modified: Tue, 17 Feb 2026 21:44:01 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af006015277ed29389ad4e6a3768d8f056eddabb833cc40cdfc2d396eb7604b`  
		Last Modified: Tue, 17 Feb 2026 21:44:01 GMT  
		Size: 13.7 MB (13743540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457803615c3a05496e7d4dd5e5a056c9159b16e916e5728d915a7428f2b8d8fa`  
		Last Modified: Tue, 17 Feb 2026 21:44:01 GMT  
		Size: 202.6 KB (202649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:0e21007f0a1d0776dbe21d77856834101f5073457d2721d1489732e07cf400d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3995342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956e6d0dfdc48ffa3af191bd4699b3a1d8763b623147f37a2d026e016bc103c3`

```dockerfile
```

-	Layers:
	-	`sha256:55671db6853817c3c7e5cf76dcefa6b38d970a7f5b90406558c49baab699dc6c`  
		Last Modified: Tue, 17 Feb 2026 21:44:01 GMT  
		Size: 4.0 MB (3974027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:062f726f4bf51d5c68cb6a8f0fd1d27ac343f33062a582625d5edfdd4b290c70`  
		Last Modified: Tue, 17 Feb 2026 21:44:00 GMT  
		Size: 21.3 KB (21315 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:800ce8aeca7c87985cd83bedba6b293b23f7b64fb838f403861fe3fa8a474d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98817534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e886f457d713614853de9b8cffd8def613028d013826fc2db63ae6628d9317de`
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
# Tue, 17 Mar 2026 01:23:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 01:23:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:23:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:23:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:23:00 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 17 Mar 2026 01:23:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='01672ca52509f4cb1ffa8aed905808fed7b984f3e279cb13d90a6e865ff6199f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='46496dfa7e58784adf96a3a2bd1ac8be9fda2d8749a9c52bf74fb582aa1449e2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='29c93e29421b9f77bc95305834f3239313466fd988111b5cf409fd9a2f727cff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='b563c5c90dcff0c1cf5a1bdc3110e560c979254a17e696902e922631264cf342';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 17 Mar 2026 01:23:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 01:23:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:23:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 03:30:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Mar 2026 03:30:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:30:44 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Mar 2026 03:30:44 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Mar 2026 03:30:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Mar 2026 03:30:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Mar 2026 03:30:44 GMT
ENV TOMCAT_MAJOR=9
# Tue, 17 Mar 2026 03:30:44 GMT
ENV TOMCAT_VERSION=9.0.115
# Tue, 17 Mar 2026 03:30:44 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Tue, 17 Mar 2026 03:30:44 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Mar 2026 03:30:53 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:30:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Mar 2026 03:30:54 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Mar 2026 03:30:54 GMT
ENTRYPOINT []
# Tue, 17 Mar 2026 03:30:54 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9760802dfd0cb54abb91f0a7edff239728c4ae9fb364b171184c3c341f45817b`  
		Last Modified: Tue, 17 Mar 2026 01:23:18 GMT  
		Size: 16.1 MB (16073512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364deb1b44d498b45d7f865ed71de7f6c0588ba6c70cb0a833efeb30ee8513ce`  
		Last Modified: Tue, 17 Mar 2026 01:23:39 GMT  
		Size: 41.3 MB (41289515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039590b91c1a5633763de654f502132ff886b8b298b16128a7aeb6eb89471d00`  
		Last Modified: Tue, 17 Mar 2026 01:23:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19eb0ad147a0608825f4cd4473901fa2e5e0634fc537bef67750ddd8b1fcb0b3`  
		Last Modified: Tue, 17 Mar 2026 01:23:38 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4aadcadbe88592aec227f91ee20ffc5a004957012252ae308f3f18480efd2dc`  
		Last Modified: Tue, 17 Mar 2026 03:31:04 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c6da916145bb2aa4456cc3d279daf44c275cd79ef0b3433d4798cbddfd1305`  
		Last Modified: Tue, 17 Mar 2026 03:31:04 GMT  
		Size: 13.8 MB (13816874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bd2e8af6ebca365d11494910ad1e7204e2761e0715cc56c47f2763010fdd66`  
		Last Modified: Tue, 17 Mar 2026 03:31:04 GMT  
		Size: 246.0 KB (245996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:876b7ac76cc09aef6d04dbce0bb65136dd7911ee6f9fca393e4aca92ae738f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a4c79c91b7dc824979a9d12d9729b1224a99e27b9c71d4cbbef9b6a1df911c`

```dockerfile
```

-	Layers:
	-	`sha256:30fd999cc2943a78d1684aefdf054c3ce8789481c51dd32b21b7ad1f05df8051`  
		Last Modified: Tue, 17 Mar 2026 03:31:04 GMT  
		Size: 4.0 MB (3970057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c7b05f6554cdc5f7b2d45826afff2c4f3e4701d6a3ad7e18e1baad3bac323c6`  
		Last Modified: Tue, 17 Mar 2026 03:31:04 GMT  
		Size: 21.3 KB (21343 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre8-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:4f457b5a175fb7dc1cf9564d35b1ef8c8861f3ec55501ee0f9cfe4bffc76e9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.9 MB (107890399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421d4ec3bbc8464f61bb6433a877192824ad77fc7d52f60c46c2d82cccbfa202`
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
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 17 Feb 2026 20:14:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='01672ca52509f4cb1ffa8aed905808fed7b984f3e279cb13d90a6e865ff6199f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='46496dfa7e58784adf96a3a2bd1ac8be9fda2d8749a9c52bf74fb582aa1449e2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='29c93e29421b9f77bc95305834f3239313466fd988111b5cf409fd9a2f727cff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='b563c5c90dcff0c1cf5a1bdc3110e560c979254a17e696902e922631264cf342';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 17 Feb 2026 20:14:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:14:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:14:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Feb 2026 01:15:02 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 18 Feb 2026 01:15:02 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 01:15:02 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 18 Feb 2026 01:15:03 GMT
WORKDIR /usr/local/tomcat
# Wed, 18 Feb 2026 01:15:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 18 Feb 2026 01:15:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 18 Feb 2026 01:15:03 GMT
ENV TOMCAT_MAJOR=9
# Wed, 18 Feb 2026 01:15:03 GMT
ENV TOMCAT_VERSION=9.0.115
# Wed, 18 Feb 2026 01:15:03 GMT
ENV TOMCAT_SHA512=8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b
# Wed, 18 Feb 2026 01:15:05 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 18 Feb 2026 01:15:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 01:15:15 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 18 Feb 2026 01:15:15 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 18 Feb 2026 01:15:15 GMT
ENTRYPOINT []
# Wed, 18 Feb 2026 01:15:15 GMT
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
	-	`sha256:b16abd84f6a59a69dea81e3f28b5394a0a6fa47212c8c66336f6158b432b0c0f`  
		Last Modified: Tue, 17 Feb 2026 20:14:33 GMT  
		Size: 41.7 MB (41723577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb03d139d9985ae75c239ef2372ecc53774a731efedb39163be6ad931d08bdb`  
		Last Modified: Tue, 17 Feb 2026 20:14:31 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bd90c01e79e2b9a827f81a14112ce86aebfce484bd7dfe68cd2729ff154388`  
		Last Modified: Tue, 17 Feb 2026 20:14:31 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3afe35d5aca7dd12cf8dca61aba975555792a807c7215c3d13444b28c008739f`  
		Last Modified: Wed, 18 Feb 2026 01:15:37 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1da7a9495d3240c868d146e211cd3fc0b0cec474221d9d8b41462f8279dcc7`  
		Last Modified: Wed, 18 Feb 2026 01:15:38 GMT  
		Size: 13.8 MB (13839979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8345c574b8ba30f242064ffb79bcd0c60d9b880ddb09192c58d95f64ea7dce81`  
		Last Modified: Wed, 18 Feb 2026 01:15:37 GMT  
		Size: 259.0 KB (259015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre8-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:1b833f0d87c255e6de15df515d8cecbc432932100c352a073f7c0606940e2b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3994036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35814127ba2d913fccac9f7bfa566ef1901c59cfa7a4084a0a787fa78b8bd8e1`

```dockerfile
```

-	Layers:
	-	`sha256:2e51e312ed44e47d67bfb860b1ad0075c77a8a9b8c2671e67f26ef4b55466a05`  
		Last Modified: Wed, 18 Feb 2026 01:15:38 GMT  
		Size: 4.0 MB (3972789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15a0830a81c3fe1e4ec46f09a521e03f0fea88e0ad5c82b1e5c130ce32460434`  
		Last Modified: Wed, 18 Feb 2026 01:15:37 GMT  
		Size: 21.2 KB (21247 bytes)  
		MIME: application/vnd.in-toto+json
