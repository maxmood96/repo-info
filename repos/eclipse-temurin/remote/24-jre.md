## `eclipse-temurin:24-jre`

```console
$ docker pull eclipse-temurin@sha256:ac24c3a17cc0cb23a5e38770564a8d2ae6cc8c13294448d6f9abd8330615b1c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
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
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `eclipse-temurin:24-jre` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:23eb1f8e0af0b86c953940e2f0d157c9ce1a173cf00fc6ec6aa62e9ded34d18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105885776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562d035877d20f58b7645e8c9b0ff21c3a084564ad996c94402691ef9a301be1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 25 Mar 2025 17:58:27 GMT
ARG RELEASE
# Tue, 25 Mar 2025 17:58:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Mar 2025 17:58:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Mar 2025 17:58:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 25 Mar 2025 17:58:27 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 25 Mar 2025 17:58:27 GMT
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e529360ccaffe024e5446922db3a3b49fa0dc74c12ba87db4650a5e39dc372`  
		Last Modified: Wed, 09 Apr 2025 01:16:19 GMT  
		Size: 15.3 MB (15337835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2623ea3e5bc8653ff6c8e41dacab0b64bc920675b68f7b6f7a51d2ce74138e12`  
		Last Modified: Wed, 09 Apr 2025 01:16:20 GMT  
		Size: 60.8 MB (60827975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35fe000e38b9659c120386817de57203da6430280b71b063372e56830ff3ae2`  
		Last Modified: Wed, 09 Apr 2025 01:16:19 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9d192129d7e83d8dd3c55f46086e893e4a5b74109bc0aa4074d069678c71244e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3088511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d0b275e587fdfbb6eec75d750009f10bacb8be707a092022ddd313f9eda046`

```dockerfile
```

-	Layers:
	-	`sha256:bbe80096ed717acf676db992ac15cf024fc1c2ed7292bbe9ff03dff2aad6f331`  
		Last Modified: Wed, 09 Apr 2025 01:16:19 GMT  
		Size: 3.1 MB (3065690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be57d3c326a7353f48f0cb3b0a0376e95414cc914d72195a7c9b6bc35f1876c3`  
		Last Modified: Wed, 09 Apr 2025 01:16:19 GMT  
		Size: 22.8 KB (22821 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre` - linux; arm64 variant v8

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

### `eclipse-temurin:24-jre` - unknown; unknown

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

### `eclipse-temurin:24-jre` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:ab5613afb8587b73150019c56d673f41be6b08b6eeba0d741e9247fae3a807ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111773434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f3e728356c380a6eb90d2ce91981e5786b2bd61ddf7f00e0c0417c1ae197a6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 25 Mar 2025 17:58:27 GMT
ARG RELEASE
# Tue, 25 Mar 2025 17:58:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Mar 2025 17:58:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Mar 2025 17:58:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 25 Mar 2025 17:58:27 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Tue, 25 Mar 2025 17:58:27 GMT
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
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfca75c36cb1748f7dd66e824e390b2962425e0866f4de497fbdd11963cc3ba`  
		Last Modified: Wed, 09 Apr 2025 04:56:51 GMT  
		Size: 16.8 MB (16765793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9931af99233a061eb3d17224d9bc9558a138992425be60af163c3a0bab843692`  
		Last Modified: Wed, 09 Apr 2025 04:56:53 GMT  
		Size: 60.7 MB (60664458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9389b40eea95abb9f17a4128ad5465ea824724dc4e78c2a4f93d327f22d3fee6`  
		Last Modified: Wed, 09 Apr 2025 04:56:50 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:90667f7035618bfd71ce2cd5c953be30768af2be51bcab5dca0aed584f90617a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3091796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b0cf15deef572de7405404d8c0ab28e81ead2e589222e616be49500ce04651`

```dockerfile
```

-	Layers:
	-	`sha256:6071ff523dfe8cd33ad1a0bc2b667cf7183c8524d615ded9c85fc683b9f0d81e`  
		Last Modified: Wed, 09 Apr 2025 04:56:50 GMT  
		Size: 3.1 MB (3068927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22653cc3d221d8b994d109fe88476b149bed38bbe69c8daefa736b9f88b8e6fa`  
		Last Modified: Wed, 09 Apr 2025 04:56:50 GMT  
		Size: 22.9 KB (22869 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre` - linux; riscv64

```console
$ docker pull eclipse-temurin@sha256:aa441f3e6e85fdece1a73cbd01e0e1a05ba459bc49432fbe5ed962defa44ac33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105545241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26b9fc99f34ee0cb1bfc10c04beab6dbdf289d8cbc3868fdde168b1baa3cde5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 25 Mar 2025 17:58:27 GMT
ARG RELEASE
# Tue, 25 Mar 2025 17:58:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Mar 2025 17:58:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Mar 2025 17:58:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 25 Mar 2025 17:58:27 GMT
ADD file:ef7c97f5dd8d665aae899afe52c54f7acaf71fa51e9d7f26e13ed6073141c666 in / 
# Tue, 25 Mar 2025 17:58:27 GMT
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
	-	`sha256:ba2f284f7444fb0b78fa804d74c44dee4b397610267539e4a6e9c41ae41e06a1`  
		Last Modified: Tue, 08 Apr 2025 11:54:06 GMT  
		Size: 30.9 MB (30943202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23393c58aa39a5ea13901eb423236631cc431a068ff10913c0e908810f2321a7`  
		Last Modified: Wed, 09 Apr 2025 05:59:40 GMT  
		Size: 16.1 MB (16107996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b25915b28efdf1507792c37950b06ae0be5fc484d4b44c7080ee81fe1451096`  
		Last Modified: Wed, 09 Apr 2025 05:59:46 GMT  
		Size: 58.5 MB (58491727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb879cf538a3aedcac6b6c6f64af4a1f610716ee482ba5ae410a4e4d85270c4`  
		Last Modified: Wed, 09 Apr 2025 05:59:37 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:525f2d68124d49a37f6b2e8a9b074e5277e99b67fd06eba615a1e78cc430fa3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3080752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d8572afd726a2b398bf2911601b0c307b6c45d6acc5d50394b78966b5b6aad`

```dockerfile
```

-	Layers:
	-	`sha256:ef5724d274961a058440f1c0a60bc9b94c9a15a965b69682da7166a2fe212ebd`  
		Last Modified: Wed, 09 Apr 2025 05:59:38 GMT  
		Size: 3.1 MB (3057883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2bbdb0e14b3706d38a038f8a4b5b5b6305f78d8157b0529d69c5c0f68be38e6`  
		Last Modified: Wed, 09 Apr 2025 05:59:37 GMT  
		Size: 22.9 KB (22869 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:f2d972a03e6959c87a0dbcb5dc8f4237653dc691937da23df59578cd0f1105cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103444599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eacdf7beb28ee5d54f0fbb9917757aab9b4ddde6be4c3dc1022d28f6d3e5f07`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 25 Mar 2025 17:58:27 GMT
ARG RELEASE
# Tue, 25 Mar 2025 17:58:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Mar 2025 17:58:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Mar 2025 17:58:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 25 Mar 2025 17:58:27 GMT
ADD file:8f287f40ca940c9bd87c8706751f5f1c5bbd0a83fd75f7d938832b226fdb936d in / 
# Tue, 25 Mar 2025 17:58:27 GMT
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
	-	`sha256:e5722f32c6281fa87f1e5f7ebe307864b50aa95a116496a205ce47478bc9b52c`  
		Last Modified: Tue, 08 Apr 2025 11:54:12 GMT  
		Size: 30.0 MB (29956206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b034bbf681312b5cea05640d7cd2668dd78601586813ff4d762258299bb6bf`  
		Last Modified: Wed, 09 Apr 2025 04:28:24 GMT  
		Size: 15.9 MB (15872889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e85aec88e3e9bd67084ce1e5286dc2ca82a4fdc9467e54c9d18887a18e6e62`  
		Last Modified: Wed, 09 Apr 2025 04:28:24 GMT  
		Size: 57.6 MB (57613190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd03fbdee484999676e2050107eb450d5b71a3fb904eb5d149e04319b4de468`  
		Last Modified: Wed, 09 Apr 2025 04:28:23 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f206fbb835f5931649db1aaf4ca23855798ce31ffcd8b717773f9941c3d8acd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3090100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809e838fd3fbb554673023c3688ffbd8eeae4c6492b5599f9cfb82b6523bd18b`

```dockerfile
```

-	Layers:
	-	`sha256:12409ea7788033d503f61270e621dfb524568157c77f97175b086de0cceae482`  
		Last Modified: Wed, 09 Apr 2025 04:28:23 GMT  
		Size: 3.1 MB (3067279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:429186a4b8e504d1c43bd0ab75e77f08012cf4de5562593e01114d50909f20a1`  
		Last Modified: Wed, 09 Apr 2025 04:28:23 GMT  
		Size: 22.8 KB (22821 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre` - windows version 10.0.26100.3775; amd64

```console
$ docker pull eclipse-temurin@sha256:44ceb30a36e3d2f5501af930738ab372e4ef358cd640a6307d881a613f6a01d6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3494414377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d886224c4975026fdef7d1c3da961d119cef2f4ec5b37b52d00b1669430eb1a0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 00:44:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:44:15 GMT
ENV JAVA_VERSION=jdk-24+36
# Wed, 09 Apr 2025 00:44:32 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_windows_hotspot_24_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_windows_hotspot_24_36.msi ;     Write-Host ('Verifying sha256 (3c49e1699ef7b3a1e6e3afb276c0d8d2dca70d91365850ccfddce66e99dd4bd4) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '3c49e1699ef7b3a1e6e3afb276c0d8d2dca70d91365850ccfddce66e99dd4bd4') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Apr 2025 00:44:40 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cd4124b95c0013563f2a51bfe1e2b164722c31b03e4d0ab1647fef3311d3f8`  
		Last Modified: Wed, 09 Apr 2025 00:44:45 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1ab3da87cfda678056923d48457eec1261b9b755bdb333ea8b8f3accad4902`  
		Last Modified: Wed, 09 Apr 2025 00:44:45 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea46d46be23b1e594169e4a3f69b8ed7133647f72d35e798f68bcca65d78f334`  
		Last Modified: Wed, 09 Apr 2025 00:44:54 GMT  
		Size: 99.4 MB (99359573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44556a554244cc2de6246eba4f9595b03e9c5af44818fb39df3ca05e7254f876`  
		Last Modified: Wed, 09 Apr 2025 00:44:45 GMT  
		Size: 372.7 KB (372719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:24-jre` - windows version 10.0.20348.3453; amd64

```console
$ docker pull eclipse-temurin@sha256:d7bd6ce49318dd0a0d1955ab7d074b0c0834d379dc64afa6237539d9a36bcac6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2370699793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d209c616429048f16eaed4b200edf6103246181dbcf3ea51426461cea9704d5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Wed, 09 Apr 2025 00:49:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:49:53 GMT
ENV JAVA_VERSION=jdk-24+36
# Wed, 09 Apr 2025 00:50:15 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_windows_hotspot_24_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_windows_hotspot_24_36.msi ;     Write-Host ('Verifying sha256 (3c49e1699ef7b3a1e6e3afb276c0d8d2dca70d91365850ccfddce66e99dd4bd4) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '3c49e1699ef7b3a1e6e3afb276c0d8d2dca70d91365850ccfddce66e99dd4bd4') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Apr 2025 00:50:21 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201c2d3fac5c5e25dedc60d804d7cabc5dab2917078afddd6f50dfa1f2e1e3fd`  
		Last Modified: Wed, 09 Apr 2025 00:50:24 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c00d78da401918570957faf19ed0067d804135119c33e8623f2d324f1988fc0`  
		Last Modified: Wed, 09 Apr 2025 00:50:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf7e92f8088ec16f4e66d7fcc5ee3014b44ffd57119422124bd8180dca8964f`  
		Last Modified: Wed, 09 Apr 2025 00:50:32 GMT  
		Size: 99.3 MB (99342358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2196833f4f4277f0bfa23aca319daea69e6f20c00e3c0368a028665ebc51e388`  
		Last Modified: Wed, 09 Apr 2025 00:50:24 GMT  
		Size: 359.1 KB (359140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:24-jre` - windows version 10.0.17763.7136; amd64

```console
$ docker pull eclipse-temurin@sha256:81d1fa7a3a73aadc1874794b6da58d2344ae31b0606aba9a9dd0c3c48b635050
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2266215320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859cc4e3592efc3b565dfe0900dc5ce5f8342446909bf48bf8f3747a5a44ae1e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 00:49:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:49:37 GMT
ENV JAVA_VERSION=jdk-24+36
# Wed, 09 Apr 2025 00:50:21 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_windows_hotspot_24_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_windows_hotspot_24_36.msi ;     Write-Host ('Verifying sha256 (3c49e1699ef7b3a1e6e3afb276c0d8d2dca70d91365850ccfddce66e99dd4bd4) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '3c49e1699ef7b3a1e6e3afb276c0d8d2dca70d91365850ccfddce66e99dd4bd4') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Apr 2025 00:50:29 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d65339a47de58292ca31db2ce749ad27c1986a227ac45b48455c406ac020c01`  
		Last Modified: Wed, 09 Apr 2025 00:50:33 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb01ec21c52e91adfd8d7933797b3d3921c00254a7f796a79cad05cabba9b30`  
		Last Modified: Wed, 09 Apr 2025 00:50:33 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18bd8c77fddfb696c9d6eed2cb20c4ceebd6f154bc65e15915a1b8ab0a84b34`  
		Last Modified: Wed, 09 Apr 2025 00:50:41 GMT  
		Size: 99.3 MB (99340641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faeea7a49498f5af4a5e536c934c79070650fe22850ed2d4a91a48119d239e2e`  
		Last Modified: Wed, 09 Apr 2025 00:50:33 GMT  
		Size: 4.1 MB (4145999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
