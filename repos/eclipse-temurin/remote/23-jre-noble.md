## `eclipse-temurin:23-jre-noble`

```console
$ docker pull eclipse-temurin@sha256:a8606b69853a2aaffc0242b318ed9123bc22af027458948d47c0b70e3579fc10
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

### `eclipse-temurin:23-jre-noble` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:916577908b9a139fd1b2f3004dce9129a356c2ed2454f0c50a485f86322d301d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98050523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d8f68e462da3b09a16bf3dc09882aeee6041cf3bd3663034b623f3e9bd2d35`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ARG RELEASE
# Wed, 23 Oct 2024 15:41:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Oct 2024 15:41:32 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1233cbec40f05c76ad926b68521ae78c6ae4f454996ef549602be6987069fa77';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_x64_linux_hotspot_23.0.1_11.tar.gz';          ;;        arm64)          ESUM='0b498a5b673cb50fe9cfd0a13bd39c7259b4fad4d930d614e1563aeb8bca7f0e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_aarch64_linux_hotspot_23.0.1_11.tar.gz';          ;;        ppc64el)          ESUM='ae5d49932f7d9b182c2d9ededa18bd4defc61873f1d717caa3d905bba870a683';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_ppc64le_linux_hotspot_23.0.1_11.tar.gz';          ;;        riscv64)          ESUM='cf65a926c2d7cbdbaa63242a8d20ce747335e7260eaaabd7bb52d51c099fda9a';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_riscv64_linux_hotspot_23.0.1_11.tar.gz';          ;;        s390x)          ESUM='d1d46933716a0eb5a6385980fa98c858c90e72bdc6d14b88d25b20980c5bc7f9';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_s390x_linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6812e7f7eaa0cfae5cf750541a9645364d05f4aa3cb587a0daf038e78dc74490`  
		Last Modified: Tue, 03 Dec 2024 02:30:27 GMT  
		Size: 15.3 MB (15334326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a41d0e7b313cc48a339d12e4277601affbbf34cc311d9759eceb98246984936`  
		Last Modified: Tue, 03 Dec 2024 02:30:27 GMT  
		Size: 53.0 MB (52961914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f5fdbf61f40b7db5df8b1c64f4c05a1334d75688869858d8762cfb2518c618`  
		Last Modified: Tue, 03 Dec 2024 02:30:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a9abd7edd8a190e5719f2bba9d575def0306d839f7e44f3e15b9242845b3ed13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3084400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f48123ce6df33118f04a9232f9a276f2adbd3eecd8d553881e4ccd4af5b56b`

```dockerfile
```

-	Layers:
	-	`sha256:b11705a0f6fff2b952349d91bded8cbb042286449ce61bb06379864bfa3ae790`  
		Last Modified: Tue, 03 Dec 2024 02:30:27 GMT  
		Size: 3.1 MB (3061403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4acd507c33660e18ba307d6d52c21977e3639681f8ba645357029f4bf6edd2b`  
		Last Modified: Tue, 03 Dec 2024 02:30:27 GMT  
		Size: 23.0 KB (22997 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre-noble` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:3f2ce358c21de6d3d0a00d4010a47a7e5bdbe152327aae634d4f736220cc3901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96206898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c500f2db411ae6054dd0ad5320f3661560ef1d4b8adb3f26d31f599d03cb6fdc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ARG RELEASE
# Wed, 23 Oct 2024 15:41:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Oct 2024 15:41:32 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1233cbec40f05c76ad926b68521ae78c6ae4f454996ef549602be6987069fa77';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_x64_linux_hotspot_23.0.1_11.tar.gz';          ;;        arm64)          ESUM='0b498a5b673cb50fe9cfd0a13bd39c7259b4fad4d930d614e1563aeb8bca7f0e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_aarch64_linux_hotspot_23.0.1_11.tar.gz';          ;;        ppc64el)          ESUM='ae5d49932f7d9b182c2d9ededa18bd4defc61873f1d717caa3d905bba870a683';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_ppc64le_linux_hotspot_23.0.1_11.tar.gz';          ;;        riscv64)          ESUM='cf65a926c2d7cbdbaa63242a8d20ce747335e7260eaaabd7bb52d51c099fda9a';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_riscv64_linux_hotspot_23.0.1_11.tar.gz';          ;;        s390x)          ESUM='d1d46933716a0eb5a6385980fa98c858c90e72bdc6d14b88d25b20980c5bc7f9';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_s390x_linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5c2ad96b0a9082eee5f39bb892628713db675cc8237c3d8e1d4f23863b158f`  
		Last Modified: Tue, 03 Dec 2024 05:53:56 GMT  
		Size: 15.3 MB (15328930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6592ac920e8af0bccf838869e3b03a91780a37277f9938820cfda1330182f201`  
		Last Modified: Tue, 03 Dec 2024 05:53:58 GMT  
		Size: 52.0 MB (51982983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccedc8d41db2a5a4769f32771ae06eda5ff06a4187ad3a8503491b36fb3ceb12`  
		Last Modified: Tue, 03 Dec 2024 05:53:56 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c40d925d208dda5cda8b3e9330418684b6226015a212de6644cb2f1c6f44d254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3084372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f1d8e834112f289258cb797edd63a0e0522445fb7bc05bdb7cedb5285af215`

```dockerfile
```

-	Layers:
	-	`sha256:002f342d1e242bc7424596375ba900d22de192f762cf78845b9f22a348f26598`  
		Last Modified: Tue, 03 Dec 2024 05:53:56 GMT  
		Size: 3.1 MB (3061241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b959ba1e055bd4ec49433a4286ce398ba02ac983c0515f2401cf8d528927216`  
		Last Modified: Tue, 03 Dec 2024 05:53:55 GMT  
		Size: 23.1 KB (23131 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre-noble` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:b929d1ea81293b250ec058852af04575d7ba4580221f664f29519520606a53d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (104041619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dbc0a5b7058198f43c385b83f56d4fe8f8b5c96268a63748ce23e8cd1fdf09f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ARG RELEASE
# Wed, 23 Oct 2024 15:41:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Oct 2024 15:41:32 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1233cbec40f05c76ad926b68521ae78c6ae4f454996ef549602be6987069fa77';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_x64_linux_hotspot_23.0.1_11.tar.gz';          ;;        arm64)          ESUM='0b498a5b673cb50fe9cfd0a13bd39c7259b4fad4d930d614e1563aeb8bca7f0e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_aarch64_linux_hotspot_23.0.1_11.tar.gz';          ;;        ppc64el)          ESUM='ae5d49932f7d9b182c2d9ededa18bd4defc61873f1d717caa3d905bba870a683';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_ppc64le_linux_hotspot_23.0.1_11.tar.gz';          ;;        riscv64)          ESUM='cf65a926c2d7cbdbaa63242a8d20ce747335e7260eaaabd7bb52d51c099fda9a';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_riscv64_linux_hotspot_23.0.1_11.tar.gz';          ;;        s390x)          ESUM='d1d46933716a0eb5a6385980fa98c858c90e72bdc6d14b88d25b20980c5bc7f9';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_s390x_linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb3ab1b9a13409a7cb3c37e77f09e73e8a56fce93a8659384ed0937a753cab0`  
		Last Modified: Tue, 03 Dec 2024 04:55:35 GMT  
		Size: 16.8 MB (16797693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01654a9fee6da936451acc7e9207a18a6ffcff58f8427265b27520ac740a834c`  
		Last Modified: Tue, 03 Dec 2024 04:55:36 GMT  
		Size: 52.9 MB (52852792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc661705dd61f703737aca3d019452c667b8f8c7f172b7d27773e0bd53a5d80`  
		Last Modified: Tue, 03 Dec 2024 04:55:34 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:faf8a673a941dfb393ec1f01d7db12febc4ca121373ce57926c4eb30b57ba103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3087681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70430a304a0f56846d1d258d7ca7fe5ea15810ce358ea90c97702877343931fb`

```dockerfile
```

-	Layers:
	-	`sha256:6a161a4ca975f61362a7dd444ef1d548dad5d5cd8a4d1573dfdfdc4aa0f37238`  
		Last Modified: Tue, 03 Dec 2024 04:55:34 GMT  
		Size: 3.1 MB (3064637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cbfedd4c0e2c0f31919e6f77c93056b8d7e693e5de3f5f45cefea6349804b84`  
		Last Modified: Tue, 03 Dec 2024 04:55:33 GMT  
		Size: 23.0 KB (23044 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre-noble` - linux; riscv64

```console
$ docker pull eclipse-temurin@sha256:8abff6271e08ac0bc80e0f165c1d0a19b677271b0326a561465daead934706b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.7 MB (97705132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d4094744ce10aa03b41391e836b77a5e4510b7b5c89e8d6b0d77a15dea74d6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 16 Oct 2024 10:27:02 GMT
ARG RELEASE
# Wed, 16 Oct 2024 10:27:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 10:27:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 10:27:03 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 10:27:43 GMT
ADD file:c7a07ab82f7f269608b3c78a3d2b0cd74630ea7220aee252fb2a61f78978b08f in / 
# Wed, 16 Oct 2024 10:27:46 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1233cbec40f05c76ad926b68521ae78c6ae4f454996ef549602be6987069fa77';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_x64_linux_hotspot_23.0.1_11.tar.gz';          ;;        arm64)          ESUM='0b498a5b673cb50fe9cfd0a13bd39c7259b4fad4d930d614e1563aeb8bca7f0e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_aarch64_linux_hotspot_23.0.1_11.tar.gz';          ;;        ppc64el)          ESUM='ae5d49932f7d9b182c2d9ededa18bd4defc61873f1d717caa3d905bba870a683';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_ppc64le_linux_hotspot_23.0.1_11.tar.gz';          ;;        riscv64)          ESUM='cf65a926c2d7cbdbaa63242a8d20ce747335e7260eaaabd7bb52d51c099fda9a';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_riscv64_linux_hotspot_23.0.1_11.tar.gz';          ;;        s390x)          ESUM='d1d46933716a0eb5a6385980fa98c858c90e72bdc6d14b88d25b20980c5bc7f9';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_s390x_linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:ee732b5fddd0a964c04b11ad9b9ec9f70f7df9e1e96825973cdf803cf1fba8e5`  
		Last Modified: Wed, 16 Oct 2024 12:48:30 GMT  
		Size: 31.0 MB (30980747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c38d40f2993ee68eb6a19703030f97e67619aa382b51f12b37877fb3d55188`  
		Last Modified: Sat, 16 Nov 2024 05:16:16 GMT  
		Size: 16.1 MB (16102234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c17bd4d34a650fe739fdce76f077402a76704ffef1088c27d4c3f6955b915f`  
		Last Modified: Sat, 16 Nov 2024 05:16:21 GMT  
		Size: 50.6 MB (50619836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d06dd2ea6ae299486677ab343d4f3ce4d515c2ecc04114c87667cb55725c7d`  
		Last Modified: Sat, 16 Nov 2024 05:16:14 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d30281cd43062eb7f1c2bc55dce6232a78774b69a15b1db50f8d0896312cff47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3076024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ddc6f00b52bf11a8684dc8a57f60f461f85280fe4407de0e4d49872a95e56ef`

```dockerfile
```

-	Layers:
	-	`sha256:4a5987cf85c68f0f50690be5548d33bd24a8f0925f6dda885d4d4b7f65a23aaa`  
		Last Modified: Sat, 16 Nov 2024 05:16:15 GMT  
		Size: 3.1 MB (3052979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:009ff5c6eddb2fa1b8149a110183abbe7cc386990a611a5e457e8406e77aa9e9`  
		Last Modified: Sat, 16 Nov 2024 05:16:14 GMT  
		Size: 23.0 KB (23045 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre-noble` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:d72002ddcbca2b1ea282f06157adfdaed9430fc52fbbebef17f6f0bdbe88eda0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95371655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5604eb4d053c2b2695bf4d987515b0f1793e3a77c2e7968a9b8166c63db11e9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ARG RELEASE
# Wed, 23 Oct 2024 15:41:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Oct 2024 15:41:32 GMT
ADD file:1c391e128b3c5e552a1401f9520290446bf94ba089c2d74a5d661001d3d8b60c in / 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1233cbec40f05c76ad926b68521ae78c6ae4f454996ef549602be6987069fa77';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_x64_linux_hotspot_23.0.1_11.tar.gz';          ;;        arm64)          ESUM='0b498a5b673cb50fe9cfd0a13bd39c7259b4fad4d930d614e1563aeb8bca7f0e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_aarch64_linux_hotspot_23.0.1_11.tar.gz';          ;;        ppc64el)          ESUM='ae5d49932f7d9b182c2d9ededa18bd4defc61873f1d717caa3d905bba870a683';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_ppc64le_linux_hotspot_23.0.1_11.tar.gz';          ;;        riscv64)          ESUM='cf65a926c2d7cbdbaa63242a8d20ce747335e7260eaaabd7bb52d51c099fda9a';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_riscv64_linux_hotspot_23.0.1_11.tar.gz';          ;;        s390x)          ESUM='d1d46933716a0eb5a6385980fa98c858c90e72bdc6d14b88d25b20980c5bc7f9';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_s390x_linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:755503a8fb36d6a0d08275c3792ab81b69fdff95054dff0aa932d6dc30107609`  
		Last Modified: Tue, 19 Nov 2024 17:38:58 GMT  
		Size: 30.0 MB (30020826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672b22b4866c87b21001ad28b113a2df2da193483a65730f05fa6c2622c0f211`  
		Last Modified: Tue, 03 Dec 2024 04:21:33 GMT  
		Size: 15.9 MB (15904400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e917791eb23023b6714032dfb8e30acb619bd9bddfe03b8c919561b47337772`  
		Last Modified: Tue, 03 Dec 2024 04:21:33 GMT  
		Size: 49.4 MB (49444114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39dbd934c3e9338e00b50d5b0c92cf5827a6dd1b737aaa6b2a3a662f5b1f1d05`  
		Last Modified: Tue, 03 Dec 2024 04:21:32 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5459a2ceaf41647544f6a15ec5c709ea051c295f1e28f390f06cad8298746c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3085992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b647aaf2b549961b44a5226ec0d1c5c674d399d94b32f1ea08f56f172249cbc`

```dockerfile
```

-	Layers:
	-	`sha256:e9064ec2fbf9b9a05ed269f5a3ae7f085f55d72d8ea39059f4d31dc2551eb658`  
		Last Modified: Tue, 03 Dec 2024 04:21:32 GMT  
		Size: 3.1 MB (3062995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6b1836b4b0268c4563f12ef274f89955bb002d3ff35b5b9b61e5b32cf85ed48`  
		Last Modified: Tue, 03 Dec 2024 04:21:32 GMT  
		Size: 23.0 KB (22997 bytes)  
		MIME: application/vnd.in-toto+json
