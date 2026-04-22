## `eclipse-temurin:8u482-b08-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:44250272671dbc1d1310b76f0a7805574bf23422e2a3fad10289bf45fbbb271b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8u482-b08-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:9415916acec4b7e34e10e4f7cd385b3d2cc2fc795109a1b60cb08f700aa9c264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114391099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff76f671d29aaaf5ea3dd2dc0ba86a054335b5d2e6025a4f26e1d9593fccc78a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 22 Apr 2026 05:17:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:17:54 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:17:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:17:54 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 22 Apr 2026 05:17:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:17:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 22 Apr 2026 05:17:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:17:55 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:17:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 22 Apr 2026 05:17:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:17:55 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 22 Apr 2026 05:17:55 GMT
ENV container oci
# Wed, 22 Apr 2026 05:17:55 GMT
COPY dir:dff10165caa8c30a8c2673a95ace4a09e747d1c9e656d37fe7e2593a4192cea1 in /      
# Wed, 22 Apr 2026 05:17:55 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:17:55 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:17:55 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:17:55 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:17:55 GMT
COPY file:1096e68e00ce2e3d16a7fbd65fd0781406fccc42abee623e8fa1f8395c75478b in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:17:56 GMT
COPY file:1096e68e00ce2e3d16a7fbd65fd0781406fccc42abee623e8fa1f8395c75478b in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:17:56 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "org.opencontainers.image.revision"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "build-date"="2026-04-22T05:17:41Z" "org.opencontainers.image.created"="2026-04-22T05:17:41Z" "release"="1776834797"org.opencontainers.image.revision=8f919d0175e713e927f4fc60c8a4a7f7d7d63a58,org.opencontainers.image.created=2026-04-22T05:17:41Z
# Wed, 22 Apr 2026 18:16:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:16:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:16:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:16:24 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:16:24 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 22 Apr 2026 18:16:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='46496dfa7e58784adf96a3a2bd1ac8be9fda2d8749a9c52bf74fb582aa1449e2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='b563c5c90dcff0c1cf5a1bdc3110e560c979254a17e696902e922631264cf342';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='01672ca52509f4cb1ffa8aed905808fed7b984f3e279cb13d90a6e865ff6199f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 22 Apr 2026 18:16:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:16:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:16:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:74bbdc6f81c25b3fa8d6367ec856d92f28db48c1860a008184a1d723c8d399cc`  
		Last Modified: Wed, 22 Apr 2026 06:14:16 GMT  
		Size: 34.6 MB (34590462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24964a375fc4e77683a83b4d57864d44b2d78e2c3e4556f43bba7fabc3c39eba`  
		Last Modified: Wed, 22 Apr 2026 18:16:42 GMT  
		Size: 37.5 MB (37473506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc881951f42c0d03aa68ca138bd4edcb33020493a89b95e70fb1c54df7e62fe`  
		Last Modified: Wed, 22 Apr 2026 18:16:42 GMT  
		Size: 42.3 MB (42324715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22049c155b15f02a57e69f7b31e1272a2db0d430ca6ea1cf933ed72f7152f641`  
		Last Modified: Wed, 22 Apr 2026 18:16:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e63e82401f56d8f2c195bd346d6ef491dde5a6a4accb1ef768643a8aca9164`  
		Last Modified: Wed, 22 Apr 2026 18:16:40 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u482-b08-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c7ab6de94bb50538eebe69dd4d2311e78c013bc5a05bffc088c5347f8a28c26c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ac6b9ab01c2fa9965985787ab7283d46c55ed13e6700c4fe1d3ec34fac345b`

```dockerfile
```

-	Layers:
	-	`sha256:e35ddf6c0204f18835dcbee235c2f64b6b01c900119e214b7a93e522512efec9`  
		Last Modified: Wed, 22 Apr 2026 18:16:40 GMT  
		Size: 3.7 MB (3734802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f6fa9505a09bba351035e812b983876b20d7d35e73197969c2c2fb2e4140009`  
		Last Modified: Wed, 22 Apr 2026 18:16:40 GMT  
		Size: 19.5 KB (19511 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u482-b08-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:2fe34883c370e1b131450408041366a30271d144f8799e78f40d07b401fe0046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111419604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4e2b792a9cbf2d2fafb66e8454a1f47956e8d61e3a67d3454d0ada437edd76`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 22 Apr 2026 05:20:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:20:36 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 22 Apr 2026 05:20:37 GMT
ENV container oci
# Wed, 22 Apr 2026 05:20:38 GMT
COPY dir:3a08e309561c3ef0f2f1f503de8f559ee625841311cafaf96b59ce47a8f1ffce in /      
# Wed, 22 Apr 2026 05:20:38 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:20:38 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:20:38 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:20:38 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:20:38 GMT
COPY file:70c2dda7fafaa9f54a42bab62bbf07c21fa030503d7cbb51eb7b6ef84bbbba51 in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:20:38 GMT
COPY file:70c2dda7fafaa9f54a42bab62bbf07c21fa030503d7cbb51eb7b6ef84bbbba51 in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:20:38 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "org.opencontainers.image.revision"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "build-date"="2026-04-22T05:20:21Z" "org.opencontainers.image.created"="2026-04-22T05:20:21Z" "release"="1776834797"org.opencontainers.image.revision=8f919d0175e713e927f4fc60c8a4a7f7d7d63a58,org.opencontainers.image.created=2026-04-22T05:20:21Z
# Wed, 22 Apr 2026 18:16:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:16:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:16:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:16:02 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:16:02 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 22 Apr 2026 18:16:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='46496dfa7e58784adf96a3a2bd1ac8be9fda2d8749a9c52bf74fb582aa1449e2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='b563c5c90dcff0c1cf5a1bdc3110e560c979254a17e696902e922631264cf342';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='01672ca52509f4cb1ffa8aed905808fed7b984f3e279cb13d90a6e865ff6199f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 22 Apr 2026 18:16:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:16:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:16:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:e8c4c206e9282db63c5bc98a6b172b79a7673404566e305674f0176bf9808f38`  
		Last Modified: Wed, 22 Apr 2026 06:16:01 GMT  
		Size: 32.7 MB (32712089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b2e0d069a7a5fb2c579c26ee99a97bf4f9a9a32f7a6627a9ccedbc26b19200`  
		Last Modified: Wed, 22 Apr 2026 18:16:19 GMT  
		Size: 37.4 MB (37416539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf273816b36550283c2abc1da46e97dff41170debe4ed29d03a3520e68f90c7`  
		Last Modified: Wed, 22 Apr 2026 18:16:19 GMT  
		Size: 41.3 MB (41288558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b78b4102ae73f9f6d8ec8e7c4ed7da7b45c4a05cb65f439024b631f89d68965`  
		Last Modified: Wed, 22 Apr 2026 18:16:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf9fc1736de609671d885acb14e722fd7dde3e478cb282b8ea1490a63747a70`  
		Last Modified: Wed, 22 Apr 2026 18:16:17 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u482-b08-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b7a7d555ca4c34b3fa2290451ed81ffb17f5194ee2a31307a639ce92cfcea176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aebe249e4fb0f5f459f3fc8f3ef3b954d79c68154dfbf8d776252b9ac973337a`

```dockerfile
```

-	Layers:
	-	`sha256:04875875f85819bc67c272211b939b649ac0f6b74445bf15ba7b160c876969f3`  
		Last Modified: Wed, 22 Apr 2026 18:16:17 GMT  
		Size: 3.7 MB (3734908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a60d59e874382b2cc33eb0f78ecf7c57e49f843ccd4d4d8e2fe409b15899523`  
		Last Modified: Wed, 22 Apr 2026 18:16:17 GMT  
		Size: 19.6 KB (19615 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u482-b08-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:8d7662cf900e240e858429d6693541155f33d30d0000ac829f4a17b6cdb7a41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119629022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152971d9eda03fe4a43176d2fb2da79cf26d666ef14a007401e87e38a0d7333c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 20 Apr 2026 01:03:47 GMT
ENV container oci
# Mon, 20 Apr 2026 01:03:48 GMT
COPY dir:56f7e656d3890224e75a1a16ae5067199386e27e9adfa336ba5808545546cc9e in /      
# Mon, 20 Apr 2026 01:03:48 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 01:03:48 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 01:03:48 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 01:03:48 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 01:03:48 GMT
COPY file:7bbce3df91c54303354eb2bfc2cec747cbe675dbc724bafe59b7a5adbf9432ea in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 01:03:48 GMT
COPY file:7bbce3df91c54303354eb2bfc2cec747cbe675dbc724bafe59b7a5adbf9432ea in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 01:03:49 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="32540b060e1a63cad21d656f09cff9da51482dc3" "org.opencontainers.image.revision"="32540b060e1a63cad21d656f09cff9da51482dc3" "build-date"="2026-04-20T01:03:36Z" "org.opencontainers.image.created"="2026-04-20T01:03:36Z" "release"="1776646707"org.opencontainers.image.revision=32540b060e1a63cad21d656f09cff9da51482dc3,org.opencontainers.image.created=2026-04-20T01:03:36Z
# Mon, 20 Apr 2026 23:00:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Apr 2026 23:00:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:00:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Apr 2026 23:00:58 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:00:58 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Mon, 20 Apr 2026 23:01:56 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='46496dfa7e58784adf96a3a2bd1ac8be9fda2d8749a9c52bf74fb582aa1449e2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='b563c5c90dcff0c1cf5a1bdc3110e560c979254a17e696902e922631264cf342';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='01672ca52509f4cb1ffa8aed905808fed7b984f3e279cb13d90a6e865ff6199f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 20 Apr 2026 23:01:58 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:01:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:01:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6d2ce28440d2316b24b69c4ac9181a2021fc4fbcccd08e544cb55b3f85789742`  
		Last Modified: Mon, 20 Apr 2026 12:18:07 GMT  
		Size: 38.7 MB (38691389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d8a467e0af186e4504fef70fa25944d04fcadf33d89978c86033d4efabe13`  
		Last Modified: Mon, 20 Apr 2026 23:01:39 GMT  
		Size: 39.2 MB (39213371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925d468454539127be2cf459d8f6f5681bd51fe1f3d37b94d6a7b9ca2ece33b5`  
		Last Modified: Mon, 20 Apr 2026 23:02:25 GMT  
		Size: 41.7 MB (41721845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926c8cef78273720f581703dfa22930f633cf4c414736866c1f062c6c0602962`  
		Last Modified: Mon, 20 Apr 2026 23:02:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1242ac21fd6acc016178e14ac15a88665b9dff9430413f51ef69d815d876b42b`  
		Last Modified: Mon, 20 Apr 2026 23:02:23 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u482-b08-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8f6781c5c23a8e610eacbed40a3c228bf3a07a633a7f91f7599a9367c50d4c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91361117b89c55d80cb1644076a79a81046e67a81b8665c0a229175c93896c5f`

```dockerfile
```

-	Layers:
	-	`sha256:6cfec2c7d9b0311d578afec9846788c87de0a94a96af1e197cfc77dcd7d1281d`  
		Last Modified: Mon, 20 Apr 2026 23:02:24 GMT  
		Size: 3.7 MB (3724239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cff460d18d816e6b781188c4ee198e8d3ce5e8466d2e1173f23db02b05cabb29`  
		Last Modified: Mon, 20 Apr 2026 23:02:23 GMT  
		Size: 19.5 KB (19541 bytes)  
		MIME: application/vnd.in-toto+json
