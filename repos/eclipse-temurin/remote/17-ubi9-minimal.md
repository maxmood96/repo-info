## `eclipse-temurin:17-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:c8571b21ff4de30525a98dafcced6c26f66595e5c624f660f48c714552c9fa34
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

### `eclipse-temurin:17-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:a94d05f87a6f6345d8f33319b7bef773e02628d781198441723ccc8276504b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.3 MB (214266364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca5af1186d728eb76c53bf65908206427ea525c4668d9639e8368f26f82fb6f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 02 Jun 2026 05:45:15 GMT
ENV container oci
# Tue, 02 Jun 2026 05:45:16 GMT
COPY dir:089626db9f0e556d2460ea9b02a44cc63366766c2d8912a1fd05fdd542cbb8e4 in /      
# Tue, 02 Jun 2026 05:45:16 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 05:45:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:aae7c733edba3a2c94cde549acbeb2025333f3fac20483f5ec988a263ea63dc6 in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:aae7c733edba3a2c94cde549acbeb2025333f3fac20483f5ec988a263ea63dc6 in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:45:17 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "org.opencontainers.image.revision"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "build-date"="2026-06-02T05:44:58Z" "org.opencontainers.image.created"="2026-06-02T05:44:58Z" "release"="1780378819"org.opencontainers.image.revision=842dd1c603c36c8d242d5ec075adccffb3bfea5c,org.opencontainers.image.created=2026-06-02T05:44:58Z
# Tue, 02 Jun 2026 22:45:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 22:45:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:45:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 22:45:19 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:45:19 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 02 Jun 2026 22:45:26 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 02 Jun 2026 22:45:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:45:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:45:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 22:45:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dd148063a98f38d63a03cea2357d237d418889b91f204f507c033c944e443f45`  
		Last Modified: Tue, 02 Jun 2026 07:03:29 GMT  
		Size: 40.7 MB (40687042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfce26a85b43f3a6f6eafb4ecc17a960fa2b5d423953c04d3fb776eb87b6ccf`  
		Last Modified: Tue, 02 Jun 2026 22:45:44 GMT  
		Size: 27.7 MB (27661482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6de81c11ca6a33674bb04242871e8d88c08a0840bb085e0a5522a261837cce`  
		Last Modified: Tue, 02 Jun 2026 22:45:47 GMT  
		Size: 145.9 MB (145915421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02e6b808069140bdf920ab8f8f9fcf0743beb9217589ba2f1f500eaf107f348`  
		Last Modified: Tue, 02 Jun 2026 22:45:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf76ef5593b8e2bfab395a0693085d99f26d514e51e01c5e04d749318a0ac5c`  
		Last Modified: Tue, 02 Jun 2026 22:45:31 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3467af52f9915d8802fcb0518251c9003d9e84ce6b4ac2ad18493061a8685b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2516258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6dc8431729e9d006bf0a9ea9a05a835e8e4fb73c66534135e752bb1ef43ec7`

```dockerfile
```

-	Layers:
	-	`sha256:58d9e810eb1f164f410e3135eed54ee631e6d6c32400046b4e455763b4701348`  
		Last Modified: Tue, 02 Jun 2026 22:45:44 GMT  
		Size: 2.5 MB (2495090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c591ca580847c322ab520a99597f1b8fa7f1d4e307b85d8f5246f679c3bf00c`  
		Last Modified: Tue, 02 Jun 2026 22:45:43 GMT  
		Size: 21.2 KB (21168 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:4bbe335d00bcca47f8c183b55a37f3fef06318d024f9329f8720757839cf1698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.7 MB (211697699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114a1beb978379591e899d190b633b1175952b0465e34130e671c267194b54c4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 02 Jun 2026 05:43:50 GMT
ENV container oci
# Tue, 02 Jun 2026 05:43:51 GMT
COPY dir:45e3b0db7c7574b63ad7ec3e8aa88c1c154d382f5d855d74a5a8b46ed379a850 in /      
# Tue, 02 Jun 2026 05:43:51 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 05:43:51 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 05:43:51 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 05:43:51 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 05:43:52 GMT
COPY file:7aad34f99b458abb22df8550ad1aaf3928f914f8d425e14ac9708e9a77642cae in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:43:52 GMT
COPY file:7aad34f99b458abb22df8550ad1aaf3928f914f8d425e14ac9708e9a77642cae in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:43:52 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "org.opencontainers.image.revision"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "build-date"="2026-06-02T05:43:37Z" "org.opencontainers.image.created"="2026-06-02T05:43:37Z" "release"="1780378819"org.opencontainers.image.revision=842dd1c603c36c8d242d5ec075adccffb3bfea5c,org.opencontainers.image.created=2026-06-02T05:43:37Z
# Tue, 02 Jun 2026 22:44:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 22:44:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:44:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 22:44:41 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:44:41 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 02 Jun 2026 22:44:48 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 02 Jun 2026 22:44:49 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:44:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:44:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 22:44:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7db43598c7e47cf895f880f92e3cee9c07787091c97802ea3f2bea8fa4848040`  
		Last Modified: Tue, 02 Jun 2026 07:03:29 GMT  
		Size: 38.9 MB (38863161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f846948eeab07fb22367851ac3b0a0659c83ffd50bd725186c9c583395c2b952`  
		Last Modified: Tue, 02 Jun 2026 22:45:08 GMT  
		Size: 28.1 MB (28097335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3df423d0bb9c2b8d177ff47b1d5883621a825f60c33a448b0f77c19d5fd01bd`  
		Last Modified: Tue, 02 Jun 2026 22:45:10 GMT  
		Size: 144.7 MB (144734785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2b9f5186e0e9f083307ecc6c4a17d5d5cf7942c21c8301440e303ba7124d64`  
		Last Modified: Tue, 02 Jun 2026 22:45:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b290a672da5f64032d057914e5a3e1e750b3c229ce3f6ea44039b9489c0a6b92`  
		Last Modified: Tue, 02 Jun 2026 22:45:06 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5c2b0a3e418428c0200609390368e49adeed25bd474543880d3a0fdaec7812e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2515743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af28986336a1cdbafbc96828dd2cfc89d31c83d76000ebd27614d9f35ecbed0`

```dockerfile
```

-	Layers:
	-	`sha256:3517a0875186728d93f7df5eae1f380770bce7c3ed96dc0477b879ea6181e925`  
		Last Modified: Tue, 02 Jun 2026 22:45:06 GMT  
		Size: 2.5 MB (2494460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb70e985a6723e602930dd40ee76154909806d1addfb0629e9d9e5ec24baca0f`  
		Last Modified: Tue, 02 Jun 2026 22:45:06 GMT  
		Size: 21.3 KB (21283 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:382bec3949f57f8f10cd50d44987df6667e5f5f1fd9d6b3194782f075b285ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (221031338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f365b6d73abf8e851b0d01e78ea4ca06f117a68efa8febff84be2ec5f5261e5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 02 Jun 2026 05:43:57 GMT
ENV container oci
# Tue, 02 Jun 2026 05:43:58 GMT
COPY dir:e2b77dc18737d07e8e5246d22c774c81a15fd49086dce884c4ad7e020854e7f1 in /      
# Tue, 02 Jun 2026 05:43:58 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 05:43:58 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 05:43:58 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 05:43:58 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 05:43:58 GMT
COPY file:51b0adf8b5a4c3a24ace6c346ea6678803925c6cc30d08b64751f980b4528cc2 in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:43:58 GMT
COPY file:51b0adf8b5a4c3a24ace6c346ea6678803925c6cc30d08b64751f980b4528cc2 in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:43:58 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "org.opencontainers.image.revision"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "build-date"="2026-06-02T05:43:46Z" "org.opencontainers.image.created"="2026-06-02T05:43:46Z" "release"="1780378819"org.opencontainers.image.revision=842dd1c603c36c8d242d5ec075adccffb3bfea5c,org.opencontainers.image.created=2026-06-02T05:43:46Z
# Tue, 02 Jun 2026 22:45:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 22:45:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:45:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 22:45:42 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:45:42 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 02 Jun 2026 22:49:55 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 02 Jun 2026 22:50:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:50:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:50:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 22:50:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5ff77d7ff78e7752137c3eba042a793ae2b415158af730c2f66c23814842a63f`  
		Last Modified: Tue, 02 Jun 2026 12:13:00 GMT  
		Size: 45.1 MB (45149918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fe7aeed3e9a0e4db7600177f2e2ad0b5eafa7a4390b1e052377528fb46b8a3`  
		Last Modified: Tue, 02 Jun 2026 22:46:32 GMT  
		Size: 30.1 MB (30090253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f859b23d825612cba6a804a80f2236fe23890454ed7092a8be9a26be91feef9`  
		Last Modified: Tue, 02 Jun 2026 22:51:35 GMT  
		Size: 145.8 MB (145788746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9661b1eaba4957c3c5f99710a2e24e76d9379bf15878df4e6727eb3e8a9b7c0`  
		Last Modified: Tue, 02 Jun 2026 22:51:31 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c720691f5667c2ec2e86d8f4b6e7299210b63047d6f8c41ac48224a27635c80`  
		Last Modified: Tue, 02 Jun 2026 22:51:31 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:100c4935d13c81f23b53131a29d2e05496d55a5defa4ed918ac3d92d1de8a69e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2514424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13dce6fe4deab5d7c7cb6b2c8953f71d11f159c81a5719de8da574cb7473d5c6`

```dockerfile
```

-	Layers:
	-	`sha256:8e04f4ce74bb114ace04130f04e5ff83b50d50c140b49ea82458bdbb3173b2c1`  
		Last Modified: Tue, 02 Jun 2026 22:51:31 GMT  
		Size: 2.5 MB (2493220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4115975b82a2f4469d95d5f039d608e581964a1fb2f133397acbd6a116709268`  
		Last Modified: Tue, 02 Jun 2026 22:51:31 GMT  
		Size: 21.2 KB (21204 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:cfe71925bdfae9839bc447c279fa37f24df398bc44a3a462f4cb071847252fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.4 MB (202394239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a8fd99732d43766312556d0705853a884118a08b167b2fa68ef54ab4873f6a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jun 2026 05:58:20 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 05:58:20 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 05:58:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 05:58:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 02 Jun 2026 05:58:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 05:58:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 02 Jun 2026 05:58:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:58:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:58:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 02 Jun 2026 05:58:20 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 05:58:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 02 Jun 2026 05:58:20 GMT
ENV container oci
# Tue, 02 Jun 2026 05:58:21 GMT
COPY dir:42d16b6fc3799c6e8e18836407138d7a47421712f6e545204e190f0bc9cd0367 in /      
# Tue, 02 Jun 2026 05:58:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 05:58:21 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 05:58:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 05:58:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 05:58:21 GMT
COPY file:4c2ab4fe2bf528858e28a71d4ac6059cf378c99fb19db56c8676a607bbe8fd92 in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:58:21 GMT
COPY file:4c2ab4fe2bf528858e28a71d4ac6059cf378c99fb19db56c8676a607bbe8fd92 in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:58:21 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "org.opencontainers.image.revision"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "build-date"="2026-06-02T05:58:08Z" "org.opencontainers.image.created"="2026-06-02T05:58:08Z" "release"="1780378819"org.opencontainers.image.revision=842dd1c603c36c8d242d5ec075adccffb3bfea5c,org.opencontainers.image.created=2026-06-02T05:58:08Z
# Tue, 02 Jun 2026 22:43:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 22:43:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:43:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 22:43:21 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:43:21 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 02 Jun 2026 22:44:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 02 Jun 2026 22:44:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:44:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:44:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 22:44:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ba9f2e747b70b6ed487f72e44a2125691e7495f0533ca3565e966694a38ee758`  
		Last Modified: Tue, 02 Jun 2026 12:12:51 GMT  
		Size: 38.8 MB (38784938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb773a8972861f38bb22fa221bbbf221dfd8c3f3058891f97c7d0a4b0a042c99`  
		Last Modified: Tue, 02 Jun 2026 22:43:57 GMT  
		Size: 27.7 MB (27694593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbf28470b3d6cd10c1a7438caf0bdcc2489b8a1598b0b1defc30a4657d97011`  
		Last Modified: Tue, 02 Jun 2026 22:44:56 GMT  
		Size: 135.9 MB (135912289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9372d9eb64b72e8268d1dd39ef4a216c5875ba70ab82c584a16ddecc323d9a`  
		Last Modified: Tue, 02 Jun 2026 22:44:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573ce693e07f4591d442b1c8ca47d2c0cdd92b1cb5ff3738d5d9ff58dc65b4ec`  
		Last Modified: Tue, 02 Jun 2026 22:44:52 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ea95944101be155158434346d0deba50089a22d5f6ae5ea49da1acc4a6a09964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9151a95c1e3c34313f24c3aca39b86f13bec5a9d37c9c101943cb7f48a9bbc5`

```dockerfile
```

-	Layers:
	-	`sha256:9b0fb78aa124a65ae2d75efd2a87968b6a2c7c4e80d8e21ac04ee457ede8341a`  
		Last Modified: Tue, 02 Jun 2026 22:44:53 GMT  
		Size: 2.5 MB (2482482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99bf5d76bba017699c3d035b6850700b04bfe600bb712b0b135ef34e2cab8e10`  
		Last Modified: Tue, 02 Jun 2026 22:44:53 GMT  
		Size: 21.2 KB (21168 bytes)  
		MIME: application/vnd.in-toto+json
