## `eclipse-temurin:17-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:d74eb2c539dd21fd14fac6c2e3f4159c5a3185d4ff37f481ee3c1f4234b5fa3c
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
$ docker pull eclipse-temurin@sha256:074b5039a328f7ff049ca579625eee404f435d0e49e8857ebcd741eabc3f5e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115938744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275be8ea54015583e7a08e1f7e8d644beb9b2338fbeab117200f4573ed15f690`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 26 May 2026 15:32:20 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:32:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:32:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:32:21 GMT
ENV container oci
# Tue, 26 May 2026 15:32:22 GMT
COPY dir:bcf46f8211a223ea361ec9cb0b5d7567aaf9ce54beddfddade034948e142ca6d in /      
# Tue, 26 May 2026 15:32:22 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:32:22 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:32:22 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:32:02Z" "org.opencontainers.image.created"="2026-05-26T15:32:02Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:32:02Z
# Tue, 26 May 2026 23:10:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:10:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:10:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:10:37 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:10:37 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 26 May 2026 23:10:40 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 26 May 2026 23:10:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:10:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:10:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:1a36cba5a1d845cee5e57e6f2dc9f828b4cc53403e207333e2220cd426126f13`  
		Last Modified: Tue, 26 May 2026 18:02:56 GMT  
		Size: 40.7 MB (40708696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a3ba0e9094c911f6745906dd135c24746cf4c0363dcfe4caf8c2edb1accce3`  
		Last Modified: Tue, 26 May 2026 23:10:53 GMT  
		Size: 27.7 MB (27664123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf129a2a37eb50e499e8d0934e6ab79775d2933b195232415d729cf9009d19e8`  
		Last Modified: Tue, 26 May 2026 23:10:54 GMT  
		Size: 47.6 MB (47563508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0233a32ec6778b7ec08c3f13bec4cb3a0c9dabe39ec020b3bf6851d7d654d2`  
		Last Modified: Tue, 26 May 2026 23:10:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8dd215029caa86c372e33202e4b3e3d3d65fcda5caabe362c96e73a4e9828e`  
		Last Modified: Tue, 26 May 2026 23:10:52 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6c187a5bdeaf006693f72aea23981518b6c947e73282c3733af413f2c13c9364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2430819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea93ef5db624179953ee53750e79d818ec339366e16853a93895cc1abfac010`

```dockerfile
```

-	Layers:
	-	`sha256:c4d3f7078a5538553fc8843abc9ea8ca49d0e94098e73537f9de957f5aff9c1c`  
		Last Modified: Tue, 26 May 2026 23:10:52 GMT  
		Size: 2.4 MB (2410609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdf25924da5d92f22a88a20b79f87b845765faa17059cb4509f4068d06129bec`  
		Last Modified: Tue, 26 May 2026 23:10:52 GMT  
		Size: 20.2 KB (20210 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:bffca44ce1514c1ef2bbb6a0f482016828ced458906ee06ff46e64ec61d866d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (113990954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0372b246c7db6217de45519a067904c8b9b8f16a3935e2d222e8bc9ed757f1c2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 26 May 2026 15:34:04 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:34:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:34:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:34:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:34:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:34:05 GMT
ENV container oci
# Tue, 26 May 2026 15:34:06 GMT
COPY dir:9311212a31ee4f8d868b9de6ebae2a0a4e5d17aa2e21f16141915c8746951a19 in /      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:34:06 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:33:51Z" "org.opencontainers.image.created"="2026-05-26T15:33:51Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:33:51Z
# Tue, 26 May 2026 23:09:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:09:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:09:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:09:24 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:09:24 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 26 May 2026 23:09:55 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 26 May 2026 23:09:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:09:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:09:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:96e18ab71592420b36f7601002b695ecc23bf6b95f86193c23b2753544d31b8a`  
		Last Modified: Tue, 26 May 2026 18:00:10 GMT  
		Size: 38.8 MB (38840156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5508350f291e5f1f937fb0610ad086d4ac4585d1eac3624a15ca5541c7e14aca`  
		Last Modified: Tue, 26 May 2026 23:09:44 GMT  
		Size: 28.1 MB (28098710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1271f2d89a6cda15c7f6b7e35f0c9e9a92ead3d6b93df9187c2096116a6b7fc9`  
		Last Modified: Tue, 26 May 2026 23:10:08 GMT  
		Size: 47.0 MB (47049670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b232a2d6b44b6ccaa71e2e6ead6bc28ea8db326441dcccb20d69864a96df77c`  
		Last Modified: Tue, 26 May 2026 23:10:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90cd08cb57a8e69763eee03d5a2971f5f65c4d63326f4d60e72656a8d2011fae`  
		Last Modified: Tue, 26 May 2026 23:10:06 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4e3091d4254f287580a8b342d91320c55931ec0759c5825b449c8c5c6ad3c717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2430281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d5e898c46aeaaf8cbbef8e82786e74acbc4f006a17ff231de1b75edde4bee7`

```dockerfile
```

-	Layers:
	-	`sha256:8cb888f715e90a3fddb1136e3bb3c507edab60039ca088c394de41534c6054ea`  
		Last Modified: Tue, 26 May 2026 23:10:06 GMT  
		Size: 2.4 MB (2409967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93ed234f0604a113dca6683488b03fe456ee5e600296976d4e450936a7c34c00`  
		Last Modified: Tue, 26 May 2026 23:10:06 GMT  
		Size: 20.3 KB (20314 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:5533f25e9843ccc44955c502b32875a9eb6156e2ed308cce2639f44fc02dece7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122767601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d607c8ce4b32315897b675f68dcc1d33f8da76d50c3836da3ee065ec17b025`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 26 May 2026 15:33:29 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:33:29 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:33:29 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:33:29 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:33:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:33:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:33:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:33:29 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:33:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:33:29 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:33:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:33:29 GMT
ENV container oci
# Tue, 26 May 2026 15:33:30 GMT
COPY dir:5e813a184cbab7cbf1fee0022ee8e55aa80387ef4835bad3a6804243f83209e4 in /      
# Tue, 26 May 2026 15:33:30 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:33:30 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:33:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:33:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:33:30 GMT
COPY file:6f186cff34757f21b3d3a096028791fe755881607c0652e8eef706352323f06b in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:33:30 GMT
COPY file:6f186cff34757f21b3d3a096028791fe755881607c0652e8eef706352323f06b in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:33:30 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:33:18Z" "org.opencontainers.image.created"="2026-05-26T15:33:18Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:33:18Z
# Tue, 26 May 2026 23:08:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:08:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:08:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:08:21 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:08:21 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 26 May 2026 23:13:04 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 26 May 2026 23:13:07 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:13:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:13:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f263dc8aecd57a446632c1e9df773e64bf709523e5ba6125cf199c6099e78689`  
		Last Modified: Tue, 26 May 2026 18:14:02 GMT  
		Size: 45.2 MB (45170860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb610a3d89ec570af77bbbb3ef8a428aab0ae8be44919b92e068743a6d993703`  
		Last Modified: Tue, 26 May 2026 23:08:56 GMT  
		Size: 30.1 MB (30094662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c652fb8fb287984ae633685f431e4521107b10843105ae8925292681af6787`  
		Last Modified: Tue, 26 May 2026 23:13:34 GMT  
		Size: 47.5 MB (47499663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db552d0295838e17d11300588a849ba84961cd4921e372f2ee1a210e3e5b6f1`  
		Last Modified: Tue, 26 May 2026 23:13:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d045a9fd7e186457685c276bc28fa31b5d397d546de1a4c9db999f08c920ba`  
		Last Modified: Tue, 26 May 2026 23:13:33 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4c627ed3d989382ff2814908a5970c2509388095bbad96063b2f63b9283bd9e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2430891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6e2c178587d3fdd6c3089296f7c3e7903285df12256f088f23ca48590ddd14`

```dockerfile
```

-	Layers:
	-	`sha256:8e354ea200c56fc3a928f7a5b6255b928a60510ee0b222bd5435e57bc8600533`  
		Last Modified: Tue, 26 May 2026 23:13:32 GMT  
		Size: 2.4 MB (2410652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ee4c2a55dcc5de1c969a5a3777552005d88901439229e731efa95646d7b80e`  
		Last Modified: Tue, 26 May 2026 23:13:32 GMT  
		Size: 20.2 KB (20239 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:9d1905362fd7317dd2c78d615f9c17bbddbb5d39d26e31048f3db49e9b7d9bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (111021411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2c3d213a1f2dfcff12a784b527fd51be3cab220568c43d2f1ac5a1c01b6da7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 26 May 2026 15:50:54 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:50:54 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:50:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:50:54 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:50:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:50:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:50:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:50:54 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:50:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:50:54 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:50:54 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:50:54 GMT
ENV container oci
# Tue, 26 May 2026 15:50:55 GMT
COPY dir:a00d53b24bbcf9097132390b191c936ff622d9b440a8f192754b910ebb84f566 in /      
# Tue, 26 May 2026 15:50:55 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:50:55 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:50:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:50:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:50:55 GMT
COPY file:48547272f4e6f96db66fd643aed1cfc9d3d7b7e696830a7dd166e3dd1a7a8aa4 in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:50:55 GMT
COPY file:48547272f4e6f96db66fd643aed1cfc9d3d7b7e696830a7dd166e3dd1a7a8aa4 in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:50:55 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:50:26Z" "org.opencontainers.image.created"="2026-05-26T15:50:26Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:50:26Z
# Tue, 26 May 2026 23:08:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:08:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:08:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:08:29 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:08:29 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 26 May 2026 23:09:23 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 26 May 2026 23:09:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:09:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:09:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6ba40b0a7d8c65538d55968f5725eca287bda3024401d2f12b225797f497e32b`  
		Last Modified: Tue, 26 May 2026 18:13:55 GMT  
		Size: 38.8 MB (38794791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f29099d61c5bb7dc3b8aed16cf293ce24315f0865f0bdb77fb98847c1b016fe`  
		Last Modified: Tue, 26 May 2026 23:08:51 GMT  
		Size: 27.7 MB (27693194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55919386959873a5c6cf5a04120b2c73b0e0a74cbc21b081082703d0f4ee9937`  
		Last Modified: Tue, 26 May 2026 23:09:43 GMT  
		Size: 44.5 MB (44531009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0405410284bbd6670ecac4a20c81eb583fa0beddaba434b87e8f6fb694066478`  
		Last Modified: Tue, 26 May 2026 23:09:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d241f3aed97546a0be33e0bc182dae6d2e79db472a1b7c5af138f87f500dc6c`  
		Last Modified: Tue, 26 May 2026 23:09:41 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:70114e1ef58dbbac465de2240790ce37203085c63c4307997504d83957f8d4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2bef8c63c5a4f12a0341ee73f3c27ea37037a2c8379d58ff41f0c91d51c0c29`

```dockerfile
```

-	Layers:
	-	`sha256:522bf7f6eeac7a07b16a60eab5c0b45b33689944cf7b27875b8ab2460e56286d`  
		Last Modified: Tue, 26 May 2026 23:09:41 GMT  
		Size: 2.4 MB (2402401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4435a2b01a4f23329a74f4f72256595e2222a5b0cbc5c2bf0306e77324cc4bcd`  
		Last Modified: Tue, 26 May 2026 23:09:41 GMT  
		Size: 20.2 KB (20210 bytes)  
		MIME: application/vnd.in-toto+json
