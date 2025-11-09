## `eclipse-temurin:11-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:599c515adfafdcc7b534da66e133c3bee8632650e56cd244b29c0fda8a93891a
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

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:5a3decec7016f50780ce1bdc5321db2c02608ae9ef6dcd458537df3aa45b48bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.7 MB (197684466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21562832b75be4650f42720a60cc061567f9f384a68c509268d8caa400222ce5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 15 Oct 2025 08:06:33 GMT
ENV container oci
# Wed, 15 Oct 2025 08:06:34 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 15 Oct 2025 08:06:34 GMT
CMD ["/bin/bash"]
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Wed, 15 Oct 2025 08:06:35 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Sat, 08 Nov 2025 17:55:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:55:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:55:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:55:38 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sat, 08 Nov 2025 17:55:38 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Sat, 08 Nov 2025 17:57:35 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 08 Nov 2025 17:57:36 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:57:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:57:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:57:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f96aa371e711e1bbcefaf896794cb5d68db0779104ba57a87f20aaf6f287c25`  
		Last Modified: Sat, 08 Nov 2025 17:56:02 GMT  
		Size: 16.6 MB (16603290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cf26689e8d6edc84364b847ae64662ca5b7435f8da4f3ef3fc2ee93311139b`  
		Last Modified: Sat, 08 Nov 2025 18:23:47 GMT  
		Size: 141.4 MB (141425235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532851247436f88bc4953fde5879a133b9d8f56ba32ce5efde0640a7946a4468`  
		Last Modified: Sat, 08 Nov 2025 17:57:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be560c3fa6a7dffff4d77f7278522d3ec9c687ff0857318929db0a287e3453b`  
		Last Modified: Sat, 08 Nov 2025 17:57:58 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:fe6690fcd1fc6d890d0fff9a37571ac3c5d53677c48eb6bc0305116de8750d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1776180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c877ebe94691eee5ec5c4644e1707d8838e04686285329bfd32bb9be53c0f7`

```dockerfile
```

-	Layers:
	-	`sha256:f19bb656ce166669cffa076dec3183865fd88e3fabc064daa58de1501a0cafaa`  
		Last Modified: Sat, 08 Nov 2025 19:20:59 GMT  
		Size: 1.8 MB (1755036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3fec1b14532cbdf42e2a8306ca15a2231da11f351bd455e81911d90402c7ec0`  
		Last Modified: Sat, 08 Nov 2025 19:21:00 GMT  
		Size: 21.1 KB (21144 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:77a9846410323420037f3a572959f4872d1242ad9940ebee391229b8b85bb6aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192691731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9f4e0324dd9b8d3ec368c1379fd22f8bd18089b1b635ec1b07a6f72c8b9dc3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.openshift.expose-services=""
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 15 Oct 2025 08:10:52 GMT
ENV container oci
# Wed, 15 Oct 2025 08:10:53 GMT
COPY dir:a993e2e2ad3cf26c4ca4b583710869f381ee3e7df7d41715015a96348230e455 in /      
# Wed, 15 Oct 2025 08:10:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 15 Oct 2025 08:10:53 GMT
CMD ["/bin/bash"]
# Wed, 15 Oct 2025 08:10:54 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 15 Oct 2025 08:10:54 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 15 Oct 2025 08:10:54 GMT
COPY file:85de04d2096a64069474160b53ad5f2cfb18b7e3f3ec2a8d26b3946f32e004c9 in /root/buildinfo/labels.json      
# Wed, 15 Oct 2025 08:10:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:10:36Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Sat, 08 Nov 2025 17:57:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:57:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:57:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:57:19 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sat, 08 Nov 2025 17:57:19 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Sat, 08 Nov 2025 17:57:26 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 08 Nov 2025 17:57:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:57:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:57:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:57:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2602e1c5e8830fe80a6207359ce01e6c9b7d6848be663c4df1e03c724149b8a6`  
		Last Modified: Wed, 15 Oct 2025 09:30:32 GMT  
		Size: 37.9 MB (37896281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda954ef433fd7958faabe39251e137af45b80af3fc8822fbec79fce5e0f6a18`  
		Last Modified: Sat, 08 Nov 2025 17:57:56 GMT  
		Size: 16.6 MB (16602806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4fdd09f4a86c19ba720dadb0894629682096080521fe523cd1df9fa799f038`  
		Last Modified: Sat, 08 Nov 2025 18:24:10 GMT  
		Size: 138.2 MB (138190226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a368dc1472113df56e384e6275a4b1b4026ecb7ac37f57274bcdaca221586c5`  
		Last Modified: Sat, 08 Nov 2025 17:57:56 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82914dfe0d1ca85f870822f2c1c279a3558880da6ca62fe2792df103bb20ed8`  
		Last Modified: Sat, 08 Nov 2025 17:57:41 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:57400986a9f7c8da8d50f01df005888e599c5e67b333e3afead9b535f9e370f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1777516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d426c5cce4acbd402cafd5c8b9ada4e188157a0a15a309e8348946fb0515a2a3`

```dockerfile
```

-	Layers:
	-	`sha256:4c4505926011647c248d0595e971283eb775622cdca2edb775122fdcc6dd7c7a`  
		Last Modified: Sat, 08 Nov 2025 19:21:04 GMT  
		Size: 1.8 MB (1756256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afb165c9c617d360c97111e85ff0fcf482b1c3330a9e9a403d30b68257714543`  
		Last Modified: Sat, 08 Nov 2025 19:21:08 GMT  
		Size: 21.3 KB (21260 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:44efcefe3353b6f16a610147979057b2f1c78556a117196fe11d417edb876bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192546364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82b1f848653aaa4e003143a097d9934d037df92924908e4139fc50b40b01ee7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Oct 2025 08:07:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 15 Oct 2025 08:07:55 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 15 Oct 2025 08:07:55 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 15 Oct 2025 08:07:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 15 Oct 2025 08:07:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 15 Oct 2025 08:07:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 15 Oct 2025 08:07:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:07:55 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:07:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 15 Oct 2025 08:07:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 15 Oct 2025 08:07:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 15 Oct 2025 08:07:55 GMT
ENV container oci
# Wed, 15 Oct 2025 08:07:55 GMT
COPY dir:449eb2f239bac2d8d364a723cb091b20b453ccb6c9e9ef4542e774b1e6a3f931 in /      
# Wed, 15 Oct 2025 08:07:56 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 15 Oct 2025 08:07:56 GMT
CMD ["/bin/bash"]
# Wed, 15 Oct 2025 08:07:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 15 Oct 2025 08:07:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 15 Oct 2025 08:07:56 GMT
COPY file:a1ec773a4fe5bc79df5be7b721d463b5573cea3333f3a512f669f32fa8283a6b in /root/buildinfo/labels.json      
# Wed, 15 Oct 2025 08:07:56 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:07:44Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Sat, 08 Nov 2025 17:57:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:57:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:57:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:57:21 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sat, 08 Nov 2025 17:57:21 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Sat, 08 Nov 2025 18:04:53 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 08 Nov 2025 18:04:56 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:04:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:04:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:04:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7d2fc558322651c1228b069dff5be5599bf4a7e595e3227e6de491f7067f1a45`  
		Last Modified: Wed, 15 Oct 2025 08:44:15 GMT  
		Size: 44.1 MB (44050495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd418b58a61783498a7a914a92baa56a29c3bdb5efae22fc9de5972b10f54d1d`  
		Last Modified: Sat, 08 Nov 2025 17:58:10 GMT  
		Size: 19.9 MB (19909128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeeadc7d29cc351f3ca443503f50266dcb6bf0f5297629539ca99d63515ea462`  
		Last Modified: Sat, 08 Nov 2025 23:01:10 GMT  
		Size: 128.6 MB (128584321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8dcd273052ac6b4ed2ee1e591c5a46b1d3e08ecab8d22327bfe7ebd18f3a45`  
		Last Modified: Sat, 08 Nov 2025 18:05:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b3472613e010f1b004f9400e3cb966b437f0c1b53db832008bba83e699ccec`  
		Last Modified: Sat, 08 Nov 2025 18:05:34 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b17df550a2c895085c2a28bc3b74700664658e699707718f187aab0f48152e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1776077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b421c7d17279bafeb13fead27bc8c1078c4a80c32aa2317af94a695ee0b975`

```dockerfile
```

-	Layers:
	-	`sha256:3c18a34a433adcfe12ca16d467642d1ceb40a459dbd764cb17b4e5e65a94e80f`  
		Last Modified: Sat, 08 Nov 2025 18:05:26 GMT  
		Size: 1.8 MB (1754927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0677f7629db608e68405b7b68fcd7186861d0dba3cfe2d2224a4f2b4209dc9b`  
		Last Modified: Sat, 08 Nov 2025 18:05:26 GMT  
		Size: 21.1 KB (21150 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:fb4ef0ec06822b8cdf9c5bd58a7eca070a3378680a260d077af3d2ee4516da0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176323379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8ad993ebaa6daf527cba3c674b750b9e53998b7efcbf18b8b6b8ebe3fc910a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Oct 2025 08:12:13 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 15 Oct 2025 08:12:13 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 15 Oct 2025 08:12:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 15 Oct 2025 08:12:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 15 Oct 2025 08:12:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 15 Oct 2025 08:12:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 15 Oct 2025 08:12:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:12:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:12:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 15 Oct 2025 08:12:14 GMT
LABEL io.openshift.expose-services=""
# Wed, 15 Oct 2025 08:12:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 15 Oct 2025 08:12:14 GMT
ENV container oci
# Wed, 15 Oct 2025 08:12:14 GMT
COPY dir:c7531cf9ca81563f111865af7c21a35f1b40cdbceb45f292beb90b52a7f09fd7 in /      
# Wed, 15 Oct 2025 08:12:14 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 15 Oct 2025 08:12:14 GMT
CMD ["/bin/bash"]
# Wed, 15 Oct 2025 08:12:14 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 15 Oct 2025 08:12:14 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 15 Oct 2025 08:12:14 GMT
COPY file:c18f78822817f13e8af547877aa1bb6f7295fa27828e91bdb8605916bb9a08c8 in /root/buildinfo/labels.json      
# Wed, 15 Oct 2025 08:12:15 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:12:03Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Sat, 08 Nov 2025 17:55:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:55:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:55:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:55:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sat, 08 Nov 2025 17:55:57 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Sat, 08 Nov 2025 17:56:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 08 Nov 2025 17:56:07 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:56:07 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:56:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:56:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a42ec211faae823c9be27da6cd639f320fbf91a4d4f8d9a8428b8b1f4f661ad4`  
		Last Modified: Wed, 15 Oct 2025 12:11:19 GMT  
		Size: 37.8 MB (37759797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7057baef8e1e56074fbebcae2ebe9fc755e75d3f376cc35d8243e5172094c140`  
		Last Modified: Sat, 08 Nov 2025 17:56:51 GMT  
		Size: 16.5 MB (16457363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b456b705caf6db0459bf03e07f88554fd64967571fe55d729d3e5981ec248ed4`  
		Last Modified: Sat, 08 Nov 2025 17:56:51 GMT  
		Size: 122.1 MB (122103802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cade3f281894b7f6e3e8b6d322d5dc11377334bad713e2cb609fce2216954c`  
		Last Modified: Sat, 08 Nov 2025 17:56:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bba8cadd673383ab2583093e3390f4d31e7b59824aba11030275cabccadd6a`  
		Last Modified: Sat, 08 Nov 2025 17:56:45 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2d04d12af0bb10c516c6fb6dce98a4c2a0e6b33b310c00f37b35a09ac3ff734d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1775418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394af7365742895cc414f7d2a32ba05e7f17d1a1d454f9204c35e20fd14b9fa2`

```dockerfile
```

-	Layers:
	-	`sha256:5bdf8a00f489cd84723b219a177bb6e090c8ed49408718c0d487552e9bab1e39`  
		Last Modified: Sat, 08 Nov 2025 17:56:33 GMT  
		Size: 1.8 MB (1754304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ce98a7e8e10fccb0cc3bb5131dd8d53068ebc20eb62186e57ec7f6f5e2bf04a`  
		Last Modified: Sat, 08 Nov 2025 17:56:33 GMT  
		Size: 21.1 KB (21114 bytes)  
		MIME: application/vnd.in-toto+json
