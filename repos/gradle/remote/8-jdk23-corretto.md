## `gradle:8-jdk23-corretto`

```console
$ docker pull gradle@sha256:80af1a83d2a1ee78bce55e9ea570cd255ed9840092734ebfb7fb49c3ad98d811
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk23-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:ea35895580d9b51116fcb59630f50fbbbab1e48389d3e351dc2da54527c4c3aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.0 MB (438019265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ccb1e6b6cd5e6817cf2a92bea6343d93e1c13b315c37d3a495befb7a027f5a9`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 17 Jan 2025 00:42:40 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 00:42:40 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 15:45:23 GMT
ARG version=23.0.2.7-1
# Tue, 21 Jan 2025 15:45:23 GMT
ARG package_version=1
# Tue, 21 Jan 2025 15:45:23 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
ENV LANG=C.UTF-8
# Tue, 21 Jan 2025 15:45:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Tue, 21 Jan 2025 15:45:23 GMT
CMD ["gradle"]
# Tue, 21 Jan 2025 15:45:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 21 Jan 2025 15:45:23 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 21 Jan 2025 15:45:23 GMT
WORKDIR /home/gradle
# Tue, 21 Jan 2025 15:45:23 GMT
ENV GRADLE_VERSION=8.12
# Tue, 21 Jan 2025 15:45:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
# Tue, 21 Jan 2025 15:45:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
USER gradle
# Tue, 21 Jan 2025 15:45:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
USER root
```

-	Layers:
	-	`sha256:fa97b7596fdd91f8ccf1ccf8ee7189f9449877cc795e39ad814638444b666c80`  
		Last Modified: Fri, 17 Jan 2025 02:00:45 GMT  
		Size: 53.2 MB (53152535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b340f28532340953799eb897c9659859e6bd3077f7debf14ecc65f8c77d21d2f`  
		Last Modified: Thu, 23 Jan 2025 23:08:23 GMT  
		Size: 177.6 MB (177576896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bed94d0e2b3e74725c90e3d162b9267699175838ddecb79a5046eb1e4072f91`  
		Last Modified: Fri, 24 Jan 2025 00:08:36 GMT  
		Size: 70.7 MB (70669187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014dc691b0b8786cb77fe34230edd85f9f72f444452cc4055b267a5e7453851e`  
		Last Modified: Fri, 24 Jan 2025 00:08:34 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7dd3ea6514d96d6d1634963431d16aaee090045666e6e5a019bdb708255b145`  
		Last Modified: Fri, 24 Jan 2025 00:08:38 GMT  
		Size: 136.6 MB (136564074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7327f4bdf57ac54d6bca421ea3ccd4690e97a6ace3c170d9614b40e4dcd3852`  
		Last Modified: Fri, 24 Jan 2025 00:08:35 GMT  
		Size: 54.9 KB (54895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk23-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:a78c909f30e3a8c36d9c54598762137afc973d7c6ea4833be190787a8bb4b530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10739575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca640866ebbf22975247cbe411288eebb69d67412648f065bab0271661efd5a7`

```dockerfile
```

-	Layers:
	-	`sha256:89b5d33cffc2a8266019b0e55a9bfaafa879ff3129909ec527382dd0b0af66dc`  
		Last Modified: Fri, 24 Jan 2025 00:08:35 GMT  
		Size: 10.7 MB (10721015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b974444fdb8cd45210e99b26c61c1e9ea9c2ae443050ceca15167c321c748d4`  
		Last Modified: Fri, 24 Jan 2025 00:08:34 GMT  
		Size: 18.6 KB (18560 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk23-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:8a692645485d1d956df0ba82783993a44ee3c0f90a8ced6c278b9fd1a53c86cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.9 MB (434866858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea62ed85f2e716b0e128f0830b80ba93d90919026d927e82933a5d562f44221`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 17 Jan 2025 00:42:44 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 00:42:44 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 15:45:23 GMT
ARG version=23.0.2.7-1
# Tue, 21 Jan 2025 15:45:23 GMT
ARG package_version=1
# Tue, 21 Jan 2025 15:45:23 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
ENV LANG=C.UTF-8
# Tue, 21 Jan 2025 15:45:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Tue, 21 Jan 2025 15:45:23 GMT
CMD ["gradle"]
# Tue, 21 Jan 2025 15:45:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 21 Jan 2025 15:45:23 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 21 Jan 2025 15:45:23 GMT
WORKDIR /home/gradle
# Tue, 21 Jan 2025 15:45:23 GMT
ENV GRADLE_VERSION=8.12
# Tue, 21 Jan 2025 15:45:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
# Tue, 21 Jan 2025 15:45:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
USER gradle
# Tue, 21 Jan 2025 15:45:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
USER root
```

-	Layers:
	-	`sha256:23c58bc83b4b2c70780808282eab12c25cdbe212cc6fa4cd0d9a4d82b1cbf7ce`  
		Last Modified: Fri, 17 Jan 2025 02:10:39 GMT  
		Size: 52.3 MB (52270199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a6b2f46042d81ee016ec4c9248f8c2bdb569a8bd480d9a76e7d984f37678e2`  
		Last Modified: Thu, 23 Jan 2025 23:26:23 GMT  
		Size: 175.6 MB (175611171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59995ab33f7c0156ba88b1a0ad01d2df92cf428beca8996c705a2cabf59c436`  
		Last Modified: Fri, 24 Jan 2025 00:13:20 GMT  
		Size: 70.4 MB (70360203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383062afcfd359ef5a883e7526ecd761f93b3d9e5a1e07973d7cc889ada4b4bb`  
		Last Modified: Fri, 24 Jan 2025 00:13:16 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b050c0bb9a0a80ff3d3f0ee5788ca4bde3234124dedf41885b7db6561aa6c2`  
		Last Modified: Fri, 24 Jan 2025 00:13:21 GMT  
		Size: 136.6 MB (136564071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffbe6967f992ab16953207bcde771f403dae511882164ae4b600c2c276a02f8`  
		Last Modified: Fri, 24 Jan 2025 00:13:17 GMT  
		Size: 59.5 KB (59534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk23-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:0c45ba45c7b7051b9f88ad028a471b9b68a8068441ccda6fb36e5ed6a398ab09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10737864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03fb27cfd77362514c71fd84cfcabb4edac76ffead75cbce449f644d3881f52a`

```dockerfile
```

-	Layers:
	-	`sha256:c99a1d285f7976e6ba8b1074efb6e4892745fd82285bbc05f143a17f842fc984`  
		Last Modified: Fri, 24 Jan 2025 00:13:17 GMT  
		Size: 10.7 MB (10719156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcb68511d61deee1ddc15384b9b6ad602c540a46f57ee777075a022df6e59876`  
		Last Modified: Fri, 24 Jan 2025 00:13:16 GMT  
		Size: 18.7 KB (18708 bytes)  
		MIME: application/vnd.in-toto+json
