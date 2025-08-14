## `eclipse-temurin:24-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:9d5c05166792c90804e3ae87666b571635c448c634ed7e79be1d6e26c15a0ea8
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

### `eclipse-temurin:24-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:df2c2b34192d0fc918a5d960bf1a90a59f6aff47c6fc68421e17294b3159362c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (128030592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a458d861964d34732d4c8c27d6f3810b009051901713170a833344b3f429f2f3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='6b06ed1d91930ef86afc7d2159948aa9b3054b154cd8afda35d1fddd158fc11d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_aarch64_linux_hotspot_24.0.2_12.tar.gz';          ;;        ppc64le)          ESUM='de9ec7034fb369ec9b5d12bba9d51984d14d859006e89ef2b86bbae9bc4c7ae4';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_ppc64le_linux_hotspot_24.0.2_12.tar.gz';          ;;        s390x)          ESUM='b25ab757f131f965195fd2cb63853299ed6bef268c845283a5a9fff562840fe2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_s390x_linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='bee902852ae8b6698e04eb1599dc94af844ae45b72b3b8ec854350b9aba41335';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_x64_linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:7ceb420857b3cf642e9e34e4e12ebf8ca5ed092e6c4b4f69ce4ed011e9e8140a`  
		Last Modified: Thu, 07 Aug 2025 18:09:52 GMT  
		Size: 39.7 MB (39651301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fdc2da5d024b8f8abe56f04e74640d84789b632e4bc998e3e86013aa400e377`  
		Last Modified: Wed, 13 Aug 2025 23:02:36 GMT  
		Size: 27.5 MB (27538721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df587dec0b48c4e4bede11151969e0f124d0e9ddbdcf85e3990803c8c0e40477`  
		Last Modified: Wed, 13 Aug 2025 23:02:38 GMT  
		Size: 60.8 MB (60838152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed95d5cddd2f0c0cc680f5132ba2ddc9d36d733ab83e06f813f97be2b3aa1c9`  
		Last Modified: Wed, 13 Aug 2025 23:02:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23051ee53c86bccfc724a3af3bf3570c36835241a35276ae2a06a68333c21fa2`  
		Last Modified: Wed, 13 Aug 2025 23:02:34 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2d46b802c005ec4dc8af549384680eca883a233072a640e844cfcf639f00e1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2420071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba9a1c05b792fb54eefaa15db657e15d41dfe3048f284330f661c216ee86a6b`

```dockerfile
```

-	Layers:
	-	`sha256:d540425c8f9a33a1398f5d0c48b953179fb9647c83baa99fd69b30c45ec90b27`  
		Last Modified: Thu, 14 Aug 2025 00:16:13 GMT  
		Size: 2.4 MB (2399872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bb9cf82d04b5e7b0ac7e4be56e3b0528fa6098e3ed7afedb083e6993111d635`  
		Last Modified: Thu, 14 Aug 2025 00:16:14 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:a2bab2ee7f372fdf7354d3379f6f2047851d52938d19d1a38f75848a0ab308e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125686900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d17ff6abeee38854b0e9c8c9ed62ac0fa136bec9d29bdbed587a6cc775f2fc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='6b06ed1d91930ef86afc7d2159948aa9b3054b154cd8afda35d1fddd158fc11d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_aarch64_linux_hotspot_24.0.2_12.tar.gz';          ;;        ppc64le)          ESUM='de9ec7034fb369ec9b5d12bba9d51984d14d859006e89ef2b86bbae9bc4c7ae4';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_ppc64le_linux_hotspot_24.0.2_12.tar.gz';          ;;        s390x)          ESUM='b25ab757f131f965195fd2cb63853299ed6bef268c845283a5a9fff562840fe2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_s390x_linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='bee902852ae8b6698e04eb1599dc94af844ae45b72b3b8ec854350b9aba41335';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_x64_linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:3bc0934ee390151f00a863b653239d67a4198b02432e2e28dc92dbdadbb22d38`  
		Last Modified: Thu, 14 Aug 2025 09:18:41 GMT  
		Size: 59.9 MB (59882692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8993901443dfb831013391aa3c093583d6bd8bb490e09c99ca390e7d492d0808`  
		Last Modified: Thu, 14 Aug 2025 10:10:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03479aa096c82bc0b3747c9ede23d4a96c56070b23d8b421e7f53b393a3a09d7`  
		Last Modified: Thu, 14 Aug 2025 10:10:23 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a63460de766b4d7b3e86597456d5bd84f410e7c730611f7015642c313110f6fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2419532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ca00fe5f3f124d46cf3f5af25a44e8f5cf1101965031686b97098fb88afe1d`

```dockerfile
```

-	Layers:
	-	`sha256:1d9b36d52f21dd580a6da03c533c631d55b94b7fda76cf1c78e7c8fdbb9f10a1`  
		Last Modified: Thu, 14 Aug 2025 12:16:21 GMT  
		Size: 2.4 MB (2399229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a8de9abe6f6b503ec674d8a740c9ae615db69d148eb6b48b29c9c8b653b91a8`  
		Last Modified: Thu, 14 Aug 2025 12:16:22 GMT  
		Size: 20.3 KB (20303 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:d54101479fb9239abdf112f393668d58711574f4033004ae26272b584591e7db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134696142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2b60c8d866c6160f3ae85c0ab8c23ed0608f3f476a6851b7bc48ac80fe70cb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='6b06ed1d91930ef86afc7d2159948aa9b3054b154cd8afda35d1fddd158fc11d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_aarch64_linux_hotspot_24.0.2_12.tar.gz';          ;;        ppc64le)          ESUM='de9ec7034fb369ec9b5d12bba9d51984d14d859006e89ef2b86bbae9bc4c7ae4';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_ppc64le_linux_hotspot_24.0.2_12.tar.gz';          ;;        s390x)          ESUM='b25ab757f131f965195fd2cb63853299ed6bef268c845283a5a9fff562840fe2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_s390x_linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='bee902852ae8b6698e04eb1599dc94af844ae45b72b3b8ec854350b9aba41335';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_x64_linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:f281ca0681ae98954af71b713276274e15bff61fd8b7fef5b5092b858fb39da8`  
		Last Modified: Thu, 14 Aug 2025 05:05:16 GMT  
		Size: 60.7 MB (60657601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf127d6e5f6071441bcb41ee1c60c2b9e03ce01f1070f968a5a6f0a929a971d0`  
		Last Modified: Thu, 14 Aug 2025 05:05:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfe9aaba6fa37f9909041ac1b551adaeecd8b226fbb20eab3fd76ee5641de96`  
		Last Modified: Thu, 14 Aug 2025 05:05:04 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:74475f23fa04c53009f168e4f645b9b7eeb7b33cfcd08291a5d7ba0de3f4a602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2419487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e9761e019d7b6162a187d5e7a3061faa4122704f921334dc2900ccf89fd856`

```dockerfile
```

-	Layers:
	-	`sha256:f1b6527d1cc0ebf305b4b5faa7076242ff367c869dadb0633774087451059e57`  
		Last Modified: Thu, 14 Aug 2025 06:16:44 GMT  
		Size: 2.4 MB (2399258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c828b7eecf76f3f5ec2edecb92206ebcb2e708be2bf756ce95e8720e0e357566`  
		Last Modified: Thu, 14 Aug 2025 06:16:45 GMT  
		Size: 20.2 KB (20229 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:44e6c182e3828eb95c7f28ff361aee0343b5c06606c2f8ee2523be12d0e2bb35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122928782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ede8cc2c6e824dcbd18183388df0b24fdf9339410c236589e88ea12a7d9ed2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='6b06ed1d91930ef86afc7d2159948aa9b3054b154cd8afda35d1fddd158fc11d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_aarch64_linux_hotspot_24.0.2_12.tar.gz';          ;;        ppc64le)          ESUM='de9ec7034fb369ec9b5d12bba9d51984d14d859006e89ef2b86bbae9bc4c7ae4';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_ppc64le_linux_hotspot_24.0.2_12.tar.gz';          ;;        s390x)          ESUM='b25ab757f131f965195fd2cb63853299ed6bef268c845283a5a9fff562840fe2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_s390x_linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='bee902852ae8b6698e04eb1599dc94af844ae45b72b3b8ec854350b9aba41335';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jre_x64_linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:283a003d317fe289596cce0f3d5d827e6b1bd1b3b531dd0b6ef556355ce0c240`  
		Last Modified: Thu, 14 Aug 2025 04:10:42 GMT  
		Size: 57.6 MB (57608041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f237a7cab7b4619da0de79d1c6a35dc7c8d80642b7756193170b6e4ed7d40397`  
		Last Modified: Thu, 14 Aug 2025 04:10:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f91c82bbac64f42cfee4c6ed9e632dfcad95262fbc7985be8079d06dcafb69d`  
		Last Modified: Thu, 14 Aug 2025 04:10:39 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3353b13fadf3dfb739d20182afaa67420ca7e456eadd5e0bc1fb35fc607bf810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2411244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5aa64a02543f1ecb94673082a17c74c173bf8d19382e8233e4c84084c58d0f1`

```dockerfile
```

-	Layers:
	-	`sha256:6bbd72e09f9b981af2a0f0756c10eef86b76a4d5564e2001a7d770ea076a954a`  
		Last Modified: Thu, 14 Aug 2025 06:16:48 GMT  
		Size: 2.4 MB (2391045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a467365ecbea00af111a92ed2eb511383fbdac755ad6cd65e289e9e87bfe42`  
		Last Modified: Thu, 14 Aug 2025 06:16:49 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json
