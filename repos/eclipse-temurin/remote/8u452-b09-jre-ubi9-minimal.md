## `eclipse-temurin:8u452-b09-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:55d5dcc2e27e406bd6354aef8d22f22bd5aee18a50dfaf5be32dd79cd3500a8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8u452-b09-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:68eb5bef31ab3c433377eebffadb88f52a0bc08a2170ed5983c256992c2f817b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 MB (109080841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be6a75d9edfd67d7d5eeb50c459cec0ac60df33a88d3534d9dbea18f131e711`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL maintainer="Red Hat, Inc."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL vendor="Red Hat, Inc."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL url="https://www.redhat.com"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.openshift.expose-services=""
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sun, 27 Apr 2025 20:21:59 GMT
ENV container oci
# Sun, 27 Apr 2025 20:21:59 GMT
COPY dir:9f1e3d7980aa1b8b007cf8dcf05575fff696655332be09ae87c8f7de7f00e923 in / 
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Sun, 27 Apr 2025 20:21:59 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL "build-date"="2025-06-24T16:31:57" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="69e50e2a07c936e700297091886db408257a857c" "release"="1750782676"
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5d0c81fd8bee49d1b9931acaecdc528fdc9393547cf5b24880445ade6b3f2384';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        ppc64le)          ESUM='d9b523defdea8b82647726de8f62b57a19f2c64020b9ab6dbc5ae4929d0ee64e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        x86_64)          ESUM='0c76f94e1b400a4da932a3f581b0788af2101819083184f40a6c76ac9b97081f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_x64_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:7073092d8bcd7b6d72345cfa87d8389a33f629b3c49ff887ad3a51c6ed8dfd83`  
		Last Modified: Tue, 24 Jun 2025 18:09:29 GMT  
		Size: 39.7 MB (39650665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601bfc79dea21f0c518a6b115ae36a88e1a66970262a1bfe37648a607e56c21d`  
		Last Modified: Wed, 25 Jun 2025 17:54:12 GMT  
		Size: 27.5 MB (27545315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a4fe36c4b99c7da68ce982b5bd85a5e61d163fbe96852c2c549781de16d95c`  
		Last Modified: Wed, 25 Jun 2025 17:54:15 GMT  
		Size: 41.9 MB (41882441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0655edd8a84b6d3d6a06a94c8ccc719c53e4ca7fbdcc76d1db202ad8c42ebd`  
		Last Modified: Wed, 25 Jun 2025 17:54:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804a8269a596dce3f7f5391981271c4c821ba06542499193a7e850145f279d5e`  
		Last Modified: Wed, 25 Jun 2025 17:54:09 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u452-b09-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:69cec847046cf8fbc5de1fe4cb260126b50fad2efcd017a1c12cbac3a9916612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2439839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace17e1241aef148bed31e7e1ccc61663f411af100f83613707a2aa5b4d5ca3e`

```dockerfile
```

-	Layers:
	-	`sha256:2a3efb1c821d2b342888371290f87d1ed40366acd2ae66f920e2ba97eed5de51`  
		Last Modified: Wed, 25 Jun 2025 18:16:54 GMT  
		Size: 2.4 MB (2420480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7111127fc2717bd613e4397d44f599e7637a94b1858b9fd528e1129d3debf257`  
		Last Modified: Wed, 25 Jun 2025 18:16:54 GMT  
		Size: 19.4 KB (19359 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u452-b09-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:5b8c2d8f0436052d954b6a3c76cc900e72ec5f1cd57ac4447278037f752b11d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106806559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd976ab2ace579a4610886829bb425edc47c238be2da6b37d54ba798a51344e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL maintainer="Red Hat, Inc."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL vendor="Red Hat, Inc."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL url="https://www.redhat.com"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.openshift.expose-services=""
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sun, 27 Apr 2025 20:21:59 GMT
ENV container oci
# Sun, 27 Apr 2025 20:21:59 GMT
COPY dir:dd3dc18ab466569b07043336c84190595a673cf78699fcf70dbf83deddf44d87 in / 
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Sun, 27 Apr 2025 20:21:59 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL "build-date"="2025-06-09T17:24:02" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e18551b8a7ac3e7aa6347d84b9f0b5c8cc8fe52" "release"="1749489516"
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5d0c81fd8bee49d1b9931acaecdc528fdc9393547cf5b24880445ade6b3f2384';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        ppc64le)          ESUM='d9b523defdea8b82647726de8f62b57a19f2c64020b9ab6dbc5ae4929d0ee64e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        x86_64)          ESUM='0c76f94e1b400a4da932a3f581b0788af2101819083184f40a6c76ac9b97081f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_x64_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f258ee7f14ce0e3998c50b14ce17a0c0115edefcb69d96c3ef016548422246c8`  
		Last Modified: Mon, 09 Jun 2025 18:09:34 GMT  
		Size: 37.9 MB (37922296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c92d528d56d0b425ec1ece8f3484b678fe8fbdfc0181c1023bc51b43374538`  
		Last Modified: Tue, 10 Jun 2025 17:44:06 GMT  
		Size: 28.0 MB (28005980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062d23d10a4516f84d08bda5d95c049380388a3555b7c1a445c510454c81ce10`  
		Last Modified: Tue, 10 Jun 2025 19:48:02 GMT  
		Size: 40.9 MB (40875865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f3f222afb76103bb78d354e3d82e16d84581975f45ce5c4a557239395fa440`  
		Last Modified: Tue, 10 Jun 2025 17:44:05 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8f18320a46570b412d0404f15d93d26328e2f180ae0d83b3b9668e06ace071`  
		Last Modified: Tue, 10 Jun 2025 17:44:06 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u452-b09-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:761f0ba4511318c6305481925eb2f2d798e863ffd28d8365c768d59e84eb7c89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2439922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7cddbadb681efa93bd9f0421ed7c6a4b91bcffc451f1dc16a33ea5091d7440d`

```dockerfile
```

-	Layers:
	-	`sha256:cd84c389a42b7c8f02c781ae9473092aa490c959fb4c8f41c5f598932bce060a`  
		Last Modified: Tue, 10 Jun 2025 18:17:19 GMT  
		Size: 2.4 MB (2420458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c236eac165a6879a72b5747abe8bc75077d2d2c9ae0d5981dd32ae36511ebe3`  
		Last Modified: Tue, 10 Jun 2025 18:17:19 GMT  
		Size: 19.5 KB (19464 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u452-b09-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:08f569e1a888b034fe0a503b3544be8e08a273f3ab04c0506404670d2257083c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115278746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14511cd5b732ddb77d8a03f880a8e6a5b581021f1f12bf21d4932078c42da335`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL maintainer="Red Hat, Inc."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL vendor="Red Hat, Inc."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL url="https://www.redhat.com"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.openshift.expose-services=""
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sun, 27 Apr 2025 20:21:59 GMT
ENV container oci
# Sun, 27 Apr 2025 20:21:59 GMT
COPY dir:d83abf82dbf4be7abfad8c73a5c54416daede00b99a88ceef5492299e80e8120 in / 
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Sun, 27 Apr 2025 20:21:59 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL "build-date"="2025-06-24T16:34:39" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="69e50e2a07c936e700297091886db408257a857c" "release"="1750782676"
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5d0c81fd8bee49d1b9931acaecdc528fdc9393547cf5b24880445ade6b3f2384';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        ppc64le)          ESUM='d9b523defdea8b82647726de8f62b57a19f2c64020b9ab6dbc5ae4929d0ee64e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        x86_64)          ESUM='0c76f94e1b400a4da932a3f581b0788af2101819083184f40a6c76ac9b97081f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_x64_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:8374cdcea99a5f341eb5030b5ece88085798cef7a6357cfcc46f8db2ab3dcbc9`  
		Last Modified: Tue, 24 Jun 2025 18:09:28 GMT  
		Size: 44.0 MB (44041398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5872ee8c9a0f398b2cc0631abe2164a5c0397d35045d1f9af834e8f8f4da60c2`  
		Last Modified: Wed, 25 Jun 2025 17:54:51 GMT  
		Size: 30.0 MB (29977285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2726431af0e9c7e9b8bf8fd0ef1e63c0169462959c8ff1618e4fb0ddbfebd4d3`  
		Last Modified: Wed, 25 Jun 2025 17:55:50 GMT  
		Size: 41.3 MB (41257646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7b48b87ff2c8fd51503491408192e19f3c333c347cc2354569d568bfc476a8`  
		Last Modified: Wed, 25 Jun 2025 17:55:46 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a7a8d9bf68d420be14364247818843221976acb46e248ca36b428bf2a49043`  
		Last Modified: Wed, 25 Jun 2025 17:55:46 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u452-b09-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:20b8f71c0c7f501ff4a38db34adae79de1961ecf150157595afc266ddfbd25b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2440565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3eacec024e0e842bf605174ab5681da7cb81f0dfb81734e171733208dfaea1`

```dockerfile
```

-	Layers:
	-	`sha256:90a162d2fa319ed7a52fdac89d78cd30085aa1e55def1f78895f0297fdc6605b`  
		Last Modified: Wed, 25 Jun 2025 18:17:11 GMT  
		Size: 2.4 MB (2421177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd0593cb00a19bcefb62b63d0c6efa8ba19f1e8ac96dccad5de3b99dd9399aba`  
		Last Modified: Wed, 25 Jun 2025 18:17:12 GMT  
		Size: 19.4 KB (19388 bytes)  
		MIME: application/vnd.in-toto+json
