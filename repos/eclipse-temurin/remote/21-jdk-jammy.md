## `eclipse-temurin:21-jdk-jammy`

```console
$ docker pull eclipse-temurin@sha256:6031628cab60fc7fdde26078ab21990cbd2c07768ab6519d95d530f6a1a66cb0
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

### `eclipse-temurin:21-jdk-jammy` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:539ada1d298e7a57bd81e9cd40d445577df89ff289f554154e6bf2226ab4ca93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207813701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca3d523cce782820b0df77179d5d9082fefbcfd4dbccbfdb34f050f27e4f793`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75721edc691669742efeb417edb7ed501690ec4402441b25ea444d7a9f5da8a8`  
		Last Modified: Fri, 31 Jan 2025 01:31:28 GMT  
		Size: 20.7 MB (20684329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76b3bc1ca13c77b9b87b437ef0dcc6a70a6cf450b2affe450f99461ca635e5b`  
		Last Modified: Fri, 31 Jan 2025 01:31:32 GMT  
		Size: 157.6 MB (157591241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b925bc590a44343b3bd87f1b65193cd17708915c7b3277f55e65d7a475f182d`  
		Last Modified: Fri, 31 Jan 2025 01:31:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1b05cc1428174c85976faa7b269d4951e294e1a760fa55dfe044b5c39fe2ec`  
		Last Modified: Fri, 31 Jan 2025 01:31:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4fa69341a502d9cac230bf9ce43c6427776f43ab266dcbf74c3491bf00754fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3972796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f76583ee38cadcc2888aa83e246576508d89f934a29171c2d363a814e8a63e`

```dockerfile
```

-	Layers:
	-	`sha256:54e7ff12dbf67b97c663295f01c6685eeba197bb88af1ed110bc4c4891fc2a23`  
		Last Modified: Fri, 31 Jan 2025 01:31:28 GMT  
		Size: 3.9 MB (3949679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16e79c034754f40b30b8a6ffb093b8c18c41ab8937c4bec5bc84648180ee0a02`  
		Last Modified: Fri, 31 Jan 2025 01:31:27 GMT  
		Size: 23.1 KB (23117 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-jammy` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:d49c78332d7ef2e696d623e798e952fee6acef543682971f1bd7d134445add25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205302403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c373a22e2b30d8c09fa3a7cdba4e6e771e1dc18753e229eac0959a54bd82c2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b6b0c7bb7379413ae307e29619a183adb45a83f4e6a69bca92d486a6c0eb5`  
		Last Modified: Wed, 22 Jan 2025 21:02:59 GMT  
		Size: 22.1 MB (22073764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912ca86ed0ad29c692b2d254c6855a7028b401640f61de65d079d14672505ba5`  
		Last Modified: Fri, 31 Jan 2025 01:45:52 GMT  
		Size: 155.9 MB (155867867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae5e26d2bfa3953ad91d843572cef37bedfb318e16ccac1ad9667976aa4a506`  
		Last Modified: Fri, 31 Jan 2025 01:45:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb2241531fc07f2088c8dad5ebbaf5f3bc4235716ee96ae70cb7fed32b86425`  
		Last Modified: Fri, 31 Jan 2025 01:45:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8bc8e370738bcbabc5d1fdea77a09996b67fc722dce01251a8a2da41d2e86f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4070263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22401b0885fc7f4c67076101c7e061a496ed3569919c699c170b256e93bf84f`

```dockerfile
```

-	Layers:
	-	`sha256:a4a47911fcb2dbc21b8bd644e025caf4ab02e43b274cf65074a72203c227c4c3`  
		Last Modified: Fri, 31 Jan 2025 01:45:48 GMT  
		Size: 4.0 MB (4047024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05144af496fff657d1ccd2c16f6ee1c4c0793f38218d6b07df8d9d2e2038ef7d`  
		Last Modified: Fri, 31 Jan 2025 01:45:47 GMT  
		Size: 23.2 KB (23239 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-jammy` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:bf5a9e8eb4b1665380ac1e8b1c5e6a80bbe1e4e4074ead305c1798407832bf51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214822013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ba8b1c7f10337ebe8306b78ce3f1c14bbd6462869cfcad6e144adba62a58ad`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9961d7af46e094ce3635c980e9e4eee0f1cd02b303482b9abc32ec7d1e7ea3a6`  
		Last Modified: Wed, 22 Jan 2025 18:44:59 GMT  
		Size: 22.6 MB (22614469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35089902caf04e4b2fd2be21e3dc93ad0e89c7bd1a67d86fa1e421632ee0bc41`  
		Last Modified: Fri, 31 Jan 2025 04:54:57 GMT  
		Size: 157.8 MB (157756859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba689cf4594add9242f233008cfb1a4ed319e8b46543373b0bb486ad83a7a3f`  
		Last Modified: Fri, 31 Jan 2025 04:54:53 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea8ce726ff3b5d9ca743af55a049013422d491f0ea55ee826c6b13453108860`  
		Last Modified: Fri, 31 Jan 2025 04:54:53 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:83eba9304499a8b59f7a3d1a033c51d676ee57ce5d07b0d07f811565d218ccee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4002101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7dcc7c912c00c806579a74106f8f93beded0906abaf8d825c3eda65bfde822`

```dockerfile
```

-	Layers:
	-	`sha256:c3ac8099c7162bd5158715a0eb98183e8c2c30689f001662666741baebb897e2`  
		Last Modified: Fri, 31 Jan 2025 04:54:53 GMT  
		Size: 4.0 MB (3978942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed4a6f32668b3f579c2890e51b52e2654a6c91737867559294bebc6fa911f623`  
		Last Modified: Fri, 31 Jan 2025 04:54:53 GMT  
		Size: 23.2 KB (23159 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-jammy` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:769cf604642e1584c2d93a36ddd0eabcdb57848c483652555a8879d7224b9003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195290974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13564cef4bac08c96f46c32389fbdf161310cc49b72280be2023b4bc167481f5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90692d310114b008dc7ca0b8cda6472c2e3918b64268e79fba6745a9e0813d73`  
		Last Modified: Wed, 22 Jan 2025 21:54:12 GMT  
		Size: 20.4 MB (20415586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6470824992053c3500652988daf48a54e4791bb820e4cbc6c7aa992167aa8d08`  
		Last Modified: Fri, 31 Jan 2025 01:46:51 GMT  
		Size: 146.9 MB (146871473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86a7cd57cd5ca4c194c36d0c4e178e8cc7dcd7eab02f7e9fff57359f683b26b`  
		Last Modified: Fri, 31 Jan 2025 01:46:48 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54b0eb293471c2dd5f6e2009d1f9308831dbd710db195a48666a78efb3fbb81`  
		Last Modified: Fri, 31 Jan 2025 01:46:48 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9e1ba4615b43b57fb546507862da2a2a898ca40e79685e2766b1e88aa2f64e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3899668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c7bd89b8f3354a4a868599814c81de632123b962f18d284fb5366c479b22b1`

```dockerfile
```

-	Layers:
	-	`sha256:cb0719092b2f648712548829b78fad157b3e7e776e7d66ff7141dd7ec8c587be`  
		Last Modified: Fri, 31 Jan 2025 01:46:48 GMT  
		Size: 3.9 MB (3876552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b58de1fd1e56dda561214bfd01a67ef1dd41fcf3fef7b681a6c738b235071ac`  
		Last Modified: Fri, 31 Jan 2025 01:46:48 GMT  
		Size: 23.1 KB (23116 bytes)  
		MIME: application/vnd.in-toto+json
