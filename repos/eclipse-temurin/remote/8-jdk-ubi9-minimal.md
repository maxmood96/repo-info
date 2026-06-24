## `eclipse-temurin:8-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:a8c2a97cf9d13e2796f7a8e01fea48f509193b96dd143a1f129e19d8616c4758
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:52693f445f76ac5298422de08c8d22934c0dd972272de1a50b214357b2a4a64e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123533193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272206a1eec5c17b29c9b49474ad09f7cc7860726134c67fef0c696bce7b4a26`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:11:46 GMT
ENV container oci
# Tue, 23 Jun 2026 05:11:46 GMT
COPY dir:f278a99c81d25e574e4095be97d2e212c8bd76544b73ffdab7eab4c5e42d12b6 in /      
# Tue, 23 Jun 2026 05:11:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:11:46 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:11:47 GMT
COPY dir:c2709a3d2c126f3448a9859c7e12a4347d4fe7ea0104c04c47ebdcbe0d9f7851 in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:11:47 GMT
COPY dir:c2709a3d2c126f3448a9859c7e12a4347d4fe7ea0104c04c47ebdcbe0d9f7851 in /root/buildinfo/      
# Tue, 23 Jun 2026 05:11:47 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:11:30Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:11:30Z" "architecture"="x86_64" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:11:30Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:03:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 23:03:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:03:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jun 2026 23:03:31 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:03:31 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Wed, 24 Jun 2026 23:03:35 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 24 Jun 2026 23:03:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 24 Jun 2026 23:03:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:03:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:689a2fa06433046ccdc79ee32d366190123758804fb645bc032123dc904e226b`  
		Last Modified: Tue, 23 Jun 2026 05:49:10 GMT  
		Size: 40.7 MB (40671135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8a928ab438b45ef2225a77d4eb4e882174cb747b41ebe1f1a471997e0cada3`  
		Last Modified: Wed, 24 Jun 2026 23:03:49 GMT  
		Size: 27.7 MB (27660308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e5de237f6d86c03bdaa30e820a5d729e9ea9b17ef184bbd1dcfd00dade071a`  
		Last Modified: Wed, 24 Jun 2026 23:03:50 GMT  
		Size: 55.2 MB (55199134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db77e94152f27e8891fac62e3311edfc52fd358bc5e4741ea9804ee226192dec`  
		Last Modified: Wed, 24 Jun 2026 23:03:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b5d4db5eff089be5160d535c6be5170774a0cb285b1e128392407028ef9b94`  
		Last Modified: Wed, 24 Jun 2026 23:03:49 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:24d898c0c8bb8fb2c780cb0e578921999949c5c46392801d0bcbb33c57a031ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7ab26074e32ccaa9c433ca770ef9587f4888bd8d1c782a9f603fc51cf5c7fb`

```dockerfile
```

-	Layers:
	-	`sha256:fa760ac444eff5bd68bd217389800145a22fd87a96ae13c93994a0fc967265ad`  
		Last Modified: Wed, 24 Jun 2026 23:03:48 GMT  
		Size: 2.6 MB (2615478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a616f64624e3752f1aed0578364c596d31db4408968745a5d2f72ac1131430d`  
		Last Modified: Wed, 24 Jun 2026 23:03:48 GMT  
		Size: 19.9 KB (19873 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:3d07248f499953fc117290edf9b9a42bfe1fe2e9ecc84e5d9099e339e6514ea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107141372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8c589987356c39cb7c24f82306aee6922371ed2635417a8f36a535e0c77e36`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:12:59 GMT
ENV container oci
# Tue, 23 Jun 2026 05:12:59 GMT
COPY dir:923fd04a317c8ab7292cc4c6490977e5f3d0a2e1ff9dc5a4ce7f5c95aef17062 in /      
# Tue, 23 Jun 2026 05:13:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:13:00 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:13:00 GMT
COPY dir:dffe6ac0f40d1fc4397ba26e90223bac1cf14e7dcba262c2807afbcac45f5ea3 in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:13:00 GMT
COPY dir:dffe6ac0f40d1fc4397ba26e90223bac1cf14e7dcba262c2807afbcac45f5ea3 in /root/buildinfo/      
# Tue, 23 Jun 2026 05:13:00 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:12:36Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:12:36Z" "architecture"="aarch64" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:12:36Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:02:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 23:02:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:02:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jun 2026 23:02:45 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:02:45 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Wed, 24 Jun 2026 23:02:50 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 24 Jun 2026 23:02:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 24 Jun 2026 23:02:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:02:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:989109f74f2ed8868dc53877eebf602a5b9e56448cce38c307c203e890a4c731`  
		Last Modified: Tue, 23 Jun 2026 06:05:10 GMT  
		Size: 38.8 MB (38805824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d50749e2d2f2dd546d7f5c28ddd2c200dee09d37fc0711abe00078264c4f58`  
		Last Modified: Wed, 24 Jun 2026 23:03:03 GMT  
		Size: 14.1 MB (14059503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3286f3dc6412d5b0de2309b0484fe310977d3607127fddb1d06a34ffc67f34`  
		Last Modified: Wed, 24 Jun 2026 23:03:04 GMT  
		Size: 54.3 MB (54273427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd88bd749688ea594346b60aefe21ca8330206aac404fad8c278a1dea9854bd`  
		Last Modified: Wed, 24 Jun 2026 23:03:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081e3349d89a3fbabe9a2ea349d02e2948e155590c64187db09a750093f6c3fa`  
		Last Modified: Wed, 24 Jun 2026 23:03:03 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e41186255e45e10c8482838d3df2f540f41e20817cb83075a264a46b1aeab172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1897371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b858adcf389926d92c627d2ce6780bd1481d5819cdacc5da16bb9bae2613f61`

```dockerfile
```

-	Layers:
	-	`sha256:bd32fb12aba453165fd4160906606ba290b7dd1b4c49f26cc5d79425f196bb01`  
		Last Modified: Wed, 24 Jun 2026 23:03:02 GMT  
		Size: 1.9 MB (1877382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00be863a982e8f61a04b56b7e7bea2c65a5d7f6af53529e904e240c7fd70a5ed`  
		Last Modified: Wed, 24 Jun 2026 23:03:02 GMT  
		Size: 20.0 KB (19989 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:dcb2257ba9649d228c6059f37aaf5b4081f5696f7f97f9d38c3b408844c97034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112974858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2277c8ae966c06ab7f756dd17346878e0301c588b408baf811b8175de9e6b66`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:13:01 GMT
ENV container oci
# Tue, 23 Jun 2026 05:13:02 GMT
COPY dir:4d2a3ebfba3e6886b6504d8dd92beaac194e548e40aa4bca182adbaa9be02afc in /      
# Tue, 23 Jun 2026 05:13:02 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:13:02 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:13:02 GMT
COPY dir:b7827d131ad066b0f131c7ebfb16ff261b70c3cbb8cf357ab0913f8aa1eef055 in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:13:02 GMT
COPY dir:b7827d131ad066b0f131c7ebfb16ff261b70c3cbb8cf357ab0913f8aa1eef055 in /root/buildinfo/      
# Tue, 23 Jun 2026 05:13:02 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:12:46Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:12:46Z" "architecture"="ppc64le" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:12:46Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:01:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 23:01:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:01:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jun 2026 23:01:50 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:01:50 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Wed, 24 Jun 2026 23:02:01 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 24 Jun 2026 23:02:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 24 Jun 2026 23:02:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:02:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:4bac72a9a1f43367def803d06c2dab63b4bb0e322cb08ee3db80259d84e62045`  
		Last Modified: Tue, 23 Jun 2026 06:12:06 GMT  
		Size: 45.1 MB (45144751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f99e1bd1d0e0245b9ff9de06dc4f155f0170e63761b11e9c13863eabbea391`  
		Last Modified: Wed, 24 Jun 2026 23:02:32 GMT  
		Size: 15.2 MB (15157790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ec056f124f1814195fdf5a0ac707060366cd675d45e2cdda2778bde89e80ee`  
		Last Modified: Wed, 24 Jun 2026 23:02:33 GMT  
		Size: 52.7 MB (52669699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7689db23e8337b3aa40c037db14325912b10900542bbccd535acf2ee3c28778`  
		Last Modified: Wed, 24 Jun 2026 23:02:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21062dc224b327f4a9d8fe981a307f3ed8255d4a58533a4b8eb0dfd620ef4846`  
		Last Modified: Wed, 24 Jun 2026 23:02:32 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:109b11bf4737b76f04092648f97e906ef157557351bc5c9be4541dce59bd444e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1897090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd6d416450201ce392f8dd313e7ec9be3fe01157a5860da546d9c0dab64ae23`

```dockerfile
```

-	Layers:
	-	`sha256:d844caf16c39fbbf3a6cf9c1abfa7a649617e29b99557f5718dd68494df9d347`  
		Last Modified: Wed, 24 Jun 2026 23:02:31 GMT  
		Size: 1.9 MB (1877181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a93bc852f462bbc59c1a78ff11df91d34d51fefaf03df1bf7ce47d065ebec91`  
		Last Modified: Wed, 24 Jun 2026 23:02:31 GMT  
		Size: 19.9 KB (19909 bytes)  
		MIME: application/vnd.in-toto+json
