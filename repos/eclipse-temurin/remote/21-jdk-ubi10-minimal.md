## `eclipse-temurin:21-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:ed8cd615a065ca145e812c860cc3a2ea086f422e72918d3e0cda401adc227035
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

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:68e158aecccb6b133cb9baf57c0d6e1e0175b8159d5d16a33a3e8f2c7cacb0eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229940333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10ccc27d1ac8b6e32411122fef922b74d1c658325c22c78a5b785550e04c743`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL io.openshift.expose-services=""
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 23 Mar 2026 01:13:56 GMT
ENV container oci
# Mon, 23 Mar 2026 01:13:56 GMT
COPY dir:e4512bf3738a47eefff7ab81e82e38ca2f5173e43ee99a65e6dd13d89e02bd8f in /      
# Mon, 23 Mar 2026 01:13:56 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 23 Mar 2026 01:13:57 GMT
CMD ["/bin/bash"]
# Mon, 23 Mar 2026 01:13:57 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 23 Mar 2026 01:13:57 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 23 Mar 2026 01:13:57 GMT
COPY file:0abc55831e7dab59520989ee7f9e642cfb86d0399f7103e87f7378145dd94508 in /usr/share/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:13:57 GMT
COPY file:0abc55831e7dab59520989ee7f9e642cfb86d0399f7103e87f7378145dd94508 in /root/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:13:57 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "org.opencontainers.image.revision"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "build-date"="2026-03-23T01:13:42Z" "org.opencontainers.image.created"="2026-03-23T01:13:42Z" "release"="1774228210"org.opencontainers.image.revision=5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6,org.opencontainers.image.created=2026-03-23T01:13:42Z
# Mon, 23 Mar 2026 18:16:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 23 Mar 2026 18:16:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:16:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 23 Mar 2026 18:16:54 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 23 Mar 2026 18:16:54 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Mon, 23 Mar 2026 18:17:25 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 23 Mar 2026 18:17:26 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 23 Mar 2026 18:17:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 23 Mar 2026 18:17:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 23 Mar 2026 18:17:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2979ea27473f21e894361ff5d915252c378d4a8073aca3908465bbbf348780b7`  
		Last Modified: Mon, 23 Mar 2026 03:10:44 GMT  
		Size: 34.6 MB (34630234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d43402aa5dff2577649e157573b815706c0b1d85d0711264fd7ff5d8c88755f`  
		Last Modified: Mon, 23 Mar 2026 18:17:12 GMT  
		Size: 37.4 MB (37446632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaccea5b6d0d6183e38a5545a76df5b910b995ec93a3f0e0e6d737b33cbb5ec2`  
		Last Modified: Mon, 23 Mar 2026 18:17:46 GMT  
		Size: 157.9 MB (157861048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4bc04c531b62b7483dd9b9e311d2f913e96fba14d54f5ee9b02156b80ab215`  
		Last Modified: Mon, 23 Mar 2026 18:17:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd9a2be913e863b70239e83e0e88233e10261155afa913abd0ebecac6e492a9`  
		Last Modified: Mon, 23 Mar 2026 18:17:43 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a7f0806091f25c1d49bfeb3a2b5bc8cfccb2911ecfe9779d8843d20ae820cc79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3812941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8d9b32009284d6aa921924bd16a16bd32e597096f5ca5674c688175f836536`

```dockerfile
```

-	Layers:
	-	`sha256:f66df9cc625f58950d8d8901e5f7cb105dc0879355d286b7e4906fc6cdf4edc8`  
		Last Modified: Mon, 23 Mar 2026 18:17:43 GMT  
		Size: 3.8 MB (3791625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ac7de8cc48dd438e06f23e3dafb7337e123519ed3b1d07498c5c80ff079727f`  
		Last Modified: Mon, 23 Mar 2026 18:17:43 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:4495936951113eac5d234706ce8c29a5e464841e2c5d746b9c27787f658efe64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.2 MB (226214094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34f44d96f420dacbdb39b0337532167509bd34e1198399ba2684d2fbbfa4cd0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL io.openshift.expose-services=""
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 23 Mar 2026 01:17:03 GMT
ENV container oci
# Mon, 23 Mar 2026 01:17:04 GMT
COPY dir:5423a2d232cda7a57202522795efee6ca78fcc0651e41ab821993b780fdf8627 in /      
# Mon, 23 Mar 2026 01:17:04 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 23 Mar 2026 01:17:04 GMT
CMD ["/bin/bash"]
# Mon, 23 Mar 2026 01:17:04 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 23 Mar 2026 01:17:05 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 23 Mar 2026 01:17:05 GMT
COPY file:c5d7f4f2dd90b98f707a017338d65e0949c625a6c68e260ee9a0d4613ffd89fd in /usr/share/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:17:05 GMT
COPY file:c5d7f4f2dd90b98f707a017338d65e0949c625a6c68e260ee9a0d4613ffd89fd in /root/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:17:05 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "org.opencontainers.image.revision"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "build-date"="2026-03-23T01:16:47Z" "org.opencontainers.image.created"="2026-03-23T01:16:47Z" "release"="1774228210"org.opencontainers.image.revision=5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6,org.opencontainers.image.created=2026-03-23T01:16:47Z
# Mon, 23 Mar 2026 18:16:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 23 Mar 2026 18:16:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:16:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 23 Mar 2026 18:16:28 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 23 Mar 2026 18:16:28 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Mon, 23 Mar 2026 18:17:03 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 23 Mar 2026 18:17:04 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 23 Mar 2026 18:17:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 23 Mar 2026 18:17:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 23 Mar 2026 18:17:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cbfdca2ca63ac63914141abb4cb933134b748fc3efb6e835daea267d6feb9296`  
		Last Modified: Mon, 23 Mar 2026 03:33:50 GMT  
		Size: 32.7 MB (32686471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435285a49d1d7ff7d5a5e281789cff8601b17dd7af100248370e5f96ecb6d2fc`  
		Last Modified: Mon, 23 Mar 2026 18:16:48 GMT  
		Size: 37.4 MB (37388993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fd9315b54040b6fb913a2ed1f075954c4cba8861624927e9583efaf3c2bd15`  
		Last Modified: Mon, 23 Mar 2026 18:17:25 GMT  
		Size: 156.1 MB (156136208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de72c5f5cac7b036c1989ceec1e88e7e834815291719e9b53a5284fb39435e2`  
		Last Modified: Mon, 23 Mar 2026 18:17:21 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487b55eb8e37c2373b3d6a9ab8a33fa1ff45122bc630d9ec38a22f8058fe71ee`  
		Last Modified: Mon, 23 Mar 2026 18:17:21 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:30d670f2473b35c16c058d48d081fd3f2869b87c5ae05860dd5f8b1254c3b5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3812483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0096ba022f532d8b38844c67876d6cb6b197418e26f3759e6d342555fd8083ce`

```dockerfile
```

-	Layers:
	-	`sha256:c4cbe441b77b32febe0df4b0177a4ad80d9087b5f657498073fae5f970f995f7`  
		Last Modified: Mon, 23 Mar 2026 18:17:22 GMT  
		Size: 3.8 MB (3791051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b11fae92bbac6ea0c7030333bf6618a18d93a7144447b4e864c2f3cb9d6655f4`  
		Last Modified: Mon, 23 Mar 2026 18:17:21 GMT  
		Size: 21.4 KB (21432 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:77309ae8d79a4eb5608d2a3a9616174d68e88879cd8ace4afc8757085255c757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235911288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60bd8fc4702e776eb87f1b5c3bf5a314aa86f31ff7e5274fc721338bc43a59a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Mar 2026 01:15:45 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 23 Mar 2026 01:15:45 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 23 Mar 2026 01:15:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 23 Mar 2026 01:15:45 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 23 Mar 2026 01:15:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 23 Mar 2026 01:15:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 23 Mar 2026 01:15:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:15:46 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:15:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 23 Mar 2026 01:15:46 GMT
LABEL io.openshift.expose-services=""
# Mon, 23 Mar 2026 01:15:46 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 23 Mar 2026 01:15:46 GMT
ENV container oci
# Mon, 23 Mar 2026 01:15:46 GMT
COPY dir:6d632c778a00dcaccd2b27492019a49da2e9ded15d90cc220bd8ef2e111c01aa in /      
# Mon, 23 Mar 2026 01:15:46 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 23 Mar 2026 01:15:46 GMT
CMD ["/bin/bash"]
# Mon, 23 Mar 2026 01:15:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 23 Mar 2026 01:15:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 23 Mar 2026 01:15:47 GMT
COPY file:c49dc785bea5c076578ee2a5e8eb4e7290c033b08769d6c1e8e12f43990c44cc in /usr/share/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:15:47 GMT
COPY file:c49dc785bea5c076578ee2a5e8eb4e7290c033b08769d6c1e8e12f43990c44cc in /root/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:15:47 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "org.opencontainers.image.revision"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "build-date"="2026-03-23T01:15:34Z" "org.opencontainers.image.created"="2026-03-23T01:15:34Z" "release"="1774228210"org.opencontainers.image.revision=5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6,org.opencontainers.image.created=2026-03-23T01:15:34Z
# Mon, 23 Mar 2026 18:25:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 23 Mar 2026 18:25:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:25:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 23 Mar 2026 18:25:02 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 23 Mar 2026 18:25:02 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Mon, 23 Mar 2026 18:28:07 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 23 Mar 2026 18:28:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 23 Mar 2026 18:28:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 23 Mar 2026 18:28:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 23 Mar 2026 18:28:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6b71f50ac5496b49a24d4e0868fe8e453f93532ef823631b2317185af571b8e7`  
		Last Modified: Mon, 23 Mar 2026 06:15:15 GMT  
		Size: 38.7 MB (38727029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c8eaa293db94961782c260ece22ece0b24bab37073f3fe6b143b29d7b188a9`  
		Last Modified: Mon, 23 Mar 2026 18:25:46 GMT  
		Size: 39.2 MB (39200511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033cd42a963879487b806b64bba62aa39e49e02fd7d4b12b20a94bcf915a08f3`  
		Last Modified: Mon, 23 Mar 2026 18:28:51 GMT  
		Size: 158.0 MB (157981330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4f08aa48eb773407ebf54680e19958b5b6fcb96be29c1c015b0eb7c4fec2a9`  
		Last Modified: Mon, 23 Mar 2026 18:28:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86348be9c478f49e5b215efd487b7961930aaede67ef2fad22913c8c94ec0296`  
		Last Modified: Mon, 23 Mar 2026 18:28:47 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:cd21e0810088987d0a5cba6bf4685e808ad465ad0449c4fab99ba44457a3f129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3799809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4478abeff792e7ea50cadc35b200c019b103d1f5582e567127dc095fa29d2f59`

```dockerfile
```

-	Layers:
	-	`sha256:e680764edab9db9fbee9761c6e6318d2c550c595237c27a0ad782711dae4af44`  
		Last Modified: Mon, 23 Mar 2026 18:28:48 GMT  
		Size: 3.8 MB (3778457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb772c1a401e811c9414779920c915f2de491049330f8b2e3ca1c106d8e76f71`  
		Last Modified: Mon, 23 Mar 2026 18:28:47 GMT  
		Size: 21.4 KB (21352 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:cfcd3a677b676c533ad33dd2780621e24b89da693db71566e100926bd345ff74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219364555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c799e164e005d0a496c3e41155001d284b22de13222c2673a000ef17faf9e491`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL io.openshift.expose-services=""
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 23 Mar 2026 01:50:52 GMT
ENV container oci
# Mon, 23 Mar 2026 01:50:53 GMT
COPY dir:a20807155e5dba5b4fe6159d124b2858e52124008e54fbaacb8e89f074571573 in /      
# Mon, 23 Mar 2026 01:50:53 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 23 Mar 2026 01:50:53 GMT
CMD ["/bin/bash"]
# Mon, 23 Mar 2026 01:50:53 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 23 Mar 2026 01:50:53 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 23 Mar 2026 01:50:53 GMT
COPY file:f444544eabeceb45eb54e7d25741c29001ce8ceeb34cf764e4e6f1bae0509e32 in /usr/share/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:50:53 GMT
COPY file:f444544eabeceb45eb54e7d25741c29001ce8ceeb34cf764e4e6f1bae0509e32 in /root/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:50:53 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "org.opencontainers.image.revision"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "build-date"="2026-03-23T01:50:09Z" "org.opencontainers.image.created"="2026-03-23T01:50:09Z" "release"="1774228210"org.opencontainers.image.revision=5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6,org.opencontainers.image.created=2026-03-23T01:50:09Z
# Mon, 23 Mar 2026 18:13:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 23 Mar 2026 18:13:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:13:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 23 Mar 2026 18:13:09 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 23 Mar 2026 18:13:09 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Mon, 23 Mar 2026 18:13:15 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 23 Mar 2026 18:13:16 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 23 Mar 2026 18:13:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 23 Mar 2026 18:13:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 23 Mar 2026 18:13:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c4143dec68dd3a33451fd532f787cf2f31d86a312b4b1a8a58cadb88900ac88`  
		Last Modified: Mon, 23 Mar 2026 06:15:08 GMT  
		Size: 34.4 MB (34429605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afaeb08174d6252e90dd2ef49bcd22e4089aa0abd5c05e34ae09915fe72186b`  
		Last Modified: Mon, 23 Mar 2026 18:13:32 GMT  
		Size: 37.8 MB (37827698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0865d8c15e1545531b39cd6ad4dc4a5e94d5fc78f7983013116452b1e02bff28`  
		Last Modified: Mon, 23 Mar 2026 18:13:45 GMT  
		Size: 147.1 MB (147104833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1688d35a1a800f796044a2b35bd9a1c1248cc68741bec1802bde539a3a6225da`  
		Last Modified: Mon, 23 Mar 2026 18:13:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212274e809c5f4cac5262b9097141bd21e0472329d1f84deb27fd854d0556e55`  
		Last Modified: Mon, 23 Mar 2026 18:13:41 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:023b751a85f42454a95ee598bf8d42aa542e822e6de981caa6041531edde58f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3798531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44fa168e0d7ca0b400c789accf3ed90fb62022ac9a9af2a4721780c48bb43dcb`

```dockerfile
```

-	Layers:
	-	`sha256:3177744f473edce55a77c3d0614a9a47121aa10e05931d1fc7469e2d022426a2`  
		Last Modified: Mon, 23 Mar 2026 18:13:41 GMT  
		Size: 3.8 MB (3777215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c313375f2ede8c75b3031e5a4d98392ba6063935770a787312474ec5382f8f62`  
		Last Modified: Mon, 23 Mar 2026 18:13:41 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json
