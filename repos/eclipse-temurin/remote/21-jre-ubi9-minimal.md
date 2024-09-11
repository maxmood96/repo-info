## `eclipse-temurin:21-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:e63b039258a1e6423ccb593fa079dd3e9d5ae228fc7d652a3d90d935d1082568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:fc3b8bc31337dda929e24f97856e24c1db189f28c8dab92fd3c44618f5ff6040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120359409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2068fd4fe5d6d87e7b2e15b19bc23ea33fe097310cbb30ec627d75e5197cb52`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 09 Sep 2024 02:59:59 GMT
ADD file:b37317a01d7c138350a7dd1214596c9e331f2443e4202fb62e450e297a8884ec in / 
# Mon, 09 Sep 2024 03:00:00 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 09 Sep 2024 03:00:00 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Mon, 09 Sep 2024 03:00:00 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Sep 2024 03:00:00 GMT
ENV container oci
# Mon, 09 Sep 2024 03:00:00 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 03:00:00 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 03:00:01 GMT
RUN rm -rf /var/log/*
# Mon, 09 Sep 2024 03:00:01 GMT
ADD file:b7994b75b70a7a3dfcf6b1fce6d3be08fac202f008a87a5e9c4a46e3ba552516 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Mon, 09 Sep 2024 03:00:01 GMT
ADD file:42184a4eb8e0b654da33b3c8593adbf1bd40e95928a3bb35c340d1f9eb9affbd in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Mon, 09 Sep 2024 03:00:01 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Mon, 09 Sep 2024 03:00:06 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Mon, 09 Sep 2024 03:00:12 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 09 Sep 2024 03:00:14 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='58845ce4275f3ec74fba075597c8216bb201773da036c4703be8b7b7b457355d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64le)          ESUM='46cf93653e2b553fb1c91760cfe2ff20999ba358d648d2df69e5948784768440';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='7fb5b09987cb41de5118fecb5a81771b3a38a245cff411b39af33dbfbca3e760';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='d3affbb011ca6c722948f6345d15eba09bded33f9947d4d67e09723e2518c12a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d4f239055d063750dddeb4ae84b23d0a708ce76be3167f93d2ba2ba70b50547`  
		Last Modified: Mon, 09 Sep 2024 20:38:20 GMT  
		Size: 39.1 MB (39082464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b328994d9bd23b172075615472354832cdadb44241996fca017f328b8c3823`  
		Last Modified: Wed, 11 Sep 2024 00:54:03 GMT  
		Size: 27.8 MB (27764026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8661b3221f4e9175b32c0a1bedb996f1005531190fef556d6a97fa13c5e8ea8e`  
		Last Modified: Wed, 11 Sep 2024 00:56:19 GMT  
		Size: 53.5 MB (53510678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07dea933e6e6e2083a1a323e195f11bf918c9a2f66809d3e89a3f1676c39690f`  
		Last Modified: Wed, 11 Sep 2024 00:56:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af382a677b4ffbf416fd85e7c0ffc9a1e87b057f7adecc8e44190567562a927e`  
		Last Modified: Wed, 11 Sep 2024 00:56:11 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:f3f6a7317a9d30bf1a2639fa5f478706f0a8d85a8c55dae9b880490c00b53c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118214794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7872b056ed2963d219eadf2faac3641fbfa0413bfe642e6a2408ef9a3f71c0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 09 Sep 2024 02:59:59 GMT
ADD file:56f22ae3154053f9bb870d963b65d5bc807ceb1db4d62ee1e134d6b82240d225 in / 
# Mon, 09 Sep 2024 03:00:00 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 09 Sep 2024 03:00:00 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Mon, 09 Sep 2024 03:00:00 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Sep 2024 03:00:00 GMT
ENV container oci
# Mon, 09 Sep 2024 03:00:00 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 03:00:00 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 03:00:02 GMT
RUN rm -rf /var/log/*
# Mon, 09 Sep 2024 03:00:02 GMT
ADD file:a072fef81c54a753e1604edc416ac2544eecc9191cf9e4acaf7cbf28183d7ce7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Mon, 09 Sep 2024 03:00:02 GMT
ADD file:b7e28c2e39378854f86cb05f59f944d37a1f7191a4c55a40adcd823d87e2c90b in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Mon, 09 Sep 2024 03:00:02 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Mon, 09 Sep 2024 03:00:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Mon, 09 Sep 2024 03:00:05 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 09 Sep 2024 03:00:07 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='58845ce4275f3ec74fba075597c8216bb201773da036c4703be8b7b7b457355d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64le)          ESUM='46cf93653e2b553fb1c91760cfe2ff20999ba358d648d2df69e5948784768440';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='7fb5b09987cb41de5118fecb5a81771b3a38a245cff411b39af33dbfbca3e760';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='d3affbb011ca6c722948f6345d15eba09bded33f9947d4d67e09723e2518c12a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:abd9eccbef61279a9e1f196b399e5d6336f30519eb5063b2b0fa30be9e4e845d`  
		Last Modified: Tue, 10 Sep 2024 14:48:49 GMT  
		Size: 37.3 MB (37337162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4383f3f4ab0221848aacb530c0ed4524f6705b84fcb60132c748d9bf10764d55`  
		Last Modified: Wed, 11 Sep 2024 00:50:26 GMT  
		Size: 28.2 MB (28239269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976a26be16d0f0c850036d168815a4a16a9f8e8fb5d9225a92d0bede06d62b46`  
		Last Modified: Wed, 11 Sep 2024 00:52:31 GMT  
		Size: 52.6 MB (52636121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f1047b43fc04dbe64b49dde591b679e31b51ca7d3fdc1662ca30e1b180b534`  
		Last Modified: Wed, 11 Sep 2024 00:52:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8357d8f10a8bd1d339a412aa855c827665113eb7ee1696d7f4a42534dbbb004`  
		Last Modified: Wed, 11 Sep 2024 00:52:25 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:f164bea8c5630cedf62811f9c2424c8132d9783f7cd0eef30b341af332567e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127451985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662e6b48ba583f2b9fc1c3db14e52cab079512eb02fb141b28beea991767ff87`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 09 Sep 2024 03:00:09 GMT
ADD file:53f505eeabbc2654e5516e5aae0ecaf62fce16a6f00ef5bda096d4bdb7176df3 in / 
# Mon, 09 Sep 2024 03:00:11 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 09 Sep 2024 03:00:11 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Mon, 09 Sep 2024 03:00:12 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Mon, 09 Sep 2024 03:00:12 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Sep 2024 03:00:12 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Mon, 09 Sep 2024 03:00:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Sep 2024 03:00:12 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Sep 2024 03:00:12 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Sep 2024 03:00:12 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Sep 2024 03:00:12 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Sep 2024 03:00:12 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Sep 2024 03:00:12 GMT
ENV container oci
# Mon, 09 Sep 2024 03:00:12 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 03:00:12 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 03:00:14 GMT
RUN rm -rf /var/log/*
# Mon, 09 Sep 2024 03:00:14 GMT
ADD file:176c74ab7f462b30313432d52b7c6f58fe2edd170551781a42448723c65e7f5f in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Mon, 09 Sep 2024 03:00:14 GMT
ADD file:6891f0d7036caee7d12991bdd35d9026311e2ed866921adfe8f47a7aea2c4bd3 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Mon, 09 Sep 2024 03:00:14 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Mon, 09 Sep 2024 03:00:16 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Mon, 09 Sep 2024 03:00:17 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 09 Sep 2024 03:00:19 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='58845ce4275f3ec74fba075597c8216bb201773da036c4703be8b7b7b457355d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64le)          ESUM='46cf93653e2b553fb1c91760cfe2ff20999ba358d648d2df69e5948784768440';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='7fb5b09987cb41de5118fecb5a81771b3a38a245cff411b39af33dbfbca3e760';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='d3affbb011ca6c722948f6345d15eba09bded33f9947d4d67e09723e2518c12a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:cd32d68ae8ad7b6fc852a3e507326fa79010c8e32d67f10b8ff3a556c8295726`  
		Last Modified: Tue, 10 Sep 2024 18:11:59 GMT  
		Size: 43.6 MB (43616552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f4590d8c9bbb50bc8088444f7f7e7079f5addeb0a5cef252098fea8c7b01d8`  
		Last Modified: Wed, 11 Sep 2024 00:26:02 GMT  
		Size: 30.3 MB (30261760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c36f3f524359c42203f38318bd26c4e90a9c856d769c85cc82ace060d91e1ee`  
		Last Modified: Wed, 11 Sep 2024 00:28:34 GMT  
		Size: 53.6 MB (53571432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9d907ae905d35caaef6bede354a34460a0e51ecd2dd0919111b1812ad2ef48`  
		Last Modified: Wed, 11 Sep 2024 00:28:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8839cbcb6eca90a6bd93e083ed3f57fa25af286f94999ead9670a74e9144468d`  
		Last Modified: Wed, 11 Sep 2024 00:28:25 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:270f9bad7b955011ed830247ebffb07bac5ef9e064012c1ea6f9ce5c9636cb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114834114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf2dba4988829cd7fa7c82c9b5cb00895f13fa785b1012a13f833ac14a19948`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 09 Sep 2024 03:00:03 GMT
ADD file:8d40c10f9f027f5f474f167499faeef6e3d6559f6ddc2ca95a8987fa9c0aaed9 in / 
# Mon, 09 Sep 2024 03:00:06 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 09 Sep 2024 03:00:06 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Mon, 09 Sep 2024 03:00:07 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Mon, 09 Sep 2024 03:00:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Sep 2024 03:00:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Mon, 09 Sep 2024 03:00:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Sep 2024 03:00:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Sep 2024 03:00:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Sep 2024 03:00:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Sep 2024 03:00:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Sep 2024 03:00:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Sep 2024 03:00:07 GMT
ENV container oci
# Mon, 09 Sep 2024 03:00:07 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 03:00:07 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 03:00:08 GMT
RUN rm -rf /var/log/*
# Mon, 09 Sep 2024 03:00:08 GMT
ADD file:538df4a720878d2d8af3716831813f400c0017437b26768453d9943abfd1cc3e in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Mon, 09 Sep 2024 03:00:08 GMT
ADD file:8aa8329cf2c2ef5c7579d955360b975dcec438ae1b3291b1267d91dafc715966 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Mon, 09 Sep 2024 03:00:08 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Mon, 09 Sep 2024 03:00:09 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Mon, 09 Sep 2024 03:00:11 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 09 Sep 2024 03:00:12 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='58845ce4275f3ec74fba075597c8216bb201773da036c4703be8b7b7b457355d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64le)          ESUM='46cf93653e2b553fb1c91760cfe2ff20999ba358d648d2df69e5948784768440';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='7fb5b09987cb41de5118fecb5a81771b3a38a245cff411b39af33dbfbca3e760';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='d3affbb011ca6c722948f6345d15eba09bded33f9947d4d67e09723e2518c12a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d5267c99eb044e958a4c01af00d35530b55934f8976717b26fca5beda78facfa`  
		Last Modified: Tue, 10 Sep 2024 18:12:04 GMT  
		Size: 37.4 MB (37365527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c74c5ce69a21b534518d260e68380bb5dcae359b4bada2aa9d4cc602fcaaef`  
		Last Modified: Wed, 11 Sep 2024 01:03:12 GMT  
		Size: 27.8 MB (27798222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ab5b7185aeb69e7d61e4496566bbf5433c23d1cfc0dcffdf7c247746e398d6`  
		Last Modified: Wed, 11 Sep 2024 01:04:37 GMT  
		Size: 49.7 MB (49668122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33f79ff50f308e92b4054809fbbb7a90b5ebc7485ef9d688379993801c2994a`  
		Last Modified: Wed, 11 Sep 2024 01:04:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3d0beae98cab9333b4cbd630ee31613676574bb18583ab1dbf08d9971d19d6`  
		Last Modified: Wed, 11 Sep 2024 01:04:30 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
