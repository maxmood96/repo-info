## `eclipse-temurin:8u492-b09-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:102e9cdcf978194053dbd4426a4f992caaf12e6b50e3f9d484ee155359fddc6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8u492-b09-jdk-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:a288dbbb43011ff19ca3884140edc3b2831fa90ce31520f0cb5db0cf6ba8d611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127877037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b126fe7bb0082ab085d9520267c0d1c9911ebae4cdc3e362eaa387c374bfa7c3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 15 Jun 2026 07:46:40 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 07:46:40 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 07:46:40 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 07:46:40 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Mon, 15 Jun 2026 07:46:40 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 07:46:40 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 15 Jun 2026 07:46:40 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 07:46:40 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 07:46:40 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 15 Jun 2026 07:46:40 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 07:46:40 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 15 Jun 2026 07:46:40 GMT
ENV container oci
# Mon, 15 Jun 2026 07:46:41 GMT
COPY dir:6795a8753f13601990edb5b5276cfe7486fb53104b262115fb35fe817c2adf3b in /      
# Mon, 15 Jun 2026 07:46:41 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 07:46:41 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 07:46:41 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 07:46:41 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 07:46:41 GMT
COPY file:014278f73576f2def6d5cfa868c2c290482e8fb486fcfb5b865bcdf04c8c034a in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 07:46:41 GMT
COPY file:014278f73576f2def6d5cfa868c2c290482e8fb486fcfb5b865bcdf04c8c034a in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 07:46:41 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="a079bd1cc91523a60704cf840463d737ba8b63de" "org.opencontainers.image.revision"="a079bd1cc91523a60704cf840463d737ba8b63de" "build-date"="2026-06-15T07:46:21Z" "org.opencontainers.image.created"="2026-06-15T07:46:21Z" "release"="1781509346"org.opencontainers.image.revision=a079bd1cc91523a60704cf840463d737ba8b63de,org.opencontainers.image.created=2026-06-15T07:46:21Z
# Mon, 15 Jun 2026 23:13:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 15 Jun 2026 23:13:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:13:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 15 Jun 2026 23:13:30 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:13:30 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Mon, 15 Jun 2026 23:13:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 15 Jun 2026 23:13:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 15 Jun 2026 23:13:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:13:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0166415a5628b463967ca89a95832b5ecafa81aeddaca2f8713bec6e36a3c9c0`  
		Last Modified: Mon, 15 Jun 2026 08:52:54 GMT  
		Size: 34.9 MB (34914006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3480c47e9ddf646af91e12f42ceec266da174e63e82ba50e665624618b81732`  
		Last Modified: Mon, 15 Jun 2026 23:13:48 GMT  
		Size: 37.8 MB (37761250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688719a2aa5d36c3b80572ca0dd20927ad356c425af52dd7b7cb7eac72afa88e`  
		Last Modified: Mon, 15 Jun 2026 23:13:49 GMT  
		Size: 55.2 MB (55199164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f7a53cdf9bdf6eb914e6fca9ea1603b856b01e48532f316b70d449bbba2028`  
		Last Modified: Mon, 15 Jun 2026 23:13:46 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2a141fd84aa169b0a966b382d1d8d53846308c721a4a72a6e062fc1ce1565c`  
		Last Modified: Mon, 15 Jun 2026 23:13:48 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u492-b09-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1a82b2751463ef629b9ef10fe6216c6ef9a58aaa68ad120f8bb04b2e2b0c20b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3932753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced36dacc530f941902937baef1395eb334f6da3a96f14ddd0595af927939cbc`

```dockerfile
```

-	Layers:
	-	`sha256:8c851800d688002470c5ca513c083d03cd975fcee74fc981b6e5d1e692ed85d5`  
		Last Modified: Mon, 15 Jun 2026 23:13:47 GMT  
		Size: 3.9 MB (3912715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d147ffddf16ea24302b45e8daec33a656f79e8bdb4e459755e641f211bae578b`  
		Last Modified: Mon, 15 Jun 2026 23:13:46 GMT  
		Size: 20.0 KB (20038 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u492-b09-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:16c85aebb63acdf2891fff38b9bbf0f1bb0fa643b92db0249e37bf0bc0bb7e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.0 MB (124992898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19fe96460cc62171169d19e7320108e4d3e31c5fd86e78a4c6d3e70fc217c548`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 15 Jun 2026 07:49:48 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 07:49:48 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 07:49:48 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 07:49:48 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Mon, 15 Jun 2026 07:49:48 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 07:49:48 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 15 Jun 2026 07:49:49 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 07:49:49 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 07:49:49 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 15 Jun 2026 07:49:49 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 07:49:49 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 15 Jun 2026 07:49:49 GMT
ENV container oci
# Mon, 15 Jun 2026 07:49:49 GMT
COPY dir:96cf4a952c323db93c5acbd83a80198d6d4c582c6075283779408766bc1f06a0 in /      
# Mon, 15 Jun 2026 07:49:49 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 07:49:50 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 07:49:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 07:49:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 07:49:50 GMT
COPY file:d017e9e035ec2f71c8ca63bbb7b57216ba5aad41669dc424f097659ae0649922 in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 07:49:50 GMT
COPY file:d017e9e035ec2f71c8ca63bbb7b57216ba5aad41669dc424f097659ae0649922 in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 07:49:50 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="a079bd1cc91523a60704cf840463d737ba8b63de" "org.opencontainers.image.revision"="a079bd1cc91523a60704cf840463d737ba8b63de" "build-date"="2026-06-15T07:49:33Z" "org.opencontainers.image.created"="2026-06-15T07:49:33Z" "release"="1781509346"org.opencontainers.image.revision=a079bd1cc91523a60704cf840463d737ba8b63de,org.opencontainers.image.created=2026-06-15T07:49:33Z
# Mon, 15 Jun 2026 23:13:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 15 Jun 2026 23:13:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:13:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 15 Jun 2026 23:13:14 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:13:14 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Mon, 15 Jun 2026 23:13:18 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 15 Jun 2026 23:13:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 15 Jun 2026 23:13:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:13:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:2181b76d100cfec8fecaf70c9c757671f616064b9f875b0fb509a7b6a6788ac5`  
		Last Modified: Mon, 15 Jun 2026 09:25:44 GMT  
		Size: 33.0 MB (33030316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77be5ab4486c50b066d6767d2553495020dc6532a6d9f87269f718bd482b5b7`  
		Last Modified: Mon, 15 Jun 2026 23:13:33 GMT  
		Size: 37.7 MB (37686528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd75f0d05790162e97b4a4a6b10070d4c6590f4dafb7b1a5a8482e7d281b756`  
		Last Modified: Mon, 15 Jun 2026 23:13:34 GMT  
		Size: 54.3 MB (54273435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32c810d54b99729b95914e9e53fa2b69d3da49001fff13a8245c23c8db8d0fd`  
		Last Modified: Mon, 15 Jun 2026 23:13:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bea3eaaadf948682b62a44ffa1d6ce61aff4c300efd999d3c4316340d971299`  
		Last Modified: Mon, 15 Jun 2026 23:13:32 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u492-b09-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:69f26551d68257ed678b928643d000cddc3152e2fb8fea8e90e2da4860ffd4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3932996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7273644a9f928ff0960a67eedb6b288bd1fd2f9e4295ab4b5f5d2e26f8d1e9`

```dockerfile
```

-	Layers:
	-	`sha256:9fa1c1f782e2e897eb983d98286e1de8d648d5fe06eb5aaed7ddfe1d9d9aa321`  
		Last Modified: Mon, 15 Jun 2026 23:13:32 GMT  
		Size: 3.9 MB (3912841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76743a440a402d6f4caa8d83596046db2898edf495da97ff8178241bad893b37`  
		Last Modified: Mon, 15 Jun 2026 23:13:32 GMT  
		Size: 20.2 KB (20155 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u492-b09-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:739780e9ac484c6f2ad495ede9faedbfba3e0fb6ad8444f67d8dcc93f8993c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131231725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957ea55894e29f3e5f182b552a3480e01531330811b018966a584c626989bd86`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 15 Jun 2026 07:46:33 GMT
ENV container oci
# Mon, 15 Jun 2026 07:46:34 GMT
COPY dir:83033203513f54fa7ad30157591855861b9bdeeadfcfaa7b39d928026e30a43e in /      
# Mon, 15 Jun 2026 07:46:34 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 07:46:34 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 07:46:34 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 07:46:34 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 07:46:34 GMT
COPY file:947556a1605dd2da1e7f452e2373e0e1a5352a517c46fbfad7c39a76efb34831 in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 07:46:34 GMT
COPY file:947556a1605dd2da1e7f452e2373e0e1a5352a517c46fbfad7c39a76efb34831 in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 07:46:34 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="a079bd1cc91523a60704cf840463d737ba8b63de" "org.opencontainers.image.revision"="a079bd1cc91523a60704cf840463d737ba8b63de" "build-date"="2026-06-15T07:46:22Z" "org.opencontainers.image.created"="2026-06-15T07:46:22Z" "release"="1781509346"org.opencontainers.image.revision=a079bd1cc91523a60704cf840463d737ba8b63de,org.opencontainers.image.created=2026-06-15T07:46:22Z
# Mon, 15 Jun 2026 23:14:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 15 Jun 2026 23:14:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:14:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 15 Jun 2026 23:14:23 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:14:23 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Mon, 15 Jun 2026 23:14:29 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 15 Jun 2026 23:14:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 15 Jun 2026 23:14:30 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:14:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:2228c93141e55e5881a02fe1a8f242a1e8a66f3a905f628abec2236bd3b86b02`  
		Last Modified: Mon, 15 Jun 2026 12:17:19 GMT  
		Size: 39.0 MB (39037515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db47c543a6c879ca8da9aa74d1ba869d99590c43dc077909f584eca08199b2a`  
		Last Modified: Mon, 15 Jun 2026 23:15:00 GMT  
		Size: 39.5 MB (39521864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111321d3188ea29432dff9af02550c28918d595330adb7255e3fc322071171eb`  
		Last Modified: Mon, 15 Jun 2026 23:15:00 GMT  
		Size: 52.7 MB (52669727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7c53e6db5c7a1ca771c2fdff58966e30f9fbbfc161d2e85c88ed7e1212feae`  
		Last Modified: Mon, 15 Jun 2026 23:14:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091baecea99edd0282ebdd17fdbb6b2a738d8741eab57720382a8509e98bbaf3`  
		Last Modified: Mon, 15 Jun 2026 23:14:50 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u492-b09-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:45786a31362cd45a16585ce6ac3a4e4e2ca0863414bcd7ed5bdf5083c35f5426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3920216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c469e3cba6bead7727bf3df361dd3381119c9489b5120c22358ba4b1d51ec09f`

```dockerfile
```

-	Layers:
	-	`sha256:f7f9a9ccf8c2032fa2ee56c94607e98e2978ea937092fd682fc865ba1fce989f`  
		Last Modified: Mon, 15 Jun 2026 23:14:57 GMT  
		Size: 3.9 MB (3900142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8abfa29b074ede5c67111e043f12ab64521d3712098ab2cf985a3c2333106b7a`  
		Last Modified: Mon, 15 Jun 2026 23:14:57 GMT  
		Size: 20.1 KB (20074 bytes)  
		MIME: application/vnd.in-toto+json
