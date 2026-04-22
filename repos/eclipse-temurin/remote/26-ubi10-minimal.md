## `eclipse-temurin:26-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:06ed1a808065fd48a5ff58d5289bfaab9874b95f98ce4fd4614eea34c8bb96fa
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

### `eclipse-temurin:26-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:0f7bc2b115a72b6e5d83f3a24ebf7cd1e61adff899ee578c1dbb04760cf4c25c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166520523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a92644072c96596d00ed72c4ae44aca92a260f2b6d60c0c6ac37d49f7c6d6e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 22 Apr 2026 05:17:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:17:54 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:17:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:17:54 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 22 Apr 2026 05:17:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:17:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 22 Apr 2026 05:17:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:17:55 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:17:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 22 Apr 2026 05:17:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:17:55 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 22 Apr 2026 05:17:55 GMT
ENV container oci
# Wed, 22 Apr 2026 05:17:55 GMT
COPY dir:dff10165caa8c30a8c2673a95ace4a09e747d1c9e656d37fe7e2593a4192cea1 in /      
# Wed, 22 Apr 2026 05:17:55 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:17:55 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:17:55 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:17:55 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:17:55 GMT
COPY file:1096e68e00ce2e3d16a7fbd65fd0781406fccc42abee623e8fa1f8395c75478b in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:17:56 GMT
COPY file:1096e68e00ce2e3d16a7fbd65fd0781406fccc42abee623e8fa1f8395c75478b in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:17:56 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "org.opencontainers.image.revision"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "build-date"="2026-04-22T05:17:41Z" "org.opencontainers.image.created"="2026-04-22T05:17:41Z" "release"="1776834797"org.opencontainers.image.revision=8f919d0175e713e927f4fc60c8a4a7f7d7d63a58,org.opencontainers.image.created=2026-04-22T05:17:41Z
# Wed, 22 Apr 2026 18:17:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:17:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:17:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:17:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:17:32 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 22 Apr 2026 18:17:38 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 22 Apr 2026 18:17:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:17:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:17:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Apr 2026 18:17:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:74bbdc6f81c25b3fa8d6367ec856d92f28db48c1860a008184a1d723c8d399cc`  
		Last Modified: Wed, 22 Apr 2026 06:14:16 GMT  
		Size: 34.6 MB (34590462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446a0aee2d15aaa238024fc63f6c75ba15856d38e0bbbeff9da1a3a450638639`  
		Last Modified: Wed, 22 Apr 2026 18:17:59 GMT  
		Size: 37.5 MB (37473595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26521de18c0cbd18f0803b3fc2eb45bdac4caf5d55a76e6667743e17bf3dbf1a`  
		Last Modified: Wed, 22 Apr 2026 18:18:00 GMT  
		Size: 94.5 MB (94454047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428dd31459ad2e2514d1b432ff3b6d9a377900bd8e5402d93ac7fd211052cb54`  
		Last Modified: Wed, 22 Apr 2026 18:17:57 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77fa5f504887197cb531aab54ed6d7ad1505c8d5091bf64493e810de2df879d`  
		Last Modified: Wed, 22 Apr 2026 18:17:58 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8241e82b1c620dacfcba7572113a81a1a019e6b86b3acc89ad87cd156a9ae327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3776514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9f17452e048139ff0de54216a755410bb0180ea2c28bf43bf86b3144d8f98e`

```dockerfile
```

-	Layers:
	-	`sha256:fb311259ce3bfcb495dc27179598693544522efe20eba32d402bc3b49341c1ae`  
		Last Modified: Wed, 22 Apr 2026 18:17:58 GMT  
		Size: 3.8 MB (3755297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77185d26812a839f7cefb9b2409be887fe6f60ad5dfd2c62e107195abf96f864`  
		Last Modified: Wed, 22 Apr 2026 18:17:57 GMT  
		Size: 21.2 KB (21217 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:d5d3ece8c9cb7929eb037990029cf5d181d05e8b0e747d86300c1fe6bb048911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163526926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a6f3607181506dc6f003d0b698e53f5aff348186f2324b293b67cf3144837e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 22 Apr 2026 05:20:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:20:36 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 22 Apr 2026 05:20:37 GMT
ENV container oci
# Wed, 22 Apr 2026 05:20:38 GMT
COPY dir:3a08e309561c3ef0f2f1f503de8f559ee625841311cafaf96b59ce47a8f1ffce in /      
# Wed, 22 Apr 2026 05:20:38 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:20:38 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:20:38 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:20:38 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:20:38 GMT
COPY file:70c2dda7fafaa9f54a42bab62bbf07c21fa030503d7cbb51eb7b6ef84bbbba51 in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:20:38 GMT
COPY file:70c2dda7fafaa9f54a42bab62bbf07c21fa030503d7cbb51eb7b6ef84bbbba51 in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:20:38 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "org.opencontainers.image.revision"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "build-date"="2026-04-22T05:20:21Z" "org.opencontainers.image.created"="2026-04-22T05:20:21Z" "release"="1776834797"org.opencontainers.image.revision=8f919d0175e713e927f4fc60c8a4a7f7d7d63a58,org.opencontainers.image.created=2026-04-22T05:20:21Z
# Wed, 22 Apr 2026 18:16:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:16:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:16:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:16:26 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:16:26 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 22 Apr 2026 18:17:00 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 22 Apr 2026 18:17:01 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:17:01 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:17:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Apr 2026 18:17:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8c4c206e9282db63c5bc98a6b172b79a7673404566e305674f0176bf9808f38`  
		Last Modified: Wed, 22 Apr 2026 06:16:01 GMT  
		Size: 32.7 MB (32712089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90cc0cfd04d8bf7d6ccd69d61211a956f29fcaea939aa0703b43a5889945a474`  
		Last Modified: Wed, 22 Apr 2026 18:16:44 GMT  
		Size: 37.4 MB (37416496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165b1e9b2701b27d76f50f8c9d4d5e63fb4450051e2dbc3681742a0cdaa1091a`  
		Last Modified: Wed, 22 Apr 2026 18:17:21 GMT  
		Size: 93.4 MB (93395922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1b22696d4d265096bb53638a3d45272f12e02ea8427fe2f2d5e5b560fd4fa9`  
		Last Modified: Wed, 22 Apr 2026 18:17:16 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa102225f8ac9d4ceb7eed421a4ced0e10149ecbbd758d24277bf6415b4c19c`  
		Last Modified: Wed, 22 Apr 2026 18:17:19 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d3713a86c5b7a2c52d4ac23c769caffb22b149287024e774c6af5197594f1788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3776053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24cacf9024a9f34c454e624abce57efd23c0c45e8df400b3ffbbeb857ff673c`

```dockerfile
```

-	Layers:
	-	`sha256:5e3daca0e0e4fb097e39d942fa747c8a72ac3a4d084b0ec0bb91ebf6f28d00ba`  
		Last Modified: Wed, 22 Apr 2026 18:17:19 GMT  
		Size: 3.8 MB (3754720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0b46c38307e648a88a18123bfa806539695e5e6aa197d6e996f50cf6dd9b88c`  
		Last Modified: Wed, 22 Apr 2026 18:17:18 GMT  
		Size: 21.3 KB (21333 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:ff86646e3cc6dfbbf8bcbedbe77d2ca469574717bd7cc4fb90d6c8d0942df7c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171743621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ce34768de630a27c62dfc773dca6802a0b7a2577bf07d1c6fd75b9adfff754`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 22 Apr 2026 05:19:25 GMT
ENV container oci
# Wed, 22 Apr 2026 05:19:26 GMT
COPY dir:8ebfd472fb6c3a18db13a69e93e153e014f1bb212fbd41469e95368f33c9855b in /      
# Wed, 22 Apr 2026 05:19:26 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:19:26 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:19:26 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:19:26 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:19:26 GMT
COPY file:1be71759ffffc91e186254d5919b2addc4c673e22dcd491b1496fe531cd50a49 in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:19:26 GMT
COPY file:1be71759ffffc91e186254d5919b2addc4c673e22dcd491b1496fe531cd50a49 in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:19:27 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "org.opencontainers.image.revision"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "build-date"="2026-04-22T05:19:14Z" "org.opencontainers.image.created"="2026-04-22T05:19:14Z" "release"="1776834797"org.opencontainers.image.revision=8f919d0175e713e927f4fc60c8a4a7f7d7d63a58,org.opencontainers.image.created=2026-04-22T05:19:14Z
# Wed, 22 Apr 2026 20:20:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 20:20:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 20:20:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 20:20:47 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 20:20:47 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 22 Apr 2026 20:30:35 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 22 Apr 2026 20:30:41 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 20:30:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 20:30:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Apr 2026 20:30:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:948a2ed1d2b45707813b0dd77e6a53e4f19eb962b9d9bd8172ed211361568ec7`  
		Last Modified: Wed, 22 Apr 2026 06:16:32 GMT  
		Size: 38.7 MB (38732470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2433584b22c8a5a7b6fce7b912874af7acd3331970ae9ba91fbe6f82ec3637a`  
		Last Modified: Wed, 22 Apr 2026 20:21:23 GMT  
		Size: 39.2 MB (39225692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ffeca0f54815557c025fef421fde73c5fd2349123de6a992deffbb687936e6`  
		Last Modified: Wed, 22 Apr 2026 20:31:22 GMT  
		Size: 93.8 MB (93783038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86523e409a3e8358de2887604c0dfe3f359e638ec0f9cbba8c03006bdac6c00`  
		Last Modified: Wed, 22 Apr 2026 20:31:19 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d98cd615a27de2bbfb195314d5fc2813387dec1bbe7dba15a77d259d53fdcf`  
		Last Modified: Wed, 22 Apr 2026 20:31:20 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3796a94eaa031bd0b696331d5aa22024dbd3bbe39cfaa2391322da6c0369cb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3747318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38af67c9e4c23e829bd2496d1f77fa000db0d4393238e82109f20e3ac905de23`

```dockerfile
```

-	Layers:
	-	`sha256:7d1053ddbeadf65c7c243db7b1e63470ed0a130e856765a8817c859d68094a87`  
		Last Modified: Wed, 22 Apr 2026 20:31:20 GMT  
		Size: 3.7 MB (3726065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d3069dcbc3947c196b1c1838719271117439d3f40cbccd609943801de065a07`  
		Last Modified: Wed, 22 Apr 2026 20:31:19 GMT  
		Size: 21.3 KB (21253 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:f9814fe2b6bac3ce0c8ee827db2fc81c2608bb815c81c9030f543bc9d048ec05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162838493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c4c81dec346fe4e8c48c3727db004b55314ed554551229fba7e0f7823f8333`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 22 Apr 2026 05:32:39 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:32:39 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:32:39 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:32:39 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 22 Apr 2026 05:32:39 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:32:39 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 22 Apr 2026 05:32:39 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:32:39 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:32:39 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 22 Apr 2026 05:32:39 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:32:39 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 22 Apr 2026 05:32:39 GMT
ENV container oci
# Wed, 22 Apr 2026 05:32:40 GMT
COPY dir:98278e95a3e2bb93450b2e648bccc4bc2352556303c23dd62fc4c7b46f277fc9 in /      
# Wed, 22 Apr 2026 05:32:40 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:32:40 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:32:40 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:32:40 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:32:40 GMT
COPY file:38c5f0375461f381e5db51646115279e3dad5b3c19eb862207cbc26ede0a9104 in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:32:40 GMT
COPY file:38c5f0375461f381e5db51646115279e3dad5b3c19eb862207cbc26ede0a9104 in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:32:40 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "org.opencontainers.image.revision"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "build-date"="2026-04-22T05:32:00Z" "org.opencontainers.image.created"="2026-04-22T05:32:00Z" "release"="1776834797"org.opencontainers.image.revision=8f919d0175e713e927f4fc60c8a4a7f7d7d63a58,org.opencontainers.image.created=2026-04-22T05:32:00Z
# Wed, 22 Apr 2026 18:16:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:16:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:16:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:16:22 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:16:22 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 22 Apr 2026 18:23:18 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 22 Apr 2026 18:23:26 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:23:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:23:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Apr 2026 18:23:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:59053ba8a9d1e0e09d61b1f59967bb9ffc4505ef8eebe01b4c6808d9bce8b3a6`  
		Last Modified: Wed, 22 Apr 2026 06:16:12 GMT  
		Size: 34.4 MB (34437922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cf755e7e06afeb41fd368fbfaae8e70f129c645bebe025cef69dbd8ac6c635`  
		Last Modified: Wed, 22 Apr 2026 18:17:40 GMT  
		Size: 37.8 MB (37849869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c1b6cf5c6abec1fd044d444af556f39a98168c58436d794173012a3fc03dec`  
		Last Modified: Wed, 22 Apr 2026 18:24:40 GMT  
		Size: 90.5 MB (90548283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38962e6908118ba21a78df1f30b1440bd0b95de374ded13565d9e4ea7e64bb3`  
		Last Modified: Wed, 22 Apr 2026 18:24:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59b06b7bd118d4f35996e1eef430168586debbafb3cf81a90eb6b29c08cca6b`  
		Last Modified: Wed, 22 Apr 2026 18:24:32 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f213276c7fc8782de4f72e61f22df41108eaf8436b2c8455791c684026499eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3747290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88052b8fa9dad76e9af1e2f402ad989ede96b298c00c254adff25de0886d1d6`

```dockerfile
```

-	Layers:
	-	`sha256:a6d1f177d2698db881154948a4c43b6576baa14534b625ca6cfff938030ffe81`  
		Last Modified: Wed, 22 Apr 2026 18:24:34 GMT  
		Size: 3.7 MB (3726073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f7231f4a4a6ab20c8c7258113cfcf0ef4b78eacae56d9f6b653d2d8fac7304d`  
		Last Modified: Wed, 22 Apr 2026 18:24:32 GMT  
		Size: 21.2 KB (21217 bytes)  
		MIME: application/vnd.in-toto+json
