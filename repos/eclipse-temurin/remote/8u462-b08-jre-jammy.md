## `eclipse-temurin:8u462-b08-jre-jammy`

```console
$ docker pull eclipse-temurin@sha256:5814be04c2da20369c06c9b123680335a95c6f62507ed639c0ad17e4598e8d8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8u462-b08-jre-jammy` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:2149d7d7a06acdd4806aff9831c19d03f410a241fd894a26465b474f55581f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87568366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0d1589707c8af1ba1cf219dd4f8e43c6930ea1d49454a2c4ef2a1116d7b28b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6e83ffc37da053352ccaa2fd3bd7d813b9674d87aa01b35ac3e54903cd33b0d8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='c34506736ab52768c59660a5d4246b94f57543c79b7e4b53d322dda3ec4a9302';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='48547114cef3ce1ab8e80c8140430d8fb2f23359d52ad6d7a0af28f5fe9c81f8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='15391b2d1bf613abd739f6ad6eeb728f4803d901cceae0d83f6bbd00da7751bf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e55dcd53039600153e2a94a9e2b80efcc495298c45daafa710e2cbaac558849`  
		Last Modified: Tue, 12 Aug 2025 17:24:20 GMT  
		Size: 16.2 MB (16150690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5371ab33cafe88ac32a90f8f47a31f59f83b87e1e4252a5b5f616c5033b83e89`  
		Last Modified: Tue, 12 Aug 2025 17:24:24 GMT  
		Size: 41.9 MB (41878272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1713cbd6be740f362b10d79d234cb4132272380f2e7e1c09462cb30439d3575b`  
		Last Modified: Tue, 12 Aug 2025 17:24:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9456c27737eb949b81db43a51b05c1096d5637db00cc473b7e13018b17b9a92`  
		Last Modified: Tue, 12 Aug 2025 17:24:16 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u462-b08-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c86792ad342f40b514e6fe6cfef1e9d268b625ad60d9d261cd30f2fb0d3fd758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78028f170618b304c089067c554b7f6584cc0841bdbc746a848c881557ebd9bd`

```dockerfile
```

-	Layers:
	-	`sha256:37722a0ace4a4fab3e69ebdd907f123c038ea0a6428b86cbb5d875263a749a09`  
		Last Modified: Tue, 12 Aug 2025 18:19:53 GMT  
		Size: 3.9 MB (3909453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cabd3e03fdbc19f2ab3fd7750cd0edd59064628dab1249bccf574bdb3334c02`  
		Last Modified: Tue, 12 Aug 2025 18:19:54 GMT  
		Size: 22.0 KB (21960 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u462-b08-jre-jammy` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:544dfe595635e5226024af8a1f1a341dbc23a7ba817ee446675ec16233c8f2b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81898021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98da59156b033e4007e4618057a933ccabf4455fec6e6f6c6ec97672565325b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:02 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:05 GMT
ADD file:56dd1608fa49343c3815b8373825d581303e97b21994ce0e1d099bf09251caea in / 
# Wed, 30 Jul 2025 05:34:06 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6e83ffc37da053352ccaa2fd3bd7d813b9674d87aa01b35ac3e54903cd33b0d8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='c34506736ab52768c59660a5d4246b94f57543c79b7e4b53d322dda3ec4a9302';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='48547114cef3ce1ab8e80c8140430d8fb2f23359d52ad6d7a0af28f5fe9c81f8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='15391b2d1bf613abd739f6ad6eeb728f4803d901cceae0d83f6bbd00da7751bf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6530e67fdf3958f32e486561f05a1170b5fbcd419c51eb435b13993ecadad7b3`  
		Last Modified: Tue, 12 Aug 2025 17:02:44 GMT  
		Size: 26.6 MB (26642919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da254942fc2ae7b2cdf3f227af1c842bdebbd1573712272ea2efe9e8d35cdaa`  
		Last Modified: Tue, 12 Aug 2025 17:25:53 GMT  
		Size: 15.9 MB (15889812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce074fd9a9631f23d8abc1e2f5330eaed12cc92511466616025685a6cd8d3f5f`  
		Last Modified: Tue, 12 Aug 2025 20:21:06 GMT  
		Size: 39.4 MB (39362881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8fffa100a5152402eb0ea59cdf3080c46e3c3f1082ad63444ae6b785d8cbd8`  
		Last Modified: Tue, 12 Aug 2025 19:22:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3fb54cadcd61cd78d78c2e11a3ee223b9588fd05980806b26ff7d67aaca8e6`  
		Last Modified: Tue, 12 Aug 2025 19:22:13 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u462-b08-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:224ae24a529be14653dd88f72dcdcbcc712f4b2d7064cecbcd878ce928cc661a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3937500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9df0146e4201e557c57e2c99dd95f4142a09d44c982964e821febb0a3147b12`

```dockerfile
```

-	Layers:
	-	`sha256:410be338b9890493cf744dd1075f3c0ed947ea078d2a6ff78ec08fcd8dc82197`  
		Last Modified: Tue, 12 Aug 2025 18:19:59 GMT  
		Size: 3.9 MB (3915454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1662cf24f868ed2322e7c43062a51946cb40a668fa08752d664fb8d2843de73`  
		Last Modified: Tue, 12 Aug 2025 18:20:00 GMT  
		Size: 22.0 KB (22046 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u462-b08-jre-jammy` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:86079959967522bb1757d1f4faa5f91eac4fa4472cb2c8e7a94b054ee363a66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84305329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4db08a4956602e3cad0a97a0857777e816512bcfcf82d773e6e0b9f49c1211c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6e83ffc37da053352ccaa2fd3bd7d813b9674d87aa01b35ac3e54903cd33b0d8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='c34506736ab52768c59660a5d4246b94f57543c79b7e4b53d322dda3ec4a9302';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='48547114cef3ce1ab8e80c8140430d8fb2f23359d52ad6d7a0af28f5fe9c81f8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='15391b2d1bf613abd739f6ad6eeb728f4803d901cceae0d83f6bbd00da7751bf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b5bc71170396faf6c1c291a060d5d6b6d6700719a4f7f1f47d7e8a843b7a6d`  
		Last Modified: Tue, 12 Aug 2025 18:31:02 GMT  
		Size: 16.1 MB (16063741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d6be77cef32ae0c6e3be94aaf7a3791cb9c041fc43a5a1deba856de93f90a6`  
		Last Modified: Tue, 12 Aug 2025 18:32:38 GMT  
		Size: 40.9 MB (40879932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800f5b91b2848512fd7dbc286138cf1e4d591ff55f34ab14278e87e9b09ff031`  
		Last Modified: Tue, 12 Aug 2025 18:32:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf9bad3d889abede65864c12909ebd3610e98ef4cd486b75576726dac37a93b`  
		Last Modified: Tue, 12 Aug 2025 18:32:36 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u462-b08-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:18206871c6626808d043081667dbfa6571dd79b2b4ca32fbd85b5b62db71f4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5068f1bec393a6302feab852f1ab3913b76cb89fcd9b22576d273b85e85ca08`

```dockerfile
```

-	Layers:
	-	`sha256:d5afa6a5252f1969c045c9bf89f2278f4e0352dc02b0f7a374a9f8616d3e9f5c`  
		Last Modified: Tue, 12 Aug 2025 21:19:57 GMT  
		Size: 3.9 MB (3909799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b070b2563a7cb322e747440581972ff8499d7faa9d35ba918bca47eb9e006af1`  
		Last Modified: Tue, 12 Aug 2025 21:19:58 GMT  
		Size: 22.1 KB (22070 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u462-b08-jre-jammy` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:1d1a59aadd66a68767a818acb5cbc4f53de2237a8f675fbb9505fc2d2a53fa98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93329247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f507895b2c6c0c0f62c76a5ecec02b20c7eee2eb828a481d0e5c8ef0f88b0d1f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:03 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Wed, 30 Jul 2025 05:34:06 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6e83ffc37da053352ccaa2fd3bd7d813b9674d87aa01b35ac3e54903cd33b0d8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='c34506736ab52768c59660a5d4246b94f57543c79b7e4b53d322dda3ec4a9302';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='48547114cef3ce1ab8e80c8140430d8fb2f23359d52ad6d7a0af28f5fe9c81f8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='15391b2d1bf613abd739f6ad6eeb728f4803d901cceae0d83f6bbd00da7751bf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10c50520b2833414582dcec4e87265a64dd9e5acd7b3ec03378e25ec51523b3`  
		Last Modified: Tue, 12 Aug 2025 17:29:14 GMT  
		Size: 17.6 MB (17624214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae118af510ca6e101481fa3514c68bbf26d3ed4be818a2fc50d67bbe5d1f852`  
		Last Modified: Tue, 12 Aug 2025 17:31:40 GMT  
		Size: 41.3 MB (41259479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d476ee145c6f5c6581e368cadb55952e28721f9333f00ca8c6254074f285ebff`  
		Last Modified: Tue, 12 Aug 2025 17:31:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b0a984cd7e0f1fffa4696caf90bd413554ee303a253aa2f145102f35daec1d`  
		Last Modified: Tue, 12 Aug 2025 17:31:35 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u462-b08-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3c646994d3b188f3c82911eff1aa39f836eaf98b4ce068c689a1d23248fb6274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3936212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da34d45153501d4a2090e9f595a8ae52c1785355e716247cea01c2b619fcf11`

```dockerfile
```

-	Layers:
	-	`sha256:8dbbafc2bfb4d12a0b509e673158b9d89458f942d946729359768305146b84f5`  
		Last Modified: Tue, 12 Aug 2025 18:20:10 GMT  
		Size: 3.9 MB (3914216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d0f23d163c6e4910cbb18f53fd831dcbdb193c252e0f7cc6f25dba72688581`  
		Last Modified: Tue, 12 Aug 2025 18:20:10 GMT  
		Size: 22.0 KB (21996 bytes)  
		MIME: application/vnd.in-toto+json
