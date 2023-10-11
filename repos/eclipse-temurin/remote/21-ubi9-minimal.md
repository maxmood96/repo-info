## `eclipse-temurin:21-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:f7cbe61b9dfd76b75cf3ccfee129ebcc89358e98ae2419ae1166b7088bdee466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `eclipse-temurin:21-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:7f5b8c2a47b313140ffc671a7231d920942106e5f51996670ca075fab7038e98
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.3 MB (224304512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b276a1eb7e83f463abc417dcdea5bfb2e692ef1cd1c0f6a297a039f3d3ba3541`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 05 Oct 2023 14:38:57 GMT
ADD file:2ff77282831ead8e1be2de9fcd07643f64492c64c71ed11f341e24f7332bd2a2 in / 
# Thu, 05 Oct 2023 14:38:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 05 Oct 2023 14:38:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 05 Oct 2023 14:38:58 GMT
ADD multi:983c894e8a29f7d84811b8480f8cb94a942803f65be70fbae4914c9f2a20c5e7 in /etc/yum.repos.d/ 
# Thu, 05 Oct 2023 14:38:58 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Oct 2023 14:38:58 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Thu, 05 Oct 2023 14:38:58 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Oct 2023 14:38:58 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Oct 2023 14:38:58 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Oct 2023 14:38:58 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Oct 2023 14:38:58 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Oct 2023 14:38:58 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Oct 2023 14:38:58 GMT
ENV container oci
# Thu, 05 Oct 2023 14:38:58 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 14:38:58 GMT
CMD ["/bin/bash"]
# Thu, 05 Oct 2023 14:38:58 GMT
RUN rm -rf /var/log/*
# Thu, 05 Oct 2023 14:38:58 GMT
ADD file:d69168032ac0af2ccddca7f0231c9160dfbc90a3f409177789bef1a6f93385f4 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-750.1696515534.json 
# Thu, 05 Oct 2023 14:38:59 GMT
ADD file:8f0d5eacbb4a0d1c410cd94f86add6634846747273665c2ed843c128a3143840 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-750.1696515534 
# Thu, 05 Oct 2023 14:38:59 GMT
LABEL "release"="750.1696515534" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-05T14:27:14" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-750.1696515534"
# Thu, 05 Oct 2023 14:38:59 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2414592-d4ca5.repo' '/etc/yum.repos.d/gitweb-a7836.repo'
# Thu, 05 Oct 2023 14:39:00 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 05 Oct 2023 14:39:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 10 Oct 2023 23:49:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 10 Oct 2023 23:49:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 23:49:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 10 Oct 2023 23:49:26 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Wed, 11 Oct 2023 18:09:55 GMT
ENV JAVA_VERSION=jdk-21+35
# Wed, 11 Oct 2023 18:10:03 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='33e440c237438aa2e3866d84ead8d4e00dc0992d98d9fd0ee2fe48192f2dbc4b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jdk_aarch64_linux_hotspot_21_35.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='82f64c53acaa045370d6762ebd7441b74e6fda14b464d54d1ff8ca941ec069e6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jdk_x64_linux_hotspot_21_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 11 Oct 2023 18:10:05 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 11 Oct 2023 18:10:05 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Wed, 11 Oct 2023 18:10:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Oct 2023 18:10:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:516f7562f02267e05bc0f8b175363c70768471b977360d0f0ab5711a8a6d25ab`  
		Last Modified: Mon, 09 Oct 2023 09:57:09 GMT  
		Size: 37.8 MB (37848606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ef34923412e703897363f1815dcc18d27c28eeafb818489cc210e1bb161c24`  
		Last Modified: Tue, 10 Oct 2023 23:52:57 GMT  
		Size: 27.9 MB (27858409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fcc74fbbd1d374b9aa83456da3562c496bf399dc1100a60518bd4fdbfaf0dce`  
		Last Modified: Wed, 11 Oct 2023 18:13:33 GMT  
		Size: 158.6 MB (158596609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec68d230400edece8724f1b15ee97edb6807cbdbcc0c49740f4a04c28e4930f0`  
		Last Modified: Wed, 11 Oct 2023 18:13:20 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e056f64f29247273642b62deb309e7d52b6d1abcb608532421c2ab3f46ba82`  
		Last Modified: Wed, 11 Oct 2023 18:13:20 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:6c74a7d3bade95d0dfbcb1b90a1b045a576692585b5c2971a0711a8c87fcece6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.3 MB (221268154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb081429bf8708a375c425b08db7f3b856d6729281bc7681aee568830322adfd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 05 Oct 2023 14:38:54 GMT
ADD file:7a7d8fbf25992fd7276405ef49134834de1383be75681df1b04b4bcea089f511 in / 
# Thu, 05 Oct 2023 14:38:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 05 Oct 2023 14:38:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 05 Oct 2023 14:38:56 GMT
ADD multi:983c894e8a29f7d84811b8480f8cb94a942803f65be70fbae4914c9f2a20c5e7 in /etc/yum.repos.d/ 
# Thu, 05 Oct 2023 14:38:56 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Oct 2023 14:38:56 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Thu, 05 Oct 2023 14:38:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Oct 2023 14:38:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Oct 2023 14:38:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Oct 2023 14:38:56 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Oct 2023 14:38:56 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Oct 2023 14:38:56 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Oct 2023 14:38:56 GMT
ENV container oci
# Thu, 05 Oct 2023 14:38:56 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 14:38:56 GMT
CMD ["/bin/bash"]
# Thu, 05 Oct 2023 14:38:57 GMT
RUN rm -rf /var/log/*
# Thu, 05 Oct 2023 14:38:57 GMT
ADD file:94efb4b1ab694ac83e1684e40584630e5704b83a70e136a93ecb2f97d83b276f in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-750.1696515534.json 
# Thu, 05 Oct 2023 14:38:57 GMT
ADD file:5465d3cdb7730b7414c1833b9e5b836537236bbd6286f2bc7d43b9d5a125ab84 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-750.1696515534 
# Thu, 05 Oct 2023 14:38:57 GMT
LABEL "release"="750.1696515534" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-05T14:27:14" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-750.1696515534"
# Thu, 05 Oct 2023 14:38:58 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2414592-d4ca5.repo' '/etc/yum.repos.d/gitweb-a7836.repo'
# Thu, 05 Oct 2023 14:38:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 05 Oct 2023 14:39:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 10 Oct 2023 23:50:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 10 Oct 2023 23:50:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 23:50:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 10 Oct 2023 23:51:02 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Wed, 11 Oct 2023 17:34:41 GMT
ENV JAVA_VERSION=jdk-21+35
# Wed, 11 Oct 2023 17:34:49 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='33e440c237438aa2e3866d84ead8d4e00dc0992d98d9fd0ee2fe48192f2dbc4b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jdk_aarch64_linux_hotspot_21_35.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='82f64c53acaa045370d6762ebd7441b74e6fda14b464d54d1ff8ca941ec069e6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jdk_x64_linux_hotspot_21_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 11 Oct 2023 17:34:53 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 11 Oct 2023 17:34:53 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Wed, 11 Oct 2023 17:34:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Oct 2023 17:34:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4d01da1f57912d023cd75f254ad72c2683a95673c84d2dbd6a594fa4051e23c1`  
		Last Modified: Mon, 09 Oct 2023 12:07:27 GMT  
		Size: 36.1 MB (36134632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcc7cef3ec071bb58b1d161769efc4edc00bc85348312499035de02c7175867`  
		Last Modified: Tue, 10 Oct 2023 23:53:49 GMT  
		Size: 28.3 MB (28284554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9ab5c22c30c552435aba38d3e876f02ab16b05951e0c6c2cc9121295c04034`  
		Last Modified: Wed, 11 Oct 2023 17:37:53 GMT  
		Size: 156.8 MB (156848081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73ec87fd2c9bf7f8bf5459162d6df90f3d4c42aca973955f99b4c43c0ac7175`  
		Last Modified: Wed, 11 Oct 2023 17:37:42 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd9a027a0e7189c1f1d75f3e305ed20b80f23b7eb94443326d00cd7a7f00fca`  
		Last Modified: Wed, 11 Oct 2023 17:37:42 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
