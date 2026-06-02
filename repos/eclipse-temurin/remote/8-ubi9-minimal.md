## `eclipse-temurin:8-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:b04bb7eb49be4d0ea45c6029f653f2272972f957ff849b54213b1a59181b5577
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
$ docker pull eclipse-temurin@sha256:9b0de318468a82fbd9cf0c3e2ac1559c734bda3aa1afa0ec39a84dac1f0c29c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.6 MB (123550418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c61cbfdaa38b6c1c623f4da6581a2f4b625810a530531b22a6ad7d3c9af0dd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
# Tue, 02 Jun 2026 22:44:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 22:44:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:44:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 22:44:31 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:44:31 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 22:44:35 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 02 Jun 2026 22:44:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:44:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:44:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:dd148063a98f38d63a03cea2357d237d418889b91f204f507c033c944e443f45`  
		Last Modified: Tue, 02 Jun 2026 07:03:29 GMT  
		Size: 40.7 MB (40687042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3476e11832c294010e92b86aa38159e9aee6840fbb9f32aded1dad6a389f2c`  
		Last Modified: Tue, 02 Jun 2026 22:44:50 GMT  
		Size: 27.7 MB (27661640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f454eab4ff7dfb5adba041946618a8724bf1b2255dfa5d75e673186ad9dce0`  
		Last Modified: Tue, 02 Jun 2026 22:44:51 GMT  
		Size: 55.2 MB (55199117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6d4e7d0edc974f3287eb4c8dae26eadbbd538b35afd510f75d67ab88dd2311`  
		Last Modified: Tue, 02 Jun 2026 22:44:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd48f13ce7e3b92720d02ad074691e0f23565d222b8b4c239fffd8d737f73c81`  
		Last Modified: Tue, 02 Jun 2026 22:44:49 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:af4624c914abaf48816d6b125e32bb5e59e67fe56c6a93a40cc121fe3724b725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8369e398d0bb233b4fb6bce8a1701aa3c5e59904595fb028d96c62ec9e341e`

```dockerfile
```

-	Layers:
	-	`sha256:946d21f328eed2e5677373ee0059be44e093196f59cf8b0209de988708fc3975`  
		Last Modified: Tue, 02 Jun 2026 22:44:48 GMT  
		Size: 2.6 MB (2615450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afcfa0f11b47353079ad43f3c950ae7655276f2cae288c1578736acd11247cc3`  
		Last Modified: Tue, 02 Jun 2026 22:44:48 GMT  
		Size: 19.9 KB (19872 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:50aab2d78141ed7c8228e6364e9bcb09e26cc996f3763be420eaa4cf54de5f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121236512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fea6e3856aca75c7e0533e6f32fc0e909b8287f7ed5f995ee145240d2110d36`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
# Tue, 02 Jun 2026 22:44:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 22:44:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:44:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 22:44:18 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:44:18 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 22:44:22 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 02 Jun 2026 22:44:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:44:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:44:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:7db43598c7e47cf895f880f92e3cee9c07787091c97802ea3f2bea8fa4848040`  
		Last Modified: Tue, 02 Jun 2026 07:03:29 GMT  
		Size: 38.9 MB (38863161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a784eea23fad136d577de7f2b68cabc5b817e1986e18eac7a4349adfb3fbe5d`  
		Last Modified: Tue, 02 Jun 2026 22:44:36 GMT  
		Size: 28.1 MB (28097332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bed43de0e7fe6a1f121add93c7a5f1ee8253c7c7b2c67fab20b58a6148a32e`  
		Last Modified: Tue, 02 Jun 2026 22:44:37 GMT  
		Size: 54.3 MB (54273403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5797b4bb559ff5b7eb024032367f2c1bde531fcaa22549a868d53784602c808`  
		Last Modified: Tue, 02 Jun 2026 22:44:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d29acddb5e670c0eea853f74faf7abb13e711e6461f3ed72069dc4537c98f0`  
		Last Modified: Tue, 02 Jun 2026 22:44:36 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:24bb83c76dddaed50b5dddd3bb8c20808e01eac85a13c793a65b082378f64972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be99696b6cbf106ab52d78ae179ce43836635a2c45ace0bea789fa60a2efe2ac`

```dockerfile
```

-	Layers:
	-	`sha256:2d30125c051983e9fb7d0155f33ac983994c5131a38bea3355b1757ed37e6017`  
		Last Modified: Tue, 02 Jun 2026 22:44:34 GMT  
		Size: 2.6 MB (2615520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e94164c577da31d59052cb64bb23c44a3a4a5b945b807fb85587651ffd9b39d8`  
		Last Modified: Tue, 02 Jun 2026 22:44:34 GMT  
		Size: 20.0 KB (19989 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:2d856f2fe6c21245283ef3fb687903ed89332fcfa52159198edc8a6cf759f515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127912488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa612e03835e01488d0232d1738481d8f384dd52a69121eb55251a3f9d8f266`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 22:45:49 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 02 Jun 2026 22:45:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:45:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:45:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:af22f900dccaabe4adc742744318c3037108e5bf7d90c92179baaf7b6a23a03b`  
		Last Modified: Tue, 02 Jun 2026 22:46:33 GMT  
		Size: 52.7 MB (52669698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14a8ddc399754923a496561cd1522cc7bdb321a85168b374a247f8e8c49e797`  
		Last Modified: Tue, 02 Jun 2026 22:46:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce95f91ec5638e9d9ed94177b9a58afac4b25a8b6c11640284edfa243a29c0a`  
		Last Modified: Tue, 02 Jun 2026 22:46:32 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9942cf53586351821ed5cac116da1abdb0672e1b8b2b31de204572260a94679f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3504dcf74539bea8c63e52735f1891fb1cc8575c45af56528b5e099f72648404`

```dockerfile
```

-	Layers:
	-	`sha256:144494f708435852ae9a7835f3a9569559a7a70c79fdbfe28d26a22f4816fe91`  
		Last Modified: Tue, 02 Jun 2026 22:46:30 GMT  
		Size: 2.6 MB (2614175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f1b687105c443fbcd87f7785c117ef3f54de4d362fd4a863aff72709e5b778`  
		Last Modified: Tue, 02 Jun 2026 22:46:30 GMT  
		Size: 19.9 KB (19908 bytes)  
		MIME: application/vnd.in-toto+json
