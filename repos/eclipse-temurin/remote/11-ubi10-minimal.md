## `eclipse-temurin:11-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:92d0d05e9e7392ed29e6de8656ef564ffcc6ed12e76ed83318b35768a14a7188
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

### `eclipse-temurin:11-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:4d4605925fc6388af09d5e3ad546c80f92ccb1556beea86202358b20219974da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.3 MB (214342641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677f3095379d5c973bb298cf3587d674ed6c8f8e6331ff427125098d6de7deef`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL io.openshift.expose-services=""
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 23 Mar 2026 01:13:56 GMT
ENV container oci
# Mon, 23 Mar 2026 01:13:56 GMT
COPY dir:e4512bf3738a47eefff7ab81e82e38ca2f5173e43ee99a65e6dd13d89e02bd8f in /      
# Mon, 23 Mar 2026 01:13:56 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 23 Mar 2026 01:13:57 GMT
CMD ["/bin/bash"]
# Mon, 23 Mar 2026 01:13:57 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 23 Mar 2026 01:13:57 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 23 Mar 2026 01:13:57 GMT
COPY file:0abc55831e7dab59520989ee7f9e642cfb86d0399f7103e87f7378145dd94508 in /usr/share/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:13:57 GMT
COPY file:0abc55831e7dab59520989ee7f9e642cfb86d0399f7103e87f7378145dd94508 in /root/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:13:57 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "org.opencontainers.image.revision"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "build-date"="2026-03-23T01:13:42Z" "org.opencontainers.image.created"="2026-03-23T01:13:42Z" "release"="1774228210"org.opencontainers.image.revision=5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6,org.opencontainers.image.created=2026-03-23T01:13:42Z
# Mon, 23 Mar 2026 18:16:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 23 Mar 2026 18:16:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:16:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 23 Mar 2026 18:16:50 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 23 Mar 2026 18:16:50 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Mon, 23 Mar 2026 18:16:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 23 Mar 2026 18:16:58 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 23 Mar 2026 18:16:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 23 Mar 2026 18:16:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 23 Mar 2026 18:16:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2979ea27473f21e894361ff5d915252c378d4a8073aca3908465bbbf348780b7`  
		Last Modified: Mon, 23 Mar 2026 03:10:44 GMT  
		Size: 34.6 MB (34630234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdaf01da6f07342831e957c72c706fdd93c1fb1bdfec31321d0819a1167a91a6`  
		Last Modified: Mon, 23 Mar 2026 18:17:16 GMT  
		Size: 37.4 MB (37446633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75df620fe4c388a1cffb736af1cee7a98a4ea627cccec390fcb8657aa2f4423`  
		Last Modified: Mon, 23 Mar 2026 18:17:20 GMT  
		Size: 142.3 MB (142263355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0692332509c77a943bb92d2650f76151c2d89c59838c39c587e9d33feb2fee76`  
		Last Modified: Mon, 23 Mar 2026 18:17:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e25a94dc2e7b5311ae0f2060be6c0fc0db270ee357b8c097c80ad8b08142e64`  
		Last Modified: Mon, 23 Mar 2026 18:17:14 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c48ae101ee5c9364db543d5268b80829cdcea3ca34ce1af2635e92bdd3c005f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3830605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d2e10fbf20d585ae0e39731de3450c4f0d9001eb1f4bc3ac168f5fb40d7af3`

```dockerfile
```

-	Layers:
	-	`sha256:01b9b48768b78aa6ab6d6412c7f580f0262eda172db29578bdcf1ca636d825f8`  
		Last Modified: Mon, 23 Mar 2026 18:17:15 GMT  
		Size: 3.8 MB (3809289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e4074f72663f0955ca41284cd5cbf5a2412265308532a394b83531696fd7308`  
		Last Modified: Mon, 23 Mar 2026 18:17:14 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:1b82ac2ffbf57f6f4fc45e158ecec98ae890253fce829fed92ec7351515da6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.0 MB (209037803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f501d35cbfd9ac14a97dc66ac440e16ad8c6bafeedc7aa03659b1261d070a783`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL io.openshift.expose-services=""
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 23 Mar 2026 01:17:03 GMT
ENV container oci
# Mon, 23 Mar 2026 01:17:04 GMT
COPY dir:5423a2d232cda7a57202522795efee6ca78fcc0651e41ab821993b780fdf8627 in /      
# Mon, 23 Mar 2026 01:17:04 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 23 Mar 2026 01:17:04 GMT
CMD ["/bin/bash"]
# Mon, 23 Mar 2026 01:17:04 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 23 Mar 2026 01:17:05 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 23 Mar 2026 01:17:05 GMT
COPY file:c5d7f4f2dd90b98f707a017338d65e0949c625a6c68e260ee9a0d4613ffd89fd in /usr/share/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:17:05 GMT
COPY file:c5d7f4f2dd90b98f707a017338d65e0949c625a6c68e260ee9a0d4613ffd89fd in /root/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:17:05 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "org.opencontainers.image.revision"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "build-date"="2026-03-23T01:16:47Z" "org.opencontainers.image.created"="2026-03-23T01:16:47Z" "release"="1774228210"org.opencontainers.image.revision=5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6,org.opencontainers.image.created=2026-03-23T01:16:47Z
# Mon, 23 Mar 2026 18:16:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 23 Mar 2026 18:16:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:16:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 23 Mar 2026 18:16:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 23 Mar 2026 18:16:34 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Mon, 23 Mar 2026 18:16:40 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 23 Mar 2026 18:16:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 23 Mar 2026 18:16:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 23 Mar 2026 18:16:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 23 Mar 2026 18:16:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cbfdca2ca63ac63914141abb4cb933134b748fc3efb6e835daea267d6feb9296`  
		Last Modified: Mon, 23 Mar 2026 03:33:50 GMT  
		Size: 32.7 MB (32686471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166588b2cf544062ff66bebc145903570b80057b1a9905a3c215073a606223e0`  
		Last Modified: Mon, 23 Mar 2026 18:17:00 GMT  
		Size: 37.4 MB (37389149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a4eeded6664bac8f6437a2f4ddc86f311d8189e8bc068ced81ad7a83fd2993`  
		Last Modified: Mon, 23 Mar 2026 18:17:02 GMT  
		Size: 139.0 MB (138959763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb344a7c555f0482d74f07259664b9420c3f8de6c38d006f6215321c9a988a00`  
		Last Modified: Mon, 23 Mar 2026 18:16:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30001fae49022674ae51c0db65bddee996caa676e0c5150b307e998f596347e6`  
		Last Modified: Mon, 23 Mar 2026 18:16:58 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b08d6246d03c2c097c0504b14fb438aa6b13d4330f1e30200ee360524f7d4ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3830764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0909d2b7d69360839acc8128e8b221fbf080a02b0bb100c7bc168e9f24a1654e`

```dockerfile
```

-	Layers:
	-	`sha256:3d0bdaad8ce96ab9b26347c1728a0b8960876d7c48a1068a71f99c6585928a48`  
		Last Modified: Mon, 23 Mar 2026 18:16:59 GMT  
		Size: 3.8 MB (3809333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d422ef5b1a099b84fc8bb3015d9cd2d4993d16b64b9b3cfdfb8f4b3e8c3bbc23`  
		Last Modified: Mon, 23 Mar 2026 18:16:58 GMT  
		Size: 21.4 KB (21431 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:0725e0dc4e2807aed4c7657206e476a35a67d07601da968766637c03b9451ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.4 MB (207429169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ef2bf2ae95210ea8a87a971a6aad58e54c2481331ec81bc9100852baf9fa45`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Mar 2026 01:15:45 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 23 Mar 2026 01:15:45 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 23 Mar 2026 01:15:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 23 Mar 2026 01:15:45 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 23 Mar 2026 01:15:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 23 Mar 2026 01:15:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 23 Mar 2026 01:15:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:15:46 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:15:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 23 Mar 2026 01:15:46 GMT
LABEL io.openshift.expose-services=""
# Mon, 23 Mar 2026 01:15:46 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 23 Mar 2026 01:15:46 GMT
ENV container oci
# Mon, 23 Mar 2026 01:15:46 GMT
COPY dir:6d632c778a00dcaccd2b27492019a49da2e9ded15d90cc220bd8ef2e111c01aa in /      
# Mon, 23 Mar 2026 01:15:46 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 23 Mar 2026 01:15:46 GMT
CMD ["/bin/bash"]
# Mon, 23 Mar 2026 01:15:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 23 Mar 2026 01:15:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 23 Mar 2026 01:15:47 GMT
COPY file:c49dc785bea5c076578ee2a5e8eb4e7290c033b08769d6c1e8e12f43990c44cc in /usr/share/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:15:47 GMT
COPY file:c49dc785bea5c076578ee2a5e8eb4e7290c033b08769d6c1e8e12f43990c44cc in /root/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:15:47 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "org.opencontainers.image.revision"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "build-date"="2026-03-23T01:15:34Z" "org.opencontainers.image.created"="2026-03-23T01:15:34Z" "release"="1774228210"org.opencontainers.image.revision=5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6,org.opencontainers.image.created=2026-03-23T01:15:34Z
# Mon, 23 Mar 2026 18:25:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 23 Mar 2026 18:25:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:25:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 23 Mar 2026 18:25:02 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 23 Mar 2026 18:25:02 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Mon, 23 Mar 2026 18:26:15 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 23 Mar 2026 18:26:18 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 23 Mar 2026 18:26:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 23 Mar 2026 18:26:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 23 Mar 2026 18:26:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6b71f50ac5496b49a24d4e0868fe8e453f93532ef823631b2317185af571b8e7`  
		Last Modified: Mon, 23 Mar 2026 06:15:15 GMT  
		Size: 38.7 MB (38727029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c8eaa293db94961782c260ece22ece0b24bab37073f3fe6b143b29d7b188a9`  
		Last Modified: Mon, 23 Mar 2026 18:25:46 GMT  
		Size: 39.2 MB (39200511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184a1e893b8761bf80649a9d72a0f7539e7a6c59e265060a4cfbb4ee3c3fd351`  
		Last Modified: Mon, 23 Mar 2026 18:26:52 GMT  
		Size: 129.5 MB (129499208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a98ecb528077b4ed3e927cffad7425e2674f73d9b0d6b5abdae33577a7fe2ac`  
		Last Modified: Mon, 23 Mar 2026 18:26:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a11421c23fef1324dd4bf1a7f6012e09bf76970d368dbd28c36fd51030da31`  
		Last Modified: Mon, 23 Mar 2026 18:26:49 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:36280ace5625686d73ad4a44ee799d19fcb6980c7e614d312765892f5ea63f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3816858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c145ef9fea0148af675e0325986e24e1d7c851d279ef7a8c9f58659b2392e6`

```dockerfile
```

-	Layers:
	-	`sha256:477668a21436f3e414218cc2905a2bb94856b3a96f9a034d07cc7bc797e0d2c2`  
		Last Modified: Mon, 23 Mar 2026 18:26:49 GMT  
		Size: 3.8 MB (3795506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457d4678dbee506a66b846a5b1c43a903936a2d044dd0809ba9f99a14f7a0fa1`  
		Last Modified: Mon, 23 Mar 2026 18:26:49 GMT  
		Size: 21.4 KB (21352 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:f11997f067d54a0bf40133f8f2f895fd71636737d6ed8ef43953f5f7b912651e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.2 MB (195232441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26060143b769fdfdfbd9ed5d1425436ccf967b2b77f43131f315c8bf18a69fc5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL io.openshift.expose-services=""
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 23 Mar 2026 01:50:52 GMT
ENV container oci
# Mon, 23 Mar 2026 01:50:53 GMT
COPY dir:a20807155e5dba5b4fe6159d124b2858e52124008e54fbaacb8e89f074571573 in /      
# Mon, 23 Mar 2026 01:50:53 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 23 Mar 2026 01:50:53 GMT
CMD ["/bin/bash"]
# Mon, 23 Mar 2026 01:50:53 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 23 Mar 2026 01:50:53 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 23 Mar 2026 01:50:53 GMT
COPY file:f444544eabeceb45eb54e7d25741c29001ce8ceeb34cf764e4e6f1bae0509e32 in /usr/share/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:50:53 GMT
COPY file:f444544eabeceb45eb54e7d25741c29001ce8ceeb34cf764e4e6f1bae0509e32 in /root/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:50:53 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "org.opencontainers.image.revision"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "build-date"="2026-03-23T01:50:09Z" "org.opencontainers.image.created"="2026-03-23T01:50:09Z" "release"="1774228210"org.opencontainers.image.revision=5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6,org.opencontainers.image.created=2026-03-23T01:50:09Z
# Mon, 23 Mar 2026 18:13:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 23 Mar 2026 18:13:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:13:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 23 Mar 2026 18:13:09 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 23 Mar 2026 18:13:09 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Mon, 23 Mar 2026 19:10:00 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 23 Mar 2026 19:10:02 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 23 Mar 2026 19:10:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 23 Mar 2026 19:10:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 23 Mar 2026 19:10:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c4143dec68dd3a33451fd532f787cf2f31d86a312b4b1a8a58cadb88900ac88`  
		Last Modified: Mon, 23 Mar 2026 06:15:08 GMT  
		Size: 34.4 MB (34429605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afaeb08174d6252e90dd2ef49bcd22e4089aa0abd5c05e34ae09915fe72186b`  
		Last Modified: Mon, 23 Mar 2026 18:13:32 GMT  
		Size: 37.8 MB (37827698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70675303e04890380d0925c91cc117f4918e2889940d59d90d218450ecc8236b`  
		Last Modified: Mon, 23 Mar 2026 19:10:27 GMT  
		Size: 123.0 MB (122972721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533b2d94db97eede1f570a7c150003875486bdfbd14de5bb596bc26e8795d851`  
		Last Modified: Mon, 23 Mar 2026 19:10:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91844f453878cb6975b1548141833e8e43ed322dfe4beed2b23bd18e7fc59e69`  
		Last Modified: Mon, 23 Mar 2026 19:10:24 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3d5c279fda3db93e1ad31a4b214e5375af0a5e437302417551fef50b2948b93a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3816198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81f2093505867f07121971623b91a7c99844d0c0360a196236d096a175e366a`

```dockerfile
```

-	Layers:
	-	`sha256:eca89e246e8475ee1d7ab1b7f799442c71c4ff886a8cd1bb299b89dac538ad34`  
		Last Modified: Mon, 23 Mar 2026 19:10:25 GMT  
		Size: 3.8 MB (3794883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54daf8a771e67b375f09bc0a2089ec6a2e8f46f88cfeaf5844857c256c76cc9c`  
		Last Modified: Mon, 23 Mar 2026 19:10:24 GMT  
		Size: 21.3 KB (21315 bytes)  
		MIME: application/vnd.in-toto+json
