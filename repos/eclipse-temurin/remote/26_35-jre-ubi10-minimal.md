## `eclipse-temurin:26_35-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:e6b8b029ad0dff6f395793fcb5171214195030bcb571c617ff019b9f6a25fb79
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

### `eclipse-temurin:26_35-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:177a3fd7912c50fc038e8c97e43f2e4c76ca17ce27ac5605c93dbdc8db3964b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136480634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5865050afff7afe9bfda2387cd14eb2136d69705d8a33b159f12d34ea224b0e3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 06 May 2026 09:10:13 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 09:10:13 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 09:10:13 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 09:10:13 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 06 May 2026 09:10:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 09:10:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 06 May 2026 09:10:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 09:10:13 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 09:10:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 06 May 2026 09:10:13 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 09:10:13 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 06 May 2026 09:10:13 GMT
ENV container oci
# Wed, 06 May 2026 09:10:13 GMT
COPY dir:c68dbe05133c31f8fd9f151252a4a29ce3fdd8d44060b74e88191790dd574dbf in /      
# Wed, 06 May 2026 09:10:13 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 09:10:14 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 09:10:14 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 09:10:14 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 09:10:14 GMT
COPY file:878ce3a57b93d24e6852d17b3cb65931afbc773f95f9596e50dac7b8ef938cc4 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 09:10:14 GMT
COPY file:878ce3a57b93d24e6852d17b3cb65931afbc773f95f9596e50dac7b8ef938cc4 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 09:10:14 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="bf211293690f866639ec8b5930bb28589978ee3f" "org.opencontainers.image.revision"="bf211293690f866639ec8b5930bb28589978ee3f" "build-date"="2026-05-06T09:09:57Z" "org.opencontainers.image.created"="2026-05-06T09:09:57Z" "release"="1778058333"org.opencontainers.image.revision=bf211293690f866639ec8b5930bb28589978ee3f,org.opencontainers.image.created=2026-05-06T09:09:57Z
# Fri, 08 May 2026 16:20:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 16:20:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:20:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 16:20:55 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 08 May 2026 16:20:55 GMT
ENV JAVA_VERSION=jdk-26+35
# Fri, 08 May 2026 16:21:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='460dff59e58d77980d8f3aa3172f53d09c17beca1a16b5762f388aee8c91656c';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='f6d3b8e1f76c1dac5c9955ba77571e8e77aa02724f7423737627244174f41d5e';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='33cdf9b2bd4699ff76fb17f8d62d8ffc86ebf05296c626bf298f4c2bc140023a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='3a65331f4c4b671a5e5bb3ae4e4a65fd0eb5bf8672c0c2fba6ba36972c4042a4';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 08 May 2026 16:21:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 16:21:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 16:21:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:92d62aafb6a18663d52e4aabc1138a75b2e6994c38e927e9099cb078cc22e6b7`  
		Last Modified: Wed, 06 May 2026 10:14:33 GMT  
		Size: 34.6 MB (34621721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212c78130b95b82c3274218b7f781c8de8a6ddd9044ed3cbacccd8daf28fa9be`  
		Last Modified: Fri, 08 May 2026 16:21:19 GMT  
		Size: 37.5 MB (37499076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5810d9b06ae3660d99082b6ef7cfb9878f64016b40a18a4da3e2d442ee269fa9`  
		Last Modified: Fri, 08 May 2026 16:21:49 GMT  
		Size: 64.4 MB (64357420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdb72c5f15fb7ddb4229a2840af62f22e2ac6c4c39b82e0cddcaa0ffec5e6a6`  
		Last Modified: Fri, 08 May 2026 16:21:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cc4cc57d7be992d40dd57e47aebc4251b3140520fa6c57130c5c688b06868e`  
		Last Modified: Fri, 08 May 2026 16:21:47 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26_35-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:315c46ae43d6e26cfcaeae1b650fe52571133ab086d25627dc20ddbaf8b8a995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5145b6af14b2a43530800841a18c062db2eafe71cde85eb001ba6a98296087`

```dockerfile
```

-	Layers:
	-	`sha256:90630cc70d5e9b24728f62a624064937712601ebf5343b4555b74c0b6e87cf9c`  
		Last Modified: Fri, 08 May 2026 16:21:47 GMT  
		Size: 3.7 MB (3711662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fa75593da30823d0a8d33cb436dd71d0432c92b66e7bbf8ecee9df147f33049`  
		Last Modified: Fri, 08 May 2026 16:21:47 GMT  
		Size: 20.3 KB (20258 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26_35-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:e91a0a98d684db3772eea74b2295f3014fd6be7214e5e28d38fa90be342fa069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.4 MB (133427873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68fd8422eebcce324f2421ac90597c19ab6a42c49080d4c4382a500034da043`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 06 May 2026 09:13:03 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 09:13:03 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 09:13:03 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 09:13:03 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 06 May 2026 09:13:03 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 09:13:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 06 May 2026 09:13:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 09:13:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 09:13:03 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 06 May 2026 09:13:03 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 09:13:03 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 06 May 2026 09:13:03 GMT
ENV container oci
# Wed, 06 May 2026 09:13:04 GMT
COPY dir:750bbe41da49fc0c3224e4824b23b1c35d4c73f39652b46f248f5dd9cad107de in /      
# Wed, 06 May 2026 09:13:04 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 09:13:04 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 09:13:04 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 09:13:04 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 09:13:05 GMT
COPY file:2221d5e6d5258b2c2c2c5ff82716a8550cb92905efa9801612122423d38aec35 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 09:13:05 GMT
COPY file:2221d5e6d5258b2c2c2c5ff82716a8550cb92905efa9801612122423d38aec35 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 09:13:05 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="bf211293690f866639ec8b5930bb28589978ee3f" "org.opencontainers.image.revision"="bf211293690f866639ec8b5930bb28589978ee3f" "build-date"="2026-05-06T09:12:48Z" "org.opencontainers.image.created"="2026-05-06T09:12:48Z" "release"="1778058333"org.opencontainers.image.revision=bf211293690f866639ec8b5930bb28589978ee3f,org.opencontainers.image.created=2026-05-06T09:12:48Z
# Fri, 08 May 2026 16:21:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 16:21:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:21:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 16:21:16 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 08 May 2026 16:21:16 GMT
ENV JAVA_VERSION=jdk-26+35
# Fri, 08 May 2026 16:21:22 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='460dff59e58d77980d8f3aa3172f53d09c17beca1a16b5762f388aee8c91656c';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='f6d3b8e1f76c1dac5c9955ba77571e8e77aa02724f7423737627244174f41d5e';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='33cdf9b2bd4699ff76fb17f8d62d8ffc86ebf05296c626bf298f4c2bc140023a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='3a65331f4c4b671a5e5bb3ae4e4a65fd0eb5bf8672c0c2fba6ba36972c4042a4';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 08 May 2026 16:21:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 16:21:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 16:21:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:e82aa3f29d1a9f34361831d6ff7b3f84cfd92ed1421ee638f165e55be85bd238`  
		Last Modified: Wed, 06 May 2026 10:17:34 GMT  
		Size: 32.7 MB (32746638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edf67c7e03be55151a10dac3af5cc9412580c7e70ca601f04e815840b37d6c5`  
		Last Modified: Fri, 08 May 2026 16:21:38 GMT  
		Size: 37.4 MB (37444040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950646631672b196d17d35c18ac69031e06fe9bdf66bb06807e14086bc0055e1`  
		Last Modified: Fri, 08 May 2026 16:21:40 GMT  
		Size: 63.2 MB (63234779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2463bcb4448a3c3c13b19f86a0d57faf93e9475667da73be3c8bf4a0b9e76fa`  
		Last Modified: Fri, 08 May 2026 16:21:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc896a24fb6fc5cbb129a4a07081650a1a3fdba1b3aed29ad71a48663fe9bf4`  
		Last Modified: Fri, 08 May 2026 16:21:29 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26_35-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b09477bc7447e0b2a99120f59faa5c4ff0f42b21cfecb94ed433f28c9ad85e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e59d3983fa040d866eabc93b36783ba59eb5cd45cc648e8aa39457489f6cefb`

```dockerfile
```

-	Layers:
	-	`sha256:5586e7891abdb9159cb7d09e98a9419dd233206a33c1efd9f2bafeb1fba2a8a4`  
		Last Modified: Fri, 08 May 2026 16:21:37 GMT  
		Size: 3.7 MB (3711073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c626377d92521dce1762305ca8c10b7818182417c47371f436aa9d37a1dd6bc`  
		Last Modified: Fri, 08 May 2026 16:21:36 GMT  
		Size: 20.4 KB (20361 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26_35-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:7e3e2785fedce5948d8ee8cd1bb35cb566a09b787490fe01c1869749106083ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141733734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c51ebb95ab50371d1f70d1f1004efe5916f9bdeac94453d71f358f34ff65dc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 06 May 2026 09:10:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 09:10:53 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 09:10:53 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 09:10:53 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 06 May 2026 09:10:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 09:10:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 06 May 2026 09:10:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 09:10:53 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 09:10:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 06 May 2026 09:10:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 09:10:53 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 06 May 2026 09:10:53 GMT
ENV container oci
# Wed, 06 May 2026 09:10:53 GMT
COPY dir:158c3f0cb7ce24639f61426b68518af6eac4aaf0de71f58d18f634631d8ec0f0 in /      
# Wed, 06 May 2026 09:10:53 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 09:10:53 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 09:10:53 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 09:10:54 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 09:10:54 GMT
COPY file:fa10e966ee7289b238e615643b46ea2d8e307515115a0ea9e2b102df79fabf33 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 09:10:54 GMT
COPY file:fa10e966ee7289b238e615643b46ea2d8e307515115a0ea9e2b102df79fabf33 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 09:10:54 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="bf211293690f866639ec8b5930bb28589978ee3f" "org.opencontainers.image.revision"="bf211293690f866639ec8b5930bb28589978ee3f" "build-date"="2026-05-06T09:10:41Z" "org.opencontainers.image.created"="2026-05-06T09:10:41Z" "release"="1778058333"org.opencontainers.image.revision=bf211293690f866639ec8b5930bb28589978ee3f,org.opencontainers.image.created=2026-05-06T09:10:41Z
# Fri, 08 May 2026 16:18:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 16:18:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:18:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 16:18:44 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 08 May 2026 16:18:44 GMT
ENV JAVA_VERSION=jdk-26+35
# Fri, 08 May 2026 16:28:19 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='460dff59e58d77980d8f3aa3172f53d09c17beca1a16b5762f388aee8c91656c';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='f6d3b8e1f76c1dac5c9955ba77571e8e77aa02724f7423737627244174f41d5e';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='33cdf9b2bd4699ff76fb17f8d62d8ffc86ebf05296c626bf298f4c2bc140023a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='3a65331f4c4b671a5e5bb3ae4e4a65fd0eb5bf8672c0c2fba6ba36972c4042a4';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 08 May 2026 16:28:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 16:28:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 16:28:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:8fabb2dd484322746fc4d1ed7e1fbca1a0509bc14f76029832e436bbc2825a8d`  
		Last Modified: Wed, 06 May 2026 12:15:25 GMT  
		Size: 38.8 MB (38751685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b7c362fde3ba2e4cb3c58a05618ebaafb430e3fbe1631353247827620d8d0d`  
		Last Modified: Fri, 08 May 2026 16:19:23 GMT  
		Size: 39.3 MB (39256885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd15f7abd71a23a76924de8a6d137124eeb328ea3cb33e36012478209b7bd29`  
		Last Modified: Fri, 08 May 2026 16:28:56 GMT  
		Size: 63.7 MB (63722745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b4c9c504fda16c578d4a05f2c1d267cf755e90a1a24734805e8bcd317afbe8`  
		Last Modified: Fri, 08 May 2026 16:28:54 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beec556903a1efc2eb7c6ffd35dba31e986e40c5333ec7083f4c2e6bb8ef5619`  
		Last Modified: Fri, 08 May 2026 16:28:54 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26_35-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5fcfc1579417c5a22a8fe86839d18c7998889e29b89520dd4758fd18df49dc9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3720074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b75449102f7e10b84981f79fa45a46b4ba6e5febe387cafcd6601bbc8182c00`

```dockerfile
```

-	Layers:
	-	`sha256:9fa29f166a1de181fc43f2444233f65dd609362c78b24f4d41011d609f74a45e`  
		Last Modified: Fri, 08 May 2026 16:28:54 GMT  
		Size: 3.7 MB (3699786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddbea15eff57cceb2c0b88d07df5415e3b9bcae4119adfe19a8dbe9938d6cc0a`  
		Last Modified: Fri, 08 May 2026 16:28:54 GMT  
		Size: 20.3 KB (20288 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26_35-jre-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:cd3ba49e0385cdec8367d124d7d96dd6947d6462f8025ea97b615b161d4e2425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134402564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5339765a44300ce9f5f6b4e045499b3f135debb8473c37279dc281d052e4e90`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 06 May 2026 09:18:23 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 09:18:23 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 09:18:23 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 09:18:23 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 06 May 2026 09:18:23 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 09:18:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 06 May 2026 09:18:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 09:18:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 09:18:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 06 May 2026 09:18:23 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 09:18:23 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 06 May 2026 09:18:23 GMT
ENV container oci
# Wed, 06 May 2026 09:18:24 GMT
COPY dir:2de320d13d9374da0da9c93af8654c20620deef9fb77e0789c2dd217c1731ec0 in /      
# Wed, 06 May 2026 09:18:24 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 09:18:24 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 09:18:24 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 09:18:24 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 09:18:24 GMT
COPY file:de510b2b1ef76ab831f854dfe5fc4dc2d485ce06def44bc72ced35b5d05e629e in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 09:18:24 GMT
COPY file:de510b2b1ef76ab831f854dfe5fc4dc2d485ce06def44bc72ced35b5d05e629e in /root/buildinfo/labels.json      
# Wed, 06 May 2026 09:18:24 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="bf211293690f866639ec8b5930bb28589978ee3f" "org.opencontainers.image.revision"="bf211293690f866639ec8b5930bb28589978ee3f" "build-date"="2026-05-06T09:17:45Z" "org.opencontainers.image.created"="2026-05-06T09:17:45Z" "release"="1778058333"org.opencontainers.image.revision=bf211293690f866639ec8b5930bb28589978ee3f,org.opencontainers.image.created=2026-05-06T09:17:45Z
# Fri, 08 May 2026 16:18:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 16:18:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:18:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 16:18:48 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 08 May 2026 16:18:48 GMT
ENV JAVA_VERSION=jdk-26+35
# Fri, 08 May 2026 16:21:56 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='460dff59e58d77980d8f3aa3172f53d09c17beca1a16b5762f388aee8c91656c';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='f6d3b8e1f76c1dac5c9955ba77571e8e77aa02724f7423737627244174f41d5e';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='33cdf9b2bd4699ff76fb17f8d62d8ffc86ebf05296c626bf298f4c2bc140023a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='3a65331f4c4b671a5e5bb3ae4e4a65fd0eb5bf8672c0c2fba6ba36972c4042a4';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 08 May 2026 16:21:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 16:21:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 16:21:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:59eaf6b643faaa0a9b84bfb511ee7041d5f1d45b964283eb78c164d14435bcf6`  
		Last Modified: Wed, 06 May 2026 12:15:13 GMT  
		Size: 34.4 MB (34447291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c567288b6c22b0aca367e6871184062ac6fdc0793ecbbf0f93c4ec5dd3e5e8ee`  
		Last Modified: Fri, 08 May 2026 16:19:20 GMT  
		Size: 37.9 MB (37882211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cda6d7bfc737a4ce04c7b58dd3fe077ed7c489c2aaef83bd38efaa8d6f3dc86`  
		Last Modified: Fri, 08 May 2026 16:22:28 GMT  
		Size: 62.1 MB (62070642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b3b7cdd3c3d3549cfaecd01d5b834e6c26149b7ae14dfb1ecffedd96bdab75`  
		Last Modified: Fri, 08 May 2026 16:22:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92642e2f281139d33cfbe56353997bc418c8692bcec8243f27240a4cf3235563`  
		Last Modified: Fri, 08 May 2026 16:22:27 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26_35-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:674d45d166c7f10bbf406a23138a8e9c5bb2fb4a15d8a53908d2fdcc18eb9780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3721289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d281acb15b33951d75f296a127c89d8ed8be840f810b95a3dec897a88a9367b2`

```dockerfile
```

-	Layers:
	-	`sha256:9e1a3ac0a486e2e3869c99132ef83d7fce9e83891bf718e508d13d615bff7fef`  
		Last Modified: Fri, 08 May 2026 16:22:27 GMT  
		Size: 3.7 MB (3701031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32e6fa7de14edcd595ca71c8dfa3ad4f4e6982a8215d844e404bb1639d167824`  
		Last Modified: Fri, 08 May 2026 16:22:27 GMT  
		Size: 20.3 KB (20258 bytes)  
		MIME: application/vnd.in-toto+json
