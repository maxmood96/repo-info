## `eclipse-temurin:11-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:0d329483a50c1f259d4b5049bc20d7910493ad2858a9f6c8da505cd06588cb65
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

### `eclipse-temurin:11-jdk-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:167a40ed7a198a3c826717d4c4695cb94bc9952da90cfb6f9be1aeab29d5b5b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.2 MB (214244665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6990d56a55fd0f7bc4cda300b05a3cc435be021bf48df8bd8237f6f26dd0f617`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Feb 2026 04:55:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 04:55:05 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 04:55:05 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 04:55:05 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 04 Feb 2026 04:55:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 04:55:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 04 Feb 2026 04:55:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 04:55:06 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 04:55:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 04 Feb 2026 04:55:06 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 04:55:06 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 04 Feb 2026 04:55:06 GMT
ENV container oci
# Wed, 04 Feb 2026 04:55:06 GMT
COPY dir:ab88dbc5c421721056a4539f41aea4ce909f7032f536329269fb1718e0c3e67d in /      
# Wed, 04 Feb 2026 04:55:07 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 04:55:07 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 04:55:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 04:55:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 04:55:07 GMT
COPY file:6cb7b50636b55f291cf75a2750279d2c83bd2761ac9a492a49d90a49cb72e8ac in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 04:55:07 GMT
COPY file:6cb7b50636b55f291cf75a2750279d2c83bd2761ac9a492a49d90a49cb72e8ac in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 04:55:08 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "org.opencontainers.image.revision"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "build-date"="2026-02-04T04:54:43Z" "org.opencontainers.image.created"="2026-02-04T04:54:43Z" "release"="1770180557"org.opencontainers.image.revision=1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b,org.opencontainers.image.created=2026-02-04T04:54:43Z
# Thu, 05 Feb 2026 22:15:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:15:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:15:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:15:48 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:15:48 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Thu, 05 Feb 2026 22:15:54 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:15:55 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:15:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:15:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:15:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:819501e18c85a616b033a682e2078167e38cd15970dd3534932af6715532259f`  
		Last Modified: Wed, 04 Feb 2026 05:56:28 GMT  
		Size: 34.6 MB (34565108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85150ed97dd6604652ea3a5958e9a79e20e4be9b32d870055a72207c8307337d`  
		Last Modified: Thu, 05 Feb 2026 22:16:12 GMT  
		Size: 37.4 MB (37413852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ff06f4c8b5ba7199405fb0e8c29d5f5d761cfa0946909f2d58cc15590afa06`  
		Last Modified: Thu, 05 Feb 2026 22:16:14 GMT  
		Size: 142.3 MB (142263284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655d33caf849e5ada5ac965b06457cc9e089338a6cdc72653278dc5ca997a3fa`  
		Last Modified: Thu, 05 Feb 2026 22:16:10 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e907ac62616d876a70f69b6056ccea65b99aaec92d94de513bf1bacbaf8dffe`  
		Last Modified: Thu, 05 Feb 2026 22:16:10 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9fbb935d8bb473f707abc70f8864deb59a96fb70e960ac5500961027c7665f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3830595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83c6edb331339e605df81af130d5a4e85e2db43d73907471c7a420f4a5b8b63`

```dockerfile
```

-	Layers:
	-	`sha256:1f01e20febabb11a543e0e4285009ad2a7272dffd13be320e35d6fbf22cecb35`  
		Last Modified: Thu, 05 Feb 2026 22:16:10 GMT  
		Size: 3.8 MB (3809279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4bec8f6d9f8c6bf1364389d9b7813954cb44b8ac9b11ced9b1585394247f91a`  
		Last Modified: Thu, 05 Feb 2026 22:16:10 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:551defa5ec86ba9af241a280ffac8db23be1bc2eb4441cc5b4ac1257946298bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.0 MB (208984850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9d6c1d4623d7405577b38ab06c6d229639abc4627a41ab2d1e0a2dea6b6d5b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 04 Feb 2026 04:56:41 GMT
ENV container oci
# Wed, 04 Feb 2026 04:56:42 GMT
COPY dir:67028d43c1066b84b1209232f64f1a4cc4b9dbbfba57178bd9cbb9c32d30e9e7 in /      
# Wed, 04 Feb 2026 04:56:42 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 04:56:42 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 04:56:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 04:56:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 04:56:42 GMT
COPY file:6daaa71ff7be172f731620b1d0190bb9c2177930f1dd64e2221f2ce09f100fc6 in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 04:56:42 GMT
COPY file:6daaa71ff7be172f731620b1d0190bb9c2177930f1dd64e2221f2ce09f100fc6 in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 04:56:43 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "org.opencontainers.image.revision"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "build-date"="2026-02-04T04:56:21Z" "org.opencontainers.image.created"="2026-02-04T04:56:21Z" "release"="1770180557"org.opencontainers.image.revision=1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b,org.opencontainers.image.created=2026-02-04T04:56:21Z
# Thu, 05 Feb 2026 22:14:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:14:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:14:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:14:45 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:14:45 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Thu, 05 Feb 2026 22:14:51 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:14:52 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:14:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:14:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:14:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e7aaef72f9aac8066ddd0c18bcd7c76fcc63212a965d38f195e0959c666aa7ce`  
		Last Modified: Wed, 04 Feb 2026 06:11:32 GMT  
		Size: 32.7 MB (32661097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b34728643edc921b0204e06802629c1d40f8a832e96eb1cf25405cd45704a4e`  
		Last Modified: Thu, 05 Feb 2026 22:15:11 GMT  
		Size: 37.4 MB (37361596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eada56a54c3b9ed4db55a65b76da261dc06b7573320ce01209e6b2fe1f0073f6`  
		Last Modified: Thu, 05 Feb 2026 22:15:13 GMT  
		Size: 139.0 MB (138959737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4777e76f129294f2baf65661335de01b6fcde7d74c1867f2f467a956074e7d`  
		Last Modified: Thu, 05 Feb 2026 22:15:09 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30c6c00750ab9ced8aab0f30dabd3d6f404fdbaa4e5ea22c186a725a22b95a1`  
		Last Modified: Thu, 05 Feb 2026 22:15:09 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4534d406ad60941754f0b2d61a3d8f86e26db91a8abaa367e910c28e6ce3a379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3830755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e665575585f1624e5ee9b699da0b1c7157b91573902b236f03d4b2155fbf29`

```dockerfile
```

-	Layers:
	-	`sha256:7aaee0a27b4fb065fb8e1b883bd7e71040becef7c3c5d5f2ca29c9208be7102e`  
		Last Modified: Thu, 05 Feb 2026 22:15:09 GMT  
		Size: 3.8 MB (3809323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84a501d937ffc14bbec2db6cab9e338787df3f0ca84a8e93bad7b0303a208bab`  
		Last Modified: Thu, 05 Feb 2026 22:15:09 GMT  
		Size: 21.4 KB (21432 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:d5a0054b505f70506ee1caa327f21655f5a02b60cebcafba54fa2a517abd5d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.4 MB (207363410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb79235f6106a2d5091906a4ebdc65c699b61e4add8fb46a6852bb45e6a59c43`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 04 Feb 2026 04:58:36 GMT
ENV container oci
# Wed, 04 Feb 2026 04:58:37 GMT
COPY dir:09fdad4b579363b2c8418a42c62ea4dc38d67115c8d53cd4a2ec14253ecaf9ad in /      
# Wed, 04 Feb 2026 04:58:37 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 04:58:37 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 04:58:37 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 04:58:37 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 04:58:37 GMT
COPY file:0c67174697cfbd406f6852cad47660b65db0ae88b3ec344fd5c165877edf759b in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 04:58:37 GMT
COPY file:0c67174697cfbd406f6852cad47660b65db0ae88b3ec344fd5c165877edf759b in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 04:58:38 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "org.opencontainers.image.revision"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "build-date"="2026-02-04T04:58:25Z" "org.opencontainers.image.created"="2026-02-04T04:58:25Z" "release"="1770180557"org.opencontainers.image.revision=1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b,org.opencontainers.image.created=2026-02-04T04:58:25Z
# Thu, 05 Feb 2026 01:21:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 01:21:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 01:21:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 01:21:18 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 01:21:18 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Thu, 05 Feb 2026 22:19:42 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:19:46 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:19:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:19:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:19:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1cff691ae927c200ee804ea0243a79390de10e4d7f5f6687bde708134b9917c4`  
		Last Modified: Wed, 04 Feb 2026 06:11:59 GMT  
		Size: 38.7 MB (38689551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907a9332059e30e789362eb783b19695b44bab5a28726fe9fd59ec73d342defd`  
		Last Modified: Thu, 05 Feb 2026 01:22:04 GMT  
		Size: 39.2 MB (39172221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88d40278617ffd2a86716374e873bba2eab8ab8289bbda445e8f03d3eb63a05`  
		Last Modified: Thu, 05 Feb 2026 22:20:25 GMT  
		Size: 129.5 MB (129499219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c273c950551388a544282c01314cc5798e70cdd0a4770bf832cb01f4d6d8ef40`  
		Last Modified: Thu, 05 Feb 2026 22:20:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfbd86a8d9fb1c6cb3d5d1a3944c1b58cc548b277d44cc2f1f19afbcd506955`  
		Last Modified: Thu, 05 Feb 2026 22:20:02 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c278f7da6485e336bf06b79f3192e9f01c0783996dc9d28e997fa8470d43f208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3816848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c2b11a46455f9252cf545ccdaa8e3c554e4e8edaebc9a00bb817b5fe6f5979`

```dockerfile
```

-	Layers:
	-	`sha256:008a358194c7b846c79d03e0844441a5e3f9b2b9d770ade9f4f88a4f51a85305`  
		Last Modified: Thu, 05 Feb 2026 22:20:22 GMT  
		Size: 3.8 MB (3795496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:926e041ac6639abeac4d0a3c854dfd5246b6acd159b5610816ad24c6f939407a`  
		Last Modified: Thu, 05 Feb 2026 22:20:21 GMT  
		Size: 21.4 KB (21352 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:6d9937263d15f064addf1c48d5a0e173e907685273855725a9fb0141a4f571aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.2 MB (195169270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7145a1472b8c413a30d672e3e6730c2357aecf5e4e337f8ad6526b9b564c77fa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 04 Feb 2026 05:11:29 GMT
ENV container oci
# Wed, 04 Feb 2026 05:11:30 GMT
COPY dir:9d4ac575a92f53870377be4b68b1588c9bc427ee283102569774f3d9158a16f9 in /      
# Wed, 04 Feb 2026 05:11:30 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 05:11:30 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 05:11:30 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 05:11:30 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 05:11:30 GMT
COPY file:bd2f18d5b9d97db31e1a3f98a0670c0f15ee13ca2c036700589166ed0ad3221a in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 05:11:30 GMT
COPY file:bd2f18d5b9d97db31e1a3f98a0670c0f15ee13ca2c036700589166ed0ad3221a in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 05:11:30 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "org.opencontainers.image.revision"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "build-date"="2026-02-04T05:09:09Z" "org.opencontainers.image.created"="2026-02-04T05:09:09Z" "release"="1770180557"org.opencontainers.image.revision=1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b,org.opencontainers.image.created=2026-02-04T05:09:09Z
# Thu, 05 Feb 2026 00:08:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 00:08:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:08:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 00:08:00 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:08:00 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Thu, 05 Feb 2026 22:15:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:15:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:15:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:15:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:15:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c5e6ba1d838b1d4e103e0457068eaff01f71c8436e4442eaa2f5c701ccbe1c6`  
		Last Modified: Wed, 04 Feb 2026 06:11:43 GMT  
		Size: 34.4 MB (34399700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f62941b4842166327c9c075b3f2cabd375978482a43694cc3006f9826a62ce`  
		Last Modified: Thu, 05 Feb 2026 00:08:22 GMT  
		Size: 37.8 MB (37794446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bccef20ee245977857c7a44344ab7d25507b43196c60baaf20ea2ac8331f27a7`  
		Last Modified: Thu, 05 Feb 2026 22:16:20 GMT  
		Size: 123.0 MB (122972704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a053eed203a4ad71f68a7b4f64f7c301c88cc5634f8dcef829bd7898ff6230`  
		Last Modified: Thu, 05 Feb 2026 22:16:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50f48009bf0e8e4dde821a2103bb2a5aa7b7da1fc974492e2e914ddc0ca0a15`  
		Last Modified: Thu, 05 Feb 2026 22:16:16 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:82920bff221d4213575158fd95e1d454859cf49dc11f68c7cd37a3113c431835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3816189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13185e97cfbd8f259b48b8824e627309b8b8ff8d5bf1bd808722ef1d2c54fe15`

```dockerfile
```

-	Layers:
	-	`sha256:2b4a372d6c806e0211d8184a75cdb87190967fb3564b7d18e191181e57226f1c`  
		Last Modified: Thu, 05 Feb 2026 22:16:17 GMT  
		Size: 3.8 MB (3794873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2ef0af3a5dfaa279fffbe0a13424117b84a0cbc7f6a016954f7d31ff30caf8f`  
		Last Modified: Thu, 05 Feb 2026 22:16:16 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json
