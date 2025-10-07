## `gradle:9-jdk17-corretto`

```console
$ docker pull gradle@sha256:f1e956dc11a3a0f08cfec33446bd3d05c758dfdf8e891035666a9367733dddfb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk17-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:cec4f9e58995ebca7b63ae2ed7d4ae8274d2039c85f8c43a6e1bcd2879f37a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.9 MB (430935339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63aa5e62aee57268bade4d6251386e975ab835f4d6925b8473ebfa4e463fca2c`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=17.0.16.8-1
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=17.0.16.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:fbd59a98b07e2495a3d310a602c2cfb73ec51acb403ff01759389020a766d513`  
		Last Modified: Wed, 01 Oct 2025 20:54:00 GMT  
		Size: 54.0 MB (54005131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066436e61e3d33b0cc28ae048efed629a64fe7d3e632846048aefbb83ad50fa0`  
		Last Modified: Mon, 06 Oct 2025 22:10:53 GMT  
		Size: 156.8 MB (156803165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370ec5a122154f61e6f8001eec814728f7afa96f6380a8b88b7436c0f946a4eb`  
		Last Modified: Mon, 06 Oct 2025 22:12:18 GMT  
		Size: 85.6 MB (85555786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55418b4b248a9c065379e797733307040a87015134610cd4a34bddc3a7356b8`  
		Last Modified: Mon, 06 Oct 2025 22:12:02 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848a0eb5feeb701456fb652cd8f59c0684e53cdd5227787ba63dec3af2542c74`  
		Last Modified: Tue, 07 Oct 2025 04:44:35 GMT  
		Size: 134.5 MB (134514677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb95b97e6cbf3c21f22e8a6a9475efbad2bcec1225dff4f62622c3431af4156`  
		Last Modified: Mon, 06 Oct 2025 22:12:02 GMT  
		Size: 54.9 KB (54899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:c20f20595855621876b9b005810bcd3ee6c8797c564244dc6ab092c0a4ab9fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11321075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6f349cfc255c9dc902da6a95779a241e072a402c624d4fd3ece4c385ba42d3`

```dockerfile
```

-	Layers:
	-	`sha256:313cbf909684fb07c99062559b403b6092f2abbe97e849b7401ca94befb5ccd4`  
		Last Modified: Mon, 06 Oct 2025 23:23:46 GMT  
		Size: 11.3 MB (11299584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:586c7dde47562209ba503dc51d017298b26110305de92008bc87049802f9d9b3`  
		Last Modified: Mon, 06 Oct 2025 23:23:47 GMT  
		Size: 21.5 KB (21491 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:78803ce938a3380851f313ef64bd1c6ac7393d89545d239bb42f5528698932ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.1 MB (428145599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d8653c1ce60b4265c0f1a02d33d9488f35452b0b7bf974e5fef773220d6e4b`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=17.0.16.8-1
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=17.0.16.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:d20954a43d82da3800edf6dd0aed422de3c1214f01f7bc8f0cb120ccc89c5d00`  
		Last Modified: Thu, 02 Oct 2025 00:57:55 GMT  
		Size: 52.9 MB (52891203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd616be23263ff6adc68def052eb1d74774c33ddd8df1898b4198f35efac337`  
		Last Modified: Mon, 06 Oct 2025 22:10:49 GMT  
		Size: 155.6 MB (155594469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6aa1e283152bf96b5c5099666403a1bc3561593f4b9d3332453d46785cf971`  
		Last Modified: Mon, 06 Oct 2025 22:12:18 GMT  
		Size: 85.1 MB (85084051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ff59976880748c688df33d6b883006dc9b9436acbd144711b93c10fa1daeac`  
		Last Modified: Mon, 06 Oct 2025 22:12:03 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be054ad30c97640483413db0f7fa7dc05f12252c5ac8af9940d6f79416d49f2e`  
		Last Modified: Tue, 07 Oct 2025 07:17:41 GMT  
		Size: 134.5 MB (134514677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c75512c316778723dad2a515710140aaa3263fb49bb51730ef3918d7afe425`  
		Last Modified: Mon, 06 Oct 2025 22:12:00 GMT  
		Size: 59.5 KB (59519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:5a0b49c6a03ee3d405976e0673bb67b6d60d4b007f8bef87d646920062643d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11320271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce6453242bb2760355785ba18525b5e822428e3f42debaa82541961abc51a36`

```dockerfile
```

-	Layers:
	-	`sha256:e7d089a3cec5d058ca1af930aa9e6e82ac0f1df419befd250f0006047a574f06`  
		Last Modified: Mon, 06 Oct 2025 23:23:55 GMT  
		Size: 11.3 MB (11298583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebd8763cdb5f446da83a4e2db04ed8c0a99857bf9f8c135c7f7b544a9fcd87b8`  
		Last Modified: Mon, 06 Oct 2025 23:23:56 GMT  
		Size: 21.7 KB (21688 bytes)  
		MIME: application/vnd.in-toto+json
