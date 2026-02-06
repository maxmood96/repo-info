## `eclipse-temurin:21-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:5de2c72777a5266cf498a41bf0cc57802e7208a15ba8338d38005506f8237eb2
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

### `eclipse-temurin:21-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:9256e8152637f93119bf644ff2506cd61617c40f0c9a31ac8d919b8c795d261e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.0 MB (124961987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230595cd282b59800319272a0d396eb350890fa5409ca51012f878dabe8e5b13`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
# Thu, 05 Feb 2026 22:13:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:13:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:13:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:13:41 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:13:41 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:20:22 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 05 Feb 2026 22:20:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:20:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:20:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:819501e18c85a616b033a682e2078167e38cd15970dd3534932af6715532259f`  
		Last Modified: Wed, 04 Feb 2026 05:56:28 GMT  
		Size: 34.6 MB (34565108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8255ab164d6bca74dab4fccc1211ea8112443b60956af072daa8620274b6889d`  
		Last Modified: Thu, 05 Feb 2026 22:14:00 GMT  
		Size: 37.4 MB (37413662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a1838b0d76277b838fc7ed9d7c06c3e7620dc7becbd0d0fca3e1afff60c2a0`  
		Last Modified: Thu, 05 Feb 2026 22:20:36 GMT  
		Size: 53.0 MB (52980802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a18d43911554f7dbb4e4eb5886c9bf64f7302de08ed375cb9cd9bccb22057e5`  
		Last Modified: Thu, 05 Feb 2026 22:20:35 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff2cd96e15d7df341b655f677a7cb60b8c4cc2926ec623a498de01a41f62c4a`  
		Last Modified: Thu, 05 Feb 2026 22:20:35 GMT  
		Size: 2.3 KB (2288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8c328cf0f77d056ba18bd368e7cea209d272f482b102db34638542995134ce98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb9f13299946aaa2a151133d71105d450a6bd2ef052a6be7b7801d1192bb9ef`

```dockerfile
```

-	Layers:
	-	`sha256:013537fe91fe1aa962aeadaff69b49a97571b1236ab3b812a80d5b71e20e847f`  
		Last Modified: Thu, 05 Feb 2026 22:20:35 GMT  
		Size: 3.7 MB (3706528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9512ebcc3619cd0272d4ca3dcd1e0236f105b9c7a5f95c39629e8d44909f0d18`  
		Last Modified: Thu, 05 Feb 2026 22:20:35 GMT  
		Size: 20.4 KB (20354 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:507e1e7af4012217dbeeda4599be1a7e6c55c2d810e091c9691ba2a118e301a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122181545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c3192dec76c244e7b5dfbf883b23297ae037953fa048b64de697c38591d827`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
# Thu, 05 Feb 2026 22:19:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:19:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:19:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:19:45 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:19:45 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:19:48 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 05 Feb 2026 22:19:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:19:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:19:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:e7aaef72f9aac8066ddd0c18bcd7c76fcc63212a965d38f195e0959c666aa7ce`  
		Last Modified: Wed, 04 Feb 2026 06:11:32 GMT  
		Size: 32.7 MB (32661097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a539e8b66b00edd9dd0cc24547f7213a89e3e1202981628483ea70ccbde4f4`  
		Last Modified: Thu, 05 Feb 2026 22:20:04 GMT  
		Size: 37.4 MB (37361779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c293282883f035f24c6aa3750da0228dc1c94d769cbfcf0d4da09230eab36f5`  
		Last Modified: Thu, 05 Feb 2026 22:20:04 GMT  
		Size: 52.2 MB (52156251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a4f31eefdab579dc9722105f9754c85ab415c9caa86b3ec1a4feb887706dde`  
		Last Modified: Thu, 05 Feb 2026 22:20:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfbd86a8d9fb1c6cb3d5d1a3944c1b58cc548b277d44cc2f1f19afbcd506955`  
		Last Modified: Thu, 05 Feb 2026 22:20:02 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a7c15c588b6d83b5966b132731e55e7f7ca0972c943d786f8e822fc9d3205b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ee80abf1dd8277b451227c3151157ab801e50046da358fbff3e3efb7d520ec`

```dockerfile
```

-	Layers:
	-	`sha256:11f539f33741e3e9ca51b11271ecef0daac0c70ad9379190ff4e317d4b99a776`  
		Last Modified: Thu, 05 Feb 2026 22:20:02 GMT  
		Size: 3.7 MB (3705942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5ada87f8ed813bae43e40d0b6cc3b4836001cd34bc2e666431b966ab7c6fc07`  
		Last Modified: Thu, 05 Feb 2026 22:20:02 GMT  
		Size: 20.5 KB (20458 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:d9a1d3ba41de236ce59db3df40f9a84e64c7f082daacabb489c073713316028c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130828846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ba6106516f558f4eee626ade8c4361a4cfb4e0f7756ff6fd09133ee6c2ac2c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:30:38 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 05 Feb 2026 22:30:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:30:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:30:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:b7f39df58dd37a5be6dcc56b37d9ed743bfd65be5d2cfe446e5f2ebf745efed5`  
		Last Modified: Thu, 05 Feb 2026 22:31:13 GMT  
		Size: 53.0 MB (52964657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fc22ce21720772d79fe5d8e913b9ec62c09064777730362f48634849a92d29`  
		Last Modified: Thu, 05 Feb 2026 22:31:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d09a9e4c0a2919a0edfececea12f7e142fced8b2c760c3c85608db1dd6ed2c`  
		Last Modified: Thu, 05 Feb 2026 22:31:09 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ad2b23e15f4bb4dca494ae6e58ef65041a9ba18d02369ddb8d3cdf0671f49909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3715656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89549e522a76d7a26a5a811523e33366176e8489c0d67a4b43d7bc7023c5a25`

```dockerfile
```

-	Layers:
	-	`sha256:be902d3052b037034d761f7a1c68ebaa0edb1bd367719abd74f1949a9f8c4ba3`  
		Last Modified: Thu, 05 Feb 2026 22:31:11 GMT  
		Size: 3.7 MB (3695273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eded48fdec1c70c8b66c8f103fff3af5ed71346d05c3acbe15596c5ec86e74f`  
		Last Modified: Thu, 05 Feb 2026 22:31:11 GMT  
		Size: 20.4 KB (20383 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:aaeb6a9502b60a7c3ee76099f4a44f0541a530132db4d3d0f60df3a23a37c2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121725261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380a4a862bfca59ca73a19238824541d34649ee5c92667dc290fba5f5c2dd563`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
# Thu, 05 Feb 2026 00:07:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 00:07:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:07:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 00:07:02 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:07:02 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:22:30 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 05 Feb 2026 22:22:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:22:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:22:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:3c5e6ba1d838b1d4e103e0457068eaff01f71c8436e4442eaa2f5c701ccbe1c6`  
		Last Modified: Wed, 04 Feb 2026 06:11:43 GMT  
		Size: 34.4 MB (34399700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd19d1328bf4040759158c3f4a9ecc47912b1ffb1b173eb92519cea4b9d9c9de`  
		Last Modified: Thu, 05 Feb 2026 00:07:35 GMT  
		Size: 37.8 MB (37794412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1185a76e966076fb3850d622ec53e7b1ad1d4aded56f5bfab15b7b07726f8ba6`  
		Last Modified: Thu, 05 Feb 2026 22:23:08 GMT  
		Size: 49.5 MB (49528731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a791caba137d9d40565c74daa8808dbe4c3d5b6aa1527892b2cfed85bdb97b87`  
		Last Modified: Thu, 05 Feb 2026 22:23:07 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fa78ae60b692ae58bf2345e15f7a1b869908ece92ad32d2de7a710fa488055`  
		Last Modified: Thu, 05 Feb 2026 22:23:07 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:76e5d9122fc0e4dfac5e76fed2fdbc2959cfca64546e42ecd86868b207fc526b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3716872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa88b4f517284bdd859577f7f04851f0798a984f363dace741efaaede32326ae`

```dockerfile
```

-	Layers:
	-	`sha256:447a48bdcdc77d773bca5c8de32c2d4eb7065aa1c6b223cd74f5395304accc08`  
		Last Modified: Thu, 05 Feb 2026 22:23:07 GMT  
		Size: 3.7 MB (3696518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23106d4c5381c02210970e0930c5106c1d38a8711f21497b74b45faa27b17446`  
		Last Modified: Thu, 05 Feb 2026 22:23:07 GMT  
		Size: 20.4 KB (20354 bytes)  
		MIME: application/vnd.in-toto+json
