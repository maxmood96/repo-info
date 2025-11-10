## `tomcat:jre17`

```console
$ docker pull tomcat@sha256:1ee7210b930e35f822cffffe2f70ba905157285221b70d673525a73421cebf87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `tomcat:jre17` - linux; amd64

```console
$ docker pull tomcat@sha256:2d9c23dbece0ce5db5fc99b64734d1a0a3db783e4ce3a6f5ad27bd7f5e5b914c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108080445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f262d080dea9fc347376069f48f7efcaa0327e62ff6ff16aa023569c9b4fce74`
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
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:54:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:54:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:54:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:54:21 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='2876b04be597a748d5daaa5e1e73a32e9e84cb1b98c1760ff79fb3a53e032de7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:53 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 19:20:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 19:20:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:20:03 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 19:20:03 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 19:20:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:20:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:20:03 GMT
ENV TOMCAT_MAJOR=11
# Sat, 08 Nov 2025 19:20:03 GMT
ENV TOMCAT_VERSION=11.0.13
# Sat, 08 Nov 2025 19:20:03 GMT
ENV TOMCAT_SHA512=cc7cc21a671cb42d0b0f7381d2933c36415bfbe7419bf2561e8f88a5b75c2f5a738f3fcf7a1096c0cec3bac14b08e43c6f37c0983ee545672ffa2888cb8dd61a
# Sat, 08 Nov 2025 19:20:03 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 08 Nov 2025 19:20:09 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 19:20:10 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 08 Nov 2025 19:20:10 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 19:20:10 GMT
ENTRYPOINT []
# Sat, 08 Nov 2025 19:20:10 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840f58d04572d35b286c0f073abe58d11f4b666b253d07917fbcbc903bae9b53`  
		Last Modified: Sat, 08 Nov 2025 17:54:45 GMT  
		Size: 17.0 MB (16972346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21adf450df11bf039e13f106fe8efe0f5be7956753ae5b494ed19bf124484583`  
		Last Modified: Sat, 08 Nov 2025 17:59:24 GMT  
		Size: 47.1 MB (47055472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dccbbe6c416331d2f4161a51dcb3bab806053dc5f9060476ecbd06f910f6c2c`  
		Last Modified: Sat, 08 Nov 2025 17:59:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa181f75edbed18d79a5f756d0513f0f28378098da44e008b1f3c5209338621`  
		Last Modified: Sat, 08 Nov 2025 17:59:10 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c103a1480f7cbcf3467d5a21d64388189ebd2e0eb67459895655065f9cc2f86e`  
		Last Modified: Sat, 08 Nov 2025 19:20:21 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b00db9fcccd21e1914064cb9dbcc77d465c296ad3ed48e2bd5471d01d4d66c5`  
		Last Modified: Sat, 08 Nov 2025 19:20:23 GMT  
		Size: 14.1 MB (14102069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12294253d8f69c26677cb13698c017f0f818d041d15a398299a8fb7c53073f8f`  
		Last Modified: Sat, 08 Nov 2025 19:20:21 GMT  
		Size: 224.8 KB (224768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:cc2297c9ba14cc6f7cc47994454623694d75564ee9c57f2442ef397c74f981cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3373649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaedaabc85247f6ec0271678aa21030d46c281226dbacb3b18015a16fa8e9114`

```dockerfile
```

-	Layers:
	-	`sha256:c59802807b0be46108eb7e21748de6eb785f1ee57353a1023f597f1632f63852`  
		Last Modified: Sat, 08 Nov 2025 21:38:24 GMT  
		Size: 3.3 MB (3349606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190921dfb959db444246bcbbf0ee7b6ec96eeaa2b230989b2e71a18da293e671`  
		Last Modified: Sat, 08 Nov 2025 21:38:25 GMT  
		Size: 24.0 KB (24043 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:ee119f2030c86498b49e7abf0f319bdf9f9297d4885b73460bc6014d35cce43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102158703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880f785a4d0f0a1d315f2b1bd94b7c1457705d02f9db030136a0923e0afe4101`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:27 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:31 GMT
ADD file:1ccdd7fca45ec88ba0ddda07e5e5acb6b40ddcb3023e0cbc04ffffdf4e30fb0a in / 
# Wed, 01 Oct 2025 13:02:31 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:52:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:52:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:52:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:52:41 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:56:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='2876b04be597a748d5daaa5e1e73a32e9e84cb1b98c1760ff79fb3a53e032de7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:56:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:56:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:56:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 19:15:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 19:15:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:15:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 19:15:39 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 19:15:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:15:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:15:39 GMT
ENV TOMCAT_MAJOR=11
# Sat, 08 Nov 2025 19:15:39 GMT
ENV TOMCAT_VERSION=11.0.13
# Sat, 08 Nov 2025 19:15:39 GMT
ENV TOMCAT_SHA512=cc7cc21a671cb42d0b0f7381d2933c36415bfbe7419bf2561e8f88a5b75c2f5a738f3fcf7a1096c0cec3bac14b08e43c6f37c0983ee545672ffa2888cb8dd61a
# Sat, 08 Nov 2025 19:15:39 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 08 Nov 2025 19:15:47 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 19:15:47 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 08 Nov 2025 19:15:47 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 19:15:47 GMT
ENTRYPOINT []
# Sat, 08 Nov 2025 19:15:47 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4afa85c5883c0db62b02025c149edaaa237af5ba25ea48039e875a802d465ac7`  
		Last Modified: Wed, 01 Oct 2025 18:03:16 GMT  
		Size: 26.9 MB (26851732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877d48b3edf53ed48debe07364b6988a7d485b8dc62b8695068f22bc14f16bd2`  
		Last Modified: Sat, 08 Nov 2025 17:53:17 GMT  
		Size: 16.3 MB (16306496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c8be6cf32cdc62bb16f4a2bbeb66e07ce43a33f862ec9b5b205c6cd8aa8c83`  
		Last Modified: Sat, 08 Nov 2025 17:56:26 GMT  
		Size: 44.7 MB (44723955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90eaa8d14eddbded6195b5aabbc80b399b9eec045fbbda0769bfbccdf298ea69`  
		Last Modified: Sat, 08 Nov 2025 17:56:26 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f493a62b651f4d908ed89bd5cc208ca258994914f4d9f26ca62d391d666a1bd`  
		Last Modified: Sat, 08 Nov 2025 17:56:23 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6484181ec52dc8655b8cae0d4740dbd7e3025cb0b5ebd3f8143bdb52e5fe5279`  
		Last Modified: Sat, 08 Nov 2025 19:16:06 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158d743ae941607e247bae4267052e7140897ca4517de305c4531573854153f6`  
		Last Modified: Sat, 08 Nov 2025 19:16:09 GMT  
		Size: 14.1 MB (14077126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c996787873e4a0ac2f93a083f4a9977e878e59d320805f7cf36a51f4c409b894`  
		Last Modified: Sat, 08 Nov 2025 19:16:06 GMT  
		Size: 196.8 KB (196753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:8187e7bd483cfc7e81a1b96c5e7197befc72499913cf9bc26cec0c4f8098dabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3376246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:467dab449b29e1837d2e6e31af30fea796405844b3ee9eab94c0b6728431c49b`

```dockerfile
```

-	Layers:
	-	`sha256:5aa30a8a314411a73ecb40e1424cda4dc0239bfc28fdcc550ac0e60b6a945f5b`  
		Last Modified: Sat, 08 Nov 2025 21:38:29 GMT  
		Size: 3.4 MB (3352010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1057e35c9845200c6fe35a3bda392282f1d08dfd2a99d668903970f06faff7e7`  
		Last Modified: Sat, 08 Nov 2025 21:38:30 GMT  
		Size: 24.2 KB (24236 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:17f5b4bde958a27ff77d27a0d473f4ae1b7e06e92b9e330053be98ff96d1d51c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106721726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef979290b2bbbb0f6529f57b98b3c11164f5ef636da09e57e3d856934a3efe1`
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
# Sat, 08 Nov 2025 17:57:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:57:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:57:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:57:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:57:32 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='2876b04be597a748d5daaa5e1e73a32e9e84cb1b98c1760ff79fb3a53e032de7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:07 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:07 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 19:17:16 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 19:17:16 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:17:16 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 19:17:16 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 19:17:16 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:17:16 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 19:17:16 GMT
ENV TOMCAT_MAJOR=11
# Sat, 08 Nov 2025 19:17:16 GMT
ENV TOMCAT_VERSION=11.0.13
# Sat, 08 Nov 2025 19:17:16 GMT
ENV TOMCAT_SHA512=cc7cc21a671cb42d0b0f7381d2933c36415bfbe7419bf2561e8f88a5b75c2f5a738f3fcf7a1096c0cec3bac14b08e43c6f37c0983ee545672ffa2888cb8dd61a
# Sat, 08 Nov 2025 19:17:17 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 08 Nov 2025 19:17:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 19:17:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 08 Nov 2025 19:17:23 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 19:17:23 GMT
ENTRYPOINT []
# Sat, 08 Nov 2025 19:17:23 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f7654790c24728ffca0008db3fdf1df7faeb35641e71a0dbdd99dfb65ed007`  
		Last Modified: Sat, 08 Nov 2025 17:58:00 GMT  
		Size: 17.0 MB (16989385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b47f716a21d2fbccbe04c456ec89dfcae0addc11eb52d71d453b6026f50ca2`  
		Last Modified: Sat, 08 Nov 2025 17:58:30 GMT  
		Size: 46.5 MB (46538330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069b1a3861811ab7766831edb90530c9b8c97852684098d8ab5e99e54f0fd7b6`  
		Last Modified: Sat, 08 Nov 2025 17:58:26 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474c5f79d85356a571ab804c8b1b56a87b02be7ca619cdcf7714d9f416284494`  
		Last Modified: Sat, 08 Nov 2025 17:58:26 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3858069419efb9f5cc996c248ba82c79a636736d6c044aa568db3e7d853f3f8d`  
		Last Modified: Sat, 08 Nov 2025 19:17:38 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bd076953d1769fb981680a86e66c68bdb1d8a16fbd45d2e4d37bb6006f8561`  
		Last Modified: Sat, 08 Nov 2025 19:17:42 GMT  
		Size: 14.1 MB (14104146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a84dc31b6cbcbc5035f3c71680e479d9ad525a8b3c050dc9c77ea89841064d`  
		Last Modified: Sat, 08 Nov 2025 19:17:38 GMT  
		Size: 225.5 KB (225512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:de086cb1bc1f4571ff2c18ab8a05e98f68e6e3272524b508e5e9466b8e31b947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3374474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808e86c7842cd0eccfd020233c00853077c60931f678e64e979a08171c0f2d86`

```dockerfile
```

-	Layers:
	-	`sha256:5d3ddb8e5bb091a968375cd66fc34ab946cb43b238cfa839d65f8cc96dd7e102`  
		Last Modified: Sat, 08 Nov 2025 21:38:33 GMT  
		Size: 3.4 MB (3350174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d9db4f428b9a001a8f96e6ccfdfc878fd3a2c4576d0c2aaafbc577468d7dfb3`  
		Last Modified: Sat, 08 Nov 2025 21:38:34 GMT  
		Size: 24.3 KB (24300 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17` - linux; ppc64le

```console
$ docker pull tomcat@sha256:285396ab9095c2e7aea43fcece8dfac1b2e932d072e32e9777164d2361e3c245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114375528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07872d2f44185a961afe08f072521ae5ea37a5a9a0f053a673e2698b4b84affd`
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
# Sat, 08 Nov 2025 17:54:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:54:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:54:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:54:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:54:06 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 18:16:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='2876b04be597a748d5daaa5e1e73a32e9e84cb1b98c1760ff79fb3a53e032de7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:16:45 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:16:45 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:16:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 22:13:13 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 22:13:13 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 22:13:13 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 22:13:13 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 22:13:13 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 22:13:13 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 22:13:13 GMT
ENV TOMCAT_MAJOR=11
# Sat, 08 Nov 2025 22:13:13 GMT
ENV TOMCAT_VERSION=11.0.13
# Sat, 08 Nov 2025 22:13:13 GMT
ENV TOMCAT_SHA512=cc7cc21a671cb42d0b0f7381d2933c36415bfbe7419bf2561e8f88a5b75c2f5a738f3fcf7a1096c0cec3bac14b08e43c6f37c0983ee545672ffa2888cb8dd61a
# Sat, 08 Nov 2025 22:13:14 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 08 Nov 2025 22:13:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 22:13:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 08 Nov 2025 22:13:23 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 22:13:23 GMT
ENTRYPOINT []
# Sat, 08 Nov 2025 22:13:23 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c3c84c9145d6e39b87361420c42775001b0a5d2bff0b29876f0b582e69bdbf`  
		Last Modified: Sat, 08 Nov 2025 17:54:48 GMT  
		Size: 18.8 MB (18814703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812296efd252ea0a9d7e7a3ee32007f54b11c4bb9ba552314250c1eae4dd5013`  
		Last Modified: Sat, 08 Nov 2025 20:15:05 GMT  
		Size: 46.9 MB (46881514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7f5e676f326341c8a6c69a16f66354e9975c8f7939b3bae92e8c55f6915e42`  
		Last Modified: Sat, 08 Nov 2025 20:15:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266efcec659c4d999fb17aac47cf4ebcf8ea640573e4361352c68ef07fb47d4a`  
		Last Modified: Sat, 08 Nov 2025 20:15:01 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545de4859aace2e868900ab6cb806724de06167deb1200ff729b552281fa5b63`  
		Last Modified: Sat, 08 Nov 2025 22:14:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc92e25ffdfa67147c909e0fb3f878b16e9948cc3d28b2c8b814a2fb44a522d`  
		Last Modified: Sat, 08 Nov 2025 22:14:03 GMT  
		Size: 14.1 MB (14116552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33b3694e6526a2f89be9970c538d63be2fd22d3c85dc2bf7e38caae34f59373`  
		Last Modified: Sat, 08 Nov 2025 22:14:00 GMT  
		Size: 256.6 KB (256590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:2832af1115ebc4734cad4e7b6a298f272134a2140809a1bc69bdcb1da0f61a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3377881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ff367af54bba95dc00306fb08da623dce40ece1fcc8be13ad3c14bcaf4a7cb`

```dockerfile
```

-	Layers:
	-	`sha256:c6332920ad0fbdd9f4ac6f32bf94fd428fd967682f31c8baa060a8ecdc079d11`  
		Last Modified: Sun, 09 Nov 2025 00:32:00 GMT  
		Size: 3.4 MB (3353731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ed4d1974801185566167e0cc681f57ca4fb01b43f801c5e3ba0cb8994cf068b`  
		Last Modified: Sun, 09 Nov 2025 00:32:00 GMT  
		Size: 24.1 KB (24150 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17` - linux; riscv64

```console
$ docker pull tomcat@sha256:1124a48cbd38ff1c6ec6a1e99cc21e17ddbfc1c4dab0cf9446cb71486d06ac2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108952054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d157d9863f20752031671d2e9270ae7fe8c3d713dd64bf37ee79a83cf182ba6a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 01 Oct 2025 13:48:30 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:48:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:48:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:48:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:49:22 GMT
ADD file:857dc87fbafae31881cff8c69aed267a033f5df226dd351ee89de918ad5678ce in / 
# Wed, 01 Oct 2025 13:49:27 GMT
CMD ["/bin/bash"]
# Sun, 09 Nov 2025 21:55:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 09 Nov 2025 21:55:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 09 Nov 2025 21:55:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 09 Nov 2025 21:55:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Nov 2025 21:55:38 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sun, 09 Nov 2025 21:56:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='2876b04be597a748d5daaa5e1e73a32e9e84cb1b98c1760ff79fb3a53e032de7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 09 Nov 2025 21:56:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 09 Nov 2025 21:56:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 09 Nov 2025 21:56:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 05:20:01 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 05:20:01 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 05:20:01 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 05:20:02 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 05:20:02 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 05:20:02 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 05:20:02 GMT
ENV TOMCAT_MAJOR=11
# Mon, 10 Nov 2025 05:20:02 GMT
ENV TOMCAT_VERSION=11.0.13
# Mon, 10 Nov 2025 05:20:02 GMT
ENV TOMCAT_SHA512=cc7cc21a671cb42d0b0f7381d2933c36415bfbe7419bf2561e8f88a5b75c2f5a738f3fcf7a1096c0cec3bac14b08e43c6f37c0983ee545672ffa2888cb8dd61a
# Mon, 10 Nov 2025 05:20:04 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Nov 2025 05:20:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 05:20:57 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 05:20:57 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 05:20:57 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 05:20:57 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ff47a256ba51b80e9880bc96be4ac2f094c47e0fcd7eec71bab85787cfa54b8b`  
		Last Modified: Mon, 13 Oct 2025 04:10:18 GMT  
		Size: 31.0 MB (30951381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f168f32147322448b62f52061211b5e8d09d625fa544b55b31e5531645eb05a`  
		Last Modified: Sun, 09 Nov 2025 21:58:38 GMT  
		Size: 17.9 MB (17864334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2d63ca6878cebe69352e155f0c0dde77aaf8af87463492caf87f84316222a8`  
		Last Modified: Sun, 09 Nov 2025 21:58:40 GMT  
		Size: 45.6 MB (45620784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052a7df6e6d0d11ce44a19f792aed6e0a15f4988b25358f27d5c059c2bdc8467`  
		Last Modified: Sun, 09 Nov 2025 21:58:36 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed89424640b4de00fcb8f5ced65e816978682f9f945132e64ac67a19cd0c8dba`  
		Last Modified: Sun, 09 Nov 2025 21:58:36 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401429f5dae415b4d341666837ef74adf247debc6977a55b61ed74eb0100b25f`  
		Last Modified: Mon, 10 Nov 2025 05:22:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300cb45455ac567423b46b9aeee4a5576a080db339345b198903efaea70af9dd`  
		Last Modified: Mon, 10 Nov 2025 05:22:44 GMT  
		Size: 14.3 MB (14284190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf52d6db3fe1a9c0fec7533172bae2306f1d3dec75fd1957b2d20aa146c961f`  
		Last Modified: Mon, 10 Nov 2025 05:22:43 GMT  
		Size: 228.7 KB (228720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:bb9736e72b64b2fd97e295d4d16f9c9eb3e7766af7c279cb60ed16807b040644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3365882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f184821e44dde3be1be1cef7f0a89fb8edf97570cba5955b8c6d03f3b20a4e1`

```dockerfile
```

-	Layers:
	-	`sha256:a4454efe7b6bc19a1f388c7c7ea0d9041c93ce0386422d7454922a8f39d2c1cc`  
		Last Modified: Mon, 10 Nov 2025 06:31:07 GMT  
		Size: 3.3 MB (3341733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac183396b05fe9be15f2b96ac0d6625d40aac074ecd0323628137b8e1f4baa3d`  
		Last Modified: Mon, 10 Nov 2025 06:31:08 GMT  
		Size: 24.1 KB (24149 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:jre17` - linux; s390x

```console
$ docker pull tomcat@sha256:41ea987a91facb41e6679c1fc4cef1591a8ad5a6039e5d8089c913ed7b372e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105866174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638f59600a147ba3b8f524efb0dab3e264941ea2f54de8ef2e34362518e25ab1`
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
# Sat, 08 Nov 2025 17:53:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:53:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:53:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:53:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:53:22 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 18:05:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='2876b04be597a748d5daaa5e1e73a32e9e84cb1b98c1760ff79fb3a53e032de7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:05:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:05:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:05:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 20:20:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 08 Nov 2025 20:20:45 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 20:20:45 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 08 Nov 2025 20:20:45 GMT
WORKDIR /usr/local/tomcat
# Sat, 08 Nov 2025 20:20:45 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 20:20:45 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 08 Nov 2025 20:20:45 GMT
ENV TOMCAT_MAJOR=11
# Sat, 08 Nov 2025 20:20:45 GMT
ENV TOMCAT_VERSION=11.0.13
# Sat, 08 Nov 2025 20:20:45 GMT
ENV TOMCAT_SHA512=cc7cc21a671cb42d0b0f7381d2933c36415bfbe7419bf2561e8f88a5b75c2f5a738f3fcf7a1096c0cec3bac14b08e43c6f37c0983ee545672ffa2888cb8dd61a
# Sat, 08 Nov 2025 20:20:46 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 08 Nov 2025 20:20:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 20:20:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 08 Nov 2025 20:20:50 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 08 Nov 2025 20:20:50 GMT
ENTRYPOINT []
# Sat, 08 Nov 2025 20:20:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:67735b72a65d308a2c2c9505d0d6e8419b7f2654a16cbd56963d88e01202d507`  
		Last Modified: Wed, 01 Oct 2025 15:43:10 GMT  
		Size: 29.9 MB (29906151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c39bab3c353e0b04d65b92f35e87c17654f9b33dfd7b7ec5b40d471bbee22e9`  
		Last Modified: Sat, 08 Nov 2025 17:54:14 GMT  
		Size: 17.6 MB (17580941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f5a49fbc4ad7136fbfffe8c21ae3955fab215081136dd4b8de40bd15c36ff1`  
		Last Modified: Sat, 08 Nov 2025 18:05:56 GMT  
		Size: 44.0 MB (44030958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22744bc2b0badcffc7aa2c5ca756f28f0dd3173ee36bcda319a700e2e252c26d`  
		Last Modified: Sat, 08 Nov 2025 18:05:53 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac04415193a2878e3431345909a44b5f80f4c022b91f39dd68b9ef8bc80695dc`  
		Last Modified: Sat, 08 Nov 2025 18:05:53 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fcc204de19ddf99df82d58f8ecd5fb5587cd2829d706880d5de7b5fd9f9d82`  
		Last Modified: Sat, 08 Nov 2025 20:21:11 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5320d935d3a8e682059c8c9263be21ac6ff6c960f23bf1323011ceb92fac2e`  
		Last Modified: Sat, 08 Nov 2025 20:21:12 GMT  
		Size: 14.1 MB (14112800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3840e8f0121907e8361ebcb5bd41756fa47aa79054863629dd14447c4a8d03`  
		Last Modified: Sat, 08 Nov 2025 20:21:11 GMT  
		Size: 232.7 KB (232680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:jre17` - unknown; unknown

```console
$ docker pull tomcat@sha256:fc5adb4d138f8988a63431dc886bba663756e398f5e5a84b1cb10606cdd01e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3375849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c8cb1133fe0e0c7e22934a490203b4fd320acec102ee4d3db8ee853f19e81e`

```dockerfile
```

-	Layers:
	-	`sha256:fbdb780024c15838bcdddb4cdc87d3473f8145385cf46bf8f767e037fa03aea6`  
		Last Modified: Sat, 08 Nov 2025 21:38:45 GMT  
		Size: 3.4 MB (3351805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:075318875a13310f857788a787b0b6ef2ea4ba3429aef2ee1487082c20989269`  
		Last Modified: Sat, 08 Nov 2025 21:38:46 GMT  
		Size: 24.0 KB (24044 bytes)  
		MIME: application/vnd.in-toto+json
