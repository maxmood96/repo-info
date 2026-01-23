## `eclipse-temurin:11-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:f4bf887834316f955fb3d3a857156b2677b830c8810ca78e1665ecd79bc834d4
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

### `eclipse-temurin:11-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:a4413351e282265e8c26cfc3a613106b14933ebcc78c337d4c6767235aec4b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115795021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:758617474b73cc359e8cf5d33e8bb0c744a04218cf2eb9b7cf4977e8158d75ed`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 22 Jan 2026 14:19:49 GMT
ENV container oci
# Thu, 22 Jan 2026 14:19:50 GMT
COPY dir:4f39f7f54b1623f2373491e5bcb10b3c35efaa04126f246c1c0ae784bb3d7f42 in /      
# Thu, 22 Jan 2026 14:19:50 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 14:19:50 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 14:19:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 14:19:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 14:19:50 GMT
COPY file:e86693423cdd34ed7ac6eb4c5f916f086a37eeca572019e4cfd639c87f98a6ae in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:19:50 GMT
COPY file:e86693423cdd34ed7ac6eb4c5f916f086a37eeca572019e4cfd639c87f98a6ae in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:19:51 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0912ab420a80f21132d8a5e29d19a23339176677" "org.opencontainers.image.revision"="0912ab420a80f21132d8a5e29d19a23339176677" "build-date"="2026-01-22T14:19:22Z" "org.opencontainers.image.created"="2026-01-22T14:19:22Z" "release"="1769090502"org.opencontainers.image.revision=0912ab420a80f21132d8a5e29d19a23339176677,org.opencontainers.image.created=2026-01-22T14:19:22Z
# Fri, 23 Jan 2026 00:59:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Jan 2026 00:59:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 00:59:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Jan 2026 00:59:59 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 23 Jan 2026 00:59:59 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Fri, 23 Jan 2026 01:00:28 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 23 Jan 2026 01:00:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 23 Jan 2026 01:00:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 23 Jan 2026 01:00:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d4f698c23e56c30d1371a123d48250f3a8dd3de24cc53c15e862c4210c331c2`  
		Last Modified: Thu, 22 Jan 2026 16:13:48 GMT  
		Size: 34.5 MB (34531934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e058e1cc867cf3feee7d101285b4bc634490d6809fa9fb43631dc7ab3dc368f`  
		Last Modified: Fri, 23 Jan 2026 01:00:16 GMT  
		Size: 37.4 MB (37368491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b25471c4c55fefd36d1b2dde68e436a2a6acf1156d5285456215522d19769d`  
		Last Modified: Fri, 23 Jan 2026 01:00:40 GMT  
		Size: 43.9 MB (43892176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0090d2690187ea0be18d330690ed4ef2acf2c57d4d2fd19f38f8f18cd151acd4`  
		Last Modified: Fri, 23 Jan 2026 01:00:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afddb813f4fc62a69ca341dada559f87821b81cf9263d9a84d7f6a5c5c733d56`  
		Last Modified: Fri, 23 Jan 2026 01:00:39 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:41391e0b033908f39ecf208e7fe6c260fb883c19f4498d9bcb2215e27e42a1db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8cac73ef619d672518f7d92081da8956ea284c7945c92b6d6441b876a60edc6`

```dockerfile
```

-	Layers:
	-	`sha256:fb288697f4cb8f8e87605cffeecd79290ba268a5f17ebbc55ebb14cc2aec7b27`  
		Last Modified: Fri, 23 Jan 2026 01:00:40 GMT  
		Size: 3.7 MB (3716459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e17db29b0efe627443fed1960c1bafe1b68452f83be59381bec2057f409d57d`  
		Last Modified: Fri, 23 Jan 2026 01:00:40 GMT  
		Size: 20.4 KB (20353 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:a3001390f06cc31f7cd8a73f8003fcddf4a906b25b8902aa3cff82a3c3d8133c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112164657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06d18cf3973b8b4cdc56b66cba668bb2444b5d4ea23d5013dd46c254c1b6791`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 22 Jan 2026 14:10:51 GMT
ENV container oci
# Thu, 22 Jan 2026 14:10:52 GMT
COPY dir:909d569786ad4226e9c77ee4fc4d27953d579517f60f8a0f25e4d85964a100a3 in /      
# Thu, 22 Jan 2026 14:10:52 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 14:10:52 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 14:10:52 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 14:10:52 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 14:10:52 GMT
COPY file:ea81599b2ebb991911687a996e9dca425fe171d768273735cf8dd2c299ff0d3d in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:10:52 GMT
COPY file:ea81599b2ebb991911687a996e9dca425fe171d768273735cf8dd2c299ff0d3d in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:10:52 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0912ab420a80f21132d8a5e29d19a23339176677" "org.opencontainers.image.revision"="0912ab420a80f21132d8a5e29d19a23339176677" "build-date"="2026-01-22T14:10:29Z" "org.opencontainers.image.created"="2026-01-22T14:10:29Z" "release"="1769090502"org.opencontainers.image.revision=0912ab420a80f21132d8a5e29d19a23339176677,org.opencontainers.image.created=2026-01-22T14:10:29Z
# Fri, 23 Jan 2026 00:58:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Jan 2026 00:58:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 00:58:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Jan 2026 00:58:23 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 23 Jan 2026 00:58:23 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Fri, 23 Jan 2026 00:58:55 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 23 Jan 2026 00:58:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 23 Jan 2026 00:58:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 23 Jan 2026 00:58:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:855d6cc175ead513a1945d3f0933680ee64146fa0bb48e8f15fcefa1fe9b0b14`  
		Last Modified: Thu, 22 Jan 2026 17:36:15 GMT  
		Size: 32.6 MB (32613686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac781c132d75e81cb50967739184f7c1157b403228369c655282bb8643ac784`  
		Last Modified: Fri, 23 Jan 2026 00:58:43 GMT  
		Size: 37.3 MB (37315606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38911275b8bddf09502cd0b824d1e73325fef502ad9f0bdb97e4b66249150afc`  
		Last Modified: Fri, 23 Jan 2026 00:59:08 GMT  
		Size: 42.2 MB (42232945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a743be246034b5808ee42b6bddece93795a5d6c8a541de88527798b8a627bb1d`  
		Last Modified: Fri, 23 Jan 2026 00:59:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab349c75f6fc8f5f731378c7166f22d807e1a7334cfa89824a01c6c9914d22b`  
		Last Modified: Fri, 23 Jan 2026 00:59:06 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f4dd67926d8f58f4f56935ff446f17b530189578e07395a1164140fdb5127998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28d8fd91f8708dfa9b1a8906f2687c7a7c1a7b7b9302c153c256b74e47f703f9`

```dockerfile
```

-	Layers:
	-	`sha256:744c88709f72715797a045a28148538ece94bc43df695de80e923a35765f0017`  
		Last Modified: Fri, 23 Jan 2026 00:59:07 GMT  
		Size: 3.7 MB (3716491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc789eee32d1ff6926e414f141c577b79c0901893584b8548a8310c6f02ace3d`  
		Last Modified: Fri, 23 Jan 2026 00:59:07 GMT  
		Size: 20.5 KB (20458 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:ef4bfe3a6bc63af30accef8aa0c529fb444daeaa1f2a337b25721451d5b939ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117187177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00667a80852880a9908ff64f92a0c3cef7a5dde5d43f0c418dc70bc7d3b48cd2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 22 Jan 2026 14:54:45 GMT
ENV container oci
# Thu, 22 Jan 2026 14:54:45 GMT
COPY dir:7bdbe74d43c251ef87ffde9a283489e444dd9e506bb8c01cd1c97a9f3ac52ddd in /      
# Thu, 22 Jan 2026 14:54:45 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 14:54:45 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 14:54:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 14:54:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 14:54:46 GMT
COPY file:fa7fed90e5fa59b018eb8aa0c4c26e4f0c5e15ab4b12ea84973f9ece212d9ed6 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:54:46 GMT
COPY file:fa7fed90e5fa59b018eb8aa0c4c26e4f0c5e15ab4b12ea84973f9ece212d9ed6 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:54:46 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="0912ab420a80f21132d8a5e29d19a23339176677" "org.opencontainers.image.revision"="0912ab420a80f21132d8a5e29d19a23339176677" "build-date"="2026-01-22T14:54:33Z" "org.opencontainers.image.created"="2026-01-22T14:54:33Z" "release"="1769090502"org.opencontainers.image.revision=0912ab420a80f21132d8a5e29d19a23339176677,org.opencontainers.image.created=2026-01-22T14:54:33Z
# Fri, 23 Jan 2026 00:57:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Jan 2026 00:57:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 00:57:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Jan 2026 00:57:54 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 23 Jan 2026 00:57:54 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Fri, 23 Jan 2026 00:59:12 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 23 Jan 2026 00:59:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 23 Jan 2026 00:59:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 23 Jan 2026 00:59:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:ca7d82d686e4448886b5d40d7ede2a94863423d05f007fae2fdf719fb557a51e`  
		Last Modified: Thu, 22 Jan 2026 18:12:54 GMT  
		Size: 38.7 MB (38718444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83cbc42d47e675c60991c0dfbc843db7691ef4e8247a33f719b14ab372f6ea2`  
		Last Modified: Fri, 23 Jan 2026 00:58:44 GMT  
		Size: 39.1 MB (39124637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7d3019542383bd88c67b3228b07a16a587761b8faca17865b2989bd0e9fecb`  
		Last Modified: Fri, 23 Jan 2026 00:59:43 GMT  
		Size: 39.3 MB (39341676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee5f6668ee1f308c90b8fdd87301fb5e049ad599ea451bb322cae9b3f22e177`  
		Last Modified: Fri, 23 Jan 2026 00:59:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd002cafe7f0325f0e49e9d62f316b8d8ba2fc41b9fa6c52e503899f968208af`  
		Last Modified: Fri, 23 Jan 2026 00:59:42 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2873eb931b8e3d9a06e20edb7dfe34d434fdd9e6a14b46775833a3643c3214bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe955c835dd22e1e7141398210c5132a61c394fbac7931f1f32170b7854002be`

```dockerfile
```

-	Layers:
	-	`sha256:e3f780ac52d166bbbbf513bd248a1acd4b83ad16ee1a33234ef382fba621cffd`  
		Last Modified: Fri, 23 Jan 2026 00:59:42 GMT  
		Size: 3.7 MB (3705210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e8a358228df8b8349cff5067c48247e3a6994aa595bd6ae35d2f9a16781dd7d`  
		Last Modified: Fri, 23 Jan 2026 00:59:42 GMT  
		Size: 20.4 KB (20384 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:e2df02246795493d28bc4bbcb3c37183d4b8baec0b7dfcbfaddfc758897e065b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109966438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:482ea51c549e9daef877b43800a8231828390386f353f203c59f7867d41dae56`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 22 Jan 2026 14:57:08 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 14:57:08 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 22 Jan 2026 14:57:08 GMT
ENV container oci
# Thu, 22 Jan 2026 14:57:08 GMT
COPY dir:b163faed476797909497b9e9cbceacce9d202c7df0108da15dd805a940495105 in /      
# Thu, 22 Jan 2026 14:57:08 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 14:57:08 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 14:57:08 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 14:57:08 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 14:57:08 GMT
COPY file:d6bdaa4e7d25601d04555b39b781ff4f9dacbc577ea220997429cff55f920063 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:57:08 GMT
COPY file:d6bdaa4e7d25601d04555b39b781ff4f9dacbc577ea220997429cff55f920063 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:57:09 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="0912ab420a80f21132d8a5e29d19a23339176677" "org.opencontainers.image.revision"="0912ab420a80f21132d8a5e29d19a23339176677" "build-date"="2026-01-22T14:54:50Z" "org.opencontainers.image.created"="2026-01-22T14:54:50Z" "release"="1769090502"org.opencontainers.image.revision=0912ab420a80f21132d8a5e29d19a23339176677,org.opencontainers.image.created=2026-01-22T14:54:50Z
# Fri, 23 Jan 2026 00:57:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Jan 2026 00:57:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 00:57:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Jan 2026 00:57:42 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 23 Jan 2026 00:57:42 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Fri, 23 Jan 2026 00:57:46 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 23 Jan 2026 00:57:46 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 23 Jan 2026 00:57:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 23 Jan 2026 00:57:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:4305950dff5b7a63645441b4e7ab741317691b48df386123d1f9cf51b053ff55`  
		Last Modified: Thu, 22 Jan 2026 18:12:46 GMT  
		Size: 34.4 MB (34360531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837e8e06eae984f24eeb3bba4016e3a03487cc51453ac39f13a90e683537e12d`  
		Last Modified: Fri, 23 Jan 2026 00:58:06 GMT  
		Size: 37.8 MB (37751630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039d3845c77661496bfc5b497b2217ec5db64bb862a12bca0843c141ec75c9ea`  
		Last Modified: Fri, 23 Jan 2026 00:58:06 GMT  
		Size: 37.9 MB (37851859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46fe6332fe33b1c977823e7047cb3743781f0e1de3bfb10f6c9aa4bbc9a618c`  
		Last Modified: Fri, 23 Jan 2026 00:58:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a937a1ea9113032e687a2cee92691e10eab9ee79a27c290897e77a51a5c36d9e`  
		Last Modified: Fri, 23 Jan 2026 00:58:06 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c2f4349d50b05ba98c68273524a6931c5b6eb6242655be604d5e72f60d57fa40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dfade0e36dc34ca4eeb0b0bb907d769d7f9da2c9b938730f7b90eb6d6b2db57`

```dockerfile
```

-	Layers:
	-	`sha256:3e80ad7a7191011cd5db523a263279de256b75aaff2bdf08db3e4affc54934a9`  
		Last Modified: Fri, 23 Jan 2026 00:58:05 GMT  
		Size: 3.7 MB (3706455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea2bf2947c87ebfbb842c9795c68c3736b71134870bf855536f738b2042994b8`  
		Last Modified: Fri, 23 Jan 2026 00:58:05 GMT  
		Size: 20.4 KB (20353 bytes)  
		MIME: application/vnd.in-toto+json
