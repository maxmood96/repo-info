## `gradle:8-jdk11-corretto`

```console
$ docker pull gradle@sha256:88e70187cc644bfd44d36894d91a40e0878fcb8394a180df7a44854e78234d36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:ae2dc17dc0332c3276d0f56966715c673d235af598e390b0c4ebdf19eec97238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.9 MB (430913563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8033a7b80d77ff5fc157f0768b37a310d114c9757267f6e3aba06b0d0043e4`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:01 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:01 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:11:21 GMT
ARG version=11.0.30.7-1
# Mon, 02 Mar 2026 23:11:21 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:11:21 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:11:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 03 Mar 2026 00:12:17 GMT
CMD ["gradle"]
# Tue, 03 Mar 2026 00:12:17 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 03 Mar 2026 00:12:17 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 03 Mar 2026 00:12:17 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 03 Mar 2026 00:12:17 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 03 Mar 2026 00:12:17 GMT
WORKDIR /home/gradle
# Tue, 03 Mar 2026 00:12:17 GMT
ENV GRADLE_VERSION=8.14.4
# Tue, 03 Mar 2026 00:12:17 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Tue, 03 Mar 2026 00:12:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 03 Mar 2026 00:12:20 GMT
USER gradle
# Tue, 03 Mar 2026 00:12:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 03 Mar 2026 00:12:21 GMT
USER root
```

-	Layers:
	-	`sha256:2584a8e504dfaf493eadaafafbabd8b97f7cb5bbe3cb6a319fb37cf3c4335d86`  
		Last Modified: Thu, 19 Feb 2026 02:57:43 GMT  
		Size: 54.0 MB (54032840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bad2af03af5188a3cc6de4fd433994d98208a28c2aadd7bd215b1c171939319`  
		Last Modified: Mon, 02 Mar 2026 23:11:43 GMT  
		Size: 153.4 MB (153362633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5890d438e9270c80e6f88d720bebf738db6e53c943c9fa3a6511f960917fba6c`  
		Last Modified: Tue, 03 Mar 2026 00:12:55 GMT  
		Size: 86.1 MB (86073200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0dcf71b91bfd14a354621948dc6737ed80d2d269733fe32871bf884084d10e`  
		Last Modified: Tue, 03 Mar 2026 00:12:48 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c3890600f28316f61a7e9823db24f4af9599e62f52b335ecda676ae4168add`  
		Last Modified: Tue, 03 Mar 2026 00:12:54 GMT  
		Size: 137.4 MB (137388302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ec373e41fd508497b646d9425fe38e13f293dd1ad6ac55eed37ea2a019b2bf`  
		Last Modified: Tue, 03 Mar 2026 00:12:48 GMT  
		Size: 54.9 KB (54908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:d367f7f7e2a9d55c60d97a012fa0ca39f3756ca2f0dcccff368de5de8e7eb38e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11387604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae2a36df0dfa5295361f134db9bddda175fdfe8e3ecd4b7e0fa07b9e571ecff`

```dockerfile
```

-	Layers:
	-	`sha256:06fb662791cde161b0b8c66ed42523805a465b4b87861ee9aecf5664a17583c8`  
		Last Modified: Tue, 03 Mar 2026 00:12:49 GMT  
		Size: 11.4 MB (11366081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e71ed32c7eb63f4228bf87a3f3728a3e6146639489ade35562ac89014673578f`  
		Last Modified: Tue, 03 Mar 2026 00:12:48 GMT  
		Size: 21.5 KB (21523 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:2297a762cc06c5cf25f2e9d5c2de6d5850eb221df76f665b67ce782ec901374a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.9 MB (427859446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d429f75a30eb2eea1dee2c94159db7ae86f449dfb4229c4e072ac680c061605d`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:04 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:04 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:12:32 GMT
ARG version=11.0.30.7-1
# Mon, 02 Mar 2026 23:12:32 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:12:32 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:12:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 03 Mar 2026 00:12:54 GMT
CMD ["gradle"]
# Tue, 03 Mar 2026 00:12:54 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 03 Mar 2026 00:12:54 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 03 Mar 2026 00:12:55 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 03 Mar 2026 00:12:55 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 03 Mar 2026 00:12:55 GMT
WORKDIR /home/gradle
# Tue, 03 Mar 2026 00:12:55 GMT
ENV GRADLE_VERSION=8.14.4
# Tue, 03 Mar 2026 00:12:55 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Tue, 03 Mar 2026 00:12:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 03 Mar 2026 00:12:58 GMT
USER gradle
# Tue, 03 Mar 2026 00:12:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 03 Mar 2026 00:12:58 GMT
USER root
```

-	Layers:
	-	`sha256:9330fae67a20d9aa2569828674140d8b67d50cfd127cb99ba0f9be275d35f976`  
		Last Modified: Thu, 19 Feb 2026 02:57:42 GMT  
		Size: 52.9 MB (52941319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7350756942f6b9b7af025da5fd26f1c03d9276b1ea1bc9aa9432be6e9b01612`  
		Last Modified: Mon, 02 Mar 2026 23:12:53 GMT  
		Size: 151.9 MB (151924448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5fcb593607d1367d6f6541b74c420c710a8a425287951918d8493ede97d79f`  
		Last Modified: Tue, 03 Mar 2026 00:13:29 GMT  
		Size: 85.5 MB (85544200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c3adad546e9886c6aa8257804075f106c51c2e825eee21f4ab1e96167dd254`  
		Last Modified: Tue, 03 Mar 2026 00:13:26 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce77aaf22c4c22581928c762b0f8f043347493d79d0b71ea1f5f375b6375c369`  
		Last Modified: Tue, 03 Mar 2026 00:13:30 GMT  
		Size: 137.4 MB (137388267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973d2c36dce66325755f07cb86a5e381060fd15df05c66c195e783a36ea5e006`  
		Last Modified: Tue, 03 Mar 2026 00:13:26 GMT  
		Size: 59.5 KB (59532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:f63477403945878962b175c3a5edff8f031c9a55f0417e9629785b260103c43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11387644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab8119de4fe9cc4374fc48c569fa41eb7843fdafc4a29c43619c214a06b8add`

```dockerfile
```

-	Layers:
	-	`sha256:61fee840eaadcc3a3089d045db55abd8f09bbec649ef889b7058204458be7d4b`  
		Last Modified: Tue, 03 Mar 2026 00:13:26 GMT  
		Size: 11.4 MB (11365924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56ee7888fc45c6e7543bca43eb78dc04fd30ba734653d5557f82fef6e395c553`  
		Last Modified: Tue, 03 Mar 2026 00:13:25 GMT  
		Size: 21.7 KB (21720 bytes)  
		MIME: application/vnd.in-toto+json
