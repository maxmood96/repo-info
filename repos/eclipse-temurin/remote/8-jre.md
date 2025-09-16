## `eclipse-temurin:8-jre`

```console
$ docker pull eclipse-temurin@sha256:17b3327b36c16c34157c2171b568cac093d0da7b798356fe79406abb8da6f2b8
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
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `eclipse-temurin:8-jre` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:bf7414ef046816185a4596828c143b96c17e11adb873e71dcdb8efc54c33854d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88575846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebdc7a4553f7b1bf576199f953a63be7c33f03195ea9a1e91ec8ffb3adb75eca`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
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
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202b6d722eed4ab5d2bfa3ba17d989bd8d7dc4a291c1209e2eb7ef260604281f`  
		Last Modified: Mon, 15 Sep 2025 22:12:58 GMT  
		Size: 17.0 MB (16971594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d178208e0a66813e04b64140b58feaa80374f7eb14cd99c1d071bdefc6fe782c`  
		Last Modified: Mon, 15 Sep 2025 22:13:01 GMT  
		Size: 41.9 MB (41878392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4666affe668460e4a397b5422be9f6bcb8d26280ce8436c066c26b8c2974d25`  
		Last Modified: Mon, 15 Sep 2025 22:12:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afdc05c4356999ee157d23190905a4036a9c537863ec25ac74c0e20874bdc45`  
		Last Modified: Mon, 15 Sep 2025 22:12:57 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:810d628f2b53d921bae4034754bc6a298e5e615b67fc11558954f5129f4cc08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3338054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bfed043b51d758826e1208c866c72afab1a08d79cbcf3f6f518638d5ea8d2d`

```dockerfile
```

-	Layers:
	-	`sha256:04d2aa7611a060d306ffeb0132009946d9f63baba020f31c5d58aa6b0e45ccd8`  
		Last Modified: Tue, 16 Sep 2025 00:18:31 GMT  
		Size: 3.3 MB (3315452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fed1a8a0058e8ecffdaae570145a8651bc8366555e376f5e82ad1937fd8f1f3`  
		Last Modified: Tue, 16 Sep 2025 00:18:32 GMT  
		Size: 22.6 KB (22602 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:4a194c30d75f68be4aadaf51a2ede5920b429a08781518b21345e05b2bd4ad6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82517132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e386e97fd8e16e3e8af69ea5da42153dd6cab18f31fce66dc48748516da93b1b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:724937f3170b06318ea1d68d111a29f384243a4dcad8729e0deab590d6d690bc in / 
# Fri, 01 Aug 2025 11:04:34 GMT
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
	-	`sha256:d7ffb5187e159334b70dbe49cbca848457358d2d2b56fe7072a42dbd9ac9c7cf`  
		Last Modified: Wed, 10 Sep 2025 09:09:41 GMT  
		Size: 26.9 MB (26852474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e228aacc3e860f1a726bfd40dfe42b12f0f30d9e3d58ab77cb95aa3dc88f961`  
		Last Modified: Mon, 15 Sep 2025 22:10:11 GMT  
		Size: 16.3 MB (16305824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768adc7e2953600c0df677951a553ac6773cd5331fcc359ba73cbe6af2e32ff5`  
		Last Modified: Mon, 15 Sep 2025 22:10:13 GMT  
		Size: 39.4 MB (39356426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e1c1ff32a90c81a5b545b106e72ae1f9c3f9dd04673c9a17d16bf40538cc36`  
		Last Modified: Mon, 15 Sep 2025 22:10:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a90985d40b3de75a53da74505ad045890865b142ed005cc72f2e4c28b6b008`  
		Last Modified: Mon, 15 Sep 2025 22:10:09 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4e726874aca622eff3822aa07a4074ca5b4a402b851637e7c539910cf7b6d8d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3344160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3166a07f4b5744662f61551e8a0a020e784df9c7907019e7e02223f8ceb4dcda`

```dockerfile
```

-	Layers:
	-	`sha256:20d7a6bcfe113566253a57587b0f5dbbd6bbdc2b01c4e5be0090b367df7ede90`  
		Last Modified: Tue, 16 Sep 2025 00:18:36 GMT  
		Size: 3.3 MB (3321450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:065631767bb1cd1d0fd073eba5074054c5bd33f39ae7d279a41052eab501bd6d`  
		Last Modified: Tue, 16 Sep 2025 00:18:37 GMT  
		Size: 22.7 KB (22710 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:716eee566972147b229feea06cb04f94fb0fb875137ac9061f0a12688366a58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86732719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286d181148b2bc02e52154a47320dc4bdb00cd8e8bbaf35c414f828349d52bbd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Fri, 01 Aug 2025 11:04:34 GMT
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
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350b81f0c352b8bffcf9fb8f0570587745e4412e762d989da797761e99917896`  
		Last Modified: Mon, 15 Sep 2025 22:12:39 GMT  
		Size: 17.0 MB (16988934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1cf9c5bcd8806fd672d6790af50af25f3f5ff55ddd3fc2f0b8a55cc4bf8fbb`  
		Last Modified: Mon, 15 Sep 2025 22:12:44 GMT  
		Size: 40.9 MB (40880057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff44485fae70bf7b408a3c4b19bea54f180884ba55f286b3d9a244c9dd63f28d`  
		Last Modified: Mon, 15 Sep 2025 22:12:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3481f85c5244a898cdca48286c1096e9eabc958a6af3bb694b331384694fe670`  
		Last Modified: Mon, 15 Sep 2025 22:12:38 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4b425124b21a97b3bde49ed4e6324211d259d498ddff891f3884d836c871b6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3339351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbbdea418abddf4386bf50cdfcec1d9ac5e6b0966887aaf57fbba803ad175dc4`

```dockerfile
```

-	Layers:
	-	`sha256:d856f73361747bf05e48b58e4573164dbe989f3a0b39e553f70ba06b76fc445d`  
		Last Modified: Tue, 16 Sep 2025 00:18:43 GMT  
		Size: 3.3 MB (3316613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aaece8a8cd395eb721e7365468539817e524190710a4726d75031f6b72fe2ad`  
		Last Modified: Tue, 16 Sep 2025 00:18:45 GMT  
		Size: 22.7 KB (22738 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:ed803639626e0ec212bb6ef68c36938c17cb680dcbe7b2f06438d4db0ea23578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94379698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8fe0ad1119016c6b3d0d799f4806d1db62a88c09ff09b5274512cd16de565fb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Fri, 01 Aug 2025 11:04:34 GMT
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
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3102a54c6b2b7ecf7a7216123f26003eec1ece4dbee7d4985813592023f98cd3`  
		Last Modified: Mon, 15 Sep 2025 22:13:52 GMT  
		Size: 18.8 MB (18814803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff169076b0c6a2735c8234670c79cc6a8231068d48387f59577e62d58946c592`  
		Last Modified: Mon, 15 Sep 2025 22:14:49 GMT  
		Size: 41.3 MB (41259359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d59b1e7ab1f0cdfdca7b2a3d08f91514cba4b287648e1600854629aa47ed45`  
		Last Modified: Mon, 15 Sep 2025 22:14:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d6494c81657de4efdb948c6f8673f1926206bdead699b9ca3f19b826d55a5b`  
		Last Modified: Mon, 15 Sep 2025 22:14:44 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ac9622d7abde71fe819ca4327be508d5b2c15cd83c4ce164a93a3bc3cc560c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3342862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75ef1d1261b148531956d34b98eab7fbd7e35b643a914f041b883f0ef9a7287`

```dockerfile
```

-	Layers:
	-	`sha256:1434366c9af1c039636856e739295fb0a0e037f03b7cab5ceb56f43d926dd4c9`  
		Last Modified: Tue, 16 Sep 2025 00:18:49 GMT  
		Size: 3.3 MB (3320210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:861e167998aaa8a8a8f73c7cb0fef93940aa5861edf83700d0b1c3663f614019`  
		Last Modified: Tue, 16 Sep 2025 00:18:50 GMT  
		Size: 22.7 KB (22652 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre` - windows version 10.0.26100.6584; amd64

```console
$ docker pull eclipse-temurin@sha256:4f3d7017489425b27995acb9860076f520dd03f9f42f91f9174e6f487d81baf6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3644454332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224ddeff818ad78684ed68571f7d70c4b6ed2f65f300e5888948a236293ea080`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 10 Sep 2025 21:49:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:49:23 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Wed, 10 Sep 2025 21:49:46 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_windows_hotspot_8u462b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_windows_hotspot_8u462b08.msi ;     Write-Host ('Verifying sha256 (22a64b7531443577dd70eb244c943111121180dbf20a6a867452ed6da99b556d) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '22a64b7531443577dd70eb244c943111121180dbf20a6a867452ed6da99b556d') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Sep 2025 21:49:53 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39bf991b65b005f2b7f122bb8e11deadf02225b06438805e32f109fda66c1ea`  
		Last Modified: Wed, 10 Sep 2025 21:57:04 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb586cde9fe79b148e95e71b779ad680dcc362288a7fdb752668a7c966c3c71e`  
		Last Modified: Wed, 10 Sep 2025 21:57:04 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a2bbff228707fa4e67a4db24ae4b13db653c1623c922995c7709ba7ecede30`  
		Last Modified: Wed, 10 Sep 2025 21:57:10 GMT  
		Size: 72.6 MB (72649119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da555e552108fcf8055d96f5fceb0875964bef88a56af7c5115c67a45b58a2ec`  
		Last Modified: Wed, 10 Sep 2025 21:57:04 GMT  
		Size: 362.9 KB (362863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre` - windows version 10.0.20348.4171; amd64

```console
$ docker pull eclipse-temurin@sha256:ffe8c0b74aeadd4af4801160619d362574d99b71f5887cefa15b0bcba3577191
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2355137285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1698652a629997873299592b3afe4b7bccf990eca0ca0d9906dbf55254035fa`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:49:23 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Wed, 10 Sep 2025 21:50:01 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_windows_hotspot_8u462b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_windows_hotspot_8u462b08.msi ;     Write-Host ('Verifying sha256 (22a64b7531443577dd70eb244c943111121180dbf20a6a867452ed6da99b556d) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '22a64b7531443577dd70eb244c943111121180dbf20a6a867452ed6da99b556d') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Sep 2025 21:50:07 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd44c79ab8a3f7bf4a2a0bde959ca4df83def6bbbf05095196af7ba6ff12c064`  
		Last Modified: Wed, 10 Sep 2025 21:55:42 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c6494d3ced0a8c66bc0ee1d6c4090b2c826898bf59baa58dc6de82134579a5`  
		Last Modified: Wed, 10 Sep 2025 21:55:42 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b478e3f9da0ca3fb85b39568cecfb47d9b7bce968c07aea9763a28a69f2182f`  
		Last Modified: Wed, 10 Sep 2025 21:55:57 GMT  
		Size: 72.6 MB (72638380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634a9f5de94901bdbc1b8f625fb9056ab97fcbf345a7b8521d2d13eb5ab5f6d1`  
		Last Modified: Wed, 10 Sep 2025 21:55:43 GMT  
		Size: 351.3 KB (351348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
