## `tomcat:9-jre17-temurin-jammy`

```console
$ docker pull tomcat@sha256:ffc79bd1c03ba00d30f471790d96aa6354e14432bf9fb7117c7345d3d63c7736
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

### `tomcat:9-jre17-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:507e856d9057379122c7e49a9ee435c99a2a7c81743957642ce8dde27dc4404c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106747367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da1e93748cf0d356341a72d6c29f9f97d4837591da80b1e299fdfb60c100721`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:46 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:46 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 02:28:26 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Jan 2026 02:28:26 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:28:26 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 16 Jan 2026 02:28:28 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Jan 2026 02:28:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jan 2026 02:28:28 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jan 2026 02:28:28 GMT
ENV TOMCAT_MAJOR=9
# Fri, 16 Jan 2026 02:28:28 GMT
ENV TOMCAT_VERSION=9.0.113
# Fri, 16 Jan 2026 02:28:28 GMT
ENV TOMCAT_SHA512=1b8d9ba5c5e2ed2b4134a3fe6f206b3bb1184391e5c112ca7ea6a49ecadca63a7fc565c83caa610f0a8341988777870302a8162a84f0880af751531cdd4a2ee5
# Fri, 16 Jan 2026 02:28:29 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 16 Jan 2026 02:28:36 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 02:28:36 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 16 Jan 2026 02:28:36 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 16 Jan 2026 02:28:36 GMT
ENTRYPOINT []
# Fri, 16 Jan 2026 02:28:36 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8770a7ccbf824857f9a328739d1ddfec21c04a1b7423007c0a74c8ab500e3675`  
		Last Modified: Thu, 15 Jan 2026 22:20:01 GMT  
		Size: 16.1 MB (16147435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5de6e8045fe0102a83fbca815f435fd81296a7937cdeb04409eeec845a3502`  
		Last Modified: Thu, 15 Jan 2026 22:20:11 GMT  
		Size: 47.1 MB (47055148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd012e01f9d2afd797ecf20b406260375e0fe120b00a6401bba84a92fc3968f3`  
		Last Modified: Thu, 15 Jan 2026 22:20:00 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b4b65fc380fc87df9d7a19c5abf67e22e913f6f0b56b870b1ee5ca46f5cdf5`  
		Last Modified: Thu, 15 Jan 2026 22:20:00 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fcb1d5c94665360bfb5704f975db6096b93f1c193fb3547c18d5c5b2d6c5d9`  
		Last Modified: Fri, 16 Jan 2026 02:28:57 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b0ea4f7546ed714fbabaefe0d662a2152a2b608b2db53ab8378e6d5b338b06`  
		Last Modified: Fri, 16 Jan 2026 02:28:51 GMT  
		Size: 13.8 MB (13775777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e80128b1c85a51791df9b7e5c6eb895423211a0eabff9e31c3f855672471b7f`  
		Last Modified: Fri, 16 Jan 2026 02:28:50 GMT  
		Size: 229.7 KB (229700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:e95b2c394a5c29e1dbe9de488960d08a31a88a1d1a6f7ea2afba2d0c8f4700f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66d763863d5711f2b342c754306698eee50b62b4c82c8a8ecfeeacb6dd4a332`

```dockerfile
```

-	Layers:
	-	`sha256:c8825fcc1ad5ef5f86e9ddff9caf836bef13e562a5511ef558e22ccafc43abaa`  
		Last Modified: Fri, 16 Jan 2026 02:28:45 GMT  
		Size: 3.9 MB (3937277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a532acaa827ea53f6c9eabc76ba1f992096043ec8c260857edcabeedfe51cb29`  
		Last Modified: Fri, 16 Jan 2026 02:28:44 GMT  
		Size: 21.2 KB (21216 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:8fab02120e3fce90c527f8df616b1ce23ed61e24ed1904858bd11834d20f2f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101175508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4b536a75c2f6b8ef3955105f851f8cafb6599eb4ca5926a80482a436e8ac2e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Jan 2026 07:02:38 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:02:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:02:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:02:38 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:02:42 GMT
ADD file:c6e8dc9cf610f17d4ed912b48dc43aef299146d67e62f2248ccd0e2cca210a77 in / 
# Fri, 09 Jan 2026 07:02:42 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:10:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:10:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:10:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:10:21 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:10:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:10:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:10:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:10:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 23:32:47 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 15 Jan 2026 23:32:47 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:32:47 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 15 Jan 2026 23:32:47 GMT
WORKDIR /usr/local/tomcat
# Thu, 15 Jan 2026 23:32:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 15 Jan 2026 23:32:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 15 Jan 2026 23:32:47 GMT
ENV TOMCAT_MAJOR=9
# Thu, 15 Jan 2026 23:32:47 GMT
ENV TOMCAT_VERSION=9.0.113
# Thu, 15 Jan 2026 23:32:47 GMT
ENV TOMCAT_SHA512=1b8d9ba5c5e2ed2b4134a3fe6f206b3bb1184391e5c112ca7ea6a49ecadca63a7fc565c83caa610f0a8341988777870302a8162a84f0880af751531cdd4a2ee5
# Thu, 15 Jan 2026 23:34:02 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 15 Jan 2026 23:34:10 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:34:11 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 15 Jan 2026 23:34:11 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 15 Jan 2026 23:34:11 GMT
ENTRYPOINT []
# Thu, 15 Jan 2026 23:34:11 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:83d1a597d0ed11bf60c1ab8ef65516448b87de3790f14ee8336174b7f9a56d82`  
		Last Modified: Fri, 09 Jan 2026 07:36:09 GMT  
		Size: 26.6 MB (26643402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3003eb8ae621f48a585bf3b6f7cd4fad0073079b8775587a9625d2bc9c40bb`  
		Last Modified: Thu, 15 Jan 2026 22:10:46 GMT  
		Size: 15.9 MB (15890620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7ded3af653e87557a2114de06b0205ba3084748e104b26c239502631609085`  
		Last Modified: Thu, 15 Jan 2026 22:10:38 GMT  
		Size: 44.7 MB (44723967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596c9dcdadc0cc7d2146b1339e0cd8f3d2a99d5d68482cf6caa42417cbf5dbc5`  
		Last Modified: Thu, 15 Jan 2026 22:10:37 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf8ae01510bc04c2d4b113e5d1d1f1d6ff5462d99e73c27e10411cad69ac781`  
		Last Modified: Thu, 15 Jan 2026 22:10:16 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4eb5efc38e69c964525475b2892e6348df0d12bcf2e64cf714a3113632e424b`  
		Last Modified: Thu, 15 Jan 2026 23:33:08 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6fdf5f407a856a624c52d966a9696dd02771951c701670d85ddc0abca957b3`  
		Last Modified: Thu, 15 Jan 2026 23:34:25 GMT  
		Size: 13.7 MB (13712551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ae407ddc47fd9b8c5411dd013ea4cdde8d7c059edeb14c56d97ab1bd5d6310`  
		Last Modified: Thu, 15 Jan 2026 23:34:18 GMT  
		Size: 202.3 KB (202327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:c0e835c093f9d9debcf47647c06ba81c247ab7e65b8f6162a0cb40ef3be25310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3960948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a1c19b44bafb15150c10581321432b04f4e4906fc462e5b460ef00bb1657f1`

```dockerfile
```

-	Layers:
	-	`sha256:0a32e8070611bdaf0b9a5ae0ee21b3a3fa8f0804fcc05893e257b0943a3b6a5f`  
		Last Modified: Fri, 16 Jan 2026 00:45:58 GMT  
		Size: 3.9 MB (3939612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b443856150d50d3e486b8b758402853b44bc4a06ee4bc6be49ccb53ffc504535`  
		Last Modified: Thu, 15 Jan 2026 23:34:18 GMT  
		Size: 21.3 KB (21336 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:b61e69d3da4c7c7ab0228dd64065dac194a750924e8c2e96ad7d9ef064a317d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (104003659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f39b394837192765b895ad3eb46cebf13cc87815558d25257550d1280db620e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:49 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:19:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:19:53 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:19:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:19:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 02:43:11 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Jan 2026 02:43:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:43:11 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 16 Jan 2026 02:43:11 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Jan 2026 02:43:11 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jan 2026 02:43:11 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jan 2026 02:43:11 GMT
ENV TOMCAT_MAJOR=9
# Fri, 16 Jan 2026 02:43:11 GMT
ENV TOMCAT_VERSION=9.0.113
# Fri, 16 Jan 2026 02:43:11 GMT
ENV TOMCAT_SHA512=1b8d9ba5c5e2ed2b4134a3fe6f206b3bb1184391e5c112ca7ea6a49ecadca63a7fc565c83caa610f0a8341988777870302a8162a84f0880af751531cdd4a2ee5
# Fri, 16 Jan 2026 02:45:54 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 16 Jan 2026 02:46:01 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 02:46:02 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 16 Jan 2026 02:46:02 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 16 Jan 2026 02:46:02 GMT
ENTRYPOINT []
# Fri, 16 Jan 2026 02:46:02 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fc3ef6de679ecac0a74cc044dd73825b9e6daa54ab0904bc8e9b9e898d5bdd`  
		Last Modified: Thu, 15 Jan 2026 22:20:05 GMT  
		Size: 16.1 MB (16065656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d903927893f88ea36a0f1ae2165c1cbabff6244e11daf33512f44c12631acd`  
		Last Modified: Thu, 15 Jan 2026 22:20:17 GMT  
		Size: 46.5 MB (46538233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05322d833bff6a327f4cb5734a53c8ecd0811c295b8d670e977218a9a12d8906`  
		Last Modified: Thu, 15 Jan 2026 22:20:14 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef01e65ce9e940b87d06c11af62f1cff2016c991c02e0b659ac1826a2466cbd5`  
		Last Modified: Thu, 15 Jan 2026 22:19:45 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b858e460fef1ce81b9626dd28ac89a684319bbca9d338289e2da00382973b0`  
		Last Modified: Fri, 16 Jan 2026 02:43:34 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cb0a63b200f4623042ffa6be037fed2fb93f39398f3ea449780afd64d00f2c`  
		Last Modified: Fri, 16 Jan 2026 02:46:10 GMT  
		Size: 13.8 MB (13785028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d3093348649c189f9ccca150a5b53592c9e1b33bb3b2c2a5a03378e77d0095`  
		Last Modified: Fri, 16 Jan 2026 02:46:15 GMT  
		Size: 228.6 KB (228600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:436c5b67f38efd7cfb870bcc28673fff3c2c23a0b86b4761eb58e87ba766c361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff92408f6843ba0f4b4a7c4ef7a792c7b7bfc72988548348d44bc765f96d71fb`

```dockerfile
```

-	Layers:
	-	`sha256:5727febee78c3685eec27e0f40e22b9915748ee815c941bf111270626835f853`  
		Last Modified: Fri, 16 Jan 2026 02:46:10 GMT  
		Size: 3.9 MB (3936946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40b0a2308253ba7bc068bc4e8b21a8ad2802b41c94808b58e38473b6a7bc612`  
		Last Modified: Fri, 16 Jan 2026 03:44:28 GMT  
		Size: 21.4 KB (21363 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:aa7e67b848e82594db7c0915271a5fb3f560ddfffa5e99d959379a107899567f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (113013191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c092a4065353bf328b57830d43acbca72be51efe1cab79e048f44dfb1ecea64e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:09:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:09:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:09:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:09:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:09:00 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:16:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:16:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:16:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:16:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 04:54:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Jan 2026 04:54:54 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 04:54:54 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 16 Jan 2026 04:54:55 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Jan 2026 04:54:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jan 2026 04:54:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jan 2026 04:54:55 GMT
ENV TOMCAT_MAJOR=9
# Fri, 16 Jan 2026 04:54:55 GMT
ENV TOMCAT_VERSION=9.0.113
# Fri, 16 Jan 2026 04:54:55 GMT
ENV TOMCAT_SHA512=1b8d9ba5c5e2ed2b4134a3fe6f206b3bb1184391e5c112ca7ea6a49ecadca63a7fc565c83caa610f0a8341988777870302a8162a84f0880af751531cdd4a2ee5
# Fri, 16 Jan 2026 05:02:42 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 16 Jan 2026 05:02:50 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 05:02:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 16 Jan 2026 05:02:51 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 16 Jan 2026 05:02:51 GMT
ENTRYPOINT []
# Fri, 16 Jan 2026 05:02:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183556a79e45cd164d41dfffcf9da5a4846b19eb406b8300431457b5010ff3f3`  
		Last Modified: Thu, 15 Jan 2026 22:09:41 GMT  
		Size: 17.6 MB (17619200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004ca264798509a08ea6ccee410a564b50a0eb5a42f1e58216b34a0c846751eb`  
		Last Modified: Thu, 15 Jan 2026 22:17:27 GMT  
		Size: 46.9 MB (46881201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeae30e596f1d1d565a863521696c50833d9594367b6717a150b7660b7f6f7d9`  
		Last Modified: Thu, 15 Jan 2026 22:17:22 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a011aa1930859a4407f64ffbb4fddcba4751ca856311b708bf6236c1d809dea`  
		Last Modified: Thu, 15 Jan 2026 22:17:22 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6654d1e62b040757949f746583e2feb21a098f86f5f0fff169feec40258be8b0`  
		Last Modified: Fri, 16 Jan 2026 04:55:34 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb9c7245ddd479776587a2f023b95286eeef5c6c935c64df5e49a3d9ace3277`  
		Last Modified: Fri, 16 Jan 2026 05:03:24 GMT  
		Size: 13.8 MB (13804122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43022a02eb0a070349d60c005df70a96aeba2b946221589e129cc54634c324c6`  
		Last Modified: Fri, 16 Jan 2026 05:03:22 GMT  
		Size: 259.1 KB (259066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:0cd5cfa90f72235da038cf7f3d3501b7f6c267beae520d204a4535f796481434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3962633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011e6eb6ea3b7f1fa3c6487a9d06c977e83293dd3c9b9ed0792a1ac7eecf003c`

```dockerfile
```

-	Layers:
	-	`sha256:dc802e0bcb70a9fe2153bfa266c8978813649c4e391a041c5eb9c3d336d23a49`  
		Last Modified: Fri, 16 Jan 2026 05:03:16 GMT  
		Size: 3.9 MB (3941365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f404a07ca349525650d290afe74e082cf3fd77097cdac4cbc115c9f730f1ae0b`  
		Last Modified: Fri, 16 Jan 2026 05:03:13 GMT  
		Size: 21.3 KB (21268 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:1133f5f217949a72ddea5bedad7c2cff6bde0b69ca76c31fd0b9154b76732bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102187086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70f84200d37f684b86d3fcb729c549035e62d867ba97d00ab7e11268a6fcce2`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:07:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:07:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:07:47 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 23:53:52 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 15 Jan 2026 23:53:52 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:53:52 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 15 Jan 2026 23:53:52 GMT
WORKDIR /usr/local/tomcat
# Thu, 15 Jan 2026 23:53:52 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 15 Jan 2026 23:53:52 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 15 Jan 2026 23:53:52 GMT
ENV TOMCAT_MAJOR=9
# Thu, 15 Jan 2026 23:53:52 GMT
ENV TOMCAT_VERSION=9.0.113
# Thu, 15 Jan 2026 23:53:52 GMT
ENV TOMCAT_SHA512=1b8d9ba5c5e2ed2b4134a3fe6f206b3bb1184391e5c112ca7ea6a49ecadca63a7fc565c83caa610f0a8341988777870302a8162a84f0880af751531cdd4a2ee5
# Thu, 15 Jan 2026 23:58:03 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 15 Jan 2026 23:58:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:58:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 15 Jan 2026 23:58:06 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 15 Jan 2026 23:58:06 GMT
ENTRYPOINT []
# Thu, 15 Jan 2026 23:58:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Thu, 15 Jan 2026 21:43:58 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676637e8890c4f623a4c39093b5a6b7d703e86468ce113096f2c9bc78c182e31`  
		Last Modified: Thu, 15 Jan 2026 22:08:18 GMT  
		Size: 16.1 MB (16146361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e9b748536a4b54bbeaed6e8579bac2a16c4986534a31b46a7f8d531c675524`  
		Last Modified: Thu, 15 Jan 2026 22:09:29 GMT  
		Size: 44.0 MB (44030721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee70f10bc792cf46fb84c159936483edcc2c3f8c468360bd38af3094333059b`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f076689551b9f17e248144f44944cc2f57617fb25e5b05a98f00722413e6bd`  
		Last Modified: Thu, 15 Jan 2026 22:09:26 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e56cc3693fcbab42a35df7dabb06ea16d604606aabd3440b377228480846cc1`  
		Last Modified: Thu, 15 Jan 2026 23:54:10 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f2f45d5d9869ea49d0fb1e860a72445e93554902f1f4c78a607a9af94caaba`  
		Last Modified: Thu, 15 Jan 2026 23:58:27 GMT  
		Size: 13.8 MB (13773484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe20d0645818f027b1438eb1d8019d7ae32374560a454d5b90263897da232544`  
		Last Modified: Thu, 15 Jan 2026 23:58:26 GMT  
		Size: 230.7 KB (230740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:f7b0e207431f29247b037d2699c20cdd46f28662787da026ce0b8b4f016ec02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3960083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e0580b248d2944fc2e5515b42ec54a4fdf7853dc990f51b3b39ddd38726977`

```dockerfile
```

-	Layers:
	-	`sha256:3c61e9869981a418db8a36dcc82f68d8175a6ec4efebb8e59ad2fac8053b85b7`  
		Last Modified: Fri, 16 Jan 2026 00:46:12 GMT  
		Size: 3.9 MB (3938868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09da9511ad34343a453d2da7e42891e75ecd665cd34a69ff4e2521c9ec595fb6`  
		Last Modified: Fri, 16 Jan 2026 00:46:13 GMT  
		Size: 21.2 KB (21215 bytes)  
		MIME: application/vnd.in-toto+json
