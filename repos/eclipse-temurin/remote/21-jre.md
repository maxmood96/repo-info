## `eclipse-temurin:21-jre`

```console
$ docker pull eclipse-temurin@sha256:ff7e4a51821d2ceee20fa05064da366f3c12be8ed18596dd2ad0999b2af3fea0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:21-jre` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:3bfbe36c89e9998df7f467fc89b9ae2e0701b3d5cbf6805bc5e74915ee4b3dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108188249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d6701a1142c4c95274de8e3dcb97b3377d8e3c4ee19f2a2eb53ffa7af522d0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:20:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:20:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:20:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:20:58 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 22:20:58 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:21:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='02cf763836c14bad4d689eb3b4efd691657de753dba07193cd1fb8691c8fe7b8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 05 Feb 2026 22:21:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:21:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:21:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91ec9501b8be4038f449ffdd4f9f2118ef6face010abf1cef803d884108b5da`  
		Last Modified: Thu, 05 Feb 2026 22:21:15 GMT  
		Size: 25.5 MB (25474314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e3becec303f71b88d9261905972c4527873aad3b31422611b3f4a46c473095`  
		Last Modified: Thu, 05 Feb 2026 22:21:16 GMT  
		Size: 53.0 MB (52985484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ad9cbcbb221583b3d91593e8ddd142ecec5226c611e49399e9480f98be934d`  
		Last Modified: Thu, 05 Feb 2026 22:21:14 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046361bb63334104dabf096b8730d1614b34fdb6b7607c70063ae2f2eb81956f`  
		Last Modified: Thu, 05 Feb 2026 22:21:14 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c1005a1affae93b0dab58c72263734d4435062e89f55a030c7298f5cffab397f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3311016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43181f0bf2556c4a878112703b3baa05fec2bc877abb15efc4261a8c12f0dd27`

```dockerfile
```

-	Layers:
	-	`sha256:f899aceb25139b39948aa1a1d4cd5b860f496326f78af838dc2d498a831ea38b`  
		Last Modified: Thu, 05 Feb 2026 22:21:14 GMT  
		Size: 3.3 MB (3287865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c678a9be259253ecc747847b27a5561c032703dc6bb0cda2918eab05392add72`  
		Last Modified: Thu, 05 Feb 2026 22:21:14 GMT  
		Size: 23.2 KB (23151 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:fe8f0949ccb1bd3453c9042e96433f35b467a95a46120e9aaf36a3e894333e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 MB (106091417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c8163b8c687e773b4bd83d5ae2fde969be1a3904f455e23f500b3840544f46`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:20:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:20:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:20:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:20:00 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 22:20:00 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:20:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='02cf763836c14bad4d689eb3b4efd691657de753dba07193cd1fb8691c8fe7b8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 05 Feb 2026 22:20:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:20:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:20:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54eb73ad2098189ee70ae47bca0f8adb386a6e22c6bd1bf1905ac973365e70f8`  
		Last Modified: Thu, 05 Feb 2026 22:20:17 GMT  
		Size: 25.1 MB (25069489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9ffb10b0c48a26ad38a341bc5dc308edb7754f3441a87e549951b1c9c52bc9`  
		Last Modified: Thu, 05 Feb 2026 22:20:18 GMT  
		Size: 52.2 MB (52155663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6f77023edfdbfe6f401e91bc8439f85db1b462664c7c3aae877ba4df8d7df`  
		Last Modified: Thu, 05 Feb 2026 22:20:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616fa20b50908f47baf72d0006de80ad9488b904484955d5df94a41a5ae7032d`  
		Last Modified: Thu, 05 Feb 2026 22:20:10 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6fea6999897d80c655ee25f207ce589a0a294b1bb36cd6bcc8f05b03afad4be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3311623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8974a236878f00bb951a6448735038ecf0d76f7746817a1eb615239aeeba741f`

```dockerfile
```

-	Layers:
	-	`sha256:f1cf32254aa906db25a75c07ee8af32f07e1d08c04a4bfc88b13ecfa009ce87a`  
		Last Modified: Thu, 05 Feb 2026 22:20:16 GMT  
		Size: 3.3 MB (3288336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6c2d046addacbfc83b387724deb1645464c1e243befd2869bcc853931a3715a`  
		Last Modified: Thu, 05 Feb 2026 22:20:16 GMT  
		Size: 23.3 KB (23287 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:aef7d640d63806a7b7fb1f58d1570c631a1ec4bf1cacd801c117149ab85ca6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115587751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21645e1afcda42c670cc996f71874412db66155dbec7382864ee8d1316b07a7f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:15:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:15:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:15:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:15:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 22:15:06 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:29:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='02cf763836c14bad4d689eb3b4efd691657de753dba07193cd1fb8691c8fe7b8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 05 Feb 2026 22:29:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:29:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:29:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4438ac1f4b9f9f88cf7d7982d911db40f34e73f7406e5ec71ff6bebd876883`  
		Last Modified: Thu, 05 Feb 2026 22:15:40 GMT  
		Size: 28.3 MB (28306219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fcbbaee8cb611cbe9d293f924ac2f9da06cb635d9f1ef4e9665c6d56ba1a37`  
		Last Modified: Thu, 05 Feb 2026 22:30:17 GMT  
		Size: 53.0 MB (52972932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff34006553bddde2b18ee90495382bc34dc3ea5322e6eabefb4dd3308170c4b`  
		Last Modified: Thu, 05 Feb 2026 22:30:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbdd4ffd49c0ff8ba306f244897e503802cf9e8a53ba08de073468e6d8cef9a`  
		Last Modified: Thu, 05 Feb 2026 22:30:15 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:71e9b07e7dcdeacecca8f3aa6f26f2c0b89c7750b3ee597a982d034b707791c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3315134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546c311a9a59b093f87c34935f9bf162d0fec6c1c46f3e618b3f8554c2b23d88`

```dockerfile
```

-	Layers:
	-	`sha256:73c7197af07ea0a776ccd892ca01f43dabf03ee45edb9ff8580b73ab0f7859e0`  
		Last Modified: Thu, 05 Feb 2026 22:30:15 GMT  
		Size: 3.3 MB (3291933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8574fc9fe9a3ea962d9f7cf5ff4a4ebab7f97aa1c39662a808292397d426f4b4`  
		Last Modified: Thu, 05 Feb 2026 22:30:15 GMT  
		Size: 23.2 KB (23201 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre` - linux; riscv64

```console
$ docker pull eclipse-temurin@sha256:a7dfd92f0d49f57b904cfc5930f00ac750d32bed6676d6eaf76c6ba2f9343322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101341180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2ebf98f08e6309ec7e21b48cffadf3851fb3155cb0f57cb441522a7dba9c73`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 13 Jan 2026 06:14:56 GMT
ARG RELEASE
# Tue, 13 Jan 2026 06:14:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 06:14:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 06:14:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 06:15:46 GMT
ADD file:8d0655de001e92042901c645c76202ac355acb6fa186561e7344a0829ffd983d in / 
# Tue, 13 Jan 2026 06:15:51 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 18:15:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 19 Jan 2026 18:15:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Jan 2026 18:15:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 19 Jan 2026 18:15:58 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Jan 2026 18:15:58 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Sun, 08 Feb 2026 00:25:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='02cf763836c14bad4d689eb3b4efd691657de753dba07193cd1fb8691c8fe7b8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 08 Feb 2026 00:25:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 08 Feb 2026 00:25:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 08 Feb 2026 00:25:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f151392858868452ec0f1f8d2947624e8dcdecf23bce587cfbd7c38a3264f9df`  
		Last Modified: Tue, 13 Jan 2026 06:36:06 GMT  
		Size: 31.0 MB (30953090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2124fa260d30e6ed877bf1d814aaa3c0d40ce2616e00d34c047a094bb9a874`  
		Last Modified: Mon, 19 Jan 2026 18:18:39 GMT  
		Size: 17.9 MB (17863891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03e4decd514a5f658706102a9c9d1bbbfcd8f197555fa190c64b41e3dcc0f31`  
		Last Modified: Sun, 08 Feb 2026 00:28:06 GMT  
		Size: 52.5 MB (52521757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24227a4b4ad50734bf6d83ed9f3ed8aee526cee84ccb8806f487fad7724b5873`  
		Last Modified: Sun, 08 Feb 2026 00:27:56 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96c1cc71a4d47a3c0a56b520d9783a06e9f405c616969a9665057482c9d2b80`  
		Last Modified: Sun, 08 Feb 2026 00:27:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:db4f896ded3fca0718c6904367e168218779e0b648fa317e8c3fefce8f95a3be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3303132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29892c98782ade629b016cfd76090a664ac5756b3a49bc7f1187c56bdcc2e5e5`

```dockerfile
```

-	Layers:
	-	`sha256:2c3d6766e54fec70877bfc360e92eab64f44c64405ea2afa9929ee7e6240d3b8`  
		Last Modified: Sun, 08 Feb 2026 00:27:57 GMT  
		Size: 3.3 MB (3279931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ec0d75e36a33b4e23b48b6487604a90b31d01c1df16742451ba47f09f62f05b`  
		Last Modified: Sun, 08 Feb 2026 00:27:56 GMT  
		Size: 23.2 KB (23201 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:bf24be0e5a0c620e757bdaa7c1fd4b8a1e2361f868100ba2d828c4dbdfdb499b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104360197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e57ef7e54312a46d98e432898ece4518203b0082abf92ccb80e17f1045df48`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 13 Jan 2026 06:29:20 GMT
ARG RELEASE
# Tue, 13 Jan 2026 06:29:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 06:29:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 06:29:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 06:29:22 GMT
ADD file:55a7874afa0094b7b4c6edc68b58164a34177fa761bc6e673ddb0c846b91f26f in / 
# Tue, 13 Jan 2026 06:29:22 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:14:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:14:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:14:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:14:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 22:14:34 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:22:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='02cf763836c14bad4d689eb3b4efd691657de753dba07193cd1fb8691c8fe7b8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 05 Feb 2026 22:22:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:22:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:22:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:88318e41cf944fd93c8b2fdfaeb1378b17ed0e2440ef9811f9820449bf19a6ad`  
		Last Modified: Tue, 13 Jan 2026 06:36:13 GMT  
		Size: 29.9 MB (29909204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed8a0d81f07036f2636d2db8bd0e36e71a8f6dbcf7a37f1b36c0626dbefb1a7`  
		Last Modified: Thu, 05 Feb 2026 22:15:39 GMT  
		Size: 24.9 MB (24907637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6da10d035e92d98eee18b1bd960d9627205c06082ecd30cebffefa5ae32a85`  
		Last Modified: Thu, 05 Feb 2026 22:22:59 GMT  
		Size: 49.5 MB (49540914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d783c1bdf8f482737be2ed07a29d4b3d060fe833b5bcda43bba2d1575308ef8`  
		Last Modified: Thu, 05 Feb 2026 22:22:58 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4418c160e1a513744f0b74746b9d7685b37fdae978e7f90e9aa8e1758ed85f0a`  
		Last Modified: Thu, 05 Feb 2026 22:22:57 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:13955ebaf1e2a31c1361c53e9a55e5cd5de5be622fa0f9ec613b3a1bc305c5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3313218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2acccd74d1db0892daf2e18248d426145863ec28e6dc4bba720b23b1f6acd4a`

```dockerfile
```

-	Layers:
	-	`sha256:aa1955d0b81a03eee822ac6ec38cdcfba0b007c977015215b4869fd0ab4b16df`  
		Last Modified: Thu, 05 Feb 2026 22:22:58 GMT  
		Size: 3.3 MB (3290065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed133cfc09bdcfa47f398e78956eb2be056b1cc19a8ab777e1cf93cb6da5171`  
		Last Modified: Thu, 05 Feb 2026 22:22:57 GMT  
		Size: 23.2 KB (23153 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:bb71ce1f084d46264d7a38dfbc92345c501efe9d239acc7ba76b54efee993c6c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1579807293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2acd2d6fc644ce098d10193c3ae5e186a1c564be6c14c427776adc080e723b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Thu, 05 Feb 2026 22:18:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Feb 2026 22:18:17 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:19:02 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_windows_hotspot_21.0.10_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_windows_hotspot_21.0.10_7.msi ;     Write-Host ('Verifying sha256 (a841118d4959b6b6eb6156fa1f2487f112afaecd124b1eb5bba203d5556efd32) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'a841118d4959b6b6eb6156fa1f2487f112afaecd124b1eb5bba203d5556efd32') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 05 Feb 2026 22:19:09 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b601f27219bae14205bab18eeffef90c3004cc219b406781f227b617c4d9e96`  
		Last Modified: Thu, 05 Feb 2026 22:19:13 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db8e9290e5571671281ca93c0d0278b55ce92d28e33a7e95472d10ed4e2d0fa`  
		Last Modified: Thu, 05 Feb 2026 22:19:13 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88676e38263396098bd94c62cf8a4b4e16396a1a4c43009e34ca1cbd84de0fa3`  
		Last Modified: Thu, 05 Feb 2026 22:19:22 GMT  
		Size: 83.6 MB (83645339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04da68c497fa91d52031b63b27cf9f61180e943fc4d838d13a3de4524efd9d37`  
		Last Modified: Thu, 05 Feb 2026 22:19:13 GMT  
		Size: 399.0 KB (398992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:a859c53890e73417507a5fe51e1d7605fd9fc077450239fd1f4ae2856ef7f017
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1919784872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b85c781553e04125719ccbb1758f13457d8711efcc6d6b123b9544ba4b869c5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Thu, 05 Feb 2026 22:15:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Feb 2026 22:23:18 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:23:35 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_windows_hotspot_21.0.10_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_windows_hotspot_21.0.10_7.msi ;     Write-Host ('Verifying sha256 (a841118d4959b6b6eb6156fa1f2487f112afaecd124b1eb5bba203d5556efd32) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'a841118d4959b6b6eb6156fa1f2487f112afaecd124b1eb5bba203d5556efd32') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 05 Feb 2026 22:23:41 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21173afceaa1d09b3f3f4b9c1c2664db824e745b9cacafb8be63e9c677fdfa78`  
		Last Modified: Thu, 05 Feb 2026 22:16:57 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27f178320fdd6c297066830d286182c61796f501b5dab94d6cca81d2deb22f8`  
		Last Modified: Thu, 05 Feb 2026 22:23:45 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea9db5d28f8bd0bad1844ba1e2e140dbad1465849799965371096a3d5b68e5b`  
		Last Modified: Thu, 05 Feb 2026 22:23:52 GMT  
		Size: 83.8 MB (83756045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d427b36391d8d79bc11a1bada65463b09b8fa9604b7b795031b56bef3e505da0`  
		Last Modified: Thu, 05 Feb 2026 22:23:45 GMT  
		Size: 367.0 KB (367040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
