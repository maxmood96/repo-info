## `tomcat:9-jre17-temurin-jammy`

```console
$ docker pull tomcat@sha256:ec8c063deeff0b5aaa5830f80ce131ab81755065c3557243d7bf76eeed3807b2
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
$ docker pull tomcat@sha256:d801a0f7366d5599f613fb4fc54d6490d3d3c221ecbcadf1f8b42ed3e8d22064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107379564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12f3e6367b033a0c26410d85a4b179252286bb3b55cf70d226956d7c9a62e2c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:09:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:09:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:09:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:09:45 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:09:45 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 01 Apr 2026 20:10:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:10:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:10:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:10:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 03 Apr 2026 18:11:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:11:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:11:14 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:11:14 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:11:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:11:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:11:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Apr 2026 18:11:14 GMT
ENV TOMCAT_VERSION=9.0.117
# Fri, 03 Apr 2026 18:11:14 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 18:11:14 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:11:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:11:22 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:11:22 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:11:22 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:11:22 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8499d88555db34ced0d9fb448fe2757038134d3dc92b148d3294903ee80ccedd`  
		Last Modified: Wed, 01 Apr 2026 20:10:02 GMT  
		Size: 16.1 MB (16149341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1e52a849ff5b204e6e43b714050e2017d63fb635d9abce8f05b8df7565202b`  
		Last Modified: Wed, 01 Apr 2026 20:10:25 GMT  
		Size: 47.4 MB (47434755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ac1704dc3fdcf3ad7057844e8b8489c48f93a985c486c5293c22694726a8fd`  
		Last Modified: Wed, 01 Apr 2026 20:10:23 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163ad111ef3730c3f16e15ea95bb50edeb081d68372392b05cb290aecee7eab3`  
		Last Modified: Wed, 01 Apr 2026 20:10:23 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec76f834c17cb8893541c58e95811d0a4bb8419cadd8d42e4024b6f670dda24`  
		Last Modified: Fri, 03 Apr 2026 18:11:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945d1607abbd9482aeedd36527be633bae25bcf8aa9863f5ad27de7fcca1864a`  
		Last Modified: Fri, 03 Apr 2026 18:11:31 GMT  
		Size: 13.8 MB (13826650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c491b94132fef80a10e67b8bfec641e054d20f57cea58366edfa5c02bf5003c7`  
		Last Modified: Fri, 03 Apr 2026 18:11:31 GMT  
		Size: 229.8 KB (229760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:5b70759a084a56b4b4bc59fe57d198cf4e7b4e0a646522c2459fc38776be9a39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3959742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e673b60344c08e06b63e4debef40f423c7d675c9cc61f4432a77b11cde69b9`

```dockerfile
```

-	Layers:
	-	`sha256:b72c0226712cd2810c129ee74f16ffca5c5da39c70dfb441caa689e22f8cd6c9`  
		Last Modified: Fri, 03 Apr 2026 18:11:31 GMT  
		Size: 3.9 MB (3938529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31f2e6fc2f1611a26b9c6348de3583764acf390cf908db18364e0a0a290c866a`  
		Last Modified: Fri, 03 Apr 2026 18:11:31 GMT  
		Size: 21.2 KB (21213 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:a00ed8b4d7741f06ee86bed196b251c6e595b0d604a11f5bb831f3f51473113e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101739550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8fb38e148f9d5af6557e891888855a0cf2d1037fb348dd7d7a25cf9ff131b17`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:eaa1e345a925acc7b826effa9fb4c3dfb4aebe47807533938898d49afe7561cb in / 
# Sun, 22 Mar 2026 18:14:12 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:08:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:08:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:08:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:08:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:08:40 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 01 Apr 2026 20:08:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:08:45 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:08:45 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:08:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 03 Apr 2026 18:09:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:09:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:09:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:09:39 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:09:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:09:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:09:39 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Apr 2026 18:09:39 GMT
ENV TOMCAT_VERSION=9.0.117
# Fri, 03 Apr 2026 18:09:39 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 18:11:33 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:11:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:11:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:11:39 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:11:39 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:11:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e7c88f36edd2a67246005d083413bd656459d3b63bab8e6a05a1018c7658daae`  
		Last Modified: Sun, 22 Mar 2026 18:43:39 GMT  
		Size: 26.8 MB (26842286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c53d90a97bd867fde9f2322d69ecaecc705feb2551ff0e40dfc4ef8f1482b27`  
		Last Modified: Wed, 01 Apr 2026 20:08:58 GMT  
		Size: 15.9 MB (15889979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a32329dc6cff5d9c328ef3268615b2d2147d44a429a514e265bf7aed39faa6`  
		Last Modified: Wed, 01 Apr 2026 20:08:59 GMT  
		Size: 45.0 MB (45044358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76b09d3385831739a7139dd5766037a7145b55335d30f601fd029bf07b7ba9f`  
		Last Modified: Wed, 01 Apr 2026 20:08:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df14e2e6119c81348938442926636bb8302b61465517feff8423bf64d32a5c65`  
		Last Modified: Wed, 01 Apr 2026 20:08:57 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d30d1665e5d3b9e3b5167be5b3e661234af3ac8d29b46432f8f80e21c8f0654`  
		Last Modified: Fri, 03 Apr 2026 18:09:56 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8818b076392a731a318b06cf9e295ad8edbbff2ecf3b8fd8f3499cc09bf9fe3`  
		Last Modified: Fri, 03 Apr 2026 18:11:48 GMT  
		Size: 13.8 MB (13757847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b98f9704d2f33770e250902d9a6781cdd8d0c5d51159319fe391c1505781e4`  
		Last Modified: Fri, 03 Apr 2026 18:11:47 GMT  
		Size: 202.4 KB (202436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:a1bb250a4a217986dffa1c84647cc02acf5849832f2a8ae696ef5d562862370e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3962196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2764b251ab01bab93577d074dedde4e43983fb560ec3a9435b5ce9f48a94c12`

```dockerfile
```

-	Layers:
	-	`sha256:1ad5f06334473ff191403152214b2f6847d66b2d07ab25a80c34610aa5fea8bc`  
		Last Modified: Fri, 03 Apr 2026 18:11:47 GMT  
		Size: 3.9 MB (3940864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a549f8b5bf1d51c79f09278d3478a349b7c3e345948640ccff82add0c0316a4`  
		Last Modified: Fri, 03 Apr 2026 18:11:47 GMT  
		Size: 21.3 KB (21332 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:c78a7b938d9f7285f4adf96f3e7e1c734e68618038bab4f389ae98f756f60e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104668559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf260bceb1bd5454d85ec4f62365ee4d59587124ad74dc617688fbc95eb5576`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:09:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:09:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:09:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:09:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:09:44 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 01 Apr 2026 20:10:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:10:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:10:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:10:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 03 Apr 2026 18:11:11 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Apr 2026 18:11:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Apr 2026 18:11:11 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Apr 2026 18:11:11 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Apr 2026 18:11:11 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:11:11 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Apr 2026 18:11:11 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Apr 2026 18:11:11 GMT
ENV TOMCAT_VERSION=9.0.117
# Fri, 03 Apr 2026 18:11:11 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 18:11:12 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:11:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:11:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:11:21 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:11:21 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:11:21 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d202f2689bfc1f8be0c2401b89369902c9e75737b17229b3ecfec10f5dfb7d`  
		Last Modified: Wed, 01 Apr 2026 20:10:03 GMT  
		Size: 16.1 MB (16073500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f6fc2d8b91a94d17ecdcbf7466e198066f345025ceccf0878b9ace792a4f38`  
		Last Modified: Wed, 01 Apr 2026 20:10:29 GMT  
		Size: 46.9 MB (46922048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca09713b16069fee4ec52202caf5893ec65747dd747f74f576be238b18aa40d8`  
		Last Modified: Wed, 01 Apr 2026 20:10:27 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95691bedf2b2e58b966ac2b99ec3d8af8891ab7d79da35f01dc3eb643074ef09`  
		Last Modified: Wed, 01 Apr 2026 20:10:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204bf3859cc01647c4177be6704df0496c3618830223385c349604c290aade22`  
		Last Modified: Fri, 03 Apr 2026 18:11:30 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d079c11f7e3fd788b17ceae7578b285c1efe3d8c974463e17c333240f04d9247`  
		Last Modified: Fri, 03 Apr 2026 18:11:30 GMT  
		Size: 13.8 MB (13834708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b04ca79856734354490660a319a72488e0b47b859b85e1abadd84352b6d0db`  
		Last Modified: Fri, 03 Apr 2026 18:11:30 GMT  
		Size: 228.7 KB (228716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:eccb5cd8e38990e901782adda6640b71c6929dd0eceee3827a138c5015c7e1d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3959559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd75c4761129582c7361820cca3f741ca78c91086f471100c294dcee85498bf`

```dockerfile
```

-	Layers:
	-	`sha256:a1013135b01bafcbc6de48146859628cc4df3e4c922fb7db4352ed10b4169d9d`  
		Last Modified: Fri, 03 Apr 2026 18:11:30 GMT  
		Size: 3.9 MB (3938198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:060eca2a0a42adc3a0a3cc4991888b256d7bdb37d7a248d027fd257235494064`  
		Last Modified: Fri, 03 Apr 2026 18:11:30 GMT  
		Size: 21.4 KB (21361 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:bb859c46913679f6b1e7585fe0d196e27a05818f06fa5e12a5461f286e3aef22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.7 MB (113717511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c5d99959c2920a7cd84306c7a87f79f7db2225ae6f6edf2cb75c9d8ef6160a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:20:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:20:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:20:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:20:51 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:20:51 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 01 Apr 2026 20:22:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:22:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:22:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:22:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 22:12:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 01 Apr 2026 22:12:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 22:12:05 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 01 Apr 2026 22:12:07 GMT
WORKDIR /usr/local/tomcat
# Wed, 01 Apr 2026 22:12:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 01 Apr 2026 22:12:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 01 Apr 2026 22:12:07 GMT
ENV TOMCAT_MAJOR=9
# Wed, 01 Apr 2026 22:12:07 GMT
ENV TOMCAT_VERSION=9.0.117
# Wed, 01 Apr 2026 22:12:07 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 18:15:39 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:15:46 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:15:47 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:15:47 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:15:47 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:15:47 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e568bb13a59c072b3af8c406e7b451459d28a2bdf653f96393ea9610f7d09959`  
		Last Modified: Wed, 01 Apr 2026 20:21:27 GMT  
		Size: 17.6 MB (17622524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f12b28cc885ccaebe18a850f239b6b7b59075cf8c7b9458589079d9cc69a78`  
		Last Modified: Wed, 01 Apr 2026 20:23:14 GMT  
		Size: 47.3 MB (47331458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af421496eab4e6fcbddc84a3f4926107037e9337f8c292c27288a5f48df0aa39`  
		Last Modified: Wed, 01 Apr 2026 20:23:13 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fd778eff2d64f7c05b436173493bf83f2b227a74da05bf428a4ff630acf3ad`  
		Last Modified: Wed, 01 Apr 2026 20:23:13 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7051f7b853e96879bbc448dcc9fc5fc31acb8d484a2eb30b5eddec999a5cd4`  
		Last Modified: Wed, 01 Apr 2026 22:12:40 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da643b88616e575a74f657f7d98a2488c95abaec1afd240c0d52bbb64bcefd4`  
		Last Modified: Fri, 03 Apr 2026 18:16:15 GMT  
		Size: 13.9 MB (13852028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c677a1dfd58372d0f0bb330c7de0b514717ea8d9abf9f73ca16f9f03663c1ad`  
		Last Modified: Fri, 03 Apr 2026 18:16:14 GMT  
		Size: 259.2 KB (259196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:6f2e8f5da4bd2f2fe2a9c39f98c9c2fb5cc7173a82c93f9af06f2e8584b46624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3963882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759c8e5bb8d2635f1e441a4255daa685f0f241a02967f9e78b99ce462ce8da43`

```dockerfile
```

-	Layers:
	-	`sha256:f08b64de8d8057d48cefeb7f40e5627715c8ad2be26d2a57e60b0a333132b2cb`  
		Last Modified: Fri, 03 Apr 2026 18:16:14 GMT  
		Size: 3.9 MB (3942617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8ad0cfdbd9d297c625dd39a34865b165841810315c44fed95f72115f209d087`  
		Last Modified: Fri, 03 Apr 2026 18:16:14 GMT  
		Size: 21.3 KB (21265 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:9-jre17-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:293040ee96f4e52a121f4f6fbd5c8ac9af4c25d4942c0891d053b0804ac33b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102816242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90013010da5f5f5fa031360c9944aac1a96c1fb4f3fe68588a08d7d5b122bb3`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sun, 22 Mar 2026 18:12:49 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:12:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:12:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:12:50 GMT
ADD file:e6d9716e3c60256d600998c1e662d7bc5ced705020e73df5a8f8327ed250efa1 in / 
# Sun, 22 Mar 2026 18:12:51 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:08:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:08:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:08:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:08:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:08:48 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 01 Apr 2026 20:09:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='437c30e861fb091d4bb2ff66a28b1d09e7ac9167f6163e286cb2968d29864e1b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:09:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:09:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:09:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 22:42:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 01 Apr 2026 22:42:45 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 22:42:45 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 01 Apr 2026 22:42:51 GMT
WORKDIR /usr/local/tomcat
# Wed, 01 Apr 2026 22:42:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 01 Apr 2026 22:42:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 01 Apr 2026 22:42:51 GMT
ENV TOMCAT_MAJOR=9
# Wed, 01 Apr 2026 22:42:51 GMT
ENV TOMCAT_VERSION=9.0.117
# Wed, 01 Apr 2026 22:42:51 GMT
ENV TOMCAT_SHA512=82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54
# Fri, 03 Apr 2026 18:11:17 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Apr 2026 18:11:20 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 18:11:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Apr 2026 18:11:20 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Apr 2026 18:11:20 GMT
ENTRYPOINT []
# Fri, 03 Apr 2026 18:11:20 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7db076360428795a3bedb94abf5c7d3527328da728852f1fa3e28cc99bb96eba`  
		Last Modified: Sun, 22 Mar 2026 18:44:00 GMT  
		Size: 28.2 MB (28202727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61594cb5a2469e67362dd6ac0dbccf92b89f433e8186d9f63201da426862ed3`  
		Last Modified: Wed, 01 Apr 2026 20:09:10 GMT  
		Size: 16.1 MB (16149500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd2f32a61fd6a64c2eb8c77bebe952c3ccf0706209e82387d6b60adb83409dc`  
		Last Modified: Wed, 01 Apr 2026 20:09:56 GMT  
		Size: 44.4 MB (44409686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91cc387888bbbd8013d2fff9bba3896e2acd25b93ed06bfb5303599484c848e`  
		Last Modified: Wed, 01 Apr 2026 20:09:55 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa6ad80faf88458292855e4d46663961bbbc7d2823882e1d86fac9da5995e6b`  
		Last Modified: Wed, 01 Apr 2026 20:09:55 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4314a6385bcf576305248b5b0a725d466fed941f666c48ac1ce1931e0eb5a50`  
		Last Modified: Wed, 01 Apr 2026 22:44:56 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2359422aeab607345eb9f5d26d9479b718c52a5fb22e69f8a26994b24bc44b`  
		Last Modified: Fri, 03 Apr 2026 18:11:35 GMT  
		Size: 13.8 MB (13820745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743cd42c5c5e34487d00728f18eeaf7aac3b427c9141edb9e30457d49b2c6b08`  
		Last Modified: Fri, 03 Apr 2026 18:11:34 GMT  
		Size: 230.9 KB (230940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:9-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:51504fba241ba0be61913401d64e8dc276f03b1d728a7cbc3566ab8cdb726d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247b6be1edd6d5d42dce9def0d832b8a47d388b9ec3e31640e9d3721e3003f3c`

```dockerfile
```

-	Layers:
	-	`sha256:de122b8f8b96f41455f8ce74f8653bbce4678eafe7b8139a74578b6122e2a674`  
		Last Modified: Fri, 03 Apr 2026 18:11:34 GMT  
		Size: 3.9 MB (3940120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:582b47d25c6cbf5f8816e5de6b13225f257f068178408e2dced76ec5a4435f03`  
		Last Modified: Fri, 03 Apr 2026 18:11:34 GMT  
		Size: 21.2 KB (21213 bytes)  
		MIME: application/vnd.in-toto+json
