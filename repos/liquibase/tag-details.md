<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `liquibase`

-	[`liquibase:4.31`](#liquibase431)
-	[`liquibase:4.31-alpine`](#liquibase431-alpine)
-	[`liquibase:4.31.0`](#liquibase4310)
-	[`liquibase:4.31.0-alpine`](#liquibase4310-alpine)
-	[`liquibase:alpine`](#liquibasealpine)
-	[`liquibase:latest`](#liquibaselatest)

## `liquibase:4.31`

```console
$ docker pull liquibase@sha256:c40d47b2eefe08f1d423bc9e06de06b1b1065931095b29f501e66fcc82f28446
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.31` - linux; amd64

```console
$ docker pull liquibase@sha256:4393667a2c6c53051a4d92d64d98c11a66631f53927035f3af23d34692978626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.9 MB (445887300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ca17a151a4e574d9108fb5c37f17e0f421b63d8bdf4d24b29b702b010d89a7`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

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
# Thu, 16 Jan 2025 15:44:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Jan 2025 15:44:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Jan 2025 15:44:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Thu, 16 Jan 2025 15:44:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
WORKDIR /liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_VERSION=0.2.8
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 16 Jan 2025 15:44:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
USER liquibase:liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb863ad3341b296314c0087afee51d271d66481a9c4c93543fea5cb3f2b0034`  
		Last Modified: Wed, 22 Jan 2025 18:28:02 GMT  
		Size: 16.1 MB (16144395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1aa630608356fc36b220aabcb3685a1860a2e3ad37841d355b189fba38875d3`  
		Last Modified: Wed, 22 Jan 2025 18:28:02 GMT  
		Size: 46.9 MB (46942122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7439c7b9afaefa8b208dfb371dbf621f71db1e1ee5b5b14bf598265b787a34a7`  
		Last Modified: Wed, 22 Jan 2025 18:28:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0da6393fd47cfa1a49b58091b48da741160efaefb8c68549b15e6d93ed3547`  
		Last Modified: Wed, 22 Jan 2025 18:28:01 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4781d8fc7539ac0f0a72679b4da255bd1827322f9930a387e2dcd4d8ae09b3b6`  
		Last Modified: Wed, 22 Jan 2025 19:38:47 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3577a9087270301d0feed27ee2a5ce7a526d509a30857c2d554f5dff3bd9de7f`  
		Last Modified: Wed, 22 Jan 2025 19:38:52 GMT  
		Size: 349.9 MB (349941637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3600e3d3ffffe9b40e02c21f5a529d0aa57f01947d993b3adde7529f844850b8`  
		Last Modified: Wed, 22 Jan 2025 19:38:47 GMT  
		Size: 3.3 MB (3318503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8228f6ce5428de4be7d2c223e36a2288567d6b2ce89074dcf4ef271d5543419`  
		Last Modified: Wed, 22 Jan 2025 19:38:47 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d981ee7570b746798b95df188b9859be1357484e8ce3ddc7b4ff0e6315ae2c`  
		Last Modified: Wed, 22 Jan 2025 19:38:47 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31` - unknown; unknown

```console
$ docker pull liquibase@sha256:e0ee55669d219dda0200cbb67735750775cba0ab2ab6bdb27fd9305386dbea43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3777396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a0f7c176f71ee8b75f34150d7d0866ce4fe51270cc7aa731fe0efa4cf5d113`

```dockerfile
```

-	Layers:
	-	`sha256:3f4dd2b219581f55218c393976fd9e31421d42c905a6e4dc42a857e057d6a7ee`  
		Last Modified: Wed, 22 Jan 2025 19:38:47 GMT  
		Size: 3.8 MB (3753213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed7659c8460ef8e0ebe67e96616cf080b2433a70032d02373bb075d8ba52e97b`  
		Last Modified: Wed, 22 Jan 2025 19:38:46 GMT  
		Size: 24.2 KB (24183 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.31` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:28b58cc60833609ce321978752bc9e7057cb87c42e00e188284910144232bd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.9 MB (442870933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2242c27af7518ca89274716d925601509556430d234dc16318fc6ca5a5a53ae6`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

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
# Thu, 16 Jan 2025 15:44:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Jan 2025 15:44:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Jan 2025 15:44:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Thu, 16 Jan 2025 15:44:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
WORKDIR /liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_VERSION=0.2.8
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 16 Jan 2025 15:44:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
USER liquibase:liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243c5e4bb1eb8f1bbd43779267016247aca843f7e671517c7f6bb4e5c737feb6`  
		Last Modified: Wed, 22 Jan 2025 20:51:45 GMT  
		Size: 16.1 MB (16062040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f15d754f13637785ee83c8f02dedc6535a18b074a46e44098fa8d58b719bc2`  
		Last Modified: Wed, 22 Jan 2025 21:06:25 GMT  
		Size: 46.4 MB (46430843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bb012a5de5a854470c1e7d79344bc7d87dbbf3389d4dd87d2d3747a3b9d282`  
		Last Modified: Wed, 22 Jan 2025 21:06:23 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784e930507116914928109ec13f072db1541abbfb6834ba65500903c9ac399f8`  
		Last Modified: Wed, 22 Jan 2025 21:06:23 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80cdb37c3f9637933e7771a701b4da902ad3f0aa64e2cefc925876cc75f26b5`  
		Last Modified: Thu, 23 Jan 2025 00:47:25 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a3ce3ae7cb82ef6fb85724754f90ead7ce0a289be3a1ee6701d9c470e8b224`  
		Last Modified: Thu, 23 Jan 2025 00:47:34 GMT  
		Size: 349.9 MB (349941637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1920c2576d263bf4dc17b26aef96033b5034961e1d491368d63755543b9aca`  
		Last Modified: Thu, 23 Jan 2025 00:47:26 GMT  
		Size: 3.1 MB (3073123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af66527cd185f80c21451cb47d292f4976d6dfd3207fcf3155fe00db0e88611`  
		Last Modified: Thu, 23 Jan 2025 00:47:26 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd7cbe7cdf250928b5c8e09146b2a1ed38a038f88b911e4c1d41dcd5d43960a`  
		Last Modified: Thu, 23 Jan 2025 00:47:27 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31` - unknown; unknown

```console
$ docker pull liquibase@sha256:5bc05b45a088c2a85b8cc934aff0e44168c1d7d494fef6d10b5ec505b46f8761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3777187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7e5e32645a956486a1ed27436332721ad0d015dfa0c7fb479dfad0f900cead`

```dockerfile
```

-	Layers:
	-	`sha256:9462d0e7057b3f2c07775a143e6f5f95790affcbb6b4f7d5d3651d6552ea5354`  
		Last Modified: Thu, 23 Jan 2025 00:47:25 GMT  
		Size: 3.8 MB (3752881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25079a4261e29ed8245597baa4120e47a41e00dad7768f5f35256a087216aaf6`  
		Last Modified: Thu, 23 Jan 2025 00:47:25 GMT  
		Size: 24.3 KB (24306 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.31-alpine`

```console
$ docker pull liquibase@sha256:4e2e21aa8763a2cbde8884fe23bd68b16bd901d6c5d0c309b85b396a04fc89e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.31-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:4d4c4e6b01bb1849c6637c1faf12507f5336086142ac5b9137566d7a0aec2b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.5 MB (419452638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d0aa58c00593567782301ea58b8f1416c454d90f1d0aa2c470d44f66acf026`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
WORKDIR /liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_VERSION=0.2.8
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 16 Jan 2025 15:44:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
USER liquibase:liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cfdb1cc9af0f4bfeadb9a483871c7b92f349a71aabc22766f7ec4ab1f0c63f`  
		Last Modified: Fri, 17 Jan 2025 00:28:29 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b62bcc79f6cc7b83b3e0ae27a7b84501fc721d4cd9b24f6e4e76b500cb3fe9`  
		Last Modified: Fri, 17 Jan 2025 00:28:30 GMT  
		Size: 62.6 MB (62620648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fd8e69c0017b56ee85c58ddf9669db8fcf06baf5277bc8c1d32d531773baf3`  
		Last Modified: Fri, 17 Jan 2025 00:28:36 GMT  
		Size: 350.0 MB (349963250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7f77e33446daaf902860d5e071509ac0118e9924d89e9752d1c7774de646e5`  
		Last Modified: Fri, 17 Jan 2025 00:28:30 GMT  
		Size: 3.2 MB (3240815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1ed0691ae4334ade6912c60e1417ea0a4b61b87ac02a2c33de3bd210e3ce9a`  
		Last Modified: Fri, 17 Jan 2025 00:28:30 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6f2dfc4b32135e9898212db687eea00b11c18b0426ecf8bafacb204454aa76`  
		Last Modified: Fri, 17 Jan 2025 00:28:30 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:5ebe166243a0c0b4a83e535da649ac258104a81aa0cac1df8769b54f8ee10c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.5 KB (401456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd59e424bfab0949fe99c2448e20a305b92e07ed04d81af7c0e13dd397f8275`

```dockerfile
```

-	Layers:
	-	`sha256:2d28198f5ad4c44413f8dcbfa06c68beee9cb643f3d26745884aad86a97468e5`  
		Last Modified: Fri, 17 Jan 2025 00:28:29 GMT  
		Size: 380.2 KB (380192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94fe91c4ea0a2c27dd2f9183918a323926e5caa52a8ff1e41da22fdad140dddc`  
		Last Modified: Fri, 17 Jan 2025 00:28:29 GMT  
		Size: 21.3 KB (21264 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.31-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:64f15a560575b60d6e7ae66add327a2d33ce0f5c2d862e3eca5b3ede9d89117c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.4 MB (419383883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ad514e4659194b10e209f402b4864275d537f90e215919594fc1e496a68041`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
WORKDIR /liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_VERSION=0.2.8
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 16 Jan 2025 15:44:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
USER liquibase:liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20133965a445a51efec08698b15cc30f0e8d8b3ba4874f704847238bba2d6b18`  
		Last Modified: Fri, 17 Jan 2025 00:29:47 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f99ff802bc3b4546d071b22870183d574e9c4e0c071535f935a9c592c89bee`  
		Last Modified: Fri, 17 Jan 2025 00:29:50 GMT  
		Size: 62.3 MB (62336531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514880a20c46e691f022ab9e0ab445eb32a56150840c38a39caf3d0eb424f053`  
		Last Modified: Fri, 17 Jan 2025 00:29:54 GMT  
		Size: 350.0 MB (349963136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487a1bbbf4be472664907276d5e140733530492d91248b5d27d5fa00a628df2`  
		Last Modified: Fri, 17 Jan 2025 00:29:48 GMT  
		Size: 3.0 MB (2991776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24c50b270e89908b6676bf3d47470a612f6239e4d8d88b4d92089634ecc3fc5`  
		Last Modified: Fri, 17 Jan 2025 00:29:48 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae42e39fed8f1ac01e1b021649411080342ad4c3e1ebea13c7a576e1f7b7f62`  
		Last Modified: Fri, 17 Jan 2025 00:29:49 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:312cd0e1d22d8b8d80a2dc3d6ac868fcad3e77c9593503737c9f928b7d60a851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.8 KB (400840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a4a397a5338f1ef34ed873807f9b1190cae7faf9c75bb2ec59340c8abdda19`

```dockerfile
```

-	Layers:
	-	`sha256:425a47641509df5fba142252d0e1d5fd1458962f1649ce714201181877abf5f7`  
		Last Modified: Fri, 17 Jan 2025 00:29:47 GMT  
		Size: 379.4 KB (379439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73e7762ff664571ee559f73c2ef019e94d53e5b5a937cdd8980c4b770a94d2a`  
		Last Modified: Fri, 17 Jan 2025 00:29:47 GMT  
		Size: 21.4 KB (21401 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.31.0`

```console
$ docker pull liquibase@sha256:c40d47b2eefe08f1d423bc9e06de06b1b1065931095b29f501e66fcc82f28446
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.31.0` - linux; amd64

```console
$ docker pull liquibase@sha256:4393667a2c6c53051a4d92d64d98c11a66631f53927035f3af23d34692978626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.9 MB (445887300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ca17a151a4e574d9108fb5c37f17e0f421b63d8bdf4d24b29b702b010d89a7`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

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
# Thu, 16 Jan 2025 15:44:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Jan 2025 15:44:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Jan 2025 15:44:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Thu, 16 Jan 2025 15:44:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
WORKDIR /liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_VERSION=0.2.8
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 16 Jan 2025 15:44:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
USER liquibase:liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb863ad3341b296314c0087afee51d271d66481a9c4c93543fea5cb3f2b0034`  
		Last Modified: Wed, 22 Jan 2025 18:28:02 GMT  
		Size: 16.1 MB (16144395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1aa630608356fc36b220aabcb3685a1860a2e3ad37841d355b189fba38875d3`  
		Last Modified: Wed, 22 Jan 2025 18:28:02 GMT  
		Size: 46.9 MB (46942122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7439c7b9afaefa8b208dfb371dbf621f71db1e1ee5b5b14bf598265b787a34a7`  
		Last Modified: Wed, 22 Jan 2025 18:28:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0da6393fd47cfa1a49b58091b48da741160efaefb8c68549b15e6d93ed3547`  
		Last Modified: Wed, 22 Jan 2025 18:28:01 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4781d8fc7539ac0f0a72679b4da255bd1827322f9930a387e2dcd4d8ae09b3b6`  
		Last Modified: Wed, 22 Jan 2025 19:38:47 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3577a9087270301d0feed27ee2a5ce7a526d509a30857c2d554f5dff3bd9de7f`  
		Last Modified: Wed, 22 Jan 2025 19:38:52 GMT  
		Size: 349.9 MB (349941637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3600e3d3ffffe9b40e02c21f5a529d0aa57f01947d993b3adde7529f844850b8`  
		Last Modified: Wed, 22 Jan 2025 19:38:47 GMT  
		Size: 3.3 MB (3318503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8228f6ce5428de4be7d2c223e36a2288567d6b2ce89074dcf4ef271d5543419`  
		Last Modified: Wed, 22 Jan 2025 19:38:47 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d981ee7570b746798b95df188b9859be1357484e8ce3ddc7b4ff0e6315ae2c`  
		Last Modified: Wed, 22 Jan 2025 19:38:47 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:e0ee55669d219dda0200cbb67735750775cba0ab2ab6bdb27fd9305386dbea43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3777396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a0f7c176f71ee8b75f34150d7d0866ce4fe51270cc7aa731fe0efa4cf5d113`

```dockerfile
```

-	Layers:
	-	`sha256:3f4dd2b219581f55218c393976fd9e31421d42c905a6e4dc42a857e057d6a7ee`  
		Last Modified: Wed, 22 Jan 2025 19:38:47 GMT  
		Size: 3.8 MB (3753213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed7659c8460ef8e0ebe67e96616cf080b2433a70032d02373bb075d8ba52e97b`  
		Last Modified: Wed, 22 Jan 2025 19:38:46 GMT  
		Size: 24.2 KB (24183 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.31.0` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:28b58cc60833609ce321978752bc9e7057cb87c42e00e188284910144232bd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.9 MB (442870933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2242c27af7518ca89274716d925601509556430d234dc16318fc6ca5a5a53ae6`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

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
# Thu, 16 Jan 2025 15:44:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Jan 2025 15:44:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Jan 2025 15:44:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Thu, 16 Jan 2025 15:44:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
WORKDIR /liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_VERSION=0.2.8
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 16 Jan 2025 15:44:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
USER liquibase:liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243c5e4bb1eb8f1bbd43779267016247aca843f7e671517c7f6bb4e5c737feb6`  
		Last Modified: Wed, 22 Jan 2025 20:51:45 GMT  
		Size: 16.1 MB (16062040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f15d754f13637785ee83c8f02dedc6535a18b074a46e44098fa8d58b719bc2`  
		Last Modified: Wed, 22 Jan 2025 21:06:25 GMT  
		Size: 46.4 MB (46430843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bb012a5de5a854470c1e7d79344bc7d87dbbf3389d4dd87d2d3747a3b9d282`  
		Last Modified: Wed, 22 Jan 2025 21:06:23 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784e930507116914928109ec13f072db1541abbfb6834ba65500903c9ac399f8`  
		Last Modified: Wed, 22 Jan 2025 21:06:23 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80cdb37c3f9637933e7771a701b4da902ad3f0aa64e2cefc925876cc75f26b5`  
		Last Modified: Thu, 23 Jan 2025 00:47:25 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a3ce3ae7cb82ef6fb85724754f90ead7ce0a289be3a1ee6701d9c470e8b224`  
		Last Modified: Thu, 23 Jan 2025 00:47:34 GMT  
		Size: 349.9 MB (349941637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1920c2576d263bf4dc17b26aef96033b5034961e1d491368d63755543b9aca`  
		Last Modified: Thu, 23 Jan 2025 00:47:26 GMT  
		Size: 3.1 MB (3073123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af66527cd185f80c21451cb47d292f4976d6dfd3207fcf3155fe00db0e88611`  
		Last Modified: Thu, 23 Jan 2025 00:47:26 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd7cbe7cdf250928b5c8e09146b2a1ed38a038f88b911e4c1d41dcd5d43960a`  
		Last Modified: Thu, 23 Jan 2025 00:47:27 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31.0` - unknown; unknown

```console
$ docker pull liquibase@sha256:5bc05b45a088c2a85b8cc934aff0e44168c1d7d494fef6d10b5ec505b46f8761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3777187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7e5e32645a956486a1ed27436332721ad0d015dfa0c7fb479dfad0f900cead`

```dockerfile
```

-	Layers:
	-	`sha256:9462d0e7057b3f2c07775a143e6f5f95790affcbb6b4f7d5d3651d6552ea5354`  
		Last Modified: Thu, 23 Jan 2025 00:47:25 GMT  
		Size: 3.8 MB (3752881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25079a4261e29ed8245597baa4120e47a41e00dad7768f5f35256a087216aaf6`  
		Last Modified: Thu, 23 Jan 2025 00:47:25 GMT  
		Size: 24.3 KB (24306 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:4.31.0-alpine`

```console
$ docker pull liquibase@sha256:4e2e21aa8763a2cbde8884fe23bd68b16bd901d6c5d0c309b85b396a04fc89e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:4.31.0-alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:4d4c4e6b01bb1849c6637c1faf12507f5336086142ac5b9137566d7a0aec2b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.5 MB (419452638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d0aa58c00593567782301ea58b8f1416c454d90f1d0aa2c470d44f66acf026`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
WORKDIR /liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_VERSION=0.2.8
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 16 Jan 2025 15:44:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
USER liquibase:liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cfdb1cc9af0f4bfeadb9a483871c7b92f349a71aabc22766f7ec4ab1f0c63f`  
		Last Modified: Fri, 17 Jan 2025 00:28:29 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b62bcc79f6cc7b83b3e0ae27a7b84501fc721d4cd9b24f6e4e76b500cb3fe9`  
		Last Modified: Fri, 17 Jan 2025 00:28:30 GMT  
		Size: 62.6 MB (62620648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fd8e69c0017b56ee85c58ddf9669db8fcf06baf5277bc8c1d32d531773baf3`  
		Last Modified: Fri, 17 Jan 2025 00:28:36 GMT  
		Size: 350.0 MB (349963250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7f77e33446daaf902860d5e071509ac0118e9924d89e9752d1c7774de646e5`  
		Last Modified: Fri, 17 Jan 2025 00:28:30 GMT  
		Size: 3.2 MB (3240815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1ed0691ae4334ade6912c60e1417ea0a4b61b87ac02a2c33de3bd210e3ce9a`  
		Last Modified: Fri, 17 Jan 2025 00:28:30 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6f2dfc4b32135e9898212db687eea00b11c18b0426ecf8bafacb204454aa76`  
		Last Modified: Fri, 17 Jan 2025 00:28:30 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:5ebe166243a0c0b4a83e535da649ac258104a81aa0cac1df8769b54f8ee10c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.5 KB (401456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd59e424bfab0949fe99c2448e20a305b92e07ed04d81af7c0e13dd397f8275`

```dockerfile
```

-	Layers:
	-	`sha256:2d28198f5ad4c44413f8dcbfa06c68beee9cb643f3d26745884aad86a97468e5`  
		Last Modified: Fri, 17 Jan 2025 00:28:29 GMT  
		Size: 380.2 KB (380192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94fe91c4ea0a2c27dd2f9183918a323926e5caa52a8ff1e41da22fdad140dddc`  
		Last Modified: Fri, 17 Jan 2025 00:28:29 GMT  
		Size: 21.3 KB (21264 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:4.31.0-alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:64f15a560575b60d6e7ae66add327a2d33ce0f5c2d862e3eca5b3ede9d89117c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.4 MB (419383883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ad514e4659194b10e209f402b4864275d537f90e215919594fc1e496a68041`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
WORKDIR /liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_VERSION=0.2.8
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 16 Jan 2025 15:44:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
USER liquibase:liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20133965a445a51efec08698b15cc30f0e8d8b3ba4874f704847238bba2d6b18`  
		Last Modified: Fri, 17 Jan 2025 00:29:47 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f99ff802bc3b4546d071b22870183d574e9c4e0c071535f935a9c592c89bee`  
		Last Modified: Fri, 17 Jan 2025 00:29:50 GMT  
		Size: 62.3 MB (62336531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514880a20c46e691f022ab9e0ab445eb32a56150840c38a39caf3d0eb424f053`  
		Last Modified: Fri, 17 Jan 2025 00:29:54 GMT  
		Size: 350.0 MB (349963136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487a1bbbf4be472664907276d5e140733530492d91248b5d27d5fa00a628df2`  
		Last Modified: Fri, 17 Jan 2025 00:29:48 GMT  
		Size: 3.0 MB (2991776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24c50b270e89908b6676bf3d47470a612f6239e4d8d88b4d92089634ecc3fc5`  
		Last Modified: Fri, 17 Jan 2025 00:29:48 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae42e39fed8f1ac01e1b021649411080342ad4c3e1ebea13c7a576e1f7b7f62`  
		Last Modified: Fri, 17 Jan 2025 00:29:49 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:4.31.0-alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:312cd0e1d22d8b8d80a2dc3d6ac868fcad3e77c9593503737c9f928b7d60a851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.8 KB (400840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a4a397a5338f1ef34ed873807f9b1190cae7faf9c75bb2ec59340c8abdda19`

```dockerfile
```

-	Layers:
	-	`sha256:425a47641509df5fba142252d0e1d5fd1458962f1649ce714201181877abf5f7`  
		Last Modified: Fri, 17 Jan 2025 00:29:47 GMT  
		Size: 379.4 KB (379439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73e7762ff664571ee559f73c2ef019e94d53e5b5a937cdd8980c4b770a94d2a`  
		Last Modified: Fri, 17 Jan 2025 00:29:47 GMT  
		Size: 21.4 KB (21401 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:4e2e21aa8763a2cbde8884fe23bd68b16bd901d6c5d0c309b85b396a04fc89e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:4d4c4e6b01bb1849c6637c1faf12507f5336086142ac5b9137566d7a0aec2b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.5 MB (419452638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d0aa58c00593567782301ea58b8f1416c454d90f1d0aa2c470d44f66acf026`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
WORKDIR /liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_VERSION=0.2.8
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 16 Jan 2025 15:44:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
USER liquibase:liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cfdb1cc9af0f4bfeadb9a483871c7b92f349a71aabc22766f7ec4ab1f0c63f`  
		Last Modified: Fri, 17 Jan 2025 00:28:29 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b62bcc79f6cc7b83b3e0ae27a7b84501fc721d4cd9b24f6e4e76b500cb3fe9`  
		Last Modified: Fri, 17 Jan 2025 00:28:30 GMT  
		Size: 62.6 MB (62620648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fd8e69c0017b56ee85c58ddf9669db8fcf06baf5277bc8c1d32d531773baf3`  
		Last Modified: Fri, 17 Jan 2025 00:28:36 GMT  
		Size: 350.0 MB (349963250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7f77e33446daaf902860d5e071509ac0118e9924d89e9752d1c7774de646e5`  
		Last Modified: Fri, 17 Jan 2025 00:28:30 GMT  
		Size: 3.2 MB (3240815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1ed0691ae4334ade6912c60e1417ea0a4b61b87ac02a2c33de3bd210e3ce9a`  
		Last Modified: Fri, 17 Jan 2025 00:28:30 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6f2dfc4b32135e9898212db687eea00b11c18b0426ecf8bafacb204454aa76`  
		Last Modified: Fri, 17 Jan 2025 00:28:30 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:5ebe166243a0c0b4a83e535da649ac258104a81aa0cac1df8769b54f8ee10c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.5 KB (401456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd59e424bfab0949fe99c2448e20a305b92e07ed04d81af7c0e13dd397f8275`

```dockerfile
```

-	Layers:
	-	`sha256:2d28198f5ad4c44413f8dcbfa06c68beee9cb643f3d26745884aad86a97468e5`  
		Last Modified: Fri, 17 Jan 2025 00:28:29 GMT  
		Size: 380.2 KB (380192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94fe91c4ea0a2c27dd2f9183918a323926e5caa52a8ff1e41da22fdad140dddc`  
		Last Modified: Fri, 17 Jan 2025 00:28:29 GMT  
		Size: 21.3 KB (21264 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:64f15a560575b60d6e7ae66add327a2d33ce0f5c2d862e3eca5b3ede9d89117c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.4 MB (419383883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ad514e4659194b10e209f402b4864275d537f90e215919594fc1e496a68041`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
WORKDIR /liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_VERSION=0.2.8
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 16 Jan 2025 15:44:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
USER liquibase:liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20133965a445a51efec08698b15cc30f0e8d8b3ba4874f704847238bba2d6b18`  
		Last Modified: Fri, 17 Jan 2025 00:29:47 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f99ff802bc3b4546d071b22870183d574e9c4e0c071535f935a9c592c89bee`  
		Last Modified: Fri, 17 Jan 2025 00:29:50 GMT  
		Size: 62.3 MB (62336531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514880a20c46e691f022ab9e0ab445eb32a56150840c38a39caf3d0eb424f053`  
		Last Modified: Fri, 17 Jan 2025 00:29:54 GMT  
		Size: 350.0 MB (349963136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487a1bbbf4be472664907276d5e140733530492d91248b5d27d5fa00a628df2`  
		Last Modified: Fri, 17 Jan 2025 00:29:48 GMT  
		Size: 3.0 MB (2991776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24c50b270e89908b6676bf3d47470a612f6239e4d8d88b4d92089634ecc3fc5`  
		Last Modified: Fri, 17 Jan 2025 00:29:48 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae42e39fed8f1ac01e1b021649411080342ad4c3e1ebea13c7a576e1f7b7f62`  
		Last Modified: Fri, 17 Jan 2025 00:29:49 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:312cd0e1d22d8b8d80a2dc3d6ac868fcad3e77c9593503737c9f928b7d60a851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.8 KB (400840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a4a397a5338f1ef34ed873807f9b1190cae7faf9c75bb2ec59340c8abdda19`

```dockerfile
```

-	Layers:
	-	`sha256:425a47641509df5fba142252d0e1d5fd1458962f1649ce714201181877abf5f7`  
		Last Modified: Fri, 17 Jan 2025 00:29:47 GMT  
		Size: 379.4 KB (379439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73e7762ff664571ee559f73c2ef019e94d53e5b5a937cdd8980c4b770a94d2a`  
		Last Modified: Fri, 17 Jan 2025 00:29:47 GMT  
		Size: 21.4 KB (21401 bytes)  
		MIME: application/vnd.in-toto+json

## `liquibase:latest`

```console
$ docker pull liquibase@sha256:c40d47b2eefe08f1d423bc9e06de06b1b1065931095b29f501e66fcc82f28446
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:latest` - linux; amd64

```console
$ docker pull liquibase@sha256:4393667a2c6c53051a4d92d64d98c11a66631f53927035f3af23d34692978626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.9 MB (445887300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ca17a151a4e574d9108fb5c37f17e0f421b63d8bdf4d24b29b702b010d89a7`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

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
# Thu, 16 Jan 2025 15:44:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Jan 2025 15:44:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Jan 2025 15:44:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Thu, 16 Jan 2025 15:44:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
WORKDIR /liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_VERSION=0.2.8
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 16 Jan 2025 15:44:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
USER liquibase:liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb863ad3341b296314c0087afee51d271d66481a9c4c93543fea5cb3f2b0034`  
		Last Modified: Wed, 22 Jan 2025 18:28:02 GMT  
		Size: 16.1 MB (16144395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1aa630608356fc36b220aabcb3685a1860a2e3ad37841d355b189fba38875d3`  
		Last Modified: Wed, 22 Jan 2025 18:28:02 GMT  
		Size: 46.9 MB (46942122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7439c7b9afaefa8b208dfb371dbf621f71db1e1ee5b5b14bf598265b787a34a7`  
		Last Modified: Wed, 22 Jan 2025 18:28:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0da6393fd47cfa1a49b58091b48da741160efaefb8c68549b15e6d93ed3547`  
		Last Modified: Wed, 22 Jan 2025 18:28:01 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4781d8fc7539ac0f0a72679b4da255bd1827322f9930a387e2dcd4d8ae09b3b6`  
		Last Modified: Wed, 22 Jan 2025 19:38:47 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3577a9087270301d0feed27ee2a5ce7a526d509a30857c2d554f5dff3bd9de7f`  
		Last Modified: Wed, 22 Jan 2025 19:38:52 GMT  
		Size: 349.9 MB (349941637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3600e3d3ffffe9b40e02c21f5a529d0aa57f01947d993b3adde7529f844850b8`  
		Last Modified: Wed, 22 Jan 2025 19:38:47 GMT  
		Size: 3.3 MB (3318503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8228f6ce5428de4be7d2c223e36a2288567d6b2ce89074dcf4ef271d5543419`  
		Last Modified: Wed, 22 Jan 2025 19:38:47 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d981ee7570b746798b95df188b9859be1357484e8ce3ddc7b4ff0e6315ae2c`  
		Last Modified: Wed, 22 Jan 2025 19:38:47 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:e0ee55669d219dda0200cbb67735750775cba0ab2ab6bdb27fd9305386dbea43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3777396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a0f7c176f71ee8b75f34150d7d0866ce4fe51270cc7aa731fe0efa4cf5d113`

```dockerfile
```

-	Layers:
	-	`sha256:3f4dd2b219581f55218c393976fd9e31421d42c905a6e4dc42a857e057d6a7ee`  
		Last Modified: Wed, 22 Jan 2025 19:38:47 GMT  
		Size: 3.8 MB (3753213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed7659c8460ef8e0ebe67e96616cf080b2433a70032d02373bb075d8ba52e97b`  
		Last Modified: Wed, 22 Jan 2025 19:38:46 GMT  
		Size: 24.2 KB (24183 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:latest` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:28b58cc60833609ce321978752bc9e7057cb87c42e00e188284910144232bd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.9 MB (442870933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2242c27af7518ca89274716d925601509556430d234dc16318fc6ca5a5a53ae6`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

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
# Thu, 16 Jan 2025 15:44:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Jan 2025 15:44:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Jan 2025 15:44:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Thu, 16 Jan 2025 15:44:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
RUN groupadd --gid 1001 liquibase &&     useradd --uid 1001 --gid liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
WORKDIR /liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LIQUIBASE_VERSION=4.31.0
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d
RUN wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_VERSION=0.2.8
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 16 Jan 2025 15:44:27 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 16 Jan 2025 15:44:27 GMT
# ARGS: LIQUIBASE_VERSION=4.31.0 LB_SHA256=ffcf80c34c8b05a50c32c423ad2899aa9e7a5cd40097628f2bc739b70654962d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN apt-get update &&     apt-get -yqq install unzip --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     mkdir /liquibase/bin &&     arch="$(dpkg --print-architecture)" &&     case "$arch" in       amd64)  DOWNLOAD_ARCH=""  ;;       arm64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apt-get purge -y --auto-remove unzip &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 16 Jan 2025 15:44:27 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 16 Jan 2025 15:44:27 GMT
USER liquibase:liquibase
# Thu, 16 Jan 2025 15:44:27 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 16 Jan 2025 15:44:27 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243c5e4bb1eb8f1bbd43779267016247aca843f7e671517c7f6bb4e5c737feb6`  
		Last Modified: Wed, 22 Jan 2025 20:51:45 GMT  
		Size: 16.1 MB (16062040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f15d754f13637785ee83c8f02dedc6535a18b074a46e44098fa8d58b719bc2`  
		Last Modified: Wed, 22 Jan 2025 21:06:25 GMT  
		Size: 46.4 MB (46430843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bb012a5de5a854470c1e7d79344bc7d87dbbf3389d4dd87d2d3747a3b9d282`  
		Last Modified: Wed, 22 Jan 2025 21:06:23 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784e930507116914928109ec13f072db1541abbfb6834ba65500903c9ac399f8`  
		Last Modified: Wed, 22 Jan 2025 21:06:23 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80cdb37c3f9637933e7771a701b4da902ad3f0aa64e2cefc925876cc75f26b5`  
		Last Modified: Thu, 23 Jan 2025 00:47:25 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a3ce3ae7cb82ef6fb85724754f90ead7ce0a289be3a1ee6701d9c470e8b224`  
		Last Modified: Thu, 23 Jan 2025 00:47:34 GMT  
		Size: 349.9 MB (349941637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1920c2576d263bf4dc17b26aef96033b5034961e1d491368d63755543b9aca`  
		Last Modified: Thu, 23 Jan 2025 00:47:26 GMT  
		Size: 3.1 MB (3073123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af66527cd185f80c21451cb47d292f4976d6dfd3207fcf3155fe00db0e88611`  
		Last Modified: Thu, 23 Jan 2025 00:47:26 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd7cbe7cdf250928b5c8e09146b2a1ed38a038f88b911e4c1d41dcd5d43960a`  
		Last Modified: Thu, 23 Jan 2025 00:47:27 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:latest` - unknown; unknown

```console
$ docker pull liquibase@sha256:5bc05b45a088c2a85b8cc934aff0e44168c1d7d494fef6d10b5ec505b46f8761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3777187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7e5e32645a956486a1ed27436332721ad0d015dfa0c7fb479dfad0f900cead`

```dockerfile
```

-	Layers:
	-	`sha256:9462d0e7057b3f2c07775a143e6f5f95790affcbb6b4f7d5d3651d6552ea5354`  
		Last Modified: Thu, 23 Jan 2025 00:47:25 GMT  
		Size: 3.8 MB (3752881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25079a4261e29ed8245597baa4120e47a41e00dad7768f5f35256a087216aaf6`  
		Last Modified: Thu, 23 Jan 2025 00:47:25 GMT  
		Size: 24.3 KB (24306 bytes)  
		MIME: application/vnd.in-toto+json
