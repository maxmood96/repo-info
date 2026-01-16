## `tomcat:10-jre17-temurin-jammy`

```console
$ docker pull tomcat@sha256:eb26900714d625e62eacf4f2bcbed9b81d36c37e4a36ae843c61d4040f502b98
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

### `tomcat:10-jre17-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:794fd90771d2967ce918581a3cd708286ea05a6dab7fa6019fbab90056f963c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107253374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0668108a02f4919aeb9608456a3002dab4e60f491dd8301b7b916ef452ae36`
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
# Mon, 08 Dec 2025 22:18:08 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 08 Dec 2025 22:18:08 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:18:08 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 08 Dec 2025 22:18:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 08 Dec 2025 22:18:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 22:18:08 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 22:18:08 GMT
ENV TOMCAT_MAJOR=10
# Mon, 08 Dec 2025 22:18:08 GMT
ENV TOMCAT_VERSION=10.1.50
# Mon, 08 Dec 2025 22:18:08 GMT
ENV TOMCAT_SHA512=c7702b0304257d80dc5bd615005fe037bd0c518e3fe77d22a58e5313fe53e6af6f4a2cf00790e3e9a669d1ae5470fb11177c9ef42f8c846d2b20dfac93e2d551
# Mon, 08 Dec 2025 22:18:08 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 08 Dec 2025 22:18:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:18:15 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Dec 2025 22:18:15 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 22:18:15 GMT
ENTRYPOINT []
# Mon, 08 Dec 2025 22:18:15 GMT
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
	-	`sha256:0a15d452bf62caa7aabf3740a7d021fa50df0e607ed68dd7b504d6404bde7a4f`  
		Last Modified: Mon, 08 Dec 2025 22:18:27 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c04a146d6e7d4e755a7a00266069ef1a95d04f7269cba82ea60f548ff133690`  
		Last Modified: Mon, 08 Dec 2025 22:18:29 GMT  
		Size: 14.3 MB (14278748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64744fc4f71bc584d057ea8ea4e48bab7dc582f2bd49a708ec5347d5f5e4a902`  
		Last Modified: Mon, 08 Dec 2025 22:18:27 GMT  
		Size: 229.7 KB (229692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:8c0156cdbb807feb7799b49a2112ca193b6b04ef8df76f4e994cca186059f167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f693f4009e48ba6e75d13313f910a39dac22bb0f0251fce6aa21b483179577f9`

```dockerfile
```

-	Layers:
	-	`sha256:76e30157e0035581e446297738699417709ecbc2d5e0d3fe8c3618980748d416`  
		Last Modified: Tue, 09 Dec 2025 00:35:27 GMT  
		Size: 3.9 MB (3939935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d8190e3021bbb5244c2856cc5d917a96c6a5aa32c54d775b1b66b64dca24ea1`  
		Last Modified: Tue, 09 Dec 2025 00:35:28 GMT  
		Size: 21.2 KB (21224 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre17-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:85bac5da81110ef4e46fdba7ab74cf9fbc3a52304bb555d8a4b2514849e7124d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101717456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6858eb7fc141b8847c3dd605b31ce9492c172abbfbc73ecef0a5294067c4ccb0`
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
# Thu, 15 Jan 2026 23:33:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 15 Jan 2026 23:33:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:33:03 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 15 Jan 2026 23:33:04 GMT
WORKDIR /usr/local/tomcat
# Thu, 15 Jan 2026 23:33:04 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 15 Jan 2026 23:33:04 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 15 Jan 2026 23:33:04 GMT
ENV TOMCAT_MAJOR=10
# Thu, 15 Jan 2026 23:33:04 GMT
ENV TOMCAT_VERSION=10.1.50
# Thu, 15 Jan 2026 23:33:04 GMT
ENV TOMCAT_SHA512=c7702b0304257d80dc5bd615005fe037bd0c518e3fe77d22a58e5313fe53e6af6f4a2cf00790e3e9a669d1ae5470fb11177c9ef42f8c846d2b20dfac93e2d551
# Thu, 15 Jan 2026 23:33:04 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 15 Jan 2026 23:33:11 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:33:12 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 15 Jan 2026 23:33:12 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 15 Jan 2026 23:33:12 GMT
ENTRYPOINT []
# Thu, 15 Jan 2026 23:33:12 GMT
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
	-	`sha256:383ee4e15feb5e64f4b4a6afeba268ab383ccbb0a29a823d356d5ed959d92183`  
		Last Modified: Thu, 15 Jan 2026 23:33:26 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b06e3c2590578fcb74d6ecf23e4a387e42ddeab32f6434d52d043743f05e77`  
		Last Modified: Thu, 15 Jan 2026 23:33:28 GMT  
		Size: 14.3 MB (14254470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e26c08b4d206bd8fb239c4032ca7eda637dfd00430af36dfd19175e7c3cefa`  
		Last Modified: Thu, 15 Jan 2026 23:33:26 GMT  
		Size: 202.4 KB (202356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:09757d4f63af450699622ce79f03b97eca1ca61150ca0ae8027dac15468a698a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3963626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84b3c6a5726f1556effde33b55465d61cc8c57ddf0cc2cf1d47df9d057904cb`

```dockerfile
```

-	Layers:
	-	`sha256:a16d2e2494c0d08ae030cbaa0bc04f7a78925098ca83dd585be0a76198caad18`  
		Last Modified: Fri, 16 Jan 2026 00:33:36 GMT  
		Size: 3.9 MB (3942282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67146e928357d274bb9fbd09e9b92b2260716c26d26ad2489b720e31df5598d8`  
		Last Modified: Fri, 16 Jan 2026 00:33:37 GMT  
		Size: 21.3 KB (21344 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre17-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:910f6b98963aa707c3390e7495bf67edb6a55e703c0ae2578b4c3ff6627b484d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104501370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7156a9af580ddc01d8e81c4aef6c85d7a555e72b0ae6c82de7fcb5e97949ed4`
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
# Mon, 08 Dec 2025 22:17:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 08 Dec 2025 22:17:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:17:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 08 Dec 2025 22:17:39 GMT
WORKDIR /usr/local/tomcat
# Mon, 08 Dec 2025 22:17:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 22:17:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 22:17:39 GMT
ENV TOMCAT_MAJOR=10
# Mon, 08 Dec 2025 22:17:39 GMT
ENV TOMCAT_VERSION=10.1.50
# Mon, 08 Dec 2025 22:17:39 GMT
ENV TOMCAT_SHA512=c7702b0304257d80dc5bd615005fe037bd0c518e3fe77d22a58e5313fe53e6af6f4a2cf00790e3e9a669d1ae5470fb11177c9ef42f8c846d2b20dfac93e2d551
# Mon, 08 Dec 2025 22:17:39 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 08 Dec 2025 22:17:47 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:17:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Dec 2025 22:17:48 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 22:17:48 GMT
ENTRYPOINT []
# Mon, 08 Dec 2025 22:17:48 GMT
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
	-	`sha256:213ea06acfef5d0e60cce6d4463eededc93e64807fa7c2e247fd5c61d8be6cfb`  
		Last Modified: Mon, 08 Dec 2025 22:18:02 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0c957c0341d4c1effc1acbcb23b4d6ad90b2fcc5a4320e3285efc6d6d2da43`  
		Last Modified: Mon, 08 Dec 2025 22:18:05 GMT  
		Size: 14.3 MB (14281753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf5ca90a1241c9d737b6ff3626c571ee8980de4c7b2a29fa63a901ab731982d`  
		Last Modified: Mon, 08 Dec 2025 22:18:05 GMT  
		Size: 228.7 KB (228658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:114b90995a4ef81ec378aaa4dd683f1e318597d7176d03b66fe5cd70c99819d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3960976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51af0fde0577726fd05d7d3d547ff92d27bec2abafed6055354a7193319d0e60`

```dockerfile
```

-	Layers:
	-	`sha256:75f5686ab8265c8580e7fe295f7dc508c4994b289b095002cd3ed7ea27f3dce1`  
		Last Modified: Tue, 09 Dec 2025 00:35:39 GMT  
		Size: 3.9 MB (3939604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56dd230eecfc5775c3384cf116ec1e389d507d81ffa06ae090e01ba67b237d9e`  
		Last Modified: Tue, 09 Dec 2025 00:35:40 GMT  
		Size: 21.4 KB (21372 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre17-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:e469a633b52f0b87ab5d46df1fe7d6b266249a5d8ae1f5e59e693d68b1b8b1b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113507407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7887692cca10fccedbec645576ba08ded7c958c7c27d9f170495bbde4a8f89a`
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
ENV TOMCAT_MAJOR=10
# Mon, 08 Dec 2025 21:59:52 GMT
ENV TOMCAT_VERSION=10.1.50
# Mon, 08 Dec 2025 21:59:52 GMT
ENV TOMCAT_SHA512=c7702b0304257d80dc5bd615005fe037bd0c518e3fe77d22a58e5313fe53e6af6f4a2cf00790e3e9a669d1ae5470fb11177c9ef42f8c846d2b20dfac93e2d551
# Mon, 08 Dec 2025 22:20:38 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 08 Dec 2025 22:20:47 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:20:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Dec 2025 22:20:49 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 22:20:49 GMT
ENTRYPOINT []
# Mon, 08 Dec 2025 22:20:49 GMT
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
	-	`sha256:e0facdc437897febeb1c479ece63d7e346482dc37d0749ca6adf82166ac33b6d`  
		Last Modified: Mon, 08 Dec 2025 22:21:17 GMT  
		Size: 14.3 MB (14293723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c75e5e421e3e0b6516946ee29dd634167712c5c2eb5630c9eeb207082ffddf0`  
		Last Modified: Mon, 08 Dec 2025 22:21:16 GMT  
		Size: 259.2 KB (259208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:5f2e6e8013e637496c7676c3367fcbb618d12df1c93df4b5062f7220b36871d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502fbc4268770bda1042c896dd1f08456e1645301a2c2bc4029b4fa6d74b73ac`

```dockerfile
```

-	Layers:
	-	`sha256:f3df0c49610da3ff7b370146d0ecd6c08361da873d27929ed98ccca280353691`  
		Last Modified: Tue, 09 Dec 2025 00:35:44 GMT  
		Size: 3.9 MB (3944023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d9de10064476dcfe8ea65ece48d5aaa942b884c9ebdbd5beebc2cd630fe0374`  
		Last Modified: Tue, 09 Dec 2025 00:35:45 GMT  
		Size: 21.3 KB (21276 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:10-jre17-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:305567b26830d517a2aa28f053d7f4f4a03d6f6010055149e232d9e6ff9bc43b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102697273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03e2dd21c76f21c437eaa0030f847684651f19ff2caab5917e227b3af5db4bf`
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
ENV TOMCAT_MAJOR=10
# Thu, 15 Jan 2026 23:53:52 GMT
ENV TOMCAT_VERSION=10.1.50
# Thu, 15 Jan 2026 23:53:52 GMT
ENV TOMCAT_SHA512=c7702b0304257d80dc5bd615005fe037bd0c518e3fe77d22a58e5313fe53e6af6f4a2cf00790e3e9a669d1ae5470fb11177c9ef42f8c846d2b20dfac93e2d551
# Thu, 15 Jan 2026 23:55:51 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 15 Jan 2026 23:55:54 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:55:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 15 Jan 2026 23:55:54 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 15 Jan 2026 23:55:54 GMT
ENTRYPOINT []
# Thu, 15 Jan 2026 23:55:54 GMT
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
	-	`sha256:1a75a2557b5ceabb06f7b3e5f8821ad2a313ff44d8f6a3852866b02f65082685`  
		Last Modified: Thu, 15 Jan 2026 23:56:15 GMT  
		Size: 14.3 MB (14283679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed336d7aefbcfdf633665115f60a554f824e502e5c18039db9c40ea128e033cb`  
		Last Modified: Thu, 15 Jan 2026 23:56:14 GMT  
		Size: 230.7 KB (230732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:10-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:9827bfbe440375b9fa5a67fa016a420786a600a5eeed76e3d72adb4876d18b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3962762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddd5d9351b5cf13da98eb983e38958e43df93af18d14728175ba95ad00df1b8`

```dockerfile
```

-	Layers:
	-	`sha256:6a5eaabcc46ee444930983b06197526df21610b7590f6fd3c3d28393b6d4b502`  
		Last Modified: Fri, 16 Jan 2026 00:33:52 GMT  
		Size: 3.9 MB (3941538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e48459512c5f33b8a5b31881dbcd152d9bffc28280eedff58a908cce7f0c234a`  
		Last Modified: Fri, 16 Jan 2026 00:33:55 GMT  
		Size: 21.2 KB (21224 bytes)  
		MIME: application/vnd.in-toto+json
