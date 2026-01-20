## `eclipse-temurin:21-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:1aaa74a39b94e5981ca5cbe2f4e0192679ee4076ba8f47ea8049ffb7fa9b82d5
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

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:d411f7557e435c69abcd2f0e05204db34c910ee201c6c95fbe03ad36823c6d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123430658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04461f12c2e1f62e040f95b9479fb97487839a04ed538a41584b733c96c76416`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Thu, 04 Dec 2025 19:45:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Dec 2025 19:45:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 19:45:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 Dec 2025 19:45:24 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 04 Dec 2025 19:45:24 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 04 Dec 2025 19:47:25 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 04 Dec 2025 19:47:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 04 Dec 2025 19:47:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:47:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:19 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58683a05ac4545db26cedb6bf069ef78065981b9418ff344b989e5547ce25b5f`  
		Last Modified: Thu, 04 Dec 2025 19:45:59 GMT  
		Size: 30.4 MB (30411196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd720f2a510a3b2bc0d9e627dc40081f1e8207b2da1090e45e4c52bcfb557326`  
		Last Modified: Thu, 04 Dec 2025 19:47:39 GMT  
		Size: 53.0 MB (52976285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d8397fe222c4ee9ec0214bc18f2cdc1d932221967832db62991d0040daa9c7`  
		Last Modified: Thu, 04 Dec 2025 19:47:37 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1884282ac936c5130c69673461f63290fda19ce293d75ae3f784c1299c74441b`  
		Last Modified: Thu, 04 Dec 2025 19:47:37 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6f36ae62c49de93007293fa0c494ce6d154a86b66ef8f65d82fa11528d97742e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2437011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c546357f47bdc80812997f79d5019713fa03d47f75bbefb07d9c69951bcf77a5`

```dockerfile
```

-	Layers:
	-	`sha256:f747774fb0b3998a7e1f2388eb24cf58d9f26cbf3909ab60f9fb3b357743142d`  
		Last Modified: Thu, 04 Dec 2025 22:15:12 GMT  
		Size: 2.4 MB (2416825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f0aa5526e8fd06656908876e00f56f996ad9eb77113112491022a53fab50c00`  
		Last Modified: Thu, 04 Dec 2025 22:15:13 GMT  
		Size: 20.2 KB (20186 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:939a45448af57f506fb1519a88b1dc6a510e1c774e37ea424f91195383a97534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121221953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4bb20819185bda88538aa6f5ae1bff5ae9e0fc35f4c963fbb0a4ce4926dc51c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:39:01 GMT
ENV container oci
# Wed, 03 Dec 2025 20:39:02 GMT
COPY dir:f4ea265792475a3d4d1f704e5646b6b392f1a575aee1ff63417d34e28530c8cb in /      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:39:02 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:03 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:38:45Z" "org.opencontainers.image.created"="2025-12-03T20:38:45Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:38:45Z
# Thu, 04 Dec 2025 19:47:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Dec 2025 19:47:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 19:47:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 Dec 2025 19:47:10 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 04 Dec 2025 19:47:10 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 04 Dec 2025 19:47:14 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 04 Dec 2025 19:47:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 04 Dec 2025 19:47:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:47:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:15f4b55884339bddb52ca0550d5b1208576ecf31649e067b468dc4e7b90745bd`  
		Last Modified: Wed, 03 Dec 2025 22:01:09 GMT  
		Size: 38.2 MB (38222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86afca07fc3331adbdb959de3ed8988dbe83f597d8bdc4c8e8eadd04dc8176d1`  
		Last Modified: Thu, 04 Dec 2025 19:47:29 GMT  
		Size: 30.9 MB (30855563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2474460ad6b1b61bfd01d8e83eab05cf2f43b703c8282f674cb3f450af0566c7`  
		Last Modified: Thu, 04 Dec 2025 19:47:29 GMT  
		Size: 52.1 MB (52141149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7681ccb01c9090bd40d51b034a1224f5029463acc597f9487612dfe33cd635d`  
		Last Modified: Thu, 04 Dec 2025 19:47:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2ed399970939ffebdf20b329b011aafb637c6ec1016b7513a7a6d4701765b3`  
		Last Modified: Thu, 04 Dec 2025 19:47:27 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9fc54043c0d3334079b0e6e9612daac7c8d26feb4c2c8e0e83a9ed5f0eecc6e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2436473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84868c1f88e998d5fb2a5e3dc6b8b308b0cb6b3fd7b0f22d3448704880a80d4a`

```dockerfile
```

-	Layers:
	-	`sha256:ff375bbf958ad695cd76ab035dd1b3b02204287773dc9fc78d6d0e8fbf75aa29`  
		Last Modified: Thu, 04 Dec 2025 19:47:28 GMT  
		Size: 2.4 MB (2416183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dd1b9dbf7fcf11a11203908f6f820269f5702ed4513f12387e4e670e375627d`  
		Last Modified: Thu, 04 Dec 2025 22:15:18 GMT  
		Size: 20.3 KB (20290 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:53ee358f0a16e60fddd2ae02f0adac7063f9389350d4bc9b2affad0c7858fae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130316485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b923965ae3803be064dabe689f36064a3ebc1e0b20bbfa7cfac529abde44533`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:38:00 GMT
ENV container oci
# Wed, 03 Dec 2025 20:38:01 GMT
COPY dir:1944394b2cb85c8bd1da6ad676bb75b09725617f627438630bb53946c4695c4a in /      
# Wed, 03 Dec 2025 20:38:01 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:38:01 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:38:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:38:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:38:01 GMT
COPY file:e9df47e0f73aa3fdb7704b0b5f90208619f4101460f662007af9ba5df5a06a9e in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:38:01 GMT
COPY file:e9df47e0f73aa3fdb7704b0b5f90208619f4101460f662007af9ba5df5a06a9e in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:38:01 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:37:49Z" "org.opencontainers.image.created"="2025-12-03T20:37:49Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:37:49Z
# Thu, 04 Dec 2025 19:45:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Dec 2025 19:45:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 19:45:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 Dec 2025 19:45:52 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 04 Dec 2025 19:45:52 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 04 Dec 2025 19:50:22 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 04 Dec 2025 19:50:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 04 Dec 2025 19:50:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:50:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0dbaabed7cc8118dfa57a21ab03f83f55ba784110782e2081afc710ef3eb3c16`  
		Last Modified: Thu, 04 Dec 2025 00:10:07 GMT  
		Size: 44.4 MB (44445850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbc041c92aa38c134e96bedbac7c177760045bc5616488fd3fda3e26cca1a60`  
		Last Modified: Thu, 04 Dec 2025 19:46:52 GMT  
		Size: 32.9 MB (32890492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776652420483997a3700bd26bfbf7e59eca68b23c16fc50f745ea52b72457f26`  
		Last Modified: Thu, 04 Dec 2025 19:51:11 GMT  
		Size: 53.0 MB (52977727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9ac015d8877f67d40d1e78416c30f5a6618e5a3826dac8ea05a5b2c938a6b7`  
		Last Modified: Thu, 04 Dec 2025 19:51:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3517ba047c6cc547d1808956171258123fd8f5cc83001affc766c23637bb114f`  
		Last Modified: Thu, 04 Dec 2025 19:51:00 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:fbcc5fc86ee19542ce245180984836e727d3b39280eb6aeb7e55ac0b335e3298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2437046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4f2775486e699388508e8b0398af52f5f01f4456a761d7f63a42e58fb6f282`

```dockerfile
```

-	Layers:
	-	`sha256:5f5a8566deac2fcd5bb855c5f7294d9b88075224343d2ab112fa11a07b906e81`  
		Last Modified: Thu, 04 Dec 2025 22:15:22 GMT  
		Size: 2.4 MB (2416830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebfcdfd1567fcf88d2f65ced05e182e48ca31497c9f9f7eb0d32f1eebfd9d5bc`  
		Last Modified: Thu, 04 Dec 2025 19:50:53 GMT  
		Size: 20.2 KB (20216 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:3853316229206584928821bcdfe14c815006edf80d5f584cfd78fd651e7cc21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 MB (118097434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f6aa9901bdad730ccbdffaac62f7ed448606d786c3da3439264d268638ffc9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:42:43 GMT
ENV container oci
# Wed, 03 Dec 2025 20:42:44 GMT
COPY dir:10eb0792500239f5e33d6b6b7941aff62593a46d7fd8ece7d8112154ea3105b1 in /      
# Wed, 03 Dec 2025 20:42:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:42:44 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:42:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:42:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:42:44 GMT
COPY file:f78d6df7f6c9ff8f12b4cd77c81f39d3e176ca1a669ebe7b8a04c5beb6be6145 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:42:44 GMT
COPY file:f78d6df7f6c9ff8f12b4cd77c81f39d3e176ca1a669ebe7b8a04c5beb6be6145 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:42:44 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:42:32Z" "org.opencontainers.image.created"="2025-12-03T20:42:32Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:42:32Z
# Thu, 04 Dec 2025 19:45:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Dec 2025 19:45:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 19:45:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 Dec 2025 19:45:21 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 04 Dec 2025 19:45:21 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 04 Dec 2025 19:47:22 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 04 Dec 2025 19:47:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 04 Dec 2025 19:47:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:47:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:8d6bf9619dce2b1902cecb7448c5bfe74272c22bbdc9eb02a2de550b72a7db66`  
		Last Modified: Thu, 04 Dec 2025 00:10:07 GMT  
		Size: 38.1 MB (38133803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a3cda5dd8ae3511f3b35c8c9ad509e28a2da6fc8f4fb3e8d565916bb0ff715`  
		Last Modified: Thu, 04 Dec 2025 19:46:22 GMT  
		Size: 30.4 MB (30445236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5432fa7c3fe5fc5df9a945604a858a2bd703646d2732fec0fce72688baad760e`  
		Last Modified: Thu, 04 Dec 2025 19:48:00 GMT  
		Size: 49.5 MB (49515977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af3de61707ca5c8504fbfe549574966a78f4c19dc8adb31353a6d90d1120fda`  
		Last Modified: Thu, 04 Dec 2025 19:47:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7126e9506504ceebb84709b8dcaece46313dfd2b5781cebfd391c214404e5e`  
		Last Modified: Thu, 04 Dec 2025 19:47:48 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3c93078976ccc3aeb8915353304b00cfe2292e0ac160a11bbd3e867ba9454734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2428803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32159d76040332e737410e59d6a74e7ea30eeb779f93ba26e5d95d12bd671f2f`

```dockerfile
```

-	Layers:
	-	`sha256:35e6c6e4425e3db7fdf69c30717d4e4d93a15b42f077f4e837916a839e73f124`  
		Last Modified: Thu, 04 Dec 2025 22:15:26 GMT  
		Size: 2.4 MB (2408617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f6905240e2b099e4e8006d24a13feeee6bf794ef66f8965bd0e45e9b33aad23`  
		Last Modified: Thu, 04 Dec 2025 22:15:27 GMT  
		Size: 20.2 KB (20186 bytes)  
		MIME: application/vnd.in-toto+json
