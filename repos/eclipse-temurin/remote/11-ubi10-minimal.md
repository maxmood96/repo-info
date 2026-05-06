## `eclipse-temurin:11-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:79863b02a1a4a55d85156330ac8a7be17dac89189f4f2df5d377579afa74ce0e
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

### `eclipse-temurin:11-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:e43fd75d0810ef0ecb847dfeadc209e58a318464e159aa3f5917846b302e7927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.0 MB (199036693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e7e6fef9affc8a3d2b3655d472ad2355f192f9ae1c88fb685cbd32f105f4a4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 01:36:53 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:36:53 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:36:53 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:36:53 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 04 May 2026 01:36:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:36:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 04 May 2026 01:36:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:36:53 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:36:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 04 May 2026 01:36:53 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:36:53 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 04 May 2026 01:36:53 GMT
ENV container oci
# Mon, 04 May 2026 01:36:54 GMT
COPY dir:90d4f1f85494d2a8bf17340af60eb04fb8df2adbe40376c2198b52d03b3dce87 in /      
# Mon, 04 May 2026 01:36:54 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:36:54 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:36:54 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:36:54 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:36:54 GMT
COPY file:44acb722ff6847a849911ad1532360393cd9c16592e8d1f9e199cff925bbc7d5 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:36:54 GMT
COPY file:44acb722ff6847a849911ad1532360393cd9c16592e8d1f9e199cff925bbc7d5 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:36:54 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="2c4967ab62628fff803457df7635994ca0e85fbc" "org.opencontainers.image.revision"="2c4967ab62628fff803457df7635994ca0e85fbc" "build-date"="2026-05-04T01:36:38Z" "org.opencontainers.image.created"="2026-05-04T01:36:38Z" "release"="1777858393"org.opencontainers.image.revision=2c4967ab62628fff803457df7635994ca0e85fbc,org.opencontainers.image.created=2026-05-04T01:36:38Z
# Tue, 05 May 2026 23:07:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 May 2026 23:07:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:07:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 May 2026 23:07:52 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 05 May 2026 23:07:52 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 05 May 2026 23:07:59 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 05 May 2026 23:08:01 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:08:01 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:08:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 May 2026 23:08:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6c2848906904fdb30be3302af6950faf3bb49f8acf1fe7da43266ab561f76092`  
		Last Modified: Mon, 04 May 2026 03:13:50 GMT  
		Size: 34.6 MB (34648199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3e0a0050aebaf322076b278aaa26e45de70bc1d097f52e23133bf4ba5f4590`  
		Last Modified: Tue, 05 May 2026 23:08:18 GMT  
		Size: 22.0 MB (22037220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8000a7ff31f85beded298e8e3135a9cd8e4be55a55af5e3a6283375ae1a01b18`  
		Last Modified: Tue, 05 May 2026 23:08:22 GMT  
		Size: 142.3 MB (142348855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad0372dd46aeace41cc19b2664b6dfdaef14073990703ab634062127d71dd6f`  
		Last Modified: Tue, 05 May 2026 23:08:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b58b631c92b528e32ee05fcb190b499fcc2c57244700b4acf931323971a8a7`  
		Last Modified: Tue, 05 May 2026 23:08:16 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:71934b99f2241d5681d0f181d0feb0378208fd7b4e421fa47d89c50971c886db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3090880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d883cd49078e44442029e7b62637dc5687f2e2344bbd4b1a4526454da1d3a4d0`

```dockerfile
```

-	Layers:
	-	`sha256:609d0d754c6a6a26972197ef44f119df732e62e9cd8bed8eb27f8a51ec30298c`  
		Last Modified: Tue, 05 May 2026 23:08:16 GMT  
		Size: 3.1 MB (3069541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63fb4b53831b89d513e136eb9669df8a27ff391394215a863817df0f231c51c4`  
		Last Modified: Tue, 05 May 2026 23:08:16 GMT  
		Size: 21.3 KB (21339 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:54b06fb04638157b5426737f7dfeea73a0b9283e644e7cded8d1a2481a3ee3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.1 MB (194056238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c212b0d6d433a6c36edf9544aafe5d208814b2a0fc5ce625c7cfc8f050e9cc5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 01:38:51 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:38:51 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:38:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:38:51 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 04 May 2026 01:38:51 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:38:51 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 04 May 2026 01:38:51 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:38:51 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:38:51 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 04 May 2026 01:38:51 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:38:51 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 04 May 2026 01:38:51 GMT
ENV container oci
# Mon, 04 May 2026 01:38:52 GMT
COPY dir:4f490e44b5cd259c269df4e89626a736e4b70875a47bc79b960d52f7b56f7967 in /      
# Mon, 04 May 2026 01:38:52 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:38:52 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:38:52 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:38:52 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:38:53 GMT
COPY file:e2c2a2ab213ef0433a1e15d666daa6e664714283c2d03394bbfa240f7cd44679 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:38:53 GMT
COPY file:e2c2a2ab213ef0433a1e15d666daa6e664714283c2d03394bbfa240f7cd44679 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:38:53 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="2c4967ab62628fff803457df7635994ca0e85fbc" "org.opencontainers.image.revision"="2c4967ab62628fff803457df7635994ca0e85fbc" "build-date"="2026-05-04T01:38:35Z" "org.opencontainers.image.created"="2026-05-04T01:38:35Z" "release"="1777858393"org.opencontainers.image.revision=2c4967ab62628fff803457df7635994ca0e85fbc,org.opencontainers.image.created=2026-05-04T01:38:35Z
# Tue, 05 May 2026 23:07:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 May 2026 23:07:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:07:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 May 2026 23:07:48 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 05 May 2026 23:07:48 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 05 May 2026 23:07:56 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 05 May 2026 23:07:58 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:07:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:07:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 May 2026 23:07:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:908809553a77ac560aff532a902be43c3a99a0dcb4f759158a75984cb82c4b9d`  
		Last Modified: Mon, 04 May 2026 06:16:39 GMT  
		Size: 32.7 MB (32711611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d709fca6869e22fad5c9b0dbb700e99686d54ee17d198ca1f03be45dd35173`  
		Last Modified: Tue, 05 May 2026 23:08:15 GMT  
		Size: 22.3 MB (22301544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2517056ab0b328421f3363fbae5bc94465d10304ab4e15347655d54c1b11f30e`  
		Last Modified: Tue, 05 May 2026 23:08:18 GMT  
		Size: 139.0 MB (139040662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d421558183ab858b7f6f496fb6dc4e0fc6e3f0217799c6846d6b6d36efd8156`  
		Last Modified: Tue, 05 May 2026 23:08:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cc53fad96bc443aeaedffe39d6cb4431f0f0f75c723571473544da655ef2de`  
		Last Modified: Tue, 05 May 2026 23:08:00 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8a0610fb2ff8c7fff6c9e51e3897591d188b2bbe63f9e3509e835ef975b7d55b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3091041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2578449a8c2fdb96be0fce8e95532b532a120aff39a38b7df0004a1b64b3db8`

```dockerfile
```

-	Layers:
	-	`sha256:9e5ee2df930f0fce710ec18392085bff9a4c643e9ccc8c99fe954e9a698d548a`  
		Last Modified: Tue, 05 May 2026 23:08:14 GMT  
		Size: 3.1 MB (3069585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c3fa2e1eace990a2b8a6ea00272f677ed2f79b6db2a4f2aebb0d025213d7855`  
		Last Modified: Tue, 05 May 2026 23:08:14 GMT  
		Size: 21.5 KB (21456 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:60923cd44e1cd71669d99694e1890a66ff9f7d1a52e08b088ca2e82c086e4481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191696232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80f4ee0587978bf438f6bbd3b43ddf7aea9895105873b938814f8810a760629`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 01:39:14 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:39:14 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:39:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:39:14 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 04 May 2026 01:39:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:39:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 04 May 2026 01:39:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:39:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:39:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 04 May 2026 01:39:15 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:39:15 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 04 May 2026 01:39:15 GMT
ENV container oci
# Mon, 04 May 2026 01:39:15 GMT
COPY dir:12413a5bdb80a75f63d061b3c0328d3ec0033dbb6ef2e4efcba8481b6ce277c7 in /      
# Mon, 04 May 2026 01:39:15 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:39:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:39:15 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:39:15 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:39:15 GMT
COPY file:727a91663c7c1ef3c87416ec38b4c09702b0fa948721f73b1c8c27f7a242068b in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:39:16 GMT
COPY file:727a91663c7c1ef3c87416ec38b4c09702b0fa948721f73b1c8c27f7a242068b in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:39:16 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="2c4967ab62628fff803457df7635994ca0e85fbc" "org.opencontainers.image.revision"="2c4967ab62628fff803457df7635994ca0e85fbc" "build-date"="2026-05-04T01:39:03Z" "org.opencontainers.image.created"="2026-05-04T01:39:03Z" "release"="1777858393"org.opencontainers.image.revision=2c4967ab62628fff803457df7635994ca0e85fbc,org.opencontainers.image.created=2026-05-04T01:39:03Z
# Tue, 05 May 2026 23:47:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 May 2026 23:47:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:47:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 May 2026 23:47:29 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 05 May 2026 23:47:29 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 05 May 2026 23:49:48 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 05 May 2026 23:49:53 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:49:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:49:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 May 2026 23:49:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f2dd1d2c3d5fda579799f9becd292589fb99f0abc7f5c226856eb2bbbbc120cc`  
		Last Modified: Mon, 04 May 2026 06:16:51 GMT  
		Size: 38.7 MB (38745905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2ee71f34837c204e126c0f30bd59bdd1c1aad2d6a82e82078b6ce249102e06`  
		Last Modified: Tue, 05 May 2026 23:48:16 GMT  
		Size: 23.3 MB (23333693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f42cb654fd52e10e50e872e159c0e9f424a7e3efaf546022483128c82df81e`  
		Last Modified: Tue, 05 May 2026 23:50:35 GMT  
		Size: 129.6 MB (129614213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791fcb875d1f1993ec583e3d082a14445d916cc53ac119b1263d8fbfb9f29513`  
		Last Modified: Tue, 05 May 2026 23:50:31 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71619b06855a193fb7a0308749085d0f58d991ee182e86add6f5b8bb989452fa`  
		Last Modified: Tue, 05 May 2026 23:50:32 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c6c90b6db68cd589c3bfbc4ffa4c383e513984dc0cc7fcc0d6686093401c255c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3084058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee7b9a65aab8361dcb1a7874b0b4b0cfbe906b9e9e48d4859a6a5a34c24c0eb`

```dockerfile
```

-	Layers:
	-	`sha256:288264ab8a07c5777f089a8223d9b4173da386379c050dcc7a553a4d43c93d03`  
		Last Modified: Tue, 05 May 2026 23:50:32 GMT  
		Size: 3.1 MB (3062682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:043154b04afc4938c2d1268d2ca262550d472dcb46bb42fb98a9c14951a0d73a`  
		Last Modified: Tue, 05 May 2026 23:50:31 GMT  
		Size: 21.4 KB (21376 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:0caeb32eacdf140e216a26823e49d442ff676520620e3e414a44e771f2efa01e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.9 MB (179858881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96c2c66897ceb1de6f2397ca9fcbd50f7771e1e963e6ee53c4806998333a545`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 01:46:56 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:46:56 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:46:56 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:46:56 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 04 May 2026 01:46:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:46:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 04 May 2026 01:46:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:46:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:46:56 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 04 May 2026 01:46:56 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:46:56 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 04 May 2026 01:46:56 GMT
ENV container oci
# Mon, 04 May 2026 01:46:56 GMT
COPY dir:cacbd48510196fa765f2d5bccb8b2b0023c608fcbd86154b6fe34e775acd2483 in /      
# Mon, 04 May 2026 01:46:56 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:46:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:46:56 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:46:57 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:46:57 GMT
COPY file:6983ce2775fc6ec74b2d7c54d91fce16f639c26d824bf41c774ba5d5ae4037e9 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:46:57 GMT
COPY file:6983ce2775fc6ec74b2d7c54d91fce16f639c26d824bf41c774ba5d5ae4037e9 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:46:57 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="2c4967ab62628fff803457df7635994ca0e85fbc" "org.opencontainers.image.revision"="2c4967ab62628fff803457df7635994ca0e85fbc" "build-date"="2026-05-04T01:46:14Z" "org.opencontainers.image.created"="2026-05-04T01:46:14Z" "release"="1777858393"org.opencontainers.image.revision=2c4967ab62628fff803457df7635994ca0e85fbc,org.opencontainers.image.created=2026-05-04T01:46:14Z
# Wed, 06 May 2026 00:08:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 May 2026 00:08:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 00:08:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 May 2026 00:08:35 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 06 May 2026 00:08:35 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 06 May 2026 00:08:41 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 06 May 2026 00:08:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 06 May 2026 00:08:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 06 May 2026 00:08:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 May 2026 00:08:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e434a7e4a8db18a3b2f706d5c1b2a02cfe20f46083a805f7dcf9e2e92903aa2e`  
		Last Modified: Mon, 04 May 2026 06:16:45 GMT  
		Size: 34.4 MB (34430001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e050a10412e65251d89d72303bf35471e8696e8e4584956371e471d0f9f274c`  
		Last Modified: Wed, 06 May 2026 00:09:22 GMT  
		Size: 22.4 MB (22365043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec86e2fe1b47a9bb05e11e0ef47204422d5845f3981eac43a80abdae3fdffc52`  
		Last Modified: Wed, 06 May 2026 00:09:24 GMT  
		Size: 123.1 MB (123061419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7fbe92066f4c9e9b2b9762b135349bd543adcb2ea051c601c5627e97adfbaa`  
		Last Modified: Wed, 06 May 2026 00:09:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303c480006d47e7c5fee0809efcca388c49d136057eb2439560743957dde13cb`  
		Last Modified: Wed, 06 May 2026 00:09:07 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6213571c397f19c5e4bf94f352e1a3a3c47e1d7d053886adc4a1d7ea326a4754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3083399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22223a2aad02c4ee56c78a2088b72d8fe11fc1f40205b3db87ac0d4c1340526e`

```dockerfile
```

-	Layers:
	-	`sha256:72ba2439e4f13fceda211a4e3e23cc9f8aa61a2a4d9c6f4059ae79e7b7776924`  
		Last Modified: Wed, 06 May 2026 00:09:22 GMT  
		Size: 3.1 MB (3062059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ab39dfd7a911379b752f8bf3cec7459ee28eb7c056914a861ead78e3a1babf7`  
		Last Modified: Wed, 06 May 2026 00:09:22 GMT  
		Size: 21.3 KB (21340 bytes)  
		MIME: application/vnd.in-toto+json
