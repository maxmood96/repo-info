## `eclipse-temurin:24-jre`

```console
$ docker pull eclipse-temurin@sha256:aa318a794b211fab9917c1aef2f670eb28d5c073f16edd3b72a0f0349c99f130
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
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64

### `eclipse-temurin:24-jre` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:3896432d43b0513821e38e9d7abfbe505057c55024fc63d7ca942f2ffc4007b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105886251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a238247dc9bc2b5d8fccee462e0b4d1815d3127fa683662ef40877475d99a0f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='88fb6ad6477ca160a554c8e636c4aa2096f6424828a7e1d90464e105df882875';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_x64_linux_hotspot_24.0.1_9.tar.gz';          ;;        arm64)          ESUM='ef2841ac661b18554961da14ae39ce7fec795fb53f6d52f0df3736c95db42e70';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_aarch64_linux_hotspot_24.0.1_9.tar.gz';          ;;        ppc64el)          ESUM='8f24261481d61470c636ba3698ab8ebd697ab6b766ce468f82513eb60dfb48b9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_ppc64le_linux_hotspot_24.0.1_9.tar.gz';          ;;        riscv64)          ESUM='f61ecea7d2b74036b51ba5f173137344ea3909c92eebe75a1f2b0ecec2037fa0';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_riscv64_linux_hotspot_24.0.1_9.tar.gz';          ;;        s390x)          ESUM='54548139feb80d2368f9ebaf1e86ea38b99cc9411c1c641b2acf9f901aedaba2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_s390x_linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5c9fa822a1e8a7b8767f61a925e4a996fade279ca52d981b06e88905d33482`  
		Last Modified: Thu, 08 May 2025 17:09:06 GMT  
		Size: 15.3 MB (15338098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98bd733c050b30d0df45ad49c8b01c62ae64506173966c5c5f6fdcc1576b8a0`  
		Last Modified: Thu, 08 May 2025 17:09:14 GMT  
		Size: 60.8 MB (60828309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141779bd67f4ce6dfe1c84578df8cfa3a860859d4ed985965e00660f8404b05f`  
		Last Modified: Thu, 08 May 2025 17:04:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ef7ec32c081a1ef9fa55232ddce50f98a84a0cc6691982732e11e3021a5f8a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3088632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8928974b412f45993930e1cf108094f02ef06225fda304c67e0a0dca0a112aa7`

```dockerfile
```

-	Layers:
	-	`sha256:bd4665675d61554823a8758cd54fd87169911a3e75491589c1cd32883a4907f1`  
		Last Modified: Mon, 05 May 2025 16:34:56 GMT  
		Size: 3.1 MB (3065720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caa80d07ca2185cab777f2332a320bfd7f0341295443455c6074b0edb9a7a20b`  
		Last Modified: Mon, 05 May 2025 16:34:56 GMT  
		Size: 22.9 KB (22912 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:3b193a0d89c0ae4f7b8a0a774d230549b1ae176da1cfbe8d545ff233cef7376e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104063204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910f73be29f7b1e1965bc8974fe61c58c1a75773a5e266c08e5c4aed6ec413bb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='88fb6ad6477ca160a554c8e636c4aa2096f6424828a7e1d90464e105df882875';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_x64_linux_hotspot_24.0.1_9.tar.gz';          ;;        arm64)          ESUM='ef2841ac661b18554961da14ae39ce7fec795fb53f6d52f0df3736c95db42e70';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_aarch64_linux_hotspot_24.0.1_9.tar.gz';          ;;        ppc64el)          ESUM='8f24261481d61470c636ba3698ab8ebd697ab6b766ce468f82513eb60dfb48b9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_ppc64le_linux_hotspot_24.0.1_9.tar.gz';          ;;        riscv64)          ESUM='f61ecea7d2b74036b51ba5f173137344ea3909c92eebe75a1f2b0ecec2037fa0';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_riscv64_linux_hotspot_24.0.1_9.tar.gz';          ;;        s390x)          ESUM='54548139feb80d2368f9ebaf1e86ea38b99cc9411c1c641b2acf9f901aedaba2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_s390x_linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fddf8a7a3bbd646657770856cf62ec3fb98ad88c54c4e98bcbaeead97ebe93b`  
		Last Modified: Thu, 08 May 2025 18:20:02 GMT  
		Size: 15.3 MB (15330839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77408f1e10df562269935cec77f7452fadf3672e218207219228326801626294`  
		Last Modified: Thu, 08 May 2025 18:20:12 GMT  
		Size: 59.9 MB (59883175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5083d3f7cc361fb55ca815fa295919f60b1a59a56609227a331b352c09583166`  
		Last Modified: Thu, 08 May 2025 18:20:01 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:dfd9142e6159779593ebe37cad26c6e20d9cf5f5d2f37a2f90617da9c5efc3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3089224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99bed7f0f3f8471012bad67e0d4cd23e875945b4ab0f98be1c9c98159aac9edc`

```dockerfile
```

-	Layers:
	-	`sha256:117f437374fe23027a39da6b9ebc603c27d5a9daf59e3e7df30264730d7df567`  
		Last Modified: Mon, 05 May 2025 16:59:59 GMT  
		Size: 3.1 MB (3066178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9964dd2adf822a007ac0ce11afbf2830b181adf045df07f27cf4fdb899f5997`  
		Last Modified: Mon, 05 May 2025 16:59:59 GMT  
		Size: 23.0 KB (23046 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:e84a802e37f2250f3a8be4239c24bda36ea3220f92568321fce63a8c76dbb028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111770451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6861f9e6a681b4a28ff2d71bd903bc495c3f8af4c742242392aede6e760ace9c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:d4d363297b0bc97147d6215ececd915564f3540c035d4c68fcdd781acaf0e4e7 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='88fb6ad6477ca160a554c8e636c4aa2096f6424828a7e1d90464e105df882875';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_x64_linux_hotspot_24.0.1_9.tar.gz';          ;;        arm64)          ESUM='ef2841ac661b18554961da14ae39ce7fec795fb53f6d52f0df3736c95db42e70';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_aarch64_linux_hotspot_24.0.1_9.tar.gz';          ;;        ppc64el)          ESUM='8f24261481d61470c636ba3698ab8ebd697ab6b766ce468f82513eb60dfb48b9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_ppc64le_linux_hotspot_24.0.1_9.tar.gz';          ;;        riscv64)          ESUM='f61ecea7d2b74036b51ba5f173137344ea3909c92eebe75a1f2b0ecec2037fa0';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_riscv64_linux_hotspot_24.0.1_9.tar.gz';          ;;        s390x)          ESUM='54548139feb80d2368f9ebaf1e86ea38b99cc9411c1c641b2acf9f901aedaba2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_s390x_linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Thu, 08 May 2025 17:06:29 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732ee4ed90538b018d9176335eef4984eda8269e4a778e0ee3889022d5992a33`  
		Last Modified: Mon, 05 May 2025 16:53:51 GMT  
		Size: 16.8 MB (16765943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f30aa7463c453e3e429104b11f9268245d682f64f42cffd5c79dd1ab3d87600`  
		Last Modified: Mon, 05 May 2025 16:53:52 GMT  
		Size: 60.7 MB (60661356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f5e0e49bf17988cf1316b53caeede61b834e15dfb541ebd53711f60fe5aa87`  
		Last Modified: Fri, 09 May 2025 08:16:43 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:fb1d2eaafc76a16f77ea095eddf5e732868dc0119e709779b3bf6463833f6c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3091918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5384c25e70002922fba397539ff66adfdfaf61a59e0a061354490976df89a738`

```dockerfile
```

-	Layers:
	-	`sha256:72d123d21195bd65f02587907aa7aa40ec8009f57b5df61d0490398e273b84e8`  
		Last Modified: Mon, 05 May 2025 16:53:50 GMT  
		Size: 3.1 MB (3068957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de3122aa7f2c817629dbde65c5e2a56f8b9d1d0192469421fa849489b83585d5`  
		Last Modified: Mon, 05 May 2025 16:53:49 GMT  
		Size: 23.0 KB (22961 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre` - linux; riscv64

```console
$ docker pull eclipse-temurin@sha256:9ac2e6801e58b985e39cbe46c58f512b97d5eaaaafd5ec3f8740d6b26dc45ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105551474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5fbbd71a2b16990a55edbc3e4dc8a2ad1c513b87cf4957eaa3541dadfd5113`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:a7f5e3a8aff782c57aa8346238f9dd99048f1bf1a67260c5949ae9396a429340 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='88fb6ad6477ca160a554c8e636c4aa2096f6424828a7e1d90464e105df882875';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_x64_linux_hotspot_24.0.1_9.tar.gz';          ;;        arm64)          ESUM='ef2841ac661b18554961da14ae39ce7fec795fb53f6d52f0df3736c95db42e70';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_aarch64_linux_hotspot_24.0.1_9.tar.gz';          ;;        ppc64el)          ESUM='8f24261481d61470c636ba3698ab8ebd697ab6b766ce468f82513eb60dfb48b9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_ppc64le_linux_hotspot_24.0.1_9.tar.gz';          ;;        riscv64)          ESUM='f61ecea7d2b74036b51ba5f173137344ea3909c92eebe75a1f2b0ecec2037fa0';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_riscv64_linux_hotspot_24.0.1_9.tar.gz';          ;;        s390x)          ESUM='54548139feb80d2368f9ebaf1e86ea38b99cc9411c1c641b2acf9f901aedaba2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_s390x_linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:617ff4840b8ccb0dd209aefc32c58a25fc5e72effac2d6267be2d5e4f07db22b`  
		Last Modified: Thu, 08 May 2025 17:24:33 GMT  
		Size: 30.9 MB (30943987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba143e4ce76d903b7480bb799a840d1bf0e38eae6cae957f8ea3d5c447c814ce`  
		Last Modified: Mon, 05 May 2025 17:45:56 GMT  
		Size: 16.1 MB (16108168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eabb29fb78bb13c5d0d01db886ba1673fd0cc2b33a68a75ff4b4184a6414e68`  
		Last Modified: Mon, 05 May 2025 17:46:02 GMT  
		Size: 58.5 MB (58497005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5429e2bb04c9174a34c370edbf0a52eb260504c60b77424ab3eb3651fad9d46`  
		Last Modified: Fri, 09 May 2025 08:16:44 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:08553bfa33c2fefed78213f38b802ed9adff14614ca4bd8a8a7f780628bd2807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3080874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf0ec56f5a4c1485a5b5465818014db641abb9f0a41c1eac24951350dedb8a5`

```dockerfile
```

-	Layers:
	-	`sha256:68908068fdb451e351dd757f42ceecc036e374892adc2b26737e59b393212cf5`  
		Last Modified: Mon, 05 May 2025 17:45:54 GMT  
		Size: 3.1 MB (3057913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:564f21c4eeebf06d84882e71f9ee438c26e8bb28a8b5f275346df0cee7f2d694`  
		Last Modified: Mon, 05 May 2025 17:45:53 GMT  
		Size: 23.0 KB (22961 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:6fd8861d9c61a02a36c7a3110ba83837c881231f41d94c24e6ac831ff471284f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103443045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e0dbf4a1b0d68b43d562bb15ee67cce3095bb73248468c2a56c514f3ff5dfb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:486993225aeae656f8d559f5c296f6c3164966e35f4b628d26e1da1b75592143 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='88fb6ad6477ca160a554c8e636c4aa2096f6424828a7e1d90464e105df882875';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_x64_linux_hotspot_24.0.1_9.tar.gz';          ;;        arm64)          ESUM='ef2841ac661b18554961da14ae39ce7fec795fb53f6d52f0df3736c95db42e70';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_aarch64_linux_hotspot_24.0.1_9.tar.gz';          ;;        ppc64el)          ESUM='8f24261481d61470c636ba3698ab8ebd697ab6b766ce468f82513eb60dfb48b9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_ppc64le_linux_hotspot_24.0.1_9.tar.gz';          ;;        riscv64)          ESUM='f61ecea7d2b74036b51ba5f173137344ea3909c92eebe75a1f2b0ecec2037fa0';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_riscv64_linux_hotspot_24.0.1_9.tar.gz';          ;;        s390x)          ESUM='54548139feb80d2368f9ebaf1e86ea38b99cc9411c1c641b2acf9f901aedaba2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_s390x_linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:52a1750d5fddc355cdc90a83890b7d582c7f145aa5d114d9582cd010b8ead145`  
		Last Modified: Thu, 08 May 2025 17:05:48 GMT  
		Size: 30.0 MB (29956186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914b4b552aff78862c45561ff5fd578b3f0ddd3fed8e7a2e0ce15405058345a0`  
		Last Modified: Mon, 05 May 2025 16:45:44 GMT  
		Size: 15.9 MB (15873136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985840aab05310632a43d7212d7823e6e6d2e3a5f411cde9e8f070dfe6779cb7`  
		Last Modified: Mon, 05 May 2025 16:45:45 GMT  
		Size: 57.6 MB (57611410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3327231c0702ecc6ad8fbd50b3457983bdbd1002c34d83d947d3270a7268d55f`  
		Last Modified: Fri, 09 May 2025 08:16:43 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f8c3e193584c5b7cb1c18ecdc0d8c6b9d78251880aff093bbbb90e9646e38975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3090221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189c8a160067b26f7a7249d7c7ccb9a67e6dc1bea9cfee2da9e3559c8c401e75`

```dockerfile
```

-	Layers:
	-	`sha256:dd226e24549ba00401f72f5a249ad83cc2b3c56966f013fa25b750cbec1a18ba`  
		Last Modified: Mon, 05 May 2025 16:45:44 GMT  
		Size: 3.1 MB (3067309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5701ad8e567113809db05007970743f8f30ad76c9d8931207826167dac0db882`  
		Last Modified: Mon, 05 May 2025 16:45:43 GMT  
		Size: 22.9 KB (22912 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre` - windows version 10.0.26100.4061; amd64

```console
$ docker pull eclipse-temurin@sha256:42959fff8c993c4d7111b19c09966571c9aa69fe9ef72f909c4cf6788d111e8a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3530527193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b022ddaaa510170d44d923c00eaa80281c09d9314104f073fc4ea69c5a81ed0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Wed, 14 May 2025 20:55:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 20:55:51 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 14 May 2025 20:56:10 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_x64_windows_hotspot_24.0.1_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_x64_windows_hotspot_24.0.1_9.msi ;     Write-Host ('Verifying sha256 (4562ea92299178db9966b7eb7abf9f8bb5269595f6627cede8fc77caf62a2789) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4562ea92299178db9966b7eb7abf9f8bb5269595f6627cede8fc77caf62a2789') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 May 2025 20:56:18 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59a8c05d13f36f76f74a2caeabdd06e72c0d912c9ef135f3f8443511586078a`  
		Last Modified: Wed, 14 May 2025 20:56:21 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f2e69095560dc0f0e1122dec1c3e6d09a12115136d5fb82f967269f0034b35`  
		Last Modified: Wed, 14 May 2025 20:56:21 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1f23363229d097ec1e7e8dc258d890e0174d0edf6e346fea4e95cfdad1a9a3`  
		Last Modified: Wed, 14 May 2025 20:56:30 GMT  
		Size: 99.4 MB (99386276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0f9c29c734ed68020cf2bcb8ee7a707e423432243106df6f921bf8e99b32b2`  
		Last Modified: Wed, 14 May 2025 20:56:21 GMT  
		Size: 372.5 KB (372538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:24-jre` - windows version 10.0.20348.3692; amd64

```console
$ docker pull eclipse-temurin@sha256:bc4db9210ac1541df6a2bc6a6b5e97e6292e0c273e51a8d5927af7988e6a277f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2373318203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1a5ddf639b3a6118dda06f3b396ac5b3d78742a5dadb2f6fddfca88b3c9d29`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 14 May 2025 21:02:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:02:14 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 14 May 2025 21:02:42 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_x64_windows_hotspot_24.0.1_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jre_x64_windows_hotspot_24.0.1_9.msi ;     Write-Host ('Verifying sha256 (4562ea92299178db9966b7eb7abf9f8bb5269595f6627cede8fc77caf62a2789) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4562ea92299178db9966b7eb7abf9f8bb5269595f6627cede8fc77caf62a2789') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 May 2025 21:02:52 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fbed535560b29e38875b7e320a36399fbe7df05e7c2fdb964f92d3d388b8e7`  
		Last Modified: Wed, 14 May 2025 21:02:54 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dde24c69a590d22256ea1a95156b28b7728661ade03836e555480bf63b931ff`  
		Last Modified: Wed, 14 May 2025 21:02:54 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d655320da2cff179dbb7f5290e6d5d6e5b6dec3db2b64457e8a54450476b80`  
		Last Modified: Wed, 14 May 2025 21:03:02 GMT  
		Size: 99.3 MB (99349568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d0e61fcd91728efb5f5a729c02710d51257fbee7c337dd9277c39e6a5527b8`  
		Last Modified: Wed, 14 May 2025 21:02:54 GMT  
		Size: 337.8 KB (337832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
