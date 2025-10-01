## `gradle:jdk24-corretto`

```console
$ docker pull gradle@sha256:eae135e59aae43985a361aced1592a9e27ce0e33fea165220f01b9804fce0fb4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk24-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:ac5de7950f21b10610bbbef303a8c7f2c9126ac7a1987428dd9ae17a3c4fe91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.4 MB (464415733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99c71b6a14b935e3f3802af762bcf3f34b6eaa4355e5a61f53c30a86e3b097a`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 12 Sep 2025 13:29:01 GMT
COPY /rootfs/ / # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
CMD ["/bin/bash"]
# Fri, 12 Sep 2025 13:29:01 GMT
ARG version=24.0.2.12-1
# Fri, 12 Sep 2025 13:29:01 GMT
ARG package_version=1
# Fri, 12 Sep 2025 13:29:01 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
ENV LANG=C.UTF-8
# Fri, 12 Sep 2025 13:29:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Fri, 12 Sep 2025 13:29:01 GMT
CMD ["gradle"]
# Fri, 12 Sep 2025 13:29:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 12 Sep 2025 13:29:01 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 12 Sep 2025 13:29:01 GMT
WORKDIR /home/gradle
# Fri, 12 Sep 2025 13:29:01 GMT
ENV GRADLE_VERSION=8.14.3
# Fri, 12 Sep 2025 13:29:01 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Fri, 12 Sep 2025 13:29:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
USER gradle
# Fri, 12 Sep 2025 13:29:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
USER root
```

-	Layers:
	-	`sha256:b6baa302384dc877580d7e1080dcca1ed66d9d3b38afc9fcc29c360239e3e362`  
		Last Modified: Tue, 16 Sep 2025 20:50:40 GMT  
		Size: 54.0 MB (54005280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf754d851e031a791bfa332414a02750f4d2fdc42b06ba77da97453c68ff0d5`  
		Last Modified: Thu, 25 Sep 2025 03:13:20 GMT  
		Size: 187.4 MB (187396532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b76777b621c403a0a244997086fc05afe26d5ab435dc5e53d16402af2072dea`  
		Last Modified: Thu, 25 Sep 2025 03:50:01 GMT  
		Size: 85.6 MB (85562140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08914cece22799f772db352b823c77cd6bc87dcdfe03a643297fb46747948289`  
		Last Modified: Thu, 25 Sep 2025 03:49:54 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e97273997d480147908549ff5c257478289a84255413e16bf7a4cefa3ae8ea`  
		Last Modified: Thu, 25 Sep 2025 03:50:04 GMT  
		Size: 137.4 MB (137395194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fdd8695673f1993a8c6ac84e37a6badcac5bcfc839fb62d41e94902fa85641`  
		Last Modified: Thu, 25 Sep 2025 03:49:54 GMT  
		Size: 54.9 KB (54910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk24-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:e1fbf492994e0c26224153aac796852a916fec2ed32bc0e9a88eeaabdd55104d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11346408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e5ff278d745d694c879b1f5154bbcf2f763af8a3e7ca0e0df69987f33645af`

```dockerfile
```

-	Layers:
	-	`sha256:25364bc448accf69c015dc15805011edc1bab5052584fe5b3f6bb4e47e9eb2df`  
		Last Modified: Thu, 25 Sep 2025 05:21:10 GMT  
		Size: 11.3 MB (11325484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb5f299e692452abb7b2872816a7355ab53a501ac53d0a75a23a77fb0abe758d`  
		Last Modified: Thu, 25 Sep 2025 05:21:11 GMT  
		Size: 20.9 KB (20924 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk24-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:9f26501fa460a9a8d01a814325320a07330872adeee8d2f607a56eaf71f864fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.0 MB (457994946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce18ea37955be7e0864e35c049ce2b8b01cbd9c0da6447d240c767ab941f030f`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 16 Sep 2025 20:09:25 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Sep 2025 20:09:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=24.0.2.12-1
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Fri, 19 Sep 2025 14:40:42 GMT
CMD ["gradle"]
# Fri, 19 Sep 2025 14:40:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 19 Sep 2025 14:40:42 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 19 Sep 2025 14:40:42 GMT
WORKDIR /home/gradle
# Fri, 19 Sep 2025 14:40:42 GMT
ENV GRADLE_VERSION=9.1.0
# Fri, 19 Sep 2025 14:40:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Fri, 19 Sep 2025 14:40:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
USER gradle
# Fri, 19 Sep 2025 14:40:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
USER root
```

-	Layers:
	-	`sha256:202438f011bd656c28426fbd92ff7e7030b77e67ebafd3bec95dbce9626db73c`  
		Last Modified: Tue, 16 Sep 2025 22:16:03 GMT  
		Size: 52.9 MB (52899438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946b11b9ef98756026bddbaf5330fbbdae8f538a9cdd2415bc38f8ddcd65509e`  
		Last Modified: Wed, 24 Sep 2025 22:11:11 GMT  
		Size: 185.4 MB (185436531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef9dd4905ea0acf9f57fef8e5c8ad07daab5cff0696644408b85b43bc5e98d1`  
		Last Modified: Wed, 24 Sep 2025 22:12:26 GMT  
		Size: 85.1 MB (85083085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db23253447c90f63382717cb0525b3259220eba1f911b0b7dea57aa918e89df8`  
		Last Modified: Wed, 24 Sep 2025 22:12:17 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd0d0f810b3b85db00a41308194283f8adac6dcd7e2adcce7144fd76c4f1483`  
		Last Modified: Thu, 25 Sep 2025 07:26:43 GMT  
		Size: 134.5 MB (134514675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292dc952c82b3baeb92599f72b7fde5b1cebfc3352ccf7b2a95166087b761aeb`  
		Last Modified: Wed, 24 Sep 2025 22:12:17 GMT  
		Size: 59.5 KB (59538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk24-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:d87633c942c585e276eea0cdd573a5b90e7fb5a089665aef730d2c0c19503819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11334336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059bb245236660f5677e31fc10a5b13a9c079b11021d74d1ac9155ba8461188d`

```dockerfile
```

-	Layers:
	-	`sha256:9ecdccbed8e4a2beca029f7c3307132d0e063516456cfc306c01ff06b3f42614`  
		Last Modified: Thu, 25 Sep 2025 02:24:30 GMT  
		Size: 11.3 MB (11312584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:682bd77e4fd3a63b9aadb21d0a70f0ba89bdb6c2ceaed180291fd4ea0045d6c3`  
		Last Modified: Thu, 25 Sep 2025 02:24:31 GMT  
		Size: 21.8 KB (21752 bytes)  
		MIME: application/vnd.in-toto+json
