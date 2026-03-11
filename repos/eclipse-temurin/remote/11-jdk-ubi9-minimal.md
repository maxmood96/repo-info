## `eclipse-temurin:11-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:346ead50f1209917c274717f682b8cfb4e514bbdbf6cff1564bd9484f099c5ad
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
$ docker pull eclipse-temurin@sha256:daad0e93d118aac3f17394ec515cb04a1227e88b8031bb4c8277ad03212b9988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 MB (212650953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a028e5cfb8ecc8d42ff823aea67e06b6377f391322ce6a24cadd3e63acfac3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.openshift.expose-services=""
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 11 Mar 2026 04:51:30 GMT
ENV container oci
# Wed, 11 Mar 2026 04:51:31 GMT
COPY dir:c1ba4c335e7831ddebf5732b67e3739a636a3d3dbf6b4d4089ed8f31a1bfbfd1 in /      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 11 Mar 2026 04:51:31 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:53f3c4e4ec21f021024505adc7a7710e18079e2a86f12f898f971cadc64b7478 in /usr/share/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:53f3c4e4ec21f021024505adc7a7710e18079e2a86f12f898f971cadc64b7478 in /root/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:51:32 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ddf3e9d218968613397a7b4df7547f25ad755449" "org.opencontainers.image.revision"="ddf3e9d218968613397a7b4df7547f25ad755449" "build-date"="2026-03-11T04:51:18Z" "org.opencontainers.image.created"="2026-03-11T04:51:18Z" "release"="1773204619"org.opencontainers.image.revision=ddf3e9d218968613397a7b4df7547f25ad755449,org.opencontainers.image.created=2026-03-11T04:51:18Z
# Wed, 11 Mar 2026 18:34:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Mar 2026 18:34:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:34:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 11 Mar 2026 18:34:31 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 11 Mar 2026 18:34:31 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 11 Mar 2026 18:34:38 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 11 Mar 2026 18:34:39 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 11 Mar 2026 18:34:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 11 Mar 2026 18:34:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Mar 2026 18:34:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1174ed37633caad5219e59c67f05fe4e54bd728c7a8cfd4ea1df16de15de2f76`  
		Last Modified: Wed, 11 Mar 2026 06:07:51 GMT  
		Size: 40.0 MB (39990896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7673fab2cfa0dfe64b95de5f1d9081e959fbb329e594754b4454e409a09b3a9`  
		Last Modified: Wed, 11 Mar 2026 18:34:55 GMT  
		Size: 30.4 MB (30394302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcd9e65dc101fa9744412cb842d5204211696d38f15d185514020f32ed43b94`  
		Last Modified: Wed, 11 Mar 2026 18:34:57 GMT  
		Size: 142.3 MB (142263334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d141c56564dbef3d178d633cfa851d7dea4c9615226fc36d147857b22cebe6a`  
		Last Modified: Wed, 11 Mar 2026 18:34:53 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02ab74d16182428cef6e3895b5078c121226777f6d875b0d7fc483f39fe0834`  
		Last Modified: Wed, 11 Mar 2026 18:34:39 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:794e78c3e27df459d27bcef97e360b1ba4bc864a8f5772ac80fc321e7e6c1964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2540834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602c33fd0cfb55b7a390fb1f05b95c06570436b19dd2eace64d6a3a0dbee243f`

```dockerfile
```

-	Layers:
	-	`sha256:3bd3c24b016acf3ad7cba7dc895c6b3277f4b53fc213922c272ca107b6d30f44`  
		Last Modified: Wed, 11 Mar 2026 18:34:53 GMT  
		Size: 2.5 MB (2519690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:369b0a38e72f27c797b4bfac41eb2799aee449a7192c0bbde36bc25ac34e3d58`  
		Last Modified: Wed, 11 Mar 2026 18:34:53 GMT  
		Size: 21.1 KB (21144 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:d016f957f6fd4aab630d9f3bd79685acb913ad2b0dfcfbd7ce9166a5a30a200c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 MB (207992417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def9b668d426a808746b4ec0efd4bb5b3e8afeebce5bf719be51014aa76c034c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.openshift.expose-services=""
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 11 Mar 2026 04:53:19 GMT
ENV container oci
# Wed, 11 Mar 2026 04:53:20 GMT
COPY dir:7796b64b73526e8dad6fca20071cfe57334a57323fbbb1f9256c4ffffa8b27db in /      
# Wed, 11 Mar 2026 04:53:20 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 11 Mar 2026 04:53:20 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 04:53:20 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 11 Mar 2026 04:53:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 11 Mar 2026 04:53:21 GMT
COPY file:186c4202737062dc84f1db98b633710a412a23c003ba73ff6ae51d727aea1cd8 in /usr/share/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:53:21 GMT
COPY file:186c4202737062dc84f1db98b633710a412a23c003ba73ff6ae51d727aea1cd8 in /root/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:53:21 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ddf3e9d218968613397a7b4df7547f25ad755449" "org.opencontainers.image.revision"="ddf3e9d218968613397a7b4df7547f25ad755449" "build-date"="2026-03-11T04:53:07Z" "org.opencontainers.image.created"="2026-03-11T04:53:07Z" "release"="1773204619"org.opencontainers.image.revision=ddf3e9d218968613397a7b4df7547f25ad755449,org.opencontainers.image.created=2026-03-11T04:53:07Z
# Wed, 11 Mar 2026 18:34:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Mar 2026 18:34:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:34:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 11 Mar 2026 18:34:02 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 11 Mar 2026 18:34:02 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 11 Mar 2026 18:34:10 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 11 Mar 2026 18:34:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 11 Mar 2026 18:34:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 11 Mar 2026 18:34:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Mar 2026 18:34:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a929c158045efa38dcdfac5809dfda6e7c13c225e0aae109412941b4ed8f3880`  
		Last Modified: Wed, 11 Mar 2026 06:07:49 GMT  
		Size: 38.2 MB (38205467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9ca0ce38c5b6d99dc032cff132a636bfa538e0dc9f7ab0d83e78d3b9157c5d`  
		Last Modified: Wed, 11 Mar 2026 18:34:28 GMT  
		Size: 30.8 MB (30824839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdfb426aeafa15d07c8ddb8ccf52394cf081172a3dc60ec1fc8f5508fbfa437`  
		Last Modified: Wed, 11 Mar 2026 18:34:31 GMT  
		Size: 139.0 MB (138959691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8b7b6764e1ef5bc7700359c09f9bdb4b23b2cb3f74f77b54555980a88eb87b`  
		Last Modified: Wed, 11 Mar 2026 18:34:27 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8d0a0d8cc05f609892a3e539b46d9586a7e77347b81bb765692ac592410f13`  
		Last Modified: Wed, 11 Mar 2026 18:34:27 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a05e03b5d42cbf7479ef6faa69c70f03a9d5d8b837457de081f5ff2db814ee46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2540938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4991a279288d672ede92651f746d95a89b9d85e347cd09fd4e34b43a38013dd`

```dockerfile
```

-	Layers:
	-	`sha256:677e2e993cb1175e0046626a8a603a632ba491ff2bb5206f8193cbbcfce6c96c`  
		Last Modified: Wed, 11 Mar 2026 18:34:27 GMT  
		Size: 2.5 MB (2519678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:462acaaf591e95628025ad17d0a3b52cbc9a22e796186a36df959a443e023531`  
		Last Modified: Wed, 11 Mar 2026 18:34:27 GMT  
		Size: 21.3 KB (21260 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:c677e9641032a20d65ac2b42b52b940b3cecf1013dca541b6b9ef522e32ce176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206830186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752faf181a5374faf2c47e7c800d2f79cc570e299a62e4992ddafc50ae62c8f0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Mar 2026 04:53:58 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 11 Mar 2026 04:53:58 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 11 Mar 2026 04:53:58 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 11 Mar 2026 04:53:58 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 11 Mar 2026 04:53:58 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 11 Mar 2026 04:53:58 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 11 Mar 2026 04:53:58 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:53:58 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:53:58 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 11 Mar 2026 04:53:58 GMT
LABEL io.openshift.expose-services=""
# Wed, 11 Mar 2026 04:53:58 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 11 Mar 2026 04:53:58 GMT
ENV container oci
# Wed, 11 Mar 2026 04:53:59 GMT
COPY dir:c16ffb4ff368c4c4701379220271e573fd98f7ef429754d838e4da274182d3d4 in /      
# Wed, 11 Mar 2026 04:53:59 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 11 Mar 2026 04:53:59 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 04:53:59 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 11 Mar 2026 04:53:59 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 11 Mar 2026 04:53:59 GMT
COPY file:96735fc1d76fbe7cf3c45c3807304493b83949ae77c293c442c668195fa626bc in /usr/share/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:54:00 GMT
COPY file:96735fc1d76fbe7cf3c45c3807304493b83949ae77c293c442c668195fa626bc in /root/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:54:00 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="ddf3e9d218968613397a7b4df7547f25ad755449" "org.opencontainers.image.revision"="ddf3e9d218968613397a7b4df7547f25ad755449" "build-date"="2026-03-11T04:53:48Z" "org.opencontainers.image.created"="2026-03-11T04:53:48Z" "release"="1773204619"org.opencontainers.image.revision=ddf3e9d218968613397a7b4df7547f25ad755449,org.opencontainers.image.created=2026-03-11T04:53:48Z
# Wed, 11 Mar 2026 18:32:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Mar 2026 18:32:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:32:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 11 Mar 2026 18:32:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 11 Mar 2026 18:32:32 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 11 Mar 2026 18:33:40 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 11 Mar 2026 18:33:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 11 Mar 2026 18:33:44 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 11 Mar 2026 18:33:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Mar 2026 18:33:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6121bae13aca039c044ec77f6c0d5c8628a9f1a6cb6026e98347fb488c0c92d1`  
		Last Modified: Wed, 11 Mar 2026 06:10:11 GMT  
		Size: 44.5 MB (44455609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f2be856b2fb1b1a7acb76036ea4b0ce4d3c01cf5e16be0f3a42cebc98397f1`  
		Last Modified: Wed, 11 Mar 2026 18:33:12 GMT  
		Size: 32.9 MB (32872967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f9f8d8fc016bff0313ac1b299de13de2b25b3bfb48a05b48a072d0f6cf43ef`  
		Last Modified: Wed, 11 Mar 2026 18:34:18 GMT  
		Size: 129.5 MB (129499189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779218ff826186ce49967f43c988fa5a9deacdd3d3369e63de05747326a45098`  
		Last Modified: Wed, 11 Mar 2026 18:34:14 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6840329d1d54eff212c742e9a6fcf12f474e4844f9508bf460882a4b97dc7436`  
		Last Modified: Wed, 11 Mar 2026 18:34:04 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:14f7180fba157e4d6287580cb475fb13f017e286c12e2547ecda46dad0c4b3ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e0729dd937ba16f76be0a2efaad57b4a8b5cfb321542315a514198d5e21720`

```dockerfile
```

-	Layers:
	-	`sha256:443e0124f2644ad7c120772f165aacfae8db9e7f5c5af9c10a49293584a0ac48`  
		Last Modified: Wed, 11 Mar 2026 18:34:14 GMT  
		Size: 2.5 MB (2517167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa4190a1401bbcd4c866a1e7dd1604b74b4dee6ac4757c299a00c12f93fe52ba`  
		Last Modified: Wed, 11 Mar 2026 18:34:14 GMT  
		Size: 21.2 KB (21180 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:620fee50432fe916cf57208e084239c9e898cc612288807f3218afe1107ff1df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191505378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db23bb4ba4e0b0bb626b23b57ca306ed0b1d76bdf555b6fd620fdaec9a75325`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Mar 2026 05:09:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 11 Mar 2026 05:09:05 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 11 Mar 2026 05:09:05 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 11 Mar 2026 05:09:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 11 Mar 2026 05:09:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 11 Mar 2026 05:09:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 11 Mar 2026 05:09:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 05:09:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 05:09:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 11 Mar 2026 05:09:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 11 Mar 2026 05:09:06 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 11 Mar 2026 05:09:06 GMT
ENV container oci
# Wed, 11 Mar 2026 05:09:06 GMT
COPY dir:a75f302c58b91e03eb462e96994a66e692bdd08299caf4a5879a83dc26c33c54 in /      
# Wed, 11 Mar 2026 05:09:06 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 11 Mar 2026 05:09:06 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 05:09:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 11 Mar 2026 05:09:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 11 Mar 2026 05:09:06 GMT
COPY file:94e309aff1f0192ed947120fc4293382d72a8b466c1a32dde7e4ec5ddd2c8d6c in /usr/share/buildinfo/labels.json      
# Wed, 11 Mar 2026 05:09:06 GMT
COPY file:94e309aff1f0192ed947120fc4293382d72a8b466c1a32dde7e4ec5ddd2c8d6c in /root/buildinfo/labels.json      
# Wed, 11 Mar 2026 05:09:07 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="ddf3e9d218968613397a7b4df7547f25ad755449" "org.opencontainers.image.revision"="ddf3e9d218968613397a7b4df7547f25ad755449" "build-date"="2026-03-11T05:08:54Z" "org.opencontainers.image.created"="2026-03-11T05:08:54Z" "release"="1773204619"org.opencontainers.image.revision=ddf3e9d218968613397a7b4df7547f25ad755449,org.opencontainers.image.created=2026-03-11T05:08:54Z
# Wed, 11 Mar 2026 18:27:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Mar 2026 18:27:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:27:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 11 Mar 2026 18:27:47 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 11 Mar 2026 18:27:47 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 11 Mar 2026 18:27:53 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 11 Mar 2026 18:27:55 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 11 Mar 2026 18:27:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 11 Mar 2026 18:27:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Mar 2026 18:27:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8b6042692ebd14654705cc63a2e114754df79af319b19ae7d1c0200f6929153c`  
		Last Modified: Wed, 11 Mar 2026 06:10:02 GMT  
		Size: 38.1 MB (38114066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fe0d6bb88471f9570c60b3a088e32e3e4a3a804dab653d21daf59b47acbf6b`  
		Last Modified: Wed, 11 Mar 2026 18:28:13 GMT  
		Size: 30.4 MB (30416178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9344b4b7c28079b8fa670c88b8cc12368cad2a110d791490712066640ce26d`  
		Last Modified: Wed, 11 Mar 2026 18:28:19 GMT  
		Size: 123.0 MB (122972716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0312364fdc3c48aa7a60f583995e8ceef2f226019449fb33f45f4025fbe593ee`  
		Last Modified: Wed, 11 Mar 2026 18:28:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67bb026db48f508dbc259baaf2216a0382cf469fcb872c19bfac422d55151c8`  
		Last Modified: Wed, 11 Mar 2026 18:28:16 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:809099f9de4dcbfc20bcef3937ad3d57d85fed3792e7b3654da18087d6c3609d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2595254102c7c1aa9ef66e5bc2410f680a65e037e38055fde8c134b8b1150e`

```dockerfile
```

-	Layers:
	-	`sha256:c675e8bae7392005e6c877be4d013d69d04abd05ed5eb92b21050cec76a07ca7`  
		Last Modified: Wed, 11 Mar 2026 18:28:16 GMT  
		Size: 2.5 MB (2507086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:890cf1a602fe6e529129afc5da5071141c81e0490259744977ebb9e1289dd33b`  
		Last Modified: Wed, 11 Mar 2026 18:28:16 GMT  
		Size: 21.1 KB (21144 bytes)  
		MIME: application/vnd.in-toto+json
