## `eclipse-temurin:11-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:3bbcf04894e3becdf72fa720bfbf196144e5f255a6a3c997260794e16bc7554b
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

### `eclipse-temurin:11-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:729026c26069007fff4e147807fd14b6bdbe275ab0c538771a39f675271e0e7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116382301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa696c95175c7da3f717897c03eaee925d7d3adb85393681e2247ae89182b005`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 20 Apr 2026 01:02:16 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 01:02:16 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 01:02:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 01:02:16 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 20 Apr 2026 01:02:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 01:02:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 20 Apr 2026 01:02:16 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 01:02:16 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 01:02:16 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 20 Apr 2026 01:02:16 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 01:02:16 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 20 Apr 2026 01:02:16 GMT
ENV container oci
# Mon, 20 Apr 2026 01:02:16 GMT
COPY dir:dd0e1195353ed5dffd0360f7175a32413cb31b4b787f27413cf4ea2f98d12b5d in /      
# Mon, 20 Apr 2026 01:02:16 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 01:02:16 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 01:02:16 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 01:02:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 01:02:17 GMT
COPY file:fbdadfc291bf0e40ec3c74e36ea45cd6d320a19b5da8cb1d3fdb33930ac6a4c0 in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 01:02:17 GMT
COPY file:fbdadfc291bf0e40ec3c74e36ea45cd6d320a19b5da8cb1d3fdb33930ac6a4c0 in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 01:02:17 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="32540b060e1a63cad21d656f09cff9da51482dc3" "org.opencontainers.image.revision"="32540b060e1a63cad21d656f09cff9da51482dc3" "build-date"="2026-04-20T01:02:00Z" "org.opencontainers.image.created"="2026-04-20T01:02:00Z" "release"="1776646707"org.opencontainers.image.revision=32540b060e1a63cad21d656f09cff9da51482dc3,org.opencontainers.image.created=2026-04-20T01:02:00Z
# Mon, 20 Apr 2026 23:06:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Apr 2026 23:06:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:06:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Apr 2026 23:06:17 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:06:17 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Mon, 20 Apr 2026 23:06:20 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='9d6a8d3a33c308bbc7332e4c2e2f9a94fbbc56417863496061ef6defef9c5391';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='d64f2f707b3940789f3d75c8cf55a409e786c3ca4c0e85f3fedf42e1e3ef63ae';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='634f7ee49a6f1e8be64dfaf91b9c0306b5662d40bd5624010f6a9c4862e4e1b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='d851e43d81ec6ff7f28efe28c42b4787a045e8f59cdcd6434dece98d8342eb8a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 20 Apr 2026 23:06:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:06:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:06:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:9ea0f884ebdb006c6d06f1f86307c899f549c7d238971fe657c84c93f6b38191`  
		Last Modified: Mon, 20 Apr 2026 11:13:13 GMT  
		Size: 34.6 MB (34611060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1cc045102cda3bfcdde8e5b45d806f80aaa359df59363fb59ccd9041a2ae27`  
		Last Modified: Mon, 20 Apr 2026 23:06:34 GMT  
		Size: 37.5 MB (37463485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd87910141e5bc2e12c563f6255c004adebcff98219e20489b8348c3c8b7d0bd`  
		Last Modified: Mon, 20 Apr 2026 23:06:34 GMT  
		Size: 44.3 MB (44305339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e178019a3fb53e3eff33dcd26e7cbdce5917ab7c365d305e9be650f245a1981`  
		Last Modified: Mon, 20 Apr 2026 23:06:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef5880acfb74b998b5c3664fc3bebf1197ad0023e1fa2a6058a66818d32e8b9`  
		Last Modified: Mon, 20 Apr 2026 23:06:31 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e4164a0748caa610b032a823e24c525dbc485708e7e4e68064de6ea1ecf4656c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3738161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959c6fa7ebd43d651e012463ebe267492539b1ab6156575a7d1bf141218f6d49`

```dockerfile
```

-	Layers:
	-	`sha256:96c6cbcdae0866cad083098578e142a37806b8a8ece346d8610e8dd4ab61d7cb`  
		Last Modified: Mon, 20 Apr 2026 23:06:32 GMT  
		Size: 3.7 MB (3717807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28794d544d141935695fd003e5f7ac2f744bdd6c3fe6de697dd92f89330e0470`  
		Last Modified: Mon, 20 Apr 2026 23:06:31 GMT  
		Size: 20.4 KB (20354 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:58f5f2c374fa1624e58da1c9fa562eb1ba3c385439b9efeaedf512192f1b08b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112725576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db27c6b8b64b1836fc048303be89356c657d23191d25e75e447e10309182abc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 20 Apr 2026 01:04:42 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 01:04:42 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 01:04:42 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 01:04:43 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 20 Apr 2026 01:04:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 01:04:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 20 Apr 2026 01:04:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 01:04:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 01:04:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 20 Apr 2026 01:04:43 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 01:04:43 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 20 Apr 2026 01:04:43 GMT
ENV container oci
# Mon, 20 Apr 2026 01:04:43 GMT
COPY dir:3dce53cd7f9d7326227f9f135d7cd4905e49967e75fffdb7305248967fd08ecb in /      
# Mon, 20 Apr 2026 01:04:44 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 01:04:44 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 01:04:44 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 01:04:44 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 01:04:44 GMT
COPY file:47b968046aebceb7e689b8f162b1d58465b394d88fb7d588f40ffa5eb8594d57 in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 01:04:44 GMT
COPY file:47b968046aebceb7e689b8f162b1d58465b394d88fb7d588f40ffa5eb8594d57 in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 01:04:44 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="32540b060e1a63cad21d656f09cff9da51482dc3" "org.opencontainers.image.revision"="32540b060e1a63cad21d656f09cff9da51482dc3" "build-date"="2026-04-20T01:04:27Z" "org.opencontainers.image.created"="2026-04-20T01:04:27Z" "release"="1776646707"org.opencontainers.image.revision=32540b060e1a63cad21d656f09cff9da51482dc3,org.opencontainers.image.created=2026-04-20T01:04:27Z
# Mon, 20 Apr 2026 23:03:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Apr 2026 23:03:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:03:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Apr 2026 23:03:47 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:03:47 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Mon, 20 Apr 2026 23:03:51 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='9d6a8d3a33c308bbc7332e4c2e2f9a94fbbc56417863496061ef6defef9c5391';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='d64f2f707b3940789f3d75c8cf55a409e786c3ca4c0e85f3fedf42e1e3ef63ae';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='634f7ee49a6f1e8be64dfaf91b9c0306b5662d40bd5624010f6a9c4862e4e1b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='d851e43d81ec6ff7f28efe28c42b4787a045e8f59cdcd6434dece98d8342eb8a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 20 Apr 2026 23:03:51 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:03:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:03:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:8aaf81d11ba9b2394d31694793b5dabaf4eed2f5a356c7de160384c76fcf3161`  
		Last Modified: Mon, 20 Apr 2026 12:17:52 GMT  
		Size: 32.7 MB (32690247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a0bf28838919d5fd2240d6a841e3975a4539538ed10e1ddd50bf55bcb47b8c`  
		Last Modified: Mon, 20 Apr 2026 23:04:05 GMT  
		Size: 37.4 MB (37401977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12118705c589129e9378cf9610a62e58805f15f9905dc0257868d1a54a3f7d5`  
		Last Modified: Mon, 20 Apr 2026 23:04:05 GMT  
		Size: 42.6 MB (42630935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd486ba8ea9f9b54ed0c72a7e7fe1edc3a49af438cbf3b7b107b199cc2b0e02`  
		Last Modified: Mon, 20 Apr 2026 23:04:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb75324977021680c591cd81b4f8482e40773efc45ecba4fb43dd78a7cd7895c`  
		Last Modified: Mon, 20 Apr 2026 23:04:03 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4937a9913f30a2bc52a7d6bd28138828dc2cc002e79e97669ef12d10041dd894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3738297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6117fb7d8144da23c8ff2521e53fcb61b2a56bf882a01b532527dcb833475666`

```dockerfile
```

-	Layers:
	-	`sha256:fea5505d1e9377ef513d1775fe0ae8e6d40813ec34de8bd2b0118835ed0f583a`  
		Last Modified: Mon, 20 Apr 2026 23:04:03 GMT  
		Size: 3.7 MB (3717839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f3c57f3583df4c1d97ad8d93c7d9aee42c8da70118cc52ea68c070c18134547`  
		Last Modified: Mon, 20 Apr 2026 23:04:03 GMT  
		Size: 20.5 KB (20458 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:5c114b2cb1a9a4c2df128443780f9c61eadfa154a84ebb32aabf93dcc5cd6b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117710124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7daaf7d23d382e67ed754ad682091f6abbdbceaf1988b85ac68fb235ee8b31`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 20 Apr 2026 01:03:47 GMT
ENV container oci
# Mon, 20 Apr 2026 01:03:48 GMT
COPY dir:56f7e656d3890224e75a1a16ae5067199386e27e9adfa336ba5808545546cc9e in /      
# Mon, 20 Apr 2026 01:03:48 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 01:03:48 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 01:03:48 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 01:03:48 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 01:03:48 GMT
COPY file:7bbce3df91c54303354eb2bfc2cec747cbe675dbc724bafe59b7a5adbf9432ea in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 01:03:48 GMT
COPY file:7bbce3df91c54303354eb2bfc2cec747cbe675dbc724bafe59b7a5adbf9432ea in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 01:03:49 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="32540b060e1a63cad21d656f09cff9da51482dc3" "org.opencontainers.image.revision"="32540b060e1a63cad21d656f09cff9da51482dc3" "build-date"="2026-04-20T01:03:36Z" "org.opencontainers.image.created"="2026-04-20T01:03:36Z" "release"="1776646707"org.opencontainers.image.revision=32540b060e1a63cad21d656f09cff9da51482dc3,org.opencontainers.image.created=2026-04-20T01:03:36Z
# Mon, 20 Apr 2026 23:00:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Apr 2026 23:00:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:00:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Apr 2026 23:00:58 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:00:58 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Mon, 20 Apr 2026 23:03:42 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='9d6a8d3a33c308bbc7332e4c2e2f9a94fbbc56417863496061ef6defef9c5391';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='d64f2f707b3940789f3d75c8cf55a409e786c3ca4c0e85f3fedf42e1e3ef63ae';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='634f7ee49a6f1e8be64dfaf91b9c0306b5662d40bd5624010f6a9c4862e4e1b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='d851e43d81ec6ff7f28efe28c42b4787a045e8f59cdcd6434dece98d8342eb8a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 20 Apr 2026 23:03:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:03:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:03:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6d2ce28440d2316b24b69c4ac9181a2021fc4fbcccd08e544cb55b3f85789742`  
		Last Modified: Mon, 20 Apr 2026 12:18:07 GMT  
		Size: 38.7 MB (38691389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d8a467e0af186e4504fef70fa25944d04fcadf33d89978c86033d4efabe13`  
		Last Modified: Mon, 20 Apr 2026 23:01:39 GMT  
		Size: 39.2 MB (39213371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88bb63113a6ca8186ac8b3612df4e2008fc0acf5c450185af631283567322269`  
		Last Modified: Mon, 20 Apr 2026 23:04:09 GMT  
		Size: 39.8 MB (39802948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c081c5f9fc5222097bf6636ba06e692aa8cf6450e8fe770088bf509ca264dd12`  
		Last Modified: Mon, 20 Apr 2026 23:04:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e85836acc29e3d4cfe7252603045db7b145ad9f213983f47f8434cda7db3ac`  
		Last Modified: Mon, 20 Apr 2026 23:04:08 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:15116d83fa85674618e1e6b5551be5a8ac13bae95b8d2b0a406aa2cb94d68ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cecca64daafac1b421b16e7816a0676ff08986293ad7ade42387b187c57ce218`

```dockerfile
```

-	Layers:
	-	`sha256:808cd4f6507bd649c80f281962647802df249ab7ec65a102869c51ab966bfa25`  
		Last Modified: Mon, 20 Apr 2026 23:04:08 GMT  
		Size: 3.7 MB (3706558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:456cef2d4a27b9bd43f5bd12882a05e71a3f9a838ffc4ee991d11f51b68ba506`  
		Last Modified: Mon, 20 Apr 2026 23:04:08 GMT  
		Size: 20.4 KB (20384 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:db6c256d02b6c389cc0b4c882561621e008acb2a79036f38f699f9e9b84e9147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110576331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0d748f001eb5897dcb7df74d20241689128362bf1124e4e5480f303bb20a64`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 20 Apr 2026 01:16:10 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 01:16:10 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 01:16:10 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 01:16:10 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 20 Apr 2026 01:16:10 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 01:16:10 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 20 Apr 2026 01:16:10 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 01:16:10 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 01:16:10 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 20 Apr 2026 01:16:10 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 01:16:10 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 20 Apr 2026 01:16:10 GMT
ENV container oci
# Mon, 20 Apr 2026 01:16:10 GMT
COPY dir:4e87af2731f02be78cfc1976cd162db8d3f5c4fdd7c727c77a82a99e955d0442 in /      
# Mon, 20 Apr 2026 01:16:10 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 01:16:10 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 01:16:10 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 01:16:10 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 01:16:10 GMT
COPY file:a467820b7ca76dd041fea2ae09e903a742727218438d9088812b788d84b3bf37 in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 01:16:10 GMT
COPY file:a467820b7ca76dd041fea2ae09e903a742727218438d9088812b788d84b3bf37 in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 01:16:11 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="32540b060e1a63cad21d656f09cff9da51482dc3" "org.opencontainers.image.revision"="32540b060e1a63cad21d656f09cff9da51482dc3" "build-date"="2026-04-20T01:15:28Z" "org.opencontainers.image.created"="2026-04-20T01:15:28Z" "release"="1776646707"org.opencontainers.image.revision=32540b060e1a63cad21d656f09cff9da51482dc3,org.opencontainers.image.created=2026-04-20T01:15:28Z
# Mon, 20 Apr 2026 23:04:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Apr 2026 23:04:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:04:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Apr 2026 23:04:17 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:04:17 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Mon, 20 Apr 2026 23:04:30 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='9d6a8d3a33c308bbc7332e4c2e2f9a94fbbc56417863496061ef6defef9c5391';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='d64f2f707b3940789f3d75c8cf55a409e786c3ca4c0e85f3fedf42e1e3ef63ae';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='634f7ee49a6f1e8be64dfaf91b9c0306b5662d40bd5624010f6a9c4862e4e1b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='d851e43d81ec6ff7f28efe28c42b4787a045e8f59cdcd6434dece98d8342eb8a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 20 Apr 2026 23:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:04:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:04:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:04715052fbc06c0056775e78575e0b8f757abb3e43e5f7db21d195f303d81dc7`  
		Last Modified: Mon, 20 Apr 2026 12:17:59 GMT  
		Size: 34.4 MB (34449818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634ad98208e9fa699c94890ad966ce076aba8c7dd5d326a137e414df039960d5`  
		Last Modified: Mon, 20 Apr 2026 23:07:01 GMT  
		Size: 37.8 MB (37842246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae5788bfcfb38409892a003ce9354563862aa83b2cec588e657284653d27c78`  
		Last Modified: Mon, 20 Apr 2026 23:07:00 GMT  
		Size: 38.3 MB (38281851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079edea0aab9a4e25605fc419891f1e9d0e6790f7eeb3aa99a8658fbd27e8b68`  
		Last Modified: Mon, 20 Apr 2026 23:06:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d1f6c26adf35b798ecb65f742af94a5a7351e41cb50855c6328a9662af55e6`  
		Last Modified: Mon, 20 Apr 2026 23:06:54 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:fd082137f90bf3b4cc5fa924608d7f61c3bf881060f97d26a0d8cc2a1b53d9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3728157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be682ae64fcfa3017c55433b1a74145f2f2aa9dfc4095e664195651815daa590`

```dockerfile
```

-	Layers:
	-	`sha256:4eff869b2248c439a183a6d3a296e60fea4b4443e0086595b9b0552fc16d7119`  
		Last Modified: Mon, 20 Apr 2026 23:06:53 GMT  
		Size: 3.7 MB (3707803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a49caad582462e48acd64118f60e47724031b35d1d3dab5f2d87362717d9c55`  
		Last Modified: Mon, 20 Apr 2026 23:06:47 GMT  
		Size: 20.4 KB (20354 bytes)  
		MIME: application/vnd.in-toto+json
