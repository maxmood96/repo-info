## `eclipse-temurin:24-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:c191c8868f4eba7b58a399eff548d360260912c5299f1d323c190f5736d1b562
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
$ docker pull eclipse-temurin@sha256:01f02dfc94810b4615722c2763dab1f8d4086af5a1e48d13cbfd1c3281e14b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157164292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e14378b3f058badfc87cda73d126dc6fccb1e26fc57535646042fc5387932c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Apr 2025 14:48:05 GMT
ENV container oci
# Wed, 23 Apr 2025 14:48:05 GMT
COPY dir:763be6363f3253ea0e05459116de22ba38b02ee7990e3e17aa7c2682d7098cf0 in /    
# Wed, 23 Apr 2025 14:48:05 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL "build-date"="2025-07-09T14:05:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='a598260e340028d9b2383c23df16aa286769a661bd3bf28a52e8c1a5774b1110';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.1_9.tar.gz';          ;;        ppc64le)          ESUM='770e7e506d5ea3baf6c4c9004a82648e29508a1c731d8425acded34906e91b09';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.1_9.tar.gz';          ;;        s390x)          ESUM='6ff3126ae0a7cff3a25b7590adc441550666750515fd7d6e2d2706b5fc9a1f6f';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.1_9.tar.gz';          ;;        x86_64)          ESUM='78832cb5ea4074f2215cde0d01d6192d09c87636fc24b36647aea61fb23b8272';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4aebf8512d837638f2ec264e09f9e51206cfe9dfbeea1dadda474ea4e2e32dc2`  
		Last Modified: Wed, 09 Jul 2025 15:41:38 GMT  
		Size: 39.7 MB (39656780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3017ba0b6f3f35fd2beffba993b70e32511eacc4ee97e6e189b51f945e9563a2`  
		Last Modified: Fri, 11 Jul 2025 23:33:58 GMT  
		Size: 27.5 MB (27545742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87d411b2ee41f011fb315e0885928bf14da795bd0d0c74f69a942bff1c24ee1`  
		Last Modified: Fri, 11 Jul 2025 23:34:12 GMT  
		Size: 90.0 MB (89959351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553ec707a04d9a942ba6fc32ca03d441cf79a30710daad64a43bf26d1cd482bb`  
		Last Modified: Fri, 11 Jul 2025 23:33:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a2b31fd367db8f1691001275d185dc22b24c88ae0290c166f528efb44328a2`  
		Last Modified: Fri, 11 Jul 2025 23:33:42 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:cc66467d03f14b52183be761a9f82d40d78f598ee5ff29cf0e82a788c23ab04f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2446626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e56a1756a17def5c5be7ae3531d6a70126770f277c466f954f00e334f019d96`

```dockerfile
```

-	Layers:
	-	`sha256:5f78e525e52ba2ee62d3c4e92ebdd07976dd546e7d653cf890517b6bdc6a9efd`  
		Last Modified: Sat, 12 Jul 2025 00:15:50 GMT  
		Size: 2.4 MB (2425496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e34a1c76ea063c75bb33335306289e202dd01743a2ab6265b645e342b757e13`  
		Last Modified: Sat, 12 Jul 2025 00:15:51 GMT  
		Size: 21.1 KB (21130 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:6ff914e4e5055b96ec762bb58ce9c34e4ed641bd617a96f20bce586b2c862e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154946151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a1da54e29689ca60cdd797df65b245b47702913bc8fe13fabeec408667923b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Apr 2025 14:48:05 GMT
ENV container oci
# Wed, 23 Apr 2025 14:48:05 GMT
COPY dir:b783331d27fd913eeb2432850fad52ee030371aaa92d5026fe285216c5bf07a4 in /    
# Wed, 23 Apr 2025 14:48:05 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json    
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL "build-date"="2025-07-09T14:10:01" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='a598260e340028d9b2383c23df16aa286769a661bd3bf28a52e8c1a5774b1110';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.1_9.tar.gz';          ;;        ppc64le)          ESUM='770e7e506d5ea3baf6c4c9004a82648e29508a1c731d8425acded34906e91b09';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.1_9.tar.gz';          ;;        s390x)          ESUM='6ff3126ae0a7cff3a25b7590adc441550666750515fd7d6e2d2706b5fc9a1f6f';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.1_9.tar.gz';          ;;        x86_64)          ESUM='78832cb5ea4074f2215cde0d01d6192d09c87636fc24b36647aea61fb23b8272';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:20903621eaed1da24bbd033a1782d897d15ed92cf3430cd60e3ec0cda4a1bb69`  
		Last Modified: Thu, 10 Jul 2025 01:38:24 GMT  
		Size: 37.9 MB (37863034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f616163d50a0cbf3a1601df8ccedc3236bfc89127db1cc57876f59772411e7`  
		Last Modified: Fri, 11 Jul 2025 23:39:32 GMT  
		Size: 28.0 MB (27987767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5425cb38070d49d0f8112f914e1768102bd4e48285a9b7f2839be063d7a1ce05`  
		Last Modified: Fri, 11 Jul 2025 23:43:23 GMT  
		Size: 89.1 MB (89092930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d489ef0fabcc6edc39765186cb59add5acc83d22c1ee3c67415c028c7cfdc2b`  
		Last Modified: Fri, 11 Jul 2025 23:43:20 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae1e3def79f803b0a781368afc1a47715e3b9d538a06aa31eec1b7cf3f6fa08`  
		Last Modified: Fri, 11 Jul 2025 23:43:20 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:05696ae3825bb3527bf6f5b670d130d7dee1eac5a727d173859807db80853e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2446111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85712b95abf19eeff5eeaaa7feb5db6b0d47a721db6f5cb3af02e2f0697f73bd`

```dockerfile
```

-	Layers:
	-	`sha256:5dbc6bc1d86f4936c576021022481ccdc4d9aae29b74556c48ca869996e9f584`  
		Last Modified: Sat, 12 Jul 2025 00:15:55 GMT  
		Size: 2.4 MB (2424865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:014d332d60ec701e89fcb8d24f74e0348afdb56fb5dbda3a672202f12a998383`  
		Last Modified: Sat, 12 Jul 2025 00:15:56 GMT  
		Size: 21.2 KB (21246 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:f7de9c636ec34dd2d2359d0ad5e132919fc3ccb9c15cbb2ccc0337c4181fde2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.9 MB (163927014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06448434e4e3c2e63f5042c13bcbce13f6c914f45b45578ce932117493939cd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Apr 2025 14:48:05 GMT
ENV container oci
# Wed, 23 Apr 2025 14:48:05 GMT
COPY dir:73930ed21f69466bc4b38ffc8263e56640090f18dc00dc206ddc704b5b9f1ca0 in /    
# Wed, 23 Apr 2025 14:48:05 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json    
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL "build-date"="2025-07-09T14:35:36" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='a598260e340028d9b2383c23df16aa286769a661bd3bf28a52e8c1a5774b1110';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.1_9.tar.gz';          ;;        ppc64le)          ESUM='770e7e506d5ea3baf6c4c9004a82648e29508a1c731d8425acded34906e91b09';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.1_9.tar.gz';          ;;        s390x)          ESUM='6ff3126ae0a7cff3a25b7590adc441550666750515fd7d6e2d2706b5fc9a1f6f';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.1_9.tar.gz';          ;;        x86_64)          ESUM='78832cb5ea4074f2215cde0d01d6192d09c87636fc24b36647aea61fb23b8272';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8ca48092d0e85ccf7e1d265436c83d1bf5ecbe3d844259987ae6b1612d5b9d28`  
		Last Modified: Thu, 10 Jul 2025 09:40:32 GMT  
		Size: 44.0 MB (44022415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a35efa0cbfd7ed6dd2d014d4e50676fd66853f250fe119d4d3eae79827a21f3`  
		Last Modified: Fri, 11 Jul 2025 23:42:45 GMT  
		Size: 30.0 MB (29979021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d74a5b7b04ec48a18791e81a7cbbfab64b576ae54d542cf7f4a82f237dba09`  
		Last Modified: Fri, 11 Jul 2025 23:50:55 GMT  
		Size: 89.9 MB (89923156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4ec4347b748003de5c3a2522e151f11623ddec0f325b2a0987a1fa8dae1c14`  
		Last Modified: Fri, 11 Jul 2025 23:50:51 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b05cf459ebb15b7dea1e85c7ce4dfc7eb292f248c348eb94d1c845b2a65e02`  
		Last Modified: Fri, 11 Jul 2025 23:50:52 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:bfccc0049d81fea78d38a159938c9dd1fc40463b64ae84c3613896336682201f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2446054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c305f68175b7875bcbefc7bbd150be4955812a803f51fbce5801faac326a1a88`

```dockerfile
```

-	Layers:
	-	`sha256:8718a7f21ad8650df626d722b325e000d38e88be6bef9468bb57ebc1203afc12`  
		Last Modified: Sat, 12 Jul 2025 00:16:00 GMT  
		Size: 2.4 MB (2424888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:294b300eb50380135ba20d2780854be29d999da923f6a179fa723da86912e712`  
		Last Modified: Sat, 12 Jul 2025 00:16:01 GMT  
		Size: 21.2 KB (21166 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:166d76be5a8be518c47a325f3b51812b488eb302da48942a4ea1e8a6447c8b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150577145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa057ad96a792e6919d808ea04701181524b58b139a3905e9862f141c6f7bd6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Apr 2025 14:48:05 GMT
ENV container oci
# Wed, 23 Apr 2025 14:48:05 GMT
COPY dir:7a55d588abc8a7ab3c25b97f3e41f6a707e103b1e1d190f3d2fc8d1f6804943a in /    
# Wed, 23 Apr 2025 14:48:05 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json    
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL "build-date"="2025-07-09T14:33:44" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='a598260e340028d9b2383c23df16aa286769a661bd3bf28a52e8c1a5774b1110';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.1_9.tar.gz';          ;;        ppc64le)          ESUM='770e7e506d5ea3baf6c4c9004a82648e29508a1c731d8425acded34906e91b09';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.1_9.tar.gz';          ;;        s390x)          ESUM='6ff3126ae0a7cff3a25b7590adc441550666750515fd7d6e2d2706b5fc9a1f6f';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.1_9.tar.gz';          ;;        x86_64)          ESUM='78832cb5ea4074f2215cde0d01d6192d09c87636fc24b36647aea61fb23b8272';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ef5ee291b5d063ed0be6e8e0f09a68e18065cf86e2cdd050c5d84d6226b78d7`  
		Last Modified: Thu, 10 Jul 2025 09:40:30 GMT  
		Size: 37.8 MB (37769032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1916ef801b87d97a6cb82e4aa522fb7c1bc9dbc82f3166178a0eb35e78689e`  
		Last Modified: Fri, 11 Jul 2025 23:34:01 GMT  
		Size: 27.6 MB (27586146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76125d1dd12f72b9933f4705622b2567a79b5a63f0cceaca22c9adce8f7cf28`  
		Last Modified: Fri, 11 Jul 2025 23:38:10 GMT  
		Size: 85.2 MB (85219546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58a6bf32ab0787f10e0a2a42585100e3abbced3f518490ab97579d6fdb5d05e`  
		Last Modified: Fri, 11 Jul 2025 23:38:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7384f0316c0b8b0d23ebf75168865bcaabc519b79a5d638ce8bdf2b43ac412`  
		Last Modified: Fri, 11 Jul 2025 23:38:05 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:09ca362a3863b319399521c3feb0d5e947cc82f190def9e3175688d48fe41b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2436568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e775b7a0589f19b343c99eee2a40d9a2a74254fe7d6f79e8cec89be17adc9398`

```dockerfile
```

-	Layers:
	-	`sha256:47fd95282c9d39bea1c8b90775b031130af7e0c42ad883599138323066f8df60`  
		Last Modified: Sat, 12 Jul 2025 00:16:05 GMT  
		Size: 2.4 MB (2415438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b18ce01b05c616e40c7ab151bb1457dc9132a666513830f6fd50e1ca92dae26`  
		Last Modified: Sat, 12 Jul 2025 00:16:06 GMT  
		Size: 21.1 KB (21130 bytes)  
		MIME: application/vnd.in-toto+json
