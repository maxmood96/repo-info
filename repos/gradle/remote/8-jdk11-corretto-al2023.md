## `gradle:8-jdk11-corretto-al2023`

```console
$ docker pull gradle@sha256:30af4b159128c85247984805343a54e39b961f2e8b477766ce1c0185f2b95abd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk11-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:6f4391fe5c3bc74a84f6f1109a3afe8df44a466cca56b01d186c153353e3aaa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.3 MB (414327991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0323866f5a63438796066cbaba590289f9cfea74c5e2607a3dc9c2033ce57b6`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=11.0.25.9-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
	-	`sha256:a185434b5b83a672c6167140db9fbc1810d175f869b2c7fe412698dcca07fce4`  
		Last Modified: Fri, 20 Dec 2024 22:32:26 GMT  
		Size: 153.9 MB (153888152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde4f0cd6aae715c7027c18d1a5819bbd82a47caa54cc1c62ed63d41b8d766db`  
		Last Modified: Fri, 20 Dec 2024 23:15:00 GMT  
		Size: 70.7 MB (70662870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366dc1a3325cde8c3b6bab41db28300ff7cfe6be4330c383a0e61b7c6c489295`  
		Last Modified: Fri, 20 Dec 2024 23:14:58 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99ac8dfbd5874daa2ef8b7ffe9dee0db91c97c41fdf88cd4bb1a17a7c73009b`  
		Last Modified: Fri, 20 Dec 2024 23:15:00 GMT  
		Size: 136.6 MB (136564074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f3f6076897b32f4955ea31103e2c8f4450d63e563b797e15f3ddea14d25e1a`  
		Last Modified: Fri, 20 Dec 2024 23:14:58 GMT  
		Size: 54.9 KB (54902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:42c95bfcf2358281eb296763985db49c28c258fea877ff708680348b58c2a76f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10762859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26f7acbc20a26175c35bf444517b81c21ed6383d3d801cdbf72a5af21d381f7`

```dockerfile
```

-	Layers:
	-	`sha256:55b885c8c5a6e7773455a1ebd968a0a3b4290805f6714943a206b65da959efbb`  
		Last Modified: Fri, 20 Dec 2024 23:14:59 GMT  
		Size: 10.7 MB (10742958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dbc517ff018af09b168dd28b664ab78e89c8ffdefb468ebbfd2ec59bd5fec2b`  
		Last Modified: Fri, 20 Dec 2024 23:14:58 GMT  
		Size: 19.9 KB (19901 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:15de56bdfd36494f283189222815477b008b87c7f0c069331b2f7ca69f5483a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.1 MB (411147490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f30efda813ec43d9890035f7f11c9a86b78b08d0ad49ade8d8e035074853ff`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
	-	`sha256:47d1587618326a4abe3cd6250460f3cdc5dac4abad906ecbe738d785605846be`  
		Last Modified: Mon, 02 Dec 2024 23:24:17 GMT  
		Size: 152.3 MB (152343072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf69cc888def5a24daacf8ed761a731170a11ccbdd6c2b66c819c82b47dd843`  
		Last Modified: Tue, 03 Dec 2024 00:24:55 GMT  
		Size: 70.4 MB (70361873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ed825f103ad727286ea22ff962a5d2987234879c93bb7e21f0e349dff849d5`  
		Last Modified: Tue, 03 Dec 2024 00:24:52 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5398e225a77bc3fa896f2813347740a1c830edeeab4f2a9df5b4798ea47262d`  
		Last Modified: Tue, 03 Dec 2024 00:24:59 GMT  
		Size: 136.9 MB (136925487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1775586b9483ad995527f623565bbf4d38a0b3fb676d695063d4aa82ce0fd690`  
		Last Modified: Tue, 03 Dec 2024 00:24:53 GMT  
		Size: 59.5 KB (59535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:6f88de5979dc12a64b8cf0885986b8db8772eb7aa2f7c6fd932ad1ad00c24d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10786789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a523afdcf4911201a5ec84837978d23e476c8a6d371fd41489789266f413b9`

```dockerfile
```

-	Layers:
	-	`sha256:8139581065ad3f8a00419378d563a954911bf4f2198875f59337f9e957ea54e9`  
		Last Modified: Tue, 03 Dec 2024 00:24:53 GMT  
		Size: 10.8 MB (10766684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8af845ba2eaf3fc3ddc80cd328a4eb53d106b974dcca02ea52590e37e105a0e5`  
		Last Modified: Tue, 03 Dec 2024 00:24:52 GMT  
		Size: 20.1 KB (20105 bytes)  
		MIME: application/vnd.in-toto+json
