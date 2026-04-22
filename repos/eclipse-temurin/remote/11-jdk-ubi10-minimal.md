## `eclipse-temurin:11-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:65968caaf5bf6f63372368ad8a85ea4efbefe5f1c6d7763d433a03480dfb563f
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
$ docker pull eclipse-temurin@sha256:74d4d19b198e9724a2a88cdd29fb993c16f7b8c18c364b5a46f6fae9f498d20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.3 MB (214329803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5a62fd7cfc06710862f529bba65ceb582e3075bc3791e60c7c59ef11758776`
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
# Wed, 22 Apr 2026 18:16:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:16:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:16:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:16:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:16:57 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 22 Apr 2026 18:17:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 22 Apr 2026 18:17:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:17:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:17:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Apr 2026 18:17:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:74bbdc6f81c25b3fa8d6367ec856d92f28db48c1860a008184a1d723c8d399cc`  
		Last Modified: Wed, 22 Apr 2026 06:14:16 GMT  
		Size: 34.6 MB (34590462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d41196ccd4e6357d04e66818a2986ef060484d8d9c4eef783980a3f4804e700`  
		Last Modified: Wed, 22 Apr 2026 18:17:25 GMT  
		Size: 37.5 MB (37473595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a57d005cfedf217b2875866530e34639e7b8a867bab685aeb9d058da8ee65bb`  
		Last Modified: Wed, 22 Apr 2026 18:17:28 GMT  
		Size: 142.3 MB (142263327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6978f2b7e45eab8c674db894081531f3468106ef5a3272c965d6ea575d0ffc2b`  
		Last Modified: Wed, 22 Apr 2026 18:17:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c17a0e7c180a3537cf58d58aaf7358088bbf37b755ecffd47e62b6c7da7d300`  
		Last Modified: Wed, 22 Apr 2026 18:17:24 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:aeacc37765e0214ec4f67a3aad7a33592ab381b5d4585c21caa62d9fae1fb9b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3830633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880125006103ac80265e6f5eaa60dd6d1c6ab86d0b490900d3ccc94dd7df4ad6`

```dockerfile
```

-	Layers:
	-	`sha256:d595b29def13f66b84bb63f1a3316d8b12f40c724e8bfa1e43d8ff989a02dc92`  
		Last Modified: Wed, 22 Apr 2026 18:17:23 GMT  
		Size: 3.8 MB (3809317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de05c83705b16ebf5fcb041d54d68e1dd088ba1a5af6821f3fd7cbee33dbe42c`  
		Last Modified: Wed, 22 Apr 2026 18:17:23 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:f938395b501639531efcc02256aa9acb8c430ec3bd5face418e33159c04c91ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.1 MB (209090644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41451c513d7d19cb31f4517889b06ccef140532b0cb8ea1ec6591bd7f42a4db5`
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
# Wed, 22 Apr 2026 18:16:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:16:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:16:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:16:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:16:05 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 22 Apr 2026 18:16:11 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 22 Apr 2026 18:16:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:16:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:16:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Apr 2026 18:16:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8c4c206e9282db63c5bc98a6b172b79a7673404566e305674f0176bf9808f38`  
		Last Modified: Wed, 22 Apr 2026 06:16:01 GMT  
		Size: 32.7 MB (32712089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51fe502eb3aa9412ac47fe447396fc11182e0577ef6af51affcc47ddd8eecc1`  
		Last Modified: Wed, 22 Apr 2026 18:16:31 GMT  
		Size: 37.4 MB (37416384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa1678df243b8b5f523bbe26d05cbf29be8b443ca626dcf96123076ce9e0eeb`  
		Last Modified: Wed, 22 Apr 2026 18:16:34 GMT  
		Size: 139.0 MB (138959753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c5fa49ae118bb10727c5b041aca2f767c227a3715bb92a5bee87ad47b49e10`  
		Last Modified: Wed, 22 Apr 2026 18:16:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1877d120f32354e75604a46bc72c91181124c1246d362adfb8bdf94b08bf5e4d`  
		Last Modified: Wed, 22 Apr 2026 18:16:29 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a690e42fa71c3e0d8872dfd0fc02ea6d64ec74b6c5fd233b4287af6f67d22c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3830793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc90c1a7540d27272314b2212b13b8e42dd2aae6237121c2bce2bfaeea00860`

```dockerfile
```

-	Layers:
	-	`sha256:fe7d25b0b3c942f233dfbf57903459220dc72b50c7b4125b92b9d9fd9d200cda`  
		Last Modified: Wed, 22 Apr 2026 18:16:29 GMT  
		Size: 3.8 MB (3809361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11f925803784ee1d5656439772466b9b98ab4f5f6dfd11a2826a64c8aba8d234`  
		Last Modified: Wed, 22 Apr 2026 18:16:29 GMT  
		Size: 21.4 KB (21432 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:704293084ff7eb567cccc88c866d7954e2eb2b0cccdc0423532ddcd9ffc42b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.5 MB (207459811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97699f07befbdb67f2ef0c76e919bcc7abd2a8d18506ca1e6dd1e6f90ad8046`
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
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 22 Apr 2026 20:23:14 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 22 Apr 2026 20:23:17 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 20:23:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 20:23:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Apr 2026 20:23:17 GMT
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
	-	`sha256:c95aafc2834fbfb051e66dbff31502338adc5d6b571adee640eeb6bd3d2baead`  
		Last Modified: Wed, 22 Apr 2026 20:23:59 GMT  
		Size: 129.5 MB (129499229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9add103439253173d0c271d411af351cc8123948c2ed5cbf6e8ae264e8fd59e4`  
		Last Modified: Wed, 22 Apr 2026 20:23:56 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9dda3c42885d0a9d6557a8d45fa74884a3c5b397b98c054a24a06e48c693e9`  
		Last Modified: Wed, 22 Apr 2026 20:23:56 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ba011d861541fdb57e14471d47b71225e929fcc2b0a0368ed4cbe30265265c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3816886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0473a02df5b3ab52dcb00305ab84636e56e5a6599aaa19ee2a1755813f81b9`

```dockerfile
```

-	Layers:
	-	`sha256:98e8e6b51b1fdb58f9f3e0bde143c6d50101d22ed8987cd1d3c2bc777bfa623d`  
		Last Modified: Wed, 22 Apr 2026 20:23:56 GMT  
		Size: 3.8 MB (3795534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86777d3a678e5ceec9ba0cd91d2e044ab67010649b5d488003c8665aae0fcba9`  
		Last Modified: Wed, 22 Apr 2026 20:23:56 GMT  
		Size: 21.4 KB (21352 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:b761113f581effaf0408b3ead0af1ed21bc57b029793ae77b8a1871b06333d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195263026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99870ded13e31afc303c280d95826f7e99eb8ff5d0d48a69ae1491a9e14576e4`
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
# Wed, 22 Apr 2026 18:16:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:16:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:16:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:16:25 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:16:25 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 22 Apr 2026 18:16:35 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 22 Apr 2026 18:16:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:16:44 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:16:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Apr 2026 18:16:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:59053ba8a9d1e0e09d61b1f59967bb9ffc4505ef8eebe01b4c6808d9bce8b3a6`  
		Last Modified: Wed, 22 Apr 2026 06:16:12 GMT  
		Size: 34.4 MB (34437922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f5f9f574b3daeca8f4702cc891ece0285c63d8e300411023f5895f380e9f97`  
		Last Modified: Wed, 22 Apr 2026 18:18:11 GMT  
		Size: 37.9 MB (37850017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e9401308465847a08e2a66378a16f69a6c251e2d6fb1b4a3f23a02d99aeae3`  
		Last Modified: Wed, 22 Apr 2026 18:18:15 GMT  
		Size: 123.0 MB (122972667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c96dc50a9f120b1cfe010929de704291608ec3e2ff4710f8576bfb7c95c169`  
		Last Modified: Wed, 22 Apr 2026 18:17:54 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3905b762d4e8040009ecd27f8d9d7711974424a61f6730df5e6969f5353378`  
		Last Modified: Wed, 22 Apr 2026 18:17:54 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a1fd3c068886632e4d742173df6f73a9dfbe79f1d706fef00de6f5f850d9aef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3816226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845d7e2e97b812b39de5381fd85a8c6318d79f5277fe41bc195160643fd6e981`

```dockerfile
```

-	Layers:
	-	`sha256:724a2d1870d63747247bf7ad4d0719df2e6316fd6773b2c0be4c83b6043a7367`  
		Last Modified: Wed, 22 Apr 2026 18:17:58 GMT  
		Size: 3.8 MB (3794911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bb2048f2b86fc8e3e899c3e7316d249e3ec3b7c4266c54c31829500846d4704`  
		Last Modified: Wed, 22 Apr 2026 18:17:55 GMT  
		Size: 21.3 KB (21315 bytes)  
		MIME: application/vnd.in-toto+json
