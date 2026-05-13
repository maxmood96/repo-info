## `gradle:7-jdk17-ubi`

```console
$ docker pull gradle@sha256:72e3506e4cc06f65baaa88cf82f619b2f630dc5a17055ee73a6b9f3573078d33
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

### `gradle:7-jdk17-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:ffb16a6aa329213892a85a054bac31d6d4cf41e60c10b1e05dadb5ab9a1b94bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.5 MB (381530285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7d8fbe64430de3e702a25d5a271a47c7ba871b68a087d1f3001f9f7a4f082b`
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
# Tue, 12 May 2026 23:33:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:33:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:33:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:33:24 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:33:24 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 12 May 2026 23:33:52 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 23:33:53 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:33:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:33:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:33:53 GMT
CMD ["jshell"]
# Wed, 13 May 2026 00:13:18 GMT
CMD ["gradle"]
# Wed, 13 May 2026 00:13:18 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 May 2026 00:13:18 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 13 May 2026 00:13:18 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 May 2026 00:13:18 GMT
WORKDIR /home/gradle
# Wed, 13 May 2026 00:13:22 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 13 May 2026 00:13:22 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 13 May 2026 00:13:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 13 May 2026 00:13:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 13 May 2026 00:13:24 GMT
USER gradle
# Wed, 13 May 2026 00:13:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 13 May 2026 00:13:25 GMT
USER root
```

-	Layers:
	-	`sha256:c06b8ad3393fea673394e067fccddfc7ef6d8cee753eba4c4dcd5d67792bfd4b`  
		Last Modified: Tue, 12 May 2026 06:00:36 GMT  
		Size: 40.0 MB (40022633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e61fb6807dca69cca509ddbd08c60e952a428c1338ba042a754a3eba7edecf`  
		Last Modified: Tue, 12 May 2026 23:33:39 GMT  
		Size: 30.4 MB (30368138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09d17d5779dfda74435e6e6340abec2d7d8b71a6c27b0d6218f96b1f8b3a400`  
		Last Modified: Tue, 12 May 2026 23:34:13 GMT  
		Size: 145.9 MB (145915424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a7b057969ee1cf0f70932d05927b0c54b454d5df7b9c18c375f063a95a5930`  
		Last Modified: Tue, 12 May 2026 23:34:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d2b922b6612a12683b2512da9156f871afad647d562fe4ad8a6180c04ed62b`  
		Last Modified: Tue, 12 May 2026 23:34:08 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47cfa171ad1f15c2176f9a050ba9fd86b9ed8492658ae2ab1f407b0b8c24a52`  
		Last Modified: Wed, 13 May 2026 00:13:42 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbcc6e0c10402abb83712fff876d1822c56a8dc802f9c7302f36c79ddf608da`  
		Last Modified: Wed, 13 May 2026 00:13:43 GMT  
		Size: 36.7 MB (36695622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f8714e4004b2757703d8573f19afe366f8add93d1791f68ecb7750ae7cd3c9`  
		Last Modified: Wed, 13 May 2026 00:13:46 GMT  
		Size: 128.5 MB (128469408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3843fc5e94eb4477d875406ec8cc75e6dd1951ec43e1744a1c9ce772a12ed9`  
		Last Modified: Wed, 13 May 2026 00:13:42 GMT  
		Size: 54.9 KB (54899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:ac62b69b1131e15858e652096b53b5b06ffe7f13a511c2d6184aff0996c35fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c645d8418ffd6a01ebc3214a23f3bb1c887338628e41ba7eb19846bbf98379e`

```dockerfile
```

-	Layers:
	-	`sha256:dd4a5905a8ea3b5eee8639f9a353498f4bd525321ce1d2f46a1673cbf1862e40`  
		Last Modified: Wed, 13 May 2026 00:13:42 GMT  
		Size: 5.3 MB (5315207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba717145d0d0ad9932e399796faf37321d7b2e7b04072d00b91c3a0c4a737f17`  
		Last Modified: Wed, 13 May 2026 00:13:42 GMT  
		Size: 23.5 KB (23547 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:3349e3831261e68deb7ee2add7c8315b20f34692b183f323a2ae605163b2bfed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.3 MB (378286355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a49db5d1b4d2c6a86273c5e6ff099fa8337989c0f249393f88dbccf2019636c`
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
# Tue, 12 May 2026 23:33:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:33:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:33:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:33:19 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:33:19 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 12 May 2026 23:33:26 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 23:33:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:33:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:33:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:33:27 GMT
CMD ["jshell"]
# Wed, 13 May 2026 00:13:23 GMT
CMD ["gradle"]
# Wed, 13 May 2026 00:13:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 May 2026 00:13:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 13 May 2026 00:13:23 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 May 2026 00:13:23 GMT
WORKDIR /home/gradle
# Wed, 13 May 2026 00:13:26 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 13 May 2026 00:13:26 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 13 May 2026 00:13:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 13 May 2026 00:13:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 13 May 2026 00:13:29 GMT
USER gradle
# Wed, 13 May 2026 00:13:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 13 May 2026 00:13:30 GMT
USER root
```

-	Layers:
	-	`sha256:cd21d11a73b4a3fb6683533da05d561785e6bdfe61eb163870493206db32b8fc`  
		Last Modified: Tue, 12 May 2026 06:10:38 GMT  
		Size: 38.2 MB (38205025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30fe5b0b4ed8f763962432bf7ace833f3daa85b1519abfa7ea7050f474d6b615`  
		Last Modified: Tue, 12 May 2026 23:33:46 GMT  
		Size: 30.8 MB (30788906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b931b26af763bec021257da98d4d924b2754cd063235f0f5af51aea36d1ffe9`  
		Last Modified: Tue, 12 May 2026 23:33:48 GMT  
		Size: 144.7 MB (144734808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ca06a4a17be26c4b097aed9d2a9ffdcf499d9f6a611452df4cfe7d583081e6`  
		Last Modified: Tue, 12 May 2026 23:33:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61140a6f506d0eeb4887ddf980ec37077776f4ebd8fa71ac603ee40749f84c6`  
		Last Modified: Tue, 12 May 2026 23:33:44 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47d29ee382546d11d9f2f539d91f877cc7aaaf6733b6603a24552c2511f94b4`  
		Last Modified: Wed, 13 May 2026 00:13:46 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1138d7552ad69b16a81cd3819c3ceb2b99ce7f021b636f6edb061037bf0c465`  
		Last Modified: Wed, 13 May 2026 00:13:48 GMT  
		Size: 36.0 MB (36024505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ce35a4a79c5ee6ef22ead777168cb7ce5ec96d4a2a8a215ea8efd9f0e29a37`  
		Last Modified: Wed, 13 May 2026 00:13:50 GMT  
		Size: 128.5 MB (128469420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbadf9e9363ce417d97172f790c60e97fb4ecd86a15d5cb4b98695394d6134c1`  
		Last Modified: Wed, 13 May 2026 00:13:47 GMT  
		Size: 59.5 KB (59531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:9337b502c4f6e215f5180e24eeb0de3c27c0e3fd0a83c5d6800992f4e0e2b48a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b766c7252e5c32c0ec7296aa0877be7931d50f787515c227d4f9ce275bc16698`

```dockerfile
```

-	Layers:
	-	`sha256:e2988ddeec73f0b6973156badfa02de1e0f37e7fe7b34bfee139b901aa0db0c6`  
		Last Modified: Wed, 13 May 2026 00:13:47 GMT  
		Size: 5.3 MB (5314609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:271026ce19ebcb701f5eb5382356f91d91ffb5a4c8192d41e81fc9cf9d8c43c0`  
		Last Modified: Wed, 13 May 2026 00:13:46 GMT  
		Size: 23.7 KB (23720 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:fbb23978c0a7f19fb4e76a455b706eaf5d00ea12f8e1a15cac85bb4243aa79bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.5 MB (389507872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c939ded81127741dc908f33c592743c2bf2954fcd6e1681e01a3c354cbf926`
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
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 12 May 2026 23:35:58 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 23:36:01 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:36:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:36:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:36:02 GMT
CMD ["jshell"]
# Wed, 13 May 2026 00:14:08 GMT
CMD ["gradle"]
# Wed, 13 May 2026 00:14:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 May 2026 00:14:08 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 13 May 2026 00:14:08 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 May 2026 00:14:08 GMT
WORKDIR /home/gradle
# Wed, 13 May 2026 00:17:48 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 13 May 2026 00:17:48 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 13 May 2026 00:17:48 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 13 May 2026 00:17:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 13 May 2026 00:17:54 GMT
USER gradle
# Wed, 13 May 2026 00:17:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 13 May 2026 00:17:55 GMT
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
	-	`sha256:39b051d4668f607f3e7f7656840598191fe5086cb12bf9495d62db695f2f8743`  
		Last Modified: Tue, 12 May 2026 23:36:39 GMT  
		Size: 145.8 MB (145788677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe1346084abe6eddede37b13459ffece9eb41afbad10d54f32ba797c08160d3`  
		Last Modified: Tue, 12 May 2026 23:36:35 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e77de35b5b1bcbbf83fbb138dfd9edea4431913cff6c5d0f5377bec19a7d64`  
		Last Modified: Tue, 12 May 2026 23:36:35 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e5ee747b40e1802d74d7871391ec408d4f83c8ac194e9f92ec5072a1b81c95`  
		Last Modified: Wed, 13 May 2026 00:15:08 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5602ce3a16cac4e7e18630d3674921e5e7f6d7afd45a00c1b7aa154c336aabda`  
		Last Modified: Wed, 13 May 2026 00:18:33 GMT  
		Size: 37.9 MB (37931497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c466a41e88a237ac27086ade44527baf6ab56d03bc1d4a1f20bfaf4e17361bf1`  
		Last Modified: Wed, 13 May 2026 00:18:35 GMT  
		Size: 128.5 MB (128469422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f808dda3473383b28637c1680722bf76d63532993c4a73cb5146672001417c`  
		Last Modified: Wed, 13 May 2026 00:18:31 GMT  
		Size: 35.0 KB (35006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:aefaff52e3618e06a0706b3c7166e503af3a9f5f085421378a976f7f1d10f832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5336175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5921c1a272c38f16ac8ff88da35b4ea2b4e5a1310699d7cdb337f6ef1ff3f731`

```dockerfile
```

-	Layers:
	-	`sha256:58e4577a3f4d81d4ea31ffae3d126eb2b907bd812e9f06943f84960f76145782`  
		Last Modified: Wed, 13 May 2026 00:18:31 GMT  
		Size: 5.3 MB (5312530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa4184ad69e391cb5ec51179badc40ff1947e47c4ddae24e35410180a7e16a6`  
		Last Modified: Wed, 13 May 2026 00:18:31 GMT  
		Size: 23.6 KB (23645 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:d06de6d73c62963f082a76717f526a5bee9da33184ac1c46443f285322047045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.3 MB (369266868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a4bf5de3e1d1bc80b0d5adf69b5e2baf92376c30be24662c1b15e6cd9ba6f5`
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
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 12 May 2026 23:34:22 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 23:34:25 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:34:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:34:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:34:26 GMT
CMD ["jshell"]
# Wed, 13 May 2026 00:15:28 GMT
CMD ["gradle"]
# Wed, 13 May 2026 00:15:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 May 2026 00:15:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 13 May 2026 00:15:28 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 May 2026 00:15:29 GMT
WORKDIR /home/gradle
# Wed, 13 May 2026 00:17:59 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 13 May 2026 00:17:59 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 13 May 2026 00:17:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 13 May 2026 00:18:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 13 May 2026 00:18:08 GMT
USER gradle
# Wed, 13 May 2026 00:18:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 13 May 2026 00:18:13 GMT
USER root
```

-	Layers:
	-	`sha256:ce111e91e194b1445a42f490d2da50a425f89166a5a9cd92ae2933436bc449dc`  
		Last Modified: Tue, 12 May 2026 06:10:58 GMT  
		Size: 38.1 MB (38131193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2beef37fbe27a9395a329db26697bbffda5310b4cf235c92b7164ae6cd167e`  
		Last Modified: Tue, 12 May 2026 23:33:58 GMT  
		Size: 30.4 MB (30383170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80821afcfed40cd817f8f94bc8ecf841cbbe34803f0724d88846888569cf4577`  
		Last Modified: Tue, 12 May 2026 23:35:35 GMT  
		Size: 135.9 MB (135912299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfb07127a4c167e5b5d70517e0e23b22ae6dac3bbae3a852a9f88bde036add9`  
		Last Modified: Tue, 12 May 2026 23:35:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eade8d9ab3c32553763a611d973aa8824fff23c03be31147308d84ffa3361fa6`  
		Last Modified: Tue, 12 May 2026 23:35:23 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a6d068493cc3c8b43ae6b6f3ea94f1eca5b292f45067c3a7bee4cb6f4ed0dc`  
		Last Modified: Wed, 13 May 2026 00:17:05 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cb0cd7306ab5dc6c49b35bb64e5fd4c283e9a5646a2b0552d9b844099c9783`  
		Last Modified: Wed, 13 May 2026 00:18:54 GMT  
		Size: 36.3 MB (36331604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f9d8369d536d4a0aa7e77a68307e9afc2c9eae80fa1a89fd3e5cdf1f5897c7`  
		Last Modified: Wed, 13 May 2026 00:18:56 GMT  
		Size: 128.5 MB (128469421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb184925f1bdf2d55bf92eba09e2c8f6666f54d22333b5d87693b8641c3dffe`  
		Last Modified: Wed, 13 May 2026 00:18:51 GMT  
		Size: 35.0 KB (35012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:54ec376ba8536639ecfb4b558d3779c174f39b95c899717f16d7352f9665d34f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5325391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164ed81bc2583a77cba11ae24d52a664219d8abc5ddee9eed6279db920bc095c`

```dockerfile
```

-	Layers:
	-	`sha256:03855264151edc45d735d69d734b06f1a82c25184b9fac0681ea05fd41b9804a`  
		Last Modified: Wed, 13 May 2026 00:18:52 GMT  
		Size: 5.3 MB (5301808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdaef6f5bfda8d6c611e07d5b2db331691b4594cc96be7dbae4dd79f4bf1dc76`  
		Last Modified: Wed, 13 May 2026 00:18:50 GMT  
		Size: 23.6 KB (23583 bytes)  
		MIME: application/vnd.in-toto+json
