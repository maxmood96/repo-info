## `gradle:8-jdk21-corretto`

```console
$ docker pull gradle@sha256:dbfe665fbd1905f8e7d73a2620fe9c243e024dc969c6b3cd473a74191f875944
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk21-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:52eb2d7cabbe9fc4b84b5d85466997e84043b17d8a142b2c8309e97cbbb0fcd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.3 MB (448312319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69aaa32d07773f6687751f46794a39a59baea03cb46f68b304f19eef088df86`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Apr 2026 22:16:32 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:16:32 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 22:49:27 GMT
ARG version=21.0.10.7-1
# Mon, 13 Apr 2026 22:49:27 GMT
ARG package_version=1
# Mon, 13 Apr 2026 22:49:27 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 13 Apr 2026 22:49:27 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 22:49:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 13 Apr 2026 23:40:11 GMT
CMD ["gradle"]
# Mon, 13 Apr 2026 23:40:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 13 Apr 2026 23:40:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 13 Apr 2026 23:40:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 13 Apr 2026 23:40:11 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 13 Apr 2026 23:40:11 GMT
WORKDIR /home/gradle
# Mon, 13 Apr 2026 23:40:11 GMT
ENV GRADLE_VERSION=8.14.4
# Mon, 13 Apr 2026 23:40:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Mon, 13 Apr 2026 23:40:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 13 Apr 2026 23:40:14 GMT
USER gradle
# Mon, 13 Apr 2026 23:40:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 13 Apr 2026 23:40:15 GMT
USER root
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a75bc9d53adfe9c175a197df5ba0f8ec3e613431d475082b153357ce4b0346`  
		Last Modified: Mon, 13 Apr 2026 22:49:55 GMT  
		Size: 170.2 MB (170193933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d9a8882217c6b1170fd51f4c9d5568e3f9b944915af37f1b6f4eab332c82b3`  
		Last Modified: Mon, 13 Apr 2026 23:40:46 GMT  
		Size: 86.1 MB (86102279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ed61f6f47b12359ab9acfc42e9273e0bd7eeccdf47b3b49ca87d89c4d9dcb2`  
		Last Modified: Mon, 13 Apr 2026 23:40:42 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110fa0871e565bbbf54152c12109be0d75fbb779c5cbcca802b92b6f0157f0fe`  
		Last Modified: Mon, 13 Apr 2026 23:40:47 GMT  
		Size: 137.4 MB (137388267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf2f3f74094f1c78d2e4ea96b8dabb756af0d3841e30041e607407ba98a1417`  
		Last Modified: Mon, 13 Apr 2026 23:40:42 GMT  
		Size: 54.9 KB (54908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:9fd0eb12b29625d4b7769b1d251c9f311c64f68497290afb2a34c08cf65b8928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11371325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e540eec22c912954cbb0bf73cb12bec645647546a6af333d61c86384b448f30f`

```dockerfile
```

-	Layers:
	-	`sha256:b61eb33d8ae1cb9f2c4502da5795b62a4474d8f25d7b8b4fa7eb8e2d67026555`  
		Last Modified: Mon, 13 Apr 2026 23:40:43 GMT  
		Size: 11.4 MB (11350444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:483cc706ddfe00b4355f30ec204aa135ba2f7551a5d67eacbef1d30afc38a35a`  
		Last Modified: Mon, 13 Apr 2026 23:40:42 GMT  
		Size: 20.9 KB (20881 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:6f417939334e89e79af8bd1b8c7a3e10dd1c8384bd4370e13ad08d06ea8a72c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.0 MB (444963308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1dd3cc4f10e6d32babe089a3ddaee6d1becb02d2efdfad1a868991c9a6805e`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Apr 2026 22:21:43 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:21:43 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 23:12:08 GMT
ARG version=21.0.10.7-1
# Mon, 13 Apr 2026 23:12:08 GMT
ARG package_version=1
# Mon, 13 Apr 2026 23:12:08 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 13 Apr 2026 23:12:08 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 23:12:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 13 Apr 2026 23:53:24 GMT
CMD ["gradle"]
# Mon, 13 Apr 2026 23:53:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 13 Apr 2026 23:53:24 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 13 Apr 2026 23:53:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 13 Apr 2026 23:53:25 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 13 Apr 2026 23:53:25 GMT
WORKDIR /home/gradle
# Mon, 13 Apr 2026 23:53:25 GMT
ENV GRADLE_VERSION=8.14.4
# Mon, 13 Apr 2026 23:53:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Mon, 13 Apr 2026 23:53:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 13 Apr 2026 23:53:27 GMT
USER gradle
# Mon, 13 Apr 2026 23:53:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 13 Apr 2026 23:53:28 GMT
USER root
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6410a32d393b489497b92e8ec46e6582435c4b53b8849f2ddc293e3d450ec835`  
		Last Modified: Mon, 13 Apr 2026 23:12:32 GMT  
		Size: 168.5 MB (168467200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a357045ee9107132fecf66fe36ea2539f751e20201be6ab590cbbb2cca987a04`  
		Last Modified: Mon, 13 Apr 2026 23:53:59 GMT  
		Size: 85.6 MB (85603892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a5d8931442fa47477cc3bdb7e859f79d793ae205a26b6984208bfe3f85437e`  
		Last Modified: Mon, 13 Apr 2026 23:53:55 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5b9f2cc443d2e5c39108ecd9ee64c87c43adb14c458abe8a794ea33f75a720`  
		Last Modified: Mon, 13 Apr 2026 23:54:00 GMT  
		Size: 137.4 MB (137388266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102c788180154aefafbb5bb31152eedc3658b2773fed00ec8a832435e99dbb49`  
		Last Modified: Mon, 13 Apr 2026 23:53:56 GMT  
		Size: 59.5 KB (59530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:afcb56aa4e8b7da95361633c5a10562820b9de0498f9ddc0db6769915ab137b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11370476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ddc07239a66185f41cfa479a18c50d147676b368e2bce825d97a13bbeec2385`

```dockerfile
```

-	Layers:
	-	`sha256:2ce953e27c1e6718a8e406806ddea8131382b1cd119be9e7c201035bbea62381`  
		Last Modified: Mon, 13 Apr 2026 23:53:56 GMT  
		Size: 11.3 MB (11349422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12652bae6fdb3fc01e15e064681be2e217095ae03ad81fa8a2bf1ce21bdf18a1`  
		Last Modified: Mon, 13 Apr 2026 23:53:56 GMT  
		Size: 21.1 KB (21054 bytes)  
		MIME: application/vnd.in-toto+json
