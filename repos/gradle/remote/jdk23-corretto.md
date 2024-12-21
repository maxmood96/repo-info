## `gradle:jdk23-corretto`

```console
$ docker pull gradle@sha256:5a9b06d01f6edc1b93d00654c3be6937568a7bf2e7a9b050fd435535c28c6ae7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk23-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:b95866ae14da535eecc13c49ae72f8ff0c062acfc118d939b12841a29e170027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.0 MB (438009567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da55fd6da59fb8b23a1116fff5bb03be24fdb1aa6eadb3f5d3b429fc60c86bc6`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=23.0.1.8-1
# Fri, 13 Dec 2024 23:01:14 GMT
ARG package_version=1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Fri, 20 Dec 2024 17:54:11 GMT
CMD ["gradle"]
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Dec 2024 17:54:11 GMT
WORKDIR /home/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_VERSION=8.12
# Fri, 20 Dec 2024 17:54:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
# Fri, 20 Dec 2024 17:54:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
USER gradle
# Fri, 20 Dec 2024 17:54:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
USER root
```

-	Layers:
	-	`sha256:351cdd1ae1934b18a2b9071735ba92b02b0a1b8775e2a03f31fdaf06f2fba243`  
		Last Modified: Mon, 16 Dec 2024 23:59:50 GMT  
		Size: 53.2 MB (53156313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e3ad49c8506e0d302aebee4fb134ecf63af597150b3973092be755c3ef985d`  
		Last Modified: Fri, 20 Dec 2024 22:33:35 GMT  
		Size: 177.6 MB (177569435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c84d104b136095284d39b70ea02f30076ec3b1e0225bb65342b35b1ad79da4`  
		Last Modified: Fri, 20 Dec 2024 23:14:59 GMT  
		Size: 70.7 MB (70663158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366dc1a3325cde8c3b6bab41db28300ff7cfe6be4330c383a0e61b7c6c489295`  
		Last Modified: Fri, 20 Dec 2024 23:14:58 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e621feaf0b6d03563790db4e14e104199ddf3f6936d8c863c93d201a4c49d8d`  
		Last Modified: Fri, 20 Dec 2024 23:14:59 GMT  
		Size: 136.6 MB (136564074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a295f11b4077b670e5058334053f76e8469130e1a708cd9fde8d359a366d029`  
		Last Modified: Fri, 20 Dec 2024 23:14:58 GMT  
		Size: 54.9 KB (54907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk23-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:45199c946d7ff76368e9056207e2502d8c902540c54271c759e26310173ff6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10739576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3eb062cf65d354b319a7fbd33053f8cb4f4c5eec8fd86521927028e97e475f3`

```dockerfile
```

-	Layers:
	-	`sha256:2fccaad2d7eebfd31a1efcf5b9c5fc2aa274a83b12db916852bf1a13cb841113`  
		Last Modified: Fri, 20 Dec 2024 23:14:58 GMT  
		Size: 10.7 MB (10721015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a86b613317d3a357559d4a15d1cc19b60c37d8ab9a0ae5f38dc54d54c3e8a0fa`  
		Last Modified: Fri, 20 Dec 2024 23:14:58 GMT  
		Size: 18.6 KB (18561 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk23-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:dfbdfbbc6cdf474791a418c5e2eff2dab46d138d59607dec314b8d5893143b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.3 MB (434299032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3749623dd009560237667d6896721ef4ce85d9e3270397b6434414374ed7585c`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Wed, 20 Nov 2024 19:11:06 GMT
CMD ["gradle"]
# Wed, 20 Nov 2024 19:11:06 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 20 Nov 2024 19:11:06 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 20 Nov 2024 19:11:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 20 Nov 2024 19:11:06 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 20 Nov 2024 19:11:06 GMT
WORKDIR /home/gradle
# Wed, 20 Nov 2024 19:11:06 GMT
ENV GRADLE_VERSION=8.11.1
# Wed, 20 Nov 2024 19:11:06 GMT
ARG GRADLE_DOWNLOAD_SHA256=f397b287023acdba1e9f6fc5ea72d22dd63669d59ed4a289a29b1a76eee151c6
# Wed, 20 Nov 2024 19:11:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f397b287023acdba1e9f6fc5ea72d22dd63669d59ed4a289a29b1a76eee151c6
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 20 Nov 2024 19:11:06 GMT
USER gradle
# Wed, 20 Nov 2024 19:11:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f397b287023acdba1e9f6fc5ea72d22dd63669d59ed4a289a29b1a76eee151c6
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 20 Nov 2024 19:11:06 GMT
USER root
```

-	Layers:
	-	`sha256:c4986d7f39b7bf5efc7dcb24fad3d45645e69ad032505693865ef726c1550fb5`  
		Last Modified: Sat, 23 Nov 2024 01:38:05 GMT  
		Size: 51.5 MB (51455844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a1a30d671c2eefa174e9ed9df10f3183c4fc537c6c954702f75aa306d4113b`  
		Last Modified: Mon, 02 Dec 2024 23:31:16 GMT  
		Size: 175.5 MB (175499891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157577cf1d12bc1d2ccd164808566b7123be1d41e9dda5f7d890201f1470d2ea`  
		Last Modified: Tue, 03 Dec 2024 00:29:05 GMT  
		Size: 70.4 MB (70356627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5d2e5d9645de3e873d0acb08f97e93e35a331d71ccbc67262402892c6014a4`  
		Last Modified: Tue, 03 Dec 2024 00:29:03 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd79381fb294d433015de76d6f27b224fd71b5e2b8f93640132d102986a285e`  
		Last Modified: Tue, 03 Dec 2024 00:29:07 GMT  
		Size: 136.9 MB (136925457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30084f62ec12ff963b71b1f070bd8ab4d9af8690fa3324d908a6714fca539180`  
		Last Modified: Tue, 03 Dec 2024 00:29:04 GMT  
		Size: 59.5 KB (59534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk23-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:0bd0081d474f1af61df9b6f325a35ca943f442fe7bf6dd684d04540150775b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10761730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a72ce1314dc489dc261ef530686a6668480c3b05583b8ce95ac6cdb64900298`

```dockerfile
```

-	Layers:
	-	`sha256:1b75a074b07799e822055fc2ee2ee1350467cc1d517ddf0193798bc01a5736d7`  
		Last Modified: Tue, 03 Dec 2024 00:29:04 GMT  
		Size: 10.7 MB (10743012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c9e6df8722e699c3da5fcdcfdcd24ad2b9f3b1ce9b9f8a2d80b6966c7e3bfd8`  
		Last Modified: Tue, 03 Dec 2024 00:29:03 GMT  
		Size: 18.7 KB (18718 bytes)  
		MIME: application/vnd.in-toto+json
