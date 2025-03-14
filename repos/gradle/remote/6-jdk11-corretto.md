## `gradle:6-jdk11-corretto`

```console
$ docker pull gradle@sha256:97fda58db83a6cc4ab3a498b97c1f4c1fd593ab3f9250c68c6d58d2ad58f15ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:a639171a7979432287cba1370a778b85fb16b89563b41e97267fca05ab43b392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.4 MB (387417924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c43f7459cadc55b08558666d167dde7a7b5b6e3d698caa046a05e4d4d7a600`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 04 Mar 2025 19:21:18 GMT
CMD ["gradle"]
# Tue, 04 Mar 2025 19:21:18 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 04 Mar 2025 19:21:18 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 04 Mar 2025 19:21:18 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 04 Mar 2025 19:21:18 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 04 Mar 2025 19:21:18 GMT
WORKDIR /home/gradle
# Tue, 04 Mar 2025 19:21:18 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 04 Mar 2025 19:21:18 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 04 Mar 2025 19:21:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 04 Mar 2025 19:21:18 GMT
USER gradle
# Tue, 04 Mar 2025 19:21:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 04 Mar 2025 19:21:18 GMT
USER root
```

-	Layers:
	-	`sha256:9ec3516d0f4b07a63d66d796b21f72a416a1968c512c2a8214a11acbb4bf7d0e`  
		Last Modified: Fri, 07 Mar 2025 22:16:15 GMT  
		Size: 53.1 MB (53126876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbeb8bd497d804215f38242789ad5959c420796173892a92e1855475217f5628`  
		Last Modified: Thu, 13 Mar 2025 22:53:15 GMT  
		Size: 153.9 MB (153895866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3421881bdaeedd98083b9b5d3bd6d21591ac75c6bd5c2601d2fb37f605d840`  
		Last Modified: Thu, 13 Mar 2025 23:09:42 GMT  
		Size: 72.3 MB (72265559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33049c15fcc7fa3bc345015bad09830d630bfe777351e92fc6cce93df8cb9ed`  
		Last Modified: Thu, 13 Mar 2025 23:09:41 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a8550cf13e8b5d830e701fa2f63e6bc27b4a6e4eccd4599d1aa45e4582fe7b`  
		Last Modified: Thu, 13 Mar 2025 23:09:43 GMT  
		Size: 107.7 MB (107696664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc098e977c1d04f18c98e7a494bb227ecb57215b5aa84c812c4d44f259ca7884`  
		Last Modified: Thu, 13 Mar 2025 23:09:42 GMT  
		Size: 431.3 KB (431282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:5d688a991cc7e6679463b006b02c84f8ef2254ca94b842e8234ba68291e6d111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10683304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72494f725f18263eb32e4404f643638bba7a6635f96b2f9cac5eb2aa2760f499`

```dockerfile
```

-	Layers:
	-	`sha256:d55c3f3da37145b5732607ef5d090088c65db1ce6a3f95fcbd92e31e2f72c46b`  
		Last Modified: Thu, 13 Mar 2025 23:09:42 GMT  
		Size: 10.7 MB (10664051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30d8f8dbeb668fa000e9ce4304f3be7fdb04f16dc26cb56e2ac74ae35a917ea`  
		Last Modified: Thu, 13 Mar 2025 23:09:42 GMT  
		Size: 19.3 KB (19253 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b51ffb0cd1bd4bc5104a7b19d2625c4d343e5e44243d22d5205055ca9009e5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.7 MB (384696547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8deaaa6ace876699ea5eef84a28a6423ccb39a08fc5731bf566851ce724ed8ed`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 04 Mar 2025 19:21:18 GMT
CMD ["gradle"]
# Tue, 04 Mar 2025 19:21:18 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 04 Mar 2025 19:21:18 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 04 Mar 2025 19:21:18 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 04 Mar 2025 19:21:18 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 04 Mar 2025 19:21:18 GMT
WORKDIR /home/gradle
# Tue, 04 Mar 2025 19:21:18 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 04 Mar 2025 19:21:18 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 04 Mar 2025 19:21:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 04 Mar 2025 19:21:18 GMT
USER gradle
# Tue, 04 Mar 2025 19:21:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 04 Mar 2025 19:21:18 GMT
USER root
```

-	Layers:
	-	`sha256:a8ae4757b69337068f85c03c42e1020f67d8e126d57f500162c47221848c93bd`  
		Last Modified: Sat, 08 Mar 2025 02:26:21 GMT  
		Size: 52.2 MB (52245978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168ba35638fff7ccd4f063f3b1dd6993ddfa04f2270bb8025ddeb210534e9384`  
		Last Modified: Fri, 14 Mar 2025 02:21:02 GMT  
		Size: 152.4 MB (152385379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96276a236f5fb30a19f72f4bd0b53dab564b5d4501aa1c4e36f9191348f7f537`  
		Last Modified: Fri, 14 Mar 2025 20:49:21 GMT  
		Size: 71.9 MB (71941815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9beb558c86a63d9da3cacec24a73889de31f5bd60fd0de6f7a783bc9aa2a502e`  
		Last Modified: Fri, 14 Mar 2025 20:49:18 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f785affe64a8495d42691b675d5588ad4845f89ff23058ec8686bebedce439`  
		Last Modified: Fri, 14 Mar 2025 21:03:02 GMT  
		Size: 107.7 MB (107696666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af87e8a428f2b3e3fbb03355e75a60e0463943d7a018ed39677d16cc6fccf1c`  
		Last Modified: Fri, 14 Mar 2025 21:02:59 GMT  
		Size: 425.0 KB (425029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:4e049bc2c8ecc28160e60b8d3fc88630d6e7551be87f8b54aa29b2480ccb58c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10683297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1031210ce1440bffda7bcbc44a49d6b95f6c4f427656ae75d6080e7270b4afe7`

```dockerfile
```

-	Layers:
	-	`sha256:aa14d661be3351fb8093f25c9a43be8af77e483f43dec345e27468115509bacf`  
		Last Modified: Fri, 14 Mar 2025 21:02:59 GMT  
		Size: 10.7 MB (10663870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:280e02f2a5cd07542691775b8d505786b91e270d0a0f084ea55f03d5fd0d7c6a`  
		Last Modified: Fri, 14 Mar 2025 21:02:58 GMT  
		Size: 19.4 KB (19427 bytes)  
		MIME: application/vnd.in-toto+json
