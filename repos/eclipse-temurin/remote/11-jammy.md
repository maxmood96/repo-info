## `eclipse-temurin:11-jammy`

```console
$ docker pull eclipse-temurin@sha256:25daa23008bae5da02ae72e572e64c4153fd6fc69b261cf85a18d2d4b4b6b883
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `eclipse-temurin:11-jammy` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:c8018dc09247246274119e1f5243904b4ed093127570f55b5e1bbbd7daac9cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.7 MB (190667215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3de40bb9089bace40b6d12108c2dc88c736a4e8ae239c3131424e3e96622ba`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:03 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 13 Nov 2025 23:20:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93cfb86c52d9a02a0a00235c089ed7bdc85581fcbad2df7f4fa12bd909742d24';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9997af0184af5a3eec8b9c31e521431f71ab4219764f54025bded4ac95f540`  
		Last Modified: Thu, 13 Nov 2025 23:20:27 GMT  
		Size: 16.2 MB (16150551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f0b6ef10bde275888f1e4eabdf96bf1fb39810178fe9e45884c8d0ee37a6ed`  
		Last Modified: Fri, 14 Nov 2025 00:17:42 GMT  
		Size: 145.0 MB (144977425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dc12bfa2e7919efde5fc34c1cf3018da75e1cf252fd1bfee26a392fe8a452b`  
		Last Modified: Thu, 13 Nov 2025 23:21:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da29d3b3f4cbc4ce873ec58088f789c93e489f329e1ae73f2c915a75412c3179`  
		Last Modified: Thu, 13 Nov 2025 23:21:06 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a3db172a9a5d6fabadeacfe59902351ab87eeab227e365cffe36406ec7fe5b91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c7dd957e469b70bcf43bab7c0c3bd47b6ba20ed036dd8ed58e8e3434e7f0a5`

```dockerfile
```

-	Layers:
	-	`sha256:0e38260d7f2656618de632de9af57c0783f80c7c261c34cf07797ddd228cff8c`  
		Last Modified: Fri, 14 Nov 2025 01:12:57 GMT  
		Size: 4.0 MB (3983966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49064a967dad701ab2091ed37d610c51c8c92f1739064fb2eaec1305650d4711`  
		Last Modified: Fri, 14 Nov 2025 01:12:58 GMT  
		Size: 23.4 KB (23439 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jammy` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:2a63273c6d8cde71122a9ac0134153cc503ec5bc0ade51ac5ccb34c324ec37a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.1 MB (180091794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f0fba0e278e06ee28652598d48dcd984e0ea0700275bff2670fd0c8dc6eeda`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Oct 2025 17:24:03 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:24:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:24:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:24:03 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:24:06 GMT
ADD file:94045c8d87683c20b28046857f569ac4ad9ec1c53b4f70e51c2badd873183cea in / 
# Mon, 13 Oct 2025 17:24:06 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:09:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:09:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:09:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:09:21 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 13 Nov 2025 23:11:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93cfb86c52d9a02a0a00235c089ed7bdc85581fcbad2df7f4fa12bd909742d24';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:11:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:11:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:11:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:11:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4179ba9965faf453aec60ab64b5f5722816899d199d00def462ceb5d7057ad8b`  
		Last Modified: Wed, 15 Oct 2025 15:02:27 GMT  
		Size: 26.6 MB (26643386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac4efe53d4d6d761b5cae150a2002f56e80bdfd4ebf832bc7a30d28e95a0250`  
		Last Modified: Thu, 13 Nov 2025 23:09:55 GMT  
		Size: 15.9 MB (15889551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf86b3a61db843afa8a51f9430690adb206ed2a9149cd9e7ea94fdcd53e12408`  
		Last Modified: Fri, 14 Nov 2025 00:17:54 GMT  
		Size: 137.6 MB (137556419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570cb308fceb99812832d2698f4e34c174f72368f4be4c63cda7b7d0d086bca3`  
		Last Modified: Thu, 13 Nov 2025 23:11:36 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169acd5c6bf1dddffe4a113f20ab3a05c18fd35b6091fb874eae2d169ec08b6`  
		Last Modified: Thu, 13 Nov 2025 23:11:33 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9c4b3d1f5f50b2d792adf993934056e6a4d380b7da74f24e15981c018cdbe607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4008560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2d6d63496139a8630966b0806a349293917a254d0ae73c9ee936c508cd8929`

```dockerfile
```

-	Layers:
	-	`sha256:6402682a50bd3332f0f0539924f1850808707e052095efaa67233c9710091c74`  
		Last Modified: Fri, 14 Nov 2025 01:13:03 GMT  
		Size: 4.0 MB (3985021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bd48f0bc98594a1b69535ea027cd396aed49555cf823891b9506cf10981d23e`  
		Last Modified: Fri, 14 Nov 2025 01:13:04 GMT  
		Size: 23.5 KB (23539 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jammy` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:9f088ee949003472de60e40b2de22d2cc933ea4eee8501ed48a3c55c73be9dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185189942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc6936c7ba8105282ebb4d4cdc7631c4781a07581d29e3de72ef9347c61a1a3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:12 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 13 Nov 2025 23:20:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93cfb86c52d9a02a0a00235c089ed7bdc85581fcbad2df7f4fa12bd909742d24';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:20:20 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:20:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:20:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0a970ce4b07b68726d7c7d9cf4c1e5c250d429307c71e724a001234cd82c44`  
		Last Modified: Thu, 13 Nov 2025 23:20:46 GMT  
		Size: 16.1 MB (16066179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed77fd8d2627057e424752b07749af4fa46c9166dfa1dae49b863c328c34bdb`  
		Last Modified: Fri, 14 Nov 2025 00:19:31 GMT  
		Size: 141.7 MB (141737442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b0ad7672facc935673ae17b0ba9af4eb1ff8de6b6f1c320abc46fed0abde8f`  
		Last Modified: Thu, 13 Nov 2025 23:20:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0798f1e93315ead6c0269bdaf161c652aad5255cb384e63988571c2f70282579`  
		Last Modified: Thu, 13 Nov 2025 23:20:44 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1d45e103433bd6f46192981068e38eb341fa96aac488262b067dd6bdd3ecb1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74673b763d8b39cdfb3328e90396160522119499fb72494649b4aa3ccf465597`

```dockerfile
```

-	Layers:
	-	`sha256:8e5fcfb6a371315bc728e06d3ced5e73780f39f2a167c60342dffc23d54d9641`  
		Last Modified: Fri, 14 Nov 2025 01:13:08 GMT  
		Size: 4.0 MB (3984252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19d46d25caf050bc56f80c4b0b501a3793d5d92f76927750405262443ee4f57a`  
		Last Modified: Fri, 14 Nov 2025 01:13:09 GMT  
		Size: 23.6 KB (23563 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jammy` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:457254e2dc400895f056a4c3dfa1cbb5973f5dc8ebba10e5f0939af0c02928ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184163442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f28bb1d262933419ea1c80bc0fa0d714cfded6814f2105049ca232bbae09230`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:11:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:11:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:11:04 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 13 Nov 2025 23:16:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93cfb86c52d9a02a0a00235c089ed7bdc85581fcbad2df7f4fa12bd909742d24';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:16:15 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:16:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:16:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0c14dcc61889e99acc58ba77c205e7f8b643ae497c00428e124e7fac3003f8`  
		Last Modified: Thu, 13 Nov 2025 23:11:46 GMT  
		Size: 17.6 MB (17623855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeefdebbf23bad88eb0e6615acfa112fa35519502b561e1437a0e3adf677d03c`  
		Last Modified: Fri, 14 Nov 2025 02:08:35 GMT  
		Size: 132.1 MB (132090423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54556efa2a2c0a4f0c377b775ae9ceabec48f7556dc2e47395aeef385c896d3f`  
		Last Modified: Thu, 13 Nov 2025 23:16:56 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb4548cc6c4e322139cf81adf43916417b9b8bd43a948e7668b6cf7b2954ee6`  
		Last Modified: Thu, 13 Nov 2025 23:16:57 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4a3baa59e2441e4f821e1194fc702b2afa1e4c93d3ee98d381b8d9602f14a9e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4008994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd987e72903316605ba02c1f550b5ca1ecd093ab3a145c0ec1229f010d2bd227`

```dockerfile
```

-	Layers:
	-	`sha256:59b80e8e7b16f58b152e23dfe59a97220e4c1e0f9e357c516b5eefe1a806cea9`  
		Last Modified: Fri, 14 Nov 2025 01:13:14 GMT  
		Size: 4.0 MB (3985511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85358c46074540696378e35d829872b4372a3e1e83ef57f694c5447d97a4ce9a`  
		Last Modified: Fri, 14 Nov 2025 01:13:14 GMT  
		Size: 23.5 KB (23483 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jammy` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:d3c927041681075777a3f981aed5f1c2c9a396f81213c8dc3efe2bef7be7afc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169856273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9eac3997ccce4507ba28e437e2069001a9358182f8700822b8f680cff839ef4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:42 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:44 GMT
ADD file:3d940f8d55eafd405ad4e9fa11689b18e385411a264e560df2a7b1b1fd1c45ea in / 
# Mon, 13 Oct 2025 17:23:44 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:09:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:09:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:09:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:09:06 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Thu, 13 Nov 2025 23:09:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        arm64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        armhf)          ESUM='93cfb86c52d9a02a0a00235c089ed7bdc85581fcbad2df7f4fa12bd909742d24';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64el)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:09:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:09:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:09:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 13 Nov 2025 23:09:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d15824160d0d57e05338a0838871eb3f72224cf5de518ea6af54ba25e7e9c4da`  
		Last Modified: Thu, 13 Nov 2025 23:02:52 GMT  
		Size: 28.0 MB (28003285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de558eecb3d8a4c4982425e8af109373d73dbc0fe2bc177a81bc5ffbc6360f2`  
		Last Modified: Thu, 13 Nov 2025 23:09:45 GMT  
		Size: 16.1 MB (16149741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754d26293dcac30b2f2c0a91525679233393affc799b8c3100fbf8a6b960fa10`  
		Last Modified: Thu, 13 Nov 2025 23:09:53 GMT  
		Size: 125.7 MB (125700805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ac6dd78c8d0f5d13d32682775bdbcd031540b749ece17ae999e11b7a0efc72`  
		Last Modified: Thu, 13 Nov 2025 23:09:43 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2abce1a719666a7d85a918b2c573140a3dc1f334e6be4d8fe7d074a9002b2a8`  
		Last Modified: Thu, 13 Nov 2025 23:09:44 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:beff5d4cbb088dfc54855117a94671475c932aa8f52a33f365dd887b8d93ed8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfdf7621b33486f3a57f2f07310588955eed498362da6e8d5a2de743f1029c2e`

```dockerfile
```

-	Layers:
	-	`sha256:6c6adaa272343df50523c1b59e8432633ce781cf88f43d89bf664809cea1e4d9`  
		Last Modified: Fri, 14 Nov 2025 01:13:19 GMT  
		Size: 4.0 MB (3981162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9de5b97eafa796389e599ca2608b4a2cf4f8a0eecda525ee967679ed73b9d6a2`  
		Last Modified: Fri, 14 Nov 2025 01:13:20 GMT  
		Size: 23.4 KB (23441 bytes)  
		MIME: application/vnd.in-toto+json
