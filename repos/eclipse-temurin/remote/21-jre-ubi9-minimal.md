## `eclipse-temurin:21-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:96350e02809c4b33501904c8037a79e48025cfde0518f878d2b3930f9c654950
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

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:30ea763ae415430eb3adfda0c76aafec25d73e1c26f95af8159c5d492a713584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123375861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d3cf707f0301ec14e3b40307ba945939b23b6d8b7708e6e90b2c1a9687ae7bd`
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
# Wed, 22 Apr 2026 18:17:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:17:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:17:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:17:23 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:17:23 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 22 Apr 2026 18:17:29 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 22 Apr 2026 18:17:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:17:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:17:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:c770e69088fa05bea8942da1c1e3fa6066cc7c288153d81443e0c9435861e0b1`  
		Last Modified: Wed, 22 Apr 2026 05:40:43 GMT  
		Size: 40.0 MB (40024775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8256b534a9d13ef1700a6aa4c9d6339d837ed5f4fe6654aabdd414594715fb9e`  
		Last Modified: Wed, 22 Apr 2026 18:17:45 GMT  
		Size: 30.4 MB (30367928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca102f83ecd97ba81408abd06d525f9239b6a2f4a2c69e029d105119e54e231e`  
		Last Modified: Wed, 22 Apr 2026 18:17:46 GMT  
		Size: 53.0 MB (52980741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0d08e863edf63245f347a194da05d985b1917097a6f855e3b87a257947b224`  
		Last Modified: Wed, 22 Apr 2026 18:17:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec968abde22243d43816e9af77da9589ffa1e2037080a826f52cc9976f3b73a8`  
		Last Modified: Wed, 22 Apr 2026 18:17:44 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1dffbc6104f55770153b65b990372559d0d4c89f9821af27398af1c38ef806eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2437143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498b25f28e625eae7310768b9353764c12ed2725e9e64f82203fed75173c7594`

```dockerfile
```

-	Layers:
	-	`sha256:c205748121a10ac4eabb1f4abbfd407fb0b108a6409335f75f6e105125bf66df`  
		Last Modified: Wed, 22 Apr 2026 18:17:44 GMT  
		Size: 2.4 MB (2416957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a41f067407efa8e016c72eb28f926ff1dfd933799e3307c67ac76bf8a8bb85ff`  
		Last Modified: Wed, 22 Apr 2026 18:17:44 GMT  
		Size: 20.2 KB (20186 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:43ea0b20fbb9851c19bd1764473f93129c3318682c763a3b5e2dddbf0e56ef54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121156141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb1f7e169b1b7a503ac287e3f949e6c82f4dfc6d89f1101ca28f4059bef6ecf`
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
# Wed, 22 Apr 2026 18:16:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:16:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:16:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:16:13 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:16:13 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 22 Apr 2026 18:16:41 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 22 Apr 2026 18:16:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:16:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:16:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:c57a97b2502dbf8d905aa782f6a2be8f57c8774e28f6d2ddf6a9a866fcc5fd8b`  
		Last Modified: Wed, 22 Apr 2026 06:11:08 GMT  
		Size: 38.2 MB (38204491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a341d0b8c7233ec1ac49133bc13e41ed24e1b87adf9e17ad4d9d01a9119ef97`  
		Last Modified: Wed, 22 Apr 2026 18:16:30 GMT  
		Size: 30.8 MB (30793019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fdb2b5539ea711aa3bae7bc378332e59c6591ca2b706076d4d90b6a4400481`  
		Last Modified: Wed, 22 Apr 2026 18:16:55 GMT  
		Size: 52.2 MB (52156215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747d2d02f2cbb4f2710160d330eda77c204c9ef6546803bbc30841b385f1a218`  
		Last Modified: Wed, 22 Apr 2026 18:16:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb937a3dbacf116736259797b7bb7b479ac05ca700595f6be96a0fce5dbd2b6`  
		Last Modified: Wed, 22 Apr 2026 18:16:53 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:53b756dd0632afdc4da02c665dd79024617a66fe32dd5b2de5c9e2724198bc25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2436605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58de17a417f6121abd3022a8ee8c7f4a725df2e52f7cfb1cfeb4fdba2fd0da9`

```dockerfile
```

-	Layers:
	-	`sha256:03b43d6b5beed147a89abd3e5d586d09100db05d5a5c857ebbddddef6f0118d5`  
		Last Modified: Wed, 22 Apr 2026 18:16:54 GMT  
		Size: 2.4 MB (2416315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62eec81f54dcffb8f8641ef72b5e58a6cc6c5b4087741f3f8dbd7c601cbf7ad0`  
		Last Modified: Wed, 22 Apr 2026 18:16:53 GMT  
		Size: 20.3 KB (20290 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:2ddeed56e5b770e37b17888b2d5fb783990588a69fae420f04a2a439b1938e4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130259417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0845b0d69a13460f0ef0ffd6b979fa395e68986063c6a9efd448a1d5240807c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 20 Apr 2026 00:48:23 GMT
ENV container oci
# Mon, 20 Apr 2026 00:48:24 GMT
COPY dir:8240d23726e865ba51f291ba4ea188782a75a0af67ec349dc8d9d3bc145ecd05 in /      
# Mon, 20 Apr 2026 00:48:24 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 00:48:24 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 00:48:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 00:48:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 00:48:24 GMT
COPY file:54c55160da8e94b0ed06988eaccac768df07b2ab8418806d9245b992ab4c1444 in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:48:24 GMT
COPY file:54c55160da8e94b0ed06988eaccac768df07b2ab8418806d9245b992ab4c1444 in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:48:25 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "org.opencontainers.image.revision"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "build-date"="2026-04-20T00:48:13Z" "org.opencontainers.image.created"="2026-04-20T00:48:13Z" "release"="1776645941"org.opencontainers.image.revision=0bc61a274edddc1467c2ad0ddc3139543c4da4da,org.opencontainers.image.created=2026-04-20T00:48:13Z
# Mon, 20 Apr 2026 23:00:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Apr 2026 23:00:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:00:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Apr 2026 23:00:52 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:00:52 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Mon, 20 Apr 2026 23:08:12 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 20 Apr 2026 23:08:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:08:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:08:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:9d0996bd7c74d1634fd0ba1753a8f74e86b97c5b41318f888d6b7bcc768131db`  
		Last Modified: Mon, 20 Apr 2026 12:13:59 GMT  
		Size: 44.4 MB (44443917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242b1bfcc64f23f4a2cc6ba069104831d0f144abd63cec2aa7e370ca093096b9`  
		Last Modified: Mon, 20 Apr 2026 23:01:35 GMT  
		Size: 32.8 MB (32848454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84038c19578717500b20064acfe4e03c389ae95c9ee68f88612f804594cb89d`  
		Last Modified: Mon, 20 Apr 2026 23:08:49 GMT  
		Size: 53.0 MB (52964629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80834e12c7c0884f0462042cbfb11ab56a97a1d7b60befe82407a610921623f8`  
		Last Modified: Mon, 20 Apr 2026 23:08:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcec7936600d67ce153b203452800dd01c6c4fca4d6833f2f901595b55a288e`  
		Last Modified: Mon, 20 Apr 2026 23:08:47 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:76157279f28258810effe1ffeaf64851524817c3022a72cb31b9998d2a622c3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2437178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df79b574c68c01414b733e1a70882393de4fbce8eebd8185e465f8dcea986524`

```dockerfile
```

-	Layers:
	-	`sha256:e746f568523ffc7be72d1fed8aa8d5b98e570b33f918feb25869fe3554d3bcef`  
		Last Modified: Mon, 20 Apr 2026 23:08:47 GMT  
		Size: 2.4 MB (2416962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8110ea224bb5deb1213b579cb97792586a305f7e38e7492f009cb553368f784`  
		Last Modified: Mon, 20 Apr 2026 23:08:47 GMT  
		Size: 20.2 KB (20216 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:d332ffc3595c2fb90766f49f6a8af6229406e6d6b28b2e4ed56eab3c72eeabd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 MB (118049199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a92b68746307ada697c39561ed60d637618f0495463042dc579bf09894228a`
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
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 22 Apr 2026 18:21:10 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 22 Apr 2026 18:21:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:21:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:21:16 GMT
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
	-	`sha256:1ab3cc388f5bb3c3e258c6f0c301e2737c37824b51ba930bcf62ba0135e77713`  
		Last Modified: Wed, 22 Apr 2026 18:22:25 GMT  
		Size: 49.5 MB (49528706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2660c5d60cf36d8cb17fce21262bd5c732588efab4738b9555f0a40a767294f6`  
		Last Modified: Wed, 22 Apr 2026 18:22:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e59418b90275a77290b068cb6a8acac5991406d477f81732af92b123795d83`  
		Last Modified: Wed, 22 Apr 2026 18:22:22 GMT  
		Size: 2.3 KB (2287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3afbf781dd1c2fe806b7607c18137d64a7526d7b3872a08c06f24f9076eeaaad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2428935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91524d7db00ae77477bc4464f02fc51d32a4c4c7c4f4bddcaf8e305e928cee8`

```dockerfile
```

-	Layers:
	-	`sha256:7bd857cb7b57d18e3162729996df875b324ca2eafb1d6a78335f9db3618ea390`  
		Last Modified: Wed, 22 Apr 2026 18:22:23 GMT  
		Size: 2.4 MB (2408749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a0d5f3a43cc5211bc2e210b2c85dcda416d6841ca7da73167a861209680ea86`  
		Last Modified: Wed, 22 Apr 2026 18:22:21 GMT  
		Size: 20.2 KB (20186 bytes)  
		MIME: application/vnd.in-toto+json
