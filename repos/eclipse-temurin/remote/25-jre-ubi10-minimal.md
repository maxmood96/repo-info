## `eclipse-temurin:25-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:be6025a0185bdaff9338446a5933cd750d39bf8ba1a63cd90f4ca9e8a184c6f3
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

### `eclipse-temurin:25-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:1fd866efd273b1f4027e6bfeb807cdbeaa910282a7370d965f0c3b18cc8944b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126470784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd162191c560dffbeda9b949dc581e377640d95c054ec99aadbd7ee4369fe6a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 26 May 2026 09:52:44 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 09:52:44 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 09:52:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 09:52:44 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 26 May 2026 09:52:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 09:52:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 26 May 2026 09:52:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 09:52:44 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 09:52:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 26 May 2026 09:52:45 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 09:52:45 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 26 May 2026 09:52:45 GMT
ENV container oci
# Tue, 26 May 2026 09:52:46 GMT
COPY dir:4a65961322c03a42263a9993a9e455b03f91a19ddc042f14a91b2092bee12ade in /      
# Tue, 26 May 2026 09:52:46 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 09:52:46 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 09:52:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 09:52:47 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 09:52:47 GMT
COPY file:3ad71f7fdda6857fd6a2d3e0ee5ab780c0c840fe960653943407106cbf070684 in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 09:52:47 GMT
COPY file:3ad71f7fdda6857fd6a2d3e0ee5ab780c0c840fe960653943407106cbf070684 in /root/buildinfo/labels.json      
# Tue, 26 May 2026 09:52:47 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="28a4d5c7cdb1969ee63337adb47fcb350a380874" "org.opencontainers.image.revision"="28a4d5c7cdb1969ee63337adb47fcb350a380874" "build-date"="2026-05-26T09:52:24Z" "org.opencontainers.image.created"="2026-05-26T09:52:24Z" "release"="1779788807"org.opencontainers.image.revision=28a4d5c7cdb1969ee63337adb47fcb350a380874,org.opencontainers.image.created=2026-05-26T09:52:24Z
# Tue, 26 May 2026 23:10:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:10:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:10:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:10:54 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:10:54 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 26 May 2026 23:10:58 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 26 May 2026 23:10:58 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:10:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:10:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:368dae9e745ec994e59731b33513a5334145ab500bb4162a1597ced6ca7d2dd0`  
		Last Modified: Tue, 26 May 2026 11:30:57 GMT  
		Size: 34.6 MB (34624420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5361522dde51f05e96f29d4b5c36025756f7b898ad7ff5a9917bfcb908294a3a`  
		Last Modified: Tue, 26 May 2026 23:11:14 GMT  
		Size: 28.9 MB (28924974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b27edbacd324167a1a40e583164e91c8cbc2e055e944bb36b651c81f2bd173`  
		Last Modified: Tue, 26 May 2026 23:11:16 GMT  
		Size: 62.9 MB (62918973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b646993906fd43d05051ef90f7e18a19b8653346f8c0d0d9e896775d2eacca3`  
		Last Modified: Tue, 26 May 2026 23:11:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74218558a996ec2f93c4bce3c7ee118e63bdf857075c3bdeeea21f6592a08cb8`  
		Last Modified: Tue, 26 May 2026 23:11:12 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2587e928ee018d3956a46713a44d4f127835ef6d974bd7c8c412ea83ace7062b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2994551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3110b751beecc3f23ffd01cb2d21ac3972d5e9fa1b1dc5ad69610f9eb8527c0`

```dockerfile
```

-	Layers:
	-	`sha256:8d93882a776f690abe0eb65db515a011f4c711867f7effa009e17dc7988d6263`  
		Last Modified: Tue, 26 May 2026 23:11:13 GMT  
		Size: 3.0 MB (2974221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6dfdd7b63c966b8c573563f2304eed282de8d0b1848c9d3d095c4b606660d4b`  
		Last Modified: Tue, 26 May 2026 23:11:12 GMT  
		Size: 20.3 KB (20330 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:279a76c9a9d6cf763326ca8c2ee290f70d9d5085499ffdd3cec6090503b7ecc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122876438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b25b6c63465463bfc4e1e4be7a67c26d4f382f93404920ca0a771272fe7ead5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 26 May 2026 09:56:13 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 09:56:13 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 09:56:13 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 09:56:13 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 26 May 2026 09:56:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 09:56:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 26 May 2026 09:56:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 09:56:13 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 09:56:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 26 May 2026 09:56:13 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 09:56:13 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 26 May 2026 09:56:13 GMT
ENV container oci
# Tue, 26 May 2026 09:56:14 GMT
COPY dir:ae54dc874bd5ff821c9cac1615bdf50508b14bc07c449a11310a695d880fa906 in /      
# Tue, 26 May 2026 09:56:14 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 09:56:14 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 09:56:14 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 09:56:14 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 09:56:15 GMT
COPY file:cbda7134a1becb5efcab0aac781af893c81e3d1aab44f2af20045a4a249708c1 in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 09:56:15 GMT
COPY file:cbda7134a1becb5efcab0aac781af893c81e3d1aab44f2af20045a4a249708c1 in /root/buildinfo/labels.json      
# Tue, 26 May 2026 09:56:15 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="28a4d5c7cdb1969ee63337adb47fcb350a380874" "org.opencontainers.image.revision"="28a4d5c7cdb1969ee63337adb47fcb350a380874" "build-date"="2026-05-26T09:55:58Z" "org.opencontainers.image.created"="2026-05-26T09:55:58Z" "release"="1779788807"org.opencontainers.image.revision=28a4d5c7cdb1969ee63337adb47fcb350a380874,org.opencontainers.image.created=2026-05-26T09:55:58Z
# Tue, 26 May 2026 23:10:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:10:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:10:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:10:26 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:10:26 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 26 May 2026 23:10:30 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 26 May 2026 23:10:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:10:30 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:10:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d44582f6016d5b17ffe3577358bcbf1bf84edfe2aba6b73b6461e6631e0a4bc7`  
		Last Modified: Tue, 26 May 2026 11:41:50 GMT  
		Size: 32.7 MB (32711602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ce5a132dc5595c1c8ec1ed9a7cd767b697ad5d4d883ac8dd64e0342aba8243`  
		Last Modified: Tue, 26 May 2026 23:10:46 GMT  
		Size: 28.3 MB (28340579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807b8ebb078372602c0c0497ce33cf2ee7257efa8827cc3e64fb66874a7b7a84`  
		Last Modified: Tue, 26 May 2026 23:10:47 GMT  
		Size: 61.8 MB (61821838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798be7b2dde03ac5654762704e83aeb56c05271936195c4804ceed1184fa340d`  
		Last Modified: Tue, 26 May 2026 23:10:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58eba08d30c098193dd34a3bb6fdc97e049f0cbe33af7fc92d52912ce547668`  
		Last Modified: Tue, 26 May 2026 23:10:45 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:bb55fa334444c7e2d0431a5e02b0aa70dc18721f0d592361b87691b7dcb6d148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2994066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24674af516bde4aaa526da7038a2e255ab5521db5c6c1e4dbb921c979838a66e`

```dockerfile
```

-	Layers:
	-	`sha256:d0eee3c6dbc5f87c08ad64a90ce2b4126f55ff1efeaaf80ea73272f3a039035e`  
		Last Modified: Tue, 26 May 2026 23:10:45 GMT  
		Size: 3.0 MB (2973632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ea2403136f1100f46f11690e191f311191a4e4a2ff9cf5d5379f71a0c1ac7a2`  
		Last Modified: Tue, 26 May 2026 23:10:44 GMT  
		Size: 20.4 KB (20434 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:565858a78582216566ba00c6d15c27c1ab761680d36b6d370bd8edfb94f5a981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (133047590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ee48b8395e2d492634fc9b3af103fbd9feccd95b71eeb3e3f0d0d1e826ba96`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 26 May 2026 10:05:34 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 10:05:34 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 10:05:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 10:05:34 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 26 May 2026 10:05:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 10:05:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 26 May 2026 10:05:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 10:05:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 10:05:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 26 May 2026 10:05:35 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 10:05:35 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 26 May 2026 10:05:35 GMT
ENV container oci
# Tue, 26 May 2026 10:05:37 GMT
COPY dir:d4fda96d22b28f66ff1bcd2a6fa4e35fa9ad60695678918f055282f9b91f573c in /      
# Tue, 26 May 2026 10:05:37 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 10:05:37 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 10:05:37 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 10:05:37 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 10:05:38 GMT
COPY file:5e4784a2db9f1899592c7ac2b4556c3bb602168493a8e32d224b97a462909960 in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 10:05:38 GMT
COPY file:5e4784a2db9f1899592c7ac2b4556c3bb602168493a8e32d224b97a462909960 in /root/buildinfo/labels.json      
# Tue, 26 May 2026 10:05:39 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="28a4d5c7cdb1969ee63337adb47fcb350a380874" "org.opencontainers.image.revision"="28a4d5c7cdb1969ee63337adb47fcb350a380874" "build-date"="2026-05-26T10:05:11Z" "org.opencontainers.image.created"="2026-05-26T10:05:11Z" "release"="1779788807"org.opencontainers.image.revision=28a4d5c7cdb1969ee63337adb47fcb350a380874,org.opencontainers.image.created=2026-05-26T10:05:11Z
# Tue, 26 May 2026 23:08:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:08:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:08:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:08:26 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:08:26 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 26 May 2026 23:16:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 26 May 2026 23:16:07 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:16:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:16:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:b4743f929036f49c12be6a577cbf8dbf4b9feeebdd83aef3c82da2056289053c`  
		Last Modified: Tue, 26 May 2026 12:17:22 GMT  
		Size: 38.8 MB (38794684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e600a5e4b5bd9ee674e2def8e4bcf01be8963cfc1697cc6243834b5ac188e995`  
		Last Modified: Tue, 26 May 2026 23:08:57 GMT  
		Size: 31.9 MB (31932676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4672bc4f54705054bf70427d5dc33021ffa62771f0b0ddc713305e03e74a64bb`  
		Last Modified: Tue, 26 May 2026 23:16:44 GMT  
		Size: 62.3 MB (62317810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cf37636024a3f6be1db159d99948b32ca7d9b49dfa59a820c6403a02a80494`  
		Last Modified: Tue, 26 May 2026 23:16:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317f4b5d69090bd581f2ab512db54d9d8ee6d274b6446b9ec1bb1d7b3b0cdc24`  
		Last Modified: Tue, 26 May 2026 23:16:42 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:62b0d99a3b9c61146ddf0edbf689a44411650554992b4ed0ba43f6176d8afa42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2989629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253a3c8b3a5c2ab4f3f3a652c810eed36af54e1019da98b46b501f0b791d4597`

```dockerfile
```

-	Layers:
	-	`sha256:d399671650085ede3b93598fbea23fbd19d3d3833b22e8cf407fbfb628c97cc1`  
		Last Modified: Tue, 26 May 2026 23:16:42 GMT  
		Size: 3.0 MB (2969269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:453a0c321119fbde59cfe92d23354f0a9ac59e5e8c30508bd9da905a5fe05365`  
		Last Modified: Tue, 26 May 2026 23:16:41 GMT  
		Size: 20.4 KB (20360 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:3fc4552c8d7d3682f25fedee6070ff564cede541ef35c4e6d1c7da8826a3c33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123378724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac93d6e72097188ceb23ffc5b6768a4ee241dac6db9eb57835ad355de631d2b3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 26 May 2026 10:43:18 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 10:43:18 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 10:43:18 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 10:43:18 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 26 May 2026 10:43:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 10:43:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 26 May 2026 10:43:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 10:43:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 10:43:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 26 May 2026 10:43:18 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 10:43:18 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 26 May 2026 10:43:18 GMT
ENV container oci
# Tue, 26 May 2026 10:43:19 GMT
COPY dir:a7c5d9f6499c23f09ef7d337bda5192f5b4deca45553e74bfae9fae1b20a60ef in /      
# Tue, 26 May 2026 10:43:19 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 10:43:19 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 10:43:19 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 10:43:19 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 10:43:21 GMT
COPY file:cf7bfba0ea2e3c47e53590ead66a27ae21af2a1dca6091ce8837539a1df6f22a in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 10:43:21 GMT
COPY file:cf7bfba0ea2e3c47e53590ead66a27ae21af2a1dca6091ce8837539a1df6f22a in /root/buildinfo/labels.json      
# Tue, 26 May 2026 10:43:22 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="28a4d5c7cdb1969ee63337adb47fcb350a380874" "org.opencontainers.image.revision"="28a4d5c7cdb1969ee63337adb47fcb350a380874" "build-date"="2026-05-26T10:43:06Z" "org.opencontainers.image.created"="2026-05-26T10:43:06Z" "release"="1779788807"org.opencontainers.image.revision=28a4d5c7cdb1969ee63337adb47fcb350a380874,org.opencontainers.image.created=2026-05-26T10:43:06Z
# Tue, 26 May 2026 23:08:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:08:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:08:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:08:27 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:08:27 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 26 May 2026 23:10:55 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d12d5b19ff7f6c4a99fd4f9eecede2c96e64df7d1f41cc84f2e9c9b38408600b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='82daf66b73505d3974d831bd244acbb1123a340b7752ced449dcdca69ff3a780';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='ee513969bef35f10afb7d06840d9a421138a3d30c062cde3dda8fe780dc451a2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='487ad434d8b121ae3902d5ad9cb830cd8e1f75fefad6e2ba80f89d60e3db95d7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jre_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 26 May 2026 23:10:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:10:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:10:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:3f3af3c01ebb5e415417fa01cdc18de3e0533f557596f831f5cdf4441dd071e3`  
		Last Modified: Tue, 26 May 2026 12:17:14 GMT  
		Size: 34.4 MB (34449572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16fbdca33934ed0f808ff86b8a4651a60bfc8237caef8d52c227be117a70e44`  
		Last Modified: Tue, 26 May 2026 23:08:52 GMT  
		Size: 28.5 MB (28525745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c027c34efdb2a76cd3d9f5c5ac60670c1e15db042a0dbef4f8fe7dfe3e2bb2`  
		Last Modified: Tue, 26 May 2026 23:11:18 GMT  
		Size: 60.4 MB (60400989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0206377971cff6572ac30af9c86cf978b6d804b88a5ef04dd71a453b54aa40`  
		Last Modified: Tue, 26 May 2026 23:11:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b70fc4ea0d2c4c144a90a24a78d22857b0e1d861d16a67dd91f6b1c6f33f42`  
		Last Modified: Tue, 26 May 2026 23:11:17 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c2a98d9209ac65fd1e766c89ed00e9e76b58adce617b58494146957887063f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2990843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b8217688ca9b580bce5105878766362a2561557303b036ab9b14adae691878`

```dockerfile
```

-	Layers:
	-	`sha256:d6998392c4dd778798ad2cb1531402696258b681fb1ce81d0c167d47ded901e6`  
		Last Modified: Tue, 26 May 2026 23:11:17 GMT  
		Size: 3.0 MB (2970514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c069087fef9c76da0ae7b2b40e556e854449304d543437f61ee9c25fa5ff48ed`  
		Last Modified: Tue, 26 May 2026 23:11:17 GMT  
		Size: 20.3 KB (20329 bytes)  
		MIME: application/vnd.in-toto+json
