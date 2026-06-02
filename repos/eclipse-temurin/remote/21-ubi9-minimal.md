## `eclipse-temurin:21-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:bb52873c046b7347f246706a641e342af1fd7c15735fcaa2345e8a048d8e4639
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

### `eclipse-temurin:21-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:6bdb38154994b0b93d46b0319ef6895098a10afb126056d8298cc22d866eed30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226523594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79836b0bc50348eaa5390a2be8afca40a41e2fa94f90afad372df604b0863f5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Tue, 02 Jun 2026 22:45:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 22:45:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:45:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 22:45:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:45:34 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 02 Jun 2026 22:45:42 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 02 Jun 2026 22:45:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:45:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:45:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 22:45:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dd148063a98f38d63a03cea2357d237d418889b91f204f507c033c944e443f45`  
		Last Modified: Tue, 02 Jun 2026 07:03:29 GMT  
		Size: 40.7 MB (40687042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9688d518c8d14e258ab0b77f7215bea3b68be63f3d94a4bf488d6386060ab479`  
		Last Modified: Tue, 02 Jun 2026 22:46:01 GMT  
		Size: 27.7 MB (27661513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d356d001f8d87bae7f8dc648085f3994b962809aa16c01f3e8eb0b0660c3b2e6`  
		Last Modified: Tue, 02 Jun 2026 22:46:04 GMT  
		Size: 158.2 MB (158172620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59fc1c83f6a9c1d15927b2d72f1ef6bb8378700052e18a01839a58647eaf399a`  
		Last Modified: Tue, 02 Jun 2026 22:46:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9da79f043bc8a4d241218594a742ce94375362b90060611beb829480fc7570`  
		Last Modified: Tue, 02 Jun 2026 22:46:00 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d4ec6544c38ce6c4d61d950cf4c5ad30714ecd9d5b2b293c32a63dd3da7a57ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2518110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc4f74f75262bd51c0eaaf48d46aebc238b4391a24956e7f77c486dcd4b3c39`

```dockerfile
```

-	Layers:
	-	`sha256:2e69689778c0f4d505798eb53d7ff5a25f0a3985699b2e3e8d57ccce110fb3de`  
		Last Modified: Tue, 02 Jun 2026 22:46:00 GMT  
		Size: 2.5 MB (2496942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e093a5565699fba75fb45fd50dbb79cc8a4fddbbbf9a90f59e75965694c62447`  
		Last Modified: Tue, 02 Jun 2026 22:46:00 GMT  
		Size: 21.2 KB (21168 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:7c4c1e281e52d7a9202da4f20bf287fb184d9c941d108bb88fc969e5706e2c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223427198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01a3f7a14af6d2d882236d3b6e209133acdabcf1d9d74a681073e7562701bad`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Tue, 02 Jun 2026 22:44:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 22:44:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:44:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 22:44:35 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:44:35 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 02 Jun 2026 22:45:07 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 02 Jun 2026 22:45:09 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:45:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:45:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 22:45:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7db43598c7e47cf895f880f92e3cee9c07787091c97802ea3f2bea8fa4848040`  
		Last Modified: Tue, 02 Jun 2026 07:03:29 GMT  
		Size: 38.9 MB (38863161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f870e305f107f46a91e1aeb7bdad39398ed9779def5cb4a8b73dc97d0abc9bf6`  
		Last Modified: Tue, 02 Jun 2026 22:44:51 GMT  
		Size: 28.1 MB (28097265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3ca38d073aa07752564c98396c64cc7c22795a3e1ee7a297d49a4958470902`  
		Last Modified: Tue, 02 Jun 2026 22:45:29 GMT  
		Size: 156.5 MB (156464352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947ae2701773f6f96d5116c6e52320bd405c3738e14a74d67d3fe422321d42d2`  
		Last Modified: Tue, 02 Jun 2026 22:45:25 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5d81c492b9cb9348ccbadc2bc469df497da960e56a57bb5671a8041abf75a7`  
		Last Modified: Tue, 02 Jun 2026 22:45:25 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2c6eb49fc9b444929bc81b7725da27e09bae5eb358ad562615eac8b6a456d124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2517596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d61da36b9a0a94641b535e189945a15496f487ead31f39c213d7c9753d61c4`

```dockerfile
```

-	Layers:
	-	`sha256:9d0ed0dc1193b3b32c2bbcf782faa246019fb4e5f353822cd8ebf41deda4f85d`  
		Last Modified: Tue, 02 Jun 2026 22:45:25 GMT  
		Size: 2.5 MB (2496312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fdfa5681c574e817bff67a63cb96a30aee7694adfa498e7c4d9809d72b1d8b6`  
		Last Modified: Tue, 02 Jun 2026 22:45:25 GMT  
		Size: 21.3 KB (21284 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:22826302ebdff2516004a144fc5ff373bf3909d8e242ef775d2a69c509880ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233591092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db34a09fe3be30f7912123ff344b9699a20fd60a1225bc49cbff68c2e46184fa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 02 Jun 2026 22:53:53 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 02 Jun 2026 22:53:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:53:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:53:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 22:53:57 GMT
CMD ["jshell"]
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
	-	`sha256:54c53049531253223d42efbb458637824867b9bebc5361eedb00f30cec7f6adc`  
		Last Modified: Tue, 02 Jun 2026 22:54:40 GMT  
		Size: 158.3 MB (158348500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f8f61831557f3b5bffe2d9cba9e96a9dd8841b98e1eb45c31060d623f9465c`  
		Last Modified: Tue, 02 Jun 2026 22:54:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa35346cab3579e8a6c3cd09a7934b058aa99ff104b0190239a13a7e41b50333`  
		Last Modified: Tue, 02 Jun 2026 22:54:37 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:be72033bc33c618cd7094f3a15b45ff1b20dbd91329b3d8e3862086554a80d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2516276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f783b2ce8f78fd833256595dff62591eb901242bd155dd857dda032640d11bae`

```dockerfile
```

-	Layers:
	-	`sha256:21d32280e8ec42bdc8c687a35f75f46b59bcde2398143e048cec3e02f7cbcf03`  
		Last Modified: Tue, 02 Jun 2026 22:54:36 GMT  
		Size: 2.5 MB (2495072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f134fbf33f2943a9e78a0da9504e1939ac3b826acaf026a5bbb65ca8bf6ecd6a`  
		Last Modified: Tue, 02 Jun 2026 22:54:36 GMT  
		Size: 21.2 KB (21204 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:8cc15de4d38c24d9cc197cf789b603ec9c10e4cd6af29d8013ea5e5ce9095e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 MB (213872096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6db82781ab938590c61e68238b6cee3e1acb2471f03ae9d447bae349ed052dd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jun 2026 05:58:20 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 05:58:20 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 05:58:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 05:58:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 02 Jun 2026 05:58:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 05:58:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 02 Jun 2026 05:58:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:58:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:58:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 02 Jun 2026 05:58:20 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 05:58:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 02 Jun 2026 05:58:20 GMT
ENV container oci
# Tue, 02 Jun 2026 05:58:21 GMT
COPY dir:42d16b6fc3799c6e8e18836407138d7a47421712f6e545204e190f0bc9cd0367 in /      
# Tue, 02 Jun 2026 05:58:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 05:58:21 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 05:58:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 05:58:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 05:58:21 GMT
COPY file:4c2ab4fe2bf528858e28a71d4ac6059cf378c99fb19db56c8676a607bbe8fd92 in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:58:21 GMT
COPY file:4c2ab4fe2bf528858e28a71d4ac6059cf378c99fb19db56c8676a607bbe8fd92 in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:58:21 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "org.opencontainers.image.revision"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "build-date"="2026-06-02T05:58:08Z" "org.opencontainers.image.created"="2026-06-02T05:58:08Z" "release"="1780378819"org.opencontainers.image.revision=842dd1c603c36c8d242d5ec075adccffb3bfea5c,org.opencontainers.image.created=2026-06-02T05:58:08Z
# Tue, 02 Jun 2026 22:43:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 22:43:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:43:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 22:43:21 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:43:21 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 02 Jun 2026 22:45:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 02 Jun 2026 22:45:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:45:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:45:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 22:45:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ba9f2e747b70b6ed487f72e44a2125691e7495f0533ca3565e966694a38ee758`  
		Last Modified: Tue, 02 Jun 2026 12:12:51 GMT  
		Size: 38.8 MB (38784938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb773a8972861f38bb22fa221bbbf221dfd8c3f3058891f97c7d0a4b0a042c99`  
		Last Modified: Tue, 02 Jun 2026 22:43:57 GMT  
		Size: 27.7 MB (27694593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f536168cc07a2101438eff7c3dd6c99c54b0523b58d9f4c7ed59aea927b672a`  
		Last Modified: Tue, 02 Jun 2026 22:45:55 GMT  
		Size: 147.4 MB (147390144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d473a1950a37d421b9af43de4eebd7e468e55b1a1e45c931f24ae584f8097778`  
		Last Modified: Tue, 02 Jun 2026 22:45:53 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7a740a9e7bd647a321ec15fe47b4e5b98769266908f7fe1755d543a974f2b7`  
		Last Modified: Tue, 02 Jun 2026 22:45:53 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6260c005e815722be683a17cb168b92034dfd66de1fce68a82d54ab34d8c0d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2505502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952b1284ee4020d64ba8da4827f6ecbc932a2f680ed07340c50ac6d7f294b1e0`

```dockerfile
```

-	Layers:
	-	`sha256:1b35e235920d8979af047c8a734dd6e8cc334655b82b200413b4ca8704171aa1`  
		Last Modified: Tue, 02 Jun 2026 22:45:53 GMT  
		Size: 2.5 MB (2484334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0f79bbc184295a121403c9672f1a336158201303007baaf3e5d3257db03e7cc`  
		Last Modified: Tue, 02 Jun 2026 22:45:53 GMT  
		Size: 21.2 KB (21168 bytes)  
		MIME: application/vnd.in-toto+json
