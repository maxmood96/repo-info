## `eclipse-temurin:24-jre-noble`

```console
$ docker pull eclipse-temurin@sha256:e8bf3deabd04579fd244812b921f37c7999337f7e297555a308e455e74e68ff9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `eclipse-temurin:24-jre-noble` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:08ec2c37434c5508ba96f174e6bda36531594be03bf4c399814714561223f029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105884419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dcbd13df903a89e4d65e7858f493fc49b66b7cb508563392c5ae9cd128d7963`
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
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
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
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af5aa274948c0dd81c4caa7c59959f002597f00ea530a394faa9f767c737938`  
		Last Modified: Tue, 03 Jun 2025 13:34:33 GMT  
		Size: 15.3 MB (15338470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70a30119a5387c93733400daabac8ade3c8785c07cb638dc23b8dbdd4e1319f`  
		Last Modified: Tue, 03 Jun 2025 13:34:41 GMT  
		Size: 60.8 MB (60828298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12b652af6f2a9b00566949cf6ee409e1b74ec0624c7dd0c18f01046c075ce08`  
		Last Modified: Tue, 03 Jun 2025 13:34:42 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f99e79599b2c59c2efae9619da90e02c09a9cd19661bf0fe060efced4ff1a25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3112810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed6a7aae319e3e24182e2801e74913409c7df5f92ef6fee3b5ca2f82f1ac077`

```dockerfile
```

-	Layers:
	-	`sha256:0c84361da89c146d6fc3a5aea6a3923deef5426ffede5d7a60cbad07a40d19b7`  
		Last Modified: Tue, 03 Jun 2025 18:00:59 GMT  
		Size: 3.1 MB (3089898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce20be69f24cc488c0ca962f5fec58870135fb925a3e73550228d020b799505d`  
		Last Modified: Tue, 03 Jun 2025 18:01:00 GMT  
		Size: 22.9 KB (22912 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre-noble` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:f78b5074809ac602fdd3c34392990afc13ef5033cf01ef39ebc43d84c61ce94d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104068514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5971b484d48520e8c034a5ca8750798bed85d88e2115d19bd2c34cb46dbaca`
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
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
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
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07f34540c589037eae64c9a960c8f6798260c951b89748fabe4f30e60656717`  
		Last Modified: Tue, 03 Jun 2025 13:34:42 GMT  
		Size: 15.3 MB (15331176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc051d7875a6bd999e142f9324b81284e5ccd02ce7ee69a33b8ed082b4fa4f3`  
		Last Modified: Tue, 03 Jun 2025 13:34:48 GMT  
		Size: 59.9 MB (59883125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b96953286b9a7e11ff1e2492aadfa13729fa3562955dd08e3f5d0b7d32f9c3`  
		Last Modified: Tue, 03 Jun 2025 13:34:50 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5159c5cdaada82eb9b08e314e7be4907e6cc2bcceed618f88b435cd1be9694f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3113403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cbfa612379675ab862f254f488db60980a821811b0e84260786483f0bfd3210`

```dockerfile
```

-	Layers:
	-	`sha256:88b921d6f1f6359a8515ccadbf37d83603d55238c68cfb7480936acc15a77937`  
		Last Modified: Tue, 03 Jun 2025 18:01:04 GMT  
		Size: 3.1 MB (3090356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a033112055ee4b3b3b372ede4ef061d2067e28e41a23afa7deeeaed103f05ac`  
		Last Modified: Tue, 03 Jun 2025 18:01:05 GMT  
		Size: 23.0 KB (23047 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre-noble` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:8039e9f58b8127f1d9b7fc743f999af20b413a1e150bb131a62b71ef2c0edf2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111755480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac94182fd78e4ebe282417ad2f7540b6911d926c52847d1f7ad2fa82e2eb1a15`
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
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
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
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Tue, 03 Jun 2025 13:31:13 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336d746f5324e8e105d2429f1e9cafd6ccdf3ab8a17902a16d4bf12d99efb579`  
		Last Modified: Wed, 04 Jun 2025 01:12:51 GMT  
		Size: 16.8 MB (16766635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04c0d4a2d89ae2f5f609307644f340f6cd94f5bb1a1db5528ff54b7453f5b5b`  
		Last Modified: Wed, 04 Jun 2025 01:13:00 GMT  
		Size: 60.7 MB (60661322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c149e48dadd3b613f9a35244fb1271a34504b14e3d542c031f25946d593d0e78`  
		Last Modified: Wed, 04 Jun 2025 01:12:45 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:81bc241d6f33fa04f1b429fce29a85aa1a762c75cbe21d2b91e68a8a84e6b82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3116220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6acae82fb20edcbaef88c4ec782186ad1c4bfe5037e0da44dd945bd336dc5036`

```dockerfile
```

-	Layers:
	-	`sha256:a806335c32e6df462015150c63c5d3339156920e78fe4c746a0ac885b2d2ce59`  
		Last Modified: Tue, 03 Jun 2025 18:01:10 GMT  
		Size: 3.1 MB (3093259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2819760117e225aee82299fbbf48cc1f6cc1fdd117cbae55bc24be30a645b101`  
		Last Modified: Tue, 03 Jun 2025 18:01:11 GMT  
		Size: 23.0 KB (22961 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre-noble` - linux; riscv64

```console
$ docker pull eclipse-temurin@sha256:604228052f87b9b9fd259832612a340c7f665cd96fa6a6fbd215fc409ec3b594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105555500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96a38c47a611b48e08c0def37efb7c6aebab4798467ee82d38669e354c8e0aa`
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
ADD file:f68263cf915d0f5d61ab9caa83da511fc9ef55d936429cb8fb542906fc38a8fa in / 
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
	-	`sha256:4ac2db62b9f8401057b5c4ebae4764d70573ec599f6a1f0b5dc2c4491ed8e39a`  
		Last Modified: Tue, 03 Jun 2025 13:37:40 GMT  
		Size: 30.9 MB (30947484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768b77bf90b4c4fd8eeecf7d356b1b81f5ceac28ffbb4c29a858e38b7b335d74`  
		Last Modified: Wed, 04 Jun 2025 01:12:51 GMT  
		Size: 16.1 MB (16108712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728849025e8baef95cfca244e05b56a2388c0d2a02be3d1f3875df8f9456fec5`  
		Last Modified: Wed, 04 Jun 2025 01:13:00 GMT  
		Size: 58.5 MB (58496989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e14679868d24ac15122efdf82b26a11257b044fee2746750d312ed5ef5d657`  
		Last Modified: Wed, 04 Jun 2025 01:12:45 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ef315184a40abb32893cbe5c8b074386316611f722793a38f594694e2ff2e5f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3104884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4cca056a5d887c08fa4b2eb55cdde88ec73e338bbaffc813941d0e56cfd07b3`

```dockerfile
```

-	Layers:
	-	`sha256:d3b312a458caf833c4ffa0d37d3728fbf6a0262e29b11038093e4ef8222eb70e`  
		Last Modified: Tue, 03 Jun 2025 18:01:16 GMT  
		Size: 3.1 MB (3081923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e62f9e6c21ce271bf68d12a8141e25158c8f4e01fb46643341c6b9efa45de3a`  
		Last Modified: Tue, 03 Jun 2025 18:01:17 GMT  
		Size: 23.0 KB (22961 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre-noble` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:c217c55ec4aa29a92e1ae6a9886594b77e3ad8f86c17bc59b9bc7d8514587c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103417075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d638c6530c121bd40f7dae2e24c5f7b2c0d042559809aa97f1ac0c7b06e27c`
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
ADD file:b6b8557b3fef6c06eb943ce735f649cf7033ab3925e70e6b43901f1f29b4d5e9 in / 
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
	-	`sha256:7fa55ab2f467363da0197dee4a8e5af9e7ba7ef5686c6f0951bc509c387b765c`  
		Last Modified: Tue, 03 Jun 2025 13:31:43 GMT  
		Size: 29.9 MB (29930056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a2bb7955115fa197c91f6da1e2a4408150a69b89bfc57e3057d61c1852f5a0`  
		Last Modified: Wed, 04 Jun 2025 01:12:53 GMT  
		Size: 15.9 MB (15873267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02d89ed6344fc4f1a5067fd52fd521d71b013fcb30df2f4ce0a8d0fe5661370`  
		Last Modified: Wed, 04 Jun 2025 01:13:01 GMT  
		Size: 57.6 MB (57611439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1116019b09c08e832b78464f9b35ceaee67d8bde247d5fef3ff6f3f5c0096b3`  
		Last Modified: Wed, 04 Jun 2025 01:12:48 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:055c34a29a754fa27f2dec7e524e3a31fccdc24a14786930d75bc473818b6fe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3114400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2660f72f77311ce2a37b395a0d71702199df6150e181e04c0af35c3ec4d60bfc`

```dockerfile
```

-	Layers:
	-	`sha256:9e51a60d68acde7fdbbc7891e245191b725a5a3c96a94c0ccaa08e76b5129e0d`  
		Last Modified: Tue, 03 Jun 2025 18:01:22 GMT  
		Size: 3.1 MB (3091487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aedb0f1e8af270495d148383d2c873d4911fd28d488c66334331eb4710d89406`  
		Last Modified: Tue, 03 Jun 2025 18:01:22 GMT  
		Size: 22.9 KB (22913 bytes)  
		MIME: application/vnd.in-toto+json
