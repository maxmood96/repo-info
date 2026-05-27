## `eclipse-temurin:25-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:b334eaf83c557581afa3a4f6f1a69cecdd944ff74882e53107b9ecd36358bee3
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

### `eclipse-temurin:25-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:e52d001856abafd0d9c317eb0404cc7edb9ff1ea5ee02a017a9ce6f0207b4917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156131187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caef656e534521aa961bde827cd6fe9918b72cd818c83f242c8935f20ee4674c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Tue, 26 May 2026 23:09:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:09:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:09:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:09:53 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:09:53 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 26 May 2026 23:10:48 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 26 May 2026 23:10:49 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:10:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:10:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 26 May 2026 23:10:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:368dae9e745ec994e59731b33513a5334145ab500bb4162a1597ced6ca7d2dd0`  
		Last Modified: Tue, 26 May 2026 11:30:57 GMT  
		Size: 34.6 MB (34624420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bd923dc421fa93848bf3fcd2b19fe2f94d0874b4d499b1fd92e8662fe320af`  
		Last Modified: Tue, 26 May 2026 23:10:08 GMT  
		Size: 28.9 MB (28924970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba96a834e39f1b206b9c792b9c19b278275c4978e8d1495e5f3420ca557abfa`  
		Last Modified: Tue, 26 May 2026 23:11:06 GMT  
		Size: 92.6 MB (92579378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c243ef86ca970077e72d81f25799abae1daac6ef319fa7803255cfa32d16055c`  
		Last Modified: Tue, 26 May 2026 23:11:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26da59f03f293200cdc4ea499b527e74cefc987306a7440c89ca96f67ae0143f`  
		Last Modified: Tue, 26 May 2026 23:11:03 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a4613682b4462f6976e87bc7c6bb3526541dcb799758404e0f83662852eb7cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3039816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bdc8d7ef8cb960ed3eff2ac77de560eb3b6fed71a2d320d6fc65b592c88536e`

```dockerfile
```

-	Layers:
	-	`sha256:d2ae65263f7377b45c4afa14964134f4ebba9083c5439ce5dd429d7cf4cfcf65`  
		Last Modified: Tue, 26 May 2026 23:11:04 GMT  
		Size: 3.0 MB (3018528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1094871d1c430d8e0fd4a563c70c7ae91f0c35ac9bda4f19d15883cbac74f188`  
		Last Modified: Tue, 26 May 2026 23:11:03 GMT  
		Size: 21.3 KB (21288 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:0a8642658898dd5cbf8fbc9e837577753d5b2790474785d1b55075e02189d725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152603552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d73a0053f45287420f009ff9dba0ace97b97c7fc77976707d6855cf73ba364a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Tue, 26 May 2026 23:09:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:09:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:09:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:09:43 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:09:43 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 26 May 2026 23:10:23 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 26 May 2026 23:10:25 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:10:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:10:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 26 May 2026 23:10:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d44582f6016d5b17ffe3577358bcbf1bf84edfe2aba6b73b6461e6631e0a4bc7`  
		Last Modified: Tue, 26 May 2026 11:41:50 GMT  
		Size: 32.7 MB (32711602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c1df6c230f9d35da82702251db2c1f7d008413743e0abf5a54a62a8f4d276a`  
		Last Modified: Tue, 26 May 2026 23:10:08 GMT  
		Size: 28.3 MB (28340639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00745369746deb246d27f8a70ad0644fa1c2866e1cb371da5d63e9c92ac6ce39`  
		Last Modified: Tue, 26 May 2026 23:10:45 GMT  
		Size: 91.5 MB (91548890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76bf23b050f9230df26dc96badf721eabfc33286513f54d638d89ccc2364e73`  
		Last Modified: Tue, 26 May 2026 23:10:41 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339749c5b1dacc298eccc71697176da567ef6e7bc1ec427f7f0446cd08276aff`  
		Last Modified: Tue, 26 May 2026 23:10:41 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:83a9cbee5d9b05ef84dbeee3382a68e823d8c702ce3bc44014602f317ffededa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3039356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0114c1e437386c3ab7bf3915eebe26624764d7926b2fea5a4cc55c5cc56fd4`

```dockerfile
```

-	Layers:
	-	`sha256:e6fdafffb0713dc914de6e1ac72504b0f415a28d4e3530251fef5f73b38c9566`  
		Last Modified: Tue, 26 May 2026 23:10:41 GMT  
		Size: 3.0 MB (3017951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c25a33904230a24c7a99b61cd7d6c6f91403f5c94be9080c154b6abd8c8259d4`  
		Last Modified: Tue, 26 May 2026 23:10:41 GMT  
		Size: 21.4 KB (21405 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:5d5d429c9af4328ee3532a50798b0108d684028419183d60b4485174e9405888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162642699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e62f1b17b9754f674fcc94ad0186a367f6c43ab3d3146a1a896f33d6d9eaaf`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 26 May 2026 23:16:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:16:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:16:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 26 May 2026 23:16:11 GMT
CMD ["jshell"]
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
	-	`sha256:86e74483bc9266336c56fe0b95889ddfedae62cb547839f425b4ea9b0efff8bd`  
		Last Modified: Tue, 26 May 2026 23:16:46 GMT  
		Size: 91.9 MB (91912916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0cb6a21247830051c439f1ad7e2dabb7cb19cedb5eb730b4eda048ae473110`  
		Last Modified: Tue, 26 May 2026 23:16:44 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9acfedf0029c430cacdd169d7bae8fbbe11fe82e1a83fe1a74d41828a13e20`  
		Last Modified: Tue, 26 May 2026 23:16:44 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b101e6b5b665106626a94a825bf5047bd247a4c979ce85c4693572069f586212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3016921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd484f037d03e46c3626a64020db1bb3a6396ad50f26766e3fbd7e50b66ab70`

```dockerfile
```

-	Layers:
	-	`sha256:752d2b700ec55d0284056940fc5eb121a6733a708fa0136a7c7a035e9651691a`  
		Last Modified: Tue, 26 May 2026 23:16:44 GMT  
		Size: 3.0 MB (2995596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad430e8face2438f2e0533eeef5d8d980ce37442b7956ed23537120ebe52169f`  
		Last Modified: Tue, 26 May 2026 23:16:44 GMT  
		Size: 21.3 KB (21325 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:7859f2875d285ec9ad2f2cbdebf06d1a10f7bbd4728fd010d9e3f00e28cebac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151399464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7f7ae0379d3305b1b282aad3ffaad32b3e09b1f7471e274b542f60eeda8232`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Tue, 26 May 2026 23:08:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:08:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:08:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:08:25 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:08:25 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 26 May 2026 23:10:51 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 26 May 2026 23:10:53 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:10:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:10:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 26 May 2026 23:10:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3f3af3c01ebb5e415417fa01cdc18de3e0533f557596f831f5cdf4441dd071e3`  
		Last Modified: Tue, 26 May 2026 12:17:14 GMT  
		Size: 34.4 MB (34449572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c036331f082117718d32b7a6dcfa78b23ee5fa1dcd892f2d797f021397b44fb8`  
		Last Modified: Tue, 26 May 2026 23:08:58 GMT  
		Size: 28.5 MB (28525803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31f2b74279c2a6192c5bd0f0e09da192c544c80a3e43c8e12dfcb867f2c47d7`  
		Last Modified: Tue, 26 May 2026 23:11:20 GMT  
		Size: 88.4 MB (88421668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011ac04ed91d185622a64c578deac5ba82ab094f42168d036a2c3b9ffedf9de3`  
		Last Modified: Tue, 26 May 2026 23:11:18 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74218558a996ec2f93c4bce3c7ee118e63bdf857075c3bdeeea21f6592a08cb8`  
		Last Modified: Tue, 26 May 2026 23:11:12 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9fb660419455fcb6068aa986aac9817c861d6c0cec449e41864300504fe4ded5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3016892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c01d988a371c40901a89bdfdcb783a726cd69a56f5d4938a3cf11670b24b8580`

```dockerfile
```

-	Layers:
	-	`sha256:67ad7d489b9d2eacbb282325918e6526a8475e4ebd63b91c5e01e796d1ae5f31`  
		Last Modified: Tue, 26 May 2026 23:11:18 GMT  
		Size: 3.0 MB (2995604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27578a261e0f2de8449f958ca4bdeb7bf50e766508304124d9730f68bfd26dc1`  
		Last Modified: Tue, 26 May 2026 23:11:18 GMT  
		Size: 21.3 KB (21288 bytes)  
		MIME: application/vnd.in-toto+json
