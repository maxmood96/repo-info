## `eclipse-temurin:25-jdk-jammy`

```console
$ docker pull eclipse-temurin@sha256:bff436312cf8a43386299913444739cc0c406dd080ecf3169c76e46313f71b89
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
$ docker pull eclipse-temurin@sha256:021ec323a310e3a879c25de504b6f0f881eb4b1ac477d788441c954108aac678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (138047469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de372bade13119a555fca67bccea21a397346e35ec9279ab7d8300976760474b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:10:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:10:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:10:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:10:46 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:10:46 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Wed, 01 Apr 2026 20:11:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:11:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:11:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:11:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 20:11:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5bce37fafe69b4d9b3204979fae4145bd531b6c55c3492f3f6e623f012ba22`  
		Last Modified: Wed, 01 Apr 2026 20:11:26 GMT  
		Size: 16.0 MB (15952650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824ef0c68858c11da1dbf0198d16734e102a225a0c2173d2e14b8bfbcc752096`  
		Last Modified: Wed, 01 Apr 2026 20:11:28 GMT  
		Size: 92.4 MB (92356092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cfbf7287ff1f834224c55ab0d50bcdaf46f550db7b1d11b82a5dab76490103`  
		Last Modified: Wed, 01 Apr 2026 20:11:25 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c458c56f7dcd41c788fb7b1a16cedd850369729201f61af0a87c9d22b112c24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3874756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:facc8a26ef26227a32f1fb9fbbb920fd97f9bef018f129c76d948cdcfda3ec60`

```dockerfile
```

-	Layers:
	-	`sha256:5db1323a64b384c39f1162c4ef693c1a5d55e995a25535b0d2c6a8c871ff7e95`  
		Last Modified: Wed, 01 Apr 2026 20:11:25 GMT  
		Size: 3.9 MB (3851103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2558b0d5522e498363c8e683dfe26a0b79b71d080d9ee044bfbfc92969ef27b0`  
		Last Modified: Wed, 01 Apr 2026 20:11:25 GMT  
		Size: 23.7 KB (23653 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jdk-jammy` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:d9fbc12d6d9ea2956e19143d271a4ba9d777c0525d27be172ec6804955efbb41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136390583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cfed849146ca84a3d17679e139d549f177eb3e7f4cc1777956b5f3debcf93ce`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:06:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:06:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:06:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:06:02 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Wed, 01 Apr 2026 20:06:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:06:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:06:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 20:06:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b82e61a5fd81de1afb165667c1360ed88e36cd21d0288dae5ab625c5e6fc6cd`  
		Last Modified: Wed, 01 Apr 2026 20:06:44 GMT  
		Size: 17.4 MB (17388778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b6dad992cb66ee8389283cae914acb51486257a28e36b7a3a46cc2a2416ba1`  
		Last Modified: Wed, 01 Apr 2026 20:06:51 GMT  
		Size: 91.4 MB (91392547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db317382a9e406e4d6987cefa5eeef1ef1e7e4993b0ba543770c4870d7ef3aa1`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:81e59e06d50232f9f17302dc0239d8ffcab9b4ca52222398dc7d1122da0ddc81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3970329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b041924f152dfe803ddc7a56579111e1808d7cfbaa4621f309e8bd92dabcb6a1`

```dockerfile
```

-	Layers:
	-	`sha256:2f658b995ddc8bffd7e8c73cb645525f0798b915afda787954be170fba494a3c`  
		Last Modified: Wed, 01 Apr 2026 20:06:44 GMT  
		Size: 3.9 MB (3946555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1183a8b8b6f5f849b25a8ea2ef36cde1a429fd461f38544234c20279263c9004`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 23.8 KB (23774 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jdk-jammy` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:646a075c0403ebd9265ca40ed86a7852a93ff36a6c7a0892eb9610c486bed5c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143235726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9946ef2f24977f9a929e16b58da71b81c715c598f5d295133003ae9577bdc341`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:25:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:25:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:25:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:25:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:25:49 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Wed, 01 Apr 2026 20:26:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:26:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:26:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:26:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 20:26:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba0ad6b647cf0f7e53e6c58bb4fd3c0c7d618a06855f97dc325d5f3866e20c`  
		Last Modified: Wed, 01 Apr 2026 20:27:01 GMT  
		Size: 16.9 MB (16857610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71af5c494744e60ce4ead522f72a595034387e511fb97e3fbf2f72d95a9c73b`  
		Last Modified: Wed, 01 Apr 2026 20:27:04 GMT  
		Size: 91.7 MB (91726141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9873189c2e6f2903da55f7c84aa95ebd358d738b7a77047ecf6e695cdcd73f`  
		Last Modified: Wed, 01 Apr 2026 20:26:04 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ebd12ef36ed5b92c650e7baf89be047a3a3803af8f680b4eaeff720848fd0650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3885532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee2a85c2c95c0008aa96fe2d199ebb0312b1b628fc0dd4745ffb09d584df117`

```dockerfile
```

-	Layers:
	-	`sha256:f86a1c7bb201e636fce0ff5fe2e67bfc8cf7c2f2391fcfb464529d5aafe1f34c`  
		Last Modified: Wed, 01 Apr 2026 20:27:00 GMT  
		Size: 3.9 MB (3861838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:214d1b38c10c02ecfba3ff14a1c12a139add725bed097a33b5ae3f8abfbfbee0`  
		Last Modified: Wed, 01 Apr 2026 20:27:00 GMT  
		Size: 23.7 KB (23694 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jdk-jammy` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:26d1324f18c61952753c4c592675827eeca9a7807799037f4fcc3f5f622b18af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132309988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b820af64a6107f8778d5a77670e640f6d4fc5dfc19ca603d1a380df673713ca2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 22 Mar 2026 18:12:49 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:12:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:12:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:12:50 GMT
ADD file:e6d9716e3c60256d600998c1e662d7bc5ced705020e73df5a8f8327ed250efa1 in / 
# Sun, 22 Mar 2026 18:12:51 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:13:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:13:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:13:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:13:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:13:02 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Wed, 01 Apr 2026 20:13:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:13:17 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:13:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:13:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 20:13:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7db076360428795a3bedb94abf5c7d3527328da728852f1fa3e28cc99bb96eba`  
		Last Modified: Sun, 22 Mar 2026 18:44:00 GMT  
		Size: 28.2 MB (28202727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6df8f547121b025169f4adb267a732e82dcfaa3d654270e22f2a2afca99d10d`  
		Last Modified: Wed, 01 Apr 2026 20:13:44 GMT  
		Size: 15.8 MB (15768686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54622daf92485b3e9ad2411b18d860d6602e3dfe39fd306f6a35e269470a901b`  
		Last Modified: Wed, 01 Apr 2026 20:13:46 GMT  
		Size: 88.3 MB (88336260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73995509963d1cc42d804d6c4e041a5bb53c6ec5d054026429e867aece77d5f0`  
		Last Modified: Wed, 01 Apr 2026 20:13:44 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d6f8dd40478e783b12eae4ff60d080a3c2f2d348a44a05285c4bf9535e570762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf0bbba7a5fd610d623721f124e4670f42db4de27a015d2bf7df84b524dcd5c`

```dockerfile
```

-	Layers:
	-	`sha256:5338a04bf2e8f974b6660958affcd0056b980c682395abd3f5c7dfbc6c6d5c4b`  
		Last Modified: Wed, 01 Apr 2026 20:13:44 GMT  
		Size: 3.8 MB (3760676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d273fa79260890b7373303a330a6ff201ad78ef27a673d4ea7eb0b11fe4db162`  
		Last Modified: Wed, 01 Apr 2026 20:13:44 GMT  
		Size: 23.7 KB (23652 bytes)  
		MIME: application/vnd.in-toto+json
