## `eclipse-temurin:17-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:5ea6d484ac9bb745ce30c6e6edbd2d5864cddc9e07ca27b1f61cffc34c6d1d76
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

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:0543e7cdead4bd897bec70a28fd1dafed64cd8f17dbfdc246caaf1e9e64009d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117833101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a422127b9c0095b3f349a4723267fd4b47211f9d6e9d86f3bb66d59740944662`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 22 Apr 2026 04:58:45 GMT
ENV container oci
# Wed, 22 Apr 2026 04:58:45 GMT
COPY dir:82e03e3ceb4a712116e9d6ecd1b99e2e729a68954b82c791f435d1cb8db14f8a in /      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 04:58:46 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:bc4dcbf01192949338f7e5550a4152e5364437463c0f897fd55b15eb58f57ead in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:bc4dcbf01192949338f7e5550a4152e5364437463c0f897fd55b15eb58f57ead in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 04:58:46 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "org.opencontainers.image.revision"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "build-date"="2026-04-22T04:58:33Z" "org.opencontainers.image.created"="2026-04-22T04:58:33Z" "release"="1776833838"org.opencontainers.image.revision=5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1,org.opencontainers.image.created=2026-04-22T04:58:33Z
# Wed, 22 Apr 2026 18:16:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:16:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:16:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:16:38 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:16:38 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 22 Apr 2026 18:17:03 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 22 Apr 2026 18:17:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:17:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:17:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:c770e69088fa05bea8942da1c1e3fa6066cc7c288153d81443e0c9435861e0b1`  
		Last Modified: Wed, 22 Apr 2026 05:40:43 GMT  
		Size: 40.0 MB (40024775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715e016f3b02c61aebe139a7d43fdbf956ea4c9f16880784ea639724e531587e`  
		Last Modified: Wed, 22 Apr 2026 18:16:54 GMT  
		Size: 30.4 MB (30368144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cac490468a1884eebc618cb9a9af708bb9cd0890bbf46a1f3e580213f2aa884`  
		Last Modified: Wed, 22 Apr 2026 18:17:16 GMT  
		Size: 47.4 MB (47437765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4c7db9304a576707a93bb8bfa70bd61d211c8f462de046776406c2b4bbaccc`  
		Last Modified: Wed, 22 Apr 2026 18:17:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfdf7043768de7610f3158e6c24005ee148eb8a85958b2d43a2861f2fe73bc2`  
		Last Modified: Wed, 22 Apr 2026 18:17:15 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d9cc86ebdf9029f0947e8bd9da0d1f2f866671a04a767994f8420a356db9b0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2435895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff76979b86b6c9856c95b7995137cdf7bbe7b5ea638c4558221bcc168f497f6`

```dockerfile
```

-	Layers:
	-	`sha256:33850bb1d926e5b2818059a1b1b266656c4fa6293038b272bdfa311b7a358764`  
		Last Modified: Wed, 22 Apr 2026 18:17:15 GMT  
		Size: 2.4 MB (2415709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe4485d85e45cad6c61ea96a261f4a46dbd034e4a3f0d356422217d85e8337e0`  
		Last Modified: Wed, 22 Apr 2026 18:17:15 GMT  
		Size: 20.2 KB (20186 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:9c251cd69b9bcad5befe415b31e07f5b2b9726769ec2a8c8b78f6b88a20727c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115915047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41922ed1d019a80f8ef6cd9011c6a81f6e0219e9eab9e11c41dce17d64055094`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 22 Apr 2026 05:00:29 GMT
ENV container oci
# Wed, 22 Apr 2026 05:00:30 GMT
COPY dir:5dfc5d431dcfd4937d8e6a4dd1184486112214c6f8d103a0640fb0f8231a0840 in /      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:00:30 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:15cced1d80c5bc31ac720f4e201d7d85c034d443588a80d803a468e8714fc167 in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:15cced1d80c5bc31ac720f4e201d7d85c034d443588a80d803a468e8714fc167 in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:00:31 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "org.opencontainers.image.revision"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "build-date"="2026-04-22T05:00:16Z" "org.opencontainers.image.created"="2026-04-22T05:00:16Z" "release"="1776833838"org.opencontainers.image.revision=5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1,org.opencontainers.image.created=2026-04-22T05:00:16Z
# Wed, 22 Apr 2026 18:16:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:16:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:16:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:16:25 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:16:25 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 22 Apr 2026 18:16:28 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 22 Apr 2026 18:16:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:16:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:16:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:c57a97b2502dbf8d905aa782f6a2be8f57c8774e28f6d2ddf6a9a866fcc5fd8b`  
		Last Modified: Wed, 22 Apr 2026 06:11:08 GMT  
		Size: 38.2 MB (38204491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9b92761190347404fdb97c5aac238f6279846a0141af4079c151a852095f51`  
		Last Modified: Wed, 22 Apr 2026 18:16:41 GMT  
		Size: 30.8 MB (30793045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c81442d4b08ccd827f916f62c06a532a38d5488175f77740af0d0160b076bc8`  
		Last Modified: Wed, 22 Apr 2026 18:16:42 GMT  
		Size: 46.9 MB (46915095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e975571e3cb18fe1e2de2ed9f9b3f31abeadbaea5bd5792de78e1ab8fa61cc2d`  
		Last Modified: Wed, 22 Apr 2026 18:16:40 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f8bad0df4a13a38717c4bc29d3a70080eccc78e7dc27134b6660421560bf61`  
		Last Modified: Wed, 22 Apr 2026 18:16:40 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e545af5a4965b4f89ad1ad53995ad931db07d11e85a67b17a913d4a7ecf30b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2435357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0049351127bff5deb5a694c8d2d54bf93cfcf2db89abde967909e14169aa13`

```dockerfile
```

-	Layers:
	-	`sha256:37717d7be0521d1f18dd021ed31deb99718ba3f657bd81640a9276aa3b7693bf`  
		Last Modified: Wed, 22 Apr 2026 18:16:40 GMT  
		Size: 2.4 MB (2415067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:716c2377a635e6fba63f0010900a8cce22abac4e64275c8f64b1e3b249be7325`  
		Last Modified: Wed, 22 Apr 2026 18:16:40 GMT  
		Size: 20.3 KB (20290 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:f56b1dd979c46dc714c7169f6c37eff110e99a5c833af4c2f9483779adf66b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124648593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97c38c342fb9ca304ec44b3f9db689468e28ef061d98e1c3aceae2892291603`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 22 Apr 2026 05:00:40 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:00:40 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:00:40 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:00:40 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 05:00:40 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:00:40 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 05:00:40 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:00:40 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:00:40 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 22 Apr 2026 05:00:40 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:00:40 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 22 Apr 2026 05:00:40 GMT
ENV container oci
# Wed, 22 Apr 2026 05:00:41 GMT
COPY dir:64d89a0791e483d93b8120232af287f142393e4b26204ca8e9d413579a7621dc in /      
# Wed, 22 Apr 2026 05:00:41 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:00:41 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:00:41 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:00:41 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:00:41 GMT
COPY file:b9343f1f830fdc49b9002ee6aa5a844e10cdd31908dcdf99bb99d96ab1cd10e8 in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:00:41 GMT
COPY file:b9343f1f830fdc49b9002ee6aa5a844e10cdd31908dcdf99bb99d96ab1cd10e8 in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:00:42 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "org.opencontainers.image.revision"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "build-date"="2026-04-22T05:00:30Z" "org.opencontainers.image.created"="2026-04-22T05:00:30Z" "release"="1776833838"org.opencontainers.image.revision=5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1,org.opencontainers.image.created=2026-04-22T05:00:30Z
# Wed, 22 Apr 2026 20:21:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 20:21:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 20:21:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 20:21:58 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 20:21:58 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 22 Apr 2026 20:26:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 22 Apr 2026 20:26:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 20:26:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 20:26:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:28663efab1a306aabfe7842862a237f686ae21b0a05ccde5f2365ef27c5851f4`  
		Last Modified: Wed, 22 Apr 2026 06:11:28 GMT  
		Size: 44.5 MB (44450308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dfd8bff75494960ba01bdf125622a2fc77fa106d9aa47c1fe85de69113a1d6`  
		Last Modified: Wed, 22 Apr 2026 20:22:48 GMT  
		Size: 32.8 MB (32848958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e12d5af02dee9a789e4d5fcdd45c529460f125a2c36362417344cb6c6cd6c5`  
		Last Modified: Wed, 22 Apr 2026 20:26:47 GMT  
		Size: 47.3 MB (47346906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1db6394eb56183364c173cfefe372b6526dc90a2e48e505acdecf6b6c1afedc`  
		Last Modified: Wed, 22 Apr 2026 20:26:45 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284a377aa09c92cda9f0d938d4ff8e07a127e4e84163a98ca101989cee75365e`  
		Last Modified: Wed, 22 Apr 2026 20:26:45 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3c5c9745329bae92de8a1e7e8463ffc1e0001df0eef4544859ee5c1d49884ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2435930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c67b32ac0147a5b311487110537e0d107874713cbdee7b1b2cc3d86c6670c7`

```dockerfile
```

-	Layers:
	-	`sha256:03152db36380c0f2007e8505ab93fb9b9e384d4f58dcbc3bc3e44b9bf3fde38c`  
		Last Modified: Wed, 22 Apr 2026 20:26:45 GMT  
		Size: 2.4 MB (2415714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7028724fd278deda035a0edf6e5e3f6f03ff1e096b7563971042edb9370198c2`  
		Last Modified: Wed, 22 Apr 2026 20:26:45 GMT  
		Size: 20.2 KB (20216 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:1b479432e94a08f209b75d0ed0a68a370f86532c66e3e5c06c2e7af29600f1d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112922398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf711c23a0bcecc56bfe071fb4c75ed498b2e5c1e0d5a0831debc4aa73f10a1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 22 Apr 2026 05:05:14 GMT
ENV container oci
# Wed, 22 Apr 2026 05:05:14 GMT
COPY dir:c10b61f0eaab474f87333058b5f0be076d9ca7550d40201126b259b146635cf0 in /      
# Wed, 22 Apr 2026 05:05:15 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:05:15 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:05:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:05:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:05:15 GMT
COPY file:94195acb2e6e678de51e9e05a9e10397a92e2f336a7de1f63b19aacc4230b754 in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:05:15 GMT
COPY file:94195acb2e6e678de51e9e05a9e10397a92e2f336a7de1f63b19aacc4230b754 in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:05:15 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "org.opencontainers.image.revision"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "build-date"="2026-04-22T05:05:02Z" "org.opencontainers.image.created"="2026-04-22T05:05:02Z" "release"="1776833838"org.opencontainers.image.revision=5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1,org.opencontainers.image.created=2026-04-22T05:05:02Z
# Wed, 22 Apr 2026 18:16:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:16:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:16:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:16:26 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:16:26 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 22 Apr 2026 18:18:54 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='88727c16610d118c0e739f62e6c99dc1cb5a7b4a93a27054fe2a3aa7150e7b5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='62a8263401366dea8a41c44a4e5d8b0d22b1f682e9084f124483441fee57044e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='b8801322ff3bf58ba06efde1ef4a23edc728de3d58e7bf6fd1e58815b0e8d6ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='8b418e38cca87945858ae911988401720095eb671357d47437b4adb49c28dcab';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 22 Apr 2026 18:18:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:19:01 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:19:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:aac8159c3d9a48859bb2e3c581e3c2dc900b6a0665fa45fbd980e797d234b4a6`  
		Last Modified: Wed, 22 Apr 2026 06:11:17 GMT  
		Size: 38.1 MB (38131833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36bcbe215132f57438e633085ed9ba659acbb28bba079eaccc56fd117fd63d3`  
		Last Modified: Wed, 22 Apr 2026 18:17:46 GMT  
		Size: 30.4 MB (30386245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe0fbcc8eb1e8840b087cb0ac892793c5e0a443823a007a7a41ec03f1015ec2`  
		Last Modified: Wed, 22 Apr 2026 18:19:54 GMT  
		Size: 44.4 MB (44401904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8663ffa76fd2e4f2a2b78372423a35db2426fed13285e5316a1fafb303b8bd7b`  
		Last Modified: Wed, 22 Apr 2026 18:19:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a0242c7f1222a4dccd3a3d1c26f2c13fef1487976a8b81f4ad6986d95f759d`  
		Last Modified: Wed, 22 Apr 2026 18:19:50 GMT  
		Size: 2.3 KB (2287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:fd16ae7eeb42a062e724dcbd90fba60f1af1bc1b4e08cc7b7e3e4d02cd62ad95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2427686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417da994d8636decba90e7469f542e28a2bd99a3d1a17af66f84b836ef19ed32`

```dockerfile
```

-	Layers:
	-	`sha256:ffaf4347efea451de38ef7aa43e630c9e8c0a02d1b692686d0d02284b9e4ab2a`  
		Last Modified: Wed, 22 Apr 2026 18:19:51 GMT  
		Size: 2.4 MB (2407501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81958223541070e1ef609b97430b03abbb6a7e1e254f9c7c9c7c93f1f6ca160e`  
		Last Modified: Wed, 22 Apr 2026 18:19:51 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json
