## `gradle:8-jdk11-corretto`

```console
$ docker pull gradle@sha256:86a5acee07a1e88d883396c396aecc7b4c51f26a7f9e9e18d6435045a4ff63f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:6bf229565071fed93d2020fc163604b2e5f943e3956b7c509ea63bbfbd4b324d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.9 MB (430879806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6549c00a56aa0a36b7420b13b009dec24a69875d0c71a8f7c0a3280d55e2538a`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:49 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:49 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:30:59 GMT
ARG version=11.0.30.7-1
# Tue, 10 Feb 2026 18:30:59 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:30:59 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:30:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 10 Feb 2026 19:06:57 GMT
CMD ["gradle"]
# Tue, 10 Feb 2026 19:06:57 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 10 Feb 2026 19:06:57 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 10 Feb 2026 19:06:57 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 10 Feb 2026 19:06:57 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 10 Feb 2026 19:06:57 GMT
WORKDIR /home/gradle
# Tue, 10 Feb 2026 19:06:57 GMT
ENV GRADLE_VERSION=8.14.4
# Tue, 10 Feb 2026 19:06:57 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Tue, 10 Feb 2026 19:07:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 10 Feb 2026 19:07:00 GMT
USER gradle
# Tue, 10 Feb 2026 19:07:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 10 Feb 2026 19:07:00 GMT
USER root
```

-	Layers:
	-	`sha256:3ffbc2e8833044834ccfc60c99f6275f3632718226c6ef0c9706b41890795123`  
		Last Modified: Mon, 09 Feb 2026 18:58:55 GMT  
		Size: 54.0 MB (54038228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4813123a6ec9537c4a8ad81d395a04d6cda2fb38203e651b03c910f6504f12a6`  
		Last Modified: Tue, 10 Feb 2026 18:31:19 GMT  
		Size: 153.4 MB (153363419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13992f241f9637305ba9962be5f8f0d0dfaa57aab773fafc3c8de852dd2464a9`  
		Last Modified: Tue, 10 Feb 2026 19:07:28 GMT  
		Size: 86.0 MB (86033291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babb79e51c8461dcc6ba3c58bf90240d65ed2d327fe7cd7969a548acb6a09250`  
		Last Modified: Tue, 10 Feb 2026 19:07:24 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d82f1f6c2786182b074ffec925181dd73085b5ceae7118afb1a4f1b4748813`  
		Last Modified: Tue, 10 Feb 2026 19:07:29 GMT  
		Size: 137.4 MB (137388294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73546cc41512dc58ee62bf443b6eb16166dc00f3e9832aa22acbe774c42c052e`  
		Last Modified: Tue, 10 Feb 2026 19:07:24 GMT  
		Size: 54.9 KB (54893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:673f51b6dea7dc84a5cbaa04dd76b6d033b6f4349220e2d51acbfbf6b3f80f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11387533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df5daec558493752552d9f83182846322a2f3b7903ea39bbf6e856fa7d404fe`

```dockerfile
```

-	Layers:
	-	`sha256:ce533e45c00123cae4e3c1a7bc086c6ae3f21cec4e13abf27296679e8589e8ae`  
		Last Modified: Tue, 10 Feb 2026 19:07:25 GMT  
		Size: 11.4 MB (11366011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f59f3efc3608c46221b1e6e0b66fd5d0d60435c05917288fa3d3917673f9b8d`  
		Last Modified: Tue, 10 Feb 2026 19:07:25 GMT  
		Size: 21.5 KB (21522 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:79bbed71da808bb9238ea13488688cd9269645135db72a99b4c1fff4c984c9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.8 MB (427801814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ad9d27c50bf83be9d9e1a7eb2201ea081346f7195fdc299013e0644fb936ed`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:36 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:36 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:30:51 GMT
ARG version=11.0.30.7-1
# Tue, 10 Feb 2026 18:30:51 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:30:51 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:30:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 10 Feb 2026 19:09:56 GMT
CMD ["gradle"]
# Tue, 10 Feb 2026 19:09:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 10 Feb 2026 19:09:56 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 10 Feb 2026 19:09:56 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 10 Feb 2026 19:09:56 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 10 Feb 2026 19:09:56 GMT
WORKDIR /home/gradle
# Tue, 10 Feb 2026 19:09:56 GMT
ENV GRADLE_VERSION=8.14.4
# Tue, 10 Feb 2026 19:09:56 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Tue, 10 Feb 2026 19:09:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 10 Feb 2026 19:09:59 GMT
USER gradle
# Tue, 10 Feb 2026 19:09:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 10 Feb 2026 19:09:59 GMT
USER root
```

-	Layers:
	-	`sha256:72831a4cffd207c00f002b53208af67cc59cf3af51b98b118c11c230a7926a2d`  
		Last Modified: Mon, 09 Feb 2026 20:01:25 GMT  
		Size: 52.9 MB (52918211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe09cbb5e7a2b065a6b8b1308384deff3a73a806922a2cad78f5af69f4a16aff`  
		Last Modified: Tue, 10 Feb 2026 18:31:13 GMT  
		Size: 151.9 MB (151920991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3176ccd592a0b637418006aab02b989f41745353c64627cc4f6f5f5459ceb1a2`  
		Last Modified: Tue, 10 Feb 2026 19:10:30 GMT  
		Size: 85.5 MB (85513135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45970162399108d94db304e6202a95fd517ef41785435d01a0a3381534c69afd`  
		Last Modified: Tue, 10 Feb 2026 19:10:26 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b75f6f6b96c45011dd81246d009c13d5f261022ecfe9832579fb59134d5a97`  
		Last Modified: Tue, 10 Feb 2026 19:10:31 GMT  
		Size: 137.4 MB (137388272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424a02c946a21fe882525b4d24c926a70caa4ac6370549b7e787d0e1876bc17a`  
		Last Modified: Tue, 10 Feb 2026 19:10:27 GMT  
		Size: 59.5 KB (59521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:391471b1cc6884119a80c4dd23f4b2a33b449d3cafa2d6002a98a51758e288da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11387573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a905200f8a5a3a1581e269dc060ecc5da61d99cb2dc70038e09dd624ddace1b5`

```dockerfile
```

-	Layers:
	-	`sha256:8ffd6c000357a26942406f94b73480d1382c7deb9eee4dfb7bd9833e9895bc1b`  
		Last Modified: Tue, 10 Feb 2026 19:10:27 GMT  
		Size: 11.4 MB (11365854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc529699bf2440329ff5ff6241a0c280eeeb7f7cd8a80730b3f05e84b82d7e47`  
		Last Modified: Tue, 10 Feb 2026 19:10:26 GMT  
		Size: 21.7 KB (21719 bytes)  
		MIME: application/vnd.in-toto+json
