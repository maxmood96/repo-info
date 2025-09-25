## `gradle:7-jdk11-corretto-al2023`

```console
$ docker pull gradle@sha256:c145c0b27325047d0005206b7cd97521232a5531fdd030b56f335e970ff84bfa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk11-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:51e4605e7cdcb828376977da5d0c989340c540a889c62eea79c5ccdbb54970bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.2 MB (422171769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebf6a55cb34fcfcc23bd33f2b3d04bbbcc72b56fb132349e61343c495e4f43f`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 10 Sep 2025 15:58:43 GMT
COPY /rootfs/ / # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
CMD ["/bin/bash"]
# Wed, 10 Sep 2025 15:58:43 GMT
ARG version=11.0.28.6-1
# Wed, 10 Sep 2025 15:58:43 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
ENV LANG=C.UTF-8
# Wed, 10 Sep 2025 15:58:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 10 Sep 2025 15:58:43 GMT
CMD ["gradle"]
# Wed, 10 Sep 2025 15:58:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 10 Sep 2025 15:58:43 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 10 Sep 2025 15:58:43 GMT
WORKDIR /home/gradle
# Wed, 10 Sep 2025 15:58:43 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 10 Sep 2025 15:58:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 10 Sep 2025 15:58:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
USER gradle
# Wed, 10 Sep 2025 15:58:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
USER root
```

-	Layers:
	-	`sha256:b6baa302384dc877580d7e1080dcca1ed66d9d3b38afc9fcc29c360239e3e362`  
		Last Modified: Tue, 16 Sep 2025 20:50:40 GMT  
		Size: 54.0 MB (54005280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a85c53f5c61cce6dc0162eb66e7a7e14c47b0962aa13f24a73b943f9d74e012`  
		Last Modified: Thu, 25 Sep 2025 03:14:46 GMT  
		Size: 154.1 MB (154074648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d358d2301cab06d6b24841ae54a8ff2f4896d5f5b54ef9cc0d0ac202670d403a`  
		Last Modified: Thu, 25 Sep 2025 03:50:14 GMT  
		Size: 85.6 MB (85565833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221f92567881e0be621a630d16d26df86b81173af5358be490dbf7b16972f003`  
		Last Modified: Thu, 25 Sep 2025 03:49:54 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9458f2e25fd4ea9da1f011b29841a8fbaf9aa2ae39728d9079597f047e3772`  
		Last Modified: Thu, 25 Sep 2025 22:30:10 GMT  
		Size: 128.5 MB (128469415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7508624c744f880437ec2404a59a966ba24b86aa056e2ae010c3134318aad2`  
		Last Modified: Thu, 25 Sep 2025 03:49:55 GMT  
		Size: 54.9 KB (54912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:fc76d87018b4dbbf7e7eb817ee20c9757516973721947e70b320d743a8a107e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11268538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:909c88b807bcf735a41e8bbdb1257c6cf96e57efc8ef16d48e032d32d13420db`

```dockerfile
```

-	Layers:
	-	`sha256:ad3366cb736bf333c9e6f50184712ad0a2b4d55d7b715993cebc7894aa286e0a`  
		Last Modified: Thu, 25 Sep 2025 05:18:33 GMT  
		Size: 11.2 MB (11247624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4610006e81d2f30a157ba3af3e5ae94d6b3969cf7e0de8b728d89d3ac07f74`  
		Last Modified: Thu, 25 Sep 2025 05:18:34 GMT  
		Size: 20.9 KB (20914 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:036c370dd9498824b4d362c9928f6e74771a6aa59ae2ebff889c4e6d768d1ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.1 MB (419095004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347136badffd3f9d22176027e213634851da948ffb52013ef16dfa3effb0d531`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 10 Sep 2025 15:58:43 GMT
COPY /rootfs/ / # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
CMD ["/bin/bash"]
# Wed, 10 Sep 2025 15:58:43 GMT
ARG version=11.0.28.6-1
# Wed, 10 Sep 2025 15:58:43 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
ENV LANG=C.UTF-8
# Wed, 10 Sep 2025 15:58:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 10 Sep 2025 15:58:43 GMT
CMD ["gradle"]
# Wed, 10 Sep 2025 15:58:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 10 Sep 2025 15:58:43 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 10 Sep 2025 15:58:43 GMT
WORKDIR /home/gradle
# Wed, 10 Sep 2025 15:58:43 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 10 Sep 2025 15:58:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 10 Sep 2025 15:58:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
USER gradle
# Wed, 10 Sep 2025 15:58:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
USER root
```

-	Layers:
	-	`sha256:202438f011bd656c28426fbd92ff7e7030b77e67ebafd3bec95dbce9626db73c`  
		Last Modified: Tue, 16 Sep 2025 22:16:03 GMT  
		Size: 52.9 MB (52899438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba67c498ac860f8cfec44394c18e432ed8fc284cdcd5fac40c1f6a02566a52e`  
		Last Modified: Wed, 24 Sep 2025 22:11:32 GMT  
		Size: 152.6 MB (152579454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e43b2b9ee2bca5500dd36e5a1469109ba1107c1e435f53f19858876d84bb15`  
		Last Modified: Wed, 24 Sep 2025 22:13:16 GMT  
		Size: 85.1 MB (85085498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1b6051a5457effd17c474ebe007de8ca047b7e2c824165e750f0b4bfcb2911`  
		Last Modified: Wed, 24 Sep 2025 22:13:13 GMT  
		Size: 1.6 KB (1643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670e93ba4af0fd28c576d6fd4240c43750f133ef036db47f6981e12dbc6e85aa`  
		Last Modified: Thu, 25 Sep 2025 12:47:20 GMT  
		Size: 128.5 MB (128469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51d316d08a8c2791826c2a98aac1c06baf699177fee94493952637418ab8c1f`  
		Last Modified: Wed, 24 Sep 2025 22:13:12 GMT  
		Size: 59.5 KB (59522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:82b7409556a31181badc2aee5374c109c9d98afce40829a4a575e74a9820cf2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11268533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92d6845518e65b2b68bd5966441f8ff154ee8bab96bf8f9745138c64d98cbb9`

```dockerfile
```

-	Layers:
	-	`sha256:272f4fec477c1df1fc6b94819d4df05537d0bb64a1e0929390ea09fded8332d0`  
		Last Modified: Thu, 25 Sep 2025 02:18:36 GMT  
		Size: 11.2 MB (11247447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80eea933647e9d5c05177f6413c4b0b16c82a18267af7f1979ae5d8bb80a1837`  
		Last Modified: Thu, 25 Sep 2025 02:18:36 GMT  
		Size: 21.1 KB (21086 bytes)  
		MIME: application/vnd.in-toto+json
