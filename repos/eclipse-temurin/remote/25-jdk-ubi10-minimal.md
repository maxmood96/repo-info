## `eclipse-temurin:25-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:7e12f07be70811528a4c8ae483b117f39e5b721f880600d7b0cb88ec869fbf80
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

### `eclipse-temurin:25-jdk-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:b386182257505f51a4aeedef89bdfcd4691b97fc46a60725acbd55e69331487b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165197034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b47f5f0ceb904535638d6312eade85eda562c4e6b06da4f46841ea56737d9a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL io.openshift.expose-services=""
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 04 Jun 2026 05:28:17 GMT
ENV container oci
# Thu, 04 Jun 2026 05:28:18 GMT
COPY dir:66f2b108fa49d46a69e413fb7db9e6ed9263f39ff05950d04e99329222ef439c in /      
# Thu, 04 Jun 2026 05:28:18 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 04 Jun 2026 05:28:18 GMT
CMD ["/bin/bash"]
# Thu, 04 Jun 2026 05:28:18 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 04 Jun 2026 05:28:18 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 04 Jun 2026 05:28:18 GMT
COPY file:fd262bedfa32870622b193d94f9285fa7e55dee323c33ad89ff9af707ddb8c11 in /usr/share/buildinfo/labels.json      
# Thu, 04 Jun 2026 05:28:18 GMT
COPY file:fd262bedfa32870622b193d94f9285fa7e55dee323c33ad89ff9af707ddb8c11 in /root/buildinfo/labels.json      
# Thu, 04 Jun 2026 05:28:18 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="21e748607cdf3bfe567bea40c2e0c654a3c7766c" "org.opencontainers.image.revision"="21e748607cdf3bfe567bea40c2e0c654a3c7766c" "build-date"="2026-06-04T05:28:04Z" "org.opencontainers.image.created"="2026-06-04T05:28:04Z" "release"="1780550715"org.opencontainers.image.revision=21e748607cdf3bfe567bea40c2e0c654a3c7766c,org.opencontainers.image.created=2026-06-04T05:28:04Z
# Fri, 05 Jun 2026 22:42:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 05 Jun 2026 22:42:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jun 2026 22:42:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 05 Jun 2026 22:42:52 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 05 Jun 2026 22:42:52 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Fri, 05 Jun 2026 22:43:21 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 05 Jun 2026 22:43:22 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 05 Jun 2026 22:43:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 05 Jun 2026 22:43:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 05 Jun 2026 22:43:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:39798aa98bd37b2e4ff77c414dd42bca72e522aa2cb338296f10696a239cb2b2`  
		Last Modified: Thu, 04 Jun 2026 06:53:25 GMT  
		Size: 34.9 MB (34854739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafae88de2327d6ae8c0b5b7750f14d9044ddf8345692d9612dab8a0628ccf19`  
		Last Modified: Fri, 05 Jun 2026 22:43:08 GMT  
		Size: 37.8 MB (37760494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ec308c2be2817c28a7db8875f5d07fa762af278c8603f2c20c909f206f375c`  
		Last Modified: Fri, 05 Jun 2026 22:43:40 GMT  
		Size: 92.6 MB (92579381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b12406fa4d78e8a7b98afe346f407380d541d5daaa762154c7994abea3b6e3`  
		Last Modified: Fri, 05 Jun 2026 22:43:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d673d3ad76bbe183a8f40c09a61f01728144133fdccd98df6d9af307b95dad`  
		Last Modified: Fri, 05 Jun 2026 22:43:37 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:815cfd65429d53c2589f80ad56111e27d100bcbf163d955b66f91484ab084138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3781034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe6ece94611e7245aee2e935bcef182089215ce09bcd9375770f1fda61191b2`

```dockerfile
```

-	Layers:
	-	`sha256:0667767418b02d373ae13e68c15413056fd6b3a3d3b6e0df1f3ecd97de68aa49`  
		Last Modified: Fri, 05 Jun 2026 22:43:37 GMT  
		Size: 3.8 MB (3759745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:268fb454c1e0790e899b2872bf86822856b5626c61f3b8926a4dbbbdbab81bfa`  
		Last Modified: Fri, 05 Jun 2026 22:43:37 GMT  
		Size: 21.3 KB (21289 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:2fcb51f613d6ece02c3f4893724994aae837a8a1526263e44cd3cc6ec367fae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162277428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1930a3f11b35101a4c0971c354abc4550f797fe9c034954d35ac81c3f1c66c1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL io.openshift.expose-services=""
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 04 Jun 2026 05:32:13 GMT
ENV container oci
# Thu, 04 Jun 2026 05:32:14 GMT
COPY dir:742cf4548328149a0d3b299bb0ecd0a71c615bfaf88aa6d4360ecf931aab8785 in /      
# Thu, 04 Jun 2026 05:32:14 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 04 Jun 2026 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 04 Jun 2026 05:32:14 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 04 Jun 2026 05:32:14 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 04 Jun 2026 05:32:14 GMT
COPY file:857742e0cb2c063297a5d6df57ad39367bc23ea5335b6bce896696d17d2eb019 in /usr/share/buildinfo/labels.json      
# Thu, 04 Jun 2026 05:32:14 GMT
COPY file:857742e0cb2c063297a5d6df57ad39367bc23ea5335b6bce896696d17d2eb019 in /root/buildinfo/labels.json      
# Thu, 04 Jun 2026 05:32:14 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="21e748607cdf3bfe567bea40c2e0c654a3c7766c" "org.opencontainers.image.revision"="21e748607cdf3bfe567bea40c2e0c654a3c7766c" "build-date"="2026-06-04T05:31:57Z" "org.opencontainers.image.created"="2026-06-04T05:31:57Z" "release"="1780550715"org.opencontainers.image.revision=21e748607cdf3bfe567bea40c2e0c654a3c7766c,org.opencontainers.image.created=2026-06-04T05:31:57Z
# Fri, 05 Jun 2026 22:43:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 05 Jun 2026 22:43:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jun 2026 22:43:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 05 Jun 2026 22:43:18 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 05 Jun 2026 22:43:18 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Fri, 05 Jun 2026 22:43:48 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 05 Jun 2026 22:43:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 05 Jun 2026 22:43:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 05 Jun 2026 22:43:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 05 Jun 2026 22:43:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ebf3c43a43d516c400d687e8a210bad7522ec8a8a6c34ae1d72a70004f06bc71`  
		Last Modified: Thu, 04 Jun 2026 06:53:34 GMT  
		Size: 33.0 MB (33039715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc4d425caa67df0867ba8b5668aaf92b64f8d1e58cfe5c582525338c6cf5da3`  
		Last Modified: Fri, 05 Jun 2026 22:43:35 GMT  
		Size: 37.7 MB (37686371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cce4f38a9d6cb07f88c887319bbb81b030c6cc6ac9d3d583ca651422563aa4`  
		Last Modified: Fri, 05 Jun 2026 22:44:09 GMT  
		Size: 91.5 MB (91548922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b9416a89ff62c9ce6bb8aa12b94aefa60c1c43126c866b92193404d374b3bb`  
		Last Modified: Fri, 05 Jun 2026 22:44:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be6d85c5fa8583ec8da3c5c15eb5e332469b4d36b379a2ff9c0427162392f5f`  
		Last Modified: Fri, 05 Jun 2026 22:44:06 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c370c5fba55cdd656ce6597d2fd9d8399f070f9d55e0c1ee6b5ce60d3976bed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3780573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ea3552cbd464f5e0fbd28c1aca854b96050fc79d36d51aa8d5eaecc2ec79af`

```dockerfile
```

-	Layers:
	-	`sha256:523fd8e5e837ea7f55e19dceb644ba47419d29287347af10f93df7276c73e7a1`  
		Last Modified: Fri, 05 Jun 2026 22:44:07 GMT  
		Size: 3.8 MB (3759168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87f282c89d6e95da1e4dc65902a96731d12b757f614f0192a796b847303972bb`  
		Last Modified: Fri, 05 Jun 2026 22:44:06 GMT  
		Size: 21.4 KB (21405 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:ceeb8daee23d054017ae9b19bd3631fce77af85416f5337f0842e39830b2494f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170446542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9eeee993668f092234f0f423a4f47da86d41ba752818d9e5cfd18131a16ac6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL io.openshift.expose-services=""
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 04 Jun 2026 05:32:40 GMT
ENV container oci
# Thu, 04 Jun 2026 05:32:41 GMT
COPY dir:39feacb07d6a39793cfb5ecb8ce42cbba48072d5e83b48decf5ed170f1dae59f in /      
# Thu, 04 Jun 2026 05:32:41 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 04 Jun 2026 05:32:41 GMT
CMD ["/bin/bash"]
# Thu, 04 Jun 2026 05:32:41 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 04 Jun 2026 05:32:41 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 04 Jun 2026 05:32:41 GMT
COPY file:5a88f34d22fc0aaa3bcdde8758372a2e49b97b3dec16ffb3a17985ea3396531b in /usr/share/buildinfo/labels.json      
# Thu, 04 Jun 2026 05:32:41 GMT
COPY file:5a88f34d22fc0aaa3bcdde8758372a2e49b97b3dec16ffb3a17985ea3396531b in /root/buildinfo/labels.json      
# Thu, 04 Jun 2026 05:32:42 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="21e748607cdf3bfe567bea40c2e0c654a3c7766c" "org.opencontainers.image.revision"="21e748607cdf3bfe567bea40c2e0c654a3c7766c" "build-date"="2026-06-04T05:32:29Z" "org.opencontainers.image.created"="2026-06-04T05:32:29Z" "release"="1780550715"org.opencontainers.image.revision=21e748607cdf3bfe567bea40c2e0c654a3c7766c,org.opencontainers.image.created=2026-06-04T05:32:29Z
# Fri, 05 Jun 2026 23:18:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 05 Jun 2026 23:18:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jun 2026 23:18:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 05 Jun 2026 23:18:00 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 05 Jun 2026 23:18:00 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Fri, 05 Jun 2026 23:21:59 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 05 Jun 2026 23:22:03 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 05 Jun 2026 23:22:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 05 Jun 2026 23:22:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 05 Jun 2026 23:22:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0548d638ade0e4394f010f8571f1879c4b09c3ac5cba2ccff7dfa8b2c88574b5`  
		Last Modified: Thu, 04 Jun 2026 06:53:50 GMT  
		Size: 39.0 MB (39010615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386aabc3a75f4ee1e9a3070c6e92d370f6789fef7ef5aa8020778d4f20d9234b`  
		Last Modified: Fri, 05 Jun 2026 23:18:37 GMT  
		Size: 39.5 MB (39520609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f466d1d548c4da503bf1394e6071455bf2fb551c32e52958d94fe011af608e7e`  
		Last Modified: Fri, 05 Jun 2026 23:22:38 GMT  
		Size: 91.9 MB (91912899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2c8809162032d2056f22b37ea491e782503f14d3ac30d926d39ad60b3c61c9`  
		Last Modified: Fri, 05 Jun 2026 23:22:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c44cdc1c452835a0aee1af8b76ae62414a538277e22c885626383819ae80877`  
		Last Modified: Fri, 05 Jun 2026 23:22:36 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5cc004b9496e67119bf3680b7d6ff6f9b26118f30233367e95467b10a2de7d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3751214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68e3e048210b55496e327e9d27a03f2dd7dd114834c9553f85ac78d41136b43`

```dockerfile
```

-	Layers:
	-	`sha256:29050f20698fbfa0ef1baaea9b341c13f419772d6ae904028a6ac5faafba93c2`  
		Last Modified: Fri, 05 Jun 2026 23:22:36 GMT  
		Size: 3.7 MB (3729889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff1f291bb17fea0823420f247ae6d0bd0ad2803b249735a76fec0baab68124da`  
		Last Modified: Fri, 05 Jun 2026 23:22:36 GMT  
		Size: 21.3 KB (21325 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jdk-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:c77f9472965221118ec49ca589dd272dc4a17df69239e597f450791a073016d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161290023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b965afab5b335ce0c962c5054348e81c3421c759340f0aed4d69c06389074d76`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL io.openshift.expose-services=""
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 04 Jun 2026 05:41:17 GMT
ENV container oci
# Thu, 04 Jun 2026 05:41:17 GMT
COPY dir:9a20d45e3984f98caa7a89f40c9769c8ed59b525d31291027bc9643813420c60 in /      
# Thu, 04 Jun 2026 05:41:18 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 04 Jun 2026 05:41:18 GMT
CMD ["/bin/bash"]
# Thu, 04 Jun 2026 05:41:18 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 04 Jun 2026 05:41:18 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 04 Jun 2026 05:41:18 GMT
COPY file:145c21488b7dd243862f15c5b9a62cfc5fc22a0ba135ab81b80fd5dfaa1db619 in /usr/share/buildinfo/labels.json      
# Thu, 04 Jun 2026 05:41:18 GMT
COPY file:145c21488b7dd243862f15c5b9a62cfc5fc22a0ba135ab81b80fd5dfaa1db619 in /root/buildinfo/labels.json      
# Thu, 04 Jun 2026 05:41:18 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="21e748607cdf3bfe567bea40c2e0c654a3c7766c" "org.opencontainers.image.revision"="21e748607cdf3bfe567bea40c2e0c654a3c7766c" "build-date"="2026-06-04T05:40:37Z" "org.opencontainers.image.created"="2026-06-04T05:40:37Z" "release"="1780550715"org.opencontainers.image.revision=21e748607cdf3bfe567bea40c2e0c654a3c7766c,org.opencontainers.image.created=2026-06-04T05:40:37Z
# Fri, 05 Jun 2026 22:54:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 05 Jun 2026 22:54:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jun 2026 22:54:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 05 Jun 2026 22:54:39 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 05 Jun 2026 22:54:39 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Fri, 05 Jun 2026 22:57:09 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 05 Jun 2026 22:57:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 05 Jun 2026 22:57:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 05 Jun 2026 22:57:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 05 Jun 2026 22:57:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:508908cfb0e80bf20878a35fc50b1b96d43933820f4d9e8454cbdb960c52bdb5`  
		Last Modified: Thu, 04 Jun 2026 06:53:41 GMT  
		Size: 34.7 MB (34726577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b711f2b1010b3a0bdac6f6c9c90783837f411ad3aff4e3fda9b12ef7924d85`  
		Last Modified: Fri, 05 Jun 2026 22:55:03 GMT  
		Size: 38.1 MB (38139315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d5782ab9fe562fafbbdfb885d7de05c83043f428f3b137aec0084b6fc315b0`  
		Last Modified: Fri, 05 Jun 2026 22:57:38 GMT  
		Size: 88.4 MB (88421715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ca4cd309b9c6878632680539c95cee87606ff706331056cf07e470a37b0b3f`  
		Last Modified: Fri, 05 Jun 2026 22:57:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a69a3a1b0eeca8e61b33e879fd43b87355e6f875104f31d6e685803591849bf`  
		Last Modified: Fri, 05 Jun 2026 22:57:36 GMT  
		Size: 2.3 KB (2287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8ab50f049ddc8f58afd5e8252b3a50c80f3dbb34ce40e7551bc47846aebc02f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3751185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eefcba19a3305915481fde8dec134f759e2b597996a49cad31520520902675c`

```dockerfile
```

-	Layers:
	-	`sha256:6b5a6cec0c4849386e88eef226f2ae18f54ba934150fd8abb141225d440aaa08`  
		Last Modified: Fri, 05 Jun 2026 22:57:36 GMT  
		Size: 3.7 MB (3729897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b3c5e3351a8cad344446fef1e70eeb63631523c5f6d147a3fbeefd64064356f`  
		Last Modified: Fri, 05 Jun 2026 22:57:36 GMT  
		Size: 21.3 KB (21288 bytes)  
		MIME: application/vnd.in-toto+json
