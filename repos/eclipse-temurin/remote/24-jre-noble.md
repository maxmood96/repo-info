## `eclipse-temurin:24-jre-noble`

```console
$ docker pull eclipse-temurin@sha256:7aa734c5fe42c1e46a6ff044131b19fe42376c270b68c7e1dc3ca0262b7f8665
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
$ docker pull eclipse-temurin@sha256:ad40d92a3974f59f404a671d109337e001e076e7c5eef404aa8c6fac45b280f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114409949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd41a80319ffcc59b35764a90d508553eb80a0b5b941b472647456ba0c47303`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e8d8f5707d765a6bfca3de61320e0bb2618191c77947bc467ac5021e6193f351';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_linux_hotspot_24_36.tar.gz';          ;;        arm64)          ESUM='782a46008490272affe0b797155c2ae8e759e10c8ba4540f1f7285ef3d2902de';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64el)          ESUM='e7c90ab80d5e9419f794aee63c8f1bf3ed29e656d4e8e967a45d3069bd643c07';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        riscv64)          ESUM='3a670b2116cfc7e806ebccf6ad3b5601936581afc666587653c47e642c0acf19';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_riscv64_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='65a9a1e685b81bf80d89a5b45d5f49655e938f3e175accf98c2cb13df07753fd';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_s390x_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed687093bc1d5d43e4719cf38d85858c2c8351940177b6c2d19cd1672aec8b9`  
		Last Modified: Tue, 25 Mar 2025 21:57:53 GMT  
		Size: 23.8 MB (23825337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086beca3d05a6469d4d940f80f65544b2f199f77dbe1b9e3cc877b55cb063da0`  
		Last Modified: Tue, 25 Mar 2025 21:57:54 GMT  
		Size: 60.8 MB (60828007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702d7a2311a8370fcb807847614284cff43a0d470016c8949fea54e0a1625de3`  
		Last Modified: Tue, 25 Mar 2025 21:57:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:138b5efb922b7544aa715cef0a72780074212b998011414cd1638d1e046e5216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3087717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2994369625c54805f2866a5c7efddefe57e9ebfbe23f0ef11337f1ca1368569a`

```dockerfile
```

-	Layers:
	-	`sha256:71d7f9c6aec94b543c92127395b4a47a20e77df29d8bd43000891e20b4ba186b`  
		Last Modified: Tue, 25 Mar 2025 21:57:52 GMT  
		Size: 3.1 MB (3064896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4848012e4ad5b1dffd3e63cb4f843011f1224a18d17901b1a4d4f36b87987c66`  
		Last Modified: Tue, 25 Mar 2025 21:57:52 GMT  
		Size: 22.8 KB (22821 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre-noble` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:a705cc4594ba7c299b8e1a3371790aa1e70cc2b945b0927696b9475d82b61798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112179585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bca3335a8ab1e5d161166d644c592f284855a8a4f1acea3a5d96facb3a6391f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e8d8f5707d765a6bfca3de61320e0bb2618191c77947bc467ac5021e6193f351';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_linux_hotspot_24_36.tar.gz';          ;;        arm64)          ESUM='782a46008490272affe0b797155c2ae8e759e10c8ba4540f1f7285ef3d2902de';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64el)          ESUM='e7c90ab80d5e9419f794aee63c8f1bf3ed29e656d4e8e967a45d3069bd643c07';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        riscv64)          ESUM='3a670b2116cfc7e806ebccf6ad3b5601936581afc666587653c47e642c0acf19';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_riscv64_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='65a9a1e685b81bf80d89a5b45d5f49655e938f3e175accf98c2cb13df07753fd';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_s390x_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e5bb2d9945fa21257f8f197dc3bcdf7b9907415cbfdcbe04fdd03cc197c66a`  
		Last Modified: Tue, 25 Mar 2025 22:06:33 GMT  
		Size: 23.4 MB (23402223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2c3369304c0ea2e93c09c52009c246ff0b0ab4f244a47a3c28f0a2d5157505`  
		Last Modified: Tue, 25 Mar 2025 22:06:34 GMT  
		Size: 59.9 MB (59881449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3ba4bee08abfa5598d96bced98e39b1f7e0cb4416d326d35181a09513f94a2`  
		Last Modified: Tue, 25 Mar 2025 22:06:32 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3d8c81d3689d504414cd93de9d68efa2d1b493a4e652a0c07d2400b2464a65fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3088309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d54d67e82b019dcb942491c44c82ddd6cbc3f27f1b86412d1918c659cb0d8288`

```dockerfile
```

-	Layers:
	-	`sha256:9494fda81b27b2ef2a7aef395ab0facde203df0e0f4a56a220edf9a353bb38f7`  
		Last Modified: Tue, 25 Mar 2025 22:06:33 GMT  
		Size: 3.1 MB (3065354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aabeb2918b2afa2cfcca7b90eb9269a57a13659ed9ffac4b215355e4e9918d01`  
		Last Modified: Tue, 25 Mar 2025 22:06:32 GMT  
		Size: 23.0 KB (22955 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre-noble` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:c718eb2b1ab3b77535a972364f7dc4cb543ccfe91fe0e5df5d24ef98ac978e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121329730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ffdfb248d4268c4b0a8c1de300afc57c7ca552c8e00aea6b7462b140c6535c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e8d8f5707d765a6bfca3de61320e0bb2618191c77947bc467ac5021e6193f351';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_linux_hotspot_24_36.tar.gz';          ;;        arm64)          ESUM='782a46008490272affe0b797155c2ae8e759e10c8ba4540f1f7285ef3d2902de';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64el)          ESUM='e7c90ab80d5e9419f794aee63c8f1bf3ed29e656d4e8e967a45d3069bd643c07';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        riscv64)          ESUM='3a670b2116cfc7e806ebccf6ad3b5601936581afc666587653c47e642c0acf19';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_riscv64_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='65a9a1e685b81bf80d89a5b45d5f49655e938f3e175accf98c2cb13df07753fd';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_s390x_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c98a96e7323d5b68d1f0880aacf6f684a889f52bfc39e7b90a1314b665374a`  
		Last Modified: Tue, 25 Mar 2025 22:10:33 GMT  
		Size: 26.3 MB (26273163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f0039bd0852ee0cdd678f401573314970c593afed050dddb10f4fa35b344e6`  
		Last Modified: Tue, 25 Mar 2025 22:10:34 GMT  
		Size: 60.7 MB (60664428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a7cc02fb74d0caf35c0182576e2fdbfa78994e71004977db352dbd4da0d625`  
		Last Modified: Tue, 25 Mar 2025 22:10:32 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7e337fc3ce5f6e169ae038877fd8045c49d58efb9dc7650ca3d5e11518330582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3091002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab7f4106136d8ffda70de48253925cad565334359d1a3b6dd92a6a060fd24dd`

```dockerfile
```

-	Layers:
	-	`sha256:4d5be52c0e404f598253e9aef0c66ca119dcdc3ec22f90e3b4a5d3d4e74687ed`  
		Last Modified: Tue, 25 Mar 2025 22:10:32 GMT  
		Size: 3.1 MB (3068133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c49b33155e1098eb02c7de58dea269c876003f092814787a5e05a75161bbb51`  
		Last Modified: Tue, 25 Mar 2025 22:10:31 GMT  
		Size: 22.9 KB (22869 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre-noble` - linux; riscv64

```console
$ docker pull eclipse-temurin@sha256:744ad6da61bc77ca1af7c8d5588d77d4ea4e137219b04e2929cb302e7ab2556c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112573653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e52fa18ec6c888f065cc739bdb9cb420407115701ef12483f1e163a7d960f4b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 27 Jan 2025 04:46:38 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:46:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:46:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:46:39 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:47:10 GMT
ADD file:69c46ae9666e78c27ca5b5f25cec1a5536ff16f17cb00104e5c77e722bd8d643 in / 
# Mon, 27 Jan 2025 04:47:12 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e8d8f5707d765a6bfca3de61320e0bb2618191c77947bc467ac5021e6193f351';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_linux_hotspot_24_36.tar.gz';          ;;        arm64)          ESUM='782a46008490272affe0b797155c2ae8e759e10c8ba4540f1f7285ef3d2902de';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64el)          ESUM='e7c90ab80d5e9419f794aee63c8f1bf3ed29e656d4e8e967a45d3069bd643c07';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        riscv64)          ESUM='3a670b2116cfc7e806ebccf6ad3b5601936581afc666587653c47e642c0acf19';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_riscv64_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='65a9a1e685b81bf80d89a5b45d5f49655e938f3e175accf98c2cb13df07753fd';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_s390x_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6e1053d729cc1718daa9369927cf6ddfbf892a846041de0e610d1c77ade136c5`  
		Last Modified: Mon, 27 Jan 2025 05:10:15 GMT  
		Size: 31.0 MB (30983910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e288c3abf955da17ed37640cdff369b31068d2544be5e243fc4ea9f37abf3b`  
		Last Modified: Tue, 25 Mar 2025 22:08:21 GMT  
		Size: 23.1 MB (23095616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc19f876645dc02be36bbd68ff57bfe570b0500b6d188db79df8e4714b8ce67`  
		Last Modified: Tue, 25 Mar 2025 22:08:26 GMT  
		Size: 58.5 MB (58491813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463ecef78d55b19a794867b2081f10523c3704a4bc83824ea34704c07a310f04`  
		Last Modified: Tue, 25 Mar 2025 22:08:17 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7b0cedb95848254c6c1db6ba0b95703be3fcef00e71429bb91ba64a5dc9071d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3079958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c793227ec0552f561d609ebee7f94b1854952d71b0d55533e5f971566ad6a4`

```dockerfile
```

-	Layers:
	-	`sha256:fdd1ec5053d427ff8b4eb99ffe98b4eb830fa9c43b488ea11459dbf4ace8e960`  
		Last Modified: Tue, 25 Mar 2025 22:08:18 GMT  
		Size: 3.1 MB (3057089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42fcbca53bea92b4a09a13881b6e7a1600169c3c2153f5e7852a05c54a943fed`  
		Last Modified: Tue, 25 Mar 2025 22:08:17 GMT  
		Size: 22.9 KB (22869 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre-noble` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:2428a122a5e1a5b7de2858e6fff5f8f4dfe24586e9bf2712edf4332ee6868c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110855025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65677c34db3a5e6488b50d704c2747601ebb2f3897bf0eb1268ce465ed746c7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 27 Jan 2025 04:15:19 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:15:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:15:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:15:19 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:15:20 GMT
ADD file:1a65bb049384da7e51a2b1e9180f11d6ec22b1427da7ca5682814abd261ba57e in / 
# Mon, 27 Jan 2025 04:15:20 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e8d8f5707d765a6bfca3de61320e0bb2618191c77947bc467ac5021e6193f351';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_linux_hotspot_24_36.tar.gz';          ;;        arm64)          ESUM='782a46008490272affe0b797155c2ae8e759e10c8ba4540f1f7285ef3d2902de';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64el)          ESUM='e7c90ab80d5e9419f794aee63c8f1bf3ed29e656d4e8e967a45d3069bd643c07';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        riscv64)          ESUM='3a670b2116cfc7e806ebccf6ad3b5601936581afc666587653c47e642c0acf19';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_riscv64_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='65a9a1e685b81bf80d89a5b45d5f49655e938f3e175accf98c2cb13df07753fd';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_s390x_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:8e1d25585ef2d346b71072d258a697a9d190e3c5754512c7cb978dbbe80911e6`  
		Last Modified: Mon, 27 Jan 2025 05:10:30 GMT  
		Size: 30.0 MB (30027563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6f1080bd2f2bf83646b134ca6816b42e59e2e1859505262a33c59cc8a04c9c`  
		Last Modified: Tue, 25 Mar 2025 22:05:12 GMT  
		Size: 23.2 MB (23211916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fc14999bcd2b2a042f54a699ce2eea2ea34091efc666d3fd140596fc06be3c`  
		Last Modified: Tue, 25 Mar 2025 22:05:14 GMT  
		Size: 57.6 MB (57613232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c072b41d84dbb2cdc26f119880b654b50dff9920ab924082dbdea14734090dc`  
		Last Modified: Tue, 25 Mar 2025 22:05:11 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5a2c85b973ac35e241ec519af406eb45e278b1bf02303ab660b413c71064bbb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3089306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235bf218930d29b6b05ebe74166957106e98f3e4f82fe18bb54b3559a0d0b00e`

```dockerfile
```

-	Layers:
	-	`sha256:870d32ce9baf8430a60c8177a487c65fc7c4f2a9a7cfaf55feb1ff8bd4d0bbf0`  
		Last Modified: Tue, 25 Mar 2025 22:05:11 GMT  
		Size: 3.1 MB (3066485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be05530c5dfa06227beb7c51cbfae01a720131ba658e6baa3ce55ea94e100d18`  
		Last Modified: Tue, 25 Mar 2025 22:05:11 GMT  
		Size: 22.8 KB (22821 bytes)  
		MIME: application/vnd.in-toto+json
