## `gradle:9-jdk21-ubi9`

```console
$ docker pull gradle@sha256:01c45bc5a2bd6c640aa5da8d2c5e52e45f23c47aaea3c22c18e4750ff0e7bbfe
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

### `gradle:9-jdk21-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:8912cd33b106bab72036b8f2e4bf227f69cafa97db2df7ce7b3551c7273603b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.5 MB (405526492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b816f953c234625b15404d3b57f69c69a60f72e6de1019734070132cee3afb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 12 May 2026 05:07:30 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 05:07:30 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 05:07:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 05:07:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 12 May 2026 05:07:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 05:07:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 May 2026 05:07:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:07:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:07:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 May 2026 05:07:30 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 05:07:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 May 2026 05:07:30 GMT
ENV container oci
# Tue, 12 May 2026 05:07:31 GMT
COPY dir:5370c41d6d8459b92eabd7b14d9158353a8d692cfb39a86c0ad6f0e8377d5a95 in /      
# Tue, 12 May 2026 05:07:31 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 05:07:31 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 05:07:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 05:07:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 05:07:31 GMT
COPY file:14972e13093e3eed917450ec88ead3bcd5bf561d5ae0ced6252f2569fa2669a1 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 05:07:31 GMT
COPY file:14972e13093e3eed917450ec88ead3bcd5bf561d5ae0ced6252f2569fa2669a1 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 05:07:31 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="cbebc1cfad3d894eb79709424b198d17236aaba5" "org.opencontainers.image.revision"="cbebc1cfad3d894eb79709424b198d17236aaba5" "build-date"="2026-05-12T05:07:12Z" "org.opencontainers.image.created"="2026-05-12T05:07:12Z" "release"="1778562320"org.opencontainers.image.revision=cbebc1cfad3d894eb79709424b198d17236aaba5,org.opencontainers.image.created=2026-05-12T05:07:12Z
# Tue, 12 May 2026 23:34:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:34:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:34:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:34:03 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:34:03 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 12 May 2026 23:34:10 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 23:34:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:34:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:34:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:34:11 GMT
CMD ["jshell"]
# Wed, 13 May 2026 00:13:13 GMT
CMD ["gradle"]
# Wed, 13 May 2026 00:13:13 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 May 2026 00:13:13 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 13 May 2026 00:13:13 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 May 2026 00:13:13 GMT
WORKDIR /home/gradle
# Wed, 13 May 2026 00:13:16 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 13 May 2026 00:13:16 GMT
ENV GRADLE_VERSION=9.5.1
# Wed, 13 May 2026 00:13:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Wed, 13 May 2026 00:13:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 13 May 2026 00:13:19 GMT
USER gradle
# Wed, 13 May 2026 00:13:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 13 May 2026 00:13:19 GMT
USER root
```

-	Layers:
	-	`sha256:c06b8ad3393fea673394e067fccddfc7ef6d8cee753eba4c4dcd5d67792bfd4b`  
		Last Modified: Tue, 12 May 2026 06:00:36 GMT  
		Size: 40.0 MB (40022633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a788d64c6c0df20ce89303b4af38c6269dca815da7aee0f72471b354a6ce833`  
		Last Modified: Tue, 12 May 2026 23:34:29 GMT  
		Size: 30.4 MB (30368218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144f09ac6d9704494e549f8e143aabec752ed019a04c04344a1e34802520d675`  
		Last Modified: Tue, 12 May 2026 23:34:32 GMT  
		Size: 158.2 MB (158172647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bfc639876bd07beb643065f96ce8053694abf1813a5ef109d50725bfcf7822`  
		Last Modified: Tue, 12 May 2026 23:34:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8379cb2e116bfbdcd5ba404c5dbfb00f68ddd833c5f60aaeda9d92e424efe1dd`  
		Last Modified: Tue, 12 May 2026 23:34:12 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe20b2b042a2ee7507ec3832e0d54080b9462e34dfde480ad398f536b1af494a`  
		Last Modified: Wed, 13 May 2026 00:13:36 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8625a4f9f68a9599fc4e1b466918059ecdb999a4c1ac812ae426f102520274`  
		Last Modified: Wed, 13 May 2026 00:13:38 GMT  
		Size: 36.7 MB (36696231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3aaaf1ecccd1f59d3f3497729be525fe205d7280f06ce47152f6cdce501d65`  
		Last Modified: Wed, 13 May 2026 00:13:41 GMT  
		Size: 140.2 MB (140236986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ae1f266a23d5e3fd52ee559c5729adf85a34dbcea0312ac925dc163f48e69a`  
		Last Modified: Wed, 13 May 2026 00:13:37 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:7d49ce2e4c2568c15b00d62bdb27d64eccfe3b9520efd0901281f3d047861bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397aff700905c36798f035475ec242b6ce5a8d37fc130ad0e183402a850a413d`

```dockerfile
```

-	Layers:
	-	`sha256:bf736ebee96219c8183edb2bcd455fbfbde2c2857820f6549148d518b40ebe39`  
		Last Modified: Wed, 13 May 2026 00:13:37 GMT  
		Size: 5.4 MB (5420754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f513105e19ee02cad7376e872933a36a9da7b12b318a5815f5ccdffb5b928817`  
		Last Modified: Wed, 13 May 2026 00:13:37 GMT  
		Size: 23.5 KB (23493 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:59944b85bd07f2b23a983f8b96dbe695b33c325ed274aca34da5415baf248d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.8 MB (401753214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a997cf2b21d5e5dc39ca905daf6a2af5cd90907622a44a5cd37bf2fe2d2955`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 12 May 2026 05:08:30 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 05:08:30 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 05:08:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 05:08:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 12 May 2026 05:08:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 05:08:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 May 2026 05:08:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:08:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:08:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 May 2026 05:08:30 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 05:08:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 May 2026 05:08:30 GMT
ENV container oci
# Tue, 12 May 2026 05:08:31 GMT
COPY dir:1ccd99245be3a0b58a1846f076e5b2ceb5e84e683dd2697432c08ac554789d9d in /      
# Tue, 12 May 2026 05:08:31 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 05:08:31 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 05:08:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 05:08:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 05:08:31 GMT
COPY file:cf956423e241a9e8b50b424962675080490b78c30504a00193ac8d9c11b9a880 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 05:08:31 GMT
COPY file:cf956423e241a9e8b50b424962675080490b78c30504a00193ac8d9c11b9a880 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 05:08:31 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="cbebc1cfad3d894eb79709424b198d17236aaba5" "org.opencontainers.image.revision"="cbebc1cfad3d894eb79709424b198d17236aaba5" "build-date"="2026-05-12T05:08:17Z" "org.opencontainers.image.created"="2026-05-12T05:08:17Z" "release"="1778562320"org.opencontainers.image.revision=cbebc1cfad3d894eb79709424b198d17236aaba5,org.opencontainers.image.created=2026-05-12T05:08:17Z
# Tue, 12 May 2026 23:32:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:32:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:32:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:32:51 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:32:51 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 12 May 2026 23:33:45 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 23:33:46 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:33:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:33:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:33:46 GMT
CMD ["jshell"]
# Wed, 13 May 2026 00:13:14 GMT
CMD ["gradle"]
# Wed, 13 May 2026 00:13:14 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 May 2026 00:13:14 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 13 May 2026 00:13:14 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 May 2026 00:13:14 GMT
WORKDIR /home/gradle
# Wed, 13 May 2026 00:13:18 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 13 May 2026 00:13:18 GMT
ENV GRADLE_VERSION=9.5.1
# Wed, 13 May 2026 00:13:18 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Wed, 13 May 2026 00:13:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 13 May 2026 00:13:20 GMT
USER gradle
# Wed, 13 May 2026 00:13:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 13 May 2026 00:13:21 GMT
USER root
```

-	Layers:
	-	`sha256:cd21d11a73b4a3fb6683533da05d561785e6bdfe61eb163870493206db32b8fc`  
		Last Modified: Tue, 12 May 2026 06:10:38 GMT  
		Size: 38.2 MB (38205025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec40cb10901f00e4143a36d9cdc60a23a981663829ccd46f2c83d1d755a80e2`  
		Last Modified: Tue, 12 May 2026 23:33:08 GMT  
		Size: 30.8 MB (30788821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655efc5f4075f4d3f79c1e68a4c155046179cba16c57fd8a94c99445791911b3`  
		Last Modified: Tue, 12 May 2026 23:34:06 GMT  
		Size: 156.5 MB (156464366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06452df1dfd584f8e388d23b7815ed082fb9d6dd2b023e4e169a810e0aadc03`  
		Last Modified: Tue, 12 May 2026 23:34:03 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1158365f24be4a85a2dec1f2b83772761f3077f6daea23a2ac6325673e93cfaf`  
		Last Modified: Tue, 12 May 2026 23:33:54 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40acda6c5b1f206a974ec1c50cdd786c1385a8992150a26ef49e426fce4e7849`  
		Last Modified: Wed, 13 May 2026 00:13:39 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff866154c2507573b6e694ffe51f2db781b6cbe4349f51f3fd939bba863cbd74`  
		Last Modified: Wed, 13 May 2026 00:13:40 GMT  
		Size: 36.0 MB (36024519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161fd9073afb184a5e53ccee43843571843f37b23f81c9aef1fedc31e2e7312a`  
		Last Modified: Wed, 13 May 2026 00:13:44 GMT  
		Size: 140.2 MB (140236981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6d586f4e6e8dffe538aa0b9418cde087d7781f0dadbb2d768ad5c8c6eed996`  
		Last Modified: Wed, 13 May 2026 00:13:38 GMT  
		Size: 29.3 KB (29338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:a92f8d9b27c39dd1ac5b1ff667b3a3c65989a0cf8d6ba2d02d46263fc7bdd7ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac022ae535cd0dce36c4c3a214b1c7474a212089e60dacb38d7e98d3b376d68`

```dockerfile
```

-	Layers:
	-	`sha256:de274d4a46967e3c88e188c1ea540c7628a7a3c65dd8e1f7286df1abef765f18`  
		Last Modified: Wed, 13 May 2026 00:13:39 GMT  
		Size: 5.4 MB (5420148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a6b0a161c726f0d862ac63573fb5a78b6bec0ec4a602be4149c1f79cbbc443a`  
		Last Modified: Wed, 13 May 2026 00:13:39 GMT  
		Size: 23.7 KB (23655 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:ccf7b4c40373fd628f2b94eac5e980654191379e75a9eaeaa4d24f2de7965590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.8 MB (413800511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed37084fb740fe54cc6b936b0fcddd35eb3c30910ff485cfc1a2d9d4c67b5600`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 12 May 2026 05:08:36 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 05:08:36 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 05:08:36 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 05:08:36 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 12 May 2026 05:08:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 05:08:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 May 2026 05:08:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:08:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:08:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 May 2026 05:08:37 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 05:08:37 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 May 2026 05:08:37 GMT
ENV container oci
# Tue, 12 May 2026 05:08:37 GMT
COPY dir:a355654efba77c17476e6a7d5b5c7ad113dd460739ab9901deec15db41210d83 in /      
# Tue, 12 May 2026 05:08:37 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 05:08:37 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 05:08:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 05:08:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 05:08:38 GMT
COPY file:b6d86ec52d4ff251e9a69e4177680b9b3b6e71d2c630134454bededfdfd3098c in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 05:08:38 GMT
COPY file:b6d86ec52d4ff251e9a69e4177680b9b3b6e71d2c630134454bededfdfd3098c in /root/buildinfo/labels.json      
# Tue, 12 May 2026 05:08:38 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="cbebc1cfad3d894eb79709424b198d17236aaba5" "org.opencontainers.image.revision"="cbebc1cfad3d894eb79709424b198d17236aaba5" "build-date"="2026-05-12T05:08:26Z" "org.opencontainers.image.created"="2026-05-12T05:08:26Z" "release"="1778562320"org.opencontainers.image.revision=cbebc1cfad3d894eb79709424b198d17236aaba5,org.opencontainers.image.created=2026-05-12T05:08:26Z
# Tue, 12 May 2026 23:31:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:31:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:31:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:31:48 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:31:48 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 12 May 2026 23:38:00 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 23:38:03 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:38:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:38:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:38:03 GMT
CMD ["jshell"]
# Wed, 13 May 2026 00:12:52 GMT
CMD ["gradle"]
# Wed, 13 May 2026 00:12:52 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 May 2026 00:12:52 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 13 May 2026 00:12:52 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 May 2026 00:12:53 GMT
WORKDIR /home/gradle
# Wed, 13 May 2026 00:13:12 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 13 May 2026 00:13:12 GMT
ENV GRADLE_VERSION=9.5.1
# Wed, 13 May 2026 00:13:12 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Wed, 13 May 2026 00:13:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 13 May 2026 00:13:17 GMT
USER gradle
# Wed, 13 May 2026 00:13:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 13 May 2026 00:13:19 GMT
USER root
```

-	Layers:
	-	`sha256:79d0e019ce895d0aca184904f5a8e1c238e93edc928ef6e5b2e268c9ea088d61`  
		Last Modified: Tue, 12 May 2026 06:11:10 GMT  
		Size: 44.4 MB (44437382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbdf1fc5ff833d1acc4507cdc17a2bf17961989ce6e84f818cc2b5117051d29`  
		Last Modified: Tue, 12 May 2026 23:32:28 GMT  
		Size: 32.8 MB (32841724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80aa51386cfb6a7cf0f3434d87e68c7f94919a48a917c2b8d18a21368a7ca5a`  
		Last Modified: Tue, 12 May 2026 23:38:47 GMT  
		Size: 158.3 MB (158348494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52287403ef217896dafba367b824bc3b3a42e05e8dda824d19db3a635032abec`  
		Last Modified: Tue, 12 May 2026 23:38:43 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3270aae8f4b887477a2252dae5ca2fae93ec71f2052111d0ccf87cdd0ba9fd56`  
		Last Modified: Tue, 12 May 2026 23:38:43 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f7f984af0b40fb6d2d455a7b6d7497c867c4be5b5fbe10a2e7fc5b88c43ef1`  
		Last Modified: Wed, 13 May 2026 00:13:55 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6256d6b693bca7d3318d769e1abcb218c0396b95f602504527d460969a881d94`  
		Last Modified: Wed, 13 May 2026 00:13:57 GMT  
		Size: 37.9 MB (37931384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854ba7c00242357532f758f725e2755502d0d26e58c4dce0d3ae25e01e69b18e`  
		Last Modified: Wed, 13 May 2026 00:14:00 GMT  
		Size: 140.2 MB (140236986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872495713913fef963b4985eaa8964e58aa06f33c771b74064347166a8e861bb`  
		Last Modified: Wed, 13 May 2026 00:13:55 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:38ee8e60c519f15d54116590245ff7d73095945ed04843319a3a605a7215bd17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5441655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3e5ec7f9d2ca536fdce93cb17645614fd83a7fc424ddb5734e418cfda3175e`

```dockerfile
```

-	Layers:
	-	`sha256:be04c2045c3a288e6bedcd5767748ee1d0640602a150c6a6b96cb0a958eeb45e`  
		Last Modified: Wed, 13 May 2026 00:13:56 GMT  
		Size: 5.4 MB (5418071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82ff566c45df25d651ad9af327738a47ae711d8534c0c7ffcc64301d18ed72af`  
		Last Modified: Wed, 13 May 2026 00:13:56 GMT  
		Size: 23.6 KB (23584 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-ubi9` - linux; s390x

```console
$ docker pull gradle@sha256:8825ed4dfbd5033e51aaecc15bf4b5a26994afa3891401ac877c80f583d04757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.5 MB (392477720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac88bac9a4774d5a43e2d724a323a93759ecb8e464aaef3cc8536ae3769c23d1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 12 May 2026 05:11:47 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 05:11:47 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 05:11:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 05:11:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 12 May 2026 05:11:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 05:11:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 May 2026 05:11:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:11:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:11:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 May 2026 05:11:47 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 05:11:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 May 2026 05:11:47 GMT
ENV container oci
# Tue, 12 May 2026 05:11:48 GMT
COPY dir:249441911c8c0633ca798490aaa1299c161ab98598d4ab2b7470ccab434a7c48 in /      
# Tue, 12 May 2026 05:11:48 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 05:11:48 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 05:11:48 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 05:11:48 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 05:11:48 GMT
COPY file:205d87f3ff6644c034e0dc9b6978b61083953f1a77745b1cda275d4a241fe854 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 05:11:48 GMT
COPY file:205d87f3ff6644c034e0dc9b6978b61083953f1a77745b1cda275d4a241fe854 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 05:11:49 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="cbebc1cfad3d894eb79709424b198d17236aaba5" "org.opencontainers.image.revision"="cbebc1cfad3d894eb79709424b198d17236aaba5" "build-date"="2026-05-12T05:11:36Z" "org.opencontainers.image.created"="2026-05-12T05:11:36Z" "release"="1778562320"org.opencontainers.image.revision=cbebc1cfad3d894eb79709424b198d17236aaba5,org.opencontainers.image.created=2026-05-12T05:11:36Z
# Tue, 12 May 2026 23:33:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:33:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:33:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:33:23 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:33:23 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 12 May 2026 23:36:08 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 23:36:15 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:36:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:36:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:36:19 GMT
CMD ["jshell"]
# Wed, 13 May 2026 00:12:34 GMT
CMD ["gradle"]
# Wed, 13 May 2026 00:12:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 May 2026 00:12:34 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 13 May 2026 00:12:34 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 May 2026 00:12:35 GMT
WORKDIR /home/gradle
# Wed, 13 May 2026 00:13:26 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 13 May 2026 00:13:26 GMT
ENV GRADLE_VERSION=9.5.1
# Wed, 13 May 2026 00:13:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Wed, 13 May 2026 00:13:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 13 May 2026 00:13:36 GMT
USER gradle
# Wed, 13 May 2026 00:13:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 13 May 2026 00:13:39 GMT
USER root
```

-	Layers:
	-	`sha256:ce111e91e194b1445a42f490d2da50a425f89166a5a9cd92ae2933436bc449dc`  
		Last Modified: Tue, 12 May 2026 06:10:58 GMT  
		Size: 38.1 MB (38131193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9b279d81e22a866d648693a16e7f23cd6048a781948bd2c0b76862ce048388`  
		Last Modified: Tue, 12 May 2026 23:33:48 GMT  
		Size: 30.4 MB (30383156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883b05d70cd4bf1320680139e3e5140724fa6bcb218948acc5ac2300a33c03f2`  
		Last Modified: Tue, 12 May 2026 23:37:30 GMT  
		Size: 147.4 MB (147390189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e42a6bc18ce949e8a37febd202b262a903e91e18d577811bd78bf64a5b3176`  
		Last Modified: Tue, 12 May 2026 23:37:25 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788b693ce172c33dc8c904311a2c193709b7617336df377bcebcfb64764088a7`  
		Last Modified: Tue, 12 May 2026 23:37:25 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1ec93c1514f8da2e6d085f8062dae414c0297e0cd56da0d6fab849d099acac`  
		Last Modified: Wed, 13 May 2026 00:14:46 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb3369780ea7b22100a2eea67f80e417c6cfb44926de6730f99744ea130491b`  
		Last Modified: Wed, 13 May 2026 00:14:49 GMT  
		Size: 36.3 MB (36331639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095e1ae4aae1393d0d0d015a4ecc3e1497fc98ef90515de6ff22411daa9f589b`  
		Last Modified: Wed, 13 May 2026 00:14:53 GMT  
		Size: 140.2 MB (140236991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1004673b12b65babd5bae8a9f15e12d509102e1810f540db5c06595ae9e12376`  
		Last Modified: Wed, 13 May 2026 00:14:45 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:878b467554f9dfc4b5f60a040a413b332f104bcc48a403346f3f989670568502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b83ebfa5e85ae1a8e5d1779c6d79db85f9dcc1a2073127cd1a93012ab6b1a34`

```dockerfile
```

-	Layers:
	-	`sha256:9cf5eaf0813604c0f19a869a5aa8d97bbb7e85eec7235f35e201b978369952d1`  
		Last Modified: Wed, 13 May 2026 00:14:46 GMT  
		Size: 5.4 MB (5407359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99b042f4197dd4e90328cb1a1bced2ca4af0d7c1fca27a3395bf8b8e532de9d7`  
		Last Modified: Wed, 13 May 2026 00:14:45 GMT  
		Size: 23.5 KB (23528 bytes)  
		MIME: application/vnd.in-toto+json
