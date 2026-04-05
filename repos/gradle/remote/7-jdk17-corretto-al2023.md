## `gradle:7-jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:d89a9b42e2629ae6c4831728668ddfc6416d79289b47c2ce4e37e7099a209ff6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:a15859b27681178dcc9b0369cec1f286b5889fd8061a4537664d803abdfdbac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.1 MB (426106978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6e9a90d0af6f301cfc928ad62421cda8f143c9f51bb67c46492749e5be9510`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:16 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:16 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:14:36 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 22:14:36 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:14:36 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:14:36 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:14:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 03 Apr 2026 23:12:08 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 23:12:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 23:12:08 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 23:12:08 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 23:12:08 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 23:12:08 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 23:12:08 GMT
ENV GRADLE_VERSION=7.6.6
# Fri, 03 Apr 2026 23:12:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Fri, 03 Apr 2026 23:12:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 23:12:10 GMT
USER gradle
# Fri, 03 Apr 2026 23:12:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 03 Apr 2026 23:12:11 GMT
USER root
```

-	Layers:
	-	`sha256:a2488c40110fb2b90385f44d9af6173894e14350935e38653aee164551cb70d6`  
		Last Modified: Thu, 02 Apr 2026 00:19:16 GMT  
		Size: 54.6 MB (54571303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa6c65371a2d0452e68a7849e65aa6fec9a2eacabd234c5f9ae4305aa623f8e`  
		Last Modified: Fri, 03 Apr 2026 22:14:58 GMT  
		Size: 156.9 MB (156911184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4783684c078b0fd37843f414c293e638a4b4035423b8aac89966e853787dceca`  
		Last Modified: Fri, 03 Apr 2026 23:12:40 GMT  
		Size: 86.1 MB (86098466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c373e31df933d9e99c4d4afb48c0f401446b424b0cd4ff54b055d0f77e3250`  
		Last Modified: Fri, 03 Apr 2026 23:12:35 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d42b8ca1349896014e78cf1f8e340bc2d23fdfcddbf2a9a47c027d925f5087d`  
		Last Modified: Fri, 03 Apr 2026 23:12:39 GMT  
		Size: 128.5 MB (128469439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f01a95d834138874bd62c65107883e66a34074d5b9f272124d8cb19e118eb0`  
		Last Modified: Fri, 03 Apr 2026 23:12:35 GMT  
		Size: 54.9 KB (54905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:e8851ace6eecd1717007bd07025c39a4d9df094a6cd75d91ee6435a9bb5af096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11279366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b6a7748bdb42a2b4dd34b8cecbbbb2b9d908cffdd68d6c13b0b07ada521fe9`

```dockerfile
```

-	Layers:
	-	`sha256:60a07063e65d382128bc3e970bd32832f93cb53f9a62299772b76fc5b3a6168a`  
		Last Modified: Fri, 03 Apr 2026 23:12:36 GMT  
		Size: 11.3 MB (11258653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e24712fbc31e0b29d0aae373f811bb49204aae9da4f22d61a4bf8dd96e1e629a`  
		Last Modified: Fri, 03 Apr 2026 23:12:35 GMT  
		Size: 20.7 KB (20713 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:8481a8d82865b86d31efcac4640fc54a2a2947cf33e6c705d03ed27e5a8375e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.3 MB (423307012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5cf3a01d911805507b3de09542ca35e75367b5c16040be3143ef2ece97d728`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:04 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:52:42 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 22:52:42 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:52:42 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:52:42 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:52:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 03 Apr 2026 23:12:42 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 23:12:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 23:12:42 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 23:12:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 23:12:42 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 23:12:42 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 23:12:42 GMT
ENV GRADLE_VERSION=7.6.6
# Fri, 03 Apr 2026 23:12:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Fri, 03 Apr 2026 23:12:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 23:12:45 GMT
USER gradle
# Fri, 03 Apr 2026 23:12:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 03 Apr 2026 23:12:45 GMT
USER root
```

-	Layers:
	-	`sha256:cf8ff26f8ca2e7db6c1eb2c69aec532f89cf3016cc84f77de00b260ba62b2ffc`  
		Last Modified: Thu, 02 Apr 2026 00:19:15 GMT  
		Size: 53.4 MB (53442825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a171146ed2608cfed7379a8e096372cbf936c9d64c321d3b501ba505f2694fb8`  
		Last Modified: Fri, 03 Apr 2026 22:53:07 GMT  
		Size: 155.7 MB (155728253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916c13ff07bd83e1bc75fb3738fc3722be2ee650228fa3cd121ba3904f3a7c5e`  
		Last Modified: Fri, 03 Apr 2026 23:13:17 GMT  
		Size: 85.6 MB (85605301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa0f3815592cda79a445bc48e85a4ae8fd9a22f9daa99afad92331ce1406e86`  
		Last Modified: Fri, 03 Apr 2026 23:13:13 GMT  
		Size: 1.6 KB (1643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa14be267ce217e9abbcf98d13d9d791fffe582aec7b409ae22fd9d278f7eca`  
		Last Modified: Fri, 03 Apr 2026 23:13:18 GMT  
		Size: 128.5 MB (128469445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bc9a3061c6bb8eee0a08b144662fd7e9234bd6f629ee8d0a74267139dbdeef`  
		Last Modified: Fri, 03 Apr 2026 23:13:13 GMT  
		Size: 59.5 KB (59513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:52712d7794d21c3b0db6ef9aa88c23ce90aac0ad9231673ab6a4b40834859398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11278517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:961d19c44a02778d1349f7738ecee29c81268510950a21cd6c5c9815c5de04aa`

```dockerfile
```

-	Layers:
	-	`sha256:73680a5daa34cf494cfbc6752b4cdc7c2329d608920128d559cffa491a72ca68`  
		Last Modified: Fri, 03 Apr 2026 23:13:14 GMT  
		Size: 11.3 MB (11257632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a6eb47f3636768f0cdd5fd3eb99bf1a49026b27f37ed3766a612cab316252aa`  
		Last Modified: Fri, 03 Apr 2026 23:13:13 GMT  
		Size: 20.9 KB (20885 bytes)  
		MIME: application/vnd.in-toto+json
