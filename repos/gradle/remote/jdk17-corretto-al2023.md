## `gradle:jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:8dfaae8f832406b8452eade355e335834133872de7e30395db7733bc4469010f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:8ea8b005d800ba2ab7fc5b5eb6762b9f6873b890022401da515a0992386e25b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.9 MB (416935740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c47d77ed55c3143ad8b634fe635e62ee904199ee956e01396307250ff99888f`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
ARG package_version=1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 20 Dec 2024 17:54:11 GMT
CMD ["gradle"]
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
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
	-	`sha256:5859f9641afaa836ca11cc6020a849fe64059acf5f0a845ca5418373b68473f3`  
		Last Modified: Fri, 20 Dec 2024 22:32:52 GMT  
		Size: 156.5 MB (156499341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d178c4a207d9fab350a7ca09588f6cd956d2447d0b17dac30259a4c8476ba9e`  
		Last Modified: Fri, 20 Dec 2024 23:15:05 GMT  
		Size: 70.7 MB (70659436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c3fc4a01d6b889ed975830c86f8f94b4ceb104331b45a098cdc5a3a1194562`  
		Last Modified: Fri, 20 Dec 2024 23:15:02 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a633cb47840ac7340b6451bed11edc34b6222b9d41cdb8461084cf3a7a814cb`  
		Last Modified: Fri, 20 Dec 2024 23:15:07 GMT  
		Size: 136.6 MB (136564072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22627f32adcc9271753e31f67f1966ead7cbea1b927b9e9bc84981546ad1923`  
		Last Modified: Fri, 20 Dec 2024 23:15:03 GMT  
		Size: 54.9 KB (54895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:47aae745ee806a23843889948870fd13a277eb6922ef6ca15be59364cfc7ad72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10737204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb556842e0dec43badbf33f9b18e8d9ac57abdae5e3f0090179c4640ba975ee`

```dockerfile
```

-	Layers:
	-	`sha256:0a58cf811c4d4ac3c87f9d4d95794dd8ae89f84655e836f34b81cdc232f58967`  
		Last Modified: Fri, 20 Dec 2024 23:15:03 GMT  
		Size: 10.7 MB (10717458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bcfce2432573c9638fa76b0a2d238f0e8903de77a8ebb9fc87c66676b6866ee`  
		Last Modified: Fri, 20 Dec 2024 23:15:03 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:1461b45774a8d440094c1e9bf5c7f95a2e2b9ff517d48a0004354c0adaf0d9de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.1 MB (414069153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43823f3a2fddf70b13c0478ca79bf5cb22734693ebaf05c2ce2c922271814e2b`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 20 Nov 2024 19:11:06 GMT
CMD ["gradle"]
# Wed, 20 Nov 2024 19:11:06 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 20 Nov 2024 19:11:06 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 20 Nov 2024 19:11:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
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
	-	`sha256:8858e01ba4c469d04882d19a60aab66b42fe752f10746ea635066a7f79a2ed80`  
		Last Modified: Mon, 02 Dec 2024 23:26:33 GMT  
		Size: 155.3 MB (155267050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06e66532fa93fc208cb40a596c4bff6c2bc860b6746b13d514aa8727ee2ccc0`  
		Last Modified: Tue, 03 Dec 2024 00:26:16 GMT  
		Size: 70.4 MB (70359572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0381dbd46e62ef583a620960a57270b9a7c1950473b0b4375ecf0de6165f12f3`  
		Last Modified: Tue, 03 Dec 2024 00:26:13 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626678be6dfbd174bbc635600bc0fa0ea368d3463ee277bc0c5214290c4e9faa`  
		Last Modified: Tue, 03 Dec 2024 00:26:17 GMT  
		Size: 136.9 MB (136925487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b035390a17a45f51d5ebfb5185d2fc5d462f0589cb507addd77e585f7ad97b97`  
		Last Modified: Tue, 03 Dec 2024 00:26:14 GMT  
		Size: 59.5 KB (59520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:bfe14bceed79e5c596ace873d0b3e2b9f90aa5b2700fe4d916d50e1db288f42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10760255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3f137fb49a784a4e2caf807aae22575923faadc789ad748fd865263e2756fc`

```dockerfile
```

-	Layers:
	-	`sha256:ac1e53d2dfd14b1dac60c0b89c327492b785f95ac946c2c21faa7994fe511c08`  
		Last Modified: Tue, 03 Dec 2024 00:26:14 GMT  
		Size: 10.7 MB (10740308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e71bbbf67c4d0002e5fb61154491c90cb725d8b352df0c0482baa911cce261d4`  
		Last Modified: Tue, 03 Dec 2024 00:26:13 GMT  
		Size: 19.9 KB (19947 bytes)  
		MIME: application/vnd.in-toto+json
