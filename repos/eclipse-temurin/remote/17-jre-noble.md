## `eclipse-temurin:17-jre-noble`

```console
$ docker pull eclipse-temurin@sha256:826b35e8365155e2b41701af8a80008b50284f7ffc9c4e9d4ec2ba4e02114a6e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `eclipse-temurin:17-jre-noble` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:19f5a033486dafbed7317e1d9001e8e43c538f6ab8b8f3af8afe04ae364c0a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93754741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c0683d34681fe1c8cd124bdca0ecf4ff33fab3c18ee7958ecae4de3f1c7e51`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:38 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='2876b04be597a748d5daaa5e1e73a32e9e84cb1b98c1760ff79fb3a53e032de7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12c659f8ac16f8d9fc5114f9b2bbc77d6367df6b5f9070ec314a45711853b3a`  
		Last Modified: Thu, 13 Nov 2025 23:22:00 GMT  
		Size: 17.0 MB (16972143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1e0321681ccbedcbfd0d195ec926ba8b1fb3ac6881aedeb6107b5d2dfa3f28`  
		Last Modified: Thu, 13 Nov 2025 23:22:04 GMT  
		Size: 47.1 MB (47055469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469f7f46f06bf8f05ffa00c679b9cfed78488d3273e4ad9a245a063d965a2083`  
		Last Modified: Thu, 13 Nov 2025 23:21:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2581bc3ff3b6d9f257d5b3f64a3d86de4713b0ffefbb3189693db6e3785a9e79`  
		Last Modified: Thu, 13 Nov 2025 23:21:59 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:847580f3c60c00b60c3a7942836516627186892fcb255fe4212ce8200fe8c9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3309330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2080a5f6b565fe39df45864948a8c940b8d824713ec3e87766818e49b0ea421f`

```dockerfile
```

-	Layers:
	-	`sha256:aaadb68f034ed10e6c3f5669e1b3b7d9e06c1e7e12a3eff430fe9a546a0a681c`  
		Last Modified: Fri, 14 Nov 2025 01:15:31 GMT  
		Size: 3.3 MB (3285349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7f72348805bd1d33e4e21f176a1873a4e5f96fe7a0600453b569ea365672b74`  
		Last Modified: Fri, 14 Nov 2025 01:15:32 GMT  
		Size: 24.0 KB (23981 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-noble` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:d54ff3ff902f194b93967716486a406140f0dd0449feb746ae2ec88c6def9d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87885073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a680aa231645b3eb8a52d84aace06d37aa5b89bf7202602bfed7113098e1c454`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:17 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:17 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:20 GMT
ADD file:dd3740083ecd2e2b1e178f1771ef73043bc7be6c831492453a755b873d8b531b in / 
# Thu, 16 Oct 2025 19:25:21 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:09:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:09:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:09:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:09:28 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:14:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='2876b04be597a748d5daaa5e1e73a32e9e84cb1b98c1760ff79fb3a53e032de7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:14:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:14:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:14:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6cdc0abf996c3192bfbda4018d34c282871d4be33fb369176002cb2199673adf`  
		Last Modified: Fri, 17 Oct 2025 08:06:35 GMT  
		Size: 26.9 MB (26852672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0d6184eab1fedb00d8072befde7c3b4597274a562208d5c523cbc1138cbd17`  
		Last Modified: Thu, 13 Nov 2025 23:09:59 GMT  
		Size: 16.3 MB (16306081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39eba0a8462f20a15f16f7be412b730d9ab13dfe9708f8961fc4625e7c26179`  
		Last Modified: Thu, 13 Nov 2025 23:14:43 GMT  
		Size: 44.7 MB (44723880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc38e604d6cdff764e8f50d785137007f8007012002099bbb31d896034f67116`  
		Last Modified: Thu, 13 Nov 2025 23:14:38 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e393eb7b86e7a6f05d3aa5386b696261b35477e183acf0bd253091bb9cea41e1`  
		Last Modified: Thu, 13 Nov 2025 23:14:38 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:90469bff3f7a9e18a150c5157ef9695fc03f01384dcae2e3e00164bc12fb1ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3311772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6522cb500bce3ec90fc82d442b38f39322fdf347bfe2dbb9bc39ed0682ed4a`

```dockerfile
```

-	Layers:
	-	`sha256:a359f1e2785511f073e1b4a8841dd49bc1e6d05eef705708bd830a3c74af6d54`  
		Last Modified: Fri, 14 Nov 2025 01:15:36 GMT  
		Size: 3.3 MB (3287686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cc190f59693b5f54a7b1643d3f93f201978af7f30c503294c828d7c7815f7a7`  
		Last Modified: Fri, 14 Nov 2025 01:15:37 GMT  
		Size: 24.1 KB (24086 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-noble` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:a781d4837eea8f15c2e0b1924643d2de0fde1f63468535a67ecee86e0f97f0f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92391794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03835612bdb8e36185bb4bc4ddf9b56cea001282b3d6cde09914bc6833066aec`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:21:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:21:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:21:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:21:17 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:21:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='2876b04be597a748d5daaa5e1e73a32e9e84cb1b98c1760ff79fb3a53e032de7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f217617b8adc8e338c40dc9cbb2fb089ae4ae063ca4eb78bf0dfc9d762cafc`  
		Last Modified: Thu, 13 Nov 2025 23:21:40 GMT  
		Size: 17.0 MB (16989109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae42f591e3344a684d2b9ff93f75c9f6662804c81d6d39e86bc6c9210e560cf6`  
		Last Modified: Thu, 13 Nov 2025 23:21:43 GMT  
		Size: 46.5 MB (46538289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf53f68aed0c96936c4fce1a47200aa8f99f2894c8171c7f1bee9996efa7f442`  
		Last Modified: Thu, 13 Nov 2025 23:21:39 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95530a3b2040ac287e294550a0badaa71a7759a355f6026f419c3f6880121ea`  
		Last Modified: Thu, 13 Nov 2025 23:21:39 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:745d63810247e8cc771ec723858144508fe4b882f0c50c0bb25369788e771e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3309935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc918ce433930e5b6766b00d118026576d726828afc6a845965d1ec3383e3880`

```dockerfile
```

-	Layers:
	-	`sha256:3e8cd59d2cbf890d19a59a750a0b321fe0cbf51a1cb94a487d352c13dc2c063d`  
		Last Modified: Fri, 14 Nov 2025 01:15:41 GMT  
		Size: 3.3 MB (3285820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7924fd114989607b2cf1b1f20f7e0ad18e3f9db51a3d9d7723a18e8a549036c2`  
		Last Modified: Fri, 14 Nov 2025 01:15:42 GMT  
		Size: 24.1 KB (24115 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-noble` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:22b75af2166f1c450d25aa929a89ba64b88b50bef4e31591e0c1a3331817924b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.0 MB (100003131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c0f4ac4dd37e40051730f96bffe6daa45b06268a699eb0c5e7f94142816f6b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:12:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:12:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:12:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:12:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:12:31 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:24:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='2876b04be597a748d5daaa5e1e73a32e9e84cb1b98c1760ff79fb3a53e032de7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:24:53 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:24:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:24:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0cf872bdb9578adf029cccb893ea39b7d62a1717f6f08db17d402977875a8b`  
		Last Modified: Thu, 13 Nov 2025 23:13:16 GMT  
		Size: 18.8 MB (18814748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c610e88a6dc2b35d7669d05ce7449a698c0e43ad8ccd76cfc79d4ef1075816`  
		Last Modified: Thu, 13 Nov 2025 23:25:27 GMT  
		Size: 46.9 MB (46881521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ad9ce4ee4363063833b155787dfff300d16b0cc0d33d1cba84158a62f1a601`  
		Last Modified: Thu, 13 Nov 2025 23:25:24 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d6386e69210f0e9bad2ae86eee587a19bc2e8850fbfecca1968f5771c5c53f`  
		Last Modified: Thu, 13 Nov 2025 23:25:25 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8faf9c41fa22d2d2e50751a8362fd3654cfe5f0e2072dee297b4aea464db60e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3313445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40657a24d19ec714eec0f583d0af89212435de20d80a09dec1726892f326c8c7`

```dockerfile
```

-	Layers:
	-	`sha256:ae4fe505e2d9815dd0061e6c2b33531f281207a7ae5314029a987ea781b4aca1`  
		Last Modified: Fri, 14 Nov 2025 01:15:46 GMT  
		Size: 3.3 MB (3289417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22c607a5e7474e63c702db113183c11c1148185bd1a962d875b99d64aa1172bc`  
		Last Modified: Fri, 14 Nov 2025 01:15:47 GMT  
		Size: 24.0 KB (24028 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-noble` - linux; riscv64

```console
$ docker pull eclipse-temurin@sha256:9af99cd70ecdc0ba4a92f02e1e5889f77c8ee1f33c73971cd3316d2d1b298dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94438942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa4b76dc8ece588b7b68bc694c4f82fed14b2ac3dc2af19a0abdf3034b567344`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 13:48:30 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:48:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:48:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:48:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:49:22 GMT
ADD file:857dc87fbafae31881cff8c69aed267a033f5df226dd351ee89de918ad5678ce in / 
# Wed, 01 Oct 2025 13:49:27 GMT
CMD ["/bin/bash"]
# Sun, 09 Nov 2025 21:55:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 09 Nov 2025 21:55:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 09 Nov 2025 21:55:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 09 Nov 2025 21:55:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Nov 2025 21:55:38 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sun, 09 Nov 2025 21:56:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='2876b04be597a748d5daaa5e1e73a32e9e84cb1b98c1760ff79fb3a53e032de7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 09 Nov 2025 21:56:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 09 Nov 2025 21:56:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 09 Nov 2025 21:56:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:ff47a256ba51b80e9880bc96be4ac2f094c47e0fcd7eec71bab85787cfa54b8b`  
		Last Modified: Mon, 13 Oct 2025 04:10:18 GMT  
		Size: 31.0 MB (30951381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f168f32147322448b62f52061211b5e8d09d625fa544b55b31e5531645eb05a`  
		Last Modified: Sun, 09 Nov 2025 21:58:38 GMT  
		Size: 17.9 MB (17864334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2d63ca6878cebe69352e155f0c0dde77aaf8af87463492caf87f84316222a8`  
		Last Modified: Sun, 09 Nov 2025 21:58:40 GMT  
		Size: 45.6 MB (45620784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052a7df6e6d0d11ce44a19f792aed6e0a15f4988b25358f27d5c059c2bdc8467`  
		Last Modified: Sun, 09 Nov 2025 21:58:36 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed89424640b4de00fcb8f5ced65e816978682f9f945132e64ac67a19cd0c8dba`  
		Last Modified: Sun, 09 Nov 2025 21:58:36 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:440ff3b6c194e54c24406d555ca85df35fe1eb27f19f747cf286c9a983ba6995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3301452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f7fd849bdb1153b6d4e38896d0eb37a32410a75df81cab5ba533c3a02001b6`

```dockerfile
```

-	Layers:
	-	`sha256:ab8537502b0aed17eeffb74426c97bea280de04bd9b413fb013aa21d99ca98e6`  
		Last Modified: Sun, 09 Nov 2025 22:13:23 GMT  
		Size: 3.3 MB (3277423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e82efdc0ec501ac266f86abb70938da19eddd623e04245ed1aa6ca734cdba2f9`  
		Last Modified: Sun, 09 Nov 2025 22:13:24 GMT  
		Size: 24.0 KB (24029 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-noble` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:d7113d694f0b0fdba09be2dd5fd81a791a3979d4f7fb3c6702b056c5f4f01142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91522112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be44727687f8009b4cbe66e0fd3a6520cfe8e17edcf879366e2d6a2d615ff68`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:14 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:14 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:16 GMT
ADD file:f7335d462150d31c3c91b13ccd3e927bc9a1b9c6664fa8905ccf68bbe3d86cd3 in / 
# Thu, 16 Oct 2025 19:25:16 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:10:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:10:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:10:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:10:26 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:10:26 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 13 Nov 2025 23:10:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='962b592e7f4196da9dc874c9bc775186d10d4515d505355516ac4eba0775645d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='2876b04be597a748d5daaa5e1e73a32e9e84cb1b98c1760ff79fb3a53e032de7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:10:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:10:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:10:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:7d5b0205a5ff16c2b58f20a113b5eb9a80393a644df077beab5d90635153dc66`  
		Last Modified: Thu, 16 Oct 2025 21:17:39 GMT  
		Size: 29.9 MB (29907597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0147a99aba12439fa4c91b74f700e26d7619845500f1c2f1faf6b732f356eb94`  
		Last Modified: Thu, 13 Nov 2025 23:10:53 GMT  
		Size: 17.6 MB (17581016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd8d5ac3b368e1acbcc0fee7732f6e466ef01cddfd09a73ac260a6d26bede28`  
		Last Modified: Thu, 13 Nov 2025 23:10:57 GMT  
		Size: 44.0 MB (44031061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add42ff867dcd0e89d9d3555a02f580fbfa461633c923c4ca9190d8792716d82`  
		Last Modified: Thu, 13 Nov 2025 23:10:51 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e597879d66d684adb943c1b7daf5fd3b4dc1b6ed0f851f3105649987a4940e83`  
		Last Modified: Thu, 13 Nov 2025 23:10:51 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:965c5a721f2c2769b67235459a79b8ccc7d35f12826ffc743d4b80ba490049b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3311530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4021f7002e1fd73933d8beb27a9fc3695adc83daea4891c83e504c13e7ddc0d`

```dockerfile
```

-	Layers:
	-	`sha256:87cec246feb6e969e1085c31818266abe610c6d4e37a82911aa425713f5d588b`  
		Last Modified: Fri, 14 Nov 2025 01:15:55 GMT  
		Size: 3.3 MB (3287549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84519489a2f4e4d00709cbc1a9fdd109d3c05218327cf491b1ce821a845a63ee`  
		Last Modified: Fri, 14 Nov 2025 01:15:55 GMT  
		Size: 24.0 KB (23981 bytes)  
		MIME: application/vnd.in-toto+json
