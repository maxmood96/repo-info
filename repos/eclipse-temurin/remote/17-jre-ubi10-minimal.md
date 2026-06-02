## `eclipse-temurin:17-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:0607548006f0008352c14214cd7ec6318adab3c17f9d154270f82f4727f0e8a0
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

### `eclipse-temurin:17-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:e8dd9b189253638c4469f99395d551ed5d28c6fb9631f70a397b7d7812c0e565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120155271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e3ad0056902cf79f06d69b827e5ea6c854cb0cee359ff3e3c3a08c21984cca`
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
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 02 Jun 2026 22:45:28 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 02 Jun 2026 22:45:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:45:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:45:28 GMT
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
	-	`sha256:0fa55a0f6e097af74c3ab7672127c6312d61e237877905d74d239d9c4125680b`  
		Last Modified: Tue, 02 Jun 2026 22:45:44 GMT  
		Size: 47.6 MB (47563539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce0a750a29ce744842eb08bd3107cbad5933e5b68f421ddcdd05891e58b977d`  
		Last Modified: Tue, 02 Jun 2026 22:45:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5dc86b99a4b90aad28c9cd43154f631a78b340507d8f0740cb5eee228c6bba0`  
		Last Modified: Tue, 02 Jun 2026 22:45:41 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a7bbf34b9eb4cbebf4aef07b72c9331163fed6065c766ff694dc53d780020842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3728234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d8ab2226a6b5d3c89a2cb40e3af2f06fb9d65721e5af37e5a1eeb5a47f8083`

```dockerfile
```

-	Layers:
	-	`sha256:69456768e9c7bb958f7a9a7614695cbf29528cfb6237a38c5313e571bac1f352`  
		Last Modified: Tue, 02 Jun 2026 22:45:42 GMT  
		Size: 3.7 MB (3707856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b511f58110eab7a42f57abea66a6d5bb373dcb19d17f33b23c873f19cf8aa8ba`  
		Last Modified: Tue, 02 Jun 2026 22:45:41 GMT  
		Size: 20.4 KB (20378 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:c2debb23678e05b8d9cce15e8d2ba2c92a65dd203e4cbde8c529f75340bf63f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117773144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de89cc6cbea7c0fa44e7bcb1f474b7d89f3937ed80a61624a3f690eb6db5655`
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
# Tue, 02 Jun 2026 22:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 22:44:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:44:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 22:44:16 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:44:16 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 02 Jun 2026 22:44:45 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 02 Jun 2026 22:44:45 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:44:45 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:44:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:7cd594d4c3afe0f66eb7cfc2a31b3e461f371776f986ab3d5084853335f5d2f7`  
		Last Modified: Tue, 02 Jun 2026 16:41:21 GMT  
		Size: 33.0 MB (33037428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d95983fb8c05e51acaf67de9498ed0e53918f48d57ab5a1f2b3da878e61ea8`  
		Last Modified: Tue, 02 Jun 2026 22:44:35 GMT  
		Size: 37.7 MB (37683614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb57bb05a29521a3fcd44914d29b8d3f9959dcdb51b927b5b41b6f4b4a65b91`  
		Last Modified: Tue, 02 Jun 2026 22:44:59 GMT  
		Size: 47.0 MB (47049684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5593453f37fe96848da281852751b58a8e7ce10034293535f1ef763c6ce72f07`  
		Last Modified: Tue, 02 Jun 2026 22:44:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56ec8f88c4ad618d3865995bac44d74fca53ceb6acfc6ef7c9dfa2fdd646371`  
		Last Modified: Tue, 02 Jun 2026 22:44:58 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ca7bcbc87dc094342dc7aa4d34c68e19204a68db4fee38d515db0c1873102fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3727752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf3d5a912775ab1424e1df1acaa0532632bc331f1caad5163b503ac2ebc7a70`

```dockerfile
```

-	Layers:
	-	`sha256:e8b086bc131c00a8c492a0ce0011894c7873812b99ae983de7be6e2dd85ecbc1`  
		Last Modified: Tue, 02 Jun 2026 22:44:58 GMT  
		Size: 3.7 MB (3707270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f63d5d5de32dd7aecf13c81628b2d73f1dc51767f819c679e4ef8addefa97b7`  
		Last Modified: Tue, 02 Jun 2026 22:44:58 GMT  
		Size: 20.5 KB (20482 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:545646cda8b6e0501a01b5fa7c9d7193067fb629a61ee75a3ce95c6106a16271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125994551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5733bd9ba484138a7b6221d2548ed7652cdee47d56386c0c57d95c39585a84da`
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
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 02 Jun 2026 22:52:08 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 02 Jun 2026 22:52:09 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:52:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:52:09 GMT
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
	-	`sha256:a50a5758ce8cfadeccabe1fd5154762250d4e10ff07f7feee1d919c99bcc7df0`  
		Last Modified: Tue, 02 Jun 2026 22:53:20 GMT  
		Size: 47.5 MB (47499708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aafa0ae3874f1ba4ee4848a8baa8a5b75ddbf39166a284ba2f38a02d670164e`  
		Last Modified: Tue, 02 Jun 2026 22:53:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ea9b83a99acab4ef51280a4fbeb3e655dfc511a430b8ac9ac39d4dc1d7dd2a`  
		Last Modified: Tue, 02 Jun 2026 22:53:18 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:32ddcf5faf532ceca7baa84ccf0faeaff38242e1be0646d54d7633a6c719ca95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3717009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c6edaa6015434369263d4771839d89d457062346ea0ea3723193de5f16d418`

```dockerfile
```

-	Layers:
	-	`sha256:11a09152550043d789239a874bb2dba4137541a4200c2cfa75c6f04f9cac57af`  
		Last Modified: Tue, 02 Jun 2026 22:53:19 GMT  
		Size: 3.7 MB (3696601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aee899002eda32a0825e74c3f9ecc9a9946d45f0276d39d73126209f28e66710`  
		Last Modified: Tue, 02 Jun 2026 22:53:18 GMT  
		Size: 20.4 KB (20408 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:38ce931d583b795bf10bc2d110b4c31e04933ac08c8b9c4001144daaa038359c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.4 MB (117380218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9e5691770de14f3f2e9f126134750e5806cf4ce9c405cb2c6a4fc39b1dff96`
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
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 02 Jun 2026 22:44:26 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 02 Jun 2026 22:44:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:44:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:44:27 GMT
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
	-	`sha256:8ab756960cf30aaef65f9afd94e25e5a92504671a4b2b9cfb6af23dd6f2ee47f`  
		Last Modified: Tue, 02 Jun 2026 22:44:47 GMT  
		Size: 44.5 MB (44531036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896c56ecb01c4b9bb68f8d05291cb1250dc8008cbd1068aa6815f5c8ad3a8172`  
		Last Modified: Tue, 02 Jun 2026 22:44:46 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19869d0e9df89ee6190c3f02223b746586f3962926a0223572786513d32dbee9`  
		Last Modified: Tue, 02 Jun 2026 22:44:46 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b358ec2a8a674ebf48c6efe7103ebf1a2826ce5cfa90f8236cdaca3b6f8a5bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3718222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8c0a028dee91fe2ec68eac11bd80b881fea27a96fab0cbd6ba519d77d946b3`

```dockerfile
```

-	Layers:
	-	`sha256:9dea0bb3bd4da99591d37d36d6ed3b76d01faabbee8a736b6973c74ca13c5274`  
		Last Modified: Tue, 02 Jun 2026 22:44:46 GMT  
		Size: 3.7 MB (3697846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6723fdfa0fb08cd56889320b6ffa92a15e349e3ac0bc97c398666481ac2f8907`  
		Last Modified: Tue, 02 Jun 2026 22:44:46 GMT  
		Size: 20.4 KB (20376 bytes)  
		MIME: application/vnd.in-toto+json
