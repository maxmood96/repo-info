## `eclipse-temurin:25-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:a5f01384ee4d1bcb60717ddd39830671bc62a6f5dd6a731f4af984c543bc4fcd
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

### `eclipse-temurin:25-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:5a44d407e019ae3e9dad7d409c6c2e12161c09247e074d210d43b0568d10410c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165171051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d722343fc23e9b2bd645412d4b1f6b7bd766596c518cd5d93520524774e3fef`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Tue, 02 Jun 2026 22:45:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 22:45:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:45:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 22:45:04 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:45:04 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 02 Jun 2026 22:45:44 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 02 Jun 2026 22:45:46 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:45:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:45:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 22:45:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e4e3984c47d80f8f7813d099ea4505637390207a530acceb3e7426232f7555a`  
		Last Modified: Tue, 02 Jun 2026 16:41:21 GMT  
		Size: 34.8 MB (34839018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4d84aed04ebeb926295e10e148d4245732f5b436e33e54dd0d68d059a3851f`  
		Last Modified: Tue, 02 Jun 2026 22:45:30 GMT  
		Size: 37.8 MB (37750224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56a0771af24173ca972966dd453f9bb6c023e2da9edd11433f295dfaa1d2fae`  
		Last Modified: Tue, 02 Jun 2026 22:46:04 GMT  
		Size: 92.6 MB (92579387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4991da7f206639a221bd6073b3450272036b2bff010494982f5df9515cdb7be`  
		Last Modified: Tue, 02 Jun 2026 22:46:02 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5168f8a56c6106709ccc3a2330fdc326e7fda272f13d17c0b7f64752008e0b1f`  
		Last Modified: Tue, 02 Jun 2026 22:46:02 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3ae207c780accfcf4dfe1c9f1c09fde3a3f1770fcc6062d6cea1198531058ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3781018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f52aead6df7fc1c13142292797a562e9065845c2f084bf349aa35664df9ad8`

```dockerfile
```

-	Layers:
	-	`sha256:6dcedf7762253b6c8ebc000fa40a5d17c3e4226dd7e583b82d1fd1c4653ec125`  
		Last Modified: Tue, 02 Jun 2026 22:46:02 GMT  
		Size: 3.8 MB (3759729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87abb28978907d412de91f930698a02465813c95c843470580e631e33abe7269`  
		Last Modified: Tue, 02 Jun 2026 22:46:02 GMT  
		Size: 21.3 KB (21289 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:ff91a7f7776283d46cbc53dac3cb1b744c4d0f51bbace93672a0d6377cdee415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162272279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d767d130450061da6b6f048830d4999f3b0d2ddfeb1b4c99488c10b807f898`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Tue, 02 Jun 2026 22:45:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 22:45:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:45:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 22:45:16 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:45:16 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 02 Jun 2026 22:45:22 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 02 Jun 2026 22:45:24 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:45:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:45:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 22:45:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7cd594d4c3afe0f66eb7cfc2a31b3e461f371776f986ab3d5084853335f5d2f7`  
		Last Modified: Tue, 02 Jun 2026 16:41:21 GMT  
		Size: 33.0 MB (33037428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50232bcad074818340230169aa55eb72bf5f1b0e17577a1cc8673c4417fb4fec`  
		Last Modified: Tue, 02 Jun 2026 22:45:43 GMT  
		Size: 37.7 MB (37683551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41631ef79ffd67b296b8978584b8e20d77fcfdb3e2f76d53d43ea8cdec64b77`  
		Last Modified: Tue, 02 Jun 2026 22:45:44 GMT  
		Size: 91.5 MB (91548881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba29cac0c53692d82faa7db39004d0d2f219e004525d38aac97a66dc3cdbd14`  
		Last Modified: Tue, 02 Jun 2026 22:45:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0675f6b7f602655a4093114ae2172823deb4f3d26e05df12121f0bb5588ec7ef`  
		Last Modified: Tue, 02 Jun 2026 22:45:41 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6c0c12745d10a07866d2808927c564efc9d55139e78e26796613b81877035922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3780557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ee35724d196cfa8f5106c49f1180c97e2eddc331885c5f6a16c837a8473f50`

```dockerfile
```

-	Layers:
	-	`sha256:1ceed6027091f9f2eadfa952557797b5587b4bec6227cd90282b0b662fd8f705`  
		Last Modified: Tue, 02 Jun 2026 22:45:41 GMT  
		Size: 3.8 MB (3759152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:677e118b0afb5aad89fedc06e2a513f61356c7575e3f77224d7f44a008dc16ed`  
		Last Modified: Tue, 02 Jun 2026 22:45:41 GMT  
		Size: 21.4 KB (21405 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:35b083cab66769967ab99dca88cfe7dd84107c11e47af2a783f26084de8b9585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170407722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:948d8e8fedd7201e93e8f778ed1340c26361f579c3d37903f32bb872eb157dd5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 02 Jun 2026 22:56:43 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 02 Jun 2026 22:56:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:57:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:57:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 22:57:00 GMT
CMD ["jshell"]
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
	-	`sha256:ba0cc110866c6e1771efade89d886c61705ec38a881ffcf9b840d71f95d2fde4`  
		Last Modified: Tue, 02 Jun 2026 22:57:51 GMT  
		Size: 91.9 MB (91912874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754a218980abf4d546edbb90e4f5b3d5bcb152c901ef745ba40689911dc097c9`  
		Last Modified: Tue, 02 Jun 2026 22:57:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b78fed1b9f14444173779c3bb65fdf6a7911e4d4a340fd928444b8fe0db441b`  
		Last Modified: Tue, 02 Jun 2026 22:57:49 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:04698d10b47ef7ceab86355d5d16aa920044bb9c33546e8f9a9c11574f2a35a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3751198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11107e1543c581212f6b0be44514cf23ec76a2d92f9ff945e17efb7b839417cb`

```dockerfile
```

-	Layers:
	-	`sha256:cb56ad4bf906e7b38b59d07ec55c69c74d8f863ab5870b0a443d3d3a8e7f358e`  
		Last Modified: Tue, 02 Jun 2026 22:57:49 GMT  
		Size: 3.7 MB (3729873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f0c4a37f693e8bc5a2979474f3e2ee5dd6ade2cbdb847d083717ee44906ac37`  
		Last Modified: Tue, 02 Jun 2026 22:57:49 GMT  
		Size: 21.3 KB (21325 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:713b2cc0802efed91546e3eab0643b40ad96350a3c22fb633f4eb881aef1d8ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161270851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959faac6e9c020cf9b66e4f0e83e5d12d7c21e7887f27a1792a19ab1dca20cfc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 02 Jun 2026 22:46:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 02 Jun 2026 22:46:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:46:07 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:46:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 22:46:07 GMT
CMD ["jshell"]
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
	-	`sha256:a346df19e04ca8d7a5f78e398528028240a7f2e6e2e3e05ed7f34c0cfe40251a`  
		Last Modified: Tue, 02 Jun 2026 22:46:34 GMT  
		Size: 88.4 MB (88421666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa1b09dacae7309c474af6158f6674c370291f863150cffe1c639038a9cc8ef`  
		Last Modified: Tue, 02 Jun 2026 22:46:32 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfa84752b22510e487d178caec3c7447b6bac4480f071eebbfbd4699a1c64d8`  
		Last Modified: Tue, 02 Jun 2026 22:46:32 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8b384feded4f6d47f90c800f3d7f996af8d3ab2920bb65938e42617c1cc2c89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3751170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356a9bc3de3ded0a37e786f865c6446874e7d53ed74ad618822e195ec479913c`

```dockerfile
```

-	Layers:
	-	`sha256:108a3531703a483aa5a5b91691ee654b8b498d9c220cc838609bfd0a928d2a40`  
		Last Modified: Tue, 02 Jun 2026 22:46:32 GMT  
		Size: 3.7 MB (3729881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0cd8dc2f680407bdbcf11d05c484be5a4ef71e91b63c6869a79d948009d23a1`  
		Last Modified: Tue, 02 Jun 2026 22:46:32 GMT  
		Size: 21.3 KB (21289 bytes)  
		MIME: application/vnd.in-toto+json
