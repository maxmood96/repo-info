## `eclipse-temurin:8-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:1ff0248fd1f55ddb87671fce94e83355657f5bf902199ed8b208313da2aaf4a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:21033f3cf50f9c0a69eec252c2ff8f5b7acfca77c59ab5b7a48559b616b14806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114404011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b605ef008fc5272325e6dd6347a67550e27d1d78c3460ca1463c57812e975e2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
# Mon, 23 Mar 2026 18:16:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 23 Mar 2026 18:16:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:16:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 23 Mar 2026 18:16:47 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 23 Mar 2026 18:16:47 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Mon, 23 Mar 2026 18:16:50 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='46496dfa7e58784adf96a3a2bd1ac8be9fda2d8749a9c52bf74fb582aa1449e2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='b563c5c90dcff0c1cf5a1bdc3110e560c979254a17e696902e922631264cf342';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='01672ca52509f4cb1ffa8aed905808fed7b984f3e279cb13d90a6e865ff6199f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 23 Mar 2026 18:16:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 23 Mar 2026 18:16:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 23 Mar 2026 18:16:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:2979ea27473f21e894361ff5d915252c378d4a8073aca3908465bbbf348780b7`  
		Last Modified: Mon, 23 Mar 2026 03:10:44 GMT  
		Size: 34.6 MB (34630234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13751a904eb1f9d520c447cbb9396dfb2e1ad527ab9cd360883cf251e5f4665d`  
		Last Modified: Mon, 23 Mar 2026 18:17:04 GMT  
		Size: 37.4 MB (37446646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4fa31578e5b38059f5f2ceb311089734ec910a93c22e1c3fdc4ce46f0f0ebf`  
		Last Modified: Mon, 23 Mar 2026 18:17:04 GMT  
		Size: 42.3 MB (42324713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b866d7a01b49556254244d3b588ae093f49696d32e1c0e89bfbb3b6322a85f7d`  
		Last Modified: Mon, 23 Mar 2026 18:17:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd365e0df4d8774714aa7b0045879c833e4bec2fb8b9da3a7f32a7d508ac776`  
		Last Modified: Mon, 23 Mar 2026 18:17:03 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e9630e9886c421311dc60652ee422645c407031715dbb87b26eac20ba9245c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d970fd31b16668380b4e5961ad0792ba6d6d81b1f1a39d86d96178ee4412ad`

```dockerfile
```

-	Layers:
	-	`sha256:6262886ccde17ef28c2f140c5f194b0a80f6cbb8f7604162aff6a76431758b5a`  
		Last Modified: Mon, 23 Mar 2026 18:17:02 GMT  
		Size: 3.7 MB (3734774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9062037b4644fef432e941e0dc17173be1eae9a486b8b65282f5de32f5af1f11`  
		Last Modified: Mon, 23 Mar 2026 18:17:01 GMT  
		Size: 19.5 KB (19510 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:8c5ce2c2d7b9ad30a510b1c6dc74b8fa98f22a6dd1909bd5f61223af93469116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111366473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e29d245582e0a8b063779505a5e244058bbc0a6ba6325f4687867bed33dc2a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
# Mon, 23 Mar 2026 18:16:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 23 Mar 2026 18:16:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:16:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 23 Mar 2026 18:16:29 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 23 Mar 2026 18:16:29 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Mon, 23 Mar 2026 18:16:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='46496dfa7e58784adf96a3a2bd1ac8be9fda2d8749a9c52bf74fb582aa1449e2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='b563c5c90dcff0c1cf5a1bdc3110e560c979254a17e696902e922631264cf342';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='01672ca52509f4cb1ffa8aed905808fed7b984f3e279cb13d90a6e865ff6199f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 23 Mar 2026 18:16:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 23 Mar 2026 18:16:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 23 Mar 2026 18:16:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:cbfdca2ca63ac63914141abb4cb933134b748fc3efb6e835daea267d6feb9296`  
		Last Modified: Mon, 23 Mar 2026 03:33:50 GMT  
		Size: 32.7 MB (32686471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3691a9c5a94416f1e4a51fe083e475312a8e13ed268e2cec6057a5628b840ab6`  
		Last Modified: Mon, 23 Mar 2026 18:16:47 GMT  
		Size: 37.4 MB (37389027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8eab3e102113eff34391b216d3431eb9d347f213b9332f6267bd8337e9edaf`  
		Last Modified: Mon, 23 Mar 2026 18:16:48 GMT  
		Size: 41.3 MB (41288558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d53ce660d5ad06f4ea25c49bee7d9c678f5bf2e9b26dca1a4197fb2359c234`  
		Last Modified: Mon, 23 Mar 2026 18:16:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4463149f16091b8cab57d501ca558ed68ba00a7f4b46f51bf7de9fe4cec068b9`  
		Last Modified: Mon, 23 Mar 2026 18:16:47 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9c46ebcd93cef83e876bb478d067cc4a9c816b13865139273756bd1d882d1998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b545f726b71d4667d701a5a8e09eb8aa78ec1a17fbb0294ae907ffcca420be`

```dockerfile
```

-	Layers:
	-	`sha256:42495fa02614b7a38737b37bf99f4129e1fe837d4277f7818b45c8a8f07c11ef`  
		Last Modified: Mon, 23 Mar 2026 18:16:45 GMT  
		Size: 3.7 MB (3734880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7a1c93d9996ed4fa29f5ee75dd894e8e46a82a34ace455e003fcba2c70b76b1`  
		Last Modified: Mon, 23 Mar 2026 18:16:45 GMT  
		Size: 19.6 KB (19615 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:458a5c2917ab283df8057c7b787fd0d99f8c11750c32d87ead263d1d8ea59faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.7 MB (119651791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ca996edcc45c76253027372e75f6b523083c309f41d1b0faf46c91b7ffd598`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
ENV JAVA_VERSION=jdk8u482-b08
# Mon, 23 Mar 2026 18:25:14 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='46496dfa7e58784adf96a3a2bd1ac8be9fda2d8749a9c52bf74fb582aa1449e2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='b563c5c90dcff0c1cf5a1bdc3110e560c979254a17e696902e922631264cf342';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='01672ca52509f4cb1ffa8aed905808fed7b984f3e279cb13d90a6e865ff6199f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 23 Mar 2026 18:25:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 23 Mar 2026 18:25:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 23 Mar 2026 18:25:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:631b41cd0dd87264de46f9acf42044c9b8dfe89d4b9d74536700c5defe8879b0`  
		Last Modified: Mon, 23 Mar 2026 18:25:46 GMT  
		Size: 41.7 MB (41721835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f73ab06a025331a9208835f5a17873c88e724b934f3056a01ee94805f3c989c`  
		Last Modified: Mon, 23 Mar 2026 18:25:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931286e04340d3b29a1dfc6bdc44d00140f383180cc471603f4131c43ed6a9ae`  
		Last Modified: Mon, 23 Mar 2026 18:25:45 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a3f079a8b3980ac7ec2a8c73544e9a580b13090ed452ac1ae94147067b94ed2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89a255cd5b3445a70653a4b058b02233cd472cdd10071e48b8a93613c3ad196`

```dockerfile
```

-	Layers:
	-	`sha256:fad24a7f0a17148e4a46ae52d137d8426e60560fbc4e7c15754e856f2c30db25`  
		Last Modified: Mon, 23 Mar 2026 18:25:44 GMT  
		Size: 3.7 MB (3724211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89474faf20e90277db69a8cdf8365f7027c501a5785d0ea6ff62e7134b520783`  
		Last Modified: Mon, 23 Mar 2026 18:25:43 GMT  
		Size: 19.5 KB (19541 bytes)  
		MIME: application/vnd.in-toto+json
