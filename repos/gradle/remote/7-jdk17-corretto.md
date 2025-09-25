## `gradle:7-jdk17-corretto`

```console
$ docker pull gradle@sha256:714aad156d66b4251f1ceef1787f519c994dd03b00bf2d8556bfe95cc0977753
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk17-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:93a30700bf81a2c14a7f535ef3cf5d276dac9cdb977047bb42d88ff952bb46b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.9 MB (424893735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a39059a454abe1de628139cd5386deaea463c117ddade1735ec3faf5294e537`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 10 Sep 2025 15:58:43 GMT
COPY /rootfs/ / # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
CMD ["/bin/bash"]
# Wed, 10 Sep 2025 15:58:43 GMT
ARG version=17.0.16.8-1
# Wed, 10 Sep 2025 15:58:43 GMT
ARG package_version=1
# Wed, 10 Sep 2025 15:58:43 GMT
# ARGS: version=17.0.16.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
ENV LANG=C.UTF-8
# Wed, 10 Sep 2025 15:58:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 10 Sep 2025 15:58:43 GMT
CMD ["gradle"]
# Wed, 10 Sep 2025 15:58:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 10 Sep 2025 15:58:43 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 10 Sep 2025 15:58:43 GMT
WORKDIR /home/gradle
# Wed, 10 Sep 2025 15:58:43 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 10 Sep 2025 15:58:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 10 Sep 2025 15:58:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
USER gradle
# Wed, 10 Sep 2025 15:58:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
USER root
```

-	Layers:
	-	`sha256:b6baa302384dc877580d7e1080dcca1ed66d9d3b38afc9fcc29c360239e3e362`  
		Last Modified: Tue, 16 Sep 2025 20:50:40 GMT  
		Size: 54.0 MB (54005280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12dd6684c9f24dc470a6beea3b0f60e59af88cc80973c45685158e242e9b972`  
		Last Modified: Thu, 25 Sep 2025 03:13:23 GMT  
		Size: 156.8 MB (156804152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79fb8ea4678d10666c33d38c0694817eec5018d4328844bc94e5b02c33e472c`  
		Last Modified: Thu, 25 Sep 2025 03:16:03 GMT  
		Size: 85.6 MB (85558317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aed4ff3e74c9559b0637781a225a89ba72bca6b1e183c0c3fcc853c5a10a2f8`  
		Last Modified: Thu, 25 Sep 2025 03:15:51 GMT  
		Size: 1.6 KB (1643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064d12f42c0e5a87f144f84d26d05d35abeeaf7399d50034a443a4aada2d6f16`  
		Last Modified: Thu, 25 Sep 2025 10:45:29 GMT  
		Size: 128.5 MB (128469416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dfb6fbb031c4ae5ed635242058e9456bf27dcad0d1e2e386fe4b0230da7b070`  
		Last Modified: Thu, 25 Sep 2025 03:15:51 GMT  
		Size: 54.9 KB (54895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:abf21bc05261a2e281930488b6e613a7698be60357896e8adb8878dbbcbadcaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11242874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25625951ff04757f5d2fd2ca0341c8c76d7791725f23b02ba2ef748502954d39`

```dockerfile
```

-	Layers:
	-	`sha256:e7592f9743fd2dc3165d82cceaf2558957c1ae6d27a313275de1d139114dbf9a`  
		Last Modified: Thu, 25 Sep 2025 05:18:43 GMT  
		Size: 11.2 MB (11222118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d8ae4d7087ee5ed3382a2c0f4e8bddafca62b5b36d561805a4ea9e1d9eab111`  
		Last Modified: Thu, 25 Sep 2025 05:18:44 GMT  
		Size: 20.8 KB (20756 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:2a40353edfc30c57a6ab200530544649236b4f5b6fbd9d34fb376e402c719899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.1 MB (422107238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd43d465768c39eda2c2fd756d9feaed6a9dc093f3dc8c5c501d5fd34e0be18`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 10 Sep 2025 15:58:43 GMT
COPY /rootfs/ / # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
CMD ["/bin/bash"]
# Wed, 10 Sep 2025 15:58:43 GMT
ARG version=17.0.16.8-1
# Wed, 10 Sep 2025 15:58:43 GMT
ARG package_version=1
# Wed, 10 Sep 2025 15:58:43 GMT
# ARGS: version=17.0.16.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
ENV LANG=C.UTF-8
# Wed, 10 Sep 2025 15:58:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 10 Sep 2025 15:58:43 GMT
CMD ["gradle"]
# Wed, 10 Sep 2025 15:58:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 10 Sep 2025 15:58:43 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 10 Sep 2025 15:58:43 GMT
WORKDIR /home/gradle
# Wed, 10 Sep 2025 15:58:43 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 10 Sep 2025 15:58:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 10 Sep 2025 15:58:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
USER gradle
# Wed, 10 Sep 2025 15:58:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
USER root
```

-	Layers:
	-	`sha256:202438f011bd656c28426fbd92ff7e7030b77e67ebafd3bec95dbce9626db73c`  
		Last Modified: Tue, 16 Sep 2025 22:16:03 GMT  
		Size: 52.9 MB (52899438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fd24def9f1346651b22961e5b32ca8c4eb0ab12446d66c8a07c7a139ad48b7`  
		Last Modified: Wed, 24 Sep 2025 22:10:55 GMT  
		Size: 155.6 MB (155593727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0466095b8b8444d7712dca7e819d56c55380eb3ca70080be089dd60f38a85b64`  
		Last Modified: Wed, 24 Sep 2025 22:12:35 GMT  
		Size: 85.1 MB (85083464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8058943f0ece31482c13e6de7666fa4ea2517e1e50445b55bed3aec041233a4f`  
		Last Modified: Wed, 24 Sep 2025 22:12:57 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6261cf645a095db5ee100132d58e852eda36b577522cfa4db73b917a9c505ed2`  
		Last Modified: Wed, 24 Sep 2025 22:12:36 GMT  
		Size: 128.5 MB (128469404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c02cd54d8c6cfe34674b2d70815aacc4af126c25a0d2c35f06fa9358b17c3c`  
		Last Modified: Wed, 24 Sep 2025 22:12:58 GMT  
		Size: 59.5 KB (59525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:c8556a7571f08b7550c5780917e601c8a7918767af2f1f2b5874bec2c1c6954a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11242022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0962842fb876b8ca977350ff90d7fb254fc2683bd781172bfe1ee91bb993565b`

```dockerfile
```

-	Layers:
	-	`sha256:df172c67e3965e7980a59dc864f1af444376192c89f3768cc6b6aa8c7ee4571e`  
		Last Modified: Thu, 25 Sep 2025 02:18:47 GMT  
		Size: 11.2 MB (11221093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cabc4d516e2889f787740dd659ebaa998e2a45972667b0656c941cdb9c63e56`  
		Last Modified: Thu, 25 Sep 2025 02:18:47 GMT  
		Size: 20.9 KB (20929 bytes)  
		MIME: application/vnd.in-toto+json
