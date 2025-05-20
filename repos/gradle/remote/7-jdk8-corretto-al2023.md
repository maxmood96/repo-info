## `gradle:7-jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:90ac02b8929e0e986d99b5531b7376da7536c0b0673e066950e9d1868da9453f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:6f547ff096892502ce3d14366e9c730a93937fa8413a64856df419f4f609ebb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.9 MB (558884147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb58c534f7495413938dfd94867a1602590f53ca34cf06e67a23bc0dfc5193ee`
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
	-	`sha256:d680ca3f92ab1808f4ae68645f57801d7a408a68d8d17cd7b28da6cfad1ad3d7`  
		Last Modified: Wed, 14 May 2025 01:42:44 GMT  
		Size: 53.6 MB (53614702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fe6cf55dc3adf66743afc67d7bcfc0ce974e2646080ac95d6c204123e58662`  
		Last Modified: Mon, 19 May 2025 23:37:53 GMT  
		Size: 330.7 MB (330665928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da055b1081b831533dbca113f7367a65c693647bd14b66f2c2dd6344a56d9d0`  
		Last Modified: Mon, 19 May 2025 23:47:32 GMT  
		Size: 51.8 MB (51816115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26866375637896947eeb5fa1376d5dc26622d63c6896c7eac545aa6d2ada1a38`  
		Last Modified: Mon, 19 May 2025 23:47:30 GMT  
		Size: 1.9 KB (1942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca9d67e6c87893e3bd3f50b4a2cc8134969cccf51ab0ed0e322fd4320ce1236`  
		Last Modified: Mon, 19 May 2025 23:47:34 GMT  
		Size: 122.7 MB (122730536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee4570fdc9df2fce70cd3dfd63631118a84dc5609bfb05d5f44f5fdd873d779`  
		Last Modified: Mon, 19 May 2025 23:47:31 GMT  
		Size: 54.9 KB (54892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:219f1788e4e65958280acf1737f52e608a1b3ad6f9d81248f0af609da411a852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17532810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2fc67d18fc924a1c9aa4b7e48b6aa58e936bacdcb4894a7a75976462fa533c`

```dockerfile
```

-	Layers:
	-	`sha256:53ecad847bfa27ca755a61b0ca2f49fd68c847bb0a1d1937c38edf878f5ffe9a`  
		Last Modified: Mon, 19 May 2025 23:47:31 GMT  
		Size: 17.5 MB (17513560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70ce81b07d88c276e8b3ece816956082eaea454c396b237b690592845ecaa858`  
		Last Modified: Mon, 19 May 2025 23:47:31 GMT  
		Size: 19.2 KB (19250 bytes)  
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
