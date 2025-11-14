## `eclipse-temurin:25-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:3bee096bf98b1e076dc4db9c8d86338bfcd19f9017c455273ddaf5129a6935a7
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
$ docker pull eclipse-temurin@sha256:c8eda85b3585ffdda6ab87453d05ba1973968059b650a983a948d911f6b34872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155292671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70860b95e56e0cd310c9342027f155b30c709e8af3b3cf2a359a4bbd5de360e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 12 Nov 2025 13:01:22 GMT
ENV container oci
# Wed, 12 Nov 2025 13:01:23 GMT
COPY dir:f2440371cac1ecd5821b1d2fdba3a255aaff3a1a77b5c3da42649fb9aa41eacf in /      
# Wed, 12 Nov 2025 13:01:23 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 13:01:23 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 13:01:23 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 13:01:23 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 13:01:23 GMT
COPY file:38c762d98ec7c6a2f80e50bd0d7f55f749ddc727f82c6ec0ecf03ddb34a3b284 in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 13:01:23 GMT
COPY file:38c762d98ec7c6a2f80e50bd0d7f55f749ddc727f82c6ec0ecf03ddb34a3b284 in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 13:01:23 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="c2904cc9bad715599f86f4c20562b90929d43731" "org.opencontainers.image.revision"="c2904cc9bad715599f86f4c20562b90929d43731" "build-date"="2025-11-12T13:01:03Z" "release"="1762952303"org.opencontainers.image.revision=c2904cc9bad715599f86f4c20562b90929d43731
# Fri, 14 Nov 2025 01:12:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:12:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:12:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 14 Nov 2025 01:12:19 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 14 Nov 2025 01:12:19 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Fri, 14 Nov 2025 01:13:28 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 14 Nov 2025 01:13:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 14 Nov 2025 01:13:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:13:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:7164be7c15828f5ba5fa7731cf51dad23a5d6c99e19fa840e574def3f4c05894`  
		Last Modified: Wed, 12 Nov 2025 17:56:02 GMT  
		Size: 34.5 MB (34515519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0fbb7557ab5bfb244bc549cff06eefb17390e0aeb1692d223a263d5ad8cc47`  
		Last Modified: Fri, 14 Nov 2025 01:12:53 GMT  
		Size: 58.2 MB (58178800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43cbee6adb124229a7a33ba44a4e8040ae0571af5a9016fd6b6741c6d3168d76`  
		Last Modified: Fri, 14 Nov 2025 01:13:56 GMT  
		Size: 62.6 MB (62595936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a2096be4e3b2cc2aa1dd8d90e4a7ece73061025227b6346b620a6afab7f43f`  
		Last Modified: Fri, 14 Nov 2025 01:13:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4914df549d9f030a19f14f96508f7c94201ca1267dfb16004c8eedf1ae5280`  
		Last Modified: Fri, 14 Nov 2025 01:13:48 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:081ff2a4195d5891c005c08a446288d2a2e939ead63d4f7618dd33bfffda5854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5625173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be2ebc3cc5fb41ac7b28b038499cc71a357a206a8c7726c2dac6f22f2c73ddad`

```dockerfile
```

-	Layers:
	-	`sha256:04ed4d2dc9845f80363674a603d517745a7389998992be8ba967d05ecc1a45f9`  
		Last Modified: Fri, 14 Nov 2025 04:17:55 GMT  
		Size: 5.6 MB (5604843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56159b4d33658ec3a01f4b813dfba05aa374cee4e4acf5196e91fafe8a81a47c`  
		Last Modified: Fri, 14 Nov 2025 04:17:56 GMT  
		Size: 20.3 KB (20330 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:6d67fd78530c59455e6069bd27a31c48183221832b21a9bfa94873f32731ff89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151932539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73af53bbea67dc92473d67882428e613b8eaf54927aa0213e123bd7803bb4b87`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 12 Nov 2025 13:07:41 GMT
ENV container oci
# Wed, 12 Nov 2025 13:07:42 GMT
COPY dir:7dfb9511ae2d70910df52107d5c96c0335e87f2a1f5d8a5592e4e62e34a4c8d6 in /      
# Wed, 12 Nov 2025 13:07:42 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 13:07:42 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 13:07:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 13:07:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 13:07:42 GMT
COPY file:5949e56b1cb83ef43c9cba7c361cdb23e3aace250acdaec4205faff29b91de6c in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 13:07:42 GMT
COPY file:5949e56b1cb83ef43c9cba7c361cdb23e3aace250acdaec4205faff29b91de6c in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 13:07:42 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="c2904cc9bad715599f86f4c20562b90929d43731" "org.opencontainers.image.revision"="c2904cc9bad715599f86f4c20562b90929d43731" "build-date"="2025-11-12T13:07:20Z" "release"="1762952303"org.opencontainers.image.revision=c2904cc9bad715599f86f4c20562b90929d43731
# Fri, 14 Nov 2025 01:28:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:28:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:28:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 14 Nov 2025 01:28:43 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 14 Nov 2025 01:28:43 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Fri, 14 Nov 2025 01:29:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 14 Nov 2025 01:29:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 14 Nov 2025 01:29:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:29:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:372b71efdab733f5ad0749f1537278e34899107888219d8358967ddbd9eb2db3`  
		Last Modified: Wed, 12 Nov 2025 18:16:55 GMT  
		Size: 32.6 MB (32601501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcb0a4fab263866977261141e74dc0ae5937c77e207be4fc79928d7c61d5fd3`  
		Last Modified: Fri, 14 Nov 2025 01:29:28 GMT  
		Size: 57.8 MB (57785591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586cbe814f7c42372cd7eac72127090f9f8567d247ba6661105f093fbf6c5d84`  
		Last Modified: Fri, 14 Nov 2025 01:30:09 GMT  
		Size: 61.5 MB (61543029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55a805520166757a0ccf815d47a46d564da25850daeaffe46d2c5159bdd9efa`  
		Last Modified: Fri, 14 Nov 2025 01:29:56 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704966c60feaa9ffcc6583374ef2f3ddf6ccb0cc0235cb632e2558b1e5a060fa`  
		Last Modified: Fri, 14 Nov 2025 01:29:56 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c8d751e7a955fddcc076b4386c83493bf32866130037e28deb819f1957970c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5624751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69b4a701f9f398c0ac0e68c3e47c24a9094fd7c0211849d3c18d152c4107f80`

```dockerfile
```

-	Layers:
	-	`sha256:8699a828d02e0681dd2adfe904fce08af85a71e08a101c42221f585a5dce2540`  
		Last Modified: Fri, 14 Nov 2025 04:18:02 GMT  
		Size: 5.6 MB (5604318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:928192105dd565eb0164a4cea5f6993ccee5d303604696192c04a3aafa254642`  
		Last Modified: Fri, 14 Nov 2025 04:18:02 GMT  
		Size: 20.4 KB (20433 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:0410cf4f8475a957602904d7552da9d8c6b4d4122852bcf2ecc5d788510a7a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161137537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574d502dc3c8dd49b185dfa41a1783b03ea3f298c2999cea512bfae2296b5f8a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 12 Nov 2025 13:21:41 GMT
ENV container oci
# Wed, 12 Nov 2025 13:21:42 GMT
COPY dir:7f428fa29fa8f7e829b041452235ccc73eb7caf26242995ea3907c084b7e797f in /      
# Wed, 12 Nov 2025 13:21:42 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 13:21:42 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 13:21:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 13:21:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 13:21:42 GMT
COPY file:aa98cda558c12f3c05f9e28e398d23d3217b73b93e9d498cde74f10837d73035 in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 13:21:42 GMT
COPY file:aa98cda558c12f3c05f9e28e398d23d3217b73b93e9d498cde74f10837d73035 in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 13:21:42 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="c2904cc9bad715599f86f4c20562b90929d43731" "org.opencontainers.image.revision"="c2904cc9bad715599f86f4c20562b90929d43731" "build-date"="2025-11-12T13:21:30Z" "release"="1762952303"org.opencontainers.image.revision=c2904cc9bad715599f86f4c20562b90929d43731
# Fri, 14 Nov 2025 02:04:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 02:04:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 02:04:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 14 Nov 2025 02:04:01 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 14 Nov 2025 02:04:01 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Fri, 14 Nov 2025 02:25:36 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 14 Nov 2025 02:25:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 14 Nov 2025 02:25:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 14 Nov 2025 02:25:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:402f9c025c3a63d9edbbd78a8cf9e2813de76854342058db2814aa404ddbcf6c`  
		Last Modified: Wed, 12 Nov 2025 18:16:57 GMT  
		Size: 38.7 MB (38746677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6af666f8de2b0c285f4b7d038631ab495275355fdde5c07cca653c2f3d29143`  
		Last Modified: Fri, 14 Nov 2025 02:05:21 GMT  
		Size: 60.4 MB (60357723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5752cb23bb36373b696e734df74ab5e5e478516af3d3ac4cec52f815f54f55e6`  
		Last Modified: Fri, 14 Nov 2025 02:26:26 GMT  
		Size: 62.0 MB (62030720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105c904d09ebb192c9edd3c9104109fcc5d8c494a0c33a53c4a89eda2c1ce60e`  
		Last Modified: Fri, 14 Nov 2025 02:26:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f413c741aa2064df84ab11a6a0297db289695b81966f019afa2a80d2c36a4e`  
		Last Modified: Fri, 14 Nov 2025 02:26:19 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:015c2fd7cbdb222065c04038fd085d412dbad7a137525b69cb13b5a6fbffb247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904d22abd7730447e68a6c5b9719cd6be42e23c57b0fbe03016ee73c5177caf6`

```dockerfile
```

-	Layers:
	-	`sha256:85d34c530c322fdcd40b40840000e42901595a85406bbda9f4e4c074e660ddfc`  
		Last Modified: Fri, 14 Nov 2025 04:18:07 GMT  
		Size: 5.6 MB (5593287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96c5b8f8491b1e200805f1d17a761cb45b3014c76cbefc90351c139507c5e994`  
		Last Modified: Fri, 14 Nov 2025 04:18:08 GMT  
		Size: 20.4 KB (20360 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:f9c8150084b0a2f7eb552f642128a5df60291dd8842cdaf7b6a4da832051baba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153147580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ab557c28a3e340026b2f28ff8d643a25bebf379b72397c2e0a4349cf2dec2e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 12 Nov 2025 13:48:02 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 12 Nov 2025 13:48:02 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 13:48:02 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 13:48:02 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 12 Nov 2025 13:48:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 13:48:02 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 12 Nov 2025 13:48:02 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 13:48:02 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 13:48:02 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 12 Nov 2025 13:48:02 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 13:48:02 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 12 Nov 2025 13:48:02 GMT
ENV container oci
# Wed, 12 Nov 2025 13:48:02 GMT
COPY dir:9f3cd8bad135d97a4278eb0e74f1a89cc165a45d6f123e529f2973da46a240af in /      
# Wed, 12 Nov 2025 13:48:02 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 13:48:02 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 13:48:02 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 13:48:02 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 13:48:03 GMT
COPY file:cb4b6de2d10271c95dac78e592bde3a3d1599b2eb6bebad022cd5ead593fccb8 in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 13:48:03 GMT
COPY file:cb4b6de2d10271c95dac78e592bde3a3d1599b2eb6bebad022cd5ead593fccb8 in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 13:48:03 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="c2904cc9bad715599f86f4c20562b90929d43731" "org.opencontainers.image.revision"="c2904cc9bad715599f86f4c20562b90929d43731" "build-date"="2025-11-12T13:45:41Z" "release"="1762952303"org.opencontainers.image.revision=c2904cc9bad715599f86f4c20562b90929d43731
# Fri, 14 Nov 2025 01:36:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:36:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:36:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 14 Nov 2025 01:36:56 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 14 Nov 2025 01:36:56 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Fri, 14 Nov 2025 01:41:01 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 14 Nov 2025 01:41:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 14 Nov 2025 01:41:01 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:41:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:2c5bd53b2567eef590494f06f626482f402fa97fb095307b2a27e75fe98f195b`  
		Last Modified: Wed, 12 Nov 2025 18:16:54 GMT  
		Size: 34.4 MB (34378541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86b5f1c27d55d732e1d564e35c7811cd6d8226b38c683337005753638213a52`  
		Last Modified: Fri, 14 Nov 2025 01:37:38 GMT  
		Size: 58.6 MB (58551503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5886567350c9b5a57d6cb585c60a4ff52746505964f201a46c3b20f5d0ecd8`  
		Last Modified: Fri, 14 Nov 2025 01:41:33 GMT  
		Size: 60.2 MB (60215119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae41281e72bc062d234c2dc3f1fe64b4e82b0a67962f6bfcc55336acc741bc4d`  
		Last Modified: Fri, 14 Nov 2025 01:41:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a558347d6fa6b4d49d472eab2978fc471dd1b9e06a955978d718e1b5fb4878`  
		Last Modified: Fri, 14 Nov 2025 01:41:27 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:39fd24de480a07b985b4327b7fa6311d74f7b01f416f4063f50459d43ddb6724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a7a08986e8b81713ef3e9f73ae2682973bb311e997cc4c108032b1f08da8e9`

```dockerfile
```

-	Layers:
	-	`sha256:44bb8bb3fb74ab0d2fcea0dafe0e9baa40ef1ce0e37eca023739e7bdfdaf1f44`  
		Last Modified: Fri, 14 Nov 2025 04:18:17 GMT  
		Size: 5.6 MB (5594148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc237fa7a1b3ab9fa94a9d7d668bfe205e4c0e10b8681e62d070651aa6d9197e`  
		Last Modified: Fri, 14 Nov 2025 04:18:18 GMT  
		Size: 20.3 KB (20330 bytes)  
		MIME: application/vnd.in-toto+json
