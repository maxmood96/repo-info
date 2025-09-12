## `gradle:8-jdk24-corretto-al2023`

```console
$ docker pull gradle@sha256:47cb8133fecd0e911c9f9f553cd8e53b91dacd1234179a260b8bfc15158b1afe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk24-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:df1c0b267c1de994591466621ce7c32b2cbcb9f6df3aeba7cc816d85b7a9bae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.3 MB (464274589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d95860a3bf5c6a9d92948b14727972687468f896997afdb065c40631587575`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Jul 2025 03:50:10 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["/bin/bash"]
# Thu, 17 Jul 2025 03:50:10 GMT
ARG version=24.0.2.12-1
# Thu, 17 Jul 2025 03:50:10 GMT
ARG package_version=1
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV LANG=C.UTF-8
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["gradle"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 17 Jul 2025 03:50:10 GMT
WORKDIR /home/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 17 Jul 2025 03:50:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
USER gradle
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
USER root
```

-	Layers:
	-	`sha256:0727f841555e830a24054117b5d53ecc18438e2e82fc78dd3cc766ca6bb76cab`  
		Last Modified: Wed, 10 Sep 2025 02:33:49 GMT  
		Size: 53.9 MB (53875706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f5546491ed02b9f45eaa39cfd205fc6ab018e0405337dce3b527b11e3bca6d`  
		Last Modified: Fri, 12 Sep 2025 02:10:15 GMT  
		Size: 187.4 MB (187392324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b205dfc47d57a4198e4d10ce80d882362e038b04ccbbed7d83957dbd1e292e`  
		Last Modified: Fri, 12 Sep 2025 02:11:26 GMT  
		Size: 85.6 MB (85554784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc6408febb21ae08b8db96a110a13fddd63f6036ee3556259b96dc50daf77b4`  
		Last Modified: Fri, 12 Sep 2025 03:52:50 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e8cf2ac399611de75dfce4914fbbc871f6eaf32960eb1e206f9eabb2cb87d0`  
		Last Modified: Fri, 12 Sep 2025 02:11:27 GMT  
		Size: 137.4 MB (137395196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc58b46f5d15634dd28a7c8263990b44df33a5794d65e9ba5887c018123e50c5`  
		Last Modified: Fri, 12 Sep 2025 02:11:21 GMT  
		Size: 54.9 KB (54899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk24-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:57c89b1d5f68ad8a36d281af5fc236b4d286321042f138f55d33f673014b6dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11346408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2838edf0f5e07ba458aea75f53d305fb7b253b2149de8de554b78efdabd82b64`

```dockerfile
```

-	Layers:
	-	`sha256:9e889b9a8ebfc639e257716d694e322758271ae8bf63e8e919d3676a4be2d4ef`  
		Last Modified: Fri, 12 Sep 2025 05:21:31 GMT  
		Size: 11.3 MB (11325484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6ea9aa0b4625919278978994167aeabd9771dc64da0d29c09f9d16da6d844f2`  
		Last Modified: Fri, 12 Sep 2025 05:21:32 GMT  
		Size: 20.9 KB (20924 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk24-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:966d03a9133c60b9802e673f9a86f45d9732b9fd9741b592e67a278972267527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.7 MB (460743815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759c3ca009a5db7723deb39181e82718ff4d756949f3eec86397a6da4983713b`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Jul 2025 03:50:10 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["/bin/bash"]
# Thu, 17 Jul 2025 03:50:10 GMT
ARG version=24.0.2.12-1
# Thu, 17 Jul 2025 03:50:10 GMT
ARG package_version=1
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV LANG=C.UTF-8
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["gradle"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 17 Jul 2025 03:50:10 GMT
WORKDIR /home/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 17 Jul 2025 03:50:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
USER gradle
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
USER root
```

-	Layers:
	-	`sha256:a2133584a03a0323a461f4ba1900a168268d3305d6206a4e0a210c92b146e94a`  
		Last Modified: Wed, 10 Sep 2025 02:34:05 GMT  
		Size: 52.8 MB (52775111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2cbebd879707334eb7f2f9a2a52fcbb43995964915e992b4dc087015d3dc3c`  
		Last Modified: Fri, 12 Sep 2025 02:11:14 GMT  
		Size: 185.4 MB (185434865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4376eb33e30c2a23587957b191ba6ce1f2ec03daca800292ad8651101b5c7937`  
		Last Modified: Fri, 12 Sep 2025 02:12:51 GMT  
		Size: 85.1 MB (85077429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fe5bf06e86f8ad4d84aa565508f6a05eee4d201e690bc807ba04ec4c793a0f`  
		Last Modified: Fri, 12 Sep 2025 02:12:45 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3392d7852f77d9c79f0558de4e256d408c8eb901dc33dd9cb589d2c7cca03fc2`  
		Last Modified: Fri, 12 Sep 2025 06:02:33 GMT  
		Size: 137.4 MB (137395195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02332fb9874dd1473918130a25cdc1d482690eff36e6567b318f450c0f9694a5`  
		Last Modified: Fri, 12 Sep 2025 02:12:46 GMT  
		Size: 59.5 KB (59538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk24-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:521a418fb3bfd633715436e5a83276b535e5a5027b121b115365a9df423aafcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11345570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c80d5a39a0091eb9857c9f097f70b22538f469a0a538ec427fb65566335277`

```dockerfile
```

-	Layers:
	-	`sha256:944a34192a6a175e2274fcc25610527cc08ff064461172f512ff2f3a7fbff2dd`  
		Last Modified: Fri, 12 Sep 2025 05:21:40 GMT  
		Size: 11.3 MB (11324473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c3d0da4dccc06db550d4200b0624e294697fb4c59958f87305a2324c29447c`  
		Last Modified: Fri, 12 Sep 2025 05:21:41 GMT  
		Size: 21.1 KB (21097 bytes)  
		MIME: application/vnd.in-toto+json
