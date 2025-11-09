## `tomcat:11-jre25-temurin-jammy`

```console
$ docker pull tomcat@sha256:6cfd3cc8a7929b5d1ef9e7783cc5fdc6f6cd84fa1cffff8c2d8683bf0c705c91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `tomcat:11-jre25-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:96d3753443afce2ddd40d1bca16f7f62c55e75354d0aca20220e421df3df7d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 MB (117958783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173c9ca18d22123a53df64930bbac64e538623a3f593f71a85725afd618751f9`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 18:00:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:00:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:00:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 18:00:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:00:32 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 18:00:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        arm64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:00:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:00:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:00:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 19:19:36 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 19:19:36 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:19:36 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 19:19:36 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 19:19:36 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:19:36 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:19:36 GMT
ENV TOMCAT_MAJOR=11
# Sat, 08 Nov 2025 19:19:36 GMT
ENV TOMCAT_VERSION=11.0.13
# Sat, 08 Nov 2025 19:19:36 GMT
ENV TOMCAT_SHA512=cc7cc21a671cb42d0b0f7381d2933c36415bfbe7419bf2561e8f88a5b75c2f5a738f3fcf7a1096c0cec3bac14b08e43c6f37c0983ee545672ffa2888cb8dd61a
# Sat, 08 Nov 2025 19:19:36 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 08 Nov 2025 19:19:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 19:19:43 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 08 Nov 2025 19:19:43 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 19:19:43 GMT
ENTRYPOINT []
# Sat, 08 Nov 2025 19:19:43 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6510df90aaf6ceaf3f951fc7d64e89b65b9b64143fd6e6f2f9f1f676545ef58`  
		Last Modified: Sat, 08 Nov 2025 18:01:16 GMT  
		Size: 11.4 MB (11404548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2228750769407eb28fa51d649bb3f5510864a02c1b7032180851726ce478f674`  
		Last Modified: Sat, 08 Nov 2025 18:01:29 GMT  
		Size: 62.7 MB (62687787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c996064fc0386a5d3a1a3d9fa56ee380b6e1bc2b989942f6a8528480102d2fe`  
		Last Modified: Sat, 08 Nov 2025 18:01:13 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d3f9e200570b04a4059c5df7b2052f7ec0eb48a4300acf66c312d19862f969`  
		Last Modified: Sat, 08 Nov 2025 19:19:58 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502d3eb79b78907491da341d76806a1285bd121a378aaf1ae28d3bc603b0b620`  
		Last Modified: Sat, 08 Nov 2025 19:20:00 GMT  
		Size: 14.1 MB (14113669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196e013eedf40542949b0ccd871db4c4191349220e69b4f11d56d096652f3ec7`  
		Last Modified: Sat, 08 Nov 2025 19:19:58 GMT  
		Size: 213.4 KB (213445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:b82421fcca1e4aa2b4cd22b837259931b147d2cf64e03b181b6d25b0f8af081c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30021f709974c320e6056d6702ca8e083dd8189840481625ffbbdbf67146a21`

```dockerfile
```

-	Layers:
	-	`sha256:d38f7dbae031760be9c7a4aab758ded56f48af89183318d9d4e6320499af6097`  
		Last Modified: Sat, 08 Nov 2025 21:39:39 GMT  
		Size: 3.7 MB (3709487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d74bddfe6abf4d17352fa753fd2b5a42a44b1350f9f86f21647cbea7317df4c`  
		Last Modified: Sat, 08 Nov 2025 21:39:40 GMT  
		Size: 21.5 KB (21533 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre25-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:15d5064c211eb2daad2f63c1b03ba9c42c3c65612bd7c0abae216833156c6e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114711497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcddbbf2d1c41999ece16942996b93c9c51c88b9a649b878e4b2d6d866475a9a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 18:00:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:00:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:00:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 18:00:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:00:02 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 18:00:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        arm64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:00:21 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:00:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:00:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 19:19:23 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 19:19:23 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:19:23 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 19:19:23 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 19:19:23 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:19:23 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:19:23 GMT
ENV TOMCAT_MAJOR=11
# Sat, 08 Nov 2025 19:19:23 GMT
ENV TOMCAT_VERSION=11.0.13
# Sat, 08 Nov 2025 19:19:23 GMT
ENV TOMCAT_SHA512=cc7cc21a671cb42d0b0f7381d2933c36415bfbe7419bf2561e8f88a5b75c2f5a738f3fcf7a1096c0cec3bac14b08e43c6f37c0983ee545672ffa2888cb8dd61a
# Sat, 08 Nov 2025 19:19:23 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 08 Nov 2025 19:19:29 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 19:19:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 08 Nov 2025 19:19:29 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 19:19:29 GMT
ENTRYPOINT []
# Sat, 08 Nov 2025 19:19:29 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a990beddf5e4b01af9c65b599641437c6ef7ac83d823f2d3b2f2327dbc8a6059`  
		Last Modified: Sat, 08 Nov 2025 18:00:45 GMT  
		Size: 11.4 MB (11357747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86e09fcb6ff39a6c4b94c1dafbba559fb4d24acb5c8e74cd5a39210562e6db7`  
		Last Modified: Sat, 08 Nov 2025 18:00:48 GMT  
		Size: 61.6 MB (61638741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae07793e0e1ee544d90107dbaec35e20c92afc4156d29b01c572d3a5a7e404b`  
		Last Modified: Sat, 08 Nov 2025 18:00:43 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698df77cd6966d99e346b1f3945fb522bf91c0b01280bc5d9830d15ce1ce0cd4`  
		Last Modified: Sat, 08 Nov 2025 19:19:44 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8edf1149ae5491a57e85c4442287cfc75da6ca0dd82bbed429e6013baf1a84`  
		Last Modified: Sat, 08 Nov 2025 19:19:47 GMT  
		Size: 14.1 MB (14116778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617ea6137c81a0c7705662bd7f1e58a7c7d49e7456ea8368d8d5f9cf346b20d8`  
		Last Modified: Sat, 08 Nov 2025 19:19:44 GMT  
		Size: 212.6 KB (212608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:90a9087f935dd7f0abb178903707079ad3bd09f69d5f751232bdf3edc3b5d131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c2e02e1bd2db07192a0555af3dce78ef9dc1c797c946bcc633e000f8e3d5ce`

```dockerfile
```

-	Layers:
	-	`sha256:6176af9e94523ea9ce77418c9a63a701337f707d4439af30f3740098a2f8bc83`  
		Last Modified: Sat, 08 Nov 2025 21:39:44 GMT  
		Size: 3.7 MB (3709150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e680b0a697233c454353b31d19f50ab143cd71b9d7b2a10f9c0f4aedfe011090`  
		Last Modified: Sat, 08 Nov 2025 21:39:45 GMT  
		Size: 21.7 KB (21694 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre25-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:1c0cee16818d0e81913692e19eae29eaaaa40bba76a132cd564e3a3c8eda908c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122835841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590742f8a7550a7811d29bc7e4e23237a306a68832fea84fb7e2238bc2013dc5`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 07:06:37 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:06:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:06:42 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 01 Oct 2025 07:06:43 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 18:33:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:33:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:33:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 18:33:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:33:29 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 18:33:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        arm64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:33:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:33:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:33:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 22:10:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 22:10:49 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 22:10:49 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 22:10:50 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 22:10:50 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 22:10:50 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 22:10:50 GMT
ENV TOMCAT_MAJOR=11
# Sat, 08 Nov 2025 22:10:50 GMT
ENV TOMCAT_VERSION=11.0.13
# Sat, 08 Nov 2025 22:10:50 GMT
ENV TOMCAT_SHA512=cc7cc21a671cb42d0b0f7381d2933c36415bfbe7419bf2561e8f88a5b75c2f5a738f3fcf7a1096c0cec3bac14b08e43c6f37c0983ee545672ffa2888cb8dd61a
# Sat, 08 Nov 2025 22:10:51 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 08 Nov 2025 22:11:02 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 22:11:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 08 Nov 2025 22:11:05 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 22:11:05 GMT
ENTRYPOINT []
# Sat, 08 Nov 2025 22:11:05 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05a419dbbdae4c74ce8cbea20f33b711554ca281ea5b632c3cbf7fed8d819f4`  
		Last Modified: Sat, 08 Nov 2025 18:34:32 GMT  
		Size: 11.9 MB (11893670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efacde85c6a9be3b7e0b804b464c7e4f0160319d2406c6114a8cbde0e096cec9`  
		Last Modified: Sat, 08 Nov 2025 18:34:34 GMT  
		Size: 62.1 MB (62123046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db4f445e55d6ead60bf318ddd25e4ca7e4425be6b9f26330912f1e66c3aaf26`  
		Last Modified: Sat, 08 Nov 2025 18:34:32 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4502b6af0a831da3fa12abdd640b138a274f9a2acb7deeda30a7d1a4f1cee23`  
		Last Modified: Sat, 08 Nov 2025 22:11:48 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9493aa74593409a0e08bb2c90e7e8f2e6df889e7797be3e7000fa8d2a1d6947`  
		Last Modified: Sat, 08 Nov 2025 22:11:51 GMT  
		Size: 14.1 MB (14126723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ac10543467c8cb8e97fd729295b8199f67fdad4321d4817073e23dd659cb35`  
		Last Modified: Sat, 08 Nov 2025 22:11:48 GMT  
		Size: 243.1 KB (243095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:863a02225a6fe9b1b430871bd42e2bc0454b134af80d99a2a7b55b22f1477b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3734425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37203e3cfc344599498e3e67e844fa68ec1f0a60858aa96fbe50f9b3c6dfb39e`

```dockerfile
```

-	Layers:
	-	`sha256:c98f6b6e652ee4e9125bb86f92697849c4ac0e3dccf5edde36e07e1f1a4591eb`  
		Last Modified: Sun, 09 Nov 2025 00:32:50 GMT  
		Size: 3.7 MB (3712833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da8da6d5ef3b314d6167fea6dfc06a10e0b5b45efbf6c81568b464ad33b16eb1`  
		Last Modified: Sun, 09 Nov 2025 00:32:51 GMT  
		Size: 21.6 KB (21592 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre25-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:add19f46faee7547ea9fe70f5f0d7f2fb641163c2d33bcfa0b4a947e42ace011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.1 MB (114145345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:051a0e3ff14f328837bf27371d506bbb6e2d13d0495102629d773c2a1937f2cc`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:26 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:28 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Wed, 01 Oct 2025 07:05:28 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 18:17:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:17:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:17:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 18:17:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:17:56 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 18:18:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        arm64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:18:09 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:18:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:18:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 21:27:31 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 21:27:31 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:27:31 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 21:27:31 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 21:27:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 21:27:31 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 21:27:31 GMT
ENV TOMCAT_MAJOR=11
# Sat, 08 Nov 2025 21:27:31 GMT
ENV TOMCAT_VERSION=11.0.13
# Sat, 08 Nov 2025 21:27:31 GMT
ENV TOMCAT_SHA512=cc7cc21a671cb42d0b0f7381d2933c36415bfbe7419bf2561e8f88a5b75c2f5a738f3fcf7a1096c0cec3bac14b08e43c6f37c0983ee545672ffa2888cb8dd61a
# Sat, 08 Nov 2025 21:27:32 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 08 Nov 2025 21:27:34 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 21:27:36 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 08 Nov 2025 21:27:36 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 21:27:36 GMT
ENTRYPOINT []
# Sat, 08 Nov 2025 21:27:36 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5224ee9f1eda0ee26a6b72e8ef1534e70542038a9b3622af533a5010050bd007`  
		Last Modified: Sat, 08 Nov 2025 18:18:49 GMT  
		Size: 11.5 MB (11497447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020ebcd5925b1404168463882e031fbd63d36dedb9fffd13627e7ce2ca4ec960`  
		Last Modified: Sat, 08 Nov 2025 18:18:49 GMT  
		Size: 60.3 MB (60310260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d0d5477cee9470b2961c247786f5e5ed28cc7024f5647c18206e991ce657aa`  
		Last Modified: Sat, 08 Nov 2025 18:18:46 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b5d88d3b7b135a50a73e2b920d2a3ca957b67a345075168cd1c16d5c73febb`  
		Last Modified: Sat, 08 Nov 2025 21:27:58 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dffb7b603d7fe4ec1e0ff9447114a6abfef7061e07f81195ae33062914b5d9`  
		Last Modified: Sat, 08 Nov 2025 21:28:00 GMT  
		Size: 14.1 MB (14117114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1e628143b824c46bfdc48f8b6626095bf0f99e6c7a33a01fb7de8679b4c7dd`  
		Last Modified: Sat, 08 Nov 2025 21:27:59 GMT  
		Size: 214.6 KB (214594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre25-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:10d50df1ed40a6444d19fdee18b660bb9f837cf4350a2028dfb9b2dd4899ff77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276c0b60e93dd682aaf4fdfc19a49286068646ea6505b9cdb239c7428deee545`

```dockerfile
```

-	Layers:
	-	`sha256:fe7126fde1fab6069add93f793cfe72a90e02129d21ead4ac5e837ea2375e3d0`  
		Last Modified: Sun, 09 Nov 2025 00:33:33 GMT  
		Size: 3.7 MB (3710472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01c4f8535706411b0c92c9bed298ee3a77191fc98e477c410acf757af9f48538`  
		Last Modified: Sun, 09 Nov 2025 00:33:34 GMT  
		Size: 21.5 KB (21534 bytes)  
		MIME: application/vnd.in-toto+json
