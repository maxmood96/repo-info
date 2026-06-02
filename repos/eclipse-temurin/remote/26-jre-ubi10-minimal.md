## `eclipse-temurin:26-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:81d873c7e3f0fea2cffe984da046abc03de9618a474bca6432eddece74203165
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

### `eclipse-temurin:26-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:6cd987b85c6ece46f2313d94292bbf80e7358da3c96c1f29a9121f47a329bd5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137024407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b0401f6851ce0d84d9b8bc023fc51d62384ad22e9a0b3eff9d4f11f17619c3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 15:15:58 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 02 Jun 2026 15:15:58 GMT
ENV container oci
# Tue, 02 Jun 2026 15:15:58 GMT
COPY dir:e8b072881a1b1351c3b2d1bd84c8a6d6b28cb6b00007243c1b82e61134e4db04 in /      
# Tue, 02 Jun 2026 15:15:58 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 15:15:58 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 15:15:59 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 15:15:59 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 15:15:59 GMT
COPY file:5abe2f7df4c217a707574e953fc9f76f54f8de027108bd9480e64819343fa499 in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 15:15:59 GMT
COPY file:5abe2f7df4c217a707574e953fc9f76f54f8de027108bd9480e64819343fa499 in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 15:15:59 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="2c7c4b29450f25f9bc18401f2298edead75bcd9f" "org.opencontainers.image.revision"="2c7c4b29450f25f9bc18401f2298edead75bcd9f" "build-date"="2026-06-02T15:15:44Z" "org.opencontainers.image.created"="2026-06-02T15:15:44Z" "release"="1780413072"org.opencontainers.image.revision=2c7c4b29450f25f9bc18401f2298edead75bcd9f,org.opencontainers.image.created=2026-06-02T15:15:44Z
# Tue, 02 Jun 2026 22:45:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 22:45:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:45:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 22:45:25 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:45:25 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Tue, 02 Jun 2026 22:45:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='bf5f733066599065de5e720edda550b39d85876f5bf23a94fee2cb6a8379cb36';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='d8f66903603c3661c0d8c03de41b76459260ed2e295ba874bb7b3f37a012c026';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='3c68d7df7d64a7738a6bd97b12fb2167774666d87bf9a309094bb2180073eb38';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='2e90cf68d31b28553fb2c8202d5a4c3a5e99a60285e125dc28c94ba5fb2ac1ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 02 Jun 2026 22:45:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:45:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:45:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e4e3984c47d80f8f7813d099ea4505637390207a530acceb3e7426232f7555a`  
		Last Modified: Tue, 02 Jun 2026 16:41:21 GMT  
		Size: 34.8 MB (34839018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2975517b72e6028da481cbc77bf8f234971d3661f5cb3ed69c4db05e8f9f5d24`  
		Last Modified: Tue, 02 Jun 2026 22:45:43 GMT  
		Size: 37.8 MB (37750298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fc76d77cb1ded47f5e143cde75c014108c19dc828d95bb10a0a500c3a5df9e`  
		Last Modified: Tue, 02 Jun 2026 22:46:13 GMT  
		Size: 64.4 MB (64432494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90cb1611ba0598b3d1fe4bf6139f2869fa10707d7afda19dfc615e9fc06cc6af`  
		Last Modified: Tue, 02 Jun 2026 22:46:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b1cb1f4c6bde7cccdca9a3c478a80c516ebab129ea633f0a39fc8a60e56f5e`  
		Last Modified: Tue, 02 Jun 2026 22:46:12 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2105c823313e07ad7443198faf73a41576993dfeec66d0efc269f2298fc164f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3733873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d61ab0d236eae8ab8bab25e54dbde7382fb28a324df4f597d9aed208c966782`

```dockerfile
```

-	Layers:
	-	`sha256:846c62cdd7bea89690864217685c71d3ee781dca174c086557d9f1183c929c38`  
		Last Modified: Tue, 02 Jun 2026 22:46:12 GMT  
		Size: 3.7 MB (3713543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6406f9cadb7b02d9151ec58aeec93744dcab3ae7f709dd16c9573d331048e6f3`  
		Last Modified: Tue, 02 Jun 2026 22:46:12 GMT  
		Size: 20.3 KB (20330 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:7291a9b04d1d5fe2a6c842a39c3a5a32478ba54e0a104a0043918380dc081c58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134064633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a7d2c9e842c6864130e898cce41dd2f95bcbc65f86676681bc581b3eff446f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 15:18:30 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 02 Jun 2026 15:18:30 GMT
ENV container oci
# Tue, 02 Jun 2026 15:18:31 GMT
COPY dir:a6b2b21a8909319c9461e822bff140e3ef1b61d198a2f277660b14bd1d6a271f in /      
# Tue, 02 Jun 2026 15:18:31 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 15:18:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 15:18:31 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 15:18:31 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 15:18:31 GMT
COPY file:cdd42785ebb0fd2c525ecf4a97b6b97bf781caa3b4c77f748f3d95a5a6d4bb88 in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 15:18:31 GMT
COPY file:cdd42785ebb0fd2c525ecf4a97b6b97bf781caa3b4c77f748f3d95a5a6d4bb88 in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 15:18:31 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="2c7c4b29450f25f9bc18401f2298edead75bcd9f" "org.opencontainers.image.revision"="2c7c4b29450f25f9bc18401f2298edead75bcd9f" "build-date"="2026-06-02T15:18:13Z" "org.opencontainers.image.created"="2026-06-02T15:18:13Z" "release"="1780413072"org.opencontainers.image.revision=2c7c4b29450f25f9bc18401f2298edead75bcd9f,org.opencontainers.image.created=2026-06-02T15:18:13Z
# Tue, 02 Jun 2026 22:45:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 22:45:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:45:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 22:45:23 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:45:23 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Tue, 02 Jun 2026 22:45:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='bf5f733066599065de5e720edda550b39d85876f5bf23a94fee2cb6a8379cb36';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='d8f66903603c3661c0d8c03de41b76459260ed2e295ba874bb7b3f37a012c026';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='3c68d7df7d64a7738a6bd97b12fb2167774666d87bf9a309094bb2180073eb38';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='2e90cf68d31b28553fb2c8202d5a4c3a5e99a60285e125dc28c94ba5fb2ac1ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 02 Jun 2026 22:45:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:45:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:45:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:7cd594d4c3afe0f66eb7cfc2a31b3e461f371776f986ab3d5084853335f5d2f7`  
		Last Modified: Tue, 02 Jun 2026 16:41:21 GMT  
		Size: 33.0 MB (33037428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c03324e05b78acf7ccd5dc6bb4f74eb5ec3b875b0dda24b9fad322b1193319`  
		Last Modified: Tue, 02 Jun 2026 22:45:45 GMT  
		Size: 37.7 MB (37683275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd76e33364c8432a2aaa40f4963f4134d6858d440b668b7cb2afc79bb8a0af23`  
		Last Modified: Tue, 02 Jun 2026 22:45:46 GMT  
		Size: 63.3 MB (63341333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce0a750a29ce744842eb08bd3107cbad5933e5b68f421ddcdd05891e58b977d`  
		Last Modified: Tue, 02 Jun 2026 22:45:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94272611401a6525f6e53316f33a384c857bd92022e23714b916c3cb3e00569`  
		Last Modified: Tue, 02 Jun 2026 22:45:43 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:266659bcd8d81c4c4abe80d6c57096267be064e716f8db76e22cc666672f28a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3733388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bf9f2714486682f172a42056d00ac55b61079673e8a1510ef0923f96ed8b84`

```dockerfile
```

-	Layers:
	-	`sha256:ff6b8ced5c1939ebea4d495f2bbcbc9680282279d15cbaca92a5a39f56f93e49`  
		Last Modified: Tue, 02 Jun 2026 22:45:43 GMT  
		Size: 3.7 MB (3712954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:030e39ff8550af9374083d2c3e6eabd296d89a6ed810504c9033c3ae7f856f25`  
		Last Modified: Tue, 02 Jun 2026 22:45:43 GMT  
		Size: 20.4 KB (20434 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:9e2948ea60a279b30928dff547ff2c309bb915e374fe6bc8be3fb5fa5d71afbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142343207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdb030bb0c7cbd668f5a4e5045d12ce4ef4bca8af4091e7192aec66d85cd350`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 02 Jun 2026 15:17:18 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 15:17:19 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 15:17:19 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 15:17:19 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Tue, 02 Jun 2026 15:17:19 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 15:17:19 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 02 Jun 2026 15:17:19 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 15:17:19 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 15:17:19 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 02 Jun 2026 15:17:19 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 15:17:19 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 02 Jun 2026 15:17:19 GMT
ENV container oci
# Tue, 02 Jun 2026 15:17:19 GMT
COPY dir:92bfd12864edc92997d2d256b8a65c081538f9c2759c99ccd4aa8bcb0106a753 in /      
# Tue, 02 Jun 2026 15:17:19 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 15:17:19 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 15:17:19 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 15:17:19 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 15:17:20 GMT
COPY file:f48578db79ab4a61ea5f93f3a6d877bb461214fcd6d5322e90176aee654cbaf2 in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 15:17:20 GMT
COPY file:f48578db79ab4a61ea5f93f3a6d877bb461214fcd6d5322e90176aee654cbaf2 in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 15:17:20 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="2c7c4b29450f25f9bc18401f2298edead75bcd9f" "org.opencontainers.image.revision"="2c7c4b29450f25f9bc18401f2298edead75bcd9f" "build-date"="2026-06-02T15:17:07Z" "org.opencontainers.image.created"="2026-06-02T15:17:07Z" "release"="1780413072"org.opencontainers.image.revision=2c7c4b29450f25f9bc18401f2298edead75bcd9f,org.opencontainers.image.created=2026-06-02T15:17:07Z
# Tue, 02 Jun 2026 22:43:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 22:43:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:43:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 22:43:53 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:43:53 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Tue, 02 Jun 2026 22:58:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='bf5f733066599065de5e720edda550b39d85876f5bf23a94fee2cb6a8379cb36';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='d8f66903603c3661c0d8c03de41b76459260ed2e295ba874bb7b3f37a012c026';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='3c68d7df7d64a7738a6bd97b12fb2167774666d87bf9a309094bb2180073eb38';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='2e90cf68d31b28553fb2c8202d5a4c3a5e99a60285e125dc28c94ba5fb2ac1ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 02 Jun 2026 22:58:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:58:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:58:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f64094e3e3609aa276182d8f78ae91793a4e608c47e7c897b908d4be321f6cb0`  
		Last Modified: Tue, 02 Jun 2026 18:16:23 GMT  
		Size: 39.0 MB (38987518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00a1dda8ba613ae060b67cb1cf9258bbca5962547117c49bc7811034334ada2`  
		Last Modified: Tue, 02 Jun 2026 22:45:02 GMT  
		Size: 39.5 MB (39504910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e04bd917bf2ee98727f34abf7849ceaf71ac3cbaa6b9361dc14500cc0d7e62`  
		Last Modified: Tue, 02 Jun 2026 22:58:51 GMT  
		Size: 63.8 MB (63848181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31605dbae709dcfd3e67a371a54ce20fe9dc23c3473b453a8705c316b00d0b6d`  
		Last Modified: Tue, 02 Jun 2026 22:58:49 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb29d869e51b2ffa7e54bb9dddbb2e9dd63416c98c9de41767791e4dc560f3d`  
		Last Modified: Tue, 02 Jun 2026 22:58:49 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e580cf9ca3e846fb39219ed25470bee976f1408ddac2ad3fc308306bce92b721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c41dc1542e7876d509b79194e4411cf57661c688f4a87203ab32a55ea074ce`

```dockerfile
```

-	Layers:
	-	`sha256:686a961ed923be49d9205bce80847e5a071eeeb8e7958b11fb8805037c198f42`  
		Last Modified: Tue, 02 Jun 2026 22:58:50 GMT  
		Size: 3.7 MB (3701667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1faf1459575f1efcd2abdb62be5e5877f0e293a23c3d994d4dd67a8fd0e17e6`  
		Last Modified: Tue, 02 Jun 2026 22:58:49 GMT  
		Size: 20.4 KB (20360 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26-jre-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:fa9edcb52cd95ebcdc60308babfb8729c6c34a074159bb580069435de5837e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134899230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f7b274e922ca4cc58bd490f000bb9082ad8b2cfe312466b351a5c7fbf8157a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 02 Jun 2026 15:29:16 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 15:29:16 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 15:29:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 15:29:16 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Tue, 02 Jun 2026 15:29:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 15:29:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 02 Jun 2026 15:29:16 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 15:29:16 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 15:29:16 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 02 Jun 2026 15:29:16 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 15:29:16 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 02 Jun 2026 15:29:16 GMT
ENV container oci
# Tue, 02 Jun 2026 15:29:16 GMT
COPY dir:0c85a1abf7afc52ab998b8b8163fb831aa7ce562a422231078f409e5a4c9ad75 in /      
# Tue, 02 Jun 2026 15:29:17 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 15:29:17 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 15:29:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 15:29:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 15:29:17 GMT
COPY file:e5fe3ee200e15ec67ab7a7520095c861775728fb94fefa880b9793f6fa30b055 in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 15:29:17 GMT
COPY file:e5fe3ee200e15ec67ab7a7520095c861775728fb94fefa880b9793f6fa30b055 in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 15:29:17 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="2c7c4b29450f25f9bc18401f2298edead75bcd9f" "org.opencontainers.image.revision"="2c7c4b29450f25f9bc18401f2298edead75bcd9f" "build-date"="2026-06-02T15:28:33Z" "org.opencontainers.image.created"="2026-06-02T15:28:33Z" "release"="1780413072"org.opencontainers.image.revision=2c7c4b29450f25f9bc18401f2298edead75bcd9f,org.opencontainers.image.created=2026-06-02T15:28:33Z
# Tue, 02 Jun 2026 22:43:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 22:43:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:43:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 22:43:22 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:43:22 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Tue, 02 Jun 2026 22:46:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='bf5f733066599065de5e720edda550b39d85876f5bf23a94fee2cb6a8379cb36';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='d8f66903603c3661c0d8c03de41b76459260ed2e295ba874bb7b3f37a012c026';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='3c68d7df7d64a7738a6bd97b12fb2167774666d87bf9a309094bb2180073eb38';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='2e90cf68d31b28553fb2c8202d5a4c3a5e99a60285e125dc28c94ba5fb2ac1ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 02 Jun 2026 22:46:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:46:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:46:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:017341eabcfbc3839e70d99b30c5183e8f03952ba5046a4c9b68b4eff2e3021c`  
		Last Modified: Tue, 02 Jun 2026 18:16:12 GMT  
		Size: 34.7 MB (34725456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417044ca2f6543b9160985c20866f1deb0bef3f87c00530b497b3a661f0eb8d3`  
		Last Modified: Tue, 02 Jun 2026 22:43:48 GMT  
		Size: 38.1 MB (38121308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c52bfa67a892c820c7a59315b9f90bfdae797f6d2ed7f1d6a7a18d642356046`  
		Last Modified: Tue, 02 Jun 2026 22:46:50 GMT  
		Size: 62.0 MB (62049868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4ab35fd90fc748f8809558d4d2307b54eb1af16f99344dc148151ac19307b3`  
		Last Modified: Tue, 02 Jun 2026 22:46:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4680f66498c18499bba0cd5ec1dddb800fae566219d2ab12652d0298275386d`  
		Last Modified: Tue, 02 Jun 2026 22:46:49 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:53e5c0a84c8344da7e7b9b91a0b529346b392355d8a692d85a44b9003be75fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3723242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab644d0dffa16e852cdfce81b5c2f755b3b2949030f8577440100ce5f914e8e`

```dockerfile
```

-	Layers:
	-	`sha256:73d67b91feb3b244f5b98099f82fc0025a3981245cf15e8028964afed2c29fac`  
		Last Modified: Tue, 02 Jun 2026 22:46:49 GMT  
		Size: 3.7 MB (3702912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a43c53649b1c4b8dcccb8bd2ff54e24f750bd3daa806826599b816e0fb3c977`  
		Last Modified: Tue, 02 Jun 2026 22:46:49 GMT  
		Size: 20.3 KB (20330 bytes)  
		MIME: application/vnd.in-toto+json
