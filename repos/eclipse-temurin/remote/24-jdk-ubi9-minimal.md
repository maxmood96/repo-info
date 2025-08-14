## `eclipse-temurin:24-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:e1da9de27f336a6907d5bac976de4598817c4c26e600563cd10e3719f069b550
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

### `eclipse-temurin:24-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:c0c9a9b038d0540de84545f81b1f6ae8dc41ef33956038b39d784b1ce2ef4095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157166688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7a1c88e66efc7181de9ad548f3eb1c8034fd20f7fdcee8db7c687e7e9020eb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV container oci
# Fri, 01 Aug 2025 11:04:34 GMT
COPY dir:fed8131dab1a07775853004683d17f14115862719c3742630632a44de821b8a8 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL "build-date"="2025-08-07T16:38:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='6f8725d186d05c627176db9c46c732a6ef3ba41d9e9b3775c4727fc8ac642bb2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.2_12.tar.gz';          ;;        ppc64le)          ESUM='00f55805b4fa34c2557428e7f43ac847a8af0177ecb0b9dd8a6016f313ec43a9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.2_12.tar.gz';          ;;        s390x)          ESUM='555059f4929ab6435eb83b496d0b969bc6a9a5c07915d5f7607f5d833e38fb39';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='aea1cc55e51cf651c85f2f00ad021603fe269c4bb6493fa97a321ad770c9b096';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7ceb420857b3cf642e9e34e4e12ebf8ca5ed092e6c4b4f69ce4ed011e9e8140a`  
		Last Modified: Thu, 07 Aug 2025 18:09:52 GMT  
		Size: 39.7 MB (39651301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b2c7a464dc475bedca177ee9660130c801ed1e4ef17d360dbc64ed320c7978`  
		Last Modified: Wed, 13 Aug 2025 23:02:54 GMT  
		Size: 27.5 MB (27538753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9117d3a370d3824b5cb2d12d68566a4aef32e8ae2d3fde5d54cf957c27dd2225`  
		Last Modified: Wed, 13 Aug 2025 23:02:58 GMT  
		Size: 90.0 MB (89974214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33678ce9fdccb90189ea15640826826eabf7536270bf7434c0c977167951dce5`  
		Last Modified: Wed, 13 Aug 2025 23:02:39 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbb0c3b4f0700a403303e981019b4c1a3219b48a219894e9e3f6b1bce9af728`  
		Last Modified: Wed, 13 Aug 2025 23:02:18 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:586f613bbaad18837db1b9b05e5e88b1963cf2d30faab23a3893c3975a0e5003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2446710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533b316eeba47fe6da62b73988ed7c9e993af74a99b2d18f961e9f97389356fa`

```dockerfile
```

-	Layers:
	-	`sha256:03f263e5c0ffe29d6c54984dcc490d5dd845189fbc4bae114868199f3a013f4c`  
		Last Modified: Thu, 14 Aug 2025 00:15:54 GMT  
		Size: 2.4 MB (2425556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39b899a38ced5c76c6bcf542f0525701f01ccbcfceefaab5aae5a8621f665d25`  
		Last Modified: Thu, 14 Aug 2025 00:15:55 GMT  
		Size: 21.2 KB (21154 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:5c9df637e63796f5f4223cafad81c8a624c7b990dda2f8928a6b733635839a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154904694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:460e6cfb9a8e9416b57c0736001e11365425020e81026b2b19a18b96a55645c4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV container oci
# Fri, 01 Aug 2025 11:04:34 GMT
COPY dir:5da5b397cee17643fbcc12434bebce628a4ff854389d189d0166a1ebc5e815db in / 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL "build-date"="2025-08-07T16:43:31" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='6f8725d186d05c627176db9c46c732a6ef3ba41d9e9b3775c4727fc8ac642bb2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.2_12.tar.gz';          ;;        ppc64le)          ESUM='00f55805b4fa34c2557428e7f43ac847a8af0177ecb0b9dd8a6016f313ec43a9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.2_12.tar.gz';          ;;        s390x)          ESUM='555059f4929ab6435eb83b496d0b969bc6a9a5c07915d5f7607f5d833e38fb39';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='aea1cc55e51cf651c85f2f00ad021603fe269c4bb6493fa97a321ad770c9b096';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ae68ff313f78851fbf66137c0a49a327986447045fa7f2497adbc1b57f88db56`  
		Last Modified: Thu, 07 Aug 2025 18:09:51 GMT  
		Size: 37.8 MB (37819116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52d35c18e9a72456397f9eeedbd19f9dc8600f65f4d8fd5d96621d533551288`  
		Last Modified: Thu, 14 Aug 2025 09:09:50 GMT  
		Size: 28.0 MB (27982673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a8fd9c3c171be7a78f877127960709be9a144092671d125b3d489792bbf0ef`  
		Last Modified: Thu, 14 Aug 2025 12:18:25 GMT  
		Size: 89.1 MB (89100487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc34106ef39d655b3c4fe75cfcc8df8081ad7420210ba1b0e3b59ee1a48218b1`  
		Last Modified: Thu, 14 Aug 2025 09:18:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce507be0a8766094cef5c67ba51a60e3c68c1acdef29c5134defdba76cdec390`  
		Last Modified: Thu, 14 Aug 2025 09:18:34 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:af443bf79a6c2f66057b224840a8f876b52b9c10a883414ede24f2349c6cc767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2446195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f85648d0cb83d2658ace07b84f3e4e1a8592bc9c8bc364da40693e4e5390d80`

```dockerfile
```

-	Layers:
	-	`sha256:e92a9f3c3d8d52d06148e93768523dee1144569a8f83fc1e5ffe8e3540bb47c3`  
		Last Modified: Thu, 14 Aug 2025 12:16:03 GMT  
		Size: 2.4 MB (2424925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13924183952b175ef7b4df185e6628991d7836da68b88ce3fb097d1c7e6f3ff5`  
		Last Modified: Thu, 14 Aug 2025 12:16:04 GMT  
		Size: 21.3 KB (21270 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:7a9f158a6a5eeef80c37856235d72eb1887656d4792d374c33ca7b0f3b5a25e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163963569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db4debd2f3c458c37695b22992bef848340e99945c43f4b9e78b5420cc37281`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV container oci
# Fri, 01 Aug 2025 11:04:34 GMT
COPY dir:b1e34ea7a28362356126333145a3caa4ced0141e04688d16b04ab649c669f43c in / 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL "build-date"="2025-08-07T16:44:50" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='6f8725d186d05c627176db9c46c732a6ef3ba41d9e9b3775c4727fc8ac642bb2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.2_12.tar.gz';          ;;        ppc64le)          ESUM='00f55805b4fa34c2557428e7f43ac847a8af0177ecb0b9dd8a6016f313ec43a9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.2_12.tar.gz';          ;;        s390x)          ESUM='555059f4929ab6435eb83b496d0b969bc6a9a5c07915d5f7607f5d833e38fb39';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='aea1cc55e51cf651c85f2f00ad021603fe269c4bb6493fa97a321ad770c9b096';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:aba3f1acf76208b8b62efdeedca86eb113101be1a85516cf6b0aae00d20e9d93`  
		Last Modified: Thu, 07 Aug 2025 18:09:54 GMT  
		Size: 44.1 MB (44060283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b238a99b2c6469409aa73a74b213065b6dcf7ea4be7280b0870ff8e470e4ff5e`  
		Last Modified: Thu, 14 Aug 2025 04:46:37 GMT  
		Size: 30.0 MB (29975842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc9ce9f7a0a2b06539a9997916f66c7c6b402f12e18e276171db91cfaad10aa`  
		Last Modified: Thu, 14 Aug 2025 13:27:30 GMT  
		Size: 89.9 MB (89925021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad33e429989ca94a5787f3633c183833bb592883dfe36d53666ad3ab8cbd2e22`  
		Last Modified: Thu, 14 Aug 2025 05:03:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925450f2b74ee708af1fd434536b8de9f41a7250ef09b383a36f476b138fc2c6`  
		Last Modified: Thu, 14 Aug 2025 05:03:05 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:21aacc3b04accbaccdd3658f6e3b07ea11bb15a40d7763ed45ea465922515e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2446138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00bf582b7336cc2ba1bbdc7c578e9288fa2b230da15dd5eeaf032495194e8fe7`

```dockerfile
```

-	Layers:
	-	`sha256:4b156395a82bf5da9f3a356ee4cd415e47c414129b3af567fd00fa029efd40ef`  
		Last Modified: Thu, 14 Aug 2025 06:16:27 GMT  
		Size: 2.4 MB (2424948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:249c41966880fcadd7885148f6d8b21175ac98fd3d78a34f5798eddb83d464f4`  
		Last Modified: Thu, 14 Aug 2025 06:16:27 GMT  
		Size: 21.2 KB (21190 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:1e75a098ecf1b404fbe8ca4cbeda4f5448935dec9e4cc082bcf18fc7f0b288da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150547102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f08c7f2ec2f07ec42acc9dd763a410a01fdb34836c350ad305af8cab45b5e5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV container oci
# Fri, 01 Aug 2025 11:04:34 GMT
COPY dir:81aabc5a8685d8fef8565a119a36f85579c02d5407baf6eca1107100bb225623 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL "build-date"="2025-08-07T16:43:10" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='6f8725d186d05c627176db9c46c732a6ef3ba41d9e9b3775c4727fc8ac642bb2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.2_12.tar.gz';          ;;        ppc64le)          ESUM='00f55805b4fa34c2557428e7f43ac847a8af0177ecb0b9dd8a6016f313ec43a9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.2_12.tar.gz';          ;;        s390x)          ESUM='555059f4929ab6435eb83b496d0b969bc6a9a5c07915d5f7607f5d833e38fb39';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='aea1cc55e51cf651c85f2f00ad021603fe269c4bb6493fa97a321ad770c9b096';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9712950bf0e31a37c30913225021f463d7b22862e610e77091d25d700d4d3267`  
		Last Modified: Thu, 07 Aug 2025 18:09:51 GMT  
		Size: 37.7 MB (37742078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d75ef921e7de3e981a3faf28304d557974df7259d88d93abe80a3e9fdd66a0`  
		Last Modified: Thu, 14 Aug 2025 04:00:48 GMT  
		Size: 27.6 MB (27576245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2265656267968c56f6aa8133b196577e3b056d89baedc14e90bfd26c441e1471`  
		Last Modified: Thu, 14 Aug 2025 04:09:01 GMT  
		Size: 85.2 MB (85226359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64ef3435de4650f2b53735a28e627d22a54a7f96d460b0a53fce1c126208326`  
		Last Modified: Thu, 14 Aug 2025 04:44:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20088aa4215f997f1bd080489fdaccd66c355b5ec7c432b6d74feff4e7d9ca46`  
		Last Modified: Thu, 14 Aug 2025 04:44:10 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6743fc9443b597845d043616cd1cc1362d242c761328feb8eaa9eed3671ff8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2436651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e810f4e2cdc24ae0d64b1f5a87d51b18a2cb21a50d6920710ebf877d5085462b`

```dockerfile
```

-	Layers:
	-	`sha256:d566653b8fe7171182d643e441ddef80227e98547ac8577311658a86c0407e48`  
		Last Modified: Thu, 14 Aug 2025 06:16:31 GMT  
		Size: 2.4 MB (2415498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d3e37b5b637cbd348d219d92364b3c8d6d4feeba12ff7907d18c33a98df654a`  
		Last Modified: Thu, 14 Aug 2025 06:16:32 GMT  
		Size: 21.2 KB (21153 bytes)  
		MIME: application/vnd.in-toto+json
