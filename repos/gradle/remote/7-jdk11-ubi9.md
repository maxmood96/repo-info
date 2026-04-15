## `gradle:7-jdk11-ubi9`

```console
$ docker pull gradle@sha256:fb8b7f599c88071ab034e386fc082cf7d0261afb89208315411eb17d8a42c41d
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

### `gradle:7-jdk11-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:56bd0dad6fdc9d3a3a92bb2ebfc2f95a18d6b297e6b2251e4ed7e94a8c024a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.9 MB (377872329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ba302beb5c32e7b457ffd2513cefebac40593bc86d75648ff92a2101ebf02e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 13 Apr 2026 18:26:37 GMT
ENV container oci
# Mon, 13 Apr 2026 18:26:38 GMT
COPY dir:5191e1ce97881b91cd281225b61de5b907dbc286c69b6681e228608a9d6bab0b in /      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 18:26:38 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:22a393f43688b6747c863a4550da665d92705a5e9519cc2d1c97b9f7499127bb in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:22a393f43688b6747c863a4550da665d92705a5e9519cc2d1c97b9f7499127bb in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:26:39 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "org.opencontainers.image.revision"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "build-date"="2026-04-13T18:26:26Z" "org.opencontainers.image.created"="2026-04-13T18:26:26Z" "release"="1776104705"org.opencontainers.image.revision=49cc6237764cacc4684bc968dd9fc53fb8abd12c,org.opencontainers.image.created=2026-04-13T18:26:26Z
# Tue, 14 Apr 2026 20:45:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Apr 2026 20:45:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 20:45:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Apr 2026 20:45:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 14 Apr 2026 20:45:32 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 14 Apr 2026 20:45:38 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 14 Apr 2026 20:45:39 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 14 Apr 2026 20:45:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Apr 2026 20:45:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Apr 2026 20:45:39 GMT
CMD ["jshell"]
# Tue, 14 Apr 2026 20:59:12 GMT
CMD ["gradle"]
# Tue, 14 Apr 2026 20:59:12 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 14 Apr 2026 20:59:12 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 14 Apr 2026 20:59:12 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 14 Apr 2026 20:59:12 GMT
WORKDIR /home/gradle
# Tue, 14 Apr 2026 20:59:16 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 14 Apr 2026 20:59:16 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 14 Apr 2026 20:59:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 14 Apr 2026 21:00:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 14 Apr 2026 21:00:28 GMT
USER gradle
# Tue, 14 Apr 2026 21:00:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 14 Apr 2026 21:00:29 GMT
USER root
```

-	Layers:
	-	`sha256:b1ed13c5ef0ac6dbcd255a5c1be9e3c9c2903872aa4ae5fa877850a48fdaee26`  
		Last Modified: Mon, 13 Apr 2026 19:17:03 GMT  
		Size: 40.0 MB (40016560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fb22d429ca0142fa2aaf4dd83e368753d8474e70b668e50b10f310fa526751`  
		Last Modified: Tue, 14 Apr 2026 20:45:57 GMT  
		Size: 30.4 MB (30369635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dee96365b2b8af6fa5c79f607e4d129e48dc6280097dda21ce3e778ca645614`  
		Last Modified: Tue, 14 Apr 2026 20:45:59 GMT  
		Size: 142.3 MB (142263242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ccab4fdd8c4bc2a852f1fa7e62d6b9c2a9e78f9165b072e6daf7bec93e1032`  
		Last Modified: Tue, 14 Apr 2026 20:45:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8dfe926bc9d0a59836cc3c4426e3069f970c168eeb7974e6283e040656daa3`  
		Last Modified: Tue, 14 Apr 2026 20:45:46 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc040b1b3397a248faa0d4603657a02f5e9408f93993a3c8607f1f17c8275d0`  
		Last Modified: Tue, 14 Apr 2026 20:59:34 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437d400be8dd3d780f279d0a15619ba1f22d74fbed07dbdd191e98da737db723`  
		Last Modified: Tue, 14 Apr 2026 20:59:35 GMT  
		Size: 36.7 MB (36694413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4840a5c5020ed39e231afad8f05a681d85e341e82f829272ad81c12b7f61c2b`  
		Last Modified: Tue, 14 Apr 2026 21:00:45 GMT  
		Size: 128.5 MB (128469421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f755cf4b3ce5a0682335a81d072a02d503857beba177c4c3ad9889ad62382d`  
		Last Modified: Tue, 14 Apr 2026 21:00:42 GMT  
		Size: 54.9 KB (54905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:c5f170d45bf0dab705de87c723e87ff366cf43f5b43683945a21074ff4bef3de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5357661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce3cc455a3149dae2f82cf3bdcc8e9e3980d343176e3ded00896fd895e1cf62`

```dockerfile
```

-	Layers:
	-	`sha256:2d4d9f99505f1e6b4ad82ac5a72894a672e24025ebf5579193e3772c91fa7a99`  
		Last Modified: Tue, 14 Apr 2026 21:00:42 GMT  
		Size: 5.3 MB (5334082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0acb804325a75ec37696514a47ae81ae6b8b149ef5b313c87d56888c3445262`  
		Last Modified: Tue, 14 Apr 2026 21:00:43 GMT  
		Size: 23.6 KB (23579 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:361261459cc7ab0c0ad1a1741097bddae89ca9ba723858c1653dc3b813b51772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.5 MB (372516649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28a859ee8f1ff01d91c6a481178d9839c0e42c2cfb0b6a8c26c2fee0e29e451`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 13 Apr 2026 18:28:23 GMT
ENV container oci
# Mon, 13 Apr 2026 18:28:24 GMT
COPY dir:50ceff14380ca413ec2568b248e47effdceffdd30707fc734a4741e902f97450 in /      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 18:28:24 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:20aaf8ce1e0136dca2eb48dbc70df34738ee917c73847beed0478c7b853d8231 in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:20aaf8ce1e0136dca2eb48dbc70df34738ee917c73847beed0478c7b853d8231 in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:28:24 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "org.opencontainers.image.revision"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "build-date"="2026-04-13T18:28:10Z" "org.opencontainers.image.created"="2026-04-13T18:28:10Z" "release"="1776104705"org.opencontainers.image.revision=49cc6237764cacc4684bc968dd9fc53fb8abd12c,org.opencontainers.image.created=2026-04-13T18:28:10Z
# Tue, 14 Apr 2026 20:45:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Apr 2026 20:45:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 20:45:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Apr 2026 20:45:23 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 14 Apr 2026 20:45:23 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 14 Apr 2026 20:45:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 14 Apr 2026 20:45:35 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 14 Apr 2026 20:45:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Apr 2026 20:45:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Apr 2026 20:45:35 GMT
CMD ["jshell"]
# Tue, 14 Apr 2026 20:56:15 GMT
CMD ["gradle"]
# Tue, 14 Apr 2026 20:56:15 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 14 Apr 2026 20:56:15 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 14 Apr 2026 20:56:15 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 14 Apr 2026 20:56:15 GMT
WORKDIR /home/gradle
# Tue, 14 Apr 2026 20:56:19 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 14 Apr 2026 20:56:19 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 14 Apr 2026 20:56:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 14 Apr 2026 20:56:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 14 Apr 2026 20:56:22 GMT
USER gradle
# Tue, 14 Apr 2026 20:56:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 14 Apr 2026 20:56:22 GMT
USER root
```

-	Layers:
	-	`sha256:f7c1b31b8294524de5dff6550312e7fc2a074a842daad5dd610d9bfdab56527d`  
		Last Modified: Mon, 13 Apr 2026 19:17:00 GMT  
		Size: 38.2 MB (38200105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681efa422a1547a4042f595ef92f8572b64e95767fdd974ef4402e56f6bb68b9`  
		Last Modified: Tue, 14 Apr 2026 20:45:53 GMT  
		Size: 30.8 MB (30797611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c33c8f48a72f485a25866f11a226366e1754e5c811979f72fec008e953d92c6`  
		Last Modified: Tue, 14 Apr 2026 20:45:56 GMT  
		Size: 139.0 MB (138959720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef53e10a48dbd6a09dda5d09ea763908d76acc48bb61e9e1348d8f52bcf3f0`  
		Last Modified: Tue, 14 Apr 2026 20:45:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909ad6772ab10804930be2a0e0eb5833462da9a14f7acdcf44637420071653fc`  
		Last Modified: Tue, 14 Apr 2026 20:45:36 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a1e771e18596b4a6a21325fa9c8ba58c0cd6ef41905589f0c429a1eb6fc4ae`  
		Last Modified: Tue, 14 Apr 2026 20:56:38 GMT  
		Size: 1.7 KB (1701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f035e9426219c329035567349ab998b0dde688dfb52cd6bf633f60cd8cc09c1c`  
		Last Modified: Tue, 14 Apr 2026 20:56:40 GMT  
		Size: 36.0 MB (36026137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adffc93d29cb23804cf1671767e9de69e49c13e84c31f90223d68a7b642128c`  
		Last Modified: Tue, 14 Apr 2026 20:56:42 GMT  
		Size: 128.5 MB (128469406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868138e0c0a8561075c875e3442d1fe4259d0507249dd6ede1159829b3353487`  
		Last Modified: Tue, 14 Apr 2026 20:56:39 GMT  
		Size: 59.5 KB (59518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:f49ba18034945f2edd1a98d00ab31d4384fb610b8eec1f271f95bbf08f9ddf50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5357858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f2bd6c1c087047847e5f7c3c86ef37daf31f76c6828424a61f9cb7a03758bc`

```dockerfile
```

-	Layers:
	-	`sha256:6da3df8c26a293646cfcf059401f23638c797f8be944644c4c208fe889a9c327`  
		Last Modified: Tue, 14 Apr 2026 20:56:39 GMT  
		Size: 5.3 MB (5334106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcaaac228316639db881d64d445d3e5002f580ae4cd80dea1e9c0b567c62f5fa`  
		Last Modified: Tue, 14 Apr 2026 20:56:39 GMT  
		Size: 23.8 KB (23752 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:baa09f5a953f99e401da1ce38475769ba2536e45d2a6272d953d7b4c6754e9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.2 MB (373231928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbd137a3ca8bea04fda2f34d4bbd348edd796c30c87fe38a160f660e0cab658`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 13 Apr 2026 18:29:33 GMT
ENV container oci
# Mon, 13 Apr 2026 18:29:34 GMT
COPY dir:24fb0b263f289ef569c594958817053360bec0e0bfe2720b67eb4bf6d63e4515 in /      
# Mon, 13 Apr 2026 18:29:34 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 18:29:34 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 18:29:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 18:29:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 18:29:34 GMT
COPY file:7062c8f1fa2df3b89f0d90bf3890fde04fbbd54d614aefabecd07515e8bba176 in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:29:34 GMT
COPY file:7062c8f1fa2df3b89f0d90bf3890fde04fbbd54d614aefabecd07515e8bba176 in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:29:35 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "org.opencontainers.image.revision"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "build-date"="2026-04-13T18:29:23Z" "org.opencontainers.image.created"="2026-04-13T18:29:23Z" "release"="1776104705"org.opencontainers.image.revision=49cc6237764cacc4684bc968dd9fc53fb8abd12c,org.opencontainers.image.created=2026-04-13T18:29:23Z
# Tue, 14 Apr 2026 20:44:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Apr 2026 20:44:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 20:44:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Apr 2026 20:44:11 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 14 Apr 2026 20:44:11 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 14 Apr 2026 20:45:08 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 14 Apr 2026 20:45:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 14 Apr 2026 20:45:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Apr 2026 20:45:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Apr 2026 20:45:12 GMT
CMD ["jshell"]
# Tue, 14 Apr 2026 20:57:47 GMT
CMD ["gradle"]
# Tue, 14 Apr 2026 20:57:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 14 Apr 2026 20:57:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 14 Apr 2026 20:57:47 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 14 Apr 2026 20:57:50 GMT
WORKDIR /home/gradle
# Tue, 14 Apr 2026 20:58:05 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 14 Apr 2026 20:58:05 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 14 Apr 2026 20:58:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 14 Apr 2026 20:59:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 14 Apr 2026 20:59:41 GMT
USER gradle
# Tue, 14 Apr 2026 20:59:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 14 Apr 2026 20:59:43 GMT
USER root
```

-	Layers:
	-	`sha256:a8de600aa1d03790e68a950fc8a9160a10a53282e2415c939e6f6e1b5180c553`  
		Last Modified: Tue, 14 Apr 2026 00:13:55 GMT  
		Size: 44.4 MB (44444159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eea7503b93e046e3992230236cc9f313ea26fd31522ce2a84d764d8f98a753d`  
		Last Modified: Tue, 14 Apr 2026 20:44:47 GMT  
		Size: 32.8 MB (32849099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e6b6fd91f7e9fc55ff60b6f38c767be21fdcb566b6b7b1638958319d97e14c`  
		Last Modified: Tue, 14 Apr 2026 20:45:44 GMT  
		Size: 129.5 MB (129499207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12db4c175ab3e86f31f3abd8f859970116e3aa96a1c9ffafd1e59dc0820f2b2`  
		Last Modified: Tue, 14 Apr 2026 20:45:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02baed26fbd11a809fbe16668017f567ef63d2436ab10d3efaf14bbdb67d6cb3`  
		Last Modified: Tue, 14 Apr 2026 20:45:38 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71087b66eaa2f76f12caf597d5fed16b75f4ab857ee4c7597974fb31fcad209`  
		Last Modified: Tue, 14 Apr 2026 20:58:53 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1380863ad69753ee4d7dc8af873bd368583d85d0a087b63f3f23325aaa7bd35e`  
		Last Modified: Tue, 14 Apr 2026 20:58:56 GMT  
		Size: 37.9 MB (37930855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1a2bd8f46a08946d5f2ac76f777c41aa60a10913a1e2e8d1d3e69c621d8e97`  
		Last Modified: Tue, 14 Apr 2026 21:00:26 GMT  
		Size: 128.5 MB (128469424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2e94e395ab914f6adb13025db17acffcdb88f1f6be787ba1d2a1dcc6aff33e`  
		Last Modified: Tue, 14 Apr 2026 21:00:23 GMT  
		Size: 35.0 KB (35013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:45fc525ec05a3e3e5acb4929717e4f7cf4cdf096615e255912f0d6f6b7bc6038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979d8dc945f0649ef3f9bf36655c3761445d67a66228c6362070e0871e7fcdf3`

```dockerfile
```

-	Layers:
	-	`sha256:c85423b9cd14135b0ef3750fa635f192fcc5cfb58c83846ca2b33c2c23f282f2`  
		Last Modified: Tue, 14 Apr 2026 21:00:22 GMT  
		Size: 5.3 MB (5330786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0274cfc1f41b55d9dac0d37accdcf6957e688c985a7f06a02a9f7f2201d75d59`  
		Last Modified: Tue, 14 Apr 2026 21:00:22 GMT  
		Size: 23.6 KB (23641 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-ubi9` - linux; s390x

```console
$ docker pull gradle@sha256:ea6aa06871581bf9359b2334e4079803ad08a79b80970f8617c29b5919fe0c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.3 MB (356316441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc401a0b2914ae7674802db6057b9d44f9d5de3ea7ebfab2fc10628f4478548c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Apr 2026 18:35:03 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 18:35:03 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 18:35:03 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 18:35:03 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 13 Apr 2026 18:35:03 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 18:35:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 13 Apr 2026 18:35:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:35:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:35:03 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 13 Apr 2026 18:35:03 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 18:35:03 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 13 Apr 2026 18:35:03 GMT
ENV container oci
# Mon, 13 Apr 2026 18:35:04 GMT
COPY dir:aad81c97bb1c65f7a47ee3ef6c9d703278e603b565bbb15c18d20e040058016c in /      
# Mon, 13 Apr 2026 18:35:04 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 18:35:04 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 18:35:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 18:35:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 18:35:04 GMT
COPY file:936893ec4ec7da36a797e7c4e078694c2e39d7f412ff09f777a9236ebad6a5e4 in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:35:04 GMT
COPY file:936893ec4ec7da36a797e7c4e078694c2e39d7f412ff09f777a9236ebad6a5e4 in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:35:04 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "org.opencontainers.image.revision"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "build-date"="2026-04-13T18:34:52Z" "org.opencontainers.image.created"="2026-04-13T18:34:52Z" "release"="1776104705"org.opencontainers.image.revision=49cc6237764cacc4684bc968dd9fc53fb8abd12c,org.opencontainers.image.created=2026-04-13T18:34:52Z
# Tue, 14 Apr 2026 20:44:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Apr 2026 20:44:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 20:44:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Apr 2026 20:44:14 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 14 Apr 2026 20:44:14 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 14 Apr 2026 20:44:21 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 14 Apr 2026 20:44:23 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 14 Apr 2026 20:44:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Apr 2026 20:44:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Apr 2026 20:44:23 GMT
CMD ["jshell"]
# Tue, 14 Apr 2026 20:56:20 GMT
CMD ["gradle"]
# Tue, 14 Apr 2026 20:56:20 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 14 Apr 2026 20:56:20 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 14 Apr 2026 20:56:20 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 14 Apr 2026 20:56:20 GMT
WORKDIR /home/gradle
# Tue, 14 Apr 2026 20:56:24 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 14 Apr 2026 20:56:24 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 14 Apr 2026 20:56:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 14 Apr 2026 20:56:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 14 Apr 2026 20:56:29 GMT
USER gradle
# Tue, 14 Apr 2026 20:56:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 14 Apr 2026 20:56:29 GMT
USER root
```

-	Layers:
	-	`sha256:188bc35e04514e4f35552e12dec8be6787ac365d49a3ea7fa542d4acf61bfd45`  
		Last Modified: Tue, 14 Apr 2026 00:13:48 GMT  
		Size: 38.1 MB (38114710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ae9687a0b2d77e6f626096a581f6657be9436e53837fecdd37bd78516ce7aa`  
		Last Modified: Tue, 14 Apr 2026 20:44:47 GMT  
		Size: 30.4 MB (30388978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e6141d996581c02d418d7fced5d885f95e9857813ce0aa81283cef5fe4f54f`  
		Last Modified: Tue, 14 Apr 2026 20:44:49 GMT  
		Size: 123.0 MB (122972667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f659d1bca244f7dcbe2311334cd7d74b483b44257e3b5377d01c721b4800664`  
		Last Modified: Tue, 14 Apr 2026 20:44:46 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423e9468fdedbdf89c99f9e0e1cee9f199858b79d56365aea5ced004a41ed6ef`  
		Last Modified: Tue, 14 Apr 2026 20:44:46 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0194f40839bbc863180ff2379e6f47eca92f2072c2a1eed935be2cab484d37`  
		Last Modified: Tue, 14 Apr 2026 20:56:52 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fa6dd013a835796d0704201e13568da4058bc38421508584b4a4ecfd4b593d`  
		Last Modified: Tue, 14 Apr 2026 20:56:53 GMT  
		Size: 36.3 MB (36331502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e462fddffeb03ba748715137435aa904b2cc84d52833bc42a088e5f40993563`  
		Last Modified: Tue, 14 Apr 2026 20:56:57 GMT  
		Size: 128.5 MB (128469423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd99d12376272ac87da401b73088b1194bde81dd0b00f677b732bc2145661207`  
		Last Modified: Tue, 14 Apr 2026 20:56:55 GMT  
		Size: 35.0 KB (34997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:8aab057227c4dfe9c5f20635642ab7483e74f563bc3b9aaa0a5847be83f4cfda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5344270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4679d3e2656c92fd4fb61342af6b9166761eda20c35764728c6d57d3559aa51c`

```dockerfile
```

-	Layers:
	-	`sha256:4336f884a14e157ec5a3ba04a3853f05ef9b2c0bede93360d4d65dd43a78df89`  
		Last Modified: Tue, 14 Apr 2026 20:56:55 GMT  
		Size: 5.3 MB (5320691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f09c54fa69f6451ebb16e60d530543524aefa3f0e88c16ab7850176bfa8bac4`  
		Last Modified: Tue, 14 Apr 2026 20:56:55 GMT  
		Size: 23.6 KB (23579 bytes)  
		MIME: application/vnd.in-toto+json
