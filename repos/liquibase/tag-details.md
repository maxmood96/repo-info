<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `liquibase`

-	[`liquibase:4.32`](#liquibase432)
-	[`liquibase:4.32-alpine`](#liquibase432-alpine)
-	[`liquibase:4.32.0`](#liquibase4320)
-	[`liquibase:4.32.0-alpine`](#liquibase4320-alpine)
-	[`liquibase:alpine`](#liquibasealpine)
-	[`liquibase:latest`](#liquibaselatest)

## `liquibase:4.32`

```console
$ docker pull liquibase@sha256:d5df8530bf4aca64c58c6cc76d7f47a091c33e125ef57b5ca27091e26df6dd78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.32` - linux; amd64

```console
$ docker pull liquibase@sha256:f7cef26c451edbf8265868fa28343564902ee4aba6c24cfc92c1603b403d5093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.7 MB (455730593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fc0482bba604856ceabfff676c4e3d753e35d92ec810515606735dba1f47ec`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

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
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33e8ebdb86dc7a920582c649882465543cb59ccf43a509416f6e6e7905183e6`  
		Last Modified: Wed, 02 Jul 2025 03:10:24 GMT  
		Size: 16.1 MB (16146378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71b536eab81d4b1b3e2c1fee8daf4304d1ea62a32cb23772727c219e1eee6ef`  
		Last Modified: Wed, 02 Jul 2025 03:10:27 GMT  
		Size: 52.9 MB (52891244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4112c5be290bc12057463f12fff689c8cae27c00c7e0f639f94d285ce9c4cdd`  
		Last Modified: Wed, 02 Jul 2025 03:10:23 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab0fa3d848a3c661740f09af88f10cc5a3cea13e177c94dfa483136ab23ad42`  
		Last Modified: Wed, 02 Jul 2025 03:10:23 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4221402984ed91e2323ad4c3ea7503cbdc207e3bcb215e3f72f2424709e590`  
		Last Modified: Wed, 02 Jul 2025 05:57:43 GMT  
		Size: 4.3 KB (4304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2890eb5cdd67d9228eab0a66c4eb3cab98288fe7e4be2c18d325624b453419`  
		Last Modified: Wed, 02 Jul 2025 06:41:53 GMT  
		Size: 353.6 MB (353635050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630c3a76138589d62bc5db897cf3784da16c8cc94c01379f675f35ecee32fbd1`  
		Last Modified: Wed, 02 Jul 2025 05:57:48 GMT  
		Size: 3.5 MB (3514812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbabe9a5ea5fd781a1ddc2f096a7d61602a1233b6417b6eeaaf018382c8046c9`  
		Last Modified: Wed, 02 Jul 2025 05:57:53 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3202c5d42df6efa13c57b177bccacddf924ffe7dd88bed9134406c3eb33bcf8d`  
		Last Modified: Wed, 02 Jul 2025 05:57:56 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.32` - unknown; unknown

```console
$ docker pull liquibase@sha256:fe91ff3201f12e409bd1678cb63991ef17b9c4e32028918d8c7d9e1ef64f6f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff89097dffb4499abeb139e22a20399aaafb9f41996d8f8460bff08d38dae1bf`

```dockerfile
```

-	Layers:
	-	`sha256:8832828d64492e7685bb772e719a0788d8d15c41b2e00f31600c970ba4936fe6`  
		Last Modified: Wed, 02 Jul 2025 06:39:20 GMT  
		Size: 3.9 MB (3941227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e934b50993475d108c4bd75a6144f3493a4863d000f444fbecec35cb0c9366e`  
		Last Modified: Wed, 02 Jul 2025 06:39:21 GMT  
		Size: 24.4 KB (24418 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.32` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:28f7505f8037db07ed7d72026b2c3cb94df8981be380306832cefa705bcd3706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.4 MB (452388643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fca682c712d51bb08cb318676c75dfd2f544b9311b7d750ac5046f1a5397ba`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

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
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
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
	-	`sha256:454ec3ba22ac3eb4e1cbe3aced0fb597d9bd1df666b839fb894c6a21d320da25`  
		Last Modified: Wed, 02 Jul 2025 05:14:29 GMT  
		Size: 52.1 MB (52070725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26d30a34f7df5fae8f971d85c94c60ef383378263715aa7f5bdcfda677f1980`  
		Last Modified: Wed, 02 Jul 2025 05:14:23 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868db56d7c15e73a39e43f047129c4bedd8aeda161c8978e45a97148a83fc291`  
		Last Modified: Wed, 02 Jul 2025 05:14:23 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014ad84cc84638e74cad2e56135ad79f37746231afccfdb1290e085941f1fbd6`  
		Last Modified: Wed, 02 Jul 2025 08:43:24 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ed8b7fc10ee151a72a14badb42655c73d8b7b579f3d245852cf26558e5677a`  
		Last Modified: Wed, 02 Jul 2025 11:48:24 GMT  
		Size: 353.6 MB (353635045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511d1fc2bfd4863b626d68cd7e762fe7cdfd7426a19f3063189c63f2dc9d3be7`  
		Last Modified: Wed, 02 Jul 2025 08:43:26 GMT  
		Size: 3.3 MB (3256287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9491337c5d41cf3ea8b71ee5e5ccd3ac518e892726e857f3bc6c8efa3cbc3d`  
		Last Modified: Wed, 02 Jul 2025 08:43:25 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d415553b38bf7ca931b3843e884a80a2fd3c9ea96e6d1e88bbb9ffa65f7e5f`  
		Last Modified: Wed, 02 Jul 2025 08:43:26 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.32` - unknown; unknown

```console
$ docker pull liquibase@sha256:9ad5ab55a8ddc2a287b8b0c39ecc08de6efaa1ab55b0be6ab7d0492206faba20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b59f37d3cfcb924da372d216dec932a022ce677ebe1df2666d26acdbf557aff`

```dockerfile
```

-	Layers:
	-	`sha256:1cb10308edf6084115b8c27aa398a0ab730b9403db53d0ce3b68fae04354cc6b`  
		Last Modified: Wed, 02 Jul 2025 09:39:22 GMT  
		Size: 3.9 MB (3940895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:473118d07cc32d36fc44cf67cfcb3a7f70de576325e9856ac98f0b6e40214029`  
		Last Modified: Wed, 02 Jul 2025 09:39:22 GMT  
		Size: 24.5 KB (24540 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.32-alpine`

```console
$ docker pull liquibase@sha256:8544830e4ca411eff42eb176feeba1b404f022df03fada5d7f1243e5613bbba6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.32-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:4c3e1a080bc81fa4240fd72c354596aa9035b18ae1d11f5309a81761e0372ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.5 MB (428538737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7b5749651c357c25993d3697b04ef5fa5b834c046760608a0d4536d794fbfe`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 15:54:00 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d254e74249fcd7b94a1781e88f1a6f82a7374fa38534597aa8ee73acc6b12d`  
		Last Modified: Tue, 03 Jun 2025 13:43:04 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa601d9e14ea7319081e6f48f04318cfb467678483e4eb561dd15c6c000ed02`  
		Last Modified: Tue, 03 Jun 2025 13:43:09 GMT  
		Size: 67.8 MB (67802051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f4f98b98e0507c8ef049e6fdc0fc8f4f2f478ab1e15be6b91e709938ec82a0`  
		Last Modified: Tue, 03 Jun 2025 13:43:20 GMT  
		Size: 353.7 MB (353659617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd18ba5867df0761825b305d7ba21b9872705937388519a51ad1329cb53d1f6c`  
		Last Modified: Tue, 03 Jun 2025 13:43:06 GMT  
		Size: 3.4 MB (3433209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac55a4e3432c438a4f536d8321a94946d57d9b5824501bf61b37b901169344`  
		Last Modified: Tue, 03 Jun 2025 13:43:07 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa192255813780f3a510a1b0b662e05189ff63a6f1ddb944b58aae60cdf6fa52`  
		Last Modified: Tue, 03 Jun 2025 13:43:08 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.32-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:320a5a919092cea878a339300632114dee3cb4852d0982765a224c5791b9a63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.9 KB (424950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c0383adc941b49fcaf669264535721596363830e5377067e400a337164ace3`

```dockerfile
```

-	Layers:
	-	`sha256:6779fcfccf29fba7d611a59c6a302f2d36f8ffd99ccd7b0c7e93b181855567f3`  
		Last Modified: Wed, 04 Jun 2025 00:04:44 GMT  
		Size: 403.2 KB (403239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1393290584387fe56550a652f4a981566d37297b4d14f5ecce2866124751255`  
		Last Modified: Wed, 04 Jun 2025 00:04:44 GMT  
		Size: 21.7 KB (21711 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.32-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:5df3fe840d73b107b6091a70c051919c25807812405031f325c52f22d51a1901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.6 MB (427626574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3b0f528bb29c9d8e983d8da8031c676143f017cf006c9bf956e36a288e1aa2`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 15:54:00 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d960cdd0c49e3498bf6ec7d87b10dad4343563e53b9d8035d65c95c55c52999`  
		Last Modified: Tue, 03 Jun 2025 15:03:02 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925c4a78c555ba3c950941e6d6271896da57b0ddefa6e1c39a006da828657e78`  
		Last Modified: Tue, 03 Jun 2025 15:03:06 GMT  
		Size: 66.8 MB (66799294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e9a29829ca0505af0c82a9601997eaf320d57e44e1a101dde1ee080157a70a`  
		Last Modified: Tue, 03 Jun 2025 15:03:25 GMT  
		Size: 353.7 MB (353659532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac9a8ecf3de910c8dad2c8db151cfb2ea7644281a2e5c4e346d19fb363bd2c0`  
		Last Modified: Tue, 03 Jun 2025 15:03:05 GMT  
		Size: 3.2 MB (3173107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0d2579a1fe9eb19872234ce6821951463ced6acccd74269887d5e646a54856`  
		Last Modified: Tue, 03 Jun 2025 15:03:06 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d372df514f79ee87a3777443c33566eb23a953b6f7af8a4f77fe316d304b83b`  
		Last Modified: Tue, 03 Jun 2025 15:03:07 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.32-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:a2ba65aaa27cd37509f5c48e4d79ad933b55d857b0b3615510dfb819cd69e81c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.3 KB (424333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1708af05fefc0c6be3e00a92e2ab51966d3aef47cfb298abc45fcc5eb99fc70`

```dockerfile
```

-	Layers:
	-	`sha256:de4ebc5acfd594b876bcf89cb72433b4b269d9b314403a4e64410bb4ea06ab0f`  
		Last Modified: Wed, 04 Jun 2025 00:04:49 GMT  
		Size: 402.5 KB (402486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c6aef5a59e7465653b4094cc2fc207c7a0c2dacbee07b2ada9f02a5f7e820d3`  
		Last Modified: Wed, 04 Jun 2025 00:04:49 GMT  
		Size: 21.8 KB (21847 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.32.0`

```console
$ docker pull liquibase@sha256:d5df8530bf4aca64c58c6cc76d7f47a091c33e125ef57b5ca27091e26df6dd78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.32.0` - linux; amd64

```console
$ docker pull liquibase@sha256:f7cef26c451edbf8265868fa28343564902ee4aba6c24cfc92c1603b403d5093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.7 MB (455730593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fc0482bba604856ceabfff676c4e3d753e35d92ec810515606735dba1f47ec`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

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
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33e8ebdb86dc7a920582c649882465543cb59ccf43a509416f6e6e7905183e6`  
		Last Modified: Wed, 02 Jul 2025 03:10:24 GMT  
		Size: 16.1 MB (16146378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71b536eab81d4b1b3e2c1fee8daf4304d1ea62a32cb23772727c219e1eee6ef`  
		Last Modified: Wed, 02 Jul 2025 03:10:27 GMT  
		Size: 52.9 MB (52891244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4112c5be290bc12057463f12fff689c8cae27c00c7e0f639f94d285ce9c4cdd`  
		Last Modified: Wed, 02 Jul 2025 03:10:23 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab0fa3d848a3c661740f09af88f10cc5a3cea13e177c94dfa483136ab23ad42`  
		Last Modified: Wed, 02 Jul 2025 03:10:23 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4221402984ed91e2323ad4c3ea7503cbdc207e3bcb215e3f72f2424709e590`  
		Last Modified: Wed, 02 Jul 2025 05:57:43 GMT  
		Size: 4.3 KB (4304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2890eb5cdd67d9228eab0a66c4eb3cab98288fe7e4be2c18d325624b453419`  
		Last Modified: Wed, 02 Jul 2025 06:41:53 GMT  
		Size: 353.6 MB (353635050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630c3a76138589d62bc5db897cf3784da16c8cc94c01379f675f35ecee32fbd1`  
		Last Modified: Wed, 02 Jul 2025 05:57:48 GMT  
		Size: 3.5 MB (3514812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbabe9a5ea5fd781a1ddc2f096a7d61602a1233b6417b6eeaaf018382c8046c9`  
		Last Modified: Wed, 02 Jul 2025 05:57:53 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3202c5d42df6efa13c57b177bccacddf924ffe7dd88bed9134406c3eb33bcf8d`  
		Last Modified: Wed, 02 Jul 2025 05:57:56 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.32.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:fe91ff3201f12e409bd1678cb63991ef17b9c4e32028918d8c7d9e1ef64f6f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff89097dffb4499abeb139e22a20399aaafb9f41996d8f8460bff08d38dae1bf`

```dockerfile
```

-	Layers:
	-	`sha256:8832828d64492e7685bb772e719a0788d8d15c41b2e00f31600c970ba4936fe6`  
		Last Modified: Wed, 02 Jul 2025 06:39:20 GMT  
		Size: 3.9 MB (3941227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e934b50993475d108c4bd75a6144f3493a4863d000f444fbecec35cb0c9366e`  
		Last Modified: Wed, 02 Jul 2025 06:39:21 GMT  
		Size: 24.4 KB (24418 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.32.0` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:28f7505f8037db07ed7d72026b2c3cb94df8981be380306832cefa705bcd3706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.4 MB (452388643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fca682c712d51bb08cb318676c75dfd2f544b9311b7d750ac5046f1a5397ba`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

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
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
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
	-	`sha256:454ec3ba22ac3eb4e1cbe3aced0fb597d9bd1df666b839fb894c6a21d320da25`  
		Last Modified: Wed, 02 Jul 2025 05:14:29 GMT  
		Size: 52.1 MB (52070725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26d30a34f7df5fae8f971d85c94c60ef383378263715aa7f5bdcfda677f1980`  
		Last Modified: Wed, 02 Jul 2025 05:14:23 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868db56d7c15e73a39e43f047129c4bedd8aeda161c8978e45a97148a83fc291`  
		Last Modified: Wed, 02 Jul 2025 05:14:23 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014ad84cc84638e74cad2e56135ad79f37746231afccfdb1290e085941f1fbd6`  
		Last Modified: Wed, 02 Jul 2025 08:43:24 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ed8b7fc10ee151a72a14badb42655c73d8b7b579f3d245852cf26558e5677a`  
		Last Modified: Wed, 02 Jul 2025 11:48:24 GMT  
		Size: 353.6 MB (353635045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511d1fc2bfd4863b626d68cd7e762fe7cdfd7426a19f3063189c63f2dc9d3be7`  
		Last Modified: Wed, 02 Jul 2025 08:43:26 GMT  
		Size: 3.3 MB (3256287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9491337c5d41cf3ea8b71ee5e5ccd3ac518e892726e857f3bc6c8efa3cbc3d`  
		Last Modified: Wed, 02 Jul 2025 08:43:25 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d415553b38bf7ca931b3843e884a80a2fd3c9ea96e6d1e88bbb9ffa65f7e5f`  
		Last Modified: Wed, 02 Jul 2025 08:43:26 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.32.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:9ad5ab55a8ddc2a287b8b0c39ecc08de6efaa1ab55b0be6ab7d0492206faba20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b59f37d3cfcb924da372d216dec932a022ce677ebe1df2666d26acdbf557aff`

```dockerfile
```

-	Layers:
	-	`sha256:1cb10308edf6084115b8c27aa398a0ab730b9403db53d0ce3b68fae04354cc6b`  
		Last Modified: Wed, 02 Jul 2025 09:39:22 GMT  
		Size: 3.9 MB (3940895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:473118d07cc32d36fc44cf67cfcb3a7f70de576325e9856ac98f0b6e40214029`  
		Last Modified: Wed, 02 Jul 2025 09:39:22 GMT  
		Size: 24.5 KB (24540 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.32.0-alpine`

```console
$ docker pull liquibase@sha256:8544830e4ca411eff42eb176feeba1b404f022df03fada5d7f1243e5613bbba6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.32.0-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:4c3e1a080bc81fa4240fd72c354596aa9035b18ae1d11f5309a81761e0372ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.5 MB (428538737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7b5749651c357c25993d3697b04ef5fa5b834c046760608a0d4536d794fbfe`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 15:54:00 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d254e74249fcd7b94a1781e88f1a6f82a7374fa38534597aa8ee73acc6b12d`  
		Last Modified: Tue, 03 Jun 2025 13:43:04 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa601d9e14ea7319081e6f48f04318cfb467678483e4eb561dd15c6c000ed02`  
		Last Modified: Tue, 03 Jun 2025 13:43:09 GMT  
		Size: 67.8 MB (67802051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f4f98b98e0507c8ef049e6fdc0fc8f4f2f478ab1e15be6b91e709938ec82a0`  
		Last Modified: Tue, 03 Jun 2025 13:43:20 GMT  
		Size: 353.7 MB (353659617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd18ba5867df0761825b305d7ba21b9872705937388519a51ad1329cb53d1f6c`  
		Last Modified: Tue, 03 Jun 2025 13:43:06 GMT  
		Size: 3.4 MB (3433209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac55a4e3432c438a4f536d8321a94946d57d9b5824501bf61b37b901169344`  
		Last Modified: Tue, 03 Jun 2025 13:43:07 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa192255813780f3a510a1b0b662e05189ff63a6f1ddb944b58aae60cdf6fa52`  
		Last Modified: Tue, 03 Jun 2025 13:43:08 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.32.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:320a5a919092cea878a339300632114dee3cb4852d0982765a224c5791b9a63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.9 KB (424950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c0383adc941b49fcaf669264535721596363830e5377067e400a337164ace3`

```dockerfile
```

-	Layers:
	-	`sha256:6779fcfccf29fba7d611a59c6a302f2d36f8ffd99ccd7b0c7e93b181855567f3`  
		Last Modified: Wed, 04 Jun 2025 00:04:44 GMT  
		Size: 403.2 KB (403239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1393290584387fe56550a652f4a981566d37297b4d14f5ecce2866124751255`  
		Last Modified: Wed, 04 Jun 2025 00:04:44 GMT  
		Size: 21.7 KB (21711 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.32.0-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:5df3fe840d73b107b6091a70c051919c25807812405031f325c52f22d51a1901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.6 MB (427626574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3b0f528bb29c9d8e983d8da8031c676143f017cf006c9bf956e36a288e1aa2`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 15:54:00 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d960cdd0c49e3498bf6ec7d87b10dad4343563e53b9d8035d65c95c55c52999`  
		Last Modified: Tue, 03 Jun 2025 15:03:02 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925c4a78c555ba3c950941e6d6271896da57b0ddefa6e1c39a006da828657e78`  
		Last Modified: Tue, 03 Jun 2025 15:03:06 GMT  
		Size: 66.8 MB (66799294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e9a29829ca0505af0c82a9601997eaf320d57e44e1a101dde1ee080157a70a`  
		Last Modified: Tue, 03 Jun 2025 15:03:25 GMT  
		Size: 353.7 MB (353659532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac9a8ecf3de910c8dad2c8db151cfb2ea7644281a2e5c4e346d19fb363bd2c0`  
		Last Modified: Tue, 03 Jun 2025 15:03:05 GMT  
		Size: 3.2 MB (3173107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0d2579a1fe9eb19872234ce6821951463ced6acccd74269887d5e646a54856`  
		Last Modified: Tue, 03 Jun 2025 15:03:06 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d372df514f79ee87a3777443c33566eb23a953b6f7af8a4f77fe316d304b83b`  
		Last Modified: Tue, 03 Jun 2025 15:03:07 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.32.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:a2ba65aaa27cd37509f5c48e4d79ad933b55d857b0b3615510dfb819cd69e81c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.3 KB (424333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1708af05fefc0c6be3e00a92e2ab51966d3aef47cfb298abc45fcc5eb99fc70`

```dockerfile
```

-	Layers:
	-	`sha256:de4ebc5acfd594b876bcf89cb72433b4b269d9b314403a4e64410bb4ea06ab0f`  
		Last Modified: Wed, 04 Jun 2025 00:04:49 GMT  
		Size: 402.5 KB (402486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c6aef5a59e7465653b4094cc2fc207c7a0c2dacbee07b2ada9f02a5f7e820d3`  
		Last Modified: Wed, 04 Jun 2025 00:04:49 GMT  
		Size: 21.8 KB (21847 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:8544830e4ca411eff42eb176feeba1b404f022df03fada5d7f1243e5613bbba6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:4c3e1a080bc81fa4240fd72c354596aa9035b18ae1d11f5309a81761e0372ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.5 MB (428538737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7b5749651c357c25993d3697b04ef5fa5b834c046760608a0d4536d794fbfe`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 15:54:00 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d254e74249fcd7b94a1781e88f1a6f82a7374fa38534597aa8ee73acc6b12d`  
		Last Modified: Tue, 03 Jun 2025 13:43:04 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa601d9e14ea7319081e6f48f04318cfb467678483e4eb561dd15c6c000ed02`  
		Last Modified: Tue, 03 Jun 2025 13:43:09 GMT  
		Size: 67.8 MB (67802051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f4f98b98e0507c8ef049e6fdc0fc8f4f2f478ab1e15be6b91e709938ec82a0`  
		Last Modified: Tue, 03 Jun 2025 13:43:20 GMT  
		Size: 353.7 MB (353659617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd18ba5867df0761825b305d7ba21b9872705937388519a51ad1329cb53d1f6c`  
		Last Modified: Tue, 03 Jun 2025 13:43:06 GMT  
		Size: 3.4 MB (3433209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac55a4e3432c438a4f536d8321a94946d57d9b5824501bf61b37b901169344`  
		Last Modified: Tue, 03 Jun 2025 13:43:07 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa192255813780f3a510a1b0b662e05189ff63a6f1ddb944b58aae60cdf6fa52`  
		Last Modified: Tue, 03 Jun 2025 13:43:08 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:320a5a919092cea878a339300632114dee3cb4852d0982765a224c5791b9a63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.9 KB (424950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c0383adc941b49fcaf669264535721596363830e5377067e400a337164ace3`

```dockerfile
```

-	Layers:
	-	`sha256:6779fcfccf29fba7d611a59c6a302f2d36f8ffd99ccd7b0c7e93b181855567f3`  
		Last Modified: Wed, 04 Jun 2025 00:04:44 GMT  
		Size: 403.2 KB (403239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1393290584387fe56550a652f4a981566d37297b4d14f5ecce2866124751255`  
		Last Modified: Wed, 04 Jun 2025 00:04:44 GMT  
		Size: 21.7 KB (21711 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:5df3fe840d73b107b6091a70c051919c25807812405031f325c52f22d51a1901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.6 MB (427626574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3b0f528bb29c9d8e983d8da8031c676143f017cf006c9bf956e36a288e1aa2`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 15:54:00 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase --home /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
RUN apk add --no-cache openjdk21-jre-headless bash # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image (Alpine)
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d960cdd0c49e3498bf6ec7d87b10dad4343563e53b9d8035d65c95c55c52999`  
		Last Modified: Tue, 03 Jun 2025 15:03:02 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925c4a78c555ba3c950941e6d6271896da57b0ddefa6e1c39a006da828657e78`  
		Last Modified: Tue, 03 Jun 2025 15:03:06 GMT  
		Size: 66.8 MB (66799294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e9a29829ca0505af0c82a9601997eaf320d57e44e1a101dde1ee080157a70a`  
		Last Modified: Tue, 03 Jun 2025 15:03:25 GMT  
		Size: 353.7 MB (353659532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac9a8ecf3de910c8dad2c8db151cfb2ea7644281a2e5c4e346d19fb363bd2c0`  
		Last Modified: Tue, 03 Jun 2025 15:03:05 GMT  
		Size: 3.2 MB (3173107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0d2579a1fe9eb19872234ce6821951463ced6acccd74269887d5e646a54856`  
		Last Modified: Tue, 03 Jun 2025 15:03:06 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d372df514f79ee87a3777443c33566eb23a953b6f7af8a4f77fe316d304b83b`  
		Last Modified: Tue, 03 Jun 2025 15:03:07 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:a2ba65aaa27cd37509f5c48e4d79ad933b55d857b0b3615510dfb819cd69e81c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.3 KB (424333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1708af05fefc0c6be3e00a92e2ab51966d3aef47cfb298abc45fcc5eb99fc70`

```dockerfile
```

-	Layers:
	-	`sha256:de4ebc5acfd594b876bcf89cb72433b4b269d9b314403a4e64410bb4ea06ab0f`  
		Last Modified: Wed, 04 Jun 2025 00:04:49 GMT  
		Size: 402.5 KB (402486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c6aef5a59e7465653b4094cc2fc207c7a0c2dacbee07b2ada9f02a5f7e820d3`  
		Last Modified: Wed, 04 Jun 2025 00:04:49 GMT  
		Size: 21.8 KB (21847 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:latest`

```console
$ docker pull liquibase@sha256:d5df8530bf4aca64c58c6cc76d7f47a091c33e125ef57b5ca27091e26df6dd78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:f7cef26c451edbf8265868fa28343564902ee4aba6c24cfc92c1603b403d5093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.7 MB (455730593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fc0482bba604856ceabfff676c4e3d753e35d92ec810515606735dba1f47ec`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

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
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33e8ebdb86dc7a920582c649882465543cb59ccf43a509416f6e6e7905183e6`  
		Last Modified: Wed, 02 Jul 2025 03:10:24 GMT  
		Size: 16.1 MB (16146378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71b536eab81d4b1b3e2c1fee8daf4304d1ea62a32cb23772727c219e1eee6ef`  
		Last Modified: Wed, 02 Jul 2025 03:10:27 GMT  
		Size: 52.9 MB (52891244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4112c5be290bc12057463f12fff689c8cae27c00c7e0f639f94d285ce9c4cdd`  
		Last Modified: Wed, 02 Jul 2025 03:10:23 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab0fa3d848a3c661740f09af88f10cc5a3cea13e177c94dfa483136ab23ad42`  
		Last Modified: Wed, 02 Jul 2025 03:10:23 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4221402984ed91e2323ad4c3ea7503cbdc207e3bcb215e3f72f2424709e590`  
		Last Modified: Wed, 02 Jul 2025 05:57:43 GMT  
		Size: 4.3 KB (4304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2890eb5cdd67d9228eab0a66c4eb3cab98288fe7e4be2c18d325624b453419`  
		Last Modified: Wed, 02 Jul 2025 06:41:53 GMT  
		Size: 353.6 MB (353635050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630c3a76138589d62bc5db897cf3784da16c8cc94c01379f675f35ecee32fbd1`  
		Last Modified: Wed, 02 Jul 2025 05:57:48 GMT  
		Size: 3.5 MB (3514812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbabe9a5ea5fd781a1ddc2f096a7d61602a1233b6417b6eeaaf018382c8046c9`  
		Last Modified: Wed, 02 Jul 2025 05:57:53 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3202c5d42df6efa13c57b177bccacddf924ffe7dd88bed9134406c3eb33bcf8d`  
		Last Modified: Wed, 02 Jul 2025 05:57:56 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:fe91ff3201f12e409bd1678cb63991ef17b9c4e32028918d8c7d9e1ef64f6f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff89097dffb4499abeb139e22a20399aaafb9f41996d8f8460bff08d38dae1bf`

```dockerfile
```

-	Layers:
	-	`sha256:8832828d64492e7685bb772e719a0788d8d15c41b2e00f31600c970ba4936fe6`  
		Last Modified: Wed, 02 Jul 2025 06:39:20 GMT  
		Size: 3.9 MB (3941227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e934b50993475d108c4bd75a6144f3493a4863d000f444fbecec35cb0c9366e`  
		Last Modified: Wed, 02 Jul 2025 06:39:21 GMT  
		Size: 24.4 KB (24418 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:28f7505f8037db07ed7d72026b2c3cb94df8981be380306832cefa705bcd3706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.4 MB (452388643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fca682c712d51bb08cb318676c75dfd2f544b9311b7d750ac5046f1a5397ba`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

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
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase --create-home --home-dir /liquibase liquibase &&     chown liquibase /liquibase # buildkit
# Fri, 23 May 2025 15:54:00 GMT
WORKDIR /liquibase
# Fri, 23 May 2025 15:54:00 GMT
ARG LIQUIBASE_VERSION=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
ARG LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_VERSION=0.2.9
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a
# Fri, 23 May 2025 15:54:00 GMT
ARG LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.description=Liquibase Container Image
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.vendor=Liquibase
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.version=4.32.0
# Fri, 23 May 2025 15:54:00 GMT
LABEL org.opencontainers.image.documentation=https://docs.liquibase.com
# Fri, 23 May 2025 15:54:00 GMT
# ARGS: LIQUIBASE_VERSION=4.32.0 LB_SHA256=10910d42ae9990c95a4ac8f0a3665a24bd40d08fb264055d78b923a512774d54 LPM_VERSION=0.2.9 LPM_SHA256=b9caecd34c98a6c19a2bc582e8064aff5251c5f1adbcd100d3403c5eceb5373a LPM_SHA256_ARM=0adb3a96d7384b4da549979bf00217a8914f0df37d1ed8fdb1b4a4baebfa104c
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in     amd64)  DOWNLOAD_ARCH=""  ;;     arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;     *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 23 May 2025 15:54:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENV DOCKER_LIQUIBASE=true
# Fri, 23 May 2025 15:54:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 23 May 2025 15:54:00 GMT
USER liquibase:liquibase
# Fri, 23 May 2025 15:54:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 23 May 2025 15:54:00 GMT
CMD ["--help"]
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
	-	`sha256:454ec3ba22ac3eb4e1cbe3aced0fb597d9bd1df666b839fb894c6a21d320da25`  
		Last Modified: Wed, 02 Jul 2025 05:14:29 GMT  
		Size: 52.1 MB (52070725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26d30a34f7df5fae8f971d85c94c60ef383378263715aa7f5bdcfda677f1980`  
		Last Modified: Wed, 02 Jul 2025 05:14:23 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868db56d7c15e73a39e43f047129c4bedd8aeda161c8978e45a97148a83fc291`  
		Last Modified: Wed, 02 Jul 2025 05:14:23 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014ad84cc84638e74cad2e56135ad79f37746231afccfdb1290e085941f1fbd6`  
		Last Modified: Wed, 02 Jul 2025 08:43:24 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ed8b7fc10ee151a72a14badb42655c73d8b7b579f3d245852cf26558e5677a`  
		Last Modified: Wed, 02 Jul 2025 11:48:24 GMT  
		Size: 353.6 MB (353635045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511d1fc2bfd4863b626d68cd7e762fe7cdfd7426a19f3063189c63f2dc9d3be7`  
		Last Modified: Wed, 02 Jul 2025 08:43:26 GMT  
		Size: 3.3 MB (3256287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9491337c5d41cf3ea8b71ee5e5ccd3ac518e892726e857f3bc6c8efa3cbc3d`  
		Last Modified: Wed, 02 Jul 2025 08:43:25 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d415553b38bf7ca931b3843e884a80a2fd3c9ea96e6d1e88bbb9ffa65f7e5f`  
		Last Modified: Wed, 02 Jul 2025 08:43:26 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:9ad5ab55a8ddc2a287b8b0c39ecc08de6efaa1ab55b0be6ab7d0492206faba20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b59f37d3cfcb924da372d216dec932a022ce677ebe1df2666d26acdbf557aff`

```dockerfile
```

-	Layers:
	-	`sha256:1cb10308edf6084115b8c27aa398a0ab730b9403db53d0ce3b68fae04354cc6b`  
		Last Modified: Wed, 02 Jul 2025 09:39:22 GMT  
		Size: 3.9 MB (3940895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:473118d07cc32d36fc44cf67cfcb3a7f70de576325e9856ac98f0b6e40214029`  
		Last Modified: Wed, 02 Jul 2025 09:39:22 GMT  
		Size: 24.5 KB (24540 bytes)  
		MIME: application/vnd.in-toto+json
