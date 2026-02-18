## `eclipse-temurin:11-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:10cf3bcfb1e007a1126e30d4bc3ad08d6b166ecb181e80423d6aec99a5b07ffe
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

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:737ad1bda9c8d429767c0cc86946439742b73faed3109009945c075b76db9d53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 MB (212694799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5281a32a310caa2e8972e76be766afc5021a598c2458e36040bf877d67cda5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:42:45 GMT
ENV container oci
# Tue, 17 Feb 2026 16:42:46 GMT
COPY dir:a84da6f36b88f4eb0d6c411f65b34c1a9d85150d3035dd516db4ece0c2569465 in /      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:42:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:42:34Z" "org.opencontainers.image.created"="2026-02-17T16:42:34Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:42:34Z
# Wed, 18 Feb 2026 19:19:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 19:19:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 19:19:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Feb 2026 19:19:48 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 18 Feb 2026 19:19:48 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 18 Feb 2026 19:19:55 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Feb 2026 19:19:56 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Feb 2026 19:19:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Feb 2026 19:19:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Feb 2026 19:19:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4638e3415987f378f2d6dd70f9c6a2869dd5ebd09e3510ba45e46bbb6ec1a3dd`  
		Last Modified: Tue, 17 Feb 2026 18:08:54 GMT  
		Size: 40.0 MB (40033596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac03a88abd4187599fa907d148fcae6330fcc9bc77e4ada5451c9e359ae46d6c`  
		Last Modified: Wed, 18 Feb 2026 19:20:14 GMT  
		Size: 30.4 MB (30395494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e268a4330767e92f7385a2098f6ed4bfaaa04e6d61410ebb1b08d4365a93978e`  
		Last Modified: Wed, 18 Feb 2026 19:20:17 GMT  
		Size: 142.3 MB (142263290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5953c4b5971b2b57ff6574941ef7277cd4b95804d4444dbc3a57019f322b7b`  
		Last Modified: Wed, 18 Feb 2026 19:20:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3f48711fd21cb4c3ab51c1c8220ee78b000ee2b6f634b76ad0601335a73f7b`  
		Last Modified: Wed, 18 Feb 2026 19:20:01 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3d24a5cb5867db9d7a5eaf6ca729887c7f366eee4a1528a52fed3db31d4c0330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2540826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c9950cba7b0031b4de01d86835423e0d5fc4280a2ebeea2e199bafc8694352`

```dockerfile
```

-	Layers:
	-	`sha256:eff9a0dbd21c69d4a80e34568a835cda39890cf13ead72f19d5d61ba74c204c2`  
		Last Modified: Wed, 18 Feb 2026 19:20:13 GMT  
		Size: 2.5 MB (2519684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35ca50fae76425732cc1f0d67ed6c743f48e270ec93c518e245f0c006264633e`  
		Last Modified: Wed, 18 Feb 2026 19:20:13 GMT  
		Size: 21.1 KB (21142 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:2bb14cc3252f69522cb103a9170f515f45298ea25ad108679bfc7ac0a3da751f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 MB (207990409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3143c756f62102008fd227dbeee9fe68ec703f1128c077e24bdc67556e8a034`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:45:44 GMT
ENV container oci
# Tue, 17 Feb 2026 16:45:45 GMT
COPY dir:ac0ab1292a52ccb276077ed994531e1a3deef7d271c3502d95032264a0448d19 in /      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:45:45 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:46 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:45:31Z" "org.opencontainers.image.created"="2026-02-17T16:45:31Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:45:31Z
# Wed, 18 Feb 2026 19:16:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 19:16:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 19:16:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Feb 2026 19:16:40 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 18 Feb 2026 19:16:40 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 18 Feb 2026 19:17:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Feb 2026 19:17:35 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Feb 2026 19:17:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Feb 2026 19:17:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Feb 2026 19:17:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:063fbd5fac6af91f4042bbe66bae69795aa46675d5b0c800ed195ad79ed8fb02`  
		Last Modified: Tue, 17 Feb 2026 18:09:11 GMT  
		Size: 38.2 MB (38202534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a2646c40d44a7a462d59bb0a2fca3186042f1c52ec9253b267e1e7b03cc022`  
		Last Modified: Wed, 18 Feb 2026 19:16:59 GMT  
		Size: 30.8 MB (30825760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e04cf01cfbdc1855cc2015a8337bab81d5fdaf48c4fec04219f8c02c781bc19`  
		Last Modified: Wed, 18 Feb 2026 19:17:53 GMT  
		Size: 139.0 MB (138959695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5230e302931f8a662d839d45782a5523ba1fcd5548464cc19509abb4edae1e3`  
		Last Modified: Wed, 18 Feb 2026 19:17:50 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7535deb827aeb33b99f184b8ff6e2c228a2732c0f5f9b625013d6f647fd039c0`  
		Last Modified: Wed, 18 Feb 2026 19:17:50 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:180b0d6b0cc522c0ab2b6bb194834f57e9cecc57baf9009116e622ca32092521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2540931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d0acb00d14dfdc09a5e7e74fdadb228e5682bfc51aed4a99051747127bd776`

```dockerfile
```

-	Layers:
	-	`sha256:345af13df4e54f430e47dba31465d8dcf9fc15f3638e5eb5b238b1128832215e`  
		Last Modified: Wed, 18 Feb 2026 19:17:50 GMT  
		Size: 2.5 MB (2519672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6780592c676eefcefd3897139dd682f28d526780d6069e279590c5ee15513ec1`  
		Last Modified: Wed, 18 Feb 2026 19:17:50 GMT  
		Size: 21.3 KB (21259 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:8c397f7743c577e462e4f3e344bd71835b1c67f2e98ae3ee667e50aa3cc9b969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206824192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567a036f5072b00385e8181c9107647806e2be8a8ece6da721286d5c79fac07f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 17:14:47 GMT
ENV container oci
# Tue, 17 Feb 2026 17:14:48 GMT
COPY dir:3a75322911f167c45a527d249b8b7a1bb61960bd0414c69e2c48ff05f3aaaa64 in /      
# Tue, 17 Feb 2026 17:14:48 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 17:14:48 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 17:14:48 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 17:14:48 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 17:14:48 GMT
COPY file:4d5fe83a4c701a100e1eaed18157926865f67ffe30ea0c801e48164ab289c12d in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 17:14:48 GMT
COPY file:4d5fe83a4c701a100e1eaed18157926865f67ffe30ea0c801e48164ab289c12d in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 17:14:48 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T17:14:36Z" "org.opencontainers.image.created"="2026-02-17T17:14:36Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T17:14:36Z
# Wed, 18 Feb 2026 19:22:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 19:22:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 19:22:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Feb 2026 19:22:09 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 18 Feb 2026 19:22:09 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 18 Feb 2026 19:23:17 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Feb 2026 19:23:21 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Feb 2026 19:23:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Feb 2026 19:23:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Feb 2026 19:23:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:722693878ac364b9d2ee6aa4d50e67ce459b9548beed24d0bb6ff115844b6e5d`  
		Last Modified: Tue, 17 Feb 2026 18:09:24 GMT  
		Size: 44.5 MB (44450261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bee69fcb88d423dd51b4ae1e9aa4be9eb53f1df38695a23566fd8e316cd932`  
		Last Modified: Wed, 18 Feb 2026 19:22:54 GMT  
		Size: 32.9 MB (32872323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce59c34c07a8766a618172f6dd611193a40eb6c4463de0078f2b8119289e0bb`  
		Last Modified: Wed, 18 Feb 2026 19:24:11 GMT  
		Size: 129.5 MB (129499187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0dc83a954d6756dbd9dfd348d3582459aaecb6ddce66c38cf9b453d8d9fce3`  
		Last Modified: Wed, 18 Feb 2026 19:24:03 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bff1c27a8f727b8539adbdb8cce36ecb8b1ffdae19c8f2393f95aa68abb1d86`  
		Last Modified: Wed, 18 Feb 2026 19:23:40 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:05ce950019cffd6c73eb6ce6ba00535d4a751e648b40a9ae772b7b9d6ad7a537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443eaf77cbf6aed5e3efc675b0477144b6df6dd80776753f32e20c0ec984bfa2`

```dockerfile
```

-	Layers:
	-	`sha256:0ba01341ab124dc7e089b3a056bca71a984e73fe867578c8cdb8962f2b04d77a`  
		Last Modified: Wed, 18 Feb 2026 19:24:03 GMT  
		Size: 2.5 MB (2517161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea16dde7cb1fba9b19073d167487b5b8d275ca12ea6713891430102dae5f4663`  
		Last Modified: Wed, 18 Feb 2026 19:24:03 GMT  
		Size: 21.2 KB (21180 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:445d45688218143813834f67aadf4901c1d2d7a3f6ca8ae475b83311859f5188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191519197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c675cfcd87a190388a4c3b6a45c11b6d41203d639e0e904c296f328cac37b9a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 17 Feb 2026 17:28:18 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 17:28:18 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 17:28:18 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 17:28:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 17:28:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 17:28:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 17:28:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 17:28:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 17:28:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 17:28:18 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 17:28:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 17:28:19 GMT
ENV container oci
# Tue, 17 Feb 2026 17:28:19 GMT
COPY dir:e19a9544af6f4f767332c726437518ba329f6c0cb823e6626d8f737e7b4e03af in /      
# Tue, 17 Feb 2026 17:28:19 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 17:28:19 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 17:28:19 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 17:28:19 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 17:28:19 GMT
COPY file:92884c81bda51cff7047f88f0f2de2d2a1934fb3649e59ef22ffd9a5bdac51d3 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 17:28:19 GMT
COPY file:92884c81bda51cff7047f88f0f2de2d2a1934fb3649e59ef22ffd9a5bdac51d3 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 17:28:20 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T17:28:07Z" "org.opencontainers.image.created"="2026-02-17T17:28:07Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T17:28:07Z
# Wed, 18 Feb 2026 19:14:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 19:14:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 19:14:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Feb 2026 19:14:16 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 18 Feb 2026 19:14:16 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 18 Feb 2026 19:14:26 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Feb 2026 19:14:29 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Feb 2026 19:14:30 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Feb 2026 19:14:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Feb 2026 19:14:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e49899ec689390291d0a567190cfeebd147dc3fea51e0dc3988e02aceb092cd0`  
		Last Modified: Tue, 17 Feb 2026 18:09:17 GMT  
		Size: 38.1 MB (38128755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6275bec23a78617f82020061d15e038c0736fe93ec68f4cfc5005fd48d8b4766`  
		Last Modified: Wed, 18 Feb 2026 19:15:14 GMT  
		Size: 30.4 MB (30415341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b9e5a4cbd5a3f87437905c779e60dbd95f1e2185a577827770842c245ab890`  
		Last Modified: Wed, 18 Feb 2026 19:15:17 GMT  
		Size: 123.0 MB (122972680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecacc48ce9eb3ac0c1406418b4743e133983efcbfc709df511020cdbc2b255c8`  
		Last Modified: Wed, 18 Feb 2026 19:15:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a294e380ea6e30a14e9aadb19db5612a7719c7b0afd56d874c00cff75fb8bf`  
		Last Modified: Wed, 18 Feb 2026 19:15:13 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:24e1fbba7ceae6a756e5f460012ac2986a381fde02b9c01d0a3bd88a7a92c072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd74aa567a2b43d1a059514f75ba32047fb2c7e53e7f6ca41b68774fe86ad57`

```dockerfile
```

-	Layers:
	-	`sha256:55b7073916692d974c8dac57adff087cca6f0ab248179611d62fb727556d1377`  
		Last Modified: Wed, 18 Feb 2026 19:15:12 GMT  
		Size: 2.5 MB (2507080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2646e9d14d0063a4428ed77e3db91ffc84645d6329007c6b167d1314aac537c`  
		Last Modified: Wed, 18 Feb 2026 19:15:11 GMT  
		Size: 21.1 KB (21144 bytes)  
		MIME: application/vnd.in-toto+json
