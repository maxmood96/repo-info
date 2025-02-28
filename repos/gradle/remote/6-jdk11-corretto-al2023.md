## `gradle:6-jdk11-corretto-al2023`

```console
$ docker pull gradle@sha256:6b1bdc1050a31e7419c9528dd27c682c438dd139c0924659e586a0f6bb339c7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk11-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:f47f1e0abebe1ed445fb67364b9d39491acd42630eb680e46da647e379e438a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.4 MB (387445493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:063b285e8e74a2d29b50e0d9b884ea628724a4ca75b71553f31df65a5572cd2f`
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
# Tue, 18 Feb 2025 21:10:38 GMT
CMD ["gradle"]
# Tue, 18 Feb 2025 21:10:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 18 Feb 2025 21:10:38 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 18 Feb 2025 21:10:38 GMT
WORKDIR /home/gradle
# Tue, 18 Feb 2025 21:10:38 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 18 Feb 2025 21:10:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 18 Feb 2025 21:10:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
USER gradle
# Tue, 18 Feb 2025 21:10:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
USER root
```

-	Layers:
	-	`sha256:0b097f308b6a69a495d5e5a13cf9ca5207eb7ed64da7124ffbd0d34037edf9bf`  
		Last Modified: Sat, 22 Feb 2025 01:44:44 GMT  
		Size: 53.2 MB (53151733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e40b02f5e94978994886dcd8f009fb4f6012f3b78983a79e5bdf3d3bd80f24`  
		Last Modified: Thu, 27 Feb 2025 21:08:29 GMT  
		Size: 153.9 MB (153895723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31265693f24bd3a8fedd318fbef56d27790c24811a788b869aa045a4b81e0f99`  
		Last Modified: Thu, 27 Feb 2025 22:08:58 GMT  
		Size: 72.3 MB (72268420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce870dc7433a77809a808cdc9155c1ee50c253a7e3a4bde98ba270d5cdca73dd`  
		Last Modified: Thu, 27 Feb 2025 22:08:56 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72114d6d1b963ad9fe967cc37cd4321cb2186c09dcfd67c618420b8139491ee4`  
		Last Modified: Thu, 27 Feb 2025 22:08:58 GMT  
		Size: 107.7 MB (107696665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbadcc44bf1a73ea572230c5932f0875ae123ba2c468d1c6b9d22e8da94dc1a7`  
		Last Modified: Thu, 27 Feb 2025 22:08:57 GMT  
		Size: 431.3 KB (431273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:28b0469cec3fef00e42c2c663b98ba869cb532371ed6e976ce57b7c6bcc615a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10683299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81376a8bddbddf03f7d777c8f50a859b971ca92f8f7e3192ec458ec70f273df1`

```dockerfile
```

-	Layers:
	-	`sha256:0eb3419420e378eedef87a6e364268e4c20fe849ed905a937c3d4405f77f8a44`  
		Last Modified: Thu, 27 Feb 2025 22:08:57 GMT  
		Size: 10.7 MB (10664047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94699a1f5715bb79f535d542e9519ed9bac2286b7f1ae83523abf153df995232`  
		Last Modified: Thu, 27 Feb 2025 22:08:56 GMT  
		Size: 19.3 KB (19252 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c7c0d5576627fdd7efba5dd1a0a29069461b5957a90f491aefb075faea4be163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.7 MB (384740575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187c84535b73028672386ed11fdc30d99f94a1c5666a8bfc2077fc736ca7f2a5`
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
# Tue, 18 Feb 2025 21:10:38 GMT
CMD ["gradle"]
# Tue, 18 Feb 2025 21:10:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 18 Feb 2025 21:10:38 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 18 Feb 2025 21:10:38 GMT
WORKDIR /home/gradle
# Tue, 18 Feb 2025 21:10:38 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 18 Feb 2025 21:10:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 18 Feb 2025 21:10:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
USER gradle
# Tue, 18 Feb 2025 21:10:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
USER root
```

-	Layers:
	-	`sha256:ae97a46dbe642672a09bd4ab6df7280b70a40f641ef4a637aa82879145ebcb67`  
		Last Modified: Sat, 22 Feb 2025 01:44:42 GMT  
		Size: 52.3 MB (52271270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235b368d8a74e27196fd9ce4f1e67ad311176f0969c16d42f9d997df479511c2`  
		Last Modified: Thu, 27 Feb 2025 21:11:42 GMT  
		Size: 152.4 MB (152387916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e433a59716811bd986b5601d6d937e74e69970bea9bf9f36c7c91338a2b020`  
		Last Modified: Thu, 27 Feb 2025 22:10:34 GMT  
		Size: 72.0 MB (71958019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fd9b36edcc4f0984e2e694605433b66b4bea07f700b9527e153e0e560894be`  
		Last Modified: Thu, 27 Feb 2025 22:10:32 GMT  
		Size: 1.6 KB (1644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c573d09c2641d2a09afc2fba3270c9aa593b89e7ff30e761a9429d297e34ae9`  
		Last Modified: Thu, 27 Feb 2025 22:20:43 GMT  
		Size: 107.7 MB (107696664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9bc2c21cfe6f66c9625ae19b22f83fb15d75400de880a1888e45764ac47ce9`  
		Last Modified: Thu, 27 Feb 2025 22:20:40 GMT  
		Size: 425.0 KB (425030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:9836e589bb559c3c8868a7295c3958c4722d49aa0bf3967200be2a62e9d96042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10683293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9350ffa2c390cadc6ae53f46a7da1cabf8dc31f4b2a37e036b508f738d80a7`

```dockerfile
```

-	Layers:
	-	`sha256:eb30627a1d43cbbabd23008b6d87a60c0bcb516495addba118275ca2f0ada492`  
		Last Modified: Thu, 27 Feb 2025 22:20:41 GMT  
		Size: 10.7 MB (10663866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40b48b7be969e3c837e27d15ce6583a820f2fc8ee43e66c8c8f32ed22c1c36fe`  
		Last Modified: Thu, 27 Feb 2025 22:20:40 GMT  
		Size: 19.4 KB (19427 bytes)  
		MIME: application/vnd.in-toto+json
