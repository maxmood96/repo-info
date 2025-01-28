## `gradle:corretto-al2023`

```console
$ docker pull gradle@sha256:e0daa81ee54f051f4c0acfe09ceffa493c2bff2a4213cdfc336d3fe8894b17e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:256267d3be1a4c596ed30e87830e2f49c3187263850550d99c3fbc277e19d045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.2 MB (430189898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd9748ddf50220d54eb393dfa3f09ba248418839466a82cc3cf6d14e1989624`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 17 Jan 2025 00:42:40 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 00:42:40 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=21.0.6.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
ARG package_version=1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 27 Jan 2025 19:22:41 GMT
CMD ["gradle"]
# Mon, 27 Jan 2025 19:22:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 27 Jan 2025 19:22:41 GMT
WORKDIR /home/gradle
# Mon, 27 Jan 2025 19:22:41 GMT
ENV GRADLE_VERSION=8.12.1
# Mon, 27 Jan 2025 19:22:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
# Mon, 27 Jan 2025 19:22:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
USER gradle
# Mon, 27 Jan 2025 19:22:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
USER root
```

-	Layers:
	-	`sha256:fa97b7596fdd91f8ccf1ccf8ee7189f9449877cc795e39ad814638444b666c80`  
		Last Modified: Fri, 17 Jan 2025 02:00:45 GMT  
		Size: 53.2 MB (53152535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54526538d126c7e701e5bad2a88c117277eaf596cbbd1417cf06d8163fba3823`  
		Last Modified: Thu, 23 Jan 2025 23:08:21 GMT  
		Size: 169.8 MB (169756115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d9f34d94a31c3ada2ce3ef51dd29f218e81d39bb06e50c4915be870528486d`  
		Last Modified: Tue, 28 Jan 2025 01:29:02 GMT  
		Size: 70.7 MB (70662726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c594c8496ff189599058d9aef4cdc4d246b52e4d32c769c8e14ad102a2b3bd91`  
		Last Modified: Tue, 28 Jan 2025 01:29:00 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5253528d4bcdbe7c87d615876c7f4a8273b59cd0a25aa4f75273804224098cf2`  
		Last Modified: Tue, 28 Jan 2025 01:29:02 GMT  
		Size: 136.6 MB (136561941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdec5f5807e171aaf52b8a054e08ed976af3ef524a16d36f64a05a0edd8abee0`  
		Last Modified: Tue, 28 Jan 2025 01:29:00 GMT  
		Size: 54.9 KB (54903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:ad383c77d68f9aa0b3b07df06a6e626563eeeaa646852b8aaab5875533ad9aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10742023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b81c7d72ec2dba7191561efb76a4b7d47c5a647359fbbbcd792ff60ab91b86`

```dockerfile
```

-	Layers:
	-	`sha256:c6c48adc2bc63b9ff6f7454d7feef05c63effb7c84c86710882ce14777b412c1`  
		Last Modified: Tue, 28 Jan 2025 01:29:01 GMT  
		Size: 10.7 MB (10721496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a3aa7bce8c0bfb5676024cfcbe73f3938013502fda447712561f9ca29fa0d2`  
		Last Modified: Tue, 28 Jan 2025 01:29:00 GMT  
		Size: 20.5 KB (20527 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:1f44fe61b59f645ce63c27d242be84a550bec02a45dd41b8ee996db7638b96ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.3 MB (427320124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3825afd1d8bae8baa189aba58d6b36988300d92763ffc00cb13cc58bb027d2d3`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 17 Jan 2025 00:42:44 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 00:42:44 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=21.0.6.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
ARG package_version=1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 27 Jan 2025 19:22:41 GMT
CMD ["gradle"]
# Mon, 27 Jan 2025 19:22:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 27 Jan 2025 19:22:41 GMT
WORKDIR /home/gradle
# Mon, 27 Jan 2025 19:22:41 GMT
ENV GRADLE_VERSION=8.12.1
# Mon, 27 Jan 2025 19:22:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
# Mon, 27 Jan 2025 19:22:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
USER gradle
# Mon, 27 Jan 2025 19:22:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
USER root
```

-	Layers:
	-	`sha256:23c58bc83b4b2c70780808282eab12c25cdbe212cc6fa4cd0d9a4d82b1cbf7ce`  
		Last Modified: Fri, 17 Jan 2025 02:10:39 GMT  
		Size: 52.3 MB (52270199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23e56705959971e6a5303bbeaaff3bb398605ff3561b9a2abe5a5f86bd115b8`  
		Last Modified: Thu, 23 Jan 2025 23:23:38 GMT  
		Size: 168.1 MB (168064367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41b4a592cb29430191d3906d967844cd0db8c0f56cfa08eb0824bffbaf341f6`  
		Last Modified: Fri, 24 Jan 2025 00:12:06 GMT  
		Size: 70.4 MB (70362384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9926b909f18f2252595b58ff21f592de3a764e2623972cff753207db265bb865`  
		Last Modified: Fri, 24 Jan 2025 00:12:03 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe21ec0f4d2a18ea3cbce6ed74df794ae39fa78734f33b005cde9fa2c18c4b5`  
		Last Modified: Tue, 28 Jan 2025 02:06:17 GMT  
		Size: 136.6 MB (136561945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6def7993e6b1ea73b0731e964c3cad53623bae71abda2de74e7cc8c4bcaaa50b`  
		Last Modified: Tue, 28 Jan 2025 02:06:13 GMT  
		Size: 59.5 KB (59549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:a9bba3edace0f67182beba973c1dba1d0b475140a5bd8bba72bdcd1ac7520bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10741269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb7685a0729f6aef78ec84f4f507d9c6b1bd3c9b5a7a0efbd63b22b90e53a02`

```dockerfile
```

-	Layers:
	-	`sha256:521b815f9c785cc4e9a56933f7b68276896ac4acf581dfd13fcbe3a6116d12c3`  
		Last Modified: Tue, 28 Jan 2025 02:06:13 GMT  
		Size: 10.7 MB (10720522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dc0e64330d0d7211a158d159dfa89b0cffd3794f82776b3c3c0bc0029114127`  
		Last Modified: Tue, 28 Jan 2025 02:06:13 GMT  
		Size: 20.7 KB (20747 bytes)  
		MIME: application/vnd.in-toto+json
