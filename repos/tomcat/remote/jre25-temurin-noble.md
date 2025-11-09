## `tomcat:jre25-temurin-noble`

```console
$ docker pull tomcat@sha256:89a24bdfadfc1c0ae42aa248f15a0a6bb4897677958eb131a8b7b2f5150a9492
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

### `tomcat:jre25-temurin-noble` - linux; amd64

```console
$ docker pull tomcat@sha256:e2e10f1f0ba678223da484ad3c97cd118460dc806351eeaa8d84ae26bbbbab93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118230838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:648558a8bfa778e9773c552729df2c59f073b535226c48fa5c3e6d68839ebafc`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 18:00:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:00:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:00:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 18:00:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:00:36 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 18:00:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        arm64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        riscv64)          ESUM='31af8beb1071d499bf4d55d4709aef49055e854c3f6b505d01296f947fde3b8f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:00:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:00:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:00:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 19:19:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 19:19:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:19:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 19:19:00 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 19:19:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:19:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:19:00 GMT
ENV TOMCAT_MAJOR=11
# Sat, 08 Nov 2025 19:19:00 GMT
ENV TOMCAT_VERSION=11.0.13
# Sat, 08 Nov 2025 19:19:00 GMT
ENV TOMCAT_SHA512=cc7cc21a671cb42d0b0f7381d2933c36415bfbe7419bf2561e8f88a5b75c2f5a738f3fcf7a1096c0cec3bac14b08e43c6f37c0983ee545672ffa2888cb8dd61a
# Sat, 08 Nov 2025 19:19:01 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 08 Nov 2025 19:19:07 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 19:19:07 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 08 Nov 2025 19:19:07 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 19:19:07 GMT
ENTRYPOINT []
# Sat, 08 Nov 2025 19:19:07 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30670d501d3ce40fe4f5bf7661c0c79c1da5957051f93d28a6907d1353494515`  
		Last Modified: Sat, 08 Nov 2025 18:01:21 GMT  
		Size: 11.5 MB (11475249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55661abd799d15a2181d8c288b176da62a5d10580e4910dedaee78af06b163b5`  
		Last Modified: Sat, 08 Nov 2025 18:01:31 GMT  
		Size: 62.7 MB (62719748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d198d9aaf04ae2088ef48826f8d34e3d44e623d7aa8effd74120bbae02ba61`  
		Last Modified: Sat, 08 Nov 2025 18:01:20 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ac41583ca3e05feba21368d119c1cd462cadeb41bdab309af3a5a7bf71ee4d`  
		Last Modified: Sat, 08 Nov 2025 19:19:27 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c33c63a63ed9799899e136624ebd99d8971ac097dc5215821d020dbb83069`  
		Last Modified: Sat, 08 Nov 2025 19:19:30 GMT  
		Size: 14.1 MB (14102547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc132fa611e4f6fb372a915eebdee0c5aa852870130441ee60018fce16bf210d`  
		Last Modified: Sat, 08 Nov 2025 19:19:30 GMT  
		Size: 207.6 KB (207631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre25-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:152f9a1896dbf53a1f8cf838224cd70c1754e2c928e544499edc15857c482bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28dd4df38b7bd5312856c7f4be9ef224a5f5e4c8d23155f3c3294370e834f8a2`

```dockerfile
```

-	Layers:
	-	`sha256:4a7ea6e6276bd1c86838185d7d1c31f95e8892318dcb803dd3a6e0f0114314aa`  
		Last Modified: Sat, 08 Nov 2025 21:39:21 GMT  
		Size: 3.1 MB (3130096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7747313586ee2f5b7962b51e7f8bde9691fba52d4160c10e7f8d733d6674e44e`  
		Last Modified: Sat, 08 Nov 2025 21:39:22 GMT  
		Size: 24.0 KB (24029 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre25-temurin-noble` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:3f98bd252baff3900838f25b1e4615efccbebf3a3ade748d336ac28a0a9f28a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116316316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc1c735924587b7a0f4ad5bb2cc4afd4fd2d46bc84bbbfa7c631f0738d49696`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:57:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:57:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:57:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:57:25 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:57:25 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 17:57:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        arm64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        riscv64)          ESUM='31af8beb1071d499bf4d55d4709aef49055e854c3f6b505d01296f947fde3b8f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:57:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:57:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:57:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 19:19:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 19:19:17 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:19:17 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 19:19:17 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 19:19:17 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:19:17 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:19:17 GMT
ENV TOMCAT_MAJOR=11
# Sat, 08 Nov 2025 19:19:17 GMT
ENV TOMCAT_VERSION=11.0.13
# Sat, 08 Nov 2025 19:19:17 GMT
ENV TOMCAT_SHA512=cc7cc21a671cb42d0b0f7381d2933c36415bfbe7419bf2561e8f88a5b75c2f5a738f3fcf7a1096c0cec3bac14b08e43c6f37c0983ee545672ffa2888cb8dd61a
# Sat, 08 Nov 2025 19:19:17 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 08 Nov 2025 19:19:24 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 19:19:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 08 Nov 2025 19:19:24 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 19:19:24 GMT
ENTRYPOINT []
# Sat, 08 Nov 2025 19:19:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecc0d6f0c28b88dd7238c9615f92cba9c20606e7397917676eec89f6fc1726b`  
		Last Modified: Sat, 08 Nov 2025 17:58:06 GMT  
		Size: 11.5 MB (11469942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c0931cdd23dec1759e3b4d532a76ac06c7143f20ded4da5e61cb1bc95db481`  
		Last Modified: Sat, 08 Nov 2025 17:58:14 GMT  
		Size: 61.7 MB (61670196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d177faed2d538cb0d70abd5d202c3f3a2d0e87030587905c12f947a802381bf1`  
		Last Modified: Sat, 08 Nov 2025 17:58:05 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c72ee75e1923129e87aa25f0156732bdae326a8fcb851b4a8c16ad67fd08dd2`  
		Last Modified: Sat, 08 Nov 2025 19:19:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e4dfd80013dec2e8bf246184ecd9338a2d4ade726ab98fdf9c2ad69d565377`  
		Last Modified: Sat, 08 Nov 2025 19:19:43 GMT  
		Size: 14.1 MB (14104498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e985f3d9a9a84a6788b341e78e67f17d68a30f29f003b3454bb8365f0a66e287`  
		Last Modified: Sat, 08 Nov 2025 19:19:41 GMT  
		Size: 207.5 KB (207452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre25-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:14a0249c17a0ef87225faae4587b21cfb2e2a38e3875fdc9379077ad4d341c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed930ffbd9064b3a416a491767e2a1eaed8c499c3a13dccacf2a65fe4754fcc`

```dockerfile
```

-	Layers:
	-	`sha256:b964122debe7354b9db6bb7d043ca468a87b70c787b0d5d5810e7864b1cc78a2`  
		Last Modified: Sat, 08 Nov 2025 21:39:26 GMT  
		Size: 3.1 MB (3130642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:096c0b965948a43c56cdbb51719c4476af1bf8b6d150f50b28d1ea5a9e796566`  
		Last Modified: Sat, 08 Nov 2025 21:39:26 GMT  
		Size: 24.3 KB (24285 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre25-temurin-noble` - linux; ppc64le

```console
$ docker pull tomcat@sha256:20d5578d7dadd341cc4c1598b1b52289aca70b23be76baa06249e25dfface116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122868261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b89032130ffb22a07ddb1da3061f58c68e4e511f4521ef022497ba9eb09c14`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 18:34:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:34:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:34:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 18:34:58 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:34:58 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 18:35:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        arm64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        riscv64)          ESUM='31af8beb1071d499bf4d55d4709aef49055e854c3f6b505d01296f947fde3b8f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:35:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:35:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:35:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 22:09:38 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 22:09:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 22:09:38 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 22:09:39 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 22:09:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 22:09:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 22:09:39 GMT
ENV TOMCAT_MAJOR=11
# Sat, 08 Nov 2025 22:09:39 GMT
ENV TOMCAT_VERSION=11.0.13
# Sat, 08 Nov 2025 22:09:39 GMT
ENV TOMCAT_SHA512=cc7cc21a671cb42d0b0f7381d2933c36415bfbe7419bf2561e8f88a5b75c2f5a738f3fcf7a1096c0cec3bac14b08e43c6f37c0983ee545672ffa2888cb8dd61a
# Sat, 08 Nov 2025 22:09:40 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 08 Nov 2025 22:09:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 22:09:52 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 08 Nov 2025 22:09:52 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 22:09:52 GMT
ENTRYPOINT []
# Sat, 08 Nov 2025 22:09:52 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7185e3b7e0b86c70bc8a316d3bf8636eae7246263a8ee2cb2efd19bcd8967c7f`  
		Last Modified: Sat, 08 Nov 2025 18:36:00 GMT  
		Size: 12.1 MB (12051438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c08d11e745c4889dbcf08e670fef00d145f43bfd77a19de934126a0a8987b9`  
		Last Modified: Sat, 08 Nov 2025 18:36:03 GMT  
		Size: 62.2 MB (62155111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c4d06c23c88af840168bab990a670beb9e56093123a4635d1fd84ec7e307f8`  
		Last Modified: Sat, 08 Nov 2025 18:36:00 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f8e9f662c5fa9a2d478eb243942a56858247e92dfab5b6af7010b611bf08da`  
		Last Modified: Sat, 08 Nov 2025 22:10:21 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea748987fa94bd76e845a41a4d1813213dbf99345561344c9e3b9d8e0421175`  
		Last Modified: Sat, 08 Nov 2025 22:10:22 GMT  
		Size: 14.1 MB (14116992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7db6246bd5fa95e73d5d05a801644b2a3cb293c7ccda7e9afdf8e0ecef81734`  
		Last Modified: Sat, 08 Nov 2025 22:10:21 GMT  
		Size: 238.7 KB (238680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre25-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:c77506cd5dca62bb56113aa5f90b72738e4d6ba30d28d9cbdf8d79c0a74d04b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3157577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4e3bd16c48257c3d32b4a77a16d96f8b7479023d7b8c28db81a6a4a9d28790`

```dockerfile
```

-	Layers:
	-	`sha256:250e1ac86b1556ea845d8240a84cd8bbc7141dc54def2ba4249ba991f8607333`  
		Last Modified: Sun, 09 Nov 2025 00:32:38 GMT  
		Size: 3.1 MB (3133441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2af5b2c1396726ccdf2df6184ef53586851259bc25e1d062715393e04c9a7633`  
		Last Modified: Sun, 09 Nov 2025 00:32:39 GMT  
		Size: 24.1 KB (24136 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre25-temurin-noble` - linux; riscv64

```console
$ docker pull tomcat@sha256:584ad322319e910e088bbd34ca75262652d607e7ef482b244be9e4369b4676e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118460917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c46f0b2cf626bf92d2f0b963186af18d62586e3e55438705a994b562bb66a898`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 25 Sep 2025 19:59:06 GMT
ARG RELEASE
# Thu, 25 Sep 2025 19:59:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 19:59:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 19:59:06 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 25 Sep 2025 19:59:06 GMT
ADD file:857dc87fbafae31881cff8c69aed267a033f5df226dd351ee89de918ad5678ce in / 
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5e3de13a1487ecc90f8b0cddc83a6cd4e053b4cd48ddcfe5d1f19178e6089fba';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_x64_linux_hotspot_25_36.tar.gz';          ;;        arm64)          ESUM='939a1517971985363b2b57b8c6008f4bd48b91f565366d6eb3bae3aa503a05e2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64el)          ESUM='f593d6c435f6498cfbdb1ca07d7b1fa33829b159abb31b992b6234c324794dad';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        riscv64)          ESUM='3ec1d5906104fb273821a5865235b673fcd2b55674c5aee68d15b429fdc7837c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_riscv64_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='485af5746df1bf3cd46da4e7f771e6d1eae5a31db695ab819c4c2401688a6871';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jre_s390x_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 13 Oct 2025 20:03:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 13 Oct 2025 20:03:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 20:03:28 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 13 Oct 2025 20:03:28 GMT
WORKDIR /usr/local/tomcat
# Mon, 13 Oct 2025 20:03:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 13 Oct 2025 20:03:28 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 13 Oct 2025 20:03:28 GMT
ENV TOMCAT_MAJOR=11
# Mon, 13 Oct 2025 20:03:28 GMT
ENV TOMCAT_VERSION=11.0.13
# Mon, 13 Oct 2025 20:03:28 GMT
ENV TOMCAT_SHA512=cc7cc21a671cb42d0b0f7381d2933c36415bfbe7419bf2561e8f88a5b75c2f5a738f3fcf7a1096c0cec3bac14b08e43c6f37c0983ee545672ffa2888cb8dd61a
# Mon, 13 Oct 2025 20:03:28 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 13 Oct 2025 20:03:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 20:03:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 13 Oct 2025 20:03:28 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 13 Oct 2025 20:03:28 GMT
ENTRYPOINT []
# Mon, 13 Oct 2025 20:03:28 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ff47a256ba51b80e9880bc96be4ac2f094c47e0fcd7eec71bab85787cfa54b8b`  
		Last Modified: Mon, 13 Oct 2025 04:10:18 GMT  
		Size: 31.0 MB (30951381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58828d390368ad3c3714bacaf6a81d87b07a08c4a5d3861021467c1f5f1ca4f7`  
		Last Modified: Wed, 15 Oct 2025 07:12:20 GMT  
		Size: 11.6 MB (11570720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266bc463790875b10592d6621664fed6338eca69c2ccf082db6e887aad5dde38`  
		Last Modified: Wed, 15 Oct 2025 07:12:24 GMT  
		Size: 61.4 MB (61441255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effc893000c359964999c297de90a67d91fdf22b2b06ce5fc982174e684d5e8e`  
		Last Modified: Wed, 15 Oct 2025 07:12:18 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78147c2eb60bd64ba09a036b2f05b4ce2f378b0163758b2a47831542d4ec30e7`  
		Last Modified: Thu, 16 Oct 2025 11:12:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4468e8c075979ff16e0efd0acd6f26f8bb26060bc754800d611959b25dbffe31`  
		Last Modified: Thu, 16 Oct 2025 11:12:46 GMT  
		Size: 14.3 MB (14284315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9d5d1fd61eac530a5d7adcf72223379b40c5ad4199f5ca85a751b6e3cd3c49`  
		Last Modified: Thu, 16 Oct 2025 11:12:44 GMT  
		Size: 210.7 KB (210727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre25-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:d0f31d1ec027fa929037ac134650867dc268f84597d85cbc717945df0605f5a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3146293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f369d63965507b422476310e799e4bf6e19ce21b38fab8cf693ecf50d2f4f18`

```dockerfile
```

-	Layers:
	-	`sha256:b34dd32d517aa5376bc2e6050306df33466a9c1b36991feeebb3c1b07f5d96ca`  
		Last Modified: Thu, 16 Oct 2025 14:31:41 GMT  
		Size: 3.1 MB (3122123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cab9194e76445a10e685d28216f71daba8c851e05cd7062ef5a0ab0e4befaaf2`  
		Last Modified: Thu, 16 Oct 2025 14:31:42 GMT  
		Size: 24.2 KB (24170 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre25-temurin-noble` - linux; s390x

```console
$ docker pull tomcat@sha256:39f1f4adb205a3de6e75de308b667dadc1026a2b4f454c971abe6d985407fb03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116346372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502fd4ff22f71c5e6058a95548cac0075cdf36d9274ec0b55681c25b603562b7`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:05 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:06 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:07 GMT
ADD file:1c921a1d937949898d3d4ba499ce8d41425fe6dd2c8fdbcddd0070f2699f05b2 in / 
# Wed, 01 Oct 2025 13:02:07 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 18:19:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:19:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:19:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 18:19:10 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:19:10 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 18:19:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        arm64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        riscv64)          ESUM='31af8beb1071d499bf4d55d4709aef49055e854c3f6b505d01296f947fde3b8f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_riscv64_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:19:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:19:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:19:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 21:26:46 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 21:26:46 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:26:46 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 21:26:47 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 21:26:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 21:26:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 21:26:47 GMT
ENV TOMCAT_MAJOR=11
# Sat, 08 Nov 2025 21:26:47 GMT
ENV TOMCAT_VERSION=11.0.13
# Sat, 08 Nov 2025 21:26:47 GMT
ENV TOMCAT_SHA512=cc7cc21a671cb42d0b0f7381d2933c36415bfbe7419bf2561e8f88a5b75c2f5a738f3fcf7a1096c0cec3bac14b08e43c6f37c0983ee545672ffa2888cb8dd61a
# Sat, 08 Nov 2025 21:26:47 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 08 Nov 2025 21:26:51 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 21:26:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 08 Nov 2025 21:26:53 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 21:26:53 GMT
ENTRYPOINT []
# Sat, 08 Nov 2025 21:26:53 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:67735b72a65d308a2c2c9505d0d6e8419b7f2654a16cbd56963d88e01202d507`  
		Last Modified: Wed, 01 Oct 2025 15:43:10 GMT  
		Size: 29.9 MB (29906151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312d03c497041436be1f60c4ccf883fcbaa69b13e058a271d439ae40a1c9ae3d`  
		Last Modified: Sat, 08 Nov 2025 18:19:53 GMT  
		Size: 11.8 MB (11768316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a0ee62bc5720ab94650690195d35ec2b0887be198dfe0489b8092aa9e97b83`  
		Last Modified: Sat, 08 Nov 2025 18:19:56 GMT  
		Size: 60.3 MB (60340575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f72a4c7c5a0d6344fcc28855b8bdb51ec0e42d49bc5c96af848f03929f08f74`  
		Last Modified: Sat, 08 Nov 2025 18:19:51 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc0fc0397b8d2280ce875d454125e1dc6c06454e7d914590a54010ae68f82f1`  
		Last Modified: Sat, 08 Nov 2025 21:27:18 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e08a79c63a660d7e7e87fff5bac3df492595d0581057f4f01703759152867c0`  
		Last Modified: Sat, 08 Nov 2025 21:27:19 GMT  
		Size: 14.1 MB (14113855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15a9412f630682c6f9bd0d88d1f4d2f636ea5b3ee4dd55356f500e31484e2fb`  
		Last Modified: Sat, 08 Nov 2025 21:27:18 GMT  
		Size: 215.0 KB (214959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre25-temurin-noble` - unknown; unknown

```console
$ docker pull tomcat@sha256:feacd9f1343b383b43ed21987366fe5e4754023de3a30c46d39bc2787527dd85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6cb0b8f9dc50124781dd595b69e0b27be99a6d4494e9a958e2fe1d261760d3`

```dockerfile
```

-	Layers:
	-	`sha256:faf495db12e03772499a2f8bca8aefa59a4c901fe711a20d700efaaea5c6d395`  
		Last Modified: Sun, 09 Nov 2025 00:32:45 GMT  
		Size: 3.1 MB (3131693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6c29f038acdad34d05d980aeb08453b6b9404a9d75249146a9b0869c8bd6f78`  
		Last Modified: Sun, 09 Nov 2025 00:32:46 GMT  
		Size: 24.0 KB (24029 bytes)  
		MIME: application/vnd.in-toto+json
