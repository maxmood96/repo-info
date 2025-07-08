## `tomcat:11-jre17-temurin-jammy`

```console
$ docker pull tomcat@sha256:74c11d27544fe29d10fda335fbf443c478501d0bd224c78b37e10c0a9a3b8df2
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

### `tomcat:11-jre17-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:5cee84910937ead099e574c43869845926c5c9eadf0cc7654534c5945792bbc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 MB (106955196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bddb432262d7f1fe2af74757d61771f91384e358626281e79dcedad1324ffaf`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 04 Jul 2025 20:15:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 20:15:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_MAJOR=11
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_VERSION=11.0.9
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_SHA512=480ae04b5fa77e4f3f02d8e32b0ac5701390e9e0d3b2e57827defde8c364a5a4b3f37d25bc46a2538a4268babc7b61999a22314cb046360b2eb3f8109973a034
# Fri, 04 Jul 2025 20:15:48 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Jul 2025 20:15:48 GMT
ENTRYPOINT []
# Fri, 04 Jul 2025 20:15:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25706e9e719c4df9907a583a3af1bbbc40149b54bc63ac893255b24d05ebe2ff`  
		Last Modified: Wed, 02 Jul 2025 03:10:17 GMT  
		Size: 16.1 MB (16146410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5006e0852115f86cb2b9abb297c58242bffb3b63d6b9d8cb26aac444a36837d8`  
		Last Modified: Wed, 02 Jul 2025 03:10:18 GMT  
		Size: 47.0 MB (46958370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e412a6aa107b415b5ed7736de94863c64915907b34bd70dd1f95411c12465394`  
		Last Modified: Wed, 02 Jul 2025 03:10:15 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a023b21e1d611c552afa7c4c7b7112fca2b91d703f849cf0388c5f572c201088`  
		Last Modified: Wed, 02 Jul 2025 03:10:24 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f63de9bcf1fbf6f08626ee33f22a464229c614af872bb9ac74d0fd9e181dbcc`  
		Last Modified: Mon, 07 Jul 2025 21:05:04 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e8a7620028f5f2e841b49d9db9a5b0fd1c9ed73caf77ab871d2bf981513c2e`  
		Last Modified: Mon, 07 Jul 2025 21:05:05 GMT  
		Size: 14.1 MB (14082484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9759576df44122b7503535f108b469376cde0299dbebd4c2a60e8f336419373b`  
		Last Modified: Mon, 07 Jul 2025 21:05:04 GMT  
		Size: 229.6 KB (229607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:f9b0bc7f45f5dda1ed9faea0872cd7f8a1fdfa6d6714059546cf5d8b06afc8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3963272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89ef8c4ddc17b744b5db7aed35e2a3523daaff227a97981585ad24f4c4eff80`

```dockerfile
```

-	Layers:
	-	`sha256:8af4c0b54ecdb2d339f15a302db3706edf17d1972bec9f433804019f16e0f87d`  
		Last Modified: Mon, 07 Jul 2025 23:32:28 GMT  
		Size: 3.9 MB (3941689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecde0261e17eed8a99f9fa4fd7bcc0473f88a8c8c779e4ce7f8b4eb61e7c3eaf`  
		Last Modified: Mon, 07 Jul 2025 23:32:29 GMT  
		Size: 21.6 KB (21583 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:a8516583aa9b1b34be809845deac64dfcceed58885589fdad4ae20088005ef6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101421197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3593d34a86629cd0504b7f4e9898621117e02b936c90597c8bb64939775d24ed`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:ae409b4c753aab53fbf5e46b332d29d614f9ed31f53ec79d39ec3fbf2d659151 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 04 Jul 2025 20:15:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 20:15:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_MAJOR=11
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_VERSION=11.0.9
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_SHA512=480ae04b5fa77e4f3f02d8e32b0ac5701390e9e0d3b2e57827defde8c364a5a4b3f37d25bc46a2538a4268babc7b61999a22314cb046360b2eb3f8109973a034
# Fri, 04 Jul 2025 20:15:48 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Jul 2025 20:15:48 GMT
ENTRYPOINT []
# Fri, 04 Jul 2025 20:15:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:446fe3fba694631d6dbb9bee9d2a2a5c22c79cba078007ea85d822fb4083a291`  
		Last Modified: Wed, 02 Jul 2025 09:16:19 GMT  
		Size: 26.6 MB (26642498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f6da559a3ad83cc7b7e25fec79cdd5832638252e8c05668ff2f7aa7e3c91e6`  
		Last Modified: Wed, 02 Jul 2025 10:25:26 GMT  
		Size: 15.9 MB (15890962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f7d4885cce4bbc68b478f57b47cea5dcd61e84d7def85d7f5f9f956ea17623`  
		Last Modified: Wed, 02 Jul 2025 10:33:01 GMT  
		Size: 44.6 MB (44627660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cee4a510f017ca1d513c70c0e483d2bf6960984a8324e22f391abb6a84a76bc`  
		Last Modified: Wed, 02 Jul 2025 10:32:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c793b752fbd93f836886b2d1cf86c4d95d523beb136a1eaf8b471073777b59f`  
		Last Modified: Wed, 02 Jul 2025 10:32:58 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fc555cdfa3758a42002521e08540ad44d6e3e08d94d342398448a3d25bfcdc`  
		Last Modified: Wed, 02 Jul 2025 12:28:59 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7305248d784f14084be64a3d67338cc2c96bbda30ae058de16ff1285b10454`  
		Last Modified: Tue, 08 Jul 2025 03:55:27 GMT  
		Size: 14.1 MB (14055123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a3aede9bfc6764512177794b4c8a144209dc4cd95d041de64caaa95d2c7d8c`  
		Last Modified: Tue, 08 Jul 2025 03:55:26 GMT  
		Size: 202.3 KB (202309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:3580a939a453f5cd93bd34dccf0d65b73c7b5fd828eec41ed3021cd8ba44c0e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd63d27c1a0457af622e9a05d742a2d01ed8d23c5c9897f99ed82b06c1dde43a`

```dockerfile
```

-	Layers:
	-	`sha256:1e524dcc64a912eca0bba7adef69e4338e88987a79be2f33ab7dd60b61f33392`  
		Last Modified: Tue, 08 Jul 2025 05:32:23 GMT  
		Size: 3.9 MB (3944032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a199caa039ad789620327d68c0076cbadaf645f30148485eb886ae117c3c11a1`  
		Last Modified: Tue, 08 Jul 2025 05:32:23 GMT  
		Size: 21.7 KB (21707 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:bd3eaaa7241af54a9a866905dcc39d22d56406a19f9b4b600c75d5bb7a301802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104208687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33743cea7ae675e04d05a6c48dff075d687f365be972b72118ca4a9bc598b88`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 04 Jul 2025 20:15:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 20:15:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_MAJOR=11
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_VERSION=11.0.9
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_SHA512=480ae04b5fa77e4f3f02d8e32b0ac5701390e9e0d3b2e57827defde8c364a5a4b3f37d25bc46a2538a4268babc7b61999a22314cb046360b2eb3f8109973a034
# Fri, 04 Jul 2025 20:15:48 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Jul 2025 20:15:48 GMT
ENTRYPOINT []
# Fri, 04 Jul 2025 20:15:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cf37c5f5e10b3110a133ed367190f7cdd79aad284aef8d5335a2aee0c5fcfc`  
		Last Modified: Wed, 02 Jul 2025 05:06:30 GMT  
		Size: 16.1 MB (16059884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d14c55838978a26b78dc539c7cde51387ff425a893d4171735af7f0d7ba449`  
		Last Modified: Wed, 02 Jul 2025 05:11:49 GMT  
		Size: 46.5 MB (46474280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1c8bd711f66399caa3b29296162472a66f4702e3c5732fdd566631662e90d7`  
		Last Modified: Wed, 02 Jul 2025 05:11:47 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04208d964e023847837542b731214011191e851dc8e4698fd7afceab4b713a78`  
		Last Modified: Wed, 02 Jul 2025 05:11:47 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bddea4989802f0fbb5fdba57f375f45f719cebb44ae473c23d2e3d2d265cb221`  
		Last Modified: Wed, 02 Jul 2025 14:34:19 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f422f1f0824066ad22efd3271ac78f1243faeb578c3c4f1ce6ef89d932b82cb2`  
		Last Modified: Tue, 08 Jul 2025 05:22:13 GMT  
		Size: 14.1 MB (14083968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087bed2d4427252550bd1bf8555e745665d20ef3278830164268aab7b594dd5c`  
		Last Modified: Tue, 08 Jul 2025 05:22:13 GMT  
		Size: 228.6 KB (228641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:3359d90a2c3106a4654e568eaab3623f1d0904dcc778537d3c44def2c66ff868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3963113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fc68492aaa87ec48afbc1bcf37c0388471b52727a5ec4227c5bb09687084be`

```dockerfile
```

-	Layers:
	-	`sha256:078efeeb998eb85ab2b88999c222071dd26fe73644913e95a39f166eb0c6b6fb`  
		Last Modified: Tue, 08 Jul 2025 08:31:13 GMT  
		Size: 3.9 MB (3941370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18cf5b1084271631d447319509c06808d4aa478fbd6f4b42cc5276f9ee40af9e`  
		Last Modified: Tue, 08 Jul 2025 08:31:13 GMT  
		Size: 21.7 KB (21743 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:f18ad6ab198ce5c3cc0b12481e3b25e1bbee30ff526a15b1f4607efdeeaca627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113188737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f89fdfff7e2d9ab49f2cc3cf81142361304e87696fdb93dc9ed715ab23265cd`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 04 Jul 2025 20:15:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 20:15:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_MAJOR=11
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_VERSION=11.0.9
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_SHA512=480ae04b5fa77e4f3f02d8e32b0ac5701390e9e0d3b2e57827defde8c364a5a4b3f37d25bc46a2538a4268babc7b61999a22314cb046360b2eb3f8109973a034
# Fri, 04 Jul 2025 20:15:48 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Jul 2025 20:15:48 GMT
ENTRYPOINT []
# Fri, 04 Jul 2025 20:15:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f595b1fb797135dd0e29ee3176dc6a26da5fdd960326b5800ab21ad59036a273`  
		Last Modified: Wed, 02 Jul 2025 03:15:14 GMT  
		Size: 17.6 MB (17618409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e245abf2e5632ad09bee58abd7edda39835fb16215364fb4809fb65270daf0`  
		Last Modified: Wed, 02 Jul 2025 03:24:18 GMT  
		Size: 46.8 MB (46769893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88a79e30a4d29cc765e5ec612f737d31b0151404ff8e23af142b3419f7a8ffd`  
		Last Modified: Wed, 02 Jul 2025 03:24:15 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c15b8b214a533629f1b9add371b06bb953a8311c88ffa9d4fadcfafbd1c6211`  
		Last Modified: Wed, 02 Jul 2025 03:24:15 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b82f9b30884755d6493d232949048e79bd9ae0f92667b37c997048067851f1`  
		Last Modified: Wed, 02 Jul 2025 14:54:27 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb40f2a3cf5e8aede69674b428d44ddada1d004973c74658b538fa062ee5637`  
		Last Modified: Tue, 08 Jul 2025 00:15:10 GMT  
		Size: 14.1 MB (14096138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1991cc978259df2f0926e97bffa156addcc5ec1ad5cfa586d325978eb4c557`  
		Last Modified: Tue, 08 Jul 2025 00:15:09 GMT  
		Size: 259.0 KB (259034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:0e5bf5334a2e811bef553e8a14aa6cd3c49f3352d3338b1a5e1b08739283dd95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3967424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bec5271130d72c16d1a4517c3380fdd08aa39833cf8585db3b65752608d0603`

```dockerfile
```

-	Layers:
	-	`sha256:68fe2dcc5565d00ac2f9dd75bff208c4e7b1b792b65b9534eb2181e4d572b06b`  
		Last Modified: Tue, 08 Jul 2025 02:30:40 GMT  
		Size: 3.9 MB (3945783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97ba1af1a46a912b9f427314b2a3de8c2117c1131714a439053eac2226dd8123`  
		Last Modified: Tue, 08 Jul 2025 02:30:41 GMT  
		Size: 21.6 KB (21641 bytes)  
		MIME: application/vnd.in-toto+json

### `tomcat:11-jre17-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:41e830aa3a476e778b40cde608e7f869fdfc513f6b6fa868c0ffc8bc75b03701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102424127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366e967e4c92b46c1ebbfba906c01f6a926ba43f4ed39195ea2bc5f1b4a94469`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:dad9a012cce363ba4f28e2a6f3efa82869330e872362e4867be1bd507ed8963a in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 04 Jul 2025 20:15:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 20:15:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_MAJOR=11
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_VERSION=11.0.9
# Fri, 04 Jul 2025 20:15:48 GMT
ENV TOMCAT_SHA512=480ae04b5fa77e4f3f02d8e32b0ac5701390e9e0d3b2e57827defde8c364a5a4b3f37d25bc46a2538a4268babc7b61999a22314cb046360b2eb3f8109973a034
# Fri, 04 Jul 2025 20:15:48 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 04 Jul 2025 20:15:48 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 04 Jul 2025 20:15:48 GMT
ENTRYPOINT []
# Fri, 04 Jul 2025 20:15:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8d24804db3a6eaf32ea752d2dd82fb21273e4e2494ca124217c93f38bc823ca5`  
		Last Modified: Wed, 02 Jul 2025 03:43:01 GMT  
		Size: 28.0 MB (28002175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b7407b9fdf832fa4e3a41a2319aa3e0d04f31104a25092c677a83bf06472d7`  
		Last Modified: Wed, 02 Jul 2025 04:15:41 GMT  
		Size: 16.1 MB (16144420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc328faaa7eddce5761c94a9be57109fdbe31819c251cbb6ed7b3cc83d3d178`  
		Last Modified: Wed, 02 Jul 2025 04:20:09 GMT  
		Size: 44.0 MB (43960915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf0146cfb718899b13a5e863494b48170acabca893205c94484f806cf322ddf`  
		Last Modified: Wed, 02 Jul 2025 04:20:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e789874d15be7df42535ed613fba7a60476742405782a444a83d3f3692900937`  
		Last Modified: Wed, 02 Jul 2025 04:20:01 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79984551e20eb72c62261f369e83adc440d11fd0e7371b390d9109e49a8f7c5e`  
		Last Modified: Wed, 02 Jul 2025 07:21:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21ee636bca84e60b5d127b016a94e01be8d7064860b34b4190d7484666883a8`  
		Last Modified: Tue, 08 Jul 2025 05:24:31 GMT  
		Size: 14.1 MB (14083169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd48af33ec5b2e235153f73a40a4577f7c0e3e5efcb9197b53dcdafc95b83817`  
		Last Modified: Tue, 08 Jul 2025 05:24:31 GMT  
		Size: 230.8 KB (230805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `tomcat:11-jre17-temurin-jammy` - unknown; unknown

```console
$ docker pull tomcat@sha256:b0b13c0d3bf8563bf92ed6d7df35ab4253312be800ff1b259a72ba51a556ab68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c0eb7b45103eae35850bf8cd46a3f66d1f1e014792c38efd33ad9015cb8d4a`

```dockerfile
```

-	Layers:
	-	`sha256:ba065cbade382d0a541ce4290c56eb481567677144634c211c53e4c3c008c4b7`  
		Last Modified: Tue, 08 Jul 2025 08:31:20 GMT  
		Size: 3.9 MB (3943280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1f2eba0642f13797742ddefd2ad2c29c8d7a32f7dbd5b6351cecaa55cbc2eb`  
		Last Modified: Tue, 08 Jul 2025 08:31:21 GMT  
		Size: 21.6 KB (21583 bytes)  
		MIME: application/vnd.in-toto+json
