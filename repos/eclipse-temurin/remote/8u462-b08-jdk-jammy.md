## `eclipse-temurin:8u462-b08-jdk-jammy`

```console
$ docker pull eclipse-temurin@sha256:2d5abe1cae0197b723fad1f347b3d12ca91d3f03ab6de046b8af873ee70cc340
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

### `eclipse-temurin:8u462-b08-jdk-jammy` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:1377cc2213af880fae9898779f5459400d13dda58030857870c5753e5109f73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.4 MB (100429838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094d606762ad037434f16a379a8ac368068d066b99ab91d45ce6d0857b817aa4`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
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
	-	`sha256:08483b5f2cfe43842a06f46c6081326e0c2dc3b3243317fd12e60f348d678964`  
		Last Modified: Tue, 12 Aug 2025 17:24:18 GMT  
		Size: 16.2 MB (16150643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3dcc561c9cd39b92ec4fc57a6058ff42002ecf195e80d8ad5748e80389c1ec`  
		Last Modified: Tue, 12 Aug 2025 17:24:18 GMT  
		Size: 54.7 MB (54739766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582c1bed63e3dd80b9aabcadc64e63ef4bcde37bb178fa1bc799c832e74f204a`  
		Last Modified: Tue, 12 Aug 2025 17:24:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6337a833f3117c3db42fc6b211b32a6b6874d435444ee9455d2e28d83e3326d1`  
		Last Modified: Tue, 12 Aug 2025 17:24:11 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u462-b08-jdk-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c5bd41e91fd70a1c19936dbceb9a2967d28eee2ddff2e0fa0c187b84dfe2e404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4107895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96e299ee496c7cc6772ab012694b11d86b1386ce839138d03e4622ffd922bec`

```dockerfile
```

-	Layers:
	-	`sha256:7e8564f5ad183ede5b71ab01ca227c6def0d04a6748e8ea9d1b01f991551112c`  
		Last Modified: Tue, 12 Aug 2025 18:19:20 GMT  
		Size: 4.1 MB (4085421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1f25f2c6a6af64a0839b2a65b8a891f55343fd45ee723545667303e0a8c600f`  
		Last Modified: Tue, 12 Aug 2025 18:19:21 GMT  
		Size: 22.5 KB (22474 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u462-b08-jdk-jammy` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:f4b236bd890c7d4e6da792b4cb200880f8d3d119b4d19c964e388afee7bc7fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92665888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4e6896a764252394e2aa7e2951960ee68f8076686b4f19ed12c99fe17326de`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
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
	-	`sha256:03a6be2aebf0453513058e04e2e021e6b799d01485c519c5b5ad36e363988739`  
		Last Modified: Tue, 12 Aug 2025 17:25:59 GMT  
		Size: 50.1 MB (50130721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c528ef2f62fbc4bff3549a5f540325a914be06447a617e6af79eb229989572a4`  
		Last Modified: Tue, 12 Aug 2025 17:25:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27262e97c185fe0eb8dd7b3e8c4a4e35e95d78b77a1bd3ea7f90a760cb33def0`  
		Last Modified: Tue, 12 Aug 2025 17:25:52 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u462-b08-jdk-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b2892e1cde1aab9ef0cd8728b1a40e1adcd6eb1caaf2582748545385bf0bd83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4111982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed0c7b1e6a24b62a5027336771115929de3a41befc06369e296d8999cc3bd51`

```dockerfile
```

-	Layers:
	-	`sha256:9ac39d7cdfcd7822629a557ded12832bb4dabb40121fea83a9930a89c89fce04`  
		Last Modified: Tue, 12 Aug 2025 18:19:27 GMT  
		Size: 4.1 MB (4089414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46e88847cd790594265b4ad2c5f5da9c7943172c6723efbcd7801361e5985da2`  
		Last Modified: Tue, 12 Aug 2025 18:19:28 GMT  
		Size: 22.6 KB (22568 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u462-b08-jdk-jammy` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:07448a3b2eb3b9fe05e447aff53764d0fa333ad73258405feedb0be75887ecea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97264929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80b5998e2a1465eeeea23e50573146e7967d8edfa29fa3112a1ce8a49dac69f`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
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
	-	`sha256:e940b12283a67ff1c771864e58b58f224257969d16e19a179b3f8289c4d4dfcb`  
		Last Modified: Tue, 12 Aug 2025 18:31:10 GMT  
		Size: 53.8 MB (53839507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d30fdff5a53ba3d2e43df30b5277041df566c24f5be4476b4e386dad68d69e`  
		Last Modified: Tue, 12 Aug 2025 18:31:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0ff686944578d38ac0413872ba73e79256657b51fdd048ef40b36aa1225695`  
		Last Modified: Tue, 12 Aug 2025 18:31:02 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u462-b08-jdk-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:64bb5d3e27f1cb6fdf61a5699230b7c768b304e09dcccef0d258d7a79a3222c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4108383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdbc5af20b39623a6fee2f82b6acee9dd073725e9548455f6be61b3da2fdce55`

```dockerfile
```

-	Layers:
	-	`sha256:c34b7e1e1e3589c552a5f29bac12add76f957f265dc2c7be1db1b895b478340c`  
		Last Modified: Tue, 12 Aug 2025 21:19:22 GMT  
		Size: 4.1 MB (4085787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcea860af19fe163f3722d1483e1fc7dd8144588f57fa430b48ecfb5d17ccb98`  
		Last Modified: Tue, 12 Aug 2025 21:19:23 GMT  
		Size: 22.6 KB (22596 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u462-b08-jdk-jammy` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:8b26b4ddd92065d7f5cbc7c7ba7c86e2f0f60dcd6dcf538870fcfbc1f67795c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104236942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e064f11afe0b24765c2e41d33809c342f2052553af9839fb00997a714745ca`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        arm64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        armhf)          ESUM='c4f29a65ca6c4c211e3af645e3fcbd9e8f0c2b8ab2b738973237f08e4dc38310';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u462b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
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
	-	`sha256:3563e462f65953d910e2846e6de3725502677044b4826058e62802811ea8a0ad`  
		Last Modified: Tue, 12 Aug 2025 17:29:23 GMT  
		Size: 52.2 MB (52167149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b266375691d61b72291e1f0d9e5169842674c1de091aecfdb3193e356c28d2ad`  
		Last Modified: Tue, 12 Aug 2025 17:29:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00321eef6c5bf0386430936d8260d05c426c784f7873c0c85189e55e3fa08055`  
		Last Modified: Tue, 12 Aug 2025 17:29:13 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u462-b08-jdk-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4de58d154b1c271e4c63b1a0b852a59d19fb51552401e10d9c9680ecd49b77c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4110690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff6f4eba0623c2e4a15cd15c4aca412c965a9bc207b3a604c9c193c49772e49`

```dockerfile
```

-	Layers:
	-	`sha256:7bdac2f41c6774ea93dd65d4751bef3971a03e0481a3d6cbfc76608c4da4cfaf`  
		Last Modified: Tue, 12 Aug 2025 18:19:38 GMT  
		Size: 4.1 MB (4088174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09be2565e1707aedbe7ba35b86f30a139d3265d4b06e58379af99863bcfc145`  
		Last Modified: Tue, 12 Aug 2025 18:19:39 GMT  
		Size: 22.5 KB (22516 bytes)  
		MIME: application/vnd.in-toto+json
