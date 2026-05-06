## `eclipse-temurin:26_35-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:d47b3087788fa3241a91e65a4a5b1aafeab9027ed6f7be41953e2b6104a0ba30
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

### `eclipse-temurin:26_35-jdk-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:2fd390dbd93a01772523da31bf1c3d451c31dba967c6e6246cb22bf0f06e4adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151141914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f46f56dc56e8dba9f587dfe5f70c48a89207485c8dc84412b51295175da294`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 01:36:53 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:36:53 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:36:53 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:36:53 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 04 May 2026 01:36:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:36:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 04 May 2026 01:36:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:36:53 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:36:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 04 May 2026 01:36:53 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:36:53 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 04 May 2026 01:36:53 GMT
ENV container oci
# Mon, 04 May 2026 01:36:54 GMT
COPY dir:90d4f1f85494d2a8bf17340af60eb04fb8df2adbe40376c2198b52d03b3dce87 in /      
# Mon, 04 May 2026 01:36:54 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:36:54 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:36:54 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:36:54 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:36:54 GMT
COPY file:44acb722ff6847a849911ad1532360393cd9c16592e8d1f9e199cff925bbc7d5 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:36:54 GMT
COPY file:44acb722ff6847a849911ad1532360393cd9c16592e8d1f9e199cff925bbc7d5 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:36:54 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="2c4967ab62628fff803457df7635994ca0e85fbc" "org.opencontainers.image.revision"="2c4967ab62628fff803457df7635994ca0e85fbc" "build-date"="2026-05-04T01:36:38Z" "org.opencontainers.image.created"="2026-05-04T01:36:38Z" "release"="1777858393"org.opencontainers.image.revision=2c4967ab62628fff803457df7635994ca0e85fbc,org.opencontainers.image.created=2026-05-04T01:36:38Z
# Tue, 05 May 2026 23:07:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 May 2026 23:07:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:07:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 May 2026 23:07:52 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 05 May 2026 23:07:52 GMT
ENV JAVA_VERSION=jdk-26+35
# Tue, 05 May 2026 23:08:55 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 05 May 2026 23:08:56 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:08:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:08:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 May 2026 23:08:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6c2848906904fdb30be3302af6950faf3bb49f8acf1fe7da43266ab561f76092`  
		Last Modified: Mon, 04 May 2026 03:13:50 GMT  
		Size: 34.6 MB (34648199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3e0a0050aebaf322076b278aaa26e45de70bc1d097f52e23133bf4ba5f4590`  
		Last Modified: Tue, 05 May 2026 23:08:18 GMT  
		Size: 22.0 MB (22037220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba0618a2604ee602fbcc92422a624bcc53f1044e5f27737b0cca5db9d2ef40c`  
		Last Modified: Tue, 05 May 2026 23:09:13 GMT  
		Size: 94.5 MB (94454073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4cb66c9ae819e6b948d1093f5c6ef99e915d7aaf6831c073b1fce82174f30a`  
		Last Modified: Tue, 05 May 2026 23:09:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67de400cbb68fbc0a0c6b4f39189cb558133dc81af111a917266e77dc8e045d`  
		Last Modified: Tue, 05 May 2026 23:09:10 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26_35-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:dec858883474a57c194b7a7790af7bfe14f438a85f23c79713f72f9aeb73dc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6431dc0aa3bd1c77db290d533e54d1e3924b41603422cf4df17ccfc0b5279d`

```dockerfile
```

-	Layers:
	-	`sha256:812f646d2bfff81ea9a54781d95eb0465181895200ae08911161dd4b773f0070`  
		Last Modified: Tue, 05 May 2026 23:09:11 GMT  
		Size: 3.0 MB (3015517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f74dc3de678365470562a7b634dca38821bd99ceb11411dd6913018a4426fea9`  
		Last Modified: Tue, 05 May 2026 23:09:10 GMT  
		Size: 21.2 KB (21217 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26_35-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:976531b721102eea9384a9a5a603299a5a7b87a6c9b269bc29ed726d4e3ac2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148411669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf14dd4dd27ae9d2ed15568057a96c7583739a857fb3067dc3347e7232ad8499`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 01:38:51 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:38:51 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:38:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:38:51 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 04 May 2026 01:38:51 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:38:51 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 04 May 2026 01:38:51 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:38:51 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:38:51 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 04 May 2026 01:38:51 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:38:51 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 04 May 2026 01:38:51 GMT
ENV container oci
# Mon, 04 May 2026 01:38:52 GMT
COPY dir:4f490e44b5cd259c269df4e89626a736e4b70875a47bc79b960d52f7b56f7967 in /      
# Mon, 04 May 2026 01:38:52 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:38:52 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:38:52 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:38:52 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:38:53 GMT
COPY file:e2c2a2ab213ef0433a1e15d666daa6e664714283c2d03394bbfa240f7cd44679 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:38:53 GMT
COPY file:e2c2a2ab213ef0433a1e15d666daa6e664714283c2d03394bbfa240f7cd44679 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:38:53 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="2c4967ab62628fff803457df7635994ca0e85fbc" "org.opencontainers.image.revision"="2c4967ab62628fff803457df7635994ca0e85fbc" "build-date"="2026-05-04T01:38:35Z" "org.opencontainers.image.created"="2026-05-04T01:38:35Z" "release"="1777858393"org.opencontainers.image.revision=2c4967ab62628fff803457df7635994ca0e85fbc,org.opencontainers.image.created=2026-05-04T01:38:35Z
# Tue, 05 May 2026 23:08:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 May 2026 23:08:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:08:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 May 2026 23:08:33 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 05 May 2026 23:08:33 GMT
ENV JAVA_VERSION=jdk-26+35
# Tue, 05 May 2026 23:08:40 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 05 May 2026 23:08:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:08:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:08:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 May 2026 23:08:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:908809553a77ac560aff532a902be43c3a99a0dcb4f759158a75984cb82c4b9d`  
		Last Modified: Mon, 04 May 2026 06:16:39 GMT  
		Size: 32.7 MB (32711611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6f915afa26573d977d0c48d4ec88425b30f344fc5e7dc24c393b70eaf92055`  
		Last Modified: Tue, 05 May 2026 23:08:59 GMT  
		Size: 22.3 MB (22301728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d845fa6e7c1ed70f91b84ac5c5c269cf510b5d65c824ca95a1e7c6c90b772906`  
		Last Modified: Tue, 05 May 2026 23:09:01 GMT  
		Size: 93.4 MB (93395909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba176bd1f5744f4bf978a89bef0045fbc8d60fc2df5e3772c679e1c15c22c93`  
		Last Modified: Tue, 05 May 2026 23:08:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f835fe70579f8cb311c6c2dd6706543ff80914fb2ea0a2224e40308d483491e1`  
		Last Modified: Tue, 05 May 2026 23:08:43 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26_35-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e3ac2264385d3334b28e83562a0aa02f98dfe9d452aa57314829d6eed9f26d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5bab70e3eb693f822ce3bcb10bd9c7adbd93bbbfa6594fc5a86c637692c4a8`

```dockerfile
```

-	Layers:
	-	`sha256:eec1726aa9181c29aa581cb64b42b50f30573991c72ec019ff9fbbd908b144db`  
		Last Modified: Tue, 05 May 2026 23:08:58 GMT  
		Size: 3.0 MB (3014940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7b86f6ca262514434fce551d40b0afedcd603ba999652f04700154b93b5119`  
		Last Modified: Tue, 05 May 2026 23:08:58 GMT  
		Size: 21.3 KB (21333 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26_35-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:eb08e2f69c9ed3928f30f183e8e51dfd74b7ba39440e0349464b6f01733f4108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155865060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3dbd777b38793c1b966a64fa21a61405ae72a958f8fe24e5dda5f91f23c195`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 01:39:14 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:39:14 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:39:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:39:14 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 04 May 2026 01:39:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:39:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 04 May 2026 01:39:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:39:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:39:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 04 May 2026 01:39:15 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:39:15 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 04 May 2026 01:39:15 GMT
ENV container oci
# Mon, 04 May 2026 01:39:15 GMT
COPY dir:12413a5bdb80a75f63d061b3c0328d3ec0033dbb6ef2e4efcba8481b6ce277c7 in /      
# Mon, 04 May 2026 01:39:15 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:39:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:39:15 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:39:15 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:39:15 GMT
COPY file:727a91663c7c1ef3c87416ec38b4c09702b0fa948721f73b1c8c27f7a242068b in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:39:16 GMT
COPY file:727a91663c7c1ef3c87416ec38b4c09702b0fa948721f73b1c8c27f7a242068b in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:39:16 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="2c4967ab62628fff803457df7635994ca0e85fbc" "org.opencontainers.image.revision"="2c4967ab62628fff803457df7635994ca0e85fbc" "build-date"="2026-05-04T01:39:03Z" "org.opencontainers.image.created"="2026-05-04T01:39:03Z" "release"="1777858393"org.opencontainers.image.revision=2c4967ab62628fff803457df7635994ca0e85fbc,org.opencontainers.image.created=2026-05-04T01:39:03Z
# Tue, 05 May 2026 23:47:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 May 2026 23:47:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:47:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 May 2026 23:47:29 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 05 May 2026 23:47:29 GMT
ENV JAVA_VERSION=jdk-26+35
# Tue, 05 May 2026 23:56:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 05 May 2026 23:57:01 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:57:01 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:57:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 May 2026 23:57:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f2dd1d2c3d5fda579799f9becd292589fb99f0abc7f5c226856eb2bbbbc120cc`  
		Last Modified: Mon, 04 May 2026 06:16:51 GMT  
		Size: 38.7 MB (38745905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2ee71f34837c204e126c0f30bd59bdd1c1aad2d6a82e82078b6ce249102e06`  
		Last Modified: Tue, 05 May 2026 23:48:16 GMT  
		Size: 23.3 MB (23333693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45beaa663df5c57aa46e9ac8e5f75b2ef228a96fb70c40b61cf511d7a6d1603`  
		Last Modified: Tue, 05 May 2026 23:57:38 GMT  
		Size: 93.8 MB (93783041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1240fa8ad61a3a4ce10b1d2287222bb8b73e3221bf2701b60d33ee7a2e420fe4`  
		Last Modified: Tue, 05 May 2026 23:57:35 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ce06abd6d31a3753e3cb8786b00fc86e55bd9308c9c257f69b51da28d74f58`  
		Last Modified: Tue, 05 May 2026 23:57:35 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26_35-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:822a3beb5e521cf72f0c9c51b422f89a52d28355c3e9c9d256e008638a8e08d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c48c401474acd52e2f6fe5770c2745d776a58cd55cd07b9c4c1b77ea613013e`

```dockerfile
```

-	Layers:
	-	`sha256:75ce765ada159d2ce7cf753e5bfb8f752794331a431c04f157d0cd49c412214c`  
		Last Modified: Tue, 05 May 2026 23:57:36 GMT  
		Size: 3.0 MB (2993209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee95a4c8b934498fe8d7861cd53e8dfa5a0ff57d5abae6c17d344d9aa9714c60`  
		Last Modified: Tue, 05 May 2026 23:57:35 GMT  
		Size: 21.3 KB (21252 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26_35-jdk-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:c82f0382051b95c982e3ada7abda94c1bd9f4573db1eedaa52093221f8ae388d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147345707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c35967b532d1f36591f93a5ea9a00242b68f025f6bae00f4b7284d5c8d284ca`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 01:46:56 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:46:56 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:46:56 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:46:56 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 04 May 2026 01:46:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:46:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 04 May 2026 01:46:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:46:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:46:56 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 04 May 2026 01:46:56 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:46:56 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 04 May 2026 01:46:56 GMT
ENV container oci
# Mon, 04 May 2026 01:46:56 GMT
COPY dir:cacbd48510196fa765f2d5bccb8b2b0023c608fcbd86154b6fe34e775acd2483 in /      
# Mon, 04 May 2026 01:46:56 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:46:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:46:56 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:46:57 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:46:57 GMT
COPY file:6983ce2775fc6ec74b2d7c54d91fce16f639c26d824bf41c774ba5d5ae4037e9 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:46:57 GMT
COPY file:6983ce2775fc6ec74b2d7c54d91fce16f639c26d824bf41c774ba5d5ae4037e9 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:46:57 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="2c4967ab62628fff803457df7635994ca0e85fbc" "org.opencontainers.image.revision"="2c4967ab62628fff803457df7635994ca0e85fbc" "build-date"="2026-05-04T01:46:14Z" "org.opencontainers.image.created"="2026-05-04T01:46:14Z" "release"="1777858393"org.opencontainers.image.revision=2c4967ab62628fff803457df7635994ca0e85fbc,org.opencontainers.image.created=2026-05-04T01:46:14Z
# Wed, 06 May 2026 00:08:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 May 2026 00:08:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 00:08:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 May 2026 00:08:35 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 06 May 2026 00:08:35 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 06 May 2026 00:14:18 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 06 May 2026 00:14:19 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 06 May 2026 00:14:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 06 May 2026 00:14:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 May 2026 00:14:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e434a7e4a8db18a3b2f706d5c1b2a02cfe20f46083a805f7dcf9e2e92903aa2e`  
		Last Modified: Mon, 04 May 2026 06:16:45 GMT  
		Size: 34.4 MB (34430001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e050a10412e65251d89d72303bf35471e8696e8e4584956371e471d0f9f274c`  
		Last Modified: Wed, 06 May 2026 00:09:22 GMT  
		Size: 22.4 MB (22365043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea62c7f5723b17be38321922d9539dc251611cb6c6f93082718442292752a220`  
		Last Modified: Wed, 06 May 2026 00:14:53 GMT  
		Size: 90.5 MB (90548243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a6f8b56c3b7064bf44f46db98b2ba0fb3e1ced23571839bd5bca679dcf957`  
		Last Modified: Wed, 06 May 2026 00:14:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0823c7a828e96585e74c08be32cd62e8153595767460a5537aefa0aec7f5884`  
		Last Modified: Wed, 06 May 2026 00:14:52 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26_35-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4d6186d7c1a017482f01d0a95efcdc8d6a08662cc087b2c38c15d3050bc16d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13093dc9557918755112c4a16b2a18032932139d00e50a4aeed575e2056a94b9`

```dockerfile
```

-	Layers:
	-	`sha256:7d724d1d12cdec0c12ecb7dbc2bac74d6c90db86724924a231d5cfb05008e617`  
		Last Modified: Wed, 06 May 2026 00:14:52 GMT  
		Size: 3.0 MB (2993217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f94459ccb2f2f89d4ea322a9bd75f6992e3f26389b27e39a7a621bf313c6fbba`  
		Last Modified: Wed, 06 May 2026 00:14:52 GMT  
		Size: 21.2 KB (21216 bytes)  
		MIME: application/vnd.in-toto+json
