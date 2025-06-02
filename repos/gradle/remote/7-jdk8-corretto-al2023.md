## `gradle:7-jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:b8fe747b218c55f7bb002621fad7a49f2f0816c542ad8247836ad4427257e6c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:fc00681d9ba645097a7035c82052d7ab621df6f0df643a232928360446be11c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.1 MB (570084295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4477626159fb8232456435f60cadc3e4e8de651a5a8a80a4139bd341bb3ad0ab`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=1.8.0_452.b09-2
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=1.8.0_452.b09-2
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 29 May 2025 19:53:06 GMT
CMD ["gradle"]
# Thu, 29 May 2025 19:53:06 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 29 May 2025 19:53:06 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 29 May 2025 19:53:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 29 May 2025 19:53:06 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 29 May 2025 19:53:06 GMT
WORKDIR /home/gradle
# Thu, 29 May 2025 19:53:06 GMT
ENV GRADLE_VERSION=7.6.4
# Thu, 29 May 2025 19:53:06 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Thu, 29 May 2025 19:53:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 29 May 2025 19:53:06 GMT
USER gradle
# Thu, 29 May 2025 19:53:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 29 May 2025 19:53:06 GMT
USER root
```

-	Layers:
	-	`sha256:d680ca3f92ab1808f4ae68645f57801d7a408a68d8d17cd7b28da6cfad1ad3d7`  
		Last Modified: Wed, 14 May 2025 01:42:44 GMT  
		Size: 53.6 MB (53614702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fe6cf55dc3adf66743afc67d7bcfc0ce974e2646080ac95d6c204123e58662`  
		Last Modified: Mon, 19 May 2025 23:37:53 GMT  
		Size: 330.7 MB (330665928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6008f4455eaa77ef078ad84045722bd10c757f969b5ac019a9e6cc893bd87`  
		Last Modified: Mon, 02 Jun 2025 16:49:13 GMT  
		Size: 63.0 MB (63016252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3805e6fbc96262c1951f635d850a41ed629326b50519ab34bf8e8fdd3cf3c320`  
		Last Modified: Mon, 02 Jun 2025 16:49:12 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de0f78c9bb7c75547cad9e7316ec1e1eb3e1c87bb6fd5eddc7774331ee4e350`  
		Last Modified: Mon, 02 Jun 2025 16:49:14 GMT  
		Size: 122.7 MB (122730527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a903f36adef7dd9531ff4368542a41b258d17b731832206077d980001a17e2`  
		Last Modified: Mon, 02 Jun 2025 16:49:12 GMT  
		Size: 54.9 KB (54905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:fe6e9486cb39259cd388599f3bfca5a111b15bc00f158995cf6b7e4360fed3ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18002335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec524b13ebbf6323a70ccf71f92384db0400dce7eb4be2f00e8081703d6d8237`

```dockerfile
```

-	Layers:
	-	`sha256:2aa79719e9f2b9ba31217e55201f3b76c44c1f652703977a607169d5aa05ea76`  
		Last Modified: Mon, 02 Jun 2025 16:49:12 GMT  
		Size: 18.0 MB (17981412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a4d0b2738f04ff2e12c67508581bf57c771dd5c441919df3d164867ff10c977`  
		Last Modified: Mon, 02 Jun 2025 16:49:12 GMT  
		Size: 20.9 KB (20923 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b29d7baa1e4aa6b5988512599f8dec00a09e3d38de1746c1b228de0fbcab4e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.2 MB (365217786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a10241cc494e262bfdd69dc8da8c60d5239e863ebf61e977d36b46f2450f5a`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 30 Mar 2025 18:23:11 GMT
COPY /rootfs/ / # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["/bin/bash"]
# Sun, 30 Mar 2025 18:23:11 GMT
ARG version=1.8.0_452.b09-2
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: version=1.8.0_452.b09-2
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
ENV LANG=C.UTF-8
# Sun, 30 Mar 2025 18:23:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["gradle"]
# Sun, 30 Mar 2025 18:23:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 30 Mar 2025 18:23:11 GMT
WORKDIR /home/gradle
# Sun, 30 Mar 2025 18:23:11 GMT
ENV GRADLE_VERSION=7.6.4
# Sun, 30 Mar 2025 18:23:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
USER gradle
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
USER root
```

-	Layers:
	-	`sha256:b9b2e8e61af6809d54a17702fba1fe6b09b2947a739f90536e2d0bb6a4ed34cb`  
		Last Modified: Wed, 14 May 2025 01:42:43 GMT  
		Size: 52.6 MB (52565737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ba910b575edfd05c7f13065f2a17cff35d62e2af5009fcfda96edd05eb5b25`  
		Last Modified: Mon, 19 May 2025 23:47:42 GMT  
		Size: 117.8 MB (117849549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5d3f3c342c5a61fea1be9d7e82a6e0a800aae741d73c389ed6f498f6195e74`  
		Last Modified: Tue, 20 May 2025 00:30:33 GMT  
		Size: 72.0 MB (72010762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a965c5ccfa78310147421e6af0ce77c47c28484b26c7fa3e2859304535ddcdc5`  
		Last Modified: Tue, 20 May 2025 00:30:31 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8085be7e6405a38887d28ff9a938e37c61c9aabb086a0e6d1620f9711c56932f`  
		Last Modified: Tue, 20 May 2025 00:34:52 GMT  
		Size: 122.7 MB (122730526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9310ce79c4752f94cb4e6acbffe7b000b84249b15d9408b9fb60b5ee017bf6ce`  
		Last Modified: Tue, 20 May 2025 00:34:46 GMT  
		Size: 59.5 KB (59530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:1957052a46a4585d3be365485825b95d6eea150191be91dd8f024999e3f11cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11097792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25130c420323eeacea027bef7f729d10fcf59ceb12b9b58635a6861be4e208ff`

```dockerfile
```

-	Layers:
	-	`sha256:253bec89d9d2ab1aee568e22b77f454dd8083c75708c41256ac3f2340078f1e7`  
		Last Modified: Tue, 20 May 2025 00:34:47 GMT  
		Size: 11.1 MB (11078370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f12583754253f3f8acb1e696f14dd6494d9f78301d656e6b903526a64516b137`  
		Last Modified: Tue, 20 May 2025 00:34:46 GMT  
		Size: 19.4 KB (19422 bytes)  
		MIME: application/vnd.in-toto+json
