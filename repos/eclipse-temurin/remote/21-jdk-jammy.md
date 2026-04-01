## `eclipse-temurin:21-jdk-jammy`

```console
$ docker pull eclipse-temurin@sha256:f780cc415d168cad9f6a41607092b67fc799f7d4f6237fab6e4f4ff31ee77938
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

### `eclipse-temurin:21-jdk-jammy` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:eb36705c2b44b5531fdad8706d6fc614a265f6bf281dbce5bc5b69fd28101f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208298693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2cc16588c8d1cb3fa454f2cfafc88c21f37b0738c436da2838de85f499a96e`
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
# Wed, 01 Apr 2026 20:10:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:10:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:10:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:10:35 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:10:35 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 01 Apr 2026 20:10:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:10:44 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:10:44 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:10:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 20:10:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7caeee667611e1f81da6511baf5412b2da018cc1bf65c3d6c6ce40c1773f39`  
		Last Modified: Wed, 01 Apr 2026 20:11:02 GMT  
		Size: 20.7 MB (20692331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b536db1568f72c6f7de89be5b3038d38bb3ace81fc64cba54a2fe9049d0861`  
		Last Modified: Wed, 01 Apr 2026 20:11:06 GMT  
		Size: 157.9 MB (157867507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a787fbd6a9ba3d67829b8905f3c58518e901d9858b6e6f5f401240b0c9d8cd67`  
		Last Modified: Wed, 01 Apr 2026 20:11:01 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8255f892d01834de9c08037ae7c63ab7c47e1add4e7d0e5d8e64386db3f290c8`  
		Last Modified: Wed, 01 Apr 2026 20:11:01 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:be2affe83e9ae3e1439e8a3ba7fce8da3c5e67e2603a07f6a81ecbdae49283b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4149760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4187a116fc206a33e64c94a77b5607558ad540dc45a4384c5b14014b8c7b9456`

```dockerfile
```

-	Layers:
	-	`sha256:20fc6eaa5d2b0db5a50487defb2052cffe9e4356343d443acb10e16db13db375`  
		Last Modified: Wed, 01 Apr 2026 20:11:01 GMT  
		Size: 4.1 MB (4126663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bfe0454f46682bed82e3695fe0f59dad6e815b038ecc5fe3577a48ecec0cac1`  
		Last Modified: Wed, 01 Apr 2026 20:11:01 GMT  
		Size: 23.1 KB (23097 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-jammy` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:c19c2208da41620d42853b5cea12708f6cdda746fb6ab79594facc8d1355a725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205857891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f7ce3edf84d0b48507e2b5a7c50727fc9ca06be9528db147d9de08f3fa1a760`
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
# Wed, 01 Apr 2026 20:10:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:10:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:10:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:10:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:10:39 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 01 Apr 2026 20:10:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:10:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:10:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:10:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 20:10:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98d5c5c46afbd5c1ccd4c26b2420889a8a62fb398c80917ca006161db51afe2`  
		Last Modified: Wed, 01 Apr 2026 20:11:07 GMT  
		Size: 22.1 MB (22109286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6711817c5bbbe977f79e66d48ae06a4ebe977f0613e3ff2200630913305fbbe2`  
		Last Modified: Wed, 01 Apr 2026 20:11:11 GMT  
		Size: 156.1 MB (156139220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c280f1c561a0f171a0441e5a28aabf639b077ac9d35a56dafc575607562483e4`  
		Last Modified: Wed, 01 Apr 2026 20:11:06 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1815a7767a4add17f59f3f11c9fcfa7a40f47ed95040d3a1c0205d889a356882`  
		Last Modified: Wed, 01 Apr 2026 20:11:06 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d7526e7e7481204e3d930b0327f6f34d22abd5862cda6b3c012ebb83de01e321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d8d4dac21bf20c1f5e5f8778c5d5693c97961ed6e388da97c81a0bcf89f64da`

```dockerfile
```

-	Layers:
	-	`sha256:d5e4d09e2d87c92ab9c479dc585faaff26894a094b45b687ec0a0f8b001b3869`  
		Last Modified: Wed, 01 Apr 2026 20:11:06 GMT  
		Size: 4.2 MB (4222133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b71095171842c176698d97493631c3494986b5c29822c623b834f351d1bde2d`  
		Last Modified: Wed, 01 Apr 2026 20:11:06 GMT  
		Size: 23.2 KB (23220 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-jammy` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:581677173554d318aa7805cbc716cfa32660e1ad316c8923da28335c78021f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.2 MB (215220511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6a11c0ce7c52973b02af9c7937158b4b3bb3253f52b26bdd20274349491602`
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
# Wed, 01 Apr 2026 20:24:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:24:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:24:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:24:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:24:09 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 01 Apr 2026 20:24:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:24:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:24:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:24:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 20:24:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee56463cac9b6c164d466e594277a3aebd5896511c18c0de5feeb9f0a3ca1b5d`  
		Last Modified: Wed, 01 Apr 2026 20:25:12 GMT  
		Size: 22.6 MB (22583606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e368981558adac6df6d3cebbbd195edf98c238d346ac9667acaf62898d2bd4`  
		Last Modified: Wed, 01 Apr 2026 20:25:14 GMT  
		Size: 158.0 MB (157984800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1837c5765bf5fe948e6e39fccbb767585f50e350649c764a149b7aac0a3b2548`  
		Last Modified: Wed, 01 Apr 2026 20:25:10 GMT  
		Size: 162.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1dc16ca3082667e8feb46060c33d8458bf8626cd7c031a3e17ec0fdd3be512`  
		Last Modified: Wed, 01 Apr 2026 20:25:10 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9c70a93318f7c18786023cabb6a88de850848968d7c0f7117f08a2e4c004cfab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4177353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b0429be711a4b3d97a84f19b1b5d8361118794448354e758c846d45bb680f74`

```dockerfile
```

-	Layers:
	-	`sha256:62c59061b27c9cb55d8b831a937438ef83e0c8921c825fa95f7bc6cc5e58e07b`  
		Last Modified: Wed, 01 Apr 2026 20:25:11 GMT  
		Size: 4.2 MB (4154213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9820b12ab1872218b3f7700eea15330770ccae523d49984878928458245817cf`  
		Last Modified: Wed, 01 Apr 2026 20:25:10 GMT  
		Size: 23.1 KB (23140 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-jammy` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:cb892cd7281ef3885b74d3b73aeb78f6991271e4b2f9c060595fa49e5867e820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195734977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b78c98815fe5412ecee62e5014da8ae496251caf082e14a2d2dd33b8fb5b04`
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
# Wed, 01 Apr 2026 20:11:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:11:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:11:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:11:51 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:11:51 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 01 Apr 2026 20:11:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 01 Apr 2026 20:11:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:12:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:12:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 20:12:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7db076360428795a3bedb94abf5c7d3527328da728852f1fa3e28cc99bb96eba`  
		Last Modified: Sun, 22 Mar 2026 18:44:00 GMT  
		Size: 28.2 MB (28202727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0779b8d04f311a67531b6a69256f026efbec47dc4f4ac6b0b0d3dbc132915c70`  
		Last Modified: Wed, 01 Apr 2026 20:12:27 GMT  
		Size: 20.4 MB (20416503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd1848fe476dbd2d7bba43f87287bd39b91a38d8ba42e1b38e2ab394c97712a`  
		Last Modified: Wed, 01 Apr 2026 20:12:32 GMT  
		Size: 147.1 MB (147113306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d26ea1efd2163d528df0d0df926fc7217fa512c492dfe39959bda41b4b35ab`  
		Last Modified: Wed, 01 Apr 2026 20:12:28 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ff8d854f986fb75f47cd79435610652d886c9f4e43e992daedd9addd9d0dc3`  
		Last Modified: Wed, 01 Apr 2026 20:12:28 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:61b131e1f99e3ba3d596603ac4de7533ca8921a4f3443d2db93dd4541874c5dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4074756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2211e6899b6769a2ae07fe3f9e2de85a9216062a6fbfe2464dbaf4cbfc35e578`

```dockerfile
```

-	Layers:
	-	`sha256:981f0dca8c425343475778ccf06dc014d7c4ee3e29083e6633a710ca0895d5f6`  
		Last Modified: Wed, 01 Apr 2026 20:12:28 GMT  
		Size: 4.1 MB (4051659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f89fa0963ad84bf32dbf0b73c8e56b1176299ac9885b52c49a75ad98ff95fd6d`  
		Last Modified: Wed, 01 Apr 2026 20:12:28 GMT  
		Size: 23.1 KB (23097 bytes)  
		MIME: application/vnd.in-toto+json
