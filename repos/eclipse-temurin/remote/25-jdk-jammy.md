## `eclipse-temurin:25-jdk-jammy`

```console
$ docker pull eclipse-temurin@sha256:1b714ef53e0cb72b510554231839ddbfd9568ffa7be55a6a6bc56c41207b5e37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `eclipse-temurin:25-jdk-jammy` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:d55a4c4655486ccc416ea96101c7b9440deb60f6f68899fb40586ed19dca4997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137623564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d31c5dbae207329612c593961b61ae31eaabe57aeed1d6f932efaefa75228c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 26 Sep 2025 12:51:13 GMT
ARG RELEASE
# Fri, 26 Sep 2025 12:51:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 26 Sep 2025 12:51:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 26 Sep 2025 12:51:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 26 Sep 2025 12:51:13 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Fri, 26 Sep 2025 12:51:13 GMT
CMD ["/bin/bash"]
# Fri, 26 Sep 2025 12:51:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 12:51:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 12:51:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
ENV JAVA_VERSION=jdk-25+36
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ee04de95ab9da7287d40bd2173076ecc2a6dd662f007bedfc6eb0380c0ef90e8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_linux_hotspot_25_36.tar.gz';          ;;        arm64)          ESUM='95716d04bdfc8b10c94f4448ea8d57a3ba872d98b53c752e4c6b48f1c95bc582';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64el)          ESUM='b060bb12b3a192a0599f03ebb9495492f78c48cb61e291e336a8b00e7798ffb0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='3e476e40f920ccfb1915d200bc7a1fba9d68c4adcc0358c5968d15613690b915';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_s390x_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 26 Sep 2025 12:51:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a2b16f7e397b5c7f75054a2a1c95539891b9e775116a7aef12da306ef25130`  
		Last Modified: Thu, 02 Oct 2025 05:02:58 GMT  
		Size: 16.0 MB (15950368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db118886b4a1bd874f68ca94d7cadefc807c941d50c96930aae67ac53201cbb3`  
		Last Modified: Thu, 02 Oct 2025 05:03:07 GMT  
		Size: 92.1 MB (92134064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0474e363db68b6324a1fcffcfbfac1b9084bb1c4e2bfb0df7557e9c92fc7bc5a`  
		Last Modified: Thu, 02 Oct 2025 05:02:09 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:68bfdfbff8abe25fd336f985642f9774498f51a07bcd8e29c18159da9bac17ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3856669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ad63d206e6202bff3e38c4af0eccc73c9caaababd941039b9cd157a43aefd0`

```dockerfile
```

-	Layers:
	-	`sha256:bb4fa73d905db0479d5d6fd49bde76250783a6bb4adaf28ed5705a9ff8b38f0c`  
		Last Modified: Thu, 02 Oct 2025 06:16:37 GMT  
		Size: 3.8 MB (3833069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39a6e42af1f9781b0fcf3f2b1ab8f9a23f9de8350f81e72febb350ec0b524fa1`  
		Last Modified: Thu, 02 Oct 2025 06:16:38 GMT  
		Size: 23.6 KB (23600 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jdk-jammy` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:f1500eac1d2f3b50856e17d3241791977de154ab974742b9156be999c835e59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135900562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0779a0ef5cd646171dd3dded7bd33172a888233ebc25b608d0ed3d0fb611b554`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 26 Sep 2025 12:51:13 GMT
ARG RELEASE
# Fri, 26 Sep 2025 12:51:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 26 Sep 2025 12:51:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 26 Sep 2025 12:51:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 26 Sep 2025 12:51:13 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Fri, 26 Sep 2025 12:51:13 GMT
CMD ["/bin/bash"]
# Fri, 26 Sep 2025 12:51:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 12:51:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 12:51:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
ENV JAVA_VERSION=jdk-25+36
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ee04de95ab9da7287d40bd2173076ecc2a6dd662f007bedfc6eb0380c0ef90e8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_linux_hotspot_25_36.tar.gz';          ;;        arm64)          ESUM='95716d04bdfc8b10c94f4448ea8d57a3ba872d98b53c752e4c6b48f1c95bc582';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64el)          ESUM='b060bb12b3a192a0599f03ebb9495492f78c48cb61e291e336a8b00e7798ffb0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='3e476e40f920ccfb1915d200bc7a1fba9d68c4adcc0358c5968d15613690b915';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_s390x_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 26 Sep 2025 12:51:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c0663900f9726dc358bd8f6c719908a1f0b3b7a5a187507b1459c71e2e29e8`  
		Last Modified: Thu, 02 Oct 2025 02:31:58 GMT  
		Size: 17.4 MB (17370140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b80e7bb8af53020db7b76d9ba97df8b8b311a4b25bdaae558810f1e96e2d12`  
		Last Modified: Thu, 02 Oct 2025 02:32:01 GMT  
		Size: 91.1 MB (91145002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2511b6f35bd02e6eecba4fea486ffba340ef081190f98ba03f04b1834ae24ff`  
		Last Modified: Thu, 02 Oct 2025 02:03:53 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:97c6803d4e07e8ff7d80a5dfb28899b5a7d0f41a8ba84367016ac7f3cf0c1f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d490ccab6d8877730cd183a9def10e3ca780f42cd143ab0b72e40086e3ff590c`

```dockerfile
```

-	Layers:
	-	`sha256:982599509ef4e83c82cdb9d47dc354f738b47f03d4d42b5a0e6b643e82a2db2f`  
		Last Modified: Thu, 02 Oct 2025 03:18:30 GMT  
		Size: 3.9 MB (3928521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa820a353f240c4d5ebea7ad5c6000cf48ae31f10ab815a4ce615307e275c031`  
		Last Modified: Thu, 02 Oct 2025 03:18:31 GMT  
		Size: 23.7 KB (23722 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jdk-jammy` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:e0d094dcb63d56f6abbd3968e88b98942ac1d2311b570053bf0f5d12a48b9ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143007772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa4bf9353fa21850ea6121203eed8580c772c7d8fb918f38102115e09fa2ed6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 26 Sep 2025 12:51:13 GMT
ARG RELEASE
# Fri, 26 Sep 2025 12:51:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 26 Sep 2025 12:51:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 26 Sep 2025 12:51:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 26 Sep 2025 12:51:13 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Fri, 26 Sep 2025 12:51:13 GMT
CMD ["/bin/bash"]
# Fri, 26 Sep 2025 12:51:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 12:51:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 12:51:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
ENV JAVA_VERSION=jdk-25+36
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ee04de95ab9da7287d40bd2173076ecc2a6dd662f007bedfc6eb0380c0ef90e8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_linux_hotspot_25_36.tar.gz';          ;;        arm64)          ESUM='95716d04bdfc8b10c94f4448ea8d57a3ba872d98b53c752e4c6b48f1c95bc582';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64el)          ESUM='b060bb12b3a192a0599f03ebb9495492f78c48cb61e291e336a8b00e7798ffb0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='3e476e40f920ccfb1915d200bc7a1fba9d68c4adcc0358c5968d15613690b915';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_s390x_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 26 Sep 2025 12:51:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad304d507756ae3ca850893e6045650f484a7f72bbaff0614e9fe4d444fb0a9`  
		Last Modified: Thu, 02 Oct 2025 03:27:07 GMT  
		Size: 16.9 MB (16856564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a8113f008443d898e8325286b1aa775fadba809064b51ea8eee593ae1cc647`  
		Last Modified: Thu, 02 Oct 2025 03:27:29 GMT  
		Size: 91.7 MB (91702104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6758956779067ed1345f317df2f61f5d7d253e86a8c01ac4c5f7da74c95ee961`  
		Last Modified: Thu, 02 Oct 2025 02:28:07 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:57c405efce747ebe60776e64910f130fa3616953b2810bfaca9c0d0dc9e6b942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3885432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b25e8340f3209353c2c383ca4af929ecf6929a604a2875d5dc0a4e5152ee0bc`

```dockerfile
```

-	Layers:
	-	`sha256:2191f1b26b60933a827e193d688f4a22ebec9155c111f3d6b82965838edbbb37`  
		Last Modified: Thu, 02 Oct 2025 03:18:34 GMT  
		Size: 3.9 MB (3861790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4018ccc3fe1cf0b3f4d9eaf2048bd5f0ed22f84642e712d9cefbd06efcbbe96f`  
		Last Modified: Thu, 02 Oct 2025 03:18:35 GMT  
		Size: 23.6 KB (23642 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jdk-jammy` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:0646cb3a1372aa9a84e9742d4171aedb12273317fa6026abb03271a8c667d739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132075976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30cf3c703cd3ebdfd8cf95dabfb685f2ec88dcc753938f91b5862f68448f5a71`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 26 Sep 2025 12:51:13 GMT
ARG RELEASE
# Fri, 26 Sep 2025 12:51:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 26 Sep 2025 12:51:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 26 Sep 2025 12:51:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 26 Sep 2025 12:51:13 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Fri, 26 Sep 2025 12:51:13 GMT
CMD ["/bin/bash"]
# Fri, 26 Sep 2025 12:51:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 12:51:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 12:51:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
ENV JAVA_VERSION=jdk-25+36
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ee04de95ab9da7287d40bd2173076ecc2a6dd662f007bedfc6eb0380c0ef90e8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_linux_hotspot_25_36.tar.gz';          ;;        arm64)          ESUM='95716d04bdfc8b10c94f4448ea8d57a3ba872d98b53c752e4c6b48f1c95bc582';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64el)          ESUM='b060bb12b3a192a0599f03ebb9495492f78c48cb61e291e336a8b00e7798ffb0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='3e476e40f920ccfb1915d200bc7a1fba9d68c4adcc0358c5968d15613690b915';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_s390x_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 26 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 26 Sep 2025 12:51:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea694d9fcf3484adcec8b2eb67828b5a7d47c5701b5ec5e2bc7c5da5c257e1f`  
		Last Modified: Thu, 02 Oct 2025 03:33:10 GMT  
		Size: 15.8 MB (15766761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ead7ca71f3c959fea29685ce68ef661f7d84b54e898a36471d2ea76088d0a9`  
		Last Modified: Thu, 02 Oct 2025 03:33:52 GMT  
		Size: 88.3 MB (88303488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f5e6270083c967bc90bd16bff31afd6a2ead33e9a4a687c6011b613c075e7e`  
		Last Modified: Thu, 02 Oct 2025 02:10:58 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2e851ba4e5eea1c403f70c654c378c233cd7a8de21eb369e2d12e2209bda4baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996810e58bdf7830f0864224f71ff52e4c3f55d3f2e554c70ca246505d7c3cc2`

```dockerfile
```

-	Layers:
	-	`sha256:0714995f220cb2cf2683c4de8910b99abeb0472b49725ea374b92a9536386618`  
		Last Modified: Thu, 02 Oct 2025 03:18:39 GMT  
		Size: 3.8 MB (3760628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ee4039c16079e5c029a648035295ea376009cf840381f02ac1b6c4535faf593`  
		Last Modified: Thu, 02 Oct 2025 03:18:40 GMT  
		Size: 23.6 KB (23599 bytes)  
		MIME: application/vnd.in-toto+json
