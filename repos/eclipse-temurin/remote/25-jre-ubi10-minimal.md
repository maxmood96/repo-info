## `eclipse-temurin:25-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:b3afce9ef408dabd96aa1415517f738214ece105ce43e5a4585306f4b4399d4e
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
$ docker pull eclipse-temurin@sha256:4e4158e02a0d16f381a34bc5dd17c568f5e343e937992b58443a33f03a7632df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154431112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924b67fe1ed63026d86e677ad384be7512b3d48577da8e4528709f3b99ea842c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL compose-id="RHEL-10.1-updates-20251031.1"
# Mon, 03 Nov 2025 17:11:09 GMT
ENV container oci
# Mon, 03 Nov 2025 17:11:10 GMT
COPY dir:b2070c3a584696dfa50295995b98f1ca6f69ef03e4ee4a779757baf0b56a1546 in /      
# Mon, 03 Nov 2025 17:11:10 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 17:11:10 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 17:11:10 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 17:11:10 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 17:11:10 GMT
COPY file:e8d237b49ae34a5f140de55c7c082573fef974034e3d7ddb0b43a196c7b15275 in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 17:11:11 GMT
COPY file:e8d237b49ae34a5f140de55c7c082573fef974034e3d7ddb0b43a196c7b15275 in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 17:11:12 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="95310b85c4dfa1ed23494ca51d86f210cb1256bf" "org.opencontainers.image.revision"="95310b85c4dfa1ed23494ca51d86f210cb1256bf" "build-date"="2025-11-03T17:10:18Z" "release"="1762189639"org.opencontainers.image.revision=95310b85c4dfa1ed23494ca51d86f210cb1256bf
# Wed, 12 Nov 2025 18:38:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Nov 2025 18:38:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:38:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Nov 2025 18:38:48 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 12 Nov 2025 18:38:48 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 12 Nov 2025 18:38:53 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 12 Nov 2025 18:38:53 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 12 Nov 2025 18:38:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 12 Nov 2025 18:38:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:e2fb7c31c3da29493a9042fb2aac284034d054c3aa5fe92e1f234b9e077ede47`  
		Last Modified: Wed, 12 Nov 2025 00:12:41 GMT  
		Size: 34.2 MB (34167037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1c9bc8d9783e339f00abd40574ced573a8788d8e857ae135cf2bf551a39eea`  
		Last Modified: Wed, 12 Nov 2025 18:39:28 GMT  
		Size: 57.7 MB (57665660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3eaa6b028490d2cf92a1026504bd580821cecfa62d79aac2af89c9204f38402`  
		Last Modified: Wed, 12 Nov 2025 18:39:32 GMT  
		Size: 62.6 MB (62595999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa5ad603dd413ad0105e46166aa65973af68a4b6e4bc8ed690c369002f43145`  
		Last Modified: Wed, 12 Nov 2025 18:39:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7a964e2391dce5428b227f26d8a0632d8ebadba3b9a1500a6b0e807ed97c57`  
		Last Modified: Wed, 12 Nov 2025 18:39:23 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a7c954c5e9c5d2046dc543ececb256339366be6ac36824c033a8ea903545a354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5625571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285aca2219683a41f6fb2a4833088ac5027484e08a1ab1d9c4e9bec8bf2c40dc`

```dockerfile
```

-	Layers:
	-	`sha256:bc2ce5bf1cc86ca111ea0a0d10746c21555860f1729970e8dc2a2b2441326a40`  
		Last Modified: Wed, 12 Nov 2025 19:15:51 GMT  
		Size: 5.6 MB (5605241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96fef16740790ff9d1b08746d52526fd2053792dc15f6147e106b9f9193bda74`  
		Last Modified: Wed, 12 Nov 2025 19:15:52 GMT  
		Size: 20.3 KB (20330 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:053e64898af19675b74d7be58298125832645f4f66808a2e66030cdd7927e6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151194278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae69b8e59fbaaa15c3901fe788caf0d64e51b09ddf98bf7b18009e1c1cc99b8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL compose-id="RHEL-10.1-updates-20251031.1"
# Mon, 03 Nov 2025 17:14:06 GMT
ENV container oci
# Mon, 03 Nov 2025 17:14:07 GMT
COPY dir:c8db51b55d4ac263e724340de097ab5a5aa8fea3d84a7bc887161a3f2c5d43d6 in /      
# Mon, 03 Nov 2025 17:14:07 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 17:14:07 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 17:14:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 17:14:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 17:14:07 GMT
COPY file:fb36c295d366f4dba8ba95e1629c37ca6425e3e98ba006db98d86ebcf2c79b44 in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 17:14:07 GMT
COPY file:fb36c295d366f4dba8ba95e1629c37ca6425e3e98ba006db98d86ebcf2c79b44 in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 17:14:08 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="95310b85c4dfa1ed23494ca51d86f210cb1256bf" "org.opencontainers.image.revision"="95310b85c4dfa1ed23494ca51d86f210cb1256bf" "build-date"="2025-11-03T17:13:46Z" "release"="1762189639"org.opencontainers.image.revision=95310b85c4dfa1ed23494ca51d86f210cb1256bf
# Wed, 12 Nov 2025 19:39:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Nov 2025 19:39:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 19:39:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Nov 2025 19:39:46 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 12 Nov 2025 19:39:46 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 12 Nov 2025 19:41:21 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 12 Nov 2025 19:41:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 12 Nov 2025 19:41:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 12 Nov 2025 19:41:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f1037a79a8a82585aa3e6b5df2e6c0a42e2f3def0513fef76cfd1daba7331879`  
		Last Modified: Wed, 12 Nov 2025 00:12:43 GMT  
		Size: 32.2 MB (32192138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f039385de436536a4878fc5323e0650e6e10bd76a940bcf77df2c0e85b3718`  
		Last Modified: Wed, 12 Nov 2025 21:00:35 GMT  
		Size: 57.5 MB (57456658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0152ac7e5919ace6fa4e87c5ef26ef28db38e811ba695484d1e3ba6ca74bf76c`  
		Last Modified: Wed, 12 Nov 2025 19:41:54 GMT  
		Size: 61.5 MB (61543060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a832e3036f00eafdf30006175bee3eed25f6387537365e49c55acb44494836`  
		Last Modified: Wed, 12 Nov 2025 19:41:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3d87caf62b5c197eab115230c8efc3ffa197a3d2f7accdfe46e8586307478f`  
		Last Modified: Wed, 12 Nov 2025 19:41:50 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:cabe2338f4bd2b2ff3986ea62882c740cd0eb0d58e7f1b46ba81ae154f2ce144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5625150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f7c3a86878d4eead3074e32f4738692279b77041076a5c558ed2c1050aaf26`

```dockerfile
```

-	Layers:
	-	`sha256:3004dfcb79efe9d77a3304a6b372a3bc6b7e38360767e1281f905cff30acd8c7`  
		Last Modified: Wed, 12 Nov 2025 22:15:22 GMT  
		Size: 5.6 MB (5604716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d187cd72b646b0206d3a7bc515be3bc826ac353d71fd0aca9e5016d631d7fc06`  
		Last Modified: Wed, 12 Nov 2025 22:15:23 GMT  
		Size: 20.4 KB (20434 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:f9320833be233979589fdac3dc0b58350e98628cd17103c014149dd20325c1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159947373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b670c246c8c26e6128a2adbb379820798b8e04c23e159b5c5224b735a7a4939e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 03 Nov 2025 18:21:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 18:21:17 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 03 Nov 2025 18:21:17 GMT
LABEL compose-id="RHEL-10.1-updates-20251031.1"
# Mon, 03 Nov 2025 18:21:17 GMT
ENV container oci
# Mon, 03 Nov 2025 18:21:19 GMT
COPY dir:bddbfbd27697aed0d6ba6e3639d53eb2bcbf54a469bc264141734564ee0873d3 in /      
# Mon, 03 Nov 2025 18:21:19 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 18:21:19 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 18:21:20 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 18:21:21 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 18:21:21 GMT
COPY file:db0b3bfc9b0c5f121f2453bb59e26e6e1b4ab566a800db9e34c541da8076e42d in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 18:21:22 GMT
COPY file:db0b3bfc9b0c5f121f2453bb59e26e6e1b4ab566a800db9e34c541da8076e42d in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 18:21:23 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="95310b85c4dfa1ed23494ca51d86f210cb1256bf" "org.opencontainers.image.revision"="95310b85c4dfa1ed23494ca51d86f210cb1256bf" "build-date"="2025-11-03T18:20:23Z" "release"="1762189639"org.opencontainers.image.revision=95310b85c4dfa1ed23494ca51d86f210cb1256bf
# Wed, 12 Nov 2025 18:51:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Nov 2025 18:51:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:51:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Nov 2025 18:51:18 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 12 Nov 2025 18:51:18 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 12 Nov 2025 19:02:08 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 12 Nov 2025 19:02:09 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 12 Nov 2025 19:02:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 12 Nov 2025 19:02:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f0606a13920710459cad07c2d91ffb3bc0d8c2d18eb333131c2e90dc0ae025c2`  
		Last Modified: Wed, 12 Nov 2025 00:12:42 GMT  
		Size: 38.2 MB (38231260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496c0fa2afff4fce2da3348f13f3ff118dfa655106daf72e83b8d728ab5a3304`  
		Last Modified: Wed, 12 Nov 2025 18:52:31 GMT  
		Size: 59.7 MB (59682969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e524ac21eb362835995a6cc5f0110acbe0dc8d3217ba07d992c26042cd91dc3`  
		Last Modified: Wed, 12 Nov 2025 19:02:46 GMT  
		Size: 62.0 MB (62030725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0bd8b93ec6f17c2ed2a6d95532ac94138b59f954657238cf1576756606726a`  
		Last Modified: Wed, 12 Nov 2025 19:02:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff662c266a3943a77e65adfd28f73723cfd9e944c1b93c711ef902065a87c873`  
		Last Modified: Wed, 12 Nov 2025 19:02:52 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4558392ebe52c59fb0abe8d172372fa5a9c605c203a7c5564596139c835fa574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f7cc87b5f8556da3f17592553521f9ca2505972c61494b25ff23f2b2c26600`

```dockerfile
```

-	Layers:
	-	`sha256:423b07645de243bc3b8563b34a0fe8c3d9933e0b9a7d039103ba37d39f6f758f`  
		Last Modified: Wed, 12 Nov 2025 19:16:01 GMT  
		Size: 5.6 MB (5593685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14602ec8992bd1cbf96a5ee49435cd7a6e299f976f59735c171321ebd0566559`  
		Last Modified: Wed, 12 Nov 2025 19:16:02 GMT  
		Size: 20.4 KB (20359 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:584539267783bd9cee4d1b8077a920f8318f0692fe256f1f6292f2f5fa97a2b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125670235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815a0a56e26dc738bb0e7c823e748a804e85eedf7bd17199d1b5d877c570dd35`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.0"       cpe="cpe:/o:redhat:enterprise_linux:10.0"       distribution-scope="public"
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 11 Nov 2025 09:53:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 11 Nov 2025 09:53:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 11 Nov 2025 09:53:26 GMT
LABEL io.openshift.expose-services=""
# Tue, 11 Nov 2025 09:53:26 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 11 Nov 2025 09:53:26 GMT
ENV container oci
# Tue, 11 Nov 2025 09:53:26 GMT
COPY dir:9f1f5449cb9454b7c05550f990009868329830ff5f598e41882e09b2985f76ce in /      
# Tue, 11 Nov 2025 09:53:26 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 11 Nov 2025 09:53:26 GMT
CMD ["/bin/bash"]
# Tue, 11 Nov 2025 09:53:26 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 11 Nov 2025 09:53:26 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 11 Nov 2025 09:53:27 GMT
COPY file:d3b5fde18206481b740a53df7391a42dcce042cfdd4edd5afeeb9637f6b9111a in /usr/share/buildinfo/labels.json      
# Tue, 11 Nov 2025 09:53:27 GMT
COPY file:d3b5fde18206481b740a53df7391a42dcce042cfdd4edd5afeeb9637f6b9111a in /root/buildinfo/labels.json      
# Tue, 11 Nov 2025 09:53:27 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="0a583d401ee29f56bb3786d762c71b4349cd93d9" "org.opencontainers.image.revision"="0a583d401ee29f56bb3786d762c71b4349cd93d9" "build-date"="2025-11-11T09:51:11Z" "release"="1762851739"org.opencontainers.image.revision=0a583d401ee29f56bb3786d762c71b4349cd93d9
# Wed, 12 Nov 2025 00:25:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Nov 2025 00:25:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:25:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Nov 2025 00:25:26 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:25:26 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 12 Nov 2025 00:44:24 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 12 Nov 2025 00:44:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 12 Nov 2025 00:44:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:44:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:1276be387a6a7c4ba51d350a6bfba6a1c72fe42d07414791e01dad4ca06bc732`  
		Last Modified: Tue, 11 Nov 2025 12:10:44 GMT  
		Size: 33.8 MB (33797474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94e9c54bbb60d78e3a1b2c270640fe5278b731547a8566cca26aacb7fbf74d5`  
		Last Modified: Wed, 12 Nov 2025 00:26:59 GMT  
		Size: 31.7 MB (31655122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7ec9c3ce14e48a5fcc7b4a37a84f8b222e7334a58456d098ed253c9d28f666`  
		Last Modified: Wed, 12 Nov 2025 00:45:22 GMT  
		Size: 60.2 MB (60215219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2f8f4b904ef56e184ca58a5dd80c5f620ded8712cb45cef96178367820c4e0`  
		Last Modified: Wed, 12 Nov 2025 00:45:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2b20254c91c4e6d4d4b9a78d94b377bb1725888b08e69beb125cc8ce34f5d1`  
		Last Modified: Wed, 12 Nov 2025 00:45:15 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2d0fb48a9cbee4d0d99862622448eb8216a68866adf511478ae0ac2a44f14bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3007468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c46eee3db2d925f23110f31dc950e9aa8ff8ab9f2c3acbe33db3252b5e4992`

```dockerfile
```

-	Layers:
	-	`sha256:771de72dad05dbd59ce1c96d89a582413f30e3d20a99ecd54c5a2d1b6aba8fe2`  
		Last Modified: Wed, 12 Nov 2025 01:17:45 GMT  
		Size: 3.0 MB (2987138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6978cc9b47c3136d7d9a0f4635ed86fabdfa6285a8048ef74af07ffd2f85df1a`  
		Last Modified: Wed, 12 Nov 2025 01:17:45 GMT  
		Size: 20.3 KB (20330 bytes)  
		MIME: application/vnd.in-toto+json
