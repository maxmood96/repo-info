## `eclipse-temurin:8u472-b08-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:843d8788d4649003068c6633baf064a98f238aafd21bb891e6e29d6fbf3745f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8u472-b08-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:88eeab15e900f3af1d4b726b64fe0d89875da6b21dc557af32405a4f524943e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112314253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e49fec94fe1f645a8e39c778a3be417d2a590153c191b4d723e9f2cff446ae9c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 22 Jan 2026 05:12:49 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:50 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 05:12:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 05:12:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 05:12:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 05:13:00 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 05:13:01 GMT
ENV container oci
# Thu, 22 Jan 2026 05:13:09 GMT
COPY dir:de0fcf5c4847724050e2f935a6ca475ba4c6d0b18e49a32c8b2e370255fb563e in /      
# Thu, 22 Jan 2026 05:13:12 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 05:13:13 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 05:13:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 05:13:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 05:13:19 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:21 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:37 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T05:09:47Z" "org.opencontainers.image.created"="2026-01-22T05:09:47Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T05:09:47Z
# Mon, 26 Jan 2026 22:04:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 26 Jan 2026 22:04:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:04:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jan 2026 22:04:37 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:04:37 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Mon, 26 Jan 2026 22:04:45 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 26 Jan 2026 22:04:45 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 26 Jan 2026 22:04:45 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 26 Jan 2026 22:04:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:55c0205b422beeca9ab8ece9c61b1e34f31686b8a7adf249272ac75b4dd57e4d`  
		Last Modified: Mon, 26 Jan 2026 04:14:55 GMT  
		Size: 40.0 MB (40005014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8452324aa79975138778d2423bda5fb74e58d6a0c5a63947d2eeabd3a8a8290`  
		Last Modified: Mon, 26 Jan 2026 22:04:57 GMT  
		Size: 30.4 MB (30419167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2f45589f10a065dc0a8f2e28e9546140b8c587e6706ef7cdf4130b8081f639`  
		Last Modified: Mon, 26 Jan 2026 22:04:57 GMT  
		Size: 41.9 MB (41887658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfb779df7e1b2499166ec716ef889e30081e8aba48e6ebd2b7efb86fd3c1500`  
		Last Modified: Mon, 26 Jan 2026 22:04:56 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319759ba58a7e435647663ae7c2151227b34f95e7b64c4886ac02f49a63753f8`  
		Last Modified: Mon, 26 Jan 2026 22:04:56 GMT  
		Size: 2.3 KB (2287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:0005721e4b18821664606591cac5cf323d91f624af73cc7a0e46ae46f2f27bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a57fb0384ab130cded0c99be81c4a66a60e0d988dc7e00e462d90e94133cd69`

```dockerfile
```

-	Layers:
	-	`sha256:781003905c2da129bbf37846340f05d294dc261dc840e69605eb9f724319377b`  
		Last Modified: Mon, 26 Jan 2026 22:04:56 GMT  
		Size: 2.4 MB (2444480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4404fa35be5c6c73b3819798129a479069a579de3fa6d86dc8811b23728b26ec`  
		Last Modified: Mon, 26 Jan 2026 22:04:56 GMT  
		Size: 19.3 KB (19347 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u472-b08-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:113efab873ad522e5477acf4e04da6caf7e885bdde09bb8c896dc36c55f04335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109966256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07a5f7e5df23b6abdb773d54fedc15a09b15e0ba7db30b55db729aed7d9f7e80`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 04:47:00 GMT
ENV container oci
# Thu, 22 Jan 2026 04:47:00 GMT
COPY dir:5911db9f5450531429169fb3bc4d156204437f84bcda3e7b49af077219ecb148 in /      
# Thu, 22 Jan 2026 04:47:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 04:47:00 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T04:46:44Z" "org.opencontainers.image.created"="2026-01-22T04:46:44Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T04:46:44Z
# Mon, 26 Jan 2026 22:04:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 26 Jan 2026 22:04:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:04:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jan 2026 22:04:52 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:04:52 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Mon, 26 Jan 2026 22:04:56 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 26 Jan 2026 22:04:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 26 Jan 2026 22:04:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 26 Jan 2026 22:04:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:acd46633fecc5c7b908a52adf94f664d167c28dd5a89ed681fe958b1c58c6963`  
		Last Modified: Mon, 26 Jan 2026 05:26:49 GMT  
		Size: 38.2 MB (38223626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dc0e127a4d30cbdf4109784bd25cddb55a63d1cf24905b2bab1181165902e5`  
		Last Modified: Mon, 26 Jan 2026 22:05:09 GMT  
		Size: 30.9 MB (30860039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493779494ab1de2ad8aa94930d74f90e1048d083b0d617fca65cf04c255a0e1d`  
		Last Modified: Mon, 26 Jan 2026 22:05:09 GMT  
		Size: 40.9 MB (40880173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c569ea409376111d60bbb8e40e95a6388eed827d2003d50b3c58c5c690670a8f`  
		Last Modified: Mon, 26 Jan 2026 22:05:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6021c23f135bb6588cae69e3e5c280915e62787f925d8331a9c3da54d415832f`  
		Last Modified: Mon, 26 Jan 2026 22:04:58 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3d98891a2b636815e9e08abda24d8b44e6f0f861cea781da1fe2b3d75e0ed04f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a0849237911dc93294b2ed4e5ab92f28237a95ce70f6143423eb746ad305d6`

```dockerfile
```

-	Layers:
	-	`sha256:6910e050f940fc4de163e4270b06edeeb109abdc9793e1a5165f22c88ac5e575`  
		Last Modified: Mon, 26 Jan 2026 22:05:07 GMT  
		Size: 2.4 MB (2444528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40c093482889e2338669d078c8097a94aaff701707af660ac903e9ae1928c9c6`  
		Last Modified: Mon, 26 Jan 2026 22:05:07 GMT  
		Size: 19.4 KB (19450 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u472-b08-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:950639e11c4ccf78c4467be4bd3ffe2f2a24cb70d503d7bdc1310971f5bb27cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.6 MB (118629327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a8092949d9cf55da683bb7136537cef4c8a3efdb9b974879ea4af30c07cb84`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 01:08:41 GMT
ENV container oci
# Mon, 19 Jan 2026 01:08:42 GMT
COPY dir:3bd7ec6f425d769a16814adff3b957a15c4cbdec659c93cd45b1a546561564a3 in /      
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 01:08:42 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:fe8dfccf0fa987a5d4946f1b72ab0cc09a6e656396d24bdd16b87ea3307e9302 in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:fe8dfccf0fa987a5d4946f1b72ab0cc09a6e656396d24bdd16b87ea3307e9302 in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 01:08:43 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T01:08:31Z" "org.opencontainers.image.created"="2026-01-19T01:08:31Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T01:08:31Z
# Tue, 20 Jan 2026 19:12:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Jan 2026 19:12:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 19:12:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Jan 2026 19:12:37 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:12:37 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 20 Jan 2026 19:12:46 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 20 Jan 2026 19:12:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 20 Jan 2026 19:12:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Jan 2026 19:12:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:cb3df95d99fa30c8131b824671f0e15d0c34235a2e7bda21e4a361d100760346`  
		Last Modified: Mon, 19 Jan 2026 06:13:36 GMT  
		Size: 44.5 MB (44459713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c7d8e1a879073a2bb5883fd40b014f62a8e14ba675ff25067ab8b020299f7b`  
		Last Modified: Tue, 20 Jan 2026 19:13:32 GMT  
		Size: 32.9 MB (32898320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8122a0ad23073f42854e5b356cbfecb4237f1247a2709d40889670ad676285a`  
		Last Modified: Tue, 20 Jan 2026 19:13:32 GMT  
		Size: 41.3 MB (41268875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef62987b042714c89ac3ca3e795b8af531ad6f54cd74fa5b6b26366c3c6cb77`  
		Last Modified: Tue, 20 Jan 2026 19:13:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305ef587453b393cf17627d4cc31d3c8019d894762bf804ab3d21d1252b80186`  
		Last Modified: Tue, 20 Jan 2026 19:13:30 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c0c9c72c64634f45e3071a1aef63102b5f247c48cd27264719439b79f8d829eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfd49283d25e54bd46b30ea85ab2bc90574dbdd61d0b49b5b0ad987f0986cc6`

```dockerfile
```

-	Layers:
	-	`sha256:d98781578d95a5461a02fd8347ba22f309a76add2e5477e1d52c32d49e5c7236`  
		Last Modified: Tue, 20 Jan 2026 19:13:30 GMT  
		Size: 2.4 MB (2445171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1fb7312cc90c8e9c507a3332d5542ee0fdc6efc9b836115e6760adc2c35b1e5`  
		Last Modified: Tue, 20 Jan 2026 19:13:29 GMT  
		Size: 19.4 KB (19377 bytes)  
		MIME: application/vnd.in-toto+json
