## `eclipse-temurin:11-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:b10f705c8c6e71e00cc245d35e0e6ccb982111cd297085dc426603be9ac59c88
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

### `eclipse-temurin:11-jdk-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:ca676a75c5f3f39e0c234ced1267752e52f4dd25ead247e030f6eafe49ae11d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214940627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10dc2aea4c798fb2333699902ec301002982d1acaf060f1e386ee4081849f740`
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
# Tue, 02 Jun 2026 22:44:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 22:44:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:44:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 22:44:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:44:57 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 02 Jun 2026 22:45:03 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 02 Jun 2026 22:45:04 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:45:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:45:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 22:45:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e4e3984c47d80f8f7813d099ea4505637390207a530acceb3e7426232f7555a`  
		Last Modified: Tue, 02 Jun 2026 16:41:21 GMT  
		Size: 34.8 MB (34839018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9329f5480ca158de4e6f3787636b2c40a116ee8cc41509132c3c9380f22295`  
		Last Modified: Tue, 02 Jun 2026 22:45:23 GMT  
		Size: 37.8 MB (37750317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3f9068cfdcc46a623dd7084e10f238ce895c641068f92ce0a8d6f504d9ca5b`  
		Last Modified: Tue, 02 Jun 2026 22:45:26 GMT  
		Size: 142.3 MB (142348876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436f06bf3960ba04c9e4360e631e8384ac7a527beadc159fca82f467babb23fd`  
		Last Modified: Tue, 02 Jun 2026 22:45:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56ec8f88c4ad618d3865995bac44d74fca53ceb6acfc6ef7c9dfa2fdd646371`  
		Last Modified: Tue, 02 Jun 2026 22:44:58 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7a0ad6cdcc4b88fc6d80de30516fffa4e4b33bb66aa57dc7586bf720cdac1b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0682b91834b927275d667fdfe0be599bfae3fd0b4a0b71b12b7518ec447088f3`

```dockerfile
```

-	Layers:
	-	`sha256:969a864a23fe41918625773f5048fa7821f7f8af08dfec2d0a1c7069ba3a1143`  
		Last Modified: Tue, 02 Jun 2026 22:45:21 GMT  
		Size: 3.8 MB (3811230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93c515f3c7868aec9e9aad12a03af8fde9cf71d81488034acb8adf8680287421`  
		Last Modified: Tue, 02 Jun 2026 22:45:21 GMT  
		Size: 21.3 KB (21339 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:636465111e5a709b76b31f1286a06f55288ec10bddbdec5eb54215cc4cf64927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209786491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e682b25d7d5af1f75b8c7f57a64c9e3bbe8e0f5861fcb94b916c662a43ce94a7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 27 May 2026 06:14:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 May 2026 06:14:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 27 May 2026 06:14:32 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 27 May 2026 06:14:32 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 27 May 2026 06:14:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 May 2026 06:14:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 27 May 2026 06:14:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:14:32 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:14:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 27 May 2026 06:14:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 May 2026 06:14:32 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 27 May 2026 06:14:32 GMT
ENV container oci
# Wed, 27 May 2026 06:14:33 GMT
COPY dir:144798cc4c14efe6d25c10c7a6f149af1045784afd86a94e99d04f534f9bbb05 in /      
# Wed, 27 May 2026 06:14:33 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 27 May 2026 06:14:33 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 06:14:33 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 27 May 2026 06:14:33 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 27 May 2026 06:14:33 GMT
COPY file:83615dc098d46f372c6688f68025f354351bfbb3ed132d56c889042d90463ecf in /usr/share/buildinfo/labels.json      
# Wed, 27 May 2026 06:14:34 GMT
COPY file:83615dc098d46f372c6688f68025f354351bfbb3ed132d56c889042d90463ecf in /root/buildinfo/labels.json      
# Wed, 27 May 2026 06:14:34 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "org.opencontainers.image.revision"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "build-date"="2026-05-27T06:14:17Z" "org.opencontainers.image.created"="2026-05-27T06:14:17Z" "release"="1779862102"org.opencontainers.image.revision=3aa29655e860e8f28ee9014c3803f132b3b1e65d,org.opencontainers.image.created=2026-05-27T06:14:17Z
# Wed, 27 May 2026 22:37:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 May 2026 22:37:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 22:37:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 May 2026 22:37:22 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 27 May 2026 22:37:22 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 27 May 2026 22:37:28 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 27 May 2026 22:37:29 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 May 2026 22:37:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 May 2026 22:37:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 27 May 2026 22:37:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:94a14999202bc800f78441edfa1b48a3f6b5a799655652a41a4ef92004acb9c3`  
		Last Modified: Wed, 27 May 2026 07:33:15 GMT  
		Size: 33.1 MB (33062079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28de4c1a48524825d270278fecd382ad76e767fc60f8c0d398cf12f7c7878085`  
		Last Modified: Wed, 27 May 2026 22:37:48 GMT  
		Size: 37.7 MB (37681340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fe2e7743baf667ef2ae3b97b5a4cb90a80fc885e4ac2cfe77ca202b4ff09bc`  
		Last Modified: Wed, 27 May 2026 22:37:51 GMT  
		Size: 139.0 MB (139040653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572c5e0af4510617406717cba2b3dc279b338963aa38dac88613259f72eea8bc`  
		Last Modified: Wed, 27 May 2026 22:37:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f7762ca9c2ab965d8ae4b50f555a482e3908f87f10f97a2c91c4b49a4ac663`  
		Last Modified: Wed, 27 May 2026 22:37:47 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:bc919ecd5434a21e493dbc9df12e78bdc4ea476276a6928b53231e2ee11e89da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695bf3a7f07e01b8dbba51cb94927defde592db0b132cb8c6997494f39e09815`

```dockerfile
```

-	Layers:
	-	`sha256:d68f392674995ddbd5beb5997b9eeed1acc1014af527304a33cb84aebb39bfe1`  
		Last Modified: Wed, 27 May 2026 22:37:47 GMT  
		Size: 3.8 MB (3811274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:253b874d0a456842b2766b59347a9ef8077eaf2e3330ebbf7f0dabc1911cc43f`  
		Last Modified: Wed, 27 May 2026 22:37:47 GMT  
		Size: 21.5 KB (21455 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:19421fd9433364cfad5468807339d9e8a191ebfb39cfda5e57760728a0e97742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208109102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33e9fe395ac3dbafee86bc3bed8adc0ea6cd3db9d5812bf9e947dd4330e89fe`
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
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 02 Jun 2026 22:46:56 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 02 Jun 2026 22:46:58 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:46:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:46:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 22:46:59 GMT
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
	-	`sha256:7f80eea15afd9831c6cbec9bf6971f81a5ca574792b960dae8137cf6457d84fd`  
		Last Modified: Tue, 02 Jun 2026 22:47:34 GMT  
		Size: 129.6 MB (129614253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8051a46e0cbf678978356b6ffa47bdb8fdbc0acab3671d3fa62a3ccffc74c5`  
		Last Modified: Tue, 02 Jun 2026 22:47:31 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5457a4f265c225936eac00b04c7b0cada5b778fdb7d88abe3b29228ae35575cc`  
		Last Modified: Tue, 02 Jun 2026 22:47:31 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e83276ce72827b84412538d4d748b73f0b3d8cf0f960051ee949883fdff0c43b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3818823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e628d71950be4d5f5a6d5c52baba11ba0990ef2eff12fba9d5b2fce5cca2d47b`

```dockerfile
```

-	Layers:
	-	`sha256:b3313b811995e76c5d8fb060d7662a521da07a004912a97c1b7d4ea920ac7781`  
		Last Modified: Tue, 02 Jun 2026 22:47:31 GMT  
		Size: 3.8 MB (3797447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c978c4e54086b7b2d498b85da76396eda2449cf93ab0927611f7dfe9921d33f3`  
		Last Modified: Tue, 02 Jun 2026 22:47:31 GMT  
		Size: 21.4 KB (21376 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:42b31599af7daeff7d0138b5aba1b8edca5fb19b6a1e6baf1ae7ef483e1a1569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195910609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:148a17983bc716b90bcdecccf50917bbf78af5ecf368bb0033712ac2f84d593b`
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
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 02 Jun 2026 22:43:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 02 Jun 2026 22:43:29 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:43:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:43:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 22:43:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:017341eabcfbc3839e70d99b30c5183e8f03952ba5046a4c9b68b4eff2e3021c`  
		Last Modified: Tue, 02 Jun 2026 18:16:12 GMT  
		Size: 34.7 MB (34725456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f99f5fdbd0efcba737483fb022a1ed4d27951717662c4abc8e0338234458978`  
		Last Modified: Tue, 02 Jun 2026 22:43:55 GMT  
		Size: 38.1 MB (38121333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a0f1116d802a3cf7f65f72850824ffab9c95ab8e03ca7a9366a5e577e6be3c`  
		Last Modified: Tue, 02 Jun 2026 22:43:57 GMT  
		Size: 123.1 MB (123061400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721387bb34c02db0e64f9dd1f566dfc3f17845dee3dfbcbab94b989508a46fc3`  
		Last Modified: Tue, 02 Jun 2026 22:43:54 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcef074faf5c8f7d13c8b54c8a798f31c3f347ec093d1f852dda64f73d262705`  
		Last Modified: Tue, 02 Jun 2026 22:43:54 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a8dddcc34c2b2b91e14c989752f7eb214ac6549b8b449bdebb4dba307de43781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3818164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433db025e28358a45914f7ef27b8640991c3cc10707537e4e5a30614fe0d2d63`

```dockerfile
```

-	Layers:
	-	`sha256:4b978a8fc731f931aad07d84424f024e6fc5fab2480b3e84153d510ebd6b3878`  
		Last Modified: Tue, 02 Jun 2026 22:43:54 GMT  
		Size: 3.8 MB (3796824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98df642d3fb0297dba4720bba4680ba7ce034f79f3f67ea556a6877b6884e934`  
		Last Modified: Tue, 02 Jun 2026 22:43:54 GMT  
		Size: 21.3 KB (21340 bytes)  
		MIME: application/vnd.in-toto+json
