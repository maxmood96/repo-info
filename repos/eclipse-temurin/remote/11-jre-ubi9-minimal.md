## `eclipse-temurin:11-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:1c5d37c925c0f4509f6facc26109c8c884f3df1a4536a08becc6972712d90748
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

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:0c5af8185b84edd5d125a119ce8fdb6a1296b73c047c837a5ccfeef080d2156f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114318735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf018c802e6aafb5508dc3c42d3fd85e2bbb64f266c4c7815c9aa60ecae5bba`
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
# Mon, 26 Jan 2026 22:04:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 26 Jan 2026 22:04:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:04:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jan 2026 22:04:18 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:04:18 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Mon, 26 Jan 2026 22:04:48 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 26 Jan 2026 22:04:48 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 26 Jan 2026 22:04:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 26 Jan 2026 22:04:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:55c0205b422beeca9ab8ece9c61b1e34f31686b8a7adf249272ac75b4dd57e4d`  
		Last Modified: Mon, 26 Jan 2026 04:14:55 GMT  
		Size: 40.0 MB (40005014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bbb8d066e23880e130a6a43cd4b27155cb76dbe6cb812c08db7522c130bf3e`  
		Last Modified: Mon, 26 Jan 2026 22:04:36 GMT  
		Size: 30.4 MB (30419130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e798de3b716c1f2e10b6109b859d65a637af3b6f43ad72aedd58a0e5c20e943e`  
		Last Modified: Mon, 26 Jan 2026 22:05:00 GMT  
		Size: 43.9 MB (43892173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63448f7800c2fa3e3f71fa209598a8a9ed468cf15526f986e1e773a6a3848d0d`  
		Last Modified: Mon, 26 Jan 2026 22:04:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6021c23f135bb6588cae69e3e5c280915e62787f925d8331a9c3da54d415832f`  
		Last Modified: Mon, 26 Jan 2026 22:04:58 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a3eb68fd17230c6ed8141dd712d931eedad0c998441ccbfaf8185565627e5c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2447043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:967026e6d5ea80b1cd790f8e1b070e7bd077613757a649175adf02d671e45e5c`

```dockerfile
```

-	Layers:
	-	`sha256:3faeba144741c945e0a949d20c0aa469f84167a8836a1cb88c9d76ddf98820e0`  
		Last Modified: Mon, 26 Jan 2026 22:04:58 GMT  
		Size: 2.4 MB (2426858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49b5fee082590168a4a4a34492f43bf9fd7e28763a0fdbb961928d3cb697cf1e`  
		Last Modified: Mon, 26 Jan 2026 22:04:58 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:03867564f84efb716df51dd4ca4ceb9224df38f40ebd71e03cabf4e3fe67c53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 MB (111319040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8e936ce0b2da408398d4c40af67f40a66e52d245c9cc5e51f9cf9ce9e55f8d`
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
# Mon, 26 Jan 2026 22:04:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 26 Jan 2026 22:04:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:04:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jan 2026 22:04:59 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:04:59 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Mon, 26 Jan 2026 22:05:02 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 26 Jan 2026 22:05:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 26 Jan 2026 22:05:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 26 Jan 2026 22:05:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:acd46633fecc5c7b908a52adf94f664d167c28dd5a89ed681fe958b1c58c6963`  
		Last Modified: Mon, 26 Jan 2026 05:26:49 GMT  
		Size: 38.2 MB (38223626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d988414ff16fa6ac71007fb17365bebba190fb10ec66b9cc9d4a8ee036a5e3`  
		Last Modified: Mon, 26 Jan 2026 22:05:15 GMT  
		Size: 30.9 MB (30860002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c44fab0b7fc4ca8e90b8ae95bd7d243c6211e8354f6769d8870143cb1ee9cb`  
		Last Modified: Mon, 26 Jan 2026 22:05:16 GMT  
		Size: 42.2 MB (42232994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2737a00bf1c7359ea313415bd8cdf9112c587d681244cc81d9c402c7184e5a`  
		Last Modified: Mon, 26 Jan 2026 22:05:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008a9f4a9bf761e94d5c316c151c394dc969368125058a2afe9b1f900f5d670f`  
		Last Modified: Mon, 26 Jan 2026 22:05:14 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:55a6d6b0a3c8630a14221f4cafd7b10942df6733e590cc9fe82840cd5e0e86f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2447124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5a70c17a355ab9263ad1a6217b6fda4e463faa533af2dab9240d98541e9761`

```dockerfile
```

-	Layers:
	-	`sha256:7472b72436a96439648af493d86c557854c02995c4690f88ef2af49d6b87c727`  
		Last Modified: Mon, 26 Jan 2026 22:05:14 GMT  
		Size: 2.4 MB (2426834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66132c20578946f473471001d6d19e111c466feaf152b9e8643ca6e98df4733f`  
		Last Modified: Mon, 26 Jan 2026 22:05:14 GMT  
		Size: 20.3 KB (20290 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:1acbacc578b94025d1be3ec1c6eef2aa4e1e004dcd9b1961bc6e281c061c4777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116702106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3000aef961c15da39aca03f5f6f596269dfaeb04aab2a5f4a24b936c8f4cf7b4`
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
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 20 Jan 2026 19:14:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 20 Jan 2026 19:14:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 20 Jan 2026 19:14:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Jan 2026 19:14:36 GMT
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
	-	`sha256:33ff5a89c1ab7b3a0a560c5dca516ec46b22122da75d5ada2c25111c619e5d2d`  
		Last Modified: Tue, 20 Jan 2026 19:15:16 GMT  
		Size: 39.3 MB (39341655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c342967a7a75a63c60879b8ab984fd0b1474a91d57b0da458d36ffd01d8ea3e`  
		Last Modified: Tue, 20 Jan 2026 19:15:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6537d9848deebada1914d8efb7c439c0066e3c56911f2d0f24f2da5ef3d914`  
		Last Modified: Tue, 20 Jan 2026 19:15:14 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5cc1ddaf56889f20d546f570c0f217cf8ab1f2ad70d8b123b519abc511ba7984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2447081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bcdea977a910032723beea3a4412bbc3bdd5b82945e901fee08155c8dbfefb4`

```dockerfile
```

-	Layers:
	-	`sha256:9db7c16fdad3dabb0cf71877087eb4714a68731425e791ee31e884732417fa6e`  
		Last Modified: Tue, 20 Jan 2026 19:15:14 GMT  
		Size: 2.4 MB (2426865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:547068aba247fa26e327424a3833bf4a374dbd1180dd713f08b1df68d5de929b`  
		Last Modified: Tue, 20 Jan 2026 19:15:14 GMT  
		Size: 20.2 KB (20216 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:16636abe0063d6b1cd4e0e2fa18d5d68237e5f4b41fe4fd9f4797f1c60fe13ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.4 MB (106438097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072dc2d503b67db20e646b3e58714ab96ac3b0c422b7dfed860410f3bd50a510`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 22 Jan 2026 04:58:45 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 04:58:45 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 04:58:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 04:58:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 04:58:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 04:58:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 04:58:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:58:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:58:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 04:58:45 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 04:58:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 04:58:45 GMT
ENV container oci
# Thu, 22 Jan 2026 04:58:45 GMT
COPY dir:aac6885cc60208b688e5345bf1882d0263712896421c4026079f2ee5542d04c3 in /      
# Thu, 22 Jan 2026 04:58:45 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 04:58:45 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 04:58:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 04:58:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 04:58:46 GMT
COPY file:0c51c116efef501ea6f2c558912c7185b4250bfc67201d9a518fec8088521239 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:58:46 GMT
COPY file:0c51c116efef501ea6f2c558912c7185b4250bfc67201d9a518fec8088521239 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:58:46 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T04:58:33Z" "org.opencontainers.image.created"="2026-01-22T04:58:33Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T04:58:33Z
# Mon, 26 Jan 2026 22:08:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 26 Jan 2026 22:08:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:08:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Jan 2026 22:08:18 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:08:18 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Mon, 26 Jan 2026 22:08:22 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8e4c0bb2488f8abd0379b660963ed981b1e136b975f3faf562e07cce81977700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='3d58318c01cc461809a8a9b15f3d52990c6e522f8a88c6b2c69dd4b57a613537';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='8487926c19c505d7f2c3b33c352962fa0f26922f29d15d0599917acf8203a67b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='97a4c089411868e24bf74a9789a819ae4164818316f8a3146460a102e8db6149';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 26 Jan 2026 22:08:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 26 Jan 2026 22:08:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 26 Jan 2026 22:08:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:e1b9d9770efd769b08fdb11a00fc5c1dfb38fe7317ac7117c4a7c576bdc5eec0`  
		Last Modified: Mon, 26 Jan 2026 06:11:55 GMT  
		Size: 38.1 MB (38131338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d11ce9e0b14a4347f7b1ace8305d243b490f08fd2278c339d8b1320e53f736`  
		Last Modified: Mon, 26 Jan 2026 22:08:41 GMT  
		Size: 30.5 MB (30452522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fea3069554c35a257dd568144c89396a735c264b609c162f9e5627a2a58e26`  
		Last Modified: Mon, 26 Jan 2026 22:08:41 GMT  
		Size: 37.9 MB (37851820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c82d1affe9bffee9999037a8ea3906dfbbdf5fc484d6af9154154e62e3c9a2`  
		Last Modified: Mon, 26 Jan 2026 22:08:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3f8cd1b8947af26f9748876b8b2669590e0f2228f0d2a2d15517f56ae31baf`  
		Last Modified: Mon, 26 Jan 2026 22:08:39 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:16593ed56bfa29dfd6876117960b9ac266ed2059c42f9892e44bc3e48bc4c8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2438840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b936c18d4dd27432d6dd278c64cb8322ca87bf78edc31ecd9d10e60e34f04cb4`

```dockerfile
```

-	Layers:
	-	`sha256:099f575b57413fe7e8f9d31711d090adb4b358756aaf31d743d567b3a722cb22`  
		Last Modified: Mon, 26 Jan 2026 22:08:39 GMT  
		Size: 2.4 MB (2418656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6c44100b62396847b6b51d3cc2eaa64e8a748ed22efbe26f3b14745346564d4`  
		Last Modified: Mon, 26 Jan 2026 22:08:39 GMT  
		Size: 20.2 KB (20184 bytes)  
		MIME: application/vnd.in-toto+json
