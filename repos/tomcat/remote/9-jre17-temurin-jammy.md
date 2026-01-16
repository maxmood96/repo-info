## `tomcat:9-jre17-temurin-jammy`

```console
$ docker pull tomcat@sha256:696037219ba7d8cbc332c846d1f343f36fa7566117e5d7f77563f90c8685af4a
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
$ docker pull tomcat@sha256:6ac4771cf26d5964ed8f5e7aac078aa56d6a018106a9757925eaa2d2d6a69cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106750396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffae816f8a8239e9b1a094c315cf9e083ce4da39a359c774e15a0aa196a323bd`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:40 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 08 Dec 2025 21:13:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 08 Dec 2025 21:13:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 21:13:41 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 08 Dec 2025 21:13:41 GMT
WORKDIR /usr/local/tomcat
# Mon, 08 Dec 2025 21:13:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 21:13:41 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 21:13:41 GMT
ENV TOMCAT_MAJOR=9
# Mon, 08 Dec 2025 21:13:41 GMT
ENV TOMCAT_VERSION=9.0.113
# Mon, 08 Dec 2025 21:13:41 GMT
ENV TOMCAT_SHA512=1b8d9ba5c5e2ed2b4134a3fe6f206b3bb1184391e5c112ca7ea6a49ecadca63a7fc565c83caa610f0a8341988777870302a8162a84f0880af751531cdd4a2ee5
# Mon, 08 Dec 2025 21:13:41 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 08 Dec 2025 21:13:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:13:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Dec 2025 21:13:50 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:13:50 GMT
ENTRYPOINT []
# Mon, 08 Dec 2025 21:13:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e27b670a0f5423b1022e278f7a378f8f36d0cf41ecab6025d51111829df44f9`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 16.2 MB (16150369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c1638c21b85db624bcc6ff565cfad268dd384bdc524c47e9019c6b0e772a8`  
		Last Modified: Tue, 13 Jan 2026 00:55:13 GMT  
		Size: 47.1 MB (47055126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e292c31f90443285e61f951097b4b2213a7ebb112514ad9e4014e1ec1ee544a`  
		Last Modified: Tue, 13 Jan 2026 00:54:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e329fb7a0e143a03a99f87ec4d7acded1e81048017d71ea84307eb3c34a052`  
		Last Modified: Tue, 13 Jan 2026 00:54:37 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee32dabe5c1ac6979565947e6a962c95f0453ba9a346cd294fed63a634c5605`  
		Last Modified: Mon, 08 Dec 2025 21:14:05 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dab0a2692aae89e98a3386da32f5d6a7d623c2c267ed476621ccd514fb96d6`  
		Last Modified: Mon, 08 Dec 2025 21:14:06 GMT  
		Size: 13.8 MB (13775759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e50c0c1a923f3ecee66d871584b8b752f43b88cee59a58e6a2d47fc746a4d9`  
		Last Modified: Mon, 08 Dec 2025 21:14:05 GMT  
		Size: 229.7 KB (229703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:fd561939b95f9b47acfa52ebb74ae147fb1cd2b1f711dd41b4b31d4af6fb2799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72af871cb2ab096ab46484f421714e3410741d12bc400e8c279f4e67010c633c`

```dockerfile
```

-	Layers:
	-	`sha256:b00c2be8b8c842ecd6795944f9aedffdc50e045276b77119af93599d05064a8d`  
		Last Modified: Mon, 08 Dec 2025 21:40:54 GMT  
		Size: 3.9 MB (3937265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2437fe4c5789c54bc8e9cfd97b97bbe89c8618ce1cb3f07e58efe6d17fb978bc`  
		Last Modified: Mon, 08 Dec 2025 21:40:55 GMT  
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
		Last Modified: Thu, 15 Jan 2026 02:42:29 GMT  
		Size: 26.6 MB (26643402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3003eb8ae621f48a585bf3b6f7cd4fad0073079b8775587a9625d2bc9c40bb`  
		Last Modified: Thu, 15 Jan 2026 22:10:46 GMT  
		Size: 15.9 MB (15890620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7ded3af653e87557a2114de06b0205ba3084748e104b26c239502631609085`  
		Last Modified: Thu, 15 Jan 2026 22:11:00 GMT  
		Size: 44.7 MB (44723967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596c9dcdadc0cc7d2146b1339e0cd8f3d2a99d5d68482cf6caa42417cbf5dbc5`  
		Last Modified: Thu, 15 Jan 2026 22:10:43 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf8ae01510bc04c2d4b113e5d1d1f1d6ff5462d99e73c27e10411cad69ac781`  
		Last Modified: Thu, 15 Jan 2026 22:10:26 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4eb5efc38e69c964525475b2892e6348df0d12bcf2e64cf714a3113632e424b`  
		Last Modified: Thu, 15 Jan 2026 23:33:08 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6fdf5f407a856a624c52d966a9696dd02771951c701670d85ddc0abca957b3`  
		Last Modified: Thu, 15 Jan 2026 23:34:25 GMT  
		Size: 13.7 MB (13712551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ae407ddc47fd9b8c5411dd013ea4cdde8d7c059edeb14c56d97ab1bd5d6310`  
		Last Modified: Thu, 15 Jan 2026 23:34:23 GMT  
		Size: 202.3 KB (202327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
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
		Last Modified: Fri, 16 Jan 2026 00:45:59 GMT  
		Size: 21.3 KB (21336 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:403ac2ea840dc43107c08b38f27331b2cd546da5004aedbee0d2d5912971ca58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (104004587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061f810ab72d392d0b5bdeef9b43561c2ead2bb0074d22c6e38d2b14a7b2923b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:55 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 08 Dec 2025 20:16:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 08 Dec 2025 20:16:35 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:16:35 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 08 Dec 2025 20:16:36 GMT
WORKDIR /usr/local/tomcat
# Mon, 08 Dec 2025 20:16:36 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 20:16:36 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 20:16:36 GMT
ENV TOMCAT_MAJOR=9
# Mon, 08 Dec 2025 20:16:36 GMT
ENV TOMCAT_VERSION=9.0.113
# Mon, 08 Dec 2025 20:16:36 GMT
ENV TOMCAT_SHA512=1b8d9ba5c5e2ed2b4134a3fe6f206b3bb1184391e5c112ca7ea6a49ecadca63a7fc565c83caa610f0a8341988777870302a8162a84f0880af751531cdd4a2ee5
# Mon, 08 Dec 2025 20:19:21 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 08 Dec 2025 20:19:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:19:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Dec 2025 20:19:29 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 20:19:29 GMT
ENTRYPOINT []
# Mon, 08 Dec 2025 20:19:29 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9052a44c968831db26eb72b9c2aebcc7b2c9bb046a8897699cfa7d6306d511f`  
		Last Modified: Tue, 13 Jan 2026 00:55:17 GMT  
		Size: 16.1 MB (16066204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d51a12b423427685ca79a8479a5f226a65a132a9ed56a125790091c03fafe50`  
		Last Modified: Tue, 13 Jan 2026 01:04:45 GMT  
		Size: 46.5 MB (46538232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524de67f9a5c091df3fde0990e81a5e1bb632baaf32c8d5690de4678c88b58a7`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a36d8859c844388715a1c3ffe685f3359ee4053030286660c8510716411912`  
		Last Modified: Tue, 13 Jan 2026 00:54:56 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b222b262336069d3b56cf12098e34de035a67aa9d992cca0201566511a79b8a`  
		Last Modified: Mon, 08 Dec 2025 20:16:59 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8519393b7eb6ed5d66a505f512683e9f613276f7ed17ca9b2a847c496050777`  
		Last Modified: Mon, 08 Dec 2025 20:19:44 GMT  
		Size: 13.8 MB (13784949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464e6113c9363f03c24c1e67ac9bd7dc6914f5a5e360a85c1239bab7602027b1`  
		Last Modified: Mon, 08 Dec 2025 20:19:43 GMT  
		Size: 228.7 KB (228680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:7d6ffccbc633237e9c967e5a2ced91172711319022f5a31c153e6eb803ca7bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656498235082f958d6199e008672da17665bbbf4cff98e9126170a512f59dac0`

```dockerfile
```

-	Layers:
	-	`sha256:eb57e5499e826b22473e8b94064a79d1d25c18cca96e678706e2953257ab11d0`  
		Last Modified: Mon, 08 Dec 2025 21:41:06 GMT  
		Size: 3.9 MB (3936934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ad774cf84d9a33b19c25ed16c4ab6598125170229a346b0ee7aa3633ac25964`  
		Last Modified: Mon, 08 Dec 2025 21:41:07 GMT  
		Size: 21.4 KB (21364 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:22ca1d45f013e77a68bb9b7e8c9702ef4bb85cf2d3a73b6c33218e890fb3c36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (113017675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b41db81a64958794a769d454432adebaffde7ddaa9ad3aacf14b616719d3d8`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:11:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:11:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:23:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 08 Dec 2025 21:59:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 08 Dec 2025 21:59:51 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 21:59:51 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 08 Dec 2025 21:59:52 GMT
WORKDIR /usr/local/tomcat
# Mon, 08 Dec 2025 21:59:52 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 21:59:52 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 21:59:52 GMT
ENV TOMCAT_MAJOR=9
# Mon, 08 Dec 2025 21:59:52 GMT
ENV TOMCAT_VERSION=9.0.113
# Mon, 08 Dec 2025 21:59:52 GMT
ENV TOMCAT_SHA512=1b8d9ba5c5e2ed2b4134a3fe6f206b3bb1184391e5c112ca7ea6a49ecadca63a7fc565c83caa610f0a8341988777870302a8162a84f0880af751531cdd4a2ee5
# Mon, 08 Dec 2025 22:10:03 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 08 Dec 2025 22:10:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:10:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Dec 2025 22:10:14 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 22:10:14 GMT
ENTRYPOINT []
# Mon, 08 Dec 2025 22:10:14 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Tue, 13 Jan 2026 01:30:07 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0c14dcc61889e99acc58ba77c205e7f8b643ae497c00428e124e7fac3003f8`  
		Last Modified: Tue, 13 Jan 2026 03:00:24 GMT  
		Size: 17.6 MB (17623855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d656bd5882a45deea0d9eb0c02206d9c7d3a358c09e046b9ac674ae1eee16970`  
		Last Modified: Tue, 13 Jan 2026 19:19:17 GMT  
		Size: 46.9 MB (46881254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbc43a5e0a163b734145c98afb725844c0c0fd07bfbf155798bbea83b985801`  
		Last Modified: Tue, 13 Jan 2026 10:25:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7945bde3783bc5526d60cfb1f3860e10070b6c5b934a93aaa05b2ac95af589cd`  
		Last Modified: Tue, 13 Jan 2026 19:54:17 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e591fa385c50567bc12eca30aba9b1d917224fff4c4725bf0f42d6300f6f2e57`  
		Last Modified: Mon, 08 Dec 2025 22:00:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeca2fac75b318b05ec6f773d0f8f31b3a2abcae32ba30ac4667cced2b80a845`  
		Last Modified: Mon, 08 Dec 2025 22:10:41 GMT  
		Size: 13.8 MB (13803988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c66fea23929875aa2720a049ec3be06e1cd7ab50183f801d223954825d66379`  
		Last Modified: Mon, 08 Dec 2025 22:10:40 GMT  
		Size: 259.2 KB (259211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:ae70d99ea3b217e3316f7893e12d67217abf6f2cc5d6143439163fe83fb5d1af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3962621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517c0ac206455a7fe52e62db5416cd7a13fc76664291dc2f8b95f1982f09ffca`

```dockerfile
```

-	Layers:
	-	`sha256:667bb2232ecd0b1945044bb820e2677519a631acc3668471eade0fad1089dab8`  
		Last Modified: Tue, 09 Dec 2025 00:42:35 GMT  
		Size: 3.9 MB (3941353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e5f92578e82808d9b6288816dec0e3c99b35145b61342fe51bb77e1323d029`  
		Last Modified: Tue, 09 Dec 2025 00:42:36 GMT  
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
		Last Modified: Thu, 15 Jan 2026 23:54:14 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
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
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
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
