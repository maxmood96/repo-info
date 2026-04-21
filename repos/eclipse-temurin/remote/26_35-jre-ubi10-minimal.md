## `eclipse-temurin:26_35-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:895897d5083a9579e42e03e781809df70d18ee0b572fde53ce8c726da6044779
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
$ docker pull eclipse-temurin@sha256:57de0add3a44e88f45db1201ded47ea9c0d7bf33be312d4e5df1b10cd4d731c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136433761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87d215303079a811c9a075baf2610b4c098f3da61bd5664336401abf6ce22da`
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
# Mon, 20 Apr 2026 23:06:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Apr 2026 23:06:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:06:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Apr 2026 23:06:20 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:06:20 GMT
ENV JAVA_VERSION=jdk-26+35
# Mon, 20 Apr 2026 23:06:51 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='460dff59e58d77980d8f3aa3172f53d09c17beca1a16b5762f388aee8c91656c';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='f6d3b8e1f76c1dac5c9955ba77571e8e77aa02724f7423737627244174f41d5e';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='33cdf9b2bd4699ff76fb17f8d62d8ffc86ebf05296c626bf298f4c2bc140023a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='3a65331f4c4b671a5e5bb3ae4e4a65fd0eb5bf8672c0c2fba6ba36972c4042a4';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 20 Apr 2026 23:06:51 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:06:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:06:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:9ea0f884ebdb006c6d06f1f86307c899f549c7d238971fe657c84c93f6b38191`  
		Last Modified: Mon, 20 Apr 2026 11:13:13 GMT  
		Size: 34.6 MB (34611060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7f3ec9a9c470c6374ff12b025adb6fc1fa1575a1bc3a99814d9d97de2b9474`  
		Last Modified: Mon, 20 Apr 2026 23:06:38 GMT  
		Size: 37.5 MB (37462894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987cb03d41eb390bdbf14333c4f570454413e42a13322b6fa609831cf156e97c`  
		Last Modified: Mon, 20 Apr 2026 23:07:07 GMT  
		Size: 64.4 MB (64357391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4822324fef4a81b561ddc5849349197379175bc7ddebc3fe28451051b1e5c3c`  
		Last Modified: Mon, 20 Apr 2026 23:07:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1f42952622c67f2fe7db07ec946f9ae6c9b182ffee4b24ef9f63f168df0244`  
		Last Modified: Mon, 20 Apr 2026 23:07:06 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26_35-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4ec9e1800845de6fc43033bb9eba953a6be01c6c6fe64ee47ee3c0bc25997431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31853122cfb503db5d11ee9f622d783ec3bf57512ac4b022b66c5ada95b5b5be`

```dockerfile
```

-	Layers:
	-	`sha256:304c6534cbdbee3f82ba44b7656ff1899be0a6e661743cb2851d6d3d0ae2254e`  
		Last Modified: Mon, 20 Apr 2026 23:07:06 GMT  
		Size: 3.7 MB (3711614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4f5e6cc5168b6c2c0ef2fc842daabe94a31ab43927446a008fcbb1816473db1`  
		Last Modified: Mon, 20 Apr 2026 23:07:06 GMT  
		Size: 20.3 KB (20257 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26_35-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:3183b8ee8b3a0f58484d7eaf5125ad2e9d807fffe4b72a9c555da5699a7b1253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133329456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c95089e5fac86957145c3586ca18fd0088e278d7cbbca736fc9cbfb075d0428`
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
# Mon, 20 Apr 2026 23:04:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Apr 2026 23:04:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:04:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Apr 2026 23:04:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:04:32 GMT
ENV JAVA_VERSION=jdk-26+35
# Mon, 20 Apr 2026 23:04:38 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='460dff59e58d77980d8f3aa3172f53d09c17beca1a16b5762f388aee8c91656c';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='f6d3b8e1f76c1dac5c9955ba77571e8e77aa02724f7423737627244174f41d5e';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='33cdf9b2bd4699ff76fb17f8d62d8ffc86ebf05296c626bf298f4c2bc140023a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='3a65331f4c4b671a5e5bb3ae4e4a65fd0eb5bf8672c0c2fba6ba36972c4042a4';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 20 Apr 2026 23:04:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:04:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:04:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:8aaf81d11ba9b2394d31694793b5dabaf4eed2f5a356c7de160384c76fcf3161`  
		Last Modified: Mon, 20 Apr 2026 12:17:52 GMT  
		Size: 32.7 MB (32690247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3d536a921f9a95e68bbfecbeaed496bd3d42de4eb02a54248ea19d276ccab1`  
		Last Modified: Mon, 20 Apr 2026 23:04:55 GMT  
		Size: 37.4 MB (37401972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb7de5a025715d08ba8abc56ae9df5b758d085d81b21bb5ac2198498198cfb7`  
		Last Modified: Mon, 20 Apr 2026 23:04:56 GMT  
		Size: 63.2 MB (63234820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e77b9a7a71a5151806336bda824106958f014ced73c7b2eb5ecc3c19771e64b`  
		Last Modified: Mon, 20 Apr 2026 23:04:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b06276767ff582a43fdd07e18b8ed9197793c8400e2401e7c3f321cadd131b`  
		Last Modified: Mon, 20 Apr 2026 23:04:53 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26_35-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3b43eb1f885f9791e05418461638c87935e53f7f212f96021e062499c6cef4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94885f000c06e49db3e818de8987467d30e1f7e375207ab8943d5d0f412d0b77`

```dockerfile
```

-	Layers:
	-	`sha256:7707084cb82ebe8fc8b897b3078bcc8ea6767bd2e895d28ef37e96b99c37bfc6`  
		Last Modified: Mon, 20 Apr 2026 23:04:53 GMT  
		Size: 3.7 MB (3711025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:625e071435fa234f712a32deda048530b12c18564b1bc15363e5ca0be60c751b`  
		Last Modified: Mon, 20 Apr 2026 23:04:53 GMT  
		Size: 20.4 KB (20362 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26_35-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:62e4ca0f6615ea4f78df6cc8367c31b19000583c0195d9c4d4e5b9056f502169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141629953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35fbac404193a0671098640d4a50188dd97451b5500f2b6fbfec6f669adbf09c`
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
ENV JAVA_VERSION=jdk-26+35
# Mon, 20 Apr 2026 23:10:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='460dff59e58d77980d8f3aa3172f53d09c17beca1a16b5762f388aee8c91656c';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='f6d3b8e1f76c1dac5c9955ba77571e8e77aa02724f7423737627244174f41d5e';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='33cdf9b2bd4699ff76fb17f8d62d8ffc86ebf05296c626bf298f4c2bc140023a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='3a65331f4c4b671a5e5bb3ae4e4a65fd0eb5bf8672c0c2fba6ba36972c4042a4';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 20 Apr 2026 23:10:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:10:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:10:14 GMT
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
	-	`sha256:ade2bf5ef9def46818317b3cbd9f52f7cbe5cdf22659a24033914672294ab731`  
		Last Modified: Mon, 20 Apr 2026 23:10:50 GMT  
		Size: 63.7 MB (63722776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4238312cfe58cb47c279795e4f7236e420ec1b3941483bf4c48010265c363eaf`  
		Last Modified: Mon, 20 Apr 2026 23:10:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe45d37cee14f172f8c03b55152a8910c3340d7fff404e361e97a581200f8c0`  
		Last Modified: Mon, 20 Apr 2026 23:10:48 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26_35-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8b874b5d7e969ffd9591f848e108ebd710f11e353a09962dc0f45cb41bc6f362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3720024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d26af65cf34cb8c0c2f77ca1ddfb0107c8e0276eebca058fc0b594e581d3ea88`

```dockerfile
```

-	Layers:
	-	`sha256:a1cf897e65da9566e0f4d0b5d57743d0872b5d8be6f5ef2910055d09233e781e`  
		Last Modified: Mon, 20 Apr 2026 23:10:48 GMT  
		Size: 3.7 MB (3699738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e2f04cdd622185c61880f45b5900c6f35999d1d3f01428ef1a52bfa2a6d9ef7`  
		Last Modified: Mon, 20 Apr 2026 23:10:48 GMT  
		Size: 20.3 KB (20286 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26_35-jre-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:e2ee54c4a10ab08f5f38a988defae2f5d718927b84fb756cfcfe1d7ad289e0cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134365191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a10865f521d7fe6f319cd7e43d5833b07ab43a5de4629c3650e6f8b5b4b424f`
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
ENV JAVA_VERSION=jdk-26+35
# Mon, 20 Apr 2026 23:16:48 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='460dff59e58d77980d8f3aa3172f53d09c17beca1a16b5762f388aee8c91656c';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='f6d3b8e1f76c1dac5c9955ba77571e8e77aa02724f7423737627244174f41d5e';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='33cdf9b2bd4699ff76fb17f8d62d8ffc86ebf05296c626bf298f4c2bc140023a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='3a65331f4c4b671a5e5bb3ae4e4a65fd0eb5bf8672c0c2fba6ba36972c4042a4';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 20 Apr 2026 23:16:53 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:16:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:16:57 GMT
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
	-	`sha256:b25aad5ba6bce148f056441cd679843608c8a4669619d608e51e1d2bec8235bf`  
		Last Modified: Mon, 20 Apr 2026 23:19:11 GMT  
		Size: 62.1 MB (62070706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a9ac0f56472ad724760ba08109997d83efba12ecef68b86959a80b08d366ff`  
		Last Modified: Mon, 20 Apr 2026 23:18:56 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0db4f3e999c7b01b5929b0f120f18d321a15e4b6981356dbecc15e0e703a785`  
		Last Modified: Mon, 20 Apr 2026 23:18:56 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26_35-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:0fea159850242be9de83e726d5a11f2801d0f533f825139123ced57227ef041d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3721240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2955be80c5d5566e1a54bb9a196efe1d2569c4325c07772d0f9ded9c94e570e`

```dockerfile
```

-	Layers:
	-	`sha256:956c365923aa6d5a0d4f322a64ff11be95c761ee82a3c6fdab7fcb684f7db28a`  
		Last Modified: Mon, 20 Apr 2026 23:19:03 GMT  
		Size: 3.7 MB (3700983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf251edc07398bdd06c06245c5cc7e96c0b0524347506b512621753c4c4fb640`  
		Last Modified: Mon, 20 Apr 2026 23:18:56 GMT  
		Size: 20.3 KB (20257 bytes)  
		MIME: application/vnd.in-toto+json
