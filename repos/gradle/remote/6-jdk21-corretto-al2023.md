## `gradle:6-jdk21-corretto-al2023`

```console
$ docker pull gradle@sha256:7626ba09be1387d911e5937bd7d45031249bcf4cc438fba060ec609f50f572ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk21-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:aa78687d69f6150a8b4a712da0ea65b81d1634e6aff35e9c006f3d7940a78c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.1 MB (403146712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896c5e25403deb0f2dcbd121b4b5e86317618e64cd229b9056eb1a1103a2bad5`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:878bc77d48b9be49ba0c1a9449cd773b9ec0a7bf22d5286569e4011e441370c3`  
		Last Modified: Thu, 06 Feb 2025 18:59:08 GMT  
		Size: 53.2 MB (53150583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8588faad644cf783ecb619f9dbb7aa8d78b7fa9c77501b94711a7bba97d2df88`  
		Last Modified: Mon, 10 Feb 2025 20:08:49 GMT  
		Size: 169.8 MB (169753173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb9f9f54226b3c0c310e6282d4c1c37d77325140fde97892d669efc0af7d85b`  
		Last Modified: Wed, 19 Feb 2025 21:30:51 GMT  
		Size: 72.1 MB (72113332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6a1890ed8c5d6fb359d576ef58fe1ee92f2d02fe4bf7f98585261b5656c3a0`  
		Last Modified: Wed, 19 Feb 2025 21:30:46 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbd35ec82596b0689c96f2177239e3cae48f6e613d012005d7d61fd58b3bba4`  
		Last Modified: Wed, 19 Feb 2025 21:30:50 GMT  
		Size: 107.7 MB (107696666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bddc743690a7a55e3b6335dc0c2f6c6618237fa0cc04896c87a9dd8d310e1337`  
		Last Modified: Wed, 19 Feb 2025 21:30:47 GMT  
		Size: 431.3 KB (431278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:b6834b3cf0059047594aa5c5447c0370d08f2bdde68894423f5a714e7ddefba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10660205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe05d5d3b5ad903fd505556c231c14cba2fae59a41970a974bf2300e52c5912e`

```dockerfile
```

-	Layers:
	-	`sha256:4f1bc728715ff5d247f0b06c23bc42afd1f6fd0ad6b87617e277f67ad9b24c35`  
		Last Modified: Wed, 19 Feb 2025 21:30:48 GMT  
		Size: 10.6 MB (10640951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87ecd02026d04871a8ad51e7bf7e4e8179bf42827b4263a3bd1d97b6acba135b`  
		Last Modified: Wed, 19 Feb 2025 21:30:46 GMT  
		Size: 19.3 KB (19254 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk21-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:1c5f92583c47c210293016b3d4b9ce904872f0fc50be1f81e7724c02c99d6df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.2 MB (400244350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4b4e331af020d4e3ba386bbf4559680af4f105b93057100a942ff197148574`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:9f14bc8b911d112fe9005a1fab86d88bf14a10f429f49d6291fd5e2395fd4442`  
		Last Modified: Thu, 06 Feb 2025 18:59:08 GMT  
		Size: 52.3 MB (52270951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7feeff8a60e4d7d7ae6e10d0a1d0796d8d07a16ed9dad63f734432e89c68d9ce`  
		Last Modified: Mon, 10 Feb 2025 20:27:14 GMT  
		Size: 168.1 MB (168063141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06945ff65c7d307d6862379032fb6b532eb9fe1e7bd7ae6a7e178447a49ed27`  
		Last Modified: Mon, 10 Feb 2025 21:12:21 GMT  
		Size: 71.8 MB (71786881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4883efbf3f642122c0880695c27a5b92dd31a0c46bbc6dc26da6623eb88f442`  
		Last Modified: Mon, 10 Feb 2025 21:12:19 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092f14ff994cdd2031ffaea299d17fa870ef39ac17ffce6ae4ac69f8528c6e94`  
		Last Modified: Wed, 19 Feb 2025 22:34:55 GMT  
		Size: 107.7 MB (107696663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7e9f71da0ad03bca722252afd80aa94a4e2f209d83e588560e57156b5b016a`  
		Last Modified: Wed, 19 Feb 2025 22:34:52 GMT  
		Size: 425.0 KB (425034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:0b3b4ef518c33f0e1bc9fedfb6f2364310ce6643d807134ba0e4cc8900046863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10659356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0468a7e2d2255d2793704c7c9b2aa2f253b5080784648685af19a85a40afdc98`

```dockerfile
```

-	Layers:
	-	`sha256:1a790935e38f651316b6ead24af76a69e8750dc966fa39bb6025fbb0372a7e3f`  
		Last Modified: Wed, 19 Feb 2025 22:34:52 GMT  
		Size: 10.6 MB (10639929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d503930d693b908f1ca3bd0703d43d59de088ecfa0218d65fc0aea04fcab3e89`  
		Last Modified: Wed, 19 Feb 2025 22:34:52 GMT  
		Size: 19.4 KB (19427 bytes)  
		MIME: application/vnd.in-toto+json
