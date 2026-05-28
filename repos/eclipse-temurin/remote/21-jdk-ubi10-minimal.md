## `eclipse-temurin:21-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:6909199cb09cd7a669dbcafb6505a6d99bfbd593c491b205d8caf8a42e9f54bd
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

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:3b9b5d9e46811fb61b8ab378c6e2ed639c4d26e5e8e5cec6be4ac1426c9049a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230827313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d67ab012ae420218434355594a70c05fd1e6ca0d521b86abfb9400941d1969`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 27 May 2026 06:12:12 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 May 2026 06:12:12 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 27 May 2026 06:12:12 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 27 May 2026 06:12:12 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 27 May 2026 06:12:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 May 2026 06:12:12 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 27 May 2026 06:12:12 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:12:12 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:12:12 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 27 May 2026 06:12:12 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 May 2026 06:12:12 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 27 May 2026 06:12:12 GMT
ENV container oci
# Wed, 27 May 2026 06:12:12 GMT
COPY dir:8cc023cf96d9d3899063545e0c3b25ee410727bc8ef5903cc1b3e3e22d98dc1f in /      
# Wed, 27 May 2026 06:12:13 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 27 May 2026 06:12:13 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 06:12:13 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 27 May 2026 06:12:13 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 27 May 2026 06:12:13 GMT
COPY file:919ce0635818e127299907aac3d5ec8b04328702d69e0d804c99d87a631c2e20 in /usr/share/buildinfo/labels.json      
# Wed, 27 May 2026 06:12:13 GMT
COPY file:919ce0635818e127299907aac3d5ec8b04328702d69e0d804c99d87a631c2e20 in /root/buildinfo/labels.json      
# Wed, 27 May 2026 06:12:13 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "org.opencontainers.image.revision"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "build-date"="2026-05-27T06:11:58Z" "org.opencontainers.image.created"="2026-05-27T06:11:58Z" "release"="1779862102"org.opencontainers.image.revision=3aa29655e860e8f28ee9014c3803f132b3b1e65d,org.opencontainers.image.created=2026-05-27T06:11:58Z
# Wed, 27 May 2026 22:37:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 May 2026 22:37:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 22:37:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 May 2026 22:37:20 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 27 May 2026 22:37:20 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Wed, 27 May 2026 22:37:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 27 May 2026 22:37:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 May 2026 22:37:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 May 2026 22:37:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 27 May 2026 22:37:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8b457fb1b26320aa35da6d429ea0efa5a81d9f904a24a8d0a4e1a1efcfd0e7b8`  
		Last Modified: Wed, 27 May 2026 07:33:17 GMT  
		Size: 34.9 MB (34902395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4388b8624524602d05952be02a0130f99ee994082bada674d1a753650cdb49`  
		Last Modified: Wed, 27 May 2026 22:37:48 GMT  
		Size: 37.7 MB (37749799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cfe212629b52054a95fca509000c57be8e5e060d56f32eaa37327e3c84b2f6`  
		Last Modified: Wed, 27 May 2026 22:37:51 GMT  
		Size: 158.2 MB (158172699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a7381c9be19ff2b8b026307de53a4a3b5cae8b566050cef45853f76fd1c75a`  
		Last Modified: Wed, 27 May 2026 22:37:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a206aa3812d97ee8323c48268b57b0c6f45dbd2154f829d0814fec9cfc41e029`  
		Last Modified: Wed, 27 May 2026 22:37:46 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9ac1ac387af9519de50bb122fdd7b6f5186e54159158c3363efc155773c5fe81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3815530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e02d7033322cedab753750842e43c91101ccc93303afad1950dbdcc930fdd0`

```dockerfile
```

-	Layers:
	-	`sha256:286b214a00b471035f6b2799af9cdd9aa70ec151cc383b61237805b9d9085118`  
		Last Modified: Wed, 27 May 2026 22:37:46 GMT  
		Size: 3.8 MB (3794191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f009112cb7302e84b59a917f09c476653a7132e2e55d6a9d72965e140d4b1162`  
		Last Modified: Wed, 27 May 2026 22:37:46 GMT  
		Size: 21.3 KB (21339 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:ca9ca7c86efa4e9c00f12003cea1d358b9ad6cb1826e5fd31e110dda8d4d34c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227210113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6075bf0436812a4afac2f92dbe88aaf6df95b998579909b146c818d5ce0def6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 27 May 2026 06:14:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 May 2026 06:14:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 27 May 2026 06:14:32 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 27 May 2026 06:14:32 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 27 May 2026 06:14:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 May 2026 06:14:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 27 May 2026 06:14:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:14:32 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:14:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 27 May 2026 06:14:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 May 2026 06:14:32 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 27 May 2026 06:14:32 GMT
ENV container oci
# Wed, 27 May 2026 06:14:33 GMT
COPY dir:144798cc4c14efe6d25c10c7a6f149af1045784afd86a94e99d04f534f9bbb05 in /      
# Wed, 27 May 2026 06:14:33 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 27 May 2026 06:14:33 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 06:14:33 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 27 May 2026 06:14:33 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 27 May 2026 06:14:33 GMT
COPY file:83615dc098d46f372c6688f68025f354351bfbb3ed132d56c889042d90463ecf in /usr/share/buildinfo/labels.json      
# Wed, 27 May 2026 06:14:34 GMT
COPY file:83615dc098d46f372c6688f68025f354351bfbb3ed132d56c889042d90463ecf in /root/buildinfo/labels.json      
# Wed, 27 May 2026 06:14:34 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "org.opencontainers.image.revision"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "build-date"="2026-05-27T06:14:17Z" "org.opencontainers.image.created"="2026-05-27T06:14:17Z" "release"="1779862102"org.opencontainers.image.revision=3aa29655e860e8f28ee9014c3803f132b3b1e65d,org.opencontainers.image.created=2026-05-27T06:14:17Z
# Wed, 27 May 2026 22:37:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 May 2026 22:37:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 22:37:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 May 2026 22:37:37 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 27 May 2026 22:37:37 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Wed, 27 May 2026 22:37:44 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 27 May 2026 22:37:45 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 May 2026 22:37:45 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 May 2026 22:37:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 27 May 2026 22:37:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:94a14999202bc800f78441edfa1b48a3f6b5a799655652a41a4ef92004acb9c3`  
		Last Modified: Wed, 27 May 2026 07:33:15 GMT  
		Size: 33.1 MB (33062079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d1fa975ce3866da18a22628155a583f5a5fc9e32c7e07a1a4af941ae713200`  
		Last Modified: Wed, 27 May 2026 22:38:05 GMT  
		Size: 37.7 MB (37681226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436af8d7ca89c65c8f929843869799df169835329e2fab087cd14762a927f40e`  
		Last Modified: Wed, 27 May 2026 22:38:08 GMT  
		Size: 156.5 MB (156464390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95c1638553cc6298c0113290ce8432b80fe389d8e3c34da01bfbf524a6f2aa7`  
		Last Modified: Wed, 27 May 2026 22:38:03 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5494ed118b1939f96c6317e15b410101f18f9fbabca555b5ee8734f4c7b46e`  
		Last Modified: Wed, 27 May 2026 22:38:04 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:97193c14102b86f62cb85ea34a127520233f25f50018fe42897fb70ce8cc40bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3815072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e72db3ec1de7c236d1065a9b5c38af5ddd89a8d965b51e541d957ef3a30589`

```dockerfile
```

-	Layers:
	-	`sha256:ff0754bca63d9a548959418efd05477515065cc3dfb4bc5e84085bb483b9c50d`  
		Last Modified: Wed, 27 May 2026 22:38:04 GMT  
		Size: 3.8 MB (3793617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88bf0b2143f487f6ff37f3acd4d93ed4686fe6f8b084e1d05460a2bded89bd3b`  
		Last Modified: Wed, 27 May 2026 22:38:04 GMT  
		Size: 21.5 KB (21455 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:3cd48b587d31ee778de4c3c401e1ef420ab5b6c3a522c4d0217e23138ec4a8be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236878311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e74ea21447d7c123d6decab2dc374bfaef44e5fdcdc15cf483321feb18e892`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 27 May 2026 06:14:57 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 May 2026 06:14:57 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 27 May 2026 06:14:58 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 27 May 2026 06:14:58 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 27 May 2026 06:14:58 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 May 2026 06:14:58 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 27 May 2026 06:14:58 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:14:58 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:14:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 27 May 2026 06:14:59 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 May 2026 06:14:59 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 27 May 2026 06:15:00 GMT
ENV container oci
# Wed, 27 May 2026 06:15:05 GMT
COPY dir:3c79ef63a7976ed53bc357ee61420f17b1c4d01f16daa9a157b46e996d5ae20c in /      
# Wed, 27 May 2026 06:15:06 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 27 May 2026 06:15:06 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 06:15:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 27 May 2026 06:15:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 27 May 2026 06:15:08 GMT
COPY file:5604aea5cf04212fca8939538465f845888885b3e8d5cba8ef672e5a589974b7 in /usr/share/buildinfo/labels.json      
# Wed, 27 May 2026 06:15:10 GMT
COPY file:5604aea5cf04212fca8939538465f845888885b3e8d5cba8ef672e5a589974b7 in /root/buildinfo/labels.json      
# Wed, 27 May 2026 06:15:11 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "org.opencontainers.image.revision"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "build-date"="2026-05-27T06:13:56Z" "org.opencontainers.image.created"="2026-05-27T06:13:56Z" "release"="1779862102"org.opencontainers.image.revision=3aa29655e860e8f28ee9014c3803f132b3b1e65d,org.opencontainers.image.created=2026-05-27T06:13:56Z
# Wed, 27 May 2026 22:50:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 May 2026 22:50:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 22:50:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 May 2026 22:50:47 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 27 May 2026 22:50:47 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Wed, 27 May 2026 22:53:43 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 27 May 2026 22:53:47 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 May 2026 22:53:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 May 2026 22:53:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 27 May 2026 22:53:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d339a2f2276a8d859309603363be4a2e3264f8a5a443e066c45ef5518856d381`  
		Last Modified: Wed, 27 May 2026 10:57:44 GMT  
		Size: 39.0 MB (39023856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58939e04772041c6139b9c72eb21d342c8fe4b6f1a4fe1a247ee089431c487cc`  
		Last Modified: Wed, 27 May 2026 22:51:27 GMT  
		Size: 39.5 MB (39503510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431979a8373c81060e064acc7468cae0b5ad0966b7fd7a8813230e5ca1e20d2d`  
		Last Modified: Wed, 27 May 2026 22:54:26 GMT  
		Size: 158.3 MB (158348525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633259eeaec8618d3139e6636b92980be8db6a89418aef00425a8ccd66bcfda7`  
		Last Modified: Wed, 27 May 2026 22:54:22 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5a2ade78297a8276c7d342e63e71ee879d196abc947929c6a573a859513744`  
		Last Modified: Wed, 27 May 2026 22:54:23 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f2d46480f140511543c407905888325335c5357ecfa7a8b15a007c2d3494f8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3802399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abf89e8e480481c559ed2b5a364f3b7af0b482fc8f8761d02cdd9946f9444864`

```dockerfile
```

-	Layers:
	-	`sha256:bb3e1b3d59be4971c5289e344c34e55821ae4fbb1d18cde4258f7421d8d43ffc`  
		Last Modified: Wed, 27 May 2026 22:54:23 GMT  
		Size: 3.8 MB (3781023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e3dcbd8feff5d44995b293f84f1a4e3354eb665a54e879cb3418a6a4fb01473`  
		Last Modified: Wed, 27 May 2026 22:54:22 GMT  
		Size: 21.4 KB (21376 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:90703541a57fb9dac100a3e21b66d69fb39760d8952d28a5384027c16aaf18ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 MB (220191767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e29de482e8e72ccf118ac7abf639579386a38da61022cce3298a16f83894efe`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 27 May 2026 06:37:00 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 May 2026 06:37:00 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 27 May 2026 06:37:00 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 27 May 2026 06:37:00 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 27 May 2026 06:37:00 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 May 2026 06:37:00 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 27 May 2026 06:37:00 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:37:00 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:37:00 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 27 May 2026 06:37:00 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 May 2026 06:37:00 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 27 May 2026 06:37:00 GMT
ENV container oci
# Wed, 27 May 2026 06:37:01 GMT
COPY dir:24d1f0c37ae2ecf8290e1663d221246314d1b68d602e33735e6d32665445372e in /      
# Wed, 27 May 2026 06:37:01 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 27 May 2026 06:37:01 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 06:37:01 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 27 May 2026 06:37:01 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 27 May 2026 06:37:01 GMT
COPY file:4188614bc7118984387709b86ec90ee5a895ba0f9b561a8cf875fcae15cc3f1f in /usr/share/buildinfo/labels.json      
# Wed, 27 May 2026 06:37:01 GMT
COPY file:4188614bc7118984387709b86ec90ee5a895ba0f9b561a8cf875fcae15cc3f1f in /root/buildinfo/labels.json      
# Wed, 27 May 2026 06:37:01 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "org.opencontainers.image.revision"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "build-date"="2026-05-27T06:36:19Z" "org.opencontainers.image.created"="2026-05-27T06:36:19Z" "release"="1779862102"org.opencontainers.image.revision=3aa29655e860e8f28ee9014c3803f132b3b1e65d,org.opencontainers.image.created=2026-05-27T06:36:19Z
# Wed, 27 May 2026 22:39:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 May 2026 22:39:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 22:39:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 May 2026 22:39:28 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 27 May 2026 22:39:28 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Wed, 27 May 2026 22:40:14 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 27 May 2026 22:40:16 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 May 2026 22:40:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 May 2026 22:40:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 27 May 2026 22:40:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5e0d999553a87b2b92e291dab9ef17c167202f1dbb15b260d71e176269309f5d`  
		Last Modified: Wed, 27 May 2026 10:57:27 GMT  
		Size: 34.7 MB (34680084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f791d9d2e9057d9aa1ff0de899ae842378191648f3f54117e24f972cf721e84`  
		Last Modified: Wed, 27 May 2026 22:39:52 GMT  
		Size: 38.1 MB (38119066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708c1fef362f54ff5788487378ff6f78d4353a759430f1ea83a10daa9e761201`  
		Last Modified: Wed, 27 May 2026 22:40:44 GMT  
		Size: 147.4 MB (147390197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d1e3907804c8a69b532970b4aaae94183061ddf07ed28756706389aaf4ac91`  
		Last Modified: Wed, 27 May 2026 22:40:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907dec967ae31a025efe5886afc2a014d5c2e8e3abc219d9c243033e4c4f6342`  
		Last Modified: Wed, 27 May 2026 22:40:41 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:bb81ecac9a7591e0c369c3b8e739653c1138f3be5559b97ef1b90442a6e4fcad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3801121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1cc63c0fb04a8ed5d117705633381239298cfa6223be8fe26d98ef2098f42ba`

```dockerfile
```

-	Layers:
	-	`sha256:7b3ec20db12f8878c25323fcc8be57492822457402eac238ada78f8fc5cee094`  
		Last Modified: Wed, 27 May 2026 22:40:41 GMT  
		Size: 3.8 MB (3779781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dae28af8a26a99e3b7ee5e13451c47567906f1c1e7496d59250b55032867f8ef`  
		Last Modified: Wed, 27 May 2026 22:40:41 GMT  
		Size: 21.3 KB (21340 bytes)  
		MIME: application/vnd.in-toto+json
