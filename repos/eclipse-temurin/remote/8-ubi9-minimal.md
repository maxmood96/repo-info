## `eclipse-temurin:8-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:18dcc6817f8a27c2c49c39cfde2a527f39ec6882994965da70b171c6ee5d5eac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:b804c316ec75858b0e6c3e954371602a3af818130a7dfddd9e6e3384390f6d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123546261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2e3eac94911fe502648561f8d7c58a6fcfbd510952a61867be139c377a8707`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:14:14 GMT
ENV container oci
# Mon, 15 Jun 2026 04:14:14 GMT
COPY dir:37b1ea11a739ebaa3fdc4f74d963b56e5e50e2e4b048d008948978527dfc6171 in /      
# Mon, 15 Jun 2026 04:14:14 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:14:14 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:14:02Z" "org.opencontainers.image.created"="2026-06-15T04:14:02Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:14:02Z
# Mon, 15 Jun 2026 23:13:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 15 Jun 2026 23:13:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:13:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 15 Jun 2026 23:13:35 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:13:35 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Mon, 15 Jun 2026 23:13:39 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 15 Jun 2026 23:13:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 15 Jun 2026 23:13:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:13:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:48538841ca5147d36a25e82713e079413d3c2a137f5ea5df68a1c5da1e3a677e`  
		Last Modified: Mon, 15 Jun 2026 04:45:40 GMT  
		Size: 40.7 MB (40680192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0516ea62bcc474893cc4708b7db39cc36eeb6600eb7da9dee69445cfdd92dd07`  
		Last Modified: Mon, 15 Jun 2026 23:13:54 GMT  
		Size: 27.7 MB (27664316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759208949e559ab29198eec8e58e10574341824fb74721b576f18bd8e2f39aa6`  
		Last Modified: Mon, 15 Jun 2026 23:13:55 GMT  
		Size: 55.2 MB (55199134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8649f12df159c0f2b1cd6f4351fe63be7fdef68dfd9297b508ba91d77215d42`  
		Last Modified: Mon, 15 Jun 2026 23:13:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c1f09f3da9c13e7030c064b53ba094bceab519479fbbb9bc267aacefc761a5`  
		Last Modified: Mon, 15 Jun 2026 23:13:54 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:735a0b1fde03d06b1542e76cf765b8c5f6467f93288b76753872e32e1961a135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8ebb4a744b03e74bb8a54b432fc3f1c1f2625f3cd6538013af0c67330b485d`

```dockerfile
```

-	Layers:
	-	`sha256:c11d03f93411c9fe6253dc268629d85b87bc0a13b45004146f1d1f0098ac7412`  
		Last Modified: Mon, 15 Jun 2026 23:13:53 GMT  
		Size: 2.6 MB (2615466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c47db5f95c0913d104236ad0b04381505cfc1a37b4f603c47bc9146024a60b4d`  
		Last Modified: Mon, 15 Jun 2026 23:13:52 GMT  
		Size: 19.9 KB (19872 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:2115dc6c14735e2e81d568e75ee7563f785996dee04ff312bdf09019752b031b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121248107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad90f36f7f3e89f6705debb1dc0ff4a906df6036c8e001b5a3a935908195e727`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:15:43 GMT
ENV container oci
# Mon, 15 Jun 2026 04:15:44 GMT
COPY dir:553346a2ec24f0a482095311bcf74fe382a66c8cb976ea0b61f6d55ee917aca4 in /      
# Mon, 15 Jun 2026 04:15:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:15:44 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:15:31Z" "org.opencontainers.image.created"="2026-06-15T04:15:31Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:15:31Z
# Mon, 15 Jun 2026 23:13:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 15 Jun 2026 23:13:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:13:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 15 Jun 2026 23:13:06 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:13:06 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Mon, 15 Jun 2026 23:13:10 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 15 Jun 2026 23:13:11 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 15 Jun 2026 23:13:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:13:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:06005d885e6ce6c0708c4294316153d2de40b8859a131bbba11795c4f1e5eb71`  
		Last Modified: Mon, 15 Jun 2026 04:58:33 GMT  
		Size: 38.9 MB (38873024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7137000a02c54b9ca82c06ae1d9909485fee1624a876639075f86a25207955a2`  
		Last Modified: Mon, 15 Jun 2026 23:13:24 GMT  
		Size: 28.1 MB (28099037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46929c84a84543b113c8ac52cc7d0dcdf25d13e10980ea7186788372d9ae645`  
		Last Modified: Mon, 15 Jun 2026 23:13:25 GMT  
		Size: 54.3 MB (54273428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18938f6315ad83df53f23ead3ba257d00bf2b2f6fa933621830223f4831ff9b1`  
		Last Modified: Mon, 15 Jun 2026 23:13:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54796c4c7eb9426ba9e15e70bf6fe2d8f4cbfc5a1bcaf6b5d8aa42cf063e7208`  
		Last Modified: Mon, 15 Jun 2026 23:13:24 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e90c468e345c4024d09fb190fa34a83d0e76db59a3a4448dab253e87f671ebba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3704df026bd34961f27f06e5e52b2e1f956cb5de9fa7118cedeab67cd001d6e`

```dockerfile
```

-	Layers:
	-	`sha256:d391d6b54d74739ff3f9fc792f894ab7eb5919d0139af828b47df84f310569c3`  
		Last Modified: Mon, 15 Jun 2026 23:13:23 GMT  
		Size: 2.6 MB (2615536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f13361a3bff442c229821db83a96b68fd474ca06c2fdc179a1f52a6af1ea50b9`  
		Last Modified: Mon, 15 Jun 2026 23:13:22 GMT  
		Size: 20.0 KB (19989 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:06207ddcfff94bff851b40236114aac1960bbbd83f2acb3f9d84e78f712342eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127925271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a950688ac479e9eab70e43170437b3d8075d4cc770b05bcc97dd0717488def92`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:14:54 GMT
ENV container oci
# Mon, 15 Jun 2026 04:14:54 GMT
COPY dir:efdade3e0178260d1a2da6ad5ac90643bb0c91f0b6715fd2f4ca2979fd79cbad in /      
# Mon, 15 Jun 2026 04:14:54 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:14:54 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:14:54 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:14:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:14:55 GMT
COPY file:e844bf29c6ce679ad36ca75749d6db974a3ec704b6b681dbf49d34fbc703890c in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:55 GMT
COPY file:e844bf29c6ce679ad36ca75749d6db974a3ec704b6b681dbf49d34fbc703890c in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:55 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:14:43Z" "org.opencontainers.image.created"="2026-06-15T04:14:43Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:14:43Z
# Mon, 15 Jun 2026 23:14:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 15 Jun 2026 23:14:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:14:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 15 Jun 2026 23:14:12 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:14:12 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Mon, 15 Jun 2026 23:14:21 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 15 Jun 2026 23:14:21 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 15 Jun 2026 23:14:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:14:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:fd098750da592cfacf74625936c645114bdb046870485748bf918ed2db1df267`  
		Last Modified: Mon, 15 Jun 2026 06:12:54 GMT  
		Size: 45.2 MB (45156026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102fbe8029dfe532f57a1538c32f741d22163601d4b4fa9e2e8a0e9afe095270`  
		Last Modified: Mon, 15 Jun 2026 23:14:51 GMT  
		Size: 30.1 MB (30096922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabdf39b6144bf7b5e1e4c7f8a1226b48fa84838e9bf0405f4fda5bafe995492`  
		Last Modified: Mon, 15 Jun 2026 23:14:52 GMT  
		Size: 52.7 MB (52669706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccaeefddb18fa2429fa8f7260e8dc7d8fa01f67d5781f1face8cf5b707b88d92`  
		Last Modified: Mon, 15 Jun 2026 23:14:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091baecea99edd0282ebdd17fdbb6b2a738d8741eab57720382a8509e98bbaf3`  
		Last Modified: Mon, 15 Jun 2026 23:14:50 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a5fb43385ee2af5cc1203980817224b8f7a7191a958419c354695c195443909b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a9a550c7f931523b10d4f6f1076654a33a18a3ad31308926416b84a9e41219`

```dockerfile
```

-	Layers:
	-	`sha256:c5b294d7561088943d48a1261ee4ee194b1b6afc7f47315df0a7bdd076bfff49`  
		Last Modified: Mon, 15 Jun 2026 23:14:49 GMT  
		Size: 2.6 MB (2614191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22afc9ffd098104c6795b74ea7b7e321156f04aa1e013818dbc00fc5d3c3d8e1`  
		Last Modified: Mon, 15 Jun 2026 23:14:49 GMT  
		Size: 19.9 KB (19909 bytes)  
		MIME: application/vnd.in-toto+json
